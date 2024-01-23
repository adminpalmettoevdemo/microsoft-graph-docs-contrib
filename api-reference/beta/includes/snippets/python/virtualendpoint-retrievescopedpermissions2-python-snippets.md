---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = RetrieveScopedPermissionsRequestBuilder.RetrieveScopedPermissionsRequestBuilderGetQueryParameters(
		filter = "permission in ('Microsoft.CloudPC/ProvisioningPolicies/Update','Microsoft.CloudPC/ProvisioningPolicies/Create')",
)

request_configuration = RetrieveScopedPermissionsRequestBuilder.RetrieveScopedPermissionsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.device_management.virtual_endpoint.retrieve_scoped_permissions.get(request_configuration = request_configuration)


```