# Meta: analiza wyników

Jak czytamy wyniki kampanii w Menedżerze reklam: jakie kolumny, jakie podziały, w jakiej kolejności szukamy problemu i jak to raportujemy.

## Zanim cokolwiek ocenisz

1. **Zakres dat.** Ustaw go świadomie i wpisz w raport. Do decyzji o kreacji: ostatnie 14-30 dni. Do decyzji o grupie i umiejscowieniach: cała historia kampanii, bo podziały na małych liczbach kłamią. Presety typu „Ostatnie 7 dni” nie liczą dzisiejszego dnia.
2. **Próba.** Nie wyciągaj wniosku z segmentu, który ma mniej niż ~10 wyników. Segment z dwoma leadami po 20 zł to szum, nie odkrycie.
3. **Punkt odniesienia to Twoja kampania.** Nie ma uniwersalnych widełek „dobrego” CTR czy CPM. Oceniasz zmianę względem własnych danych, a w sprzedaży i tak liczy się jedno: czy kampania zarabia. Dobry współczynnik konwersji przy złym wyniku finansowym to nadal zła kampania. [SPRAWDZONE]
4. **Rekomendacje Mety** (wynik sposobności, „zwiększ budżet”, „dodaj film”) to podpowiedzi pod wydatki, a nie pod Twój wynik. Nie traktujemy ich jako wskazówek. [SPRAWDZONE]
5. **Sygnał od klienta.** Raz w tygodniu pytaj, ile leadów albo zamówień było prawdziwych. Podział, który wygląda dziwnie, ale wyniki się spinają, zostawiamy. Podział, który wygląda dziwnie **i** klient narzeka na jakość, naprawiamy od razu.

## Widok kolumn

Raz na konto: tabela, „Kolumny”, „Dostosuj kolumny”, usuń domyślne, dodaj poniższe, zapisz jako widok. Wszędzie, gdzie jest wybór, bierz wariant **„(kliknięcia linku)”**, bo zwykłe kliknięcia liczą też kliknięcia w zdjęcie czy profil.

| Zawsze | Leady (dodatkowo) | Sprzedaż (dodatkowo) |
|---|---|---|
| Wydana kwota | Leady | Zakupy, wartość zakupów |
| Zasięg, wyświetlenia | Koszt leada | Koszt zakupu, **ROAS** |
| Częstotliwość | | Dodania do koszyka i ich koszt |
| CPM | | Kliknięcia linku |
| CTR (kliknięcia linku) | | Wyświetlenia strony docelowej |
| CPC (kliknięcia linku) | | |

## Podziały: co sprawdzamy i jakie wzorce się powtarzają

Kolejność od najczęściej przydatnego. Każdy podział sprawdzaj na poziomie kampanii, za całą historię.

### 1. Umiejscowienie

Najczęściej tu leżą pieniądze do odzyskania. Typowy wzorzec przy automatycznych umiejscowieniach: **Reels potrafią zjadać 40% budżetu i więcej przy koszcie wyniku o 25-35% wyższym niż zwykły feed na Facebooku.** Algorytm wybiera tanie wyświetlenia, a nie tani wynik. [SPRAWDZONE RAZ]

Co zrobić:
- Zrób wersję kreacji dedykowaną pod Reels (pion 9:16, hook w pierwszej sekundzie), zamiast puszczać tam przycięty materiał z feedu.
- Jeśli to nie pomoże w 2 tygodnie, rozdziel: osobny zestaw na feed i osobny na Reels z mniejszym budżetem.
- Sprawdź, czy nie są włączone automatyczne ulepszenia kreacji, które przerabiają materiał pod słabe miejsca.
- Feed na Instagramie i Marketplace często mają najniższy CTR. Jeśli zjadają zauważalną część budżetu bez wyników, to sygnał do działania.

Wnioski o umiejscowieniach nie przenoszą się między kreacjami: miejsce, które było najdroższe przy jednej kreacji, potrafi być najtańsze przy następnej. Sprawdzaj każdą kampanię osobno. [SPRAWDZONE RAZ]

### 2. Wiek i płeć

Przy Advantage+ wiek i płeć to tylko podpowiedź, a nie granica. Zawsze sprawdź, gdzie faktycznie poszły pieniądze. Wzorce, które się powtarzają: [SPRAWDZONE]

- **Najlepszy segment nie dostaje proporcjonalnie więcej budżetu.** Grupa z najtańszym wynikiem potrafi dostawać tyle samo co grupa o połowę droższa. Wtedy przesuń sugestię wieku w stronę najlepszego segmentu.
- **Sugestia wieku z ustawień bywa odwrotna do rzeczywistości.** W B2B najtańsze leady często dają starsi decydenci (45-64), a nie 25-44, nawet jeśli intuicja mówi inaczej.
- **Bardzo tanie wyniki od najmłodszych (18-24) w B2B to czerwona flaga, a nie sukces.** Najłatwiej wypełniają formularz ci, którzy nie mają nic do kupienia. Sprawdź z klientem, czy to były firmy.
- **65+ klika dużo i kupuje mało.** Segment z wysokim CTR i najdroższym wynikiem to zwykle przypadkowe kliknięcia najstarszych użytkowników.
- **Płeć w B2C:** kreacja potrafi przyciągać zupełnie inną grupę niż kupujący (np. zdjęcie ciała przy usłudze kosmetycznej), a algorytm uczy się dalej na złych kliknięciach.

