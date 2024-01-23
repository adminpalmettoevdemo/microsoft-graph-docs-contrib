---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = ApiConnectorConfigurationRequestBuilder.ApiConnectorConfigurationRequestBuilderGetQueryParameters(
		expand = ["postFederationSignup","postAttributeCollection"],
)

request_configuration = ApiConnectorConfigurationRequestBuilder.ApiConnectorConfigurationRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity.b2x_user_flows.by_b2x_identity_user_flow_id('b2xIdentityUserFlow-id').api_connector_configuration.get(request_configuration = request_configuration)


```