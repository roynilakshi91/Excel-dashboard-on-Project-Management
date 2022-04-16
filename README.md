# Interactive Dashboard in Excel



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
 * Getting the list of dates using function and connect it with thwe scroll bar =SEQUENCE(1,26,MIN(D13:D58)+workings!D12,1)
 * Conditional Formatting
    * Progress bar
    * Formatting the weekend date  =AND(WEEKDAY(K$12,2)>5,$B13<>"")
    * Adjusting the format of the date list =$K$12<>""
    * Color the days with "Completed" task =AND(K$12 >= $D13,WORKDAY.INTL($D13,$H13,1)-1>=K$12)
    * Color the days with "In Progress" task =AND(K$12>=WORKDAY.INTL($D13,$H13,1),$E13<>1,$K12<=$G13)
    * Color the days with "Not Started" task =AND(K$12>=WORKDAY.INTL($D13,$H13,1),$E13=0,$K12<=$G13)
 

