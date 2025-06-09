# Intro to Business Analytics Course Datasets
This table includes curated datasets for an introductory business analytics course. Each entry includes the dataset’s year, a short description, suitability criteria (showing the number of variables, target variable if applicable, and types of data quality issues), and the GitHub link or dataset source.

| Dataset Name | Year | Description | Business Application | # Variables | Target Variable | Data Quality Issues | Special Features | GitHub Link | Relevant Majors/Minors |
|:-------------|:-----|:------------|:----------------------|:------------|:----------------|:--------------------|:------------------|:------------|:------------------------|
| **Hotels** | 2020 | Hotel bookings including cancellations, stay duration, guest demographics. | Hospitality analytics, revenue mgmt. | 32 | `is_canceled` | Missing values, outliers, categorical encoding | Rich categorical + numeric mix | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-02-11/readme.md) | Business Administration, Operations & Supply Chain, Information Systems |
| **Student Loan Payments** | 2019 | Loan performance by institution and borrower demographics. | Higher ed finance, student aid policy | 20+ | `repayment_rate` | Missing data, skewed distributions, standardization needed | Good regression/classification use | [GitHub](https://github.com/rfordatascience/tidytuesday/tree/main/data/2019/2019-11-26) | Finance, QAMO |
| **Super Bowl Commercials** | 2021 | Ad data by brand and viewer impact across 20+ years. | Marketing, media performance | ~15 | `funny` or `likeability` (proxy) | Categorical encoding, missing features | API access + text features | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-03-02/readme.md) | Marketing, Business Analytics (minor) |
| **GPT Detectors** | 2023 | AI-generated text classifications with detector outputs. | AI fairness, model evaluation | ~10 | `label` (AI vs Human) | Class imbalance, text preprocessing | Probabilistic & categorical features | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-07-18/readme.md) | Information Systems, Business Analytics (minor) |
| **School Diversity** | 2019 | Racial diversity metrics across schools and districts. | Public policy, education equity | ~12 | None explicitly | Merging districts, categorical encoding | Geographic + merging tasks | [GitHub](https://github.com/rfordatascience/tidytuesday/tree/main/data/2019/2019-09-24) | Management, QAMO |
| **Big Tech Stock Prices** | 2023 | Daily stock data for major tech companies. | Financial markets, tech sector analysis | ~7 (per company) | `close` | Missing trading days, volatility outliers | Time series friendly | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-02-07/readme.md) | Finance, FinTech (minor), QAMO |
| **Economic Diversity and Student Outcomes** | 2024 | Outcomes vs. income demographics in higher education. | Socioeconomic mobility studies | ~15 | `median_earnings` | Requires merging/joining, NA values | Institutional join, multiple sources | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-03-10/readme.md) | Finance, Business Administration, QAMO |
| **Wealth and Income Over Time** | 2021 | Longitudinal trends in earnings, wealth by race/income. | Economic inequality analysis | ~20 | `wealth_gap` (engineered) | Gaps over time, missing race data | Strong for time series cleaning | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-02-09/readme.md) | QAMO, Finance |
| **SF Rents** | 2022 | Rental prices in San Francisco over time. | Urban economics, housing markets | ~10–12 | `rent` | Price outliers, missing records, standardization | Outliers, geospatial prep needed | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2022/2022-07-05/readme.md) | Real Estate, Business Analytics (minor) |
| **Monthly State Retail Sales** | 2022 | Monthly retail sales across U.S. states. | Retail trends, geographic comparisons | ~15 | `sales` | Seasonal gaps, NA values, numeric scaling | Ideal for seasonal modeling | [GitHub](https://github.com/rfordatascience/tidytuesday/tree/main/data/2022/2022-12-13) | Marketing, Operations & Supply Chain, Business Analytics (minor) |
| **Global Holidays and Travel** | 2024 | Human mobility patterns based on holiday calendars. | Tourism analysis, mobility planning | ~12 | None (engineer mobility flag) | Missing geolocations, holiday anomalies | Geospatial + temporal complexity | [GitHub](https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-12-24/readme.md) | Operations & Supply Chain, Marketing |
| **Megatelco Customer Survey** | 2023 | Demographic, usage, and churn survey data from a telecom firm. | Churn analysis, customer segmentation | ~15 | `Leave` | Categorical harmonization, inconsistent NA entries | Survey + behavioral + financial fields | *Local* | Information Systems, Business Analytics |
| **Amazon Reviews** | 2022 | User review sentiment data scraped from Amazon product pages. | NLP, product analytics | 4 | `sentiment` | Sparse text length, class imbalance | Free-text with target label | *Local* | Marketing, Business Analytics |
| **AdviseInvest Historical** | 2023 | Past customers’ profiles and outcomes for an investment firm. | Investment decision behavior, churn | ~10 | `Leave` | Some missing entries | Binary classification | *Local* | Finance, QAMO |
| **AdviseInvest New Customers** | 2023 | Unlabeled new investor data for prediction. | Profile scoring, churn modeling | ~9 | Unknown | Missing satisfaction, no outcomes | Supervised learning setup | *Local* | Finance, Business Analytics |
| **Superstore Retail Orders** | 2017 | Order and sales data across regions and products. | Retail operations, profit analysis | ~18 | `Profit` or `Sales` | Date parsing, inconsistent regions | Joinable categories & dates | *Local* | Business Analytics, Marketing |

---

## Hotels  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-02-11/readme.md" target="_blank">GitHub Source</a>

**Description:** Hotel booking data including customer demographics, booking changes, cancellations, and revenue-related information. Useful for teaching customer segmentation and predictive modeling in hospitality.

### Data Dictionary

#### `hotel_bookings.csv`

| Variable                     | Class     | Description |
|:-----------------------------|:----------|:------------|
| hotel                        | character | Hotel type (Resort or City) |
| is_canceled                  | double    | Was the booking canceled (1=yes, 0=no) |
| lead_time                   | double    | Days between booking and arrival |
| arrival_date_year           | double    | Year of arrival |
| arrival_date_month          | character | Month of arrival |
| stays_in_weekend_nights     | double    | Weekend nights stayed |
| stays_in_week_nights        | double    | Week nights stayed |
| adults                      | double    | Number of adults |
| children                    | double    | Number of children |
| babies                      | double    | Number of babies |
| meal                        | character | Meal package type |
| country                     | character | Country of origin (ISO) |
| market_segment              | character | Booking segment (e.g. TA, TO) |
| distribution_channel        | character | Booking channel |
| is_repeated_guest           | double    | Is this a repeated guest? |
| previous_cancellations      | double    | Previous canceled bookings |
| previous_bookings_not_canceled | double | Previous non-canceled bookings |
| reserved_room_type          | character | Reserved room type code |
| assigned_room_type          | character | Assigned room type code |
| booking_changes             | double    | Number of changes to booking |
| deposit_type                | character | Type of deposit made |
| agent                       | character | Booking agent ID |
| company                     | character | Booking company ID |
| days_in_waiting_list        | double    | Days on waiting list |
| customer_type               | character | Type of customer |
| adr                         | double    | Average Daily Rate |
| required_car_parking_spaces | double    | Parking spaces requested |
| total_of_special_requests   | double    | Count of special requests |
| reservation_status          | character | Final reservation status |
| reservation_status_date     | double    | Date of final status |

---

## Student Loan Payments  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2019/2019-03-12/readme.md" target="_blank">GitHub Source</a>

**Description:** Financial data covering loan performance and repayment trends by U.S. government agencies. Excellent for policy analysis and finance modeling exercises.

### Data Dictionary

#### `loans.csv`

| Variable           | Class     | Description |
|:------------------|:----------|:------------|
| agency_name        | character | Name of loan agency |
| year               | integer   | Two-digit year |
| quarter            | integer   | Quarter (1–4) |
| starting           | double    | Total value at start of quarter |
| added              | double    | Amount added during quarter |
| total              | double    | Total dollars repaid |
| consolidation      | double    | Value of consolidated loans |
| rehabilitation     | double    | Value of rehabilitated loans |
| voluntary_payments | double    | Total voluntary borrower payments |
| wage_garnishments  | double    | Total wage garnishment payments |

---

## Super Bowl Commercials  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-02-02/readme.md" target="_blank">GitHub Source</a>

**Description:** Metadata about Super Bowl ads including ad themes, brand, YouTube performance metrics, and viewer reactions. Ideal for sentiment analysis, marketing strategy evaluation, and text mining.

### Data Dictionary

#### `youtube.csv`

| Variable                  | Class     | Description |
|:-------------------------|:----------|:------------|
| year                     | double    | Super Bowl year |
| brand                    | character | Advertiser brand |
| superbowl_ads_dot_com_url | character | Ad URL |
| youtube_url              | character | YouTube video URL |
| funny                    | logical   | Contains humor |
| show_product_quickly     | logical   | Product shown early |
| patriotic                | logical   | Patriotic content |
| celebrity                | logical   | Includes celebrity |
| danger                   | logical   | Shows danger |
| animals                  | logical   | Features animals |
| use_sex                  | logical   | Sexual content |
| id                       | character | YouTube ID |
| kind                     | character | API kind |
| etag                     | character | API etag |
| view_count               | integer   | View count |
| like_count               | integer   | Likes |
| dislike_count            | integer   | Dislikes |
| favorite_count           | integer   | Favorites |
| comment_count            | integer   | Comments |
| published_at             | character | Publish date |
| title                    | character | Video title |
| description              | character | Description text |
| thumbnail                | character | Thumbnail URL |
| channel_title            | character | YouTube channel |
| category_id              | character | Content category ID |

---

## GPT Detectors  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-04-18/readme.md" target="_blank">GitHub Source</a>

**Description:** Data from AI text detectors assessing whether essays are human- or AI-generated. Enables discussions on AI ethics, model calibration, and NLP model performance.

### Data Dictionary

#### `detectors.csv`

| Variable    | Class     | Description |
|:------------|:----------|:------------|
| kind        | character | Human vs AI authored text |
| .pred_AI    | double    | Probability text is AI-generated |
| .pred_class | character | AI/Human classification result |
| detector    | character | Name of the model/detector |
| native      | character | Whether human writer is native English speaker |
| name        | character | Experiment label |
| model       | character | AI model name |
| document_id | double    | Essay identifier |
| prompt      | character | Prompt used to generate AI essay |

---

## School Diversity  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2019/2019-01-15/readme.md" target="_blank">GitHub Source</a>

**Description:** U.S. school district-level racial diversity data over two academic years. Supports geographic, demographic, and equity-based clustering and segmentation.


### Data Dictionary

#### `school_diversity.csv`

| Variable     | Class     | Description |
|:-------------|:----------|:------------|
| LEAID        | character | Unique school ID |
| LEA_NAME     | character | School District Name |
| ST           | character | State abbreviation |
| d_Locale_Txt | character | School type and locale |
| SCHOOL_YEAR  | character | Academic year (1994-95 or 2016-17) |
| AIAN         | double    | American Indian/Alaska Native % |
| Asian        | double    | Asian % of student population |
| Black        | double    | Black % |
| Hispanic     | double    | Hispanic % |
| White        | double    | White % |
| Multi        | double    | Multiracial % |
| Total        | double    | Total student count |
| diverse      | character | Diversity category |
| variance     | double    | Variance ratio |
| int_group    | character | Integration level |

---

## Big Tech Stock Prices  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-02-07/readme.md" target="_blank">GitHub Source</a>

**Description:** Daily market data for major tech companies. Great for exploring time series forecasting, volatility, and sector performance.

### Data Dictionary

#### `big_tech_stock_prices.csv`

| Variable     | Class     | Description |
|:-------------|:----------|:------------|
| stock_symbol | character | Ticker symbol |
| date         | double    | Date of record |
| open         | double    | Market open price |
| high         | double    | Daily high |
| low          | double    | Daily low |
| close        | double    | Market close price (adjusted) |
| adj_close    | double    | Adjusted close (CRSP standards) |
| volume       | double    | Shares traded |

#### `big_tech_companies.csv`

| Variable     | Class     | Description |
|:-------------|:----------|:------------|
| stock_symbol | character | Ticker symbol |
| company      | character | Full company name |

---

## Economic Diversity and Student Outcomes  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-03-10/readme.md" target="_blank">GitHub Source</a>

**Description:** Institutional-level educational cost, earnings, and income diversity data. Useful for socioeconomic mobility analysis and institutional comparison.

### Data Dictionary

#### `tuition_cost.csv`

| Variable             | Class     | Description |
|:---------------------|:----------|:------------|
| name                 | character | Institution name |
| state                | character | State |
| state_code           | character | State abbreviation |
| type                 | character | Institution type |
| degree_length        | character | 2- or 4-year |
| room_and_board       | double    | Cost of housing |
| in_state_tuition     | double    | In-state tuition |
| in_state_total       | double    | In-state total cost |
| out_of_state_tuition | double    | Out-of-state tuition |
| out_of_state_total   | double    | Out-of-state total cost |

#### `tuition_income.csv`

| Variable    | Class     | Description |
|:------------|:----------|:------------|
| name        | character | School name |
| state       | character | State |
| total_price | double    | Tuition price |
| year        | double    | Year |
| campus      | character | Campus type |
| net_cost    | double    | Net tuition paid |
| income_lvl  | character | Income level bracket |

#### `salary_potential.csv`

| Variable                  | Class     | Description |
|:--------------------------|:----------|:------------|
| rank                      | double    | Salary rank |
| name                      | character | School name |
| state_name                | character | State |
| early_career_pay          | double    | Early career salary |
| mid_career_pay            | double    | Mid career salary |
| make_world_better_percent| double    | Alumni impact sentiment |
| stem_percent              | double    | STEM enrollment %

#### `historical_tuition.csv`

| Variable     | Class     | Description |
|:-------------|:----------|:------------|
| type         | character | School type |
| year         | character | Academic year |
| tuition_type | character | Tuition category |
| tuition_cost | double    | Tuition amount |

#### `diversity_school.csv`

| Variable         | Class     | Description |
|:------------------|:----------|:------------|
| name             | character | Institution name |
| total_enrollment | double    | Total enrollment |
| state            | character | State |
| category         | character | Demographic category |
| enrollment       | double    | Enrollment by group |

---

## Wealth and Income Over Time  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-02-09/readme.md" target="_blank">GitHub Source</a>

**Description:** Multi-decade indicators of economic inequality broken down by race and income bracket. Supports longitudinal and cohort analyses of wealth distribution.

### Data Dictionary

#### `lifetime_earn.csv`

| Variable      | Class     | Description |
|:--------------|:----------|:------------|
| gender        | character | Gender group |
| race          | character | Racial group |
| lifetime_earn | double    | Average lifetime earnings |

#### `student_debt.csv`

| Variable      | Class     | Description |
|:--------------|:----------|:------------|
| year          | double    | Year |
| race          | character | Racial group |
| loan_debt     | double    | Average loan debt |
| loan_debt_pct | double    | Percent with debt |

#### `retirement.csv`

| Variable   | Class     | Description |
|:-----------|:----------|:------------|
| year       | double    | Year |
| race       | character | Racial group |
| retirement | double    | Avg. retirement savings |

#### `home_owner.csv`

| Variable       | Class     | Description |
|:---------------|:----------|:------------|
| year           | double    | Year |
| race           | character | Racial group |
| home_owner_pct | double    | % homeowners |

#### `race_wealth.csv`

| Variable      | Class     | Description |
|:--------------|:----------|:------------|
| type          | character | "Mean" or "Median" |
| year          | double    | Year |
| race          | character | Racial group |
| wealth_family | double    | Avg. wealth |

#### `income_time.csv`

| Variable      | Class     | Description |
|:--------------|:----------|:------------|
| year          | integer   | Year |
| percentile    | character | Income percentile |
| income_family | double    | Income value |

#### `income_limits.csv`

| Variable        | Class     | Description |
|:----------------|:----------|:------------|
| year            | double    | Year |
| race            | character | Racial group |
| dollar_type     | character | Year-adjusted dollars |
| number          | double    | Household count |
| income_quintile | character | Income quintile |
| income_dollars  | double    | Income value |

#### `income_aggregate.csv`

| Variable        | Class     | Description |
|:----------------|:----------|:------------|
| year            | double    | Year |
| race            | character | Racial group |
| number          | double    | Households |
| income_quintile | character | Quintile |
| income_share    | double    | % of total income |

#### `income_distribution.csv`

| Variable            | Class     | Description |
|:--------------------|:----------|:------------|
| year                | integer   | Year |
| race                | character | Racial group |
| number              | double    | Households |
| income_median       | integer   | Median income |
| income_med_moe      | integer   | Margin of error for median |
| income_mean         | integer   | Mean income |
| income_mean_moe     | integer   | Margin of error for mean |
| income_bracket      | character | Income range |
| income_distribution | double    | % in bracket |

#### `income_mean.csv`

| Variable        | Class     | Description |
|:----------------|:----------|:------------|
| year            | double    | Year |
| race            | character | Racial group |
| dollar_type     | character | Dollar standard |
| income_quintile | character | Quintile group |
| income_dollars  | double    | Average income |



## SF Rents  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2022/2022-07-05/readme.md#sf-rents" target="_blank">GitHub Source</a>

**Description:** Rental listings, building permits, and construction output data from San Francisco. Rich for real estate analysis, geospatial visualization, and urban policy topics.

### Data Dictionary

#### `rent.csv`

| Variable     | Class     | Description |
|:-------------|:----------|:------------|
| post_id      | character | Unique listing ID |
| date         | double    | Listing date |
| year         | double    | Year of listing |
| nhood        | character | Neighborhood |
| city         | character | City |
| county       | character | County |
| price        | double    | Listing price (USD) |
| beds         | double    | Number of bedrooms |
| baths        | double    | Number of bathrooms |
| sqft         | double    | Square footage |
| room_in_apt  | double    | Is this a room within an apartment? |
| address      | character | Street address |
| lat          | double    | Latitude |
| lon          | double    | Longitude |
| title        | character | Listing title |
| descr        | character | Listing description |
| details      | character | Additional listing details |

#### `sf_permits.csv`

| Variable                               | Class     | Description |
|:--------------------------------------|:----------|:------------|
| permit_number                          | character | Permit ID |
| permit_type                            | double    | Numeric type code |
| permit_type_definition                 | character | Definition of permit type |
| permit_creation_date                   | double    | Date permit was created |
| block                                  | character | Block ID |
| lot                                    | character | Lot ID |
| street_number                          | double    | Street number |
| street_number_suffix                   | character | Suffix for street number |
| street_name                            | character | Street name |
| street_suffix                          | character | Street suffix (e.g., Ave, St) |
| unit                                   | double    | Unit number |
| unit_suffix                            | character | Unit suffix |
| description                            | character | Permit description |
| status                                 | character | Current status of the permit |
| status_date                            | double    | Date of current status |
| filed_date                             | double    | Date filed |
| issued_date                            | double    | Date issued |
| completed_date                         | double    | Date construction completed |
| first_construction_document_date       | double    | First construction doc date |
| structural_notification                | character | Structural notification status |
| number_of_existing_stories             | double    | Existing number of stories |
| number_of_proposed_stories             | double    | Proposed number of stories |
| voluntary_soft_story_retrofit          | character | Soft-story retrofit status |
| fire_only_permit                       | character | Fire permit status |
| permit_expiration_date                 | double    | Expiration date |
| estimated_cost                         | double    | Estimated project cost |
| revised_cost                           | double    | Revised project cost |
| existing_use                           | character | Current land use |
| existing_units                         | double    | Number of existing units |
| proposed_use                           | character | Proposed land use |
| proposed_units                         | double    | Number of proposed units |
| plansets                               | double    | Number of plan sets |
| tidf_compliance                        | logical   | TIDF compliance |
| existing_construction_type             | double    | Code for current construction type |
| existing_construction_type_description | character | Description of current construction |
| proposed_construction_type             | double    | Code for proposed construction type |
| proposed_construction_type_description | character | Description of proposed construction |
| site_permit                            | character | Site permit code |
| supervisor_district                    | double    | Supervisor district |
| neighborhoods_analysis_boundaries      | character | Neighborhood category |
| zipcode                                | double    | ZIP code |
| location                               | character | Geolocation string |
| record_id                              | double    | Unique record ID |
| date                                   | double    | Associated date |

#### `new_construction.csv`

| Variable             | Class     | Description |
|:---------------------|:----------|:------------|
| cartodb_id           | integer   | Unique ID |
| the_geom             | logical   | Geometry type |
| the_geom_webmercator | logical   | Geometry in Web Mercator projection |
| county               | character | County name |
| year                 | integer   | Year of record |
| totalproduction      | integer   | Total housing units produced |
| sfproduction         | integer   | Single-family units produced |
| mfproduction         | integer   | Multi-family units produced |
| mhproduction         | integer   | Mobile homes produced |
| source               | character | Source of data |

---

## Monthly State Retail Sales  
<a href="https://github.com/rfordatascience/tidytuesday/tree/main/data/2022/2022-12-13" target="_blank">GitHub Source</a>

**Description:** Monthly retail sales data across U.S. states, categorized by retail subsector. Excellent for time-series analysis, seasonality modeling, and regional economic comparisons.

### Data Dictionary

#### `state_retail.csv`

| Variable      | Class     | Description |
|:--------------|:----------|:------------|
| fips          | character | 2-digit State Federal Information Processing Standards (FIPS) code. [Reference](https://www.census.gov/library/reference/code-lists/ansi/ansi-codes-for-states.html) |
| state_abbr    | character | 2-letter USPS state abbreviation (or "USA"). [Reference](https://www.census.gov/library/reference/code-lists/ansi/ansi-codes-for-states.html) |
| naics         | integer   | 3-digit NAICS subsector code |
| subsector     | character | Retail subsector description |
| year          | integer   | Year of record |
| month         | integer   | Month of record |
| change_yoy    | character | Year-over-year % change in retail sales value |
| change_yoy_se | character | Standard error of year-over-year % change |
| coverage_code | character | Code reflecting level of coverage and imputation |

#### `coverage_codes.csv`

| Variable      | Class     | Description |
|:--------------|:----------|:------------|
| coverage_code | character | Imputation and coverage code |
| coverage      | character | Full definition of the coverage code |

---

## Global Holidays and Travel  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-12-24/readme.md" target="_blank">GitHub Source</a>

**Description:** Combines global public and cultural holiday data with monthly international and domestic air passenger counts. Suitable for tourism, mobility planning, and geotemporal analysis.

### Data Dictionary

#### `global_holidays.csv`

| Variable | Class     | Description |
|:----------|:----------|:-------------|
| ADM_name | character | Name of the administering location (country or political subdivision) |
| ISO3     | character | 3-letter ISO code for the location (see [ISO Codes - 2024-11-12](https://tidytues.day/2024/2024-11-12)) |
| Date     | date      | Date of the observance |
| Name     | character | Name of the holiday or observance |
| Type     | character | Type of observance: "Half-day holiday", "Local holiday", "Local observance", "Observance", "Public holiday", "Special holiday", or "Working day (replacement)" |

#### `monthly_passengers.csv`

| Variable      | Class     | Description |
|:---------------|:----------|:-------------|
| ISO3          | character | 3-letter ISO code (see [ISO Codes - 2024-11-12](https://tidytues.day/2024/2024-11-12)) |
| Year          | integer   | Year of air travel |
| Month         | integer   | Month of air travel |
| Total         | double    | Total number of air passengers (thousands) from official statistics |
| Domestic      | double    | Domestic air passengers (thousands) from official statistics |
| International | double    | International air passengers (thousands) from official statistics |
| Total_OS      | double    | Total air passengers (thousands) from open source data |

---

---

## Megatelco New Customer Data  
**Description:** Demographic and usage profile data on new customers acquired by Megatelco. Useful for churn prediction and customer segmentation modeling.

### Data Dictionary

#### `megatelco_new_customer_data.csv`

| Variable         | Class     | Description |
|:----------------|:----------|:------------|
| ID              | integer   | Unique customer ID |
| College         | integer   | 1 if attended some college, 0 otherwise |
| Income          | double    | Annual income of the customer |
| House           | double    | Estimated house price (if available) |
| DataOverage     | double    | Average MBs used over the plan limit |
| DataLeftover    | double    | Average MBs unused under the plan limit |
| DataUsed        | double    | Average MBs used per month |
| Texts           | double    | Average number of monthly text messages |
| Over15MinCalls  | double    | Average number of long-duration calls/month |
| CallDuration    | double    | Average call duration in minutes |
| OS              | character | Operating system of customer's phone |
| HandsetPrice    | double    | Retail price of the handset |
| Satisfaction    | character | Satisfaction level (high, med, low) |
| UsageLevel      | character | Reported usage level (high, med, low) |
| ChangePlan      | character | Intent to change provider (high, med, low) |

---

## Megatelco Leave Survey  
**Description:** Survey responses from customers who recently churned or renewed service. Contains satisfaction, usage, and demographic indicators for churn analysis.

### Data Dictionary

#### `megatelco_leave_survey.csv`

| Variable         | Class     | Description |
|:----------------|:----------|:------------|
| ID              | integer   | Customer identifier |
| College         | integer   | Has the customer attended some college (1=yes) |
| Income          | double    | Annual income of customer |
| House           | double    | Estimated home price |
| DataOverage     | double    | Average MBs over limit |
| DataLeftover    | double    | Average MBs unused |
| DataUsed        | double    | Monthly average MBs used |
| Texts           | double    | Text messages per month |
| Over15MinCalls  | double    | Calls over 15 mins/month |
| CallDuration    | double    | Average call length |
| OS              | character | Operating system |
| HandsetPrice    | double    | Price of phone |
| Satisfaction    | character | Reported satisfaction |
| UsageLevel      | character | Reported usage level |
| ChangePlan      | character | Considering provider switch |
| Leave           | character | Whether customer left or stayed |

---

## Amazon Reviews  
**Description:** User reviews of Amazon products, likely including rating scores, sentiment, and review text useful for NLP or classification models.

### Data Dictionary

#### `amazon-reviews2.csv`

| Variable     | Class     | Description |
|:-------------|:----------|:------------|
| rating       | double    | Star rating (1 to 5) |
| title        | character | Title of the review |
| body         | character | Full review text |
| sentiment    | character | Derived sentiment label |

---

## AdviseInvest Historical Customer Data  
**Description:** Performance data and features on past customers of AdviseInvest, including demographic and behavior variables used for investment profile modeling.

### Data Dictionary

#### `adviseinvest_historical_data.csv`

| Variable         | Class     | Description |
|:----------------|:----------|:------------|
| ID              | integer   | Unique customer ID |
| Age             | double    | Age of customer |
| MaritalStatus   | character | Marital status |
| IncomeLevel     | character | Categorical income level |
| Education       | character | Highest education completed |
| RiskTolerance   | character | Risk tolerance profile |
| InvestmentPref  | character | Preferred investment style |
| AdvisorVisits   | double    | Number of advisor interactions |
| PortfolioSize   | double    | Size of current portfolio (USD) |
| Leave           | character | Whether customer stayed or left |

---

## AdviseInvest New Customer Data  
**Description:** Latest incoming client profiles for prediction of future churn or segmentation into risk/investment categories.

### Data Dictionary

#### `adviseinvest_new_customer_data.csv`

| Variable         | Class     | Description |
|:----------------|:----------|:------------|
| ID              | integer   | Customer ID |
| Age             | double    | Age |
| MaritalStatus   | character | Marital status |
| IncomeLevel     | character | Income group |
| Education       | character | Education level |
| RiskTolerance   | character | Risk profile |
| InvestmentPref  | character | Preferred strategy |
| AdvisorVisits   | double    | Visits to financial advisor |
| PortfolioSize   | double    | Portfolio value |

---

## Superstore Retail Orders  
**Description:** A dataset of product orders from a fictional retail superstore. Includes customer segments, order dates, shipping details, sales, and profits.

### Data Dictionary

#### `superstore_retail_orders.csv`

| Variable           | Class     | Description |
|:-------------------|:----------|:------------|
| Order ID           | character | Unique order identifier |
| Customer ID        | character | Unique customer identifier |
| Segment            | character | Customer segment |
| Country            | character | Country of order |
| City               | character | City of delivery |
| State              | character | State of delivery |
| Postal Code        | character | ZIP code |
| Region             | character | Sales region |
| Product ID         | character | ID of the product |
| Category           | character | Product category |
| Sub-Category       | character | Product sub-category |
| Product Name       | character | Product description |
| Sales              | double    | Total sales value |
| Quantity           | double    | Quantity sold |
| Discount           | double    | Discount applied |
| Profit             | double    | Profit from sale |
| Order Date         | date      | Date of order |
| Ship Date          | date      | Shipment date |
| Ship Mode          | character | Delivery speed |

---

## Super Bowl Commercials  
**Description:** Metadata and features of Super Bowl advertisements, covering branding tactics, presence of celebrities, humor, and YouTube engagement metrics.

### Data Dictionary

#### `x_superbowl.csv`

| Variable        | Class     | Description |
|:----------------|:----------|:------------|
| year            | double    | Year of Super Bowl |
| brand           | character | Advertiser |
| funny           | logical   | Contains humor |
| show_product_quickly | logical | Shows product early |
| patriotic       | logical   | Patriotic content |
| celebrity       | logical   | Features celebrity |
| danger          | logical   | Dangerous situations |
| animals         | logical   | Uses animals |
| use_sex         | logical   | Uses sexuality |
| view_count      | integer   | Number of views |
| like_count      | integer   | Number of likes |
| dislike_count   | integer   | Number of dislikes |
| favorite_count  | integer   | Number of favorites |
| comment_count   | integer   | Number of comments |
| published_at    | character | Publish date on YouTube |

---


