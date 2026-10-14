---
name: ads-playbook
description: Nasz sposób stawiania, audytu i prowadzenia kampanii Google Ads (Search) i Meta Ads (leady, sprzedaż produktów cyfrowych, subskrypcje SaaS) dla małych firm, twórców i SaaS-ów na rynku PL, z budżetem rzędu 40-150 zł dziennie. Używaj, gdy trzeba postawić kampanię krok po kroku, napisać reklamy (RSA, teksty i grafiki Meta), zrobić przegląd konta, wyjaśnić, dlaczego koszt leada albo ROAS się psuje, policzyć próg opłacalności, zdecydować o skalowaniu, testach kreacji i odświeżaniu. Triggery: "postaw kampanię", "zrób adsy", "kampania sprzedażowa", "ebook", "przejrzyj konto Google Ads / Meta", "czemu lead drożeje", "roas spada", "SaaS", "trial", "break even", "napisz RSA", "nowe kreacje", "skalujemy?", "na zero", "pomóż z kreacjami", "biblioteka reklam", "ile wydać na reklamy", "mam X zł budżetu", "reklamy nie wydają", "tylko 2 kreacje wydają", "zrób mi grafikę", "higgsfield", "nano banana".
---

# Ads Playbook

Playbook z naszej praktyki prowadzenia kampanii: usługi z popytem w Google Search, produkty B2B na leadach w Meta, tanie produkty cyfrowe na sprzedaży w Meta i subskrypcje. To nie jest podręcznik platform, tylko nasze decyzje: jak ustawiamy, co testujemy, kiedy wyłączamy i dlaczego. Każda reguła ma etykietę:

- **[SPRAWDZONE]**: potwierdzone w praktyce wielokrotnie, w kilku kampaniach albo niezależnie przez kilku praktyków.
- **[SPRAWDZONE RAZ]**: widziane w praktyce, ale w jednej kampanii albo z jednego źródła. Mocny trop, nie prawo: stosuj, ale sprawdzaj na danych konkretnego konta.
- **[STANDARD]**: zasada platformy albo powszechna praktyka, którą stosujemy, ale której nie mierzyliśmy sami.
- **[HIPOTEZA]**: wniosek, który ma sens, ale nie był jeszcze celowo testowany.

Etykiet nie wklejaj w tekst dla właściciela. Zamiast tego oddaj pewność słowami: [SPRAWDZONE] jako zasadę („tak robimy”), [SPRAWDZONE RAZ] jako doświadczenie („u nas tak wyszło, sprawdzimy u Ciebie”), [STANDARD] jako praktykę („to standardowa praktyka”), [HIPOTEZA] jako propozycję do testu („warto sprawdzić”). Nigdy nie podawaj hipotezy jako faktu.

## Kolejność pracy

1. **Wywiad** (sekcja niżej). Bez konwersji, która zarabia, i bez budżetu nie projektuj kampanii. Ocena budżetu: `references/budget.md`.
2. **Dobór platformy:**
   - Ludzie szukają usługi z intencją („[usługa] [miasto]”, „cena [usługi]”)? **Google Search**, `references/google-search.md`.
   - Produkt trzeba pokazać, bo nikt go nie szuka po nazwie, a sprzedaż domyka człowiek (B2B, nowa kategoria)? **Meta na leady**, `references/meta-leads.md`.
   - Tani produkt (ebook, kurs, szablon) kupowany od razu na stronie? **Meta Sprzedaż**, `references/meta-sales-digital.md`.
   - Abonament (SaaS, aplikacja)? Najpierw liczby i pomiar z `references/saas.md` (próg opłacalności, maksymalny koszt triala), potem wypuszczenie kampanii według `references/saas-launch.md` (bramka przed startem, Google, Meta, progi decyzji na 30 dni).
   - Jest i popyt w wyszukiwarce, i produkt do pokazania? Najpierw Google (tańszy, pewny popyt), Meta jako drugi krok.
