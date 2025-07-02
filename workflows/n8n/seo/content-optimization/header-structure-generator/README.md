# 📝 Header Structure Generator (N8N)

## Automation Description

The N8N workflow generates optimal header structure for SEO articles based on competitor content analysis.

## How it works?

1. **Retrieves keywords** from Google Sheets
2. **Analyzes search results** for each keyword
3. **Fetches content** from TOP competitor results
4. **Analyzes header structure** in competitor content
5. **Generates header list** using language model
6. **Saves results** to Google Sheets

## Requirements

### APIs and Tools
- Google Sheets node
- HTTP Request node ([SerpData.io](https://serpdata.io/) API)
- HTTP Request node (OpenAI API)
- Web Scraping node
- Google Sheets node (results saving)

### Input Data Structure
Google Sheets should contain columns:
- `keyword` - keyword to analyze
- `url` - target page URL (optional)

## Configuration

1. Configure Google Sheets connections
2. Set API keys (SerpAPI, OpenAI)
3. Configure generation parameters
4. Set trigger (manual or scheduled)

## Results

The workflow generates:
- List of H1, H2, H3 headers
- Article structure suggestions
- Keyword coverage analysis
- Optimization recommendations

## Usage

1. Add keywords to Google Sheets
2. Run the workflow
3. Check generated structure in results sheet
4. Adjust headers as needed

---

*Workflow requires API keys configuration before use.* 