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

## ⚙️ Technology Stack

<table>
  <tr>
    <th>Category</th>
    <th>Technologies</th>
  </tr>
  <tr>
    <td><strong>Programming</strong></td>
    <td>Python, SQL</td>
  </tr>
  <tr>
    <td><strong>Data Processing</strong></td>
    <td>Pandas</td>
  </tr>
  <tr>
    <td><strong>Cloud Storage</strong></td>
    <td>Amazon S3</td>
  </tr>
  <tr>
    <td><strong>Data Warehouse</strong></td>
    <td>Snowflake</td>
  </tr>
  <tr>
    <td><strong>Transformation</strong></td>
    <td>dbt / dbt-snowflake</td>
  </tr>
  <tr>
    <td><strong>Orchestration</strong></td>
    <td>Apache Airflow</td>
  </tr>
  <tr>
    <td><strong>Containers</strong></td>
    <td>Docker</td>
  </tr>
  <tr>
    <td><strong>AI / LLM</strong></td>
    <td>OpenAI</td>
  </tr>
  <tr>
    <td><strong>Embeddings</strong></td>
    <td><code>text-embedding-3-small</code></td>
  </tr>
  <tr>
    <td><strong>LLM</strong></td>
    <td><code>gpt-4o-mini</code></td>
  </tr>
  <tr>
    <td><strong>Application Layer</strong></td>
    <td>Streamlit</td>
  </tr>
  <tr>
    <td><strong>Version Control</strong></td>
    <td>Git / GitHub</td>
  </tr>
</table>

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