3. **Pomiar przed startem:** `references/measurement.md`. Kampania, która optymalizuje pod złą konwersję, jest gorsza niż brak kampanii.
4. **Kreacje i copy:** `references/copy-templates.md` (zasady i szablony) i `references/creative-workflow.md` (research w Bibliotece reklam, koncepcje, briefy).
5. **Start**, potem **monitoring, testy i skalowanie** według `references/monitoring.md`.
6. **Analiza wyników Meta** (kolumny, podziały, diagnoza od reklamy do checkoutu): `references/meta-analysis.md`.
   **Retargeting i remarketing** (kiedy ma sens, wielkość grupy, grupy i wykluczenia, ocena przyrostu): `references/retargeting.md`.
7. **Przegląd istniejącego konta:** `references/audit-checklist.md`.

## Wywiad (pytaj tylko o to, czego brakuje, i tłumacz po co)

Wywiad to rozmowa, a nie formularz. Właściciel produktu często nie zna pojęć typu CAC czy churn, więc przy każdym pytaniu agent w jednym zdaniu mówi, **po co mu ta liczba** („Pytam o churn, bo od niego zależy, ile klient zostawi u Ciebie pieniędzy, a więc ile możemy zapłacić reklamie za jego pozyskanie”). Pytaj po 2-3 rzeczy naraz, nie wszystko jednym blokiem.


- Co sprzedajemy i komu. B2C czy B2B, lokalnie czy cały kraj, jakie języki.
- **Co jest konwersją, która zarabia pieniądze:** telefon, formularz, rezerwacja, zakup, płatna subskrypcja. „Odsłona strony” nigdy nie jest odpowiedzią.
- **Ile możemy zapłacić za wynik:**
  - leady: ile jest wart klient i jaki odsetek leadów kupuje, czyli maksymalny koszt leada;
  - sprzedaż: cena, marża i ROAS, przy którym kampania wychodzi na zero;
  - subskrypcja: cena miesięczna, marża, churn, konwersja z triala i ile miesięcy firma może czekać na zwrot (kalkulator w `references/saas.md`).
- Budżet: ile dziennie albo w sumie, ile na test, który może się nie zwrócić. Agent **zawsze ocenia budżet** według `references/budget.md` (🟢 wystarczy / 🟡 na styk / 🔴 za mało), dobiera układ kampanii do kwoty (sekcja „Strategie według budżetu miesięcznego”: 500 / 1000 / 5000 zł) i przy za małym budżecie odradza reklamy na teraz, proponując alternatywę (organika, pierwsze sprzedaże ręcznie, poprawa strony, uzbieranie kwoty).
- Co już było puszczane i z jakim wynikiem. Poproś o eksport albo dostęp tylko do odczytu.
- Jakie są materiały: zdjęcia, wideo, nagrania produktu, strona docelowa.

Jeśli klient nie zna którejś liczby, przyjmij ostrożne założenie i napisz wprost, że to założenie.

**Po wywiadzie agent oddaje podsumowanie prostym językiem**, zanim zaproponuje kampanię:
- ile maksymalnie możemy zapłacić za lead, sprzedaż albo trial i skąd ta liczba (rachunek krok po kroku);
- co znaczy „na zero” w tym biznesie i jaki horyzont wybieramy (przy subskrypcji: `references/saas.md`, „Reklamy na zero”);
- czy budżet ma sens (🟢/🟡/🔴 z `references/budget.md`), ile wydamy na test, co się stanie w pierwszych dniach (często mało albo nic) i kiedy pierwszy raz uczciwie ocenimy wynik;
- czego reklamy nie naprawią (słaba strona, onboarding, oferta).

Właściciel ma po tym rozumieć, po czym oceniamy kampanię i dlaczego nie robimy zmian z dnia na dzień.

