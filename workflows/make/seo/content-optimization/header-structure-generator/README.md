# Header Structure Generator

## Overview

The Header Structure Generator is an advanced SEO automation that creates comprehensive article outlines and header structures based on competitor analysis and keyword research. This automation combines SERP analysis, content extraction, and AI-powered outline generation to help content creators develop well-structured, SEO-optimized articles.

## Tools Used

- **Google Sheets**: For input/output data management
- **SerpData API**: For SERP analysis and competitor research
- **Jina AI**: For content extraction from competitor URLs
- **OpenAI GPT-4o-mini**: For fact extraction from competitor content
- **OpenAI GPT-4o**: For generating article outlines and header structures

## How to Use

### Prerequisites
1. **Google Sheets Setup**: Create a spreadsheet with the following columns:
   - Column A: Keywords (input)
   - Column B: SERP Results (output)
   - Column C: Extracted Facts (output)
   - Column D: Generated Outline (output)

2. **API Connections**:
   - SerpData API with Bearer token
   - OpenAI API connection
   - Google Sheets connection

### Setup Instructions
1. Import the JSON file into Make
2. Configure the Google Sheets connection to point to your spreadsheet
3. Add your SerpData API Bearer token in the HTTP request headers
4. Configure your OpenAI API connection
5. Update the spreadsheet ID and sheet name in the Google Sheets modules

### Usage Process
1. Add keywords to column A of your Google Sheets
2. The automation will automatically process each new row
3. Results will be populated in columns B, C, and D

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