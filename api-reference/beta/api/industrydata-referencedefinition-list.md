---
title: "List referenceDefinitions"
description: "Get a list of the referenceDefinition objects and their properties."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industry-data-etl"
doc_type: apiPageType
---

# List referenceDefinitions

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [referenceDefinition](../resources/industrydata-referencedefinition.md) objects and their properties.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "industrydata_referencedefinition_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-referencedefinition-list-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /external/industryData/referenceDefinitions
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

If successful, this method returns a `200 OK` response code and a collection of [microsoft.graph.industryData.referenceDefinition](../resources/industrydata-referencedefinition.md) objects in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "list_referencedefinition"
}
-->

```http
GET https://graph.microsoft.com/beta/external/industryData/referenceDefinitions
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.industryData.referenceDefinition)"
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "code": "home",
      "createdDateTime": "0001-01-01T00:00:00Z",
      "id": "RefEmailAddressType-home",
      "isDisabled": false,
      "lastModifiedDateTime": "0001-01-01T00:00:00Z",
      "referenceType": "RefEmailAddressType",
      "sortIndex": 10,
      "source": "CEDS"
    },
    {
      "code": "01",
      "createdDateTime": "0001-01-01T00:00:00Z",
      "id": "RefGradeLevel-01",
      "isDisabled": false,
      "lastModifiedDateTime": "0001-01-01T00:00:00Z",
      "referenceType": "RefGradeLevel",
      "sortIndex": 60,
      "source": "CEDS"
    },
    {
      "code": "02",
      "createdDateTime": "0001-01-01T00:00:00Z",
      "id": "RefGradeLevel-02",
      "isDisabled": false,
      "lastModifiedDateTime": "0001-01-01T00:00:00Z",
      "referenceType": "RefGradeLevel",
      "sortIndex": 70,
      "source": "CEDS"
    },
    {
      "code": "undergraduate",
      "createdDateTime": "0001-01-01T00:00:00Z",
      "id": "RefGradeLevel-undergraduate",
      "isDisabled": false,
      "lastModifiedDateTime": "0001-01-01T00:00:00Z",
      "referenceType": "RefGradeLevel",
      "sortIndex": 270,
      "source": "Contoso"
    },
    {
      "code": "username",
      "createdDateTime": "0001-01-01T00:00:00Z",
      "id": "RefIdentifierType-username",
      "isDisabled": false,
      "lastModifiedDateTime": "0001-01-01T00:00:00Z",
      "referenceType": "RefIdentifierType",
      "sortIndex": 40,
      "source": "IMS Global"
    },
    {
      "code": "academicTrust",
      "createdDateTime": "0001-01-01T00:00:00Z",
      "id": "RefOrgType-academicTrust",
      "isDisabled": false,
      "lastModifiedDateTime": "0001-01-01T00:00:00Z",
      "referenceType": "RefOrgType",
      "sortIndex": 140,
      "source": "Contoso"
    }
  ]
}
```
