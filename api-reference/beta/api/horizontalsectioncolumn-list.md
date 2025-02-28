---
title: 'List horizontalSectionColumns'
description: 'Get a list of the horizontalSectionColumn objects and their properties.'
author: sangle7
ms.localizationpriority: medium
ms.prod: sharepoint
doc_type: apiPageType
---

# List horizontalSectionColumns

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [horizontalSectionColumn](../resources/horizontalsectioncolumn.md) objects and their properties. Sort by `id` in ascending order.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | Sites.Read.All, Sites.ReadWrite.All         |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | Sites.Read.All, Sites.ReadWrite.All         |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /sites/{sitesId}/pages/{sitePageId}/canvasLayout/horizontalSections/{horizontalSectionId}/columns
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

If successful, this method returns a `200 OK` response code and a collection of [horizontalSectionColumn](../resources/horizontalsectioncolumn.md) objects in the response body.

## Examples

### Request

The following is an example of a request.


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "list_horizontalsectioncolumn"
}
-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/sites/{sitesId}/pages/{sitePageId}/canvasLayout/horizontalSections/{horizontalSectionId}/columns
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/list-horizontalsectioncolumn-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/list-horizontalsectioncolumn-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/list-horizontalsectioncolumn-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/list-horizontalsectioncolumn-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/list-horizontalsectioncolumn-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/list-horizontalsectioncolumn-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

The following is an example of the response

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.horizontalSectionColumn)"
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.horizontalSectionColumn",
      "id": "1",
      "width": 6
    },
    {
      "@odata.type": "#microsoft.graph.horizontalSectionColumn",
      "id": "2",
      "width": 6
    }
  ]
}
```
