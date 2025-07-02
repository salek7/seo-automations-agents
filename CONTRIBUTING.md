# 🤝 Contributing

Thank you for your interest in contributing to SEO Automations and Agents! This file contains all the information needed to add your automation to the repository.

## 📋 How to add your automation?

### 1. Preparing the automation

#### File structure
Each automation should have the following structure:

```
workflows/
├── make/
│   └── seo/
│       └── [kategoria]/
│           └── [nazwa-automatyzacji]/
│               ├── README.md          # Opis automatyzacji
│               ├── scenario.json      # Plik Make (opcjonalnie)
│               └── metadata.json      # Metadane (opcjonalnie)
├── n8n/
│   └── seo/
│       └── [kategoria]/
│           └── [nazwa-automatyzacji]/
│               ├── README.md          # Opis automatyzacji
│               ├── workflow.json      # Plik N8N (opcjonalnie)
│               └── metadata.json      # Metadane (opcjonalnie)
└── colab/
    └── seo/
        └── [kategoria]/
            └── [nazwa-automatyzacji]/
                ├── README.md          # Opis automatyzacji
                ├── notebook.ipynb     # Plik Google Colab (opcjonalnie)
                └── metadata.json      # Metadane (opcjonalnie)
```

#### SEO Categories
- `keyword-research` - Keyword research
- `competitor-analysis` - Competitor analysis
- `content-optimization` - Content optimization
- `technical-seo` - Technical SEO

### 2. Requirements for README.md

Each automation must have a `README.md` file with the following sections:

#### Required sections:
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

#### Optional sections:
- `Examples` - Usage examples
- `Troubleshooting` - Problem solving
- `Limitations` - Limitations

### 3. Naming

#### Directory names:
- Use `kebab-case` (e.g., `keyword-research`)
- Avoid spaces and special characters
- Use descriptive names

#### File names:
- `README.md` - automation description
- `scenario.json` - Make file
- `workflow.json` - N8N file
- `notebook.ipynb` - Google Colab notebook
- `metadata.json` - metadata (optional)

### 4. Code Quality

#### Requirements:
- **Documentation**: Each automation must be well documented
- **Readability**: Code should be readable and understandable
- **Errors**: Automation should not contain errors
- **Security**: Do not place API keys in code

#### Best practices:
- Add comments in code
- Use descriptive variable names
- Test automation before adding
- Check if all APIs are available

### 5. Adding process

#### Step 1: Fork the repository
1. Go to the [repository](https://github.com/salek7/seo-automations-agents)
2. Click "Fork" in the top right corner
3. Clone your forked repository

#### Step 2: Add automation
1. Create a new branch: `git checkout -b feature/add-automation`
2. Add automation files in the appropriate structure
3. Update the main `README.md` (add to table)
4. Check if everything works

#### Step 3: Testing
1. Test the automation in Make/N8N
2. Check if README is complete
3. Make sure there are no errors

#### Step 4: Pull Request
1. Commit changes: `git commit -m "Added: [automation name]"`
2. Push changes: `git push origin feature/add-automation`
3. Create Pull Request on GitHub
4. Describe what was added in the PR description

### 6. Pull Request Template

```markdown
## 🎯 What was added?
Brief description of automation

## 📁 Files added
- `workflows/make/seo/[category]/[name]/README.md`
- `workflows/n8n/seo/[category]/[name]/README.md`
- `workflows/make/seo/[category]/[name]/scenario.json` (optional)
- `workflows/n8n/seo/[category]/[name]/workflow.json` (optional)

## ✅ What was checked?
- [ ] Automation works in Make/N8N
- [ ] README is complete
- [ ] No errors in code
- [ ] Main README was updated
- [ ] No API keys in code

## 🧪 How to test?
Instructions for testing automation
```

### 7. Rules

#### Allowed:
- ✅ SEO automations for Make, N8N, and Google Colab
- ✅ Free APIs and tools
- ✅ Well-documented automations
- ✅ Useful for SEO community

#### Not allowed:
- ❌ Automations with paid APIs (without free alternatives)
- ❌ Automations unrelated to SEO
- ❌ Code with errors or without documentation
- ❌ API keys in code
- ❌ Automations violating copyright

### 8. Support

#### Need help?
- Open an [Issue](https://github.com/salek7/seo-automations-agents/issues)
- Check existing automations as examples
- Contact maintainers

#### Useful links:
- [Make Documentation](https://www.make.com/en/help)
- [N8N Documentation](https://docs.n8n.io/)
- [Google Colab Documentation](https://colab.research.google.com/notebooks/)
- [GitHub Guides](https://guides.github.com/)

---

**Thank you for contributing! 🚀** 