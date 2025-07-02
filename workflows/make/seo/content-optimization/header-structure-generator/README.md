# Header Structure Generator

## Overview

The Header Structure Generator is an advanced SEO automation that creates comprehensive article outlines and header structures based on competitor analysis and keyword research. This automation combines SERP analysis, content extraction, and AI-powered outline generation to help content creators develop well-structured, SEO-optimized articles.

## 🔄 Automation Flow

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Google Sheets │    │   SerpData API  │    │   Jina AI       │
│   (Trigger)     │───▶│   (SERP Data)   │───▶│   (Content      │
│   Keyword Input │    │   Top 10 Results│    │    Extraction)  │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Content       │    │   Content       │    │   JSON          │
│   Processing    │    │   Aggregation   │    │   Transformation│
│   (Top 5 URLs)  │    │   (Combine)     │    │   (Format)      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 ▼
                    ┌─────────────────────────┐
                    │   OpenAI GPT-4o-mini    │
                    │   (Fact Extraction)     │
                    │   XML Format Output     │
                    └─────────────────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │   OpenAI GPT-4o        │
                    │   (Outline Generation)  │
                    │   HTML Format Output    │
                    └─────────────────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │   Google Sheets         │
                    │   (Results Update)      │
                    │   Columns B, C, D       │
                    └─────────────────────────┘
```

### Flow Description:
1. **🔍 Input**: Keyword from Google Sheets (Column A)
2. **📊 SERP Analysis**: Fetch top 10 organic results via SerpData API
3. **📄 Content Extraction**: Extract content from top 5 competitor URLs using Jina AI
4. **🔄 Processing**: Aggregate and format extracted content
5. **🧠 AI Analysis**: 
   - **Facts**: Extract relevant facts using GPT-4o-mini
   - **Outline**: Generate article structure using GPT-4o
6. **📝 Output**: Update Google Sheets with results (Columns B, C, D)

## Tools Used

- **Google Sheets**: For input/output data management
- **SerpData API**: For SERP analysis and competitor research
- **Jina AI**: For content extraction from competitor URLs
- **OpenAI GPT-4o-mini**: For fact extraction from competitor content
- **OpenAI GPT-4o**: For generating article outlines and header structures

## How to Use

### Prerequisites
1. **Google Sheets Setup**: Use the provided template or create a spreadsheet with the following structure:
   - **Column A**: "Keyword" (Keywords) - input
   - **Column B**: "Serps" (SERP Results) - output
   - **Column C**: "Facts" (Extracted Facts) - output  
   - **Column D**: "Outline" (Generated Outline) - output
   - **Columns E-R**: Additional data columns (optional)

   **📋 Template**: [Google Sheets Template](https://docs.google.com/spreadsheets/d/1aY6QQyK5GoWmMaafN-zIURrL52KC3ER70q0GwbwIarc/edit?usp=sharing)

2. **API Connections**:
   - SerpData API with Bearer token
   - OpenAI API connection
   - Google Sheets connection

### Setup Instructions
1. **Copy the Template**: Use the provided Google Sheets template or create your own with the same structure
2. **Import the JSON**: Import the `Header Structure Generator.json` file into Make
3. **Configure Connections**:
   - Update Google Sheets connection to point to your spreadsheet
   - Add your SerpData API Bearer token in the HTTP request headers
   - Configure your OpenAI API connection
4. **Update Settings**:
   - Spreadsheet ID: Your target spreadsheet ID
   - Sheet name: "Sheet1" (or your preferred sheet name)
   - Ensure headers are included in the configuration

### Usage Process
1. **Add Keywords**: Enter your target keywords in column A of the Google Sheets
2. **Run Automation**: The automation will automatically process each new row
3. **Get Results**: Results will be populated in columns B, C, and D:
   - **Column B**: SERP analysis results (JSON format)
   - **Column C**: Extracted facts from competitor content (XML format)
   - **Column D**: Generated article outline (HTML format)

### Example Workflow
1. Add keyword "Jak obrać ziemiaki?" to column A, row 2
2. Automation processes the keyword and analyzes SERPs
3. Extracts content from top 5 competitor pages
4. Generates facts and creates article outline
5. Results appear in columns B, C, and D of the same row

### Sample Data Structure

| Column | Header | Content Type | Example |
|--------|--------|--------------|---------|
| A | Keyword | Input | "Jak obrać ziemiaki?" |
| B | Serps | Output (JSON) | `{"organic_results": [{"title": "...", "url": "...", "snippet": "..."}]}` |
| C | Facts | Output (XML) | `<facts><fact>Ziemniaki najlepiej obierać na zimno</fact></facts>` |
| D | Outline | Output (HTML) | `<h1>Jak obrać ziemiaki?</h1><h2>I. Wprowadzenie</h2>...` |

### Expected Results Format

**Column B - SERP Results:**
```json
{
  "organic_results": [
    {
      "title": "Jak obrać ziemiaki? 5 sprawdzonych sposobów",
      "url": "https://example.com/jak-obrac-ziemniaki",
      "snippet": "Poznaj najlepsze metody obierania ziemniaków..."
    },
    {
      "title": "Szybkie obieranie ziemniaków - poradnik",
      "url": "https://example2.com/szybkie-obieranie",
      "snippet": "Jak szybko i skutecznie obrać ziemniaki..."
    }
  ]
}
```

**Column C - Extracted Facts:**
```xml
<facts>
  <fact>Ziemniaki najlepiej obierać na zimno, przed gotowaniem</fact>
  <fact>Ostry nóż zapewnia czyste i szybkie obieranie</fact>
  <fact>Można używać obieraczki do warzyw dla szybszego efektu</fact>
  <fact>Obieranie na gorąco ułatwia usuwanie skórki</fact>
  <fact>Warto moczyć ziemniaki w zimnej wodzie po obraniu</fact>
