# Onboarding Dewelopera — {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________  
> Dla: nowego developera / Ciebie po dłuższej przerwie

---

## Witaj w projekcie

```
[2–3 zdania o projekcie — co to jest, dla kogo, jaki problem rozwiązuje]
```

**Klient:** {{KLIENT_FIRMA}}  
**URL produkcji:** {{HOSTING_URL}}  
**Repozytorium:** {{GITHUB_REPO}}  
**Główny kontakt:** _______________

---

## Krok 1 — Dostępy (poproś Zleceniodawcę)

- [ ] Dostęp do repozytorium GitHub: {{GITHUB_REPO}}
- [ ] Klucze do `.env.local` (patrz `docs/secrets/README.md`)
- [ ] Dostęp do panelu Firebase / hostingu
- [ ] Dostęp do narzędzia do zarządzania zadaniami: _______________
- [ ] Zaproszenie do kanału komunikacyjnego: _______________
- [ ] Dostęp do stagingu: _______________

---

## Krok 2 — Uruchomienie Lokalne

Szczegółowa instrukcja: `docs/runbook/README.md`

```bash
# Szybki start
git clone {{GITHUB_REPO}}
cd {{NAZWA_PROJEKTU}}
cp .env.example .env.local   # Uzupełnij kluczami od Zleceniodawcy
npm install
npm run dev
```

**Sprawdź że działa:** otwórz http://localhost:3000 — powinna pojawić się strona logowania.

---

## Krok 3 — Zrozum Projekt

Czytaj w tej kolejności:

1. Ten dokument (jesteś tutaj)
2. `docs/architecture/README.md` — stack, diagram systemu, dlaczego takie decyzje
3. `docs/decisions/README.md` — indeks ADR, kluczowe wybory projektowe
4. `docs/data/README.md` — model danych, reguły biznesowe
5. `ROADMAP.md` — aktualny stan i priorytety

**Czas na wdrożenie:** ok. ___ godzin zanim zaczniesz produktywnie pracować.

---

## Krok 4 — Workflow Git

```
main / master     ← tylko przez PR, nigdy bezpośrednio
  └── develop     ← integracyjna, CI deploy na staging
        └── feature/nazwa-zadania   ← tu pracujesz
        └── fix/nazwa-buga
        └── chore/nazwa-zadania
```

### Jak tworzyć PR

1. Utwórz gałąź od `develop`: `git checkout -b feature/moja-funkcja`
2. Zrób zmiany, commituj małymi krokami
3. Otwórz PR do `develop`
4. Czekaj na code review od: _______________
5. Po zatwierdzeniu merge — CI deployuje na staging

**Konwencja commitów:**
```
feat: dodaj moduł X
fix: napraw błąd w Y
chore: zaktualizuj zależności
docs: zaktualizuj README
refactor: przepisz logikę Z
test: dodaj testy dla W
```

---

## Krok 5 — Zasady Pracy

### Kodowanie

- Stack: `docs/architecture/README.md`
- Formatowanie: _______________ (Prettier / ESLint — reguły w `.prettierrc` / `.eslintrc`)
- Języki: TypeScript / JavaScript / _______________
- Testy: `docs/testing/README.md` — pisz testy dla nowych funkcji
- Komentarze w kodzie: _______________ (po polsku / po angielsku)

### Co robić gdy...

| Sytuacja | Co robić |
|----------|----------|
| Nie rozumiesz wymagania | Zapytaj _______________ przed implementacją |
| Znalazłeś buga | Sprawdź czy jest w backlogu, jeśli nie — otwórz issue |
| Chcesz zmienić architekturę | Najpierw ADR, potem implementacja |
| Coś blokuje Twoją pracę | Zgłoś od razu, nie czekaj do końca dnia |
| Skończyłeś zadanie | Zaktualizuj `ROADMAP.md`, otwórz PR |

---

## Krok 6 — Komunikacja

| Kanał | Do czego | Kto |
|-------|----------|-----|
| _______________ | Bieżące pytania, blokery | Wszyscy |
| E-mail | Formalne ustalenia | Zewnętrzni |
| _______________ | Zarządzanie zadaniami | Wszyscy |
| Spotkania video | Code review, demo | Co ___ tygodni |

**Daily standup:** _______________ (czy jest / kiedy / gdzie)  
**Code review:** PR otwierasz → ktoś reviewuje w ciągu ___ godzin roboczych

---

## Środowiska i Deploymenty

Szczegóły: `docs/deployment/README.md`

| Środowisko | URL | Kto deployuje |
|------------|-----|---------------|
| Lokalne | http://localhost:3000 | Ty |
| Staging | _______________ | CI automatycznie (po merge do `develop`) |
| Produkcja | {{HOSTING_URL}} | _______________ (ręcznie / CI z zatwierdzeniem) |

---

## Najczęstsze Pytania

**P: Gdzie znajdę klucze API?**  
O: Poproś _______________ o `.env.local`. Nie ma ich w repozytorium.

**P: Jak wdrożyć zmiany na staging?**  
O: Merge do `develop` — CI zrobi to automatycznie.

**P: Jak zgłosić błąd produkcyjny?**  
O: Najpierw zadzwoń / napisz na _______________, potem otwórz issue.

**P: Czy mogę commitować bezpośrednio do `main`?**  
O: Nie. Zawsze przez PR z code review.

**P: Co jeśli zepsuję coś na stagingu?**  
O: Staging jest po to żeby psuć — poinformuj zespół i napraw.

---

## Kluczowe Kontakty

| Rola | Osoba | Kontakt |
|------|-------|---------|
| Zleceniodawca / Lead | _______________ | _______________ |
| Point of Contact (Klient) | {{KLIENT_KONTAKT}} | {{KLIENT_EMAIL}} |
| Pilne / Awaryjne | _______________ | _______________ |

---

*Coś niejasne? Zaktualizuj ten dokument po wdrożeniu — dla następnej osoby.*
