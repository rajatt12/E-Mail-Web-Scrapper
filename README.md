# 📧 E-Mail Web Scraper using Python

A Python-based automation tool that extracts publicly available email addresses from company websites.

This project reads a CSV file containing company names and website URLs, visits multiple commonly used pages (Careers, Contact, About, etc.), extracts email addresses using Regular Expressions, prioritizes HR-related emails, and exports the results into a structured CSV file.

---

## 🚀 Features

- Reads company website list from CSV
- Automatically checks multiple common pages
- Extracts emails using Regex
- Filters HR-related emails (hr, career, job, recruit, talent)
- Removes duplicate emails
- Handles errors (timeouts, invalid URLs)
- Saves results into structured CSV format

---

## 🛠 Tech Stack

- Python 3.x
- requests
- BeautifulSoup (bs4)
- re (Regular Expressions)
- pandas
- urllib.parse

---
## 📂 Project Structure

E-Mail-Web-Scraper/

│
├── companies.csv # Input file containing company names & websites

├── script.ipynb # Main Python script for scraping emails

├── companies_with_emails.csv # Generated output file with extracted emails

└── README.md # Project documentation

---

## 📥 Input File Format (companies.csv)

Your CSV file must follow this structure:

Company_Name,Website  
TCS,https://www.tcs.com  
Infosys,https://www.infosys.com  
Wipro,https://www.wipro.com  

Required columns:
- Company_Name
- Website

---

## ⚙️ Installation

Install required dependencies:

pip install requests beautifulsoup4 pandas

---

## ▶️ How to Run

Run the script from the project directory:

python script.ipynb

After execution, a new file will be generated:

companies_with_emails.csv

---

## 📊 Output Format

| Company_Name | Website | Extracted_Email |
|--------------|----------|----------------|
| TCS | https://tcs.com | hr@tcs.com |
| Infosys | https://infosys.com | Not Found |

---

## 🧠 How It Works

1. Reads company websites from companies.csv
2. Iterates through each company
3. Visits multiple common paths:
   - /
   - /careers
   - /career
   - /jobs
   - /contact
   - /about
   - /join-us
4. Extracts emails using regex pattern:
   [a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+
5. Removes duplicate emails
6. Filters HR-related emails
7. Saves results into output CSV

---

## ⚠️ Disclaimer

This tool is intended for educational purposes only.
Always respect website terms of service and scraping policies before using it on real-world websites.

---

## 🚀 Future Improvements

- Add multithreading for faster scraping
- Add User-Agent headers
- Add logging system
- Add retry mechanism
- Integrate automatic email sender
- Store results in a database

---

## 👨‍💻 Author

Developed using Python for automation and learning purposes.
