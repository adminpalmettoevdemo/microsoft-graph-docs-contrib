---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = FeatureRolloutPolicyItemRequestBuilder.FeatureRolloutPolicyItemRequestBuilderGetQueryParameters(
		expand = ["appliesTo"],
)

request_configuration = FeatureRolloutPolicyItemRequestBuilder.FeatureRolloutPolicyItemRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.policies.feature_rollout_policies.by_feature_rollout_policy_id('featureRolloutPolicy-id').get(request_configuration = request_configuration)


```