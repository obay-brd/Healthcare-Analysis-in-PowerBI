# Healthcare Analysis Dashboard

## Project Overview

This project presents an interactive healthcare analytics dashboard developed in **Microsoft Power BI**. It analyzes hospital discharge activity, surgical-program volume, surgeon capacity, patient demographics, and selected performance indicators. The dashboard is designed to turn detailed healthcare records into clear insights that can support operational planning and evidence-based decision-making.

## Objectives

- Compare discharge volumes across hospitals and surgical programs.
- Evaluate the relationship between patient demand and surgeon capacity.
- Explore patient demographics, including age groups and other available characteristics.
- Identify high-volume hospitals, procedures, and areas of potential resource pressure.
- Provide users with interactive filters for focused analysis.

## Dashboard Features

- KPI cards summarizing total discharges, total surgeons, and other key measures.
- Hospital-level and surgical-program comparisons.
- Patient age-band categorization for demographic analysis.
- Interactive slicers and filters for exploring specific hospitals and patient groups.
- Custom DAX measures and calculated columns.
- A summarized hospital-level table created with `SUMMARIZECOLUMNS()`.

## Tools and Technologies

- **Power BI Desktop** — data modelling, analysis, and dashboard development
- **Power Query** — data cleaning and transformation
- **DAX** — calculated measures, columns, and summary tables
- **Microsoft Excel/CSV** — source-data storage, where applicable

## Data Preparation

The dataset was prepared in Power Query before being loaded into the data model. The preparation process included:

- Reviewing and correcting data types.
- Handling blank or inconsistent values.
- Renaming fields for readability.
- Creating categories such as patient age bands.
- Preparing hospital, discharge, and surgeon fields for analysis.

## Example DAX

The project uses DAX to create calculated fields and summary tables. For example:

```DAX
surgical_program_volume_summary =
SUMMARIZECOLUMNS(
    hospital_discharges[facility_name],
    "Total Discharges", [Total Discharges],
    "Total Surgeons", [Total Surgeons]
)
```

## Key Insights

> Replace the points below with findings from your final dashboard.

- **Highest discharge volume:** [Hospital or surgical program]
- **Largest surgeon capacity:** [Hospital or surgical program]
- **Most represented patient group:** [Age band or demographic group]
- **Operational finding:** [Brief explanation of an important pattern]

## Dashboard Preview

Add a screenshot of the completed dashboard to an `images` folder and update the path below:

```markdown
![Healthcare Analysis Dashboard](images/healthcare-dashboard.png)
```

## Repository Structure

```text
healthcare-analysis-power-bi/
├── README.md
├── Healthcare Analysis.pbix
├── data/
│   └── healthcare-data.csv
└── images/
    └── healthcare-dashboard.png
```

> Do not upload confidential, personally identifiable, or restricted patient information to GitHub. Use only public, anonymized, or permitted data.

## How to Use This Project

1. Download or clone this repository.
2. Open `Healthcare Analysis.pbix` in Power BI Desktop.
3. Update the data-source path if Power BI requests it.
4. Select **Refresh** to load the latest permitted data.
5. Use the dashboard slicers and visuals to explore the analysis.

## Future Improvements

- Add trend analysis when multiple reporting periods are available.
- Include additional measures for efficiency and patient outcomes.
- Add drill-through pages for hospital- and program-level details.
- Publish a sanitized version through Power BI Service for portfolio viewing.

## Author

**Obay Baradie**  
Economics and Management Science graduate with training in data analytics, predictive analytics, and business intelligence.

## Disclaimer

This project is intended for educational and portfolio purposes. The analysis should not be interpreted as medical advice or used as the sole basis for clinical decisions.


