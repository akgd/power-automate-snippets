Use coalesce to prevent passing null values to actions that would fail, such as "Format Number". If your format number action is not first in scope, you can configure run-after on "has failed" instead of this.

```coalesce(items('Apply_to_each')?['BestValue'], -1)```
