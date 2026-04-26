# Dokumentacja API — {{NAZWA_PROJEKTU}}
> Ostatnia aktualizacja: _______________

## Informacje Ogólne

| Parametr | Wartość |
|----------|---------|
| Base URL (produkcja) | {{HOSTING_URL}}/api |
| Base URL (staging) | _______________ |
| Wersja API | v1 |
| Format | JSON |
| Autoryzacja | Bearer Token (JWT) / Firebase Auth |

---

## Autoryzacja

```
Authorization: Bearer <token>
```

Tokeny uzyskiwane przez: _______________  
Czas życia tokenu: ___  
Odświeżanie: _______________

---

## Konwencje

- Daty: ISO 8601 (`2026-04-26T10:00:00Z`)
- ID zasobów: _______________
- Paginacja: `?page=1&limit=20`
- Kody błędów: standardowe HTTP + `{ "error": "kod", "message": "opis" }`

---

## Endpointy

### Moduł: _______________

#### `GET /api/v1/_______________`

Opis: _______________

**Query params:**

| Parametr | Typ | Wymagany | Opis |
|----------|-----|----------|------|
| | | | |

**Odpowiedź 200:**
```json
{
  "data": [],
  "total": 0,
  "page": 1
}
```

---

#### `POST /api/v1/_______________`

Opis: _______________

**Body:**
```json
{
  "field": "value"
}
```

**Odpowiedź 201:**
```json
{
  "id": "abc123",
  "createdAt": "2026-04-26T10:00:00Z"
}
```

---

#### `PUT /api/v1/_______________/:id`

Opis: _______________

**Body:**
```json
{
  "field": "new_value"
}
```

**Odpowiedź 200:**
```json
{
  "id": "abc123",
  "updatedAt": "2026-04-26T10:00:00Z"
}
```

---

#### `DELETE /api/v1/_______________/:id`

Opis: _______________

**Odpowiedź 204:** (brak body)

---

### Moduł: _______________

> Skopiuj sekcję powyżej i uzupełnij dla każdego modułu.

---

## Kody Błędów

| Kod HTTP | Kod błędu | Opis |
|----------|-----------|------|
| 400 | `VALIDATION_ERROR` | Nieprawidłowe dane wejściowe |
| 401 | `UNAUTHORIZED` | Brak lub nieprawidłowy token |
| 403 | `FORBIDDEN` | Brak uprawnień do zasobu |
| 404 | `NOT_FOUND` | Zasób nie istnieje |
| 409 | `CONFLICT` | Konflikt (np. duplikat) |
| 500 | `SERVER_ERROR` | Błąd serwera |

---

## Przykłady (curl)

```bash
# Pobierz listę
curl -H "Authorization: Bearer TOKEN" \
  {{HOSTING_URL}}/api/v1/___

# Utwórz zasób
curl -X POST \
  -H "Authorization: Bearer TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"field": "value"}' \
  {{HOSTING_URL}}/api/v1/___
```

---

## Webhooks (jeśli dotyczy)

| Zdarzenie | URL | Opis |
|-----------|-----|------|
| | | |

---

## Limity (Rate Limiting)

| Endpoint | Limit | Okno |
|----------|-------|------|
| Ogólny | ___ req | 1 minuta |
| Auth | ___ req | 15 minut |
