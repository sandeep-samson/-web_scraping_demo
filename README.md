# Web Scraping Demo

The provided Python script is a web scraping tool designed to extract job postings from XYZ.com, an Indian job search website. It utilizes Selenium for browser automation and BeautifulSoup for HTML parsing.

**Script Flow**

1.  **Initialization**: The script starts by importing necessary libraries, including `time`, `pandas`, and Selenium's `webdriver`.
2.  **Browser Setup**: A Chrome browser instance is created using Selenium.
3.  **Navigation**: The script navigates to Naukri.com.
4.  **Search Query**: The search input field is located, and a search query `"web scraping"` is sent to it.
5.  **Button Click**: The corresponding button on the page is clicked.
6.  **Scraping Loop**: A while loop continuously scrapes the webpage for job postings until stopped.

**Job Posting Scraping**

For each job posting:

1.  **HTML Parsing**: BeautifulSoup parses the HTML of the current webpage.
2.  **Postings Identification**: All job postings on the page with class name `cust-job-tuple` are identified.
3.  **Detail Extraction**: For each posting, details like link, title, company name, experience, salary, and location are extracted.

**Data Storage**

*   **DataFrame Initialization**: An empty pandas DataFrame is created to store scraped data with column names 'Title', 'Comp Name', 'Exprience', 'Salary', 'Location', and 'Link'.
*   **Row Creation**: For each posting, a new row is created in the DataFrame.
*   **Data Append**: The newly created row is appended to the main DataFrame.

**Saving Scraped Data**

After all job postings have been scraped, the script saves the data to a CSV file named `scraped_data.csv`.

**Cleanup**

Finally, the browser instance is closed.
