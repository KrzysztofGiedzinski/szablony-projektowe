# Jak korzystać z dokumentacji projektu

## Kiedy sięgam po który dokument?

---

## 1. Nowy klient pyta "co potrzebujesz?"

👉 Otwórz: `BRIEF_PROJEKTOWY.md`

Wyślij klientowi lub skopiuj do Google Docs. Wypełniacie razem na 1. spotkaniu. To podstawa wyceny i umowy.

---

## 2. Zaczynam nowy projekt

👉 Kolejność działania:

1. Wypełnij Brief z klientem
2. Uzupełnij `README.md` — nazwa, opis, status
3. Uzupełnij `ROADMAP.md` — co robimy najpierw
4. Uzupełnij `docs/architecture/README.md` — stack i dlaczego
5. Uzupełnij `docs/secrets/README.md` — jakie klucze będą potrzebne
6. Uzupełnij `docs/runbook/README.md` — jak uruchomić projekt lokalnie

---

## 3. Wybieram technologię

👉 Otwórz: `docs/decisions/`

Stwórz nowy plik: `ADR-XXX-nazwa-decyzji.md`. Skopiuj szablon z `ADR-001-stack.md`.

**Kiedy pisać ADR:**
- Wybór bazy danych / frameworka
- Zmiana architektury
- Każda decyzja o której za miesiąc zapytasz "dlaczego tak?"

---

## 4. Wracam po przerwie

👉 Kolejność czytania:

1. `README.md` — o co chodzi
2. `ROADMAP.md` — gdzie skończyłem
3. `docs/decisions/README.md` — jakie decyzje podjąłem
4. `docs/runbook/README.md` — jak uruchomić

---

## 5. Kończę etap / sprint

👉 Działaj tak:

1. Zaktualizuj `ROADMAP.md` — przesuń do ✅
2. `git commit -m "feat: co zrobiłem"`
3. `git push`

---

## 6. Klient prosi o zmianę zakresu

👉 Działaj tak:

1. Oceń wpływ na harmonogram i budżet
2. Zapisz w `ROADMAP.md`
3. Powiedz klientowi: **"Złota zasada — to wymaga Change Request"**
4. Zaktualizuj ADR jeśli zmiana dotyczy architektury

---

## Złota zasada dokumentacji

> Pisz dla siebie za 6 miesięcy. Wyobraź sobie że wracasz po pół roku przerwy. Czy rozumiesz? Jeśli tak — jest dobrze.
