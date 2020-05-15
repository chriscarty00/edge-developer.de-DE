---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 9d16f1c72a3921b220bd0046e78ed0c6b32a718a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653933"
---
# Schnittstellen IWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das PermissionRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Der Ursprung des Webinhalts, der die Berechtigung anfordert.
[get_PermissionType](#get_permissiontype) | Der Typ der angeforderten Berechtigung.
[get_IsUserInitiated](#get_isuserinitiated) | "True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.
[get_State](#get_state) | Der Status einer Berechtigungs Anfrage, also
[put_State](#put_state) | Legt die State-Eigenschaft fest.
[GetDeferral](#getdeferral) | Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.

## Member

#### get_Uri 

Der Ursprung des Webinhalts, der die Berechtigung anfordert.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### get_PermissionType 

Der Typ der angeforderten Berechtigung.

> Public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE *-Wert)

#### get_IsUserInitiated 

"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.

> Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.

#### get_State 

Der Status einer Berechtigungs Anfrage, also

> Public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE *-Wert)

Gibt an, ob die Anforderung erteilt wurde. Der Standardwert ist WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Legt die State-Eigenschaft fest.

> Public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE Wert)

#### GetDeferral 

Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.

> öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * Stundung)

Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.

