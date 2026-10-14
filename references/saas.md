# SaaS: reklamy pod subskrypcję

Kampanie dla produktu w abonamencie (aplikacja, narzędzie online, SaaS B2C albo dla małych firm). Ta część stoi głównie na rachunku ekonomii subskrypcji i na lekcjach z innych typów kampanii, dlatego większość reguł to [STANDARD] albo [HIPOTEZA]. Po pierwszych kampaniach SaaS podmień je na własne liczby.

Najważniejsza różnica względem ebooka: **pieniądze przychodzą później niż koszt reklamy.** Ebook za 57 zł zarabia albo nie tego samego dnia. Abonament za 49 zł miesięcznie zarabia przez kolejne miesiące, o ile klient nie zrezygnuje. Dlatego ROAS z dnia zakupu kłamie, a decyzje opierasz na progu opłacalności (break even), który liczysz przed startem.

## 1. Policz próg opłacalności, zanim wydasz złotówkę

Potrzebujesz pięciu liczb od klienta:

| Liczba | Skąd | Przykład |
|---|---|---|
| Cena miesięczna netto (ARPU) | cennik, średnia z planów | 49 zł |
| Marża brutto | po kosztach serwerów, API, prowizji płatności | 80% |
| Churn miesięczny | ile % płacących odchodzi w miesiącu | 8% |
| Konwersja trial → płatny | z panelu albo Stripe'a | 15% |
| Akceptowalny czas zwrotu (payback) | ile miesięcy firma może czekać na zwrot | 4 miesiące |

Z nich:

- **Zysk brutto z klienta miesięcznie** = cena × marża = 49 × 0,8 = **39 zł**
- **Średni czas życia klienta** = 1 / churn = 1 / 0,08 = **12,5 miesiąca**
- **LTV** (zysk brutto z klienta przez całe życie) = 39 × 12,5 = **~490 zł**
- **Maksymalny koszt pozyskania płacącego klienta (CAC)**, mniejsza z dwóch wartości:
  - według zwrotu: 39 zł × 4 miesiące = **156 zł**
  - według LTV: 490 / 3 = **163 zł** (zasada „LTV co najmniej 3x CAC”, [STANDARD])
  - → **max CAC ≈ 156 zł**
- **Maksymalny koszt triala** = max CAC × konwersja trial → płatny = 156 × 0,15 = **~23 zł**

To ostatnia liczba jest Twoim progiem w Menedżerze reklam i w Google Ads. **Jeśli wychodzi bardzo nisko (rzędu kilku złotych za trial), potraktuj to jako sygnał ostrzegawczy:** zanim wydasz budżet, zaproponuj podniesienie wartości klienta (plan roczny, wyższa cena, trial z kartą zamiast bez), bo przy tak niskim progu płatne reklamy rzadko się spinają. Test i tak to zweryfikuje, ale owner ma wiedzieć z góry. [HIPOTEZA] **Trial po 23 zł to zero, trial po 15 zł to zysk, trial po 40 zł to strata**, nawet jeśli kampania „wygląda dobrze”.

Mała firma albo projekt bez finansowania: skróć akceptowalny zwrot do 1-3 miesięcy. Reklama nie może zjadać gotówki szybciej, niż wraca. [HIPOTEZA, rozsądek finansowy]

**Plany roczne** płacone z góry skracają zwrot do zera: klient płaci np. 10 miesięcy z góry, więc nawet drogie pozyskanie spina się od pierwszego dnia. Jeśli produkt ma plan roczny, pokaż go w reklamie i na stronie i licz próg osobno dla rocznych.

### ROAS przy subskrypcji

Jeśli Meta albo Google raportuje wartość pierwszej płatności, **ROAS z pierwszego miesiąca na poziomie progu to nie 1, tylko 1 / miesiące zwrotu.** Przy zwrocie w 4 miesiące ROAS 0,25 z pierwszej płatności (liczony od zysku brutto) jest na zero. Patrz na ROAS kohorty po 3 i 6 miesiącach (ile wróciło od klientów pozyskanych w danym miesiącu), a nie na ROAS z dnia.

### Zwrot z uwzględnieniem churnu

