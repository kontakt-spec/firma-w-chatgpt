# Weryfikacja faktów o Business Hub

Data: 16.11.2026. Metoda: próba odczytu każdego źródła narzędziem do pobierania stron oraz wyszukiwanie zmian po 14.11.2026.

## Co udało się otworzyć

| Źródło | Wynik |
|---|---|
| openai.com/index/introducing-businesses-chatgpt | Nie otwiera się automatowi (błąd 403). |
| help.openai.com, artykuł 20001635 | Nie otwiera się automatowi (błąd 403). Wariant help-lb.openai.com też nie. |
| developers.openai.com/api/docs/bots | Otwarte. Potwierdzone role robotów OAI-SearchBot, GPTBot, ChatGPT-User. |
| bezlaga.pl | Otwarte. Publikacja 14.11.2026. |
| jarekszmajduch.pl | Otwarte. Publikacja 11.11.2026. |
| sebastianbarys.pl | Otwarte. Publikacja 12.11.2026. |
| emeraldmedia.pl | Otwarte. Publikacja 12.11.2026. |
| delante.pl | Otwarte. Publikacja 12.11.2026. |
| datanorth.ai | Otwarte. Publikacja 11.11.2026. |
| findskill.ai | Otwarte. Publikacja 11.11.2026. |

Wniosek: oficjalnych stron OpenAI o Business Hub nie potwierdziłem bezpośrednio. Fakty z briefu potwierdziłem w siedmiu źródłach wtórnych, które opisują te strony i w większości się zgadzają. Plik z faktami w skillu mówi o tym otwarcie (punkt 10.7).

## Fakty z briefu: status

| Fakt | Status |
|---|---|
| Start bety 10.11.2026 | Potwierdzone we wszystkich źródłach. |
| Panel chatgpt.com/business-hub i boczne menu | Potwierdzone (emeraldmedia, delante, bezlaga, findskill). |
| Cztery metody potwierdzenia związku z firmą, nie każdy widzi wszystkie | Potwierdzone (barys, szmajduch, bezlaga, emeraldmedia, findskill). |
| Decyzja OpenAI mailem, potem osobna weryfikacja w Persona | Potwierdzone. |
| Persona: dokument, czasem dane rejestrowe i dowód umocowania; zgodność z CEIDG albo KRS | Potwierdzone (barys, emeraldmedia). |
| Dopiero po Persona: publikacja, plik produktowy, statystyki, agent | Potwierdzone (barys cytuje pomoc, findskill). |
| Zmiany przechodzą moderację | Potwierdzone (barys, emeraldmedia, findskill). |
| Pola profilu | Potwierdzone (barys, findskill, emeraldmedia). |
| Plik produktowy: CSV, URL, Shopify; start w USA | Potwierdzone (emeraldmedia, findskill). |
| Statystyki z 28 dni: wzmianki, kliknięcia, tematy; progi; brak pojedynczych rozmów | Potwierdzone. |
| Brak gwarancji pozycji i sprzedaży; reklamy bez wpływu na odpowiedzi | Potwierdzone (findskill cytuje, pozostali streszczają). |
| Business Agent tylko w USA | Potwierdzone. |
| Darmowe w becie, opłat nie wykluczono | Potwierdzone (bezlaga, findskill, datanorth za Digiday). |
| „Dispute ownership” w menu profilu | Potwierdzone. |
| Polska: lokale na liście oczekujących | Potwierdzone (szmajduch, bezlaga, emeraldmedia). |
| Polska: pierwsze firmy online zweryfikowane ok. 12.11 | Potwierdzone w jednym źródle (bezlaga). |
| Persona 5 minut, zgoda po niecałych 40 minutach | Potwierdzone w jednym źródle (bezlaga), jeden przypadek. |
| Licencja bezterminowa i nieodwołalna (pkt 4.2), statystyki poufne (pkt 6) | Potwierdzone w omówieniu (barys). Szmajduch pisze o licencji bezterminowej, także po rezygnacji. Samego regulaminu nie czytałem. |

## Rozbieżności

1. Usługi w Polsce. Emeraldmedia: jedna ścieżka „Usługi” (wizyty u klientów albo praca zdalna) z etykietą „Coming soon”. Bezlaga: usługi z dojazdem i zdalne mają „Coming soon”, ale firma „sprzedająca lub świadcząca usługi przez internet” może zgłosić profil. Barys: firma usługowa zobaczyła „Join waitlist”, a ekranu „Coming soon” autor nie opisuje. Skill mówi o tym wprost i każe sprawdzić w panelu.
2. Niebieski znaczek. Strona produktu OpenAI kontra pomoc OpenAI (według barys i findskill). Skill nie obiecuje znaczka.
3. Statystyki. Emeraldmedia dodaje „wyświetlenia profilu”. Findskill zaznacza, że pomoc OpenAI ich nie definiuje. Skill trzyma się trzech wskaźników.
4. Agencje. Bezlaga: agencja nie przejmie profilu za firmę. Emeraldmedia i findskill: zespół albo agencję dodaje się w panelu. To się nie wyklucza. Skill opisuje obie rzeczy razem.
5. Wymóg strony www. Datanorth i findskill: na początku przejęcie wymaga strony. Polskie źródła tego nie podkreślają. Skill podaje to jako „źródła podają”.

## Zmiany po 14.11.2026

Wyszukiwanie z 16.11.2026 nie zwróciło żadnych doniesień o zmianach dla Polski po 14.11. Najnowsze polskie źródło to bezlaga.pl z 14.11.

## Skille w ChatGPT

- OpenAI Academy (otwarte): skille w ChatGPT używają pliku SKILL.md i otwartego standardu Agent Skills. Można je budować poza ChatGPT i wgrywać. W becie są domyślnie wyłączone i włącza je właściciel przestrzeni roboczej.
- Źródła wtórne (composio.dev z 16.09.2026, tonyreviewsthings.com z 5.08.2026): wgrywanie przez Skills, Create, Upload from your computer. Dostępność: plany Business, Enterprise, Healthcare i Edu. Co do Plus i Pro źródła się różnią. Free i Go nie mają.
- Artykułu pomocy OpenAI o skillach nie udało się otworzyć (403).

Wniosek dla repo: ten sam folder ze SKILL.md powinien działać w ChatGPT u osób, które mają skille. Większość odbiorców rolki ich nie ma, dlatego repo zawiera też wersję do wklejenia w `chatgpt/instrukcja-do-chatgpt.md`.

## Skille w Claude

Źródło: support.claude.com, artykuły „Using Skills in Claude” i „How to create custom skills” (otwarte 16.11.2026).
- Plany: Free, Pro, Max, Ultra, Team, Enterprise. Wymaga włączonego wykonywania kodu i tworzenia plików.
- Wgrywanie: Customize, Skills, przycisk „+”, „Create skill”, „Upload a skill”, plik ZIP.
- ZIP ma zawierać folder skilla jako element główny. Nazwa folderu ma być taka jak nazwa skilla.
- Rozbieżność: artykuł pomocy podaje limit opisu 200 znaków. Walidator ze skilla skill-creator od Anthropic przyjmuje 1024 znaki, zgodnie ze specyfikacją Agent Skills. Opis w tym repo ma ponad 200 znaków i mieści się w 1024. Trzeba to sprawdzić przy pierwszym wgraniu.
