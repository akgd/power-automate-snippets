### Only run if  first version
```@equals(triggerBody()['{VersionNumber}'],'1.0')```

### Only run if folder
```@equals(triggerBody()?['{IsFolder}'],true)```