# Monitoring, odświeżanie, skalowanie

## Rytm

| Kiedy | Co |
|---|---|
| Dzień 1-3 | Czy reklamy zostały zatwierdzone, czy wydają, czy konwersja się zlicza. Niczego nie zmieniaj. |
| Dzień 7 | Google: raport wyszukiwanych haseł, dopisz wykluczenia. Meta: która reklama dostaje budżet, plus podziały wiek / płeć / umiejscowienie (`meta-analysis.md`). |
| Dzień 14 | Pierwsza ocena wyniku (koszt leada albo ROAS) względem celu. |
| Co tydzień | Raport z `measurement.md`, wykluczenia, zmęczenie kreacji. |
| Po progu testu (sprzedaż) albo co 4-6 tygodni (leady) | Nowa koncepcja albo partia kreacji. Patrz „Kiedy wyłączyć kampanię” i „Testowanie kreacji”. |

## Nowe konto reklamowe

- Świeże konto potrafi przez pierwsze dni wydawać grosze albo nic, czasem kilka dni z rzędu po parę złotych. To normalne, nie zmieniaj ustawień i nie stawiaj wszystkiego od nowa. [SPRAWDZONE]
- „Rozgrzewanie” konta przed startem ma sens tylko wtedy, gdy kampania i tak ma ruszyć za jakiś czas. Jeśli możesz odpalić dziś, odpalaj. Rozgrzewanie trwa dłużej niż sam przestój nowego konta. [SPRAWDZONE RAZ]
- Limit wydatków rośnie sam, gdy konto regularnie wydaje i płatności przechodzą. Odrzucone płatności go hamują. Meta nie podaje, jak szybko rośnie. [SPRAWDZONE]
- Płatności: Meta lubi karty kredytowe i debetowe z dużych banków, gorzej znosi karty fintechów (np. Wise). Problemy z bankiem, BLIK-iem czy limitem karty to najczęstszy powód „konto nic nie wydaje”. [SPRAWDZONE RAZ]
- Na początku Meta pobiera opłaty częściej, potem rzadziej, mniej więcej co kilka dni.

## Czytanie wahań

- Anomalię z 1-2 dni ignoruj. Przy budżetach 50-100 zł dziennie jeden dzień z 5 sprzedażami i drugi z zerem to szum, a nie sygnał. [SPRAWDZONE]
- Weekendy zwykle sprzedają gorzej niż dni robocze. Nie zmieniaj budżetu pod dzień tygodnia bez święta albo wydarzenia. [SPRAWDZONE RAZ]
- Święta: Boże Narodzenie realnie zamraża ruch, Wielkanoc zwykle tylko na jeden dzień. [HIPOTEZA]
- Zakres dat: presety typu „Ostatnie 7 dni” nie liczą dzisiejszego dnia. Do sprawdzenia, czy reklama w ogóle wydaje, ustaw zakres maksymalny albo „Dzisiaj”.

## Kiedy wyłączyć kampanię (produkt cyfrowy)

To jedyne źródło progów dla produktów cyfrowych. SKILL.md i `meta-sales-digital.md` odsyłają tutaj.

**Próg testu koncepcji** = większa z kwot: ~400 zł albo 3 × cena produktu. Przy ebooku za 57 zł to ~400 zł, przy kursie za 197 zł ~600 zł. Oceniasz całą koncepcję (kampanię albo zestaw reklam z jedną koncepcją), a nie pojedynczy zestaw w porównaniu z drugim.

| Sytuacja | Decyzja | Etykieta |
|---|---|---|
| Nowa koncepcja: minęły co najmniej 2 pełne dni **i** wydała ≥ 2 × cena produktu **i** zero sprzedaży | Wyłącz koncepcję i postaw następną, wyraźnie inną. Nie czekaj, aż „się nauczy”: nawet jeśli ruszy, będzie odrabiać stratę ze startu | [SPRAWDZONE RAZ] |
| Doszła do progu testu, sprzedaje, ale koszt sprzedaży > 2 × cena | Zmień koncepcję | [SPRAWDZONE RAZ] |
| Doszła do progu testu, koszt sprzedaży poniżej progu opłacalności | Zostaw, dokładaj nowe kreacje obok | [SPRAWDZONE] |
| Kampania, która już zarabiała, cichnie na 1-2 dni | Nic nie zmieniaj, dzieje się to nawet przy zwycięskich kreacjach | [SPRAWDZONE] |
| Poniżej progów | „Za wcześnie”, podaj kwotę, po której wracamy | [SPRAWDZONE] |

