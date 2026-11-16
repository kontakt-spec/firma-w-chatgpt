# Raport z testów

Data: 16.11.2026. Wersja skilla: 1.0.0.

## Jak testowałem

Przeszedłem skill krok po kroku według `SKILL.md`, tak jak zrobiłby to model, który go wykonuje. Strony otwierałem naprawdę, narzędziem do pobierania stron. Pełne wyniki są w `tests/wyniki/`.

Ograniczenie metody: skill pisał i testował ten sam model, w jednej sesji. To słabszy test niż niezależne uruchomienia na czystym koncie. Przed publikacją warto wgrać ZIP do Claude i puścić scenariusz a) oraz c) jeszcze raz.

Drugie ograniczenie: narzędzie do pobierania stron zwraca streszczenie strony, a nie surowy kod. Dlatego punkty checklisty o tekście na grafikach i o treści ładowanej skryptem sprawdziłem tylko pośrednio.

## Checklista oceny

1. Fakty ze strony: tabela faktów ze źródłami.
2. Braki i niespójności z priorytetem i konkretną poprawką.
3. Gotowy profil, wszystkie pola, [DO UZUPEŁNIENIA] tam, gdzie brak danych.
4. Pytania testowe jak od klienta i instrukcja oceny.
5. Instrukcja dla Polski z datą i zastrzeżeniem o becie.
6. Brak fake newsów i obietnic.
7. Nic nie zmyślone: każdy fakt o firmie ma pokrycie na stronie albo w słowach użytkownika.
8. Prosty język.
9. Brak myślników w roli pauzy.
10. Instrukcja pasuje do typu firmy.

## Wyniki

| Kryterium | a) scaleupai.pl | b) aichampion.pl | c) restauracja z lokalem | d1) bez strony | d2) strona zablokowana |
|---|---|---|---|---|---|
| 1. Fakty ze strony | tak | tak | tak | tak (od użytkownika) | nie dotyczy |
| 2. Braki z poprawkami | tak, 10 | tak, 7 | tak, 10 | tak, plan zamiast braków | nie dotyczy |
| 3. Profil | tak | tak | tak | tak | nie dotyczy |
| 4. Pytania testowe | tak, 10 | tak, 10 | tak, 10 | tak, 9 | nie dotyczy |
| 5. Instrukcja z datą | tak | tak | tak | tak | zapowiedziana |
| 6. Brak fake newsów | tak | tak | tak | tak | tak |
| 7. Nic nie zmyślone | tak | tak | tak po poprawce | tak | tak |
| 8. Prosty język | tak po poprawce | tak po poprawce | tak po poprawce | tak | tak |
| 9. Brak myślników | tak | tak | tak | tak | tak |
| 10. Dopasowanie do typu | tak | tak | tak | tak | zapowiedziane |
| Ocena | zaliczony | zaliczony | zaliczony | zaliczony | zaliczony |

Kryterium 9 sprawdziłem skryptem na całym katalogu. Jedyne łączniki ze spacjami po obu stronach to nazwa rejestrowa „ScaleUP - Paweł Czapczyk” cytowana ze strony.

## Co znalazł każdy test

### a) scaleupai.pl (usługi B2B)

Skill znalazł prawdziwe problemy, których nie widać bez porównania podstron:
- trzy warianty nazwy (ScaleUP, ScaleUP AI, ScaleUP - Paweł Czapczyk),
- różne domeny adresu e-mail na scaleupai.pl i aichampion.pl,
- różne miejscowości na obu stronach,
- trzy różne czasy wdrożenia na trzech podstronach,
- brak pełnej nazwy rejestrowej w regulaminie.

Ścieżka: usługi. Skill powiedział wprost, że źródła są sprzeczne, i nie zgadywał.

### b) aichampion.pl (edukacja online)

Skill oddzielił nazwę marki od nazwy sprzedawcy, wypełnił polityki dostawy i zwrotów z regulaminu i zauważył trzy liczby opisujące czas trwania. Ścieżka: sprzedaż online, z zastrzeżeniem, że źródła opisują ją głównie na sklepach.

### c) restauracja z lokalem (nazwa ukryta)

Najciekawszy wynik: na stronie głównej numer domu i kod pocztowy są zlane w jeden ciąg cyfr. Narzędzie przy czytaniu jednej z podstron samo odczytało przez to zły numer domu. To pokazuje na żywo, po co jest ten skill.

Skill dobrał listę oczekujących i nie opisał pliku produktowego ani weryfikacji domeny jako kroków dostępnych dziś.

### d1) firma bez strony

Skill powiedział uczciwie o dwóch przeszkodach (brak strony, „Coming soon” dla usług z dojazdem), zadał pytania w jednej wiadomości i ułożył profil oraz treść prostej strony wyłącznie z odpowiedzi użytkownika.

### d2) strona, której nie da się otworzyć

Prawdziwy przypadek: strona lokalnej firmy (nazwa ukryta) zwróciła błąd. Skill nie zgadywał treści, nie użył danych z katalogów, dał dwie drogi dalej i nie stwierdził, że strona blokuje ChatGPT.

