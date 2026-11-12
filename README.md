<div align="center">

# 🏠 Roofing Appointment Funnel Dashboard

### From booked to sold: see exactly where roofing leads are lost, and who closes them.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-1F3A5F?style=for-the-badge)
![Pages](https://img.shields.io/badge/Report%20Pages-8-E8743B?style=for-the-badge)
![Rows](https://img.shields.io/badge/Appointments-11%2C741-2A9D8F?style=for-the-badge)

</div>

---

## 📌 Overview

A Power BI report that analyses a roofing company's appointment funnel (**Appointment set → Confirmed → SIT → Sold**) across **11,741 cleaned appointments** (23 Oct 2024 – 15 Nov 2025). It shows where appointments drop off, how no-shows and booking lead time hurt results, and which setters, sales reps, offices and lead sources perform best.

![KPI cards](https://raw.githubusercontent.com/Karanagarwal03/Roofing-Company/main/images/kpi_cards.png)

## 🔻 The Funnel

Only about **1 in 17** appointments ends in a net sale. Most of the loss happens before the rep even arrives.

![Appointment funnel](https://raw.githubusercontent.com/Karanagarwal03/Roofing-Company/main/images/funnel.png)

## 🏢 Inside Sales vs Outreach

Inside Sales brings volume and better confirmation. Outreach confirms less but closes better once the rep sits down.

![Office comparison](https://raw.githubusercontent.com/Karanagarwal03/Roofing-Company/main/images/office_comparison.png)

> Charts above are drawn from the values shown in the report with no slicers applied. See the [Build Guide](docs/Report_Build_Guide.docx) for the exact figures behind each visual.

---

## 📊 Report Pages

| # | Page | What it answers |
|---|------|-----------------|
| 1 | **Executive Overview** | 8 KPI cards, funnel, weekly trend, office comparison |
| 2 | **Funnel & Bottleneck** | Where appointments are lost between stages |
| 3 | **Setter Performance** | Quality-adjusted setter ranking, not just volume |
| 4 | **Sales Rep Performance** | Rep results and assignment completeness |
| 5 | **Office & Channel** | Inside Sales vs Outreach vs Solar vs Self Gen |
| 6 | **No-Shows & DaysOut** | No-show behaviour and the effect of booking lead time |
| 7 | **Lead Source & Vendor** | Real-time (vendor) vs non-real-time leads |
| 8 | **Insights & Recommendations** | Key findings and what to do next |

Every page has six slicers (Date, Office, Setter, SalesRep, LeadType, DaysOutBucket) and a **Reset Filter** button.

## 🔍 Key Insights

- **Customer no-shows:** 933 appointments (12.65%), a large avoidable leak after confirmation.
- **Confirmation gap:** Inside Sales confirms 67.5% of appointments vs 50.8% for Outreach.
- **Close quality:** Outreach net close rate (16.7%) beats Inside Sales (12.9%).
- **Not comparable:** Solar Appts have no Dispo recorded and Self Gen only holds appointments that already became visits, so both are labelled and excluded from rate comparisons.

## 🧹 Data Cleaning

11,860 raw rows were reduced to **11,741** by removing:

| Removed | Rows |
|---|---|
| Duplicate entries | 47 |
| Booked after the 15 Nov 2025 extract cutoff | 34 |
| Placeholder rows | 20 |
| Test rows | 10 |
| Rows with no Appt Day | 8 |

## 🗂️ Repository Structure

```
Roofing-Company/
├── powerbi/
│   └── Roofing_Company.pbix                      # Power BI report (8 pages)
├── data/
│   └── Roofing_Appoinments_Master_Table.xlsx     # Source appointments data
├── docs/
│   ├── Report_Answers_to_Requirements.docx       # How each page answers the brief
│   └── Report_Build_Guide.docx                   # Every slicer, filter and chart explained
├── images/                                       # Charts used in this README
├── README.md
└── .gitignore
```

## 🚀 How to Use

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows).
2. Download or clone this repository.
3. Open `powerbi/Roofing_Company.pbix`.
4. If prompted, point the data source to `data/Roofing_Appoinments_Master_Table.xlsx` (Home → Transform data → Data source settings).

## 📚 Documentation

- 📄 [**Report Answers to Requirements**](docs/Report_Answers_to_Requirements.docx): maps every requirement in the brief to the page and visual that answers it, with the logic and values.
- 📄 [**Report Build Guide**](docs/Report_Build_Guide.docx): documents every slicer, filter and chart, and why it was used.

## ⚠️ Assumptions

Where the brief was open to interpretation, the documents tag items as `ASSUMPTION` or `BUSINESS CLARIFICATION REQUIRED`, for example:

- **Net Sold** is read as `Sold` only (cancelled sales removed), and **Gross Sold** as `Sold + Sold Then Canceled`.
- No-shows stay in the **SIT rate** denominator (`SIT Rate = SITs / Confirmed`) so the problem is not hidden.

## 🛠️ Tools

Power BI · DAX · Power Query · Excel

## 👤 Author

**Karan Agarwal**: [GitHub](https://github.com/Karanagarwal03)

---

<div align="center">⭐ If you found this useful, give the repo a star!</div>

