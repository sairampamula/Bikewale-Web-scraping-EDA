[README for web scrapng.md](https://github.com/user-attachments/files/33109875/README.for.web.scrapng.md)
# Bikewale-Web-scraping-EDA# BikeWale Web Scraping & Exploratory Data Analysis

## 📌 Project Overview

This project collects motorcycle and scooter information from
**BikeWale** using web scraping and performs **Exploratory Data Analysis
(EDA)** to understand patterns in the two-wheeler market.

The project focuses on:

-   Web scraping
-   Data collection
-   Data cleaning and preprocessing
-   Exploratory Data Analysis
-   Data visualization
-   Business-oriented insights

This project is intended for **data analysis and visualization**, not
machine learning model building.

------------------------------------------------------------------------

## 🎯 Objectives

The main objectives of this project are:

1.  Scrape bike information from BikeWale.
2.  Convert the scraped information into a structured dataset.
3.  Clean and prepare the data for analysis.
4.  Analyze brands, prices, ratings, mileage, specifications and fuel
    type.
5.  Compare petrol and electric bikes.
6.  Identify patterns and trends using charts.
7.  Generate meaningful insights from the dataset.

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   **Python**
-   **Pandas**
-   **NumPy**
-   **Matplotlib**
-   **Seaborn**
-   **Requests**
-   **Regular Expressions (`re`)**
-   **JSON**
-   **Jupyter Notebook / Google Colab**

------------------------------------------------------------------------

## 🌐 Web Scraping Approach

The project uses Python requests to access BikeWale pages.

The scraping workflow is:

``` text
BikeWale Website
       ↓
HTTP Request
       ↓
HTML Response
       ↓
Extract embedded JSON data
       ↓
Parse JSON
       ↓
Extract bike information
       ↓
Pandas DataFrame
       ↓
CSV Dataset
       ↓
EDA & Visualization
```

The project extracts embedded `__INITIAL_STATE__` JSON data from the
webpage and converts the relevant bike information into tabular form.

------------------------------------------------------------------------

## 📊 Dataset

The initial dataset contains:

-   **522 bike records**
-   **18 columns**
-   **61 brands**

Important attributes include:

  -----------------------------------------------------------------------
  Column                              Description
  ----------------------------------- -----------------------------------
  `brand`                             Bike manufacturer

  `model`                             Bike/scooter model

  `price`                             Listed price

  `price_label`                       Price availability/label

  `is_electric`                       Whether the vehicle is electric

  `rating`                            User rating

  `review_count`                      Number of reviews

  `mileage_kmpl`                      Mileage in km/l

  `displacement_cc`                   Engine displacement

  `max_power_bhp`                     Maximum power in bhp

  `kerb_weight_kg`                    Kerb weight

  `charging_time_hours`               Charging time for applicable
                                      electric vehicles

  `max_power_kw`                      Maximum power in kW

  `launched_on`                       Launch date
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🧹 Data Preprocessing

Since this project is focused on EDA rather than machine learning, only
analysis-related preprocessing was performed.

### Steps performed

1.  Checked dataset shape and structure.
2.  Checked data types.
3.  Checked missing values.
4.  Checked duplicate records.
5.  Removed duplicate rows.
6.  Reset the DataFrame index.
7.  Converted `launched_on` into datetime format.
8.  Created `launch_year` and `launch_month`.
9.  Cleaned text columns using `str.strip()`.
10. Created a readable `fuel_type` column.
11. Checked numerical columns for invalid negative values.
12. Removed records with `price = 0` for price-focused EDA because zero
    does not represent an actual bike price.

### Missing Values

Missing values were **not automatically replaced with zero or mean
values**.

For example, `charging_time_hours` may naturally be unavailable for
petrol bikes. Therefore, such values were retained as missing instead of
being treated as invalid.

------------------------------------------------------------------------

## 📈 Exploratory Data Analysis

The following areas were analyzed:

### 1. Brand Analysis

-   Number of models by brand
-   Top brands by model count
-   Average price by brand
-   Average rating by brand

### 2. Price Analysis

-   Price distribution
-   Most expensive bikes
-   Most affordable bikes
-   Average price by brand
-   Price comparison between petrol and electric bikes

### 3. Fuel Type Analysis

-   Petrol vs electric bike distribution
-   Electric models by brand
-   Average price by fuel type
-   Average rating by fuel type

### 4. Rating & Review Analysis

-   Rating distribution
-   Most reviewed bikes
-   Average rating by brand
-   Relationship between rating and review count

### 5. Performance Analysis

-   Mileage distribution
-   Top bikes by mileage
-   Engine displacement vs price
-   Power vs price
-   Kerb weight vs maximum power

### 6. Time Analysis

-   Bikes launched by year
-   Bikes launched by month

### 7. Correlation Analysis

Correlation between numerical variables such as:

-   Price
-   Rating
-   Review count
-   Mileage
-   Engine displacement
-   Maximum power
-   Kerb weight
-   Charging time

------------------------------------------------------------------------

## 🔍 Key Insights

Some important findings from the analysis include:

-   The dataset contains **522 bikes across 61 brands**.
-   **Petrol bikes dominate** the dataset, while electric models also
    have a meaningful presence.
-   **Honda** has the highest representation in the dataset with 39
    models, followed by Kawasaki with 37.
-   The valid-price data contains bikes ranging from entry-level models
    to premium motorcycles priced up to **₹1 crore**.
-   **Ducati** has the highest average price among the brands shown in
    the analysis.
-   The most expensive bike identified is **Ducati Panigale V4
    Lamborghini**, priced at approximately ₹1 crore.
-   The average available bike rating is approximately **4.29/5**.
-   **Bajaj Freedom** records the highest mileage in the analyzed
    dataset at **91 km/l**.
-   The analysis shows clear differences between manufacturers in terms
    of pricing, model availability and market positioning.

> Note: Correlation indicates association between variables; it does not
> prove causation.

------------------------------------------------------------------------

## 📊 Visualizations

The project includes visualizations such as:

-   Bar charts
-   Pie charts
-   Histograms
-   Box plots
-   Scatter plots
-   Line charts
-   Correlation heatmaps

These visualizations are used to communicate patterns in the dataset
clearly.

------------------------------------------------------------------------

## 📁 Project Structure

A suggested GitHub repository structure is:

``` text
BikeWale-Web-Scraping-EDA/
│
├── Web_Scraping_Project.ipynb
├── bikewale_cleaned.csv
├── bikewale_analysis_ready.csv
├── BikeWale_Web_Scraping_EDA_Project.pptx
├── README.md
└── images/
    └── charts/
```

------------------------------------------------------------------------

## 🚀 How to Run the Project

### 1. Clone the repository

``` bash
git clone <your-repository-url>
```

### 2. Open the notebook

Open:

``` text
Web_Scraping_Project.ipynb
```

using Jupyter Notebook, JupyterLab, or Google Colab.

### 3. Install required libraries

``` bash
pip install pandas numpy matplotlib seaborn requests
```

### 4. Run the notebook

Execute the cells from top to bottom.

------------------------------------------------------------------------

## 💾 Output

The project produces a cleaned dataset that can be used for further
analysis and visualization.

The main outputs include:

-   Cleaned BikeWale dataset
-   EDA tables
-   Statistical summaries
-   Data visualizations
-   Project presentation

------------------------------------------------------------------------

## ⚠️ Disclaimer

This project is created for **educational and data-analysis purposes**.

The scraped information reflects the data available on the source
website at the time of collection. Prices, ratings, specifications and
availability may change over time.

Please respect the target website's terms of service, robots.txt, rate
limits and applicable policies when performing web scraping.

------------------------------------------------------------------------

## 👨‍💻 Skills Demonstrated

This project demonstrates practical skills in:

-   Web scraping
-   HTML/JSON data extraction
-   Regular expressions
-   Python
-   Pandas
-   NumPy
-   Data cleaning
-   Exploratory Data Analysis
-   Data visualization
-   Statistical interpretation
-   Business insight generation

------------------------------------------------------------------------

## 📌 Future Improvements

Possible extensions include:

-   Build an interactive Power BI dashboard.
-   Add more bike categories and historical data.
-   Analyze price trends over time.
-   Compare manufacturers across multiple performance metrics.
-   Perform advanced statistical analysis.
-   Build a bike recommendation system.
-   Develop a machine learning model for price prediction.

------------------------------------------------------------------------

## ⭐ Conclusion

The BikeWale Web Scraping & EDA project demonstrates how publicly
available web data can be transformed into a structured dataset and
analyzed to identify useful market patterns.

The analysis provides insights into **brand representation, pricing,
fuel type, ratings, mileage and motorcycle specifications**, making the
project a practical example of a complete beginner-level data analytics
workflow.
