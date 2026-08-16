# Bingeplay
# 🎬 BingePlay Data Analytics

BingePlay is a **data analytics and SQL-based minor project** designed to analyze user behavior, subscription patterns, content performance, viewing activity, engagement, revenue, and potential churn in a streaming platform.

The project combines **Python, Pandas, NumPy, MySQL, SQLAlchemy, and PyMySQL** to perform real-world data analysis using SQL queries and Python.

## 📌 Project Overview

The BingePlay analytics system uses a relational database containing information about users, subscriptions, shows, ratings, and watch sessions.

The project focuses on answering important business questions such as:

* How much monthly recurring revenue is generated?
* How are user signups growing?
* Which devices are used most frequently?
* How are ratings distributed?
* Do BingePlay Originals perform better than acquired content?
* Which users show binge-watching behavior?
* Which users signed up but never watched?
* Which Premium or Family users only watch Basic-plan content?
* How successful are subscription upgrades?
* Which shows generate the most comeback activity?
* Which users maintain long-term engagement?
* Which users show potential churn signals?

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* MySQL
* SQL
* SQLAlchemy
* PyMySQL
* Jupyter Notebook / Google Colab

## 🗄️ Database

The project uses a MySQL database named:

`bingeplay`

The database contains tables related to:

* Users
* Shows
* Subscriptions
* Watch Sessions
* Ratings

SQL queries are executed through SQLAlchemy and the results are loaded into Pandas DataFrames for analysis.

## 📊 Key Analysis Performed

### 1. Active Revenue

As of 30 June 2024:

* Active subscriptions: **2,340**
* Monthly recurring revenue: **₹784,260**

### 2. Signup Momentum

User signups increased during the first half of 2024.

* January: 350
* February: 400
* March: 500
* April: 550
* May: 600
* June: 600

May and June recorded the highest number of signups.

### 3. Device Analytics

The project analyzes:

* Total sessions
* Total watch minutes
* Average watch minutes per session
* Completion rate

Mobile recorded the highest number of sessions and total watch minutes.

### 4. Rating Distribution

The analysis found that:

**71.34% of all ratings were 4 or 5 stars.**

This indicates generally positive user feedback toward the available content.

### 5. Originals vs Acquired Content

| Content Type        | Shows | Average IMDb Rating |
| ------------------- | ----: | ------------------: |
| BingePlay Originals |    30 |                7.92 |
| Acquired Content    |    70 |                6.63 |

BingePlay Originals performed better by approximately **1.29 IMDb rating points**.

### 6. Binge Day Detection

A binge day is defined as a user watching the same show at least five times on the same calendar date.

Results:

* Total binge days: **414**
* Top binge user: **U02956**
* Binge days for top user: **8**

### 7. Users Who Never Watched

Among Q1 2024 signups:

* Total Q1 signups: **1,250**
* Users who never watched: **226**

This identifies users who registered but did not convert into active viewers.

### 8. Premium/Family Over-Paying Users

The analysis identified:

**6 Premium/Family users**

whose entire watch history consisted only of content available on the Basic plan.

These users may represent potential downgrade or plan-optimization opportunities.

### 9. Upgrade Success Cohort

The analysis identified:

* Qualifying users: **55**
* Average time from signup to first upgrade: **64.96 days**

These users started with Basic and later upgraded to Premium or Family while remaining active.

### 10. Cliffhanger Comebacks

A cliffhanger comeback occurs when a user has an incomplete session and returns to watch the same show within 1–7 days.

Results:

* Total comeback events: **4,345**
* Top show: **S088 — Rayalaseema Raga**
* Comeback events for the top show: **64**

### 11. Consecutive-Week Engagement

The project identifies users who watched at least one session for four or more consecutive calendar weeks.

Results:

* Users with 4+ week streaks: **1,675**
* Longest streak: **26 weeks**
* Example user with longest streak: **U00213**

### 12. Churn Signal Detection

Users were identified when their June 2024 watch minutes dropped by at least 50% compared with May 2024.

Results:

**521 users were identified as potential churn signals.**

These users can be considered potential targets for retention campaigns.

## 🔄 Project Workflow

```text
Raw Database
     ↓
MySQL Database
     ↓
SQL Queries
     ↓
SQLAlchemy Connection
     ↓
Pandas DataFrames
     ↓
Data Analysis
     ↓
Business Insights
     ↓
Churn / Engagement / Revenue Insights
```

## 📁 Project Structure

```text
BingePlay/
│
├── BingePlay_minor_project_3.ipynb
│
└── README.md
```

If the database setup file is added later, the structure can be extended to:

```text
BingePlay/
│
├── BingePlay_minor_project_3.ipynb
├── bingeplay_setup.sql
├── README.md
└── requirements.txt
```

## ⚙️ Installation

Install the required Python libraries:

```bash
pip install pandas numpy pymysql sqlalchemy
```

For Google Colab:

```python
!pip install pymysql sqlalchemy
```

## 🗄️ MySQL Setup

Create the BingePlay database and import the provided SQL setup file.

Example:

```bash
mysql -u root -p bingeplay < bingeplay_setup.sql
```

Then configure the SQLAlchemy connection:

```python
from sqlalchemy import create_engine

engine = create_engine(
    "mysql+pymysql://root:YOUR_PASSWORD@localhost/bingeplay"
)
```

Replace `YOUR_PASSWORD` with your MySQL password.

**Note:** Do not upload real passwords or database credentials to GitHub.

## ▶️ How to Run

### Using Jupyter Notebook

1. Install Python.
2. Install the required libraries.
3. Start Jupyter Notebook.
4. Open `BingePlay_minor_project_3.ipynb`.
5. Configure the MySQL database.
6. Update the database connection credentials.
7. Run the notebook cells sequentially.

### Using Google Colab

1. Upload the notebook to Google Colab.
2. Install the required packages.
3. Set up MySQL if required by the environment.
4. Configure the database connection.
5. Execute the notebook cells sequentially.

## 📈 Business Insights

The analysis provides useful insights for a streaming platform:

* Revenue monitoring through active subscriptions
* User acquisition tracking
* Device usage analysis
* Content quality comparison
* Identification of binge-watching users
* Detection of inactive new users
* Subscription plan optimization
* Upgrade behavior analysis
* Content comeback analysis
* Long-term engagement measurement
* Early churn detection

These insights can help streaming platforms improve **customer retention, subscription strategies, content planning, and user engagement**.

## 🎯 Project Objectives

The main objectives of BingePlay are:

1. Analyze streaming user behavior.
2. Understand subscription and revenue patterns.
3. Measure content performance.
4. Identify highly engaged users.
5. Detect potential churn users.
6. Analyze subscription upgrades.
7. Generate meaningful business insights using SQL and Python.

## 👩‍💻 Skills Demonstrated

Through this project, the following skills were demonstrated:

* SQL Query Writing
* MySQL Database Management
* Python Programming
* Pandas Data Analysis
* NumPy
* Database Connectivity
* Data Aggregation
* CTEs
* Window Functions
* Subqueries
* Date-Based Analysis
* Cohort Analysis
* User Engagement Analysis
* Churn Analysis
* Business Intelligence

