---
title: "Update inboundFlow"
description: "Update the properties of an inboundFlow object."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industry-data-etl"
doc_type: apiPageType
---

# Update inboundFlow

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of an [inboundFlow](../resources/industrydata-inboundflow.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "industrydata_inboundflow_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-inboundflow-update-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
PATCH /external/industryData/inboundFlows/{inboundFlowId}
```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request body

[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]

| Property           | Type           | Description                                                                                                                                                                                                                                          |
| :----------------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| displayName        | String         | The name of the process. Inherited from [industryDataActivity](../resources/industrydata-industrydataactivity.md). Required.                                                                                                                         |
| effectiveDateTime  | DateTimeOffset | The start of the time window when the flow is allowed to run. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 is `2014-01-01T00:00:00Z`. Required. |
| expirationDateTime | DateTimeOffset | The end of the time window when the flow is allowed to run. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 is `2014-01-01T00:00:00Z`. Optional.   |

### Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "update_inboundfileflow"
}
-->

```http
PATCH https://graph.microsoft.com/beta/external/industryData/inboundFlows/7bd62d17-8c37-4494-f68d-08daddab2911
Content-Type: application/json
Content-length: 246

{
  "@odata.type": "#microsoft.graph.industryData.inboundFlow",
  "displayName": "My Inbound Flow",
  "effectiveDateTime": "2022-03-12T16:40:46.924769+05:30",
  "expirationDateTime": "2023-03-12T16:40:46.924769+05:30"
}
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->

```http
HTTP/1.1 204 No Content
```
