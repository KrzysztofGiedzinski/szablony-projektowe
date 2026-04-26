# ZAŁĄCZNIK NR 2 DO UMOWY {{NUMER_UMOWY}}
# UMOWA POWIERZENIA PRZETWARZANIA DANYCH OSOBOWYCH
## (art. 28 Rozporządzenia RODO)

---

**Miejscowość:** _______________  
**Data zawarcia:** _______________  
*(data tożsama z datą Umowy głównej)*

---

### STRONY

**ADMINISTRATOR DANYCH:**

Firma: **{{KLIENT_FIRMA}}**  
Adres: {{KLIENT_ADRES}}  
NIP: **{{KLIENT_NIP}}**  
Reprezentowana przez: **{{KLIENT_KONTAKT}}** ({{KLIENT_STANOWISKO}})  

zwany dalej **„Administratorem"**

**PODMIOT PRZETWARZAJĄCY:**

Imię i Nazwisko / Firma: _______________  
Adres: _______________  
NIP: _______________  

zwany dalej **„Podmiotem Przetwarzającym"**

---

## § 1. Przedmiot i cel powierzenia

1. Administrator powierza Podmiotowi Przetwarzającemu przetwarzanie danych osobowych w zakresie niezbędnym do realizacji Umowy głównej nr {{NUMER_UMOWY}}, tj. wdrożenia i utrzymania systemu informatycznego **{{NAZWA_PROJEKTU}}**.

2. Dane osobowe są przetwarzane wyłącznie w celu:
   - Umożliwienia logowania pracowników Administratora do systemu {{NAZWA_PROJEKTU}}
   - Przypisania operacji (skanowań NFC, transferów sprzętu) do konkretnych pracowników
   - Naliczania punktów rzetelności w module grywalizacji
   - Generowania raportów dostępności i aktywności

---

## § 2. Kategorie osób, których dane dotyczą

Przetwarzanie dotyczy danych osobowych następujących kategorii osób:
- Pracownicy Administratora (Robotnicy, Kierownicy, Magazynierzy)
- Ewentualnie: pracownicy podwykonawców Administratora (jeśli zostaną dodani do systemu)

---

## § 3. Zakres przetwarzanych danych

| Kategoria danych | Cel przetwarzania |
|-----------------|-------------------|
| Imię i nazwisko | Identyfikacja w systemie, logi operacji |
| Adres e-mail | Logowanie (Firebase Auth) |
| Numer telefonu | Dane kontaktowe kierownika (opcjonalnie) |
| Rola w systemie (Robotnik/Kierownik/Magazynier) | Kontrola dostępu |
| Przypisana lokalizacja (budowa) | Śledzenie operacji sprzętowych |
| Historia operacji w systemie | Immutable logi — audyt i grywalizacja |
| Punkty rzetelności | Grywalizacja |
| Preferencja językowa | Lokalizacja interfejsu |

**Podmiot Przetwarzający nie przetwarza:**
- Danych wrażliwych (art. 9 RODO)
- Danych finansowych pracowników
- Danych biometrycznych

---

## § 4. Czas przetwarzania

1. Podmiot Przetwarzający przetwarza dane przez cały okres obowiązywania Umowy głównej.

2. Po zakończeniu Umowy głównej Podmiot Przetwarzający:
   - Na żądanie Administratora — zwraca wszystkie dane w ciągu **14 dni**
   - Usuwa kopie danych ze swoich systemów roboczych w ciągu **30 dni**
   - Potwierdza usunięcie danych na piśmie

---

## § 5. Obowiązki Podmiotu Przetwarzającego

Podmiot Przetwarzający zobowiązuje się do:

1. **Przetwarzania danych wyłącznie na udokumentowane polecenie Administratora** — tj. wyłącznie w celu realizacji Umowy głównej.

2. **Zapewnienia poufności** — osoby upoważnione do przetwarzania danych zobowiązane są do zachowania tajemnicy.

