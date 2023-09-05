---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = BookingStaffMember(
	odata_type = "#microsoft.graph.bookingStaffMember",
	working_hours = [
		BookingWorkHours(
			odata_type = "#microsoft.graph.bookingWorkHours",
			day = DayOfWeek.Monday,
			time_slots = [
			]
			additional_data = {
					"day@odata_type" : "#microsoft.graph.dayOfWeek",
					"time_slots@odata_type" : "#Collection(microsoft.graph.bookingWorkTimeSlot)",
			}
		),
		BookingWorkHours(
			odata_type = "#microsoft.graph.bookingWorkHours",
			day = DayOfWeek.Tuesday,
			time_slots = [
				BookingWorkTimeSlot(
					odata_type = "#microsoft.graph.bookingWorkTimeSlot",
					end_time = "17:00:00.0000000",
					start_time = "08:00:00.0000000",
				),
			]
			additional_data = {
					"day@odata_type" : "#microsoft.graph.dayOfWeek",
					"time_slots@odata_type" : "#Collection(microsoft.graph.bookingWorkTimeSlot)",
			}
		),
		BookingWorkHours(
			odata_type = "#microsoft.graph.bookingWorkHours",
			day = DayOfWeek.Wednesday,
			time_slots = [
				BookingWorkTimeSlot(
					odata_type = "#microsoft.graph.bookingWorkTimeSlot",
					end_time = "17:00:00.0000000",
					start_time = "08:00:00.0000000",
				),
			]
			additional_data = {
					"day@odata_type" : "#microsoft.graph.dayOfWeek",
					"time_slots@odata_type" : "#Collection(microsoft.graph.bookingWorkTimeSlot)",
			}
		),
		BookingWorkHours(
			odata_type = "#microsoft.graph.bookingWorkHours",
			day = DayOfWeek.Thursday,
			time_slots = [
				BookingWorkTimeSlot(
					odata_type = "#microsoft.graph.bookingWorkTimeSlot",
					end_time = "17:00:00.0000000",
					start_time = "08:00:00.0000000",
				),
			]
			additional_data = {
					"day@odata_type" : "#microsoft.graph.dayOfWeek",
					"time_slots@odata_type" : "#Collection(microsoft.graph.bookingWorkTimeSlot)",
			}
		),
		BookingWorkHours(
			odata_type = "#microsoft.graph.bookingWorkHours",
			day = DayOfWeek.Friday,
			time_slots = [
				BookingWorkTimeSlot(
					odata_type = "#microsoft.graph.bookingWorkTimeSlot",
					end_time = "17:00:00.0000000",
					start_time = "08:00:00.0000000",
				),
			]
			additional_data = {
					"day@odata_type" : "#microsoft.graph.dayOfWeek",
					"time_slots@odata_type" : "#Collection(microsoft.graph.bookingWorkTimeSlot)",
			}
		),
	]
)

result = await graph_client.solutions.booking_businesses.by_booking_businesse_id('bookingBusiness-id').staff_members.by_staff_member_id('bookingStaffMemberBase-id').patch(request_body = request_body)


```