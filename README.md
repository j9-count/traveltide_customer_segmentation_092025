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
  
### 2. Run All Cells Sequentially:

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



``` 
## 📂 Project Structure: 

```
TravelTide_Segmentation_Project/
├── TravelTide_Segmentation.ipynb           # ✅ Main analysis notebook (Cells 1-18)
├── customer_rewards_assignment.csv         # ✅ Output: Customer-reward mapping
├── segment_summary.csv                     # ✅ Output: Segment characteristics
├── traveltide_presentation_chart.png       # ✅ Output: Growth chart for slides
├── investment_vs_revenue_chart.png         # ✅ Output: ROI visualization
├── requirements.txt                        # ✅ Python dependencies
├── README.md                               # ✅ This documentation
├── executive_summary.md                    # ✅ Business summary
└── presentation_slides.md                  # ✅ Slide content (5-8 min talk)
```


## 🔬 Methodology

### 1. Data Quality Pipeline

* Missing value imputation (KNN, median/mode strategies)

* Outlier detection and treatment (IQR + Isolation Forest)

* Business rule validation (age, dates, pricing constraints)

* Data type standardization and duplicate removal

### 2. Feature Engineering
   
#### Demographic Features:

* Age, account tenure, family status, location

#### Behavioral Features (RFM Analysis):

* Recency: Days since last session

* Frequency: Total sessions and booking frequency

* Monetary: Total spend and average transaction value

#### Travel Pattern Features:

* Flight preferences (seats, return flights, checked bags)

* Hotel preferences (nights, rooms, rate categories)

* Seasonal patterns and destination diversity

### 3. Segmentation Algorithms Tested

**1. K-Means Clustering**  - Centroid-based partitioning

**2. Gaussian Mixture Models**  - Probabilistic clustering

**3. Hierarchical Clustering**  - Agglomerative approach

**4. DBSCAN** -  Density-based clustering

#### Selection Criteria:

* Silhouette Score (cluster cohesion and separation)

* Calinski-Harabasz Index (cluster validity)

* Davies-Bouldin Index (cluster similarity)

* Business interpretability
#### Best Model: K-Means with 4 clusters (Silhouette Score: 0.72)



## 📈 Key Results

### Customer Segments Identified

**1. Premium Frequent Flyers (25% - 1,431 customers)**
   
* Average spend: $2,500/year (~$167/booking)

* Booking frequency: 15+ sessions/year

* Characteristics: Value convenience and flexibility

**2. Deal-Seeking Regulars (35% - 2,003 customers)**
   
* Average spend: $1,200/year (~$100/booking)

* Booking frequency: 12+ sessions/year

* Characteristics: Price-conscious but loyal

**3. Luxury Occasional Travelers (20% - 1,144 customers)**
   
* Average spend: $3,000/trip

* Booking frequency: 5-8 sessions/year

* Characteristics: Quality-focused for special occasions

**4. Budget-Conscious Explorers (20% - 1,144 customers)**
   
* Average spend: $800/trip

* Booking frequency: 5-7 sessions/year

* Characteristics: Need engagement incentives



## 🎁 Personalized Rewards Strategy


| Segment | Assigned Rewards | Strategic Rationale |
|---------|------------------|---------------------|
| Premium Frequent | Free hotel night, No cancellation fees, Exclusive discounts | Flexibility and convenience |
| Deal-Seeking | Exclusive discounts, Free checked bag, No cancellation fees | Cost savings and value |
| Luxury Occasional | Free hotel meal, Free hotel night, Exclusive discounts | Quality enhancements |
| Budget-Conscious | Free hotel meal, Exclusive discounts, Free checked bag | Multiple value-adds |

---






## 💰 Business Impact






## 🚀 Implementation Roadmap



## 📊 Monitoring & Evaluation