3. **Wdrożenia środków technicznych i organizacyjnych** zapewniających bezpieczeństwo danych, w szczególności:
   - Szyfrowanie danych w transmisji (HTTPS/TLS)
   - Szyfrowanie danych w spoczynku (Firebase Firestore — szyfrowanie Google)
   - Kontrola dostępu oparta na rolach (Firestore Security Rules)
   - Uwierzytelnianie użytkowników (Firebase Auth)
   - Regularne kopie zapasowe

4. **Nieudostępniania danych dalszym podmiotom** bez uprzedniej zgody Administratora, z zastrzeżeniem § 6.

5. **Pomocy Administratorowi** w wywiązywaniu się z obowiązków określonych w art. 32–36 RODO (bezpieczeństwo, zgłaszanie naruszeń, ocena skutków, uprzednie konsultacje).

6. **Udzielenia dostępu do informacji** niezbędnych do wykazania spełnienia obowiązków z art. 28 RODO oraz umożliwienia Administratorowi lub audytorowi przeprowadzenia audytów.

7. **Niezwłocznego informowania Administratora** (nie później niż w ciągu **24 godzin**) o każdym przypadku naruszenia bezpieczeństwa danych osobowych.

---

## § 6. Podpowierzenie przetwarzania (dalsze powierzenie)

1. Podmiot Przetwarzający korzysta z usług następujących podwykonawców (dalszych podmiotów przetwarzających):

| Podwykonawca | Siedziba | Zakres przetwarzania | Podstawa |
|--------------|----------|---------------------|----------|
| Google LLC (Firebase) | USA (dane w EU — europe-central2, Warszawa) | Hosting, baza danych, uwierzytelnianie, storage | Standardowe Klauzule Umowne (SCCs) |
| GitHub Inc. (Microsoft) | USA | Przechowywanie kodu źródłowego (bez danych osobowych użytkowników) | SCCs |

2. Podmiot Przetwarzający informuje Administratora o planowanych zmianach podwykonawców z wyprzedzeniem **14 dni**, dając możliwość wyrażenia sprzeciwu.

3. Podwykonawcy spełniają wymagania RODO — Google Firebase posiada certyfikaty ISO 27001, SOC 2/3 i przetwarza dane w regionie `europe-central2` (Warszawa).

---

## § 7. Prawa osób, których dane dotyczą

1. Podmiot Przetwarzający zobowiązuje się wspierać Administratora w realizacji praw osób, których dane dotyczą:
   - Prawo dostępu do danych (art. 15 RODO)
   - Prawo do sprostowania (art. 16 RODO)
   - Prawo do usunięcia danych (art. 17 RODO)
   - Prawo do ograniczenia przetwarzania (art. 18 RODO)
   - Prawo do przenoszenia danych (art. 20 RODO)

2. W przypadku otrzymania żądania od osoby, której dane dotyczą, Podmiot Przetwarzający niezwłocznie (nie później niż w ciągu **48 godzin**) przekazuje je Administratorowi.

---

## § 8. Naruszenia bezpieczeństwa

1. W przypadku stwierdzenia naruszenia bezpieczeństwa danych osobowych Podmiot Przetwarzający:
   - Informuje Administratora w ciągu **24 godzin** od wykrycia
   - Przekazuje: opis naruszenia, kategorie i szacunkową liczbę osób, możliwe konsekwencje, podjęte środki zaradcze
   - Współpracuje przy ewentualnym zgłoszeniu do UODO (art. 33 RODO — Administrator ma 72h)

---

## § 9. Postanowienia końcowe

1. Umowa wchodzi w życie z dniem podpisania Umowy głównej i obowiązuje przez czas jej trwania.
2. W sprawach nieuregulowanych stosuje się przepisy RODO oraz polskiego prawa ochrony danych osobowych.
3. Umowę sporządzono w dwóch jednobrzmiących egzemplarzach.

---

## PODPISY

&nbsp;

___________________________  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ___________________________  
**ADMINISTRATOR DANYCH** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **PODMIOT PRZETWARZAJĄCY**  
_(Zamawiający)_ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; _(Wykonawca)_

Data: _______________ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Data: _______________
