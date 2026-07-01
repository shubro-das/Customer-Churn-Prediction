# Project Phases

# Phase 1 — Data Foundation (SQL + Data Engineering)

## Phase Overview

In any production machine learning project, data is the foundation. Before building dashboards, training models, or deploying AI services, the data must be understood, validated, organized, and transformed into a reliable analytical dataset.

The objective of this phase is to simulate the work of a Junior Data Scientist or Analytics Engineer. Rather than immediately building machine learning models, the focus is on understanding how business data is stored, ensuring its quality, and preparing it for downstream analytics and machine learning tasks.

This phase establishes the data foundation that every subsequent phase of the project will depend upon.

---

# Objectives

By the end of this phase, the project should have:

* A clear understanding of the business problem from a data perspective.
* A complete understanding of the dataset and business entities.
* A documented data dictionary describing every feature.
* A validated dataset with identified quality issues.
* A reproducible SQL-based data preparation pipeline.
* A clean analytical dataset ready for analytics and machine learning.
* Documentation explaining every transformation applied to the data.

---

## Data Understanding

* Explore the dataset.
* Identify all available tables or logical entities.
* Understand each feature.
* Classify numerical and categorical variables.
* Identify the prediction target.
* Understand relationships between customer information and business behavior.

---

## Database Design

* Relational databases
* Primary Keys
* Foreign Keys
* Table relationships
* Entity relationship thinking
* Database normalization (conceptual understanding)

---

## PostgreSQL

Store the project data inside PostgreSQL.

Practice:

* Database creation
* Table creation
* Data import
* Data exploration
* SQL querying

---

## SQL

Develop production-quality SQL skills including:

* SELECT
* WHERE
* ORDER BY
* GROUP BY
* HAVING
* CASE statements
* Aggregate functions
* JOINs
* Common Table Expressions (CTEs)
* Window Functions
* Views

Every query should answer a real business question instead of being written only for practice.

---

## Data Quality Assessment

Evaluate the reliability of the data.

Topics include:

* Missing values
* Duplicate records
* Invalid values
* Inconsistent categories
* Outlier detection
* Data completeness
* Data consistency
* Schema validation

Every identified issue should be documented before applying any fixes.

---

## Data Validation

Implement validation checks to ensure the analytical dataset is reliable.

Examples include:

* Primary key uniqueness
* Valid value ranges
* Required field validation
* Referential integrity
* Data type validation
* Business rule validation

---

## Data Dictionary

Create documentation describing every feature.

For each column document:

* Business meaning
* Data type
* Allowed values
* Missing value policy
* Whether the feature is available during prediction
* Potential business importance

---

## Feature Preparation

Before machine learning begins:

* Remove unnecessary columns.
* Identify possible data leakage.
* Standardize data formats.
* Prepare features for downstream analytics.

No feature engineering for model performance will occur in this phase. The goal is to prepare trustworthy input data.

---

## Reproducibility

All data preparation should be reproducible.

The project should ensure that anyone can regenerate the analytical dataset by rerunning the data preparation pipeline without manually editing files.

---

# Deliverables

At the end of Phase 1, the project should produce:

### Documentation

* Business Overview
* Data Source Documentation
* Data Dictionary
* Database Schema Documentation
* Data Quality Report
* Data Validation Report
* Data Preparation Documentation

### Database

* PostgreSQL database
* Clean relational tables
* SQL scripts
* Reusable database views

### Data Assets

* Raw dataset (unchanged)
* Validated dataset
* Analytical dataset

### Code

* SQL scripts
* Data loading scripts
* Data validation pipeline
* Data preparation pipeline

---

# Success Criteria

Phase 1 will be considered successful when:

* The business problem is clearly understood.
* Every feature is documented.
* Data quality issues have been identified and addressed appropriately.
* SQL scripts successfully recreate the analytical dataset.
* The analytical dataset is reproducible.
* The dataset is trusted for analytics and machine learning.
* No manual editing of raw data is required.

---

# Why This Phase Matters

Machine learning models are only as good as the data they are trained on. A reliable data foundation reduces errors, improves reproducibility, and enables analysts and machine learning engineers to focus on solving business problems instead of fixing inconsistent data.

This phase mirrors the initial work carried out in many production data science projects, where understanding, validating, and preparing data often consumes a significant portion of the overall project effort.

