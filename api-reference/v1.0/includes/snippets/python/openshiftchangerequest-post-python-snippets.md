---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = OpenShiftChangeRequest(
	sender_message = "Can I take this shift?",
	open_shift_id = "577b75d2-a927-48c0-a5d1-dc984894e7b8",
)

request_configuration = OpenShiftChangeRequestsRequestBuilder.OpenShiftChangeRequestsRequestBuilderPostRequestConfiguration()
request_configuration.headers.add("Authorization", "Bearer {token}")


result = await graph_client.teams.by_team_id('team-id').schedule.open_shift_change_requests.post(request_body, request_configuration = request_configuration)


```