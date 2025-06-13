# NVIDIA News Analysis with Semantic Search and AI Insights 🚀

## 📊 About
This project leverages advanced AI technologies to analyze NVIDIA news in real-time, providing semantic search capabilities, sentiment analysis, and investment insights. Built with LangChain, ChromaDB, and Google's Gemini AI, it offers a powerful tool for tracking NVIDIA's developments and market impact.

## ✨ Features
- 🔍 Real-time news fetching from multiple sources
- 🤖 Semantic search using ChromaDB and LangChain
- 📈 Sentiment analysis and trend detection
- 💡 AI-powered news interpretation using Gemini
- 📊 Topic clustering and analysis
- 💰 Investment insights and recommendations


## 🧠 Tools & Technologies

| Tool/Library              | Purpose                               |
|---------------------------|----------------------------------------|
| `feedparser`, `bs4`       | News scraping and RSS feed parsing     |
| `HuggingFaceEmbeddings`   | Sentence-level embeddings              |
| `Chroma`                  | Vector database for fast similarity search |
| `transformers`            | Sentiment analysis pipeline            |
| `langchain` + `Gemini`    | Prompting and LLM-powered interpretation |
| `Secrets`                  | Secure API key handling                |
| `pandas`, `nltk`, `sklearn` | Data handling and clustering (optional) |

## 🧩 Project Structure

```bash
├── news_fetcher.py        # Class to fetch and clean news
├── semantic_search.py     # Embedding, vectorstore, and search
├── news_analyzer.py       # Gemini-powered interpretation
├── main.py                # Main execution logic
├── README.md              # Project overview (this file)

```

## 🚀 Getting Started

### Prerequisites
```bash
pip install -r requirements.txt
```

### Environment Setup
1. Clone the repository
```bash
git clone https://github.com/gamzeakkurt/nvidia-news-analysis.git
cd nvidia-news-analysis
```

2. Set up your API keys
```bash
# Add your Google API key to Kaggle secrets
kaggle secrets set GOOGLE_API_KEY="your-api-key"
```

3. Run the analysis
```bash
python main.py
```

## 📝 Usage Examples

### Basic News Search
```python
# Initialize components
fetcher = NewsFetcher()
analyzer = NewsAnalyzer()

# Fetch and analyze news
df = fetcher.fetch_all_news()
vectorstore = analyzer.create_vectorstore(df)
results = analyzer.search_news("NVIDIA's latest AI developments", vectorstore)
```

### Investment Analysis
```python
# Get investment insights
news_items = "\n".join([f"- {doc.page_content}" for doc in results])
investment_analysis = analyzer.interpret_news(news_items)
```

## 📊 Output Examples
- Semantic search results
- News clustering
- Sentiment analysis
- Investment recommendations

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments
- Google Gemini AI
- LangChain
- ChromaDB
- HuggingFace

## 📫 Contact

Project Link: [https://github.com/gamzeakkurt/nvidia-news-analysis](https://github.com/gamzeakkurt/nvidia-news-analysis)


## 📈 Future Enhancements
- [ ] Add more news sources
- [ ] Implement real-time alerts
- [ ] Add historical analysis
- [ ] Create web interface
- [ ] Add more advanced visualization
- [ ] Implement automated trading signals
