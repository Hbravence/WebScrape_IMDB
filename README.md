# IMDb Top 250 Web Scraping Project

## Project Overview
This project focuses on scraping data from the IMDb Top 250 movies list. The goal was to extract, clean, and analyze the data to gain insights into trends such as the most common release years. The dataset was ultimately stored in a CSV file for further exploration.

## Challenges & Solution Approach
Initially, I attempted to scrape the data using the `requests` library and `BeautifulSoup`. However, the IMDb Top 250 list loads dynamically, meaning that only a partial dataset (the first 25 movies) was retrievable. Since the content was generated via JavaScript, traditional static scraping techniques were ineffective.

To overcome this, I incorporated **Selenium**, a browser automation tool that enabled interaction with the page. I built a function to **scroll down to the end of the list**, ensuring that all 250 movies were fully loaded before extraction.

## Technical Implementation

### Web Scraping Process
- Used Selenium to simulate scrolling and capture the dynamically loaded HTML.
- Printed the first movie’s HTML at the highest **DOM hierarchy** level to understand the structure.
- Parsed movie details and stored them in a dictionary.
- Iterated over each movie entry to build a complete dataset.

### Data Cleaning & Structuring
- Converted the dataset into a **Pandas DataFrame**.
- Cleaned and structured the data for analysis.
- Extracted relevant insights.

### Analysis Performed
- Identified the **most popular release year** based on the number of entries in the IMDb Top 250.
- Found that **1994** had the highest number of top-rated movies.

### Data Export
- Saved the final dataset as a **CSV file** for future use.

## Key Takeaways
- **Dynamic web pages require interactive scraping techniques**, such as Selenium, to access complete datasets.
- **Understanding DOM hierarchy** was essential for efficient data extraction.
- Even simple analyses, such as identifying the most popular movie release year, can provide interesting insights.

## Next Steps
While the primary goal was to demonstrate web scraping, future improvements could include:
- Expanding the analysis (e.g., genre distributions, director trends).
- Enhancing automation to scrape additional movie-related details.
- Optimizing performance to reduce script execution time.

## Dependencies
- Python  
- Selenium  
- Pandas  
- BeautifulSoup  

## Usage
To run this project:

```bash
pip install selenium pandas beautifulsoup4
