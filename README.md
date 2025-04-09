# Web Scraping Wuzzuf Platform for Data Analyst Jobs

This project is focused on scraping job data from the Wuzzuf platform. It extracts job titles, company names, locations, job links, and job types for **Data Analyst** and **Business Data Analyst** positions. The scraping is done using Python libraries such as BeautifulSoup and Requests, and the extracted data is saved directly into a CSV file.

## Project Overview

The goal of this project is to gather detailed information about job postings from the Wuzzuf platform, specifically focusing on Data Analyst and Business Data Analyst positions. By scraping relevant data, the project aims to create a collection of job listings in CSV format that can be easily analyzed for trends and insights.

### Features
- Extracts **job title**, **company name**, **location**, **job link**, and **job type**.
- Scrapes data for **Data Analyst** and **Business Data Analyst** job positions.
- Uses **BeautifulSoup** for parsing HTML content.
- Makes HTTP requests with the **Requests** library.
- Saves the collected data in a **CSV** file.
- Data collection from two different URLs to capture a wide range of listings.

## Installation

To run this project, you will need to install the following dependencies:

```bash
pip install requests
pip install beautifulsoup4
```

## How to Use

1. Clone or download the project.
2. Open the Jupyter Notebook.
3. Run the cells to initiate the scraping process.
4. The script will collect the job data and store it in a CSV file named `wuzzuf_job_data.csv`.

## Code Walkthrough

1. **Requests**: The `requests` library is used to send GET requests to the Wuzzuf job listings pages.
2. **BeautifulSoup**: Parses the HTML content of the response and extracts the required job information (title, company name, location, job link, job type).
3. **CSV File**: The extracted data is written directly to a CSV file (`wuzzuf_job_data.csv`) without using a dictionary.
4. **URLs**: Two URLs are used to extract job data for Data Analyst and Business Data Analyst positions.
5. The data is stored in rows with columns representing the job title, company name, location, job link, and job type.

## Example Output

The script will generate a CSV file (`wuzzuf_job_data.csv`) with the following columns:

| Job Title            | Company Name        | Location    | Job Link                          | Job Type   |
|----------------------|---------------------|-------------|-----------------------------------|------------|
| Data Analyst         | XYZ Corp            | Cairo       | [Link](https://www.wuzzuf.com)    | Full-time  |
| Business Data Analyst| ABC Ltd             | Alexandria  | [Link](https://www.wuzzuf.com)    | Part-time |

## Dependencies

Make sure you have the following libraries installed before running the code:

- `requests`: To send HTTP requests to the Wuzzuf platform.
- `beautifulsoup4`: For parsing the HTML content of the web pages.
- `pandas`: (Optional) If you want to further manipulate the data.

You can install all dependencies by running:

```bash
pip install -r requirements.txt
```

Create a `requirements.txt` file with the following content:

```
requests
beautifulsoup4
pandas
```

## How the Script Works

### Step 1: Send HTTP Requests
The script first sends GET requests to the two URLs for Data Analyst and Business Data Analyst job listings. This allows it to fetch the raw HTML content of those pages.

### Step 2: Parse HTML with BeautifulSoup
After receiving the HTML content, **BeautifulSoup** is used to parse the page and extract the relevant information, such as:
- **Job title**
- **Company name**
- **Location**
- **Job link**
- **Job type** (e.g., Full-time, Part-time)

### Step 3: Write Data to CSV
The extracted data is written directly to a CSV file (`wuzzuf_job_data.csv`). Each row in the CSV file represents a job posting, and the columns include:
- Job Title
- Company Name
- Location
- Job Link
- Job Type

### Step 4: Output the Data
The data is stored in a CSV file that can be opened in tools like Excel or used for further analysis.



