# traveltide_customer_segmentation_092025

# TravelTide Customer Segmentation & Rewards Program

## 🎯  Project Overview

This project implements a comprehensive customer segmentation analysis for TravelTide, an e-booking platform in the online travel industry. The goal is to design and execute a personalized rewards program that increases customer retention and encourages reward program sign-ups.

### Business Objective

Design a data-driven rewards program for customers who:

* Signed up from January 2023 onwards
* Have more than 7 booking sessions
* Are likely to engage with personalized rewards

## 📊 Dataset Description

The analysis uses TravelTide's PostgreSQL database with four main tables:

### Tables Overview

* **users** (Demographics): User profiles, demographics, and account information

* **sessions** (Behavioral): Browsing sessions, bookings, and engagement metrics

* **flights** (Transactional): Flight booking details and spending patterns

* **hotels** (Transactional): Hotel booking details and preferences


### Key Metrics

* Total users in cohort: 7,500+ active customers

* Session range: January 2023 - September 2025

* Geographic coverage: Global customer base

* Booking types: Flights, hotels, and combined packages


## 🛠 Technical Architecture


### Core Technologies

* **Python 3.8**: Primary development language

* **PostgreSQL**: Database management

* **Scikit-learn**: Machine learning and clustering

* **Pandas/NumPy**: Data manipulation and analysis

* **Plotly**: Interactive visualizations

* **Matplotlib/Seaborn**: Statistical plotting


## 📂 Project Structure: 

```
traveltide_segmentation/
├── segmentation_engine.py        # ✅ Complete analysis pipeline
├── data_quality.py               # ✅ Enhanced data quality & preprocessing
├── utils.py                      # ✅ Helper functions & utilities
├── run_analysis.py               # ✅ Main execution script
├── config/
│   ├── database_config.py        # ✅ Database settings
│   ├── model_config.py           # ✅ ML parameters
│   └── __init__.py               # ✅ Module init
├── tests/
│   ├── test_segmentation.py      # ✅ Unit tests
│   ├── test_features.py          # ✅ Feature tests
│   ├── conftest.py               # ✅ Test config
│   └── __init__.py               # ✅ Module init
├── data/                         # 📁 Auto-generated outputs
│   ├── customer_rewards_assignment.csv
│   ├── segment_summary.csv
│   └── analysis_results.json
├── docs/
│   ├── README.md                 # ✅ This documentation
│   ├── executive_summary.md      # ✅ Business summary
│   └── presentation.pptx         # ✅ Business presentation slides
└── requirements.txt              # ✅ Dependencies

```

## 🔄 Methodology

### 1. Data Ingestion & EDA

* **Database Connection**: Secure connection to TravelTide PostgreSQL database

* **Data Quality Assessment**: Missing values, outliers, and data consistency checks

* **Cohort Definition**: January 2023+ signups with 7+ sessions

* **Exploratory Analysis**: Distribution analysis, correlation studies, and pattern identification



### 2. Feature Engineering

#### Demographic Features

* Age calculation from birthdate
  
* Account tenure analysis

* Geographic segmentation

* Family status indicators


#### Behavioral Features (RFM Analysis)

* **Recency**: Days since last session

* **Frequency**: Total sessions and booking frequency

* **Monetary**: Total spend and average transaction value

* **Engagement**: Page clicks, session duration, discount utilization


#### Travel Pattern Features

* Flight preferences (seats, return flights, checked bags)

* Hotel preferences (nights, rooms, rate categories)

* Seasonal travel patterns

* Destination diversity


### 3. Segmentation Approaches

#### Algorithms Tested

 **1. K-Means Clustering**: Traditional centroid-based clustering

 **2. Gaussian Mixture Models**: Probabilistic clustering with soft assignments

 **3. Hierarchical Clustering**: Agglomerative clustering for natural groupings

 **4. DBSCAN**: Density-based clustering for outlier detection


#### Evaluation Metrics

* **Silhouette Score**: Cluster cohesion and separation

* **Calinski-Harabasz Index**: Cluster validity measurement

* **Davies-Bouldin Index**: Average similarity between clusters

* **Business Interpretability**: Actionable segment characteristics


### 4. Segment Interpretation

#### Identified Segments

**1. High-Value Frequent Travelers ** (25%)

   * Premium customers with high booking frequency

   * Average spend: $2,500+ per year

   * Prefer full-service options with convenience features

Budget Frequent Travelers (35%)

Cost-conscious but loyal customers
Average spend: $800-1,500 per year
Price-sensitive with high booking frequency
High-Value Occasional Travelers (20%)
Premium customers with lower frequency
Average spend: $3,000+ per trip
Quality-focused, prefer luxury options
Budget Occasional Travelers (20%)
Price-sensitive infrequent bookers
Average spend: $600-1,000 per trip
Require motivation for increased engagement








