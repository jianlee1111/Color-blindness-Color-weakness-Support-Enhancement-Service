# Google Image Crawler (for Colab)

## Overview
This program is a Python-based crawler that automatically collects and downloads images from **Google Image Search**.  
By entering a keyword, the script uses Selenium to navigate the image search results, clicks thumbnails to retrieve the **full-resolution image URLs**, and saves them locally or in Google Drive.

This project is designed to work in **Google Colab**, with automatic setup of `Chromium` and `Chromedriver`.

---

## Features
- Automatic image collection based on user-input keyword  
- Auto-scrolling and dynamic loading of Google Image Search results  
- Thumbnail clicking to extract high-resolution image URLs  
- Image downloading using `requests` with custom User-Agent (to prevent 403 errors)  
- Automatic folder creation and Google Drive support  
- Duplicate URL filtering and data URL exclusion

---

## Tech Stack
| Component | Description |
|------------|-------------|
| Python 3.9+ | Programming language |
| Selenium | Web automation and scrolling/clicking |
| BeautifulSoup | HTML parsing (optional) |
| Requests | Image downloading |
| Chromium / Chromedriver | Browser and driver for Colab |
| Google Colab | Execution environment and Drive integration |

---

## Project Structure
