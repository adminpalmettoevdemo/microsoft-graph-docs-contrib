---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = GetM365AppUserDetailWithPeriodRequestBuilder.GetM365AppUserDetailWithPeriodRequestBuilderGetQueryParameters(
		format = "application/json",
)

request_configuration = GetM365AppUserDetailWithPeriodRequestBuilder.GetM365AppUserDetailWithPeriodRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

await graph_client.reports.get_m365_app_user_detail(period='{period}'.get(request_configuration = request_configuration)


```