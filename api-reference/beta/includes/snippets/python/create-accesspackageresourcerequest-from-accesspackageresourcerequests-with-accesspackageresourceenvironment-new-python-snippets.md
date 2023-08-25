---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = AccessPackageResourceRequest(
	catalog_id = "de9315c1-272b-4905-924b-cc112ca180c7",
	access_package_resource = AccessPackageResource(
		display_name = "Community Outreach",
		description = "https://contoso.sharepoint.com/sites/CSR",
		resource_type = "SharePoint Online Site",
		origin_id = "https://contoso.sharepoint.com/sites/CSR",
		origin_system = "SharePointOnline",
		access_package_resource_environment = AccessPackageResourceEnvironment(
			origin_id = "https://contoso-admin.sharepoint.com/",
		),
	),
	request_type = "AdminAdd",
)

result = await graph_client.identity_governance.entitlement_management.acces_package_resource_requests.post(request_body = request_body)


```