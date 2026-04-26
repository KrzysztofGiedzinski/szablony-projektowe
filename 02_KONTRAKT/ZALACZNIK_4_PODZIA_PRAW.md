# ZAŁĄCZNIK NR 4 DO UMOWY {{NUMER_UMOWY}}
## Specyfikacja Elementów Objętych Przeniesieniem Praw Autorskich

> Dokument wymagany przy wyborze **Wariantu C** własności kodu (§ 11 umowy).  
> Jeśli wybrano Wariant A lub B — ten załącznik nie dotyczy.

---

**Data:** _______________  
**Projekt:** {{NAZWA_PROJEKTU}}  
**Umowa:** {{NUMER_UMOWY}}

---

## 1. Elementy Dedykowane — Prawa Przenoszone na Zamawiającego

> Na te elementy Zamawiający nabywa pełne autorskie prawa majątkowe z chwilą zapłaty wynagrodzenia (§ 6 umowy).

| Lp. | Element | Opis | Lokalizacja w repozytorium |
|-----|---------|------|---------------------------|
| 1 | Konfiguracja brandingowa | Logo, kolory, nazwy, komunikaty specyficzne dla {{KLIENT_FIRMA}} | `/src/config/brand.*` |
| 2 | Dane i schematy klienta | Struktura kategorii, lista lokalizacji, dane pracowników | `/src/data/client/` |
| 3 | Dokumentacja użytkownika | Instrukcje pisane pod specyfikę {{KLIENT_FIRMA}} | `/docs/user/` |
| 4 | | | |
| 5 | | | |

---

## 2. Elementy Generyczne — Licencja Niewyłączna dla Zamawiającego

> Na te elementy Wykonawca udziela niewyłącznej licencji (Wariant A). Wykonawca zachowuje prawa autorskie i może korzystać z nich w innych projektach.

| Lp. | Element | Opis | Lokalizacja w repozytorium |
|-----|---------|------|---------------------------|
| 1 | Framework aplikacji | Szkielet projektu, konfiguracja build tools | `/` (root) |
| 2 | Komponenty UI | Biblioteka wspólnych komponentów interfejsu | `/src/components/` |
| 3 | Moduł autoryzacji | Logika logowania, zarządzanie rolami | `/src/auth/` |
| 4 | Integracje zewnętrzne | Kod integracji z Firebase, płatnościami itp. | `/src/integrations/` |
| 5 | Narzędzia i helpery | Funkcje pomocnicze, walidatory, formaty | `/src/utils/` |
| 6 | | | |

---

## 3. Zasady Interpretacji

1. W razie wątpliwości co do kwalifikacji elementu — decyduje Wykonawca, po konsultacji z Zamawiającym.
2. Elementy nieuwzględnione na żadnej z powyższych list są traktowane jako Generyczne (licencja niewyłączna).
3. Nowe elementy stworzone w ramach Change Requestów po podpisaniu umowy wymagają osobnego określenia statusu w danym CR.

---

## 4. Zobowiązania Wykonawcy

1. Wykonawca przekaże Zamawiającemu elementy Dedykowane w formie wydzielonego archiwum (.zip) lub oddzielnej gałęzi repozytorium w ciągu **14 dni** od odbioru końcowego.
2. Wykonawca nie udostępni elementów Dedykowanych podmiotom trzecim bez pisemnej zgody Zamawiającego.

---

## Podpisy

Strony potwierdzają zgodność podziału praw przedstawionego w niniejszym załączniku:

&nbsp;

___________________________  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ___________________________  
**WYKONAWCA** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **ZAMAWIAJĄCY**  
Data: _______________ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Data: _______________
