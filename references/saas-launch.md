# SaaS: wypuszczenie kampanii krok po kroku

Jak wypuszczamy reklamy dla produktu w abonamencie: od bramki przed startem, przez budowę kampanii w Google i Meta, po decyzje w pierwszych 30 dniach. Liczby (próg opłacalności, maksymalny koszt triala) i pomiar są w `saas.md`. Bez nich nie zaczynaj.

Etykiety jak w całym playbooku. Większość reguł SaaS to [STANDARD] i [HIPOTEZA]: przenosimy zasady sprawdzone przy leadach i sprzedaży na ekonomię subskrypcji.

## 0. Bramka przed startem

Kampania nie rusza, dopóki każdy punkt nie jest „tak”.

**Liczby**
- [ ] Policzony maksymalny CAC i maksymalny koszt triala (`saas.md`, kalkulator). To one są progami w całym planie niżej.
- [ ] Budżet testu zatwierdzony przez klienta: ~40 × maksymalny koszt triala na kanał, z akceptacją, że może pójść na naukę.

**Pomiar**
- [ ] Rejestracja / start triala zlicza się w Mecie (pixel + Conversions API) i w Google (konwersja główna). Sprawdzone testową rejestracją.
- [ ] Przy rejestracji zapisujesz w bazie `gclid`, `fbclid`/`_fbc`, `_fbp` i UTM-y. Bez tego płatności po trialu nie połączysz z reklamą. **Najczęściej pomijany punkt.**
- [ ] Płatność wysyłana z serwera (webhook bramki płatności) do Conversions API i do Google przez import konwersji, z wartością. Może ruszyć tydzień po starcie, ale musi być przed oceną pierwszej kohorty.
- [ ] Zdefiniowana aktywacja: jedno zdarzenie, po którym użytkownik „poczuł” produkt (pierwszy projekt, pierwszy import, pierwsza wysłana faktura). Zlicza się jako zdarzenie dodatkowe.

**Landing i oferta**
- [ ] Osobny landing dla każdej intencji: kategoria, porównanie z konkurencją, marka (strona główna wystarczy).
- [ ] Nad zgięciem: efekt w nagłówku (nie lista funkcji), zrzut albo krótkie nagranie produktu, jeden przycisk („Wypróbuj za darmo”), informacja „bez karty”, jeśli to prawda.
- [ ] Rejestracja w 1-2 krokach, najlepiej z logowaniem Google. Każde dodatkowe pole obniża konwersję z reklamy.
- [ ] Pierwsza wartość w produkcie w kilka minut. Jeśli onboarding trwa dzień, reklamy będą „drogie”, choć problem jest w produkcie. [STANDARD]
- [ ] Cennik widoczny albo łatwy do znalezienia. Plan roczny pokazany obok miesięcznego.
- [ ] Strona szybka na telefonie i w przeglądarce w aplikacji Facebooka.

## 1. Który kanał najpierw

| Sytuacja | Start | Dlaczego |
|---|---|---|
| Ludzie szukają kategorii albo konkurencji („program do X”, „[konkurent] alternatywa”) | **Google Search** | Gotowy popyt, najwyższa intencja |
| Nowa kategoria, której nikt nie szuka, produkt łatwy do pokazania na nagraniu ekranu | **Meta** | Popyt trzeba wywołać kreacją |
| B2B z drogim abonamentem i demo z handlowcem | **Google** na frazy z intencją + **Meta na leady** (`meta-leads.md`), lead = umówione demo | Mały wolumen, wysoka wartość klienta |
| Jest jedno i drugie | Google najpierw, Meta po 2-3 tygodniach, gdy pomiar i landing są sprawdzone | Google szybciej pokaże, czy oferta i strona konwertują |

[STANDARD]

## 2. Google Search: budowa

**Trzy kampanie, każda z własnym budżetem i landingiem:**

