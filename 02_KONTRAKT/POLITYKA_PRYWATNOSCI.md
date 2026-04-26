# POLITYKA PRYWATNOŚCI
## {{NAZWA_PROJEKTU}}

> Dokument publiczny — dostępny dla użytkowników aplikacji.  
> Wymagany przez RODO (art. 13 i 14). Dostosuj do faktycznego zakresu przetwarzania danych.

**Wersja:** 1.0  
**Data wejścia w życie:** _______________  
**Ostatnia aktualizacja:** _______________

---

## 1. Administrator Danych Osobowych

Administratorem danych osobowych przetwarzanych w aplikacji **{{NAZWA_PROJEKTU}}** jest:

**{{KLIENT_FIRMA}}**  
Adres siedziby: {{KLIENT_ADRES}}  
NIP: {{KLIENT_NIP}}  
E-mail kontaktowy: {{KLIENT_EMAIL}}  
Telefon: {{KLIENT_TEL}}

zwana dalej **„Administratorem"**.

> **Uwaga:** Administratorem jest Zamawiający (Twój klient) — to on decyduje o celach i sposobach przetwarzania danych swoich użytkowników. Wykonawca (deweloper) jest Podmiotem Przetwarzającym działającym na podstawie Umowy Powierzenia (Załącznik nr 2 do umowy).

---

## 2. Inspektor Ochrony Danych (IOD)

> Usuń tę sekcję, jeśli Administrator nie powołał IOD.

Administrator powołał Inspektora Ochrony Danych, z którym można skontaktować się:  
E-mail: _______________

---

## 3. Jakie Dane Osobowe Przetwarzamy

### 3.1 Dane konta użytkownika

| Kategoria danych | Przykłady | Czy wymagane? |
|-----------------|-----------|---------------|
| Dane identyfikacyjne | Imię, nazwisko | Tak |
| Dane kontaktowe | Adres e-mail, numer telefonu | Tak |
| Dane uwierzytelniające | Hash hasła (nigdy w postaci jawnej) | Tak |
| Dane o roli | Przypisana rola w systemie | Tak |
| | | |

### 3.2 Dane generowane automatycznie

| Kategoria | Opis | Cel |
|-----------|------|-----|
| Logi aktywności | Data, godzina, typ operacji, ID użytkownika | Bezpieczeństwo i audyt |
| Adres IP | Przy logowaniu | Bezpieczeństwo |
| Dane urządzenia | Typ przeglądarki / systemu (jeśli dotyczy) | Diagnostyka |

### 3.3 Dane wrażliwe

> Usuń tę sekcję, jeśli aplikacja nie przetwarza danych wrażliwych.

Aplikacja **[przetwarza / nie przetwarza]** danych szczególnych kategorii (art. 9 RODO), takich jak: _______________.  
Podstawa przetwarzania: _______________.

---

## 4. Cele i Podstawy Prawne Przetwarzania

| Cel przetwarzania | Podstawa prawna (RODO) | Okres retencji |
|-------------------|----------------------|----------------|
| Realizacja umowy / dostęp do systemu | Art. 6 ust. 1 lit. b — wykonanie umowy | Czas trwania konta + ___ lat |
| Bezpieczeństwo systemu i wykrywanie nadużyć | Art. 6 ust. 1 lit. f — prawnie uzasadniony interes | ___ miesięcy |
| Wypełnienie obowiązków prawnych (np. podatkowych) | Art. 6 ust. 1 lit. c — obowiązek prawny | 5 lat (przepisy podatkowe) |
| _______________ | _______________ | _______________ |

---

## 5. Komu Przekazujemy Dane

Dane mogą być przekazywane następującym kategoriom odbiorców:

| Odbiorca | Cel | Lokalizacja |
|----------|-----|-------------|
| Dostawca hostingu / infrastruktury (np. Google Firebase) | Przechowywanie danych | UE / USA (standardowe klauzule umowne) |
| Podmiot Przetwarzający — deweloper systemu | Utrzymanie techniczne | Polska |
| _______________ | _______________ | _______________ |

> Dane **nie są** sprzedawane ani udostępniane podmiotom trzecim w celach marketingowych.

### Przekazywanie poza EOG

> Usuń tę sekcję, jeśli dane nie są przekazywane poza EOG.

