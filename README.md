# Firma w ChatGPT

Skill, który sprawdza, jak AI rozumie Twoją firmę na podstawie strony www, i przygotowuje gotowy opis do profilu w ChatGPT Business Hub.

Stan wiedzy: 16.11.2026. Wersja 1.0.0.

## Co to jest

10 listopada 2026 OpenAI uruchomiło w wersji beta Business Hub. To panel, w którym firma może przejąć swój profil w ChatGPT, poprawić opis, ofertę i kontakt oraz zobaczyć statystyki. Adres panelu: chatgpt.com/business-hub.

Jest haczyk. OpenAI mówi wprost, że samo przejęcie profilu nie gwarantuje wyższej pozycji ani sprzedaży. ChatGPT opisuje firmę na podstawie tego, co znajdzie o niej w internecie. Jeśli strona mówi co innego niż profil albo nie mówi nic konkretnego, profil tego nie naprawi.

Dlatego ten skill zaczyna od strony.

## Co dostaniesz

Podajesz adres strony i nazwę firmy. Po kilku minutach masz:

1. **Tabelę faktów.** Co da się odczytać o firmie ze strony: nazwa, oferta, dla kogo, obszar działania, ceny, godziny, kontakt, dane rejestrowe.
2. **Listę braków i niespójności.** Każdy z priorytetem i konkretną poprawką, często z gotowym zdaniem do wklejenia na stronę.
3. **Gotowy profil do Business Hub.** Wszystkie pola po polsku, tylko na podstawie faktów ze strony. Czego brakuje, jest oznaczone [DO UZUPEŁNIENIA].
4. **Pytania testowe do ChatGPT.** Takie, jakie zadałby klient, plus instrukcja, jak ocenić odpowiedzi.
5. **Instrukcję Business Hub dla Polski.** Dopasowaną do typu firmy: sklep internetowy, lokal, usługi z dojazdem, usługi zdalne.
6. **Kod danych strukturalnych** (schema.org) do przekazania osobie, która opiekuje się stroną. Jako dobra praktyka, nie jako gwarancja.

Skill działa też wtedy, gdy strona się nie otwiera (poprosi o wklejenie treści) i gdy firma nie ma strony (przygotuje opis i plan prostej strony).

## Instalacja w Claude

Potrzebujesz konta na claude.ai. Według pomocy Claude skille działają na planach Free, Pro, Max, Team i Enterprise.

1. **Pobierz plik.** Na tej stronie kliknij plik `firma-w-chatgpt.zip`, a potem przycisk pobierania (ikona strzałki w dół, „Download raw file”). Nie rozpakowuj go.
2. **Włącz tworzenie plików.** W Claude wejdź w Ustawienia (Settings), potem Możliwości (Capabilities), i włącz „Code execution and file creation”. W nowszym układzie ustawień ta opcja nazywa się „Create and edit files”. Bez niej skille nie działają.
3. **Wgraj skill.** Wejdź w Customize, potem Skills. Kliknij „+”, potem „Create skill”, potem „Upload a skill”. Wybierz pobrany plik ZIP.
4. **Włącz skill.** Na liście skilli przesuń przełącznik przy „firma-w-chatgpt”.

Nazwy przycisków mogą się trochę różnić, bo Claude zmienia interfejs. Aktualna instrukcja jest w pomocy Claude: https://support.claude.com/en/articles/12512180-using-skills-in-claude

Jeśli korzystasz z planu Team albo Enterprise, skille musi najpierw włączyć właściciel organizacji.

## Jak użyć

Otwórz nową rozmowę w Claude i napisz:

```
Użyj skilla firma-w-chatgpt. Moja firma: [nazwa]. Strona: [adres strony].
```

Przykład:

```
Użyj skilla firma-w-chatgpt. Moja firma: Studio Wnętrz Kowalska. Strona: https://przyklad.pl
```

Nie masz strony? Napisz:

```
Użyj skilla firma-w-chatgpt. Nie mam strony. Opiszę firmę.
```

Włącz w Claude wyszukiwanie w internecie (Web search), żeby skill mógł otworzyć Twoją stronę. Jeśli go nie włączysz, skill poprosi o wklejenie treści strony.

## Użycie w ChatGPT

ChatGPT ma własne skille w tym samym formacie (folder z plikiem SKILL.md). Według źródeł z jesieni 2026 nie są one dostępne na planach Free i Go, w planach firmowych włącza je administrator, a co do Plus i Pro źródła się różnią. Dlatego są dwie drogi.

