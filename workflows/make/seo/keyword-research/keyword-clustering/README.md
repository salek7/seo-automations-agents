# Klasteryzacja słów kluczowych - Make

## Opis automatyzacji

Automatyzacja do grupowania słów kluczowych na podstawie współwystępowania tych samych adresów URL w wynikach wyszukiwania Google. Słowa kluczowe, które prowadzą do podobnych stron, są grupowane w logiczne klastry.

## Funkcjonalności

### Główne możliwości:
- **Pobieranie wyników wyszukiwania** - automatyczne pobieranie URL-i z Google dla każdego słowa kluczowego
- **Analiza współwystępowania URL-i** - identyfikacja wspólnych domen i stron między słowami kluczowymi
- **Klasteryzacja na podstawie URL-i** - grupowanie słów kluczowych według podobieństwa wyników
- **Wizualizacja klastrów** - generowanie wykresów i diagramów pokazujących relacje
- **Eksport wyników** - zapisywanie klastrów do CSV, Excel lub JSON

### Dodatkowe funkcje:
- **Analiza domen** - identyfikacja głównych domen w klastrach
- **Filtrowanie wyników** - usuwanie nieistotnych URL-i
- **Analiza konkurencji** - porównanie z konkurencyjnymi stronami
- **Priorytetyzacja klastrów** - ranking według potencjału i wolumenu

## Struktura automatyzacji

### Moduły:
1. **Input Processing** - przetwarzanie listy słów kluczowych
2. **Search Results Scraping** - pobieranie wyników z Google dla każdego słowa kluczowego
3. **URL Extraction** - wyciąganie adresów URL z wyników wyszukiwania
4. **Similarity Analysis** - obliczanie podobieństwa między słowami kluczowymi na podstawie wspólnych URL-i
5. **Clustering Algorithm** - algorytm grupowania (Jaccard Similarity)
6. **Cluster Analysis** - analiza i walidacja klastrów
7. **Visualization** - generowanie wykresów
8. **Export** - eksport wyników

### Integracje:
- **Google Search API/SerpAPI** - pobieranie wyników wyszukiwania
- **Google Sheets** - import/eksport danych
- **Airtable** - zarządzanie klastrami
- **Slack/Teams** - powiadomienia o gotowych klastrach
- **Google Analytics** - analiza ruchu dla klastrów

## Konfiguracja

### Wymagane API:
- Google Search API lub SerpAPI (klucz)
- Google Sheets API (opcjonalnie)
- Airtable API (opcjonalnie)

### Parametry wejściowe:
- Lista słów kluczowych (CSV/Excel)
- Liczba wyników do analizy (domyślnie 10)
- Próg podobieństwa (0.1-1.0)
- Minimalna wielkość klastra
- Filtry domen (opcjonalnie)

## Wyniki

### Format wyjściowy:
- **Klastry z nazwami** - pogrupowane słowa kluczowe z opisami
- **Wspólne URL-e** - lista adresów URL występujących w klastrze
- **Statystyki klastrów** - wielkość, gęstość, jakość
- **Wizualizacje** - wykresy podobieństwa i hierarchii
- **Raport analityczny** - szczegółowe podsumowanie

### Metryki:
- **Jaccard Index** - współczynnik podobieństwa między słowami kluczowymi
- **Cluster density** - gęstość URL-i w klastrze
- **Domain diversity** - różnorodność domen w klastrze
- **Search volume** - suma wolumenu wyszukiwań w klastrze

## Zastosowania

### SEO:
- Organizacja kampanii PPC
- Planowanie treści
- Analiza nisz tematycznych
- Optymalizacja struktury strony

### Content Marketing:
- Planowanie kalendarza treści
- Identyfikacja luk tematycznych
- Analiza trendów
- Personalizacja treści

## Instrukcja użycia

1. **Przygotuj dane** - lista słów kluczowych w formacie CSV
2. **Skonfiguruj parametry** - ustaw próg podobieństwa i liczbę wyników
3. **Uruchom automatyzację** - wykonaj scenario w Make
4. **Przejrzyj klastry** - sprawdź jakość grupowania
5. **Eksportuj wyniki** - zapisz do wybranej platformy

## Wymagania techniczne

- Make.com account
- Google Search API lub SerpAPI access
- Podstawowa znajomość SEO
- Dostęp do danych słów kluczowych

## Wsparcie

W przypadku problemów z automatyzacją, sprawdź:
- Poprawność formatu danych wejściowych
- Konfigurację API keys dla wyszukiwania
- Limity API dla Google Search/SerpAPI
- Połączenie internetowe 