# 📝 Header Structure Generator

## Automation Description

The automation generates optimal header structure for SEO articles based on competitor content analysis.

## How it works?

1. **Retrieves keywords** from Google Sheets
2. **Analyzes search results** for each keyword
3. **Fetches content** from TOP competitor results
4. **Analyzes header structure** in competitor content
5. **Generates header list** using language model
6. **Saves results** to Google Sheets

## Requirements

### APIs and Tools
- Google Sheets API
- [SerpData.io](https://serpdata.io/) API for fetching search results
- OpenAI API (or similar) for generating headers
- Web Scraping API for content retrieval

### Input Data Structure
Google Sheets should contain columns:
- `keyword` - keyword to analyze
- `url` - target page URL (optional)

## Configuration

1. Configure API connections
2. Set Google Sheets ID
3. Configure generation parameters (number of headers, style)
4. Set execution frequency

## Results

The automation generates:
- List of H1, H2, H3 headers
- Article structure suggestions
- Keyword coverage analysis
- Optimization recommendations

## Usage

1. Add keywords to Google Sheets
2. Run the automation
3. Check generated structure in results sheet
4. Adjust headers as needed

---

*Automation requires API keys configuration before use.* 