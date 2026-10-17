# SentiScrape 📊🤖

SentiScrape is a Python-based Jupyter Notebook tool that automatically scrapes customer reviews from a given product URL, analyzes the sentiment using large language models (via the Groq API), and visualizes the key focus areas driving customer feedback.

Whether you are an e-commerce seller looking for product feedback or a buyer doing deep research, SentiScrape extracts actionable insights from walls of text in seconds.

## ✨ Features
* **Automated Web Scraping:** Extracts paragraph text directly from a provided product link using `BeautifulSoup`. (Includes a fallback sample dataset if websites block the scraper).
* **LLM-Powered Analysis:** Leverages lightning-fast, open-source LLMs via the **Groq API** to read reviews and extract:
  * **Sentiment:** Positive, Negative, or Neutral.
  * **Focus Areas:** Specific features mentioned (e.g., "battery life", "customer service", "build quality").
* **Data Visualization:** Generates beautiful charts using `Seaborn` and `Matplotlib` to show sentiment distribution and the most discussed product features.
* **Actionable Insights:** Automatically summarizes the data to highlight the top complaints driving negative reviews.

## 🛠️ Technologies Used
* **Python 3**
* **Jupyter Notebook**
* **Groq API** (LLM inference)
* **BeautifulSoup & Requests** (Web scraping)
* **Pandas** (Data manipulation)
* **Matplotlib & Seaborn** (Data visualization)

## 🚀 Getting Started

### Prerequisites
1. Python installed on your machine.
2. Jupyter Notebook installed (`pip install notebook`).
3. A free API key from [Groq Console](https://console.groq.com/).

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Menodore/SentiScrape.git
   cd SentiScrape
   ```
2. Install the required Python packages:
   ```bash
   pip install groq beautifulsoup4 requests pandas matplotlib seaborn
   ```

### Usage
1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook product_analyzer.ipynb
   ```
2. In **Cell 2**, replace the placeholder with your actual Groq API key:
   ```python
   GROQ_API_KEY = "your_actual_api_key_here"
   ```
3. Run the notebook cell by cell. 
4. When prompted in **Cell 3**, paste the URL of the product you want to analyze.
5. Watch as the notebook scrapes the data, queries the LLM, and generates your insight graphs!

## ⚠️ Notes on Web Scraping
Major e-commerce websites (like Amazon, Flipkart, etc.) have strict anti-scraping measures. If the standard `requests` library gets blocked (returning 0 reviews), this notebook is designed to automatically fall back to a set of sample reviews so you can still test and see the LLM analysis and visualization pipeline in action. 

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Menodore/SentiScrape/issues).

## 📝 License
This project is [MIT](https://choosealicense.com/licenses/mit/) licensed.
