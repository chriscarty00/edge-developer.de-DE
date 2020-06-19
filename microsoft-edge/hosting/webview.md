---
description: Hosten von Webinhalten in Ihrer Windows 10-App mit dem WebView (EdgeHTML)-Steuerelement
title: Microsoft Edge WebView für Windows 10-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: x-ms-WebView, MSHTMLWebViewElement, WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: aa9bef7bf214cf4f4ffdb4d68ad3a1a86ac2977b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752206"
---
# <span data-ttu-id="cb1df-104">WebView (EdgeHTML) für Windows 10-apps</span><span class="sxs-lookup"><span data-stu-id="cb1df-104">WebView (EdgeHTML) for Windows 10 apps</span></span>  

[!INCLUDE [deprecation-note](./includes/deprecation-note.md)]  

<span data-ttu-id="cb1df-105">Das WebView (EdgeHTML)-Steuerelement ermöglicht das Hosten von Webinhalten in Ihrer Windows 10-app.</span><span class="sxs-lookup"><span data-stu-id="cb1df-105">The WebView (EdgeHTML) control enables you to host web content in your Windows 10 app.</span></span>  

<span data-ttu-id="cb1df-106">Sie können es als XAML-Element (für [universelle Windows-Plattform (UWP)-apps](/uwp/api/Windows.UI.Xaml.Controls.WebView) und [Windows Forms-und WPF-Desktopanwendungen](/windows/communitytoolkit/controls/wpf-winforms/webview)) oder als HTML-Element (x-ms-WebView)-/DOM-Objekt (MSHTMLWebViewElement) für JavaScript-basierte Windows 10-Apps verwenden, wie hier beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb1df-106">You can use it as a XAML element (for [Universal Windows Platform (UWP) apps](/uwp/api/Windows.UI.Xaml.Controls.WebView) and [Windows Forms and WPF desktop applications](/windows/communitytoolkit/controls/wpf-winforms/webview)), or an HTML element (x-ms-webview)/DOM object (MSHTMLWebViewElement) for JavaScript-based Windows 10 apps, as described here.</span></span>  

