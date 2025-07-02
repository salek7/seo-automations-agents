# 🚀 SEO Automations and Agents

**Free SEO Automations for Make, N8N and Google Colab**

A collection of ready-to-use SEO automations and AI agents that will help you optimize marketing and analytical processes. All automations are free and ready to import in Make (Integromat), N8N, and Google Colab.

## 🎯 What you'll find in this repository?

### 📊 SEO Automations

| Name | Category | Status | Make | N8N | Google Colab | Description |
|------|----------|--------|------|-----|-------------|-------------|
| [Deep Research Agent](workflows/make/seo/keyword-research/deep-research-agent/) | Keyword Research | 🔄 In Progress | ❌ | ❌ | ❌ | Multi-step research agent like ChatGPT Deep Research |
| [Self-Saturation Analyzer](workflows/make/seo/technical-seo/self-saturation-analyzer/) | Technical SEO | 🔄 In Progress | ❌ | ❌ | ❌ | Evaluates chances for organic results vs self-saturation |
| [Comprehensive Keyword Research](workflows/make/seo/keyword-research/comprehensive-keyword-research/) | Keyword Research | 🔄 In Progress | ❌ | ❌ | ❌ | Complete research with 7 data types in structured sheets |
| [Header Structure Generator](workflows/make/seo/content-optimization/header-structure-generator/) | Content Optimization | 🔄 In Progress | ❌ | ❌ | ❌ | Generates header structure based on competitor analysis |
| [Query Expansion & Fan-out Generator](workflows/make/seo/keyword-research/query-expansion-generator/) | Keyword Research | ⏳ In Queue | ❌ | ❌ | ❌ | Generates synthetic queries according to Google patents |
| [Keyword Intent Classification](workflows/make/seo/keyword-research/intent-classification/) | Keyword Research | ⏳ In Queue | ❌ | ❌ | ❌ | Classifies keywords by user intent |
| [AI Overviews Monitor](workflows/make/seo/technical-seo/ai-overviews-monitor/) | Technical SEO | ⏳ In Queue | ❌ | ❌ | ❌ | Tracks presence in Google AI Overviews |
| [Rapid Keyword Research](workflows/make/seo/keyword-research/rapid-keyword-research/) | Keyword Research | ⏳ In Queue | ❌ | ❌ | ❌ | Replaces hours of work with seconds of automation |

**Status Legend:**
- 🔄 **In Progress** - Currently being developed and tested
- ⏳ **In Queue** - Planned for development
- ✅ **Ready** - Fully implemented and tested

**Availability:**
- ✅ **Available** - Ready to import and use
- ❌ **Not Available** - Not yet implemented

### 🛠️ Tools
- **Make (Integromat)** - ready-to-import scenarios
- **N8N** - workflows to copy
- **Google Colab** - Jupyter notebooks for data analysis and automation

### 🤖 AI Assistant Integration (MCP)

All automations can be used with AI assistants through MCP (Model Context Protocol) servers:

#### Make MCP Server
- **Official MCP Server** from Make: [developers.make.com/mcp-server](https://developers.make.com/mcp-server)
- **Features**: Running "On Demand" scenarios as tools for AI
- **Benefits**: 
  - Scenarios as callable tools for AI
  - Bidirectional communication between AI and automations
  - Available on all plans (including free)

#### N8N MCP Servers
- **[mcp-n8n-builder](https://github.com/spences10/mcp-n8n-builder)** - Programmatic creation and management of workflows
- **[n8n-mcp](https://github.com/czlonkowski/n8n-mcp)** - Alternative MCP server for N8N
- **Features**: 
  - Create, modify and manage workflows
  - Schema and node type validation
  - Smart suggestions for similar node types
  - Workflow execution management

**Usage example**: AI assistant can automatically modify SEO automations based on your requirements, adding new features or adapting existing workflows.

## 📁 Repository Structure

```
workflows/
├── make/           # Make automations
│   └── seo/        # SEO category
│       ├── keyword-research/
│       ├── competitor-analysis/
│       ├── content-optimization/
│       └── technical-seo/
├── n8n/            # N8N automations
│   └── seo/        # SEO category
│       ├── keyword-research/
│       ├── competitor-analysis/
│       ├── content-optimization/
│       └── technical-seo/
└── colab/          # Google Colab notebooks
    └── seo/        # SEO category
        ├── keyword-research/
        ├── competitor-analysis/
        ├── content-optimization/
        └── technical-seo/
```

## 🚀 Quick Start

### For Make (Integromat)
1. Go to the `workflows/make/seo/` directory
2. Choose the automation you're interested in
3. Download the JSON file
4. Import in Make: **Settings → Import → Upload JSON**

### For N8N
1. Go to the `workflows/n8n/seo/` directory
2. Choose the workflow you're interested in
3. Copy the JSON content
4. Paste in N8N: **Import from JSON**

### For Google Colab
1. Go to the `workflows/colab/seo/` directory
2. Choose the notebook you're interested in
3. Open the `.ipynb` file in Google Colab
4. Follow the instructions in the notebook

## 📚 Documentation

- [📖 Installation guides](docs/installation-guides/)
- [📋 Usage guides](docs/usage-guides/)
- [💡 Examples](docs/examples/)

## 🤝 Contributing

Want to add your SEO automation? Join the community!

### 🚀 How to add your automation?
1. **Check** [CONTRIBUTING.md](CONTRIBUTING.md) - detailed instructions
2. **Use** [README template](docs/README_TEMPLATE.md) for new automations
3. **Fork** the repository and create a Pull Request
4. **Test** the automation before adding

### 📋 Requirements for new automations:
- ✅ SEO automation for Make or N8N
- ✅ Free APIs and tools
- ✅ Complete documentation
- ✅ Tested functionality
- ✅ No API keys in code

### 🎯 SEO Categories:
- **Keyword Research** - keyword research
- **Competitor Analysis** - competitor analysis
- **Content Optimization** - content optimization
- **Technical SEO** - technical SEO

### 📞 Support:
- [Issues](https://github.com/salek7/seo-automations-agents/issues) - report problems
- [Discussions](https://github.com/salek7/seo-automations-agents/discussions) - discussions
- [Code of Conduct](CODE_OF_CONDUCT.md) - community guidelines

## 📝 License

All automations are available under the MIT license - you can use them commercially and modify as needed.

## ⭐ Support

If you like the project, give it a star! ⭐

---

**Built with ❤️ for the SEO community** 