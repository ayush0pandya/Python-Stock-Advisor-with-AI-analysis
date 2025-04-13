## 📊 Stock Advisor AI

A Python-based AI assistant that analyzes real-time stock data and the latest market news to recommend whether to **Buy**, **Hold**, or **Sell** a stock — powered by the **OpenAI GPT model**, **Twelve Data**, and **NewsAPI**.

---

### 🚀 Features

- 🔍 Converts company names into official stock ticker symbols using AI
- 💵 Fetches **real-time stock prices** via [Twelve Data API](https://twelvedata.com/)
- 📰 Pulls the latest **5 news headlines** from [NewsAPI](https://newsapi.org/)
- 🧠 Analyzes price + headlines with **OpenAI GPT-3.5-Turbo** and suggests investment action
- 🧼 Fully documented, readable code with modular functions

---

### 📦 Requirements

- Python 3.7+
- `requests` library
- OpenAI account and API key
- Twelve Data API key
- NewsAPI key

---

### 🔐 Setup

1. **Install dependencies**
   ```bash
   pip install requests
   ```

2. **Add your API keys**  
   Replace the placeholders in the code with your real keys:
   ```python
   client = OpenAI(api_key="your-openai-api-key")
   NewsApiKey = "your-twelvedata-api-key"
   NewsApiKey = "your-newsapi-key"
   ```

   > 🔐 For better security, store keys in environment variables and use `os.getenv("API_KEY_NAME")`.

---

### 🧪 How It Works

1. You enter a **company name** (e.g., `Apple`)
2. The AI returns the stock symbol (e.g., `AAPL`) and full company name (`Apple Inc.`)
3. It fetches:
   - The **current stock price**
   - The **5 latest news headlines**
4. GPT-3.5 analyzes both and suggests:
   - ✅ Buy
   - 🟡 Hold
   - ❌ Sell

---

### 🧱 Main Functions

| Function              | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| `get_names()`         | Uses GPT to return stock symbol + full company name                        |
| `getStockPrice()`     | Calls Twelve Data API to fetch real-time stock price                        |
| `get_news_headlines()`| Uses NewsAPI to get latest 5 headlines about the company                    |
| `get_recommendation()`| Uses OpenAI to analyze and recommend Buy/Hold/Sell based on price + news   |

---

### 📷 Sample Output

```text
Enter what stock you want to know more about: Tesla
Current price of TSLA is: $204.34
Let's see what you should do:

Buy – Tesla stock looks promising with positive developments in recent news.
```

---

### 🤖 Tech Stack

- Python
- OpenAI GPT-3.5 Turbo
- Twelve Data API
- NewsAPI
- REST API Integration

---

### ⚠️ Disclaimer

This tool is for **educational purposes only**. It does **not provide real financial advice**. Always do your own research or consult a licensed advisor before investing.
