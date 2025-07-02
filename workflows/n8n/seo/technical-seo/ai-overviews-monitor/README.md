# 🤖 Monitor AI Overviews (N8N)

## Opis automatyzacji

Workflow N8N śledzi obecność Twojej strony w AI Overviews Google - nowym formacie wyników wyszukiwania, którego tradycyjne narzędzia SEO jeszcze nie monitorują. Wykorzystuje [SerpData.io](https://serpdata.io/) do pobierania wyników i analizuje zawartość AI Overviews.

## Jak działa?

1. **Pobiera listę słów kluczowych** z Google Sheets (z GSC lub ręcznych badań)
2. **Pobiera wyniki wyszukiwania** dla każdego słowa kluczowego z SerpData.io
3. **Wykrywa AI Overviews** w wynikach wyszukiwania
4. **Ekstrahuje zawartość AI Overview** i źródła referencyjne
5. **Sprawdza obecność Twojej strony** w AI Overviews
6. **Loguje wszystko** w strukturalnym arkuszu Google Sheets

## Co to są AI Overviews?

AI Overviews to nowy format wyników Google, który:
- **Automatycznie generuje** podsumowania na podstawie wielu źródeł
- **Wyświetla się na górze** wyników wyszukiwania
- **Zawiera linki** do źródłowych stron
- **Jest dynamiczny** i zmienia się w czasie
- **Nie jest jeszcze monitorowany** przez tradycyjne narzędzia SEO

## Wymagania

### API i narzędzia
- Google Sheets node
- HTTP Request node ([SerpData.io](https://serpdata.io/) API)
- HTTP Request node (Web Scraping API - opcjonalnie)
- Google Sheets node (zapis wyników)

### Struktura danych wejściowych
Google Sheets powinien zawierać kolumny:
- `keyword` - słowo kluczowe do monitorowania
- `target_domain` - Twoja domena (np. example.com)
- `language` - język (domyślnie: pl)
- `location` - lokalizacja (domyślnie: Poland)

## Co monitoruje workflow?

### Obecność AI Overviews
- **Czy AI Overview** pojawia się dla danego słowa kluczowego
- **Pozycja AI Overview** w wynikach wyszukiwania
- **Typ AI Overview** (tekst, lista, tabela, etc.)

### Zawartość AI Overview
- **Główny tekst** AI Overview
- **Struktura** (nagłówki, listy, tabele)
- **Długość** zawartości
- **Tematyka** i kontekst

### Źródła referencyjne
- **Lista wszystkich źródeł** użytych w AI Overview
- **Domeny źródłowe** i ich pozycje
- **Linki do konkretnych stron** źródłowych
- **Czy Twoja strona** jest wśród źródeł

### Analiza konkurencji
- **Które strony** najczęściej pojawiają się jako źródła
- **Typy treści** preferowane przez AI Overviews
- **Strategie** konkurencji w AI Overviews

## Konfiguracja

1. **Przygotuj listę słów kluczowych** w Google Sheets
2. **Skonfiguruj połączenia** (SerpData.io, Google Sheets)
3. **Ustaw domenę docelową** do monitorowania
4. **Skonfiguruj trigger** (ręczny lub czasowy)

## Wyniki

Workflow generuje:
- **Raport obecności** w AI Overviews
- **Analizę zawartości** AI Overviews
- **Listę źródeł referencyjnych**
- **Statystyki konkurencji**
- **Rekomendacje** optymalizacji

### Kolumny wynikowe
- `keyword` - słowo kluczowe
- `ai_overview_present` - czy AI Overview jest obecny (Tak/Nie)
- `ai_overview_position` - pozycja AI Overview (1, 2, 3, etc.)
- `ai_overview_content` - główna zawartość AI Overview
- `ai_overview_type` - typ AI Overview (tekst, lista, tabela)
- `your_domain_present` - czy Twoja domena jest w źródłach (Tak/Nie)
- `source_domains` - lista domen źródłowych
- `source_links` - linki do stron źródłowych
- `monitored_at` - data monitorowania

## Użycie

1. **Dodaj słowa kluczowe** do Google Sheets
2. **Ustaw swoją domenę** do monitorowania
3. **Uruchom workflow**
4. **Sprawdź raport** w arkuszu wyników
5. **Analizuj szanse** na pojawienie się w AI Overviews

## Korzyści

### Dla SEO
- **Monitorowanie nowego formatu** wyników Google
- **Identyfikacja szans** na pojawienie się w AI Overviews
- **Analiza konkurencji** w AI Overviews
- **Optymalizacja treści** pod AI Overviews

### Dla content marketing
- **Zrozumienie preferencji** AI Overviews
- **Dostosowanie treści** do formatu AI
- **Identyfikacja tematów** z potencjałem AI Overviews
- **Strategia link building** dla AI Overviews

### Dla digital marketing
- **Nowe możliwości** zwiększenia widoczności
- **Analiza trendów** w wynikach wyszukiwania
- **Konkurencyjna analiza** w czasie rzeczywistym
- **Raportowanie** dla klientów

## Dlaczego to ważne?

- **AI Overviews rośnie** - coraz więcej zapytań ma AI Overviews
- **Tradycyjne narzędzia nie monitorują** tego formatu
- **Nowe możliwości** zwiększenia widoczności
- **Konkurencyjna przewaga** w monitorowaniu

---

*Workflow wymaga skonfigurowania kluczy API przed użyciem.* 