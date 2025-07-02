# 🎯 Klasyfikacja intencji słów kluczowych (N8N)

## Opis automatyzacji

Workflow N8N klasyfikuje słowa kluczowe według ich intencji użytkownika na podstawie analizy wyników wyszukiwania Google. Wykorzystuje [SerpData.io](https://serpdata.io/) do pobierania wyników i AI do klasyfikacji.

## Jak działa?

1. **Pobiera listę słów kluczowych** z Google Sheets
2. **Pobiera wyniki wyszukiwania** dla każdego słowa kluczowego z SerpData.io
3. **Analizuje strukturę wyników** (typy wyników, featured snippets, PAA)
4. **Klasyfikuje intencję** używając modelu AI
5. **Kategoryzuje słowa kluczowe** według typów intencji
6. **Zapisuje wyniki** do Google Sheets z oceną pewności

## Typy intencji

### 🔍 Informational (Informacyjne)
Użytkownik szuka informacji, definicji, wyjaśnień.
- **Przykłady:** "co to jest", "jak działa", "definicja"
- **Wyniki:** Artykuły, definicje, tutoriale, Wikipedia
- **Featured snippets:** Częste

### 🛒 Commercial (Komercyjne)
Użytkownik rozważa zakup, porównuje opcje.
- **Przykłady:** "najlepszy", "porównanie", "recenzja"
- **Wyniki:** Recenzje, porównania, rankingi
- **Featured snippets:** Częste

### 💰 Transactional (Transakcyjne)
Użytkownik chce dokonać zakupu lub konkretnej akcji.
- **Przykłady:** "kup", "cena", "zamów", "sklep"
- **Wyniki:** Sklepy, cenniki, formularze zamówień
- **Featured snippets:** Rzadkie

### 🧭 Navigational (Nawigacyjne)
Użytkownik szuka konkretnej strony lub marki.
- **Przykłady:** "nazwa firmy", "facebook", "kontakt"
- **Wyniki:** Oficjalne strony, social media
- **Featured snippets:** Bardzo rzadkie

### 🔧 Local (Lokalne)
Użytkownik szuka usług lub produktów w swojej okolicy.
- **Przykłady:** "warszawa", "blisko mnie", "otwarte"
- **Wyniki:** Mapy, lokalne firmy, godziny otwarcia
- **Featured snippets:** Częste

## Wymagania

### API i narzędzia
- Google Sheets node
- HTTP Request node ([SerpData.io](https://serpdata.io/) API)
- HTTP Request node (OpenAI API)
- HTTP Request node (Embedding API)
- Google Sheets node (zapis wyników)

### Struktura danych wejściowych
Google Sheets powinien zawierać kolumny:
- `keyword` - słowo kluczowe do klasyfikacji
- `language` - język (domyślnie: pl)
- `location` - lokalizacja (domyślnie: Poland)

## Algorytm klasyfikacji

### Analiza wyników SERP
1. **Typy wyników** - organiczne, PPC, mapy, video, shopping
2. **Featured snippets** - obecność i typ
3. **People Also Ask** - pytania użytkowników
4. **Struktura danych** - recenzje, ceny, lokalizacje
5. **Domeny** - typy stron (sklepy, blogi, encyklopedie)

### Model AI
- **Prompt engineering** dla klasyfikacji intencji
- **Context window** z wynikami wyszukiwania
- **Confidence score** dla każdej klasyfikacji
- **Fallback logic** dla niepewnych przypadków

## Konfiguracja

1. **Przygotuj listę słów kluczowych** w Google Sheets
2. **Skonfiguruj połączenia** (SerpData.io, OpenAI)
3. **Ustaw parametry klasyfikacji** (język, lokalizacja)
4. **Skonfiguruj trigger** (ręczny lub czasowy)

## Wyniki

Workflow generuje:
- **Klasyfikację intencji** dla każdego słowa kluczowego
- **Ocenę pewności** klasyfikacji (0-100%)
- **Analizę struktury SERP** (typy wyników)
- **Rekomendacje** dla strategii content marketing
- **Statystyki** rozkładu intencji

### Kolumny wynikowe
- `keyword` - słowo kluczowe
- `intent_type` - typ intencji (Informational/Commercial/Transactional/Navigational/Local)
- `confidence_score` - ocena pewności (0-100%)
- `serp_features` - cechy SERP (featured snippet, PAA, maps, etc.)
- `content_recommendation` - rekomendacja typu treści
- `classified_at` - data klasyfikacji

## Użycie

1. **Dodaj słowa kluczowe** do Google Sheets
2. **Uruchom workflow**
3. **Przeanalizuj klasyfikacje** w arkuszu wyników
4. **Dostosuj strategię treści** na podstawie intencji
5. **Zoptymalizuj** content marketing dla każdego typu intencji

## Korzyści

### Dla content marketing
- **Dopasowanie treści** do intencji użytkowników
- **Optymalizacja konwersji** dla różnych typów zapytań
- **Planowanie content calendar** według intencji
- **A/B testing** różnych podejść

### Dla SEO
- **Struktura treści** dostosowana do intencji
- **Optymalizacja meta tagów** według typu zapytania
- **Internal linking** bazujący na intencji
- **Featured snippet optimization**

---

*Workflow wymaga skonfigurowania kluczy API przed użyciem.* 