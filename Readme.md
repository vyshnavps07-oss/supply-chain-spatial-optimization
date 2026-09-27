# 🌐 Geospatial Supply Chain Optimization: Spatial Bottleneck Analysis

**Strategic Impact:** Quantified $202,155 in localized logistics inefficiencies and mathematically proposed 3 new distribution hubs to neutralize a 7.9% system-wide delivery failure rate.

## 📊 Executive Summary
In modern e-commerce, last-mile delivery inefficiencies and regional infrastructure limitations result in severe capital bleed. This project transitions away from traditional descriptive dashboarding to deploy spatial machine learning and geospatial engineering. By analyzing over 100,000 logistics records, this project maps the exact geographic coordinates of supply chain bottlenecks and calculates the financial capital tied up in delayed freight, culminating in a mathematically optimized facility location strategy.

## 📉 The Business Problem
An e-commerce enterprise is experiencing a high rate of delivery delays, compounding logistics overhead, and risking customer churn. While the overall delay rate is known, the company lacks visibility into the specific **spatial distribution of financial loss**. 
* **The Goal:** Identify exactly *where* the supply chain is breaking down, quantify the associated financial loss in those specific geographic zones, and propose optimal locations for new distribution hubs to recover operational losses.

## 🛠️ Methodology & Data Architecture
**1. Financial & Logistics Data Engineering**
* **Data Ingestion & Cleaning:** Engineered a robust Python pipeline to ingest the relational *Olist Brazilian E-Commerce dataset*. Cleaned spatial GPS jitter by aggregating 5-digit CEP (postal code) prefixes and purged temporal "time travel" anomalies.
* **Metric Engineering:** Formulated the "Delivery Delta" (Actual vs. Estimated Delivery) to isolate delayed orders. Modeled a Financial Loss Exposure metric encompassing freight cost and estimated churn replacement value.

**2. Geospatial Visualization & Spatial Filtering**
* Filtered statistical noise to isolate 849 chronic regional bottleneck zones. 
* Deployed `folium` to render an interactive OpenStreetMap layer. Rather than mapping simple order volume, the heatmap was dynamically weighted by **financial loss density**, providing a clear visual of where capital is actively bleeding.

**3. Facility Location Optimization (Machine Learning)**
* Deployed an unsupervised **K-Means Spatial Clustering** algorithm against the geometric coordinates (latitude/longitude) of the chronic delay zones.
* Calculated the geographic centroids of the heaviest financial loss clusters to propose three mathematically optimal coordinates for new strategic fulfillment centers.

## 🚀 Key Results & Insights
* **System-Wide Delay Rate:** 7.90% of all completed logistics cycles failed to meet estimated delivery targets.
* **Financial Loss Exposure:** $202,155 localized revenue bleed tied directly to spatial inefficiencies.
* **The Volume vs. Distance Paradox:** The spatial mapping proved that the heaviest financial losses are not occurring in remote, hard-to-reach inland regions (like the Amazon basin), but are heavily concentrated in the primary southeastern economic corridor (São Paulo and Rio de Janeiro) where high-value customer density overwhelms existing logistics infrastructure.

## 📋 Executive Recommendation
To optimize routing, reduce freight overhead, and neutralize the $202k localized revenue bleed, the enterprise must strategically acquire distribution assets at the following calculated coordinates:

* 📍 **Primary Hub (Southeast):** Lat `-22.145`, Lng `-44.851`
  * *Impact:* Placed in the Paraíba Valley, this intercepts the massive financial bleed between São Paulo and Rio de Janeiro. **(Highest immediate ROI).**
* 📍 **Secondary Hub (South):** Lat `-27.256`, Lng `-51.030`
  * *Impact:* Anchors the Santa Catarina region to capture the secondary delay clusters spreading down the southern coast.
* 📍 **Tertiary Hub (Northeast):** Lat `-8.478`, Lng `-40.165`
  * *Impact:* Consolidates and efficiently routes the scattered, long-distance deliveries plaguing the northern states.

## 💻 Tech Stack
* **Languages:** Python
* **Data Engineering:** `pandas`, `numpy`
* **Geospatial & Visualization:** `folium`, `geopandas`
* **Machine Learning:** `scikit-learn` (K-Means Clustering)