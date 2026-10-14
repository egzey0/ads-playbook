# Meta: kampania sprzedażowa pod produkt cyfrowy

Jak stawiamy od zera kampanię Sprzedaż pod tani produkt cyfrowy (ebook, kurs, szablon za kilkadziesiąt złotych), z zakupem na stronie. Kolejność jak w Menedżerze reklam. Na leady zobacz `meta-leads.md`.

## 0. Zanim klikniesz „Utwórz”

- **Waluta konta reklamowego** ustawiana przy zakładaniu, potem nie da się jej zmienić. Dla PL: złotówki.
- **Domena:** zweryfikuj ją w ustawieniach portfolio firmowego.
- **Płatności:** dodawaj w przeglądarce na komputerze. Doładowanie przez aplikację na iPhonie dolicza prowizję Apple. Przy zakładaniu reklamy sprawdź, czy wybrane jest właściwe konto, to z podpiętą płatnością.
- **Najpierw strona i reklamy, potem dopieszczanie produktu.** Klient nie zobaczy, jak dobry jest ebook, jeśli strona i reklama nie przekonają go do zakupu. Zrób plan produktu, ale najwięcej czasu daj stronie sprzedażowej i kreacjom. [SPRAWDZONE RAZ]
- **Strona na własnej domenie czy na platformie sprzedażowej:** ten sam produkt na własnej stronie i na stronie platformy z gotowym checkoutem sprzedaje z reklam bardzo podobnie. Wybieraj według wygody, nie według wyniku reklam. [SPRAWDZONE RAZ]
- **Portfolio firmowe, nie konto prywatne.** Konto reklamowe trzymaj w portfolio biznesowym (Business Manager). Konto „prywatne” nie ma żadnych plusów, a w portfolio wszystko masz w jednym miejscu. Konto reklamowe z innej niszy w tym samym portfolio niczemu nie szkodzi. [SPRAWDZONE]
- **Pixel i zdarzenia.** W Menedżerze zdarzeń, w zestawie danych strony, zakładka „Testowanie zdarzeń”: przejdź całą drogę klienta, od wejścia na stronę przez koszyk i dane płatności po prawdziwy zakup, i sprawdź, czy każde zdarzenie się pojawia (PageView, wyświetlenie zawartości, dodanie do koszyka, przejście do kasy, zakup). Do testu wyłącz adblocka, inaczej zdarzenia się nie pokażą. Zdarza się, że część zdarzeń zaczyna się łapać dopiero po starcie kampanii, więc nie panikuj, jeśli test pokazuje nie wszystko. Na platformach typu Shopify czy WordPress podpięcie pixela to zwykle wklejenie jego ID w integracjach sklepu. [SPRAWDZONE]
- Najlepiej pixel + API konwersji. GA4 i GTM są miłe do porównania, ale nie są warunkiem startu.
- Profil IG podepnij do strony na Facebooku. Pomaga, a reklamy i tak idą z „autora” strony, nie z Twojego prywatnego profilu. [STANDARD]

## 1. Kampania

| Ustawienie | Wartość | Dlaczego |
|---|---|---|
| Typ zakupu | Aukcja | |
| Cel | Sprzedaż | Optymalizacja pod zakup, a nie pod kliknięcia |
| Reklamy katalogu Advantage+ | wyłączone | Produkt cyfrowy, brak katalogu |
| Budżet | **na poziomie zestawu reklam** (ABO), nie kampanii | Dzielimy budżet po równo między testowane grupy (np. 2 × 30-40 zł). Wtedy oba zestawy wydają tyle samo i wynik da się porównać. Przy budżecie kampanii Meta potrafi od razu przerzucić wszystko na jedną grupę i nie wiesz, czy druga była gorsza, czy tylko nie dostała szansy. |
| Test A/B | wyłączony | Testujemy przez osobne zestawy i reklamy |
| Nazwa | opisowa, z prefiksem inicjałów | patrz `google-search.md`, konwencja nazw |

## 2. Zestawy reklam: dwa obok siebie

Stawiamy od razu dwa zestawy z tym samym budżetem i tymi samymi reklamami, żeby porównać grupę szeroką z grupą z podpowiedziami.

**Wspólne ustawienia:**

