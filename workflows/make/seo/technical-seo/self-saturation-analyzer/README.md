# 📊 Self-Saturation Analyzer

## Automation Description

The automation evaluates the self-saturation parameter based on keywords from Google Sheets. It analyzes how much space is occupied by snippets that don't provide links and page visits, and assesses the chances for regular organic results.

## What is Self-Saturation?

Self-saturation is a phenomenon where Google displays so many featured snippets, AI Overviews, People Also Ask, and other SERP elements that little space remains for traditional organic results with links.

## How it works?

1. **Retrieves keywords** from Google Sheets
2. **Fetches search results** for each keyword from SerpData.io
3. **Analyzes SERP structure** and identifies different result types
4. **Calculates self-saturation score** based on:
   - Featured snippets
   - AI Overviews
   - People Also Ask
   - Knowledge panels
   - Shopping results
   - Video results
   - Map results
5. **Assesses chances for organic results** for each keyword
6. **Saves results** to Google Sheets with recommendations

## Analyzed Result Types

### Snippets without links (Self-Saturation)
- **Featured snippets** - answers without links
- **AI Overviews** - AI summaries
- **Knowledge panels** - knowledge base information
- **Rich snippets** - structured data
- **Video snippets** - video thumbnails

### Results with links (Organic Opportunities)
- **Organic results** - traditional links
- **Shopping results** - shopping results
- **Local results** - local results
- **News results** - news results

## Requirements

### APIs and Tools
- Google Sheets API
- [SerpData.io](https://serpdata.io/) API for fetching search results
- OpenAI API (optional) for semantic analysis

### Input Data Structure
Google Sheets should contain columns:
- `keyword` - keyword to analyze
- `target_domain` - Your domain (optional)
- `language` - language (default: en)
- `location` - location (default: United States)

## Self-Saturation Assessment Algorithm

### Self-Saturation Score (0-100%)
1. **Featured snippets** - 20% weight
2. **AI Overviews** - 25% weight
3. **People Also Ask** - 15% weight
4. **Knowledge panels** - 10% weight
5. **Video results** - 10% weight
6. **Shopping results** - 10% weight
7. **Map results** - 10% weight

### Organic Opportunities Score (0-100%)
- **Number of organic results** in TOP 10
- **Available positions** for traditional links
- **Competitiveness** of organic results
- **Ranking potential** for new pages

## Configuration

1. **Prepare keyword list** in Google Sheets
2. **Configure API connections** (SerpData.io, Google Sheets)
3. **Set analysis parameters** (weights for different result types)
4. **Configure frequency** of execution

## Results

The automation generates:
- **Self-saturation score** for each keyword
- **Organic opportunities score** - chances for organic results
- **SERP structure analysis** - distribution of different result types
- **Recommendations** for SEO strategy
- **Keyword prioritization**

### Output Columns
- `keyword` - keyword
- `self_saturation_score` - self-saturation assessment (0-100%)
- `organic_opportunities_score` - organic chances (0-100%)
- `featured_snippets_count` - number of featured snippets
- `ai_overviews_present` - whether AI Overviews are present (Yes/No)
- `paa_questions_count` - number of PAA questions
- `organic_results_count` - number of organic results
- `serp_structure` - SERP structure (list of result types)
- `recommendation` - recommendation (Target/Avoid/Moderate)
- `analyzed_at` - analysis date

## Results Interpretation

### Self-Saturation Score
- **0-30%** - Low self-saturation, good organic chances
- **31-60%** - Medium self-saturation, moderate chances
- **61-100%** - High self-saturation, difficult organic chances

### Organic Opportunities Score
- **80-100%** - Excellent chances for organic results
- **60-79%** - Good chances for organic results
- **40-59%** - Moderate chances for organic results
- **0-39%** - Difficult chances for organic results

## Usage

1. **Add keywords** to Google Sheets
2. **Run the automation**
3. **Analyze self-saturation scores** in the results sheet
4. **Prioritize keywords** according to organic opportunities
5. **Adjust SEO strategy** based on recommendations

## Benefits

### For SEO
- **Identification of keywords** with organic potential
- **Avoiding keywords** with high self-saturation
- **Optimization of budgets** for keyword research
- **Content marketing strategy** based on opportunities

### For content marketing
- **Topic prioritization** according to organic potential
- **Content adaptation** to available result types
- **Campaign planning** based on self-saturation
- **A/B testing** of different approaches

### For digital marketing
- **ROI optimization** of keyword research
- **Competitive analysis** of SERP structure
- **Reporting** for clients about organic opportunities
- **Link building strategy** based on self-saturation

---

*Automation requires API keys configuration before use.* 