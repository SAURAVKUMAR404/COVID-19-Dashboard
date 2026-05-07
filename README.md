# 🦠 COVID-19 Global Analysis Dashboard

A comprehensive COVID-19 data analysis dashboard built using Microsoft Excel and Power BI, analyzing global cases, deaths, vaccinations, and economic impact from 2020 to 2023.

---

## 📊 Dashboard Pages

| Page | Description |
|---|---|
| Global Dashboard | Overview of global cases, deaths, vaccinations and death rate |
| Country Analysis | Deep dive into individual country statistics |
| Vaccination Tracker | Global vaccination progress and distribution |
| Economic Analysis | Impact of GDP, HDI and population on COVID outcomes |

---

##  Key Insights

-  771 Million total confirmed cases worldwide
-  7 Million total deaths globally
-  6 Billion* vaccine doses administered
-  0.90% global death rate
-  Asia led the world in total vaccinations
-  Richer countries had significantly lower death rates
-  USA had the highest total cases despite not having the largest population

---

##  Dataset

| Detail | Info |
|---|---|
| Source | Our World in Data (OWID) |
| Link | [OWID COVID-19 Dataset](https://github.com/owid/covid-19-data) |
| Coverage | Global — 200+ countries |
| Date Range | January 2020 — December 2023 |
| Rows | 350,000+ |
| Columns | 24 key columns |

---

##  Tools Used

- Microsoft Excel — Data cleaning, filtering and preparation
- Power BI Desktop — Dashboard building and visualization
- DAX — Custom measures and calculations
- Power Query — Data transformation and type fixing

---

## 📁 Project Files

| File | Description |
|---|---|
| `COVID_Dashboard.pbix` | Power BI project file |
| `COVID_Dashboard.pdf` | PDF export of dashboard |
| `COVID_Dashboard_Data.xlsx` | Cleaned Excel dataset |
| `README.md` | Project documentation |

---

## DAX Measures Used

```dax
Total Cases = 
CALCULATE(
    SUMX(VALUES(covid_data[location]),
    CALCULATE(MAX(covid_data[total_cases]))),
    FILTER(covid_data, LEFT(covid_data[iso_code], 4) <> "OWID")
)

Total Deaths = 
CALCULATE(
    SUMX(VALUES(covid_data[location]),
    CALCULATE(MAX(covid_data[total_deaths]))),
    FILTER(covid_data, LEFT(covid_data[iso_code], 4) <> "OWID")
)

Death Rate % = DIVIDE([Total Deaths], [Total Cases]) * 100
```

---

##  How to Use

1. Download the `COVID_Dashboard.pbix` file
2. Open it in **Power BI Desktop** (free download from Microsoft)
3. Use the slicers to filter by country, continent or year
4. Navigate between pages using the tabs at the bottom

---

## Author

Saurav Kumar
- saurav91991.sks91@gmail.com
- SVCET Chittoor

---

## License

This project is licensed under the MIT License.

---

##  Acknowledgements

- [Our World in Data](https://ourworldindata.org/) for providing the dataset
- [Microsoft Power BI](https://powerbi.microsoft.com/) for the visualization tool
