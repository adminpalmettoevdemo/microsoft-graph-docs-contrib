---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ClaimsMappingPolicy(
	display_name = "UpdateClaimsPolicy",
)

result = await graph_client.policies.claim_mapping_policies.by_claim_mapping_policie_id('claimsMappingPolicy-id').patch(request_body = request_body)


```