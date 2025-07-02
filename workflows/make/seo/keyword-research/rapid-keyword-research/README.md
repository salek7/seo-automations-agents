# ⚡ Szybkie badania słów kluczowych

## Opis automatyzacji

Automatyzacja zastępuje godziny ręcznego badania słów kluczowych, generując w sekundy w pełni sformatowany arkusz Google Sheets z wszystkimi potrzebnymi danymi SEO. Idealna dla agencji SEO i specjalistów digital marketing.

## Jak działa?

1. **Pobiera główne słowa kluczowe** z Google Sheets
2. **Generuje wariacje słów kluczowych** automatycznie
3. **Pobiera dane z SerpData.io**:
   - Wolumen wyszukiwań
   - CPC (koszt za kliknięcie)
   - Trudność słowa kluczowego
4. **Pobiera autouzupełnienie Google** dla każdego słowa kluczowego
5. **Ekstrahuje pytania "Ludzie pytają również"** (PAA)
6. **Scrapuje dane z pierwszej strony SERP** dla analizy konkurencji
7. **Formatuje wszystko** w gotowy arkusz Google Sheets

## Co zawiera wynik?

### Podstawowe dane słów kluczowych
- **Główne słowo kluczowe** i jego wariacje
- **Wolumen wyszukiwań** (miesięczny)
- **CPC** (koszt za kliknięcie w reklamach)
- **Trudność rankingu** (0-100)
- **Konkurencyjność** (niska/średnia/wysoka)

### Autouzupełnienie Google
- **Sugestie autouzupełnienia** dla każdego słowa kluczowego
- **Popularne wariacje** używane przez użytkowników
- **Długie frazy** (long-tail keywords)
- **Trendy wyszukiwań**

### People Also Ask (PAA)
- **Pytania użytkowników** związane z słowem kluczowym
- **Odpowiedzi** z wyników wyszukiwania
- **Potencjał content marketing** dla każdego pytania
- **Struktura FAQ** do optymalizacji

### Analiza SERP (pierwsza strona)
- **Domeny konkurencji** w TOP 10
- **Typy treści** (artykuły, sklepy, recenzje)
- **Featured snippets** i ich typy
- **Struktura wyników** (organiczne, PPC, mapy)

## Wymagania

### API i narzędzia
- Google Sheets API
- [SerpData.io](https://serpdata.io/) API do pobierania wyników wyszukiwania
- Web Scraping API do ekstrakcji danych SERP
- OpenAI API (opcjonalnie) do generowania wariacji

### Struktura danych wejściowych
Google Sheets powinien zawierać kolumny:
- `primary_keyword` - główne słowo kluczowe
- `language` - język (domyślnie: pl)
- `location` - lokalizacja (domyślnie: Poland)
- `depth` - głębokość analizy (1-3)

## Struktura wyników

### Arkusze Google Sheets
1. **Main Keywords** - główne słowa kluczowe z metadanymi
2. **Keyword Variations** - wariacje i sugestie
3. **Autocomplete Data** - dane autouzupełnienia
4. **People Also Ask** - pytania użytkowników
5. **SERP Analysis** - analiza pierwszej strony wyników
6. **Competitive Insights** - insights o konkurencji

### Kolumny w każdym arkuszu
- `keyword` - słowo kluczowe
- `search_volume` - wolumen wyszukiwań
- `cpc` - koszt za kliknięcie
- `difficulty` - trudność rankingu
- `competition` - konkurencyjność
- `trend` - trend wyszukiwań
- `serp_features` - cechy SERP (featured snippet, PAA, etc.)

## Konfiguracja

1. **Przygotuj listę głównych słów kluczowych** w Google Sheets
2. **Skonfiguruj połączenia API** (SerpData.io, Google Sheets)
3. **Ustaw parametry badania** (głębokość, język, lokalizacja)
4. **Skonfiguruj częstotliwość** uruchamiania

## Korzyści

### Oszczędność czasu
- **Godziny pracy** skrócone do sekund
- **Automatyczne formatowanie** danych
- **Gotowe do użycia** arkusze Google Sheets
- **Brak ręcznego kopiowania** danych

### Kompletność danych
- **Wszystkie potrzebne metadane** w jednym miejscu
- **Autouzupełnienie Google** - często pomijane przez narzędzia
- **PAA questions** - złoto dla content marketing
- **Analiza konkurencji** z pierwszej strony SERP

### Dla agencji SEO
- **Szybkie badania** dla klientów
- **Profesjonalne raporty** w formacie Google Sheets
- **Skalowalność** - obsługa wielu projektów
- **Konkurencyjna przewaga** w szybkości dostarczania

### Dla specjalistów digital marketing
- **Szybkie insights** dla strategii content
- **Identyfikacja szans** na ranking
- **Optymalizacja budżetów** reklamowych
- **Planowanie treści** na podstawie PAA

## Użycie

1. **Dodaj główne słowa kluczowe** do Google Sheets
2. **Uruchom automatyzację**
3. **Sprawdź wygenerowany arkusz** z wszystkimi danymi
4. **Wykorzystaj insights** do strategii SEO/content marketing
5. **Podejmij decyzje** na podstawie kompletnych danych

## Dlaczego wariacje słów kluczowych są kluczowe?

- **Pokrycie długiego ogona** - 70% ruchu organicznego
- **Niższa konkurencja** w wariacjach
- **Wyższe konwersje** z precyzyjnych fraz
- **Lepsze pozycjonowanie** w AI Mode Google

---

*Automatyzacja wymaga skonfigurowania kluczy API przed użyciem.* 