| Kampania | Słowa | Landing | Budżet | Strategia na start |
|---|---|---|---|---|
| `[INICJAŁY] Brand` | własna nazwa, `[marka]`, `"[marka] logowanie"` wykluczone | strona główna | mały, 5-15 zł dziennie | Maks. liczba konwersji |
| `[INICJAŁY] Konkurencja` | `"[konkurent] alternatywa"`, `"[konkurent] vs"`, `"zamiennik [konkurent]"`, `"lepszy niż [konkurent]"` | strona porównania | 30-40% budżetu | Maks. liczba konwersji |
| `[INICJAŁY] Kategoria` | `"program do [czynność]"`, `"aplikacja do [czynność]"`, `"[kategoria] dla [grupa]"`, `"jak [czynność, którą robi produkt]"` | landing kategorii | reszta | Maks. liczba konwersji |

- Kampania na markę ma sens dopiero, gdy ktoś ją wyszukuje (sprawdź w Planerze słów kluczowych albo Search Console). Wcześniej pomiń.
- Konwersja główna na start: rejestracja / trial. Płatność importowana jako konwersja dodatkowa, dopóki nie ma jej ~15-30 miesięcznie. Potem płatność z wartością staje się główna, a strategia przechodzi na wartość konwersji. [STANDARD]
- Docelowy CPA ustawiaj dopiero po ~30 konwersjach w kampanii i nie niżej niż ~maksymalny koszt triala.
- Dopasowania, nazwy i struktura RSA jak w `google-search.md`.
- Cudzej marki nie używaj w tekście reklamy, tylko w słowach kluczowych. Strona porównania musi być uczciwa, bo kłamstwo w porównaniu kończy się zgłoszeniem.
- Wykluczenia na start: darmowy, za darmo, free, crack, chomikuj, open source, pobierz za darmo, praca, kurs, szablon, wzór, logowanie (chyba że masz darmowy plan, szablony jako lead magnet albo to Twoja kampania na markę).
- Komponenty: linki do podstron „Cennik”, „Porównanie”, „Integracje”, „Opinie”, „Umów demo”; objaśnienia z okresem próbnym i „bez karty”.

**RSA pod SaaS: wypełnij nawiasy**

```
N1  {KeyWord:Program do [Czynność]}                    (bez pinu)
N2  [Kategoria] dla [Grupa]                             (bez pinu)
N3  Alternatywa dla [Arkusza / Starego Sposobu]         (bez pinu)
N4  [Efekt] w [Czas]                                    (bez pinu)
N5  [X] Dni Za Darmo, Bez Karty                         (pin 3)   tylko jeśli prawda
N6  Start w [X] Minut                                   (pin 3)
N7  Integracja z [Narzędzie A] i [Narzędzie B]          (pin 3)
N8  Od [X] zł Miesięcznie                               (pin 3)
N9  [Liczba] Firm Już Korzysta                          (pin 3)   tylko prawdziwa liczba

O1  [Efekt dla klienta] bez [ból]. Załóż konto w [X] minut i sprawdź sam.
O2  [Funkcja 1], [funkcja 2] i [funkcja 3] w jednym miejscu. [X] dni za darmo.
O3  Przenieś dane z [konkurent / arkusz] w kilka minut. Pomożemy przy starcie.
O4  Plan od [X] zł miesięcznie, rocznie taniej o [Y]%. Bez umowy, anulujesz kiedy chcesz.
```

## 3. Meta: budowa

**Samoobsługowy SaaS (rejestracja na stronie):**

| Ustawienie | Wartość | Dlaczego |
|---|---|---|
| Cel kampanii | Kontakty albo Sprzedaż, z konwersją na stronie: ten, w którym Menedżer reklam pozwala wybrać Twoje zdarzenie (rejestracja i trial są zwykle w Kontaktach, płatność w Sprzedaży) | Optymalizacja pod zdarzenie, a nie pod kliknięcia |
| Budżet dzienny | budżet testu / ~30 dni, podzielony po równo na dwa zestawy | Ma starczyć do oceny pierwszej kohorty płacących, a nie skończyć się w tydzień |
| Zdarzenie | start triala / rejestracja na starcie, aktywacja albo płatność później (`saas.md`) | Algorytm potrzebuje kilkudziesięciu zdarzeń tygodniowo |
| Budżet | na poziomie zestawu, dwa zestawy po równo | Uczciwe porównanie grup, jak w `meta-sales-digital.md` |
| Zestaw A `ADV+` | szeroko, wiek jako sugestia pod użytkownika produktu. Minimalny wiek podnoś tylko, jeśli produkt naprawdę nie jest dla młodszych (reguła „min. 25” z produktów cyfrowych nie przenosi się automatycznie na SaaS) | Zwykle wygrywa |
| Zestaw B `ADV+ podpowiedzi` | B2B: przecięcie stanowisko / rola **i** zainteresowanie narzędziami z kategorii. B2C: przecięcie sytuacja życiowa **i** zainteresowanie tematem (np. podróże **i** nauka języków) | Celujemy w osobę, która ma problem, a nie w temat |
| Reklamy | jedna kreacja na reklamę, 5-10 na start, 5 tekstów, 5 nagłówków | Widać, która koncepcja sprowadza płacących |
| CTA | „Zarejestruj się” | Mówi, co się stanie, a pierwszy krok jest darmowy. Nie „Kup teraz” ani „Dowiedz się więcej” |
| Ulepszenia Advantage+ | nakładki i ulepszone materiały wizualne wył., reszta według `meta-sales-digital.md` | |

