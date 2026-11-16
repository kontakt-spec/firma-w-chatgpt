# Scenariusze testowe

Każdy scenariusz to polecenie, jakie mógłby wpisać prawdziwy użytkownik. Test polega na przejściu skilla krok po kroku według `SKILL.md`, z prawdziwym otwieraniem stron.

## a) Usługi B2B

Polecenie: „Sprawdź moją firmę w ChatGPT. Firma: ScaleUP AI, strona: scaleupai.pl”

Co ma się wydarzyć: skill czyta stronę główną i podstrony, zauważa różnice w nazwie i danych, dobiera ścieżkę dla usług i mówi wprost, że źródła są tu sprzeczne.

Wynik: `wyniki/a-scaleupai.md`

## b) Edukacja online

Polecenie: „Jak ChatGPT widzi moją firmę? aichampion.pl, AI Champion”

Co ma się wydarzyć: skill rozpoznaje sprzedaż online, wypełnia polityki dostawy i zwrotów z regulaminu, oddziela nazwę marki od nazwy sprzedawcy.

Wynik: `wyniki/b-aichampion.md`

## c) Firma lokalna z lokalem

Polecenie: „Sprawdź moją firmę w ChatGPT: [nazwa restauracji], [adres strony]” (prawdziwa restauracja z lokalem, nazwa ukryta)

Co ma się wydarzyć: skill rozpoznaje lokal, opisuje listę oczekujących, nie opisuje pliku produktowego ani weryfikacji domeny jako dostępnych dziś kroków.

Wynik: nie publikujemy, bo to audyt firmy trzeciej.

## d1) Firma bez strony

Polecenie: „FIRMA. nie mam strony tylko facebooka, hydraulik żywiec. da się coś z tym zrobić?”

Co ma się wydarzyć: skill mówi uczciwie o wymogu strony i o „Coming soon”, zadaje pytania w jednej wiadomości, układa profil i plan treści strony z odpowiedzi użytkownika.

Wynik: `wyniki/d1-firma-bez-strony.md`

## d2) Strona, której nie da się otworzyć

Polecenie: „Sprawdź moją firmę w ChatGPT: [nazwa firmy], [adres strony]” (prawdziwa strona, nazwa ukryta)

Co ma się wydarzyć: skill mówi, że strona się nie otworzyła, nie zgaduje treści, prosi o wklejenie albo opis, nie twierdzi, że strona blokuje ChatGPT.

Wynik: nie publikujemy, bo dotyczy firmy trzeciej.

## Pytania kontrolne o wyzwalanie opisu

Skill powinien się włączyć:
- „sprawdź moją firmę w ChatGPT, strona to mojafirma.pl”
- „jak założyć wizytówkę firmy w ChatGPT?”
- „słyszałem o Business Hub, co mam tam wpisać o swoim gabinecie?”
- „czemu ChatGPT nie poleca mojego sklepu?”
- „how do I claim my business profile in ChatGPT?”
- „FIRMA”

Skill nie powinien się włączyć:
- „napisz mi opis firmy na stronę główną” (zwykła prośba o tekst)
- „ile kosztuje plan ChatGPT Business dla zespołu 5 osób?” (inny produkt)
- „zrób audyt SEO mojej strony pod Google” (inne narzędzie)
- „stwórz własnego GPT do obsługi klienta” (inne zadanie)

Tych pytań nie uruchamiałem automatycznie. Narzędzie do pomiaru wyzwalania wymaga wiersza poleceń Claude Code i wielu uruchomień. Lista jest do ręcznego sprawdzenia po instalacji.
