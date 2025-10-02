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


