---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2
ms.openlocfilehash: 6717542349cff327875b609168dff0b82a933668
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012163"
---
# <span data-ttu-id="6ca54-104">Schnittstellen ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="6ca54-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="6ca54-105">WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.</span><span class="sxs-lookup"><span data-stu-id="6ca54-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="6ca54-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6ca54-106">Summary</span></span>

 <span data-ttu-id="6ca54-107">Member</span><span class="sxs-lookup"><span data-stu-id="6ca54-107">Members</span></span>                        | <span data-ttu-id="6ca54-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6ca54-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="6ca54-110">Fügen Sie einen Ereignishandler für das ContainsFullScreenElementChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-110">Add an event handler for the ContainsFullScreenElementChanged event.</span></span>
[<span data-ttu-id="6ca54-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="6ca54-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="6ca54-112">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="6ca54-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="6ca54-114">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="6ca54-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="6ca54-116">Fügen Sie einen Ereignishandler für das FrameNavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="6ca54-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="6ca54-118">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="6ca54-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="6ca54-120">Fügen Sie einen Ereignishandler für das History-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-120">Add an event handler for the HistoryChanged event.</span></span>
[<span data-ttu-id="6ca54-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="6ca54-122">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="6ca54-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="6ca54-124">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="6ca54-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="6ca54-126">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="6ca54-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="6ca54-128">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="6ca54-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="6ca54-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="6ca54-130">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="6ca54-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="6ca54-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="6ca54-132">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="6ca54-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="6ca54-134">Fügen Sie einen Ereignishandler für das Quellpfad-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-134">Add an event handler for the SourceChanged event.</span></span>
[<span data-ttu-id="6ca54-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="6ca54-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="6ca54-136">Fügen Sie einen Ereignishandler für das WebMessageReceived-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-136">Add an event handler for the WebMessageReceived event.</span></span>
[<span data-ttu-id="6ca54-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="6ca54-138">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="6ca54-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="6ca54-140">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="6ca54-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="6ca54-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="6ca54-142">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="6ca54-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="6ca54-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="6ca54-144">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="6ca54-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="6ca54-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="6ca54-146">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="6ca54-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="6ca54-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="6ca54-148">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6ca54-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="6ca54-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="6ca54-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="6ca54-150">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="6ca54-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="6ca54-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="6ca54-152">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="6ca54-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="6ca54-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="6ca54-154">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="6ca54-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="6ca54-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="6ca54-156">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="6ca54-156">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="6ca54-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="6ca54-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="6ca54-158">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="6ca54-158">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="6ca54-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="6ca54-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="6ca54-160">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="6ca54-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="6ca54-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="6ca54-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="6ca54-162">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="6ca54-162">The title for the current top level document.</span></span>
[<span data-ttu-id="6ca54-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="6ca54-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="6ca54-164">Das [ICoreWebView2Settings](icorewebview2settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="6ca54-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="6ca54-165">get_Source</span></span>](#get_source) | <span data-ttu-id="6ca54-166">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="6ca54-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="6ca54-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="6ca54-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="6ca54-168">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="6ca54-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="6ca54-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="6ca54-169">GoBack</span></span>](#goback) | <span data-ttu-id="6ca54-170">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="6ca54-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="6ca54-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="6ca54-171">GoForward</span></span>](#goforward) | <span data-ttu-id="6ca54-172">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="6ca54-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="6ca54-173">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="6ca54-173">Navigate</span></span>](#navigate) | <span data-ttu-id="6ca54-174">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="6ca54-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="6ca54-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="6ca54-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="6ca54-176">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="6ca54-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="6ca54-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="6ca54-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="6ca54-178">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="6ca54-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="6ca54-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="6ca54-180">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="6ca54-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="6ca54-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="6ca54-182">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="6ca54-183">Laden</span><span class="sxs-lookup"><span data-stu-id="6ca54-183">Reload</span></span>](#reload) | <span data-ttu-id="6ca54-184">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-184">Reload the current page.</span></span>
[<span data-ttu-id="6ca54-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="6ca54-186">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContainsFullScreenElementChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-186">Remove an event handler previously added with add_ContainsFullScreenElementChanged.</span></span>
[<span data-ttu-id="6ca54-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="6ca54-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="6ca54-188">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="6ca54-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="6ca54-190">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="6ca54-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="6ca54-192">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="6ca54-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="6ca54-194">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="6ca54-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="6ca54-196">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="6ca54-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="6ca54-198">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="6ca54-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="6ca54-200">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="6ca54-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="6ca54-202">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="6ca54-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="6ca54-204">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="6ca54-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="6ca54-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="6ca54-206">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="6ca54-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="6ca54-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="6ca54-208">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="6ca54-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="6ca54-210">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="6ca54-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="6ca54-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="6ca54-212">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="6ca54-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="6ca54-214">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="6ca54-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="6ca54-216">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="6ca54-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="6ca54-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="6ca54-218">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="6ca54-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="6ca54-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="6ca54-220">Entfernen Sie das entsprechende JavaScript `AddScriptToExecuteOnDocumentCreated` , das mit der angegebenen Skript-ID hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-220">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>
[<span data-ttu-id="6ca54-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="6ca54-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="6ca54-222">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="6ca54-223">Stop</span><span class="sxs-lookup"><span data-stu-id="6ca54-223">Stop</span></span>](#stop) | <span data-ttu-id="6ca54-224">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="6ca54-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="6ca54-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="6ca54-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="6ca54-226">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="6ca54-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="6ca54-228">Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="6ca54-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="6ca54-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="6ca54-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="6ca54-230">Grund für das Verschieben des Fokus</span><span class="sxs-lookup"><span data-stu-id="6ca54-230">Reason for moving focus.</span></span>
[<span data-ttu-id="6ca54-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="6ca54-232">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6ca54-232">The type of a permission request.</span></span>
[<span data-ttu-id="6ca54-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="6ca54-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="6ca54-234">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6ca54-234">Response to a permission request.</span></span>
[<span data-ttu-id="6ca54-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="6ca54-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="6ca54-236">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="6ca54-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="6ca54-238">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6ca54-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="6ca54-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="6ca54-240">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="6ca54-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="6ca54-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="6ca54-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="6ca54-242">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="6ca54-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="6ca54-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="6ca54-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="6ca54-244">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="6ca54-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="6ca54-245">Member</span><span class="sxs-lookup"><span data-stu-id="6ca54-245">Members</span></span>

#### <span data-ttu-id="6ca54-246">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-246">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="6ca54-247">Fügen Sie einen Ereignishandler für das ContainsFullScreenElementChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-247">Add an event handler for the ContainsFullScreenElementChanged event.</span></span>

> <span data-ttu-id="6ca54-248">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-248">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-249">ContainsFullScreenElementChanged wird ausgelöst, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-249">ContainsFullScreenElementChanged fires when the ContainsFullScreenElement property changes.</span></span> <span data-ttu-id="6ca54-250">Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-250">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="6ca54-251">Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-251">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="6ca54-252">Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.</span><span class="sxs-lookup"><span data-stu-id="6ca54-252">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="6ca54-253">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="6ca54-253">add_ContentLoading</span></span> 

<span data-ttu-id="6ca54-254">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-254">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="6ca54-255">Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-255">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-256">ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-256">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="6ca54-257">ContentLoading wird nicht ausgelöst, wenn dieselbe Seitennavigation ausgeführt wird (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigationselemente).</span><span class="sxs-lookup"><span data-stu-id="6ca54-257">ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="6ca54-258">Dies folgt auf das NavigationStarting-Ereignis und das Source-Ereignis und steht vor den Ereignissen "History" und "NavigationCompleted".</span><span class="sxs-lookup"><span data-stu-id="6ca54-258">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="6ca54-259">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-259">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="6ca54-260">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-260">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="6ca54-261">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-261">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-262">DocumentTitleChanged wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-262">DocumentTitleChanged fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="6ca54-263">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-263">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="6ca54-264">Fügen Sie einen Ereignishandler für das FrameNavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-264">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="6ca54-265">Public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-265">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-266">FrameNavigationCompleted wird ausgelöst, wenn ein untergeordneter Frame vollständig geladen wurde (Body. OnLoad hat ausgelöst) oder das Laden mit Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-266">FrameNavigationCompleted fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the FrameNavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    CHECK_FAILURE(m_webView->add_FrameNavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    std::wstring error_msg = WebErrorStatusToString(webErrorStatus);
                    MessageBox(nullptr,
                       (std::wstring(L"IFrame navigation failed with the ") +
                         L"give in error " + error_msg).c_str(),
                       L"Navigation Failure", MB_OK);
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_frameNavigationCompletedToken));
```

#### <span data-ttu-id="6ca54-267">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-267">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="6ca54-268">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-268">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="6ca54-269">Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-269">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-270">FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-270">FrameNavigationStarting fires when a child frame in the WebView requests permission to navigate to a different URI.</span></span> <span data-ttu-id="6ca54-271">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6ca54-271">This will fire for redirects as well.</span></span>

<span data-ttu-id="6ca54-272">Entsprechende Navigationselemente können blockiert werden, bis der Ereignishandler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-272">Corresponding navigations can be blocked until the event handler returns.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### <span data-ttu-id="6ca54-273">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-273">add_HistoryChanged</span></span> 

<span data-ttu-id="6ca54-274">Fügen Sie einen Ereignishandler für das History-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-274">Add an event handler for the HistoryChanged event.</span></span>

> <span data-ttu-id="6ca54-275">Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-275">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-276">Historyist hört die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="6ca54-276">HistoryChanged listens to the change of navigation history for the top level document.</span></span> <span data-ttu-id="6ca54-277">Verwenden Sie "History", um zu überprüfen, ob sich der CanGoBack/CanGoForward-Wert geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6ca54-277">Use HistoryChanged to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="6ca54-278">"History" wird auch für die Verwendung von GoBack/GoForward ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6ca54-278">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="6ca54-279">"History" wird nach "sourcely" und "ContentLoading" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6ca54-279">HistoryChanged fires after SourceChanged and ContentLoading.</span></span>

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                m_toolbar->SetItemEnabled(Toolbar::Item_BackButton, canGoBack);
                m_toolbar->SetItemEnabled(Toolbar::Item_ForwardButton, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="6ca54-280">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-280">add_NavigationCompleted</span></span> 

<span data-ttu-id="6ca54-281">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-281">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="6ca54-282">Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-282">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-283">NavigationCompleted wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-283">NavigationCompleted fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
                m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="6ca54-284">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-284">add_NavigationStarting</span></span> 

<span data-ttu-id="6ca54-285">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-285">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="6ca54-286">Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-286">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-287">NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-287">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="6ca54-288">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6ca54-288">This will fire for redirects as well.</span></span>

<span data-ttu-id="6ca54-289">Entsprechende Navigationselemente können blockiert werden, bis der Ereignishandler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-289">Corresponding navigations can be blocked until the event handler returns.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### <span data-ttu-id="6ca54-290">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-290">add_NewWindowRequested</span></span> 

<span data-ttu-id="6ca54-291">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-291">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="6ca54-292">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-292">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-293">Mswebviewnewwindowrequested wird ausgelöst, wenn der Inhalt in der WebView-Anforderung zum Öffnen eines neuen Fensters, beispielsweisedurch Window. Open, anfordert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-293">NewWindowRequested fires when content inside the WebView requests to open a new window, such as through window.open.</span></span> <span data-ttu-id="6ca54-294">Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-294">The app can pass a target WebView that will be considered the opened window.</span></span>

<span data-ttu-id="6ca54-295">Skripts, die im neuen Fenster angefordert wurden, können blockiert werden, bis der Ereignishandler zurückgegeben wird, wenn keine Verzögerung für die Ereignis args übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-295">Scripts resulted in the new window requested can be blocked until the event handler returns if a deferral is not taken on the event args.</span></span> <span data-ttu-id="6ca54-296">Wenn eine Verzögerung durchgeführt wird, werden Skripts blockiert, bis der Verzögerungs Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-296">If a deferral is taken, then scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));
                AppWindow* newAppWindow;

                wil::com_ptr<ICoreWebView2WindowFeatures> windowFeatures;
                CHECK_FAILURE(args->get_WindowFeatures(&windowFeatures));

                RECT windowRect = {0};
                UINT32 left = 0;
                UINT32 top = 0;
                UINT32 height = 0;
                UINT32 width = 0;
                BOOL shouldHaveToolbar = true;

                BOOL hasPosition = FALSE;
                BOOL hasSize = FALSE;
                CHECK_FAILURE(windowFeatures->HasPosition(&hasPosition));
                CHECK_FAILURE(windowFeatures->HasSize(&hasSize));

                bool useDefaultWindow = true;

                if (!!hasPosition && !!hasSize)
                {
                    CHECK_FAILURE(windowFeatures->get_Left(&left));
                    CHECK_FAILURE(windowFeatures->get_Top(&top));
                    CHECK_FAILURE(windowFeatures->get_Height(&height));
                    CHECK_FAILURE(windowFeatures->get_Width(&width));
                    useDefaultWindow = false;
                }
                CHECK_FAILURE(windowFeatures->get_Toolbar(&shouldHaveToolbar));

                windowRect.left = left;
                windowRect.right = left + (width < s_minNewWindowSize ? s_minNewWindowSize : width);
                windowRect.top = top;
                windowRect.bottom = top + (height < s_minNewWindowSize ? s_minNewWindowSize : height);

                if (!useDefaultWindow)
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"", false, nullptr, true, windowRect, !!shouldHaveToolbar);
                }
                else
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"");
                }
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="6ca54-297">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-297">add_PermissionRequested</span></span> 

<span data-ttu-id="6ca54-298">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-298">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="6ca54-299">Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-299">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-300">PermissionRequested wird ausgelöst, wenn Inhalt in einer WebView die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-300">PermissionRequested fires when content in a WebView requests permission to access some privileged resources.</span></span>

<span data-ttu-id="6ca54-301">Wenn für die Ereignis-args keine Verzögerung übernommen wird, können die nachfolgenden Skripts blockiert werden, bis der Ereignishandler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-301">If a deferral is not taken on the event args, the subsequent scripts can be blocked until the event handler returns.</span></span> <span data-ttu-id="6ca54-302">Wenn eine Verzögerung durchgeführt wird, werden die Skripts blockiert, bis der Verzögerungs Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-302">If a deferral is taken, then the scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        COREWEBVIEW2_PERMISSION_KIND kind = COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        COREWEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? COREWEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? COREWEBVIEW2_PERMISSION_STATE_DENY
            :                     COREWEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="6ca54-303">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="6ca54-303">add_ProcessFailed</span></span> 

<span data-ttu-id="6ca54-304">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-304">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="6ca54-305">Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-305">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-306">ProcessFailed wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-306">ProcessFailed fires when a WebView process is terminated unexpectedly or becomes unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        COREWEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process exited unexpectedly. Reload page?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                CHECK_FAILURE(m_webView->Reload());
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="6ca54-307">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="6ca54-307">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="6ca54-308">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-308">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="6ca54-309">Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-309">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-310">ScriptDialogOpening wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung, Eingabeaufforderung oder beforeunload) für die WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-310">ScriptDialogOpening fires when a JavaScript dialog (alert, confirm, prompt, or beforeunload) will show for the webview.</span></span> <span data-ttu-id="6ca54-311">Dieses Ereignis wird nur ausgelöst, wenn die ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-311">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="6ca54-312">Das ScriptDialogOpening-Ereignis kann verwendet werden, um Dialogfelder zu unterdrücken oder Standarddialogfelder durch benutzerdefinierte Dialogfelder zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-312">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

<span data-ttu-id="6ca54-313">Wenn für die Ereignis-args keine Verzögerung übernommen wird, können die nachfolgenden Skripts blockiert werden, bis der Ereignishandler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-313">If a deferral is not taken on the event args, the subsequent scripts can be blocked until the event handler returns.</span></span> <span data-ttu-id="6ca54-314">Wenn eine Verzögerung durchgeführt wird, werden die Skripts blockiert, bis der Verzögerungs Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-314">If a deferral is taken, then the scripts are blocked until the deferral is completed.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            COREWEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### <span data-ttu-id="6ca54-315">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-315">add_SourceChanged</span></span> 

<span data-ttu-id="6ca54-316">Fügen Sie einen Ereignishandler für das Quellpfad-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-316">Add an event handler for the SourceChanged event.</span></span>

> <span data-ttu-id="6ca54-317">Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-317">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-318">Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-318">SourceChanged fires when the Source property changes.</span></span> <span data-ttu-id="6ca54-319">Die Quelle wird ausgelöst, um zu einer anderen Website oder zu einer anderen Fragment-Navigation zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="6ca54-319">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="6ca54-320">Sie wird nicht für andere Navigationsarten wie "Seiten-Reload" oder "History. pushState" mit der gleichen URL wie die aktuelle Seite ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6ca54-320">It will not fire for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="6ca54-321">Die Quelle wird vor ContentLoading für die Navigation zu einem neuen Dokument ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6ca54-321">SourceChanged fires before ContentLoading for navigation to a new document.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="6ca54-322">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="6ca54-322">add_WebMessageReceived</span></span> 

<span data-ttu-id="6ca54-323">Fügen Sie einen Ereignishandler für das WebMessageReceived-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-323">Add an event handler for the WebMessageReceived event.</span></span>

> <span data-ttu-id="6ca54-324">öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*-Handler, EventRegistrationToken \*-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-324">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-325">WebMessageReceived wird ausgelöst, wenn die ICoreWebView2Settings:: IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-325">WebMessageReceived fires when the ICoreWebView2Settings::IsWebMessageEnabled setting is set and the top level document of the WebView calls `window.chrome.webview.postMessage`.</span></span> <span data-ttu-id="6ca54-326">Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-326">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```html
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```
 <span data-ttu-id="6ca54-327">Wenn PostMessage aufgerufen wird, wird die Invoke-Methode des Handlers aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-327">When postMessage is called, the handler's Invoke method will be called with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="6ca54-328">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-328">add_WebResourceRequested</span></span> 

<span data-ttu-id="6ca54-329">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-329">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="6ca54-330">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-330">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-331">WebResourceRequested wird ausgelöst, wenn die WebView eine URL-Anforderung an einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-331">WebResourceRequested fires when the WebView is performing a URL request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="6ca54-332">Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-332">At least one filter must be added for the event to fire.</span></span>

<span data-ttu-id="6ca54-333">Die angeforderte Webressource kann blockiert werden, bis der Ereignishandler zurückgegeben wird, wenn keine Verzögerung für die Ereignis args übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-333">The web resource requested can be blocked until the event handler returns if a deferral is not taken on the event args.</span></span> <span data-ttu-id="6ca54-334">Wenn eine Verzögerung durchgeführt wird, wird die angeforderte Webressource blockiert, bis die Verzögerung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-334">If a deferral is taken, then the web resource requested is blocked until the deferral is completed.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="6ca54-335">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-335">add_WindowCloseRequested</span></span> 

<span data-ttu-id="6ca54-336">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-336">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="6ca54-337">Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-337">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6ca54-338">WindowCloseRequested wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close.</span><span class="sxs-lookup"><span data-stu-id="6ca54-338">WindowCloseRequested fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="6ca54-339">Die APP sollte das Fenster WebView und verwandte APP schließen, wenn dies für die APP sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-339">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>([this](
                                                                    ICoreWebView2* sender,
                                                                    IUnknown* args) {
            if (m_isPopupWindow)
            {
                CloseAppWindow();
            }
            return S_OK;
        }).Get(),
        nullptr));
```

#### <span data-ttu-id="6ca54-340">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="6ca54-340">AddHostObjectToScript</span></span> 

<span data-ttu-id="6ca54-341">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-341">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="6ca54-342">Public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR-Name; Variant \*-Objekt)</span><span class="sxs-lookup"><span data-stu-id="6ca54-342">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="6ca54-343">Hostobjekte werden als Hostobjekt Proxys über `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-343">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="6ca54-344">Hostobjekt Proxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-344">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="6ca54-345">Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="6ca54-345">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="6ca54-346">Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="6ca54-346">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="6ca54-347">Wenn der Anwendungscode beispielsweise Folgendes durchführt:</span><span class="sxs-lookup"><span data-stu-id="6ca54-347">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="6ca54-348">JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen:</span><span class="sxs-lookup"><span data-stu-id="6ca54-348">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="6ca54-349">Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-349">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="6ca54-350">Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-350">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="6ca54-351">Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-351">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="6ca54-352">Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-352">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="6ca54-353">Arrays von nach Verweistypen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-353">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="6ca54-354">VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-354">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="6ca54-355">In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-355">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="6ca54-356">Darüber hinaus werden alle Hostobjekte als verfügbar gemacht `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-356">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="6ca54-357">Hier werden die Hostobjekte als synchrone Hostobjekt Proxys verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="6ca54-357">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="6ca54-358">Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="6ca54-358">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="6ca54-359">Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.hostObjects.<name>` API verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-359">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="6ca54-360">Synchrone Hostobjekt Proxys und asynchrone Hostobjekt Proxys können beide Proxys für dasselbe Hostobjekt bereithalten.</span><span class="sxs-lookup"><span data-stu-id="6ca54-360">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="6ca54-361">Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Hostobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.</span><span class="sxs-lookup"><span data-stu-id="6ca54-361">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="6ca54-362">Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-362">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="6ca54-363">Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.</span><span class="sxs-lookup"><span data-stu-id="6ca54-363">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="6ca54-364">Host Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-364">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="6ca54-365">Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-365">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="6ca54-366">Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.hostObjects.options.forceLocalProperties` lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-366">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="6ca54-367">Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-367">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="6ca54-368">Sie können diesem Array nach Bedarf weitere hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-368">You can add more to this array as required.</span></span>

<span data-ttu-id="6ca54-369">Es gibt eine Methode `chrome.webview.hostObjects.cleanupSome` , mit der die Garbage Collection von Hostobjekt Proxys am besten abläuft.</span><span class="sxs-lookup"><span data-stu-id="6ca54-369">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="6ca54-370">Host Objektproxys verfügen zusätzlich über die folgenden Methoden, die lokal ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="6ca54-370">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="6ca54-371">applyHostFunction, gethostproperty, sethostproperty: führen Sie einen Methodenaufruf, eine Eigenschaft Get oder einen Eigenschaftssatz für das Hostobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="6ca54-371">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="6ca54-372">Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-372">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="6ca54-373">Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="6ca54-373">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="6ca54-374">`proxy.applyHostFunction('toString')`Wird aber `toString` stattdessen auf dem Host Proxyobjekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-374">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="6ca54-375">getlocalproperty, setlocalproperty: Ausführen von Eigenschaften abrufen oder Eigenschaftssatz lokal.</span><span class="sxs-lookup"><span data-stu-id="6ca54-375">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="6ca54-376">Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Hostobjekt Proxy selbst zu erzwingen, anstatt auf das Hostobjekt, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-376">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="6ca54-377">Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Host Proxyobjekt benannt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-377">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="6ca54-378">`proxy.getLocalProperty('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-378">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="6ca54-379">Synchronisierung: asynchrone Hostobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die eine Versprechung für einen synchronen Hostobjekt Proxy für dasselbe Hostobjekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-379">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="6ca54-380">Gibt beispielsweise `chrome.webview.hostObjects.sample.methodCall()` einen asynchronen Hostobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="6ca54-380">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="6ca54-381">Stattdessen können Sie die `sync` Methode zum Abrufen eines synchronen Hostobjekt Proxys verwenden:</span><span class="sxs-lookup"><span data-stu-id="6ca54-381">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="6ca54-382">Async: synchrone Hostobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Hostobjekt Proxy für dasselbe Hostobjekt blockiert und zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-382">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="6ca54-383">Gibt beispielsweise `chrome.webview.hostObjects.sync.sample.methodCall()` einen synchronen Hostobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="6ca54-383">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="6ca54-384">Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Hostobjekt Proxys für dasselbe Hostobjekt:</span><span class="sxs-lookup"><span data-stu-id="6ca54-384">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="6ca54-385">dann: asynchrone Hostobjekt Proxys verfügen über eine then-Methode.</span><span class="sxs-lookup"><span data-stu-id="6ca54-385">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="6ca54-386">Auf diese Weise können Sie warten.</span><span class="sxs-lookup"><span data-stu-id="6ca54-386">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="6ca54-387">gibt eine Verheißung zurück, die mit einer Darstellung des Hostobjekts aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-387">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="6ca54-388">Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ca54-388">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="6ca54-389">Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ca54-389">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="6ca54-390">Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Hostobjekt Proxys zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ca54-390">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="6ca54-391">Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-391">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="6ca54-392">Asynchrone Hostobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-392">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="6ca54-393">Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-393">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="6ca54-394">Synchrone Hostobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-394">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="6ca54-395">Das Festlegen einer Eigenschaft für einen asynchronen Hostobjekt Proxy funktioniert etwas anders.</span><span class="sxs-lookup"><span data-stu-id="6ca54-395">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="6ca54-396">Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-396">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="6ca54-397">Dies ist eine Anforderung des JavaScript-Proxy Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ca54-397">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="6ca54-398">Wenn Sie asynchron warten müssen, bis der Eigenschaftssatz abgeschlossen ist, verwenden Sie die sethostproperty-Methode, die eine Verheißung zurückgibt, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ca54-398">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="6ca54-399">Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-399">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="6ca54-400">Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6ca54-400">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IHostObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        [propget] HRESULT IndexedProperty(INT index, [out, retval] BSTR * stringResult);
        [propput] HRESULT IndexedProperty(INT index, [in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);

    };
```
 <span data-ttu-id="6ca54-401">Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-401">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="6ca54-402">In diesem Fall nennen wir `sample` Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6ca54-402">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_hostObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddHostObjectToScript multiple times in a row without
            // calling RemoveHostObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(
                m_webView->AddHostObjectToScript(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```
 <span data-ttu-id="6ca54-403">Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.hostObjects.sample` Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="6ca54-403">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

```html
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = await chrome.webview.hostObjects.sample.property;
        document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
        const propertyValue = chrome.webview.hostObjects.sync.sample.property;
        document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyAsyncInput").value;
        // The following line will work but it will return immediately before the property value has actually been set.
        // If you need to set the property and wait for the property to change value, use the setHostProperty function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setHostProperty function.
        await chrome.webview.hostObjects.sample.setHostProperty("property", propertyValue);
        document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
        const propertyValue = document.getElementById("setPropertySyncInput").value;
        chrome.webview.hostObjects.sync.sample.property = propertyValue;
        document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("getIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("getIndexedPropertyAsyncParam").value);
        const resultValue = await chrome.webview.hostObjects.sample.IndexedProperty[index];
        document.getElementById("getIndexedPropertyAsyncOutput").textContent = resultValue;
        });
        document.getElementById("setIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("setIndexedPropertyAsyncParam1").value);
        const value = document.getElementById("setIndexedPropertyAsyncParam2").value;;
        chrome.webview.hostObjects.sample.IndexedProperty[index] = value;
        document.getElementById("setIndexedPropertyAsyncOutput").textContent = "Set";
        });
        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
        const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
        const resultValue = await chrome.webview.hostObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
        const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
        const resultValue = chrome.webview.hostObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
        chrome.webview.hostObjects.sample.CallCallbackAsynchronously(() => {
        document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
        });
        });
```
<span data-ttu-id="6ca54-404">Das verfügbar machen von Host Objekten für Skripts hat ein Sicherheitsrisiko.</span><span class="sxs-lookup"><span data-stu-id="6ca54-404">Exposing host objects to script has security risk.</span></span> <span data-ttu-id="6ca54-405">Befolgen Sie die [bewährten Methoden](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span><span class="sxs-lookup"><span data-stu-id="6ca54-405">Please follow [best practices](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span></span>

#### <span data-ttu-id="6ca54-406">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="6ca54-406">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="6ca54-407">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-407">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="6ca54-408">Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="6ca54-408">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="6ca54-409">Mit dieser Methode wird ein Skript eingefügt, das auf allen Dokument-und untergeordneten Frameseiten Navigationen auf oberster Ebene ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-409">This method injects a script that runs on all top-level document and child frame page navigations.</span></span> <span data-ttu-id="6ca54-410">Diese Methode wird asynchron ausgeführt, und Sie müssen warten, bis der vervollständigungshandler fertig ist, bevor das eingefügte Skript ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ca54-410">This method runs asynchronously, and you must wait for the completion handler to finish before the injected script is ready to run.</span></span> <span data-ttu-id="6ca54-411">Nach Abschluss dieser Methode wird die Methode des Handlers `Invoke` mit dem `id` injizierten Skript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-411">When this method completes, the handler's `Invoke` method is called with the `id` of the injected script.</span></span> `id` <span data-ttu-id="6ca54-412">ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6ca54-412">is a string.</span></span> <span data-ttu-id="6ca54-413">Wenn Sie das eingefügte Skript entfernen möchten, verwenden Sie `RemoveScriptToExecuteOnDocumentCreated` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-413">To remove the injected script, use `RemoveScriptToExecuteOnDocumentCreated`.</span></span>

<span data-ttu-id="6ca54-414">Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat.</span><span class="sxs-lookup"><span data-stu-id="6ca54-414">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="6ca54-415">Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-415">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="6ca54-416">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="6ca54-416">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="6ca54-417">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-417">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="6ca54-418">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="6ca54-418">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="6ca54-419">Der URI-Parameter kann eine Platzhalterzeichenfolge (' \* ': 0 oder mehr; "?": genau eins) sein.</span><span class="sxs-lookup"><span data-stu-id="6ca54-419">The URI parameter can be a wildcard string ('\*': zero or more, '?': exactly one).</span></span> <span data-ttu-id="6ca54-420">nullptr entspricht L "".</span><span class="sxs-lookup"><span data-stu-id="6ca54-420">nullptr is equivalent to L"".</span></span> <span data-ttu-id="6ca54-421">Eine Beschreibung der Ressourcenkontext Filter finden Sie unter COREWEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="6ca54-421">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="6ca54-422">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="6ca54-422">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="6ca54-423">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6ca54-423">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="6ca54-424">Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="6ca54-424">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="6ca54-425">Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="6ca54-425">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="6ca54-426">Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-426">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="6ca54-427">Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="6ca54-427">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="6ca54-428">Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-428">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="6ca54-429">Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-429">Invoke will be called with the method's return object as a JSON string.</span></span>

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="6ca54-430">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="6ca54-430">CapturePreview</span></span> 

<span data-ttu-id="6ca54-431">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-431">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="6ca54-432">Public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) Image Format, IStream \* ImageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \*-Handler)</span><span class="sxs-lookup"><span data-stu-id="6ca54-432">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="6ca54-433">Geben Sie das Format des Bilds mit dem ImageFormat-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="6ca54-433">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="6ca54-434">Die resultierenden Bild Binärdaten werden in den bereitgestellten ImageStream-Parameter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ca54-434">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="6ca54-435">Wenn CapturePreview den Schreibvorgang in den Datenstrom abgeschlossen hat, wird die Invoke-Methode für den bereitgestellten Handler-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-435">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="6ca54-436">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="6ca54-436">ExecuteScript</span></span> 

<span data-ttu-id="6ca54-437">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-437">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="6ca54-438">Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="6ca54-438">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="6ca54-439">Dies wird asynchron ausgeführt, und wenn ein Handler im ExecuteScriptCompletedHandler-Parameter bereitgestellt wird, wird die Invoke-Methode mit dem Ergebnis der Auswertung des bereitgestellten JavaScript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-439">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="6ca54-440">Der Ergebniswert ist eine JSON-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6ca54-440">The result value is a JSON encoded string.</span></span> <span data-ttu-id="6ca54-441">Wenn das Ergebnis undefiniert ist, einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird der JSON-NULL-Wert als Zeichenfolge "Null" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ca54-441">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="6ca54-442">Beachten Sie, dass eine Funktion, die keinen expliziten Rückgabewert aufweist, undefined zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-442">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="6ca54-443">Wenn das ausgeführte Skript eine nicht behandelte Ausnahme auslöst, ist das Ergebnis auch "Null".</span><span class="sxs-lookup"><span data-stu-id="6ca54-443">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="6ca54-444">Diese Methode wird asynchron angewendet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-444">This method is applied asynchronously.</span></span> <span data-ttu-id="6ca54-445">Wenn die Methode nach dem NavigationStarting-Ereignis während einer Navigation aufgerufen wird, wird das Skript beim Laden des Skripts im neuen Dokument ausgeführt, und zwar um den Zeitpunkt, zu dem ContentLoading ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-445">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="6ca54-446">ExecuteScript funktioniert auch dann, wenn ICoreWebView2Settings:: IsScriptEnabled auf "false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-446">ExecuteScript will work even if ICoreWebView2Settings::IsScriptEnabled is set to FALSE.</span></span>

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### <span data-ttu-id="6ca54-447">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="6ca54-447">get_BrowserProcessId</span></span> 

<span data-ttu-id="6ca54-448">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-448">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="6ca54-449">Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="6ca54-449">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="6ca54-450">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="6ca54-450">get_CanGoBack</span></span> 

<span data-ttu-id="6ca54-451">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="6ca54-451">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="6ca54-452">Public HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="6ca54-452">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="6ca54-453">Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoBack geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-453">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="6ca54-454">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="6ca54-454">get_CanGoForward</span></span> 

<span data-ttu-id="6ca54-455">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="6ca54-455">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="6ca54-456">Public HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="6ca54-456">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="6ca54-457">Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoForward geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-457">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="6ca54-458">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="6ca54-458">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="6ca54-459">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="6ca54-459">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="6ca54-460">Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="6ca54-460">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="6ca54-461">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="6ca54-461">get_DocumentTitle</span></span> 

<span data-ttu-id="6ca54-462">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="6ca54-462">The title for the current top level document.</span></span>

> <span data-ttu-id="6ca54-463">öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="6ca54-463">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="6ca54-464">Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-464">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="6ca54-465">get_Settings</span><span class="sxs-lookup"><span data-stu-id="6ca54-465">get_Settings</span></span> 

<span data-ttu-id="6ca54-466">Das [ICoreWebView2Settings](icorewebview2settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-466">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="6ca54-467">öffentliche HRESULT- [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \* \*-Einstellungen)</span><span class="sxs-lookup"><span data-stu-id="6ca54-467">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="6ca54-468">get_Source</span><span class="sxs-lookup"><span data-stu-id="6ca54-468">get_Source</span></span> 

<span data-ttu-id="6ca54-469">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="6ca54-469">The URI of the current top level document.</span></span>

> <span data-ttu-id="6ca54-470">Public HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="6ca54-470">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="6ca54-471">Dieser Wert ändert sich möglicherweise als Teil der Ereignis Befeuerungs Quelle für einige Fälle, beispielsweise das Navigieren zu einer anderen Website oder zu einer anderen Fragment-Navigation.</span><span class="sxs-lookup"><span data-stu-id="6ca54-471">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="6ca54-472">Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-472">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="6ca54-473">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="6ca54-473">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="6ca54-474">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="6ca54-474">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="6ca54-475">Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="6ca54-475">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="6ca54-476">Der eventName-Parameter ist der vollständige Name des Ereignisses im Format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-476">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="6ca54-477">Eine Liste der Beschreibungen von devtools-Protokollereignissen und Ereignis args finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="6ca54-477">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="6ca54-478">GoBack</span><span class="sxs-lookup"><span data-stu-id="6ca54-478">GoBack</span></span> 

<span data-ttu-id="6ca54-479">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="6ca54-479">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="6ca54-480">Public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="6ca54-480">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="6ca54-481">GoForward</span><span class="sxs-lookup"><span data-stu-id="6ca54-481">GoForward</span></span> 

<span data-ttu-id="6ca54-482">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="6ca54-482">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="6ca54-483">Public HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="6ca54-483">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="6ca54-484">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="6ca54-484">Navigate</span></span> 

<span data-ttu-id="6ca54-485">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="6ca54-485">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="6ca54-486">öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="6ca54-486">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="6ca54-487">Weitere Informationen finden Sie in den Navigations Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-487">See the navigation events for more information.</span></span> <span data-ttu-id="6ca54-488">Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-488">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(GetAddressBar());
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(GetAddressBar(), buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
}
```

#### <span data-ttu-id="6ca54-489">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="6ca54-489">NavigateToString</span></span> 

<span data-ttu-id="6ca54-490">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="6ca54-490">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="6ca54-491">Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="6ca54-491">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="6ca54-492">Der htmlContent-Parameter darf nicht größer als 2 MB in der Gesamtgröße sein.</span><span class="sxs-lookup"><span data-stu-id="6ca54-492">The htmlContent parameter may not be larger than 2 MB in total size.</span></span> <span data-ttu-id="6ca54-493">Der Ursprung der neuen Seite lautet: leer.</span><span class="sxs-lookup"><span data-stu-id="6ca54-493">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="6ca54-494">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="6ca54-494">OpenDevToolsWindow</span></span> 

<span data-ttu-id="6ca54-495">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-495">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="6ca54-496">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="6ca54-496">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="6ca54-497">Wenn das devtools-Fenster bereits geöffnet ist, wird Nothing aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-497">Does nothing if called when the DevTools window is already open.</span></span>

#### <span data-ttu-id="6ca54-498">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="6ca54-498">PostWebMessageAsJson</span></span> 

<span data-ttu-id="6ca54-499">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-499">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="6ca54-500">Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="6ca54-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="6ca54-501">Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6ca54-501">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="6ca54-502">JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen:</span><span class="sxs-lookup"><span data-stu-id="6ca54-502">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="6ca54-503">Das Ereignis args ist eine Instanz von `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="6ca54-503">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="6ca54-504">Die ICoreWebView2Settings:: IsWebMessageEnabled-Einstellung muss wahr sein, oder diese Methode schlägt mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="6ca54-504">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="6ca54-505">Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-505">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="6ca54-506">Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-506">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="6ca54-507">Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="6ca54-507">See add_WebMessageReceived for information on sending messages from the HTML document in the WebView to the host.</span></span> <span data-ttu-id="6ca54-508">Diese Nachricht wird asynchron gesendet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-508">This message is sent asynchronously.</span></span> <span data-ttu-id="6ca54-509">Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="6ca54-509">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="6ca54-510">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="6ca54-510">PostWebMessageAsString</span></span> 

<span data-ttu-id="6ca54-511">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-511">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="6ca54-512">Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="6ca54-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="6ca54-513">Dies verhält sich auf die gleiche Weise wie PostWebMessageAsJson, aber die `window.chrome.webview` Dateneigenschaft des Nachrichtenereignisses arg ist eine Zeichenfolge mit dem gleichen Wert wie webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="6ca54-513">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="6ca54-514">Verwenden Sie diese anstelle von PostWebMessageAsJson, wenn Sie über einfache Zeichenfolgen anstelle von JSON-Objekten kommunizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6ca54-514">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="6ca54-515">Laden</span><span class="sxs-lookup"><span data-stu-id="6ca54-515">Reload</span></span> 

<span data-ttu-id="6ca54-516">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="6ca54-516">Reload the current page.</span></span>

> <span data-ttu-id="6ca54-517">Public HRESULT [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="6ca54-517">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="6ca54-518">Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren.</span><span class="sxs-lookup"><span data-stu-id="6ca54-518">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="6ca54-519">Das zurück/weiter-Protokoll wird jedoch nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-519">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="6ca54-520">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-520">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="6ca54-521">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContainsFullScreenElementChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-521">Remove an event handler previously added with add_ContainsFullScreenElementChanged.</span></span>

> <span data-ttu-id="6ca54-522">Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-522">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-523">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="6ca54-523">remove_ContentLoading</span></span> 

<span data-ttu-id="6ca54-524">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-524">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="6ca54-525">Public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-525">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-526">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-526">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="6ca54-527">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-527">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="6ca54-528">Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-528">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-529">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-529">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="6ca54-530">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-530">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="6ca54-531">Public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-531">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-532">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-532">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="6ca54-533">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-533">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="6ca54-534">Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-534">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-535">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-535">remove_HistoryChanged</span></span> 

<span data-ttu-id="6ca54-536">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-536">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="6ca54-537">Public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-537">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-538">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6ca54-538">remove_NavigationCompleted</span></span> 

<span data-ttu-id="6ca54-539">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-539">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="6ca54-540">Public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-540">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-541">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6ca54-541">remove_NavigationStarting</span></span> 

<span data-ttu-id="6ca54-542">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-542">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="6ca54-543">Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-543">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-544">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-544">remove_NewWindowRequested</span></span> 

<span data-ttu-id="6ca54-545">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-545">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="6ca54-546">Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-546">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-547">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-547">remove_PermissionRequested</span></span> 

<span data-ttu-id="6ca54-548">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-548">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="6ca54-549">Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-549">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-550">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="6ca54-550">remove_ProcessFailed</span></span> 

<span data-ttu-id="6ca54-551">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-551">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="6ca54-552">Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-552">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-553">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="6ca54-553">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="6ca54-554">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-554">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="6ca54-555">Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-555">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-556">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="6ca54-556">remove_SourceChanged</span></span> 

<span data-ttu-id="6ca54-557">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-557">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="6ca54-558">Public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-558">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-559">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="6ca54-559">remove_WebMessageReceived</span></span> 

<span data-ttu-id="6ca54-560">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-560">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="6ca54-561">Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-561">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-562">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-562">remove_WebResourceRequested</span></span> 

<span data-ttu-id="6ca54-563">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-563">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="6ca54-564">Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-564">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-565">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="6ca54-565">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="6ca54-566">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-566">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="6ca54-567">Public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="6ca54-567">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6ca54-568">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="6ca54-568">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="6ca54-569">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="6ca54-569">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="6ca54-570">Public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="6ca54-570">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="6ca54-571">Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-571">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="6ca54-572">Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="6ca54-572">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="6ca54-573">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="6ca54-573">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="6ca54-574">Entfernen Sie das entsprechende JavaScript `AddScriptToExecuteOnDocumentCreated` , das mit der angegebenen Skript-ID hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-574">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>

> <span data-ttu-id="6ca54-575">Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="6ca54-575">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="6ca54-576">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="6ca54-576">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="6ca54-577">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-577">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="6ca54-578">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="6ca54-578">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="6ca54-579">Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-579">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="6ca54-580">Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-580">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="6ca54-581">Stop</span><span class="sxs-lookup"><span data-stu-id="6ca54-581">Stop</span></span> 

<span data-ttu-id="6ca54-582">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="6ca54-582">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="6ca54-583">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="6ca54-583">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="6ca54-584">Skripts werden nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="6ca54-584">Does not stop scripts.</span></span>

#### <span data-ttu-id="6ca54-585">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="6ca54-585">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="6ca54-586">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-586">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="6ca54-587">Enum- [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="6ca54-587">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="6ca54-588">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-588">Values</span></span>                         | <span data-ttu-id="6ca54-589">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-589">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-590">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="6ca54-590">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="6ca54-591">PNG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="6ca54-591">PNG image format.</span></span>
<span data-ttu-id="6ca54-592">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="6ca54-592">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="6ca54-593">JPEG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="6ca54-593">JPEG image format.</span></span>

#### <span data-ttu-id="6ca54-594">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-594">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="6ca54-595">Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="6ca54-595">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="6ca54-596">Enum- [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span><span class="sxs-lookup"><span data-stu-id="6ca54-596">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="6ca54-597">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-597">Values</span></span>                         | <span data-ttu-id="6ca54-598">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-598">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-599">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="6ca54-599">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="6ca54-600">Dem Fenster Nachrichten WM_KEYDOWN entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-600">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="6ca54-601">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="6ca54-601">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="6ca54-602">Dem Fenster Nachrichten WM_KEYUP entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-602">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="6ca54-603">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="6ca54-603">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="6ca54-604">Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-604">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="6ca54-605">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="6ca54-605">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="6ca54-606">Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-606">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="6ca54-607">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="6ca54-607">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="6ca54-608">Grund für das Verschieben des Fokus</span><span class="sxs-lookup"><span data-stu-id="6ca54-608">Reason for moving focus.</span></span>

> <span data-ttu-id="6ca54-609">Enum- [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="6ca54-609">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="6ca54-610">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-610">Values</span></span>                         | <span data-ttu-id="6ca54-611">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-611">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-612">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="6ca54-612">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="6ca54-613">Der Fokus für die Code Einstellung in WebView.</span><span class="sxs-lookup"><span data-stu-id="6ca54-613">Code setting focus into WebView.</span></span>
<span data-ttu-id="6ca54-614">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="6ca54-614">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="6ca54-615">Verschieben des Fokus aufgrund von Tabstopps vorwärts</span><span class="sxs-lookup"><span data-stu-id="6ca54-615">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="6ca54-616">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="6ca54-616">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="6ca54-617">Verschieben des Fokus aufgrund von Tabstopps rückwärts</span><span class="sxs-lookup"><span data-stu-id="6ca54-617">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="6ca54-618">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-618">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="6ca54-619">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6ca54-619">The type of a permission request.</span></span>

> <span data-ttu-id="6ca54-620">Enum- [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="6ca54-620">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="6ca54-621">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-621">Values</span></span>                         | <span data-ttu-id="6ca54-622">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-622">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-623">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="6ca54-623">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="6ca54-624">Unbekannte Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="6ca54-624">Unknown permission.</span></span>
<span data-ttu-id="6ca54-625">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="6ca54-625">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="6ca54-626">Berechtigung zum Aufzeichnen von Audio.</span><span class="sxs-lookup"><span data-stu-id="6ca54-626">Permission to capture audio.</span></span>
<span data-ttu-id="6ca54-627">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="6ca54-627">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="6ca54-628">Berechtigung zum Aufzeichnen von Videos.</span><span class="sxs-lookup"><span data-stu-id="6ca54-628">Permission to capture video.</span></span>
<span data-ttu-id="6ca54-629">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="6ca54-629">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="6ca54-630">Berechtigung für den Zugriff auf Geolocation.</span><span class="sxs-lookup"><span data-stu-id="6ca54-630">Permission to access geolocation.</span></span>
<span data-ttu-id="6ca54-631">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="6ca54-631">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="6ca54-632">Berechtigung zum Senden von webbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-632">Permission to send web notifications.</span></span>
<span data-ttu-id="6ca54-633">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="6ca54-633">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="6ca54-634">Berechtigung für den Zugriff auf den generischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="6ca54-634">Permission to access generic sensor.</span></span>
<span data-ttu-id="6ca54-635">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="6ca54-635">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="6ca54-636">Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste</span><span class="sxs-lookup"><span data-stu-id="6ca54-636">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="6ca54-637">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="6ca54-637">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="6ca54-638">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6ca54-638">Response to a permission request.</span></span>

> <span data-ttu-id="6ca54-639">Enum- [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="6ca54-639">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="6ca54-640">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-640">Values</span></span>                         | <span data-ttu-id="6ca54-641">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-641">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-642">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6ca54-642">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="6ca54-643">Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-643">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="6ca54-644">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="6ca54-644">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="6ca54-645">Erteilen Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6ca54-645">Grant the permission request.</span></span>
<span data-ttu-id="6ca54-646">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="6ca54-646">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="6ca54-647">Verweigern Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6ca54-647">Deny the permission request.</span></span>

#### <span data-ttu-id="6ca54-648">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="6ca54-648">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="6ca54-649">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-649">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="6ca54-650">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="6ca54-650">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="6ca54-651">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN. [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="6ca54-651">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="6ca54-652">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-652">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="6ca54-653">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6ca54-653">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="6ca54-654">Enum- [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="6ca54-654">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="6ca54-655">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-655">Values</span></span>                         | <span data-ttu-id="6ca54-656">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-656">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-657">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="6ca54-657">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="6ca54-658">Gibt an, dass der Browserprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-658">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="6ca54-659">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="6ca54-659">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="6ca54-660">Gibt an, dass der Renderprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ca54-660">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="6ca54-661">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="6ca54-661">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="6ca54-662">Gibt an, dass der Renderprozess nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="6ca54-662">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="6ca54-663">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="6ca54-663">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="6ca54-664">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="6ca54-664">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="6ca54-665">Enum- [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="6ca54-665">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="6ca54-666">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-666">Values</span></span>                         | <span data-ttu-id="6ca54-667">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-668">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="6ca54-668">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="6ca54-669">Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-669">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="6ca54-670">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="6ca54-670">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="6ca54-671">Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-671">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="6ca54-672">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="6ca54-672">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="6ca54-673">Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-673">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="6ca54-674">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="6ca54-674">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="6ca54-675">Ein Dialogfeld, das über das beforeunload-JavaScript-Ereignis aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6ca54-675">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="6ca54-676">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="6ca54-676">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="6ca54-677">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="6ca54-677">Error status values for web navigations.</span></span>

> <span data-ttu-id="6ca54-678">Enum- [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="6ca54-678">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="6ca54-679">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-679">Values</span></span>                         | <span data-ttu-id="6ca54-680">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-680">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-681">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="6ca54-681">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="6ca54-682">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6ca54-682">An unknown error occurred.</span></span>
<span data-ttu-id="6ca54-683">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="6ca54-683">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="6ca54-684">Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.</span><span class="sxs-lookup"><span data-stu-id="6ca54-684">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="6ca54-685">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="6ca54-685">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="6ca54-686">Das SSL-Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-686">The SSL certificate has expired.</span></span>
<span data-ttu-id="6ca54-687">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6ca54-687">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="6ca54-688">Das SSL-Clientzertifikat enthält Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ca54-688">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="6ca54-689">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="6ca54-689">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="6ca54-690">Das SSL-Zertifikat wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-690">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="6ca54-691">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="6ca54-691">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="6ca54-692">Das SSL-Zertifikat ist ungültig &ndash; Dies könnte bedeuten, dass das Zertifikat nicht mit den öffentlichen Schlüssel Pins für den Hostnamen übereinstimmte. das Zertifikat wird von einer nicht vertrauenswürdigen Zertifizierungsstelle signiert oder mit einem schwachen Vorzeichen Algorithmus, das Zertifikat behauptet, dass DNS-Namen gegen Namenseinschränkungen verstoßen, das Zertifikat einen schwachen Schlüssel enthält, der Gültigkeitszeitraum des Zertifikats zu lang ist, fehlender Sperrungsinformationen oder Sperrungs Mechanismus, nicht eindeutiger [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)Hostname, fehlender Zertifikat Transparenzinformationen oder das Zertifikat an</span><span class="sxs-lookup"><span data-stu-id="6ca54-692">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="6ca54-693">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="6ca54-693">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="6ca54-694">Der Host ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="6ca54-694">The host is unreachable.</span></span>
<span data-ttu-id="6ca54-695">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6ca54-695">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="6ca54-696">Die Verbindung hat ein Zeitlimit überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ca54-696">The connection has timed out.</span></span>
<span data-ttu-id="6ca54-697">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="6ca54-697">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="6ca54-698">Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ca54-698">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="6ca54-699">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="6ca54-699">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="6ca54-700">Die Verbindung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-700">The connection was aborted.</span></span>
<span data-ttu-id="6ca54-701">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="6ca54-701">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="6ca54-702">Die Verbindung wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6ca54-702">The connection was reset.</span></span>
<span data-ttu-id="6ca54-703">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="6ca54-703">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="6ca54-704">Die Internet Verbindung wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-704">The Internet connection has been lost.</span></span>
<span data-ttu-id="6ca54-705">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="6ca54-705">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="6ca54-706">Verbindung mit Ziel kann nicht hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-706">Cannot connect to destination.</span></span>
<span data-ttu-id="6ca54-707">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="6ca54-707">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="6ca54-708">Der angegebene Hostname konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="6ca54-708">Could not resolve provided host name.</span></span>
<span data-ttu-id="6ca54-709">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="6ca54-709">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="6ca54-710">Der Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-710">The operation was canceled.</span></span>
<span data-ttu-id="6ca54-711">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="6ca54-711">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="6ca54-712">Die Anforderungs Umleitung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-712">The request redirect failed.</span></span>
<span data-ttu-id="6ca54-713">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="6ca54-713">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="6ca54-714">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6ca54-714">An unexpected error occurred.</span></span>

#### <span data-ttu-id="6ca54-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="6ca54-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="6ca54-716">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="6ca54-716">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="6ca54-717">Enum- [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="6ca54-717">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="6ca54-718">Werte</span><span class="sxs-lookup"><span data-stu-id="6ca54-718">Values</span></span>                         | <span data-ttu-id="6ca54-719">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="6ca54-719">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6ca54-720">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="6ca54-720">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="6ca54-721">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-721">All resources.</span></span>
<span data-ttu-id="6ca54-722">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="6ca54-722">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="6ca54-723">Dokument Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-723">Document resources.</span></span>
<span data-ttu-id="6ca54-724">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="6ca54-724">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="6ca54-725">CSS-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-725">CSS resources.</span></span>
<span data-ttu-id="6ca54-726">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="6ca54-726">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="6ca54-727">Bildressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-727">Image resources.</span></span>
<span data-ttu-id="6ca54-728">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="6ca54-728">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="6ca54-729">Andere Medienressourcen wie Videos.</span><span class="sxs-lookup"><span data-stu-id="6ca54-729">Other media resources such as videos.</span></span>
<span data-ttu-id="6ca54-730">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="6ca54-730">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="6ca54-731">Schriftartressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-731">Font resources.</span></span>
<span data-ttu-id="6ca54-732">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="6ca54-732">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="6ca54-733">Skriptressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-733">Script resources.</span></span>
<span data-ttu-id="6ca54-734">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="6ca54-734">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="6ca54-735">XML-HTTP-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-735">XML HTTP requests.</span></span>
<span data-ttu-id="6ca54-736">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="6ca54-736">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="6ca54-737">Abrufen der API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="6ca54-737">Fetch API communication.</span></span>
<span data-ttu-id="6ca54-738">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="6ca54-738">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="6ca54-739">Texttracking-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-739">TextTrack resources.</span></span>
<span data-ttu-id="6ca54-740">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="6ca54-740">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="6ca54-741">EventSource-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="6ca54-741">EventSource API communication.</span></span>
<span data-ttu-id="6ca54-742">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="6ca54-742">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="6ca54-743">WebSocket-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="6ca54-743">WebSocket API communication.</span></span>
<span data-ttu-id="6ca54-744">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="6ca54-744">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="6ca54-745">Web App-Manifeste</span><span class="sxs-lookup"><span data-stu-id="6ca54-745">Web App Manifests.</span></span>
<span data-ttu-id="6ca54-746">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="6ca54-746">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="6ca54-747">Signierte http-Exchanges.</span><span class="sxs-lookup"><span data-stu-id="6ca54-747">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="6ca54-748">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="6ca54-748">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="6ca54-749">Ping-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-749">Ping requests.</span></span>
<span data-ttu-id="6ca54-750">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="6ca54-750">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="6ca54-751">Berichte zu CSP-Verstößen</span><span class="sxs-lookup"><span data-stu-id="6ca54-751">CSP Violation Reports.</span></span>
<span data-ttu-id="6ca54-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="6ca54-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="6ca54-753">Andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ca54-753">Other resources.</span></span>

