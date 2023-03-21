---
title: "Get fileValidateOperation"
description: "Read the properties and relationships of a fileValidateOperation object."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industry-data-etl"
doc_type: apiPageType
---

# Get fileValidateOperations

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [fileValidateOperation](../resources/industrydata-filevalidateoperation.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "industrydata_filevalidateoperation_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-filevalidateoperation-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /external/industryData/operations/{fileValidateOperationId}
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

If successful, this method returns a `200 OK` response code and a [microsoft.graph.industryData.fileValidateOperation](../resources/industrydata-filevalidateoperation.md) object in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "get_fileValidateOperation",
  "sampleKeys": ["581b2ef8-dda2-4a3e-bb62-df13fd4a5808"]
}
-->

```http
GET https://graph.microsoft.com/beta/external/industryData/operations/581b2ef8-dda2-4a3e-bb62-df13fd4a5808
```

### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.industryData.fileValidateOperation"
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.industryData.fileValidateOperation",
  "createdDateTime": "2022-12-14T05:54:35.400029Z",
  "errors": [
    {
      "code": "RequiredFileNotFound",
      "details": [],
      "innerError": null,
      "message": "When trying to validate required file orgs.csv encountered RequiredFileNotFound error.",
      "target": "orgs.csv"
    }
  ],
  "id": "d194fa3e-18c9-47a1-0fb1-08dad8e7a876",
  "lastActionDateTime": "2022-12-14T05:54:43.8410226Z",
  "resourceLocation": "https://graph.microsoft.com/beta/industryData/dataConnectors/022da4a0-c239-4b07-abed-08dad8e7a07a",
  "status": "succeeded",
  "statusDetail": null,
  "validatedFiles": [],
  "warnings": [
    {
      "code": "OptionalFileNotFound",
      "details": [],
      "innerError": null,
      "message": "When trying to validate file classes.csv encountered OptionalFileNotFound error.",
      "target": "classes.csv"
    },
    {
      "code": "OptionalFileNotFound",
      "details": [],
      "innerError": null,
      "message": "When trying to validate file enrollments.csv encountered OptionalFileNotFound error.",
      "target": "enrollments.csv"
    }
  ]
}
```
