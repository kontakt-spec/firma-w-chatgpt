# Business Hub w ChatGPT: fakty, źródła i rzeczy niepewne

Stan wiedzy: 16.11.2026. To jest beta. OpenAI zmienia ją bez zapowiedzi, więc każdą informację stąd podawaj użytkownikowi z datą.

Jak korzystać z tego pliku: wszystko, co mówisz o Business Hub, ma wynikać z tego pliku albo z tego, co sam sprawdzisz teraz u źródła (jeśli masz wyszukiwarkę). Jeśli czegoś tu nie ma, powiedz „tego nie wiem” i odeślij do panelu albo do pomocy OpenAI. Nie dopowiadaj.

Spis treści:
1. Co to jest
2. Kroki przejęcia profilu
3. Weryfikacja tożsamości (Persona)
4. Pola profilu
5. Statystyki (Insights)
6. Czego profil nie daje
7. Polska: co widzi jaki typ firmy
8. Koszt
9. Warunki, o których warto wiedzieć przed kliknięciem
10. Rzeczy sporne i niepewne
11. Co wiadomo o tym, skąd ChatGPT bierze informacje o firmie
12. Źródła

## 1. Co to jest

- OpenAI uruchomiło „Businesses in ChatGPT” 10.11.2026 jako betę.
- Business Hub to panel do zarządzania profilem firmy. Adres: chatgpt.com/business-hub. Jest też w bocznym menu ChatGPT. W Polsce panel się otwiera i ma polski interfejs.
- Całość składa się z czterech części: panel Business Hub, profil firmy, statystyki (Insights) i Business Agent.
- Nie myl tego z planem „ChatGPT Business”. To płatna subskrypcja dla zespołów i osobna rzecz. Do profilu firmy nie trzeba płatnego planu ani konta reklamowego.
- Wiele firm, także polskich, ma już profil, którego same nie zakładały. Powstał z danych z internetu.
- Business Agent (agent firmy, który odpowiada klientom w ChatGPT) działa na razie tylko dla kwalifikujących się sklepów internetowych i usług online w USA, które mają stronę. Nie przyjmuje zamówień ani rezerwacji. Dla Polski nie ma terminu.

## 2. Kroki przejęcia profilu

Według pomocy OpenAI, opisanej w źródłach z punktu 12:

1. Zaloguj się do ChatGPT i otwórz Business Hub.
2. Wyszukaj firmę po nazwie. Jeśli jest, wybierz wpis, potwierdź konto ChatGPT, z którego będziesz nim zarządzać, i kliknij „Get started”. Jeśli firmy nie ma, niektóre firmy działające online mogą utworzyć nowy profil.
3. Wybierz model działalności (patrz punkt 7).
4. Potwierdź związek z firmą jedną z metod:
   - kod na telefon firmowy (SMS albo automatyczne połączenie),
   - kod na firmowy adres e-mail,
   - rekord TXT w DNS domeny (zmiana w DNS może zadziałać po kilku minutach albo po kilku godzinach),
   - połączenie ze sklepem Shopify.
   Panel pokazuje tylko metody dostępne dla danej firmy. Nie każdy zobaczy wszystkie cztery.
5. Poczekaj na decyzję OpenAI. Przychodzi mailem. OpenAI może poprosić o dodatkowe dane. Czasu rozpatrzenia nie gwarantuje.
6. Przejdź osobną weryfikację tożsamości w serwisie Persona (punkt 3).
7. Dopiero potem zarządzasz profilem: publikujesz zmiany, podpinasz plik produktowy, widzisz statystyki.

Zmiany w profilu przechodzą moderację OpenAI. Nie pojawiają się od razu.

Jeśli ktoś przejął profil Twojej firmy przed Tobą, w menu profilu (trzy kropki) jest opcja „Dispute ownership”. Spór też kończy się weryfikacją w Persona.

Profil przejmuje właściciel albo osoba, którą upoważnił. Współpracowników i agencję dodaje się potem w panelu, każdy na swoim koncie ChatGPT. Każda marka i każdy oddział to osobne zgłoszenie. Centralnego zarządzania wieloma lokalizacjami na razie nie ma.

## 3. Weryfikacja tożsamości (Persona)

