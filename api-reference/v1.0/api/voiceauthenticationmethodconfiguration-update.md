---
title: "Update voiceAuthenticationMethodConfiguration"
description: "Update the properties of a voiceAuthenticationMethodConfiguration object."
author: "jpettere"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Update voiceAuthenticationMethodConfiguration
Namespace: microsoft.graph

Update the properties of a [voiceAuthenticationMethodConfiguration](../resources/voiceauthenticationmethodconfiguration.md) object, which represents the voice call authentication method policy for the Azure AD tenant.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "voiceauthenticationmethodconfiguration_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/voiceauthenticationmethodconfiguration-update-permissions.md)]

For delegated scenarios, the administrator needs one of the following [Azure AD roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):

* Authentication Policy Administrator
* Global Administrator

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /policies/authenticationMethodsPolicy/authenticationMethodConfigurations/voice
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]

|Property|Type|Description|
|:---|:---|:---|
|excludeTargets|[excludeTarget](../resources/excludetarget.md) collection|Groups of users that are excluded from the policy.|
|isOfficePhoneAllowed|Boolean|`true` if users can register office phones, otherwise, `false`.|
|state|authenticationMethodState|Possible values are: `enabled`, `disabled`.|

>**Note:** The `@odata.type` property with a value of `#microsoft.graph.voiceAuthenticationMethodConfiguration` must be included in the body.

## Response

If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.

## Examples

### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "update_voiceauthenticationmethodconfiguration"
}
-->
``` http
PATCH https://graph.microsoft.com/v1.0/policies/authenticationMethodsPolicy/authenticationMethodConfigurations/voice
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.voiceAuthenticationMethodConfiguration",
  "isOfficePhoneAllowed": "false"
}
```


### Response
The following is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