| Ustawienie | Wartość |
|---|---|
| Lokalizacja konwersji | Witryna internetowa |
| Cel wyników | Maksymalizuj liczbę konwersji |
| Zestaw danych | pixel strony |
| Zdarzenie konwersji | **Zakup**. Meta zaleca zdarzenie, którego będzie ~40-50 tygodniowo, a przy nowym produkcie tylu zakupów nie ma. Mimo to przy produktach cyfrowych ustawiamy zakup i wychodzi lepiej. Dodanie do koszyka albo przejście do kasy to uczciwa alternatywa, gdy zakupów jest bardzo mało. Nigdy wyświetlenie strony. |
| Cel kosztu wyniku | brak |
| Model atrybucji | standardowy |
| Budżet | **40 zł dziennie na zestaw** (Meta może wydać do ~1,75x dziennie, średnio wyjdzie 40) |
| Harmonogram | od teraz, bez daty zakończenia |
| Lokalizacja | Polska |
| Minimalny wiek | podnieś do 25 (więcej Meta nie pozwala). To dodatkowy sygnał, że produkt nie jest dla nastolatków. |
| Wiek jako sugestia | pod grupę produktu, np. 40-60. **Nigdy górnej granicy „65+”**: otwiera reklamę na najstarszych użytkowników, którzy klikają wszystko, co zobaczą w feedzie, i nie kupują. Nawet gdy grupa to realnie 40-65, ustaw 60 albo 64. |
| Płeć | wszyscy, chyba że produkt jest wyraźnie dla jednej płci. Wtedy zawężasz nawet w szerokiej grupie Advantage+. |
| Reklamodawca i płatnik (wymóg UE) | nazwa firmy |

**Zestaw A, `ADV+`:** „pusta” grupa Advantage+, ewentualnie z wiekiem i płcią. Meta sama szuka kupujących na podstawie treści kreacji i strony, a potem danych o tym, kto klika i kupuje. Przy ebookach w mniej więcej 8 na 10 przypadków to ten zestaw wygrywa. [SPRAWDZONE]

**Zestaw B, `ADV+ zainteresowania`:** to samo plus szczegółowe opcje jako *podpowiedź* dla algorytmu, zbudowane jako przecięcie: „pasuje do” jednej grupy (np. rodzice małych dzieci) **i musi też pasować do** drugiej (np. właściciele firm, własna działalność, właściciele małych firm). Celujemy w konkretną osobę z grupy docelowej, a nie w zainteresowanie tematem. Szacunkowe wielkości grup w podpowiedziach nie są liczbą osób w Polsce, traktuj je tylko do porównania, która grupa jest większa. Niektóre grupy da się łatwo wyłapać (rodzice, właściciele firm), inne słabo i wtedy ten zestaw wychodzi prawie tak szeroki jak pierwszy. Teoretycznie zawężony powinien wygrać, w praktyce częściej wygrywa szeroki. Dowiesz się dopiero po starcie. [SPRAWDZONE RAZ jako setup, wynik zależy od niszy]

Zestaw szeroki (`ADV+`) na starcie prawie zawsze idzie gorzej, bo pixel jeszcze nic nie wie. Nie wyłączaj go na rzecz drugiego zestawu, zanim oba nie dojdą do progu testu. Wyłączenie całej koncepcji, która nic nie sprzedaje, to osobna reguła (`monitoring.md`). [SPRAWDZONE]

## 3. Reklamy

- **Jedna kreacja na jedną reklamę.** Ustawiasz `R1` z grafiką 1, potem powielasz reklamę i w `R2` podmieniasz tylko grafikę, i tak dalej. Na start 5-10 kreacji w zestawie. Wtedy w wynikach widać, która grafika sprzedaje. [SPRAWDZONE RAZ]
- Gdy zestaw `ADV+` ma komplet reklam, **powielasz cały zestaw** i w kopii dodajesz tylko podpowiedzi zainteresowań. Oba zestawy mają wtedy identyczne reklamy i różnią się wyłącznie grupą.
- **Tożsamość:** strona na FB, konto IG (albo „użyj strony na Facebooku”).
- **Format:** pojedynczy obraz lub film, przesyłanie ręczne.
- **Miejsce docelowe:** witryna, adres strony sprzedażowej.
- **Kadrowanie:** liczą się dwa formaty, kwadrat 1:1 (feed) i pion 9:16 (relacje, rolki). Poziomy 1,91:1 wyświetla się w miejscach, gdzie prawie nas nie ma. W kadrowaniu zostaw kwadrat jako oryginał, a przy pionie kliknij „Zastąp” i wgraj osobną grafikę 9:16. Przycięty kwadrat wygląda źle. W pionie pilnuj bezpiecznych stref: na górze jest nazwa strony, na dole tekst reklamy i przycisk. Przycisk albo kluczowe hasło na grafice 9:16 umieść mniej więcej na środku, żeby nic go nie zasłoniło.
- **Tekst:** zawsze **5 tekstów głównych i 5 nagłówków**, ile tylko Meta pozwala. Każdy wariant z innym hookiem i w innym stylu, patrz `copy-templates.md`, „5 wariantów tekstu”. Opis zostaw pusty albo krótki.
- **Wezwanie do działania:** przy produktach cyfrowych zawsze „Kup teraz”. To dodatkowy bodziec dokładnie do tego, czego chcemy.
- **Promocje / kody rabatowe:** jeśli masz prawdziwy kod (np. sezonowy), dodaj go. W przeglądarce w aplikacji Facebooka pokazuje się wtedy na dole strony z informacją, że kod działa. Bez kodu zostaw wyłączone.
- **Linki do witryny i katalog:** wyłączone. Wszystko, co Meta podpowiada w tej sekcji poza kodem promocyjnym, idzie na „wył.”.
- **Ulepszenia Advantage+ (AI):** przejdź każde z osobna, nie akceptuj hurtem. [SPRAWDZONE RAZ]

  | Ulepszenie | Decyzja | Dlaczego |
  |---|---|---|
  | Dodawanie nakładek (tekst AI na grafice) | **zawsze wył.** | Wygląda tanio, potrafi dodać losowy tekst w losowym kolorze |
  | Ulepszone materiały wizualne (poszerzanie, przycinanie przez AI) | **wył.** | Formaty pod umiejscowienia przygotowaliśmy sami, AI może je tylko popsuć |
  | Podgląd strony docelowej przy komentarzach | może zostać | Klient w komentarzach widzi kawałek strony, to nie szkodzi |
  | Muzyka | może zostać | W rolkach muzyka w tle pomaga |
  | Ulepszenia tekstu | może zostać | Meta czasem pokaże nagłówek w miejscu tekstu głównego, zwykle na Instagramie. Przeważnie działa dobrze |

