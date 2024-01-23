---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = OrganizationalBranding(
	sign_in_page_text = "Default",
	username_hint_text = "DefaultHint",
)

request_configuration = BrandingRequestBuilder.BrandingRequestBuilderPatchRequestConfiguration()
request_configuration.headers.add("Accept-Language", "0")


result = await graph_client.organization.by_organization_id('organization-id').branding.patch(request_body, request_configuration = request_configuration)


```