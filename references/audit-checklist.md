# Przegląd konta: checklista

Przechodź po kolei. Przy każdym punkcie zapisz stan (OK / problem / brak danych) i, jeśli się da, ile to kosztuje miesięcznie. W raporcie najpierw 3 najdroższe problemy.

## Wspólne

- [ ] Forma płatności działa (brak banera o odrzuconej płatności).
- [ ] Wiadomo, co jest konwersją, która zarabia, i to ona jest główna.
- [ ] Znany jest próg opłacalności: maksymalny koszt leada, ROAS na zero albo maksymalny koszt triala.
- [ ] Budżet dzienny i testowy nie jest poniżej minimum z `budget.md`. Zbyt mały budżet rozbity na wiele zestawów to częsty powód „reklamy nie działają”.
- [ ] Nazwy kampanii mówią, kto je postawił i co robią (`[INICJAŁY] Opis`).
- [ ] Zakres dat w raporcie jest jawny (7 / 30 / 90 dni / cała historia).

## Google Search

- [ ] Główna konwersja to formularz, telefon albo zakup, nie odsłona. **Najczęstszy i najdroższy błąd.**
- [ ] Partnerzy wyszukiwania i sieć reklamowa wyłączone w kampanii Search.
- [ ] Są wykluczające słowa kluczowe (konto + kampanie).
- [ ] Słowa w dopasowaniu przybliżonym mają uzasadnienie i wykluczenia; w przeciwnym razie zmień na wyrażenie lub ścisłe.
- [ ] Raport wyszukiwanych haseł był przeglądany w ostatnich 14 dniach.
- [ ] Każda RSA ma min. 10 nagłówków i 4 opisy, dynamiczne N1-N2, korzyści przypięte na 3.
- [ ] Brak literówek w komponentach (przeczytaj każdy).
- [ ] Komponenty: linki do podstron, objaśnienia, połączenie, lokalizacja, obrazy.
- [ ] Landing pasuje do grupy (kampania lokalna = podstrona oferty).

## Meta: wspólne

- [ ] Kolumny z wariantem „(kliknięcia linku)”, zapisany widok konta (`meta-analysis.md`).
- [ ] Podział na wiek i płeć zgadza się z ofertą (Advantage+ potrafi pójść w 65+ albo w złą płeć).
- [ ] Żadne umiejscowienie nie zjada większości budżetu przy wyraźnie gorszym wyniku.
- [ ] Ulepszenia Advantage+ przejrzane pojedynczo: nakładki i ulepszone materiały wizualne wyłączone.
- [ ] Żadna reklama nie zjada ponad 50% budżetu przy wyniku gorszym niż średnia.
- [ ] Najstarsza aktywna kreacja ma mniej niż 8 tygodni albo wciąż trzyma wynik.
- [ ] Ruch na stronę (jeśli jest strona): wyświetlenia strony docelowej to co najmniej ~70% kliknięć linku.

## Meta na leady

- [ ] Cel Kontakty, formularz natywny albo pixel + CAPI ze zdarzeniem Lead.
- [ ] Odbiorcy Advantage+ z sygnałami zainteresowań i stanowisk.
- [ ] Wykluczeni ci, którzy wysłali formularz w ostatnich 90 dniach, a grupa obejmuje formularz używany w obecnej kampanii.
- [ ] 4-6 reklam w zestawie, różne formaty (wideo produktu, UGC, statyk).
- [ ] Koszt leada miesiąc po miesiącu: czy jest trend wzrostowy (patrz „Ile żyje kreacja” w `meta-leads.md`).
- [ ] Klient raportuje jakość leadów.

## Meta sprzedaż (produkt cyfrowy)

- [ ] Cel Sprzedaż, zdarzenie konwersji Zakup, pixel (najlepiej z API konwersji) przechodzi test zdarzeń.
- [ ] Budżet na poziomie zestawu, co najmniej dwa zestawy z identycznymi reklamami (szeroki i z podpowiedziami).
- [ ] Minimalny wiek ustawiony twardo, wiek docelowy jako sugestia, bez górnej granicy 65+.
- [ ] Jedna kreacja na reklamę, 5 tekstów i 5 nagłówków, CTA „Kup teraz”, osobny kadr 9:16.
- [ ] Żadna koncepcja nie wydała więcej niż próg testu (większa z kwot: ~400 zł albo 3 × cena) bez zwycięzcy, a mimo to dalej leci.
- [ ] Nowe kampanie, które przez 2-3 dni nie sprzedają, są wyłączane, a nie ratowane (`monitoring.md`).
- [ ] Ocena po wyniku finansowym (ROAS względem progu, koszt sprzedaży względem ceny), nie po CTR.
- [ ] Koszt dodania do koszyka i koszt zakupu spinają się z ceną produktu.
- [ ] Brak osobnej kampanii remarketingowej przy tanim produkcie (albo jest uzasadnienie liczbami).

## SaaS

- [ ] Próg opłacalności policzony: maksymalny CAC i maksymalny koszt triala (`saas.md`). Progi decyzji z `saas-launch.md` stosowane.
- [ ] Przy rejestracji zapisywane są identyfikatory kliknięć (`gclid`, `_fbc`, `_fbp`) i UTM-y.
- [ ] Płatność trafia do Mety (Conversions API) i Google (import konwersji) z serwera, z wartością.
- [ ] Osobne landingi dla kategorii, porównania z konkurencją i marki.
- [ ] Aktywacja zdefiniowana i porównywana: ruch z reklam vs organiczny.
- [ ] Wiadomo, pod co optymalizuje kampania (trial, aktywacja, płatność) i dlaczego.
- [ ] Konwersja trial → płatny liczona osobno dla ruchu z reklam, kohortami.
- [ ] Google: osobna kampania na markę i na frazy z konkurencją, z własnymi landingami.
- [ ] Decyzje o skalowaniu oparte na płacących z kohorty, nie na samym koszcie triala.
