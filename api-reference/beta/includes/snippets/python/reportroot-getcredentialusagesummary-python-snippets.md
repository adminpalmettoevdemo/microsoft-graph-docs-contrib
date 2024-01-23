---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = GetCredentialUsageSummaryWithPeriodRequestBuilder.GetCredentialUsageSummaryWithPeriodRequestBuilderGetQueryParameters(
		filter = "feature eq 'registration'",
)

request_configuration = GetCredentialUsageSummaryWithPeriodRequestBuilder.GetCredentialUsageSummaryWithPeriodRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.reports.get_credential_usage_summary_with_period("{period}").get(request_configuration = request_configuration)


```