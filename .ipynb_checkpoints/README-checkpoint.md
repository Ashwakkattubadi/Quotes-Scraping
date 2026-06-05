# Quotes Scraper

A Python web scraping project that collects quotes and author information from the Quotes to Scrape website, stores the raw HTML pages locally, extracts structured data using BeautifulSoup, and exports the cleaned data to a CSV file using Pandas.

## Features

* Scrapes quotes from multiple pages
* Handles pagination automatically
* Stores raw HTML pages for future use and debugging
* Extracts quote text and author names
* Creates a structured dataset
* Exports data to CSV format

## Technologies Used

* Python
* Requests
* BeautifulSoup4
* lxml
* Pandas

## Project Structure

```text
project/
│
├── scraped_data/
│   ├── page1.html
│   ├── page2.html
│   ├── ...
│
├── clean_data/
│   └── data.csv
│
├── scraper.py
└── README.md
```

## How It Works

### Step 1: Data Collection

The scraper visits each page of the website and downloads the HTML content.

Example pages:

```text
https://quotes.toscrape.com/page/1/
https://quotes.toscrape.com/page/2/
...
```

The downloaded HTML files are stored inside the `scraped_data` folder.

### Step 2: Data Extraction

BeautifulSoup parses each saved HTML file and extracts:

* Quote text
* Author name

### Step 3: Data Storage

The extracted data is stored in a Pandas DataFrame and exported to:

```text
clean_data/data.csv
```

## Sample Output

| Quote                                                           | Author          |
| --------------------------------------------------------------- | --------------- |
| “The world as we have created it is a process of our thinking.” | Albert Einstein |
| “It is our choices, Harry, that show what we truly are.”        | J.K. Rowling    |
| “A day without sunshine is like, you know, night.”              | Steve Martin    |

## What I Learned

* Sending HTTP requests using Requests
* Handling pagination in web scraping
* Parsing HTML with BeautifulSoup
* Using CSS selectors for data extraction
* Reading and writing files in Python
* Working with Pandas DataFrames
* Exporting structured data to CSV

## Future Improvements

* Extract tags associated with each quote
* Store data in a database
* Add logging and error handling
* Build a command-line interface
* Scrape additional websites and combine datasets

## Dataset Size

* Pages Scraped: 10
* Quotes Extracted: 100
* Authors Extracted: 100

## Author

Ashwak Kattubadi
