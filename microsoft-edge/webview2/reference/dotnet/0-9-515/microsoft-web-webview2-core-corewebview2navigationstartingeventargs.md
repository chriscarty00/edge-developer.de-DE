---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ea3936ac1267fa085f62db843f5cac3fad2635b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879786"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse 

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen. Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Ereignis-args für das NavigationStarting-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Abbrechen](#cancel) | Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.
[Isumgeleitet](#isredirected) | "True", wenn die Navigation umgeleitet wird.
[IsUserInitiated](#isuserinitiated) | "True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.
[Navigations-Nr](#navigationid) | Die ID der Navigation.
[RequestHeaders](#requestheaders) | Die HTTP-Anforderungsheader für die Navigation.
[URI](#uri) | Der URI der angeforderten Navigation.

## Member

#### Abbrechen 

Der Host kann dieses Flag so einstellen, dass die Navigation abgebrochen wird.

> öffentlicher bool- [Abbruch](#cancel)

Wenn dies der Fall ist, ist es so, als ob die Navigation nie stattgefunden hat und der Inhalt der aktuellen Seite intakt bleibt. Aus Leistungsgründen können HTTP-Anforderungen auftreten, während der Host reagiert. Das bedeutet, dass Cookies für einen Teil einer Anforderung für die Navigation eingestellt und verwendet werden können.

#### Isumgeleitet 

"True", wenn die Navigation umgeleitet wird.

> öffentliche bool- [isumgeleitet](#isredirected)

#### IsUserInitiated 

"True", wenn die Navigation im Gegensatz zur programmgesteuerten Navigation durch eine Benutzergeste initiiert wurde.

> public bool [IsUserInitiated](#isuserinitiated)

#### Navigations-Nr 

Die ID der Navigation.

> öffentliche ULONG- [Navigations](#navigationid) -Nr

#### RequestHeaders 

Die HTTP-Anforderungsheader für die Navigation.

> öffentliche HttpRequestHeaders- [RequestHeaders](#requestheaders)

Beachten Sie, dass die HTTP-Anforderungs Kopfzeilen in einem NavigationStarting-Ereignis nicht geändert werden können.

#### URI 

Der URI der angeforderten Navigation.

> öffentlicher Zeichenfolgen- [URI](#uri)

