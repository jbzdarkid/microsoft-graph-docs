---
title: "industryDataConnector: validate"
description: "Perform validations applicable for the specific instance of the data connector."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industry-data-etl"
doc_type: apiPageType
---

# industryDataConnector: validate

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Perform validations applicable for the specific instance of the data connector.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "industrydata_industrydataconnector_validate" } -->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-industrydataconnector-validate-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
POST /external/industryData/dataConnectors/{industryDataConnectorId}/validate
POST /external/industryData/inboundFlows/{inboundFlowId}/dataConnector/validate
```

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this action returns a `202 Accepted` response code.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "industrydataconnectorthis.validate",
  "sampleKeys": ["8c010e87-c28b-4350-bdc1-65ec29258b93"]
}
-->

```http
POST https://graph.microsoft.com/beta/external/industryData/dataConnectors/8c010e87-c28b-4350-bdc1-65ec29258b93/validate
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->

```http
HTTP/1.1 202 Accepted
```