**SaaS B2B z demo:** kampania na leady z formularzem (`meta-leads.md`). W formularzu pytanie kwalifikujące o wielkość zespołu albo obecne narzędzie. Lead to umówione demo, nie pobrany e-book.

**Kreacje do przetestowania na start** (każda koncepcja jako osobna reklama): [STANDARD, kolejność do sprawdzenia]

1. **Nagranie ekranu „problem → kilka kliknięć → efekt”**, 15-30 s, z napisami, pion i kwadrat. Zwykle najmocniejsze w SaaS.
2. **Jedno zdanie bólu na zdjęciu z codziennej pracy grupy** (bałagan w arkuszu, sterta papierów, wieczór nad fakturami). Ta sama zasada, która wygrywa przy produktach cyfrowych.
3. **Przed i po:** stary sposób (arkusz, papier, trzy narzędzia) obok produktu.
4. **Założyciel do kamery:** 20-40 s, dlaczego zrobił narzędzie i dla kogo. Surowe nagranie telefonem.
5. **Liczba:** „[X] godzin miesięcznie mniej na [czynność]”, tylko jeśli masz ją od prawdziwych użytkowników.
6. **Porównanie:** „[stary sposób] vs [produkt]” jako prosta tabela.

**5 tekstów pod SaaS:**
1. Krótki ból + efekt: „Wciąż [czynność] w arkuszu? [Produkt] robi to za Ciebie w [czas]. [X] dni za darmo.”
2. Dzień z życia: krótka historia osoby z grupy, która traciła czas na [czynność], i jak wygląda jej tydzień teraz. Postać może być przykładowa, ale nie może udawać opinii prawdziwego klienta (bez cudzysłowu, bez „pisze nasza klientka”). Prawdziwa historia zawsze lepsza.
3. Liczby: ile czasu albo pieniędzy oszczędza, ile osób już korzysta (tylko prawdziwe liczby).
4. Porównanie: czym różni się od [stary sposób / konkurent], bez wymieniania marki konkurenta z nazwy.
5. Głos założyciela: pierwsza osoba, dlaczego powstał produkt.

Nagłówki 4-6 słów: efekt („Faktury w 2 minuty”), oferta („14 dni za darmo”), zaczepka („Wciąż robisz to ręcznie?”). Zasady pisania jak w `copy-templates.md`: efekt zamiast funkcji, bez żargonu, bez obietnic, których nie da się dotrzymać.

**Remarketing:** w SaaS ma sens, w odróżnieniu od tanich produktów. Mała kampania (10-20% budżetu Meta) do osób, które założyły trial i nie zapłaciły, plus do odwiedzających cennik. Treść: opinie, case z liczbą, plan roczny, pomoc we wdrożeniu. [HIPOTEZA]

## 4. Pierwsze 30 dni: progi decyzji

`P` = maksymalny koszt triala z kalkulatora. `CAC` = maksymalny koszt płacącego klienta.

