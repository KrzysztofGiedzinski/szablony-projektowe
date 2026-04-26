# AUDIT PRODUKCYJNY — {{NAZWA_PROJEKTU}}
## Checklista gotowości do wdrożenia produkcyjnego

---

**Projekt:** {{NAZWA_PROJEKTU}}  
**Klient:** {{KLIENT_FIRMA}}  
**Wersja:** _______________  
**Data audytu:** _______________  
**Audyt przeprowadził:** _______________  

---

> **Zasada:** Każda sekcja musi być w całości zatwierdzona zanim projekt przejdzie do produkcji.  
> Niezaliczona pozycja = projekt **NIE** jest gotowy do wdrożenia.  
> Po zaliczeniu wszystkich sekcji podpisz **Protokół Gotowości Produkcyjnej** na końcu dokumentu.

---

## 1. AUDYT KODU I ARCHITEKTURY

### 1.1 Jakość kodu
- [ ] Brak błędów kompilacji (TypeScript / build)
- [ ] Linter nie zgłasza błędów (`npm run lint`)
- [ ] Code review przeprowadzony przez drugą osobę
- [ ] Brak kodu debugującego (`console.log`, `debugger`, `TODO: usunąć`)
- [ ] Brak zakomentowanego kodu produkcyjnego
- [ ] Brak zahardkodowanych wartości konfiguracyjnych (URL, klucze, hasła)

### 1.2 Zależności
- [ ] `npm audit` — brak krytycznych i wysokich podatności
- [ ] Wszystkie zależności zaktualizowane do stabilnych wersji
- [ ] Brak nieużywanych zależności w `package.json`
- [ ] `package-lock.json` / `yarn.lock` aktualny i w repozytorium

### 1.3 Architektura
- [ ] Architektura zgodna z dokumentacją (`04_TECHNIKA/architektura/README.md`)
- [ ] Decyzje architektoniczne udokumentowane w ADR (`04_TECHNIKA/decyzje/`)
- [ ] Brak znanych długów technicznych blokujących produkcję

**Sekcja 1 zaliczona przez:** _______________ **Data:** _______________

---

## 2. AUDYT BEZPIECZEŃSTWA

### 2.1 Uwierzytelnianie i autoryzacja
- [ ] Wszystkie endpointy wymagają autentykacji (poza publicznymi)
- [ ] Weryfikacja uprawnień na poziomie zasobu (nie tylko zalogowania)
- [ ] Sesje i tokeny mają rozsądny czas wygaśnięcia
- [ ] Mechanizm wylogowania działa poprawnie
- [ ] Ochrona przed brute-force (rate limiting na logowaniu)

### 2.2 Komunikacja i dane
- [ ] HTTPS wymuszony na wszystkich środowiskach
- [ ] Certyfikat SSL ważny i skonfigurowany z auto-odnowieniem
- [ ] Nagłówki bezpieczeństwa ustawione (CSP, HSTS, X-Frame-Options)
- [ ] Dane wrażliwe szyfrowane w bazie danych

### 2.3 OWASP Top 10
- [ ] **A01** Broken Access Control — weryfikacja uprawnień do zasobów
- [ ] **A02** Cryptographic Failures — dane wrażliwe szyfrowane
- [ ] **A03** Injection — walidacja i sanityzacja wszystkich danych wejściowych
- [ ] **A04** Insecure Design — architektura bezpieczeństwa przemyślana
- [ ] **A05** Security Misconfiguration — środowisko produkcyjne poprawnie skonfigurowane
- [ ] **A06** Vulnerable Components — zależności bez znanych podatności
- [ ] **A07** Auth Failures — silne uwierzytelnianie, brak domyślnych haseł
- [ ] **A09** Security Logging — logowanie zdarzeń bezpieczeństwa włączone
- [ ] **A10** SSRF — walidacja zewnętrznych żądań (jeśli dotyczy)

### 2.4 Sekrety i konfiguracja
- [ ] Żadne klucze API ani hasła nie są w repozytorium (`git log` sprawdzony)
- [ ] `.env` i `.env.local` w `.gitignore`
- [ ] Zmienne środowiskowe produkcyjne skonfigurowane na serwerze
- [ ] Klucze serwisowe mają minimalne wymagane uprawnienia

**Sekcja 2 zaliczona przez:** _______________ **Data:** _______________

---

## 3. AUDYT FUNKCJONALNY (UAT)

### 3.1 Zakres MVP
- [ ] Wszystkie funkcje z Załącznika nr 1 (Specyfikacja) działają zgodnie z opisem
- [ ] Kryteria odbioru z Załącznika nr 1 spełnione
- [ ] Scenariusze edge case przetestowane

### 3.2 Testy
- [ ] Testy jednostkowe przechodzą (`npm run test`)
- [ ] Testy integracyjne przechodzą
- [ ] Testy E2E dla krytycznych ścieżek przechodzą
- [ ] Testy akceptacyjne (UAT) przeprowadzone przez klienta

