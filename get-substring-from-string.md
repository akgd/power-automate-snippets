### Extract ID (for identifers with no spaces)
Say you have a string like this: *IT Request 27362 SP ID: 136 Renewal Alert: Some specific application*

To extract the ticket number and SharePoint ID, use compose or variable actions and the following expressions:
```
split(trim(split(variables('emailSubject'),'IT Service Request')[1]), ' ')[0]
split(trim(split(variables('emailSubject'),'SP ID:')[1]), ' ')[0]
```
