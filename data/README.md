# 🗃️ Course Data

Job postings for Data Analyst, Data Engineer and Data Scientist roles, July 2025 to June 2026, as a star schema.

Short link to this page: **[lukeb.co/claude-data-files](https://lukeb.co/claude-data-files)**

| Table | Rows | One row is |
|---|---|---|
| `job_postings_fact` | 491,140 | a job posting |
| `company_dim` | 65,970 | a company |
| `skills_dim` | 960 | a skill |
| `skills_job_dim` | 3,159,600 | a skill listed on a posting |

## Option 1: Download the file

**[data_jobs.duckdb](https://github.com/lukebarousse/Claude_Data_Analytics_Course/releases/download/data-v1/data_jobs.duckdb)** (47.5 MB, DuckDB database), from the [`data-v1` release](https://github.com/lukebarousse/Claude_Data_Analytics_Course/releases/tag/data-v1).

> The file opens in DuckDB 1.0 or newer.

You can also ask Claude to download it. The short link points to the same file:

```
Download this database and list its tables with row counts: lukeb.co/claude-data-jobs
```

> Claude Code downloads it. In a Claude chat, Claude's network access can block the download. If it does, allow `lukeb.co`, `github.com` and `release-assets.githubusercontent.com` in your Claude settings, or use Option 2.

## Option 2: Query it in BigQuery

The same tables are in a public BigQuery dataset: **`datanerd-tech.course_claude`**. Any signed-in Google account can read it. Your queries run in your own project (a free BigQuery sandbox works), so you copy nothing.

```sql
SELECT COUNT(*) AS postings
FROM `datanerd-tech.course_claude.job_postings_fact`;
-- 491140
```

Every table and column has a description.

<!-- TODO: sandbox setup steps + Claude BigQuery connector steps -->

## Good to know

- `skills_dim`: Hugging Face, IBM Watson and Red Hat each have two `skill_id`s. To count jobs per skill, group by `skills` and use `COUNT(DISTINCT job_id)`.
- The data is a fixed snapshot. It does not update, so your numbers match the videos.
