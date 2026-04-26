# UMOWA O WDROŻENIE I UTRZYMANIE SYSTEMU INFORMATYCZNEGO
## {{NAZWA_PROJEKTU}} — Cyfrowy System Zarządzania Sprzętem Budowlanym

---

**Numer umowy:** {{NUMER_UMOWY}}  
**Miejscowość:** _______________  
**Data zawarcia:** _______________

---

### STRONY UMOWY

**WYKONAWCA:**

Imię i Nazwisko / Firma: _______________  
Adres prowadzenia działalności: _______________  
NIP: _______________ | REGON: _______________  
Numer rachunku bankowego: _______________  
E-mail: _______________ | Tel.: _______________  

zwany dalej **„Wykonawcą"**

**ZAMAWIAJĄCY:**

Firma: **{{KLIENT_FIRMA}}**  
Adres siedziby: {{KLIENT_ADRES}}  
NIP: **{{KLIENT_NIP}}** | REGON: _______________  
Reprezentowana przez: **{{KLIENT_KONTAKT}}** (stanowisko: {{KLIENT_STANOWISKO}})  
E-mail: _______________ | Tel.: **{{KLIENT_TEL}}**  

zwana dalej **„Zamawiającym"**

---

## ROZDZIAŁ I — PRZEDMIOT UMOWY

### § 1. Przedmiot umowy

1. Wykonawca zobowiązuje się do wdrożenia systemu informatycznego **{{NAZWA_PROJEKTU}}** — cyfrowego systemu do śledzenia i zarządzania sprzętem oraz materiałami budowlanymi, zwanego dalej **„Systemem"**.

2. Umowa obejmuje dwa etapy:
   - **Etap I:** Jednorazowe wdrożenie Systemu (Opłata wdrożeniowa)
   - **Etap II:** Ciągłe utrzymanie i wsparcie techniczne (Abonament miesięczny)

3. Szczegółowy zakres funkcjonalny Systemu określa **Załącznik nr 1** do niniejszej umowy (Specyfikacja techniczna {{NAZWA_PROJEKTU}} v1.0).

---

## ROZDZIAŁ II — ZAKRES WDROŻENIA

### § 2. Zakres Fazy 1 (MVP — Minimum Viable Product)

W ramach opłaty wdrożeniowej Wykonawca dostarczy:

**A. Panel webowy (dostęp przez przeglądarkę)**
- Dashboard z widokiem wartości majątku w czasie rzeczywistym
- Moduł Magazyn — stan ilościowy i wartościowy per lokalizacja
- Moduł Asortyment — katalog sprzętu z cenami jednostkowymi
- Moduł Lokalizacje — zarządzanie magazynami i budowami
- Moduł Kategorie — hierarchiczna struktura asortymentu (do 6 poziomów)
- Moduł Handshake — protokół cyfrowego potwierdzenia transportów
- System logowania z zarządzaniem uprawnieniami (role: Kierownik, Magazynier, Robotnik)
- Strona Pomocy z instrukcją obsługi

**B. Aplikacja mobilna (iOS i Android)**
- Logowanie z przypisaniem do lokalizacji
- Ekran główny z przeglądem stanu magazynowego
- Flow skanowania NFC: skan tagu → zdjęcie → potwierdzenie operacji
- Praca offline z synchronizacją po odzysku zasięgu internetowego

**C. Backend i infrastruktura**
- Konfiguracja bazy danych Firebase Firestore
- Reguły bezpieczeństwa i kontrola dostępu
- Firebase Storage na zdjęcia sprzętu
- Hosting panelu webowego (Firebase Hosting)
- Import danych Zamawiającego (wykaz sprzętu, kategorie, lokalizacje)

**D. Uruchomienie i szkolenie**
- Szkolenie dla Kierownika i Magazyniera (do ___ godzin)
- Szkolenie dla Robotników z obsługi aplikacji mobilnej (do ___ godzin)
- Dokumentacja użytkownika w języku polskim

### § 3. Zakres Faz opcjonalnych (odrębne zlecenia)

