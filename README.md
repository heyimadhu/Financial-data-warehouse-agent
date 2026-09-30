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


## 🔄 Data Engineering Pipeline

<table>
  <tr>
    <th>Stage</th>
    <th>Technology</th>
    <th>Purpose</th>
  </tr>
  <tr>
    <td><strong>1. Data Source</strong></td>
    <td>CSV / Zomato Dataset</td>
    <td>Raw restaurant, customer, food, order, and review data</td>
  </tr>
  <tr>
    <td><strong>2. Data Lake</strong></td>
    <td>Amazon S3</td>
    <td>Store raw datasets in the cloud</td>
  </tr>
  <tr>
    <td><strong>3. Data Warehouse</strong></td>
    <td>Snowflake</td>
    <td>Load and store structured raw data</td>
  </tr>
  <tr>
    <td><strong>4. Transformation</strong></td>
    <td>dbt</td>
    <td>Clean, transform, test, and model the data</td>
  </tr>
  <tr>
    <td><strong>5. Data Modeling</strong></td>
    <td>dbt</td>
    <td>Build dimensions, facts, and analytical marts</td>
  </tr>
  <tr>
    <td><strong>6. Orchestration</strong></td>
    <td>Apache Airflow</td>
    <td>Automate and schedule the complete pipeline</td>
  </tr>
  <tr>
    <td><strong>7. AI Processing</strong></td>
    <td>OpenAI</td>
    <td>Review enrichment, RAG, and text-to-SQL</td>
  </tr>
  <tr>
    <td><strong>8. Applications</strong></td>
    <td>Streamlit</td>
    <td>Provide interactive AI and data exploration interfaces</td>
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
