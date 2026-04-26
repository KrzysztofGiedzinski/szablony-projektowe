# WŁASNOŚĆ KODU ŹRÓDŁOWEGO W POLSKIM PORZĄDKU PRAWNYM
## Opracowanie dla projektu BUILD-TRACK

> Dokument wewnętrzny — podstawa do negocjacji z klientem  
> ⚠️ Nie stanowi porady prawnej — przed podpisaniem skonsultuj z radcą prawnym

---

## 1. PODSTAWA PRAWNA

Kod źródłowy programu komputerowego jest **utworem** w rozumieniu polskiego prawa i podlega ochronie na podstawie:

- **Ustawa z dnia 4 lutego 1994 r. o prawie autorskim i prawach pokrewnych**  
  (Dz.U. 1994 Nr 24 poz. 83 z późn. zm.) — dalej: „PrAut"
- **Dyrektywa 2009/24/WE** o ochronie prawnej programów komputerowych (implementowana przez PrAut)
- **Kodeks cywilny** — w zakresie umów przeniesienia praw

Przepisy szczególne dla programów komputerowych: **art. 74–77 PrAut**

---

## 2. DWA RODZAJE PRAW AUTORSKICH

Prawo autorskie w Polsce dzieli się na dwa niezależne zestawy praw:

### A. Autorskie prawa osobiste (art. 16 PrAut)
- Chronią **więź twórcy z dziełem**
- Są **niezbywalne** — nie można ich przenieść ani zrzec się (nawet umową)
- Przysługują twórcy **zawsze i na zawsze**, bez względu na treść umowy
- Obejmują m.in.:
  - Prawo do autorstwa (bycia wymienionym jako twórca)
  - Prawo do integralności dzieła (sprzeciw wobec zniekształceń)
  - Prawo do nadzoru nad sposobem korzystania z dzieła

**Praktyczna konsekwencja dla BUILD-TRACK:**  
Krzysztof Giedziński zawsze pozostaje **autorem** systemu BUILD-TRACK — nawet jeśli przeniesie wszystkie prawa majątkowe na Vestę.

---

### B. Autorskie prawa majątkowe (art. 17 PrAut)
- Dają prawo do **korzystania z dzieła i rozporządzania nim**
- Są **zbywalne** — można je przenieść lub udzielić licencji
- To właśnie te prawa są przedmiotem negocjacji z klientem
- Obejmują tzw. **pola eksploatacji** (art. 50 PrAut) — lista sposobów korzystania

---

## 3. KLUCZOWA ZASADA: KTO DOMYŚLNIE JEST WŁAŚCICIELEM?

### Zasada ogólna — twórca jest właścicielem (art. 8 § 1 PrAut)
> *„Prawo autorskie przysługuje twórcy"*

**Freelancer / Wykonawca tworzący kod na zlecenie:**
- Domyślnie zachowuje **pełne prawa majątkowe** do stworzonego kodu
- Klient **nie nabywa automatycznie żadnych praw** do kodu tylko dlatego, że za niego zapłacił
- Bez odpowiedniej umowy klient może używać systemu, ale **nie jest jego właścicielem**

### Wyjątek 1 — utwór pracowniczy (art. 12 PrAut)
- Gdy twórca jest **pracownikiem** (umowa o pracę) i tworzy kod w ramach obowiązków służbowych
- Prawa majątkowe przechodzą na pracodawcę **automatycznie** po przyjęciu dzieła
- **Nie dotyczy freelancerów** — umowa zlecenie i o dzieło nie są umową o pracę

### Wyjątek 2 — programy komputerowe stworzone przez pracownika (art. 74 ust. 3 PrAut)
- Przepis szczególny dla programów komputerowych
- Jeśli pracownik (umowa o pracę) stworzył program w wyniku wykonywania obowiązków — prawa należą do pracodawcy
- Znowu: **nie dotyczy relacji Wykonawca–Zamawiający** na podstawie umowy o dzieło/zlecenie

