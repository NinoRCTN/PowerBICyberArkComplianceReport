# PowerBICyberArkComplianceReport
Display CyberArk Compliance Report in Power BI Chart


# First Run
Create a new directory (for example C:\CyberArkComplianceReport), save "CyberArk Compliance Report.pbix" and example Compliance Report "ComplianceReport.xlsx".
Run Power BI, open file "CyberArk Compliance Report.pbix", and from "Transform Data > Data source settings" set Data Source to point "ComplianceReport.xlsx".


# Import CyberArk Compliance Report
From CyberArk PVWA generate a new Compliance Report and download. Open Compliance Report file and save as "ComplianceReport.xlsx" in the data directory.
From Power BI use "Refresh" button to reload Data


# Data
Two data table are used for create the Chart
- Period: represents a set of days within which the password change is expected (7, 15, 30, 60, 90).
- Report: represents the Compliance Report imported from CyberArk PVWA


# Filter
A series of filters are applied to shape the result according to specific needs (for example remove Platform with non password change).
From "Transform Data" it's possible to change the filter settings:
- Removing_Safes (for example "Vaultinternal", "PSM")
- Removing_Platforms (for example "Oracle Database")


# Page
Main page includes two Pie charts and one Donut chart
- Compliance Status: this is the main graph as it represents the real situation of the accounts managed in CyberArk.
- Periodic Change Password: the scheduled password change in next days
- Password Change Mode: the change mode set by Platform

Platforms page include a Stacked column chart of the compliace status by Platforms

Safes page include a Stacked column chart of the compliace status by Safes