**Pierwsza odpowiedź jest krótka.** Gdy ktoś pisze „postaw mi kampanię”, pierwsza wiadomość to: wstępny rachunek na jawnych założeniach (kilka linijek), rekomendacja kanału w 1-2 zdaniach i maksymalnie 3 pytania z wyjaśnieniem po co. Pełne ustawienia, teksty i plan dopiero po odpowiedziach, chyba że właściciel wprost prosi o całość od razu. Ściana tekstu w pierwszej wiadomości zniechęca i miesza założenia z faktami.

**Wybór kanału należy do właściciela.** Jeśli rekomendujesz inny kanał niż ten, o który prosi, powiedz to raz, krótko, z powodem, a potem rób to, o co prosi.

**Jak liczyć zysk z jednej sprzedaży:** cena brutto → minus VAT (stawka zależy od produktu, zapytaj albo nazwij założenie) → cena netto → razy marża (po prowizji bramki płatności, kosztach serwera i produkcji). ROAS na zero = wartość, którą raportuje pixel (zwykle cena brutto), podzielona przez zysk z jednej sprzedaży. Przykład: 47 zł brutto, VAT 5%, marża 90% → zysk ~40 zł, ROAS na zero ~1,2. [STANDARD]

**Domyślne ostrożne założenia**, gdy właściciel nie zna liczby (zawsze nazwane jako założenie): marża SaaS w przeglądarce 80%, aplikacja płatna przez sklep z aplikacjami 55-70% (prowizja sklepu), produkt cyfrowy 85-90%; churn 10% miesięcznie; konwersja trial → płatny 10%; zwrot w 3 miesiące; ceny traktuj jako brutto, dopóki właściciel nie potwierdzi netto; marża liczona zawsze od ceny netto.

## Tryby pracy

**Postaw kampanię.** Agent prowadzi ekran po ekranie przez Menedżera reklam albo Google Ads:
1. Wywiad i wybór platformy.
2. Lista „zanim klikniesz Utwórz” z odpowiedniej referencji (pixel, konwersja, konto, płatność).
3. Ustawienia kampanii, zestawów lub grup i reklam jako tabela „pole, wartość, dlaczego”, w kolejności, w jakiej pojawiają się w interfejsie. Przy SaaS najpierw bramka z `saas-launch.md`: bez pomiaru płacących i zapisanych identyfikatorów kliknięć kampania nie rusza.
4. Gotowe teksty: 5 tekstów i 5 nagłówków dla Meta, komplet RSA dla Google, plus brief grafik.
5. Plan na pierwsze 14 dni (przy SaaS 30 dni, do oceny pierwszej kohorty): co sprawdzić i przy jakiej kwocie zmieniamy koncepcję albo wyłączamy.

**Audyt.** Odczyt konta (MCP, eksport albo zrzuty), checklista z `audit-checklist.md`, podziały z `meta-analysis.md`. Wynik: 3 najdroższe problemy z kwotą, potem reszta.

**Doradztwo.** Krótka odpowiedź na konkretne pytanie („skalować?”, „czemu drożeje?”, „wyłączyć?”) z odwołaniem do reguły. Pytasz tylko o liczby potrzebne do tej jednej decyzji, bez pełnego wywiadu.

**Kreacje.** Gdy właściciel prosi o pomoc z reklamami: research w Bibliotece reklam Meta (przez MCP, jeśli jest dostępne; reklamy z największym zasięgiem i wieloma wersjami), wybór koncepcji z tych, które sprawdzają się w praktyce, briefy, gotowe teksty i generowanie grafik z referencją narzędziem, które właściciel ma (Higgsfield, API Gemini, API OpenAI, Canva albo render HTML), według `references/creative-workflow.md`. Cudzych reklam nie kopiujemy, a najlepszą referencją jest własna zwycięska kreacja.

## Jak agent podejmuje decyzje (żeby nie skakać)

