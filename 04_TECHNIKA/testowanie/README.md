# Strategia Testowania — {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________

## Podejście

```
[Opisz filozofię testowania w projekcie — np. "Priorytetem są testy integracyjne i e2e
krytycznych ścieżek biznesowych. Unit testy piszemy tylko dla logiki domenowej."]
```

---

## Piramida Testów

| Poziom | Narzędzie | Pokrycie celu | Czas uruchomienia |
|--------|-----------|---------------|-------------------|
| Unit | _______________ | ___% | < ___ s |
| Integracyjne | _______________ | — | < ___ s |
| E2E | _______________ | Krytyczne ścieżki | < ___ min |
| Manualne | — | Testy akceptacyjne | — |

---

## Uruchomienie Testów

```bash
# Wszystkie testy
npm run test

# Unit testy z coverage
npm run test:coverage

# Testy E2E (wymaga działającego środowiska)
npm run test:e2e

# Watch mode (deweloperski)
npm run test:watch
```

---

## Testy Jednostkowe (Unit)

**Co testujemy:** logika biznesowa, walidatory, transformacje danych, helpery.  
**Czego NIE testujemy unit-testami:** komponenty UI, zapytania do bazy, integracje zewnętrzne.

**Lokalizacja:** `src/**/__tests__/*.test.ts` lub `src/**/*.spec.ts`

**Konwencja nazewnictwa:**
```
opisywana_funkcja.test.ts
```

---

## Testy Integracyjne

**Co testujemy:** endpointy API, reguły bezpieczeństwa bazy, integracje z zewnętrznymi serwisami (z mockami).

**Lokalizacja:** `tests/integration/`

**Środowisko:** _______________

---

## Testy E2E

**Co testujemy:** krytyczne ścieżki użytkownika (happy path + najważniejsze edge cases).

**Krytyczne ścieżki do pokrycia:**

| # | Ścieżka | Priorytet |
|---|---------|-----------|
| 1 | Rejestracja / Logowanie | 🔴 Krytyczny |
| 2 | _______________ | 🔴 Krytyczny |
| 3 | _______________ | 🟡 Ważny |
| 4 | _______________ | 🟡 Ważny |
| 5 | _______________ | 🟢 Nice-to-have |

**Lokalizacja:** `tests/e2e/`

---

## Testy Akceptacyjne (UAT)

Testy wykonywane przez Zamawiającego na środowisku stagingowym przed odbiorem.

### Checklista UAT

| # | Scenariusz | Wykonuje | Wynik |
|---|------------|----------|-------|
| 1 | Zaloguj się jako _______________ | {{KLIENT_KONTAKT}} | ⬜ |
| 2 | _______________ | | ⬜ |
| 3 | _______________ | | ⬜ |
| 4 | _______________ | | ⬜ |
| 5 | _______________ | | ⬜ |

**Zgłaszanie błędów UAT:** _______________ (kanał/narzędzie)

---

## CI/CD — Kiedy Uruchamiają się Testy

| Zdarzenie | Testy |
|-----------|-------|
| Pull Request (każdy) | Unit + Integracyjne |
| Merge do `main` / `develop` | Unit + Integracyjne + E2E |
| Deploy na produkcję | Smoke test |

---

## Dane Testowe

**Jak generować:** _______________  
**Seed skrypt:** `npm run seed:test`  
**Reset środowiska testowego:** `npm run reset:test`

**Konta testowe:**

| Rola | Login | Hasło |
|------|-------|-------|
| Admin | test-admin@___ | *** (patrz secrets) |
| Użytkownik | test-user@___ | *** |

---

## Definicja "Gotowe" (Definition of Done)

Funkcja / feature jest gotowy gdy:

- [ ] Kod przeszedł code review
- [ ] Testy jednostkowe napisane i przechodzą
- [ ] Testy integracyjne przechodzą
- [ ] Przetestowano manualnie na stagingu
- [ ] Brak regresji w istniejących testach E2E
- [ ] Dokumentacja zaktualizowana (jeśli dotyczy)