Dane mogą być przekazywane do państw trzecich (np. USA — serwery Google). Przekazanie odbywa się na podstawie:
- [ ] Standardowych Klauzul Umownych (SCC) zatwierdzonych przez Komisję Europejską
- [ ] Decyzji o adekwatności (np. EU-US Data Privacy Framework)
- [ ] Inne: _______________

---

## 6. Prawa Użytkownika

Jako osoba, której dane dotyczą, przysługują Ci następujące prawa:

| Prawo | Co oznacza | Jak skorzystać |
|-------|-----------|----------------|
| **Dostępu** (art. 15) | Możesz otrzymać kopię swoich danych | E-mail: {{KLIENT_EMAIL}} |
| **Sprostowania** (art. 16) | Możesz poprawić nieprawidłowe dane | Ustawienia konta lub e-mail |
| **Usunięcia** (art. 17) | Możesz żądać usunięcia danych („prawo do bycia zapomnianym") | E-mail: {{KLIENT_EMAIL}} |
| **Ograniczenia** (art. 18) | Możesz ograniczyć przetwarzanie | E-mail: {{KLIENT_EMAIL}} |
| **Przenoszenia** (art. 20) | Możesz otrzymać dane w formacie CSV/JSON | E-mail: {{KLIENT_EMAIL}} |
| **Sprzeciwu** (art. 21) | Możesz sprzeciwić się przetwarzaniu na podstawie uzasadnionego interesu | E-mail: {{KLIENT_EMAIL}} |

**Termin odpowiedzi:** do 30 dni od otrzymania żądania (możliwe przedłużenie do 90 dni w złożonych przypadkach).

**Prawo do skargi:** Masz prawo złożyć skargę do Prezesa Urzędu Ochrony Danych Osobowych (UODO), ul. Stawki 2, 00-193 Warszawa, [www.uodo.gov.pl](https://uodo.gov.pl).

---

## 7. Bezpieczeństwo Danych

Administrator stosuje następujące środki techniczne i organizacyjne:

- Szyfrowanie transmisji danych (HTTPS / TLS)
- Szyfrowanie danych w spoczynku (jeśli dotyczy)
- Kontrola dostępu oparta na rolach
- Regularne kopie zapasowe
- Monitorowanie i logowanie zdarzeń bezpieczeństwa
- Procedury reagowania na incydenty bezpieczeństwa

---

## 8. Pliki Cookie

> Dostosuj tę sekcję do rzeczywistego użycia cookies w aplikacji.

Aplikacja używa następujących rodzajów plików cookie:

| Rodzaj | Nazwa | Cel | Okres ważności |
|--------|-------|-----|----------------|
| Niezbędne | `session_token` | Utrzymanie sesji zalogowanego użytkownika | Do zamknięcia sesji |
| Niezbędne | _______________ | _______________ | _______________ |
| Analityczne | _______________ | _______________ | _______________ |

> Cookies niezbędne są stosowane na podstawie prawnie uzasadnionego interesu i nie wymagają zgody. Cookies analityczne wymagają zgody użytkownika.

---

## 9. Zautomatyzowane Podejmowanie Decyzji

Aplikacja **[stosuje / nie stosuje]** zautomatyzowanego podejmowania decyzji ani profilowania w rozumieniu art. 22 RODO.

> Usuń odpowiednią opcję. Jeśli stosuje — opisz logikę, znaczenie i konsekwencje.

---

## 10. Zmiany Polityki Prywatności

Administrator zastrzega sobie prawo do zmiany niniejszej Polityki. O istotnych zmianach użytkownicy będą informowani:
- [ ] Powiadomieniem w aplikacji
- [ ] Wiadomością e-mail
- [ ] Wyświetleniem komunikatu przy następnym logowaniu

Dalsze korzystanie z aplikacji po wejściu w życie zmian oznacza ich akceptację.

---

## 11. Kontakt

W sprawach związanych z ochroną danych osobowych prosimy o kontakt:

**{{KLIENT_FIRMA}}**  
E-mail: {{KLIENT_EMAIL}}  
Telefon: {{KLIENT_TEL}}  
Adres korespondencyjny: {{KLIENT_ADRES}}

---

*Niniejsza Polityka Prywatności obowiązuje od _______________.*  
*Wersja dokumentu: 1.0*
