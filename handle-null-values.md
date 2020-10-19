Use coalesce to prevent passing null values to actions that would fail, such as "Format Currency"

```coalesce(items('Apply_to_each')?['BestValue'], -1)```