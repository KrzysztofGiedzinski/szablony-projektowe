# Szablony Projektowe — Krzysztof Giedziński

Zestaw sprawdzonych szablonów dokumentacji do projektów webowych i mobilnych (B2B/SaaS).

## Jak używać

1. Skopiuj cały folder do nowego projektu
2. Przeszukaj i zamień placeholdery `{{...}}` właściwymi wartościami
3. Usuń sekcje które nie dotyczą projektu
4. Uzupełniaj na bieżąco zgodnie z `JAK_UZYWAC.md`

## Główne placeholdery

| Placeholder | Znaczenie |
|-------------|-----------|
| `{{NAZWA_PROJEKTU}}` | Nazwa systemu/aplikacji |
| `{{OPIS_PROJEKTU}}` | Krótki opis w 1-2 zdaniach |
| `{{KLIENT_FIRMA}}` | Pełna nazwa firmy klienta |
| `{{KLIENT_NIP}}` | NIP klienta |
| `{{KLIENT_ADRES}}` | Adres siedziby klienta |
| `{{KLIENT_KONTAKT}}` | Imię i nazwisko osoby kontaktowej |
| `{{KLIENT_STANOWISKO}}` | Stanowisko osoby kontaktowej |
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

## Struktura

```
_SZABLONY/
├── README.md                              ← Jesteś tutaj
├── JAK_UZYWAC.md                          ← Kiedy sięgasz po który dokument
│
├── 01_SPRZEDAZ/                           ← Zanim podpiszesz umowę
│   ├── OFERTA.md                          ← Szablon oferty handlowej
│   ├── BRIEF_PROJEKTOWY.md                ← Formularz do wypełnienia z klientem
│   └── BRIEF_GRAFICZNY.md                 ← Brief dla designera / studia graficznego
│
├── 02_KONTRAKT/                           ← Dokumenty prawne z klientem
│   ├── NDA.md                             ← Umowa o poufności
│   ├── LIST_INTENCYJNY.md                 ← List intencyjny (przed umową)
│   ├── UMOWA_WDROZENIOWA.md               ← Umowa IT: wdrożenie + abonament
│   ├── ZALACZNIK_1_SPECYFIKACJA.md        ← Zakres, funkcje, kryteria odbioru
│   ├── ZALACZNIK_2_RODO.md                ← Umowa powierzenia danych (art. 28 RODO)
│   ├── ZALACZNIK_3_PROTOKOL_ODBIORU.md    ← Podpisywany przy każdym odbiorze
│   ├── ZALACZNIK_4_PODZIA_PRAW.md         ← Podział praw autorskich (Wariant C)
│   ├── REGULAMIN.md                       ← Regulamin korzystania z systemu
│   ├── POLITYKA_PRYWATNOSCI.md            ← Polityka prywatności RODO
│   └── WLASNOSC_KODU_PRAWO_PL.md         ← Opracowanie prawne własności kodu
│
├── 03_PROJEKT/                            ← Zarządzanie projektem na co dzień
│   ├── KICKOFF.md                         ← Agenda kickoffu + checklista startu
│   ├── ROADMAP.md                         ← Stan i plan projektu
│   ├── RAPORT_TYGODNIOWY.md               ← Cotygodniowy raport postępów dla klienta
│   ├── PROTOKOL_SPOTKANIA.md              ← Notatka z każdego spotkania
│   └── CHANGE_REQUEST.md                  ← Formularz zmiany zakresu z wyceną
│
├── 04_TECHNIKA/                           ← Dokumentacja techniczna dla developera
│   ├── ONBOARDING_DEWELOPERA.md           ← Jak nowy developer wchodzi w projekt
│   ├── architektura/README.md             ← Stack, diagram systemu, środowiska
│   ├── api/README.md                      ← Dokumentacja endpointów API
│   ├── dane/README.md                     ← Model danych, schematy, reguły biznesowe
│   ├── decyzje/                           ← ADR — dziennik decyzji architektonicznych
│   │   ├── README.md                      ← Indeks wszystkich ADR
│   │   └── ADR-001-stack.md               ← Szablon decyzji
│   ├── uruchomienie/README.md             ← Jak uruchomić projekt lokalnie
│   ├── sekrety/README.md                  ← Mapa sekretów i dostępów (bez wartości!)
│   ├── testowanie/README.md               ← Strategia testowania, UAT, DoD
│   ├── bezpieczenstwo/CHECKLIST.md        ← Checklista OWASP + RODO
│   ├── monitoring/README.md               ← Alerty, uptime, procedura incydentów
│   └── wdrozenie/README.md                ← CI/CD, pipeline, rollback
│
├── 05_PRZEKAZANIE/                        ← Odbiór i zamknięcie projektu
│   ├── CHECKLIST_GO_LIVE.md               ← Checklista na dzień uruchomienia
│   ├── RAPORT_KONCOWY.md                  ← Raport końcowy dla klienta
│   ├── DOKUMENTACJA_UZYTKOWNIKA.md        ← Instrukcja obsługi per rola
│   └── PLAN_SZKOLEN.md                    ← Plan i harmonogram szkoleń
│
└── 06_WEWNETRZNE/                         ← Tylko dla Ciebie — nie pokazuj klientowi
    ├── ARKUSZ_NEGOCJACYJNY.md             ← Kalkulacja i argumenty negocjacyjne
    ├── HARMONOGRAM_PLATNOSCI.md           ← Tabela transz i abonamentów
    ├── UMOWA_PODWYKONAWCA.md              ← Kontrakt B2B z podwykonawcą
    └── POSTMORTEM.md                      ← Analiza projektu po zakończeniu
```

---
*Szablony opracowane na podstawie projektu BUILD-TRACK (2026). Aktualizowane po konsultacjach z prawnikami i praktyką projektową.*
