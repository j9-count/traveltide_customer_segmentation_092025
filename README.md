# traveltide_customer_segmentation_092025

# TravelTide Customer Segmentation & Rewards Program

## 🎯  Project Overview

This project implements a comprehensive customer segmentation analysis for TravelTide, an e-booking platform in the online travel industry. Using machine learning clustering algorithms, the analysis  identifies distinct customer segments and designs personalized rewards programs to  increase customer  retention, boost  booking frequency, and encourage reward program sign-ups.


**Analysis Scope**: 5,722 active customers (January 2023 - September 2025)

 **Methodology**: ML-powered segmentation with behavioral, demographic, and RFM analysis

**Outcome**: 4 customer segments with tailored reward strategies projecting 296% ROI



## 📊 Dataset Description

The analysis uses TravelTide's PostgreSQL database with four main tables:

### Tables Overview

* **users** (Demographics): 7,500+ user profiles with demographic and account information

* **sessions** (Behavioral): 50,000+ booking sessions with engagement metrics

* **flights** (Transactional): 15,000+ flight bookings with spending patterns

* **hotels** (Transactional): 12,000+ hotel bookings with preference data

#### Cohort Criteria:

* Sign-up date: January 2023 onwards

* Minimum activity: 7+ booking sessions

* Result: 5,722 eligible customers analyzed  



## 🛠 Technical Architecture

**Platform**: Google Colab (Jupyter Notebook) 
<br>
**Language**: Python 3.10+
<br>
**Key Libraries**:

* **Pandas, NumPy**: Data manipulation and analysis

* **psycopg2, SQLAlchemy**: Databas
  
* **Scikit-learn**: Machine learning and clustering (K-Means, Gaussian Mixture, Hierarchical, DBSCAN)

* **Plotly**: Interactive visualizations

* **Matplotlib/Seaborn**: Statistical plotting



## 🚀 Quick Start

### Prerequisites

* Google Account (for Colab access)
  
* Access to TravelTide PostgreSQL database


## Running the Analysis

### 1. Open the Notebook:
   
* Go to Google Colab

* Upload TravelTide_Segmentation.ipynb with shared link:
  
### Run All Cells Sequentially:

Cell 1-4: Import libraries

Cell 5: Define classes and configuration

Cell 6: Load and clean data

Cell 7-8: Exploratory data analysis

Cell 9-10: Feature engineering and preparation

Cell 11-12: Apply clustering algorithms

Cell 13: Interpret customer segments

Cell 14: Assign personalized rewards

Cell 15: Generate business recommendations

Cell 16: Save results and display summary

Cell 17-18: Generate presentation charts (optional)


**Download Results:**

* customer_rewards_assignment.csv - Main deliverable

* segment_summary.csv - Segment statistics
  
* Chart PNG files for presentation


## Database Configuration

The database connection is configured in Cell 5:

```python
DATABASE_URL = "postgresql+psycopg2://Test:bQNxVzJL4g6u@ep-noisy-flower-846766.us-east-2.aws.neon.tech/TravelTide?sslmode=require"
COHORT_START_DATE = '2023-01-01'
MIN_SESSIONS = 7



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

**1. High-Value Frequent Travelers**  (25%)

 *  Premium customers with high booking frequency

 *  Average spend: $2,500+ per year

 *  Prefer full-service options with convenience features

**2. Budget Frequent Travelers**    (35%)

 * Cost-conscious but loyal customers

 * Average spend: $800-1,500 per year

 * Price-sensitive with high booking frequency

**3. High-Value Occasional Travelers**     (20%)
   
 * Premium customers with lower frequency

 * Average spend: $3,000+ per trip

 * Quality-focused, prefer luxury options

**4. Budget Occasional Travelers**   (20%)
   
 * Price-sensitive infrequent bookers

 * Average spend: $600-1,000 per trip

 * Require motivation for increased engagement


## 🎁 Personalized Rewards Program

### Reward Categories

**1. Free Hotel Meal**: Complimentary breakfast or dining credit

**2. Free Checked Bag:** Waived baggage fees for flights

**3. No Cancellation Fees**: Flexible booking modifications

**4. Exclusive Discounts**: Member-only pricing and flash sales

**5. Free Hotel Night**: Complimentary night with flight bookings



### Segment-Specific Assignments


**High-Value Frequent Travellers**

* ✅ 1 night free hotel with flight
  
* ✅ Exclusive discounts
  
* ✅ No cancellation fees
  
**Budget Frequent Travellers**

* ✅ Exclusive discounts

* ✅ Free checked bag

* ✅ No cancellation fees

**High-Value Occasional Travellers**

* ✅ Free hotel meal

* ✅ 1 night free hotel with flight

* ✅ Exclusive discounts

**Budget Occasional Travellers**

* ✅ Free hotel meal

* ✅ Exclusive discounts

* ✅ Free checked bag


## 📈 Expected Business Impact


### Customer Retention Improvements

* **15-20% increase** in booking frequency for occasional travellers

* **10-15% improvement** in customer lifetime value

* **25-30% boost** in rewards program enrollment

### Revenue Projections

* **$2.1M additional revenue** from increased bookings (12-month projection)

* **$450K in incremental profit** from improved retention

* **ROI of 340%** on rewards program investment


## 🚀 Implementation Roadmap

### Phase 1: Program Launch (Months 1-2)

* Deploy segmentation model to production

* Implement reward assignment logic

* Launch customer communication campaign

* Set up tracking and analytics infrastructure

### Phase 2: Optimization (Months 3-4)

* Monitor reward redemption rates

* A/B test different reward combinations

* Refine segment definitions based on performance

* Expand program to additional customer cohorts

### Phase 3: Scale & Enhance (Months 5-6)

* Integrate real-time segmentation updates

* Add predictive modeling for churn prevention

* Implement dynamic reward personalization

* Launch referral program extensions


## 📊 Monitoring & Evaluation

### KPI Dashboard Metrics

* **Enrollment Rate**: Percentage of eligible customers joining rewards program

* **Redemption Rate**: Frequency of reward utilization

* **Booking Frequency**: Change in customer booking patterns

* **Customer Lifetime Value**: Long-term value improvement

* **Net Promoter Score**: Customer satisfaction measurement


### Evaluation Schedule

* **Weekly**: Enrollment and redemption tracking

* **Monthly**: Segment performance analysis

* **Quarterly**: ROI assessment and strategy refinement

* **Annually**: Complete program effectiveness review


## 🔧 Installation & Setup

### Prerequisites
`bash`

Python 3.8+ 
<br>
PostgreSQL client 
<br>
Git 



### Installation Steps

`bash`

*`#Clone repository`* 
<br>
git clone https://github.com/j9-count/traveltide_customer_segmentation_092025/blob/main/README.md
<br>
cd customer-segmentation

*`#Create virtual environment`* 
<br>
python -m venv venv
<br>
 source venv/bin/activate # On Windows: venv\Scripts\activate


*`#Install dependencies`* pip install -r requirements.txt


*`#Set up environment variables`* 
<br>
cp config/.env.example config/.env 
<br>
*`#Edit config/.env with your database credentials`*


*`#Run the analysis`* 
<br>
python src/segmentation_engine.py





### Environment Variables

`env`
<br>
DATABASE_URL=postgresql+psycopg2://username:password@host:port/database
<br>
COHORT_START_DATE=2023-01-01
<br>
MIN_SESSIONS=7






### 📋 Usage Examples

### Basic Segmentation Analysis
python
<br>
from src.segmentation_engine import TravelTideSegmentation

*`#Initialize engine`*
<br>
segmentation = TravelTideSegmentation(DATABASE_URL)


*`#Run complete analysis`*
<br>
results = segmentation.run_full_analysis()


*`#Access results`*
<br>
segments = results['segments']
<br>
rewards = results['reward_assignments']


### Custom Segment Analysis

python
<br>
*`#Load specific user cohort`*
<br>
custom_cohort = segmentation.get_cohort(
   <br>
      start_date='2023-01-01',
    <br>
      min_sessions=7,
    <br>
      countries=['US', 'CA', 'UK']
)

*`#Apply segmentation`*
<br>
custom_results = segmentation.segment_customers(custom_cohort)


```python
# Load specific user cohort
custom_cohort = segmentation.get_cohort(
    start_date='2023-06-01',
    min_sessions=10,
    countries=['US', 'CA', 'UK']
)









