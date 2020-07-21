---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 5711a1dbf501df55fefc9709763c1fe225865e11
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886430"
---
# <span data-ttu-id="67433-104">0.8.355-Interface-IWebView2WebView</span><span class="sxs-lookup"><span data-stu-id="67433-104">0.8.355 - interface IWebView2WebView</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView
  : public IUnknown
```

<span data-ttu-id="67433-105">WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.</span><span class="sxs-lookup"><span data-stu-id="67433-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="67433-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="67433-106">Summary</span></span>

 <span data-ttu-id="67433-107">Member</span><span class="sxs-lookup"><span data-stu-id="67433-107">Members</span></span>                        | <span data-ttu-id="67433-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67433-109">get_Settings</span><span class="sxs-lookup"><span data-stu-id="67433-109">get_Settings</span></span>](#get_settings) | <span data-ttu-id="67433-110">Das [IWebView2Settings](IWebView2Settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-110">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="67433-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="67433-111">get_Source</span></span>](#get_source) | <span data-ttu-id="67433-112">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="67433-112">The URI of the current top level document.</span></span>
[<span data-ttu-id="67433-113">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="67433-113">Navigate</span></span>](#navigate) | <span data-ttu-id="67433-114">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="67433-114">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="67433-115">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="67433-115">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="67433-116">Verschieben des Fokus in WebView</span><span class="sxs-lookup"><span data-stu-id="67433-116">Move focus into WebView.</span></span>
[<span data-ttu-id="67433-117">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="67433-117">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="67433-118">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="67433-118">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="67433-119">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-119">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="67433-120">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-120">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="67433-121">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-121">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="67433-122">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-122">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="67433-123">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="67433-123">add_DocumentStateChanged</span></span>](#add_documentstatechanged) | <span data-ttu-id="67433-124">Fügen Sie einen Ereignishandler für das DocumentStateChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-124">Add an event handler for the DocumentStateChanged event.</span></span>
[<span data-ttu-id="67433-125">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="67433-125">remove_DocumentStateChanged</span></span>](#remove_documentstatechanged) | <span data-ttu-id="67433-126">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentStateChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-126">Remove an event handler previously added with add_DocumentStateChanged.</span></span>
[<span data-ttu-id="67433-127">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="67433-127">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="67433-128">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-128">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="67433-129">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="67433-129">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="67433-130">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-130">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="67433-131">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-131">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="67433-132">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-132">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="67433-133">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-133">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="67433-134">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-134">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="67433-135">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="67433-135">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="67433-136">Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-136">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="67433-137">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="67433-137">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="67433-138">Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-138">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="67433-139">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="67433-139">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="67433-140">Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-140">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="67433-141">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="67433-141">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="67433-142">Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-142">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="67433-143">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="67433-143">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="67433-144">Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-144">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="67433-145">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="67433-145">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="67433-146">Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-146">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="67433-147">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="67433-147">add_WebResourceRequested_deprecated</span></span>](#add_webresourcerequested_deprecated) | <span data-ttu-id="67433-148">Diese API wird als veraltet markiert, bitte verwenden Sie die neue add_WebResourceRequested-API.</span><span class="sxs-lookup"><span data-stu-id="67433-148">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>
[<span data-ttu-id="67433-149">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="67433-149">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="67433-150">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-150">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="67433-151">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="67433-151">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="67433-152">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-152">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="67433-153">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="67433-153">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="67433-154">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-154">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="67433-155">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="67433-155">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="67433-156">Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-156">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="67433-157">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="67433-157">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="67433-158">Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-158">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="67433-159">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="67433-159">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="67433-160">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-160">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="67433-161">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="67433-161">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="67433-162">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-162">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="67433-163">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="67433-163">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="67433-164">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-164">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="67433-165">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="67433-165">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="67433-166">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-166">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="67433-167">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="67433-167">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="67433-168">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="67433-168">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="67433-169">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="67433-169">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="67433-170">Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-170">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="67433-171">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="67433-171">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="67433-172">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="67433-172">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="67433-173">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="67433-173">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="67433-174">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-174">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="67433-175">Laden</span><span class="sxs-lookup"><span data-stu-id="67433-175">Reload</span></span>](#reload) | <span data-ttu-id="67433-176">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="67433-176">Reload the current page.</span></span>
[<span data-ttu-id="67433-177">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="67433-177">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="67433-178">Die WebView-Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="67433-178">The webview bounds.</span></span>
[<span data-ttu-id="67433-179">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="67433-179">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="67433-180">Die Bounds-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="67433-180">Set the Bounds property.</span></span>
[<span data-ttu-id="67433-181">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="67433-181">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="67433-182">Der Zoomfaktor für die aktuelle Seite im WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-182">The zoom factor for the current page in the WebView.</span></span>
[<span data-ttu-id="67433-183">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="67433-183">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="67433-184">Festlegen der ZoomFactor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="67433-184">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="67433-185">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="67433-185">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="67433-186">Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="67433-186">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="67433-187">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="67433-187">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="67433-188">Festlegen der IsVisible-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="67433-188">Set the IsVisible property.</span></span>
[<span data-ttu-id="67433-189">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="67433-189">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="67433-190">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in diesem [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="67433-190">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>
[<span data-ttu-id="67433-191">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="67433-191">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="67433-192">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="67433-192">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="67433-193">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="67433-193">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="67433-194">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="67433-194">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="67433-195">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="67433-195">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="67433-196">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-196">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="67433-197">Schließen</span><span class="sxs-lookup"><span data-stu-id="67433-197">Close</span></span>](#close) | <span data-ttu-id="67433-198">Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.</span><span class="sxs-lookup"><span data-stu-id="67433-198">Closes the webview and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="67433-199">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="67433-199">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="67433-200">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="67433-200">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="67433-201">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="67433-201">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="67433-202">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="67433-202">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="67433-203">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="67433-203">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="67433-204">Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-204">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>
[<span data-ttu-id="67433-205">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="67433-205">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="67433-206">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="67433-206">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="67433-207">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="67433-207">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="67433-208">Kann im WebView zur vorherigen Seite im Navigationsverlauf navigieren.</span><span class="sxs-lookup"><span data-stu-id="67433-208">Can navigate the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="67433-209">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="67433-209">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="67433-210">Kann im WebView zur nächsten Seite im Navigationsverlauf navigieren.</span><span class="sxs-lookup"><span data-stu-id="67433-210">Can navigate the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="67433-211">GoBack</span><span class="sxs-lookup"><span data-stu-id="67433-211">GoBack</span></span>](#goback) | <span data-ttu-id="67433-212">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="67433-212">Navigates the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="67433-213">GoForward</span><span class="sxs-lookup"><span data-stu-id="67433-213">GoForward</span></span>](#goforward) | <span data-ttu-id="67433-214">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="67433-214">Navigates the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="67433-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="67433-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#webview2_capture_preview_image_format) | <span data-ttu-id="67433-216">Bildformat, das von der [IWebView2WebView:: CapturePreview](#capturepreview) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="67433-216">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>
[<span data-ttu-id="67433-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="67433-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#webview2_script_dialog_kind) | <span data-ttu-id="67433-218">Art des in der [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) -Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="67433-218">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>
[<span data-ttu-id="67433-219">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="67433-219">WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#webview2_process_failed_kind) | <span data-ttu-id="67433-220">Art des in der [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) -Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="67433-220">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>
[<span data-ttu-id="67433-221">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="67433-221">WEBVIEW2_PERMISSION_TYPE</span></span>](#webview2_permission_type) | <span data-ttu-id="67433-222">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="67433-222">The type of a permission request.</span></span>
[<span data-ttu-id="67433-223">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="67433-223">WEBVIEW2_PERMISSION_STATE</span></span>](#webview2_permission_state) | <span data-ttu-id="67433-224">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="67433-224">Response to a permission request.</span></span>
[<span data-ttu-id="67433-225">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="67433-225">WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#webview2_move_focus_reason) | <span data-ttu-id="67433-226">Grund für das Verschieben des Fokus</span><span class="sxs-lookup"><span data-stu-id="67433-226">Reason for moving focus.</span></span>
[<span data-ttu-id="67433-227">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="67433-227">WEBVIEW2_WEB_ERROR_STATUS</span></span>](#webview2_web_error_status) | <span data-ttu-id="67433-228">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="67433-228">Error status values for web navigations.</span></span>
[<span data-ttu-id="67433-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="67433-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#webview2_web_resource_context) | <span data-ttu-id="67433-230">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="67433-230">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="67433-231">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="67433-231">Navigation events</span></span>

<span data-ttu-id="67433-232">Die normale Abfolge von Navigations Ereignissen lautet NavigationStarting, DocumentStateChanged und dann NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="67433-232">The normal sequence of navigation events is NavigationStarting, DocumentStateChanged and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="67433-234">Beachten Sie, dass dies für Navigationsereignisse mit dem gleichen Navigations-Event-arg gilt.</span><span class="sxs-lookup"><span data-stu-id="67433-234">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="67433-235">Navigationsereignisse mit unterschiedlichen Navigations-Event-args können sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="67433-235">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="67433-236">Wenn Sie beispielsweise eine Navigation auf das NavigationStarting-Ereignis warten und dann eine andere Navigation starten, sehen Sie die NavigationStarting für die erste Navigation, gefolgt von der NavigationStarting der zweiten Navigation, gefolgt von der NavigationCompleted für die erste Navigation und dann allen anderen geeigneten Navigations Ereignissen für die zweite Navigation.</span><span class="sxs-lookup"><span data-stu-id="67433-236">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="67433-237">In Fehlerfällen kann es sich um ein DocumentStateChanged-Ereignis handeln, das davon abhängt, ob die Navigation auf einer Fehlerseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="67433-237">In error cases there may or may not be a DocumentStateChanged event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="67433-238">Im Fall einer HTTP-Umleitung gibt es mehrere NavigationStarting-Ereignisse in einer Zeile, wobei für diejenigen, die dem ersten Folgen, das isredirect-Flag festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="67433-238">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="67433-239">Bei untergeordneten Frames in WebView ist das einzige ausgelöste Navigations Ereignis das NavigationStarting-Ereignis, das Host die Möglichkeit gibt, unter Frame-Navigationselemente zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="67433-239">For subframes inside WebView, the only navigation event fired is the NavigationStarting event which gives host the ability to block subframe navigations.</span></span>

## <span data-ttu-id="67433-240">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="67433-240">Process model</span></span>

<span data-ttu-id="67433-241">WebView2 verwendet das gleiche Prozessmodell wie der Edge-Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="67433-241">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="67433-242">Es gibt einen Edge-Browserprozess pro angegebenen Benutzerdatenverzeichnis in einer Benutzersitzung, die jedem WebView2-Aufrufprozess dient, der das Benutzerdatenverzeichnis angibt.</span><span class="sxs-lookup"><span data-stu-id="67433-242">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="67433-243">Dies bedeutet, dass ein Edge-Browser-Prozess möglicherweise mehrere Anruf Prozesse bedient, und ein Aufrufprozess möglicherweise mehrere Edge-Browser-Prozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="67433-243">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="67433-245">In einem Browserprozess gibt es eine Reihe von Renderer-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="67433-245">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="67433-246">Diese werden nach Bedarf erstellt, um potenziell mehrere Frames in verschiedenen Webansichten zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="67433-246">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="67433-247">Die Anzahl der Renderer-Prozesse variiert basierend auf dem Feature "Website Isolierungs Browser" und der Anzahl der unterschiedlichen getrennten Ursprünge, die in verknüpften Webansichten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="67433-247">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="67433-249">Mithilfe des ProcessFailure-Ereignisses können Sie auf Abstürze reagieren und in diesen Browser-und Renderer-Prozessen hängen bleiben.</span><span class="sxs-lookup"><span data-stu-id="67433-249">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="67433-250">Sie können zugeordnete Browser-und Renderer-Prozesse mit der Close-Methode sicher Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="67433-250">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="67433-251">Threadingmodell</span><span class="sxs-lookup"><span data-stu-id="67433-251">Threading model</span></span>

<span data-ttu-id="67433-252">Der WebView2 muss in einem UI-Thread erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="67433-252">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="67433-253">Insbesondere ein Thread mit einer Nachrichten Pumpe.</span><span class="sxs-lookup"><span data-stu-id="67433-253">Specifically a thread with a message pump.</span></span> <span data-ttu-id="67433-254">Alle Rückrufe werden in diesem Thread ausgeführt, und Aufrufe an die WebView müssen in diesem Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67433-254">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="67433-255">Es ist nicht sicher, die WebView aus einem anderen Thread zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="67433-255">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="67433-256">Rückrufe, einschließlich Ereignishandlern und Vervollständigungs Handlern, werden seriell ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67433-256">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="67433-257">Das heißt, wenn Sie einen Ereignishandler ausführen und eine Nachrichtenschleife beginnen, werden keine anderen Ereignishandler oder Abschluss Rückrufe erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67433-257">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="67433-258">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="67433-258">Security</span></span>

<span data-ttu-id="67433-259">Überprüfen Sie immer die Source-Eigenschaft von WebView, bevor Sie executeScript, PostWebMessageAsJson, PostWebMessageAsString oder eine andere Methode verwenden, um Informationen an die WebView zu senden.</span><span class="sxs-lookup"><span data-stu-id="67433-259">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="67433-260">Die WebView kann über den Endbenutzer, der mit der Seite oder dem Skript auf der Seite interagiert, die Navigation verursacht hat, zu einer anderen Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="67433-260">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="67433-261">Achten Sie auf ähnliche Weise auf AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="67433-261">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="67433-262">Alle zukünftigen Navigationselemente führen dieses Skript aus, und wenn es Zugriff auf Informationen bietet, die nur für einen bestimmten Ursprung vorgesehen sind, kann jedes HTML-Dokumentzugriff haben.</span><span class="sxs-lookup"><span data-stu-id="67433-262">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="67433-263">Bei der Untersuchung des Ergebnisses eines executeScript-Methodenaufrufs, eines WebMessageReceived-Ereignisses, immer überprüfen der Quelle des Absenders oder eines anderen Mechanismus zum Empfangen von Informationen aus einem HTML-Dokument in einer WebView überprüfen Sie, ob der URI des HTML-Dokuments Ihren Erwartungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="67433-263">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="67433-264">Wenn Sie eine Nachricht erstellen, die Sie in eine WebView senden möchten, verwenden Sie PostWebMessageAsJson, und erstellen Sie den JSON-Zeichenfolgenparameter mithilfe einer JSON-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="67433-264">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="67433-265">Dadurch werden potenzielle Unfälle von Codierungsinformationen in eine JSON-Zeichenfolge oder ein Skript vermieden, und sichergestellt, dass keine von Angreifern gesteuerte Eingabe den restlichen Teil der JSON-Nachricht ändern oder ein beliebiges Skript ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="67433-265">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="67433-266">Zeichenfolgentypen</span><span class="sxs-lookup"><span data-stu-id="67433-266">String types</span></span>

<span data-ttu-id="67433-267">Zeichenfolgenparameter sind LPWSTR NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="67433-267">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="67433-268">Der aufgerufene ordnet die Zeichenfolge mithilfe von CoTaskMemAlloc zu.</span><span class="sxs-lookup"><span data-stu-id="67433-268">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="67433-269">Der Besitz wird an den Anrufer übertragen, und es ist dem Anrufer überlassen, den Speicher mit CoTaskMemFree zu befreien.</span><span class="sxs-lookup"><span data-stu-id="67433-269">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="67433-270">Zeichenfolge in Parametern sind LPCWSTR NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="67433-270">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="67433-271">Der Aufrufer stellt sicher, dass die Zeichenfolge für die Dauer des synchronen Funktionsaufrufs gültig ist.</span><span class="sxs-lookup"><span data-stu-id="67433-271">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="67433-272">Wenn der aufgerufene diesen Wert nach Abschluss des Funktionsaufrufs bis zu einem gewissen Punkt beibehalten muss, muss der aufgerufene eine eigene Kopie des Zeichenfolgenwerts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="67433-272">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="67433-273">URI-und JSON-Analyse</span><span class="sxs-lookup"><span data-stu-id="67433-273">URI and JSON parsing</span></span>

<span data-ttu-id="67433-274">Verschiedene Methoden stellen URIs und JSON als Zeichenfolgen bereit oder akzeptieren Sie.</span><span class="sxs-lookup"><span data-stu-id="67433-274">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="67433-275">Verwenden Sie für die Analyse und Generierung dieser Zeichenfolgen ihre eigene bevorzugte Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="67433-275">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="67433-276">Wenn WinRT für Ihre app verfügbar ist, können Sie `RuntimeClass_Windows_Data_Json_JsonObject` JSON-Zeichenfolgen verwenden und erstellen oder URIs analysieren und `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` erstellen.</span><span class="sxs-lookup"><span data-stu-id="67433-276">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="67433-277">Beide arbeiten in Win32-apps.</span><span class="sxs-lookup"><span data-stu-id="67433-277">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="67433-278">Wenn Sie IUri und CreateUri zum Analysieren von URIs verwenden, sollten Sie möglicherweise die folgenden URI-Erstellungs Flags verwenden, damit CreateUri-Verhalten der URI-Analyse in der WebView genauer entspricht:</span><span class="sxs-lookup"><span data-stu-id="67433-278">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="67433-279">Debuggen</span><span class="sxs-lookup"><span data-stu-id="67433-279">Debugging</span></span>

<span data-ttu-id="67433-280">Öffnen Sie devtools mit den normalen Tastenkombinationen: `F12` oder `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="67433-280">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="67433-281">Sie können die `--auto-open-devtools-for-tabs` Befehlsargument Schalter verwenden, um das devtools-Fenster sofort zu öffnen, wenn Sie das erste Mal eine WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="67433-281">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="67433-282">Informationen zum Bereitstellen zusätzlicher Befehlszeilenargumente für den Browserprozess finden Sie unter Dokumentation zu WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-282">See CreateWebView documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="67433-283">Schauen Sie sich den LoaderOverride-Registrierungsschlüssel an, um verschiedene Builds von WebView2 zu testen, ohne die Anwendung in der WebView-Dokumentation zu ändern.</span><span class="sxs-lookup"><span data-stu-id="67433-283">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateWebView documentation.</span></span>

