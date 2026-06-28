# Data Analyst Portfolio

Junior data analyst in training. Documenting my learning path and projects in SQL, Python, and data visualization.

---

## Skills in Progress

- SQL (Intermediate → Advanced) — joins, aggregation, schema design
- Python (pandas, data manipulation)
- Data Visualization (Power BI, Recharts)
- Relational databases (PostgreSQL, row-level security)
- Statistics for Data Analysis

---

## Projects

| Project | Tools | Description |
|---------|-------|-------------|
| [Life-OS Dashboard](https://github.com/ridhouta/life-os) | PostgreSQL · Supabase · Next.js · Recharts · Vercel | Full-stack personal analytics dashboard. Designed a normalized Postgres schema with row-level security, wrote the aggregation queries behind every chart, and deployed it to production. Debugged real schema and auth issues along the way. |
| [Mental Health of International Students](./01-mental-health-sql/) | PostgreSQL | Analyzing how length of stay affects depression, social connectedness, and acculturative stress in international students. |

---

## Featured: Life-OS Dashboard

A personal analytics dashboard I built to track health, study, productivity, and finances in one place — and to practice working with a real relational database end to end.

**Live demo:** https://life-os-puce-tau.vercel.app
**Code:** https://github.com/ridhouta/life-os

What it demonstrates for data work specifically:

- **Schema design** — a normalized PostgreSQL schema across ~13 tables (daily logs, tasks, workouts, study sessions, budget transactions, savings, funds), each scoped to a user.
- **Access control** — row-level security policies (`auth.uid() = user_id`) so every query is automatically filtered to the right user at the database level.
- **Aggregation** — the trend charts (mood over time, study minutes per day, income vs expense per month, expenses by category) are driven by grouped SQL aggregations, not hardcoded data.
- **Debugging with real signals** — diagnosed a silent write failure by reading server logs and tracing a PostgreSQL error code (`42703`, column does not exist) back to a schema/code column-name mismatch.

This project was built with AI-assisted development (Claude Code). I made all the architecture and product decisions — the data model, the success/failure logic, the feature set — and worked through every bug and the full deployment myself.

---

## About

International Relations student at Kazan Federal University transitioning into data analytics. Currently completing DataCamp's Data Analyst track, with a focus on SQL and PostgreSQL.

- GitHub: [ridhouta](https://github.com/ridhouta)
