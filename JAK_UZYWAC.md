# Jak korzystać z dokumentacji projektu

## Kiedy sięgam po który dokument?

---

## 1. Nowy klient pyta "co potrzebujesz?"

👉 Otwórz: `01_SPRZEDAZ/BRIEF_PROJEKTOWY.md`

Wyślij klientowi lub skopiuj do Google Docs. Wypełniacie razem na 1. spotkaniu. To podstawa wyceny i umowy.

---

## 2. Przygotowuję ofertę

👉 Kolejność:

1. `01_SPRZEDAZ/BRIEF_PROJEKTOWY.md` — zbierz wymagania
2. `06_WEWNETRZNE/ARKUSZ_NEGOCJACYJNY.md` — wyceń wewnętrznie
3. `01_SPRZEDAZ/OFERTA.md` — przygotuj ofertę dla klienta
4. `02_KONTRAKT/NDA.md` — podpisz przed ujawnieniem szczegółów (opcjonalne)
5. `02_KONTRAKT/LIST_INTENCYJNY.md` — wyraź wolę współpracy (opcjonalne)

---

## 3. Podpisuję umowę

👉 Dokumenty do przygotowania:

1. `02_KONTRAKT/UMOWA_WDROZENIOWA.md` — główna umowa
2. `02_KONTRAKT/ZALACZNIK_1_SPECYFIKACJA.md` — zakres i kryteria odbioru
3. `02_KONTRAKT/ZALACZNIK_2_RODO.md` — zawsze przy przetwarzaniu danych osobowych
4. `02_KONTRAKT/ZALACZNIK_4_PODZIA_PRAW.md` — tylko jeśli wybrano Wariant C własności kodu
5. `06_WEWNETRZNE/HARMONOGRAM_PLATNOSCI.md` — przygotuj wewnętrzny harmonogram fakturowania

---

## 4. Zaczynam projekt (Kickoff)

👉 Kolejność działania:

1. `03_PROJEKT/KICKOFF.md` — przeprowadź spotkanie inauguracyjne
2. `02_KONTRAKT/ZALACZNIK_1_SPECYFIKACJA.md` — potwierdź zakres z klientem
3. `03_PROJEKT/ROADMAP.md` — zaplanuj co robimy najpierw
4. `04_TECHNIKA/architektura/README.md` — zapisz stack i uzasadnienie
5. `04_TECHNIKA/sekrety/README.md` — zaplanuj jakie klucze będą potrzebne
6. `04_TECHNIKA/uruchomienie/README.md` — opisz jak uruchomić projekt lokalnie
7. `01_SPRZEDAZ/BRIEF_GRAFICZNY.md` — wypełnij jeśli projekt obejmuje UI design

---

## 5. Pracuję nad projektem (codziennie)

👉 Narzędzia na co dzień:

- `03_PROJEKT/ROADMAP.md` — aktualizuj codziennie
- `03_PROJEKT/RAPORT_TYGODNIOWY.md` — wysyłaj co tydzień do klienta
- `03_PROJEKT/PROTOKOL_SPOTKANIA.md` — wypełniaj po każdym spotkaniu
- `04_TECHNIKA/decyzje/` — pisz ADR przy każdej ważnej decyzji technicznej

---

## 6. Wybieram technologię

👉 Otwórz: `04_TECHNIKA/decyzje/`

Stwórz nowy plik: `ADR-XXX-nazwa-decyzji.md`. Skopiuj szablon z `ADR-001-stack.md`.

**Kiedy pisać ADR:**
- Wybór bazy danych / frameworka
- Zmiana architektury
- Każda decyzja o której za miesiąc zapytasz "dlaczego tak?"

---

## 7. Wracam po przerwie

👉 Kolejność czytania:

1. `README.md` — o co chodzi w projekcie
2. `03_PROJEKT/ROADMAP.md` — gdzie skończyłem
3. `04_TECHNIKA/decyzje/README.md` — jakie decyzje podjąłem
4. `04_TECHNIKA/uruchomienie/README.md` — jak uruchomić
5. `04_TECHNIKA/ONBOARDING_DEWELOPERA.md` — jeśli wraca ktoś nowy

---

## 8. Klient prosi o zmianę zakresu

👉 Działaj tak:

1. Oceń wpływ na harmonogram i budżet
2. Wypełnij `03_PROJEKT/CHANGE_REQUEST.md`
3. Powiedz klientowi: **"Złota zasada — to wymaga Change Request"**
4. Zaktualizuj ADR jeśli zmiana dotyczy architektury

---

## 9. Zatrudniam podwykonawcę

👉 Dokumenty:

1. `06_WEWNETRZNE/UMOWA_PODWYKONAWCA.md` — kontrakt B2B
2. `04_TECHNIKA/ONBOARDING_DEWELOPERA.md` — wdrożenie w projekt

---

## 10. Wdrażam projekt na produkcję (Go-Live)

👉 Kolejność:

1. `04_TECHNIKA/bezpieczenstwo/CHECKLIST.md` — sprawdź bezpieczeństwo
2. `04_TECHNIKA/wdrozenie/README.md` — wykonaj deploy zgodnie z instrukcją
3. `05_PRZEKAZANIE/CHECKLIST_GO_LIVE.md` — wypełniaj punkt po punkcie

---

## 11. Przekazuję projekt klientowi

👉 Dokumenty:

1. `02_KONTRAKT/ZALACZNIK_3_PROTOKOL_ODBIORU.md` — do podpisania
2. `05_PRZEKAZANIE/RAPORT_KONCOWY.md` — podsumowanie dla klienta
3. `05_PRZEKAZANIE/PLAN_SZKOLEN.md` — przeprowadź szkolenia
4. `05_PRZEKAZANIE/DOKUMENTACJA_UZYTKOWNIKA.md` — dostarcz instrukcję

---

## 12. Kończę etap / sprint

👉 Działaj tak:

1. Zaktualizuj `03_PROJEKT/ROADMAP.md` — przesuń do ✅
2. `git commit -m "feat: co zrobiłem"`
3. `git push`

---

## 13. Projekt zakończony — wyciągam wnioski

👉 Otwórz: `06_WEWNETRZNE/POSTMORTEM.md`

Wypełnij szczerze. Zaktualizuj szablony w `_SZABLONY` jeśli czegoś brakowało.

---

## Złota zasada dokumentacji

> Pisz dla siebie za 6 miesięcy. Wyobraź sobie że wracasz po pół roku przerwy. Czy rozumiesz? Jeśli tak — jest dobrze.