|  |  |  
|:--- |:--- |  
| [**<span data-ttu-id="cb1df-107">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="cb1df-107">Events</span></span>**](#events) | <span data-ttu-id="cb1df-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span><span class="sxs-lookup"><span data-stu-id="cb1df-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span></span> |  
| [**<span data-ttu-id="cb1df-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="cb1df-109">Methods</span></span>**](#methods) | <span data-ttu-id="cb1df-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [GoBack](#goback), [GoForward](#goforward), [Navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Aktualisieren](#refresh), [Beenden](#stop)</span><span class="sxs-lookup"><span data-stu-id="cb1df-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward](#goforward), [navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [refresh](#refresh), [stop](#stop)</span></span> |  
| [**<span data-ttu-id="cb1df-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb1df-111">Properties</span></span>**](#properties) | <span data-ttu-id="cb1df-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [Process](#process), [Settings](#settings), [src](#src), [Width](#width)</span><span class="sxs-lookup"><span data-stu-id="cb1df-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [process](#process), [settings](#settings), [src](#src), [width](#width)</span></span> |  

## <span data-ttu-id="cb1df-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb1df-113">Syntax</span></span>  

```javascript
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```  

## <span data-ttu-id="cb1df-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb1df-114">Remarks</span></span>  

### <span data-ttu-id="cb1df-115">WebView versus IFRAME</span><span class="sxs-lookup"><span data-stu-id="cb1df-115">WebView versus iframe</span></span>  

<span data-ttu-id="cb1df-116">Wie bei einem standardmäßigen HTML- [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) -Element können Sie WebView verwenden, um Remote Seiten über HTTP und lokale Seiten (*MS-AppX-Web:///*) aus Ihrem App-Paket zu laden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-116">Like a standard HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) element, you can use WebView to load remote pages over HTTP and local pages (*ms-appx-web:///*) from your app package.</span></span>  <span data-ttu-id="cb1df-117">Die WebView-Ansicht kann aber auch:</span><span class="sxs-lookup"><span data-stu-id="cb1df-117">However, the WebView can also:</span></span>  

*   <span data-ttu-id="cb1df-118">Laden von Seiten und Ressourcen aus Ihren [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) -Ordnern (lokal, Roaming, Temp) (*MS-APPDATA:///*) und [in-Memory-Streams](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)</span><span class="sxs-lookup"><span data-stu-id="cb1df-118">Load pages and resources from your [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, roaming, temp) folders (*ms-appdata:///*) and [in-memory streams](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*ms-local-stream:///*)</span></span>  
*   <span data-ttu-id="cb1df-119">Bereitstellen von Browser ähnlichen Steuerelementen: für das [zurück](#goback) gehen und [weiterleiten](#goforward) im Navigationsverlauf sowie zum [Beenden](#stop) oder [Aktualisieren](#refresh) der aktuellen Seite.</span><span class="sxs-lookup"><span data-stu-id="cb1df-119">Provide browser-like controls: for going [back](#goback) and [forward](#goforward) in navigation history, and [stopping](#stop) or [refreshing](#refresh) the current page.</span></span>  
*   <span data-ttu-id="cb1df-120">[Erfassen Sie Screenshots von Webinhalten](#capturepreviewtoblobasync) , wodurch die Implementierung des Windows 10-APP- [Freigabe](/windows/uwp/app-to-app/share-data) Vertrags einfach ist.</span><span class="sxs-lookup"><span data-stu-id="cb1df-120">[Capture screenshots of web content](#capturepreviewtoblobasync) making it easy to implement the Windows 10 app [Share](/windows/uwp/app-to-app/share-data) contract.</span></span>  
*   <span data-ttu-id="cb1df-121">Ermöglichen Sie JavaScript-Code, der in einer WebView ausgeführt wird, um benutzerdefinierte Ereignisse ([MSWebViewScriptNotify](#mswebviewscriptnotify)) für Ihre APP auszulösen, und ermöglichen Sie Ihrer APP das Ausführen von JavaScript innerhalb der WebView ([invokeScriptAsync](#invokescriptasync)).</span><span class="sxs-lookup"><span data-stu-id="cb1df-121">Allow JavaScript code running within a webview to raise custom events ([MSWebViewScriptNotify](#mswebviewscriptnotify)) to your app, and allow your app to run JavaScript within the webview ([invokeScriptAsync](#invokescriptasync)).</span></span>  
*   <span data-ttu-id="cb1df-122">Bereitstellen von optimierten WebView-Inhalts Ereignissen:</span><span class="sxs-lookup"><span data-stu-id="cb1df-122">Provide you with fine-tuned webview content events:</span></span>  
    
    | <span data-ttu-id="cb1df-123">WebView-DOM-Ereignis</span><span class="sxs-lookup"><span data-stu-id="cb1df-123">WebView DOM event</span></span> | <span data-ttu-id="cb1df-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb1df-124">Description</span></span> |  
    |:--- |:--- |  
    | [<span data-ttu-id="cb1df-125">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="cb1df-125">MSWebViewNavigationStarting</span></span>](#mswebviewnavigationstarting) | <span data-ttu-id="cb1df-126">Gibt an, dass die WebView mit der Navigation beginnt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-126">Indicates the WebView is starting to navigate.</span></span>  |  
    | [<span data-ttu-id="cb1df-127">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="cb1df-127">MSWebViewContentLoading</span></span>](#mswebviewcontentloading) | <span data-ttu-id="cb1df-128">Der HTML-Inhalt wird heruntergeladen und in das Steuerelement geladen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-128">The HTML content is downloaded and is being loaded into the control.</span></span>  |  
    | [<span data-ttu-id="cb1df-129">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="cb1df-129">MSWebViewDOMContentLoaded</span></span>](#mswebviewdomcontentloaded) | <span data-ttu-id="cb1df-130">Gibt an, dass die wichtigsten DOM-Elemente geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-130">Indicates that the main DOM elements have finished loading.</span></span>  |  
    | [<span data-ttu-id="cb1df-131">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="cb1df-131">MSWebViewNavigationCompleted</span></span>](#mswebviewnavigationcompleted) | <span data-ttu-id="cb1df-132">Gibt an, dass die Navigation abgeschlossen ist und alle Medienelemente gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-132">Indicates the navigation is complete, and all media elements are rendered.</span></span>  |  
    | [<span data-ttu-id="cb1df-133">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="cb1df-133">MSWebViewUnviewableContentIdentified</span></span>](#mswebviewunviewablecontentidentified) | <span data-ttu-id="cb1df-134">Die WebView hat festgestellt, dass der Inhalt nicht HTML war.</span><span class="sxs-lookup"><span data-stu-id="cb1df-134">The WebView found the content was not HTML.</span></span>  |  
    | [<span data-ttu-id="cb1df-135">UnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="cb1df-135">UnsafeContentWarningDisplaying</span></span>](#mswebviewunsafecontentwarningdisplaying) | <span data-ttu-id="cb1df-136">Die WebView zeigt eine Warnungsseite für Inhalte, die vom Windows-SmartScreen- *Filter*als unsicher gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-136">The WebView shows a warning page for content that was reported as unsafe by Windows *SmartScreen Filter*.</span></span>  |  
    
    <span data-ttu-id="cb1df-137">... einschließen entsprechender [Ereignisse](#events) für iframe-Inhalte, die in einer WebView geladen wurden (beispielsweise [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) usw.)</span><span class="sxs-lookup"><span data-stu-id="cb1df-137">...including corresponding [events](#events) for iframe content loaded within a WebView (such as [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) and so on).</span></span> 

### <span data-ttu-id="cb1df-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="cb1df-138">Printing</span></span>  

<span data-ttu-id="cb1df-139">Wenn eine Windows-App mit JavaScript gedruckt wird, `<x-ms-webview>` werden die Tags `<iframe>` vor dem Drucken in Tags umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-139">When a Windows app using JavaScript is printed, the `<x-ms-webview>` tags are transformed into `<iframe>` tags before printing.</span></span>  <span data-ttu-id="cb1df-140">Neben dem normalen Unterschied zwischen der Anzeige auf dem Bildschirm und dem gerenderten Ausdruck für den Druck gelten die auf Elemente angewendeten CSS-Formatvorlagen `<iframe>` dann für die `<iframe>` Transformation von `<x-ms-webview>` .</span><span class="sxs-lookup"><span data-stu-id="cb1df-140">Besides the normal difference between displaying on screen and rendered for print, CSS styles applied to `<iframe>` elements are then applicable to the `<iframe>` transformed from `<x-ms-webview>`.</span></span>  

### <span data-ttu-id="cb1df-141">Dienstmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="cb1df-141">Service workers</span></span>  

<span data-ttu-id="cb1df-142">Beginnend mit dem [2018-Update für Windows 10 Oktober](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18) [werden Dienstmitarbeiter im WebView-Steuerelement](/microsoft-edge/dev-guide#service-workers) (zusätzlich zum Microsoft Edge-Browser und Windows 10-apps mit JavaScript) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-142">Starting with the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [service workers are supported in the WebView control](/microsoft-edge/dev-guide#service-workers) (in addition to the Microsoft Edge browser and Windows 10 apps with JavaScript).</span></span>  

<span data-ttu-id="cb1df-143">x64-App-Architekturen erfordern neutrale (Any CPU)-oder x64-Pakete, da Dienstmitarbeiter in WOW64-Prozessen nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-143">x64 app architectures require Neutral (Any CPU) or x64 packages, as service workers are not supported in WoW64 processes.</span></span>  <span data-ttu-id="cb1df-144">(Um Speicherplatz zu sparen, ist die WoW-Version der erforderlichen DLLs nicht nativ in Windows enthalten.)</span><span class="sxs-lookup"><span data-stu-id="cb1df-144">(To conserve disk space, the WoW version of the required DLLs are not natively included in Windows.)</span></span>  

### <span data-ttu-id="cb1df-145">Threadingmodell und Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="cb1df-145">Threading model and reliability</span></span>  

<span data-ttu-id="cb1df-146">Durch das Erstellen einer WebView über `document.createElement("x-ms-webview")` oder über `<x-ms-webview>` Markup wird ein WebView für einen neuen eindeutigen Thread im App-Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-146">Creating a WebView via `document.createElement("x-ms-webview")` or via `<x-ms-webview>` markup creates a WebView on a new unique thread in the app's process.</span></span>  <span data-ttu-id="cb1df-147">Die Ausführung auf einem neuen eindeutigen Thread bedeutet, dass die APP oder andere Webansichten von einem WebView-Skript mit langer Laufzeit nicht hängen können.</span><span class="sxs-lookup"><span data-stu-id="cb1df-147">Running on a new unique thread means that long running script from one WebView is unable to hang the app or other WebViews.</span></span>  <span data-ttu-id="cb1df-148">Durch das Erstellen einer WebView über den `new MSWebView()` Konstruktor wird eine WebView in einem separaten WebView-Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-148">Creating a WebView via the `new MSWebView()` constructor creates a WebView in a separate WebView process.</span></span>  <span data-ttu-id="cb1df-149">Die Ausführung in einem eindeutigen Prozess bedeutet, dass die APP neben dem Schutz vor Skripts mit langer Ausführungszeit auch vor Webinhalten geschützt ist, die den WebView-Prozess abstürzen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-149">Running in a unique process means that in addition to protection from long running script, the app is also protected from web content that crashes the WebView process.</span></span>  <span data-ttu-id="cb1df-150">Durch das Erstellen einer WebView über die [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) Methode wird auch eine WebView in einem separaten Prozess erstellt, die dem Aufrufer jedoch mehr Kontrolle über Prozesseinstellungen und das Gruppieren von Webansichten in WebView-Prozessen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="cb1df-150">Creating a WebView via the [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) method also creates a WebView in a separate process but allows the caller more control over process settings and grouping WebViews in WebView processes.</span></span>  <span data-ttu-id="cb1df-151">Weitere Informationen finden Sie unter `MSWebViewProcess`.</span><span class="sxs-lookup"><span data-stu-id="cb1df-151">See `MSWebViewProcess` for more information.</span></span>  

### <span data-ttu-id="cb1df-152">WinRT-API-Zugriff</span><span class="sxs-lookup"><span data-stu-id="cb1df-152">WinRT API access</span></span>  

<span data-ttu-id="cb1df-153">Eine UWP-App kann HTML-Dokumenten in Webviews den Zugriff auf WinRT-APIs ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-153">A UWP app may allow HTML documents inside WebViews to have access to WinRT APIs.</span></span>  <span data-ttu-id="cb1df-154">Dies erfolgt über das WindowsRuntimeAccess-Attribut der untergeordneten Rule-Elemente des ApplicationContentUriRules-Elements der AppxManifest.xml der UWP-app.</span><span class="sxs-lookup"><span data-stu-id="cb1df-154">This is via the WindowsRuntimeAccess attribute of the Rule child elements of the ApplicationContentUriRules element of the AppxManifest.xml of the UWP app.</span></span>  <span data-ttu-id="cb1df-155">Wenn Sie WindowsRuntimeAccess auf "alle" und HTML-Dokumente mit übereinstimmenden URIs setzen, ist die Verwendung von WinRT zulässig.</span><span class="sxs-lookup"><span data-stu-id="cb1df-155">Set WindowsRuntimeAccess to 'all' and HTML documents with matching URIs will be allowed to use WinRT.</span></span>  <span data-ttu-id="cb1df-156">Dies entspricht dem Bereitstellen von WinRT-Zugriff auf HTML-Inhalte in JavaScript-UWP-apps, daher finden Sie weitere Informationen unter [Aufrufen von WinRT-APIs aus ihrer PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) .</span><span class="sxs-lookup"><span data-stu-id="cb1df-156">This is the same as providing WinRT access to HTML content in JavaScript UWP apps so see [Call WinRT APIs from your PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) for more information.</span></span>  

<span data-ttu-id="cb1df-157">UI-bezogene WinRT-APIs funktionieren möglicherweise nicht, wenn Sie von einer WebView aufgerufen werden, die in einem eigenen Thread ausgeführt wird, aber möglicherweise funktioniert, wenn Sie von einer WebView aufgerufen wird, die in einem</span><span class="sxs-lookup"><span data-stu-id="cb1df-157">UI related WinRT APIs may not work when called from a WebView running on its own thread but may work when called from a WebView running in a separate WebView process.</span></span>  <span data-ttu-id="cb1df-158">Bei Verwendung einer WebView in einem eigenen eindeutigen Thread ist dieser Thread nicht der Ansicht-Thread der app.</span><span class="sxs-lookup"><span data-stu-id="cb1df-158">When using a WebView on its own unique thread, that thread is not the app's view thread.</span></span>  <span data-ttu-id="cb1df-159">Einige UI-bezogene WinRT-APIs müssen aus dem Ansicht-Thread der app aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-159">Some UI related WinRT APIs require to be called from the app's view thread.</span></span>  <span data-ttu-id="cb1df-160">Webansichten, die in einem separaten WebView-Prozess erstellt wurden, werden in einem Ansicht-Thread ausgeführt und sollten daher nicht den gleichen Einschränkungen unterliegen, wie die WebView-Ausführung in einem eigenen eindeutigen Thread.</span><span class="sxs-lookup"><span data-stu-id="cb1df-160">WebViews created in a separate WebView process do run on a view thread and so should not face the same restrictions as WebView's running on their own unique thread.</span></span>  <span data-ttu-id="cb1df-161">Wenn Sie Probleme mit UI-bezogenen WinRT-APIs in einer WebView haben, stellen Sie sicher, dass Sie eine WebView in einem eigenen WebView-Prozess verwenden, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb1df-161">If you have trouble with UI related WinRT APIs in a WebView ensure that you're using a WebView in its own WebView process as described above.</span></span>  

### <span data-ttu-id="cb1df-162">AppCache-Speichereinschränkungen</span><span class="sxs-lookup"><span data-stu-id="cb1df-162">AppCache storage limitations</span></span>  

<span data-ttu-id="cb1df-163">Anwendungen, die JavaScript-Unterstützung der Anwendungs Cache-API (oder AppCache) verwenden, wie in der [HTML5-Spezifikation](https://go.microsoft.com/fwlink/p/?LinkId=228542)definiert, um Offline-Webanwendungen zu erstellen, müssen die verfügbaren Speichereinschränkungen beachten.</span><span class="sxs-lookup"><span data-stu-id="cb1df-163">Applications using JavaScript support of the Application Cache API (or AppCache), as defined in the [HTML5 specification](https://go.microsoft.com/fwlink/p/?LinkId=228542), to create offline web applications must observe available storage limitations.</span></span>  <span data-ttu-id="cb1df-164">Dies gilt insbesondere für Geräte mit wenig Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="cb1df-164">This is especially true in devices with limited memory space.</span></span>  <span data-ttu-id="cb1df-165">Die praktischen Grenzwerte für die Größe der AppCache sind immer eine Funktion des verfügbaren Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="cb1df-165">The practical limits on the size of the AppCache are always a function of available disk storage space.</span></span>  <span data-ttu-id="cb1df-166">Nachfolgend sind die allgemeinen Richtlinien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-166">The general guidelines are shown below.</span></span>  

| <span data-ttu-id="cb1df-167">Datenträgergröße</span><span class="sxs-lookup"><span data-stu-id="cb1df-167">Volume size</span></span> |<span data-ttu-id="cb1df-168">AppCache pro Domäne</span><span class="sxs-lookup"><span data-stu-id="cb1df-168">AppCache per domain</span></span> | <span data-ttu-id="cb1df-169">AppCache pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="cb1df-169">AppCache per user</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="cb1df-170">Bis zu 4 GB</span><span class="sxs-lookup"><span data-stu-id="cb1df-170">Up to 4GB</span></span> | <span data-ttu-id="cb1df-171">10MB</span><span class="sxs-lookup"><span data-stu-id="cb1df-171">10MB</span></span> | <span data-ttu-id="cb1df-172">50 MB</span><span class="sxs-lookup"><span data-stu-id="cb1df-172">50MB</span></span> |  
| <span data-ttu-id="cb1df-173">4GB bis 16GB</span><span class="sxs-lookup"><span data-stu-id="cb1df-173">4GB to 16GB</span></span> | <span data-ttu-id="cb1df-174">50 MB</span><span class="sxs-lookup"><span data-stu-id="cb1df-174">50MB</span></span> | <span data-ttu-id="cb1df-175">500MB</span><span class="sxs-lookup"><span data-stu-id="cb1df-175">500MB</span></span> |  
| <span data-ttu-id="cb1df-176">16GB bis 32 GB</span><span class="sxs-lookup"><span data-stu-id="cb1df-176">16GB to 32 GB</span></span> | <span data-ttu-id="cb1df-177">50 MB</span><span class="sxs-lookup"><span data-stu-id="cb1df-177">50MB</span></span> | <span data-ttu-id="cb1df-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="cb1df-178">1GB</span></span> |  

<span data-ttu-id="cb1df-179">Da alle Windows10-apps das gleiche AppCache-Kontingent Modell verwenden sollen, gilt die verfügbare Festplattenspeicher Beschränkung sowohl für Desktop-als auch für Telefon-apps.</span><span class="sxs-lookup"><span data-stu-id="cb1df-179">All Windows10 apps are intended to use the same AppCache quota model, so the available disk storage limitation applies to both desktop and phone apps.</span></span>  <span data-ttu-id="cb1df-180">Das ist auch eine harte Grenze, nachdem Seiten, die in **WebView** geladen wurden, 1 GB *AppCache* Speicherplatz verbraucht haben. Anforderungen für zusätzlichen *AppCache* -Speicher oberhalb dieser Grenze werden verweigert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-180">The is also a hard limit after pages loaded inside **WebView** together have consumed 1 GB of *AppCache* space; requests for additional *AppCache* storage above this limit will be denied.</span></span>  

<span data-ttu-id="cb1df-181">Weitere Informationen finden Sie unter Beispiel für ein [HTML-WebView-Steuerelement](https://go.microsoft.com/fwlink/p/?linkid=309825) und die JSBrowser, die [die WebView-Steuerelement Dokumentation nutzbar](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) macht.</span><span class="sxs-lookup"><span data-stu-id="cb1df-181">For more information, see the [HTML WebView control sample](https://go.microsoft.com/fwlink/p/?linkid=309825) and the JSBrowser's [Harnessing the WebView control](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) documentation.</span></span>  

## <span data-ttu-id="cb1df-182">Veranstaltungen</span><span class="sxs-lookup"><span data-stu-id="cb1df-182">Events</span></span>  

### <span data-ttu-id="cb1df-183">departingFocus</span><span class="sxs-lookup"><span data-stu-id="cb1df-183">departingFocus</span></span>  

<span data-ttu-id="cb1df-184">Gibt an, dass der Fokus vom **WebView** in die APP abgeht.</span><span class="sxs-lookup"><span data-stu-id="cb1df-184">Indicates focus departing from the **webview** into the app.</span></span>  <span data-ttu-id="cb1df-185">Wird ausgelöst, wenn das Dokument der obersten Ebene des Webviews Window. departFocus aufruft.</span><span class="sxs-lookup"><span data-stu-id="cb1df-185">Fires when the webview's top level document calls window.departFocus.</span></span>  <span data-ttu-id="cb1df-186">Die FocusNavigationEvent-args im departingFocus-Ereignis entsprechen den Parametern, die für departFocus bereitgestellt werden, mit der Ausnahme, dass die Ursprungs Parameter aus dem Benutzers-Koordinatenraum des Webviews in den Koordinatenbereich des WebView-Host Dokuments übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-186">The FocusNavigationEvent args in the departingFocus event match the parameters provided to departFocus except the origin parameters are translated from the webview's document's coordinate space to the coordinate space of the webview host document.</span></span>  <span data-ttu-id="cb1df-187">Weitere Informationen finden Sie unter WebView. navigateFocus-Methode und entsprechendes Window-navigatingFocus-Ereignis zum Übertragen des Fokus vom Host auf WebView.</span><span class="sxs-lookup"><span data-stu-id="cb1df-187">See the webview.navigateFocus method and corresponding window navigatingFocus event for transferring focus from host to webview.</span></span>  <span data-ttu-id="cb1df-188">Ein Beispiel für eine Implementierung der Fokusnavigation über die Tastatur oder das Gamepad, die dieses Ereignis behandelt, finden Sie in der [TVJS-Navigations Bibliothek](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .</span><span class="sxs-lookup"><span data-stu-id="cb1df-188">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that handles this event.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```  

#### <span data-ttu-id="cb1df-189">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-189">Event Information</span></span>  

|            |      |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-190">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-190">Interface</span></span>** | [<span data-ttu-id="cb1df-191">FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-191">FocusNavigationEvent</span></span>](./webview/FocusNavigationEvent.md) |  
| **<span data-ttu-id="cb1df-192">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-192">Synchronous</span></span>** | <span data-ttu-id="cb1df-193">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-193">Yes</span></span> |   
| **<span data-ttu-id="cb1df-194">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-194">Bubbles</span></span>** | <span data-ttu-id="cb1df-195">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-195">Yes</span></span> |  
| **<span data-ttu-id="cb1df-196">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-196">Cancelable</span></span>** | <span data-ttu-id="cb1df-197">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-197">No</span></span> |  

### <span data-ttu-id="cb1df-198">MSWebViewContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="cb1df-198">MSWebViewContainsFullScreenElementChanged</span></span>  

<span data-ttu-id="cb1df-199">Tritt auf, wenn sich der Status ändert, ob die **WebView** derzeit ein voll Bildelement enthält.</span><span class="sxs-lookup"><span data-stu-id="cb1df-199">Occurs when the status changes of whether or not the **webview** currently contains a full screen element.</span></span>  <span data-ttu-id="cb1df-200">Verwenden Sie die containsFullScreenElement-Eigenschaft auf den aktuellen Wert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-200">Use the containsFullScreenElement property to the current value.</span></span>  <span data-ttu-id="cb1df-201">Vollbild-Element hier bezieht sich auf den [Fullscreen-DOM-APIs](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) -Begriff eines Vollbild-Elements über die Funktionen "Element. requestFullScreen" und "Document. exitFullScreen Dom".</span><span class="sxs-lookup"><span data-stu-id="cb1df-201">Full screen element here refers to the [Fullscreen DOM APIs](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) notion of a full screen element via the element.requestFullScreen and document.exitFullScreen DOM functions.</span></span>  

```javascript
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```  

#### <span data-ttu-id="cb1df-202">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-202">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-203">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-203">Interface</span></span>** | **<span data-ttu-id="cb1df-204">Ereignis</span><span class="sxs-lookup"><span data-stu-id="cb1df-204">Event</span></span>** |  
| **<span data-ttu-id="cb1df-205">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-205">Synchronous</span></span>** | <span data-ttu-id="cb1df-206">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-206">Yes</span></span> |  
| **<span data-ttu-id="cb1df-207">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-207">Bubbles</span></span>** | <span data-ttu-id="cb1df-208">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-208">No</span></span> |   
| **<span data-ttu-id="cb1df-209">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-209">Cancelable</span></span>** | <span data-ttu-id="cb1df-210">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-210">No</span></span> |  

### <span data-ttu-id="cb1df-211">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="cb1df-211">MSWebViewContentLoading</span></span>  

<span data-ttu-id="cb1df-212">Gibt an, dass der HTML-Inhalt heruntergeladen und in das Steuerelement geladen wird.</span><span class="sxs-lookup"><span data-stu-id="cb1df-212">Indicates that the HTML content is downloaded and is being loaded into the control.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```  

#### <span data-ttu-id="cb1df-213">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-213">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-214">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-214">Interface</span></span>** | [<span data-ttu-id="cb1df-215">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-215">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="cb1df-216">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-216">Synchronous</span></span>** | <span data-ttu-id="cb1df-217">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-217">Yes</span></span>  |  
| **<span data-ttu-id="cb1df-218">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-218">Bubbles</span></span>** | <span data-ttu-id="cb1df-219">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-219">No</span></span> |   
| **<span data-ttu-id="cb1df-220">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-220">Cancelable</span></span>** | <span data-ttu-id="cb1df-221">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-221">No</span></span> |  

### <span data-ttu-id="cb1df-222">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="cb1df-222">MSWebViewDOMContentLoaded</span></span>  

<span data-ttu-id="cb1df-223">Gibt an, dass die wichtigsten DOM-Elemente geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-223">Indicates that the main DOM elements have finished loading.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```  

#### <span data-ttu-id="cb1df-224">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-224">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-225">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-225">Interface</span></span>** | [<span data-ttu-id="cb1df-226">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-226">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="cb1df-227">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-227">Synchronous</span></span>** |<span data-ttu-id="cb1df-228">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-228">Yes</span></span> |  
| **<span data-ttu-id="cb1df-229">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-229">Bubbles</span></span>** | <span data-ttu-id="cb1df-230">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-230">No</span></span> |  
| **<span data-ttu-id="cb1df-231">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-231">Cancelable</span></span>** | <span data-ttu-id="cb1df-232">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-232">No</span></span> |   

### <span data-ttu-id="cb1df-233">MSWebViewFrameContentLoading</span><span class="sxs-lookup"><span data-stu-id="cb1df-233">MSWebViewFrameContentLoading</span></span>  

<span data-ttu-id="cb1df-234">Gibt an, dass der HTML-Inhalt heruntergeladen und in das `<iframe>` Steuerelement geladen wird.</span><span class="sxs-lookup"><span data-stu-id="cb1df-234">Indicates that the HTML content downloaded and is being loaded into the `<iframe>` control.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```  

#### <span data-ttu-id="cb1df-235">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-235">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-236">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-236">Interface</span></span>** | [<span data-ttu-id="cb1df-237">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-237">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="cb1df-238">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-238">Synchronous</span></span>** | <span data-ttu-id="cb1df-239">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-239">Yes</span></span> |  
| **<span data-ttu-id="cb1df-240">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-240">Bubbles</span></span>** | <span data-ttu-id="cb1df-241">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-241">No</span></span> |  
| **<span data-ttu-id="cb1df-242">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-242">Cancelable</span></span>** | <span data-ttu-id="cb1df-243">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-243">No</span></span> |   

### <span data-ttu-id="cb1df-244">MSWebViewFrameDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="cb1df-244">MSWebViewFrameDOMContentLoaded</span></span>  

<span data-ttu-id="cb1df-245">Gibt an, dass die wichtigsten DOM-Elemente das Laden in `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="cb1df-245">Indicates that the main DOM elements have finished loading in the `<iframe>`.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```  

#### <span data-ttu-id="cb1df-246">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-246">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-247">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-247">Interface</span></span>** | [<span data-ttu-id="cb1df-248">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-248">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="cb1df-249">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-249">Synchronous</span></span>** | <span data-ttu-id="cb1df-250">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-250">Yes</span></span> |  
| **<span data-ttu-id="cb1df-251">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-251">Bubbles</span></span>** | <span data-ttu-id="cb1df-252">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-252">No</span></span> |   
| **<span data-ttu-id="cb1df-253">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-253">Cancelable</span></span>** | <span data-ttu-id="cb1df-254">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-254">No</span></span> |  

### <span data-ttu-id="cb1df-255">MSWebViewFrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="cb1df-255">MSWebViewFrameNavigationCompleted</span></span>  

<span data-ttu-id="cb1df-256">Gibt an, dass die Navigation abgeschlossen ist und alle Medienelemente in der gerendert werden `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="cb1df-256">Indicates the navigation is complete, and all media elements are rendered in the `<iframe>`.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```  

#### <span data-ttu-id="cb1df-257">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-257">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-258">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-258">Interface</span></span>** | [<span data-ttu-id="cb1df-259">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-259">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |  
| **<span data-ttu-id="cb1df-260">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-260">Synchronous</span></span>** | <span data-ttu-id="cb1df-261">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-261">Yes</span></span> |  
| **<span data-ttu-id="cb1df-262">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-262">Bubbles</span></span>** | <span data-ttu-id="cb1df-263">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-263">No</span></span> |   
| **<span data-ttu-id="cb1df-264">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-264">Cancelable</span></span>** | <span data-ttu-id="cb1df-265">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-265">No</span></span> |  

### <span data-ttu-id="cb1df-266">MSWebViewFrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="cb1df-266">MSWebViewFrameNavigationStarting</span></span>  

<span data-ttu-id="cb1df-267">Gibt an `<iframe>` , dass eine innerhalb einer **WebView** beginnt, zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="cb1df-267">Indicates a `<iframe>` within a **webview** is starting to navigate.</span></span>  <span data-ttu-id="cb1df-268">Dieser wird ausgelöst, bevor Ressourcen aus dem Netzwerk für die Navigation abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-268">This is fired before obtaining any resources from the network for the navigation.</span></span>  <span data-ttu-id="cb1df-269">Die Navigation wird erst gestartet, wenn alle MSWebViewFrameNavigationStarting-Ereignishandler abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="cb1df-269">The navigation is not started until all MSWebViewFrameNavigationStarting event handlers complete.</span></span>  <span data-ttu-id="cb1df-270">Dieses Ereignis kann über einen Anruf abgebrochen werden `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="cb1df-270">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span>  <span data-ttu-id="cb1df-271">Wenn die Ansicht abgebrochen wird, wird die Navigation nicht durch die WebView ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-271">If cancelled, the WebView will not perform the navigation.</span></span>  

```javascript
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```  

#### <span data-ttu-id="cb1df-272">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-272">Event Information</span></span>  

|  |  |
|:--- |:--- |  
| **<span data-ttu-id="cb1df-273">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-273">Interface</span></span>** | [<span data-ttu-id="cb1df-274">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-274">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="cb1df-275">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-275">Synchronous</span></span>** | <span data-ttu-id="cb1df-276">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-276">Yes</span></span> |  
| **<span data-ttu-id="cb1df-277">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-277">Bubbles</span></span>** |<span data-ttu-id="cb1df-278">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-278">No</span></span> |   
| **<span data-ttu-id="cb1df-279">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-279">Cancelable</span></span>** | <span data-ttu-id="cb1df-280">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-280">Yes</span></span> |  

### <span data-ttu-id="cb1df-281">MSWebViewLongRunningScriptDetected</span><span class="sxs-lookup"><span data-stu-id="cb1df-281">MSWebViewLongRunningScriptDetected</span></span>  

<span data-ttu-id="cb1df-282">Tritt in regelmäßigen Abständen während einer unterbrechungsfreien Skriptausführung in der **WebView**auf, sodass Sie das Skript anhalten können.</span><span class="sxs-lookup"><span data-stu-id="cb1df-282">Occurs periodically during uninterrupted script execution in the **webview**, letting you halt the script.</span></span>  

```javascript
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```  

#### <span data-ttu-id="cb1df-283">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-283">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-284">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-284">Interface</span></span>** | [<span data-ttu-id="cb1df-285">LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-285">LongRunningScriptDetectedEvent</span></span>](./webview/LongRunningScriptDetectedEvent.md) |  
| **<span data-ttu-id="cb1df-286">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-286">Synchronous</span></span>** | <span data-ttu-id="cb1df-287">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-287">Yes</span></span> |  
| **<span data-ttu-id="cb1df-288">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-288">Bubbles</span></span>** | <span data-ttu-id="cb1df-289">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-289">No</span></span> |  
| **<span data-ttu-id="cb1df-290">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-290">Cancelable</span></span>** | <span data-ttu-id="cb1df-291">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-291">No</span></span> |  

### <span data-ttu-id="cb1df-292">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="cb1df-292">MSWebViewNavigationCompleted</span></span>  

<span data-ttu-id="cb1df-293">Gibt an, dass die Navigation abgeschlossen ist und alle Medienelemente gerendert werden oder ein Navigationsfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cb1df-293">Indicates the navigation is complete, and all media elements are rendered or there was a navigation error.</span></span>  <span data-ttu-id="cb1df-294">Überprüfen Sie die Eigenschaft Event args issuccess, um zu ermitteln, ob die Navigation erfolgreich war, und die webErrorStatus-Eigenschaft, um Details zum Navigationsfehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-294">Check the event args isSuccess property to tell if the navigation was successful and the webErrorStatus property for details on the navigation error.</span></span>  <span data-ttu-id="cb1df-295">Navigationsfehler können auftreten, bevor Inhalte aus dem Netzwerk abgerufen werden, beispielsweise, wenn der Hostname eines URIs nicht aufgelöst wird, wobei das MSWebViewNavigationStarted-Ereignis ausgelöst wird, gefolgt vom MSWebViewNavigationCompleted-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cb1df-295">Navigation errors can occur before obtaining any content from the network for instance if the hostname of a URI does not resolve in which case the MSWebViewNavigationStarted event will fire followed by the MSWebViewNavigationCompleted event.</span></span>  <span data-ttu-id="cb1df-296">Navigationsfehler können auch auftreten, nachdem eine Fehlerseite von einem Webserver empfangen wurde, beispielsweise eine 404-Seite von einem HTTP-Server, in dem alle Navigationsereignisse ausgelöst werden, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded und dann MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="cb1df-296">Navigation errors may also occur after receiving an error page from a web server, for instance a 404 page from an HTTP server in which case all navigation events will fire, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, and then MSWebViewNavigationCompleted.</span></span>  <span data-ttu-id="cb1df-297">Wenn Sie eine Fehlerseite für die APP-Navigation für Fälle bereitstellen möchten, in denen der Webserver keine Fehlerseite bereitgestellt hat, müssen Sie überprüfen, ob MSWebViewContentLoading nicht für eine fehlerhafte Navigation ausgelöst wurde, die angibt, dass keine Fehlerseite für den Server bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cb1df-297">To provide an app navigation error page for cases where the web server hasn't provided an error page, you'll need to check if MSWebViewContentLoading hasn't fired for a failed navigation which indicates there is no server provided error page.</span></span>  

```javascript
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```  

#### <span data-ttu-id="cb1df-298">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-298">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-299">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-299">Interface</span></span>** | [<span data-ttu-id="cb1df-300">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-300">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |  
| **<span data-ttu-id="cb1df-301">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-301">Synchronous</span></span>** | <span data-ttu-id="cb1df-302">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-302">Yes</span></span> |  
| **<span data-ttu-id="cb1df-303">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-303">Bubbles</span></span>** | <span data-ttu-id="cb1df-304">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-304">No</span></span> |   
| **<span data-ttu-id="cb1df-305">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-305">Cancelable</span></span>** | <span data-ttu-id="cb1df-306">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-306">No</span></span> |  

### <span data-ttu-id="cb1df-307">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="cb1df-307">MSWebViewNavigationStarting</span></span>  

<span data-ttu-id="cb1df-308">Gibt an, dass die **WebView** mit der Navigation beginnt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-308">Indicates the **webview** is starting to navigate.</span></span>  <span data-ttu-id="cb1df-309">Dieser wird ausgelöst, bevor Ressourcen aus dem Netzwerk für die Navigation abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-309">This is fired before obtaining any resources from the network for the navigation.</span></span>  <span data-ttu-id="cb1df-310">Die Navigation wird erst gestartet, wenn alle MSWebViewNavigationStarting-Ereignishandler abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="cb1df-310">The navigation is not started until all MSWebViewNavigationStarting event handlers complete.</span></span>  <span data-ttu-id="cb1df-311">Dieses Ereignis kann über einen Anruf abgebrochen werden `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="cb1df-311">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span>  <span data-ttu-id="cb1df-312">Wenn die Ansicht abgebrochen wird, wird die Navigation nicht durch die WebView ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-312">If cancelled, the WebView will not perform the navigation.</span></span>  

```javascript
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```  

#### <span data-ttu-id="cb1df-313">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-313">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-314">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-314">Interface</span></span>** | [<span data-ttu-id="cb1df-315">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-315">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="cb1df-316">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-316">Synchronous</span></span>** | <span data-ttu-id="cb1df-317">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-317">No</span></span> |  
| **<span data-ttu-id="cb1df-318">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-318">Bubbles</span></span>** | <span data-ttu-id="cb1df-319">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-319">Yes</span></span> |   
| **<span data-ttu-id="cb1df-320">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-320">Cancelable</span></span>** | <span data-ttu-id="cb1df-321">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-321">Yes</span></span> |  

### <span data-ttu-id="cb1df-322">MSWebViewNewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="cb1df-322">MSWebViewNewWindowRequested</span></span>  

<span data-ttu-id="cb1df-323">Wird ausgelöst, wenn der Inhalt in **WebView** versucht, ein neues Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-323">Raised when content in **webview** is trying to open a new window.</span></span>  <span data-ttu-id="cb1df-324">Wenn das Ereignis nicht abgebrochen wird, startet WebView den URI der neuen Fenster Anforderung im Standardbrowser des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="cb1df-324">If the event isn't cancelled the webview will launch the URI of the new window request in the user's default browser.</span></span>  

```javascript
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```  

#### <span data-ttu-id="cb1df-325">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-325">Event Information</span></span>  

|  |  |  
|:---|:--- |  
| **<span data-ttu-id="cb1df-326">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-326">Interface</span></span>** | [<span data-ttu-id="cb1df-327">NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="cb1df-327">NavigationEventWithReferrer</span></span>](./webview/NavigationEventWithReferrer.md) |  
| **<span data-ttu-id="cb1df-328">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-328">Synchronous</span></span>** | <span data-ttu-id="cb1df-329">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-329">Yes</span></span> |  
| **<span data-ttu-id="cb1df-330">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-330">Bubbles</span></span>** | <span data-ttu-id="cb1df-331">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-331">No</span></span> |  
| **<span data-ttu-id="cb1df-332">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-332">Cancelable</span></span>** | <span data-ttu-id="cb1df-333">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-333">Yes</span></span> |  

### <span data-ttu-id="cb1df-334">MSWebViewPermissionRequested</span><span class="sxs-lookup"><span data-stu-id="cb1df-334">MSWebViewPermissionRequested</span></span>  

<span data-ttu-id="cb1df-335">Gibt an, dass der Inhalt in der **WebView** auf Funktionen (wie Geolocation oder Pointer Lock Access) zugreifen soll, für die normalerweise Endbenutzerberechtigungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cb1df-335">Indicates that content in the **webview**  is trying to access functionality (such as geolocation, or pointer lock access) that normally requires end-user permissions.</span></span>  <span data-ttu-id="cb1df-336">Wenn kein Ereignishandler registriert ist oder der Ereignishandler EventArgs. permissionRequest. allow (), verzögern () oder DENY () nicht aufruft, wird standardmäßig die Berechtigungsanforderung abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-336">If no event handler is registered or if the event handler doesn't call eventArgs.permissionRequest.allow(), defer(), or deny(), then by default the permission request will be denied.</span></span>  <span data-ttu-id="cb1df-337">Wenn Sie entscheiden müssen, ob die Berechtigung zum Beispiel asynchron zugelassen oder verweigert wird, wenn Sie den Benutzer auffordern müssen, verwenden Sie EventArgs. permissionRequest. verzögern ().</span><span class="sxs-lookup"><span data-stu-id="cb1df-337">If you need to decide if permission is allowed or denied asynchronously for instance if you need to prompt the user, use eventArgs.permissionRequest.defer().</span></span>  <span data-ttu-id="cb1df-338">Die Berechtigungsanforderung wird verzögert, bis Sie WebView. getDeferredPermissionRequestById oder WebView. getDeferredPermissionRequests verwenden und Allow () oder DENY () auf dem DeferredPermissionRequest mit dem entsprechenden ID-Wert aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-338">The permission request will be deferred until you use webview.getDeferredPermissionRequestById or webview.getDeferredPermissionRequests and call allow() or deny() on the DeferredPermissionRequest with the corresponding id value.</span></span>  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```  

#### <span data-ttu-id="cb1df-339">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-339">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-340">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-340">Interface</span></span>** | [<span data-ttu-id="cb1df-341">PermissionRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-341">PermissionRequestedEvent</span></span>](./webview/PermissionRequestedEvent.md) |  
| **<span data-ttu-id="cb1df-342">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-342">Synchronous</span></span>** | <span data-ttu-id="cb1df-343">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-343">Yes</span></span> |  
| **<span data-ttu-id="cb1df-344">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-344">Bubbles</span></span>** | <span data-ttu-id="cb1df-345">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-345">No</span></span> |   
| **<span data-ttu-id="cb1df-346">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-346">Cancelable</span></span>** | <span data-ttu-id="cb1df-347">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-347">No</span></span> |  

### <span data-ttu-id="cb1df-348">MSWebViewProcessExited</span><span class="sxs-lookup"><span data-stu-id="cb1df-348">MSWebViewProcessExited</span></span>  

<span data-ttu-id="cb1df-349">Gibt an, dass der **WebView** -Komponenten Prozess abstürzte.</span><span class="sxs-lookup"><span data-stu-id="cb1df-349">Indicates that the **webview** component process crashsed.</span></span>  <span data-ttu-id="cb1df-350">Dies ist nur für eine Out-of-Process-WebView relevant.</span><span class="sxs-lookup"><span data-stu-id="cb1df-350">This is only relevant for an out-of-process WebView.</span></span>  <span data-ttu-id="cb1df-351">Im Abschnitt "Hinweise" finden Sie Informationen zum Erstellen einer Out-of-Process-WebView im Gegensatz zu einer in-Process-WebView.</span><span class="sxs-lookup"><span data-stu-id="cb1df-351">See the Remarks section for how to create an out-of-process WebView as opposed to an in-process WebView.</span></span>  <span data-ttu-id="cb1df-352">Nachdem dieses Ereignis ausgelöst wurde, wird die entsprechende WebView in einen abgestürzten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-352">After this event fires, the corresponding WebView is put into a crashed state.</span></span>  <span data-ttu-id="cb1df-353">Beim Aufrufen der meisten WebView-spezifischen Methoden oder beim Zugriff auf die meisten WebView-spezifischen Eigenschaften einer abgestürzten WebView wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cb1df-353">Calling most WebView specific methods or accessing most WebView specific properties on a crashed WebView will throw an exception.</span></span>  <span data-ttu-id="cb1df-354">Wenn Sie dieses Ereignis wiederherstellen möchten, entfernen Sie den abgestürzten WebView aus dem Dom, und ersetzen Sie ihn durch einen neuen WebView.</span><span class="sxs-lookup"><span data-stu-id="cb1df-354">To recover from this event, remove the crashed WebView from the DOM and replace it with a new WebView.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```  

#### <span data-ttu-id="cb1df-355">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-355">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-356">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-356">Interface</span></span>** | **<span data-ttu-id="cb1df-357">Ereignis</span><span class="sxs-lookup"><span data-stu-id="cb1df-357">Event</span></span>** |  
| **<span data-ttu-id="cb1df-358">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-358">Synchronous</span></span>** | <span data-ttu-id="cb1df-359">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-359">Yes</span></span> |  
| **<span data-ttu-id="cb1df-360">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-360">Bubbles</span></span>** | <span data-ttu-id="cb1df-361">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-361">No</span></span> |   
| **<span data-ttu-id="cb1df-362">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-362">Cancelable</span></span>** | <span data-ttu-id="cb1df-363">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-363">No</span></span> |  

### <span data-ttu-id="cb1df-364">MSWebViewWebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="cb1df-364">MSWebViewWebResourceRequested</span></span>  

<span data-ttu-id="cb1df-365">Wird ausgelöst, wenn eine Seite im **WebView** -Element eine Ressource anfordert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-365">Raised when a page inside the **webview** element requests a resource.</span></span>  

```javascript
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```  

#### <span data-ttu-id="cb1df-366">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-366">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-367">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-367">Interface</span></span>** | [<span data-ttu-id="cb1df-368">WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-368">WebResourceRequestedEvent</span></span>](./webview/WebResourceRequestedEvent.md) |  
| **<span data-ttu-id="cb1df-369">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-369">Synchronous</span></span>** | <span data-ttu-id="cb1df-370">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-370">Yes</span></span> |  
| **<span data-ttu-id="cb1df-371">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-371">Bubbles</span></span>** | <span data-ttu-id="cb1df-372">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-372">No</span></span> |   
| **<span data-ttu-id="cb1df-373">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-373">Cancelable</span></span>** | <span data-ttu-id="cb1df-374">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-374">No</span></span> |  


### <span data-ttu-id="cb1df-375">MSWebViewScriptNotify</span><span class="sxs-lookup"><span data-stu-id="cb1df-375">MSWebViewScriptNotify</span></span>  

<span data-ttu-id="cb1df-376">Wird ausgelöst, wenn eine Seite im **WebView** -Element die **Window. external. Notify** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="cb1df-376">Raised when a page inside the **webview** element calls the **window.external.notify** method.</span></span>  <span data-ttu-id="cb1df-377">Die Window. external. Notify-Methode steht nur für Dokumente mit URIs zur Verfügung, die den Regeln im manifest's-ApplicationContentUriRules der App entsprechen oder durch Festlegen von WebView. Settings. isScriptNotifyAllowed auf true xxxxxxxxxxxxxxx zugelassen wurden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-377">The window.external.notify method is only available to documents with URIs that match rules in the app's manifest's ApplicationContentUriRules or that has been programatically allowed via setting webview.settings.isScriptNotifyAllowed to true.</span></span>  <span data-ttu-id="cb1df-378">Darüber hinaus steht Window. external. Notify nur für das Dokument der obersten Ebene von WebView zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cb1df-378">Additionally window.external.notify is only available to the webview's top level document.</span></span>  

```javascript
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```  

#### <span data-ttu-id="cb1df-379">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-379">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-380">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-380">Interface</span></span>** | [<span data-ttu-id="cb1df-381">ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-381">ScriptNotifyEvent</span></span>](./webview/ScriptNotifyEvent.md) |  
| **<span data-ttu-id="cb1df-382">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-382">Synchronous</span></span>** | <span data-ttu-id="cb1df-383">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-383">Yes</span></span> |  
| **<span data-ttu-id="cb1df-384">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-384">Bubbles</span></span>** | <span data-ttu-id="cb1df-385">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-385">No</span></span> |  
| **<span data-ttu-id="cb1df-386">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-386">Cancelable</span></span>** | <span data-ttu-id="cb1df-387">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-387">No</span></span> |  

### <span data-ttu-id="cb1df-388">MSWebViewUnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="cb1df-388">MSWebViewUnsafeContentWarningDisplaying</span></span>  

<span data-ttu-id="cb1df-389">Tritt auf, wenn die **WebView** eine Warnungsseite für Inhalte anzeigt, die vom SmartScreen-Filter als unsicher gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-389">Occurs when the **webview** shows a warning page for content that was reported as unsafe by SmartScreen Filter.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```  

#### <span data-ttu-id="cb1df-390">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-390">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-391">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-391">Interface</span></span>** | **<span data-ttu-id="cb1df-392">Ereignis</span><span class="sxs-lookup"><span data-stu-id="cb1df-392">Event</span></span>** |  
| **<span data-ttu-id="cb1df-393">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-393">Synchronous</span></span>** |<span data-ttu-id="cb1df-394">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-394">Yes</span></span> |  
| **<span data-ttu-id="cb1df-395">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-395">Bubbles</span></span>** |<span data-ttu-id="cb1df-396">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-396">No</span></span> |   
| **<span data-ttu-id="cb1df-397">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-397">Cancelable</span></span>** |<span data-ttu-id="cb1df-398">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-398">No</span></span> |  

### <span data-ttu-id="cb1df-399">MSWebViewUnsupportedUriSchemeIdentified</span><span class="sxs-lookup"><span data-stu-id="cb1df-399">MSWebViewUnsupportedUriSchemeIdentified</span></span>  

<span data-ttu-id="cb1df-400">Wird ausgelöst, wenn die Navigation zu einem Uniform Resource Identifier (URI) erfolgt, den die **WebView** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-400">Raised when there is navigation to an Uniform Resource Identifier (URI) that the **webview** does not support.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```  

#### <span data-ttu-id="cb1df-401">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-401">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-402">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-402">Interface</span></span>** | [<span data-ttu-id="cb1df-403">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-403">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="cb1df-404">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-404">Synchronous</span></span>** | <span data-ttu-id="cb1df-405">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-405">Yes</span></span> |  
| **<span data-ttu-id="cb1df-406">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-406">Bubbles</span></span>** | <span data-ttu-id="cb1df-407">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-407">No</span></span> |  
| **<span data-ttu-id="cb1df-408">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-408">Cancelable</span></span>** | <span data-ttu-id="cb1df-409">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-409">Yes</span></span> |  

### <span data-ttu-id="cb1df-410">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="cb1df-410">MSWebViewUnviewableContentIdentified</span></span>  

<span data-ttu-id="cb1df-411">Wird ausgelöst, wenn die **WebView** versucht, zu Webinhalten mit einem nicht unterstützten Inhaltstyp zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="cb1df-411">Raised when the **webview** attempts to navigate to web content with an unsupported content type.</span></span>  <span data-ttu-id="cb1df-412">Beispielsweise werden PDF-Dateien zurzeit nicht von WebView unterstützt, und die Navigation zu PDF-Dokumenten wird nicht durch navigiert und stattdessen dieses Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cb1df-412">For example, PDFs are currently not supported by webview and navigations to PDF documents will not navigate and instead raise this event.</span></span>  

```javascript
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```  

#### <span data-ttu-id="cb1df-413">Ereignisinformationen</span><span class="sxs-lookup"><span data-stu-id="cb1df-413">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-414">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-414">Interface</span></span>** | [<span data-ttu-id="cb1df-415">UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="cb1df-415">UnviewableContentIdentifiedEvent</span></span>](./webview/UnviewableContentIdentifiedEvent.md) |  
| **<span data-ttu-id="cb1df-416">Synchron</span><span class="sxs-lookup"><span data-stu-id="cb1df-416">Synchronous</span></span>** | <span data-ttu-id="cb1df-417">Ja</span><span class="sxs-lookup"><span data-stu-id="cb1df-417">Yes</span></span> |  
| **<span data-ttu-id="cb1df-418">Blasen</span><span class="sxs-lookup"><span data-stu-id="cb1df-418">Bubbles</span></span>** | <span data-ttu-id="cb1df-419">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-419">No</span></span> |   
| **<span data-ttu-id="cb1df-420">Abbrechbar</span><span class="sxs-lookup"><span data-stu-id="cb1df-420">Cancelable</span></span>** | <span data-ttu-id="cb1df-421">Nein</span><span class="sxs-lookup"><span data-stu-id="cb1df-421">No</span></span> |  

## <span data-ttu-id="cb1df-422">Methoden</span><span class="sxs-lookup"><span data-stu-id="cb1df-422">Methods</span></span>  

### <span data-ttu-id="cb1df-423">addWebAllowedObject</span><span class="sxs-lookup"><span data-stu-id="cb1df-423">addWebAllowedObject</span></span>  

<span data-ttu-id="cb1df-424">Fügt ein systemeigenes Windows-Runtime-Objekt als globalen Parameter zum Dokument auf oberster Ebene innerhalb einer **WebView**hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb1df-424">Adds a native Windows Runtime object as a global parameter to the top-level document inside of a **webview**.</span></span>  

<span data-ttu-id="cb1df-425">Das Objekt wird nicht in das aktuelle Dokument eingefügt, sondern eher auf das nächste Dokument der obersten Ebene, in das die WebView navigiert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-425">The object is not injected into the current document, but rather the next top-level document to which the webview navigates.</span></span>  <span data-ttu-id="cb1df-426">Das Objekt wird eingefügt, bevor ein Skript aus dem HTML-Dokument ausgeführt wird, damit Sie sich auf das Objekt im globalen Skript Ihres Dokuments verlassen können.</span><span class="sxs-lookup"><span data-stu-id="cb1df-426">The object is injected before any script from the HTML document runs so you can rely on the object in your document's global script.</span></span>  

<span data-ttu-id="cb1df-427">Sie sollten addWebAllowedObject entweder während eines MSWebViewNavigationStarting-Ereignisses oder vor dem expliziten Aufrufen einer Navigate-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-427">You should use addWebAllowedObject either during an MSWebViewNavigationStarting event or before explicitly calling a navigate method.</span></span>  <span data-ttu-id="cb1df-428">In diesen Fällen wird das Objekt in das Dokument der entsprechenden Navigation eingefügt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-428">In these cases the object is injected into the document of the corresponding navigation.</span></span>  <span data-ttu-id="cb1df-429">Wenn Sie es in einem anderen Kontext aufrufen, können Sie nicht sicher sein, in welches Dokument Sie Ihr Objekt einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="cb1df-429">Calling it in some other context, you don't have a way to be certain into what document you'll inject your object.</span></span>  

<span data-ttu-id="cb1df-430">Wenn Sie addWebAllowedObject mehrmals hintereinander aufrufen, werden mehrere Objekte in das Dokument eingefügt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-430">Calling addWebAllowedObject multiple times in a row will inject multiple objects into the document.</span></span>  <span data-ttu-id="cb1df-431">Wenn Sie beide vor einem expliziten Navigate-Aufruf und dann erneut während des entsprechenden MSWebViewNavigationStarting-Ereignisses aufrufen, sind beide Aufrufe erfolgreich, und es werden mehrere Objekte eingefügt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-431">If you call it both before an explicit navigate call and then again during the corresponding MSWebViewNavigationStarting event, both calls will succeed and you'll have multiple objects injected.</span></span>  <span data-ttu-id="cb1df-432">Wenn Sie mehrere Male mit dem gleichen Namen-Parameter anrufen, werden der letzte Anruf WINS und die vorherigen Anrufe mit diesem Namen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-432">If you call multiple times with the same name parameter, the last call wins and the previous calls with that name are ignored.</span></span>  

<span data-ttu-id="cb1df-433">Wenn ein Navigate fehlschlägt oder umgeleitet wird, werden die addWebAllowedObject-Aufrufe für diese Navigation ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-433">If a navigate fails or is redirected, the addWebAllowedObject calls for that navigation are ignored.</span></span>  <span data-ttu-id="cb1df-434">Wenn Sie Umleitungen behandeln möchten, können Sie die MSWebViewNavigationStarting-Ereignisüberwachung für Umleitungen abonnieren und addWebAllowedObject entsprechend den für Ihre Anwendung geeigneten Kriterien wieder aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-434">If you want to handle redirects you can subscribe to the MSWebViewNavigationStarting event watch for redirects and call addWebAllowedObject again according to whatever criteria is appropriate for your application.</span></span>  <span data-ttu-id="cb1df-435">Auch wenn ein Dokument alle Objekte, die über addWebAllowedObject für dieses Dokument injiziert wurden, entfernt, wird es nicht zum nächsten Dokument weitergeleitet, und Sie müssen addWebAllowedObject explizit aufrufen, wenn Sie diese übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="cb1df-435">Similarly, once a document navigates away any objects injected via addWebAllowedObject for that document will not carry over to the next document and you'll need to explicitly call addWebAllowedObject if you want them to carry over.</span></span>  

<span data-ttu-id="cb1df-436">Wenn Sie addWebAllowedObject für ein Dokument aufrufen, das ansonsten keinen WinRT-Zugriff hat, oder wenn es [AllowForWebOnly Zugriff über ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) hat, wird das Objekt nur injiziert, wenn das Objekt das Windows. Foundation. Metadata. AllowForWeb-Metadatenattribute-Attribut aufweist.</span><span class="sxs-lookup"><span data-stu-id="cb1df-436">If you call addWebAllowedObject for a document that has no WinRT access otherwise, or if it has [AllowForWebOnly access via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) then the object will only be injected if the object has the Windows.Foundation.Metadata.AllowForWeb metadata attribute.</span></span>  <span data-ttu-id="cb1df-437">Andernfalls schlägt die Injektion fehl, und ein Fehler wird an die JavaScript-Entwicklerkonsole gemeldet.</span><span class="sxs-lookup"><span data-stu-id="cb1df-437">Otherwise injection will fail and an error will be reported to the JavaScript developer console.</span></span>  <span data-ttu-id="cb1df-438">Wenn Sie für ein Dokument mit voll WinRT Zugriff aufgerufen wird, wird das Objekt unabhängig vom AllowForWeb-Attribut eingefügt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-438">If called on a document that has full WinRT access, then the object will be injected regardless of the AllowForWeb attribute.</span></span>  

<span data-ttu-id="cb1df-439">Darüber hinaus muss das Objekt die IAgileObject-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="cb1df-439">Additionally, the object must implement the IAgileObject interface.</span></span>  <span data-ttu-id="cb1df-440">Dies liegt daran, dass die XAML-und HTML-WebView-Elemente in den AStA-Ansicht-Threads Ihrer app ausgeführt werden und der JavaScript-Thread der WebView ein anderer Asta-Thread ist, und wir möchten App-Entwickler ermutigen, sicherzustellen, dass Ihr Objekt auf dem JavaScript-Thread ausgeführt werden kann, ohne den App-Ansichts Thread nach Möglichkeit zu blockieren</span><span class="sxs-lookup"><span data-stu-id="cb1df-440">This is because the XAML and HTML webview elements run on their app's ASTA view threads and the WebView's JavaScript thread is a different ASTA thread and we want to encourage app developers to ensure their object can run on the JavaScript thread without blocking the app view thread if possible.</span></span>  

<span data-ttu-id="cb1df-441">Der Name-Parameter muss ein gültiger JavaScript-Eigenschaftsname sein, da andernfalls der Aufruf automatisch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-441">The name parameter must be a valid JavaScript property name otherwise the call will fail silently.</span></span>  <span data-ttu-id="cb1df-442">Wenn der Name einer Eigenschaft entspricht, die bereits im globalen Objekt vorhanden ist, wird diese Eigenschaft überschrieben, wenn die Eigenschaft konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb1df-442">If the name is of a property that already exists on the global object then that property is overwritten if the property is configurable.</span></span>  <span data-ttu-id="cb1df-443">Nicht konfigurierbare Eigenschaften für das globale Objekt werden nicht überschrieben, und der addWebAllowedObject-Aufruf verfällt automatisch.</span><span class="sxs-lookup"><span data-stu-id="cb1df-443">Non-configurable properties on the global object are not overwritten and the addWebAllowedObject call fails silently.</span></span>  <span data-ttu-id="cb1df-444">JavaScript-Eigenschaften, die über addWebAllowedObject erstellt wurden, sind beschreibbar, konfigurierbar und aufzählbar.</span><span class="sxs-lookup"><span data-stu-id="cb1df-444">JavaScript properties created via addWebAllowedObject are writable, configurable, and enumerable.</span></span>  

```javascript
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```  

#### <span data-ttu-id="cb1df-445">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-445">Parameters</span></span>  

*<span data-ttu-id="cb1df-446">name</span><span class="sxs-lookup"><span data-stu-id="cb1df-446">name</span></span>*  

*   <span data-ttu-id="cb1df-447">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-447">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-448">Der Name des Objekts, das für das Dokument in der **WebView**verfügbar gemacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb1df-448">The name of the object to expose to the document in the **webview**.</span></span>  

*<span data-ttu-id="cb1df-449">applicationObject</span><span class="sxs-lookup"><span data-stu-id="cb1df-449">applicationObject</span></span>*  

*   <span data-ttu-id="cb1df-450">Typ: **Object**</span><span class="sxs-lookup"><span data-stu-id="cb1df-450">Type: **Object**</span></span>  
*   <span data-ttu-id="cb1df-451">Das Objekt, das für das Dokument in der **WebView**verfügbar gemacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb1df-451">The object to expose to the document in the **webview**.</span></span>  

#### <span data-ttu-id="cb1df-452">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-452">Return value</span></span>  

<span data-ttu-id="cb1df-453">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-453">This method does not return a value.</span></span>  

#### <span data-ttu-id="cb1df-454">Zusätzliche Features und Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb1df-454">Additional features and requirements</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-455">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb1df-455">Minimum supported client</span></span>** | <span data-ttu-id="cb1df-456">Windows10 (nur Windows Store-Apps)</span><span class="sxs-lookup"><span data-stu-id="cb1df-456">Windows10 (Windows Store apps only)</span></span> |    
| **<span data-ttu-id="cb1df-457">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb1df-457">Minimum supported server</span></span>** | <span data-ttu-id="cb1df-458">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb1df-458">None supported</span></span> |   
| **<span data-ttu-id="cb1df-459">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="cb1df-459">Minimum supported phone</span></span>** | <span data-ttu-id="cb1df-460">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb1df-460">None supported</span></span> |  

### <span data-ttu-id="cb1df-461">buildLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="cb1df-461">buildLocalStreamUri</span></span>  

<span data-ttu-id="cb1df-462">Erstellt einen URI, den Sie an [navigateToLocalStreamUri](#methods)übergeben können.</span><span class="sxs-lookup"><span data-stu-id="cb1df-462">Creates a URI that you can pass to [navigateToLocalStreamUri](#methods).</span></span>  

```javascript
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```  

#### <span data-ttu-id="cb1df-463">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-463">Parameters</span></span>  

*<span data-ttu-id="cb1df-464">contentIdentifier</span><span class="sxs-lookup"><span data-stu-id="cb1df-464">contentIdentifier</span></span>*  

*   <span data-ttu-id="cb1df-465">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-465">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-466">Ein eindeutiger Bezeichner für den Inhalt, auf den der URI verweist.</span><span class="sxs-lookup"><span data-stu-id="cb1df-466">A unique identifier for the content the URI is referencing.</span></span>  <span data-ttu-id="cb1df-467">Damit wird der Stamm des URIs definiert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-467">This defines the root of the URI.</span></span>  

*<span data-ttu-id="cb1df-468">relativePath</span><span class="sxs-lookup"><span data-stu-id="cb1df-468">relativePath</span></span>*  

*  <span data-ttu-id="cb1df-469">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-469">Type: **String**</span></span>  
*  <span data-ttu-id="cb1df-470">Der Pfad zur Ressource relativ zum Stamm.</span><span class="sxs-lookup"><span data-stu-id="cb1df-470">The path to the resource, relative to the root.</span></span>  

#### <span data-ttu-id="cb1df-471">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-471">Return value</span></span>  

<span data-ttu-id="cb1df-472">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-472">Type: **String**</span></span>  

<span data-ttu-id="cb1df-473">Der URI, der durch kombinieren und Normalisieren von *contentIdentifier* und *relativePath*erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cb1df-473">The URI created by combining and normalizing the *contentIdentifier* and *relativePath*.</span></span>  

#### <span data-ttu-id="cb1df-474">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cb1df-474">Example</span></span>  

<span data-ttu-id="cb1df-475">Im folgenden Beispiel wird ein typischer Anwendungsfall veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cb1df-475">The following example illustrates a typical use case.</span></span>  

```javascript
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### <span data-ttu-id="cb1df-476">capturePreviewToBlobAsync</span><span class="sxs-lookup"><span data-stu-id="cb1df-476">capturePreviewToBlobAsync</span></span>  

<span data-ttu-id="cb1df-477">Erstellt ein Bild des aktuellen [WebView-Elements](./webview.md) und schreibt es in das angegebene Image-Element.</span><span class="sxs-lookup"><span data-stu-id="cb1df-477">Creates an image of the current [webview element](./webview.md) and write it to the specified image element.</span></span>  

```javascript
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```  

#### <span data-ttu-id="cb1df-478">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-478">Parameters</span></span>  

<span data-ttu-id="cb1df-479">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb1df-479">This method has no parameters.</span></span>  

#### <span data-ttu-id="cb1df-480">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-480">Return value</span></span>  

<span data-ttu-id="cb1df-481">Geben Sie Folgendes ein: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="cb1df-481">Type: **MSWebViewAsyncOperation**</span></span>  

<span data-ttu-id="cb1df-482">Ein **MSWebViewAsyncOperation** -Objekt, das nach Abschluss ein **BLOB** -Objekt bereitstellt, das das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="cb1df-482">An **MSWebViewAsyncOperation** object that, when it completes, provides a **Blob** object that contains the image.</span></span>  <span data-ttu-id="cb1df-483">Bei Verwendung von **capturePreviewToBlobAsync**müssen Sie nach dem Definieren des Vorgangs Erfolgs-und Fehlerhandler definieren.</span><span class="sxs-lookup"><span data-stu-id="cb1df-483">When using **capturePreviewToBlobAsync**, you need to define success and error handlers after defining the operation.</span></span>  <span data-ttu-id="cb1df-484">Nachdem Sie die Ereignishandler angewendet haben, rufen Sie die Start-Methode für das [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) -Objekt auf, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-484">After applying the event handlers, call the start method on the [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) object to execute the operation.</span></span>  

### <span data-ttu-id="cb1df-485">captureSelectedContentToDataPackageAsync</span><span class="sxs-lookup"><span data-stu-id="cb1df-485">captureSelectedContentToDataPackageAsync</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cb1df-486">Diese Methode ist veraltet und hat ein bekanntes Problem.</span><span class="sxs-lookup"><span data-stu-id="cb1df-486">This method has been deprecated and has a known issue.</span></span>  <span data-ttu-id="cb1df-487">Vermeiden Sie es, diese Methode in Ihrem Produktionscode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-487">Avoid using this method in your production code.</span></span>  

<span data-ttu-id="cb1df-488">Ruft asynchron ein [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) ab, das den ausgewählten Inhalt in der **WebView**enthält.</span><span class="sxs-lookup"><span data-stu-id="cb1df-488">Asynchronously gets a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) that contains the selected content within the **webview**.</span></span>  

```javascript
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```  

#### <span data-ttu-id="cb1df-489">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-489">Parameters</span></span>  

<span data-ttu-id="cb1df-490">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb1df-490">This method has no parameters.</span></span>  

#### <span data-ttu-id="cb1df-491">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-491">Return value</span></span>  

<span data-ttu-id="cb1df-492">Geben Sie Folgendes ein: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="cb1df-492">Type: **MSWebViewAsyncOperation**</span></span>  

<span data-ttu-id="cb1df-493">Ein **MSWebViewAsyncOperation** -Objekt, das nach Abschluss ein [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) -Objekt bereitstellt, das das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="cb1df-493">An **MSWebViewAsyncOperation** object that, when it completes, provides a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) object that contains the image.</span></span>  <span data-ttu-id="cb1df-494">Bei Verwendung von **captureSelectedContentToDataPackageAsync**müssen Sie nach dem Definieren des Vorgangs Erfolgs-und Fehlerhandler definieren.</span><span class="sxs-lookup"><span data-stu-id="cb1df-494">When using **captureSelectedContentToDataPackageAsync**, you need to define success and error handlers after defining the operation.</span></span>  <span data-ttu-id="cb1df-495">Nachdem Sie die Ereignishandler angewendet haben, rufen Sie die Start-Methode für das MSWebViewAsyncOperation-Objekt auf, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-495">After applying the event handlers, call the start method on the MSWebViewAsyncOperation object to execute the operation.</span></span>  

```javascript
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();
```  

### <span data-ttu-id="cb1df-496">invokeScriptAsync</span><span class="sxs-lookup"><span data-stu-id="cb1df-496">invokeScriptAsync</span></span>  

<span data-ttu-id="cb1df-497">Führt als asynchrone Aktion die angegebene Skriptfunktion aus dem aktuell geladenen HTML-Code mit bestimmten Argumenten aus.</span><span class="sxs-lookup"><span data-stu-id="cb1df-497">As an asynchronous action, executes the specified script function from the currently loaded HTML, with specific arguments.</span></span>  

```javascript
webview.invokeScriptAsync(functionName, ...args)
```  

#### <span data-ttu-id="cb1df-498">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-498">Parameters</span></span>  

**<span data-ttu-id="cb1df-499">FunctionName</span><span class="sxs-lookup"><span data-stu-id="cb1df-499">functionName</span></span>**  

*   <span data-ttu-id="cb1df-500">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-500">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-501">Der Name der aufzurufenden Funktion.</span><span class="sxs-lookup"><span data-stu-id="cb1df-501">The name of the function to invoke.</span></span>  <span data-ttu-id="cb1df-502">Hierbei handelt es sich um einen Eigenschaftsnamen im globalen Fensterobjekt im Dokument der obersten Ebene von WebView.</span><span class="sxs-lookup"><span data-stu-id="cb1df-502">This is a property name on the global window object of the WebView's top level document.</span></span>  <span data-ttu-id="cb1df-503">Dies kann eine integrierte globale Funktion wie eval oder Open sein, oder es kann sich um eine Skript definierte Funktion für das globale Window-Objekt handeln.</span><span class="sxs-lookup"><span data-stu-id="cb1df-503">This can be a built-in global function like eval or open, or it can be a script defined function on the global window object.</span></span>  <span data-ttu-id="cb1df-504">Es können nur Funktionen im Dokument der obersten Ebene der WebView aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-504">Only functions in the top level document of the WebView may be invoked.</span></span>  

**<span data-ttu-id="cb1df-505">args</span><span class="sxs-lookup"><span data-stu-id="cb1df-505">args</span></span>**  

*   <span data-ttu-id="cb1df-506">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-506">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-507">Optionale Zeichenfolgenparameter, die an die aufgerufene Funktion übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-507">Optional string parameters to pass to the invoked function.</span></span>  <span data-ttu-id="cb1df-508">Nach Funktionsname sind alle zusätzlichen Parameter für invokeScriptAsync Zeichenfolgen, die an die aufgerufene Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-508">After functionName, any additional parameters to invokeScriptAsync are strings passed to the invoked function.</span></span>  

#### <span data-ttu-id="cb1df-509">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-509">Return value</span></span>  

<span data-ttu-id="cb1df-510">Geben Sie Folgendes ein: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="cb1df-510">Type: **MSWebViewAsyncOperation**</span></span>  

<span data-ttu-id="cb1df-511">Bei Verwendung von **invokeScriptAsync**müssen Sie nach dem Definieren des Vorgangs Erfolgs-und Fehlerhandler definieren.</span><span class="sxs-lookup"><span data-stu-id="cb1df-511">When using **invokeScriptAsync**, you need to define success and error handlers after defining the operation.</span></span>  <span data-ttu-id="cb1df-512">Nachdem Sie die Ereignishandler angewendet haben, rufen Sie **MSWebViewAsyncOperation. Start** auf, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cb1df-512">After applying the event handlers, call **MSWebViewAsyncOperation.start** to execute the operation.</span></span>  <span data-ttu-id="cb1df-513">Wenn das Complete-Ereignis des MSWebViewAsyncOperation ausgelöst wird, ist die Ergebniseigenschaft des MSWebViewAsyncOperation der Zeichenfolgen Rückgabewert aus dem Aufrufen der Funktion.</span><span class="sxs-lookup"><span data-stu-id="cb1df-513">If the MSWebViewAsyncOperation's complete event fires then the MSWebViewAsyncOperation's result property is the string return value from invoking the function.</span></span>  <span data-ttu-id="cb1df-514">Die Verwendung des Rückgabewerts der aufgerufenen Funktion ermöglicht es dem WebView-Inhalt, synchron zurück zum WebView-Host zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="cb1df-514">Using the invoked function's return value allows for the WebView content to communication synchronously back to the WebView host.</span></span>  <span data-ttu-id="cb1df-515">Wenn die WebView-Inhalte stattdessen asynchron an den WebView-Host weitergeleitet werden sollen, lesen Sie das MSWebViewScriptNotify-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cb1df-515">To instead have the WebView content communicate asynchronously back to the WebView host see the MSWebViewScriptNotify event.</span></span>  <span data-ttu-id="cb1df-516">Wenn die aufgerufene Funktion eine nicht behandelte Ausnahme auslöst, wird das MSWebViewAsyncOperation-Fehlerereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cb1df-516">If the function invoked throws an unhandled exception then the MSWebViewAsyncOperation's error event will fire.</span></span>  

```javascript
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```  

### <span data-ttu-id="cb1df-517">getDeferredPermissionRequests</span><span class="sxs-lookup"><span data-stu-id="cb1df-517">getDeferredPermissionRequests</span></span>  

<span data-ttu-id="cb1df-518">Gibt eine Liste der verzögerten Berechtigungsanforderungen zurück, die von Inhalten im **WebView** -Steuerelement ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-518">Returns a list of deferred permission requests issued by content in the **webview** control.</span></span>  

```javascript
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```  

#### <span data-ttu-id="cb1df-519">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-519">Parameters</span></span>  

<span data-ttu-id="cb1df-520">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb1df-520">This method has no parameters.</span></span>  

#### <span data-ttu-id="cb1df-521">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-521">Return value</span></span>  

<span data-ttu-id="cb1df-522">Geben Sie Folgendes ein: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="cb1df-522">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>  

<span data-ttu-id="cb1df-523">Die angegebene verzögerte Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="cb1df-523">The specified deferred permission request.</span></span>  

#### <span data-ttu-id="cb1df-524">Zusätzliche Features und Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb1df-524">Additional features and requirements</span></span>  

|  | |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-525">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb1df-525">Minimum supported client</span></span>** | <span data-ttu-id="cb1df-526">Windows10 (nur Windows Store-Apps)</span><span class="sxs-lookup"><span data-stu-id="cb1df-526">Windows10 (Windows Store apps only)</span></span> |  
| **<span data-ttu-id="cb1df-527">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb1df-527">Minimum supported server</span></span>** | <span data-ttu-id="cb1df-528">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb1df-528">None supported</span></span> |  
| **<span data-ttu-id="cb1df-529">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="cb1df-529">Minimum supported phone</span></span>** | <span data-ttu-id="cb1df-530">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb1df-530">None supported</span></span> |  


### <span data-ttu-id="cb1df-531">getDeferredPermissionRequestById</span><span class="sxs-lookup"><span data-stu-id="cb1df-531">getDeferredPermissionRequestById</span></span>  

<span data-ttu-id="cb1df-532">Gibt die angegebene verzögerte Berechtigungsanforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-532">Returns the specified deferred permission request.</span></span>  

```javascript
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```  

#### <span data-ttu-id="cb1df-533">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-533">Parameters</span></span>  

*<span data-ttu-id="cb1df-534">id</span><span class="sxs-lookup"><span data-stu-id="cb1df-534">id</span></span>*  

*   <span data-ttu-id="cb1df-535">Typ: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="cb1df-535">Type: **unsigned long**</span></span>  
*   <span data-ttu-id="cb1df-536">Die ID der verzögerten Berechtigungsanforderung, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="cb1df-536">The ID of the deferred permission request you wish to get.</span></span>  

#### <span data-ttu-id="cb1df-537">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-537">Return value</span></span>  

<span data-ttu-id="cb1df-538">Geben Sie Folgendes ein: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="cb1df-538">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>  

<span data-ttu-id="cb1df-539">Die angegebene verzögerte Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="cb1df-539">The specified deferred permission request.</span></span>  

#### <span data-ttu-id="cb1df-540">Zusätzliche Features und Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb1df-540">Additional features and requirements</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="cb1df-541">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb1df-541">Minimum supported client</span></span>** | <span data-ttu-id="cb1df-542">Windows10 (nur Windows Store-Apps)</span><span class="sxs-lookup"><span data-stu-id="cb1df-542">Windows10 (Windows Store apps only)</span></span> |  
| **<span data-ttu-id="cb1df-543">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb1df-543">Minimum supported server</span></span>** | <span data-ttu-id="cb1df-544">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb1df-544">None supported</span></span> |  
| **<span data-ttu-id="cb1df-545">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="cb1df-545">Minimum supported phone</span></span>** | <span data-ttu-id="cb1df-546">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb1df-546">None supported</span></span> |  

### <span data-ttu-id="cb1df-547">GoBack</span><span class="sxs-lookup"><span data-stu-id="cb1df-547">goBack</span></span>  

<span data-ttu-id="cb1df-548">Navigiert die **WebView** zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="cb1df-548">Navigates the **webview** to the previous page in the navigation history.</span></span>  

```javascript
webview.goBack();
```  

#### <span data-ttu-id="cb1df-549">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-549">Parameters</span></span>  

<span data-ttu-id="cb1df-550">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb1df-550">This method has no parameters.</span></span>  

#### <span data-ttu-id="cb1df-551">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-551">Return value</span></span>  

<span data-ttu-id="cb1df-552">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-552">This method does not return a value.</span></span>  

### <span data-ttu-id="cb1df-553">GoForward</span><span class="sxs-lookup"><span data-stu-id="cb1df-553">goForward</span></span>  

<span data-ttu-id="cb1df-554">Navigiert die **WebView** zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="cb1df-554">Navigates the **webview** to the next page in the navigation history.</span></span>  

```javascript
webview.goForward();
```  

#### <span data-ttu-id="cb1df-555">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-555">Parameters</span></span>  

<span data-ttu-id="cb1df-556">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb1df-556">This method has no parameters.</span></span>  

#### <span data-ttu-id="cb1df-557">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-557">Return value</span></span>  

<span data-ttu-id="cb1df-558">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-558">This method does not return a value.</span></span>  

### <span data-ttu-id="cb1df-559">Navigieren</span><span class="sxs-lookup"><span data-stu-id="cb1df-559">navigate</span></span>  

<span data-ttu-id="cb1df-560">Lädt den HTML-Inhalt mit dem angegebenen URI (Uniform Resource Identifier).</span><span class="sxs-lookup"><span data-stu-id="cb1df-560">Loads the HTML content at the specified Uniform Resource Identifier (URI).</span></span>  

```javascript
webview.navigate(uri);
```  

#### <span data-ttu-id="cb1df-561">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-561">Parameters</span></span>  

**<span data-ttu-id="cb1df-562">Uri</span><span class="sxs-lookup"><span data-stu-id="cb1df-562">uri</span></span>**  

*   <span data-ttu-id="cb1df-563">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-563">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-564">Der URI, der geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb1df-564">The URI to load.</span></span>  

#### <span data-ttu-id="cb1df-565">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-565">Return value</span></span>  

<span data-ttu-id="cb1df-566">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-566">This method does not return a value.</span></span>  

### <span data-ttu-id="cb1df-567">navigateFocus</span><span class="sxs-lookup"><span data-stu-id="cb1df-567">navigateFocus</span></span>  

<span data-ttu-id="cb1df-568">Navigiert den Fokus auf die **WebView**.</span><span class="sxs-lookup"><span data-stu-id="cb1df-568">Navigates focus onto the **webview**.</span></span>  <span data-ttu-id="cb1df-569">Löst das window's-navigatingfocus-Ereignis des WebView-Dokuments auf oberster Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="cb1df-569">Fires the webview's top level document's window's navigatingfocus event.</span></span>  <span data-ttu-id="cb1df-570">Die im navigatingfocus-Ereignis verwendeten FocusNavigationEvent-Argumente entsprechen den Parametern für navigateFocus, mit der Ausnahme, dass die Ursprungs Parameter aus dem Koordinatenraum des Host Dokuments in den Koordinatenbereich des obersten Dokuments der WebView-Ebene übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cb1df-570">The FocusNavigationEvent args used in the navigatingfocus event match the parameters provided to navigateFocus except the origin parameters are translated from the host document's coordinate space to the coordinate space of the webview's top level document.</span></span>  <span data-ttu-id="cb1df-571">Weitere Informationen finden Sie unter WebView departingFocus-Ereignis und entsprechende Window. departFocus-Methode zum Übertragen des Fokus vom WebView auf den Host.</span><span class="sxs-lookup"><span data-stu-id="cb1df-571">See the webview departingFocus event and corresponding window.departFocus method for transferring focus from the webview to the host.</span></span>  <span data-ttu-id="cb1df-572">Ein Beispiel für eine Implementierung der Fokusnavigation über die Tastatur oder das Gamepad, die diese Methode verwendet, finden Sie in der [TVJS-Navigations Bibliothek](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .</span><span class="sxs-lookup"><span data-stu-id="cb1df-572">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that uses this method.</span></span>  

```javascript
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```  

#### <span data-ttu-id="cb1df-573">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-573">Parameters</span></span>  

*<span data-ttu-id="cb1df-574">navigationReason</span><span class="sxs-lookup"><span data-stu-id="cb1df-574">navigationReason</span></span>*  

*   <span data-ttu-id="cb1df-575">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-575">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-576">Der Grund für die Navigation.</span><span class="sxs-lookup"><span data-stu-id="cb1df-576">The reason for the navigation.</span></span>  <span data-ttu-id="cb1df-577">Der Wert sollte entweder "Left", "up", "Right" oder "Down" sein.</span><span class="sxs-lookup"><span data-stu-id="cb1df-577">The value should be either "left", "up", "right", or "down".</span></span>  <span data-ttu-id="cb1df-578">Es ist die Richtung, in der sich der Fokus von dem aktuell fokussierten Element entfernt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-578">It is the direction in which focus is moving away from the currently focused element.</span></span>  

*<span data-ttu-id="cb1df-579">Ursprung</span><span class="sxs-lookup"><span data-stu-id="cb1df-579">origin</span></span>*  

*   <span data-ttu-id="cb1df-580">Typ: **Object**</span><span class="sxs-lookup"><span data-stu-id="cb1df-580">Type: **Object**</span></span>  
*   <span data-ttu-id="cb1df-581">Der Ursprung der Navigation.</span><span class="sxs-lookup"><span data-stu-id="cb1df-581">The origin of the navigation.</span></span>  <span data-ttu-id="cb1df-582">Hierbei handelt es sich um ein JavaScript-Objekt mit den Eigenschaften "originLeft", "originTop", "originWidth" und "originHeight".</span><span class="sxs-lookup"><span data-stu-id="cb1df-582">This is a JavaScript object with properties "originLeft", "originTop", "originWidth", and "originHeight".</span></span>  <span data-ttu-id="cb1df-583">Diese Werte sollten die Position und Größe des aktuell fokussierten Elements beschreiben, von dem der Fokus verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="cb1df-583">These values should describe the position and size of the currently focused element away from which focus is moving.</span></span>  

#### <span data-ttu-id="cb1df-584">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-584">Return value</span></span>  

<span data-ttu-id="cb1df-585">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-585">This method does not return a value.</span></span>  

### <span data-ttu-id="cb1df-586">navigateToLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="cb1df-586">navigateToLocalStreamUri</span></span>  

<span data-ttu-id="cb1df-587">Lädt lokalen Webinhalt am angegebenen URI mithilfe eines [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span><span class="sxs-lookup"><span data-stu-id="cb1df-587">Loads local web content at the specified URI using a [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span></span>  

```javascript
webview.navigateToLocalStreamUri(source, streamResolver); 
```  

#### <span data-ttu-id="cb1df-588">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-588">Parameters</span></span>  

*<span data-ttu-id="cb1df-589">Quelle</span><span class="sxs-lookup"><span data-stu-id="cb1df-589">source</span></span>*  

*   <span data-ttu-id="cb1df-590">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-590">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-591">Ein MS-local-Stream-URI, der den zu ladenden lokalen HTML-Inhalt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-591">An ms-local-stream URI identifying the local HTML content to load.</span></span>  <span data-ttu-id="cb1df-592">Erstellen Sie diese Zeichenfolge mithilfe von [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span><span class="sxs-lookup"><span data-stu-id="cb1df-592">Create this string using [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span></span>  

*<span data-ttu-id="cb1df-593">streamResolver</span><span class="sxs-lookup"><span data-stu-id="cb1df-593">streamResolver</span></span>*  

*   <span data-ttu-id="cb1df-594">Geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="cb1df-594">Type: any</span></span>  
*   <span data-ttu-id="cb1df-595">Ein Resolver, der den URI in einen zu ladenden Stream konvertiert.</span><span class="sxs-lookup"><span data-stu-id="cb1df-595">A resolver that converts the URI into a stream to load.</span></span>  

#### <span data-ttu-id="cb1df-596">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-596">Return value</span></span>  

<span data-ttu-id="cb1df-597">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-597">This method does not return a value.</span></span>  

### <span data-ttu-id="cb1df-598">navigateToString</span><span class="sxs-lookup"><span data-stu-id="cb1df-598">navigateToString</span></span>  

<span data-ttu-id="cb1df-599">Lädt den angegebenen HTML-Inhalt als neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="cb1df-599">Loads the specified HTML content as a new document.</span></span>  

```javascript
webview.navigateToString(contents);
```  

#### <span data-ttu-id="cb1df-600">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-600">Parameters</span></span>  

*<span data-ttu-id="cb1df-601">Inhalt</span><span class="sxs-lookup"><span data-stu-id="cb1df-601">contents</span></span>*  

*   <span data-ttu-id="cb1df-602">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-602">Type: **String**</span></span>  
*   <span data-ttu-id="cb1df-603">Der anzuzeigende HTML-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-603">The HTML content to display.</span></span>  

#### <span data-ttu-id="cb1df-604">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-604">Return value</span></span>  

<span data-ttu-id="cb1df-605">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-605">This method does not return a value.</span></span>  

### <span data-ttu-id="cb1df-606">navigateWithHttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="cb1df-606">navigateWithHttpRequestMessage</span></span>  

<span data-ttu-id="cb1df-607">Navigiert die WebView zu einem Uniform Resource Identifier (URI) mit einer POST-Anforderung und HTTP-Headern.</span><span class="sxs-lookup"><span data-stu-id="cb1df-607">Navigates the webview to a Uniform Resource Identifier (URI) with a POST request and HTTP headers.</span></span>  

```javascript
webview.navigateWithHttpRequestMessage(requestMessage);
```  

#### <span data-ttu-id="cb1df-608">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-608">Parameters</span></span>  

*<span data-ttu-id="cb1df-609">RequestMessage</span><span class="sxs-lookup"><span data-stu-id="cb1df-609">requestMessage</span></span>*  

*   <span data-ttu-id="cb1df-610">Geben Sie Folgendes ein: **HttpRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="cb1df-610">Type: **HttpRequestMessage**</span></span>  
*   <span data-ttu-id="cb1df-611">Die Details der HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cb1df-611">The details of the HTTP request.</span></span>  

#### <span data-ttu-id="cb1df-612">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-612">Return value</span></span>  

<span data-ttu-id="cb1df-613">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-613">This method does not return a value.</span></span>  

#### <span data-ttu-id="cb1df-614">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb1df-614">Remarks</span></span>  

> [!WARNING]
> <span data-ttu-id="cb1df-615">Wenn Sie dieser Anforderung zusätzliche Kopfzeilen wie Authentifizierungsanmeldeinformationen hinzufügen, denken Sie daran, dass diese Überschriften auch bei nachfolgenden untergeordneten Anforderungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cb1df-615">If you add additional headers to this request, such as authentication credentials, remember that those headers will also be included with any subsequent child requests.</span></span>  <span data-ttu-id="cb1df-616">Verwenden Sie Vorsicht, um eine versehentliche Offenlegung vertraulicher oder personenbezogener Informationen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="cb1df-616">Use caution to prevent accidental disclosure of confidential or personal information.</span></span>  

### <span data-ttu-id="cb1df-617">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cb1df-617">refresh</span></span>  

<span data-ttu-id="cb1df-618">Lädt den aktuellen Inhalt in der **WebView**erneut.</span><span class="sxs-lookup"><span data-stu-id="cb1df-618">Reloads the current content in the **webview**.</span></span>  

```javascript
webview.refresh();
```  

#### <span data-ttu-id="cb1df-619">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-619">Parameters</span></span>  

<span data-ttu-id="cb1df-620">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb1df-620">This method has no parameters.</span></span>  

#### <span data-ttu-id="cb1df-621">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-621">Return value</span></span>  

<span data-ttu-id="cb1df-622">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-622">This method does not return a value.</span></span>  

### <span data-ttu-id="cb1df-623">stop</span><span class="sxs-lookup"><span data-stu-id="cb1df-623">stop</span></span>  

<span data-ttu-id="cb1df-624">Hält die aktuelle **WebView** -Navigation oder den Download an.</span><span class="sxs-lookup"><span data-stu-id="cb1df-624">Halts the current **webview** navigation or download.</span></span>  

```javascript
webview.stop();
```  

#### <span data-ttu-id="cb1df-625">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb1df-625">Parameters</span></span>  

<span data-ttu-id="cb1df-626">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb1df-626">This method has no parameters.</span></span>  

#### <span data-ttu-id="cb1df-627">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb1df-627">Return value</span></span>  

<span data-ttu-id="cb1df-628">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb1df-628">This method does not return a value.</span></span>  

## <span data-ttu-id="cb1df-629">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb1df-629">Properties</span></span>  

### <span data-ttu-id="cb1df-630">canGoBack</span><span class="sxs-lookup"><span data-stu-id="cb1df-630">canGoBack</span></span>  

<span data-ttu-id="cb1df-631">Ruft einen Wert ab, der angibt, ob die **WebView** rückwärts navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="cb1df-631">Gets a value that indicates whether the **webview** can navigate backward.</span></span>  

<span data-ttu-id="cb1df-632">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-632">This property is read-only.</span></span>  

```javascript
var canGoBack = webview.canGoBack;
```  

#### <span data-ttu-id="cb1df-633">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-633">Property value</span></span>  

<span data-ttu-id="cb1df-634">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="cb1df-634">Type: **Boolean**</span></span>  

<span data-ttu-id="cb1df-635">" **True** ", wenn die **WebView** rückwärts navigieren kann; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cb1df-635">**True** if the **webview** can navigate backward; otherwise, **false**.</span></span>  

### <span data-ttu-id="cb1df-636">canGoForward</span><span class="sxs-lookup"><span data-stu-id="cb1df-636">canGoForward</span></span>  

<span data-ttu-id="cb1df-637">Ruft einen Wert ab, der angibt, ob die **WebView** vorwärts navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="cb1df-637">Gets a value that indicates whether the **webview** can navigate forward.</span></span>  

<span data-ttu-id="cb1df-638">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-638">This property is read-only.</span></span>  

```javascript
var canGoForward = webview.canGoForward;
```  

#### <span data-ttu-id="cb1df-639">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-639">Property value</span></span>  

<span data-ttu-id="cb1df-640">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="cb1df-640">Type: **Boolean**</span></span>  

<span data-ttu-id="cb1df-641">" **True** ", wenn die **WebView** vorwärts navigieren kann; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cb1df-641">**True** if the **webview** can navigate forward; otherwise, **false**.</span></span>  

### <span data-ttu-id="cb1df-642">containsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="cb1df-642">containsFullScreenElement</span></span>  

<span data-ttu-id="cb1df-643">Ruft einen Wert ab, der angibt, ob die **WebView** ein Element enthält, das den Vollbildmodus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-643">Gets a value that indicates whether the **webview** contains an element that supports full screen.</span></span>  <span data-ttu-id="cb1df-644">Weitere Informationen finden Sie im MSWebViewContainsFullScreenElementChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cb1df-644">See the MSWebViewContainsFullScreenElementChanged event for more info.</span></span>  

<span data-ttu-id="cb1df-645">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-645">This property is read-only.</span></span>  

```javascript
var containsFullScreenElement = webview.containsFullScreenElement;
```  

#### <span data-ttu-id="cb1df-646">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-646">Property value</span></span>  

<span data-ttu-id="cb1df-647">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="cb1df-647">Type: **Boolean**</span></span>  

<span data-ttu-id="cb1df-648">" **True** ", wenn die **WebView** ein Element enthält, das Vollbild unterstützt; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cb1df-648">**True** if the **webview** contains an element that supports full screen; otherwise, **false**.</span></span>  

### <span data-ttu-id="cb1df-649">documentTitle</span><span class="sxs-lookup"><span data-stu-id="cb1df-649">documentTitle</span></span>  

<span data-ttu-id="cb1df-650">Ruft den Titel der Seite ab, die derzeit in der **WebView**angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cb1df-650">Gets the title of the page currently displayed in the **webview**.</span></span>  

<span data-ttu-id="cb1df-651">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-651">This property is read-only.</span></span>  

```javascript
var documentTitle = webview.documentTitle;
```  

#### <span data-ttu-id="cb1df-652">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-652">Property value</span></span>  

<span data-ttu-id="cb1df-653">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-653">Type: **String**</span></span>  

<span data-ttu-id="cb1df-654">Der Seitentitel</span><span class="sxs-lookup"><span data-stu-id="cb1df-654">The page title.</span></span>  

### <span data-ttu-id="cb1df-655">height</span><span class="sxs-lookup"><span data-stu-id="cb1df-655">height</span></span>  

<span data-ttu-id="cb1df-656">Ruft die Höhe von **WebView**ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cb1df-656">Gets or sets the height of the **webview**.</span></span>  

```javascript
var height = webview.height;
webview.height = height;
```  

#### <span data-ttu-id="cb1df-657">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-657">Property value</span></span>  

<span data-ttu-id="cb1df-658">Typ: **Zahl**</span><span class="sxs-lookup"><span data-stu-id="cb1df-658">Type: **Number**</span></span>  

<span data-ttu-id="cb1df-659">Die Höhe von **WebView**.</span><span class="sxs-lookup"><span data-stu-id="cb1df-659">The height of the **webview**.</span></span>  

### <span data-ttu-id="cb1df-660">Prozess manipuliert wird.</span><span class="sxs-lookup"><span data-stu-id="cb1df-660">process</span></span>  

<span data-ttu-id="cb1df-661">Ruft den **WebView** -Prozess ab.</span><span class="sxs-lookup"><span data-stu-id="cb1df-661">Gets the **webview** process.</span></span>  

<span data-ttu-id="cb1df-662">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-662">This property is read-only.</span></span>  

```javascript
var process = webview.process;
webview.process = process;
```  

#### <span data-ttu-id="cb1df-663">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-663">Property value</span></span>  

<span data-ttu-id="cb1df-664">Geben Sie Folgendes ein: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span><span class="sxs-lookup"><span data-stu-id="cb1df-664">Type: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span></span>  

### <span data-ttu-id="cb1df-665">settings</span><span class="sxs-lookup"><span data-stu-id="cb1df-665">settings</span></span>  

<span data-ttu-id="cb1df-666">Ruft ein [MSWebViewSettings](./webview/MSWebViewSettings.md) -Objekt ab, das Eigenschaften zum Aktivieren oder Deaktivieren von **WebView** -Features enthält.</span><span class="sxs-lookup"><span data-stu-id="cb1df-666">Gets a [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>  

<span data-ttu-id="cb1df-667">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb1df-667">This property is read-only.</span></span>  

```javascript
var settings = webview.settings;
webview.settings = settings;
```  

#### <span data-ttu-id="cb1df-668">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-668">Property value</span></span>  

<span data-ttu-id="cb1df-669">Geben Sie Folgendes ein: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span><span class="sxs-lookup"><span data-stu-id="cb1df-669">Type: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span></span>  

<span data-ttu-id="cb1df-670">Ein [MSWebViewSettings](./webview/MSWebViewSettings.md) -Objekt, das Eigenschaften zum Aktivieren oder Deaktivieren von **WebView** -Features enthält.</span><span class="sxs-lookup"><span data-stu-id="cb1df-670">A [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>  

### <span data-ttu-id="cb1df-671">src</span><span class="sxs-lookup"><span data-stu-id="cb1df-671">src</span></span>  

<span data-ttu-id="cb1df-672">Ruft die URI-Quelle (Uniform Resource Identifier) des HTML-Inhalts ab, der im **WebView** -Steuerelement angezeigt werden soll, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cb1df-672">Gets or sets the Uniform Resource Identifier (URI) source of the HTML content to display in the **webview** control.</span></span>  

```javascript
var src = webview.src;
webview.src = src;
```  

#### <span data-ttu-id="cb1df-673">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-673">Property value</span></span>  

<span data-ttu-id="cb1df-674">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb1df-674">Type: **String**</span></span>  

<span data-ttu-id="cb1df-675">Die URI-Quelle des HTML-Inhalts, der im **WebView** -Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb1df-675">The URI source of the HTML content to display in the **webview** control.</span></span>  

### <span data-ttu-id="cb1df-676">width</span><span class="sxs-lookup"><span data-stu-id="cb1df-676">width</span></span>  

<span data-ttu-id="cb1df-677">Ruft die Breite von **WebView**ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cb1df-677">Gets or sets the width of the **webview**.</span></span>  

```javascript
var width = webview.width;
webview.width = width;
```  

#### <span data-ttu-id="cb1df-678">Eigenschaftenwert</span><span class="sxs-lookup"><span data-stu-id="cb1df-678">Property value</span></span>  

<span data-ttu-id="cb1df-679">Typ: **Zahl**</span><span class="sxs-lookup"><span data-stu-id="cb1df-679">Type: **Number**</span></span>  

<span data-ttu-id="cb1df-680">Die Breite von **WebView**.</span><span class="sxs-lookup"><span data-stu-id="cb1df-680">The width of the **webview**.</span></span>  
