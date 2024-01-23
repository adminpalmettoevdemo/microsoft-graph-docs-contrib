---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)

query_params = MeetingAttendanceReportItemRequestBuilder.MeetingAttendanceReportItemRequestBuilderGetQueryParameters(
		expand = ["attendanceRecords"],
)

request_configuration = MeetingAttendanceReportItemRequestBuilder.MeetingAttendanceReportItemRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.me.online_meetings.by_online_meeting_id('onlineMeeting-id').attendance_reports.by_meeting_attendance_report_id('meetingAttendanceReport-id').get(request_configuration = request_configuration)


```