- **Powiązane multimedia:** jeśli Meta sama dorzuci do reklamy grafiki z Twoich wcześniejszych kampanii, usuń je. Testujemy inaczej (niżej).
- **Monitorowanie:** zdarzenia z witryny z tego samego pixela, parametry UTM jeśli używasz analityki.
- Przed publikacją obejrzyj podgląd w każdym umiejscowieniu.

Wskazówek typu „zwiększ budżet”, „dodaj film”, „wynik sposobności” nie traktujemy jako instrukcji. Kampania może mieć wynik 85/100 i być dobrze ustawiona.

## Obserwujący na Instagramie: promowanie z aplikacji

Jeśli celem jest zbudowanie profilu (obserwujący pod sprzedaż organiczną), a nie sprzedaż z reklamy: promuj posty z poziomu profilu na Instagramie, nie z Menedżera reklam. W praktyce daje to tańszych obserwujących. [SPRAWDZONE, bez wyjaśnienia dlaczego]

- Konto musi być profesjonalne (twórca lub firma).
- Cel „Odwiedziny profilu” do zbierania obserwujących, najlepiej z lead magnetem („zostaw komentarz, wyślę Ci X”). Cel „Wiadomość” przy sprzedaży przez DM.
- Promuj istniejące posty z siatki (mają już polubienia i komentarze), a dark posty tylko wyjątkowo.
- Targetowanie automatyczne w aplikacji działa jak grupa podobnych do Twoich obecnych obserwujących.

## 4. Po publikacji

- Nowe konto może kilka dni prawie nie wydawać. To normalne (`monitoring.md`).
- Progi wyłączania i oceny koncepcji: tylko według `monitoring.md`, „Kiedy wyłączyć kampanię”. Próg testu to większa z kwot: ~400 zł albo 3 × cena produktu.
- Oceniasz po ROAS, nie po CTR czy współczynniku konwersji.

## Czego nie robimy przy tanich produktach

- **Osobnych kampanii remarketingowych.** Przy produkcie za kilkadziesiąt złotych płacisz za każde kolejne wyświetlenie temu samemu człowiekowi, który i tak często nie kupi. Meta i tak sama dogrywa reklamy osobom, które już były na stronie, w ramach zwykłej kampanii. Rozdzielanie na zimne i ciepłe ma coraz mniej sensu. [SPRAWDZONE]
- **Duplikowania kampanii, żeby podnieść budżet** (`monitoring.md`).
- **Ratowania kampanii, która od startu nie sprzedaje.** Patrz `monitoring.md`, „Kiedy wyłączyć kampanię”.

## Przed publikacją: ostatnia kontrola

- [ ] Właściwa strona na FB i konto IG w każdej reklamie (przy kilku stronach Meta potrafi podstawić przypadkową).
- [ ] Budżety w obu zestawach równe i poprawne.
- [ ] Zestaw danych i zdarzenie Zakup wybrane w obu zestawach.
- [ ] Każda reklama ma kadr 1:1 i 9:16, 5 tekstów, 5 nagłówków, „Kup teraz”, link do strony sprzedażowej.
- [ ] Nakładki i ulepszone materiały wizualne wyłączone, powiązane multimedia usunięte.
