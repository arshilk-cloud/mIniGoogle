# miniGoogle (1998) 🔍

A lightweight, static web demonstration contrasting the **Traditional Search Ranking (pre-1998)** with **Google's PageRank Algorithm (1998)**.

Built purely with **HTML & CSS**.

---

## 💡 Overview

In the early days of the web, search engines (like AltaVista, Lycos, Excite) ranked search results primarily by **keyword frequency** (how often a term appeared in the page text). This led to rampant **keyword stuffing**, where low-value spam pages easily gamed the system.

In 1998, Larry Page and Sergey Brin introduced **PageRank**, treating hyperlinks as **"votes of confidence"**:
- A link from page A to page B counts as a vote for page B.
- Links from pages that themselves have high authority carry more weight.

---

## 📊 Dataset Comparison (Query: `"pizza"`)

| Page | URL | Inbound Links (Votes) | Keyword Occurrences | Traditional Rank | PageRank (1998) |
|---|---|---|---|---|---|
| 2 | `best-pizza-pune.com` | **4** (Pages 1, 3, 4, 5) | 2 | #3 (Buried) | **#1 (Top Authority)** |
| 1 | `pune-food-guide.com` | **2** (Pages 2, 6) | 1 | #4 | **#2 (High Trust)** |
| 3 | `college-canteen-blog.com` | **1** (Page 2) | 1 | #5 | **#3 (Trusted by #1)** |
| 4 | `pizza-recipes-home.com` | **1** (Page 3) | 3 | #2 | **#4** |
| 5 | `cheap-eats-pune.com` | **1** (Page 4) | 1 | #6 | **#5** |
| 6 | `pizza-pizza-pizza.com` | **0** (No votes) | 10 | **#1 (Spam winner)** | **#6 (Demoted)** |

---

## 🚀 How to Run Locally

Start a local HTTP server:
```bash
python3 -m http.server 8000
```
Then visit [http://localhost:8000](http://localhost:8000) in your browser.