- Persona to zewnętrzna firma, która sprawdza tożsamość.
- Może poprosić o: dokument tożsamości wydany przez państwo, dane rejestrowe firmy, dowód, że masz prawo reprezentować firmę.
- Nazwa, adres i numer rejestrowy albo podatkowy muszą się zgadzać z oficjalnymi rejestrami. Polskie źródła mówią tu o CEIDG albo KRS.
- Wysłanie dokumentów to jeszcze nie zgoda. Bez zatwierdzonej weryfikacji nie opublikujesz zmian, nie podepniesz pliku produktowego, nie zobaczysz statystyk i nie utworzysz agenta.
- Jeden polski autor podał czas: Persona 5 minut, zgoda OpenAI po niecałych 40 minutach. To jeden przypadek, a nie norma. OpenAI nie podaje czasu.
- Gdy tworzysz profil od zera, zatwierdzenie publikuje go automatycznie.

Co przygotować przed startem:
- dowód osobisty albo paszport osoby, która przejmuje profil,
- aktualny wpis z CEIDG albo odpis z KRS (nazwa, adres, NIP dokładnie tak jak w rejestrze),
- pełnomocnictwo albo inny dowód umocowania, jeśli profil przejmuje ktoś inny niż właściciel lub członek zarządu,
- dostęp do firmowego telefonu, firmowej skrzynki e-mail albo do ustawień domeny (DNS).

## 4. Pola profilu

Pola wymieniane w źródłach: adres strony www, opis firmy, kategoria, logo, zdjęcie w tle, polityka dostaw, polityka zwrotów oraz inne pola opcjonalne. Jedno źródło wymienia też „dane dla rozmów”, np. zakres usług, czas realizacji, obszar działania.

Wymóg dokładności z zasad OpenAI: nazwa, kategoria, adres albo obszar działania, godziny, kontakt i to, co firma sprzedaje, mają być prawdziwe i aktualne. Zasady zakazują podszywania się, fałszywych i zdublowanych profili.

Sklepy mogą podpiąć plik produktowy (ceny, dostępność): CSV według specyfikacji OpenAI, adres hostowanego pliku albo katalog Shopify. Plik produktowy działa od startu w USA. Sklepy z innych rynków wymagają indywidualnego potwierdzenia przez OpenAI.

Nie znamy limitów znaków ani dokładnych polskich nazw pól w panelu. Nie zgaduj ich. Powiedz użytkownikowi, że nazwy pól w panelu mogą się trochę różnić.

## 5. Statystyki (Insights)

- Okres: ostatnie 28 dni.
- Wskaźniki: wzmianki, kliknięcia w stronę, tematy rozmów („discovery topics”).
- Dane są zbiorcze. Pokazują się dopiero po przekroczeniu progu, którego OpenAI nie podaje. Puste pole nie musi oznaczać zera.
- Firma nie widzi pojedynczych rozmów ani pytań użytkowników.
- Firma online: wzmianka liczy się wtedy, gdy ChatGPT linkuje do jej strony. Sama nazwa marki bez linku się nie liczy. Firma lokalna: liczy się pokazanie wyniku dla jej lokalizacji.
- Kliknięcie to kliknięcie w link w ChatGPT. Nie potwierdza wizyty ani zakupu.

## 6. Czego profil nie daje

To są stanowiska OpenAI przytaczane w źródłach. Powtarzaj je wiernie i nie łagodź:

- Przejęcie profilu nie gwarantuje wyższej pozycji ani sprzedaży.
- Przejęcie nie daje bezpośredniej kontroli nad niezależnymi rekomendacjami ChatGPT.
- Reklamy nie wpływają na niezależne odpowiedzi ChatGPT.
- Podpięcie pliku produktowego nie gwarantuje, że ChatGPT poleci produkty.
- ChatGPT może pokazywać informacje o firmie także z innych źródeł niż profil.

Dlatego nigdy nie obiecuj, że profil „poprawi pozycję w ChatGPT” albo że „ChatGPT zacznie polecać firmę”. Uczciwa wersja: profil pozwala poprawić dane, które firma kontroluje, i zobaczyć statystyki.

## 7. Polska: co widzi jaki typ firmy