</facts>
```

**Column D - Generated Outline:**
```html
<h1>Jak obrać ziemiaki? Kompletny poradnik</h1>

<h2>I. Wprowadzenie</h2>
<h3>A. Dlaczego warto nauczyć się obierać ziemniaki?</h3>
<h3>B. Przygotowanie do obierania</h3>

<h2>II. Metody obierania ziemniaków</h2>
<h3>A. Obieranie nożem - tradycyjna metoda</h3>
<h3>B. Używanie obieraczki do warzyw</h3>
<h3>C. Obieranie na gorąco</h3>

<h2>III. Wskazówki i triki</h2>
<h3>A. Wybór odpowiedniego noża</h3>
<h3>B. Technika obierania</h3>
<h3>C. Co zrobić po obraniu</h3>

<h2>IV. Podsumowanie</h2>
<h3>A. Najlepsze metody obierania</h3>
<h3>B. Dodatkowe wskazówki</h3>
```

## Step-by-Step Process

### 1. **Google Sheets Trigger** (Module 7)
- **Function**: Watches for new rows in Google Sheets
- **Input**: Keywords from column A
- **Configuration**: 
  - Spreadsheet ID: Your target spreadsheet
  - Sheet: Sheet1
  - Limit: 1 row at a time
  - Headers: Included

### 2. **SERP Analysis** (Module 5)
- **Function**: Fetches SERP data for the keyword
- **API**: SerpData.io
- **Parameters**:
  - URL: `https://api.serpdata.io/v1/search?keyword={{keyword}}&hl=pl&gl=pl`
  - Method: GET
  - Headers: Authorization Bearer token
- **Output**: Top 10 organic search results

### 3. **Content Extraction Setup** (Module 64)
- **Function**: Prepares top 10 results for processing
- **Input**: Organic results from SERP analysis
- **Output**: Array of competitor URLs

### 4. **Content Extraction** (Module 31)
- **Function**: Extracts content from competitor URLs
- **API**: Jina AI Reader
- **URL**: `https://r.jina.ai/{{competitor_url}}`
- **Filter**: Processes only top 5 results
- **Error Handling**: Ignores failed extractions

### 5. **Content Processing** (Module 84)
- **Function**: Processes extracted content data
- **Input**: Raw content from Jina AI
- **Output**: Structured content array

### 6. **Content Aggregation** (Module 88)
- **Function**: Combines all extracted content
- **Input**: Individual content pieces
- **Output**: Aggregated competitor content

### 7. **JSON Transformation** (Module 91)
- **Function**: Converts aggregated content to JSON format
- **Input**: Aggregated content array
- **Output**: JSON-formatted content for AI processing

