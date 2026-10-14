# Budżet: czy ma sens i co zrobić, gdy jest za mały

Agent zawsze ocenia budżet, zanim zaproponuje kampanię. Przy za małym budżecie kampania nie da żadnej wiedzy: algorytm się nie nauczy, test nie dojdzie do progu, a owner uzna, że „reklamy nie działają”. Lepiej powiedzieć to wprost i zaproponować inną drogę.

## 1. Najpierw doprecyzuj

- „50 zł” to **dziennie** czy **w sumie**? Ta różnica zmienia odpowiedź z „za mało” na „wystarczy”.
- Ile z tego jest na **test**, który może się nie zwrócić, a ile na **prowadzenie**, gdy coś już działa?
- Czy owner jest gotów dołożyć, jeśli test pokaże sygnał?

## 2. Minimalne sensowne budżety

Liczby to minimum, przy którym test w ogóle coś powie. Ich źródło jest w kolumnie „Skąd”.

| Typ kampanii | Dziennie (minimum) | Na pierwszy test (minimum) | Skąd |
|---|---|---|---|
| Meta, sprzedaż produktu cyfrowego | ~30-40 zł na zestaw, 2 zestawy | 2-3 × próg testu (`monitoring.md`), czyli zwykle ~800-1200 zł, bo pierwsza koncepcja rzadko wygrywa | [SPRAWDZONE] |
| Meta, leady | ~40 zł na zestaw | koszt ~10 leadów przy maksymalnym koszcie leada (np. max 80 zł → ~800 zł) | [SPRAWDZONE RAZ] |
| SaaS (Meta albo Google) | budżet testu / ~30 dni | ~40 × maksymalny koszt triala na kanał (`saas.md`) | [STANDARD] |
| Google Search, usługa lokalna | ~30-50 zł na kampanię | cały miesiąc, bo przy małej liczbie zapytań ocena trwa tygodnie | [SPRAWDZONE RAZ] |

Poniżej ~20 zł dziennie na zestaw w Meta algorytm uczy się bardzo wolno, a wyniki to głównie przypadek. [STANDARD]

## 3. Ocena: 🟢 / 🟡 / 🔴

| Ocena | Kiedy | Co mówi agent |
|---|---|---|
| 🟢 **Wystarczy** | budżet ≥ minimum na test i ≥ minimum dziennie | Stawiamy kampanię według playbooka |
| 🟡 **Na styk** | budżet starcza na jeden test, ale nie na kolejną koncepcję, albo dziennie jest blisko minimum | Stawiamy wersję okrojoną: jeden zestaw zamiast dwóch, jedna koncepcja i od razu uczciwa informacja, że po pierwszej rundzie może zabraknąć na drugą. Jeden kanał, nie dwa |
| 🔴 **Za mało** | budżet poniżej minimum na test albo poniżej ~20 zł dziennie na zestaw | Odradzamy płatne reklamy na teraz i proponujemy alternatywę (sekcja 4). Jeśli owner mimo to chce, robimy najtańszy sensowny wariant i z góry mówimy, że wynik niczego nie przesądzi |

Przykład: „Mam 50 zł na reklamę ebooka za 57 zł”.
- 50 zł **w sumie**: mniej niż cena jednej sprzedaży i jedna ósma progu testu, więc 🔴.
- 50 zł **dziennie**: ~1500 zł miesięcznie, czyli na test wystarczy, ale dziennie starcza tylko na jeden zestaw, więc 🟡 (wersja okrojona).
- 🟢 dla Meta sprzedaży zaczyna się od ~70-80 zł dziennie, czyli od dwóch zestawów po 35-40 zł.

**Gdy dolna granica progu zjada prawie cały budżet** (np. test SaaS za 300 zł, a pierwsza ocena wypada przy 250 zł), to jest 🟡 z jedną decyzją: powiedz ownerowi wprost, że wynik pozwoli tylko na jedną ocenę (iść dalej czy nie), a nie na porównanie wariantów.

## 3a. Wersje okrojone (🟡) i najtańszy wariant (🔴)

