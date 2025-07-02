# 🎯 Automation Name

## Automation Description
Brief description of what the automation does (2-3 sentences).

## How it works?
1. **Step 1** - description of first step
2. **Step 2** - description of second step
3. **Step 3** - description of third step
4. **Step 4** - description of fourth step

## Requirements

### APIs and Tools
- [SerpData.io](https://serpdata.io/) API for search
- Google Sheets API for data management
- OpenAI API for analysis and content generation
- Web Scraping API for content retrieval
- [Other required APIs]

### Input Data Structure
Google Sheets should contain columns:
- `keyword` - keyword to analyze
- `domain` - domain to analyze
- `language` - search language
- `country` - search country

## Konfiguracja

1. **Skonfiguruj API klucze** w Make/N8N
2. **Przygotuj Google Sheets** z danymi wejściowymi
3. **Ustaw parametry** automatyzacji
4. **Przetestuj** na małym zestawie danych

## Wyniki

Automatyzacja generuje:
- **Analizę konkurencji** z TOP 10 wyników
- **Strukturę nagłówków** na podstawie analizy
- **Rekomendacje** optymalizacji treści
- **Raport** w formacie PDF/Google Docs

### Struktura danych wyjściowych
- `keyword` - oryginalne słowo kluczowe
- `competitors` - lista konkurentów
- `header_structure` - proponowana struktura nagłówków
- `recommendations` - rekomendacje optymalizacji
- `report_url` - link do pełnego raportu
- `completed_at` - data zakończenia analizy

## Użycie

1. **Dodaj słowa kluczowe** do Google Sheets
2. **Uruchom automatyzację**
3. **Poczekaj** na zakończenie analizy
4. **Pobierz raport** z wynikami
5. **Zastosuj rekomendacje** w swojej treści

## Korzyści

### Dla SEO specjalistów
- **Oszczędność czasu** - automatyzacja analizy konkurencji
- **Lepsze wyniki** - oparte na danych rekomendacje
- **Skalowalność** - analiza wielu słów kluczowych
- **Standaryzacja** - jednolity proces analizy

### Dla firm
- **Konkurencyjna przewaga** - lepsze pozycjonowanie
- **Optymalizacja treści** - wyższe pozycje w Google
- **ROI** - szybsze osiąganie celów SEO
- **Automatyzacja** - mniej pracy manualnej

## Przykłady

### Przykład 1: Analiza słowa kluczowego "SEO tools"
```
Input: "SEO tools"
Output: 
- 5 konkurentów z TOP 10
- Struktura nagłówków: H1, H2, H3
- Rekomendacje: dodaj sekcję "Porównanie narzędzi"
```

### Przykład 2: Analiza domeny konkurencyjnej
```
Input: "example.com"
Output:
- Analiza 10 stron konkurencji
- Wzorce struktury treści
- Rekomendacje optymalizacji
```

## Troubleshooting

### Problem: Błąd API
**Rozwiązanie**: Sprawdź czy klucz API jest poprawny i ma odpowiednie uprawnienia.

### Problem: Brak wyników
**Rozwiązanie**: Sprawdź czy słowo kluczowe jest poprawne i czy API zwraca wyniki.

### Problem: Błąd Google Sheets
**Rozwiązanie**: Sprawdź czy struktura danych wejściowych jest poprawna.

## Limitations

- **Ograniczenia API** - maksymalnie 100 zapytań dziennie
- **Języki** - obsługuje tylko angielski i polski
- **Domeny** - maksymalnie 10 domen na raz
- **Czas wykonania** - może trwać do 5 minut

## Wsparcie

Potrzebujesz pomocy? Sprawdź:
- [Dokumentacja API](https://serpdata.io/docs)
- [Make Help Center](https://www.make.com/en/help)
- [N8N Documentation](https://docs.n8n.io/)

---

*Automatyzacja wymaga skonfigurowania kluczy API przed użyciem.* 