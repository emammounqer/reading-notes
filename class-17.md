# Class 17 - Web Scraping

## What are the key differences between scraping static and dynamic websites?

Usually, dynamic websites use AJAX to load content dynamically, or even the whole site is based on a Single-Page Application (SPA) technology.

In contrast to dynamic websites, we can observe static websites containing all the requested content on the page load.

In order to scrape dynamic websites, We need the HTML to be run in a browser to see the correct values and then be able to capture those values programmatically.

## Explain at least three techniques or best practices that can be employed to avoid getting blocked while scraping websites

- **Make the crawling slower**:
To scrape websites respectfully, slow down crawling speed, mimic human behavior, use delays and limit concurrent requests. Employ auto throttling mechanisms and periodically optimize crawling speed to adapt to changing conditions.

- **Do not follow the same crawling pattern**:
If you are crawling a website, do not follow the same crawling pattern. For example, if you are crawling a website and you are sending requests to the same page every 10 seconds, you are likely to get blocked. Instead, you should crawl the website in a random fashion. For example, you can crawl the website in a random fashion by sending requests to different pages at random intervals.

- **Use a proxy**:
If you are scraping a website, you should use a proxy. A proxy is a server that acts as an intermediary between your computer and the website you are scraping. A proxy will hide your IP address and will make it look like you are accessing the website from a different location. This will help you avoid getting blocked.

## What is Playwright, and how does it assist in web scraping tasks? Provide an example of a use case where Playwright would be particularly beneficial

Playwright is an effective web scraping tool that can facilitate data extraction with minimal effort.

Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable and fast.

```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch()
    page = browser.new_page()
    page.goto("http://whatsmyuseragent.org/")
    page.screenshot(path="example.png")
    browser.close()
```

## Describe the purpose of using Xpath in web scraping, and provide an example of an Xpath expression to select a specific HTML element from a webpage

the purpose of using Xpath in web scraping is to select a specific HTML element from a webpage.

```python
    page.click("input[name=\"q\"]")
    page.fill("input[name=\"q\"]", "playwright github")
    page.press("input[name=\"q\"]", "Enter")
    page.wait_for_selector("text=microsoft/playwright: Node.js library to automate …")
    page.click("text=microsoft/playwright: Node.js library to automate …")
    page.click("text=Code")
```
