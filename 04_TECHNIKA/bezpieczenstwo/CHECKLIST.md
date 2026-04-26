# Checklista Bezpieczeństwa — {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________  
> Sprawdzana przed każdym wdrożeniem produkcyjnym.

---

## 1. Sekrety i Konfiguracja

- [ ] Żadne klucze API ani hasła nie są zahardkodowane w kodzie
- [ ] `.env` i `.env.local` są w `.gitignore`
- [ ] Zmienne środowiskowe produkcyjne przechowywane bezpiecznie (Vault / panel hostingu)
- [ ] Różne klucze API dla środowisk dev / staging / produkcja
- [ ] Klucze serwisowe mają tylko wymagane uprawnienia (zasada minimalnych uprawnień)
- [ ] Plan rotacji kluczy (harmonogram w `docs/secrets/README.md`)

---

## 2. Autoryzacja i Uwierzytelnianie

- [ ] Wszystkie endpointy chronione — brak dostępu bez tokenu / sesji
- [ ] Reguły bezpieczeństwa bazy danych (Firestore Rules / RLS) skonfigurowane i przetestowane
- [ ] Role i uprawnienia działają zgodnie ze specyfikacją (Załącznik nr 1)
- [ ] Tokeny JWT / sesje mają rozsądny czas wygaśnięcia
- [ ] Mechanizm wylogowania (invalidacja tokenów / sesji)
- [ ] Ochrona przed atakami brute-force na logowanie (rate limiting / blokada po X próbach)
- [ ] Weryfikacja e-mail po rejestracji (jeśli dotyczy)

---

## 3. Komunikacja i Dane w Transmisji

- [ ] HTTPS na wszystkich środowiskach (certyfikat SSL ważny i auto-odnawiany)
- [ ] HTTP → HTTPS redirect skonfigurowany
- [ ] Nagłówki bezpieczeństwa ustawione:
  - [ ] `Strict-Transport-Security` (HSTS)
  - [ ] `Content-Security-Policy` (CSP)
  - [ ] `X-Frame-Options: DENY`
  - [ ] `X-Content-Type-Options: nosniff`
  - [ ] `Referrer-Policy`

---

## 4. Walidacja Danych Wejściowych (OWASP Top 10)

- [ ] **Injection (A03):** Wszystkie dane wejściowe walidowane i sanityzowane
- [ ] **XSS (A03):** Dane od użytkownika escapowane przy renderowaniu w HTML
- [ ] **IDOR (A01):** Weryfikacja czy użytkownik ma dostęp do konkretnego zasobu (nie tylko czy jest zalogowany)
- [ ] **Mass Assignment:** Tylko dozwolone pola mogą być ustawiane przez API
- [ ] **File Upload:** Walidacja typu, rozmiaru i zawartości pliku (jeśli dotyczy)
- [ ] **CSRF:** Ochrona przed Cross-Site Request Forgery (tokeny CSRF lub SameSite cookies)

---

## 5. Zależności i Biblioteki

- [ ] `npm audit` (lub ekwiwalent) — brak krytycznych podatności
- [ ] Zależności zaktualizowane do bezpiecznych wersji
- [ ] Brak porzuconych / nieobsługiwanych bibliotek z podatnościami
- [ ] `package-lock.json` / `yarn.lock` w repozytorium (dla reproducible builds)

---

## 6. RODO i Dane Osobowe

- [ ] Zidentyfikowane wszystkie miejsca gdzie przechowywane są dane osobowe
- [ ] Podpisana Umowa Powierzenia Danych (Załącznik nr 2)
- [ ] Dane osobowe szyfrowane w spoczynku (jeśli wymagane)
- [ ] Mechanizm usunięcia danych użytkownika (prawo do bycia zapomnianym)
- [ ] Logi nie zawierają danych osobowych w czystym tekście
- [ ] Dostęp do danych osobowych logowany (audit log)

---

## 7. Backup i Odtwarzanie

- [ ] Automatyczny backup danych co ___ godzin
- [ ] Backup testowany — weryfikacja odtworzenia danych
- [ ] Backup przechowywany w innej lokalizacji niż produkcja
- [ ] Procedura disaster recovery udokumentowana w `docs/runbook/README.md`
- [ ] RTO (Recovery Time Objective): ___ godzin
- [ ] RPO (Recovery Point Objective): ___ godzin

---

## 8. Monitoring i Wykrywanie Incydentów

- [ ] Alerty na błędy 5xx (próg: ___ błędów / minutę)
- [ ] Alert na niedostępność aplikacji (uptime monitoring)
- [ ] Logowanie nieudanych prób logowania
- [ ] Audit log kluczowych operacji (kto co zmienił i kiedy)
- [ ] Plan reagowania na incydent bezpieczeństwa (kontakt: _______________)

---

## 9. Infrastruktura

- [ ] Reguły firewalla — tylko niezbędne porty otwarte
- [ ] Dostęp do panelu admina ograniczony (IP whitelist / VPN)
- [ ] Baza danych niedostępna bezpośrednio z internetu
- [ ] Środowisko produkcyjne odseparowane od dev / staging

---

## Wynik Przeglądu

| Data | Sprawdzający | Wynik | Uwagi |
|------|-------------|-------|-------|
| _______________ | _______________ | ✅ / ⚠️ / ❌ | |

**Otwarte kwestie bezpieczeństwa:**

| # | Problem | Ryzyko | Termin | Status |
|---|---------|--------|--------|--------|
| | | 🔴 Wysokie / 🟡 Średnie / 🟢 Niskie | | ⬜ |
