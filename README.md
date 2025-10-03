# traveltide_customer_segmentation_092025

# TravelTide Customer Segmentation & Rewards Program

## 🎯  Project Overview

This project implements a comprehensive customer segmentation analysis for TravelTide, an e-booking platform in the online travel industry. Using machine learning clustering algorithms, the analysis  identifies distinct customer segments and designs personalized rewards programs to  increase customer  retention, boost  booking frequency, and encourage reward program sign-ups.


**Analysis Scope**: 5,722 active customers (January 2023 - September 2025)

 **Methodology**: ML-powered segmentation with behavioral, demographic, and RFM analysis

**Outcome**: 4 customer segments with tailored reward strategies projecting 296% ROI

---

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

---

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

---

## 🚀 Quick Start

### Prerequisites

* Google Account (for Colab access)
  
* Access to TravelTide PostgreSQL database


## Running the Analysis

### 1. Open the Notebook:
   
* Go to Google Colab

* Upload TravelTide_Customer_Segmentation_Analysis.ipynb with shared link: https://colab.research.google.com/drive/1n-Bad82nEnXbruiOsCl08FyKYmRfrJC1?usp=sharing
  
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

Cell 19-20: Generate presentation charts (optional)


3. **Download Results:**
   - `customer_rewards_assignment.csv` - Main deliverable
   - `segment_summary.csv` - Segment statistics
   - Chart PNG files for presentation


## Database Configuration

The database connection is configured in Cell 5:
```python
DATABASE_URL = "postgresql+psycopg2://Test:bQNxVzJL4g6u@ep-noisy-flower-846766.us-east-2.aws.neon.tech/TravelTide?sslmode=require"
COHORT_START_DATE = '2023-01-01'
MIN_SESSIONS = 7 
```

