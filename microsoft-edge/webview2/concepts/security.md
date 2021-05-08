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
# <span data-ttu-id="23e4a-104">Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="23e4a-104">Best practices for developing secure WebView2 applications</span></span>  

<span data-ttu-id="23e4a-105">Das [WebView2-Steuerelement ermöglicht][Webview2Main] Entwicklern das Hosten von Webinhalten in den systemeigenen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="23e4a-105">The [WebView2 control][Webview2Main] allows developers to host web content in the native applications.</span></span> <span data-ttu-id="23e4a-106">Bei ordnungsgemäßer Verwendung bietet das Hosten von Webinhalten mehrere Vorteile, z. B. die Verwendung der webbasierten Benutzeroberfläche, den Zugriff auf Features der Webplattform, die plattformübergreifende Freigabe von Code und so weiter.</span><span class="sxs-lookup"><span data-stu-id="23e4a-106">When used correctly, hosting web content offers several advantages, such as using web-based UI, accessing features of the web platform, sharing code cross-platform, and so on.</span></span>  <span data-ttu-id="23e4a-107">Um Sicherheitsrisiken zu vermeiden, die durch das Hosten von Webinhalten entstehen können, müssen Sie ihre WebView2-Anwendung so entwerfen, dass die Interaktionen zwischen den Webinhalten und der Hostanwendung genau überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="23e4a-107">To avoid vulnerabilities that can arise from hosting web content, make sure to design your WebView2 application to closely monitor interactions between the web content and the host application.</span></span>  

1.  <span data-ttu-id="23e4a-108">Behandeln Sie alle Webinhalte als unsicher.</span><span class="sxs-lookup"><span data-stu-id="23e4a-108">Treat all web content as insecure.</span></span>  
    *   <span data-ttu-id="23e4a-109">Überprüfen Sie Webnachrichten und Hostobjektparameter, bevor sie verwendet werden, da Webnachrichten und Parameter falsch formatiert sein können (unbeabsichtigt oder bösartig\) und dazu führen, dass sich die App unerwartet verhält.</span><span class="sxs-lookup"><span data-stu-id="23e4a-109">Validate web messages and host object parameters before consuming each, because web messages and parameters can be malformed \(unintentionally or maliciously\) and cause the app to behave unexpectedly.</span></span>
    *   <span data-ttu-id="23e4a-110">Überprüfen Sie immer den Ursprung des Dokuments, das in WebView2 ausgeführt wird, und bewerten Sie die Vertrauenswürdigkeit des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="23e4a-110">Always check the origin of the document running inside WebView2 and assess the trustworthiness of the content.</span></span>  
1.  <span data-ttu-id="23e4a-111">Entwerfen Sie bestimmte Webnachrichten und Hostobjektinteraktionen, anstatt generische Proxys zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="23e4a-111">Design specific web messages and host object interactions instead of using generic proxies.</span></span>  
1.  <span data-ttu-id="23e4a-112">Legen Sie die folgenden Optionen zum Einschränken der Webinhaltsfunktionalität durch Ändern [von ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] oder [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]bereit.</span><span class="sxs-lookup"><span data-stu-id="23e4a-112">Set the following options to restrict web content functionality by modifying [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].</span></span>  
    *   <span data-ttu-id="23e4a-113">Legen Sie auf , wenn Sie nicht erwarten, dass `AreHostObjectsAllowed` der `false` Webinhalt auf Hostobjekte zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="23e4a-113">Set `AreHostObjectsAllowed` to `false`, if you do not expect the web content to access host objects.</span></span>  
    *   <span data-ttu-id="23e4a-114">Legen Sie auf , wenn Sie nicht erwarten, dass der Webinhalt Webnachrichten an Ihre `IsWebMessageEnabled` `false` systemeigene Anwendung postt.</span><span class="sxs-lookup"><span data-stu-id="23e4a-114">Set `IsWebMessageEnabled` to `false`, if you do not expect the web content to post web messages to your native application.</span></span>  
    *   <span data-ttu-id="23e4a-115">Set `IsScriptEnabled` to , if you do not expect the web content to run scripts `false` \(for example, when showing static html content\).</span><span class="sxs-lookup"><span data-stu-id="23e4a-115">Set `IsScriptEnabled` to `false`, if you do not expect the web content to run scripts \(for example, when showing static html content\).</span></span>  
    *   <span data-ttu-id="23e4a-116">Legen Sie auf , wenn Sie nicht erwarten, dass `AreDefaultScriptDialogsEnabled` der `false` Webinhalt angezeigt oder `alert` `prompt` Dialogfelder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="23e4a-116">Set `AreDefaultScriptDialogsEnabled` to `false`, if you do not expect the web content to show `alert` or `prompt` dialog boxes.</span></span>  
1.  <span data-ttu-id="23e4a-117">Verwenden Sie in den folgenden Schritten die Und-Ereignisse, um Einstellungen basierend auf dem Ursprung der `NavigationStarting` `FrameNavigationStarting` neuen Seite zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="23e4a-117">In the following steps, use the `NavigationStarting` and `FrameNavigationStarting` events to update settings based on the origin of the new page.</span></span>  
    1.  <span data-ttu-id="23e4a-118">Um zu verhindern, dass Ihre Anwendung zu bestimmten Seiten navigiert, verwenden Sie die Ereignisse, um die Seiten- oder Framenavigation zu überprüfen und zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="23e4a-118">To prevent your application from navigating to certain pages, use the events to check and then block page or frame navigation.</span></span>  
    1.  <span data-ttu-id="23e4a-119">Wenn Sie zu einer neuen Seite navigieren, müssen Sie möglicherweise die Eigenschaftswerte für [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] oder [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] wie zuvor beschrieben anpassen.</span><span class="sxs-lookup"><span data-stu-id="23e4a-119">When navigating to a new page, you may need to adjust the property values on [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] as previously described.</span></span>  
1.  <span data-ttu-id="23e4a-120">Wenn Sie zu einem neuen Dokument navigieren, verwenden Sie das Ereignis, um `ContentLoading` verfügbar gemachte Hostobjekte mithilfe von zu `RemoveHostObjectFromScript` entfernen.</span><span class="sxs-lookup"><span data-stu-id="23e4a-120">When navigating to a new document, use the `ContentLoading` event to remove exposed host objects using `RemoveHostObjectFromScript`.</span></span>  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "Schnittstelle ICoreWebView2Settings | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "CoreWebView2Settings Class (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
