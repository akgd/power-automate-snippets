Use coalesce to prevent passing null values to actions that would fail, such as "Format Number". Alternatively, configure run-after on "has failed".

```coalesce(items('Apply_to_each')?['BestValue'], -1)```