Stan z testów polskich autorów z 11 do 14.11.2026. Przy budowie tego pliku 16.11.2026 nie znaleźliśmy doniesień o zmianach po 14.11. OpenAI nie publikuje listy krajów ani terminów. Zapowiada tylko, że z czasem otworzy kolejne rynki i typy firm.

| Typ firmy | Co zobaczysz w panelu | Co możesz zrobić dziś |
|---|---|---|
| Sklep internetowy, sprzedaż online | Pełna ścieżka: profil, weryfikacja (domena, e-mail, telefon albo Shopify), potem Persona. Pierwsze polskie firmy online zweryfikowano ok. 12.11.2026. | Przejąć albo utworzyć profil i przejść weryfikację. Uwaga: jeśli istniejący wpis ma adres fizyczny, może skończyć się listą oczekujących. |
| Firma z lokalem, do którego przychodzą klienci (sklep stacjonarny, restauracja, gabinet, biuro) | „Join the waitlist”, potem „You're on the waitlist”. Według pomocy OpenAI lokalne sklepy i restauracje mogą na razie przejąć tylko istniejący wpis w USA. | Znaleźć swój wpis, zapisać się na listę oczekujących (bez opłat i bez dokumentów). OpenAI ma napisać mailem, gdy będzie można dokończyć. Terminu nie ma. |
| Usługi z dojazdem do klienta (np. dekarz, hydraulik, firma budowlana) | Etykieta „Coming soon”. Ścieżka nieaktywna. | Sprawdzić, czy wpis istnieje i co w nim jest. Przygotować dane i stronę. Sprawdzać panel co jakiś czas. |
| Usługi zdalne i usługi online (np. agencja, konsulting, szkolenia online) | Źródła są sprzeczne. Jedne podają „Coming soon” razem z usługami z dojazdem. Inne podają, że firma, która sprzedaje albo świadczy usługi przez internet, może zgłosić profil. Jeden autor (firma usługowa) zobaczył „Join waitlist”. | Sprawdzić samemu w panelu. To zajmuje minutę. Powiedz użytkownikowi wprost, że tu źródła się różnią i że wynik zależy od tego, co pokaże panel. |
| Firma bez strony www | Źródła podają, że na początku przejęcie wymaga strony. | Przygotować dane i treść pod przyszłą stronę. Sprawdzić, czy wpis mimo to istnieje. |

Komunikat „Contact support” przy profilu oznacza według jednego źródła, że profil jest zablokowany.

## 8. Koszt

Profil i statystyki są w becie darmowe. Tak podają VentureBeat i Digiday za Benjim Shomairem z OpenAI. Nie wykluczył on opłat w przyszłości. Oficjalnego cennika nie ma. Reklamy w ChatGPT to osobna, płatna usługa.

## 9. Warunki, o których warto wiedzieć przed kliknięciem

Te punkty znamy z polskich omówień regulaminu „Businesses in ChatGPT Terms” (wersja z 9.11.2026), a nie z samego regulaminu. Podawaj je jako „według omówień regulaminu” i radź przeczytać regulamin przed akceptacją:

- Licencja OpenAI na podstawowe dane firmy (nazwa, adres, kontakt, kategoria, godziny, strona) jest opisana jako bezterminowa i nieodwołalna (pkt 4.2). Według drugiego źródła trwa także po rezygnacji.
- Opublikowanego profilu nie da się usunąć ani ukryć. Usunąć można tylko szkic.
- Dane ze statystyk są poufne (pkt 6). Wolno ich używać do własnej analizy i udostępniać podwykonawcom, którzy działają w imieniu firmy. Publikowanie ich wymaga zgody OpenAI.
- Wpis firmy może istnieć i być wyświetlany bez zgody firmy.
- Regulamin nie obiecuje pozycji, widoczności, ruchu ani sprzedaży.
- Zapis na listę oczekujących też odbywa się na warunkach regulaminu. Akceptuje się go przez samo korzystanie z usługi.

Nie jesteś prawnikiem użytkownika. Nie interpretuj regulaminu ponad to, co wyżej.

## 10. Rzeczy sporne i niepewne

Mów o nich otwarcie, gdy temat się pojawi:

1. Niebieski znaczek. Strona produktu OpenAI sugeruje, że znaczek pokazuje przejęty profil. Pomoc OpenAI mówi, że samo przejęcie go nie daje i że pojawia się po zatwierdzeniu w Persona. Większość źródeł ufa pomocy. Nie obiecuj znaczka.
2. Usługi zdalne w Polsce. Patrz tabela w punkcie 7.
3. „Wyświetlenia profilu” w statystykach. Jedno polskie źródło wymienia je jako czwarty wskaźnik. Pomoc OpenAI ich nie definiuje. Trzymaj się trzech wskaźników z punktu 5.
4. Czas weryfikacji. Znamy jeden przypadek (punkt 3). Nie podawaj go jako typowego.
5. Opłaty w przyszłości. Nie wiadomo.
6. Regulamin. Znamy go z omówień (punkt 9).
7. Oficjalne strony OpenAI (ogłoszenie i pomoc) blokowały automatyczny odczyt przy budowie tego pliku. Fakty pochodzą więc z opisów tych stron w kilku niezależnych źródłach, które się ze sobą zgadzają, oraz z testów polskich autorów. Tam, gdzie się nie zgadzają, jest to zaznaczone wyżej.

## 11. Co wiadomo o tym, skąd ChatGPT bierze informacje o firmie

Rozdzielaj trzy poziomy pewności. Użytkownik ma wiedzieć, na którym poziomie jest dana rada.

Potwierdzone w dokumentacji OpenAI:
- ChatGPT opisuje firmy na podstawie informacji z internetu i może korzystać z innych źródeł niż profil.
- OpenAI ma robota OAI-SearchBot, który służy do wyszukiwania w ChatGPT. Strony, które go blokują w pliku robots.txt, nie będą pokazywane w odpowiedziach wyszukiwania ChatGPT (mogą się pojawić tylko jako zwykły link). GPTBot to osobny robot do trenowania modeli. Zablokowanie GPTBot nie wyłącza strony z wyszukiwania w ChatGPT.

Rozsądne, ale bez gwarancji:
- Jasna, spójna strona z tekstem, który da się przeczytać, ułatwia zrozumienie firmy każdemu, kto ją czyta: klientowi, wyszukiwarce i modelowi AI. Jeśli Ty jako model nie możesz czegoś odczytać ze strony (tekst na grafice, PDF, treść ładowana skryptem), jest spora szansa, że inne automaty też tego nie odczytają. To wniosek, a nie obietnica OpenAI.
- Te same dane (nazwa, adres, telefon) w różnych miejscach w sieci zmniejszają ryzyko pomyłek.

Dobra praktyka bez dowodu wpływu na ChatGPT:
- Dane strukturalne schema.org. Pomagają wyszukiwarkom i porządkują dane. OpenAI nie potwierdziło, że wpływają na to, kogo ChatGPT poleca.
- Plik llms.txt. To propozycja społeczności. Nie ma potwierdzenia, że ChatGPT z niego korzysta. Nie polecaj go jako sposobu na widoczność.
- Sztuczki typu „pisz pod AI”, upychanie fraz, kupowanie wzmianek. Brak dowodów, a część łamie zasady.

## 12. Źródła

OpenAI:
- Ogłoszenie: https://openai.com/index/introducing-businesses-chatgpt/
- Pomoc: https://help.openai.com/en/articles/20001635-setting-up-your-business-on-chatgpt
- Roboty OpenAI: https://developers.openai.com/api/docs/bots (odczytane bezpośrednio 16.11.2026)

Polskie testy i omówienia:
- https://bezlaga.pl/blog/profil-firmy-w-chatgpt (14.11.2026)
- https://jarekszmajduch.pl/poradniki/profil-firmy-w-chatgpt/ (11.11.2026)
- https://sebastianbarys.pl/blog/chatgpt-business-hub (12.11.2026)
- https://emeraldmedia.pl/wizytowka-firmy-chatgpt-business-hub-instrukcja/ (12.11.2026)
- https://delante.pl/profil-firmy-chatgpt-business-hub/ (12.11.2026)

Inne:
- https://datanorth.ai/news/chatgpt-business-hub-claim-profile (11.11.2026)
- https://findskill.ai/blog/claim-your-business-in-chatgpt-business-hub-setup-2026/ (11.11.2026)
