# 🔍 Kompleksowe badania słów kluczowych

## Opis automatyzacji

Automatyzacja przeprowadza kompleksowe badania słów kluczowych wykorzystując [SerpData.io](https://serpdata.io/) API. Tworzy dedykowany plik badań w nowym folderze Google Drive na podstawie szablonu z Google Sheets.

## Jak działa?

1. **Pobiera parametry początkowe** z szablonu Google Sheets
2. **Tworzy nowy folder** w Google Drive dla projektu
3. **Kopiuje szablon** do nowego folderu
4. **Pobiera dane słów kluczowych** z SerpData.io:
   - Powiązane słowa kluczowe
   - Sugestie słów kluczowych
   - Pomysły na słowa kluczowe
   - Autouzupełnienie
   - Podtematy
   - Wyniki SERP
   - "Ludzie pytają również" (PAA)
5. **Organizuje dane** w strukturalnych arkuszach Google Sheets
6. **Tworzy podsumowanie** w głównym arkuszu

## Wymagania

### API i narzędzia
- Google Sheets API
- Google Drive API
- [SerpData.io](https://serpdata.io/) API
- OpenAI API (dla dodatkowych sugestii)

### Struktura danych wejściowych
Google Sheets szablon powinien zawierać:
- `primary_keyword` - główne słowo kluczowe
- `language` - język (domyślnie: pl)
- `location` - lokalizacja (domyślnie: Poland)
- `depth` - głębokość analizy (1-3)

## Struktura wyników

### Arkusze Google Sheets
1. **Related Keywords** - powiązane słowa kluczowe
2. **Keyword Suggestions** - sugestie słów kluczowych
3. **Keyword Ideas** - pomysły na słowa kluczowe
4. **Autocomplete** - autouzupełnienie
5. **Subtopics** - podtematy
6. **SERP Analysis** - analiza wyników wyszukiwania
7. **People Also Ask** - pytania użytkowników
8. **Master Summary** - główne podsumowanie

### Kolumny w każdym arkuszu
- `keyword` - słowo kluczowe
- `search_volume` - wolumen wyszukiwań
- `difficulty` - trudność rankingu
- `cpc` - koszt za kliknięcie
- `competition` - konkurencyjność
- `trend` - trend wyszukiwań
- `related_terms` - powiązane terminy

## Konfiguracja

1. **Przygotuj szablon Google Sheets** z parametrami wejściowymi
2. **Skonfiguruj połączenia API** (SerpData.io, Google Sheets, Google Drive)
3. **Ustaw parametry badań** (głębokość, język, lokalizacja)
4. **Skonfiguruj częstotliwość** uruchamiania (ręcznie lub automatycznie)

## Korzyści

### Dla zespołów marketingowych
- **Automatyczne generowanie** pomysłów na treści
- **Analiza konkurencji** i szans na ranking
- **Optymalizacja budżetów** reklamowych
- **Raportowanie** wydajności słów kluczowych

### Dla zespołów sprzedażowych
- **Dostosowanie ofert** do wyszukiwań klientów
- **Identyfikacja** intencji zakupowych
- **Optymalizacja** procesów sprzedażowych

## Użycie

1. **Przygotuj szablon** z głównymi słowami kluczowymi
2. **Uruchom automatyzację**
3. **Sprawdź wygenerowany plik** w Google Drive
4. **Przeanalizuj wyniki** w poszczególnych arkuszach
5. **Wykorzystaj insights** do strategii content marketing

## Harmonogram i współpraca

- **Regularne uruchamianie** - automatyczne badania co tydzień/miesiąc
- **Współpraca cross-funkcyjna** - dostęp dla zespołów marketingowych i sprzedażowych
- **Pomiar wydajności** - śledzenie zmian pozycji słów kluczowych
- **Ciągła optymalizacja** - dostosowanie strategii na podstawie wyników

## Wyniki

Automatyzacja generuje:
- **Kompletny raport** badań słów kluczowych
- **Strukturalne dane** w Google Sheets
- **Analizę konkurencji** i szans na ranking
- **Rekomendacje** dla content marketing
- **Insights** dla zespołów sprzedażowych

---

*Automatyzacja wymaga skonfigurowania kluczy API przed użyciem.* 