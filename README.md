#B2B Sales Perfromance Dashboard 
##NovaTech Solutions 

##Project Overview 
A two page interactive Power BI dashboard tracking sales pupeline perfformance and rep-level metrics for a B2B SaaS company across 3 regions.

## Project Problem Statement 
NovaTech solutions needed a central view of pipeline health, rep performance and revenue vs target tracking across their 12-person sales team 

## Dashboard Page 1- Performance Overview
- win rate, avg deal cycle in days, Total deals( all in KPI cards)
- Open Pipeline Value by stage (Funnel Chart)
- Total Deals by Deal stage
- Target vs Monthly Revenue Trend

## Dashboard Page 2 - Sales Rep Performance 
- Revenue closed by Rep
- Deals won vs lost by rep
- Top 5 reps by win rate
- Top 5 reps by Performance leaderboard
- Revenue by region

- ## DAX Measures Used
- win rate = DIVIDE(CALCULATE(COUNTROWS(Sales_Transactions), Sales_Transactions[Deal Stage] = "Closed Won"),
            CALCULATE(COUNTROWS(Sales_Transactions), Sales_Transactions[Deal Stage] IN {"Closed Won", "Closed Lost"}))
- Revenue Closed = CALCULATE(SUM(Sales_Transactions[Deal Value]), Sales_Transactions[Deal Stage]= "Closed Won")
- Target Table (New Table) 
  = DATATABLE("Month", STRING, "Revenue Target",INTEGER,
    {
        {"Jan 2024",18000},
        {"Feb 2024",19000},
        {"Mar 2024",20000},
        {"Apr 2024",21500},
        {"May 2024",23000},
        {"Jun 2024",24500},
        {"Jul 2024",26000},
        {"Aug 2024",27500},
        {"Sep 2024",29000},
        {"Oct 2024",31000},
        {"Nov 2024",33000},
        {"Dec 2024",36000},
        {"Jan 2025",38000},
        {"Feb 2025",40000},
        {"Mar 2025",42500},
        {"Apr 2025",45000},
        {"May 2025",47500},
        {"Jun 2025",50000},
        {"Jul 2025",53000},
        {"Aug 2025",56000},
        {"Sep 2025",59000},
        {"Oct 2025",62000},
} 
## Tools Used
-Power BI (dara visualization)
- DAX (Measures for KPIs and Tables)
- Microsoft Excel (data source)

## Files
- Dashboard pbix file
##Author
Kamsi Chiadi aka Kamsitheanalyst



        {"Nov 2025",65000},
        {"Dec 2025",70000}
    }
