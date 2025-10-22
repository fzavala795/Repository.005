# Repository.005
Power BI Dashboard to track key financial metrics: Revenue, COGS, Expense, Profit Margin.
## Data Used
Excel Sample data in two separate sheets uploaded into separate tables, which includes all the relevant information for this exercise.

Date Table created to intersect both tables, not being used in first tab.

## Measures Built
The following measures were built to completed tab “Page 1”, where “ACT” represents Actual amounts and “BGT” represents budget.

The data can be sliced by Department, and visualize by BU and location.

•	ACT COGS = ABS(CALCULATE(SUM('Actual Data'[Amount]),USERELATIONSHIP('Actual Data'[Department],'Budget Data'[Department]),'Actual Data'[Account Type]="COGS"))

•	ACT Expenses = ABS(CALCULATE(SUM('Actual Data'[Amount]),USERELATIONSHIP('Actual Data'[Department],'Budget Data'[Department]),'Actual Data'[Account Type]="Expenses"))

•	ACT Profit = [ACT Revenue]-[ACT COGS]-[ACT Expenses]

•	ACT Profit Margin = DIVIDE([ACT Profit],[ACT Revenue])

•	ACT Revenue = ABS(CALCULATE(SUM('Actual Data'[Amount]),USERELATIONSHIP('Actual Data'[Department],'Budget Data'[Department]),'Actual Data'[Account Type]="Revenue"))

•	BGT COGS = ABS(CALCULATE(SUM('Budget Data'[Amount]),'Actual Data'[Account Type]="COGS"))

•	BGT Expenses = ABS(CALCULATE(SUM('Budget Data'[Amount]),'Actual Data'[Account Type]="Expenses"))

•	BGT Profit = [BGT Revenue]-[BGT COGS]- [BGT Expenses]

•	BGT Profit Margin = DIVIDE([BGT Profit],[BGT Revenue])

•	BGT Revenue = ABS(CALCULATE(SUM('Budget Data'[Amount]),'Budget Data'[Account Type]="Revenue"))


## Visuals
The visuals are used to showcase some of the options are: Cards, button slicer, line and column charts, matrix and donut chart.

## Dashboard File
<a href=https://github.com/fzavala795/Repository.005/blob/main/Repository.005%20Dashboard.pbix> Repository.005 Dashboard</a>

## Visual Images
**Tab1 as intended when accessing dashboard:**

![Screenshot (495)](https://github.com/fzavala795/Repository.005/blob/main/Screenshot1.jpg)




**Tab1 shown with Dept1 selected in the Button Slice pane**

![Screenshot (495)](https://github.com/fzavala795/Repository.005/blob/main/Screenshot2.jpg)