### Wniosek dla BUILD-TRACK
> Krzysztof Giedziński tworzy kod jako **niezależny wykonawca** (nie pracownik Vesty).  
> Bez wyraźnego zapisu w umowie — **kod należy do Krzysztofa**, nie do Vesty.  
> Vesta ma prawo **używać** systemu, ale nie może go np. odsprzedać ani modyfikować bez zgody.

---

## 4. PRZENIESIENIE PRAW MAJĄTKOWYCH

Jeśli klient chce być **właścicielem** kodu, umowa musi zawierać wyraźne przeniesienie praw.

### Wymogi formalne (art. 53 PrAut)
- **Forma pisemna pod rygorem nieważności** — ustne ustalenia nie wystarczą
- Musi wymieniać **pola eksploatacji** (każde pole osobno)
- Przeniesienie obejmuje tylko wskazane pola — reszta zostaje u twórcy

### Pola eksploatacji dla oprogramowania (art. 50 + art. 74 PrAut)

| Pole eksploatacji | Co oznacza |
|-------------------|------------|
| Trwałe lub czasowe zwielokrotnienie | Instalacja, uruchamianie, wyświetlanie, przesyłanie |
| Tłumaczenie, adaptacja, zmiana układu | Modyfikacja kodu, tworzenie wersji pochodnych |
| Rozpowszechnianie, w tym najem lub użyczenie | Sprzedaż, oddanie w dzierżawę innym |
| Publiczne udostępnianie w taki sposób, aby każdy mógł mieć dostęp | Udostępnienie przez internet (SaaS) |
| Reprodukcja kodu źródłowego | Kopiowanie kodu |
| Dekompilacja w granicach ustawy | Odtworzenie kodu maszynowego |

### Co musi zawierać zapis o przeniesieniu praw

```
Wykonawca przenosi na Zamawiającego całość autorskich praw 
majątkowych do Systemu BUILD-TRACK na następujących polach 
eksploatacji: [lista pól], bez ograniczeń terytorialnych i 
czasowych, z chwilą zapłaty pełnego wynagrodzenia.
```

---

## 5. LICENCJA — ALTERNATYWA DLA PRZENIESIENIA PRAW

Zamiast przeniesienia praw, Wykonawca może udzielić **licencji** — zachowując własność.

| Cecha | Przeniesienie praw | Licencja wyłączna | Licencja niewyłączna |
|-------|-------------------|-------------------|---------------------|
| Wykonawca zostaje właścicielem | ❌ Nie | ✅ Tak | ✅ Tak |
| Klient może modyfikować kod | Zależy od zapisu | Zależy od zapisu | Zależy od zapisu |
| Klient może odsprzedać | ✅ Tak | ❌ Zazwyczaj nie | ❌ Zazwyczaj nie |
| Wykonawca może użyć kodu w innych projektach | ❌ Nie | ❌ Nie | ✅ Tak |
| Forma | Pisemna | Pisemna | Pisemna lub ustna |
| Typowe zastosowanie | Klient chce pełnej kontroli | Klient chce wyłączności | Standardowa umowa IT |

---

## 6. TRZY WARIANTY DLA BUILD-TRACK

### Wariant A — Licencja niewyłączna (rekomendowany dla Ciebie)
**Wykonawca zachowuje prawa, Vesta ma licencję na używanie**

Plusy dla Ciebie:
- Możesz reużywać komponenty w innych projektach
- Możesz pokazywać BUILD-TRACK jako referencję
- Możesz rozwijać system równolegle dla innych klientów branży

Plusy dla Vesty:
- Płaci mniej (brak premii za przeniesienie praw)
- Nadal ma pełne prawo do używania systemu
- Może żądać dostępu do kodu na wypadek zakończenia współpracy

Zapis umowny:
```
Wykonawca udziela Zamawiającemu niewyłącznej, nieograniczonej 
terytorialnie i czasowo licencji na korzystanie z Systemu 
BUILD-TRACK na następujących polach eksploatacji: [lista].
Licencja jest udzielona pod warunkiem zapłaty pełnego 
wynagrodzenia wdrożeniowego.
```

---

### Wariant B — Przeniesienie praw (korzystny dla klienta)
**Vesta staje się właścicielem kodu po zapłacie**

