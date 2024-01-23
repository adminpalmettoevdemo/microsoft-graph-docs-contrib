---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = PlannerPlanDetails(
	shared_with = PlannerUserIds(
		additional_data = {
				"6463a5ce-2119-4198-9f2a-628761df4a62" : True,
				"d95e6152-f683-4d78-9ff5-67ad180fea4a" : False,
		}
	),
	category_descriptions = PlannerCategoryDescriptions(
		category1 = "Indoors",
		category3 = None,
	),
)

request_configuration = DetailsRequestBuilder.DetailsRequestBuilderPatchRequestConfiguration()
request_configuration.headers.add("Prefer", "return=representation")
request_configuration.headers.add("If-Match", "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc=\"")


result = await graph_client.planner.plans.by_planner_plan_id('plannerPlan-id').details.patch(request_body, request_configuration = request_configuration)


```