**Zanim wyłączysz z powodu „zera”, sprawdź, czy zero jest prawdziwe:** zamówienia w systemie płatności vs zakupy w Menedżerze reklam, zdarzenie Zakup w Menedżerze zdarzeń, wyświetlenia strony vs kliknięcia linku. Jeśli sprzedaż była, a pomiar jej nie widzi, naprawiasz pomiar, a nie koncepcję. [SPRAWDZONE]

Zestawu szerokiego nie wyłączasz osobno na rzecz zestawu z podpowiedziami, zanim oba nie dojdą do progu testu: szeroki na starcie prawie zawsze idzie gorzej (`meta-sales-digital.md`).

Jedna nieudana kampania, a nawet dwie, to nie dowód, że nisza czy produkt nie działa. Jeśli wcześniej ktoś kupił, choćby kilka osób, produkt się sprzedaje i trzeba mocniejszej kreacji. Zdarza się, że trzy kampanie nie dają nic, a czwarta, nowa, sprzedaje od pierwszych złotówek. Traktuj kampanie jak serię prób, a nie jak jeden projekt do ratowania. [SPRAWDZONE RAZ]

Kampanię oceniasz po jednym: czy wychodzisz na plus, czyli koszt sprzedaży względem ceny produktu. Sprzedaż za 40-50 zł przy produkcie za 97 zł to dobry wynik, nawet jeśli CTR wygląda przeciętnie. Dużo wejść, polubień i sesji bez sprzedaży to zły wynik. Część klientów porzuca koszyk i to w produktach cyfrowych normalne.

## Zmęczenie kreacji

Sygnały (te same progi obowiązują w całym playbooku): [SPRAWDZONE RAZ]
- CTR (kliknięcia linku) reklamy spada o 30-50% względem jej pierwszych 2 tygodni.
- Koszt wyniku rośnie ponad 1,5 × względem najlepszego okresu.
- Częstotliwość za ostatnie 30 dni: powyżej ~2,5 przy wąskim rynku (lokalnie, B2B), powyżej ~3,5 przy szerokim.
- Zwykle 2 z 3 sygnałów naraz. Jeden sygnał to powód do obserwacji, nie do działania.

Typowy przebieg: kreacje ze startu działają 4-8 tygodni, potem koszt wyniku skacze 2-3 razy i bez nowych kreacji już nie wraca. Najczęstszy błąd w tym momencie to dokładanie budżetu zamiast kreacji.

**Co robić:** nowa partia kreacji, dodana do istniejącego zestawu. Zwycięzców nie wyłączaj, dopóki nowe ich nie przebiją.

## Testowanie kreacji