### 3.3 Kompatybilność
- [ ] Działa na Chrome (ostatnie 2 wersje)
- [ ] Działa na Firefox (ostatnie 2 wersje)
- [ ] Działa na Safari (ostatnie 2 wersje)
- [ ] Działa na Edge (ostatnie 2 wersje)
- [ ] Responsywność — działa na mobile (jeśli wymagane)
- [ ] Aplikacja mobilna przetestowana na iOS (jeśli dotyczy)
- [ ] Aplikacja mobilna przetestowana na Android (jeśli dotyczy)

### 3.4 Dostępność
- [ ] Kontrast tekstu min. 4.5:1 (WCAG 2.1 AA)
- [ ] Nawigacja klawiaturą działa
- [ ] Komunikaty błędów są czytelne i pomocne

**Sekcja 3 zaliczona przez:** _______________ **Data:** _______________

---

## 4. AUDYT WYDAJNOŚCI

### 4.1 Czasy ładowania
- [ ] Czas ładowania strony głównej < ___ ms (P95)
- [ ] Czas odpowiedzi API < ___ ms (P95)
- [ ] Lighthouse score: Performance ≥ ___ / 100

### 4.2 Skalowalność
- [ ] Przetestowano z ___ równoczesnymi użytkownikami
- [ ] Brak wycieków pamięci (memory leaks) pod obciążeniem
- [ ] Zapytania bazodanowe zoptymalizowane (brak N+1)
- [ ] Indeksy bazy danych skonfigurowane dla kluczowych zapytań

### 4.3 Zasoby
- [ ] Obrazy zoptymalizowane (kompresja, właściwe formaty)
- [ ] Pliki statyczne serwowane z CDN / cache
- [ ] Bundle JavaScript < ___ KB (gzipped)

**Sekcja 4 zaliczona przez:** _______________ **Data:** _______________

---

## 5. AUDYT INFRASTRUKTURY I DEVOPS

### 5.1 Środowisko produkcyjne
- [ ] Środowisko produkcyjne skonfigurowane i przetestowane
- [ ] Oddzielone od środowiska stagingowego / deweloperskiego
- [ ] Domena skonfigurowana i DNS propagowany
- [ ] SSL/TLS skonfigurowany i przetestowany
- [ ] Zmienne środowiskowe produkcyjne ustawione

### 5.2 Monitoring i alerty
- [ ] Monitoring uptime skonfigurowany (sprawdza co 1 min)
- [ ] Alert na niedostępność aplikacji — ktoś otrzyma powiadomienie
- [ ] Alert na błędy 5xx skonfigurowany
- [ ] Logi aplikacji dostępne i przeszukiwalne
- [ ] Dashboard monitoringu dostępny (`docs/monitoring/README.md`)

### 5.3 Backup i odtwarzanie
- [ ] Automatyczny backup danych skonfigurowany (co ___ godzin)
- [ ] Backup przetestowany — odtworzenie danych zweryfikowane
- [ ] Procedura rollback udokumentowana i przetestowana (`docs/deployment/README.md`)
- [ ] RTO (Recovery Time Objective): ___ godzin — osiągalne
- [ ] RPO (Recovery Point Objective): ___ godzin — osiągalne

### 5.4 CI/CD
- [ ] Pipeline CI/CD skonfigurowany
- [ ] Deploy na produkcję wymaga zatwierdzenia
- [ ] Automatyczne testy uruchamiają się przy każdym PR

**Sekcja 5 zaliczona przez:** _______________ **Data:** _______________

---

## 6. AUDYT RODO I PRAWNY

### 6.1 Ochrona danych osobowych
- [ ] Zidentyfikowano wszystkie miejsca przetwarzania danych osobowych
- [ ] Podpisana Umowa Powierzenia Przetwarzania Danych (Załącznik nr 2)
- [ ] Polityka Prywatności opublikowana i dostępna dla użytkowników
- [ ] Regulamin opublikowany i dostępny dla użytkowników
- [ ] Mechanizm usunięcia danych użytkownika zaimplementowany
- [ ] Logi nie zawierają danych osobowych w czystym tekście
- [ ] Dane osobowe nie wyciekają w odpowiedziach API

### 6.2 Licencje
- [ ] Licencje wszystkich bibliotek open-source sprawdzone
- [ ] Brak konfliktów licencji z modelem biznesowym
- [ ] Własność kodu ustalona zgodnie z umową (§ 11)

### 6.3 Dokumentacja prawna
- [ ] Umowa wdrożeniowa podpisana
- [ ] Specyfikacja techniczna (Załącznik nr 1) podpisana
- [ ] Warunki hostingu i SLA uzgodnione

**Sekcja 6 zaliczona przez:** _______________ **Data:** _______________

---

## 7. AUDYT DOKUMENTACJI