Poniższe funkcje wykraczają poza Fazę 1 i będą realizowane na podstawie osobnych zleceń lub aneksów:

| Faza | Zakres |
|------|--------|
| **Faza 2** | Fizyczne tagi NFC On-Metal, kamera w apce mobilnej, tryb offline, wielojęzyczność (PL/EN) |
| **Faza 3** | Grywalizacja (punkty rzetelności, rankingi), raporty PDF, harmonogram przeglądów |

---

## ROZDZIAŁ III — TERMINY

### § 4. Harmonogram wdrożenia

| Kamień milowy | Termin | Warunek |
|---------------|--------|---------|
| Podpisanie umowy i wpłata zaliczki | _______________ | — |
| Dostarczenie danych przez Zamawiającego | _______________ | Do ___ dni od podpisania |
| Wdrożenie MVP (Faza 1) | _______________ | Do ___ tygodni od dostarczenia danych |
| Szkolenie użytkowników | _______________ | W ciągu ___ tygodni od wdrożenia |
| Odbiór końcowy Fazy 1 | _______________ | Do ___ dni od szkolenia |

### § 5. Warunki dotrzymania terminów

1. Terminy określone w § 4 obowiązują pod warunkiem terminowego dostarczenia przez Zamawiającego:
   - Wykazu sprzętu i materiałów (plik Excel/CSV)
   - Struktury kategorii asortymentu
   - Listy lokalizacji (nazwa, adres, kierownik)
   - Listy pracowników z rolami i językami
   - Dostępu do kont e-mail pracowników

2. Opóźnienia wynikające z braku ww. danych przedłużają termin wdrożenia o czas zwłoki Zamawiającego.

---

## ROZDZIAŁ IV — WYNAGRODZENIE

### § 6. Opłata wdrożeniowa (jednorazowa)

1. Za wdrożenie Fazy 1 (§ 2) Zamawiający zapłaci Wykonawcy wynagrodzenie w wysokości:

   **_______________ zł netto** (słownie: _______________)  
   + VAT ___ % = **_______________ zł brutto**

2. Płatność w następujących transzach:

| Transza | Kwota netto | Termin | Warunek |
|---------|-------------|--------|---------|
| Zaliczka (___%) | _______________ zł | Do ___ dni od podpisania umowy | — |
| Transza II (___%) | _______________ zł | Po wdrożeniu MVP | Podpisanie protokołu odbioru |
| Transza III (___%) | _______________ zł | Po szkoleniu | Podpisanie protokołu końcowego |

### § 7. Abonament miesięczny (utrzymanie)

1. Po odbiorze końcowym Fazy 1 Zamawiający zapłaci miesięczny abonament w wysokości:

   **_______________ zł netto/miesiąc** (słownie: _______________)  
   + VAT ___ % = **_______________ zł brutto/miesiąc**

2. Abonament obejmuje:
   - Utrzymanie infrastruktury Firebase (hosting, baza danych, storage)
   - Monitorowanie dostępności systemu 24/7
   - Aktualizacje bezpieczeństwa
   - Wsparcie techniczne: ___ godzin/miesiąc (czas reakcji: do ___ godzin roboczych)
   - Drobne poprawki i ulepszenia (do ___ godzin/miesiąc łącznie)
   - Backup danych co ___ godziny

3. Abonament jest płatny **z góry do ___ dnia każdego miesiąca** na podstawie faktury VAT.

4. Abonament nie obejmuje:
   - Nowych funkcjonalności wykraczających poza zakres § 2
   - Migracji danych ze starych systemów (po zakończeniu wdrożenia)
   - Zakupu tagów NFC i sprzętu fizycznego
   - Szkolenia nowych pracowników Zamawiającego (rozliczane osobno: ___ zł/h)

### § 8. Zmiany zakresu (Change Request)

1. Wszelkie zmiany w zakresie wdrożenia, wykraczające poza § 2, wymagają pisemnego zlecenia zmiany (**Change Request**).

