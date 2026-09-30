# Zomato AI Data Engineering — End-to-End Project

An end-to-end data engineering project that builds a complete pipeline for processing Zomato-style food delivery data and turning it into analytics and AI-powered applications.

The project brings together cloud storage, data warehousing, transformation, orchestration, and Generative AI into a single workflow.

**Data Flow:**

Zomato/Food Delivery Dataset → Amazon S3 → Snowflake → dbt → Apache Airflow → AI Applications

---

## 📌 Project Overview

This project demonstrates how raw food delivery data can be transformed into structured, analytics-ready datasets and then used for AI-powered applications.

The pipeline covers:

- Data ingestion and cloud storage with **Amazon S3**
- Data warehousing with **Snowflake**
- Data transformation and modeling with **dbt**
- Workflow orchestration with **Apache Airflow**
- Containerized services using **Docker**
- LLM-based review enrichment
- Retrieval-Augmented Generation (RAG)
- Natural-language-to-SQL querying
- Streamlit applications for interacting with the data

The project follows a medallion-style architecture:

**Bronze → Silver → Gold → AI**

---



### Pipeline

```text
                    Food Delivery Dataset
                             │
                             ▼
                       Amazon S3
                       Data Lake
                             │
                             ▼
                        Snowflake
                       RAW / Bronze
                             │
                             ▼
                          dbt
                      STAGING / Silver
                             │
                             ▼
                       dbt Models
                       MARTS / Gold
                             │
                             ▼
                     Apache Airflow
                      Orchestration
                             │
                             ▼
                       AI Layer
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
        Review Enrichment    RAG       Text-to-SQL