- Testujemy koncepcje, a nie kosmetykę. Przy produkcie cyfrowym zmieniaj koncepcję **diametralnie po każdym progu testu bez zwycięzcy** (większa z kwot: ~400 zł albo 3 × cena), aż coś zaskoczy. Licz się z tym, że zanim kampania zacznie zarabiać, kilka takich rund pójdzie na wynik w okolicy zera. Kiedy koncepcja trafi, ROAS potrafi skoczyć kilkukrotnie i utrzymać się przy skalowaniu. Start kampanii to zawsze jej najgorszy moment, bo pixel dopiero się uczy. [SPRAWDZONE RAZ]
- Koncepcje warte przetestowania po kolei: ilustracje AI z hookiem, proste i krzykliwe grafiki z wielkim hookiem, dopracowane grafiki pod inny problem klienta, **zdjęcie z codziennego życia grupy docelowej plus jedno mocne zdanie**. Ta ostatnia najczęściej wygrywa (`copy-templates.md`). [SPRAWDZONE RAZ]
- **Gdzie wrzucać nowe kreacje:** w większości przypadków do istniejącego zestawu. Nowy zestaw zakładaj tylko pod wyraźnie nowy pomysł (inna grupa, inny kąt). [SPRAWDZONE]
- **Kreacje, które nie dostają budżetu:** patrz sekcja niżej.
- **Ile reklam w zestawie:** do ~6-8 aktywnych. Jeśli po dorzuceniu nowych wychodzi więcej, wyłącz te stare, które wydały już co najmniej próg testu przy wyraźnie gorszym wyniku. Zwycięzcy zostają. [STANDARD]
- Kampania, która „odjechała” bez wyraźnej przyczyny (koszt wejścia na stronę spada, a konwersja z nim): czasem pomaga postawienie jej klona od nowa. [SPRAWDZONE RAZ, nie zawsze działa]

## Kreacje, które nie dostają budżetu

Typowa sytuacja: w zestawie 4-8 kreacji, a wydają 1-2. Owner pyta, co z resztą.

**Dlaczego tak jest:** Meta szybko przewiduje, które reklamy dadzą najwięcej wyników, i pakuje w nie budżet. To normalne zachowanie, nie błąd. Kreacja bez budżetu nie jest „przegrana”, tylko **niesprawdzona**: Meta nie ma o niej danych, więc nie wiadomo, czy jest słaba. [SPRAWDZONE]

**Decyzja krok po kroku:**

1. **Czy te, które wydają, trzymają wynik** (koszt sprzedaży, leada, triala poniżej progu)?
   - **Tak:** zostaw wszystko tak, jak jest. Nie wyłączaj reklam bez budżetu, bo nic nie kosztują, a mogą zacząć wydawać, gdy zwycięzcy się zmęczą, często po 2-4 tygodniach. [SPRAWDZONE RAZ]
   - **Nie:** problem jest w zwycięzcach, a nie w reszcie. Działasz według progów (`Kiedy wyłączyć kampanię`, `Zmęczenie kreacji`): nowa partia kreacji albo zmiana koncepcji.
2. **Nie wyłączaj zwycięzcy, żeby „zmusić” Metę do wydawania na resztę.** Zestaw traci wtedy najlepszą reklamę, a budżet rozlewa się na niesprawdzone. Wynik prawie zawsze spada. [STANDARD]
3. **Nie przenoś pojedynczych kreacji do innego zestawu tylko po to, żeby wydały.** W nowym zestawie i tak dostaną budżet tylko wtedy, gdy będą jedyne albo najlepsze, a Ty rozbijasz budżet i naukę na więcej części. [STANDARD]
4. **Jeśli naprawdę chcesz sprawdzić kreację, która nie wydaje** (np. to inna koncepcja, w którą wierzysz), masz dwie uczciwe drogi:
   - **Test kreacji w Mecie** (sekcja „Testowanie materiałów reklamowych” w reklamie): porównanie do 5 wersji, Meta sama dzieli budżet równo między nie. To najprostszy sposób na wymuszenie równego wydatku. [STANDARD]
   - **Osobny zestaw testowy** z tą samą grupą, małym budżetem (≥ ~20-25 zł dziennie) i tylko nową koncepcją. Ma sens tylko wtedy, gdy to wyraźnie inny pomysł (nowy kąt, nowy format), a nie wariant istniejącej grafiki. [SPRAWDZONE RAZ]
5. **Wyłączasz kreację dopiero, gdy wydała próg testu** (sprzedaż: większa z kwot ~400 zł albo 3 × cena; leady: koszt ~10 leadów) z wyraźnie gorszym wynikiem niż reszta. Albo gdy zestaw ma już więcej niż ~6-8 aktywnych reklam i trzeba zrobić miejsce. [SPRAWDZONE]
6. **Robienie miejsca, gdy reklamy bez budżetu nigdy nie dojdą do progu:** wyłączasz najstarsze z nich, które są wariantami tej samej koncepcji co zwycięzca (inny kolor, inny tekst na tej samej grafice). Zostawiasz te, które są wyraźnie inną koncepcją, bo to one dają szansę na nowego zwycięzcę. [STANDARD]
7. **Zwycięzca z małą liczbą wyników** (np. 5 sprzedaży) to „prowadzi”, a nie „wygrał”. Zostawiasz go, ale nie skalujesz na nim, dopóki nie ma ~10 wyników. [STANDARD]