Prosty rachunek „max CAC = zysk miesięczny × miesiące zwrotu” zakłada, że nikt nie odchodzi. Kohorta traci jednak co miesiąc część klientów, więc realny zwrot trwa dłużej. Zysk z kohorty po N miesiącach na jednego pozyskanego klienta:

```
zysk_po_N = zysk_mies × (1 − (1 − churn)^N) / churn
```

Przykład: zysk 50 zł, churn 5%. Po 3 miesiącach kohorta oddaje ~143 zł na klienta, a nie 150 zł, po 4 miesiącach ~186 zł. Przy CAC 180 zł zwrot następuje w 4. miesiącu, a nie po 3,6. Agent podaje właścicielowi tę wersję, gdy ten pyta „kiedy mi się zwróci”. [STANDARD]

## 2. Pomiar: optymalizuj pod płacących, nie pod konta

Ta sama pułapka co z odsłonami strony jako konwersją w Google: jeśli algorytm dostaje „rejestrację” jako sukces, nauczy się znajdować ludzi, którzy zakładają darmowe konta i nigdy nie płacą. [SPRAWDZONE RAZ na innym typie kampanii, logika ta sama]

Zdarzenia do skonfigurowania:

| Zdarzenie | Meta | Google | Kiedy używać do optymalizacji |
|---|---|---|---|
| Rejestracja / start triala | `StartTrial` albo `CompleteRegistration` | konwersja z tagu | na start, bo jest ich dużo |
| Aktywacja (np. ukończony onboarding, pierwszy projekt) | zdarzenie niestandardowe | konwersja z tagu | gdy triali jest dużo, ale mało z nich płaci |
| Pierwsza płatność | `Subscribe` z wartością | import konwersji offline / rozszerzone konwersje | gdy płatnych jest ~30-50 tygodniowo |

- **Przy rejestracji zapisuj w bazie** `gclid`, `fbclid`/`_fbc`, `_fbp` i UTM-y użytkownika. Bez tego płatność, która przyjdzie po trialu, nie ma się do czego przypiąć. [STANDARD]
- **Płatność wysyłaj z serwera**, z webhooka Stripe'a (albo innej bramki) do Conversions API Mety i do Google przez import konwersji. Pixel w przeglądarce nie zobaczy płatności, która przychodzi po 14 dniach triala. Do zdarzenia dołącz e-mail (zahashowany) i identyfikator kliknięcia (`fbclid`/`fbc`, `gclid`), żeby platforma połączyła płatność z reklamą. [STANDARD]
- **Kolejność optymalizacji:** zaczynasz od triala, bo inaczej algorytm nie ma się na czym uczyć. Gdy widzisz, że triale z reklam płacą rzadziej niż organiczne, przełączasz na aktywację. Na płatność przełączasz, gdy jest jej dość tygodniowo. [STANDARD]
- Jakość triala sprawdzaj kohortami: ile triali z danego tygodnia i kampanii zamieniło się w płatnych. Bez tego koszt triala jest półprawdą.

## 3. Reklamy „na zero”: kiedy to dobra strategia

Wielu właścicieli SaaS-ów świadomie puszcza reklamy na zero albo lekko pod kreską. To nie jest błąd, jeśli wiadomo, **na zero w jakim horyzoncie**:

| Horyzont „zera” | Co to znaczy | Kiedy ma sens |
|---|---|---|
| Na pierwszej płatności | Koszt pozyskania = pierwsza wpłata klienta | Prawie nigdy przy miesięcznym abonamencie: tak liczony próg jest zbyt surowy i blokuje każdy kanał. Ma sens przy planach rocznych płaconych z góry |
| Na zwrocie w X miesięcy | Koszt pozyskania wraca po X miesiącach płacenia | **Domyślny wybór.** X ustala właściciel według gotówki: 1-3 miesiące bez finansowania, 6-12 z finansowaniem |
| Na całym LTV | Koszt pozyskania = cały zysk z klienta przez jego życie | Tylko świadomie, z zapasem gotówki, gdy liczy się wzrost (dane, efekt sieci, polecenia). Każdy błąd w szacunku churnu robi z tego stratę |

