# Pomiar: przed startem

Zasada: algorytm optymalizuje dokładnie pod to, co mu dasz jako konwersję. Zła konwersja oznacza, że płacisz za złych ludzi i nie wiesz o tym, bo raport wygląda dobrze.

## Google

- **Główne** konwersje (te, pod które optymalizuje strategia): wysłanie formularza (strona podziękowania albo zdarzenie), kliknięcie w telefon na stronie, połączenie z reklamy dłuższe niż 60 s, rezerwacja lub zakup.
- **Dodatkowe** (tylko do obserwacji, nie do optymalizacji): odsłona strony, przewinięcie, kliknięcie w mapę.
- Nie dawaj „Wyświetlenia strony” jako głównej konwersji. To częsty błąd: gdy jest jedyną konwersją, strategia „Maksymalizuj liczbę konwersji” optymalizuje pod odsłony, a raport pokazuje „konwersje”, które niczego nie znaczą. [SPRAWDZONE RAZ]
- Sprawdź tag: Google Tag Assistant albo podgląd w GTM. Konwersja ma się pojawić w Google Ads w ciągu 24 h od testowego wysłania. [STANDARD]
- Ruch z UE: baner zgód musi przekazywać decyzję do Google (Consent Mode v2). Bez tego część konwersji nie trafia do Google Ads, a listy remarketingowe rosną wolno albo wcale. Sprawdź w Tag Assistant, czy po akceptacji zgód stan zgody zmienia się na „granted”. [STANDARD]

## Meta

- Formularz natywny mierzy się sam, bez pixela. To główny powód, dla którego u małych B2B zaczynamy od niego. [SPRAWDZONE RAZ]
- Jeśli lead idzie na stronę: pixel + Conversions API ze zdarzeniem `Lead` i deduplikacją. [STANDARD]
- Jakość leadów sprawdzaj ręcznie co tydzień z klientem: ile leadów to rozmowa, ile to oferta. Koszt leada bez tej informacji jest półprawdą. [STANDARD]

## Sprzedaż na stronie

- Pixel + Conversions API ze zdarzeniami `ViewContent`, `AddToCart`, `InitiateCheckout`, `Purchase` z wartością i walutą, z deduplikacją. [STANDARD]
- Test całej ścieżki przed startem: Menedżer zdarzeń, „Testowanie zdarzeń”, prawdziwy zakup od wejścia po płatność, adblock wyłączony (`meta-sales-digital.md`). [SPRAWDZONE]

## Subskrypcja

- Płatność przychodzi po trialu, więc pixel jej nie zobaczy. Wysyłaj ją z serwera (webhook bramki płatności) do Conversions API i do Google przez import konwersji. Szczegóły i kolejność optymalizacji w `saas.md`. [STANDARD]

## Raport tygodniowy (minimum)

| Kolumna | Skąd |
|---|---|
| Wydatki | platforma |
| Leady / konwersje główne | platforma |
| Koszt leada | platforma |
| CTR, CPM / CPC | platforma |
| Leady zakwalifikowane przez klienta | klient |
| Sprzedaż z leadów | klient |
