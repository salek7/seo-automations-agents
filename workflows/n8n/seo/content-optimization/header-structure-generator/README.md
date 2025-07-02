# 📝 Generator struktury nagłówków (N8N)

## Opis automatyzacji

Workflow N8N generuje optymalną strukturę nagłówków dla artykułów SEO na podstawie analizy treści konkurencji.

## Jak działa?

1. **Pobiera słowa kluczowe** z Google Sheets
2. **Analizuje wyniki wyszukiwania** dla każdego słowa kluczowego
3. **Pobiera treści** z TOP wyników konkurencji
4. **Analizuje strukturę nagłówków** w treściach konkurencji
5. **Generuje listę nagłówków** za pomocą modelu językowego
6. **Zapisuje wyniki** do Google Sheets

## Wymagania

### API i narzędzia
- Google Sheets node
- HTTP Request node ([SerpData.io](https://serpdata.io/) API)
- HTTP Request node (OpenAI API)
- Web Scraping node
- Google Sheets node (zapis wyników)

### Struktura danych wejściowych
Google Sheets powinien zawierać kolumny:
- `keyword` - słowo kluczowe do analizy
- `url` - URL strony docelowej (opcjonalnie)

## Konfiguracja

1. Skonfiguruj połączenia z Google Sheets
2. Ustaw klucze API (SerpAPI, OpenAI)
3. Skonfiguruj parametry generowania
4. Ustaw trigger (ręczny lub czasowy)

## Wyniki

Workflow generuje:
- Listę nagłówków H1, H2, H3
- Sugestie struktury artykułu
- Analizę pokrycia słów kluczowych
- Rekomendacje optymalizacji

## Użycie

1. Dodaj słowa kluczowe do Google Sheets
2. Uruchom workflow
3. Sprawdź wygenerowaną strukturę w arkuszu wyników
4. Dostosuj nagłówki według potrzeb

---

*Workflow wymaga skonfigurowania kluczy API przed użyciem.* 