### Droga 1: dla każdego, bez instalacji

1. Otwórz w tym repozytorium plik `chatgpt/instrukcja-do-chatgpt.md`.
2. Skopiuj całą jego treść (przycisk „Copy raw file”).
3. Otwórz nowy czat w ChatGPT, wklej treść, a pod spodem dopisz nazwę firmy i adres strony.

Jeśli chcesz wracać do tego narzędzia, utwórz w ChatGPT projekt i wklej treść pliku w pole instrukcji projektu. Plik ma około 7100 znaków, żeby zmieścił się w polu instrukcji projektu albo własnego GPT.

### Droga 2: jeśli masz skille w ChatGPT

Jeśli w bocznym menu ChatGPT widzisz Skills, wybierz Create, potem „Upload from your computer” i wskaż plik `firma-w-chatgpt.zip` albo sam plik `SKILL.md`. Tę ścieżkę znam z opisów innych autorów. Oficjalnej strony pomocy OpenAI nie udało mi się otworzyć przy budowie skilla, więc przyciski mogą wyglądać inaczej.

Ważne przy obu drogach: pytania testowe zadawaj w nowym czacie, a nie w tym, w którym ChatGPT przeczytał już Twoją stronę. Inaczej wynik będzie zafałszowany.

## Ograniczenia i zastrzeżenia

- **Beta się zmienia.** Wszystko, co skill mówi o Business Hub, to stan na 16.11.2026. Jeśli panel pokazuje coś innego, wierz panelowi.
- **Skill nie wie, co ChatGPT odpowiada o Twojej firmie.** Ocenia stronę. To, co mówi ChatGPT, sprawdzasz sam pytaniami testowymi.
- **Żadnych gwarancji widoczności.** Skill nie obiecuje, że ChatGPT zacznie Cię polecać. Nikt uczciwy tego nie obieca. Jasne i spójne informacje powinny zmniejszać ryzyko pomyłek. To rozsądne założenie, a nie obietnica.
- **Dane strukturalne i llms.txt.** Schema.org to dobra praktyka dla wyszukiwarek. OpenAI nie potwierdziło, że wpływa na rekomendacje ChatGPT. Nie ma też potwierdzenia, że ChatGPT korzysta z plików llms.txt, więc skill ich nie poleca.
- **Polska.** Według testów polskich autorów z 11 do 14.11.2026 pełną ścieżkę przechodzą głównie sklepy internetowe i firmy sprzedające online. Firmy z lokalem trafiają na listę oczekujących. Usługi z dojazdem mają etykietę „Coming soon”. Dla usług zdalnych źródła są sprzeczne.
- **Źródła.** Oficjalne strony OpenAI o Business Hub blokują automatyczny odczyt. Fakty pochodzą z ich opisów w kilku niezależnych źródłach i z polskich testów. Pełna lista, daty i rzeczy sporne są w pliku `firma-w-chatgpt/references/business-hub-fakty.md`.
- **Regulamin.** Według omówień regulaminu opublikowanego profilu nie da się usunąć, a licencja na podstawowe dane firmy jest bezterminowa. Przeczytaj regulamin OpenAI, zanim go zaakceptujesz. Skill nie zastępuje prawnika.
- **Skill czyta to, co jest publiczne.** Jeśli strona wymaga logowania albo blokuje automaty, poprosi Cię o wklejenie treści.
- **Sprawdź wynik.** AI może się pomylić przy czytaniu strony. Zanim wkleisz profil do panelu, przeczytaj go i porównaj z rzeczywistością.

## Co jest w repozytorium

```
firma-w-chatgpt.zip            gotowy plik do wgrania do Claude
firma-w-chatgpt/SKILL.md       instrukcja dla modelu
firma-w-chatgpt/references/    fakty o Business Hub, checklista strony, szablon wyniku
chatgpt/                       wersja do wklejenia w ChatGPT
tests/                         plan, scenariusze, wyniki testów i raport
CHANGELOG.md                   historia zmian
LICENSE                        licencja MIT
```

## Licencja

MIT. Możesz używać, zmieniać i udostępniać dalej.

## Autor

Paweł Czapczyk. Uczę specjalistów i małe firmy, jak używać AI w pracy bez zgadywania. Darmowy webinar: https://webinar.aichampion.pl
