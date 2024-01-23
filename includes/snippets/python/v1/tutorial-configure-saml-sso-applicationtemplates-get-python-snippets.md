---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = ApplicationTemplatesRequestBuilder.ApplicationTemplatesRequestBuilderGetQueryParameters(
		filter = "displayName eq 'AWS IAM Identity Center (successor to AWS Single Sign-On)'",
)

request_configuration = ApplicationTemplatesRequestBuilder.ApplicationTemplatesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.application_templates.get(request_configuration = request_configuration)


```