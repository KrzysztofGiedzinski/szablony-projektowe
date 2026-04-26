# Deployment — {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________

## Środowiska

| Środowisko | URL | Gałąź git | Kto deployuje | Kiedy |
|------------|-----|-----------|---------------|-------|
| Lokalne | http://localhost:3000 | dowolna | Developer | Na żądanie |
| Staging | _______________ | `develop` | Automatycznie (CI) | Po merge do `develop` |
| Produkcja | {{HOSTING_URL}} | `main` / `master` | Ręcznie lub CI | Po zatwierdzeniu |

---

## Pipeline CI/CD

**Narzędzie:** _______________  (GitHub Actions / GitLab CI / inne)  
**Plik konfiguracyjny:** `.github/workflows/deploy.yml` / _______________

### Automatyczny pipeline (staging)

```
Push do `develop`
  → Testy jednostkowe
  → Testy integracyjne
  → Build
  → Deploy na staging
  → Smoke test
  → Powiadomienie na _______________
```

### Ręczny deploy (produkcja)

```
Merge do `main`
  → Testy jednostkowe + integracyjne (wymagane przejście)
  → Code review (wymagane)
  → Ręczne zatwierdzenie deploy'u przez: _______________
  → Build produkcyjny
  → Deploy na produkcję
  → Smoke test
  → Powiadomienie na _______________
```

---

## Deploy Ręczny (Bez CI)

```bash
# 1. Upewnij się że jesteś na właściwej gałęzi
git checkout main
git pull origin main

# 2. Zainstaluj zależności
npm ci

# 3. Uruchom testy
npm run test

# 4. Zbuduj aplikację
npm run build

# 5. Wdróż
# [Opisz konkretną komendę — np. firebase deploy / vercel deploy / etc.]
```

---

## Zmienne Środowiskowe

Zmienne produkcyjne przechowywane w: _______________

Przed deployem na produkcję sprawdź czy wszystkie zmienne są ustawione:

```bash
# Sprawdź zmienne (przykład dla Vercel)
vercel env ls production

# Sprawdź zmienne (przykład dla Firebase)
firebase functions:config:get
```

Pełna lista zmiennych: `docs/secrets/README.md`

---

## Rollback

### Szybki rollback (ostatnia wersja)

```bash
# GitHub Actions — reruruchom poprzedni udany workflow
# lub:

git revert HEAD
git push origin main
# CI automatycznie wdroży poprzednią wersję
```

### Rollback do konkretnej wersji

```bash
git log --oneline -10   # Znajdź hash commita
git checkout <hash>
git push origin main --force  # UWAGA: tylko w nagłym przypadku!
```

> **Zawsze** poinformuj {{KLIENT_KONTAKT}} o rollbacku i przyczynie.

---

## Checklista Przed Deployem na Produkcję

- [ ] Kod przeszedł code review
- [ ] Wszystkie testy przechodzą (CI zielone)
- [ ] Changelog zaktualizowany
- [ ] Staging przetestowany i zaakceptowany
- [ ] Backup danych wykonany (dla deployów z migracją danych)
- [ ] Okno deploymentu uzgodnione z klientem (jeśli wrażliwy czas)
- [ ] Plan rollbacku gotowy
- [ ] Monitoring aktywny

---

## Migracje Bazy Danych

> Opisz procedurę migracji danych przy nowych wersjach.

```bash
# Uruchomienie migracji
npm run migrate

# Sprawdzenie stanu migracji
npm run migrate:status

# Cofnięcie ostatniej migracji (rollback)
npm run migrate:rollback
```

**Zasada:** Migracje muszą być **backwards-compatible** — stara wersja kodu musi działać z nową strukturą danych przez minimum ___ godzin.

---

## Historia Deployów

| Data | Wersja | Co zmieniono | Kto | Status |
|------|--------|-------------|-----|--------|
| _______________ | v1.0.0 | Pierwsze wdrożenie | _______________ | ✅ |
| _______________ | | | | |
