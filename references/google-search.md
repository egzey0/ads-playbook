# Google Ads: kampania Search

Wszystkie przykłady fraz i tekstów to szablony. W nawiasach kwadratowych podstaw usługę, kategorię i warianty klienta.

## Ustawienia kampanii

| Ustawienie | Wartość | Etykieta |
|---|---|---|
| Typ | Search, tylko sieć wyszukiwania Google (wyłącz partnerów i sieć reklamową) | [SPRAWDZONE RAZ] |
| Budżet | 50 zł dziennie na kampanię na start | [SPRAWDZONE RAZ] |
| Strategia | Maksymalizuj liczbę konwersji, bez docelowego CPA na starcie; docelowy CPA dopiero po ~30 prawdziwych konwersjach | [STANDARD] |
| Rotacja reklam | Optymalizuj | [STANDARD] |
| Harmonogram | Cały dzień, dopóki dane nie pokażą martwych godzin | [SPRAWDZONE RAZ] |
| Urządzenia | Wszystkie | [SPRAWDZONE RAZ] |

**Warunek startu:** w koncie musi być główna konwersja, która oznacza pieniądze (formularz, telefon, rezerwacja). Patrz `measurement.md`. Częsty błąd: jedyną konwersją są „Wyświetlenia strony”. Strategia optymalizuje wtedy pod odsłony, a raport pokazuje „konwersje”, które niczego nie znaczą. [SPRAWDZONE RAZ]

## Struktura: dwie kampanie obok siebie

**1. `[INICJAŁY] Keywords_global`: kampania na intencję, cały kraj** [SPRAWDZONE RAZ]
- Lokalizacja: cały kraj. Języki: polski plus te, którymi realnie mówią klienci.
- Słowa kluczowe **tylko w dopasowaniu do wyrażenia `"..."` i ścisłym `[...]`**. Żadnych przybliżonych.
- Dwie warstwy słów:
  - **Ogólne** (główny wolumen): `"[usługa] [kategoria]"`, `"[usługa] [kategoria] premium"`, `"[synonim usługi] [kategoria]"`.
  - **Długi ogon pod konkretny wariant** (tanie kliknięcia, często za grosze): `"[usługa] [konkretny model / wariant]"`, `[[usługa] [wariant]]`. Jedno słowo na wariant.
- Typowy obraz: kilka fraz ogólnych niesie prawie cały ruch, długi ogon ma mało wyświetleń, ale kosztuje grosze, więc go zostawiamy.

**Usługa, do której klient musi przyjechać** (studio, gabinet, warsztat, szkoła): kampania na cały kraj nie ma sensu. Stawiasz tylko kampanię lokalną z punktu 2, a cały budżet idzie w nią. Zasięg: promień, jaki klient realnie pokona kilka razy w tygodniu (zwykle 5-15 km w mieście), a nie całe województwo. [STANDARD]

**2. Kampania lokalna** [SPRAWDZONE RAZ, z zastrzeżeniem]
- Lokalizacja: miasto bazowe + kilkanaście miejscowości wokół. Język: polski.
- Słowa z nazwą miasta: `"[usługa] [kategoria] [miasto]"`.
- Dopasowanie przybliżone tylko z listą wykluczeń. Bez niej płacisz za zapytania bez kluczowego słowa kategorii, czyli za klientów konkurencji z innego segmentu. [HIPOTEZA: sprawdź w raporcie wyszukiwanych haseł]
- Landing: podstrona oferty, nie strona główna.

**Konwencja nazw:** `[INICJAŁY_ZESPOŁU] Opis_zasięgu`, np. `[AB] Keywords_global`. Od razu widać, kto kampanię postawił i czy to nasza struktura, czy coś zastanego. Ten sam prefiks stosujemy w Meta. [SPRAWDZONE RAZ]

