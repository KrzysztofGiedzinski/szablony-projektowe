# Szablony Projektowe — Krzysztof Giedziński

Zestaw sprawdzonych szablonów dokumentacji do projektów webowych i mobilnych (B2B/SaaS).

## Jak używać

1. Skopiuj cały folder do nowego projektu
2. Przeszukaj i zamień placeholdery `{{...}}` właściwymi wartościami
3. Usuń sekcje które nie dotyczą projektu
4. Uzupełniaj na bieżąco zgodnie z `docs/JAK_UZYWAC.md`

## Główne placeholdery

| Placeholder | Znaczenie |
|-------------|-----------|
| `{{NAZWA_PROJEKTU}}` | Nazwa systemu/aplikacji |
| `{{OPIS_PROJEKTU}}` | Krótki opis w 1-2 zdaniach |
| `{{KLIENT_FIRMA}}` | Pełna nazwa firmy klienta |
| `{{KLIENT_NIP}}` | NIP klienta |
| `{{KLIENT_ADRES}}` | Adres siedziby klienta |
| `{{KLIENT_KONTAKT}}` | Imię i nazwisko osoby kontaktowej |
| `{{KLIENT_EMAIL}}` | E-mail klienta |
| `{{KLIENT_TEL}}` | Telefon klienta |
| `{{WYKONAWCA_FIRMA}}` | Twoja firma / imię i nazwisko |
| `{{WYKONAWCA_NIP}}` | Twój NIP |
| `{{WYKONAWCA_EMAIL}}` | Twój e-mail |
| `{{WYKONAWCA_TEL}}` | Twój telefon |
| `{{DATA_UMOWY}}` | Data zawarcia umowy |
| `{{NUMER_UMOWY}}` | Numer umowy (np. PT/001/2026) |
| `{{KWOTA_WDROZENIE}}` | Opłata wdrożeniowa netto |
| `{{KWOTA_ABONAMENT}}` | Abonament miesięczny netto |
| `{{HOSTING_URL}}` | URL produkcyjny aplikacji |
| `{{GITHUB_REPO}}` | Link do repozytorium GitHub |

## Zawartość

```
_SZABLONY/
├── BRIEF_PROJEKTOWY.md         ← Wypełniasz z klientem na 1. spotkaniu
├── ROADMAP.md                  ← Stan i plan projektu
├── docs/
│   ├── JAK_UZYWAC.md           ← Meta-instrukcja
│   ├── architecture/README.md  ← Stack i architektura
│   ├── data/README.md          ← Model danych
│   ├── decisions/              ← ADR — dziennik decyzji
│   ├── runbook/README.md       ← Jak uruchomić projekt
│   └── secrets/README.md       ← Mapa sekretów i dostępów
└── prawne/
    ├── LIST_INTENCYJNY.md
    ├── UMOWA_WDROZENIOWA.md    ← Umowa IT: wdrożenie + abonament
    ├── ZALACZNIK_2_RODO.md     ← Umowa powierzenia danych (art. 28 RODO)
    ├── ARKUSZ_NEGOCJACYJNY.md  ← Wewnętrzna kalkulacja (nie dla klienta!)
    └── WLASNOSC_KODU.md        ← Opracowanie prawne własności kodu
```

---
*Szablony opracowane na podstawie projektu BUILD-TRACK (2026). Aktualizowane po konsultacjach z prawnikami i praktyką projektową.*