Plusy dla Vesty:
- Pełna kontrola — może modyfikować, rozwijać z innym wykonawcą
- Bezpieczeństwo — niezależność od Ciebie
- Może odsprzedać system

Minusy dla Ciebie:
- Tracisz prawa do swojej pracy
- Nie możesz reużyć kodu
- Powinieneś naliczyć **premię za przeniesienie praw** (standardowo +20–40% do ceny)

Zapis umowny:
```
Z chwilą zapłaty pełnego wynagrodzenia wdrożeniowego Wykonawca 
przenosi na Zamawiającego całość autorskich praw majątkowych 
do Systemu BUILD-TRACK na wszystkich polach eksploatacji 
znanych w chwili zawarcia umowy, bez ograniczeń terytorialnych 
i czasowych, wraz z wyłącznym prawem zezwalania na wykonywanie 
zależnego prawa autorskiego.
```

---

### Wariant C — Rozdzielony (pragmatyczny, rekomendowany)
**Silnik/framework zostaje u Ciebie, customizacja Vesty należy do Vesty**

Zasada: Oddzielasz:
- **Kod generyczny** (framework, komponenty Firebase, UI kit) → Twoje
- **Kod specyficzny dla Vesty** (dane, konfiguracja, logo, specyficzne raporty) → Vesty

Zapis umowny:
```
Wykonawca przenosi na Zamawiającego autorskie prawa majątkowe 
do elementów Systemu stworzonych wyłącznie na zamówienie 
Zamawiającego [lista], zachowując prawa do elementów 
generycznych i wielokrotnego użytku [lista].
Zamawiającemu udzielana jest licencja niewyłączna na elementy 
generyczne przez czas trwania umowy.
```

---

## 7. OCHRONA WYKONAWCY — CO WPISAĆ DO UMOWY

Bez względu na wybrany wariant, zawsze wpisuj:

### Klauzula esrow (zabezpieczenie klienta przy Wariancie A)
```
W przypadku zaprzestania świadczenia usług przez Wykonawcę 
z przyczyn od niego zależnych, Wykonawca zobowiązuje się 
przekazać Zamawiającemu pełną kopię kodu źródłowego wraz 
z dokumentacją techniczną w terminie 14 dni.
```

### Klauzula portfolio (Twoje prawo do referencji)
```
Wykonawca ma prawo do wymieniania Systemu BUILD-TRACK 
jako realizacji w swoim portfolio, po uprzednim uzyskaniu 
pisemnej zgody Zamawiającego na ujawnienie nazwy klienta.
```

### Klauzula wynagrodzenia za przeniesienie (jeśli Wariant B)
```
Wynagrodzenie za wdrożenie obejmuje jednorazową opłatę 
za przeniesienie autorskich praw majątkowych w wysokości 
___ zł netto, stanowiącej integralną część ceny wdrożenia.
```

---

## 8. PODSUMOWANIE — REKOMENDACJA DLA BUILD-TRACK

| Pytanie | Rekomendacja |
|---------|-------------|
| Który wariant wybrać? | **Wariant A** (licencja niewyłączna) lub **Wariant C** (rozdzielony) |
| Ile doliczyć za przeniesienie praw (Wariant B)? | +25–40% do ceny wdrożenia |
| Czy wpisać klauzulę esrow? | **Tak** — daje klientowi bezpieczeństwo |
| Czy wpisać klauzulę portfolio? | **Tak** — Twoje prawo do referencji |
| Czy forma pisemna jest obowiązkowa? | **Tak** — dla każdego przeniesienia i licencji wyłącznej |
| Czy umowa ustna wystarczy? | **Nie** — nieważna w zakresie praw autorskich |

---

*Opracowanie na podstawie: Ustawa o prawie autorskim i prawach pokrewnych (Dz.U. 1994 Nr 24 poz. 83), orzecznictwo Sądu Najwyższego, praktyka umów IT w Polsce.*  
*⚠️ Nie stanowi porady prawnej. Skonsultuj z radcą prawnym przed podpisaniem umowy.*
