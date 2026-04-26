# Mapa Sekretów i Dostępów — {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________

⚠️ **Ten plik NIE zawiera wartości sekretów — tylko informacje gdzie je znaleźć.**

## Rejestr sekretów

| Sekret | Plik | Gdzie znaleźć | Status |
|--------|------|---------------|--------|
| | `.env.local` | | ⬜ |
| | `.env.local` | | ⬜ |

## Integracje zewnętrzne

| Serwis | Cel | Status |
|--------|-----|--------|
| | | ⬜ Planowane |

## Procedura rotacji kluczy

1. Wygeneruj nowy klucz w panelu serwisu
2. Zaktualizuj `.env.local`
3. Zaktualizuj zmienne na serwerze produkcyjnym
4. Przetestuj aplikację
5. Usuń stary klucz

## Checklista bezpieczeństwa

- [ ] `.env.local` w `.gitignore`
- [ ] Klucze serwisowe w `.gitignore`
- [ ] Reguły bezpieczeństwa bazy danych skonfigurowane
- [ ] Backup sekretów w bezpiecznym miejscu (menadżer haseł)
- [ ] Rotacja kluczy co 6 miesięcy w kalendarzu