## <span data-ttu-id="67433-284">Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="67433-284">Versioning</span></span>

<span data-ttu-id="67433-285">Nachdem Sie eine bestimmte Version des SDK zum Erstellen Ihrer APP verwendet haben, wird Ihre APP möglicherweise mit einer älteren oder neueren Version der installierten Browser-Binärdateien ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67433-285">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="67433-286">Bis Version 1.0.0.0 von WebView2 können sich während der Updates Änderungen ändern, die verhindern, dass Ihr SDK mit unterschiedlichen Versionen der installierten Browser-Binärdateien funktioniert.</span><span class="sxs-lookup"><span data-stu-id="67433-286">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="67433-287">Nach der Version 1.0.0.0 können verschiedene Versionen des SDKs mit unterschiedlichen Versionen des installierten Browsers funktionieren, indem Sie die folgenden bewährten Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="67433-287">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="67433-288">Wenn Sie Änderungen an der API berücksichtigen möchten, müssen Sie sicherstellen, dass Sie beim Aufrufen der DLL-Export CreateWebView2Environment und beim Aufrufen von QueryInterface für ein beliebiges WebView2-Objekt auf Fehler überprüfen.</span><span class="sxs-lookup"><span data-stu-id="67433-288">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateWebView2Environment and when calling QueryInterface on any WebView2 object.</span></span> <span data-ttu-id="67433-289">Ein Rückgabewert von E_NOINTERFACE kann darauf hindeuten, dass das SDK nicht mit den Binärdateien des Edge-Browsers kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="67433-289">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="67433-290">Das Überprüfen auf Fehler von QueryInterface berücksichtigt auch Fälle, in denen das SDK neuer als die Version des Edge-Browsers ist und Ihre APP versucht, eine Schnittstelle zu verwenden, von der der Edge-Browser nichts weiß.</span><span class="sxs-lookup"><span data-stu-id="67433-290">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="67433-291">Wenn eine Schnittstelle nicht zur Verfügung steht, können Sie das zugeordnete Feature nach Möglichkeit deaktivieren oder den Endbenutzer anderweitig darüber informieren, dass Sie den Browser aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="67433-291">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="67433-292">Member</span><span class="sxs-lookup"><span data-stu-id="67433-292">Members</span></span>

