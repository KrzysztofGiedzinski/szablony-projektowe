# Obsługa Błędów i System Zgłaszania — {{NAZWA_PROJEKTU}}

> Szablon oparty na implementacji w projekcie Klimatyzatron (2026-05-10).  
> Każda aplikacja trafiająca do klienta **musi** mieć ten system przed wdrożeniem.  
> Bez tego klient widzi biały ekran i dzwoni z pretensjami zamiast wysłać logi.

---

## Filozofia

Klient nie jest developerem. Gdy coś się posypie, potrzebuje:
1. Czytelnego komunikatu (nie białego ekranu)
2. Jasnej instrukcji co zrobić (3 kroki, nie więcej)
3. Jednego kliknięcia by do Ciebie napisać — z gotowymi danymi diagnostycznymi

---

## Krok 1 — Strony błędów Next.js (~30 minut, zero zależności)

Utwórz cztery pliki. Każdy musi być `"use client"` (wymóg Next.js).

### Pliki do stworzenia

| Plik | Kiedy działa |
|------|-------------|
| `src/app/error.tsx` | Błąd runtime w dowolnej trasie aplikacji |
| `src/app/global-error.tsx` | Błąd krytyczny w root layout (ostatnia linia obrony) |
| `src/app/not-found.tsx` | Adres URL nie istnieje (404) |
| `src/app/[panel]/error.tsx` | Błąd w konkretnym panelu (np. installer, dashboard) |

### Wzorzec — error.tsx

```tsx
"use client";
import { useEffect } from "react";

export default function Error({
  error,
  reset,
}: {
  error: Error & { digest?: string };
  reset: () => void;
}) {
  useEffect(() => { console.error(error); }, [error]);

  function buildMailto() {
    const subject = encodeURIComponent(`Błąd — ${typeof window !== "undefined" ? window.location.pathname : ""}`);
    const body = encodeURIComponent(
      `Proszę nie usuwać poniższych danych — pomagają w diagnozie.\n\n` +
      `Data: ${new Date().toLocaleString("pl-PL")}\n` +
      `URL: ${typeof window !== "undefined" ? window.location.href : ""}\n` +
      `Kod błędu: ${error.digest ?? "brak"}\n` +
      `Opis: ${error.message ?? "brak"}\n` +
      `Przeglądarka: ${typeof navigator !== "undefined" ? navigator.userAgent : ""}\n\n` +
      `--- Co robiłem/am przed błędem ---\n`
    );
    return `mailto:{{KONTAKT_EMAIL}}?subject=${subject}&body=${body}`;
  }

  return (
    <div className="min-h-screen flex items-center justify-center px-4 bg-gray-100">
      <div className="w-full max-w-sm">
        {/* ikona błędu + tytuł */}
        <div className="bg-white rounded-2xl border border-gray-200 p-6 space-y-5">

          {/* Ścieżka działania — ZAWSZE 3 kroki */}
          <div className="space-y-2">
            <p className="text-xs font-semibold text-gray-500 uppercase tracking-wide">Co zrobić?</p>
            <ol className="space-y-1.5 text-sm text-gray-700">
              <li>1. Kliknij <strong>Spróbuj ponownie</strong> — większość błędów znika po odświeżeniu.</li>
              <li>2. Jeśli błąd wróci — kliknij <strong>Zgłoś błąd</strong> i wyślij gotowego maila.</li>
              <li>3. Wróć do panelu i kontynuuj pracę w innych sekcjach.</li>
            </ol>
          </div>

          <div className="space-y-2">
            <button onClick={reset} className="w-full bg-blue-600 text-white py-2 rounded-lg text-sm font-medium">
              Spróbuj ponownie
            </button>
            <a href={buildMailto()} className="block w-full text-center py-2 rounded-lg text-sm border border-gray-300">
              Zgłoś błąd (email)
            </a>
            <a href="/dashboard" className="block w-full text-center py-2 text-sm text-gray-500">
              Wróć do panelu
            </a>
          </div>
        </div>
      </div>
    </div>
  );
}
```

### global-error.tsx — uwaga: wymaga `<html>` i `<body>`

```tsx
"use client";
// Identyczna logika jak error.tsx, ale owinięta w:
export default function GlobalError({ error, reset }) {
  return (
    <html lang="pl">
      <body className="...">
        {/* ta sama zawartość */}
      </body>
    </html>
  );
}
```

### Różnicowanie kanału kontaktu

- **Panel managera** → email (`mailto:{{KONTAKT_EMAIL}}`)
- **Panel instalatora** → telefon (instalatorzy nie piszą maili na budowie)

---

## Krok 2 — Sentry (~1 godzina, wymaga rejestracji)

> Wdrożyć gdy pojawi się **pierwszy płacący klient spoza pilota**.

**Dlaczego Sentry a nie tylko email?**  
Email od klienta zawiera to co klient napisał. Sentry zawiera stack trace, sesję użytkownika, replay wideo, częstotliwość błędu.

### Setup

```bash
npx @sentry/wizard@latest -i nextjs
```

Kreator automatycznie tworzy `sentry.client.config.ts`, `sentry.server.config.ts` i modyfikuje `next.config.ts`.

### Zmienne środowiskowe

```env
SENTRY_DSN=https://xxx@xxx.ingest.sentry.io/xxx
SENTRY_ORG=nazwa-organizacji
SENTRY_PROJECT=nazwa-projektu
```

### Co daje darmowy tier

- 5 000 błędów / miesiąc
- Stack trace każdego błędu JS (frontend + server)
- Przeglądarka, user ID, timestamp
- Alert na email przy nowym typie błędu

---

## Checklist — zanim oddasz projekt klientowi

- [ ] `src/app/error.tsx` — istnieje i ma przycisk "Zgłoś błąd" z `mailto:`
- [ ] `src/app/global-error.tsx` — istnieje (owinięty w `<html><body>`)
- [ ] `src/app/not-found.tsx` — istnieje, ma link powrotny
- [ ] Każdy izolowany panel (`/installer`, `/admin`) ma własny `error.tsx`
- [ ] Email w `mailto:` jest aktualny i należy do Ciebie
- [ ] Przetestowano ręcznie: biały ekran już nie pojawia się nigdzie
- [ ] (opcjonalne) Sentry skonfigurowany dla płacących klientów

---

## Dlaczego to ważne — argument do rozmowy z klientem

> „Gdy coś się posypie — a w każdej aplikacji prędzej czy później się posypie — chcę wiedzieć o tym zanim Ty zadzwonisz. System błędów sprawia, że dostaję raport z dokładnym miejscem awarii, a Ty jednym kliknięciem wysyłasz mi diagnostykę. Zamiast 30 minut debugowania w ciemno mam gotową odpowiedź w 5 minut."

---

*Szablon stworzony na bazie Klimatyzatron · Kod z Sensem · 2026-05-10*
