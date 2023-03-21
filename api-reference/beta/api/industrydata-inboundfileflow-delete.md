---
title: "Delete inboundFileFlow"
description: "Delete an inboundFileFlow object."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industry-data-etl"
doc_type: apiPageType
---

# Delete inboundFileFlow

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Delete an [inboundFileFlow](../resources/industrydata-inboundfileflow.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "industrydata_inboundfileflow_delete" } -->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-inboundfileflow-delete-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
DELETE /external/industryData/inboundFlows/{inboundFlowId}
```

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "delete_inboundflow"
}
-->

```http
DELETE https://graph.microsoft.com/beta/external/industryData/inboundFlows/7bd62d17-8c37-4494-f68d-08daddab2911
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
