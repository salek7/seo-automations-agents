# 🚀 Nodes Hub Automations

**Darmowe automatyzacje SEO dla Make i N8N**

Kolekcja gotowych do użycia automatyzacji SEO, które pomogą Ci zoptymalizować procesy marketingowe i analityczne. Wszystkie automatyzacje są darmowe i gotowe do importu w Make (Integromat) i N8N.

## 🎯 Co znajdziesz w tym repozytorium?

### 📊 Automatyzacje SEO

| Nazwa | Kategoria | Make | N8N | Opis |
|-------|-----------|------|-----|------|
| [Generator struktury nagłówków](workflows/make/seo/content-optimization/header-structure-generator/) | Content Optimization | ✅ | [✅](workflows/n8n/seo/content-optimization/header-structure-generator/) | Generuje strukturę nagłówków na podstawie analizy konkurencji |
| [Generator Query Expansion & Fan-out](workflows/make/seo/keyword-research/query-expansion-generator/) | Keyword Research | ✅ | [✅](workflows/n8n/seo/keyword-research/query-expansion-generator/) | Generuje syntetyczne zapytania zgodnie z patentami Google |
| [Kompleksowe badania słów kluczowych](workflows/make/seo/keyword-research/comprehensive-keyword-research/) | Keyword Research | ✅ | [✅](workflows/n8n/seo/keyword-research/comprehensive-keyword-research/) | Pełne badania z 7 typami danych w strukturalnych arkuszach |
| [Klasyfikacja intencji słów kluczowych](workflows/make/seo/keyword-research/intent-classification/) | Keyword Research | ✅ | [✅](workflows/n8n/seo/keyword-research/intent-classification/) | Klasyfikuje słowa kluczowe według intencji użytkownika |
| [Monitor AI Overviews](workflows/make/seo/technical-seo/ai-overviews-monitor/) | Technical SEO | ✅ | [✅](workflows/n8n/seo/technical-seo/ai-overviews-monitor/) | Śledzi obecność w AI Overviews Google |
| [Szybkie badania słów kluczowych](workflows/make/seo/keyword-research/rapid-keyword-research/) | Keyword Research | ✅ | [✅](workflows/n8n/seo/keyword-research/rapid-keyword-research/) | Zastępuje godziny pracy sekundami automatyzacji |
| [Analizator Self-Saturation](workflows/make/seo/technical-seo/self-saturation-analyzer/) | Technical SEO | ✅ | [✅](workflows/n8n/seo/technical-seo/self-saturation-analyzer/) | Ocenia szanse na organiczne wyniki vs self-saturation |
| [Deep Research Agent](workflows/make/seo/keyword-research/deep-research-agent/) | Keyword Research | ✅ | [✅](workflows/n8n/seo/keyword-research/deep-research-agent/) | Agent wieloetapowych badań jak ChatGPT Deep Research |

### 🛠️ Narzędzia
- **Make (Integromat)** - gotowe scenariusze do importu
- **N8N** - workflow'y do skopiowania

### 🤖 Integracja z AI Asystentami (MCP)

Wszystkie automatyzacje można wykorzystać z AI asystentami poprzez MCP (Model Context Protocol) serwery:

#### Make MCP Server
- **Oficjalny MCP Server** od Make: [developers.make.com/mcp-server](https://developers.make.com/mcp-server)
- **Funkcje**: Uruchamianie scenariuszy "On Demand" jako narzędzi dla AI
- **Korzyści**: 
  - Scenariusze jako callable tools dla AI
  - Dwukierunkowa komunikacja między AI a automatyzacjami
  - Dostępne na wszystkich planach (w tym darmowym)

#### N8N MCP Servers
- **[mcp-n8n-builder](https://github.com/spences10/mcp-n8n-builder)** - Programatyczne tworzenie i zarządzanie workflow'ami
- **[n8n-mcp](https://github.com/czlonkowski/n8n-mcp)** - Alternatywny MCP server dla N8N
- **Funkcje**: 
  - Tworzenie, modyfikacja i zarządzanie workflow'ami
  - Walidacja schematów i typów node'ów
  - Inteligentne sugestie dla podobnych typów node'ów
  - Zarządzanie wykonaniami workflow'ów

**Przykład użycia**: AI asystent może automatycznie modyfikować automatyzacje SEO na podstawie Twoich wymagań, dodając nowe funkcjonalności lub dostosowując istniejące workflow'y.

## 📁 Struktura repozytorium

```
workflows/
├── make/           # Automatyzacje dla Make
│   └── seo/        # Kategoria SEO
│       ├── keyword-research/
│       ├── competitor-analysis/
│       ├── content-optimization/
│       └── technical-seo/
└── n8n/            # Automatyzacje dla N8N
    └── seo/        # Kategoria SEO
        ├── keyword-research/
        ├── competitor-analysis/
        ├── content-optimization/
        └── technical-seo/
```

## 🚀 Szybki start

### Dla Make (Integromat)
1. Przejdź do katalogu `workflows/make/seo/`
2. Wybierz interesującą Cię automatyzację
3. Pobierz plik JSON
4. Zaimportuj w Make: **Settings → Import → Upload JSON**

### Dla N8N
1. Przejdź do katalogu `workflows/n8n/seo/`
2. Wybierz interesujący Cię workflow
3. Skopiuj zawartość JSON
4. Wklej w N8N: **Import from JSON**

## 📚 Dokumentacja

- [📖 Instrukcje instalacji](docs/installation-guides/)
- [📋 Instrukcje użycia](docs/usage-guides/)
- [💡 Przykłady](docs/examples/)

## 🤝 Współtworzenie

Chcesz dodać swoją automatyzację? Sprawdź [CONTRIBUTING.md](CONTRIBUTING.md)!

## 📝 Licencja

Wszystkie automatyzacje są dostępne na licencji MIT - możesz je używać komercyjnie i modyfikować według potrzeb.

## ⭐ Wsparcie

Jeśli projekt Ci się podoba, daj gwiazdkę! ⭐

---

**Tworzone z ❤️ dla społeczności SEO** 