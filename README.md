# Pulse Assignment 4 – SaaS Review Scraper

## Purpose
This project collects reviews of SaaS products from online platforms and saves them in JSON format.  
It demonstrates web scraping techniques, structured data handling, and robust error management using Python.

## Chosen Platform
- **Capterra**

Capterra was chosen because it offers publicly accessible reviews for SaaS products and a consistent page structure, making it suitable for scraping exercises.


## Technologies Used
- Python 3
- Requests library
- BeautifulSoup (bs4) for HTML parsing

## Project Files
pulse-review-scraper/
│
├── scraper.py # Main script to fetch and save reviews
├── requirements.txt # Python dependencies
├── README.md # This documentation
└── output.json # Scraped reviews saved in JSON



## Setup Instructions

1. Create virtual environment
```bash
python -m venv venv
venv\Scripts\activate

2. Install dependencies
pip install -r requirements.txt

Running the Scraper

Run the Python script:

python scraper.py


The program will generate output.json containing the reviews.

Sample Output
[
  {
    "title": "Excellent collaboration tool",
    "review": "Slack improves team communication and productivity.",
    "source": "Capterra"
  }
]

Handling Access Restrictions (HTTP 403)

Sometimes websites block automated requests (HTTP 403).
This scraper includes a fallback mechanism that provides sample review data when live scraping is blocked.
This ensures the script always produces valid JSON and demonstrates graceful error handling.

