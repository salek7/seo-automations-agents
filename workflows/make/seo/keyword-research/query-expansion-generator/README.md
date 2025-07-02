# 🔍 Generator Query Expansion & Fan-out

## Opis automatyzacji

Automatyzacja generuje syntetyczne zapytania (Query Fan-out) na podstawie głównych słów kluczowych, wykorzystując różne typy ekspansji zapytań zgodnie z najnowszymi patentami Google.

## Jak działa?

1. **Pobiera główne słowa kluczowe** z Google Sheets
2. **Generuje syntetyczne zapytania** używając różnych typów ekspansji:
   - Related Queries (zapytania powiązane)
   - Implicit Queries (zapytania ukryte)
   - Comparative Queries (zapytania porównawcze)
   - Recent Queries (zapytania kontekstowe)
   - Personalized Queries (zapytania spersonalizowane)
   - Reformulation Queries (zapytania przeformułowane)
   - Entity-Expanded Queries (zapytania z ekspansją encji)
3. **Analizuje wyniki wyszukiwania** dla każdego syntetycznego zapytania
4. **Oblicza widoczność** w AI Mode dla każdego zapytania
5. **Tworzy macierz zapytań** z ocenami widoczności
6. **Zapisuje wyniki** do Google Sheets

## Wymagania

### API i narzędzia
- Google Sheets API
- [SerpData.io](https://serpdata.io/) API do pobierania wyników wyszukiwania
- OpenAI API (lub podobne) do generowania syntetycznych zapytań
- Embedding API do analizy semantycznej

### Struktura danych wejściowych
Google Sheets powinien zawierać kolumny:
- `primary_keyword` - główne słowo kluczowe
- `category` - kategoria tematyczna (opcjonalnie)
- `target_location` - lokalizacja docelowa (opcjonalnie)

## Typy syntetycznych zapytań

### Related Queries
Zapytania semantycznie lub kategorycznie powiązane z oryginalnym zapytaniem.

### Implicit Queries
Zapytania wywnioskowane z intencji użytkownika - co użytkownik prawdopodobnie miał na myśli.

### Comparative Queries
Zapytania porównujące produkty, encje lub opcje.

### Recent Queries
Zapytania kontekstowe bazujące na historii wyszukiwań użytkownika.

### Personalized Queries
Zapytania dostosowane do konkretnych zainteresowań, lokalizacji lub historii użytkownika.

### Reformulation Queries
Przeformułowania leksykalne lub składniowe zachowujące główną intencję.

### Entity-Expanded Queries
Zapytania z ekspansją encji na podstawie relacji w Knowledge Graph.

## Konfiguracja

1. Skonfiguruj połączenia z API
2. Ustaw parametry generowania dla każdego typu zapytania
3. Skonfiguruj filtry różnorodności i kategoryzacji
4. Ustaw częstotliwość uruchamiania

## Wyniki

Automatyzacja generuje:
- Macierz syntetycznych zapytań z ocenami widoczności
- Analizę pokrycia różnych typów zapytań
- Rekomendacje optymalizacji treści
- Mapę szans na widoczność w AI Mode

## Użycie

1. Dodaj główne słowa kluczowe do Google Sheets
2. Uruchom automatyzację
3. Przeanalizuj macierz zapytań w arkuszu wyników
4. Dostosuj strategię treści na podstawie wyników

## Znaczenie dla SEO

- Ranking #1 dla głównego zapytania daje tylko 25% szans na widoczność w AI Mode
- Konieczne jest rankingowanie dla wielu potencjalnych podzapytań
- Treść musi być semantycznie gęsta i dobrze dopasowana do zróżnicowanych intencji
- Należy inżynierować relewancję nie tylko dla głównych terminów, ale dla rozszerzonej przestrzeni zapytań

---

*Automatyzacja wymaga skonfigurowania kluczy API przed użyciem.* 