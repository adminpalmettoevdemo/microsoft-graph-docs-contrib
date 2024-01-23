---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

request_body = Schedule(
	enabled = True,
	time_zone = "America/Chicago",
	provision_status = OperationStatus.Completed,
	provision_status_code = None,
	open_shifts_enabled = True,
	swap_shifts_requests_enabled = True,
	offer_shift_requests_enabled = True,
	time_off_requests_enabled = True,
	start_day_of_week = DayOfWeek.Tuesday,
	activities_included_when_copying_shifts_enabled = True,
	time_clock_enabled = True,
	time_clock_settings = TimeClockSettings(
		approved_location = GeoCoordinates(
			altitude = 1024.13,
			latitude = 26.13246,
			longitude = 24.34616,
		),
	),
)

result = await graph_client.teams.by_team_id('team-id').schedule.put(request_body)


```