---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 018d986ac0941406a62786bfb6e3666cf33dc09f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653922"
---
# Schnittstellen ICoreWebView2PermissionRequestedEventArgs 

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das PermissionRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsUserInitiated](#get_isuserinitiated) | "True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.
[get_PermissionKind](#get_permissionkind) | Der Typ der angeforderten Berechtigung.
[get_State](#get_state) | Der Status einer Berechtigungs Anfrage, also
[get_Uri](#get_uri) | Der Ursprung des Webinhalts, der die Berechtigung anfordert.
[GetDeferral](#getdeferral) | Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.
[put_State](#put_state) | Legt die State-Eigenschaft fest.

## Member

#### get_IsUserInitiated 

"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.

> Public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.

#### get_PermissionKind 

Der Typ der angeforderten Berechtigung.

> Public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND *-Wert)

#### get_State 

Der Status einer Berechtigungs Anfrage, also

> Public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE *-Wert)

Gibt an, ob die Anforderung erteilt wurde. Der Standardwert ist COREWEBVIEW2_PERMISSION_STATE_DEFAULT.

#### get_Uri 

Der Ursprung des Webinhalts, der die Berechtigung anfordert.

> Public HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### GetDeferral 

Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.

> öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Stundung)

Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.

#### put_State 

Legt die State-Eigenschaft fest.

> Public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE Wert)

