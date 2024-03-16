# PowerBICyberArkComplianceReport
Display CyberArk Compliance Report in Power BI Chart

# Version 1.1 
Update table structure

# Version 2.0
Update table structure
Add filter for Device Type and Platform


# First Run 1.1
Create a new directory (for example C:\CyberArkComplianceReport), copy "CyberArk Compliance Report" pbix file and the example file of Compliance Report "ComplianceReport.xlsx"
Run Power BI, open file "CyberArk Compliance Report.pbix", and from "Transform Data > Data source settings" set Data Source to point "C:\CyberArkComplianceReport\ComplianceReport.xlsx"

# First Run 2.0
Copy the example file of Inventory Report "InventoryReport.xlsx"
Run Power BI, open file "CyberArk Compliance Report.pbix", and from "Transform Data > Data source settings" set Data Source to point "C:\CyberArkComplianceReport\InventoryReport.xlsx"


# Import CyberArk Reports
From CyberArk PVWA generate and download a new Compliance Report. Open Compliance Report file and save as "ComplianceReport.xlsx" in the data directory (C:\CyberArkComplianceReport\)
From CyberArk PVWA generate and download a new Inventory Report. Open Inventory Report file and save as "InventoryReport.xlsx" in the data directory (C:\CyberArkComplianceReport\) (The inventory Report is requested only for 2.x vesions)
From Power BI use "Refresh" button to reload Data


# Data
Two data table are used for create the Chart
- Period: represents a set of days within which the password change is expected (7, 15, 30, 60, 90)
- Report: represents the Compliance Report imported from CyberArk PVWA


# Filter
A series of filters are applied to shape the result according to specific needs (for example remove Platform with not password change applied)
From "Transform Data" it's possible to change the filter settings:
- Removing_Safes (for example "Vaultinternal", "PSM")
- Removing_Platforms (for example "Oracle Database")


# Page
Main page includes two Pie charts and one Donut chart
- Compliance Status: this is the main graph as it represents the real situation of the accounts managed in CyberArk
- Periodic Change Password: the scheduled password change in next days
- Password Change Mode: the change mode set by Platform

Platforms page include a Stacked column chart of the compliace status by Platforms

Safes page include a Stacked column chart of the compliace status by Safes


# Logo and Teme
Insert a logo and change the theme colors if you want to use corporate ones