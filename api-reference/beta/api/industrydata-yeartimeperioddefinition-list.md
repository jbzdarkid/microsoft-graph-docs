---
title: "List yearTimePeriodDefinitions"
description: "Get a list of the yearTimePeriodDefinition objects and their properties."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industry-data-etl"
doc_type: apiPageType
---

# List yearTimePeriodDefinitions

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [yearTimePeriodDefinition](../resources/industrydata-yeartimeperioddefinition.md) objects and their properties.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "industrydata_yeartimeperioddefinition_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-yeartimeperioddefinition-list-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /external/industryData/years
```

## Optional query parameters

This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [microsoft.graph.industryData.yearTimePeriodDefinition](../resources/industrydata-yeartimeperioddefinition.md) objects in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "list_yearTimePeriodDefinition"
}
-->

```http
GET https://graph.microsoft.com/beta/external/industryData/years
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.industryData.yearTimePeriodDefinition)"
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.context": "https://graph.microsoft.com/beta/$metadata#external/industryData/years/$entity",
      "displayName": "Fiscal Year 2022",
      "endDate": "2023-06-15",
      "id": "ebf18762-ab92-487e-21d1-08daddab28bb",
      "startDate": "2022-09-01",
      "year": {
        "code": "2022"
      }
    }
  ]
}
```
