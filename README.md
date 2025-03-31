# Insider Threat Detection 🔍

## Overview

This project aims to identify potential insider threats within an organization by analyzing employee activity data, including file access, email behavior, login patterns, and role assignments. Through detailed investigation and data analysis, I uncovered usr-zvn as a likely insider threat based on suspicious patterns. Additionally, the repository includes Python code to analyze login and logoff patterns for Finance staff in January, visualized with bar charts.

The journey began with a broad goal: detect anomalous behavior among employees. After diving into the data, the evidence pointed to usr-zvn as the primary suspect.

## Project Structure

* **Insider_Threat_Detection.ipynb**: Jupyter notebook with the code for data analysis and visualization.
* **Data Files**:
    * email_data.csv: Email activity logs.
    * file_data.csv: File access logs.
    * web_data.csv: Web activity logs.
    * login_data.csv: Login and logoff logs.
    * usb_data.csv: USB activity logs.
    * employee_data.csv: Employee role assignments.
* **README.md**: This file, outlining the project and findings.

## The Investigation 🎯
Initially, the task was to sift through employee data to spot potential insider threats. I analyzed various datasets—file access, emails, logins, and roles—looking for anomalies. Here’s how I pinpointed usr-zvn as the insider:

#### Key Discoveries
* **Excessive File Access**: usr-zvn accessed /docs/clients 3,716 times in a year—way more than any other employee. This raised a red flag about possible misuse.
* **Dual Roles**: Unlike others, usr-zvn was registered in both Finance and Security roles, granting unusual privileges that could be exploited.
* **Suspicious Emails**: They sent 116 emails to themselves, an odd pattern hinting at data exfiltration.
* **Login Anomalies**: While most staff logged in between 7-9 AM and off between 5-6 PM, usr-zvn’s patterns seemed off (further login analysis could confirm this).

## Data Analysis 📊

The notebook includes:

1. **Data Loading**: Imports CSV files into pandas DataFrames with datetime parsing.
2. **Finance Staff Login Analysis**:
    * Filters login data for Finance staff in January.
    * Visualizes login/logoff distributions by hour.
    * Identifies peak login and logoff times.
    * Node Graph to see the connections of users.
3. **Insider Threat Detection:** Custom analysis that led to identifying usr-zvn.

**Visualization**

![alt text](Images\image.png)

![alt text](Images\image-1.png)

![alt text](Images\image-2.png)

![alt text](Images\image-3.png)

![alt text](Images\image-4.png)


## Conclusion
After piecing together these clues, the evidence strongly suggests usr-zvn is an insider threat. The combination of excessive access, dual roles, and self-emailing paints a picture of deliberate misuse—confirmed through my analysis.

## Setup Instructions
**Prerequisites**
* Python 3.x
* Libraries: pandas, matplotlib, seaborn, warnings

Install dependencies:
``` 
pip install pandas matplotlib seaborn
```

**Running the Analysis**
1. Clone the repo:
```
git clone https://github.com/fiftybucks101/Insider_Threat_Detection.git
cd Insider_Threat_Detection
```
2. Place the data files in the same directory as the notebook.
3. Open the notebook
```
jupyter notebook Insider_Threat_Detection.ipynb
```
4. Run all cells to explore the data and see the visualizations


