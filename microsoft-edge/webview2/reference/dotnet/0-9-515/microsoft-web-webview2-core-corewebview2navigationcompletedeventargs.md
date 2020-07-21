---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e2e973e2ee1817decd24bbc1d0dc3daa9709795c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885079"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Ereignis-args für das NavigationCompleted-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Issuccess](#issuccess) | "True", wenn die Navigation erfolgreich ist.
[Navigations-Nr](#navigationid) | Die ID der Navigation.
[WebErrorStatus](#weberrorstatus) | Der Fehlercode, wenn die Navigation fehlgeschlagen ist.

## Member

#### Issuccess 

"True", wenn die Navigation erfolgreich ist.

> public bool [issuccess](#issuccess)

Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.

#### Navigations-Nr 

Die ID der Navigation.

> öffentliche ULONG- [Navigations](#navigationid) -Nr

#### WebErrorStatus 

Der Fehlercode, wenn die Navigation fehlgeschlagen ist.

> öffentliche CoreWebView2WebErrorStatus- [WebErrorStatus](#weberrorstatus)

