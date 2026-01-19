# 📚 Books To Scrape – Multi-Page Web Scraper (Python)

A simple Python project that scrapes book data from multiple pages of  
[BooksToScrape.com](https://books.toscrape.com/) using **BeautifulSoup** and **Pandas**.

This project extends a single-page scraper to handle **multiple pages**.

---

## 🧠 Project Overview

The goal of this project is to practice real-world web scraping by:
- Looping through multiple pages
- Understanding URL patterns
- Extracting structured data from HTML
- Cleaning simple text fields
- Saving the final dataset into a CSV file

The code is intentionally kept **simple and beginner-friendly**.

---

## 📊 Data Extracted

For each book across multiple pages, the scraper collects:

- **Title** – Full book title  
- **Price** – Book price (currency symbol removed)  
- **Star Rating** – One, Two, Three, Four, Five  
- **Availability** – Stock status (e.g. *In stock*)  
- **Image** – Full image URL  
- **Link** – Full book detail page URL  

---

## 🧩 Technologies Used

- Python 3  
- requests  
- BeautifulSoup (bs4)  
- pandas  

---

## ⚙️ How It Works

1. **Page Range Input**  
   The user specifies a start and end page.

2. **Send Requests**  
   The script loops through pages and sends HTTP requests.

3. **Parse HTML**  
   BeautifulSoup parses each page’s HTML.

4. **Extract Book Data**  
   Each book is located inside `<article class="product_pod">`.

5. **Store Results**  
   All extracted data is stored in lists and converted to a DataFrame.

6. **Save CSV**  
   The final dataset is saved as `books_multi_page.csv`.

---

## 📁 Project Structure

```text
books-to-scrape-multi-page/
│
├── books_scraper_multi_page.py
├── books_multi_page.csv
└── README.md
