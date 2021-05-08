---
description: Informationen zum Entwickeln sicherer WebView2-Anwendungen
title: Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html, security
ms.openlocfilehash: d53417cc1ac98b44565692edbaec06216f7c110b
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119002"
---
# Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen  

Das [WebView2-Steuerelement ermöglicht][Webview2Main] Entwicklern das Hosten von Webinhalten in den systemeigenen Anwendungen. Bei ordnungsgemäßer Verwendung bietet das Hosten von Webinhalten mehrere Vorteile, z. B. die Verwendung der webbasierten Benutzeroberfläche, den Zugriff auf Features der Webplattform, die plattformübergreifende Freigabe von Code und so weiter.  Um Sicherheitsrisiken zu vermeiden, die durch das Hosten von Webinhalten entstehen können, müssen Sie ihre WebView2-Anwendung so entwerfen, dass die Interaktionen zwischen den Webinhalten und der Hostanwendung genau überwacht werden.  

1.  Behandeln Sie alle Webinhalte als unsicher.  
    *   Überprüfen Sie Webnachrichten und Hostobjektparameter, bevor sie verwendet werden, da Webnachrichten und Parameter falsch formatiert sein können (unbeabsichtigt oder bösartig\) und dazu führen, dass sich die App unerwartet verhält.
    *   Überprüfen Sie immer den Ursprung des Dokuments, das in WebView2 ausgeführt wird, und bewerten Sie die Vertrauenswürdigkeit des Inhalts.  
1.  Entwerfen Sie bestimmte Webnachrichten und Hostobjektinteraktionen, anstatt generische Proxys zu verwenden.  
1.  Legen Sie die folgenden Optionen zum Einschränken der Webinhaltsfunktionalität durch Ändern [von ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] oder [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]bereit.  
    *   Legen Sie auf , wenn Sie nicht erwarten, dass `AreHostObjectsAllowed` der `false` Webinhalt auf Hostobjekte zu zugreifen.  
    *   Legen Sie auf , wenn Sie nicht erwarten, dass der Webinhalt Webnachrichten an Ihre `IsWebMessageEnabled` `false` systemeigene Anwendung postt.  
    *   Set `IsScriptEnabled` to , if you do not expect the web content to run scripts `false` \(for example, when showing static html content\).  
    *   Legen Sie auf , wenn Sie nicht erwarten, dass `AreDefaultScriptDialogsEnabled` der `false` Webinhalt angezeigt oder `alert` `prompt` Dialogfelder angezeigt wird.  
1.  Verwenden Sie in den folgenden Schritten die Und-Ereignisse, um Einstellungen basierend auf dem Ursprung der `NavigationStarting` `FrameNavigationStarting` neuen Seite zu aktualisieren.  
    1.  Um zu verhindern, dass Ihre Anwendung zu bestimmten Seiten navigiert, verwenden Sie die Ereignisse, um die Seiten- oder Framenavigation zu überprüfen und zu blockieren.  
    1.  Wenn Sie zu einer neuen Seite navigieren, müssen Sie möglicherweise die Eigenschaftswerte für [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] oder [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] wie zuvor beschrieben anpassen.  
1.  Wenn Sie zu einem neuen Dokument navigieren, verwenden Sie das Ereignis, um `ContentLoading` verfügbar gemachte Hostobjekte mithilfe von zu `RemoveHostObjectFromScript` entfernen.  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "Schnittstelle ICoreWebView2Settings | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "CoreWebView2Settings Class (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
