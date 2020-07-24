---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2
ms.openlocfilehash: a1da6789027234130c58078871d7da23b4e285ba
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895497"
---
# <span data-ttu-id="4f7cf-104">Schnittstellen ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="4f7cf-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="4f7cf-105">WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="4f7cf-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4f7cf-106">Summary</span></span>

 <span data-ttu-id="4f7cf-107">Member</span><span class="sxs-lookup"><span data-stu-id="4f7cf-107">Members</span></span>                        | <span data-ttu-id="4f7cf-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4f7cf-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="4f7cf-110">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="4f7cf-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="4f7cf-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="4f7cf-112">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="4f7cf-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="4f7cf-114">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="4f7cf-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="4f7cf-116">Fügen Sie einen Ereignishandler für das FrameNavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="4f7cf-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="4f7cf-118">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="4f7cf-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="4f7cf-120">Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-120">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="4f7cf-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="4f7cf-122">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="4f7cf-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="4f7cf-124">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="4f7cf-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="4f7cf-126">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="4f7cf-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="4f7cf-128">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="4f7cf-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="4f7cf-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="4f7cf-130">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="4f7cf-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="4f7cf-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="4f7cf-132">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="4f7cf-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="4f7cf-134">Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-134">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="4f7cf-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="4f7cf-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="4f7cf-136">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-136">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="4f7cf-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="4f7cf-138">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="4f7cf-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="4f7cf-140">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="4f7cf-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="4f7cf-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="4f7cf-142">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="4f7cf-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="4f7cf-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="4f7cf-144">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="4f7cf-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="4f7cf-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="4f7cf-146">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="4f7cf-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="4f7cf-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="4f7cf-148">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="4f7cf-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="4f7cf-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="4f7cf-150">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="4f7cf-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="4f7cf-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="4f7cf-152">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="4f7cf-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="4f7cf-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="4f7cf-154">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="4f7cf-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="4f7cf-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="4f7cf-156">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-156">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="4f7cf-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="4f7cf-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="4f7cf-158">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-158">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="4f7cf-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="4f7cf-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="4f7cf-160">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="4f7cf-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="4f7cf-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="4f7cf-162">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-162">The title for the current top level document.</span></span>
