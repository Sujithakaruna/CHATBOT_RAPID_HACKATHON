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

## ⚙️ How It Works

1. **User Input**: You type a company name (e.g., "Tesla").
2. **News Search**: The chatbot uses DuckDuckGo to find the latest news links.
3. **Content Extraction**: Each news link is parsed with `newspaper3k` to extract the full article text.
4. **Summarization**: The article content is summarized using the HuggingFace summarization model (`sshleifer/distilbart-cnn-12-6`).
5. **Response Styling**: Based on your selected style (Formal, Casual, Bullet Points), the summary is formatted and returned to you.
6. **Chat UI**: All interaction happens via a beautiful and simple **Gradio** interface.

---

## 💬 Example Styles

- **Formal**: "According to recent news, Tesla announced..."
- **Casual**: "Hey! Guess what? Tesla just dropped some hot updates..."
---

## 🤖 AI Model Used

- Model: `sshleifer/distilbart-cnn-12-6`  
- Library: [🤗 HuggingFace Transformers](https://huggingface.co/transformers/)
- Task: Summarization (`pipeline("summarization")`)

---

## 🚀 How to Run on Google Colab

1. Open [Google Colab](https://colab.research.google.com/)
2. Paste your full code.
3. Install the required packages:

```python
!pip install gradio duckduckgo-search newspaper3k transformers
