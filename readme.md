NYC Yellow Taxi Analysis – November 2025
Project Overview

This project explores NYC Yellow Taxi trips for November 2025 to uncover patterns in trip volumes, fares, tips, distances, durations, payment methods, and hotspot zones. The goal is to gain actionable insights on trip behavior and fare dynamics, suitable for portfolio demonstration and professional sharing.

Dataset

Parquet dataset (yellow_tripdata_2025-11.parquet): Contains 4.18 million taxi trips with 20 columns including pickup/dropoff times, distances, fares, tips, payment type, and location IDs.

Lookup table (taxi_zone_lookup.csv): Maps LocationID to human-readable Zone and Borough, allowing analysis of spatial patterns in pickup and dropoff locations.

Tools Used

Python 3.x

pandas (data manipulation)

matplotlib (visualization)

Analysis Performed
1. Trips per Hour

Counted trips by hour of pickup (pickup_hour).

Insight: Peak trips occur 12:00–18:00, with consistent activity from 00:00–08:00, likely due to airport trips and night-shift commuters.

2. Average Fare & Tip by Hour

Grouped trips by hour, calculated average fare and average tip.

Insight: Highest average fare occurs at 5:00 AM, likely due to long airport trips. Tips are higher during peak hours.

3. Trip Distances & Durations

Calculated trip duration in minutes and summarized trip distances.

Insight: Most trips are shorter than 5 miles and less than 20 minutes, with a few outliers representing long-distance rides.

4. Payment Type Analysis

Mapped numeric payment_type codes to Cash, Credit Card, Dispute, No Charge.

Counted trips and calculated average fare, tip, and total amount per payment method.

Insight:

Credit Cards dominate (~76% of trips) and account for almost all tips.

Cash (~10% of trips) rarely contributes tips.

Dispute/No Charge trips are few but have slightly higher fares.

5. Pickup and Dropoff Zones (Hotspots)

Merged PULocationID and DOLocationID with the lookup table to get readable zone names.

Counted trips per pickup and dropoff zone.

Insight: Midtown Manhattan and airport areas dominate as both pickup and dropoff locations.

Key Insights

Peak Hours: 12:00–18:00 busiest; 00:00–08:00 active for airports/night shifts.

Fare Patterns: 5:00 AM trips have the highest average fares.

Tip Behavior: Almost exclusively from credit card payments.

Trip Characteristics: Most trips are short in distance and duration; outliers exist.

Spatial Patterns: Certain zones (Midtown, airports) generate the most trips, highlighting NYC travel demand patterns.

Next Steps / Optional

Include weather and congestion data to study their impact on fares and trip durations.

Develop predictive models for fare or tip estimation using time, distance, and location features.

Integrate interactive maps or heatmaps of pickups/dropoffs for enhanced visualization.

Data Relationships

The Parquet dataset contains all raw trip records.

The lookup table provides human-readable zones and boroughs for numeric location IDs (PULocationID, DOLocationID).

Merging the datasets enables location-based analysis, such as identifying hotspot zones or incorporating spatial features into predictive modeling.