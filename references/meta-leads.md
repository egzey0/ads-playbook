# Meta: kampania na leady (formularz natywny)

Dla produktu, którego nikt nie szuka po nazwie, a który da się pokazać na wideo, i gdzie sprzedaż domyka człowiek: B2B, nowa kategoria, usługa z efektem „przed i po”.

## Ustawienia

| Poziom | Ustawienie | Wartość | Etykieta |
|---|---|---|---|
| Kampania | Cel | Kontakty (Leads) | [SPRAWDZONE RAZ] |
| Kampania | Nazwa | `[INICJAŁY] Lead`, odświeżenia jako nowe reklamy, nie nowe kampanie | [SPRAWDZONE RAZ] |
| Zestaw | Miejsce konwersji | Formularz natywny (instant form), bez strony i bez pixela | [SPRAWDZONE RAZ] |
| Zestaw | Optymalizacja | Leady; „Quality lead” nie daje wyraźnej przewagi przy małym budżecie | [SPRAWDZONE RAZ] |
| Zestaw | Strategia | Najwyższy wolumen, bez limitu stawki | [SPRAWDZONE RAZ] |
| Zestaw | Budżet | 40-100 zł dziennie na zestaw | [SPRAWDZONE RAZ] |
| Zestaw | Atrybucja | 1 dzień po wyświetleniu / 7 dni po kliknięciu | [STANDARD] |
| Zestaw | Miejsca wyświetlania | Automatyczne, potem korekta po podziale umiejscowień (`meta-analysis.md`) | [SPRAWDZONE RAZ] |

## Odbiorcy: „adv+ szeroko”

- Kraj, odbiorcy Advantage+ **włączeni**.
- Wiek jako sugestia ustawiony pod decydentów. W B2B zacznij od 40-60, a nie od 25-50: starsi decydenci zwykle dają tańsze i lepsze leady. Po 2-3 tygodniach skoryguj według podziału na wiek. [HIPOTEZA do testu]
- Zainteresowania i stanowiska podawane **jako sygnał, nie jako zawężenie**: zainteresowanie „b2b” plus 2-3 tematy branży klienta, do tego stanowiska typu właściciel firmy, CEO, założyciel, kierownik działu, który kupuje. [SPRAWDZONE RAZ]
- Wersja bez żadnych sygnałów („adv+ full”) przy małym budżecie nie jest lepsza. Sygnały zostawiamy. [SPRAWDZONE RAZ, mała próba]
- Wyklucz osoby, które w ostatnich 90 dniach wysłały już formularz (grupa odbiorców z interakcji z formularzem). Inaczej płacisz drugi raz za tych samych ludzi. [SPRAWDZONE RAZ]
- Ta grupa musi obejmować **formularz, którego używa obecna kampania**. Grupa założona przy starej kampanii zwykle ma tylko stare formularze, a wtedy wykluczenie niczego nie wyklucza. Sprawdź ID formularza w edycji reklamy i przy każdym nowym formularzu dopisz go do grupy. Więcej grup do retargetingu i wykluczeń: `retargeting.md`. [SPRAWDZONE RAZ]

## Lokalne usługi dla klientów indywidualnych

Remonty, usługi domowe, gabinety: ta sama kampania na leady, z innymi ustawieniami grupy i kreacji. [STANDARD]
- Lokalizacja: promień wokół obszaru, który realnie obsługujesz, a nie całe województwo.
- Bez zainteresowań B2B. Wiek jako sugestia pod osobę, która podejmuje decyzję o usłudze (np. właściciele mieszkań).
- Kreacje: przed i po z prawdziwych realizacji, krótkie nagranie z pracy, zdjęcie zespołu na miejscu. Mało grafik ze stocka.
- Formularz: pytanie o zakres usługi, termin i miejscowość lub kod pocztowy. Odfiltruje to większość pomyłek.

## Struktura reklam

- **Jedna kampania, jeden zestaw, 4-6 reklam** w środku. Meta sama przesuwa budżet na zwycięzcę. [SPRAWDZONE RAZ]
- Nazwy krótkie, typ i numer: `R1`…`R6` (wideo), `Static1`… (grafiki), `Rolka [n]` (UGC). Po nazwie widać format i partię.
- **Nowe kreacje dodawaj jako nowe reklamy obok zwycięzców**, nie w nowej kampanii, chyba że zmieniasz odbiorców. Odświeżenia stawiane jako osobne kampanie zwykle wypadają gorzej niż kontynuacja, bo zaczynają naukę od zera. [SPRAWDZONE RAZ]
- **Nową reklamę z nowym obrazem zakładaj przez „Utwórz reklamę” w zestawie**, nie przez duplikat reklamy, która korzysta z istniejącego posta. Taki duplikat po podmianie mediów nie ma linku formularza i publikacja kończy się błędem „link field is required”, a w edytorze nie ma pola, żeby to naprawić. Kolejne warianty rób już jako duplikaty tej nowej reklamy i podmieniaj w nich tylko media. [SPRAWDZONE RAZ]
- **Nie przypisuj ręcznie grafik do umiejscowień** („Dostosuj media”) w reklamie na formularz. To też wymaga linku i kończy się tym samym błędem. Pion i kwadrat Meta dopasuje sama z grafiki 4:5. [SPRAWDZONE RAZ]
- **W oknie duplikowania odznacz podpowiedzi Mety** (np. weryfikacja SMS w formularzu, muzyka w Reels). Zmieniają formularz albo kreację, czyli dokładają drugą zmianę naraz. Przy grafikach z tekstem wyłącz też ulepszenia Advantage+ (retusz, animacja, nakładki, poprawki tekstu), bo potrafią przyciąć albo przerobić tekst na grafice. [SPRAWDZONE RAZ]

## Jakie kreacje działają w B2B

| Format | Jak wypada | Dlaczego |
|---|---|---|
| Wideo produktu w działaniu, z napisami, plus długi tekst z listą korzyści | najlepiej, najwyższy CTR | Widać, co produkt robi, a jedna mocna liczba w nagłówku daje powód do kliknięcia |
| Krótkie wideo z parametrami technicznymi plus darmowa wycena jako CTA | dobrze | Konkret plus niski próg kontaktu |
| Rolka z jednym zdaniem i hashtagami | niestabilnie | Potrafi zjeść dużą część budżetu przy przeciętnym koszcie leada. Pilnuj jej ręcznie |
| Statyczne grafiki | słabiej niż wideo | W B2B trudno grafiką pokazać, jak działa produkt |

[SPRAWDZONE RAZ]

## Ile żyje kreacja

Przy tych samych kreacjach koszt leada rośnie z czasem w przewidywalny sposób: pierwsze 4-8 tygodni to najtańsze leady, potem CTR spada mniej więcej o połowę, a koszt leada rośnie 2-3 razy i bez nowych kreacji już nie wraca. Nowa kampania z nowymi kreacjami powtarza tę samą krzywą. [SPRAWDZONE RAZ]

Wniosek: plan nowej partii kreacji co 4-6 tygodni ustalasz z klientem przed startem, a nie wtedy, gdy wynik już siadł (`monitoring.md`).

## Formularz

- Krótki: imię, telefon, e-mail, firma, plus 1 pytanie kwalifikujące (np. o skalę firmy albo termin zakupu). [STANDARD]
- Typ „większa intencja” (ekran potwierdzenia przed wysłaniem), jeśli leady są śmieciowe. [STANDARD]
- Leady trzeba odbierać w ciągu godzin, nie dni. Pobieraj je automatycznie do CRM, maila albo komunikatora. [STANDARD]
