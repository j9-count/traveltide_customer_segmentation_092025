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