Zasady:
- **Zero liczysz od zysku brutto, nie od przychodu.** Abonament 49 zł przy marży 80% to 39 zł, a nie 49 zł.
- **Na zero na LTV to decyzja właściciela, nie domyślne ustawienie agenta.** Agent zawsze pokazuje oba progi (zwrot i LTV) i pyta, który wybieramy.
- **„Na zero” wymaga dobrych danych o churnie.** Przy produkcie młodszym niż kilka miesięcy churn jest zgadywany. Wtedy próg liczysz na zwrocie, nie na LTV. [STANDARD]
- **Reklamy na zero mają uzasadnienie tylko z zyskiem pośrednim:** polecenia, opinie, dane o użytkownikach, upsell do wyższego planu. Agent pyta, czy taki zysk istnieje i czy właściciel go mierzy. [HIPOTEZA]

## 4. Model oferty a reklamy

Model wejścia do produktu zmienia to, co liczysz i pod co optymalizujesz. [STANDARD]

| Model | Plusy dla reklam | Minusy | Kiedy |
|---|---|---|---|
| Trial bez karty | Dużo rejestracji, algorytm szybko się uczy | Niska konwersja na płacących, dużo „turystów” | Produkt tani, łatwy do sprawdzenia w kilka minut |
| Trial z kartą | Mniej rejestracji, ale wyraźnie wyższa konwersja na płacących i szybszy sygnał „płatny” | Wyższy koszt rejestracji, wymaga mocniejszej strony | Gdy trial bez karty daje dużo kont i mało płacących |
| Freemium | Najtańsza rejestracja | Płacący pojawiają się po tygodniach albo miesiącach, trudno ocenić kampanię | Produkt z efektem sieci albo naturalnym limitem darmowego planu |
| Demo z handlowcem | Wysoka wartość leada | Mały wolumen, długi cykl | Drogi abonament B2B |

Przy małym budżecie i trialu bez karty, który słabo konwertuje, test „trial z kartą” bywa szybszą drogą do opłacalnych reklam niż kolejne kreacje. [HIPOTEZA]

### Aplikacja mobilna (płatność w App Store / Google Play)

Ten playbook jest pisany głównie pod SaaS z rejestracją i płatnością w przeglądarce. Przy aplikacji mobilnej różnice są duże: [STANDARD]
- Marża spada o prowizję sklepu (15-30%), więc próg kosztu pozyskania jest niższy.
- Kampanie na instalacje i zdarzenia w aplikacji wymagają SDK (Meta, Google) albo partnera pomiarowego (MMP). Na iOS pomiar jest ograniczony przez prywatność Apple i wyniki są przybliżone.
- Jeśli to możliwe, kieruj reklamy na stronę z rejestracją i płatnością w przeglądarce, a aplikację podawaj jako miejsce korzystania. Pomiar i marża są wtedy jak przy zwykłym SaaS.

Gdy właściciel ma tylko płatności w sklepie, agent mówi wprost, że ta część playbooka jest ograniczona, i nie zgaduje ustawień kampanii na instalacje.

## 5. Wypuszczenie kampanii

Bramka przed startem, wybór kanału, budowa kampanii w Google i Meta, kreacje, teksty i progi decyzji w pierwszych 30 dniach: `saas-launch.md`.

## 6. Kalkulator do skopiowania

```
# procenty wpisuj jako ułamki: 80% = 0.8, 8% = 0.08
cena_mies        = ___ zł netto
marza            = ___ %
churn_mies       = ___ %
trial_na_platny  = ___ %
zwrot_mies       = ___ (ile miesięcy możemy czekać)

zysk_mies   = cena_mies × marza
ltv         = zysk_mies / churn_mies
max_cac     = min(zysk_mies × zwrot_mies, ltv / 3)
max_trial   = max_cac × trial_na_platny
budzet_test = max_trial × 40
```

Agent liczy to w wywiadzie, zanim zaproponuje budżet i strukturę kampanii. Jeśli klient nie zna churnu albo konwersji z triala, przyjmij ostrożnie churn 10% i konwersję 10% i napisz wprost, że to założenie.
