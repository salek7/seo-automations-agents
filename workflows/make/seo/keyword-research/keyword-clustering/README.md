# Keyword Clustering - Make

## Automation Description

Automation for grouping keywords based on the co-occurrence of the same URLs in Google search results. Keywords that lead to similar pages are grouped into logical clusters.

## Features

### Main capabilities:
- **Search Results Retrieval** - automatic extraction of URLs from Google for each keyword
- **URL Co-occurrence Analysis** - identification of common domains and pages between keywords
- **URL-based Clustering** - grouping keywords based on result similarity
- **Cluster Visualization** - generation of charts and diagrams showing relationships
- **Results Export** - saving clusters to CSV, Excel or JSON

### Additional features:
- **Domain Analysis** - identification of main domains in clusters
- **Results Filtering** - removal of irrelevant URLs
- **Competitive Analysis** - comparison with competitor pages
- **Cluster Prioritization** - ranking by potential and volume

## Automation Structure

### Modules:
1. **Input Processing** - processing the keyword list
2. **Search Results Scraping** - retrieving results from Google for each keyword
3. **URL Extraction** - extracting URLs from search results
4. **Similarity Analysis** - calculating similarity between keywords based on shared URLs
5. **Clustering Algorithm** - grouping algorithm (Jaccard Similarity)
6. **Cluster Analysis** - analysis and validation of clusters
7. **Visualization** - chart generation
8. **Export** - results export

### Integrations:
- **Google Search API/SerpAPI** - search results retrieval
- **Google Sheets** - data import/export
- **Airtable** - cluster management
- **Slack/Teams** - notifications about completed clusters
- **Google Analytics** - traffic analysis for clusters

## Configuration

### Required APIs:
- Google Search API or SerpAPI (key)
- Google Sheets API (optional)
- Airtable API (optional)

### Input parameters:
- Keyword list (CSV/Excel)
- Number of results to analyze (default: 10)
- Similarity threshold (0.1-1.0)
- Minimum cluster size
- Domain filters (optional)

## Results

### Output format:
- **Named clusters** - grouped keywords with descriptions
- **Shared URLs** - list of URLs occurring in the cluster
- **Cluster statistics** - size, density, quality
- **Visualizations** - similarity and hierarchy charts
- **Analytical report** - detailed summary

### Metrics:
- **Jaccard Index** - similarity coefficient between keywords
- **Cluster density** - URL density in cluster
- **Domain diversity** - domain diversity in cluster
- **Search volume** - sum of search volumes in cluster

## Applications

### SEO:
- PPC campaign organization
- Content planning
- Topic niche analysis
- Website structure optimization

### Content Marketing:
- Content calendar planning
- Topic gap identification
- Trend analysis
- Content personalization

## Usage Instructions

1. **Prepare data** - keyword list in CSV format
2. **Configure parameters** - set similarity threshold and number of results
3. **Run automation** - execute scenario in Make
4. **Review clusters** - check grouping quality
5. **Export results** - save to chosen platform

## Technical Requirements

- Make.com account
- Google Search API or SerpAPI access
- Basic SEO knowledge
- Access to keyword data

## Support

If you encounter issues with the automation, check:
- Input data format correctness
- Search API keys configuration
- Google Search/SerpAPI limits
- Internet connection 