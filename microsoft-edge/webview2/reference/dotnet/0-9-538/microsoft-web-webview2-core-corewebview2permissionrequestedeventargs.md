---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 58d87d1815b81969c4424eacfcec26ffe425192e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698776"
---
# Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Ereignis-args für das PermissionRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | "True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.
[PermissionKind](#permissionkind) | Der Typ der angeforderten Berechtigung.
[Status](#state) | Der Status einer Berechtigungs Anfrage, also
[URI](#uri) | Der Ursprung des Webinhalts, der die Berechtigung anfordert.
[GetDeferral](#getdeferral) | Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.

## Member

#### IsUserInitiated 

"True", wenn die Berechtigungsanforderung durch eine Benutzergeste initiiert wurde.

> public bool [IsUserInitiated](#isuserinitiated)

Beachten Sie, dass das initiieren über eine Benutzergeste nicht bedeutet, dass der Benutzer auf die zugeordnete Ressource zugreifen soll.

#### PermissionKind 

Der Typ der angeforderten Berechtigung.

> öffentliche CoreWebView2PermissionKind- [PermissionKind](#permissionkind)

#### Status 

Der Status einer Berechtigungs Anfrage, also

> öffentlicher CoreWebView2PermissionState- [Zustand](#state)

Gibt an, ob die Anforderung erteilt wurde.

Der Standardwert ist CoreWebView2PermissionState. default.

#### URI 

Der Ursprung des Webinhalts, der die Berechtigung anfordert.

> öffentlicher Zeichenfolgen- [URI](#uri)

#### GetDeferral 

Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.

> Public CoreWebView2Deferral [getstundungal](#getdeferral)()

Entwickler können das verzögerte Objekt verwenden, um die berechtigungsentscheidung zu einem späteren Zeitpunkt zu treffen.