2. Procedura Change Request:
   - Zamawiający zgłasza zmianę pisemnie (e-mail)
   - Wykonawca wycenia zmianę w ciągu ___ dni roboczych
   - Po akceptacji wyceny przez Zamawiającego — realizacja zgodnie z ustalonym terminem
   - Zmiana zakresu może wpłynąć na termin i wynagrodzenie

3. **Złota zasada:** Wszystko co nie jest zapisane w umowie lub zatwierdzonym Change Request — nie istnieje jako zobowiązanie Wykonawcy.

---

## ROZDZIAŁ V — PRAWA I OBOWIĄZKI STRON

### § 9. Obowiązki Wykonawcy

1. Wdrożenie Systemu zgodnie z § 2 i harmonogramem z § 4.
2. Informowanie Zamawiającego o postępach prac minimum raz w tygodniu.
3. Niezwłoczne zgłaszanie przeszkód mogących wpłynąć na termin wdrożenia.
4. Zapewnienie bezpieczeństwa danych Zamawiającego zgodnie z RODO.
5. Utrzymanie kodu źródłowego w repozytorium Git (GitHub).
6. Świadczenie usług abonamentowych zgodnie z § 7.

### § 10. Obowiązki Zamawiającego

1. Dostarczenie danych niezbędnych do wdrożenia w terminach z § 5.
2. Wyznaczenie Osoby Kontaktowej (Point of Contact) z uprawnieniami decyzyjnymi.
3. Terminowe regulowanie płatności zgodnie z § 6 i § 7.
4. Udostępnienie pracowników na szkolenie w uzgodnionym terminie.
5. Zakup tagów NFC On-Metal na własny koszt (niezbędne do Fazy 2).
6. Nieudostępnianie danych dostępowych do Systemu osobom nieupoważnionym.

---

## ROZDZIAŁ VI — WŁASNOŚĆ I LICENCJA

### § 11. Autorskie prawa majątkowe do kodu źródłowego

> **INSTRUKCJA:** Wybierz jeden z trzech wariantów poniżej i usuń pozostałe przed podpisaniem.  
> Szczegółowe uzasadnienie prawne każdego wariantu — patrz: `WLASNOSC_KODU_PRAWO_PL.md`

---

#### ► WARIANT A — Licencja niewyłączna *(Wykonawca zachowuje prawa)*

1. System {{NAZWA_PROJEKTU}} stanowi utwór w rozumieniu art. 1 ustawy z dnia 4 lutego 1994 r. o prawie autorskim i prawach pokrewnych (Dz.U. 1994 Nr 24 poz. 83 z późn. zm.). Autorskie prawa osobiste przysługują Wykonawcy i nie podlegają przeniesieniu.

2. Z chwilą zapłaty pełnego wynagrodzenia wdrożeniowego (§ 6) Wykonawca udziela Zamawiającemu **niewyłącznej, nieograniczonej terytorialnie i czasowo licencji** na korzystanie z Systemu na następujących polach eksploatacji (art. 50 PrAut):
   - trwałe i czasowe zwielokrotnianie programu — instalacja, uruchamianie, wyświetlanie, przesyłanie i przechowywanie
   - tłumaczenie, adaptacja, zmiana układu lub jakiekolwiek inne zmiany w programie — w zakresie niezbędnym do prawidłowego używania Systemu przez Zamawiającego
   - publiczne udostępnianie Systemu pracownikom Zamawiającego przez sieć internet

3. Licencja nie obejmuje prawa do:
   - sublicencjonowania (udostępniania Systemu osobom trzecim odpłatnie)
   - sprzedaży, najmu lub innego odpłatnego rozporządzania Systemem
   - usuwania lub zmieniania informacji o autorstwie

4. Autorskie prawa majątkowe pozostają przy Wykonawcy. Wykonawca może korzystać z kodu Systemu lub jego komponentów w innych projektach, z zastrzeżeniem zachowania poufności danych Zamawiającego (§ 15).

---

#### ► WARIANT B — Przeniesienie pełnych praw majątkowych *(Zamawiający nabywa własność)*

