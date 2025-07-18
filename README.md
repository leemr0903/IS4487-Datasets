# Intro to Business Analytics Module Dataset Assignment Plan

| Module | Topic                         | Lab Dataset                                  | Assignment Dataset                                                |
|--------|-------------------------------|----------------------------------------------|-------------------------------------------------------------------|
| 1      | Overview of Business Analytics | —                                            | Case Study                                                        |
| 2      | Intro to Analytical Models     | —                                            | Case Study                                                        |
| 3      | Business Understanding         | —                                            | Case Study                                                        |
| 4      | Data Understanding             | [SF Rents](#sf-rents)                        | [AdviseInvest](#adviseinvest)                                     |
| 5      | EDA – Summary Measures         | [SF Rents](#sf-rents)                        | [Hotels](#hotels)                                                 |
| 6      | Data Preparation               | [Megatelco_Duplicates](#megatelco_duplicates) | [Inside Airbnb – City Dataset](https://insideairbnb.com/get-the-data/) |
| 7      | Data Transformation            | [Megatelco_Duplicates](#megatelco_duplicates) | [Inside Airbnb – City Dataset](https://insideairbnb.com/get-the-data/) |
| 8      | Exam Week                      | —                                            | —                                                                 |
| 9      | Modeling & Evaluation I        | [SF Rents](#sf-rents)                        | [Hotels](#hotels)                                                 |
| 10     | Modeling & Evaluation II       | [SF Rents](#sf-rents)                        | [AdviseInvest](#adviseinvest)                                     |
| 11     | Modeling & Evaluation III      | [Employee Attrition](#employee-attrition)    | [Global Holidays & Travel](#global-holidays-and-travel)          |
| 12     | Modeling & Evaluation IV       | [Super Bowl Commercials](#super-bowl-commercials) | [GPT Detectors](#gpt-detectors) or Super Bowl dataset             |
| 13     | Modeling & Evaluation V        | [Online Food Orders & Restaurant Reviews](#online-food-orders) | [Amazon Sales Dataset](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset) |
| 14     | Model Deployment               | [Reddit Post Titles](#reddit-post-titles)    | [YFinance – Stock Prices](https://finance.yahoo.com/)             |
| 15     | Final Project & Wrap-Up        | Student Choice                               | —                                                                 |


# Dataset Outlines

This table includes curated datasets for an introductory business analytics course. Each entry includes the dataset’s year, a short description, suitability criteria (showing the number of variables, target variable if applicable, and types of data quality issues), and the GitHub link or dataset source.

| Dataset Name                 | Year | Description                                                           | Business Application                        | # Variables | Target Variable         | Data Quality Issues                      | Special Features                         | GitHub/Source                                                                                          | Relevant Majors/Minors                           |
|-----------------------------|------|-----------------------------------------------------------------------|---------------------------------------------|-------------|--------------------------|-------------------------------------------|------------------------------------------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| **SF Rents**                | 2022 | Rental prices in San Francisco over time.                            | Urban economics, housing markets            | ~12         | `rent`                   | Price outliers, missing records           | Outliers, geospatial prep                | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2022/2022-07-05/readme.md)       | Real Estate, Business Analytics (minor)         |
| **Megatelco_Duplicates**    | 2023 | Demographic, usage, and churn survey data from a telecom firm.       | Churn analysis, customer segmentation       | 16          | `Leave`                  | Categorical harmonization, NA entries     | Survey + behavioral + financial fields   | *Local (CSV uploaded)*                                                                                 | Information Systems, Business Analytics          |
| **Online Food Orders**      | 2023 | Survey data on online food delivery user behavior.                   | Customer profiling, food delivery trends    | 13          | —                        | Ambiguous target, parsing cleanup         | Geolocation, preferences, frequency      | *Local (CSV uploaded)*                                                                                 | Marketing, Business Analytics                    |
| **Restaurant Reviews**      | 2020s| Free-text restaurant reviews with binary sentiment labels.           | NLP, sentiment analysis                     | 2           | `Liked`                  | Sparse entries, binary imbalance possible | NLP-ready binary text                    | *Local (TSV uploaded)*                                                                                 | Marketing, Business Analytics                    |
| **Amazon Reviews**          | 2022 | Product review sentiment from Amazon product pages.                  | NLP, product analytics                      | 16          | `sentiment`              | Class imbalance, sparse text              | Free-text reviews                        | *Local (CSV uploaded)*                                                                                 | Marketing, Business Analytics                    |
| **Super Bowl Commercials**  | 2021 | Super Bowl ad features and viewer response over 20+ years.           | Media, branding, marketing impact           | ~15         | `likeability` (proxy)    | Missing flags, categorical encoding       | Text, categorical features               | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-03-02/readme.md)       | Marketing, Business Analytics (minor)           |
| **x_superbowl**             | 2021 | Super Bowl-related tweet metadata and sentiment classification.      | Social media monitoring, ad response        | 34          | Inferred from context    | Text preprocessing, imbalance             | Tweets, real-time text                   | *Local (CSV uploaded)*                                                                                 | Marketing, Information Systems                   |
| **GPT Detectors**           | 2023 | Labeled examples of AI- vs human-written text for detection.         | Model evaluation, AI detection              | ~10         | `label`                  | Text prep, class imbalance                 | Probabilistic + categorical flags        | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-07-18/readme.md)       | Info Systems, Business Analytics (minor)        |
| **Hotels**                  | 2020 | Hotel bookings with cancellations, length of stay, guest info.       | Hospitality, pricing, segmentation          | 32          | `is_canceled`            | Categorical encoding, missing data        | Categorical + numeric mix                | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-02-11/readme.md)       | Business Admin, Ops & Supply Chain, IS           |
| **School Diversity**        | 2019 | Demographic diversity data across school districts.                  | Policy, education, geographic segmentation  | ~12         | None                     | Categorical encoding, merging              | Region-based joins                        | [GitHub](https://github.com/rfordatascience/tidytuesday/tree/main/data/2019/2019-09-24)                | QAMO, Public Policy                              |
| **Monthly State Retail Sales** | 2022 | Retail sales at state level over time.                                | Trend modeling, seasonal analysis           | ~15         | `sales`                  | Missing values, seasonal gaps             | Time series friendly                     | [GitHub](https://github.com/rfordatascience/tidytuesday/tree/main/data/2022/2022-12-13)                | Marketing, Ops & Supply Chain                    |
| **Global Holidays and Travel** | 2024 | Mobility and travel based on global holiday calendars.               | Travel demand forecasting, planning         | ~12         | None                     | Missing geolocation, temporal anomalies   | Geospatial + time features               | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-12-24/readme.md)       | Ops & Supply Chain, Marketing                    |
| **Airbnb City Sample**      | 2023 | Airbnb listings scraped from selected cities.                        | Rental pricing, location analysis           | 74          | Varies                  | Missing prices, feature variability       | Real-world, location rich                | [Inside Airbnb](https://insideairbnb.com/get-the-data/)                                               | Real Estate, Business Analytics (minor)         |
| **Reddit Post Titles**      | 2024 | Reddit thread titles and metadata for text modeling.                 | Topic modeling, online discourse analysis   | Varies      | Varies                  | Needs API retrieval                       | Text, time, topic classification         | Reddit API                                                                                             | Marketing, Info Systems                          |
| **Employee Attrition**      | 2022 | HR dataset including job satisfaction, income, and attrition.        | HR analytics, workforce planning            | 29          | `Attrition`              | Survey bias, categorical harmonization     | Balanced classes, job categories         | *Local or standard HR data (not uploaded here)*                                                       | HR Management, Business Analytics                |
| **AdviseInvest Historical** | 2023 | Historical investment client outcomes and profile data.              | Investment decisions, client profiling      | ~10         | `Leave`                  | NA entries, binary targets                 | Classification problem setup             | *Local (not uploaded)*                                                                                 | Finance, Business Analytics                      |
| **AdviseInvest New Customers** | 2023 | Unlabeled new investor profile data.                                  | Scoring, predictive modeling                | ~9          | —                        | No labels, missing fields                 | Model scoring scenario                   | *Local (not uploaded)*                                                                                 | Finance, Business Analytics                      |



# Dataset Descriptions and Data Dictionaries – Labs & Assignments

---

## SF Rents  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2022/2022-07-05/readme.md)  
**Description:** Rental listing data from San Francisco including prices, locations, room sizes, and geospatial metadata. Useful for EDA, clustering, and price prediction.

### Data Dictionary

| Variable     | Class     | Description |
|--------------|-----------|-------------|
| post_id      | character | Unique identifier for the listing |
| date         | date      | Listing posting date |
| year         | integer   | Year of the listing |
| nhood        | character | Neighborhood of the listing |
| city         | character | City name |
| county       | character | County name |
| price        | float     | Rental price in USD |
| beds         | float     | Number of bedrooms |
| baths        | float     | Number of bathrooms |
| sqft         | float     | Square footage |
| room_in_apt  | float     | Whether listing is a room in an apartment (1=yes, 0=no) |
| address      | character | Address string |
| lat          | float     | Latitude |
| lon          | float     | Longitude |
| title        | character | Listing title |
| descr        | character | Description text |
| details      | character | Additional listing metadata |

---

## Hotels  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-02-11/readme.md)  
**Description:** Hotel bookings from a resort and city hotel. Includes information on guests, reservation modifications, cancellations, and stay details. Useful for classification and segmentation.

### Data Dictionary

| Variable                     | Class     | Description |
|------------------------------|-----------|-------------|
| hotel                        | character | Hotel type (City or Resort) |
| is_canceled                  | integer   | 1 = canceled, 0 = not canceled |
| lead_time                   | integer   | Days between booking and arrival |
| arrival_date_year           | integer   | Year of arrival |
| arrival_date_month          | character | Month of arrival |
| stays_in_weekend_nights     | integer   | Nights stayed on weekend |
| stays_in_week_nights        | integer   | Nights stayed during week |
| adults                      | integer   | Number of adults |
| children                    | integer   | Number of children |
| babies                      | integer   | Number of babies |
| meal                        | character | Type of meal booked |
| country                     | character | Country code |
| market_segment              | character | Type of booking source |
| distribution_channel        | character | Booking channel used |
| is_repeated_guest           | integer   | 1 = yes, 0 = no |
| previous_cancellations      | integer   | Number of past cancellations |
| previous_bookings_not_canceled | integer | Past bookings not canceled |
| reserved_room_type          | character | Reserved room type |
| assigned_room_type          | character | Actual assigned room |
| booking_changes             | integer   | Number of changes made to booking |
| deposit_type                | character | Type of deposit paid |
| agent                       | character | Booking agent ID |
| company                     | character | Company ID for booking |
| days_in_waiting_list        | integer   | Days customer was on waiting list |
| customer_type               | character | Booking type (contract, transient) |
| adr                         | float     | Average Daily Rate (price) |
| required_car_parking_spaces | integer   | Requested parking spots |
| total_of_special_requests   | integer   | Number of special requests |
| reservation_status          | character | Current reservation status |
| reservation_status_date     | date      | Date of the status |

---

## Megatelco_Duplicates  
**Source:** Local CSV (`megatelco_leave_survey_duplicates.csv`)  
**Description:** Customer survey and service data from a telecom company. Used for classification and feature engineering.

### Data Dictionary

| Variable           | Class     | Description |
|--------------------|-----------|-------------|
| college            | character | 1 = attended college, 0 = no |
| income             | integer   | Annual income |
| data_overage_mb    | integer   | Average MB used beyond plan |
| data_leftover_mb   | integer   | MB unused from plan |
| data_mb_used       | integer   | Average monthly data usage |
| texts_sent         | integer   | Monthly text messages sent |
| over_15min_calls   | integer   | Calls >15 min per month |
| call_minutes       | integer   | Total monthly call minutes |
| os                 | character | Operating system (e.g., Android) |
| phone_price        | integer   | Retail phone price |
| satisfaction       | character | Categorical satisfaction level |
| usage              | character | Categorical usage frequency |
| change_plan        | character | Intention to switch provider |
| area               | character | Region/area label |
| handset_model      | character | Model or series of phone |
| leave              | character | Target variable (leave or stay) |

---

## Airbnb City Sample  
**Source:** [Inside Airbnb](https://insideairbnb.com/get-the-data/)  
**Description:** City-specific Airbnb data scraped from public listings. Students choose a city, download the `listings.csv` file, and use it for EDA and transformation.

### Sample Data Dictionary (varies by city)

| Variable              | Class     | Description |
|-----------------------|-----------|-------------|
| id                    | integer   | Unique listing ID |
| name                  | character | Title of listing |
| host_id               | integer   | ID of host |
| neighbourhood         | character | Local neighborhood |
| latitude              | float     | Latitude |
| longitude             | float     | Longitude |
| room_type             | character | Room type (entire home, shared, etc.) |
| price                 | character | Price (cleaning needed) |
| minimum_nights        | integer   | Minimum stay length |
| number_of_reviews     | integer   | Number of reviews |
| availability_365      | integer   | Days available per year |
| last_review           | date      | Date of most recent review |

---

## School Diversity  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/tree/main/data/2019/2019-09-24)  
**Description:** School district racial diversity stats used for demographic clustering.

### Data Dictionary

| Variable     | Class     | Description |
|--------------|-----------|-------------|
| LEAID        | character | School district ID |
| LEA_NAME     | character | District name |
| ST           | character | State |
| SCHOOL_YEAR  | character | Year range |
| AIAN         | float     | Native American %
| Asian        | float     | Asian %
| Black        | float     | Black %
| Hispanic     | float     | Hispanic %
| White        | float     | White %
| Multi        | float     | Multiracial %
| Total        | integer   | Total students |
| diverse      | character | Diversity classification |
| variance     | float     | Variance ratio of racial groups |

---

## AdviseInvest Historical & New Customers  
**Source:** Local CSVs  
**Description:** Simulated customer financial profile data for classification and scoring.

### Data Dictionary (Historical)

| Variable         | Class     | Description |
|------------------|-----------|-------------|
| ID               | integer   | Customer ID |
| Age              | float     | Age of customer |
| MaritalStatus    | character | Marital status |
| IncomeLevel      | character | Income level category |
| Education        | character | Education background |
| RiskTolerance    | character | Risk profile |
| InvestmentPref   | character | Preferred investment type |
| AdvisorVisits    | float     | Number of advisor visits |
| PortfolioSize    | float     | Portfolio value in USD |
| Leave            | character | Target: Did they leave (Yes/No) |

---

## Employee Attrition  
**Source:** Local (or standard HR dataset)  
**Description:** Synthetic HR dataset with employee-level indicators related to turnover. Used for binary classification and HR analytics.

### Sample Data Dictionary

| Variable           | Class     | Description |
|--------------------|-----------|-------------|
| Age                | integer   | Employee age |
| BusinessTravel     | character | Frequency of business travel |
| Department         | character | Department name |
| DistanceFromHome   | integer   | Commute distance |
| Education          | integer   | Education level |
| Gender             | character | Gender |
| JobRole            | character | Role title |
| MonthlyIncome      | float     | Monthly salary |
| OverTime           | character | Works overtime (Yes/No) |
| Attrition          | character | Target: Did they leave? (Yes/No) |

---

## Monthly State Retail Sales  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/tree/main/data/2022/2022-12-13)  
**Description:** Monthly retail performance by NAICS subsector and state.

### Data Dictionary

| Variable       | Class     | Description |
|----------------|-----------|-------------|
| fips           | character | State FIPS code |
| state_abbr     | character | State abbreviation |
| naics          | integer   | NAICS subsector code |
| subsector      | character | Retail type |
| year           | integer   | Year |
| month          | integer   | Month |
| change_yoy     | character | % Change YoY |
| change_yoy_se  | character | SE of change |
| coverage_code  | character | Coverage/imputation label |

---

## Global Holidays and Travel  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-12-24/readme.md)  
**Description:** Holiday and airline passenger data used for demand modeling.

### Data Dictionary (Holidays)

| Variable     | Class     | Description |
|--------------|-----------|-------------|
| ADM_name     | character | Country or region name |
| ISO3         | character | Country code |
| Date         | date      | Holiday date |
| Name         | character | Holiday name |
| Type         | character | Holiday type |

---

## Super Bowl Commercials  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-03-02/readme.md)  
**Description:** YouTube metadata for Super Bowl ads, including tags and viewer engagement metrics.

### Data Dictionary

| Variable         | Class     | Description |
|------------------|-----------|-------------|
| brand            | character | Advertiser |
| year             | integer   | Super Bowl year |
| funny            | logical   | Uses humor |
| patriotic        | logical   | Has patriotic themes |
| celebrity        | logical   | Uses celebrity |
| view_count       | integer   | Number of views |
| like_count       | integer   | Number of likes |
| title            | character | Video title |
| description      | character | Description of ad |
| category_id      | character | YouTube content category |

---

## GPT Detectors  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-07-18/readme.md)  
**Description:** AI text detection model outputs used to classify human vs. GPT-written essays.

### Data Dictionary

| Variable       | Class     | Description |
|----------------|-----------|-------------|
| kind           | character | Source (Human or AI) |
| .pred_AI       | float     | Probability it's AI |
| .pred_class    | character | Predicted label |
| detector       | character | Detector model used |
| native         | character | Native English speaker flag |

---

## Online Food Orders  
**Source:** Local CSV  
**Description:** Survey data exploring demographic and behavioral factors influencing food delivery use.

### Data Dictionary

| Variable            | Class     | Description |
|---------------------|-----------|-------------|
| Age                 | float     | Age of user |
| Gender              | character | Gender |
| Marital Status      | character | Marital status |
| Occupation          | character | Job or sector |
| Monthly Income      | character | Categorical income range |
| Educational Qualifications | character | Education level |
| Family size         | float     | Household size |
| Feedback            | character | Free-text review |
| order frequency     | character | Ordering frequency category |

---

## Restaurant Reviews  
**Source:** Local TSV  
**Description:** Short reviews labeled as liked (positive) or not liked (negative). Used in NLP text classification.

### Data Dictionary

| Variable | Class     | Description |
|----------|-----------|-------------|
| Review   | character | Text of the review |
| Liked    | integer   | 1 = Positive, 0 = Negative sentiment |

---

## Amazon Reviews  
**Source:** Local CSV  
**Description:** Product reviews and sentiment ratings scraped from Amazon. Used for classification or regression.

### Data Dictionary

| Variable     | Class     | Description |
|--------------|-----------|-------------|
| rating       | float     | Product rating (1–5) |
| title        | character | Title of the review |
| body         | character | Full review text |
| sentiment    | character | Derived sentiment (Positive/Negative) |

---

## Big Tech Stock Prices  
**Source:** [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-02-07/readme.md)  
**Description:** Time series data on stock prices for major tech firms.

### Data Dictionary

| Variable     | Class     | Description |
|--------------|-----------|-------------|
| stock_symbol | character | Ticker |
| date         | date      | Trading day |
| open         | float     | Opening price |
| high         | float     | Daily high |
| low          | float     | Daily low |
| close        | float     | Closing price |
| adj_close    | float     | Adjusted close |
| volume       | integer   | Shares traded |

---

## Reddit Post Titles  
**Source:** Reddit API  
**Description:** Students collect Reddit post titles related to business or career topics using the Reddit API.

### Data Dictionary

| Variable     | Class     | Description |
|--------------|-----------|-------------|
| title        | character | Title of post |
| created_utc  | datetime  | Timestamp |
| subreddit    | character | Subreddit name |
| author       | character | Username |
| num_comments | integer   | Comment count |
| score        | integer   | Net upvotes |

---

## YFinance Stock Monitoring  
**Source:** [YFinance Python API](https://pypi.org/project/yfinance/)  
**Description:** Students use API to extract real-time market data for a stock ticker of their choice.

### Data Dictionary (via `.history()`)

| Variable     | Class     | Description |
|--------------|-----------|-------------|
| Date         | datetime  | Trading date |
| Open         | float     | Market open |
| High         | float     | Day high |
| Low          | float     | Day low |
| Close        | float     | Market close |
| Volume       | integer   | Shares traded |
| Dividends    | float     | Dividend paid |
| Stock Splits | float     | Stock split value |

---
