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
ms.openlocfilehash: c82c37d7127d69700f35fbf9e2a69f85159a7109
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698800"
---
# Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