## Co poprawiłem po testach

Runda 1:

| Problem | Gdzie wyszedł | Poprawka |
|---|---|---|
| Parafraza dodała szczegół, którego nie było na stronie („desery z własnej pracowni” zamiast „własne wypieki”) | c | Poprawiony wynik. Do `SKILL.md` dodana zasada o upiększaniu przy parafrazie z tym przykładem. |
| Instrukcja użyła nazwy przycisku „Get started”, której nie było w pliku z faktami | c | Fakt dodany do `business-hub-fakty.md` ze źródła (jarekszmajduch.pl). |
| Uwaga o regulaminie przy zapisie na listę oczekujących nie miała pokrycia w pliku z faktami | c | Fakt dodany do `business-hub-fakty.md` ze źródła (sebastianbarys.pl). |
| Szablon nie miał miejsca na liczby i obietnice firmy, więc mieszały się z faktami | a, b | Dodany wiersz „Deklaracje firmy, których nie weryfikowałem”. |
| Wynik zawierał same problemy, bez słowa o tym, co działa | a, b, c | Dodane zdanie „Co jest w porządku”. |
| Pytania testowe nie łączyły się ze znalezionymi niespójnościami | a, b, c | Dodane zdanie „U Ciebie zwróć uwagę na...”. |
| Szablon nie przewidywał firmy bez strony w punktach 4 i 8 | d1 | Dodane warianty w szablonie i w `SKILL.md`. |
| Brak informacji, których podstron skill nie czytał | c | Dodane pole „Nie czytałem” w nagłówku wyniku. |

Runda 2 (przegląd oczami właściciela małej firmy):

| Problem | Poprawka |
|---|---|
| Słowo „robots.txt” pojawiało się bez wyjaśnienia | Wyjaśnienie w nawiasie w szablonie i w wynikach. |
| README sugerowało pewność co do wpływu spójnych danych | Zdanie zmienione na „rozsądne założenie, a nie obietnica”. |
| README zakładało, że użytkownik ma włączone wyszukiwanie w Claude | Dodana instrukcja włączenia i informacja, co się stanie bez niego. |

Po poprawkach przeszedłem checklistę jeszcze raz na wszystkich pięciu wynikach. Wszystkie kryteria spełnione.

## Kontrola faktów o Business Hub w wynikach

Każde zdanie o Business Hub w pięciu wynikach porównałem z plikiem `business-hub-fakty.md`. Lista użytych twierdzeń i ich pokrycie:

| Twierdzenie w wynikach | Punkt w pliku z faktami |
|---|---|
| Lokale w Polsce trafiają na listę oczekujących, wpisy lokalne tylko w USA | 7 |
| Usługi z dojazdem mają „Coming soon” | 7 |
| Dla usług zdalnych źródła są sprzeczne | 7, 10 |
| Sprzedaż online przechodzi pełną ścieżkę | 7 |
| Przejęcie na początku wymaga strony | 7 |
| Cztery metody potwierdzenia, rekord TXT działa z opóźnieniem | 2 |
| Decyzja mailem, potem Persona, dokumenty, zgodność z CEIDG albo KRS | 2, 3 |
| Jeden przypadek: 5 minut i niecałe 40 minut | 3 |
| Moderacja zmian, brak terminów | 2 |
| Statystyki z 28 dni, progi, wzmianka z linkiem | 5 |
| Brak gwarancji pozycji i kontroli nad rekomendacjami | 6 |
| Profilu nie da się usunąć, licencja bezterminowa, według omówień | 9 |
| Darmowe w becie, opłat nie wykluczono | 8 |
| Robot OAI-SearchBot i robots.txt | 11 |
| Schema.org bez potwierdzonego wpływu | 11 |

Nie znalazłem twierdzenia bez pokrycia.

## Kontrola techniczna

- Frontmatter `SKILL.md` przechodzi walidator ze skilla skill-creator. Opis skrócony do 190 znaków, bo Claude.ai przy wgrywaniu ZIP przyjmuje maksymalnie 200 znaków (support.claude.com, artykuł 12512198).
- `SKILL.md` ma 144 linie.
- ZIP zawiera folder `firma-w-chatgpt/` jako element główny, zgodnie z pomocą Claude.
- Wersja dla ChatGPT ma około 7100 znaków.
- W katalogu nie ma adresów e-mail, numerów telefonów (poza fikcyjnym 000 000 000 w teście d1), numerów NIP ani pauz i półpauz.

## Czego nie sprawdziłem

- Nie wgrałem ZIP do prawdziwego konta Claude. Nie mam do tego narzędzia.
- Nie sprawdziłem wgrywania skilla w ChatGPT.
- Nie zmierzyłem, jak często opis skilla włącza go przy różnych poleceniach.
- Nie otworzyłem oficjalnych stron OpenAI o Business Hub (błąd 403). Szczegóły w `WERYFIKACJA-FAKTOW.md`.
- Nie zadałem pytań testowych w ChatGPT. To robi użytkownik.
