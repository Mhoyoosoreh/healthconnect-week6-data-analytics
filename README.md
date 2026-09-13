# HealthConnect Week 6 – Advanced Analytics & Decision Support

**AnalystLab Africa – Week 6 Experience Lab**  
**Track:** Data Analytics  
**Project:** HealthConnect Clinic

## Project Overview

This project continues the HealthConnect Clinic analytics work developed during Week 5.

Week 6 focuses on moving from initial analysis and dashboard development into **advanced analytics, KPI validation, decision support, dashboard improvement, and cross-track integration**.

The overall project question is:

> **How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?**

Week 6 builds on the validated Week 5 findings while introducing deeper segment analysis, relationship analysis, KPI validation, refined conclusions, and collaboration with the Data Science track.

---

## Week 6 Objectives

The main objectives of this project were to:

- Investigate the most important findings from Week 5 in greater depth.
- Validate whether key findings remain meaningful.
- Analyse patterns across relevant appointment and patient segments.
- Investigate relationships that may help explain no-show behaviour.
- Validate the KPIs developed during Week 5.
- Identify findings with the greatest potential business impact.
- Translate analytical findings into practical HealthConnect actions.
- Provide validated analytical evidence to the Data Science track.
- Review and refine the Week 5 conclusions.
- Improve the existing Power BI dashboard.
- Document evidence supporting recommendations and cross-track integration.
- Prepare analytical requirements for Week 7 testing and refinement.

---

## Key Week 6 Findings

### 1. Booking Lead Time and No-Show Behaviour

Booking lead time remained one of the strongest patterns identified in the analysis.

| Booking Lead Group | No-Show Rate |
|---|---:|
| 0–9 days | 29.01% |
| 10–19 days | 37.11% |
| 20–29 days | 44.44% |
| 30–39 days | 50.53% |
| 40–49 days | 61.62% |
| 50–59 days | 67.92% |
| 60+ days | 68.09% |

The results show a clear increase in no-show rates as the time between booking and appointment becomes longer.

The 60+ day group contains relatively few appointments and should therefore be interpreted cautiously.

---

### 2. Previous No-Show History

Previous no-show behaviour was also strongly associated with future no-shows.

| Previous No-Shows | No-Show Rate |
|---|---:|
| 0 | 43.51% |
| 1 | 53.49% |
| 2 | 59.36% |
| 3 | 67.95% |
| 4 | 66.67% |
| 5 | 100.00% |

The main pattern is an increase in future no-show rates as previous no-show history increases.

The groups with four and five previous no-shows are very small and should not be treated as stable population-level estimates.

---

### 3. Reminder Status

Appointments with reminders had a lower observed no-show rate than appointments without reminders.

| Reminder Sent | No-Show Rate |
|---|---:|
| No | 51.39% |
| Yes | 47.36% |

This represents a **4.03 percentage-point difference**.

The finding indicates an association between reminder status and lower no-show rates, but it does not establish that reminders directly caused the reduction.

---

## Advanced Segment and Relationship Analysis

Week 6 expanded the analysis by examining how important factors interact.

Key areas investigated included:

- Booking lead time × appointment type
- Previous no-shows × appointment type
- Reminder status × appointment type
- Booking lead time × previous no-shows
- Reminder status × previous no-shows
- Booking lead time × reminder status

The analysis showed that the relationship between booking lead time and no-shows generally persisted across appointment types.

It also showed that previous no-show history can compound the risk associated with longer booking lead times.

These interactions provide more useful decision-support information than examining each factor independently.

---

## KPI Validation

The main Week 5 KPIs were rechecked during Week 6.

| KPI | Validated Result |
|---|---:|
| Total Appointments | 5,000 |
| No-Show Rate | 48.46% |
| Attendance Rate | 46.28% |
| Cancellation Rate | 5.26% |
| Reminder No-Show Gap | 4.03 percentage points |

The KPI calculations remained consistent after the additional Week 6 analysis.

---

## Cross-Track Integration

During Week 6, the Data Analytics track collaborated with the **Data Science track**.

Validated analytical findings were shared to support modelling decisions and interpretation.

The Data Science feedback provided additional confirmation that:

- Booking lead time was the strongest predictive feature in the model.
- Historical no-show behaviour was also an important predictive feature.
- The observed reminder relationship was consistent with the modelling/analysis results.
- Specialist Consultation had a higher model error rate, but this should not be confused with having the highest no-show rate.
- Appointment type interacts with booking lead time and previous behaviour and may be useful for further modelling during Week 7.

This integration helped connect the analytical findings with model interpretation and future feature-development decisions.

---

## Business Recommendations

Based on the validated findings, HealthConnect should consider:

1. **Strengthening support for long-lead appointments**
   - Apply stronger or earlier confirmation and reminder processes to appointments booked far in advance.

2. **Targeting patients with previous no-shows**
   - Provide additional confirmation or patient support for patients with a history of missed appointments.

3. **Maintaining and improving reminder coverage**
   - Continue using appointment reminders and evaluate their timing and effectiveness.

4. **Using combined risk factors**
   - Consider booking lead time together with previous no-show behaviour and appointment type rather than relying on a single variable.

5. **Further testing before operational deployment**
   - Validate these patterns through future modelling and testing before introducing automated interventions.

---

## Dashboard Improvements

The Week 6 dashboard was developed from the Week 5 dashboard rather than rebuilt from scratch.

Improvements included:

- Refinement of key analytical visuals.
- Greater emphasis on booking lead time and previous no-show behaviour.
- Continued analysis of reminder impact.
- Addition of the **Reminder No-Show Gap – 4.03 pp** KPI.
- Preservation of the Week 5 dashboard as the original version.
- Improved decision-support focus for Week 6.

---

## Data Limitations and Risks

Important limitations considered during Week 6 include:

- Small sample sizes in some higher-risk groups.
- Unstable percentages in very small segments.
- Observational data cannot establish causation.
- Some potentially important behavioural or operational factors may not be available in the dataset.
- Model predictions include an uncertainty zone that requires further testing.
- Interactions between appointment type, booking lead time and previous behaviour require additional validation.
- Analytical findings should be interpreted alongside modelling and testing results.

---

## Week 7 Analytical Focus

The Week 6 findings provide a foundation for Week 7 testing and refinement.

Planned areas include:

- Testing the stability of important analytical relationships.
- Further investigation of appointment type × booking lead time interactions.
- Testing the usefulness of combined risk factors.
- Monitoring model uncertainty and error patterns.
- Validating analytical recommendations.
- Supporting further model and solution refinement.

---

## Repository Structure

```text
healthconnect-week6-data-analytics/
│
├── README.md
│
├── Dashboard/
│   └── HealthConnect_Week6_Analytics.pbix
│
├── Documentation/
│   ├── Week6_Advanced_Analytics_Decision_Support_Report.docx
│   ├── Week6_Project_Summary.docx
│   └── Cross_Track_Integration_Evidence.docx
│
└── Images/
    └── HealthConnect_Week6_Dashboard.png
