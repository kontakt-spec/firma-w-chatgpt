# Plan skilla „Firma w ChatGPT”

## Cel

Skill ma dowieźć to, co obiecuje rolka: przejść przez stronę firmy, wypisać braki i ułożyć gotowy opis do profilu w Business Hub. Do tego pytania testowe i instrukcja dla Polski. Ma działać od razu po instalacji u osoby bez wiedzy technicznej.

## Kto używa

Właściciel małej firmy albo specjalista (marketing, reklamy, projektowanie, e-commerce). Zna swój biznes. Nie zna DNS, schema.org ani robots.txt.

## Przepływ rozmowy

1. Użytkownik podaje adres strony i nazwę firmy. Jeśli nie poda, skill pyta raz, krótko.
2. Skill czyta stronę główną i 5 do 8 podstron (oferta, o nas, kontakt, cennik, FAQ, regulamin).
3. Skill ustala typ firmy: sklep online, lokal, usługi z dojazdem, usługi zdalne, mieszany.
4. Skill przechodzi checklistę i wybiera 5 do 10 braków z priorytetem i poprawką.
5. Jeśli jest wyszukiwarka: krótkie porównanie z danymi poza stroną.
6. Skill układa profil. Brak faktu to [DO UZUPEŁNIENIA].
7. Skill układa 8 do 10 pytań testowych i instrukcję oceny.
8. Skill dobiera instrukcję Business Hub do typu firmy.
9. Skill oddaje wynik w stałym układzie i zadaje najwyżej jedno pytanie na końcu.

## Fallbacki

| Sytuacja | Zachowanie |
|---|---|
| Strona się nie otwiera | Skill mówi, co się stało. Prosi o wklejenie treści albo opis firmy. Nie odtwarza strony z pamięci. Zaznacza blokadę jako temat dla web developera, bez twierdzenia, że ChatGPT też jest blokowany. |
| Brak narzędzia do otwierania stron | Od razu prosi o wklejenie treści. |
| Firma bez strony | Mówi uczciwie, że przejęcie profilu na razie wymaga strony. Zbiera dane od użytkownika. Układa profil, plan treści przyszłej strony, pytania testowe i instrukcję. |
| Brak wyszukiwarki | Jedno zdanie, że nie sprawdził danych poza stroną, i lista rzeczy do samodzielnego porównania. |
| Typ firmy niejasny | Skill podaje ocenę, zaznacza, że to ocena, i prosi o potwierdzenie na końcu. |

## Format wyniku

1. W skrócie
2. Jak AI widzi Twoją firmę teraz (6 obszarów, ocena: Jasne, Częściowo, Niejasne)
3. Co wiem o firmie ze strony (tabela faktów ze źródłami)
4. Braki i niespójności (priorytet, stan, powód, poprawka)
5. Gotowy profil do Business Hub
6. Pytania testowe do ChatGPT z instrukcją oceny
7. Business Hub krok po kroku dla Twojej firmy
8. Dane strukturalne dla web developera (opcjonalnie)
9. Co zrobić po kolei
Stopka: data stanu wiedzy, zastrzeżenie, jedna linijka o autorze.

## Podział na pliki

- `SKILL.md`: przepływ, zasady, fallbacki. Krótki, żeby model miał go w całości w kontekście.
- `references/business-hub-fakty.md`: wszystkie fakty o Business Hub z datą, źródłami i listą rzeczy spornych. Osobny plik, bo to on będzie aktualizowany, gdy beta się zmieni.
- `references/checklista-strony.md`: 27 punktów kontroli strony, priorytety i wzór poprawki.
- `references/szablon-wyniku.md`: układ wyniku.

## Zasady uczciwości

- Fakty o firmie tylko ze strony albo od użytkownika.
- Fakty o Business Hub tylko z pliku z faktami albo ze sprawdzenia u źródła, z datą.
- Żadnych obietnic widoczności. Trzy poziomy pewności dla rad: potwierdzone przez OpenAI, rozsądne bez gwarancji, dobra praktyka bez dowodu.

## Testy

Cztery przypadki plus jeden dodatkowy:
- a) scaleupai.pl: usługi B2B, wdrożenia AI,
- b) aichampion.pl: edukacja online,
- c) prawdziwa restauracja z lokalem (nazwa ukryta),
- d1) firma bez strony (opis od użytkownika),
- d2) prawdziwa strona lokalnej firmy (nazwa ukryta), która nie otworzyła się narzędziu.

Każdy wynik oceniam checklistą z `tests/RAPORT.md`.
