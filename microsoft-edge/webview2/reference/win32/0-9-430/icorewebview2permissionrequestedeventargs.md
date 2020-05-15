---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 529f4a444b3ad6d0d5831da6015831b077102354
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653744"
---
# Schnittstellen ICoreWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

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

