# Data Dictionary for IS4487 Datasets

---

## Hotels  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-02-11/readme.md" target="_blank">GitHub Source</a>

### Booking Variables:
- <strong>is_canceled</strong>: Whether the reservation was canceled  
- Lead Time: Days between booking and arrival  
- Stay nights: Weekend and weekday durations  
- Meal, Room Type, Deposit Type: Booking attributes  
- Special Requests: Number of extra service needs  

### Customer Variables:
- Country: Customer origin  
- Market Segment: Booking source  
- Customer Type: Contract type or loyalty level  

### Other Variables:
- Assigned vs Reserved Room: Discrepancy  
- ADR: Average Daily Rate  

---

## Student Loan Payments  
<a href="https://github.com/rfordatascience/tidytuesday/tree/main/data/2019/2019-11-26" target="_blank">GitHub Source</a>

### Loan Variables:
- <strong>repayment_rate</strong>: Success rate on repayment  
- Default Rate: % of borrowers who defaulted  
- Cohort Year: Entry year group  

### Institution Variables:
- School Type: Public, private, for-profit  
- Location: Regional info  

### Demographics:
- Pell Grant %: Proxy for low-income access  
- Median Income: Entering students/families  

---

## Super Bowl Commercials  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-03-02/readme.md" target="_blank">GitHub Source</a>

### Ad Attributes:
- <strong>funny, patriotic, animal use</strong>: Binary descriptors  
- Duration: Ad length  
- Brand: Advertised product  
- Likeability: Viewer reaction  

### Metadata:
- Year: Super Bowl year  
- Type: Ad category  

---

## GPT Detectors  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-07-18/readme.md" target="_blank">GitHub Source</a>

### Prediction Fields:
- <strong>label</strong>: AI vs Human output  
- Probabilities: Model scores  

### Text Features:
- Readability, Token Length, Entropy  

---

## School Diversity  
<a href="https://github.com/rfordatascience/tidytuesday/tree/main/data/2019/2019-09-24" target="_blank">GitHub Source</a>

### Race Composition:
- % by race: White, Black, Hispanic, Asian  
- Diversity Index: Composite score  

### Location Info:
- District ID: Coded ID  
- State, Urbanicity  

---

## Big Tech Stock Prices  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2023/2023-04-25/readme.md" target="_blank">GitHub Source</a>

- <strong>close</strong>: Daily closing price  
- Volume: Shares traded  
- High/Low: Price extremes  
- Date, Ticker: ID fields  

---

## Economic Diversity and Student Outcomes  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-02-20/readme.md" target="_blank">GitHub Source</a>

- <strong>median_earnings</strong>: Post-college earnings  
- Employment rate: Follow-up outcomes  
- Income levels: Parent/family income  
- First-gen status  
- Control: Public/Private indicator  

---

## Wealth and Income Over Time  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-01-12/readme.md" target="_blank">GitHub Source</a>

- <strong>wealth_gap</strong>: Engineered inequality metric  
- Income, Wealth: Longitudinal measures  
- Year, Panel ID: Tracking data  

---

## SF Rents  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2022/2022-04-26/readme.md" target="_blank">GitHub Source</a>

- Rent: Median monthly rent  
- Unit size, Year built  
- ZIP code, lat/lon  
- Date: Monthly time stamp  

---

## Monthly State Retail Sales  
<a href="https://github.com/rfordatascience/tidytuesday/blob/main/data/2022/2022-03-29/readme.md" target="_blank">GitHub Source</a>

- <strong>sales</strong>: State-by-month sales figures  
- Category: Retail segment  
- State, Month: Identifiers  

---

## Megatelco

### Demographic:
- College: (one, zero)  
- Income, House Price  

### Usage:
- Data Overage / Leftover / Used  
- Texts, Long Calls, Avg Duration  

### Phone:
- OS: Android/iOS  
- Handset Price  

### Attitudes:
- Satisfaction, Usage, Change-of-plan flags  

### Labels:
- <strong>leave</strong>: STAY/LEAVE  
- ID: Customer code  

---

## Superstore Orders

- Order ID, Date, Year-Month  
- Customer Name, Email  
- Product Name, Line, Price  
- Quantity  
- Product Status  
- Order Type: Online/Retail  
- Location: City, State  

---

## AdviseInvest New

- Income, Age, Gender, Job  
- Dependents, Rent, Own Res, New Car  
- Chk/Sav Acct (coded)  
- Num Accts, Mobile  
- Customer ID  

---

## AdviseInvest History

- All from "New" plus:  
- Answered (0/1), Product (target)  

---

## Amazon Reviews

- One column: Full review text  
- Suitable for NLP classification or sentiment analysis  

---

## X Super Bowl Tweets

- Text, Timestamp  
- Tweet ID, Conversation ID  
- Author ID  
- Language, Location  
- Mentions, URLs  
- Good for hashtag classification, keyword mining, time series NLP  

---
