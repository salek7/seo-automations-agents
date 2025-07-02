# 🤝 Współtworzenie

Dziękujemy za zainteresowanie współtworzeniem Nodes Hub Automations! Ten plik zawiera wszystkie informacje potrzebne do dodania Twojej automatyzacji do repozytorium.

## 📋 Jak dodać swoją automatyzację?

### 1. Przygotowanie automatyzacji

#### Struktura plików
Każda automatyzacja powinna mieć następującą strukturę:

```
workflows/
├── make/
│   └── seo/
│       └── [kategoria]/
│           └── [nazwa-automatyzacji]/
│               ├── README.md          # Opis automatyzacji
│               ├── scenario.json      # Plik Make (opcjonalnie)
│               └── metadata.json      # Metadane (opcjonalnie)
└── n8n/
    └── seo/
        └── [kategoria]/
            └── [nazwa-automatyzacji]/
                ├── README.md          # Opis automatyzacji
                ├── workflow.json      # Plik N8N (opcjonalnie)
                └── metadata.json      # Metadane (opcjonalnie)
```

#### Kategorie SEO
- `keyword-research` - Badania słów kluczowych
- `competitor-analysis` - Analiza konkurencji
- `content-optimization` - Optymalizacja treści
- `technical-seo` - Techniczne SEO

### 2. Wymagania dla README.md

Każda automatyzacja musi mieć plik `README.md` z następującymi sekcjami:

#### Obowiązkowe sekcje:
```markdown
# 🎯 Nazwa automatyzacji

## Opis automatyzacji
Krótki opis tego, co robi automatyzacja (2-3 zdania).

## Jak działa?
1. Krok 1
2. Krok 2
3. Krok 3

## Wymagania
### API i narzędzia
- Lista wymaganych API i narzędzi

### Struktura danych wejściowych
Opis struktury danych wejściowych (Google Sheets, etc.)

## Konfiguracja
Instrukcje konfiguracji

## Wyniki
Opis wyników i struktury danych wyjściowych

## Użycie
Instrukcje użycia

## Korzyści
Lista korzyści z używania automatyzacji
```

#### Opcjonalne sekcje:
- `Przykłady` - Przykłady użycia
- `Troubleshooting` - Rozwiązywanie problemów
- `Limitations` - Ograniczenia

### 3. Nazewnictwo

#### Nazwy katalogów:
- Używaj `kebab-case` (np. `keyword-research`)
- Unikaj spacji i znaków specjalnych
- Używaj opisowych nazw

#### Nazwy plików:
- `README.md` - opis automatyzacji
- `scenario.json` - plik Make
- `workflow.json` - plik N8N
- `metadata.json` - metadane (opcjonalnie)

### 4. Jakość kodu

#### Wymagania:
- **Dokumentacja**: Każda automatyzacja musi być dobrze udokumentowana
- **Czytelność**: Kod powinien być czytelny i zrozumiały
- **Błędy**: Automatyzacja nie powinna zawierać błędów
- **Bezpieczeństwo**: Nie umieszczaj kluczy API w kodzie

#### Dobre praktyki:
- Dodaj komentarze w kodzie
- Używaj opisowych nazw zmiennych
- Testuj automatyzację przed dodaniem
- Sprawdź czy wszystkie API są dostępne

### 5. Proces dodawania

#### Krok 1: Fork repozytorium
1. Przejdź do [repozytorium](https://github.com/salek7/nodes_hub_automations)
2. Kliknij "Fork" w prawym górnym rogu
3. Sklonuj swoje forkowane repozytorium

#### Krok 2: Dodaj automatyzację
1. Utwórz nową gałąź: `git checkout -b feature/dodaj-automatyzacje`
2. Dodaj pliki automatyzacji w odpowiedniej strukturze
3. Zaktualizuj główny `README.md` (dodaj do tabeli)
4. Sprawdź czy wszystko działa

#### Krok 3: Testowanie
1. Przetestuj automatyzację w Make/N8N
2. Sprawdź czy README jest kompletne
3. Upewnij się, że nie ma błędów

#### Krok 4: Pull Request
1. Zatwierdź zmiany: `git commit -m "Dodano: [nazwa automatyzacji]"`
2. Wypchnij zmiany: `git push origin feature/dodaj-automatyzacje`
3. Utwórz Pull Request na GitHub
4. Opisz co zostało dodane w opisie PR

### 6. Szablon Pull Request

```markdown
## 🎯 Co zostało dodane?
Krótki opis automatyzacji

## 📁 Pliki dodane
- `workflows/make/seo/[kategoria]/[nazwa]/README.md`
- `workflows/n8n/seo/[kategoria]/[nazwa]/README.md`
- `workflows/make/seo/[kategoria]/[nazwa]/scenario.json` (opcjonalnie)
- `workflows/n8n/seo/[kategoria]/[nazwa]/workflow.json` (opcjonalnie)

## ✅ Co zostało sprawdzone?
- [ ] Automatyzacja działa w Make/N8N
- [ ] README jest kompletne
- [ ] Nie ma błędów w kodzie
- [ ] Główny README został zaktualizowany
- [ ] Nie ma kluczy API w kodzie

## 🧪 Jak przetestować?
Instrukcje testowania automatyzacji
```

### 7. Zasady

#### Dozwolone:
- ✅ Automatyzacje SEO dla Make i N8N
- ✅ Darmowe API i narzędzia
- ✅ Dobrze udokumentowane automatyzacje
- ✅ Przydatne dla społeczności SEO

#### Niedozwolone:
- ❌ Automatyzacje z płatnymi API (bez darmowych alternatyw)
- ❌ Automatyzacje niezwiązane z SEO
- ❌ Kod z błędami lub bez dokumentacji
- ❌ Klucze API w kodzie
- ❌ Automatyzacje naruszające prawa autorskie

### 8. Wsparcie

#### Potrzebujesz pomocy?
- Otwórz [Issue](https://github.com/salek7/nodes_hub_automations/issues)
- Sprawdź istniejące automatyzacje jako przykład
- Skontaktuj się z maintainerami

#### Przydatne linki:
- [Make Documentation](https://www.make.com/en/help)
- [N8N Documentation](https://docs.n8n.io/)
- [GitHub Guides](https://guides.github.com/)

---

**Dziękujemy za współtworzenie! 🚀** 