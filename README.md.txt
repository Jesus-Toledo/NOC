# NOC Performance Analytics

**Network Operations Center | Data Analytics Case Study | 2025–2026**

An end-to-end data analytics project focused on ticket management, operational performance, resolution time, and SLA compliance using Databricks SQL and Microsoft Power BI.

## Project Overview

Network Operations Centers (NOCs) manage large volumes of incidents and service requests. Monitoring ticket volume, resolution time, and Service Level Agreement (SLA) compliance helps operations teams identify performance issues and prioritize investigations.

This project transforms ticket-level data into an interactive Power BI dashboard to explore operational workload, resolution patterns, and SLA outcomes.

## Business Objectives

- Monitor overall ticket volume and ticket status.
- Analyze monthly ticket trends across 2025 and 2026.
- Compare workload by priority, region, equipment type, and incident category.
- Evaluate average resolution time (MTTR).
- Analyze reported SLA compliance and identify areas requiring further investigation.
- Present actionable findings through interactive visualizations.

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Databricks SQL | Source data exploration and SQL analysis |
| Power Query | Data inspection and preparation |
| Microsoft Power BI | Data modeling and interactive dashboards |
| DAX | KPI calculations and business measures |
| Git & GitHub | Version control and project documentation |

## Data Sources & Model

The project uses two main tables from Databricks:

- **tickets:** ticket identifiers, creation and closure dates, status, priority, incident category, region, city, and resolution time.
- **equipos:** equipment identifiers, equipment type, model, region, and installation date.

The Power BI data model connects tickets to equipment through `equipo_id`, allowing ticket analysis by equipment attributes.

The report includes data-quality considerations such as missing resolution times, missing closure dates, and tickets without a matching equipment record.

## Dashboard Pages

### 1. Executive Overview

Provides a high-level summary of operational performance through KPI cards, monthly ticket trends, ticket status distribution, ticket volume by priority, and the reported SLA compliance rate.

**Key metrics:**
- Total Tickets
- Average Resolution Time
- Closed Tickets
- Open Tickets
- In-Progress Tickets
- SLA Compliance Rate

<!-- Replace the filename below with your actual screenshot filename. -->
![Executive Overview Dashboard](screenshots/executive-overview.png)

### 2. Operational Performance

Explores ticket distribution and workload across incident categories, equipment types, regions, priorities, and days of the week.

The page also includes a monthly ticket volume matrix by priority and average resolution time comparisons.

![Operational Performance Dashboard](screenshots/operational-performance.png)

### 3. SLA & Resolution Analysis

Focuses on SLA status, resolution-time intervals, ticket status by priority, and monthly ticket activity compared with tickets containing closure dates.

This page helps identify patterns that require further investigation into service performance.

![SLA and Resolution Dashboard](screenshots/sla-resolution.png)

## Key Findings

The current analysis produced the following results:

| Metric | Result |
|---|---:|
| Total tickets | 10,020 |
| Average resolution time | 22.25 hours |
| Closed tickets | 7,267 |
| Open tickets | 971 |
| In-progress tickets | 1,782 |
| Reported SLA compliance | 17.64% |

Additional observations:

- **Backlog:** 2,753 tickets are open or in progress and warrant monitoring.
- **Resolution time:** 5,318 tickets fall into the intervals above 12 hours, according to the current resolution-time classification.
- **Incident categories:** Connectivity and Intermittency account for 4,487 tickets combined.
- **Weekly workload:** Friday has the highest displayed ticket volume, while Tuesday has the lowest.
- **Data coverage:** August 2026 is incomplete, with records available only through August 14.

## Business Recommendations

Based on the current findings, the following actions are recommended:

1. Validate SLA definitions and targets by priority.
2. Investigate SLA breaches by priority, incident category, region, and equipment type.
3. Review the age and ownership of open and in-progress tickets.
4. Examine recurring Connectivity and Intermittency incidents.
5. Compare monthly trends using equivalent date ranges to account for incomplete periods.

These recommendations are investigation priorities, not confirmed root causes.

## Methodology

The project follows an end-to-end analytics workflow:

1. Explore source data using Databricks SQL.
2. Inspect data quality, column types, and missing values in Power Query.
3. Build the Power BI data model and establish table relationships.
4. Create DAX measures for KPIs and operational metrics.
5. Design interactive dashboard pages for executive and operational analysis.
6. Interpret results and document business recommendations.

## Limitations

- August 2026 represents a partial month.
- Missing resolution times cannot be treated as zero.
- The reported SLA compliance rate is calculated over tickets classified as compliant or breached in the current model, rather than all tickets.
- The analysis identifies patterns but does not establish the root causes of SLA breaches.
- Equipment-based findings should account for tickets without a matching equipment record.

## Conclusion

NOC Performance Analytics demonstrates how SQL, data preparation, data modeling, and business intelligence can be combined to transform operational ticket data into actionable insights.

The dashboard provides visibility into ticket demand, backlog, resolution performance, and SLA outcomes. The findings highlight areas for further investigation and demonstrate an end-to-end data analytics workflow using Databricks SQL and Power BI.

## Author

**Jesús Toledo**  
Systems Engineering | Data Analytics | Business Intelligence

