---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = AlertConfigurationsRequestBuilder.AlertConfigurationsRequestBuilderGetQueryParameters(
		filter = "scopeId eq '/' and scopeType eq 'DirectoryRole'",
		expand = ["alertDefinition"],
)

request_configuration = AlertConfigurationsRequestBuilder.AlertConfigurationsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_governance.role_management_alerts.alert_configurations.get(request_configuration = request_configuration)


```