---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = ExternalPartnerSettingsRequestBuilder.ExternalPartnerSettingsRequestBuilderGetQueryParameters(
		select = ["id","partnerId","enableConnection"],
)

request_configuration = ExternalPartnerSettingsRequestBuilder.ExternalPartnerSettingsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.device_management.virtual_endpoint.external_partner_settings.get(request_configuration = request_configuration)


```