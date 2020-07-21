---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e29765a4b8a3e620b8c627c7b05b9f0b4ff63f95
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886416"
---
# 0.9.430-Interface-ICoreWebView2PermissionRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das PermissionRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Der Ursprung des Webinhalts, der die Berechtigung anfordert.
[get_PermissionKind](#get_permissionkind) | Der Typ der angeforderten Berechtigung.
[get_IsUserInitiated](#get_isuserinitiated) | "True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.
[get_State](#get_state) | Der Status einer Berechtigungs Anfrage, also
[put_State](#put_state) | Legt die State-Eigenschaft fest.
[GetDeferral](#getdeferral) | Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.

## Member

#### get_Uri 

Der Ursprung des Webinhalts, der die Berechtigung anfordert.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### get_PermissionKind 

Der Typ der angeforderten Berechtigung.

> Public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND *-Wert)

#### get_IsUserInitiated 

"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.

> Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.

#### get_State 

Der Status einer Berechtigungs Anfrage, also

> Public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE *-Wert)

Gibt an, ob die Anforderung erteilt wurde. Der Standardwert ist CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Legt die State-Eigenschaft fest.

> Public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE Wert)

#### GetDeferral 

Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.

> öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * Stundung)

Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.

