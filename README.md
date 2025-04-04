# Telecom Churn Analysis - EDA & Visualization using Power BI

![Cover Image](design/Home.png)

## Overview
This project provides an end-to-end analysis of telecom customer churn and retention. It combines comprehensive Exploratory Data Analysis (EDA) and data cleaning performed in a Jupyter Notebook with interactive dashboards built in Power BI. The goal is to uncover key insights about customer behavior, identify churn drivers, and recommend actionable strategies to improve customer retention.

## Table of Contents
- [Introduction](#introduction)
- [Data Description](#data-description)
- [Tools & Technologies](#tools--technologies)
- [Project Structure](#project-structure)
- [EDA & Data Cleaning](#eda--data-cleaning)
- [Power BI Dashboard](#power-bi-dashboard)
- [Key Insights & Recommendations](#key-insights--recommendations)
- [How to Run](#how-to-run)
- [Contributing](#contributing)
- [Contributors](#contributors)
- [License](#license)

## Introduction
Telecom companies face significant challenges in retaining customers. This project analyzes a comprehensive telecom dataset to:
- Identify patterns and trends related to customer churn.
- Explore factors influencing customer retention.
- Provide interactive visualizations that empower stakeholders to make data-driven decisions.

## Data Description
The dataset comprises 38 columns and 7,043 entries, including key information such as:
- **Customer Demographics & Account Details:** `Customer ID`, `Gender`, `Age`, `Married`, `Number of Dependents`, `City`, `Zip Code`, etc.
- **Service Information:** `Phone Service`, `Internet Service`, `Internet Type`, `Multiple Lines`, `Avg Monthly Long Distance Charges`, `Monthly Charge`, `Total Charges`, etc.
- **Churn Information:** `Customer Status`, `Churn Category`, `Churn Reason`
- **Usage Metrics:** `Tenure in Months`, `Total Refunds`, `Total Extra Data Charges`, `Total Long Distance Charges`, `Total Revenue`, etc.

## Tools & Technologies
- **Python** (Pandas, Seaborn, Matplotlib) – for data cleaning and EDA.
- **Jupyter Notebook** – for exploratory analysis.
- **Power BI** – for interactive data visualization and dashboard creation.
- **SQL & Excel** – for initial data extraction and transformations (if applicable).

## Project Structure

## EDA & Data Cleaning
The Jupyter Notebook (`notebooks/Telecom_Churn_EDA.ipynb`) covers:
- **Data Preprocessing:** Cleaning missing values, correcting data types, and standardizing column names.
- **Exploratory Data Analysis:** Visualizing distributions (e.g., Age, Tenure in Months), examining relationships (e.g., Tenure vs. Customer Status, Internet Service impact on churn), and exploring key metrics.
- **Feature Engineering:** Creating useful groups (e.g., "Tenure Group") to better segment customer data.

Example visualizations include:
- Histograms and KDE plots for the **Age** distribution.
- Boxplots comparing **Tenure in Months** for different **Customer Status** values.
- Count plots for service types segmented by churn status.

## Power BI Dashboard
The Power BI dashboard provides interactive insights through multiple pages:
1. **Overview:** Displays key performance indicators such as Total Revenue, Total Refunds, Total Charges, Total Customers, Churn Rate, and Joined Rate.
2. **Churn Analysis:** Detailed visuals exploring churn drivers like contract type, monthly charges, customer tenure, and churn reasons.
3. **Retention Analysis:** Focuses on customer retention, highlighting retention rates across internet service types, contract types, and tenure groups.

## Key Insights & Recommendations
- **Churn Drivers:** Factors such as high monthly charges, specific contract types, and service dissatisfaction significantly drive customer churn.
- **Retention Strategies:** Higher retention rates are observed among customers with longer tenures and particular service types. Recommendations include targeted promotions, enhanced customer support, and loyalty programs.
- **Financial Impact:** Balancing churn and retention is critical for maintaining revenue, underscoring the need for proactive strategies in at-risk segments.

## How to Run
### Run the EDA:
1. Open the Jupyter Notebook (`notebooks/Telecom_Churn_EDA.ipynb`) using Jupyter Notebook or JupyterLab.
2. Execute the cells to explore data trends and insights.

### Explore the Dashboard:
1. Open the Power BI file (`powerbi/Telecom_Churn_Retention.pbix`) in Power BI Desktop.
2. Interact with the dashboard visuals to gain deeper insights into churn and retention patterns.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request with your suggestions and improvements.

## Contributors
- **[Abdulrahman Khalifa](https://www.linkedin.com/in/abdulrahman-m-khalifa/)**
- **[Mohamed Roshdy](https://www.linkedin.com/in/mohamedaroshdy/)**  

## License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
