# pulse-review-scraper
Pulse Assignment 4 – SaaS Review Scraper
Overview

This project is a Python-based web scraping script developed as part of Pulse Assignment 4.
The objective of this assignment is to collect SaaS product reviews from an online platform and store them in a structured JSON format.

In this implementation, reviews are scraped from Capterra for a SaaS product (Slack) using Python libraries.

Purpose

The purpose of this project is to demonstrate:

Web scraping using Python

Extracting structured review data from HTML pages

Handling request failures gracefully

Saving scraped data in JSON format

The script focuses on simplicity while meeting all the assignment requirements.

Data Source
Capterra

Capterra is used as the review source because it provides publicly available SaaS product reviews with clear HTML structure.
The platform contains review titles and descriptions that can be easily extracted using HTML parsing techniques.

Features Implemented

Sends HTTP requests with custom headers to avoid blocking

Scrapes review titles and review descriptions

Extracts data only when valid review elements are found

Implements basic error handling using try–except

Uses fallback sample data if scraping fails

Stores output in a clean JSON format

Technologies Used

Python 3 – Core programming language

Requests – For making HTTP requests

BeautifulSoup (bs4) – For parsing HTML content

JSON module – For storing output data

Code Explanation (High Level)

Sends a GET request to the Capterra review page using a custom User-Agent.

Parses the HTML content using BeautifulSoup.

Locates review blocks using <article> tags.

Extracts:

Review title (<h3>)

Review content (<p>)

Stores extracted reviews in a Python list.

If scraping fails or the site blocks the request, fallback review data is used.

Saves the final output into output.json.

Project Structure
pulse-review-scraper/
│
├── scraper.py        # Python script for scraping reviews
├── output.json       # Generated JSON file with reviews
├── requirements.txt # Dependency list
└── README.md        # Project documentation

How to Run the Project
Step 1: Install dependencies
pip install requests beautifulsoup4

Step 2: Run the script
python scraper.py

Output Format

The script generates an output.json file containing an array of reviews.

Each review includes:

title – Review title

review – Review description

source – Review platform (Capterra)

Sample Output
[
  {
    "title": "Excellent collaboration tool",
    "review": "Slack improves team communication and productivity.",
    "source": "Capterra"
  }
]

Error Handling

Handles request failures using try–except blocks

Detects non-200 HTTP responses

Provides fallback sample review data if scraping fails

Prevents program crashes due to missing HTML elements

Notes

This project is created strictly for educational purposes.

The implementation is original and completed individually.

The script demonstrates a simple and effective approach to web scraping without unnecessary complexity.

Conclusion

This project successfully fulfills the requirements of Pulse Assignment 4 by scraping SaaS reviews, handling errors gracefully, and generating structured JSON output using Python.
