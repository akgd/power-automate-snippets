Check if SharePoint date field is empty. If yes, return nothing. If no, add five hours date (to resolve time zone issue) and format.
```if(empty(triggerBody()?['Date2']),'',formatDateTime(addHours(triggerBody()?['Date2'],5),'yyyy-MM-dd'))```
