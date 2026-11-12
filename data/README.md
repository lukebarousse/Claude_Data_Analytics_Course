# 🗃️ Course Data

Job postings for Data Analyst, Data Engineer and Data Scientist roles, July 2025 to June 2026, as a star schema.

| Table | Rows | One row is |
|---|---|---|
| `job_postings_fact` | 491,140 | a job posting |
| `company_dim` | 65,970 | a company |
| `skills_dim` | 960 | a skill |
| `skills_job_dim` | 3,159,600 | a skill listed on a posting |

## Option 1: Download the file

**[data_jobs.duckdb](https://github.com/lukebarousse/Claude_Data_Analytics_Course/releases/download/data-v1/data_jobs.duckdb)** (44.3 MB, DuckDB database), from the [`data-v1` release](https://github.com/lukebarousse/Claude_Data_Analytics_Course/releases/tag/data-v1).

You can also paste this link into a Claude chat and ask Claude to download the file and open it:

```
https://github.com/lukebarousse/Claude_Data_Analytics_Course/releases/download/data-v1/data_jobs.duckdb
```

## Option 2: Query it in BigQuery

<!-- TODO: public BigQuery dataset name + sandbox setup steps -->
