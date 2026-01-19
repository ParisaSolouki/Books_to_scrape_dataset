# 📚 BooksToScrape Web Scraper (Python)

A simple Python web scraping project that extracts book information from  
[BooksToScrape.com](https://books.toscrape.com/) using **BeautifulSoup** and **Pandas**.

This project is designed as a **learning and practice exercise** for web scraping fundamentals.

---

## 🧠 Project Overview

The goal of this project is to understand how real websites are structured
and how to extract useful data from HTML pages.

In this project, I practiced:
- Sending HTTP requests to a live website
- Parsing HTML structure with BeautifulSoup
- Extracting data from tags and attributes
- Handling relative URLs
- Cleaning simple text data
- Saving scraped data into a CSV file

---

## 📊 Data Extracted

For each book on the first page of the website, the following information is collected:

- **Title** – Full book title  
- **Price** – Book price (currency symbol removed)  
- **Star Rating** – Rating as text (One, Two, Three, Four, Five)  
- **Availability** – Stock status (e.g. *In stock*)  
- **Image URL** – Full URL of the book image  
- **Book Link** – Full URL to the book detail page  

---

## 🧩 Technologies Used

- **Python 3**
- **requests** – to download web pages
- **BeautifulSoup (bs4)** – to parse and navigate HTML
- **pandas** – to store data and export CSV files

---

## ⚙️ How It Works

1. **Send Request**  
   The script sends an HTTP request to the BooksToScrape website and retrieves the HTML content.

2. **Parse HTML**  
   BeautifulSoup parses the HTML document so specific elements can be found easily.

3. **Locate Book Containers**  
   Each book is inside an `<article class="product_pod">` element.

4. **Extract Data**  
   From each book container, the scraper extracts:
   - Title from the `title` attribute inside `<h3><a>`
   - Price from `<p class="price_color">`
   - Star rating from the `class` attribute of `<p class="star-rating">`
   - Availability from the text inside `<p class="instock availability">`
   - Image and book links (converted to full URLs)

5. **Store and Save**  
   The extracted data is stored in a Pandas DataFrame and saved as a CSV file.

---

## 📁 Project Structure

```text
books-to-scrape-scraper/
│
├── books_scraper.py
├── books_page1.csv
└── README.md

```
