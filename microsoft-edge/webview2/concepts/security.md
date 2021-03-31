---
description: Grundlegendes zur Entwicklung sicherer WebView2-Anwendungen
title: Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge HTML, Sicherheit
ms.openlocfilehash: d53417cc1ac98b44565692edbaec06216f7c110b
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119002"
---
# <span data-ttu-id="a815d-104">Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="a815d-104">Best practices for developing secure WebView2 applications</span></span>  

<span data-ttu-id="a815d-105">Das [WebView2-Steuerelement][Webview2Main] ermöglicht Entwicklern das Hosten von Webinhalten in den systemeigenen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a815d-105">The [WebView2 control][Webview2Main] allows developers to host web content in the native applications.</span></span> <span data-ttu-id="a815d-106">Wenn Sie ordnungsgemäß verwendet werden, bietet das Hosten von Webinhalten mehrere Vorteile, beispielsweise die Verwendung einer webbasierten Benutzeroberfläche, den Zugriff auf die Features der Webplattform, das Freigeben von Code plattformübergreifend usw.</span><span class="sxs-lookup"><span data-stu-id="a815d-106">When used correctly, hosting web content offers several advantages, such as using web-based UI, accessing features of the web platform, sharing code cross-platform, and so on.</span></span>  <span data-ttu-id="a815d-107">Um Sicherheitsanfälligkeiten zu vermeiden, die durch das Hosten von Webinhalten entstehen können, sollten Sie Ihre WebView2-Anwendung so entwerfen, dass die Interaktionen zwischen dem Webinhalt und der Hostanwendung genau überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="a815d-107">To avoid vulnerabilities that can arise from hosting web content, make sure to design your WebView2 application to closely monitor interactions between the web content and the host application.</span></span>  

1.  <span data-ttu-id="a815d-108">Behandeln Sie alle Web-Inhalte als unsicher.</span><span class="sxs-lookup"><span data-stu-id="a815d-108">Treat all web content as insecure.</span></span>  
    *   <span data-ttu-id="a815d-109">Überprüfen Sie Web-Nachrichten und Hostobjekt Parameter, bevor Sie Sie verwenden, da Webnachrichten und Parameterfehler Haft sein können (unbeabsichtigt oder böswillig) und die APP unerwartet verhält.</span><span class="sxs-lookup"><span data-stu-id="a815d-109">Validate web messages and host object parameters before consuming each, because web messages and parameters can be malformed \(unintentionally or maliciously\) and cause the app to behave unexpectedly.</span></span>
    *   <span data-ttu-id="a815d-110">Überprüfen Sie immer die Herkunft des in WebView2 ausgeführten Dokuments, und bewerten Sie die Vertrauenswürdigkeit des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="a815d-110">Always check the origin of the document running inside WebView2 and assess the trustworthiness of the content.</span></span>  
1.  <span data-ttu-id="a815d-111">Entwerfen Sie bestimmte webnachrichts-und Hostobjekt Interaktionen, anstatt generische Proxys zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a815d-111">Design specific web messages and host object interactions instead of using generic proxies.</span></span>  
1.  <span data-ttu-id="a815d-112">Setzen Sie die folgenden Optionen, um die Webinhalts Funktionalität durch Ändern von [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] oder [CoreWebView2Settings (.net)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="a815d-112">Set the following options to restrict web content functionality by modifying [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].</span></span>  
    *   <span data-ttu-id="a815d-113">`AreHostObjectsAllowed`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte auf Hostobjekte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a815d-113">Set `AreHostObjectsAllowed` to `false`, if you do not expect the web content to access host objects.</span></span>  
    *   <span data-ttu-id="a815d-114">`IsWebMessageEnabled`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte Webnachrichten in ihrer systemeigenen Anwendung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a815d-114">Set `IsWebMessageEnabled` to `false`, if you do not expect the web content to post web messages to your native application.</span></span>  
    *   <span data-ttu-id="a815d-115">Legen `IsScriptEnabled` `false` Sie auf, wenn Sie nicht erwarten, dass die Webinhalte Skripts ausführen \(beispielsweise, wenn statischer HTML-Inhalt angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="a815d-115">Set `IsScriptEnabled` to `false`, if you do not expect the web content to run scripts \(for example, when showing static html content\).</span></span>  
    *   <span data-ttu-id="a815d-116">`AreDefaultScriptDialogsEnabled`Auf `false` , wenn Sie nicht erwarten, dass die Webinhalte angezeigt werden `alert` oder `prompt` Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a815d-116">Set `AreDefaultScriptDialogsEnabled` to `false`, if you do not expect the web content to show `alert` or `prompt` dialog boxes.</span></span>  
1.  <span data-ttu-id="a815d-117">Verwenden Sie in den folgenden Schritten die `NavigationStarting` Ereignisse und, `FrameNavigationStarting` um die Einstellungen basierend auf dem Ursprung der neuen Seite zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a815d-117">In the following steps, use the `NavigationStarting` and `FrameNavigationStarting` events to update settings based on the origin of the new page.</span></span>  
    1.  <span data-ttu-id="a815d-118">Um zu verhindern, dass Ihre Anwendung zu bestimmten Seiten navigiert, verwenden Sie die Ereignisse, um die Seiten-oder Frame Navigation zu überprüfen und dann zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="a815d-118">To prevent your application from navigating to certain pages, use the events to check and then block page or frame navigation.</span></span>  
    1.  <span data-ttu-id="a815d-119">Wenn Sie zu einer neuen Seite navigieren, müssen Sie möglicherweise die Eigenschaftswerte in [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] oder [CoreWebView2Settings (.net)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] wie zuvor beschrieben anpassen.</span><span class="sxs-lookup"><span data-stu-id="a815d-119">When navigating to a new page, you may need to adjust the property values on [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] as previously described.</span></span>  
1.  <span data-ttu-id="a815d-120">Verwenden Sie beim Navigieren zu einem neuen Dokument das `ContentLoading` Ereignis, um verfügbar gemachte Hostobjekte mit zu entfernen `RemoveHostObjectFromScript` .</span><span class="sxs-lookup"><span data-stu-id="a815d-120">When navigating to a new document, use the `ContentLoading` event to remove exposed host objects using `RemoveHostObjectFromScript`.</span></span>  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "Schnittstelle ICoreWebView2Settings | Microsoft docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "CoreWebView2Settings-Klasse (Microsoft. Web. WebView2. Core) | Microsoft docs"  
