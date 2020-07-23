---
description: Grundlegendes zur Entwicklung sicherer WebView2-Anwendungen
title: Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge HTML, Sicherheit
ms.openlocfilehash: f30163954f1906f71afa520b87d58c7647a5250a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894305"
---
# Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen  

Das [WebView2-Steuerelement][Webview2Main] ermöglicht Entwicklern das Hosten von Webinhalten in den systemeigenen Anwendungen. Wenn Sie ordnungsgemäß verwendet werden, bietet das Hosten von Webinhalten mehrere Vorteile, beispielsweise die Verwendung einer webbasierten Benutzeroberfläche, den Zugriff auf die Features der Webplattform, das Freigeben von Code plattformübergreifend usw.  Um Sicherheitsanfälligkeiten zu vermeiden, die durch das Hosten von Webinhalten entstehen können, sollten Sie Ihre WebView2-Anwendung so entwerfen, dass die Interaktionen zwischen dem Webinhalt und der Hostanwendung genau überwacht werden.  

1.  Behandeln Sie alle Web-Inhalte als unsicher.  
    *   Überprüfen Sie Web-Nachrichten und Hostobjekt Parameter, bevor Sie Sie verwenden, da Webnachrichten und Parameterfehler Haft sein können (unbeabsichtigt oder böswillig) und die APP unerwartet verhält.
    *   Überprüfen Sie immer die Herkunft des in WebView2 ausgeführten Dokuments, und bewerten Sie die Vertrauenswürdigkeit des Inhalts.  
1.  Entwerfen Sie bestimmte webnachrichts-und Hostobjekt Interaktionen, anstatt generische Proxys zu verwenden.  
1.  Setzen Sie die folgenden Optionen, um die Webinhalts Funktionalität durch Ändern von [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] oder [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings]zu beschränken.  
    *   `AreHostObjectsAllowed`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte auf Hostobjekte zugreifen.  
    *   `IsWebMessageEnabled`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte Webnachrichten in ihrer systemeigenen Anwendung bereitstellen.  
    *   Legen `IsScriptEnabled` `false` Sie auf, wenn Sie nicht erwarten, dass die Webinhalte Skripts ausführen \ (beispielsweise, wenn statischer HTML-Inhalt angezeigt wird).  
    *   `AreDefaultScriptDialogsEnabled`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte angezeigt werden `alert` oder `prompt` Dialogfelder angezeigt werden.  
1.  Verwenden Sie in den folgenden Schritten die `NavigationStarting` Ereignisse und, `FrameNavigationStarting` um die Einstellungen basierend auf dem Ursprung der neuen Seite zu aktualisieren.  
    1.  Um zu verhindern, dass Ihre Anwendung zu bestimmten Seiten navigiert, verwenden Sie die Ereignisse, um die Seiten-oder Frame Navigation zu überprüfen und dann zu blockieren.  
    1.  Wenn Sie zu einer neuen Seite navigieren, müssen Sie möglicherweise die Eigenschaftswerte in [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] oder [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings] wie zuvor beschrieben anpassen.  
1.  Verwenden Sie beim Navigieren zu einem neuen Dokument das `ContentLoading` Ereignis, um verfügbar gemachte Hostobjekte mit zu entfernen `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[Webview2ReferenceWin3209538Icorewebview2settings]: ../reference/win32/0-9-538/icorewebview2settings.md "Schnittstelle ICoreWebView2Settings | Microsoft docs"  

[Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings]: ../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings.md "Microsoft. Web. WebView2. Core. CoreWebView2Settings Klasse | Microsoft docs"  
