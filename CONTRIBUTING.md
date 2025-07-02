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
│       └── [category]/
│           └── [automation-name]/
│               ├── README.md          # Automation description
│               ├── scenario.json      # Make file (optional)
│               └── metadata.json      # Metadata (optional)
├── n8n/
│   └── seo/
│       └── [category]/
│           └── [automation-name]/
│               ├── README.md          # Automation description
│               ├── workflow.json      # N8N file (optional)
│               └── metadata.json      # Metadata (optional)
└── colab/
    └── seo/
        └── [category]/
            └── [automation-name]/
                ├── README.md          # Automation description
                ├── notebook.ipynb     # Google Colab file (optional)
                └── metadata.json      # Metadata (optional)
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
# 🎯 Automation Name

## Automation Description
Brief description of what the automation does (2-3 sentences).

## How it works?
1. Step 1
2. Step 2
3. Step 3

## Requirements
### APIs and Tools
- List of required APIs and tools

### Input Data Structure
Description of input data structure (Google Sheets, etc.)

## Configuration
Configuration instructions

## Results
Description of results and output data structure

## Usage
Usage instructions

## Benefits
List of benefits from using the automation
```

#### Optional sections:
- `Examples` - Usage examples
- `Troubleshooting` - Problem solving
- `Limitations` - Limitations
- `Technical Requirements` - Technical requirements
- `Cost Considerations` - Cost analysis
- `Use Cases` - Specific use cases
- `Performance Notes` - Performance information

#### Example README structure (based on Header Structure Generator):

```markdown
# 🎯 Header Structure Generator

## Automation Description
The Header Structure Generator is an advanced SEO automation that creates comprehensive article outlines and header structures based on competitor analysis and keyword research. This automation combines SERP analysis, content extraction, and AI-powered outline generation to help content creators develop well-structured, SEO-optimized articles.

## How it works?
1. Retrieves keywords from Google Sheets
2. Analyzes search results for each keyword using SerpData API
3. Extracts content from top 5 competitor URLs using Jina AI
4. Processes and aggregates competitor content
5. Extracts relevant facts using OpenAI GPT-4o-mini
6. Generates article outline using OpenAI GPT-4o
7. Updates Google Sheets with results

## Requirements
### APIs and Tools
- Google Sheets API
- SerpData API for SERP analysis
- Jina AI for content extraction
- OpenAI API (GPT-4o-mini and GPT-4o)

### Input Data Structure
Google Sheets with columns:
- Column A: "Keyword" (input)
- Column B: "Serps" (output)
- Column C: "Facts" (output)
- Column D: "Outline" (output)

## Configuration
1. Import the JSON file into Make
2. Configure Google Sheets connection
3. Add SerpData API Bearer token
4. Configure OpenAI API connection
5. Update spreadsheet ID and sheet name

## Results
- **Column B**: SERP analysis results (JSON format)
- **Column C**: Extracted facts from competitor content (XML format)
- **Column D**: Generated article outline (HTML format)

## Usage
1. Add keywords to column A of Google Sheets
2. Automation processes each new row automatically
3. Results appear in columns B, C, and D

## Benefits
- Time savings: Automates hours of manual competitor research
- Quality improvement: Based on actual SERP analysis
- SEO optimization: Creates outlines optimized for search engines
- Consistency: Provides standardized outline structure
- Scalability: Can process multiple keywords efficiently
- Data-driven: Uses real competitor data to inform content strategy

## Technical Requirements
- Make.com account with appropriate plan
- SerpData API subscription
- OpenAI API access
- Google Sheets with proper permissions

## Cost Considerations
- SerpData API calls per keyword
- OpenAI API tokens for fact extraction and outline generation
- Make.com operations based on your plan

## Use Cases
- Content Marketing Teams: Generate outlines for blog posts
- SEO Agencies: Create content briefs for clients
- Digital Publishers: Develop article structures
- E-commerce Sites: Create product category content outlines

## Performance Notes
- Total processing time: 80-125 seconds per keyword
- Parallel processing for content extraction
- Error handling for failed extractions
- Respects API rate limits
```

### 3. Naming

#### Directory names:
- Use `kebab-case` (e.g., `keyword-research`, `header-structure-generator`)
- Avoid spaces and special characters
- Use descriptive names
- Use English names for consistency

#### File names:
- `README.md` - automation description
- `scenario.json` - Make file (or custom name like `Header Structure Generator.json`)
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