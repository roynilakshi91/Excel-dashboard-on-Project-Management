# Excel-dashboard-on-Project-Management

Formatting :

* End Date =WORKDAY.INTL([@[Start Date]]-1,[@Duration],1)
* Creationg Pivot table
* Ungroupping start and end date
* Renaming Sum of budget to Budget and sum of actual to actual
* Number formatting using "Value flield setting"
* Count of Project Status:
      * Not started = COUNTIF('Dashboard '!E7:E53,"="&0)
      * In progress = =COUNTIFS('Dashboard '!E7:E53,"<>"&0,'Dashboard '!E7:E53,"<"&1)
      * Completed  =COUNTIF('Dashboard '!E7:E53,"="&1)
      * Remaining = Not Started + In progress
      * Total = Not Started + In progress + Completed
      
 * Donut chart-
     * Days Completed = Sum of Days Completed / Sum of Duration
     * Days Remaining = 1- Days Completed
     * Actual% = Actual/Budget
     * Budget% = 1-Actual%
    
 * Bar Graph -
 In millions (0.0,,/M;-0.0,,\M)
     * Budget 
     * Actual
 
 * Slicer for Project and Manager
 * Date Range = TEXT(MIN(D13:D58),"MMM-D-YY")&" to "&TEXT(MAX(G13:G58),"MMM-D-YY")
 * Adding a scroll bar to change the date
 * 

