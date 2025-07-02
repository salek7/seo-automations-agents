# 🎯 Automation Name

## Automation Description
Brief description of what the automation does (2-3 sentences).

## How it works?
1. **Step 1** - description of first step
2. **Step 2** - description of second step
3. **Step 3** - description of third step
4. **Step 4** - description of fourth step

## Requirements

### APIs and Tools
- [SerpData.io](https://serpdata.io/) API for search
- Google Sheets API for data management
- OpenAI API for analysis and content generation
- Web Scraping API for content retrieval
- [Other required APIs]

### Input Data Structure
Google Sheets should contain columns:
- `keyword` - keyword to analyze
- `domain` - domain to analyze
- `language` - search language
- `country` - search country

## Configuration

1. **Configure API keys** in Make/N8N
2. **Prepare Google Sheets** with input data
3. **Set automation parameters**
4. **Test** on a small dataset

## Results

The automation generates:
- **Competitor analysis** from TOP 10 results
- **Header structure** based on analysis
- **Content optimization recommendations**
- **Report** in PDF/Google Docs format

### Output Data Structure
- `keyword` - original keyword
- `competitors` - list of competitors
- `header_structure` - proposed header structure
- `recommendations` - optimization recommendations
- `report_url` - link to full report
- `completed_at` - analysis completion date

## Usage

1. **Add keywords** to Google Sheets
2. **Run the automation**
3. **Wait** for analysis completion
4. **Download report** with results
5. **Apply recommendations** to your content

## Benefits

### For SEO specialists
- **Time savings** - automation of competitor analysis
- **Better results** - data-driven recommendations
- **Scalability** - analysis of multiple keywords
- **Standardization** - consistent analysis process

### For companies
- **Competitive advantage** - better positioning
- **Content optimization** - higher Google rankings
- **ROI** - faster achievement of SEO goals
- **Automation** - less manual work

## Examples

### Example 1: Analysis of keyword "SEO tools"
```
Input: "SEO tools"
Output: 
- 5 competitors from TOP 10
- Header structure: H1, H2, H3
- Recommendations: add "Tool Comparison" section
```

### Example 2: Analysis of competitor domain
```
Input: "example.com"
Output:
- Analysis of 10 competitor pages
- Content structure patterns
- Optimization recommendations
```

## Troubleshooting

### Problem: API Error
**Solution**: Check if the API key is correct and has appropriate permissions.

### Problem: No Results
**Solution**: Check if the keyword is correct and if the API returns results.

### Problem: Google Sheets Error
**Solution**: Check if the input data structure is correct.

## Limitations

- **API limitations** - maximum 100 queries per day
- **Languages** - supports only English and Polish
- **Domains** - maximum 10 domains at once
- **Execution time** - may take up to 5 minutes

## Support

Need help? Check:
- [API Documentation](https://serpdata.io/docs)
- [Make Help Center](https://www.make.com/en/help)
- [N8N Documentation](https://docs.n8n.io/)

---

*Automation requires API keys configuration before use.* 