#### <span data-ttu-id="67433-293">get_Settings</span><span class="sxs-lookup"><span data-stu-id="67433-293">get_Settings</span></span> 

<span data-ttu-id="67433-294">Das [IWebView2Settings](IWebView2Settings.md) -Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-294">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="67433-295">öffentliche HRESULT- [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \* \*-Einstellungen)</span><span class="sxs-lookup"><span data-stu-id="67433-295">public HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="67433-296">get_Source</span><span class="sxs-lookup"><span data-stu-id="67433-296">get_Source</span></span> 

<span data-ttu-id="67433-297">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="67433-297">The URI of the current top level document.</span></span>

> <span data-ttu-id="67433-298">Public HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="67433-298">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="67433-299">Dieser Wert ändert sich möglicherweise als Teil des DocumentStateChanged-Ereignis Auslösens für einige Fälle wie das Navigieren zu einem anderen Website-oder Fragment-Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="67433-299">This value potentially changes as a part of the DocumentStateChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="67433-300">Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="67433-300">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="67433-301">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="67433-301">Navigate</span></span> 

<span data-ttu-id="67433-302">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="67433-302">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="67433-303">öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="67433-303">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="67433-304">Weitere Informationen finden Sie in den Navigations Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="67433-304">See the navigation events for more information.</span></span> <span data-ttu-id="67433-305">Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="67433-305">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### <span data-ttu-id="67433-306">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="67433-306">MoveFocus</span></span> 

<span data-ttu-id="67433-307">Verschieben des Fokus in WebView</span><span class="sxs-lookup"><span data-stu-id="67433-307">Move focus into WebView.</span></span>

