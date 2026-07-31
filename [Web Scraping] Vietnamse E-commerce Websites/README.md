# 🛒 E-commerce Product Data Crawling

A Python-based web scraping project designed to collect product information from two of Vietnam's largest e-commerce platforms—**Lazada** and **Tiki**. The project automates data extraction for product listings, pricing, ratings, reviews, brands, and seller information, creating structured datasets for market research, competitive analysis, and downstream data analytics.

## 📊 Key Features

- Automated product data collection from Lazada and Tiki
- Product name, category, price, and discount extraction
- Product ratings and customer review statistics
- Brand and seller information collection
- Pagination support for large-scale crawling
- Export structured datasets for further analysis

## 🧹 Data Collection Process

The project consists of two independent crawlers developed for Lazada and Tiki, following a common scraping workflow.

The workflow includes:

- Sending HTTP requests to product listing pages
- Parsing HTML responses
- Extracting product attributes
- Handling multiple pages of search results
- Cleaning and validating collected data
- Exporting datasets to CSV format for analysis

The resulting datasets can be used for price monitoring, competitor benchmarking, recommendation systems, customer behavior analysis, and business intelligence applications.

## 📁 Tools & Technologies

- **Python**
- **Requests** – HTTP requests
- **BeautifulSoup** – HTML parsing
- **Pandas** – Data processing and cleaning
- **CSV** – Data storage
- **Jupyter Notebook**

## 🧠 Additional Highlights

- Automated web scraping workflow
- Multi-platform e-commerce data collection
- Structured and clean datasets ready for analysis
- Reusable crawler architecture for other online marketplaces
