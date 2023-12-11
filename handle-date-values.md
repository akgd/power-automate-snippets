Format now like 2020-02-01

```formatDateTime(utcNow(),'yyyy-MM-dd')```

Format SharePoint date like 2020-02-01

```formatDateTime(body('Get_item')?['YourDateField'],'yyyy-MM-dd')```

Format SharePoint date like 02/01/2020

```formatDateTime(body('Get_item')?['YourDateField'],'MM/dd/yyyy')```

Format SharePoint date like 02/01/2020 3:02 PM

```formatDateTime(body('Get_item')?['YourDateField'],'yyyy h:mm tt')```

Format SharePoint date like Monday, December 20, 2021

```formatDateTime(body('Get_item')?['YourDateField'],'dddd, MMMM dd, yyyy')```

Format SharePoint date for use in REST queries

```formatDateTime(addDays(utcNow(), -1),'yyyy-MM-ddThh:mm:ss')```

Check if SharePoint date field is empty. If yes, return nothing. If no, add five hours date (to resolve time zone issues for site set to Eastern US time) and format.

```if(empty(triggerBody()?['YourDateField']),'',formatDateTime(addHours(triggerBody()?['YourDateField'],5),'yyyy-MM-dd'))```

Get the day of the week. This returns 0-6 (Sunday to Saturday)

```dayOfWeek(utcNow())```

Get the day of the month

```dayOfMonth(utcNow())```
