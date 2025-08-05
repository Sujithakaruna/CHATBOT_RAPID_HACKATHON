# 🧠 Smart News Chatbot

A smart AI chatbot that fetches and summarizes the latest news about any company you ask for — all in real-time using free and open-source tools. It also supports friendly responses and different output styles like Formal, Casual, and Bullet Points.

---

## 📌 Features

- 🔍 Real-time news scraping using DuckDuckGo Search
- 📰 Extracts full news article content using Newspaper3k
- 🤖 Summarizes news using Hugging Face Transformers
- 💬 Responds to greetings in a friendly way
- 🎨 Output styles: Formal, Casual, Bullet Points
- 🌐 Gradio UI for easy interaction

---

## 🛠️ Tech Stack
Gradio – Used to build the interactive user interface for the chatbot.

DuckDuckGo Search – To fetch the latest news links related to the company or topic.

Newspaper3k – To extract the full news content (title, text, publication date) from each URL.

Transformers (HuggingFace) – Used for summarizing the extracted news articles using pre-trained AI models like t5-small or bart-large-cnn.

BeautifulSoup (optional) – Used for parsing raw HTML if newspaper3k fails or needs assistance.

Google Colab – The development and runtime environment for coding, testing, and deploying the project online.

---

## 💡 How It Works

1. **User enters a company name** (e.g., Tesla).
2. The chatbot:
   - Searches for the latest news using DuckDuckGo.
   - Extracts article content using `newspaper3k`.
   - Summarizes it using HuggingFace’s `distilbart-cnn-12-6` model.
   - Formats the summary in your chosen style.
3. Returns the clean summary + links to full articles.

---

## 🚀 Getting Started

### 🔧 Install Dependencies (in Colab or locally)

```bash
!pip install gradio duckduckgo-search newspaper3k transformers
