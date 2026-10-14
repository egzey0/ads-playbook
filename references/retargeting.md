# Retargeting i remarketing

To jedno i to samo: reklama do ludzi, którzy już mieli kontakt z firmą (byli na stronie, obejrzeli wideo, otworzyli formularz, dodali do koszyka). W Meta to grupy niestandardowe odbiorców, w Google segmenty danych (dawniej listy remarketingowe).

Najpierw decyzja, czy osobna kampania w ogóle ma sens. Zwykła kampania w Meta i tak dogrywa reklamy ciepłym osobom, więc osobny retargeting to dodatkowy koszt, który musi się obronić.

## 1. Kiedy ma sens

| Sytuacja | Osobny retargeting? | Etykieta |
|---|---|---|
| Tani produkt cyfrowy kupowany od razu | Nie. Szczegóły w `meta-sales-digital.md`, „Czego nie robimy” | [SPRAWDZONE] |
| SaaS z trialem | Tak, mała kampania do osób z trialem bez płatności i do odwiedzających cennik (`saas-launch.md`) | [HIPOTEZA] |
| B2B na leadach, decyzja trwa tygodniami | Tak, gdy ciepła grupa jest dość duża (sekcja 2) i masz coś nowego do powiedzenia | [STANDARD] |
| Droższy produkt w sklepie (dłuższy namysł) | Tak, porzucone koszyki i oglądający produkt | [STANDARD] |
| Usługa z popytem w Google | Zwykle wystarczą listy w kampanii Search w trybie obserwacji (sekcja 5), bez osobnej kampanii | [STANDARD] |

Osobna kampania ma sens tylko, gdy wszystkie trzy warunki są spełnione:
1. Ciepła grupa jest dość duża, żeby częstotliwość nie wystrzeliła (sekcja 2).
2. Masz dla ciepłych osób inny przekaz niż w zimnej reklamie: dowód, odpowiedź na obiekcję, ofertę z terminem.
3. Wartość klienta uzasadnia kilka wyświetleń tej samej osobie.

Przy budżecie 🟡 albo 🔴 (`budget.md`) nie dzielimy pieniędzy na zimne i ciepłe. Wszystko idzie w jedną kampanię.

## 2. Czy grupa jest dość duża

**Meta.** Policz, ile razy dziennie jedna osoba zobaczy reklamę:

> wyświetlenia dziennie = budżet dzienny / CPM × 1000
> częstotliwość dzienna = wyświetlenia dziennie / liczba osób w grupie

Przykład: 20 zł dziennie, CPM 30 zł, to ~670 wyświetleń dziennie. Przy grupie 2000 osób to ~0,33 dziennie, czyli ~2,3 tygodniowo, więc OK. Przy grupie 500 osób wychodzi ~9 tygodniowo, czyli za dużo: zmniejsz budżet albo poszerz okno. Celuj w ~2-3 wyświetlenia tygodniowo na osobę. [HIPOTEZA: próg do sprawdzenia na koncie]

Poniżej ~1000 osób w grupie osobna kampania zwykle nie ma sensu, bo za mało wyświetleń, a kreacje szybko się męczą. [STANDARD]

**Google.** Lista musi mieć co najmniej 1000 aktywnych użytkowników z ostatnich 30 dni, żeby działała w sieci wyszukiwania, i 100 w sieci reklamowej i na YouTube. Mniejsza lista jest widoczna w koncie, ale nie wyświetla reklam. [STANDARD]

## 3. Grupy do zbudowania (Meta)

| Grupa | Okno | Do czego | Etykieta |
|---|---|---|---|
| Wysłali formularz | 90 dni | **Tylko wykluczenie** we wszystkich kampaniach na leady. Grupa musi obejmować **obecny** formularz: stara grupa często ma tylko formularze z poprzednich kampanii. Przy każdym nowym formularzu dopisz go do grupy | [SPRAWDZONE RAZ] |
| Otworzyli formularz, nie wysłali | 30 dni | Retargeting leadów: ci ludzie byli o krok od kontaktu | [STANDARD] |
| Obejrzeli ≥50% wideo albo ThruPlay | 30-90 dni | Retargeting B2B: obejrzeli produkt, ale się nie odezwali | [STANDARD] |
| Interakcja ze stroną FB lub profilem IG | 30-90 dni | Szersza ciepła grupa, gdy powyższe są za małe | [STANDARD] |
| Odwiedzili stronę (pixel) | 30 dni | Sklep, SaaS, usługi ze stroną | [STANDARD] |
| Odwiedzili cennik albo kartę produktu | 14 dni | Najgorętsi na stronie | [STANDARD] |
| Dodali do koszyka, nie kupili | 7-14 dni | Sklep z droższym produktem | [STANDARD] |
| Kupili, płacący klienci | 180 dni albo lista klientów | Wykluczenie z kampanii pozyskania. Źródło dla grup podobnych | [STANDARD] |

