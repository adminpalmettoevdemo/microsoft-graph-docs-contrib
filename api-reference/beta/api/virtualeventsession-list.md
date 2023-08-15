---
title: "List virtualEventSessions"
description: "Get a list of all virtualEventSession objects under a virtual event."
author: "awang119"
ms.localizationpriority: medium
ms.prod: "cloud-communications"
doc_type: apiPageType
---

# List virtualEventSessions

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of all [virtualEventSession](../resources/virtualeventsession.md) objects under a virtual event.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|VirtualEvent.Read|
|Delegated (personal Microsoft account)|Not supported.|
|Application|VirtualEvent.Read.All|

> [!NOTE]
>
> To use application permissions for this API, tenant administrators must create an [application access policy](/graph/cloud-communication-online-meeting-application-access-policy) and assign it to a user. This allows the authorized application to access registrants' information from virtual events created by that specific user.

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
To list all sessions of a webinar:

``` http
GET /solutions/virtualEvents/webinars/{webinarId}/sessions
```

## Optional query parameters

This method does not support the OData query parameters. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [virtualEventSession](../resources/virtualeventsession.md) objects in the response body.

## Examples

### Request

The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "list_virtualeventsessions",
  "sampleKeys": ["f8ce2a5f-0e6a-4186-aa90-1f64bc023566@5466a424-aadf-425c-9b24-034ca28d4bdd"]
}
-->
``` http
GET https://graph.microsoft.com/beta/solutions/virtualEvents/webinars/f8ce2a5f-0e6a-4186-aa90-1f64bc023566@5466a424-aadf-425c-9b24-034ca28d4bdd/sessions
```

### Response

The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.virtualEventSession)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.virtualEventSession",
      "id": "8d62dd52-4dff-4c75-96a9-f905cc3ff942",
      "startDateTime": "2023-08-08T12:30:00Z",
      "endDateTime": "2023-08-09T22:00:00Z",
      "joinWebUrl": "https://teams.microsoft.com/l/meetup-join/19%3ameeting_ZDVjNzk3OWEtYjc2NS00NTA1LTkyMzQtYTYzMGI5YmFmMjM5%40thread.v2/0?context=%7b%22Tid%22%3a%2272f988bf-86f1-41af-91ab-2d7cd011db47%22%2c%22Oid%22%3a%221cd068e4-5b08-4e75-a7f9-7b4e067a0820%22%7d",
      "subject": "Session one",
      "participants": {
        "@odata.type": "microsoft.graph.meetingParticipants"
      },
      "isBroadcast": null,
      "broadcastSettings": null,
      "capabilities": [],
      "audioConferencing": null,
      "chatInfo": {
        "threadId": "19:meeting_ZDVjNzk3OWEtYjc2NS00NTA1LTkyMzQtYTYzMGI5YmFmMjM5@thread.v2",
        "messageId": "0",
        "replyChainMessageId": null
      },
      "videoTeleconferenceId": null,
      "externalId": null,
      "joinMeetingIdSettings": null,
      "lobbyBypassSettings": null,
      "isEntryExitAnnounced": null,
      "allowedPresenters": null,
      "allowAttendeeToEnableMic": null,
      "allowAttendeeToEnableCamera": null,
      "allowMeetingChat": null,
      "shareMeetingChatHistoryDefault": null,
      "allowTeamworkReactions": null,
      "recordAutomatically": null,
      "watermarkProtection": null,
      "allowParticipantsToChangeName": null
    }
  ]
}
```
