# Big-Data-Project

The DfT Road Safety Vehicle Dataset (2020–2024)

Your PySpark analysis workflow

Your group presentation findings

Your individual reflective report

Your peer‑evaluation summary

Your dataset cleaning rules

Your D → I → K framework outputs

# UK Road Safety Vehicle Dataset (2020–2024) – Big Data Project

Group 5 – MSc Data Science | University of the West of England, Bristol
Members: Iyenoma Goodnews Osabuohien (26001003), Tharsana Kanakarasa, Chukwuemeka Ohiaeri, Ahanaf Pervez

# Table of Contents

# Project Overview

Dataset Description

Technology Stack

Data Cleaning & Quality Rules

Exploratory Data Analysis (EDA)

Key Findings (D → I → K Framework)

E‑Scooter Trend Analysis

Collision Structure Analysis

Conclusion & Limitations

Individual Reflection Summary

Peer Evaluation Summary

Recommended Next Steps

# Project Overview

This Big Data project analyses the DfT STATS19 Road Safety Vehicle Dataset (2020–2024) using PySpark to process:

920,692 vehicle-level records

32 columns

5 years of police-reported personal-injury collisions

The project focuses on:

Vehicle type dominance

Driver demographics

Annual changes in vehicle composition

E-scooter involvement trends

Multi-vehicle collision patterns

Data completeness and missingness

Reproducible Big Data workflows using PySpark

# Dataset Description

Source: UK Department for Transport – Road Safety Open Data
File: Vehicle-level STATS19 dataset
Years: 2020, 2021, 2022, 2023, 2024
Rows: 920,692
Columns: 32
Unit: One vehicle involved in a police-reported personal-injury collision

# Technology Stack

| Component           | Tool                               |
| ------------------- | ---------------------------------- |
| Big Data Processing | **PySpark (Google Colab)**         |
| Data Cleaning       | PySpark DataFrame API              |
| Visualisation       | Matplotlib / Seaborn               |
| Documentation       | Markdown, PowerPoint               |
| Dataset Lookup      | DfT STATS19 official documentation |

# Data Cleaning & Quality Rules

# Decode coded values

All DfT STATS19 coded fields were converted to human-readable labels.

# Use valid denominators

Invalid values were removed only from analyses where they matter (e.g., age, engine capacity).

# Check record identity

No duplicate vehicle keys found.

# Validate final dataset

All 920,692 rows retained; each analysis applied field-specific validity rules.

# PySpark reproducibility

All grouped queries and charts were generated using PySpark transformations.

# Exploratory Data Analysis (EDA)

EDA explored:

Vehicle type distribution

Driver age profiles

Annual record counts

Engine capacity patterns

E-scooter involvement

Vehicles per collision

Missingness by year

# Key Findings (D → I → K Framework)

1. Cars dominate the dataset
   Data:  
   Cars = 628,614 records (68.8% of valid vehicle types)

Information:  
Passenger vehicles overwhelmingly dominate police-reported collisions.

Knowledge:  
Exposure-adjusted rates are needed before claiming cars are “riskier.”

2. Young-driver representation varies sharply by vehicle type
   Data:  
   Share of drivers aged 17–29:

50–125cc motorcycles: 55.3%

Cars: 27.4%

Large goods vehicles: 9.4%

Information:  
Motorcycle riders skew younger.

Knowledge:  
Education may help, but these are involvement counts, not risk rates.

3. Vehicle composition changed modestly by year
   Data:  
   Car share rose from 68.39% → 69.15%  
   Pedal-cycle share fell from 10.04% → 8.45%

Information:  
Small shifts in modal share.

Knowledge:  
Changes may reflect travel patterns, not safety outcomes.

4. Recorded vehicle counts peaked in 2022
   Data:  
   2020: 167,375
   2022: 193,545 (peak)
   2024: 183,514 (↓ 5.2% from peak)

Information:  
Involvement volume fluctuates.

Knowledge:  
Traffic exposure and reporting influence counts.

# E‑Scooter Trend Analysis

Data:

2020: 461

2021: 1,365

2022–2024: ~1,300–1,400 per year

Information:  
+196.1% increase from 2020 → 2021.

Knowledge:  
Growth likely due to rental trials and reporting—not necessarily increased risk.

# Collision Structure Analysis

Data:

One vehicle: 28.9%

Two vehicles: 62.3%

Three+ vehicles: 8.8%

Information:  
Two-vehicle collisions are most common.

Knowledge:  
One-vehicle records may still involve pedestrians or cyclists.

# Conclusion & Limitations

# Scale & reproducibility

PySpark processed 920k+ records with consistent grouped queries.

# Strongest findings

Cars dominate

2022 was the peak year

E-scooter involvement rose sharply

Two-vehicle collisions are most common

# Interpret carefully

These are involvement counts, not collision rates

Missingness increased in 2024

Exposure data is required for risk analysis

# Individual Reflection Summary (Student ID: 26001003)

Your reflection highlights:

Major technical contribution:

Downloading dataset

Setting up PySpark

Cleaning rules

Lookup table decoding

Writing core analysis queries

Generating charts

What went well:

Strong technical foundation

Accurate PySpark outputs

Clear visualisations

Challenges:

Early misunderstanding of lookup tables

Required pipeline rebuild

Learning:

Importance of planning before coding

Balancing technical work with presentation preparation

# Peer Evaluation Summary

| Student            | Mark | Comment                                                        |
| ------------------ | ---- | -------------------------------------------------------------- |
| **Iyenoma (Self)** | 4.0  | —                                                              |
| **Tharsana**       | 3.0  | Supported cleaning, verified codes, improved presentation      |
| **Chukwuemeka**    | 2.0  | Helpful in communication and discussions                       |
| **Ahanaf**         | 3.0  | Worked on visualisations, D → I → K, connected Colab to slides |

Total = 12 (required for 4 members × average score 3)

# Recommended Next Steps

Join vehicle, collision, and casualty files

Analyse:

Severity

Weather

Speed limits

Road type

Add exposure measures (traffic volume, population)

Build machine learning models for:

Severity prediction

Collision type classification

E-scooter risk profiling
