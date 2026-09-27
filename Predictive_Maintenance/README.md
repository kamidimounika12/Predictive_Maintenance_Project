
# Predictive Maintenance Analysis using Databricks & PySpark

## Project Overview

This project implements an end-to-end Predictive Maintenance solution using Databricks, PySpark, and Spark SQL. The objective is to analyze machine telemetry, maintenance, failure, and error data to identify failure patterns, detect anomalies, evaluate machine reliability, forecast machine behavior, and optimize maintenance schedules.

The project follows the Medallion Architecture (Bronze, Silver, and Gold Layers) to build a scalable data engineering and analytics pipeline.

---

# Business Problem

Manufacturing organizations often face unexpected machine failures that lead to:

* Production downtime
* Increased maintenance costs
* Reduced equipment efficiency
* Revenue loss

This project aims to predict and prevent failures by analyzing historical machine data and generating actionable maintenance insights.

---

# Project Objectives

* Build a Bronze-Silver-Gold data pipeline
* Analyze machine failure patterns
* Identify high-risk machines
* Detect anomalies in telemetry data
* Evaluate maintenance effectiveness
* Forecast future machine behavior
* Improve maintenance planning
* Increase equipment reliability

---

# Dataset Information

| Dataset     | Records |
| ----------- | ------: |
| Machines    |     100 |
| Telemetry   | 876,100 |
| Errors      |   3,919 |
| Failures    |     761 |
| Maintenance |   3,286 |

### Data Sources

The project uses:

* Telemetry Data
* Error Logs
* Failure Records
* Maintenance Records
* Machine Information

---

# Project Architecture

```text
Raw Data
    │
    ▼
Bronze Layer
(Raw Ingestion)
    │
    ▼
Silver Layer
(Data Cleaning & Transformation)
    │
    ▼
Gold Layer
(Business Analytics)
    │
    ▼
Insights & Visualizations
```

---

# Bronze Layer

### Purpose

Store raw data without modifications.

### Tables

```text
bronze_telemetry
bronze_errors
bronze_failures
bronze_maint
bronze_machines
```

### Activities

* Data ingestion
* Schema validation
* Raw storage

---

# Silver Layer

### Purpose

Clean and transform data.

### Activities

* Null value checks
* Datetime conversion
* Data type validation
* Feature engineering
* Age group creation

### Tables

```text
silver_telemetry
silver_errors
silver_failures
silver_maint
silver_machines
```

---

# Gold Layer Analytics

## Q1: Error Pattern Analysis

### Objective

Identify frequently occurring machine errors.

### Findings

* Error3 occurred most frequently.
* Error4 occurred least frequently.

### Business Benefit

Early identification of recurring machine issues.

---

## Q2: Machine Age Analysis

### Objective

Analyze telemetry behavior across machine age groups.

### Findings

* Similar telemetry readings across age groups.
* Age alone is not a strong failure indicator.

### Business Benefit

Maintenance decisions should rely on sensor behavior rather than age alone.

---

## Q3: Maintenance Impact Analysis

### Objective

Evaluate telemetry readings before and after maintenance.

### Findings

* Sensor readings remained relatively stable.
* Maintenance helped maintain operational consistency.

### Business Benefit

Supports preventive maintenance strategies.

---

## Q4: Telemetry Forecasting

### Objective

Predict future voltage values.

### Results

* MAE = 13.09

### Business Benefit

Forecasting helps anticipate equipment behavior.

---

## Q5: Anomaly Detection

### Objective

Identify abnormal machine behavior.

### Results

* 148 high-risk records detected.

### Business Benefit

Early warning system for potential failures.

---

## Q6: Failure Probability Modeling

### Objective

Identify machines with highest risk.

### High-Risk Machines

```text
98
99
37
22
73
```

### Business Benefit

Prioritize maintenance resources efficiently.

---

## Q7: Machine Reliability Analysis

### Most Reliable Machines

```text
77
6
72
```

### Least Reliable Machines

```text
99
98
22
```

### Business Benefit

Supports asset management decisions.

---

## Q8: Failure Type Analysis

### Findings

| Component | Failures |
| --------- | -------: |
| Comp2     |      259 |
| Comp1     |      192 |
| Comp4     |      179 |
| Comp3     |      131 |

### Business Benefit

Focus maintenance on critical components.

---

## Q9: Maintenance Optimization

### Findings

* Total Maintenance Activities: 3,286
* Comp2 received the highest maintenance attention.
* Comp2 also recorded the highest failures.

### Business Benefit

Improves maintenance scheduling efficiency.

---

## Q10: Executive Summary

Consolidated all findings and generated business recommendations for predictive maintenance implementation.

---

# Key Project Results

| Metric                 |   Value |
| ---------------------- | ------: |
| Machines               |     100 |
| Telemetry Records      | 876,100 |
| Error Records          |   3,919 |
| Failure Records        |     761 |
| Maintenance Records    |   3,286 |
| High-Risk Records      |     148 |
| Forecasting MAE        |   13.09 |
| Most Failed Component  |   Comp2 |
| Most Reliable Machine  |      77 |
| Least Reliable Machine |      99 |

---

# Technologies Used

* Databricks
* Apache Spark
* PySpark
* Spark SQL
* Delta Lake
* Data Visualization
* Medallion Architecture

---

# Skills Demonstrated

* Data Engineering
* ETL Pipeline Development
* Data Cleaning
* Data Transformation
* Feature Engineering
* Exploratory Data Analysis
* Predictive Analytics
* Anomaly Detection
* Forecasting
* Reliability Analysis
* Data Visualization

---

# Future Enhancements

* Real-time streaming analytics
* Machine learning failure prediction models
* Predictive maintenance dashboard
* Automated alert system
* Integration with IoT sensor platforms

---

# Author

**Mounika Kamidi**
B.Tech Computer Science and Engineering
Databricks | PySpark | SQL | Data Analytics