### 7.1 Dokumentacja techniczna
- [ ] `04_TECHNIKA/architektura/README.md` — stack i diagram systemu uzupełniony
- [ ] `04_TECHNIKA/uruchomienie/README.md` — runbook kompletny (inny developer może uruchomić projekt)
- [ ] `04_TECHNIKA/api/README.md` — API udokumentowane (jeśli dotyczy)
- [ ] `04_TECHNIKA/sekrety/README.md` — mapa sekretów aktualna
- [ ] `04_TECHNIKA/wdrozenie/README.md` — procedura deploymentu opisana
- [ ] `04_TECHNIKA/monitoring/README.md` — monitoring opisany

### 7.2 Dokumentacja dla klienta
- [ ] `05_PRZEKAZANIE/DOKUMENTACJA_UZYTKOWNIKA.md` — gotowa i sprawdzona
- [ ] Dokumentacja użytkownika dostarczona klientowi w formacie PDF
- [ ] Szkolenie przeprowadzone (`05_PRZEKAZANIE/PLAN_SZKOLEN.md` wypełniony)
- [ ] Lista obecności ze szkolenia podpisana

### 7.3 Stan projektu
- [ ] `03_PROJEKT/ROADMAP.md` — aktualny, Faza 1 w sekcji ✅ Zrobione
- [ ] `README.md` — opis projektu aktualny, URL produkcji wpisany

**Sekcja 7 zaliczona przez:** _______________ **Data:** _______________

---

## 8. AUDYT BIZNESOWY I ODBIORCZY

### 8.1 Akceptacja klienta
- [ ] Klient przeprowadził testy akceptacyjne (UAT) na środowisku stagingowym
- [ ] Wszystkie uwagi z UAT wdrożone lub formalnie odrzucone z uzasadnieniem
- [ ] Protokół Odbioru (Załącznik nr 3) podpisany przez klienta
- [ ] Klient zaakceptował wygląd i działanie systemu

### 8.2 Gotowość operacyjna
- [ ] Klient wyznaczył administratora systemu
- [ ] Konta produkcyjne dla użytkowników klienta utworzone
- [ ] Dane produkcyjne zaimportowane / zmigrowane (jeśli dotyczy)
- [ ] Klient zna procedurę zgłaszania błędów (e-mail / telefon)
- [ ] Harmonogram abonamentu uzgodniony i zaakceptowany

### 8.3 Komunikacja wdrożeniowa
- [ ] Data i godzina go-live uzgodniona z klientem
- [ ] Okno serwisowe dla wdrożenia zaplanowane
- [ ] Plan komunikacji dla użytkowników końcowych przygotowany (jeśli dotyczy)

**Sekcja 8 zaliczona przez:** _______________ **Data:** _______________

---

## 9. CHECKLISTA GO-LIVE

> Ostateczna checklista wykonywana w dniu wdrożenia.  
> Szczegółowa procedura: `05_PRZEKAZANIE/CHECKLIST_GO_LIVE.md`

- [ ] Backup danych wykonany przed wdrożeniem
- [ ] Deploy na produkcję przeprowadzony bez błędów
- [ ] Smoke test wszystkich krytycznych funkcji — zaliczony
- [ ] Monitoring potwierdza poprawne działanie systemu
- [ ] Klient poinformowany o uruchomieniu
- [ ] Dostępy produkcyjne przekazane klientowi

---

## PROTOKÓŁ GOTOWOŚCI PRODUKCYJNEJ

> Sekcja do wypełnienia po zaliczeniu **wszystkich** 8 sekcji audytu.

### Wynik audytu

| Sekcja | Status | Zaliczył | Data |
|--------|--------|----------|------|
| 1. Kod i Architektura | ✅ / ❌ | | |
| 2. Bezpieczeństwo | ✅ / ❌ | | |
| 3. Funkcjonalny (UAT) | ✅ / ❌ | | |
| 4. Wydajność | ✅ / ❌ | | |
| 5. Infrastruktura i DevOps | ✅ / ❌ | | |
| 6. RODO i Prawo | ✅ / ❌ | | |
| 7. Dokumentacja | ✅ / ❌ | | |
| 8. Biznesowy i Odbiorczy | ✅ / ❌ | | |

### Decyzja

- [ ] ✅ **PROJEKT GOTOWY DO PRODUKCJI** — wszystkie sekcje zaliczone, wdrożenie autoryzowane
- [ ] ⚠️ **WDROŻENIE WARUNKOWE** — sekcje niezaliczone: _______________ (ryzyko zaakceptowane przez: _______________)
- [ ] ❌ **PROJEKT NIE JEST GOTOWY** — niezaliczone sekcje: _______________ — wdrożenie zablokowane

### Otwarte punkty (jeśli wdrożenie warunkowe)

| # | Opis | Odpowiedzialny | Termin |
|---|------|----------------|--------|
| | | | |
| | | | |

---

### Podpisy

&nbsp;

___________________________  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ___________________________  
**WYKONAWCA** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **ZAMAWIAJĄCY**  
_______________ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _______________  
Data: _______________ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Data: _______________

---

*Po podpisaniu tego dokumentu projekt przechodzi oficjalnie do fazy produkcyjnej.*  
*Plik zatwierdź w DocFlow klikając przycisk „Zatwierdź" — będzie widoczny jako ✓ gotowy do produkcji.*