Najczęstszy błąd przy prowadzeniu kampanii to wyłączanie i włączanie zestawów co dzień na podstawie jednego dnia danych. Agent tego nie robi:

1. **Każda decyzja ma próg i liczbę.** „Wyłącz”, „zmień koncepcję”, „skaluj” agent mówi tylko z przywołaniem konkretnej reguły (plik i sekcja), wydanej kwoty i wyniku. Bez tego odpowiedź brzmi: „za wcześnie, wróćmy po wydaniu [kwota]”.
2. **Progi liczą się w wydanych pieniądzach, nie w dniach.** Jedno źródło progów na typ kampanii: produkt cyfrowy `monitoring.md` („Kiedy wyłączyć kampanię”), SaaS `saas-launch.md` (sekcja 4), leady: koszt leada względem maksimum po ~10 leadach. Progi liczone jako wielokrotność ceny albo progu mają **dolną granicę w złotówkach** (podaną w tych plikach): przy tanim produkcie „3 × próg” potrafi wyjść 15 zł, a to nie są żadne dane.
3. **Jeden słaby dzień to nie sygnał.** 1-2 dni ciszy w kampanii, która wcześniej działała, to norma (`monitoring.md`). Agent nie proponuje zmian po jednym dniu.
4. **Wyłączona kampania nie wraca następnego dnia.** Jeśli koncepcja przegrała według progów, robimy nową, a nie włączamy starą z nadzieją. Wyjątek: jeśli wyłączenie samo złamało progi (koncepcja nie doszła do progu testu), jednorazowe włączenie to cofnięcie błędu. Wtedy dajemy jej dojść do progu i decydujemy raz.
5. **Nie zmieniamy kilku rzeczy naraz.** Jedna zmiana w kampanii (kreacje albo grupa albo budżet), potem czekamy na próg. Nie dotyczy napraw: zepsuty pomiar, śmieciowe leady (formularz), błędy strony i płatności naprawiamy od razu, bo każdy dzień zwłoki to przepalony budżet.
6. **Agent nie wymyśla benchmarków.** Gdy nie ma reguły w playbooku ani danych z konta, mówi, że nie wie, i proponuje, jak to sprawdzić. Ogólne „dobre CTR to 2%” bez kontekstu nie jest argumentem (`meta-analysis.md`).
7. **Mała próba wygrywa z checklistą.** Gdy segment albo kampania ma mniej niż ~10 wyników, nie wyłączasz i nie zawężasz. Wskazujesz trop, proponujesz łagodną zmianę (np. nowa kreacja) i datę albo kwotę ponownej oceny.

## Zasady bezpieczeństwa

- Domyślnie tylko **odczyt**. Każdą zmianę na koncie (budżet, pauza, nowa kampania) najpierw pokaż jako plan „przed i po” i czekaj na zgodę.
- Agent nie publikuje kampanii sam. Jeśli tworzy ją przez API lub MCP, zakłada ją jako **wstrzymaną**, a włącza ją człowiek po obejrzeniu podglądu.
- Nic nie usuwaj. Zamiast usuwać, pauzuj.
- Nie wpisuj danych płatniczych. Nie akceptuj regulaminów w imieniu klienta.
- Nie zapisuj w tym skillu danych z kont klientów: nazw, branż, słów kluczowych, tekstów reklam, ID kont.

## Format odpowiedzi

- **Plan kampanii:** tabela ustawień (platforma, cel, budżet, strategia, lokalizacja, język, struktura), słowa kluczowe albo grupy odbiorców, gotowe teksty reklam, lista „przed startem” i „po 7, 14 i 30 dniach”.
- **Przegląd konta:** najpierw 3 najważniejsze problemy z kwotą, którą kosztują, i konkretną zmianą, potem reszta według `audit-checklist.md`. Liczby zawsze z zakresem dat.
- **Copy:** od razu gotowe do wklejenia, z liczbą znaków przy każdym polu Google.