---



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
└── presentation_slides.md                  # ✅ Slide content 
```

---

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

---


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

### Financial Projections (12-Month Outlook)

#### Revenue Impact:

* Additional bookings: $2,100,000

* Increased customer lifetime value: $1,850,000

* Reduced churn savings: $675,000

* Total Revenue: $4,625,000

#### Investment Required:

* Reward program costs: $1,350,000

* Technology implementation: $125,000

* Marketing campaign: $85,000

**Total Investment: $1,560,000**

**ROI: 296%**

#### Expected Improvements

* Booking frequency: +15%

* Customer lifetime value: +20%

* Net Promoter Score: 7.2 → 8.5

* Program enrollment: 85% target



---

## 📊 Main TravelTideSegmentation Class Methods

The core analysis is performed by the `TravelTideSegmentation` class defined in Cell 5:

**Data & Quality:**
- `connect_and_load_data()` - Load data from PostgreSQL database
- Quality checks integrated via `ComprehensiveDataQuality` class

**Analysis Pipeline:**
- `exploratory_data_analysis()` - Initial EDA with statistics
- `create_eda_visualizations()` - Generate exploratory charts
- `prepare_segmentation_features()` - Engineer 40+ features
- `prepare_features_for_clustering()` - Scale and prepare data

**Segmentation:**
- `perform_multiple_segmentations()` - Test 4 clustering algorithms
- `evaluate_segmentation_quality()` - Compare models with metrics
- `interpret_segments()` - Characterize each customer group

**Rewards & Recommendations:**
- `assign_personalized_rewards()` - Map rewards to segments
- `create_visualizations()` - Generate interactive dashboards
- `generate_recommendations()` - Business strategy suggestions
- `save_results()` - Export CSV deliverables

---


## 📤 Deliverables

### Generated Files

1. **customer_rewards_assignment.csv** (Primary Deliverable)
   - Columns: user_id, segment_id, segment_name, assigned_rewards
   - 5,722 customer records with personalized reward assignments

2. **segment_summary.csv**
   - Segment characteristics and statistics
   - Customer counts and percentages per segment

3. **Visualization Charts** (for presentation)
   - `traveltide_presentation_chart.png` - Customer growth chart
   - `investment_vs_revenue_chart.png` - ROI comparison

### Documentation

- **README.md** - Technical documentation (this file)
- **executive_summary.md** - Business-focused summary with ROI analysis
- **presentation_slides.md** - 8-slide deck content (5-8 minute talk)

---

## 🎯 Success Metrics & Monitoring

### KPI Dashboard

**Immediate Indicators (30 Days):**
- Reward program sign-up rate: Target 85%
- Customer engagement with communications
- Early reward redemptions

**Short-Term Metrics (90 Days):**
- Booking frequency by segment
- Reward redemption rates: Target 65%
- Customer satisfaction scores

**Long-Term Impact (6-12 Months):**
- Customer lifetime value growth
- Churn reduction by segment
- Revenue per customer
- Net Promoter Score improvement

### Monitoring Schedule
- **Weekly:** Enrollment and redemption tracking
- **Monthly:** Segment performance analysis
- **Quarterly:** ROI assessment and strategy refinement

---

## 💡 Key Recommendations

### Implementation Roadmap

**Phase 1: Launch (Months 1-2)**
- Deploy segmentation model to production
- Implement reward assignment logic
- Execute targeted communication campaigns
- Set up analytics dashboard

**Phase 2: Optimize (Months 3-4)**
- Monitor reward redemption rates
- A/B test reward combinations
- Refine segment boundaries based on performance
- Collect and integrate customer feedback

**Phase 3: Scale (Months 5-6)**
- Expand to additional customer cohorts
- Add dynamic personalization features
- Implement churn prediction models
- Launch referral program extensions

### Segment-Specific Strategies

**High-Value Segments:**
- VIP customer service line
- Dedicated account managers
- Premium upgrade opportunities
- Exclusive travel packages

**Frequent Travelers:**
- Tier-based loyalty program
- Priority booking and support
- Mobile app enhancements
- Personalized recommendations

**Budget Segments:**
- Deal notifications and alerts
- Flexible payment options
- Budget travel guides
- Price drop notifications

**Occasional Travelers:**
- Seasonal travel reminders
- Planning assistance and guides
- Simplified booking process
- Re-engagement campaigns




---

## 🔧 Customization

### Modifying Cohort Criteria

Edit Cell 5 configuration:

```python
COHORT_START_DATE = '2023-01-01'  # Change start date
MIN_SESSIONS = 7                   # Change minimum sessions
```

### Adjusting Number of Segments

In Cell 11, modify the clustering parameters:

```python
algorithms = {
    'kmeans': [KMeans(n_clusters=k, random_state=42) for k in range(3, 8)],
    # Adjust range(3, 8) to test different numbers of clusters
}
```

### Adding Custom Rewards

In Cell 14, modify the reward options dictionary:

```python
reward_options = {
    'free_hotel_meal': 'Free hotel meal',
    'free_checked_bag': 'Free checked bag',
    # Add new rewards here
    'your_new_reward': 'Your Reward Description'
}
```

---

## 📞 Support & Contact

**For Technical Issues:**
- Review notebook cell outputs for error messages
- Check database connection in Cell 5
- Verify all libraries are imported (Cells 3-4)

**For Business Questions:**
- Refer to `executive_summary.md` for strategic insights
- Review `presentation_slides.md` for stakeholder communication

---

## 📄 Dependencies

See `requirements.txt` for complete list. Key dependencies:

```
pandas>=2.0.0
numpy>=1.24.0
scikit-learn>=1.3.0
psycopg2-binary>=2.9.0
SQLAlchemy>=2.0.0
matplotlib>=3.7.0
seaborn>=0.12.0
plotly>=5.15.0
```

**Note:** Google Colab has most libraries pre-installed. Additional installs handled in Cell 4 if needed.

---

## 🎉 Project Status

**Status:** ✅ Complete and Production-Ready  
**Version:** 1.0.0  
**Last Updated:** October 2025  
**Analysis Date:** September 2025

**Ready for:**
- Executive presentation
- Technical implementation
- Stakeholder approval
- Production deployment

---

## 🏆 Key Achievements

- ✅ Analyzed 5,722 active customers with 95%+ data quality
- ✅ Identified 4 distinct segments with 0.72 silhouette score
- ✅ Designed personalized rewards with 296% projected ROI
- ✅ Created actionable implementation roadmap
- ✅ Delivered presentation-ready visualizations
- ✅ Generated complete customer-reward assignments

---

**For questions or clarifications, refer to the Executive Summary or review the notebook cell outputs for detailed analysis results.**