| Kanał | 🟡 na styk | 🔴 owner mimo wszystko chce |
|---|---|---|
| Meta, sprzedaż / leady | jeden zestaw szeroki (`ADV+`) ≥ ~25-30 zł dziennie, 3-5 kreacji, bez drugiego zestawu do porównania | promowanie najlepszego posta z aplikacji Instagrama pod obserwujących albo 2-3 dni po ~20-25 zł jako test strony (czy ludzie dochodzą do strony i koszyka), a nie test sprzedaży |
| Meta, SaaS | jak wyżej, z celem trial. Jeśli budżet testu / 30 dni wychodzi poniżej ~25 zł dziennie, skróć test do 2-3 tygodni zamiast schodzić poniżej minimum dziennego | Meta odpuść, zostań przy Google na najgorętszych frazach albo organice |
| Google, SaaS | jedna kampania zamiast trzech: frazy z konkurencją i najgorętsze frazy kategorii, ≥ ~15-20 zł dziennie. Marka dopiero, gdy ktoś jej szuka | tylko frazy „[konkurent] alternatywa” w dopasowaniu ścisłym |
| Google, usługa lokalna | jedna kampania lokalna, wąski promień, tylko frazy z miastem | jedna kampania, kilka najbardziej oczywistych fraz, mniejszy promień |

Przy 🔴 zawsze mówisz z góry: „to sprawdzi, czy ludzie w ogóle reagują, ale nie powie, czy reklamy się opłacą”.

## 3b. Strategie według budżetu miesięcznego

Gotowe układy dla trzech typowych kwot. Kwoty są **miesięczne** (dzienne to około 1/30). Liczby wynikają z minimów w sekcji 2, a podział między kanały to nasza propozycja startowa, którą korygujesz po pierwszej ocenie. [HIPOTEZA, chyba że przy wierszu jest inaczej]

### 500 zł miesięcznie (~16 zł dziennie): 🔴 dla większości

Za mało na rzetelny test płatnej kampanii w Meta. W Google działa tylko przy usłudze z wyraźnym popytem.

| Biznes | Co robimy | Czego nie robimy |
|---|---|---|
| Usługa lokalna z popytem | Jedna kampania Google Search, 5-10 najgorętszych fraz z miastem, wąski promień, cały budżet tutaj | Meta, sieć reklamowa, dopasowanie przybliżone |
| B2B na leadach | Bez kampanii na leady. Promowanie najlepszego posta albo rolki z aplikacji Instagrama, reszta w organikę i kontakt ręczny (sekcja 4) | Kampania Kontakty: jeden lead może kosztować więcej niż cały budżet |
| Produkt cyfrowy | 2-3 dni po ~20-25 zł jako test strony (czy ludzie dochodzą do koszyka) albo promowanie posta pod obserwujących | Kampania Sprzedaż z dwoma zestawami |
| SaaS | Google tylko na frazy „[konkurent] alternatywa” w dopasowaniu ścisłym | Meta, kampania na markę, której nikt jeszcze nie szuka |

Wynik po miesiącu: sygnał (czy ktoś reaguje), a nie odpowiedź, czy reklamy się opłacą. Powiedz to ownerowi przed startem.

### 1000 zł miesięcznie (~33 zł dziennie): 🟡 na styk

Jeden kanał, jedna kampania, jeden zestaw. Na pierwszą ocenę zwykle trzeba całego miesiąca.

| Biznes | Co robimy | Czego nie robimy |
|---|---|---|
| Usługa lokalna z popytem | Google Search, jedna kampania lokalna ~30-35 zł dziennie, frazy z miastem w wyrażeniu i ścisłym. Ocena po miesiącu | Drugi kanał. Remarketing |
| B2B na leadach | Meta Kontakty: jeden zestaw szeroki ~33 zł dziennie, 3-4 kreacje, formularz natywny, wykluczenie osób, które już wysłały formularz. Ocena po ~10 leadach, przy maksymalnym koszcie leada ~80 zł to prawie cały budżet | Dwa zestawy do porównania. Osobny retargeting |
| Produkt cyfrowy | Meta Sprzedaż: jeden zestaw ~30-35 zł dziennie, jedna koncepcja, 3-5 kreacji. Starcza na jeden test, nie na drugą koncepcję | Retargeting (`retargeting.md`). Kilka koncepcji naraz |
| SaaS | Google: jedna kampania na frazy konkurencji i najgorętsze frazy kategorii. Meta odpuszczamy | Kampania na markę przed popytem na nią |

### 5000 zł miesięcznie (~165 zł dziennie): 🟢

Wystarczy na dwa kanały albo na porządny test w jednym, z rezerwą na kreacje.

