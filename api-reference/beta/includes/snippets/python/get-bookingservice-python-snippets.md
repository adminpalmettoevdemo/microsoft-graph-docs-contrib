---
description: "Automatically generated file. DO NOT MODIFY"
---

```python



graph_client = GraphServiceClient(credentials, scopes)


result = await graph_client.booking_businesses.by_booking_business_id('bookingBusiness-id').services.by_booking_service_id('bookingService-id').get()


```