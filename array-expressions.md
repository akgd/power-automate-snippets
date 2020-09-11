### Array length
```
length(outputs('Get_items')?['body/value'])
```

### Get "ID" property from the first array item (SharePoint response in this case)
```
first(outputs('Get_items')?['body/value'])['ID']
```