> <span data-ttu-id="67433-308">öffentliche HRESULT- [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) Grund)</span><span class="sxs-lookup"><span data-stu-id="67433-308">public HRESULT [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="67433-309">WebView erhält den Fokus, und der Fokus wird auf das korrespondierende Element auf der Seite gesetzt, die in der WebView gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="67433-309">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="67433-310">Aus Programm Gründen wird der Fokus auf das zuvor fokussierte Element oder auf das Standardelement gesetzt, wenn kein zuvor fokussiertes Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="67433-310">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="67433-311">Aus dem nächsten Grund wird der Fokus auf das erste Element gesetzt.</span><span class="sxs-lookup"><span data-stu-id="67433-311">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="67433-312">Aus vorherigen Gründen wird der Fokus auf das letzte Element gesetzt.</span><span class="sxs-lookup"><span data-stu-id="67433-312">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="67433-313">WebView kann auch den Fokus über die Benutzerinteraktion erhalten, wie das Klicken in WebView oder die Tab-Taste.</span><span class="sxs-lookup"><span data-stu-id="67433-313">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="67433-314">Für die Tab-Taste kann die APP MoveFocus mit der nächsten oder vorherigen aufrufen, um mit Tab und UMSCHALT + TAB auszurichten, wenn Sie beschließt, dass die WebView das nächste Tabbed-Element ist.</span><span class="sxs-lookup"><span data-stu-id="67433-314">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="67433-315">Oder die APP kann IsDialogMessage als Teil der Nachrichtenschleife aufrufen, damit die Plattform die Tab-Funktion automatisch verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="67433-315">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="67433-316">Die Plattform wird durch alle Fenster mit WS_TABSTOP gedreht.</span><span class="sxs-lookup"><span data-stu-id="67433-316">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="67433-317">Wenn die WebView den Fokus von IsDialogMessage erhält, wird der Fokus intern auf das erste oder letzte Element für Tab und UMSCHALT + TAB gesetzt.</span><span class="sxs-lookup"><span data-stu-id="67433-317">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (int i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="67433-318">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="67433-318">NavigateToString</span></span> 

<span data-ttu-id="67433-319">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="67433-319">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="67433-320">Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="67433-320">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="67433-321">Der htmlContent-Parameter darf nicht größer als 2 MB Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="67433-321">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="67433-322">Der Ursprung der neuen Seite lautet: leer.</span><span class="sxs-lookup"><span data-stu-id="67433-322">The origin of the new page will be about:blank.</span></span>

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="67433-323">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-323">add_NavigationStarting</span></span> 

<span data-ttu-id="67433-324">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-324">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="67433-325">Public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-325">public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-326">NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="67433-326">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="67433-327">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67433-327">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
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

#### <span data-ttu-id="67433-328">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-328">remove_NavigationStarting</span></span> 

<span data-ttu-id="67433-329">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-329">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="67433-330">Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-330">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-331">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="67433-331">add_DocumentStateChanged</span></span> 

<span data-ttu-id="67433-332">Fügen Sie einen Ereignishandler für das DocumentStateChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-332">Add an event handler for the DocumentStateChanged event.</span></span>

> <span data-ttu-id="67433-333">Public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-333">public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-334">DocumentStateChanged wird ausgelöst, wenn neuer Inhalt im Hauptframe der WebView geladen wird oder wenn dieselbe Seitennavigation ausgeführt wird (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigation).</span><span class="sxs-lookup"><span data-stu-id="67433-334">DocumentStateChanged fires when new content has started loading on the webview's main frame or if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="67433-335">Dies folgt dem NavigationStarting-Ereignis und geht dem NavigationCompleted-Ereignis voraus.</span><span class="sxs-lookup"><span data-stu-id="67433-335">This follows the NavigationStarting event and precedes the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="67433-336">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="67433-336">remove_DocumentStateChanged</span></span> 

<span data-ttu-id="67433-337">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentStateChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-337">Remove an event handler previously added with add_DocumentStateChanged.</span></span>

> <span data-ttu-id="67433-338">Public HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-338">public HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-339">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="67433-339">add_NavigationCompleted</span></span> 

<span data-ttu-id="67433-340">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-340">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="67433-341">Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-341">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-342">Das NavigationCompleted-Ereignis wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-342">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="67433-343">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="67433-343">remove_NavigationCompleted</span></span> 

<span data-ttu-id="67433-344">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-344">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="67433-345">Public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-345">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-346">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-346">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="67433-347">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-347">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="67433-348">Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-348">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-349">FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="67433-349">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="67433-350">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67433-350">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### <span data-ttu-id="67433-351">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67433-351">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="67433-352">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-352">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="67433-353">Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-353">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-354">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="67433-354">add_MoveFocusRequested</span></span> 

<span data-ttu-id="67433-355">Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-355">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="67433-356">Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-356">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-357">MoveFocusRequested wird ausgelöst, wenn der Benutzer versucht, die Tab-Taste aus der WebView zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="67433-357">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="67433-358">Der Fokus der WebView wurde nicht geändert, wenn dieses Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="67433-358">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="67433-359">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="67433-359">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="67433-360">Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-360">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="67433-361">Public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-361">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-362">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="67433-362">add_GotFocus</span></span> 

<span data-ttu-id="67433-363">Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-363">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="67433-364">Public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-364">public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-365">GotFocus wird ausgelöst, wenn WebView den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="67433-365">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="67433-366">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="67433-366">remove_GotFocus</span></span> 

<span data-ttu-id="67433-367">Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-367">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="67433-368">Public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-368">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-369">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="67433-369">add_LostFocus</span></span> 

<span data-ttu-id="67433-370">Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-370">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="67433-371">Public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-371">public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-372">LostFocus wird ausgelöst, wenn WebView den Fokus verloren hat.</span><span class="sxs-lookup"><span data-stu-id="67433-372">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="67433-373">In dem Fall, in dem das MoveFocusRequested-Ereignis ausgelöst wird, liegt der Fokus weiterhin auf WebView, wenn das MoveFocusRequested-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="67433-373">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="67433-374">Der verlorene Fokus wird erst dann ausgelöst, wenn der app-Code oder die Standardaktion des MoveFocusRequested-Ereignisses den Fokus von WebView absetzen.</span><span class="sxs-lookup"><span data-stu-id="67433-374">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="67433-375">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="67433-375">remove_LostFocus</span></span> 

<span data-ttu-id="67433-376">Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-376">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="67433-377">Public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-377">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-378">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="67433-378">add_WebResourceRequested_deprecated</span></span> 

<span data-ttu-id="67433-379">Diese API wird als veraltet markiert, bitte verwenden Sie die neue add_WebResourceRequested-API.</span><span class="sxs-lookup"><span data-stu-id="67433-379">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>

> <span data-ttu-id="67433-380">Public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \* const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \* const resourceContextFilter, size_t filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-380">public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \*const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \*const resourceContextFilter,SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-381">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-381">Add an event handler for the WebResourceRequested event.</span></span> <span data-ttu-id="67433-382">Wird ausgelöst, wenn die WebView eine HTTP-Anforderung ausführt.</span><span class="sxs-lookup"><span data-stu-id="67433-382">Fires when the WebView has performs any HTTP request.</span></span> <span data-ttu-id="67433-383">Verwenden Sie urlFilter, um eine Liste mit der Größe filterLength von URLs zu übergeben, auf die Sie lauschen möchten.</span><span class="sxs-lookup"><span data-stu-id="67433-383">Use urlFilter to pass in a list with size filterLength of urls to listen for.</span></span> <span data-ttu-id="67433-384">Jeder URL-Eintrag unterstützt auch Platzhalter: "\*" entspricht NULL oder mehr Zeichen, und "?" entspricht genau einem Zeichen.</span><span class="sxs-lookup"><span data-stu-id="67433-384">Each url entry also supports wildcards: '\*' matches zero or more characters, and '?' matches exactly one character.</span></span> <span data-ttu-id="67433-385">Stellen Sie für jeden urlFilter-Eintrag eine übereinstimmende resourceContextFilter bereit, die die Ressourcentypen darstellt, für die WebResourceRequested ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="67433-385">For each urlFilter entry, provide a matching resourceContextFilter representing the types of resources for which WebResourceRequested should fire.</span></span> <span data-ttu-id="67433-386">Ist filterLength 0, wird das Ereignis für alle Netzwerkanforderungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67433-386">If filterLength is 0, the event will fire for all network requests.</span></span> <span data-ttu-id="67433-387">Die unterstützten Ressourcen Kontexte sind: Document, Stylesheet, Image, Media, Font, Script, XMLHttpRequest, FETCH.</span><span class="sxs-lookup"><span data-stu-id="67433-387">The supported resource contexts are: Document, Stylesheet, Image, Media, Font, Script, XHR, Fetch.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
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

#### <span data-ttu-id="67433-388">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="67433-388">remove_WebResourceRequested</span></span> 

<span data-ttu-id="67433-389">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-389">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="67433-390">Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-390">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-391">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="67433-391">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="67433-392">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-392">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="67433-393">Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-393">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-394">Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung oder Eingabeaufforderung) für die WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="67433-394">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="67433-395">Dieses Ereignis wird nur ausgelöst, wenn die IWebView2Settings:: AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="67433-395">This event only fires if the IWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
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

#### <span data-ttu-id="67433-396">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="67433-396">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="67433-397">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-397">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="67433-398">Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-398">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-399">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="67433-399">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="67433-400">Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-400">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="67433-401">Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-401">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-402">Das Ereignis wird ausgelöst, wenn die ZoomFactor-Eigenschaft des WebView geändert wird.</span><span class="sxs-lookup"><span data-stu-id="67433-402">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="67433-403">Das Ereignis konnte ausgelöst werden, weil der Aufrufer die ZoomFactor-Eigenschaft geändert hat, oder weil der Benutzer den Zoom manuell geändert hat.</span><span class="sxs-lookup"><span data-stu-id="67433-403">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="67433-404">Wenn Sie vom Aufrufer über die ZoomFactor-Eigenschaft geändert wird, wird der interne Zoomfaktor sofort aktualisiert, und es gibt kein ZoomFactorChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67433-404">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="67433-405">WebView ordnet den zuletzt verwendeten Zoomfaktor für jede Website zu.</span><span class="sxs-lookup"><span data-stu-id="67433-405">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="67433-406">Daher ist es möglich, dass sich der Zoomfaktor ändert, wenn Sie zu einer anderen Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="67433-406">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="67433-407">Wenn sich der Zoomfaktor aufgrund dieser Änderung ändert, wird das ZoomFactorChanged-Ereignis direkt hinter dem DocumentStateChanged-Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67433-407">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the DocumentStateChanged event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="67433-408">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="67433-408">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="67433-409">Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-409">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="67433-410">Public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-410">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-411">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="67433-411">add_PermissionRequested</span></span> 

<span data-ttu-id="67433-412">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-412">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="67433-413">Public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-413">public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-414">Wird ausgelöst, wenn Inhalt in einer WebView-Anforderung die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.</span><span class="sxs-lookup"><span data-stu-id="67433-414">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="67433-415">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="67433-415">remove_PermissionRequested</span></span> 

<span data-ttu-id="67433-416">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-416">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="67433-417">Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-417">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-418">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="67433-418">add_ProcessFailed</span></span> 

<span data-ttu-id="67433-419">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="67433-419">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="67433-420">Public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-420">public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-421">Wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="67433-421">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="67433-422">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="67433-422">remove_ProcessFailed</span></span> 

<span data-ttu-id="67433-423">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-423">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="67433-424">Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-424">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-425">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="67433-425">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="67433-426">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="67433-426">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="67433-427">Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="67433-427">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="67433-428">Das eingefügte Skript gilt für alle zukünftigen Dokumente und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie mit RemoveScriptToExecuteOnDocumentCreated entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="67433-428">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="67433-429">Diese wird asynchron angewendet, und Sie müssen warten, bis der vervollständigungshandler ausgeführt wird, bevor Sie sicher sein können, dass das Skript für zukünftige Navigationen ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="67433-429">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="67433-430">Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat.</span><span class="sxs-lookup"><span data-stu-id="67433-430">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="67433-431">Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.</span><span class="sxs-lookup"><span data-stu-id="67433-431">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="67433-432">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="67433-432">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="67433-433">Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-433">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="67433-434">Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="67433-434">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="67433-435">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="67433-435">ExecuteScript</span></span> 

<span data-ttu-id="67433-436">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="67433-436">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="67433-437">Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="67433-437">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="67433-438">Dies wird asynchron ausgeführt, und wenn ein Handler im ExecuteScriptCompletedHandler-Parameter bereitgestellt wird, wird die Invoke-Methode mit dem Ergebnis der Auswertung des bereitgestellten JavaScript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="67433-438">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="67433-439">Der Ergebniswert ist eine JSON-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="67433-439">The result value is a JSON encoded string.</span></span> <span data-ttu-id="67433-440">Wenn das Ergebnis undefiniert ist, einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird der JSON-NULL-Wert als Zeichenfolge "Null" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67433-440">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="67433-441">Beachten Sie, dass eine Funktion, die keinen expliziten Rückgabewert aufweist, undefined zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="67433-441">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="67433-442">Wenn das ausgeführte Skript eine nicht behandelte Ausnahme auslöst, ist das Ergebnis auch "Null".</span><span class="sxs-lookup"><span data-stu-id="67433-442">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="67433-443">Diese Methode wird asynchron angewendet.</span><span class="sxs-lookup"><span data-stu-id="67433-443">This method is applied asynchronously.</span></span> <span data-ttu-id="67433-444">Wenn der Aufruf erfolgt, während sich die WebView in einem Dokument befindet und eine Navigation nach dem Aufruf erfolgt, aber bevor das JavaScript ausgeführt wird, wird das Skript nicht ausgeführt, und der Handler wird mit E_FAIL für seinen errorCode-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="67433-444">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="67433-445">ExecuteScript funktioniert auch dann, wenn IsScriptEnabled auf "false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="67433-445">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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
            Callback<IWebView2ExecuteScriptCompletedHandler>(
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

#### <span data-ttu-id="67433-446">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="67433-446">CapturePreview</span></span> 

<span data-ttu-id="67433-447">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-447">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="67433-448">Public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) Image Format, IStream \* ImageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \*-Handler)</span><span class="sxs-lookup"><span data-stu-id="67433-448">public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="67433-449">Geben Sie das Format des Bilds mit dem ImageFormat-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="67433-449">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="67433-450">Die resultierenden Bild Binärdaten werden in den bereitgestellten ImageStream-Parameter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="67433-450">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="67433-451">Wenn CapturePreview den Schreibvorgang in den Datenstrom abgeschlossen hat, wird die Invoke-Methode für den bereitgestellten Handler-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="67433-451">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="67433-452">Laden</span><span class="sxs-lookup"><span data-stu-id="67433-452">Reload</span></span> 

<span data-ttu-id="67433-453">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="67433-453">Reload the current page.</span></span>

> <span data-ttu-id="67433-454">Public HRESULT [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="67433-454">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="67433-455">Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren.</span><span class="sxs-lookup"><span data-stu-id="67433-455">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="67433-456">Das zurück/weiter-Protokoll wird jedoch nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="67433-456">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="67433-457">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="67433-457">get_Bounds</span></span> 

<span data-ttu-id="67433-458">Die WebView-Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="67433-458">The webview bounds.</span></span>

> <span data-ttu-id="67433-459">öffentliche HRESULT- [get_Bounds](#get_bounds)(Rect \* bounds)</span><span class="sxs-lookup"><span data-stu-id="67433-459">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="67433-460">Begrenzungen sind relativ zum übergeordneten HWND.</span><span class="sxs-lookup"><span data-stu-id="67433-460">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="67433-461">Die APP hat zwei Möglichkeiten, um eine WebView-Position zu positionieren:</span><span class="sxs-lookup"><span data-stu-id="67433-461">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="67433-462">Erstellen Sie ein untergeordnetes HWND, das das übergeordnete HWND von WebView ist.</span><span class="sxs-lookup"><span data-stu-id="67433-462">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="67433-463">Positionieren Sie dieses Fenster, in dem sich die WebView befinden soll.</span><span class="sxs-lookup"><span data-stu-id="67433-463">Position this window where the WebView should be.</span></span> <span data-ttu-id="67433-464">Verwenden Sie in diesem Fall (0, 0) für die Bound's obere linke Ecke des Webviews (den Offset).</span><span class="sxs-lookup"><span data-stu-id="67433-464">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="67433-465">Verwenden Sie das oberste Fenster der App als übergeordnetes WebView-HWND.</span><span class="sxs-lookup"><span data-stu-id="67433-465">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="67433-466">Stellen Sie die Bound's-obere linke Ecke der WebView so ein, dass die WebView in der APP richtig positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="67433-466">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="67433-467">Die Werte der Bounds befinden sich im Koordinatenbereich des Hosts.</span><span class="sxs-lookup"><span data-stu-id="67433-467">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="67433-468">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="67433-468">put_Bounds</span></span> 

<span data-ttu-id="67433-469">Die Bounds-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="67433-469">Set the Bounds property.</span></span>

> <span data-ttu-id="67433-470">öffentliche HRESULT- [put_Bounds](#put_bounds)(Rect-Begrenzungen)</span><span class="sxs-lookup"><span data-stu-id="67433-470">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### <span data-ttu-id="67433-471">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="67433-471">get_ZoomFactor</span></span> 

<span data-ttu-id="67433-472">Der Zoomfaktor für die aktuelle Seite im WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-472">The zoom factor for the current page in the WebView.</span></span>

> <span data-ttu-id="67433-473">öffentliche HRESULT- [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="67433-473">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="67433-474">Der Zoomfaktor wird pro Website beibehalten.</span><span class="sxs-lookup"><span data-stu-id="67433-474">The zoom factor is persisted per site.</span></span> <span data-ttu-id="67433-475">Beachten Sie, dass das Ändern des Zoomfaktors `window.innerWidth/innerHeight` zu einer Änderung des Seitenlayouts führen kann.</span><span class="sxs-lookup"><span data-stu-id="67433-475">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="67433-476">Wenn WebView von einer anderen Website zu einer Seite navigiert, wird der Zoomfaktor für die vorherige Seite nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="67433-476">When WebView navigates to a page from a different site, the zoom factor set for the previous page will not be applied.</span></span> <span data-ttu-id="67433-477">Wenn die APP den Zoomfaktor für eine bestimmte Seite einstellen möchte, befindet sich der früheste Ort im DocumentStateChanged-Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="67433-477">If the app wants to set the zoom factor for a certain page, the earliest place to do it is in the DocumentStateChanged event handler.</span></span> <span data-ttu-id="67433-478">Wenn dies der Fall ist, wird möglicherweise ein ZoomFactorChanged-Ereignis für den beibehaltenen Zoomfaktor empfangen, bevor das ZoomFactorChanged-Ereignis für den angegebenen Zoomfaktor empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="67433-478">Note that if it does that, it might receive a ZoomFactorChanged event for the persisted zoom factor before receiving the ZoomFactorChanged event for the specified zoom factor.</span></span> <span data-ttu-id="67433-479">Die Angabe einer ZoomFactor kleiner oder gleich 0 ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="67433-479">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="67433-480">WebView verfügt auch über einen internen unterstützten Zoomfaktor Bereich.</span><span class="sxs-lookup"><span data-stu-id="67433-480">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="67433-481">Wenn sich ein angegebener Zoomfaktor außerhalb dieses Bereichs befindet, wird er normalisiert, sodass er innerhalb des Bereichs liegt, und ein ZoomFactorChanged-Ereignis wird für den tatsächlich angewendeten Zoomfaktor ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67433-481">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="67433-482">Wenn diese Bereichs Normalisierung erfolgt, meldet die ZoomFactor-Eigenschaft den Zoomfaktor, der während der vorherigen Änderung der ZoomFactor-Eigenschaft angegeben wird, bis das ZoomFactorChanged-Ereignis empfangen wird, nachdem WebView den normalisierten Zoomfaktor angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="67433-482">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="67433-483">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="67433-483">put_ZoomFactor</span></span> 

<span data-ttu-id="67433-484">Festlegen der ZoomFactor-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="67433-484">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="67433-485">öffentliche HRESULT- [put_ZoomFactor](#put_zoomfactor)(Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="67433-485">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="67433-486">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="67433-486">get_IsVisible</span></span> 

<span data-ttu-id="67433-487">Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="67433-487">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="67433-488">öffentliche HRESULT- [get_IsVisible](#get_isvisible)(bool \* isVisible)</span><span class="sxs-lookup"><span data-stu-id="67433-488">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="67433-489">Wenn IsVisible auf "false" festgelegt ist, ist die WebView transparent und wird nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="67433-489">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="67433-490">Dies wirkt sich jedoch nicht auf das Fenster aus, das die WebView enthält (den HWND-Parameter, der an CreateView übergeben wurde).</span><span class="sxs-lookup"><span data-stu-id="67433-490">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateWebView).</span></span> <span data-ttu-id="67433-491">Wenn Sie möchten, dass das Fenster ebenfalls ausgeblendet wird, rufen Sie ShowWindow direkt zusätzlich zum Ändern der IsVisible-Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="67433-491">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="67433-492">WebView als untergeordnetes Fenster ruft keine Fenster Meldungen ab, wenn das oberste Fenster minimiert oder wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="67433-492">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="67433-493">Aus Leistungsgründen sollte Entwickler die IsVisible-Eigenschaft der WebView-Eigenschaft auf "false" festlegen, wenn das App-Fenster minimiert wird, und zurück zu "true", wenn das App-Fenster wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="67433-493">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="67433-494">Das App-Fenster kann dies tun, indem SC_MINIMIZE und SC_RESTORE Befehl beim empfangen WM_SYSCOMMAND Nachricht behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="67433-494">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="67433-495">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="67433-495">put_IsVisible</span></span> 

<span data-ttu-id="67433-496">Festlegen der IsVisible-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="67433-496">Set the IsVisible property.</span></span>

> <span data-ttu-id="67433-497">öffentliche HRESULT- [put_IsVisible](#put_isvisible)(bool isVisible)</span><span class="sxs-lookup"><span data-stu-id="67433-497">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="67433-498">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="67433-498">PostWebMessageAsJson</span></span> 

<span data-ttu-id="67433-499">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in diesem [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="67433-499">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>

> <span data-ttu-id="67433-500">Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="67433-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="67433-501">Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67433-501">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="67433-502">JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen:</span><span class="sxs-lookup"><span data-stu-id="67433-502">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="67433-503">Das Ereignis args ist eine Instanz von `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="67433-503">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="67433-504">Die IWebView2Settings:: IsWebMessageEnabled-Einstellung muss wahr sein, oder diese Methode schlägt mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="67433-504">The IWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="67433-505">Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-505">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="67433-506">Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt.</span><span class="sxs-lookup"><span data-stu-id="67433-506">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="67433-507">Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="67433-507">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="67433-508">Diese Nachricht wird asynchron gesendet.</span><span class="sxs-lookup"><span data-stu-id="67433-508">This message is sent asynchronously.</span></span> <span data-ttu-id="67433-509">Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="67433-509">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="67433-510">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="67433-510">PostWebMessageAsString</span></span> 

<span data-ttu-id="67433-511">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="67433-511">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="67433-512">Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="67433-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="67433-513">Dies verhält sich auf die gleiche Weise wie PostWebMessageAsJson, aber die `window.chrome.webview` Dateneigenschaft des Nachrichtenereignisses arg ist eine Zeichenfolge mit dem gleichen Wert wie webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="67433-513">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="67433-514">Verwenden Sie diese anstelle von PostWebMessageAsJson, wenn Sie über einfache Zeichenfolgen anstelle von JSON-Objekten kommunizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="67433-514">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="67433-515">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="67433-515">add_WebMessageReceived</span></span> 

<span data-ttu-id="67433-516">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="67433-516">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="67433-517">öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \*-Handler, EventRegistrationToken \*-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-517">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-518">Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="67433-518">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```cpp
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

 <span data-ttu-id="67433-519">Wenn PostMessage aufgerufen wird, wird der [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) -Satz über diese SetWebMessageReceivedEventHandler-Methode aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="67433-519">When postMessage is called, the [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="67433-520">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="67433-520">remove_WebMessageReceived</span></span> 

<span data-ttu-id="67433-521">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-521">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="67433-522">Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-522">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-523">Schließen</span><span class="sxs-lookup"><span data-stu-id="67433-523">Close</span></span> 

<span data-ttu-id="67433-524">Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.</span><span class="sxs-lookup"><span data-stu-id="67433-524">Closes the webview and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="67433-525">Public HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="67433-525">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="67433-526">Durch Bereinigen des Browsers Instanz werden die Ressourcen freigegeben, die die WebView-Ansicht einschalten.</span><span class="sxs-lookup"><span data-stu-id="67433-526">Cleaning up the browser instace will release the resources powering the webview.</span></span> <span data-ttu-id="67433-527">Die Browserinstanz wird heruntergefahren, wenn keine anderen Webansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67433-527">The browser instance will be shut down if there are no other webviews using it.</span></span>

<span data-ttu-id="67433-528">Nach dem Aufruf von Close werden alle Methodenaufrufe fehlschlagen, und die Ereignishandler werden nicht mehr ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="67433-528">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="67433-529">Insbesondere gibt die WebView Ihre Verweise auf die Ereignishandler frei, wenn Close aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="67433-529">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="67433-530">Close wird implizit aufgerufen, wenn die WebView den endgültigen Bezug verliert und zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="67433-530">Close is implicitly called when the WebView loses its final reference and is destructed.</span></span> <span data-ttu-id="67433-531">Es empfiehlt sich jedoch, explizit Close aufzurufen, um einen zufälligen Zyklus von Verweisen zwischen WebView und app-Code zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="67433-531">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="67433-532">Insbesondere wenn Sie einen Verweis auf die WebView in einem Ereignishandler aufzeichnen, erstellen Sie einen Referenz Zyklus zwischen WebView und dem Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="67433-532">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="67433-533">Schließen bricht diesen Zyklus ab, indem alle Ereignishandler freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="67433-533">Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="67433-534">Um diese Situation zu vermeiden, empfiehlt es sich jedoch, sowohl explizit Close für die WebView aufzurufen und keinen Verweis auf die WebView zu erfassen, um sicherzustellen, dass die WebView ordnungsgemäß bereinigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="67433-534">But to avoid this situation it is best practice to both explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### <span data-ttu-id="67433-535">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="67433-535">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="67433-536">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="67433-536">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="67433-537">Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="67433-537">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="67433-538">Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="67433-538">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="67433-539">Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="67433-539">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="67433-540">Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="67433-540">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="67433-541">Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="67433-541">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="67433-542">Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="67433-542">Invoke will be called with the method's return object as a JSON string.</span></span>

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
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="67433-543">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="67433-543">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="67433-544">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="67433-544">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="67433-545">Public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR EventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* Handler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="67433-545">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="67433-546">Eine Liste und eine Beschreibung der verfügbaren Ereignisse finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="67433-546">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available events.</span></span> <span data-ttu-id="67433-547">Der eventName-Parameter ist der vollständige Name des Ereignisses im Format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="67433-547">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="67433-548">Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="67433-548">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="67433-549">Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter-Objekt des CDP-Ereignisses als JSON-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="67433-549">Invoke will be called with the an event args object containing the CDP event's parameter object as a JSON string.</span></span>

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
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="67433-550">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="67433-550">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="67433-551">Entfernen Sie einen Ereignishandler, der zuvor mit add_DevToolsProtocolEventReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-551">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="67433-552">Public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR EventName, EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="67433-552">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName,EventRegistrationToken token)</span></span>

#### <span data-ttu-id="67433-553">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="67433-553">get_BrowserProcessId</span></span> 

<span data-ttu-id="67433-554">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="67433-554">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="67433-555">Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="67433-555">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="67433-556">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="67433-556">get_CanGoBack</span></span> 

<span data-ttu-id="67433-557">Kann im WebView zur vorherigen Seite im Navigationsverlauf navigieren.</span><span class="sxs-lookup"><span data-stu-id="67433-557">Can navigate the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="67433-558">Public HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="67433-558">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="67433-559">get_CanGoBack ändern Sie den Wert mit dem DocumentStateChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67433-559">get_CanGoBack change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="67433-560">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="67433-560">get_CanGoForward</span></span> 

<span data-ttu-id="67433-561">Kann im WebView zur nächsten Seite im Navigationsverlauf navigieren.</span><span class="sxs-lookup"><span data-stu-id="67433-561">Can navigate the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="67433-562">Public HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="67433-562">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="67433-563">get_CanGoForward ändern Sie den Wert mit dem DocumentStateChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="67433-563">get_CanGoForward change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="67433-564">GoBack</span><span class="sxs-lookup"><span data-stu-id="67433-564">GoBack</span></span> 

<span data-ttu-id="67433-565">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="67433-565">Navigates the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="67433-566">Public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="67433-566">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="67433-567">GoForward</span><span class="sxs-lookup"><span data-stu-id="67433-567">GoForward</span></span> 

<span data-ttu-id="67433-568">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="67433-568">Navigates the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="67433-569">Public HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="67433-569">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="67433-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="67433-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="67433-571">Bildformat, das von der [IWebView2WebView:: CapturePreview](#capturepreview) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="67433-571">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>

> <span data-ttu-id="67433-572">Enum- [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="67433-572">enum [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="67433-573">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-573">Values</span></span>                         | <span data-ttu-id="67433-574">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-574">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="67433-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="67433-576">PNG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="67433-576">PNG image format.</span></span>
<span data-ttu-id="67433-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="67433-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="67433-578">JPEG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="67433-578">JPEG image format.</span></span>

#### <span data-ttu-id="67433-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="67433-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="67433-580">Art des in der [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) -Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="67433-580">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>

> <span data-ttu-id="67433-581">Enum- [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="67433-581">enum [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="67433-582">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-582">Values</span></span>                         | <span data-ttu-id="67433-583">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-583">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="67433-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="67433-585">Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="67433-585">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="67433-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="67433-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="67433-587">Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="67433-587">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="67433-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="67433-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="67433-589">Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="67433-589">A dialog invoked via the window.prompt JavaScript function.</span></span>

#### <span data-ttu-id="67433-590">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="67433-590">WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="67433-591">Art des in der [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) -Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="67433-591">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>

> <span data-ttu-id="67433-592">Enum- [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="67433-592">enum [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)</span></span>

 <span data-ttu-id="67433-593">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-593">Values</span></span>                         | <span data-ttu-id="67433-594">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-594">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="67433-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="67433-596">Gibt an, dass der Browserprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-596">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="67433-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="67433-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="67433-598">Gibt an, dass der Renderprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="67433-598">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="67433-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="67433-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="67433-600">Gibt an, dass der Renderprozess nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="67433-600">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="67433-601">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="67433-601">WEBVIEW2_PERMISSION_TYPE</span></span> 

<span data-ttu-id="67433-602">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="67433-602">The type of a permission request.</span></span>

> <span data-ttu-id="67433-603">Enum- [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)</span><span class="sxs-lookup"><span data-stu-id="67433-603">enum [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)</span></span>

 <span data-ttu-id="67433-604">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-604">Values</span></span>                         | <span data-ttu-id="67433-605">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-605">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="67433-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="67433-607">Unbekannte Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="67433-607">Unknown permission.</span></span>
<span data-ttu-id="67433-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="67433-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span></span>            | <span data-ttu-id="67433-609">Berechtigung zum Aufzeichnen von Audio.</span><span class="sxs-lookup"><span data-stu-id="67433-609">Permission to capture audio.</span></span>
<span data-ttu-id="67433-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span><span class="sxs-lookup"><span data-stu-id="67433-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span></span>            | <span data-ttu-id="67433-611">Berechtigung zum Aufzeichnen von Videos.</span><span class="sxs-lookup"><span data-stu-id="67433-611">Permission to capture video.</span></span>
<span data-ttu-id="67433-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="67433-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span></span>            | <span data-ttu-id="67433-613">Berechtigung für den Zugriff auf Geolocation.</span><span class="sxs-lookup"><span data-stu-id="67433-613">Permission to access geolocation.</span></span>
<span data-ttu-id="67433-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="67433-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span></span>            | <span data-ttu-id="67433-615">Berechtigung zum Senden von webbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="67433-615">Permission to send web notifications.</span></span>
<span data-ttu-id="67433-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="67433-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span></span>            | <span data-ttu-id="67433-617">Berechtigung für den Zugriff auf den generischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="67433-617">Permission to access generic sensor.</span></span>
<span data-ttu-id="67433-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="67433-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span></span>            | <span data-ttu-id="67433-619">Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste</span><span class="sxs-lookup"><span data-stu-id="67433-619">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="67433-620">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="67433-620">WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="67433-621">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="67433-621">Response to a permission request.</span></span>

> <span data-ttu-id="67433-622">Enum- [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="67433-622">enum [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)</span></span>

 <span data-ttu-id="67433-623">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-623">Values</span></span>                         | <span data-ttu-id="67433-624">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-624">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="67433-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="67433-626">Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.</span><span class="sxs-lookup"><span data-stu-id="67433-626">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="67433-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="67433-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="67433-628">Erteilen Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="67433-628">Grant the permission request.</span></span>
<span data-ttu-id="67433-629">WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="67433-629">WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="67433-630">Verweigern Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="67433-630">Deny the permission request.</span></span>

#### <span data-ttu-id="67433-631">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="67433-631">WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="67433-632">Grund für das Verschieben des Fokus</span><span class="sxs-lookup"><span data-stu-id="67433-632">Reason for moving focus.</span></span>

> <span data-ttu-id="67433-633">Enum- [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)</span><span class="sxs-lookup"><span data-stu-id="67433-633">enum [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)</span></span>

 <span data-ttu-id="67433-634">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-634">Values</span></span>                         | <span data-ttu-id="67433-635">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-635">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="67433-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="67433-637">Der Fokus für die Code Einstellung in WebView.</span><span class="sxs-lookup"><span data-stu-id="67433-637">Code setting focus into WebView.</span></span>
<span data-ttu-id="67433-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="67433-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="67433-639">Verschieben des Fokus aufgrund von Tabstopps vorwärts</span><span class="sxs-lookup"><span data-stu-id="67433-639">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="67433-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="67433-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="67433-641">Verschieben des Fokus aufgrund von Tabstopps rückwärts</span><span class="sxs-lookup"><span data-stu-id="67433-641">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="67433-642">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="67433-642">WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="67433-643">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="67433-643">Error status values for web navigations.</span></span>

> <span data-ttu-id="67433-644">Enum- [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="67433-644">enum [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)</span></span>

 <span data-ttu-id="67433-645">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-645">Values</span></span>                         | <span data-ttu-id="67433-646">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-646">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="67433-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="67433-648">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="67433-648">An unknown error occurred.</span></span>
<span data-ttu-id="67433-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="67433-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="67433-650">Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.</span><span class="sxs-lookup"><span data-stu-id="67433-650">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="67433-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="67433-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="67433-652">Das SSL-Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="67433-652">The SSL certificate has expired.</span></span>
<span data-ttu-id="67433-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="67433-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="67433-654">Das SSL-Clientzertifikat enthält Fehler.</span><span class="sxs-lookup"><span data-stu-id="67433-654">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="67433-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="67433-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="67433-656">Das SSL-Zertifikat wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="67433-656">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="67433-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="67433-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="67433-658">Das SSL-Zertifikat ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="67433-658">The SSL certificate is invalid.</span></span>
<span data-ttu-id="67433-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="67433-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="67433-660">Der Host ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="67433-660">The host is unreachable.</span></span>
<span data-ttu-id="67433-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="67433-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="67433-662">Die Verbindung hat ein Zeitlimit überschritten.</span><span class="sxs-lookup"><span data-stu-id="67433-662">The connection has timed out.</span></span>
<span data-ttu-id="67433-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="67433-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="67433-664">Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67433-664">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="67433-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="67433-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="67433-666">Die Verbindung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="67433-666">The connection was aborted.</span></span>
<span data-ttu-id="67433-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="67433-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="67433-668">Die Verbindung wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="67433-668">The connection was reset.</span></span>
<span data-ttu-id="67433-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="67433-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="67433-670">Die Internet Verbindung wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="67433-670">The Internet connection has been lost.</span></span>
<span data-ttu-id="67433-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="67433-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="67433-672">Verbindung mit Ziel kann nicht hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="67433-672">Cannot connect to destination.</span></span>
<span data-ttu-id="67433-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="67433-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="67433-674">Der angegebene Hostname konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="67433-674">Could not resolve provided host name.</span></span>
<span data-ttu-id="67433-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="67433-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="67433-676">Der Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="67433-676">The operation was canceled.</span></span>
<span data-ttu-id="67433-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="67433-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="67433-678">Die Anforderungs Umleitung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="67433-678">The request redirect failed.</span></span>
<span data-ttu-id="67433-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="67433-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="67433-680">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="67433-680">An unexpected error occurred.</span></span>

#### <span data-ttu-id="67433-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="67433-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="67433-682">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="67433-682">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="67433-683">Enum- [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="67433-683">enum [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)</span></span>

 <span data-ttu-id="67433-684">Werte</span><span class="sxs-lookup"><span data-stu-id="67433-684">Values</span></span>                         | <span data-ttu-id="67433-685">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67433-685">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="67433-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="67433-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="67433-687">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-687">All resources.</span></span>
<span data-ttu-id="67433-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="67433-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="67433-689">Dokument Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-689">Document resources.</span></span>
<span data-ttu-id="67433-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="67433-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="67433-691">CSS-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-691">CSS resources.</span></span>
<span data-ttu-id="67433-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="67433-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="67433-693">Bildressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-693">Image resources.</span></span>
<span data-ttu-id="67433-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="67433-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="67433-695">Andere Medienressourcen wie Videos.</span><span class="sxs-lookup"><span data-stu-id="67433-695">Other media resources such as videos.</span></span>
<span data-ttu-id="67433-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="67433-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="67433-697">Schriftartressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-697">Font resources.</span></span>
<span data-ttu-id="67433-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="67433-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="67433-699">Skriptressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-699">Script resources.</span></span>
<span data-ttu-id="67433-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="67433-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="67433-701">XML-HTTP-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="67433-701">XML HTTP requests.</span></span>
<span data-ttu-id="67433-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="67433-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="67433-703">Abrufen der API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="67433-703">Fetch API communication.</span></span>
<span data-ttu-id="67433-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="67433-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="67433-705">Texttracking-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-705">TextTrack resources.</span></span>
<span data-ttu-id="67433-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="67433-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | 
<span data-ttu-id="67433-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="67433-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | 
<span data-ttu-id="67433-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="67433-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | 
<span data-ttu-id="67433-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="67433-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | 
<span data-ttu-id="67433-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="67433-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | 
<span data-ttu-id="67433-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="67433-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | 
<span data-ttu-id="67433-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="67433-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="67433-713">Andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="67433-713">Other resources.</span></span>