Krótsze okno daje cieplejszych ludzi, ale mniejszą grupę i wyższy CPM. Startuj od 30 dni. [STANDARD]

## 4. Ustawienia kampanii (Meta)

- **Cel taki sam jak w głównej kampanii** (Kontakty albo Sprzedaż), a nie Ruch czy Zasięg. Do ciepłych płacimy za wynik, nie za kliknięcia. [STANDARD]
- **Odbiorcy Advantage+ traktują grupę niestandardową jako sugestię** i wychodzą poza nią. Przy prawdziwym retargetingu przełącz na pierwotne opcje odbiorców, żeby reklama trafiała tylko do ciepłej grupy. [STANDARD]
- **Wykluczenia zawsze:** osoby, które już wysłały formularz albo kupiły (sekcja 3).
- **Budżet:** 10-20% budżetu Meta, ale nie więcej, niż wynika z sekcji 2. [HIPOTEZA]
- **Kreacje inne niż w zimnej kampanii.** Ciepły człowiek już widział produkt. Teraz potrzebuje powodu, żeby się odezwać:
  - dowód: case z liczbą, opinia klienta, realizacja;
  - odpowiedź na najczęstszą obiekcję: cena, czas wdrożenia, „czy to u mnie zadziała”;
  - jak wygląda współpraca krok po kroku i co się dzieje po wysłaniu formularza;
  - oferta z konkretem: bezpłatna wycena, pomiar na miejscu, termin.

  Szablony tekstów: `copy-templates.md`. [STANDARD]
- **Częstotliwość:** pilnuj tygodniowej. Gdy rośnie powyżej ~5 i jednocześnie rośnie koszt wyniku, odśwież kreacje albo zmniejsz budżet (`monitoring.md`, „Zmęczenie kreacji”). [HIPOTEZA]

## 5. Google

- **Listy w kampanii Search w trybie „Obserwacja”**, a nie „Kierowanie”. Obserwacja niczego nie zawęża, tylko pokazuje wyniki osobno dla osób z listy. Po 2-4 tygodniach porównaj koszt konwersji listy z resztą. [STANDARD]
- **Przy inteligentnych strategiach ustalania stawek** (Maks. liczba konwersji, docelowy CPA) ręczne korekty stawek dla list nie działają. Algorytm i tak sam korzysta z sygnału, że ktoś był na stronie. Listy dodajesz wtedy dla wglądu w wyniki. [STANDARD]
- **Remarketing w sieci reklamowej i Demand Gen** tylko przy droższym produkcie i liście, która spełnia progi z sekcji 2. Wyklucz aplikacje mobilne i treści dla dzieci, bo tam ucieka budżet na przypadkowe kliknięcia. [STANDARD]
- **Lista klientów (Customer Match)** wymaga konta spełniającego zasady Google i zgody klientów na marketing. Używaj jej przede wszystkim do wykluczeń. [STANDARD]
- **Zgody w UE:** bez Consent Mode v2 listy rosną wolno albo wcale, bo trafiają na nie tylko osoby, które zaakceptowały ciasteczka. Sprawdź to przed zakładaniem kampanii remarketingowej (`measurement.md`). [STANDARD]
- **Wykluczenia:** osoby, które już dokonały konwersji, w każdej kampanii pozyskania.

## 6. Jak oceniać

Retargeting prawie zawsze wygląda w raporcie świetnie, bo łapie ludzi, którzy często i tak by się odezwali. Dlatego:

- **Patrz na wynik całego konta**, a nie tylko na koszt wyniku kampanii retargetingowej. Porównaj łączną liczbę leadów albo sprzedaży z okresem przed retargetingiem przy podobnym budżecie zimnej kampanii. Jeśli suma nie wzrosła, retargeting tylko przejął wyniki, które i tak by były. [STANDARD]
- **Próg wyłączenia:** jeśli kampania wydała równowartość ~3 maksymalnych kosztów wyniku i nie dała żadnego, wyłącz ją albo zmień przekaz. Przy produkcie ze sprzedażą na stronie dolną granicę w złotówkach liczysz jak próg testu w `monitoring.md`, „Kiedy wyłączyć kampanię”. [HIPOTEZA]
- **Test przyrostu** (conversion lift w Meta, eksperymenty w Google) daje prawdziwą odpowiedź, ale wymaga większego budżetu. Przy małych kontach wystarczy porównanie całego konta przed i po.

## 7. Czego nie robimy

- Osobnego retargetingu przy tanim produkcie cyfrowym (`meta-sales-digital.md`).
- Dzielenia małego budżetu na zimne i ciepłe.
- Kampanii na Zasięg albo Ruch do ciepłych osób.
- Puszczania ciepłym tej samej kreacji co w zimnej kampanii.
- Retargetingu bez wykluczenia osób, które już wysłały formularz albo kupiły.
