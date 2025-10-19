# 📚 BooksToScrape Web Scraper

A simple Python web scraping project that extracts book titles, prices, and links from [BooksToScrape.com](https://books.toscrape.com/) using **BeautifulSoup** and **Pandas**.

---

## 🧠 Project Overview

This project demonstrates the fundamentals of web scraping:
- Sending HTTP requests using `requests`
- Parsing HTML structure using `BeautifulSoup`
- Extracting specific tags and attributes
- Storing data in a clean Pandas DataFrame
- Exporting the scraped data into a CSV file

---

## 🧩 Technologies Used

- **Python 3.x**
- **BeautifulSoup4**
- **Requests**
- **Pandas**

---

## ⚙️ How It Works

1. **Connect to Website:**  
   The script sends a request to the BooksToScrape website and downloads the HTML page.

2. **Parse the HTML:**  
   BeautifulSoup parses the HTML so you can easily find specific tags and classes.

3. **Extract Data:**  
   Each book’s data is located inside an `<article class="product_pod">` tag.  
   The scraper extracts:
   - Title → from `<h3><a title="..."></a></h3>`
   - Price → from `<p class="price_color">`
   - Link → from the `href` attribute inside the `<a>` tag.

4. **Store and Save:**  
   The extracted data is saved in a structured Pandas DataFrame and exported as `books_to_scrape_dataset.csv`.

---

## 📊 Sample Output

| Title | Price | Link |
|-------|--------|------|
| A Light in the Attic | £51.77 | catalogue/a-light-in-the-attic_1000/index.html |
| Tipping the Velvet | £53.74 | catalogue/tipping-the-velvet_999/index.html |
| Soumission | £50.10 | catalogue/soumission_998/index.html |

---

## 🧱 How to Run

### 1️⃣ Install Dependencies
```bash
pip install requests beautifulsoup4 pandas
