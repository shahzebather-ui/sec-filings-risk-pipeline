# sec-filings-risk-pipeline
Python pipeline for extracting and structuring risk and vulnerability disclosures from SEC EDGAR filings across large public companies.

# SEC Filings Risk Pipeline (EDGAR)

## Overview
This project implements a Python-based pipeline to extract, clean, and structure risk and vulnerability disclosures from SEC EDGAR filings across large public companies. The workflow focuses on parsing unstructured regulatory text and preparing analysis-ready datasets for downstream research and modeling.

## Scope
The pipeline targets key disclosure sections including:
- Item 1A: Risk Factors
- Item 1C: Cybersecurity

The analysis was conducted across hundreds of large-cap public companies.

## Approach
- Ingest SEC EDGAR filings in HTML/XBRL format
- Parse and normalize relevant disclosure sections
- Clean and standardize unstructured text outputs
- Process filings in controlled batches (20–50 filings per run) to improve runtime stability and enable execution at scale

## Implementation Notes
The original research codebase was adapted and extended to support batching, improved preprocessing logic, and more reliable large-scale execution. Batch-based processing was introduced after full-scale runs across all companies proved unstable.

## Tools
Python, Pandas, BeautifulSoup / lxml, regex, Jupyter

## Data Notes
SEC filings are sourced from the public EDGAR system. Raw filings and extracted datasets are not included in this repository due to size and storage constraints.
