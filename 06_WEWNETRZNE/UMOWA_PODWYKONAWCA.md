# UMOWA O WSPÓŁPRACY (B2B) — PODWYKONAWCA
## Projekt: {{NAZWA_PROJEKTU}}

---

**Numer umowy:** PKW-___  
**Miejscowość:** _______________  
**Data zawarcia:** _______________

---

### STRONY

**ZLECENIODAWCA:**

Imię i Nazwisko / Firma: _______________  
Adres prowadzenia działalności: _______________  
NIP: _______________ | REGON: _______________  
E-mail: _______________ | Tel.: _______________  

zwany dalej **„Zleceniodawcą"**

**PODWYKONAWCA:**

Imię i Nazwisko / Firma: _______________  
Adres prowadzenia działalności: _______________  
NIP: _______________ | REGON: _______________  
E-mail: _______________ | Tel.: _______________  

zwany dalej **„Podwykonawcą"**

---

> **Kontekst:** Zleceniodawca realizuje projekt {{NAZWA_PROJEKTU}} na rzecz {{KLIENT_FIRMA}} na podstawie odrębnej umowy. Niniejsza umowa reguluje współpracę z Podwykonawcą przy realizacji części tego projektu.

---

## § 1. Przedmiot Umowy

1. Zleceniodawca zleca, a Podwykonawca przyjmuje do realizacji następujący zakres prac:

```
[Opisz szczegółowo — np. "Projektowanie UI/UX modułów X i Y", "Implementacja backendu Firebase", etc.]
```

2. Szczegółowy zakres prac określa **Załącznik nr 1** (Specyfikacja zakresu podwykonawcy) do niniejszej umowy.

3. Podwykonawca realizuje prace zgodnie z:
   - Specyfikacją z Załącznika nr 1
   - Wytycznymi technicznymi Zleceniodawcy
   - Harmonogramem projektu (Załącznik nr 2)

---

## § 2. Harmonogram i Terminy

| Kamień milowy | Termin | Deliverable |
|---------------|--------|-------------|
| Start prac | _______________ | — |
| _______________ | _______________ | _______________ |
| _______________ | _______________ | _______________ |
| Dostarczenie całości | _______________ | Kod + dokumentacja |

1. Podwykonawca zobowiązuje się informować Zleceniodawcę o zagrożeniach terminów **niezwłocznie**, nie później niż ___ dni przed planowanym terminem dostarczenia.

2. Opóźnienie z winy Podwykonawcy przekraczające ___ dni roboczych uprawnia Zleceniodawcę do naliczenia kary umownej lub rozwiązania umowy.

---

## § 3. Wynagrodzenie

### Wariant A — Stała kwota (Fixed Price)

Za wykonanie całości prac określonych w § 1 Podwykonawcy przysługuje wynagrodzenie:

**_______________ zł netto** + VAT ___% = **_______________ zł brutto**

Płatność w transzach:

| Transza | % | Kwota netto | Termin / Warunek |
|---------|---|-------------|-----------------|
| Zaliczka | ___% | ___ zł | Przy podpisaniu umowy |
| Transza II | ___% | ___ zł | Po dostarczeniu _______________ |
| Rozliczenie końcowe | ___% | ___ zł | Po odbiorze całości |

---

### Wariant B — Time & Material (Stawka godzinowa)

Podwykonawcy przysługuje wynagrodzenie według stawki:

**_______________ zł netto / godzinę**

Maksymalny budżet bez dodatkowej zgody: **_______________ zł netto**

Rozliczenie: miesięcznie / po zakończeniu każdego etapu, na podstawie raportu czasu pracy (timesheet).

---

> **Instrukcja:** Wybierz jeden wariant i usuń drugi przed podpisaniem.

### Postanowienia wspólne

1. Faktura VAT wystawiana przez Podwykonawcę w ciągu ___ dni od spełnienia warunków płatności.
2. Termin płatności: ___ dni od otrzymania prawidłowo wystawionej faktury.
3. Dane do faktury: _______________

---

## § 4. Własność Kodu i Prawa Autorskie

1. Z chwilą zapłaty wynagrodzenia (lub każdej transzy) Podwykonawca przenosi na Zleceniodawcę **całość autorskich praw majątkowych** do wytworzonych przez siebie materiałów (kod, grafiki, dokumentacja), na wszystkich polach eksploatacji określonych w art. 50 ustawy o prawie autorskim.

2. Przeniesienie praw następuje bez ograniczeń terytorialnych i czasowych.

