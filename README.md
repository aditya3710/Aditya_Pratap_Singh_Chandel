# 🎮 The Telemetry Engine

**A Hybrid Machine Learning Architecture for Dynamic Monetization and Player Retention**

## 📊 Executive Summary

The modern "Games as a Service" (Live-Ops) industry bleeds revenue through two unoptimized gaps: **Blind Monetization** (failing to target high-value players early) and **Frustration-Induced Churn** (players quitting due to consecutive losses).

**The Telemetry Engine** is a game-agnostic, B2B machine learning pipeline that solves this. It utilizes a hybrid architecture (Unsupervised + Supervised ML) to simultaneously predict a player's Lifetime Value (LTV) for targeted storefront marketing, while monitoring live telemetry to trigger Dynamic Difficulty Adjustments (DDA) and prevent player churn.

---

## 🏗️ System Architecture

The project is broken into a 3-Phase Machine Learning Pipeline:

### Phase 1: Persona Discovery (Unsupervised Learning)

* **Objective:** Discover hidden spending personas without pre-labeled data.
* **Algorithm:** PCA + K-Means Clustering (K=3).
* **Action:** Segments historical player data into business categories: *Casuals*, *Grinders*, and *Whales*.

### Phase 2: Early-Game Monetization Prediction (Supervised Learning)

* **Objective:** Predict a brand-new player's LTV persona within their first 24 hours.
* **Algorithm:** Random Forest Classifier.
* **Action:** Analyzes Day 1 mechanical engagement to accurately predict the Phase 1 cluster, allowing the Marketing API to dynamically serve premium cosmetic bundles or ad-based monetization on Day 2.

### Phase 3: Real-Time Frustration Monitor (Supervised Learning)

* **Objective:** Prevent rage-quitting by monitoring split-second live match data.
* **Algorithm:** Logistic Regression (Probability Scoring).
* **Action:** Ingests live telemetry (health, armor, time). If the probability of failure crosses **75%**, the engine triggers a game-logic API to deploy "Dynamic Assists" (e.g., lowering enemy AI), saving the Customer Acquisition Cost (CAC).

---

## 📂 Datasets Used

This architecture proves cross-genre scalability by utilizing two distinct Kaggle datasets:

1. **Monetization Engine:** `cookie_cats.csv` (Mobile Game A/B Testing & Retention Data) - ~90k rows.
2. **Live Telemetry Engine:** `csgo_round_snapshots.csv` (Tactical PC Shooter Live Data) - ~122k rows.

---

## 🚀 Installation & Usage

1. **Clone the repository:**
```bash
git clone https://github.com/aditya3710/Aditya_Pratap_Singh_Chandel.git
cd Aditya_Pratap_Singh_Chandel

```


2. **Install dependencies:**
Ensure you have Python installed, then run:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

```


3. **Run the Engine:**
Open the Jupyter Notebook to view the visualized pipeline and the dynamic live-inference dashboard.
```bash
jupyter notebook telemetry_engine.ipynb

```



---

## 💼 Business Impact & ROI

* **Eradicated CAC Waste:** By identifying when a player is statistically about to quit out of frustration, the DDA engine prevents churn, directly salvaging marketing acquisition costs.
* **Optimized Conversion Rates:** Eliminates "spray and pray" marketing by identifying high-LTV "Whales" on Day 1, allowing for aggressive, targeted microtransaction UI scaling.
* **A/B Testing Integration:** Leverages statistical significance testing on paywall pacing to inform product management decisions prior to ML deployment.

---

## 👨‍💻 About the Author

**Aditya Pratap Singh Chandel** *IPM Candidate at IIM Rohtak | Marketing, Business Development & Analytics*

Bridging the gap between raw data science and high-level business strategy. Passionate about utilizing machine learning to drive revenue growth, optimize consumer behavior, and build scalable B2B tech products.

* 🔗 **LinkedIn:** [(https://www.linkedin.com/in/aditya-pratap-singh-chandel-260720325/)]
* 📧 **Email:** [ipm06adityap@iimrohtak.ac.in]
* 🎓 **Institution:** Indian Institute of Management (IIM) Rohtak

