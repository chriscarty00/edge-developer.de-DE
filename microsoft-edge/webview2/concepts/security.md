---
description: Grundlegendes zur Entwicklung sicherer WebView2-Anwendungen
title: Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge HTML, Sicherheit
ms.openlocfilehash: e71dbe9ad98b7156d8888da074e30a96683469d5
ms.sourcegitcommit: e49b86082da884299fdd485d3311d63a7688c0d0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2020
ms.locfileid: "10755396"
---
# Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen

Das [WebView2-Steuerelement](https://docs.microsoft.com/microsoft-edge/webview2/) ermöglicht Entwicklern das Hosten von Webinhalten in ihren systemeigenen Anwendungen. Wenn Sie ordnungsgemäß verwendet werden, bietet das Hosten von Webinhalten mehrere Vorteile, beispielsweise die Verwendung einer webbasierten Benutzeroberfläche, den Zugriff auf die Features der Webplattform, das Freigeben von Code plattformübergreifend usw. Um Sicherheitsanfälligkeiten zu vermeiden, die durch das Hosten von Webinhalten entstehen können, sollten Sie Ihre WebView2-Anwendung so entwerfen, dass die Interaktionen zwischen dem Webinhalt und der Hostanwendung genau überwacht werden. 

1. Behandeln aller Webinhalte als unsicher
    - Überprüfen Sie Web-Nachrichten und Hostobjekt Parameter, bevor Sie Sie verwenden, da webnach richten und Parameterfehler Haft (unbeabsichtigt oder böswillig) sein können und die APP unerwartet verhält.
    - Überprüfen Sie immer die Herkunft des in WebView2 ausgeführten Dokuments, und bewerten Sie die Vertrauenswürdigkeit des Inhalts. 

2. Entwerfen Sie bestimmte webnachrichts-und Hostobjekt Interaktionen, anstatt generische Proxys zu verwenden.

3. Beschränken Sie die Webinhalts Funktionalität, indem Sie [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) oder [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net) wie folgt ändern:
    - `AreHostObjectsAllowed`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte auf Hostobjekte zugreifen.
    - `IsWebMessageEnabled`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte Webnachrichten in der systemeigenen Anwendung bereitstellen. 
    - Legen `IsScriptEnabled` `false` Sie auf, wenn Sie nicht erwarten, dass der Webinhalt Skripts ausführt (beispielsweise beim Anzeigen von statischen HTML-Inhalten).
    - `AreDefaultScriptDialogsEnabled`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte angezeigt werden `alert` oder `prompt` Dialogfelder angezeigt werden.

4.  Verwenden Sie `NavigationStarting` die `FrameNavigationStarting` Ereignisse und, um die Einstellungen basierend auf dem Ursprung der neuen Seite wie folgt zu aktualisieren:
    1.  Um zu verhindern, dass Ihre Anwendung zu bestimmten Seiten navigiert, verwenden Sie diese Ereignisse, um die Seiten-oder Frame Navigation zu überprüfen und dann zu blockieren. 
    2.  Wenn Sie zu einer neuen Seite navigieren, müssen Sie möglicherweise die Eigenschaftswerte in [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) oder [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net) wie oben beschrieben anpassen.

5. Verwenden Sie beim Navigieren zu einem neuen Dokument das `ContentLoading` Ereignis, um verfügbar gemachte Hostobjekte mit zu entfernen `RemoveHostObjectFromScript` . 