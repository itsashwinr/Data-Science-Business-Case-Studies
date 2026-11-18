# Delhivery – Logistics Data Analysis & Feature Engineering

## Project Overview

This project focuses on analyzing Delhivery's logistics and delivery operations using trip-level data.

The objective is to understand delivery patterns, evaluate route performance, investigate differences between actual and estimated delivery times, and identify opportunities to improve operational efficiency through data-driven insights.

The analysis involves data preprocessing, feature engineering, exploratory data analysis, statistical analysis, and hypothesis testing using Python.

## Business Problem

Delhivery aims to improve its logistics operations through better data quality, operational visibility, and delivery performance analysis.

The challenge is to process raw logistics data, combine multiple delivery segments into meaningful trip-level records, identify patterns in transportation and delivery times, and evaluate differences between actual operational performance and routing estimates.

## Project Objectives

- Understand the structure and quality of logistics data.
- Perform data cleaning and preprocessing.
- Aggregate individual delivery segments into trip-level records.
- Analyze delivery routes and transportation types.
- Compare actual delivery times with estimated delivery times.
- Investigate distance and time variations.
- Identify patterns and operational inefficiencies.
- Perform statistical analysis and hypothesis testing.
- Generate actionable business recommendations.

## Dataset Description

The dataset contains approximately 145,000 records and 24 attributes related to logistics trips and delivery segments.

### Key Attributes

| Attribute | Description |
|---|---|
| trip_uuid | Unique identifier for a trip |
| route_schedule_uuid | Unique route schedule identifier |
| route_type | Transportation type (FTL or Carting) |
| source_center | Origin distribution center |
| destination_center | Destination distribution center |
| trip_creation_time | Time when the trip was created |
| od_start_time | Trip starting timestamp |
| od_end_time | Trip ending timestamp |
| start_scan_to_end_scan | Time between start and end scans |
| actual_distance_to_destination | Actual distance to destination |
| actual_time | Actual cumulative delivery time |
| osrm_time | Estimated time from OSRM |
| osrm_distance | Estimated distance from OSRM |
| segment_actual_time | Actual time for a delivery segment |
| segment_osrm_time | Estimated time for a delivery segment |
| segment_osrm_distance | Estimated distance for a delivery segment |

## Tools & Technologies

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Statistical Analysis:** SciPy
- **Techniques:** EDA, Data Cleaning, Feature Engineering, Hypothesis Testing, Correlation Analysis

## Methodology

### 1. Data Understanding
- Examined dataset structure, dimensions, and data types.
- Identified important logistics attributes.
- Analyzed training and testing data distribution.

### 2. Data Cleaning and Preprocessing
- Handled missing values.
- Identified duplicate records.
- Converted timestamp columns into appropriate datetime formats.
- Examined inconsistent and unusual observations.

### 3. Data Aggregation
- Grouped delivery records using trip and source-destination identifiers.
- Aggregated individual delivery segments into meaningful trip-level records.
- Applied suitable aggregation methods to numerical and categorical attributes.

### 4. Feature Engineering
- Derived total trip duration.
- Analyzed actual and estimated delivery times.
- Examined segment-level and trip-level distance and time metrics.

### 5. Exploratory Data Analysis
- Analyzed route types and delivery patterns.
- Investigated trip creation trends by time and date.
- Examined source and destination centers.
- Studied numerical distributions and relationships between variables.
- Identified outliers and unusual observations.

### 6. Statistical Analysis
- Performed correlation analysis.
- Examined differences between actual and estimated delivery times.
- Used distribution checks and statistical tests to evaluate relevant hypotheses.

## Key Findings

- The dataset contains approximately 14,817 unique trip IDs.
- Approximately 71.9% of the trip records belong to the training dataset and 28.1% to the testing dataset.
- Carting is the most common route type.
- The analysis identified approximately 1,508 unique source centers and 1,481 destination centers.
- Delivery activity generally increases after noon, reaching its highest observed level around 10 PM.
- The 38th week recorded the highest trip activity in the analyzed data.
- Numerical delivery metrics exhibit strong positive correlations, with several correlations exceeding 0.90.
- Actual delivery times and estimated routing times were investigated to understand operational variations.

## Business Recommendations

- Improve delivery time estimation by continuously comparing actual performance with routing estimates.
- Monitor high-volume routes and distribution centers to identify operational bottlenecks.
- Use historical trip patterns to improve workforce and vehicle allocation.
- Investigate routes with significant differences between actual and estimated delivery times.
- Improve data quality and standardization across logistics operations.
- Monitor delivery performance using segment-level and trip-level operational KPIs.

## Conclusion

This case study demonstrates how data analysis and feature engineering can transform raw logistics records into meaningful operational insights.

By combining delivery segments, analyzing route performance, investigating time and distance variations, and applying statistical techniques, the project provides a foundation for improving logistics efficiency and supporting data-driven operational decisions.

---

**Project Category:** Business Analytics | Logistics & Supply Chain Analytics  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy
