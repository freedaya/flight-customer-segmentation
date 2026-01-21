# ✈️ Flight Customer Segmentation (K-Means + PCA Insights)

## 👋 Hey there!  
This project is about grouping airline customers based on their travel habits and loyalty patterns using **K-Means clustering**. The goal is to understand customers better and give actionable insights for marketing and retention.  

## 🎯 What’s the Goal?  
- Identify distinct customer segments from flight and loyalty data  
- Understand key characteristics of each group  
- Provide actionable business recommendations  

## 📂 Dataset Overview  
Columns used in this project:  
- **MEMBER_NO-b**: Customer ID  
- **FFP_DATE**: Frequent Flyer Program Join Date  
- **FIRST_FLIGHT_DATE**: Date of first flight  
- **GENDER**: Customer gender  
- **FFP_TIER**: Frequent Flyer Program tier  
- **WORK_CITY**: Home city  
- **WORK_PROVINCE**: Home province  
- **WORK_COUNTRY**: Home country  
- **AGE**: Customer age  
- **LOAD_TIME**: Data extraction date  
- **FLIGHT_COUNT**: Number of flights  
- **BP_SUM**: Travel/Booking plan  
- **SUM_YR_1**: Total points/credit year 1  
- **SUM_YR_2**: Total points/credit year 2  
- **SEG_KM_SUM**: Total distance flown (km)  
- **LAST_FLIGHT_DATE**: Last flight date  
- **LAST_TO_END**: Time from last flight to booking  
- **AVG_INTERVAL**: Average interval between flights  
- **MAX_INTERVAL**: Maximum interval between flights  
- **EXCHANGE_COUNT**: Number of redemptions  
- **avg_discount**: Average discount received  
- **Points_Sum**: Total points earned  
- **Point_NotFlight**: Points not used  

> **Note:** This project was done in **Jupyter Notebook** 📝  

## 🔍 Analysis Workflow  
- Data preprocessing (missing values, feature selection)  
- Exploratory Data Analysis (EDA) to find patterns  
- K-Means clustering to segment customers  
- PCA for dimensionality reduction & visualization  
- Determining optimal clusters with Elbow Method & Silhouette Score  
- Cluster profiling and business insights  

## 📊 PCA Insights  
- **PC1 = Customer Value & Activity Level**  
  - High value & frequent flyers = right side  
  - Low value & rare flyers = left side  
  - Features: `SEG_KM_SUM`, `BP_SUM`, `MEMBERSHIP_DAYS`, `AVG_KM_PER_FLIGHT`  

- **PC2 = Recency & Engagement Pattern**  
  - Recently active = top  
  - Dormant = bottom  
  - Features: `LAST_TO_END`, `AVG_INTERVAL`, `avg_discount`  

## 📈 Cluster Segmentation  
- **Cluster 0 (Red)**: Core Loyal Customers (high value & activity, top-right)  
- **Cluster 1 (Blue)**: Dormant / Low Value Users (low activity, bottom-left)  
- **Cluster 2 (Green)**: Active Users, Price-Sensitive (top-right but below Cluster 0)  
- **Cluster 3 (Purple)**: New / Growing Users (top-left)  

## 💡 Business Recommendations  

**Cluster 0 – Core Loyal Customers**  
- Exclusive loyalty perks (priority boarding, bonus mileage)  
- Personalized offers based on travel history  
- Focus on experience & convenience, not discounts  
- **Goal:** Maintain revenue & increase lifetime value  

**Cluster 1 – Dormant / Low Value Users**  
- Re-activation campaigns (email, push notifications)  
- Limited-time discounts  
- Minimal resource allocation  
- **Goal:** Test reactivation potential with low cost  

**Cluster 2 – Active, Price-Sensitive Users**  
- Dynamic pricing & targeted promotions  
- Bundling flights + add-ons  
- Rewards based on frequency, not transaction value  
- Encourage migration to loyal cluster through non-discount benefits  
- **Goal:** Increase margin without losing flight frequency  

**Cluster 3 – New / Growing Users**  
- Strong onboarding journey  
- Educate about loyalty program benefits  
- Light promotions (welcome bonus)  
- Encourage repeat bookings soon  
- **Goal:** Convert into long-term loyal customers  

## 🛠 Tools & Libraries Used  
- Python  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  
- Jupyter Notebook  