| Kiedy | Co sprawdzasz | Decyzja |
|---|---|---|
| Dzień 1-3 | Czy reklamy wydają, czy rejestracje się zliczają w obu platformach i w bazie (z identyfikatorami kliknięć) | Nic nie zmieniaj w kampaniach. Napraw tylko pomiar, jeśli nie działa |
| Po wydaniu 3 × P w zestawie (ale nie mniej niż ~60 zł) | Czy jest choć jeden trial | Zero triali: problem z landingiem albo przekazem. Sprawdź ruch na stronę (`meta-analysis.md`) i formularz rejestracji |
| Po wydaniu ~10 × P w zestawie (ale nie mniej niż ~250 zł) | Koszt triala | Poniżej P: zostaw w spokoju. Od P do 2 × P: zostaw i dorzuć 2-3 nowe kreacje obok. Powyżej 2 × P: zmień koncepcję kreacji albo grupę |
| Dzień 7-14 | Odsetek aktywacji z reklam vs z ruchu organicznego | Wyraźnie niższa aktywacja z reklam: przekaz obiecuje coś innego niż produkt daje albo grupa jest zła. Przełącz optymalizację na aktywację, jeśli jest jej dość |
| Koniec triali pierwszej kohorty (np. dzień 14-21) | Ile triali zapłaciło, realny CAC = wydatki / płacący | CAC poniżej max: skaluj. CAC do 1,5 × max: popraw onboarding i kreacje, nie skaluj. CAC powyżej 1,5 × max: zatrzymaj kanał, napraw lejek w produkcie |
| Dzień 30 | Pełny raport kohorty, koszt triala w trendzie, które koncepcje sprowadzają płacących | Plan na kolejny miesiąc: skalowanie, nowe koncepcje albo zmiana oferty (np. trial z kartą) |

- **Skaluj tylko na płacących**, nie na tanich trialach. Podnoszenie budżetu jak w `monitoring.md`: ostrożnie +10-20% co 2-3 dni albo odważniej przy dużym zapasie pod progiem.
- **Kampanię Google na konkurencję oceniaj osobno.** Ma zwykle droższe kliknięcie i lepszą konwersję na płacących. Nie wyłączaj jej za wysoki koszt kliknięcia.
- **Kiedy problem nie jest w reklamie:** dużo triali, mało aktywacji, mało płacących. Wtedy więcej budżetu tylko pogłębia stratę. Najpierw onboarding, e-maile w trialu i oferta.

## 4a. Po 30 dniach: skalowanie działającej kampanii

Gdy masz już realny CAC z kilku kohort, decyzję o budżecie opierasz na **zapasie** = 1 − (realny CAC / max CAC). [HIPOTEZA, progi do potwierdzenia]

| Zapas | Decyzja |
|---|---|
| ≥ 30% (np. CAC 100 zł przy max 150 zł) | Skaluj odważniej, większymi krokami |
| 10-30% | Skaluj ostrożnie, +10-20% co 2-3 dni, pilnuj CAC kolejnej kohorty |
| < 10% | Nie skaluj. Nowe kreacje, onboarding albo plan roczny, żeby zrobić zapas |
| CAC powyżej max | Wróć do poprzedniego budżetu. Powyżej 1,5 × max: zatrzymaj kanał i napraw lejek |

Przy każdym skalowaniu CAC zwykle rośnie, bo algorytm sięga po gorzej dopasowanych ludzi. Następną decyzję podejmujesz po kohorcie z nowym budżetem, nie wcześniej.

## 5. Raport tygodniowy SaaS

| Kanał / kampania | Wydatki | Triale | Koszt triala vs P | Aktywacje | Płacący (kohorta) | Realny CAC vs max | Uwagi |
|---|---|---|---|---|---|---|---|

Zawsze z zakresem dat. Płacących przypisuj do tygodnia rejestracji (kohorta), a nie do tygodnia płatności.

## 6. Najczęstsze błędy przy SaaS

- Optymalizacja pod rejestrację przez miesiące bez sprawdzenia, czy te konta płacą.
- Brak zapisanych identyfikatorów kliknięć przy rejestracji, przez co płatności nie da się przypisać do reklamy.
- Jeden landing dla wszystkich intencji (strona główna dla fraz z konkurencją).
- Ocena kampanii po 3 dniach, zanim jakikolwiek trial mógł się zamienić w płatność.
- Skalowanie budżetu, gdy problem leży w onboardingu.
- Reklama obiecuje coś, czego produkt nie robi od pierwszych minut. Tanie triale, zero aktywacji.
