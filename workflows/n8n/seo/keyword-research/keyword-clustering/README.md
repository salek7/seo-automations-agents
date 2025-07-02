# Klasteryzacja słów kluczowych - N8N

## Opis automatyzacji

Automatyzacja do grupowania słów kluczowych na podstawie współwystępowania tych samych adresów URL w wynikach wyszukiwania Google. Słowa kluczowe, które prowadzą do podobnych stron, są grupowane w logiczne klastry.

## Funkcjonalności

### Główne możliwości:
- **Pobieranie wyników wyszukiwania** - automatyczne pobieranie URL-i z Google dla każdego słowa kluczowego
- **Analiza współwystępowania URL-i** - identyfikacja wspólnych domen i stron między słowami kluczowymi
- **Klasteryzacja na podstawie URL-i** - grupowanie słów kluczowych według podobieństwa wyników
- **Wizualizacja interaktywna** - dynamiczne wykresy i diagramy pokazujące relacje
- **Eksport wieloformatowy** - CSV, Excel, JSON, PDF

### Zaawansowane funkcje:
- **Analiza domen** - identyfikacja głównych domen w klastrach
- **Filtrowanie wyników** - usuwanie nieistotnych URL-i
- **Cluster optimization** - optymalizacja jakości grupowania
- **Competitive analysis** - porównanie z konkurencyjnymi stronami
- **Trend analysis** - analiza trendów w klastrach

## Architektura workflow

### Węzły N8N:
1. **HTTP Request** - pobieranie wyników wyszukiwania z Google
2. **Function** - wyciąganie URL-i z wyników wyszukiwania
3. **Function** - algorytm klasteryzacji (Jaccard Similarity)
4. **Google Sheets** - import/eksport danych
5. **Chart.js** - generowanie wizualizacji
6. **Email/Slack** - powiadomienia
7. **Webhook** - trigger automatyzacji

### Integracje:
- **Google Search API/SerpAPI** - pobieranie wyników wyszukiwania
- **Google Sheets** - zarządzanie danymi
- **Airtable** - baza danych klastrów
- **Slack/Teams** - komunikacja zespołu
- **Google Analytics** - analiza wydajności
- **Chart.js/D3.js** - wizualizacje

## Konfiguracja

### Wymagane API:
- Google Search API lub SerpAPI (klucz)
- Google Sheets API
- Airtable API (opcjonalnie)
- Slack/Teams API (opcjonalnie)

### Parametry konfiguracyjne:
- **Input data** - lista słów kluczowych
- **Number of search results** - liczba wyników do analizy (domyślnie 10)
- **Similarity threshold** - próg podobieństwa (0.1-1.0)
- **Min cluster size** - minimalna wielkość klastra
- **Domain filters** - filtry domen (opcjonalnie)

## Wyniki i raporty

### Format wyjściowy:
- **Structured clusters** - pogrupowane słowa kluczowe z nazwami
- **Wspólne URL-e** - lista adresów URL występujących w klastrze
- **Cluster metrics** - wielkość, gęstość, spójność
- **Visualization files** - PNG, SVG, HTML
- **Analytical report** - szczegółowa analiza

### Metryki wydajności:
- **Jaccard Index** - współczynnik podobieństwa między słowami kluczowymi
- **Cluster density** - gęstość URL-i w klastrze
- **Domain diversity** - różnorodność domen w klastrze
- **Search volume** - suma wolumenu wyszukiwań w klastrze

## Zastosowania biznesowe

### SEO i Marketing:
- **Content planning** - planowanie treści według klastrów
- **PPC campaigns** - organizacja kampanii reklamowych
- **Site structure** - optymalizacja struktury strony
- **Competitive analysis** - analiza konkurencji

### Content Strategy:
- **Topic clusters** - identyfikacja tematów głównych
- **Content gaps** - wykrywanie luk tematycznych
- **Audience targeting** - segmentacja odbiorców
- **Performance tracking** - śledzenie wydajności

## Instrukcja implementacji

### Krok 1: Przygotowanie danych
```javascript
// Przykład struktury danych wejściowych
const keywords = [
  { keyword: "najlepsze buty sportowe", volume: 1000 },
  { keyword: "buty do biegania", volume: 800 },
  // ...
];

// Przykład wyników wyszukiwania
const searchResults = {
  "najlepsze buty sportowe": [
    "https://example.com/best-sports-shoes",
    "https://competitor.com/sports-shoes",
    // ...
  ]
};
```

### Krok 2: Konfiguracja workflow
1. Skonfiguruj węzeł HTTP Request dla pobierania wyników wyszukiwania
2. Ustaw parametry API dla Google Search/SerpAPI
3. Skonfiguruj algorytm klasteryzacji (Jaccard Similarity)
4. Dodaj węzły eksportu i wizualizacji

### Krok 3: Uruchomienie i monitoring
1. Testuj na małym zbiorze danych
2. Dostosuj parametry klasteryzacji
3. Uruchom na pełnym zbiorze
4. Monitoruj wyniki i optymalizuj

## Optymalizacja wydajności

### Najlepsze praktyki:
- **Batch processing** - przetwarzanie wsadowe dużych zbiorów
- **Caching** - cache'owanie wyników analizy semantycznej
- **Parallel processing** - równoległe przetwarzanie klastrów
- **Error handling** - obsługa błędów i retry logic

### Monitoring:
- **API limits** - monitorowanie limitów Google Search/SerpAPI
- **Processing time** - śledzenie czasu przetwarzania
- **Quality metrics** - kontrola jakości klasteryzacji
- **Resource usage** - wykorzystanie zasobów

## Rozwiązywanie problemów

### Częste problemy:
- **Poor clustering quality** - dostosuj próg podobieństwa
- **API rate limits** - zaimplementuj rate limiting dla wyszukiwania
- **Memory issues** - przetwarzaj dane w batch'ach
- **Inconsistent results** - sprawdź jakość danych wejściowych

### Debugging:
- **Log analysis** - analiza logów workflow
- **Data validation** - walidacja danych wejściowych
- **Step-by-step testing** - testowanie pojedynczych węzłów
- **Performance profiling** - profilowanie wydajności

## Wymagania techniczne

- N8N instance (self-hosted lub cloud)
- Google Search API lub SerpAPI access
- Podstawowa znajomość JavaScript
- Dostęp do danych słów kluczowych
- Wystarczające zasoby obliczeniowe

## Wsparcie i dokumentacja

- N8N documentation
- Google Search API documentation
- SerpAPI documentation
- Community forums
- GitHub issues 