[<span data-ttu-id="4f7cf-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="4f7cf-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="4f7cf-164">Das [ICoreWebView2Settings](icorewebview2settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="4f7cf-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="4f7cf-165">get_Source</span></span>](#get_source) | <span data-ttu-id="4f7cf-166">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="4f7cf-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="4f7cf-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="4f7cf-168">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="4f7cf-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="4f7cf-169">GoBack</span></span>](#goback) | <span data-ttu-id="4f7cf-170">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="4f7cf-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="4f7cf-171">GoForward</span></span>](#goforward) | <span data-ttu-id="4f7cf-172">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="4f7cf-173">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="4f7cf-173">Navigate</span></span>](#navigate) | <span data-ttu-id="4f7cf-174">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="4f7cf-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="4f7cf-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="4f7cf-176">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="4f7cf-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="4f7cf-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="4f7cf-178">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="4f7cf-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="4f7cf-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="4f7cf-180">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="4f7cf-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="4f7cf-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="4f7cf-182">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="4f7cf-183">Laden</span><span class="sxs-lookup"><span data-stu-id="4f7cf-183">Reload</span></span>](#reload) | <span data-ttu-id="4f7cf-184">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-184">Reload the current page.</span></span>
[<span data-ttu-id="4f7cf-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="4f7cf-186">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-186">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="4f7cf-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="4f7cf-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="4f7cf-188">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="4f7cf-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="4f7cf-190">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="4f7cf-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="4f7cf-192">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="4f7cf-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="4f7cf-194">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="4f7cf-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="4f7cf-196">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="4f7cf-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="4f7cf-198">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="4f7cf-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="4f7cf-200">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="4f7cf-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="4f7cf-202">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="4f7cf-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="4f7cf-204">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="4f7cf-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="4f7cf-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="4f7cf-206">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="4f7cf-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="4f7cf-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="4f7cf-208">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="4f7cf-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="4f7cf-210">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="4f7cf-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="4f7cf-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="4f7cf-212">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="4f7cf-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="4f7cf-214">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="4f7cf-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="4f7cf-216">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="4f7cf-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="4f7cf-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="4f7cf-218">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="4f7cf-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="4f7cf-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="4f7cf-220">Entfernen Sie das entsprechende JavaScript `AddScriptToExecuteOnDocumentCreated` , das mit der angegebenen Skript-ID hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-220">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>
[<span data-ttu-id="4f7cf-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="4f7cf-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="4f7cf-222">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="4f7cf-223">Stop</span><span class="sxs-lookup"><span data-stu-id="4f7cf-223">Stop</span></span>](#stop) | <span data-ttu-id="4f7cf-224">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="4f7cf-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="4f7cf-226">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="4f7cf-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="4f7cf-228">Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="4f7cf-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="4f7cf-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="4f7cf-230">Grund für das Verschieben des Fokus</span><span class="sxs-lookup"><span data-stu-id="4f7cf-230">Reason for moving focus.</span></span>
[<span data-ttu-id="4f7cf-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="4f7cf-232">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-232">The type of a permission request.</span></span>
[<span data-ttu-id="4f7cf-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="4f7cf-234">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-234">Response to a permission request.</span></span>
[<span data-ttu-id="4f7cf-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="4f7cf-236">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="4f7cf-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="4f7cf-238">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="4f7cf-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="4f7cf-240">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="4f7cf-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="4f7cf-242">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="4f7cf-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="4f7cf-244">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="4f7cf-245">Member</span><span class="sxs-lookup"><span data-stu-id="4f7cf-245">Members</span></span>

#### <span data-ttu-id="4f7cf-246">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-246">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="4f7cf-247">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-247">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="4f7cf-248">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-248">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-249">Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-249">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="4f7cf-250">Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-250">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="4f7cf-251">Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-251">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="4f7cf-252">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="4f7cf-252">add_ContentLoading</span></span> 

<span data-ttu-id="4f7cf-253">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-253">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="4f7cf-254">Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-254">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-255">ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden ContentLoading werden nicht ausgelöst, wenn dieselbe Seitennavigation erfolgt (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigation).</span><span class="sxs-lookup"><span data-stu-id="4f7cf-255">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="4f7cf-256">Dies folgt auf das NavigationStarting-Ereignis und das Source-Ereignis und steht vor den Ereignissen "History" und "NavigationCompleted".</span><span class="sxs-lookup"><span data-stu-id="4f7cf-256">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="4f7cf-257">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-257">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="4f7cf-258">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-258">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="4f7cf-259">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-259">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-260">Das Ereignis wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-260">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="4f7cf-261">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-261">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="4f7cf-262">Fügen Sie einen Ereignishandler für das FrameNavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-262">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="4f7cf-263">Public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-263">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-264">Das FrameNavigationCompleted-Ereignis wird ausgelöst, wenn ein untergeordneter Frame vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-264">FrameNavigationCompleted event fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="4f7cf-265">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-265">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="4f7cf-266">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-266">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="4f7cf-267">Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-267">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-268">FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-268">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="4f7cf-269">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-269">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="4f7cf-270">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-270">add_HistoryChanged</span></span> 

<span data-ttu-id="4f7cf-271">Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-271">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="4f7cf-272">Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-272">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-273">Verwenden Sie abrechnungshistorieändern, um zu überprüfen, ob sich CanGoBack/CanGoForward-Wert geändert hat.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-273">Use HistoryChange to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="4f7cf-274">"History" wird auch für die Verwendung von GoBack/GoForward ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-274">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="4f7cf-275">"History" wird nach "sourcely" und "ContentLoading" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-275">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="4f7cf-276">Fügen Sie einen Ereignishandler für das History-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-276">Add an event handler for the HistoryChanged event.</span></span> 
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

#### <span data-ttu-id="4f7cf-277">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-277">add_NavigationCompleted</span></span> 

<span data-ttu-id="4f7cf-278">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-278">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="4f7cf-279">Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-279">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-280">Das NavigationCompleted-Ereignis wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-280">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="4f7cf-281">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-281">add_NavigationStarting</span></span> 

<span data-ttu-id="4f7cf-282">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-282">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="4f7cf-283">Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-283">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-284">NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-284">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="4f7cf-285">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-285">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="4f7cf-286">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-286">add_NewWindowRequested</span></span> 

<span data-ttu-id="4f7cf-287">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-287">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="4f7cf-288">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-288">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-289">Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-289">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="4f7cf-290">Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-290">The app can pass a target webview that will be considered the opened window.</span></span>

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

                wil::com_ptr<ICoreWebView2ExperimentalNewWindowRequestedEventArgs>
                    experimentalArgs;
                CHECK_FAILURE(args->QueryInterface(IID_PPV_ARGS(&experimentalArgs)));
                wil::com_ptr<ICoreWebView2ExperimentalWindowFeatures> windowFeatures;
                CHECK_FAILURE(experimentalArgs->get_WindowFeatures(&windowFeatures));

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
                  newAppWindow = new AppWindow(m_creationModeId, L"", nullptr, true, windowRect, !!shouldHaveToolbar);
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

#### <span data-ttu-id="4f7cf-291">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-291">add_PermissionRequested</span></span> 

<span data-ttu-id="4f7cf-292">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-292">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="4f7cf-293">Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-293">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-294">Wird ausgelöst, wenn Inhalt in einer WebView-Anforderung die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-294">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="4f7cf-295">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="4f7cf-295">add_ProcessFailed</span></span> 

<span data-ttu-id="4f7cf-296">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-296">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="4f7cf-297">Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-297">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-298">Wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-298">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="4f7cf-299">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="4f7cf-299">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="4f7cf-300">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-300">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="4f7cf-301">Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-301">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-302">Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung oder Eingabeaufforderung) für die WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-302">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="4f7cf-303">Dieses Ereignis wird nur ausgelöst, wenn die ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-303">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="4f7cf-304">Das ScriptDialogOpening-Ereignis kann verwendet werden, um Dialogfelder zu unterdrücken oder Standarddialogfelder durch benutzerdefinierte Dialogfelder zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-304">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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

#### <span data-ttu-id="4f7cf-305">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-305">add_SourceChanged</span></span> 

<span data-ttu-id="4f7cf-306">Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-306">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="4f7cf-307">Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-307">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-308">Die Quelle wird ausgelöst, um zu einer anderen Website oder zu einer anderen Fragment-Navigation zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-308">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="4f7cf-309">Sie wird nicht für andere Navigations Typen wie "Seiten-Reload" oder "History. pushState" mit der gleichen URL wie die aktuelle Seite ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-309">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="4f7cf-310">Die Quelle wird vor ContentLoading für die Navigation zu einem neuen Dokument ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-310">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="4f7cf-311">Fügen Sie einen Ereignishandler für das Quellpfad-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-311">Add an event handler for the SourceChanged event.</span></span> 
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

#### <span data-ttu-id="4f7cf-312">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="4f7cf-312">add_WebMessageReceived</span></span> 

<span data-ttu-id="4f7cf-313">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-313">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="4f7cf-314">öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*-Handler, EventRegistrationToken \*-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-314">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-315">Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-315">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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
 <span data-ttu-id="4f7cf-316">Wenn PostMessage aufgerufen wird, wird der [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) -Satz über diese SetWebMessageReceivedEventHandler-Methode aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-316">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="4f7cf-317">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-317">add_WebResourceRequested</span></span> 

<span data-ttu-id="4f7cf-318">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-318">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="4f7cf-319">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-319">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-320">Wird ausgelöst, wenn die WebView eine URL-Anforderung für einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-320">Fires when the WebView is performing a URL request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="4f7cf-321">Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-321">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="4f7cf-322">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-322">add_WindowCloseRequested</span></span> 

<span data-ttu-id="4f7cf-323">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-323">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="4f7cf-324">Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-324">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="4f7cf-325">Wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-325">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="4f7cf-326">Die APP sollte das Fenster WebView und verwandte APP schließen, wenn dies für die APP sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-326">The app should close the WebView and related app window if that makes sense to the app.</span></span>

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

#### <span data-ttu-id="4f7cf-327">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="4f7cf-327">AddHostObjectToScript</span></span> 

<span data-ttu-id="4f7cf-328">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-328">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="4f7cf-329">Public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR-Name; Variant \*-Objekt)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-329">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="4f7cf-330">Hostobjekte werden als Hostobjekt Proxys über `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-330">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="4f7cf-331">Hostobjekt Proxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-331">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="4f7cf-332">Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-332">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="4f7cf-333">Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-333">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="4f7cf-334">Wenn der Anwendungscode beispielsweise Folgendes durchführt:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-334">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="4f7cf-335">JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-335">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="4f7cf-336">Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-336">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="4f7cf-337">Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-337">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="4f7cf-338">Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-338">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="4f7cf-339">Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-339">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="4f7cf-340">Arrays von nach Verweistypen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-340">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="4f7cf-341">VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-341">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="4f7cf-342">In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-342">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="4f7cf-343">Darüber hinaus werden alle Hostobjekte als verfügbar gemacht `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-343">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="4f7cf-344">Hier werden die Hostobjekte als synchrone Hostobjekt Proxys verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-344">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="4f7cf-345">Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-345">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="4f7cf-346">Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.hostObjects.<name>` API verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-346">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="4f7cf-347">Synchrone Hostobjekt Proxys und asynchrone Hostobjekt Proxys können beide Proxys für dasselbe Hostobjekt bereithalten.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-347">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="4f7cf-348">Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Hostobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-348">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="4f7cf-349">Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-349">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="4f7cf-350">Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-350">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="4f7cf-351">Host Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-351">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="4f7cf-352">Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-352">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="4f7cf-353">Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.hostObjects.options.forceLocalProperties` lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-353">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="4f7cf-354">Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-354">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="4f7cf-355">Sie können diesem Array nach Bedarf weitere hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-355">You can add more to this array as required.</span></span>

<span data-ttu-id="4f7cf-356">Es gibt eine Methode `chrome.webview.hostObjects.cleanupSome` , mit der die Garbage Collection von Hostobjekt Proxys am besten abläuft.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-356">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="4f7cf-357">Host Objektproxys verfügen zusätzlich über die folgenden Methoden, die lokal ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-357">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="4f7cf-358">applyHostFunction, gethostproperty, sethostproperty: führen Sie einen Methodenaufruf, eine Eigenschaft Get oder einen Eigenschaftssatz für das Hostobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-358">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="4f7cf-359">Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-359">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="4f7cf-360">Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-360">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="4f7cf-361">`proxy.applyHostFunction('toString')`Wird aber `toString` stattdessen auf dem Host Proxyobjekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-361">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="4f7cf-362">getlocalproperty, setlocalproperty: Ausführen von Eigenschaften abrufen oder Eigenschaftssatz lokal.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-362">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="4f7cf-363">Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Hostobjekt Proxy selbst zu erzwingen, anstatt auf das Hostobjekt, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-363">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="4f7cf-364">Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Host Proxyobjekt benannt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-364">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="4f7cf-365">`proxy.getLocalProperty('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-365">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="4f7cf-366">Synchronisierung: asynchrone Hostobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die eine Versprechung für einen synchronen Hostobjekt Proxy für dasselbe Hostobjekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-366">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="4f7cf-367">Gibt beispielsweise `chrome.webview.hostObjects.sample.methodCall()` einen asynchronen Hostobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-367">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="4f7cf-368">Stattdessen können Sie die `sync` Methode zum Abrufen eines synchronen Hostobjekt Proxys verwenden:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-368">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="4f7cf-369">Async: synchrone Hostobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Hostobjekt Proxy für dasselbe Hostobjekt blockiert und zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-369">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="4f7cf-370">Gibt beispielsweise `chrome.webview.hostObjects.sync.sample.methodCall()` einen synchronen Hostobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-370">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="4f7cf-371">Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Hostobjekt Proxys für dasselbe Hostobjekt:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-371">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="4f7cf-372">dann: asynchrone Hostobjekt Proxys verfügen über eine then-Methode.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-372">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="4f7cf-373">Auf diese Weise können Sie warten.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-373">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="4f7cf-374">gibt eine Verheißung zurück, die mit einer Darstellung des Hostobjekts aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-374">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="4f7cf-375">Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-375">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="4f7cf-376">Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-376">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="4f7cf-377">Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Hostobjekt Proxys zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-377">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="4f7cf-378">Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-378">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="4f7cf-379">Asynchrone Hostobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-379">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="4f7cf-380">Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-380">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="4f7cf-381">Synchrone Hostobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-381">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="4f7cf-382">Das Festlegen einer Eigenschaft für einen asynchronen Hostobjekt Proxy funktioniert etwas anders.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-382">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="4f7cf-383">Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-383">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="4f7cf-384">Dies ist eine Anforderung des JavaScript-Proxy Objekts.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-384">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="4f7cf-385">Wenn Sie asynchron warten müssen, bis der Eigenschaftssatz abgeschlossen ist, verwenden Sie die sethostproperty-Methode, die eine Verheißung zurückgibt, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-385">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="4f7cf-386">Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-386">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="4f7cf-387">Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-387">For example, suppose you have a COM object with the following interface</span></span>

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
 <span data-ttu-id="4f7cf-388">Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-388">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="4f7cf-389">In diesem Fall nennen wir `sample` Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-389">In this case we name it `sample`:</span></span>

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
 <span data-ttu-id="4f7cf-390">Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.hostObjects.sample` Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-390">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

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
        // If you need to set the property and wait for the property to change value, use the setRemote function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setRemote function.
        await chrome.webview.hostObjects.sample.setRemote("property", propertyValue);
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
<span data-ttu-id="4f7cf-391">Das verfügbar machen von Host Objekten für Skripts hat ein Sicherheitsrisiko.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-391">Exposing host objects to script has security risk.</span></span> <span data-ttu-id="4f7cf-392">Befolgen Sie die [bewährten Methoden](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span><span class="sxs-lookup"><span data-stu-id="4f7cf-392">Please follow [best practices](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span></span>

#### <span data-ttu-id="4f7cf-393">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="4f7cf-393">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="4f7cf-394">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-394">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="4f7cf-395">Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-395">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="4f7cf-396">Mit dieser Methode wird ein Skript eingefügt, das auf allen Dokument-und untergeordneten Frameseiten Navigationen auf oberster Ebene ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-396">This method injects a script that runs on all top-level document and child frame page navigations.</span></span> <span data-ttu-id="4f7cf-397">Diese Methode wird asynchron ausgeführt, und Sie müssen warten, bis der vervollständigungshandler fertig ist, bevor das eingefügte Skript ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-397">This method runs asynchronously, and you must wait for the completion handler to finish before the injected script is ready to run.</span></span> <span data-ttu-id="4f7cf-398">Nach Abschluss dieser Methode wird die Methode des Handlers `Invoke` mit dem `id` injizierten Skript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-398">When this method completes, the handler's `Invoke` method is called with the `id` of the injected script.</span></span> `id` <span data-ttu-id="4f7cf-399">ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-399">is a string.</span></span> <span data-ttu-id="4f7cf-400">Wenn Sie das eingefügte Skript entfernen möchten, verwenden Sie `RemoveScriptToExecuteOnDocumentCreated` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-400">To remove the injected script, use `RemoveScriptToExecuteOnDocumentCreated`.</span></span>

<span data-ttu-id="4f7cf-401">Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-401">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="4f7cf-402">Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-402">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="4f7cf-403">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="4f7cf-403">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="4f7cf-404">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-404">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="4f7cf-405">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-405">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="4f7cf-406">Der URI-Parameter kann eine Platzhalterzeichenfolge (' ': 0 oder mehr; '? ': genau eins) sein.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-406">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="4f7cf-407">nullptr entspricht L "".</span><span class="sxs-lookup"><span data-stu-id="4f7cf-407">nullptr is equivalent to L"".</span></span> <span data-ttu-id="4f7cf-408">Eine Beschreibung der Ressourcenkontext Filter finden Sie unter COREWEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-408">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="4f7cf-409">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="4f7cf-409">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="4f7cf-410">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-410">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="4f7cf-411">Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-411">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="4f7cf-412">Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-412">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="4f7cf-413">Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-413">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="4f7cf-414">Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-414">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="4f7cf-415">Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-415">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="4f7cf-416">Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-416">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="4f7cf-417">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="4f7cf-417">CapturePreview</span></span> 

<span data-ttu-id="4f7cf-418">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-418">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="4f7cf-419">Public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) Image Format, IStream \* ImageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \*-Handler)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-419">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="4f7cf-420">Geben Sie das Format des Bilds mit dem ImageFormat-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-420">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="4f7cf-421">Die resultierenden Bild Binärdaten werden in den bereitgestellten ImageStream-Parameter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-421">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="4f7cf-422">Wenn CapturePreview den Schreibvorgang in den Datenstrom abgeschlossen hat, wird die Invoke-Methode für den bereitgestellten Handler-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-422">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="4f7cf-423">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="4f7cf-423">ExecuteScript</span></span> 

<span data-ttu-id="4f7cf-424">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-424">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="4f7cf-425">Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-425">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="4f7cf-426">Dies wird asynchron ausgeführt, und wenn ein Handler im ExecuteScriptCompletedHandler-Parameter bereitgestellt wird, wird die Invoke-Methode mit dem Ergebnis der Auswertung des bereitgestellten JavaScript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-426">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="4f7cf-427">Der Ergebniswert ist eine JSON-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-427">The result value is a JSON encoded string.</span></span> <span data-ttu-id="4f7cf-428">Wenn das Ergebnis undefiniert ist, einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird der JSON-NULL-Wert als Zeichenfolge "Null" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-428">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="4f7cf-429">Beachten Sie, dass eine Funktion, die keinen expliziten Rückgabewert aufweist, undefined zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-429">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="4f7cf-430">Wenn das ausgeführte Skript eine nicht behandelte Ausnahme auslöst, ist das Ergebnis auch "Null".</span><span class="sxs-lookup"><span data-stu-id="4f7cf-430">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="4f7cf-431">Diese Methode wird asynchron angewendet.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-431">This method is applied asynchronously.</span></span> <span data-ttu-id="4f7cf-432">Wenn die Methode nach dem NavigationStarting-Ereignis während einer Navigation aufgerufen wird, wird das Skript beim Laden des Skripts im neuen Dokument ausgeführt, und zwar um den Zeitpunkt, zu dem ContentLoading ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-432">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="4f7cf-433">ExecuteScript funktioniert auch dann, wenn IsScriptEnabled auf "false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-433">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="4f7cf-434">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="4f7cf-434">get_BrowserProcessId</span></span> 

<span data-ttu-id="4f7cf-435">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-435">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="4f7cf-436">Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-436">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="4f7cf-437">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="4f7cf-437">get_CanGoBack</span></span> 

<span data-ttu-id="4f7cf-438">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-438">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="4f7cf-439">Public HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-439">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="4f7cf-440">Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoBack geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-440">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="4f7cf-441">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="4f7cf-441">get_CanGoForward</span></span> 

<span data-ttu-id="4f7cf-442">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-442">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="4f7cf-443">Public HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-443">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="4f7cf-444">Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoForward geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-444">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="4f7cf-445">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="4f7cf-445">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="4f7cf-446">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-446">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="4f7cf-447">Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-447">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="4f7cf-448">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="4f7cf-448">get_DocumentTitle</span></span> 

<span data-ttu-id="4f7cf-449">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-449">The title for the current top level document.</span></span>

> <span data-ttu-id="4f7cf-450">öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-450">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="4f7cf-451">Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-451">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="4f7cf-452">get_Settings</span><span class="sxs-lookup"><span data-stu-id="4f7cf-452">get_Settings</span></span> 

<span data-ttu-id="4f7cf-453">Das [ICoreWebView2Settings](icorewebview2settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-453">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="4f7cf-454">öffentliche HRESULT- [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \* \*-Einstellungen)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-454">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="4f7cf-455">get_Source</span><span class="sxs-lookup"><span data-stu-id="4f7cf-455">get_Source</span></span> 

<span data-ttu-id="4f7cf-456">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-456">The URI of the current top level document.</span></span>

> <span data-ttu-id="4f7cf-457">Public HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-457">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="4f7cf-458">Dieser Wert ändert sich möglicherweise als Teil der Ereignis Befeuerungs Quelle für einige Fälle, beispielsweise das Navigieren zu einer anderen Website oder zu einer anderen Fragment-Navigation.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-458">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="4f7cf-459">Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-459">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="4f7cf-460">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="4f7cf-460">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="4f7cf-461">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-461">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="4f7cf-462">Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-462">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="4f7cf-463">Der eventName-Parameter ist der vollständige Name des Ereignisses im Format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-463">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="4f7cf-464">Eine Liste der Beschreibungen von devtools-Protokollereignissen und Ereignis args finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-464">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="4f7cf-465">GoBack</span><span class="sxs-lookup"><span data-stu-id="4f7cf-465">GoBack</span></span> 

<span data-ttu-id="4f7cf-466">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-466">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="4f7cf-467">Public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="4f7cf-467">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="4f7cf-468">GoForward</span><span class="sxs-lookup"><span data-stu-id="4f7cf-468">GoForward</span></span> 

<span data-ttu-id="4f7cf-469">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-469">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="4f7cf-470">Public HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="4f7cf-470">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="4f7cf-471">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="4f7cf-471">Navigate</span></span> 

<span data-ttu-id="4f7cf-472">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-472">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="4f7cf-473">öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-473">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="4f7cf-474">Weitere Informationen finden Sie in den Navigations Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-474">See the navigation events for more information.</span></span> <span data-ttu-id="4f7cf-475">Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-475">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

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

#### <span data-ttu-id="4f7cf-476">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="4f7cf-476">NavigateToString</span></span> 

<span data-ttu-id="4f7cf-477">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-477">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="4f7cf-478">Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-478">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="4f7cf-479">Der htmlContent-Parameter darf nicht größer als 2 MB Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-479">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="4f7cf-480">Der Ursprung der neuen Seite lautet: leer.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-480">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="4f7cf-481">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="4f7cf-481">OpenDevToolsWindow</span></span> 

<span data-ttu-id="4f7cf-482">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-482">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="4f7cf-483">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="4f7cf-483">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="4f7cf-484">Wenn das devtools-Fenster bereits geöffnet ist, wird nichts aufgerufen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-484">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="4f7cf-485">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="4f7cf-485">PostWebMessageAsJson</span></span> 

<span data-ttu-id="4f7cf-486">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-486">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="4f7cf-487">Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-487">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="4f7cf-488">Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-488">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="4f7cf-489">JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen:</span><span class="sxs-lookup"><span data-stu-id="4f7cf-489">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="4f7cf-490">Das Ereignis args ist eine Instanz von `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="4f7cf-490">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="4f7cf-491">Die ICoreWebView2Settings:: IsWebMessageEnabled-Einstellung muss wahr sein, oder diese Methode schlägt mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-491">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="4f7cf-492">Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-492">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="4f7cf-493">Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-493">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="4f7cf-494">Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-494">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="4f7cf-495">Diese Nachricht wird asynchron gesendet.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-495">This message is sent asynchronously.</span></span> <span data-ttu-id="4f7cf-496">Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-496">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="4f7cf-497">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="4f7cf-497">PostWebMessageAsString</span></span> 

<span data-ttu-id="4f7cf-498">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-498">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="4f7cf-499">Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-499">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="4f7cf-500">Dies verhält sich auf die gleiche Weise wie PostWebMessageAsJson, aber die `window.chrome.webview` Dateneigenschaft des Nachrichtenereignisses arg ist eine Zeichenfolge mit dem gleichen Wert wie webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-500">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="4f7cf-501">Verwenden Sie diese anstelle von PostWebMessageAsJson, wenn Sie über einfache Zeichenfolgen anstelle von JSON-Objekten kommunizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-501">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="4f7cf-502">Laden</span><span class="sxs-lookup"><span data-stu-id="4f7cf-502">Reload</span></span> 

<span data-ttu-id="4f7cf-503">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-503">Reload the current page.</span></span>

> <span data-ttu-id="4f7cf-504">Public HRESULT [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="4f7cf-504">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="4f7cf-505">Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-505">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="4f7cf-506">Das zurück/weiter-Protokoll wird jedoch nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-506">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="4f7cf-507">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-507">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="4f7cf-508">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-508">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="4f7cf-509">Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-509">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-510">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="4f7cf-510">remove_ContentLoading</span></span> 

<span data-ttu-id="4f7cf-511">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-511">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="4f7cf-512">Public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-512">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-513">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-513">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="4f7cf-514">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-514">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="4f7cf-515">Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-515">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-516">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-516">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="4f7cf-517">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-517">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="4f7cf-518">Public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-518">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-519">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-519">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="4f7cf-520">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-520">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="4f7cf-521">Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-521">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-522">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-522">remove_HistoryChanged</span></span> 

<span data-ttu-id="4f7cf-523">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-523">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="4f7cf-524">Public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-524">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-525">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="4f7cf-525">remove_NavigationCompleted</span></span> 

<span data-ttu-id="4f7cf-526">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-526">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="4f7cf-527">Public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-527">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-528">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="4f7cf-528">remove_NavigationStarting</span></span> 

<span data-ttu-id="4f7cf-529">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-529">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="4f7cf-530">Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-530">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-531">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-531">remove_NewWindowRequested</span></span> 

<span data-ttu-id="4f7cf-532">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-532">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="4f7cf-533">Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-533">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-534">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-534">remove_PermissionRequested</span></span> 

<span data-ttu-id="4f7cf-535">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-535">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="4f7cf-536">Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-536">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-537">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="4f7cf-537">remove_ProcessFailed</span></span> 

<span data-ttu-id="4f7cf-538">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-538">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="4f7cf-539">Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-539">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-540">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="4f7cf-540">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="4f7cf-541">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-541">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="4f7cf-542">Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-542">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-543">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="4f7cf-543">remove_SourceChanged</span></span> 

<span data-ttu-id="4f7cf-544">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-544">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="4f7cf-545">Public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-545">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-546">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="4f7cf-546">remove_WebMessageReceived</span></span> 

<span data-ttu-id="4f7cf-547">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-547">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="4f7cf-548">Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-548">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-549">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-549">remove_WebResourceRequested</span></span> 

<span data-ttu-id="4f7cf-550">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-550">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="4f7cf-551">Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-551">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-552">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="4f7cf-552">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="4f7cf-553">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-553">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="4f7cf-554">Public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-554">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="4f7cf-555">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="4f7cf-555">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="4f7cf-556">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-556">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="4f7cf-557">Public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-557">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="4f7cf-558">Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-558">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="4f7cf-559">Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-559">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="4f7cf-560">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="4f7cf-560">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="4f7cf-561">Entfernen Sie das entsprechende JavaScript `AddScriptToExecuteOnDocumentCreated` , das mit der angegebenen Skript-ID hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-561">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>

> <span data-ttu-id="4f7cf-562">Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-562">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="4f7cf-563">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="4f7cf-563">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="4f7cf-564">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-564">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="4f7cf-565">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-565">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="4f7cf-566">Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-566">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="4f7cf-567">Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-567">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="4f7cf-568">Stop</span><span class="sxs-lookup"><span data-stu-id="4f7cf-568">Stop</span></span> 

<span data-ttu-id="4f7cf-569">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-569">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="4f7cf-570">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="4f7cf-570">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="4f7cf-571">Skripts werden nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-571">Does not stop scripts.</span></span>

#### <span data-ttu-id="4f7cf-572">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-572">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="4f7cf-573">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-573">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="4f7cf-574">Enum- [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-574">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="4f7cf-575">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-575">Values</span></span>                         | <span data-ttu-id="4f7cf-576">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-576">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-577">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="4f7cf-577">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="4f7cf-578">PNG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-578">PNG image format.</span></span>
<span data-ttu-id="4f7cf-579">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="4f7cf-579">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="4f7cf-580">JPEG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-580">JPEG image format.</span></span>

#### <span data-ttu-id="4f7cf-581">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-581">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="4f7cf-582">Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-582">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="4f7cf-583">Enum- [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-583">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="4f7cf-584">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-584">Values</span></span>                         | <span data-ttu-id="4f7cf-585">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-585">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-586">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="4f7cf-586">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="4f7cf-587">Dem Fenster Nachrichten WM_KEYDOWN entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-587">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="4f7cf-588">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="4f7cf-588">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="4f7cf-589">Dem Fenster Nachrichten WM_KEYUP entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-589">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="4f7cf-590">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="4f7cf-590">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="4f7cf-591">Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-591">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="4f7cf-592">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="4f7cf-592">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="4f7cf-593">Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-593">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="4f7cf-594">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="4f7cf-594">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="4f7cf-595">Grund für das Verschieben des Fokus</span><span class="sxs-lookup"><span data-stu-id="4f7cf-595">Reason for moving focus.</span></span>

> <span data-ttu-id="4f7cf-596">Enum- [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-596">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="4f7cf-597">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-597">Values</span></span>                         | <span data-ttu-id="4f7cf-598">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-598">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-599">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="4f7cf-599">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="4f7cf-600">Der Fokus für die Code Einstellung in WebView.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-600">Code setting focus into WebView.</span></span>
<span data-ttu-id="4f7cf-601">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-601">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="4f7cf-602">Verschieben des Fokus aufgrund von Tabstopps vorwärts</span><span class="sxs-lookup"><span data-stu-id="4f7cf-602">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="4f7cf-603">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-603">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="4f7cf-604">Verschieben des Fokus aufgrund von Tabstopps rückwärts</span><span class="sxs-lookup"><span data-stu-id="4f7cf-604">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="4f7cf-605">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-605">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="4f7cf-606">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-606">The type of a permission request.</span></span>

> <span data-ttu-id="4f7cf-607">Enum- [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-607">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="4f7cf-608">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-608">Values</span></span>                         | <span data-ttu-id="4f7cf-609">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-609">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-610">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="4f7cf-610">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="4f7cf-611">Unbekannte Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-611">Unknown permission.</span></span>
<span data-ttu-id="4f7cf-612">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-612">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="4f7cf-613">Berechtigung zum Aufzeichnen von Audio.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-613">Permission to capture audio.</span></span>
<span data-ttu-id="4f7cf-614">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="4f7cf-614">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="4f7cf-615">Berechtigung zum Aufzeichnen von Videos.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-615">Permission to capture video.</span></span>
<span data-ttu-id="4f7cf-616">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="4f7cf-616">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="4f7cf-617">Berechtigung für den Zugriff auf Geolocation.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-617">Permission to access geolocation.</span></span>
<span data-ttu-id="4f7cf-618">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-618">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="4f7cf-619">Berechtigung zum Senden von webbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-619">Permission to send web notifications.</span></span>
<span data-ttu-id="4f7cf-620">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-620">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="4f7cf-621">Berechtigung für den Zugriff auf den generischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-621">Permission to access generic sensor.</span></span>
<span data-ttu-id="4f7cf-622">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="4f7cf-622">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="4f7cf-623">Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste</span><span class="sxs-lookup"><span data-stu-id="4f7cf-623">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="4f7cf-624">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-624">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="4f7cf-625">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-625">Response to a permission request.</span></span>

> <span data-ttu-id="4f7cf-626">Enum- [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-626">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="4f7cf-627">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-627">Values</span></span>                         | <span data-ttu-id="4f7cf-628">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-628">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-629">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-629">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="4f7cf-630">Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-630">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="4f7cf-631">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="4f7cf-631">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="4f7cf-632">Erteilen Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-632">Grant the permission request.</span></span>
<span data-ttu-id="4f7cf-633">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="4f7cf-633">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="4f7cf-634">Verweigern Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-634">Deny the permission request.</span></span>

#### <span data-ttu-id="4f7cf-635">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-635">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="4f7cf-636">Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-636">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="4f7cf-637">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-637">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="4f7cf-638">Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN.[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-638">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="4f7cf-639">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-639">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="4f7cf-640">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-640">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="4f7cf-641">Enum- [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-641">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="4f7cf-642">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-642">Values</span></span>                         | <span data-ttu-id="4f7cf-643">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-643">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-644">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-644">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="4f7cf-645">Gibt an, dass der Browserprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-645">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="4f7cf-646">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-646">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="4f7cf-647">Gibt an, dass der Renderprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-647">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="4f7cf-648">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-648">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="4f7cf-649">Gibt an, dass der Renderprozess nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-649">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="4f7cf-650">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="4f7cf-650">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="4f7cf-651">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-651">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="4f7cf-652">Enum- [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-652">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="4f7cf-653">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-653">Values</span></span>                         | <span data-ttu-id="4f7cf-654">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-654">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-655">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-655">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="4f7cf-656">Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-656">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="4f7cf-657">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="4f7cf-657">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="4f7cf-658">Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-658">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="4f7cf-659">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-659">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="4f7cf-660">Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-660">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="4f7cf-661">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="4f7cf-661">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="4f7cf-662">Ein Dialogfeld, das über das beforeunload-JavaScript-Ereignis aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-662">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="4f7cf-663">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-663">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="4f7cf-664">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-664">Error status values for web navigations.</span></span>

> <span data-ttu-id="4f7cf-665">Enum- [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-665">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="4f7cf-666">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-666">Values</span></span>                         | <span data-ttu-id="4f7cf-667">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-668">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="4f7cf-668">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="4f7cf-669">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-669">An unknown error occurred.</span></span>
<span data-ttu-id="4f7cf-670">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-670">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="4f7cf-671">Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-671">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="4f7cf-672">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-672">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="4f7cf-673">Das SSL-Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-673">The SSL certificate has expired.</span></span>
<span data-ttu-id="4f7cf-674">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4f7cf-674">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="4f7cf-675">Das SSL-Clientzertifikat enthält Fehler.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-675">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="4f7cf-676">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-676">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="4f7cf-677">Das SSL-Zertifikat wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-677">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="4f7cf-678">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="4f7cf-678">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="4f7cf-679">Das SSL-Zertifikat ist ungültig &ndash; Dies könnte bedeuten, dass das Zertifikat nicht mit den öffentlichen Schlüssel Pins für den Hostnamen übereinstimmte. das Zertifikat wird von einer nicht vertrauenswürdigen Zertifizierungsstelle signiert oder mit einem schwachen Vorzeichen Algorithmus, das Zertifikat behauptet, dass DNS-Namen gegen Namenseinschränkungen verstoßen, das Zertifikat einen schwachen Schlüssel enthält, der Gültigkeitszeitraum des Zertifikats zu lang ist, fehlender Sperrungsinformationen oder Sperrungs Mechanismus, nicht eindeutiger [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)Hostname, fehlender Zertifikat Transparenzinformationen oder das Zertifikat an</span><span class="sxs-lookup"><span data-stu-id="4f7cf-679">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="4f7cf-680">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-680">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="4f7cf-681">Der Host ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-681">The host is unreachable.</span></span>
<span data-ttu-id="4f7cf-682">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-682">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="4f7cf-683">Die Verbindung hat ein Zeitlimit überschritten.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-683">The connection has timed out.</span></span>
<span data-ttu-id="4f7cf-684">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-684">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="4f7cf-685">Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-685">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="4f7cf-686">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-686">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="4f7cf-687">Die Verbindung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-687">The connection was aborted.</span></span>
<span data-ttu-id="4f7cf-688">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="4f7cf-688">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="4f7cf-689">Die Verbindung wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-689">The connection was reset.</span></span>
<span data-ttu-id="4f7cf-690">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-690">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="4f7cf-691">Die Internet Verbindung wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-691">The Internet connection has been lost.</span></span>
<span data-ttu-id="4f7cf-692">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-692">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="4f7cf-693">Verbindung mit Ziel kann nicht hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-693">Cannot connect to destination.</span></span>
<span data-ttu-id="4f7cf-694">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-694">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="4f7cf-695">Der angegebene Hostname konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-695">Could not resolve provided host name.</span></span>
<span data-ttu-id="4f7cf-696">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-696">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="4f7cf-697">Der Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-697">The operation was canceled.</span></span>
<span data-ttu-id="4f7cf-698">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="4f7cf-698">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="4f7cf-699">Die Anforderungs Umleitung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-699">The request redirect failed.</span></span>
<span data-ttu-id="4f7cf-700">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="4f7cf-700">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="4f7cf-701">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-701">An unexpected error occurred.</span></span>

#### <span data-ttu-id="4f7cf-702">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-702">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="4f7cf-703">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-703">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="4f7cf-704">Enum- [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="4f7cf-704">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="4f7cf-705">Werte</span><span class="sxs-lookup"><span data-stu-id="4f7cf-705">Values</span></span>                         | <span data-ttu-id="4f7cf-706">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-706">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="4f7cf-707">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="4f7cf-707">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="4f7cf-708">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-708">All resources.</span></span>
<span data-ttu-id="4f7cf-709">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-709">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="4f7cf-710">Dokument Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-710">Document resources.</span></span>
<span data-ttu-id="4f7cf-711">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="4f7cf-711">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="4f7cf-712">CSS-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-712">CSS resources.</span></span>
<span data-ttu-id="4f7cf-713">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-713">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="4f7cf-714">Bildressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-714">Image resources.</span></span>
<span data-ttu-id="4f7cf-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="4f7cf-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="4f7cf-716">Andere Medienressourcen wie Videos.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-716">Other media resources such as videos.</span></span>
<span data-ttu-id="4f7cf-717">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-717">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="4f7cf-718">Schriftartressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-718">Font resources.</span></span>
<span data-ttu-id="4f7cf-719">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-719">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="4f7cf-720">Skriptressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-720">Script resources.</span></span>
<span data-ttu-id="4f7cf-721">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="4f7cf-721">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="4f7cf-722">XML-HTTP-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-722">XML HTTP requests.</span></span>
<span data-ttu-id="4f7cf-723">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="4f7cf-723">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="4f7cf-724">Abrufen der API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-724">Fetch API communication.</span></span>
<span data-ttu-id="4f7cf-725">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="4f7cf-725">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="4f7cf-726">Texttracking-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-726">TextTrack resources.</span></span>
<span data-ttu-id="4f7cf-727">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-727">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="4f7cf-728">EventSource-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-728">EventSource API communication.</span></span>
<span data-ttu-id="4f7cf-729">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="4f7cf-729">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="4f7cf-730">WebSocket-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-730">WebSocket API communication.</span></span>
<span data-ttu-id="4f7cf-731">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="4f7cf-731">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="4f7cf-732">Web App-Manifeste</span><span class="sxs-lookup"><span data-stu-id="4f7cf-732">Web App Manifests.</span></span>
<span data-ttu-id="4f7cf-733">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="4f7cf-733">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="4f7cf-734">Signierte http-Exchanges.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-734">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="4f7cf-735">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="4f7cf-735">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="4f7cf-736">Ping-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-736">Ping requests.</span></span>
<span data-ttu-id="4f7cf-737">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="4f7cf-737">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="4f7cf-738">Berichte zu CSP-Verstößen</span><span class="sxs-lookup"><span data-stu-id="4f7cf-738">CSP Violation Reports.</span></span>
<span data-ttu-id="4f7cf-739">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="4f7cf-739">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="4f7cf-740">Andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4f7cf-740">Other resources.</span></span>

