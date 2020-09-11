---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 5f63cd8a9dc16ee82d77fe4b5a0b705eb79e7c6f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010939"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