Co zrobić: obok dotychczasowego zestawu dodaj zestaw **bez Advantage+ audience** z twardym wiekiem lub płcią i porównaj koszt wyniku po 7-14 dniach. Przy formularzach nie zostawiaj wieku 18-65+ bez ograniczeń w ofertach, które nie są dla seniorów.

### 3. Urządzenie

W leadach B2B z formularza natywnego system telefonu (iOS czy Android) zwykle niczego nie różnicuje. [SPRAWDZONE RAZ]

W sprzedaży B2C warto to sprawdzić: produkt pozycjonowany jako premium, a kupowany głównie z Androida, może oznaczać, że kreacja nie wygląda premium. [HIPOTEZA]

### 4. Pozostałe

- **Region:** w kampaniach na cały kraj sprawdź województwa, zanim zaczniesz zawężać. Kampanie w obcym języku na wiele krajów: sprawdzaj kraje obowiązkowo, wynik bywa z zupełnie innego kraju niż zakładany.
- **Karta karuzeli:** ułóż karuzelę od karty z najlepszym wynikiem.
- **Dzień tygodnia:** tylko przy kampaniach ciągłych z kilkoma miesiącami danych. Przy budżetach 40-100 zł dziennie nie ma na to dość wolumenu.
- **Tekst i nagłówek:** patrz `copy-templates.md`, sekcja testowania.

## Diagnoza: gdzie się psuje

Idź od góry i zatrzymaj się na pierwszym poziomie, który nie gra.

**1. Czy reklama w ogóle przyciąga?** CTR (kliknięcia linku), CPM, częstotliwość. Progi zmęczenia kreacji są w `monitoring.md` („Zmęczenie kreacji”): spadek CTR o 30-50%, koszt wyniku ponad 1,5 ×, częstotliwość ponad ~2,5 (wąski rynek) albo ~3,5 (szeroki). Przy zmęczeniu nie ruszasz grupy ani budżetu, tylko robisz nowe kreacje.

**2. Czy przyciąga właściwych ludzi?** Podziały wiek / płeć / umiejscowienie powyżej. Dobry CTR od złej grupy to pułapka, a nie wynik.

**3. Leady: czy są prawdziwe?** Ile leadów było rozmową handlową, a ile ofertą. Jeśli jakość spada, dodaj do formularza pytanie kwalifikujące albo przełącz na formularz „większa intencja”.

**4. Ruch na stronę (gdy lead lub sprzedaż jest na stronie):** porównaj kliknięcia linku z wyświetleniami strony docelowej. Jeśli strona ładuje się wolno albo psuje w przeglądarce Facebooka, część kliknięć nigdy jej nie zobaczy. Około 70% to norma, 80-85% to dobry wynik. Wyraźnie poniżej 70% sprawdź czas ładowania, poprawność linku i to, czy zdarzenie PageView w ogóle się odpala. [SPRAWDZONE]

**5. Sprzedaż:** koszyk i zakup. Jeśli koszt dodania do koszyka jest tak wysoki, że przy normalnym odsetku zakupów nie da się wyjść na plus, problem jest na stronie (ścieżka, karta produktu, przyciski na telefonie), a nie w reklamie. Dużo koszyków i mało zakupów to checkout: płatności, koszt dostawy pokazany za późno, błędy formularza. Część porzuconych koszyków jest normalna.

## Jak raportować wynik analizy

Najpierw 3 rzeczy, które kosztują najwięcej, każda z kwotą i konkretną zmianą. Przykład formatu:

1. Reels: [X]% budżetu przy koszcie wyniku o [Y]% wyższym niż feed. Około [Z] zł do odzyskania miesięcznie. Zmiana: kreacja pod Reels albo osobny zestaw.
2. Segment [wiek/płeć]: [X] zł przy koszcie wyniku [Y] zł, a segment [inny] daje wynik po [Z] zł. Zmiana: przesunąć sugestię wieku.
3. Zmęczenie kreacji od [kiedy]: CTR z [X]% do [Y]%. Zmiana: nowa partia kreacji tego typu, który wygrał.

Potem reszta, z zakresem dat przy każdej liczbie.

**Jak wycenić problem:** (koszt wyniku w problematycznym segmencie − koszt wyniku w najlepszym porównywalnym segmencie) × liczba wyników segmentu, przeliczone na 30 dni. Podawaj to jako górną granicę („do ~X zł miesięcznie”), bo tańszy segment nie utrzyma swojej ceny przy większym budżecie. Gdy problemu nie da się wycenić bez dodatkowych danych (np. wyniki per reklama), napisz wprost, czego brakuje.
