# CHECKLISTA GO-LIVE — {{NAZWA_PROJEKTU}}

> Wypełniać sekwencyjnie w dniu uruchomienia produkcji.  
> Każdy punkt musi być ✅ zanim przejdziesz do następnego bloku.  
> Osoby zaangażowane: Wykonawca + {{KLIENT_KONTAKT}} (Zamawiający)

---

**Data go-live:** _______________  
**Okno czasowe:** ___:___ – ___:___  
**Prowadzi:** _______________  
**Obecni:** _______________

---

## BLOK A — Dzień Przed Go-Live

### A1. Kod i Build

- [ ] Wszystkie funkcje z Załącznika nr 1 są zaimplementowane i przetestowane na stagingu
- [ ] Testy automatyczne przechodzą (CI zielone)
- [ ] Nie ma otwartych błędów krytycznych ani ważnych
- [ ] Build produkcyjny zbudowany i przetestowany lokalnie
- [ ] Gałąź `main` / `master` jest aktualna i gotowa do deployu
- [ ] CHANGELOG zaktualizowany do wersji v1.0.0

### A2. Infrastruktura

- [ ] Domena skonfigurowana i propagowana (DNS TTL obniżony dzień wcześniej)
- [ ] Certyfikat SSL zainstalowany i ważny (min. ___ dni)
- [ ] HTTP → HTTPS redirect działa
- [ ] Zmienne środowiskowe produkcyjne ustawione (patrz `docs/secrets/README.md`)
- [ ] Backup danych z stagingu wykonany (jeśli migracja danych)

### A3. Backup i Rollback

- [ ] Plan rollbacku przygotowany i przetestowany (patrz `docs/deployment/README.md`)
- [ ] Backup bazy danych stagingowej zrobiony
- [ ] Wiadomo kto i jak wykonuje rollback w razie problemów
- [ ] Czas na rollback oszacowany: max ___ minut

---

## BLOK B — Go-Live: Deployment

### B1. Deploy

- [ ] Poinformowano klienta o starcie okna go-live
- [ ] Stara wersja (jeśli dotyczy) wycofana / wyłączona
- [ ] Migracja danych przeprowadzona (jeśli dotyczy)
- [ ] Deploy wykonany: ___:___ (godzina)
- [ ] Build na produkcji ukończony bez błędów

### B2. Konfiguracja Postartu

- [ ] Zmienne środowiskowe zweryfikowane na produkcji
- [ ] Pierwsze konto administratora utworzone
- [ ] Dane testowe / seed data usunięte z produkcji (jeśli dotyczy)
- [ ] Import danych klienta wykonany (jeśli dotyczy)
- [ ] Pierwsze konta użytkowników dla klienta utworzone

---

## BLOK C — Weryfikacja Po Deployu (Smoke Test)

### C1. Dostępność

- [ ] {{HOSTING_URL}} odpowiada z kodem 200
- [ ] Strona ładuje się w < ___ sekund
- [ ] Certyfikat SSL ważny (kłódka w przeglądarce)
- [ ] Wersja aplikacji w stopce / About to v1.0.0

### C2. Krytyczne Ścieżki (Happy Path)

- [ ] Logowanie działa (test kontem admina)
- [ ] Logowanie działa (test kontem zwykłego użytkownika)
- [ ] _______________ działa (główna funkcja systemu)
- [ ] _______________ działa
- [ ] _______________ działa
- [ ] Wylogowanie działa

### C3. Bezpieczeństwo

- [ ] Dostęp bez logowania → przekierowanie na stronę logowania
- [ ] Użytkownik bez uprawnień nie widzi zasobów admina
- [ ] HTTPS wymuszony (HTTP → redirect)
- [ ] Nagłówki bezpieczeństwa ustawione (sprawdź: [securityheaders.com](https://securityheaders.com))

### C4. Integracje Zewnętrzne

- [ ] _______________ (np. e-mail) działa
- [ ] _______________ (np. płatności) działa w trybie produkcyjnym
- [ ] _______________ działa

---

## BLOK D — Monitoring i Alerty

- [ ] Monitoring uptime aktywny i działa (patrz `docs/monitoring/README.md`)
- [ ] Alert na downtime skonfigurowany i przetestowany
- [ ] Alert na błędy 5xx skonfigurowany
- [ ] Logi aplikacji spływają do narzędzia monitoringu
- [ ] Backup automatyczny uruchomiony (pierwszy backup wykonany)
- [ ] Panel monitoringu dostępny dla Wykonawcy

---

## BLOK E — Komunikacja i Finalizacja

### E1. Przekazanie Klientowi

- [ ] Klient powiadomiony o uruchomieniu systemu
- [ ] Dane dostępowe przekazane {{KLIENT_KONTAKT}}
- [ ] URL produkcyjny potwierdzony: {{HOSTING_URL}}
- [ ] Krótka instrukcja pierwszego logowania wysłana

### E2. Dokumentacja

- [ ] `docs/deployment/README.md` zaktualizowany o datę i wersję v1.0.0
- [ ] `ROADMAP.md` — Faza 1 przeniesiona do ✅ Zrobione
- [ ] `README.md` projektu zaktualizowany (URL produkcji, status)

### E3. Formalności

- [ ] Protokół Odbioru (Załącznik nr 3) gotowy do podpisania
- [ ] Faktura za transzę końcową / rozliczenie przygotowane

---

## BLOK F — Obserwacja Po Go-Live

> Wykonaj ___ godzin po uruchomieniu.

- [ ] Brak błędów krytycznych w logach
- [ ] Uptime 100% przez pierwsze ___ godzin
- [ ] Użytkownicy klienta zalogowali się pomyślnie
- [ ] Brak zgłoszeń od klienta dotyczących problemów

---

## Wynik Go-Live

| | |
|---|---|
| **Status** | ✅ Sukces / ⚠️ Sukces z zastrzeżeniami / ❌ Rollback |
| **Czas uruchomienia** | ___:___ |
| **Czas go-live (od startu do weryfikacji)** | ___ minut |
| **Problemy napotkane** | |
| **Notatki** | |

---

*Checklista wypełniona przez:* _______________  
*Data i godzina zakończenia:* _______________
