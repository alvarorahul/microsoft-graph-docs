---
title: "Update app in a chat"
description: "Update an app installed in a chat and bring it in sync with the current version available in the tenant app catalog."
author: "laujan"
localization_priority: Priority
ms.prod: "microsoft-teams"
doc_type: apiPageType
---

# Update app in a chat

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update [teamsAppInstallation](../resources/teamsappinstallation.md) of an [app](../resources/teamsapp.md) within a [chat](../resources/chat.md).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | TeamsAppInstallation.ReadWriteSelfForChat, TeamsAppInstallation.ReadWriteForChat |
|Delegated (personal Microsoft account) | Not supported.   |
|Application | TeamsAppInstallation.ReadWriteSelfForChat.All, TeamsAppInstallation.ReadWriteForChat.All |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
POST /chats/{chatId}/installedApps/{appInstallationId}/upgrade
```

## Response

If successful, this method returns a `200 OK` response code and an updated [teamsApp](../resources/teamsapp.md) object in the response body.

## Example: Upgrade an app installed in a chat

### Request

<!-- {
  "blockType": "request",
  "name": "update_installedApp"
}-->

```http
POST https://graph.microsoft.com/beta/chats/{chatId}/installedApps/{appInstallationId}/upgrade
```

### Response

<!-- {
  "blockType": "response",
  "truncated": true
}
-->

```http
HTTP/1.1 204 No Content
Content-type: application/json

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```