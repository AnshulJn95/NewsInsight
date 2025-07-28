# 📰 NewsInsight: News Research & Q&A Tool

**NewsInsight** is an intelligent and user-friendly research tool that simplifies information extraction from news articles. Built using LangChain, FAISS, and Gemini (Google Generative AI), it enables users to input article URLs and ask insightful questions — perfect for staying informed about the financial and stock market domain.

## 🔍 Features

- ✅ **Multi-URL Input**: Input multiple article URLs via an intuitive sidebar interface
- 🧠 **Automated Content Processing**: Automatically fetches and processes content using `SeleniumURLLoader`
- ✂️ **Smart Text Chunking**: Splits large article content into optimized chunks for efficient embedding
- 🧬 **Advanced Embeddings**: Uses Google's `Gemini Embeddings` to convert text into high-quality vector representations
- ⚡ **Fast Retrieval**: Stores embeddings in **FAISS** for lightning-fast and accurate information retrieval
- 🤖 **Intelligent Q&A**: Query articles via LLM (`Gemini Flash`) and get insightful answers with source citations
- 💾 **Persistent Storage**: Stores vector index locally for reuse — no need to reprocess articles every time
- 🎯 **Domain Focused**: Optimized for financial and stock market news analysis
- 🔑 **Direct API Integration**: Streamlined setup with direct API key configuration

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- Google API key for Gemini

### Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/AnshulJn95/NewsInsight.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd NewsInsight
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure API Key**:
   - Open `main.py` in your preferred text editor
   - Locate the API key configuration section
   - Replace `"YOUR_API_KEY_HERE"` with your actual Google Gemini API key:
   ```python
   # Direct API key configuration
   GOOGLE_API_KEY = "your_actual_gemini_api_key_here"
   ```

## 💡 Usage

### Running the Application

1. **Start the Streamlit App**:
   ```bash
   streamlit run main.py
   ```

2. **Using the Web Interface**:
   - Paste up to 3 URLs of news articles in the sidebar
   - Click "⚙️ Process URLs" to load and embed the articles
   - Ask any question related to the article content in the main interface
   - View detailed answers with source URLs and citations
   - Explore different aspects of the news through follow-up questions

### Tips for Best Results
- Use URLs from reputable financial news sources
- Wait for processing to complete before asking questions
- Ask specific questions for more targeted responses
- Use follow-up questions to dive deeper into topics

## 📁 Project Structure

```
NewsInsight/
├── main.py                  # Main Streamlit application (contains API key)
├── requirements.txt         # Python dependencies  
├── faiss_store_gemini/      # Directory for saved FAISS index
├── README.md               # Project documentation
└── .gitignore             # Git ignore file
```

## 🌐 Example Articles Used

Here are some sample financial news articles you can test with:

- [Tata Motors, Mahindra gain production-linked payouts](https://www.moneycontrol.com/news/business/tata-motors-mahindra-gain-certificates-for-production-linked-payouts-11281691.html)
- [Tata Motors launches Punch iCNG](https://www.moneycontrol.com/news/business/tata-motors-launches-punch-icng-price-starts-at-rs-7-1-lakh-11098751.html)  
- [Buy Tata Motors – KR Choksey](https://www.moneycontrol.com/news/business/stocks/buy-tata-motors-target-of-rs-743-kr-choksey-11080811.html)

## 🛠️ Technologies Used

- **Frontend**: Streamlit
- **LLM Framework**: LangChain
- **Vector Database**: FAISS
- **Language Model**: Google Gemini (Flash & Embeddings)
- **Web Scraping**: SeleniumURLLoader

## 🔧 Configuration

### API Key Setup
The application uses a **direct API key configuration** approach for simplicity:

1. Open `main.py`
2. Find the API key section at the top of the file
3. Replace the placeholder with your actual key:
   ```python
   # API Configuration
   GOOGLE_API_KEY = "your_actual_gemini_api_key_here"
   ```

⚠️ **Security Note**: Since the API key is directly embedded in the code, ensure you don't accidentally commit it to public repositories.

### Customization Options
- Modify chunk size and overlap in the text processing section
- Adjust the number of retrieved documents for Q&A
- Customize the Streamlit UI theme and layout
- Add support for additional news sources

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. **Important**: Remove your API key before committing
4. Commit your changes (`git commit -m 'Add amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

### Areas for Contribution
- Enhanced security with environment variable support
- Support for additional news sources
- UI/UX improvements
- Performance optimizations
- Additional export formats

## 📋 Requirements

```txt
streamlit
langchain
faiss-cpu
google-generativeai
selenium
beautifulsoup4
```

## 🐛 Troubleshooting

### Common Issues

**Issue**: API key not working
- **Solution**: Ensure your Google API key is correctly set in `main.py` and has Gemini API access enabled

**Issue**: FAISS index not loading
- **Solution**: Delete the `faiss_store_gemini/` directory and reprocess your URLs

**Issue**: Selenium WebDriver errors
- **Solution**: Make sure you have the appropriate WebDriver installed for your browser

**Issue**: Module not found errors
- **Solution**: Ensure all dependencies are installed using `pip install -r requirements.txt`

## 🔒 Security Considerations

Since this project uses direct API key configuration:

- **Never commit your actual API key** to version control
- Consider using `.gitignore` to exclude files with sensitive data
- For production deployment, consider migrating to environment variables
- Regularly rotate your API keys for security

## 👨💻 Author

**Anshul Jain**
- GitHub: [@AnshulJn95](https://github.com/AnshulJn95)
- Project: [NewsInsight](https://github.com/AnshulJn95/NewsInsight)

**⭐ If you found this project helpful, please give it a star!**