1. System {{NAZWA_PROJEKTU}} stanowi utwór w rozumieniu art. 1 ustawy z dnia 4 lutego 1994 r. o prawie autorskim i prawach pokrewnych. Autorskie prawa osobiste przysługują Wykonawcy i nie podlegają przeniesieniu.

2. Z chwilą zapłaty pełnego wynagrodzenia wdrożeniowego (§ 6), które obejmuje jednorazową opłatę za przeniesienie praw autorskich w wysokości **_______________ zł netto**, Wykonawca przenosi na Zamawiającego **całość autorskich praw majątkowych** do Systemu {{NAZWA_PROJEKTU}} na następujących polach eksploatacji (art. 50 i art. 74 PrAut):
   - trwałe i czasowe zwielokrotnianie programu w całości lub w części
   - tłumaczenie, adaptacja, zmiana układu lub jakiekolwiek inne zmiany w programie
   - rozpowszechnianie, w tym użyczenie lub najem programu lub jego kopii
   - publiczne udostępnianie w taki sposób, aby każdy mógł mieć do niego dostęp w miejscu i czasie przez siebie wybranym

3. Przeniesienie następuje bez ograniczeń terytorialnych i czasowych, wraz z **wyłącznym prawem zezwalania na wykonywanie zależnego prawa autorskiego** (art. 46 PrAut).

4. Wykonawca gwarantuje, że System jest jego oryginalnym dziełem i nie narusza praw osób trzecich.

---

#### ► WARIANT C — Prawa rozdzielone *(podział na kod generyczny i dedykowany)*

1. System {{NAZWA_PROJEKTU}} stanowi utwór złożony, na który składają się elementy generyczne (wielokrotnego użytku) oraz elementy stworzone dedykowanie dla Zamawiającego.

2. Z chwilą zapłaty pełnego wynagrodzenia wdrożeniowego (§ 6) Wykonawca:

   **a) Przenosi autorskie prawa majątkowe** na Zamawiającego do następujących elementów Systemu:
   - Konfiguracja systemu specyficzna dla Vesta (branding, logo, dane lokalizacji)
   - Schematy kategorii asortymentu Zamawiającego
   - Zaimportowane dane i struktura danych klienta
   — na polach eksploatacji wymienionych w Wariancie B powyżej.

   **b) Udziela niewyłącznej licencji** na elementy generyczne (framework aplikacji, komponenty UI, integracje Firebase) — na warunkach Wariantu A powyżej.

3. Podział elementów zostanie dookreślony w Załączniku nr 4 (Specyfikacja elementów objętych przeniesieniem praw).

---

#### Postanowienia wspólne dla wszystkich wariantów

5. **Dostęp do kodu źródłowego:** Zamawiający ma prawo wglądu do repozytorium kodu (GitHub) przez cały czas trwania umowy.

6. **Klauzula esrow — zabezpieczenie Zamawiającego:** W przypadku zaprzestania świadczenia usług przez Wykonawcę z przyczyn od niego zależnych, Wykonawca zobowiązuje się w ciągu **14 dni** przekazać Zamawiającemu pełną kopię kodu źródłowego, dokumentację techniczną i dane dostępowe do infrastruktury Firebase.

7. **Klauzula portfolio:** Wykonawca ma prawo wymienić System {{NAZWA_PROJEKTU}} jako realizację w swoim portfolio zawodowym. Ujawnienie nazwy Zamawiającego wymaga jego pisemnej zgody.

### § 12. Dane Zamawiającego

1. Wszystkie dane wprowadzone do Systemu przez Zamawiającego są wyłączną własnością Zamawiającego.
2. Wykonawca zobowiązuje się nie udostępniać danych Zamawiającego osobom trzecim.
3. Wykonawca przetwarza dane osobowe pracowników Zamawiającego wyłącznie w celu realizacji niniejszej umowy (podstawa: RODO art. 28 — Umowa Powierzenia Przetwarzania Danych, stanowiąca **Załącznik nr 2**).

