# Google Image Scraper for image_crawling

This Python script uses Selenium and BeautifulSoup to scrape images from Google Image Search based on a user-provided keyword and saves them to Google Drive.

## Features

*   Takes a search keyword as input.
*   Scrolls down the Google Images page to load more results.
*   Extracts image URLs from the search results.
*   Downloads images and saves them to a specified folder in Google Drive.
*   Runs in headless mode (no browser window displayed).

## Prerequisites

Before running this script, make sure you have the following installed:

*   Python 3.6+
*   `pip` package manager

## Installation

1.  Clone this repository (or download the script).
2.  Install the required Python libraries:

    ```bash
    pip install beautifulsoup4 selenium
    ```
3.  **For Google Colab:**
    *   Mount your Google Drive.
    *   The necessary `chromium-browser` and `chromedriver` setup is handled within the provided Colab notebook cells.
4.  **For Local Execution:**
    *   Install Google Chrome browser.
    *   Download the appropriate `chromedriver` executable for your Chrome version from [https://chromedriver.chromium.org/downloads](https://chromedriver.chromium.org/downloads).
    *   Make sure the `chromedriver` executable is in your system's PATH or provide the full path to the executable in the script.

## Usage

1.  Run the Python script:

    ```bash
    python your_script_name.py
    ```
2.  When prompted, enter the search keyword for the images you want to download.
3.  The script will scrape and save the images to your Google Drive (or local machine if you modify the save path).

## Code Explanation

*   The script uses `selenium` to automate browser actions like opening the page and scrolling.
*   It uses `beautifulsoup4` to parse the HTML content and find image elements.
*   Image URLs are extracted from `src` or `data-src` attributes.
*   `urllib.request.urlretrieve` is used to download the images.
*   Images are saved to `/content/drive/MyDrive/Colab Notebooks/images/<your_keyword>/` in Google Drive when run in Colab. You can change this path for local execution.
*   The script runs in headless mode (`--headless`) meaning the browser window is not visible during execution.

## Notes

*   This script relies on the current structure of the Google Image Search page. Changes to the website's HTML structure may break the script.
*   Be mindful of Google's terms of service and robots.txt when scraping. Avoid making too many requests in a short period to prevent being blocked.
*   The number of images downloaded depends on the number of scrolls (`num` variable) and the number of images loaded per scroll.
