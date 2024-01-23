---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = SoftwareOathAuthenticationMethodConfiguration(
	odata_type = "#microsoft.graph.softwareOathAuthenticationMethodConfiguration",
	state = AuthenticationMethodState.Disabled,
)

result = await graph_client.policies.authentication_methods_policy.authentication_method_configurations.by_authentication_method_configuration_id('authenticationMethodConfiguration-id').patch(request_body)


```