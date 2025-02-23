# Movie Data Scraping and Analysis

**A data-driven project that scrapes movie data and performs exploratory data analysis (EDA) to uncover insights about genres, user ratings, return on investment (RIO), and durations.**

## Table of Contents
- [Introduction](#introduction)
- [Data Collection](#data-collection)
- [Data Processing](#data-processing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Results and Insights](#results-and-insights)
- [Future Improvements](#future-improvements)


## Introduction
This project focuses on collecting and analyzing movie data from **The Movie Database (TMDb)**. The goal is to understand the relationship between movie genres, user ratings, return on investment (RIO), and movie durations by applying **data scraping, data preprocessing, and data analysis**.

The project consists of two main components:
1. **Web Scraping:** Extracting key movie details from TMDb, including title, release year, user ratings, descriptions, directors, screenplay, genres, revenue, and budget.
2. **Exploratory Data Analysis (EDA):** Analyzing trends and patterns in movie data to understand audience preferences, financial performance, and runtime variations.

## Data Collection
The movie data is collected using **Request and BeautifulSoup** for web scraping from TMDb.
The process involves:
- Extracting movie URLs dynamically by navigating through multiple pages.
- Parsing movie details such as **title, release year, user ratings, description, genre, director, screenplay, revenue, and budget**.
- Handling potential website limitations by introducing **random delays** between requests to avoid being blocked.
- Storing the collected data into structured CSV files for further analysis.

Additionally, an extra dataset is scraped, including: **movie length (runtime), original language, media statistics (number of videos, backdrops, and posters associated with each movie)**

The collected datasets are later merged for a comprehensive analysis.


## Data Processing
After collecting the data, the following preprocessing steps are applied:
- **Cleaning Missing Values:** Filling in missing data fields and handling inconsistencies in scraped content.
- **Data Type Conversion:** Converting numerical fields like user scores, revenue, and budget into appropriate formats.
- **Handling Categorical Data:** Splitting genres and ensuring each movie can be analyzed within multiple genre categories.
- **Merging Datasets:** Combining the main dataset with additional scraped data for deeper insights.

To ensure high-quality analysis, **data transformation** is also performed, including:
- Normalizing revenue and budget values to remove currency formatting.
- Converting runtime from hours and minutes format into a standardized numerical format (minutes).
- Removing outliers and anomalous data points that could skew analysis.


## Exploratory Data Analysis
### **1. Relationship Between Movie Genres and User Ratings**
- Investigates how different **movie genres** impact **user ratings**.
- Uses **box plots and bar charts** to visualize the distribution of ratings across genres.
- Highlights genres with consistently **high or low audience ratings**.
<img width="500" alt="Screenshot 2025-02-23 at 15 26 29" src="https://github.com/user-attachments/assets/3e317c6f-65ed-474a-ba33-da449b30be60" />
<img width="500" alt="Screenshot 2025-02-23 at 15 27 29" src="https://github.com/user-attachments/assets/6b490fa8-8373-44e8-a2ef-a6180a1f4453" />


### **2. Relationship Between Movie Genres and Return on Investment (RIO)**
- Analyzes how **financial performance varies across movie genres**.
- Computes **RIO (Return on Investment) as (Revenue - Budget) / Budget**.
- Identifies **profitable and underperforming genres** through statistical analysis and **line charts**.
<img width="600" alt="Screenshot 2025-02-23 at 15 29 09" src="https://github.com/user-attachments/assets/45809bfc-497d-4d24-8a05-874e20f23525" />



### **3. Relationship Between Movie Duration and Genres**
- Studies how **runtime varies across different movie genres**.
- Uses **line charts and box plots** to examine **average movie length per genre**.
- Identify **which genres tend to have longer or shorter movies**.
<img width="500" alt="Screenshot 2025-02-23 at 15 30 41" src="https://github.com/user-attachments/assets/dd9b9943-d0f5-421c-8af3-156b398ba66c" />
<img width="500" alt="Screenshot 2025-02-23 at 15 30 54" src="https://github.com/user-attachments/assets/09ea24ac-6f69-4202-b2f7-d32322cc03af" />



## Results and Insights
- **User Ratings Trends:** **Fantasy, Family, and Animation** movies receive the highest average user scores, indicating broad audience appeal.
- **Financial Performance:** Certain genres like **Action and Sci-Fi** tend to have **higher RIO** due to international appeal, while **Drama and Documentary** movies often show lower financial returns.
- **Runtime Differences:** **Historical movies** tend to be significantly **longer**, averaging over 140 minutes, while **TV movies** are the shortest, averaging just 67 minutes.
- **Inconsistent Data Observations:** Some genres like **War and Music** have fewer samples, leading to **high variability in user ratings and financial performance**.


## Future Improvements
- **Expand Data Scope:** Scrape a **larger dataset** (e.g., 1000+ movies) to improve accuracy.
- **Sentiment Analysis:** Analyze **user reviews and comments** to understand audience opinions beyond numerical ratings.
- **Machine Learning Models:** Implement **predictive models** to forecast **movie success based on historical data**.
- **Streaming Platform Data:** Compare **box office movies with streaming-exclusive releases** to explore new trends.
