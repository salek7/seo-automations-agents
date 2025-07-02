# 📝 Generator struktury nagłówków

## Opis automatyzacji

Automatyzacja generuje optymalną strukturę nagłówków dla artykułów SEO na podstawie analizy treści konkurencji.

## Jak działa?

1. **Pobiera słowa kluczowe** z Google Sheets
2. **Analizuje wyniki wyszukiwania** dla każdego słowa kluczowego
3. **Pobiera treści** z TOP wyników konkurencji
4. **Analizuje strukturę nagłówków** w treściach konkurencji
5. **Generuje listę nagłówków** za pomocą modelu językowego
6. **Zapisuje wyniki** do Google Sheets

## Wymagania

### API i narzędzia
- Google Sheets API
- [SerpData.io](https://serpdata.io/) API do pobierania wyników wyszukiwania
- OpenAI API (lub podobne) do generowania nagłówków
- Web Scraping API do pobierania treści

### Struktura danych wejściowych
Google Sheets powinien zawierać kolumny:
- `keyword` - słowo kluczowe do analizy
- `url` - URL strony docelowej (opcjonalnie)

## Konfiguracja

1. Skonfiguruj połączenia z API
2. Ustaw ID arkusza Google Sheets
3. Skonfiguruj parametry generowania (liczba nagłówków, styl)
4. Ustaw częstotliwość uruchamiania

## Wyniki

Automatyzacja generuje:
- Listę nagłówków H1, H2, H3
- Sugestie struktury artykułu
- Analizę pokrycia słów kluczowych
- Rekomendacje optymalizacji

## Użycie

1. Dodaj słowa kluczowe do Google Sheets
2. Uruchom automatyzację
3. Sprawdź wygenerowaną strukturę w arkuszu wyników
4. Dostosuj nagłówki według potrzeb

---

*Automatyzacja wymaga skonfigurowania kluczy API przed użyciem.* 