**Test kreacji w Mecie** trwa co najmniej ~7 dni i potrzebuje budżetu, który da każdej wersji choć kilka wyników (przy sprzedaży zwykle próg testu na całość testu). To osobna zmiana, więc nie uruchamiaj go w tym samym tygodniu co zmianę budżetu albo grupy. [STANDARD]

**Zestaw Advantage+ (szeroki) i kampanie Advantage+:** zasady są te same. W szerokich grupach koncentracja budżetu na 1-2 reklamach jest jeszcze silniejsza, bo algorytm ma więcej swobody. Nie zawężaj grupy tylko po to, żeby rozłożyć budżet na kreacje. Grupa i kreacje to dwie osobne decyzje. [STANDARD]

**Co odpowiedzieć ownerowi:** „Te reklamy nie są złe, tylko jeszcze nie sprawdzone. Dopóki zwycięzcy trzymają wynik, zostawiamy je w spokoju. Jeśli chcesz przetestować którąś konkretnie, zróbmy test kreacji z równym budżetem, zamiast wyłączać zwycięzcę.”

## Skalowanie budżetu

- Ile możesz podnieść, zależy od zapasu nad progiem opłacalności. Przy leadach liczysz go jako maksymalny koszt leada / obecny koszt leada, przy SaaS według `saas-launch.md` (4a), przy sprzedaży przez ROAS. Przy ROAS 3-4 i progu 1 jest dużo miejsca. Przy ROAS 1,3 prawie żadnego, bo większy budżet każe Mecie szukać coraz mniej dopasowanych ludzi i konwersja spada. [SPRAWDZONE RAZ]
- **Ostrożnie:** +10-20% co 2-3 dni, dopóki wynik się trzyma. To bezpieczna droga przy małym budżecie albo wąskiej grupie. [STANDARD]
- **Odważnie:** większy skok od razu. Strach przed „resetem uczenia” jest przesadzony: jeśli masz poduszkę finansową, 1-2 słabsze dni zwykle i tak zarabiają więcej niż powolne podnoszenie. Decyduje to, ile możesz stracić i jak szeroka jest grupa. Szerokość grupy ma znaczenie przy budżetach czterocyfrowych dziennie, a nie przy 50 zł. [SPRAWDZONE RAZ]
- **Nie duplikuj kampanii, żeby podnieść budżet.** Od lat nie ma takiej potrzeby, podnoś w miejscu. [SPRAWDZONE RAZ]
- Nie podnoś budżetu „bo spodziewam się dobrego dnia”. Podnoś, bo wynik z kilku dni na to pozwala.
- **Nie skaluj na zmęczonych kreacjach.** Kilkukrotne podbicie budżetu na kreacjach sprzed kilku miesięcy daje wyższy koszt wyniku, a większość nowych pieniędzy zjada zwykle jedna słabsza reklama. [SPRAWDZONE RAZ]
- Jeśli Meta pakuje większość budżetu w jedną reklamę z gorszym wynikiem niż reszta i ta reklama wydała już sensowną kwotę, wyłącz ją ręcznie. [SPRAWDZONE RAZ]

## Google: cotygodniowo

- Raport wyszukiwanych haseł: dopisz wykluczenia (dopasowanie do wyrażenia), dodaj nowe dobre frazy jako słowa kluczowe.
- Słowa, które wydały 2-3x docelowy koszt leada bez konwersji: obniż albo wstrzymaj, ale dopiero gdy konwersje mierzą prawdziwe leady. [STANDARD]
- Komponenty RSA z oceną „Niska” przez ponad 2 tygodnie: podmień.