| Biznes | Podział startowy | Co jeszcze |
|---|---|---|
| Usługa lokalna z popytem | Google ~70% (Search: główna kampania plus osobna na najgorętsze frazy), Meta ~30% (leady lokalne z formularzem, przed i po z realizacji) | Listy remarketingowe w Search w trybie obserwacji. Osobny retargeting w Meta tylko przy grupie ≥ ~1000 osób |
| B2B na leadach | Meta: dwa zestawy po ~65 zł dziennie (szeroki plus wariant z twardym wiekiem decydentów albo innym przekazem), 4-6 reklam. Google tylko, jeśli ktoś szuka kategorii, i tylko tyle, ile wchłoną te frazy (liczone jak przy SaaS niżej) | Retargeting 10-20% budżetu Meta, gdy grupy z `retargeting.md` są dość duże. Nowa partia kreacji co 4-6 tygodni, ustal to od razu |
| Produkt cyfrowy | Meta Sprzedaż: dwa zestawy po ~40 zł dziennie na start, reszta jako rezerwa na skalowanie zwycięzcy (`monitoring.md`, „Skalowanie budżetu”) i na drugą koncepcję | Bez osobnego retargetingu. Promowanie najlepszych postów pod obserwujących jako tańsze uzupełnienie |
| SaaS | Bez stałego procentu. Google dostaje tyle, ile wchłoną frazy z intencją (konkurencja, kategoria, marka, gdy ktoś jej szuka), a reszta idzie do Meta z celem trial (`saas-launch.md`). Ile wchłonie Google: miesięczna liczba zapytań z Planera słów kluczowych × ~5% CTR × szacowany CPC. Przy nowej kategorii albo produkcie dla klientów indywidualnych Google bywa bliskie zera i prawie wszystko idzie do Meta | Mała kampania do osób z trialem bez płatności i odwiedzających cennik, gdy grupa jest dość duża |

Przy 5000 zł nie wydawaj od razu całości. Startuj od minimum z sekcji 2 na każdy element (~60-70% kwoty), a resztę dokładaj dopiero temu, co przeszło pierwszą ocenę. Skalowanie bez sygnału to najszybszy sposób na przepalenie budżetu. [STANDARD]

### Kwota pomiędzy

Wybierz bliższy niższy poziom i dołóż różnicę do tego, co już działa. Nie dokładaj nowego kanału. Przykład: 2500 zł dla B2B to układ z 1000 zł plus drugi zestaw w Meta, a nie Meta plus Google po połowie.

## 4. Gdy budżet jest za mały: co zamiast reklam

Agent proponuje 1-2 drogi pasujące do sytuacji, a nie całą listę:

- **Organiczne rolki na Instagramie i TikToku.** Za darmo, a przy okazji testują hooki i tematy, które potem zostaną reklamami. Rolka, która sama się niesie, to najlepszy kandydat na kreację. [STANDARD]
- **Promowanie najlepszych postów z aplikacji Instagrama** pod obserwujących (`meta-sales-digital.md`). Tańsze niż kampania sprzedażowa, buduje publiczność pod sprzedaż organiczną. [SPRAWDZONE]
- **Pierwsze sprzedaże ręcznie:** znajomi, grupy na Facebooku, społeczności, wiadomości do 20 osób z grupy docelowej. Pierwsze 5-10 sprzedaży bez reklam daje dowód, że oferta działa, i opinie do kreacji. [STANDARD]
- **Najpierw naprawić to, co reklamy i tak by obnażyły:** strona sprzedażowa, oferta, onboarding w SaaS. Reklama na słabej stronie przepala każdy budżet. [SPRAWDZONE]
- **Google tylko na najgorętsze frazy:** marka i „[konkurent] alternatywa” przy SaaS, „[usługa] [miasto]” przy usłudze lokalnej. Mały budżet idzie wtedy tylko tam, gdzie intencja jest najwyższa. [STANDARD]
- **Odłożyć i uzbierać:** ustalić z ownerem kwotę, przy której wracamy (minimum na test z sekcji 2), i do tego czasu robić organikę.

## 5. Jak o tym mówić

- Wprost i bez zawstydzania: „Za 50 zł reklama nie zdąży się niczego nauczyć, więc wynik nic Ci nie powie. Szkoda tych pieniędzy. Proponuję zamiast tego…”.
- Zawsze z liczbą: ile trzeba, żeby test miał sens, i skąd ta liczba.
- Decyzja należy do ownera. Jeśli mimo wszystko chce puścić reklamy, agent robi najtańszy sensowny wariant, a nie odmawia.
