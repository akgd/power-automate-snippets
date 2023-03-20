### If choice equals value
```@equals(triggerBody()?['Status'], 'Released')```
else try
```@equals(triggerBody()?['YourChoiceField']?['Value'], 'Target Choice')```

### If modified by email
```@not(equals(triggerBody()?['Editor']?['Email'], 'automate@email.com'))```

### If modified by email
```@equals(triggerBody()?['Editor']?['Email'], 'automate@email.com')```

### If first version
```@equals(triggerBody()['{VersionNumber}'],'1.0')```

### If is folder
```@equals(triggerBody()?['{IsFolder}'],true)```
