# 🚀 AI Financial Analyst

An intelligent multi-agent system that provides comprehensive stock analysis reports for Indian equity markets. The system mimics a professional financial research team, with specialized AI agents handling different aspects of investment research.

## 📊 Overview

This AI-powered financial analyst delivers institutional-quality research reports by coordinating multiple specialized agents, each replicating the role of financial industry professionals. Users simply input a company name and receive detailed analysis via email within minutes.

## 🏗️ System Architecture

### Multi-Agent Workflow

```
User Input → Input Analyzer → [Metrics Agent + Growth Agent + Consensus Agent] → Reporter Agent → Email Agent → User
```

### 🎯 Agent Roles & Responsibilities

| Agent | Industry Role | Responsibility |
|-------|---------------|----------------|
| **Input Analyzer** | Research Intake Specialist | Validates queries and filters out non-financial requests |
| **Metrics Agent** | Quantitative Analyst | Extracts critical financial metrics from trusted sources |
| **Growth Research Agent** | Equity Research Associate | Analyzes latest news, reports, and growth prospects |
| **Consensus Agent** | Senior Research Analyst | Gathers market consensus and provides independent assessment |
| **Reporter Agent** | Investment Research Writer | Synthesizes data into professional investment reports |
| **Email Agent** | Client Relations Coordinator | Delivers complete analysis to user's inbox |

## ✨ Features

- **🔍 Intelligent Input Validation**: Automatically filters relevant financial queries
- **📈 Comprehensive Analysis**: 5 key financial metrics tailored to each company
- **📰 Latest Market Intelligence**: Real-time news and financial report analysis  
- **🎯 Expert Consensus**: Top analyst recommendations with independent assessment
- **📄 Professional Reports**: Institutional-quality investment research
- **📧 Email Delivery**: Automated report delivery via SendGrid
- **🇮🇳 India-Focused**: Specialized for Indian stock markets (BSE/NSE)
- **⚡ Fast Processing**: Complete analysis in under 5 minutes

## 🛠️ Tech Stack

- **LLM APIs**: OpenAI SDK, Google Gemini API
- **Frontend**: Gradio (Clean chat interface)
- **Email Service**: SendGrid API
- **Architecture**: Multi-agent system with specialized roles
- **Market Focus**: Indian equity markets
- **Data Sources**: BSE/NSE, Moneycontrol, Economic Times, Company Reports

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Google Gemini API key  
- SendGrid API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-financial-analyst.git
   cd ai-financial-analyst
   ```

2. **Create virtual environment**
   ```bash
   python -m venv agents
   source agents/bin/activate  # On Windows: agents\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   
   Create a `.env` file in the `agents` folder:
   ```env
   GEMINI_API_KEY=your_gemini_api_key
   SENDGRID_API_KEY=your_sendgrid_api_key
   SENDER_EMAIL=your_verified_sender_email
   ```

### Usage

1. **Run the application**
   ```bash
   cd agents/2_openai/deep_research
   uv run dotenv -f ../../.env run -- python deep_research.py
   ```

2. **Access the interface**
   - Open your browser to `http://localhost:7860`
   - Enter a company name (e.g., "Reliance Industries", "TCS", "HDFC Bank")
   - Click "Run" and wait for analysis
   - Check your email for the detailed report

### Example Queries

- ✅ "Analyze Reliance Industries"
- ✅ "TCS stock analysis"
- ✅ "HDFC Bank investment prospects"
- ❌ "What's the weather today?" (Out of scope)

## 📋 Sample Output

The system generates comprehensive reports including:

- **Executive Summary** with investment recommendation
- **Key Financial Metrics** (5 most critical for the company)
- **Growth Outlook** with sector context
- **Investment Highlights** (top 3 reasons to invest)
- **Risk Assessment** (key concerns to monitor)
- **Analyst Consensus** vs independent view
- **Conclusion** with target price and time horizon

## 🔧 Project Structure

```
ai-financial-analyst/
├── agents/
│   ├── .env                          # Environment variables
│   └── 2_openai/
│       └── deep_research/
│           ├── deep_research.py      # Main Gradio app
│           ├── research_manager.py   # Agent orchestration
│           ├── agents/
│           │   ├── input_analyzer.py
│           │   ├── metrics_agent.py
│           │   ├── growth_agent.py
│           │   ├── consensus_agent.py
│           │   ├── reporter_agent.py
│           │   └── email_agent.py
│           └── requirements.txt
├── README.md
└── LICENSE
```

## ⚙️ Configuration

### Customizing Agents

Each agent can be customized by modifying their respective prompt files or parameters:

- **Metrics Focus**: Adjust industry-specific metrics in `metrics_agent.py`
- **Data Sources**: Configure preferred financial data sources
- **Report Format**: Customize report structure in `reporter_agent.py`
- **Email Template**: Modify email formatting in `email_agent.py`

## 📈 Performance

- **Response Time**: ~3-5 minutes per analysis
- **Accuracy**: Based on latest available financial data
- **Coverage**: 500+ Indian listed companies
- **Update Frequency**: Real-time news and quarterly financials

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## ⚠️ Disclaimer

**IMPORTANT**: This application is for educational and research purposes only. It does not constitute investment advice. Always consult with qualified financial advisors before making investment decisions. Past performance does not guarantee future results.

## 🙏 Acknowledgments

- Inspired by **Ed Donner's LLM Engineering Course**
- Thanks to the open-source AI community
- Financial data sources: BSE, NSE, Moneycontrol, Economic Times

## 📞 Support

- **Issues**: Create a GitHub issue
- **Questions**: Open a discussion
- **Email**: sakshamsamj22@gmail.com

---

**Built with ❤️ for the Indian financial community**

*Star ⭐ this repo if you found it helpful!*
