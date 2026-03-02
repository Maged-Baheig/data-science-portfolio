# 🚲 US Bikeshare Data Explorer

**Interactive Python CLI for exploring US bikeshare data**

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📋 Project Overview

| Aspect | Details |
|--------|---------|
| **Course** | Udacity Data Analysis Professional Nanodegree (FWD) |
| **Year** | 2020 |
| **Type** | Data Wrangling / Interactive Data Exploration |
| **Data** | US Bikeshare data (Chicago, New York, Washington) |
| **Period** | January 2017 – June 2017 |

---

## 🎯 Objective

Build an **interactive command-line tool** that allows users to explore US bikeshare data by:
- Selecting a city (Chicago, New York, Washington)
- Filtering by month and/or day
- Computing and displaying descriptive statistics
- Viewing raw data samples on demand

---

## ✨ Features

### 🔍 Interactive Filtering
- **City Selection:** Chicago, New York, or Washington
- **Month Filter:** January through June, or All
- **Day Filter:** Any day of the week, or All

### 📊 Statistics Computed

| Category | Statistics |
|----------|------------|
| **Time Statistics** | Most popular month, day, and start hour |
| **Station Statistics** | Most popular start station, end station, and trip |
| **Trip Duration** | Total and average travel time (seconds, minutes, hours) |
| **User Statistics** | User type counts, gender distribution, birth year analysis |
| **Summary Statistics** | Dataset shape, size, null values, descriptive stats |

### 🛡️ Robust Error Handling
- Input validation for all user selections
- Keyboard interrupt handling (Ctrl+C)
- Graceful exit options
- Clear error messages and retry prompts

### 📱 User Experience
- Welcome messages and clear instructions
- Visual formatting with ASCII art borders
- Loading animations
- Confirmation prompts before processing
- Option to restart or exit at any point

---

## 🚀 How to Run

### Prerequisites
```bash
pip install pandas
Run the Program
Bash

python bikeshare.py
Required Data Files
Place these CSV files in the same directory as bikeshare.py:

chicago.csv
new_york_city.csv
washington.csv
Note: Data files are not included in this repository due to size. They were provided as part of the Udacity nanodegree.

📁 Project Structure
text

us-bikeshare/
├── README.md           # This file
├── bikeshare.py        # Main Python script
└── requirements.txt    # Dependencies
🔧 Technical Implementation
Core Functions
Function	Purpose
get_filters()	Collect and validate user input for city, month, day
load_data()	Load and filter data based on user selections
summary_stats()	Display dataset overview and descriptive statistics
time_stats()	Compute most frequent times of travel
station_stats()	Find most popular stations and trips
trip_duration_stats()	Calculate total and average trip duration
user_stats()	Analyze user demographics
display_rawdata()	Show raw data in chunks of 5 rows
restart()	Handle program restart or exit
Data Processing
Python

# Key transformations performed:
df['Start Time'] = pd.to_datetime(df['Start Time'])
df['Start Month'] = df['Start Time'].dt.strftime("%b")
df['Start Day'] = df['Start Time'].dt.strftime("%a")
df['Start Hour'] = df['Start Time'].dt.hour
df['Trip'] = df['Start Station'] + " -TO-> " + df['End Station']
📊 Sample Output
text

╔════════════════════════════════════════════════════════════════╗
║  Statistics on the most frequent times of travel               ║
╚════════════════════════════════════════════════════════════════╝

Most Popular month: Jun
Most Popular day: Wed
Most Popular Start Hour: 5 PM

🕘 This statistics calc took 0.12 seconds.
🛠️ Tools & Technologies
Tool	Purpose
Python 3.x	Programming language
Pandas	Data manipulation and analysis
sys	System-specific parameters and functions
time	Time-related functions
📚 Skills Demonstrated
✅ Python Scripting – Modular function design, main() structure
✅ Data Wrangling – DateTime parsing, column creation, filtering
✅ Pandas Proficiency – read_csv, value_counts, mode, groupby operations
✅ User Experience Design – Interactive CLI with clear prompts
✅ Error Handling – Try-except blocks, input validation
✅ Code Documentation – Comprehensive comments and docstrings
🔗 Related Projects
Twitter WeRateDogs Wrangling – API data extraction and cleaning
Main Portfolio – Full data science project collection
📜 Acknowledgments
Udacity – For the excellent Data Analysis Professional Nanodegree
Motivate – For providing the bikeshare datasets
FWD (Egypt) – For sponsoring the scholarship
👤 Author
Maged Baheig

LinkedIn: https://www.linkedin.com/in/magedbaheig
GitHub: https://github.com/Maged-Baheig
Email: magedbaheig@gmail.com
