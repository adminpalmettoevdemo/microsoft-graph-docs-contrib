---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)


request_configuration = PlannerBucketItemRequestBuilder.PlannerBucketItemRequestBuilderDeleteRequestConfiguration()
request_configuration.headers.add("If-Match", "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"")


await graph_client.planner.buckets.by_planner_bucket_id('plannerBucket-id').delete(request_configuration = request_configuration)


```