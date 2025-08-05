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

   Tool                                        | Purpose |
                                    |---------------------------------|
 `Gradio`                          | For building the user interface |
 `DuckDuckGo Search`               | To get the latest news links |
 `Newspaper3k`                     | To extract full article content from URLs |
 `Transformers` (HuggingFace)      | For summarizing news articles |
 `BeautifulSoup` (used optionally) | For HTML parsing if needed |
 `Google Colab`                    | For development and running the project online |

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