3. Podwykonawca gwarantuje, że dostarczone materiały są jego oryginalnym dziełem i nie naruszają praw osób trzecich.

4. Podwykonawca zobowiązuje się do nieujawniania kodu i dokumentacji projektu podmiotom trzecim.

5. Podwykonawca **nie ma prawa** używać kodu stworzonego w ramach niniejszej umowy w innych projektach bez pisemnej zgody Zleceniodawcy.

---

## § 5. Poufność

1. Podwykonawca zobowiązuje się zachować w tajemnicy wszelkie informacje dotyczące projektu, klienta końcowego ({{KLIENT_FIRMA}}), kodu i architektury systemu przez **___ lat** od zakończenia współpracy.

2. Podwykonawca nie może ujawniać faktu współpracy z Zleceniodawcą przy projekcie {{NAZWA_PROJEKTU}} bez jego pisemnej zgody.

3. Podwykonawca zobowiązuje się podpisać odrębną Umowę NDA jeśli Zleceniodawca tego zażąda.

---

## § 6. RODO

1. Jeśli Podwykonawca przetwarza dane osobowe użytkowników systemu w trakcie prac, robi to wyłącznie na udokumentowane polecenie Zleceniodawcy i zgodnie z obowiązującymi przepisami RODO.

2. Podwykonawca zobowiązuje się do podpisania stosownej umowy powierzenia przetwarzania danych jeśli zakres prac tego wymaga.

---

## § 7. Jakość i Standardy

Podwykonawca zobowiązuje się do:

1. Pisania kodu zgodnego z uzgodnionym stylem i standardami projektu (patrz `docs/architecture/README.md` projektu)
2. Pisania testów jednostkowych / integracyjnych dla dostarczanego kodu (zakres: _______________)
3. Dokumentowania kodu w zakresie uzgodnionym ze Zleceniodawcą
4. Przeprowadzania code review na żądanie Zleceniodawcy
5. Pracy wyłącznie na dedykowanej gałęzi git i tworzenia Pull Requestów do zatwierdzenia

---

## § 8. Gwarancja i Poprawki

1. Podwykonawca udziela ___ miesięcy gwarancji na dostarczone prace, licząc od daty odbioru.
2. W ramach gwarancji Podwykonawca bezpłatnie usuwa błędy wynikające z jego pracy w terminie:
   - Błąd krytyczny: do ___ godzin
   - Błąd ważny: do ___ godzin roboczych
   - Błąd drobny: do ___ dni roboczych

---

## § 9. Zakaz Konkurencji i Podbierania Klientów

> Usuń tę sekcję jeśli nie jest potrzebna.

1. Przez ___ miesięcy od zakończenia współpracy Podwykonawca nie będzie nawiązywał bezpośredniej współpracy z {{KLIENT_FIRMA}} z pominięciem Zleceniodawcy.
2. Naruszenie tego zakazu uprawnia Zleceniodawcę do dochodzenia kary umownej w wysokości _______________ zł.

---

## § 10. Rozwiązanie Umowy

1. Każda ze Stron może rozwiązać umowę za ___ dniowym wypowiedzeniem.
2. Zleceniodawca może rozwiązać umowę ze skutkiem natychmiastowym w przypadku:
   - rażącego naruszenia Regulaminu lub standardów projektu
   - opóźnienia przekraczającego ___ dni bez uzasadnienia
   - naruszenia klauzuli poufności
3. Przy rozwiązaniu umowy Podwykonawca zobowiązuje się przekazać wszystkie wytworzone materiały w stanie zaawansowania na dzień rozwiązania, za wynagrodzeniem proporcjonalnym do wykonanej pracy.

---

## § 11. Postanowienia Końcowe

1. Podwykonawca jest niezależnym wykonawcą — niniejsza umowa nie tworzy stosunku pracy ani spółki.
2. Podwykonawca samodzielnie odprowadza podatki i składki ZUS wynikające z niniejszej umowy.
3. Umowa podlega prawu polskiemu.
4. Spory rozstrzygane przez sąd właściwy dla siedziby Zleceniodawcy.
5. Umowę sporządzono w dwóch jednobrzmiących egzemplarzach.

---

## Załączniki

- **Załącznik nr 1** — Specyfikacja zakresu prac Podwykonawcy
- **Załącznik nr 2** — Harmonogram

---

## Podpisy

&nbsp;

___________________________  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ___________________________  
**ZLECENIODAWCA** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **PODWYKONAWCA**  
Data: _______________ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Data: _______________
