# Njiwa Water Project

A **Power BI** project that analyses a water improvement programme across five provinces (Banjira, Kabara, Dunama, Kandara, and Zarawa). It shows how many people have access to basic water, how projects are progressing, and how much money has been spent.

<img width="1607" height="955" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/9d8b38eb-12cc-4dd3-957c-92806b404b88" />
<img width="1528" height="956" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/6b632c05-8d84-4378-9d26-e35fb3c87ccc" />


## Project Goal

To turn raw water project data into a clear report that helps answer:

- How many people have access to basic water?
- How many projects are completed and how many are pending?
- How does the total cost compare with the budget?
- Which province and which improvement type cost the most?
- Which vendors finish projects faster and at a lower cost?

## Features

- 3-page interactive report with navigation buttons
- KPI cards for population, water access, and project status
- Filled map showing project completion by province
- Cost breakdown by province and by improvement type
- Cost vs budget gauge
- Vendor comparison by project duration and average cost
- Key Influencers visual to find what increases project cost
- Slicers for improvement type, water source, location type (Rural or Urban), and completion date

## Key Numbers

| Measure | Value |
|---------|-------|
| Total Population | 28M |
| Population with Basic Water | 13M |
| % Population with Basic Water | 47.83% |
| Uncompleted Projects | 20K |
| Completed Projects | 21.61% |
| Total Cost | 33.79M |
| Budget | 30.52M |

## Report Pages

**1. Dashboard:** the home page with KPI cards, a project completion map, cost by province, cost by improvement, and cost vs budget.

**2. Cost Dashboard:** detailed cost analysis. *(Add a short description of your visuals here.)*

**3. Report Dashboard:** detailed analysis with vendor tables, improvements by province, a Key Influencers visual, a scatter plot of completed projects vs average cost, and filters.

## Data Cleaning

Done in Power Query:

- Set the correct data types
- Removed blank rows and unused columns
- Trimmed extra spaces and converted text to lowercase
- Replaced wrong or inconsistent values

<img width="1920" height="991" alt="Screenshot (97)" src="https://github.com/user-attachments/assets/1f385021-d440-40c6-98a2-70f549721336" />

## Data Model

The model has **8 tables** connected by **6 relationships**, with `water_source` at the centre.

<img width="1920" height="958" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/3efd19f3-cb5b-4e71-b7d8-2d33d5bee960" />


| Table | Contains |
|-------|----------|
| project_progress | Projects, costs, dates, duration, and improvements |
| water_source | Source type, people served, and queue time |
| location | Province, town, and location type |
| visits | Visit count and time in queue |
| vendors | Company name, type, and owner |
| infrastructure_cost | Cost of each improvement |
| well_pollution | Water quality results |
| Measures Table | All DAX measures |


## Tools Used

| Tool | Use |
|------|-----|
| Power BI Desktop | Building the report |
| Power Query | Cleaning the data |
| DAX | Creating measures |

## How to Run

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows only).
2. Clone or download this repository:
   ```bash
   git clone https://github.com/abinanthan1/Water-Project.git
   ```
3. Open `Water Project.pbix`.
4. Click **Refresh** if the data does not load. If the file path breaks, update it in **Home > Transform data > Data source settings**.

## Main Findings

- Only **47.83%** of the population has basic water access.
- **Install RO filter** is the most common improvement (1,082 completed) and the costliest (14.3M).
- **Kabara** has the most improvements (4,033).
- **Banjira** has the largest share of total cost (about 33%).
- Total cost (33.79M) is above the budget (30.52M).
- Projects with more taps nearby have a higher budgeted cost.
- The correlation between completed projects and average cost by province is **0.59**, a moderate positive link.

## Future Improvements

- Add a water quality and pollution page
- Add a vendor ranking page
- Publish the report to Power BI Service
- Add a mobile layout

## Author

**Abinanthan**
GitHub: [abinanthan1](https://github.com/abinanthan1)

## License

This project is free to use for learning purposes.