### 8. **Fact Extraction** (Module 68)
- **Function**: Extracts relevant facts from competitor content
- **AI Model**: GPT-4o-mini
- **System Prompt**: Detailed instructions for fact extraction including:
  - Extract unique and significant facts
  - Combine similar facts to avoid redundancy
  - Focus on industry-relevant information
  - Use generic terms instead of specific brands
  - Include brand names only when highly relevant
- **Output**: Structured facts in XML format

### 9. **Outline Generation** (Module 71)
- **Function**: Creates article outline and header structure
- **AI Model**: GPT-4o
- **System Prompt**: Comprehensive outline generation including:
  - Analyze competitor content structure
  - Identify gaps and improvement areas
  - Brainstorm unique angles and titles
  - Create HTML-structured outline with H1, H2, H3 tags
  - Include introduction, main sections, and conclusion
- **Output**: Complete article outline in HTML format

### 10. **Results Update** (Module 72)
- **Function**: Updates Google Sheets with results
- **Columns Updated**:
  - Column B: SERP results (JSON)
  - Column C: Extracted facts (XML)
  - Column D: Generated outline (HTML)
- **Row**: Same row as the original keyword

## 🏗️ Make Modules Architecture

```
Module 7: Google Sheets (Trigger)
├── Watches for new rows
├── Reads keyword from Column A
└── Triggers automation

Module 5: HTTP Request (SerpData API)
├── Fetches SERP data
├── Gets top 10 organic results
└── Returns competitor URLs

Module 64: Basic Feeder
├── Processes organic results
├── Prepares for iteration
└── Filters top results

Module 31: HTTP Request (Jina AI)
├── Extracts content from URLs
├── Handles top 5 results only
└── Error handling for failed extractions

Module 84: Basic Feeder
├── Processes extracted content
├── Formats data structure
└── Prepares for aggregation

Module 88: Basic Aggregator
├── Combines all content pieces
├── Creates unified dataset
└── Prepares for AI processing

Module 91: JSON Transform
├── Converts to JSON format
├── Structures data for AI
└── Optimizes for token usage

Module 68: OpenAI GPT-4o-mini
├── Extracts facts from content
├── Uses XML output format
└── Focuses on industry insights

Module 71: OpenAI GPT-4o
├── Generates article outline
├── Creates HTML structure
└── Provides comprehensive structure

Module 72: Google Sheets (Update)
├── Updates original row
├── Writes to columns B, C, D
└── Completes automation cycle
```

### Module Dependencies:
- **7 → 5**: Trigger to SERP analysis
- **5 → 64**: SERP data to content processing
- **64 → 31**: URLs to content extraction
- **31 → 84**: Raw content to processing
- **84 → 88**: Processed content to aggregation
- **88 → 91**: Aggregated content to JSON
- **91 → 68**: JSON to fact extraction
- **68 → 71**: Facts to outline generation
- **71 → 72**: Outline to results update

## ⏱️ Process Timeline

```
Timeline: 0s ────────────────────────────────────────────────────────── 120s

0s    10s    20s    30s    40s    50s    60s    70s    80s    90s    100s   110s   120s
│      │      │      │      │      │      │      │      │      │      │      │      │
├─🔍───┤      │      │      │      │      │      │      │      │      │      │      │
│Input │      │      │      │      │      │      │      │      │      │      │      │
│      ├─📊───┤      │      │      │      │      │      │      │      │      │      │
│      │SERP  │      │      │      │      │      │      │      │      │      │      │
│      │      ├─📄───┤      │      │      │      │      │      │      │      │      │
│      │      │Extract│      │      │      │      │      │      │      │      │      │
│      │      │      ├─🔄───┤      │      │      │      │      │      │      │      │
│      │      │      │Process│      │      │      │      │      │      │      │      │
│      │      │      │      ├─🧠───┤      │      │      │      │      │      │      │
│      │      │      │      │Facts │      │      │      │      │      │      │      │
│      │      │      │      │      ├─🧠───┤      │      │      │      │      │      │
│      │      │      │      │      │Outline│      │      │      │      │      │      │
│      │      │      │      │      │      ├─📝───┤      │      │      │      │      │
│      │      │      │      │      │      │Output│      │      │      │      │      │
│      │      │      │      │      │      │      │      │      │      │      │      │
```

