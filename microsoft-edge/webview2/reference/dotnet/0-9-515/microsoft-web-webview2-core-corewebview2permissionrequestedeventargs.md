---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2bfa4559824c9bb397648249ead8fa8cb60c281c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884631"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

