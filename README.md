# Stack Overflow Developer Survey Analysis

## Overview
This project analyzes the Stack Overflow Developer Survey to uncover current and emerging technology trends, developer demographics, and job market demand. It combines survey data analysis with job posting data (collected via a custom Jobs API) and web-scraped salary data to build a complete picture of the developer technology landscape.

## Objectives
- Identify the most-used and most-wanted programming languages, databases, cloud platforms, and web frameworks
- Explore developer demographics (age, education level, geographic distribution)
- Analyze job posting demand by technology
- Compare average annual salary across programming languages
- Build an interactive dashboard to visualize all findings

## Data Sources
- **Stack Overflow Developer Survey** — current/future technology usage and demographics
- **Job posting data** — collected via a custom Flask Jobs API (`job-postings.xlsx`)
- **Programming language salary data** — collected via web scraping (`popular-languages.csv`)

## Tools & Technologies
- **Python** (Jupyter notebooks) — data cleaning, transformation, and analysis
- **IBM Cognos Analytics** — interactive dashboard (3 tabs: Current Technology Usage, Future Technology Trend, Demographics)
- **Flask** — API for serving job posting data
- **BeautifulSoup / Requests** — web scraping salary data
- **Pandas** — data wrangling and CSV/Excel export

## Repository Contents
```
├── notebooks/          # Jupyter notebooks (Jobs API, web scraping, analysis)
├── data/                # job-postings.xlsx, popular-languages.csv, survey data
├── presentation/        # Final capstone presentation (.pptx)
├── dashboard/            # Cognos dashboard screenshots/exports
└── README.md
```

## Methodology
1. Cleaned and analyzed survey responses in Python using Jupyter notebooks
2. Split and exploded multi-select survey fields (languages, databases, platforms, frameworks) for accurate counting
3. Computed top-10 rankings for current usage and future interest across each technology category
4. Built a Flask API to serve job posting records, then queried it by technology to get posting counts
5. Scraped average annual salary by programming language from a public data source
6. Built an interactive 3-tab dashboard in IBM Cognos Analytics

## Key Findings

### Technology Trends
- JavaScript, SQL, and HTML/CSS are the most widely used languages today; PostgreSQL leads as the top database
- Go and Rust show the strongest upward momentum among languages developers want to learn, while Java's future interest is declining
- AWS dominates cloud platform usage, both currently and for future adoption
- React and Node.js are the leading web frameworks in both current use and future interest
- Redis is climbing sharply in future database interest; Supabase emerges as a new top-10 database to watch

### Demographics
- Most respondents are aged 25–34 (41.3%) and hold a Bachelor's degree
- Respondent base skews toward early/mid-career developers

### Job Postings & Salary
- C dominates job postings by a wide margin (25,114 postings) — far ahead of Java (3,428) and JavaScript (2,248), likely reflecting sustained demand in systems, embedded, and enterprise software roles
- Python (1,173) and Oracle (899) round out the next tier of in-demand skills
- Despite C's overwhelming posting volume, it does not appear among the highest-paying languages — hiring demand and average salary don't always move together
- Swift commands the highest average annual salary ($130,801), followed by Python ($114,383) and C++ ($113,865)
- SQL ($84,793) and PHP ($84,727) have the lowest average salaries among the languages analyzed
- Python stands out as a strong all-around choice — solid job posting demand paired with one of the highest average salaries

## Implications
- Prioritize training budgets toward JavaScript/TypeScript, Go, and Rust
- Standardize on PostgreSQL with Redis for caching in new architecture decisions
- Continue investing in AWS-based infrastructure and React/Node.js tooling
- Use job posting volume and salary data together, not in isolation, when evaluating which skills to prioritize


## Presentation
See `presentation/` for the full capstone story deck covering methodology, findings, and conclusions.

## Author
Gandhar Dhage 

## Acknowledgments
Built as part of the IBM Data Analyst Professional Certificate capstone project.
