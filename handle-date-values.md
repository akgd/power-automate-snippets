Format SharePoint date like 2020-02-01.

```formatDateTime(body('Get_item')?['NotificationDateCalc'],'yyyy-MM-dd')```

Format SharePoint date like 02/01/2020.

```formatDateTime(body('Get_item')?['NotificationDateCalc'],'MM/dd/yyyy')```

Check if SharePoint date field is empty. If yes, return nothing. If no, add five hours date (to resolve our time zone issues) and format.

```if(empty(triggerBody()?['Date2']),'',formatDateTime(addHours(triggerBody()?['Date2'],5),'yyyy-MM-dd'))```
