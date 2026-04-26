# Runbook — Instrukcja Uruchomienia {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________

## Wymagania wstępne

| Narzędzie | Wersja | Instalacja |
|-----------|--------|------------|
| Node.js | | |
| npm / yarn / pnpm | | |
| [inne] | | |

## Pierwsze uruchomienie

```bash
# 1. Klonowanie
git clone {{GITHUB_REPO}}
cd {{NAZWA_PROJEKTU}}

# 2. Zależności
npm install

# 3. Zmienne środowiskowe
cp .env.example .env.local
# Uzupełnij .env.local (patrz docs/secrets/README.md)

# 4. Start
npm run dev
```

## Zmienne środowiskowe

Skopiuj `.env.example` do `.env.local` i uzupełnij:

| Zmienna | Opis | Gdzie znaleźć |
|---------|------|---------------|
| | | |

## Uruchomienie lokalne

```bash
npm run dev        # Serwer deweloperski
npm run build      # Build produkcyjny
npm run test       # Testy
```

## Deploy na produkcję

```bash
# [Opisz proces deployu]
npm run build
# ...
```

**URL produkcji:** {{HOSTING_URL}}

## Przydatne komendy

| Komenda | Co robi |
|---------|---------|
| `npm run dev` | Serwer deweloperski |
| `npm run build` | Build produkcyjny |

## Troubleshooting

_Uzupełniaj na bieżąco gdy napotkasz problemy._

| Problem | Rozwiązanie |
|---------|-------------|
| | |