**Grupy reklam:** jedna kampania = jedna grupa = jedna RSA na start. Rozbijaj na grupy dopiero wtedy, gdy jakiś temat (np. konkretny wariant) ma własny landing i ponad ~100 kliknięć miesięcznie. [SPRAWDZONE RAZ na starcie; rozbijanie to STANDARD]

## Reklama RSA: szablon

Limity: nagłówek do 30 znaków (do 15 sztuk), opis do 90 znaków (do 4 sztuk). [STANDARD]

**Nagłówki 1-2: dynamiczne** (bez przypinania) [SPRAWDZONE RAZ]
- `[Usługa] {LOCATION(City)}`
- `[Kategoria] {LOCATION(City):Polska}`: wstawia miasto użytkownika, a gdy go nie zna, „Polska”.
- `{KeyWord:[Usługa] [Kategoria]}`: wstawia wpisane słowo kluczowe. Daj 3-4 warianty pod główne frazy.

**Nagłówki z korzyściami: przypięte na pozycję 3** [SPRAWDZONE RAZ]
Pozycja 1 łapie zapytanie, pozycja 3 sprzedaje. Każdy nagłówek ma jeden konkret:
- usługa dodatkowa: `[Usługa dodatkowa] [Kiedy/Gdzie]`
- zdjęta obawa klienta: `[Obawa] Załatwiona` / `Bez [Obawy]`
- oferta: `[Wariant A], [Wariant B], [Wariant C]`
- mniej tarcia: `[Czynność] w [X] Minuty`
- cena: `Ceny Już Od [X] zł / [Jednostka]`

Nagłówki w Title Case. [SPRAWDZONE RAZ]

**4 opisy, każdy o czymś innym** [SPRAWDZONE RAZ]
1. Co dokładnie dostajesz (warianty, stan, standard).
2. Liczba, która robi wrażenie (parametr albo oszczędność).
3. Druga oferta lub segment (np. wersja długoterminowa).
4. Elastyczność i cena.

Przed publikacją przeczytaj każdy komponent na głos. Literówka w opisie potrafi wisieć tygodniami, bo nikt nie czyta gotowej reklamy. [SPRAWDZONE RAZ]

## Do zrobienia od razu przy starcie

- **Wykluczające słowa kluczowe.** Startowa lista na poziomie konta: praca, darmowy, używane, sprzedaż, części, gra / gry, zdjęcia, tapety, wikipedia, kurs, forum. **Przejrzyj ją pod branżę przed dodaniem:** „kurs” wyklucza „kurs jogi”, „sprzedaż” wyklucza sklep. Po tygodniu dopisz wykluczenia na podstawie raportu wyszukiwanych haseł. [STANDARD]
- **Komponenty:** min. 4 linki do podstron, 4 objaśnienia, połączenie telefoniczne (jeśli klient odbiera), lokalizacja (jeśli jest wizytówka Google), obrazy. Brak komponentów to tracony CTR za darmo. [STANDARD]
- **Forma płatności z zapasem.** Odrzucona karta = kampania stoi. [SPRAWDZONE]
- **Zapis w zewnętrznym systemie rezerwacji:** jeśli system ma integrację z Google Ads lub GA4, użyj jej jako konwersji głównej. Jeśli nie, konwersją główną jest kliknięcie „Zapisz się / Zarezerwuj” prowadzące do systemu (mierzone tagiem na Twojej stronie), a co tydzień porównujesz to z liczbą nowych zapisów w systemie. [STANDARD]
- **Mało konwersji** (poniżej ~30 miesięcznie): zostań przy „Maksymalizuj liczbę konwersji”, nie ustawiaj docelowego CPA. Oceniaj po tygodniach, nie po dniach. [STANDARD]

## Czego się spodziewać

Przy dobrze dobranej intencji i wąskiej niszy CTR na poziomie kilkunastu procent nie jest niczym dziwnym, a długi ogon kosztuje grosze za kliknięcie. Koszt konwersji oceniasz dopiero wtedy, gdy konwersja mierzy prawdziwy kontakt albo sprzedaż.
