# Dynamic-Pricing-for-Urban-Parking-Lots
A real-time dynamic pricing system for smart urban parking lots. This system leverages streaming data and machine learning models to optimize pricing based on demand, congestion, special events, and competitor pricing.

🚀 Project Overview

This project implements:

Dynamic, data-driven pricing strategies for parking lots.

Real-time simulation using Pathway for event ingestion.

Interactive visualization with Bokeh.

Machine Learning models to adapt pricing using various environmental features.

🛠 Tech Stack

Python 3.9+

Pandas: data manipulation

Pathway: event stream processing and ingestion

Bokeh: real-time visual dashboards

scikit-learn: model evaluation and RMSE tuning

Mermaid.js: architecture diagram

📐 System Architecture

graph TD
    A[User / Sensors] -->|Raw Data| B[dataset.csv or Stream API]
    B --> C[Pathway Stream Engine]
    C --> D1[Model 1: Linear]
    C --> D2[Model 2: Demand-Based]
    C --> D3[Model 3: Competitive Pricing]
    D1 & D2 & D3 --> E[Price Decision Output]
    E --> F[Bokeh Dashboard Visualization]

🔄 Workflow Explanation

Ingestion:

dataset.csv is parsed with timestamps to simulate streaming behavior.

Pathway reads and emits the data row-by-row as if it were live.

Processing:

Three models are provided:

Model 1 (Linear): A simple proportional increase based on occupancy.

Model 2 (Demand-Based): Combines occupancy, queue, traffic, special days, and vehicle type.

Model 3 (Competitive): Adds location-based competitor analysis.

Tuning:

Lambda values are optimized using RMSE over a test set.

Output:

All prices are fed into a Bokeh-based dashboard that updates in real time.