### Estimated Processing Times:
- **🔍 Input Processing**: ~5-10 seconds
- **📊 SERP Analysis**: ~10-15 seconds
- **📄 Content Extraction**: ~20-30 seconds (5 URLs × 4-6s each)
- **🔄 Data Processing**: ~5-10 seconds
- **🧠 Fact Extraction**: ~15-20 seconds (GPT-4o-mini)
- **🧠 Outline Generation**: ~20-30 seconds (GPT-4o)
- **📝 Results Update**: ~5-10 seconds

**Total Estimated Time**: 80-125 seconds per keyword

### Performance Notes:
- **Parallel Processing**: Content extraction runs in parallel for multiple URLs
- **Error Handling**: Failed extractions don't stop the process
- **API Limits**: Respects rate limits for SerpData and OpenAI APIs
- **Scalability**: Processes one keyword at a time for optimal quality

## Key Features

### Intelligent Fact Extraction
- Automatically identifies and extracts relevant facts from competitor content
- Combines similar information to avoid redundancy
- Focuses on industry-wide insights rather than brand-specific details
- Maintains accuracy and relevance to the target keyword

### Advanced Outline Generation
- Creates comprehensive article structures with proper heading hierarchy
- Identifies unique angles and opportunities based on competitor analysis
- Generates multiple title options and attention-grabbing hooks
- Includes introduction, main sections, subsections, and conclusion

### SEO-Optimized Structure
- Based on actual SERP analysis and competitor research
- Identifies content gaps and improvement opportunities
- Creates outlines that address user intent and search queries
- Optimized for both search engines and user experience

### Automated Workflow
- Fully automated processing from keyword input to outline output
- Handles errors gracefully (ignores failed content extractions)
- Processes one keyword at a time to ensure quality
- Updates results directly in Google Sheets for easy access

## Output Format

### SERP Results (Column B)
```json
{
  "organic_results": [
    {
      "title": "Competitor Title",
      "url": "https://competitor.com/article",
      "snippet": "Article description..."
    }
  ]
}
```

### Extracted Facts (Column C)
```xml
<facts>
  <fact>Key industry insight 1</fact>
  <fact>Important statistic or data point</fact>
  <fact>Trend or development in the field</fact>
</facts>
```

### Generated Outline (Column D)
```html
<h1>Main Article Title</h1>

<h2>I. Introduction</h2>
<h3>A. Brief overview</h3>
<h3>B. Importance of the topic</h3>

<h2>II. First Main Section</h2>
<h3>A. Subsection 1</h3>
<h3>B. Subsection 2</h3>

<h2>III. Second Main Section</h2>
<h3>A. Subsection 1</h3>
<h3>B. Subsection 2</h3>

<h2>IV. Conclusion</h2>
<h3>A. Summary of key points</h3>
<h3>B. Final thoughts or call to action</h3>
```

## Benefits

1. **Time Savings**: Automates hours of manual competitor research and outline creation
2. **Quality Improvement**: Based on actual SERP analysis and competitor content
3. **SEO Optimization**: Creates outlines optimized for search engines and user intent
4. **Consistency**: Provides standardized outline structure across all articles
5. **Scalability**: Can process multiple keywords efficiently
6. **Data-Driven**: Uses real competitor data to inform content strategy

## Use Cases

- **Content Marketing Teams**: Generate outlines for blog posts and articles
- **SEO Agencies**: Create content briefs for clients
- **Digital Publishers**: Develop article structures for editorial calendars
- **E-commerce Sites**: Create product category content outlines
- **Educational Content**: Develop structured learning materials

## Technical Requirements

- Make.com account with appropriate plan
- SerpData API subscription
- OpenAI API access
- Google Sheets with proper permissions
- Internet connection for API calls

## Cost Considerations

- SerpData API calls per keyword
- OpenAI API tokens for fact extraction and outline generation
- Make.com operations based on your plan
- Jina AI content extraction (if applicable)

## Limitations

- Depends on quality of competitor content available
- Requires proper API setup and authentication
- Processing time varies based on content length and complexity
- Results quality depends on AI model performance
- Limited to languages supported by the APIs used 