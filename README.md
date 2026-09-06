# 📹 Global Video Trends: Scalable Multi-Country Data Engineering Pipeline

[![Language](https://img.shields.io/badge/Language-Python%203.10+-3776AB?style=flat&logo=python)](https://www.python.org/)
[![Engine](https://img.shields.io/badge/Engine-Pandas%20%7C%20Relational%20ETL-150458?logo=pandas)](https://pandas.pydata.org/)
[![Data](https://img.shields.io/badge/Dataset-Global%20YouTube%20Trending-red?logo=youtube)](#)

> High-performance data wrangling and relational schema harmonization on high-cardinality, multi-country video streaming datasets in Python & Pandas.

---

## 📌 Executive Summary

Raw streaming analytics data across multiple international territories is inherently messy: divergent category JSON mappings, malformed character encodings in unstructured tags, disabled interaction flags, and asynchronous publication timestamps.

This repository implements an end-to-end **computational data pipeline in Python and Pandas** that cleans, harmonizes, and queries massive multi-country YouTube trending datasets:
- Merges multi-territory tables while dynamically injecting country-level provenance metadata.
- Implements **temporal window clustering** to dissect publication timing patterns.
- Resolves complex relational joins between tabular metrics and international category metadata JSON files.
- Optimizes computational aggregations across high-cardinality multi-index groupings.

---

## 🔍 Analytical & Engineering Operations

### 1. Relational Normalization & Category Mapping
- Unifies distinct country-level tabular feeds into an integrated relational DataFrame.
- Resolves disparate category ID integers against multi-lingual JSON definition dictionaries, validating orphaned and non-assignable category codes.

### 2. High-Cardinality String & Tag Parsing
- Decomposes concatenated delimiter-separated tag strings without blowing up memory footprint.
- Computes global and country-specific tag frequencies and evaluates cross-territory tag virality.

### 3. Temporal Window Clustering
- Clusters publication timestamps into discrete **10-minute operational intervals**.
- Evaluates average view count, like/dislike ratios, and comment velocity per time bucket to isolate optimal global distribution windows.

### 4. Error-State Partitioning & Anomaly Isolation
- Identifies and partitions disabled feedback records (`comments_disabled`, `ratings_disabled`, `video_error_or_removed`) into dedicated anomaly DataFrames for diagnostic tracing.

---

## 💻 Notebook Architecture

- **`FCS Project.ipynb`**: Complete, self-contained interactive Python pipeline featuring structured code chunks, execution timing, and detailed markdown rationale for every transformation step.

---

**Author:** Francesco Colombini  
[GitHub Profile](https://github.com/FRA-0023) · [LinkedIn](https://www.linkedin.com/in/francescocolombini/)