---

## ROZDZIAŁ VII — GWARANCJA I SLA

### § 13. Gwarancja na wdrożenie

1. Wykonawca udziela ___ miesięcy gwarancji na wdrożenie, licząc od daty odbioru końcowego.
2. W ramach gwarancji Wykonawca zobowiązuje się do bezpłatnego usunięcia błędów oprogramowania w terminie:
   - Błąd krytyczny (System niedostępny): do ___ godzin
   - Błąd poważny (kluczowa funkcja niedostępna): do ___ godzin roboczych
   - Błąd drobny: do ___ dni roboczych

### § 14. SLA (Service Level Agreement) — dla abonamentu

| Parametr | Wartość |
|----------|---------|
| Dostępność systemu | ___% miesięcznie |
| Czas reakcji na zgłoszenie | Do ___ godzin roboczych |
| Czas usunięcia błędu krytycznego | Do ___ godzin |
| Czas usunięcia błędu poważnego | Do ___ godzin roboczych |
| Czas usunięcia błędu drobnego | Do ___ dni roboczych |
| Okno serwisowe (planowane przerwy) | Niedziela 02:00–04:00 |

---

## ROZDZIAŁ VIII — WARUNKI OGÓLNE

### § 15. Poufność

1. Obie Strony zobowiązują się do zachowania w tajemnicy wszelkich informacji poufnych uzyskanych w trakcie współpracy przez okres ___ lat od zakończenia umowy.
2. Za informacje poufne uważa się w szczególności: dane o sprzęcie Zamawiającego, dane pracowników, wartość kontraktu, treść umowy.

### § 16. Odpowiedzialność

1. Wykonawca nie ponosi odpowiedzialności za szkody wynikające z:
   - Nieprawidłowego użytkowania Systemu przez pracowników Zamawiającego
   - Przerw w działaniu usług Firebase (Google) — niezależnych od Wykonawcy
   - Braku lub utraty tagów NFC (elementy fizyczne)
   - Działania siły wyższej

2. Odpowiedzialność Wykonawcy z tytułu niniejszej umowy jest ograniczona do wysokości opłaty wdrożeniowej netto.

### § 17. Czas trwania i rozwiązanie umowy

1. Umowa wdrożeniowa (Rozdział II–VI) jest zawarta na czas realizacji Fazy 1.
2. Umowa abonamentowa (§ 7) jest zawarta na czas nieokreślony z możliwością wypowiedzenia przez każdą ze Stron z zachowaniem ___ miesięcznego okresu wypowiedzenia.
3. W przypadku zalegania z płatnościami abonamentowymi przez ___ miesiące Wykonawca może zawiesić świadczenie usług po uprzednim pisemnym wezwaniu do zapłaty.

### § 18. Zmiany umowy

Wszelkie zmiany niniejszej umowy wymagają formy pisemnej pod rygorem nieważności (aneks podpisany przez obie Strony).

### § 19. Prawo właściwe i spory

1. Umowa podlega prawu polskiemu.
2. Spory wynikające z umowy Strony będą rozwiązywać polubownie.
3. W przypadku braku porozumienia, spory rozstrzygać będzie sąd właściwy dla siedziby Wykonawcy.

### § 20. Postanowienia końcowe

1. Umowę sporządzono w dwóch jednobrzmiących egzemplarzach, po jednym dla każdej ze Stron.
2. Integralną część umowy stanowią:
   - **Załącznik nr 1** — Specyfikacja techniczna {{NAZWA_PROJEKTU}} v1.0
   - **Załącznik nr 2** — Umowa Powierzenia Przetwarzania Danych (RODO)
   - **Załącznik nr 3** — Protokół odbioru (do wypełnienia po wdrożeniu)

---

## PODPISY

&nbsp;

___________________________  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ___________________________  
**WYKONAWCA** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **ZAMAWIAJĄCY**  
_______________ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _______________  
(imię, nazwisko, stanowisko) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (imię, nazwisko, stanowisko)

Data: _______________ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Data: _______________
