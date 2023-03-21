---
title: "List roleGroups"
description: "Get a list of the roleGroup objects and their properties."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industry-data-etl"
doc_type: apiPageType
---

# List roleGroups

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [roleGroup](../resources/industrydata-rolegroup.md) objects and their properties.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "industrydata_rolegroup_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-rolegroup-list-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /external/industryData/roleGroups
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

If successful, this method returns a `200 OK` response code and a collection of [microsoft.graph.industryData.roleGroup](../resources/industrydata-rolegroup.md) objects in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "list_rolegroup"
}
-->

```http
GET https://graph.microsoft.com/beta/external/industryData/roleGroups
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.industryData.roleGroup)"
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "displayName": "Staff",
      "id": "staff",
      "roles": [
        {
          "code": "faculty"
        },
        {
          "code": "teacher"
        }
      ]
    },
    {
      "displayName": "Students",
      "id": "students",
      "roles": [
        {
          "code": "student"
        }
      ]
    }
  ]
}
```
