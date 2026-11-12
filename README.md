# Roofing Company – Appointment Funnel Dashboard

A Power BI report that analyses a roofing company's appointment funnel – from appointment set, to confirmed, to sit (rep visits the customer), to sold – and shows where appointments are lost and which setters, reps, offices and lead sources perform best.

## Key numbers (no filters applied)

| Metric | Value |
|---|---|
| Total appointments (cleaned) | 11,741 |
| Confirmed | 7,378 (62.84%) |
| SITs | 4,947 (67.05% of confirmed) |
| Gross sold | 827 (16.72% close rate) |
| Net sold | 681 (13.77% net close rate) |

Data covers 23 Oct 2024 – 15 Nov 2025. 11,860 raw rows were cleaned to 11,741 (placeholder, test, undated, post-cutoff and duplicate rows removed).

## Report pages

1. **Executive Overview** – 8 KPI cards, funnel, weekly trend, office comparison
2. **Funnel & Bottleneck** – where appointments are lost between stages
3. **Setter Performance** – quality-adjusted setter ranking
4. **Sales Rep Performance** – rep results and assignment completeness
5. **Office & Channel** – Inside Sales vs Outreach vs other offices
6. **No-Shows & DaysOut** – no-show behaviour and the effect of booking lead time
7. **Lead Source & Vendor** – real-time (vendor) vs non-real-time leads
8. **Insights & Recommendations** – key findings and recommendations

## Repository structure

```
Roofing-Company/
├── powerbi/
│   └── Roofing_Company.pbix                      # Power BI report
├── data/
│   └── Roofing_Appoinments_Master_Table.xlsx     # Source appointments data
├── docs/
│   ├── Report_Answers_to_Requirements.docx       # How each page answers the brief
│   └── Report_Build_Guide.docx                   # Slicers, filters and charts page by page
├── README.md
└── .gitignore
```

## How to use

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows).
2. Download or clone this repository.
3. Open `powerbi/Roofing_Company.pbix`.
4. If prompted, update the data source path (Home → Transform data → Data source settings) to point to `data/Roofing_Appoinments_Master_Table.xlsx`.

## Documentation

- **Report_Answers_to_Requirements** – maps every requirement in the brief to the page and visual that answers it, with the logic and values.
- **Report_Build_Guide** – documents every slicer, filter and chart, and why it was used.

## Assumptions

Where the brief was open to interpretation, the documents mark items as `ASSUMPTION` or `BUSINESS CLARIFICATION REQUIRED` (for example how Net Sold is defined and whether no-shows stay in the SIT rate denominator).

## Tools

Power BI (DAX, Power Query) · Excel

## Author

Karan Agarwal – [GitHub](https://github.com/Karanagarwal03)
