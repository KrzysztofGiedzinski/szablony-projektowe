# Monitoring i Alerty — {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________

## Narzędzia Monitoringu

| Narzędzie | Cel | URL / Panel |
|-----------|-----|-------------|
| _______________ | Uptime / dostępność | |
| _______________ | Logi aplikacji | |
| _______________ | Metryki wydajności | |
| _______________ | Błędy (error tracking) | |

---

## Co Monitorujemy

### Dostępność (Uptime)

| Endpoint | Oczekiwany status | Częstotliwość sprawdzania |
|----------|-------------------|--------------------------|
| {{HOSTING_URL}} | 200 OK | Co 1 minutę |
| {{HOSTING_URL}}/api/health | 200 OK | Co 1 minutę |
| _______________ | | |

**Cel SLA:** ___% miesięcznie  
**Okno serwisowe (bez alertów):** Niedziela 02:00–04:00

---

### Wydajność

| Metryka | Próg ostrzeżenia | Próg krytyczny |
|---------|-----------------|----------------|
| Czas odpowiedzi API (P95) | > ___ ms | > ___ ms |
| Czas ładowania strony (P95) | > ___ ms | > ___ ms |
| Użycie CPU | > ___% | > ___% |
| Użycie RAM | > ___% | > ___% |
| Rozmiar bazy danych | > ___ GB | > ___ GB |

---

### Błędy Aplikacji

| Metryka | Próg alertu |
|---------|-------------|
| Liczba błędów 5xx / minutę | > ___ |
| Liczba nieudanych logowań / 15 min | > ___ |
| Błędy krytyczne (uncaught exceptions) | Każdy jeden |

---

## Alerty — Kto Reaguje

| Typ alertu | Kanał powiadomienia | Kto reaguje | Czas reakcji |
|------------|---------------------|-------------|--------------|
| Aplikacja niedostępna (downtime) | SMS + E-mail | _______________ | Natychmiast |
| Błąd krytyczny w kodzie | E-mail | _______________ | Do ___ h |
| Przekroczenie progu wydajności | E-mail | _______________ | Do ___ h roboczych |
| Alert bezpieczeństwa | SMS + E-mail | _______________ | Natychmiast |

**Kontakt awaryjny (24/7):** _______________ | _______________

---

## Procedura Reagowania na Incydent

### Aplikacja niedostępna

1. Sprawdź status hostingu / Firebase: _______________
2. Sprawdź logi: _______________
3. Jeśli problem po stronie hostingu — poczekaj na naprawę u dostawcy, poinformuj klienta
4. Jeśli problem po stronie kodu — rollback do poprzedniej wersji:
   ```bash
   # [Opisz komendę rollback]
   ```
5. Poinformuj {{KLIENT_KONTAKT}} o incydencie i czasie rozwiązania

### Błąd Krytyczny

1. Zidentyfikuj źródło w logach
2. Oceń wpływ na użytkowników
3. Jeśli dotyczy danych — sprawdź integralność
4. Napraw i wdróż fix
5. Opisz incydent w `docs/runbook/README.md` w sekcji Troubleshooting

---

## Backup

| Parametr | Wartość |
|----------|---------|
| Częstotliwość backupu | Co ___ godziny |
| Przechowywanie | ___ dni |
| Lokalizacja backupu | _______________ |
| Testowanie odtwarzania | Co ___ miesięcy |

**Jak przywrócić backup:**
```bash
# [Opisz procedurę]
```

---

## Raportowanie Dostępności

Miesięczny raport dostępności jest generowany automatycznie / ręcznie i wysyłany do {{KLIENT_EMAIL}} do ___ dnia każdego miesiąca.

| Miesiąc | Dostępność | Incydenty | Uwagi |
|---------|-----------|-----------|-------|
| | | | |
