---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d80570a82559fccb6ae3896f7543ed75959436fa
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884428"
---
# <span data-ttu-id="710d2-104">0.9.430-Interface-ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="710d2-104">0.9.430 - interface ICoreWebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="710d2-105">WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.</span><span class="sxs-lookup"><span data-stu-id="710d2-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="710d2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="710d2-106">Summary</span></span>

 <span data-ttu-id="710d2-107">Member</span><span class="sxs-lookup"><span data-stu-id="710d2-107">Members</span></span>                        | <span data-ttu-id="710d2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="710d2-109">get_Settings</span><span class="sxs-lookup"><span data-stu-id="710d2-109">get_Settings</span></span>](#get_settings) | <span data-ttu-id="710d2-110">Das ICoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-110">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="710d2-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="710d2-111">get_Source</span></span>](#get_source) | <span data-ttu-id="710d2-112">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="710d2-112">The URI of the current top level document.</span></span>
[<span data-ttu-id="710d2-113">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="710d2-113">Navigate</span></span>](#navigate) | <span data-ttu-id="710d2-114">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="710d2-114">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="710d2-115">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="710d2-115">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="710d2-116">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="710d2-116">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="710d2-117">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-117">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="710d2-118">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-118">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="710d2-119">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-119">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="710d2-120">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-120">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="710d2-121">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="710d2-121">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="710d2-122">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-122">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="710d2-123">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="710d2-123">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="710d2-124">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-124">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="710d2-125">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-125">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="710d2-126">Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-126">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="710d2-127">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-127">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="710d2-128">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-128">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="710d2-129">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-129">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="710d2-130">Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="710d2-130">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="710d2-131">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-131">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="710d2-132">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-132">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="710d2-133">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="710d2-133">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="710d2-134">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-134">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="710d2-135">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="710d2-135">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="710d2-136">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-136">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="710d2-137">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-137">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="710d2-138">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-138">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="710d2-139">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-139">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="710d2-140">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-140">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="710d2-141">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="710d2-141">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="710d2-142">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-142">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="710d2-143">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="710d2-143">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="710d2-144">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-144">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="710d2-145">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-145">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="710d2-146">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-146">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="710d2-147">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-147">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="710d2-148">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-148">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="710d2-149">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="710d2-149">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="710d2-150">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-150">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="710d2-151">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="710d2-151">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="710d2-152">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-152">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="710d2-153">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="710d2-153">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="710d2-154">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-154">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="710d2-155">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="710d2-155">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="710d2-156">Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-156">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="710d2-157">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="710d2-157">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="710d2-158">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-158">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="710d2-159">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="710d2-159">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="710d2-160">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-160">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="710d2-161">Laden</span><span class="sxs-lookup"><span data-stu-id="710d2-161">Reload</span></span>](#reload) | <span data-ttu-id="710d2-162">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="710d2-162">Reload the current page.</span></span>
[<span data-ttu-id="710d2-163">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="710d2-163">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="710d2-164">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-164">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="710d2-165">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="710d2-165">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="710d2-166">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="710d2-166">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="710d2-167">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="710d2-167">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="710d2-168">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="710d2-168">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="710d2-169">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="710d2-169">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="710d2-170">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-170">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="710d2-171">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="710d2-171">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="710d2-172">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="710d2-172">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="710d2-173">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="710d2-173">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="710d2-174">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="710d2-174">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="710d2-175">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="710d2-175">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="710d2-176">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="710d2-176">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="710d2-177">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="710d2-177">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="710d2-178">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="710d2-178">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="710d2-179">GoBack</span><span class="sxs-lookup"><span data-stu-id="710d2-179">GoBack</span></span>](#goback) | <span data-ttu-id="710d2-180">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="710d2-180">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="710d2-181">GoForward</span><span class="sxs-lookup"><span data-stu-id="710d2-181">GoForward</span></span>](#goforward) | <span data-ttu-id="710d2-182">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="710d2-182">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="710d2-183">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="710d2-183">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="710d2-184">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="710d2-184">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="710d2-185">Stop</span><span class="sxs-lookup"><span data-stu-id="710d2-185">Stop</span></span>](#stop) | <span data-ttu-id="710d2-186">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="710d2-186">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="710d2-187">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-187">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="710d2-188">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-188">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="710d2-189">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-189">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="710d2-190">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-190">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="710d2-191">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-191">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="710d2-192">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-192">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="710d2-193">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-193">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="710d2-194">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-194">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="710d2-195">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="710d2-195">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="710d2-196">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="710d2-196">The title for the current top level document.</span></span>
[<span data-ttu-id="710d2-197">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="710d2-197">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="710d2-198">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-198">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="710d2-199">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="710d2-199">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="710d2-200">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-200">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="710d2-201">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="710d2-201">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="710d2-202">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-202">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="710d2-203">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-203">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="710d2-204">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="710d2-204">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="710d2-205">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-205">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="710d2-206">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-206">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="710d2-207">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="710d2-207">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="710d2-208">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="710d2-208">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="710d2-209">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-209">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="710d2-210">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-210">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="710d2-211">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-211">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="710d2-212">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-212">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="710d2-213">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="710d2-213">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="710d2-214">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-214">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="710d2-215">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="710d2-215">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="710d2-216">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-216">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="710d2-217">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-217">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="710d2-218">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-218">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="710d2-219">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-219">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="710d2-220">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-220">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="710d2-221">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="710d2-221">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#core_webview2_capture_preview_image_format) | <span data-ttu-id="710d2-222">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-222">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="710d2-223">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="710d2-223">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#core_webview2_script_dialog_kind) | <span data-ttu-id="710d2-224">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="710d2-224">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="710d2-225">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="710d2-225">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#core_webview2_process_failed_kind) | <span data-ttu-id="710d2-226">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="710d2-226">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="710d2-227">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="710d2-227">CORE_WEBVIEW2_PERMISSION_KIND</span></span>](#core_webview2_permission_kind) | <span data-ttu-id="710d2-228">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="710d2-228">The type of a permission request.</span></span>
[<span data-ttu-id="710d2-229">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="710d2-229">CORE_WEBVIEW2_PERMISSION_STATE</span></span>](#core_webview2_permission_state) | <span data-ttu-id="710d2-230">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="710d2-230">Response to a permission request.</span></span>
[<span data-ttu-id="710d2-231">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="710d2-231">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span>](#core_webview2_web_error_status) | <span data-ttu-id="710d2-232">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="710d2-232">Error status values for web navigations.</span></span>
[<span data-ttu-id="710d2-233">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="710d2-233">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#core_webview2_web_resource_context) | <span data-ttu-id="710d2-234">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="710d2-234">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="710d2-235">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="710d2-235">Navigation events</span></span>

<span data-ttu-id="710d2-236">Die normale Abfolge von Navigations Ereignissen lautet NavigationStarting, sourced, ContentLoading und dann NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="710d2-236">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="710d2-238">Beachten Sie, dass dies für Navigationsereignisse mit dem gleichen Navigations-Event-arg gilt.</span><span class="sxs-lookup"><span data-stu-id="710d2-238">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="710d2-239">Navigationsereignisse mit unterschiedlichen Navigations-Event-args können sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="710d2-239">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="710d2-240">Wenn Sie beispielsweise eine Navigation auf das NavigationStarting-Ereignis warten und dann eine andere Navigation starten, sehen Sie die NavigationStarting für die erste Navigation, gefolgt von der NavigationStarting der zweiten Navigation, gefolgt von der NavigationCompleted für die erste Navigation und dann allen anderen geeigneten Navigations Ereignissen für die zweite Navigation.</span><span class="sxs-lookup"><span data-stu-id="710d2-240">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="710d2-241">In Fehlerfällen kann es sich um ein ContentLoading-Ereignis handeln, das davon abhängt, ob die Navigation auf einer Fehlerseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-241">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="710d2-242">Im Fall einer HTTP-Umleitung gibt es mehrere NavigationStarting-Ereignisse in einer Zeile, wobei für diejenigen, die dem ersten Folgen, das isredirect-Flag festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-242">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="710d2-243">Verwenden Sie FrameNavigationStarting, um die Navigation innerhalb von unter Frames in der WebView zu überwachen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="710d2-243">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="710d2-244">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="710d2-244">Process model</span></span>

<span data-ttu-id="710d2-245">WebView2 verwendet das gleiche Prozessmodell wie der Edge-Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="710d2-245">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="710d2-246">Es gibt einen Edge-Browserprozess pro angegebenen Benutzerdatenverzeichnis in einer Benutzersitzung, die jedem WebView2-Aufrufprozess dient, der das Benutzerdatenverzeichnis angibt.</span><span class="sxs-lookup"><span data-stu-id="710d2-246">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="710d2-247">Dies bedeutet, dass ein Edge-Browser-Prozess möglicherweise mehrere Anruf Prozesse bedient, und ein Aufrufprozess möglicherweise mehrere Edge-Browser-Prozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="710d2-247">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="710d2-249">In einem Browserprozess gibt es eine Reihe von Renderer-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="710d2-249">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="710d2-250">Diese werden nach Bedarf erstellt, um potenziell mehrere Frames in verschiedenen Webansichten zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="710d2-250">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="710d2-251">Die Anzahl der Renderer-Prozesse variiert basierend auf dem Feature "Website Isolierungs Browser" und der Anzahl der unterschiedlichen getrennten Ursprünge, die in verknüpften Webansichten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-251">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="710d2-253">Mithilfe des ProcessFailure-Ereignisses können Sie auf Abstürze reagieren und in diesen Browser-und Renderer-Prozessen hängen bleiben.</span><span class="sxs-lookup"><span data-stu-id="710d2-253">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="710d2-254">Sie können zugeordnete Browser-und Renderer-Prozesse mit der Close-Methode sicher Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="710d2-254">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="710d2-255">Threadingmodell</span><span class="sxs-lookup"><span data-stu-id="710d2-255">Threading model</span></span>

<span data-ttu-id="710d2-256">Der WebView2 muss in einem UI-Thread erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-256">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="710d2-257">Insbesondere ein Thread mit einer Nachrichten Pumpe.</span><span class="sxs-lookup"><span data-stu-id="710d2-257">Specifically a thread with a message pump.</span></span> <span data-ttu-id="710d2-258">Alle Rückrufe werden in diesem Thread ausgeführt, und Aufrufe an die WebView müssen in diesem Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-258">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="710d2-259">Es ist nicht sicher, die WebView aus einem anderen Thread zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="710d2-259">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="710d2-260">Rückrufe, einschließlich Ereignishandlern und Vervollständigungs Handlern, werden seriell ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710d2-260">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="710d2-261">Das heißt, wenn Sie einen Ereignishandler ausführen und eine Nachrichtenschleife beginnen, werden keine anderen Ereignishandler oder Abschluss Rückrufe erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710d2-261">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="710d2-262">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="710d2-262">Security</span></span>

<span data-ttu-id="710d2-263">Überprüfen Sie immer die Source-Eigenschaft von WebView, bevor Sie executeScript, PostWebMessageAsJson, PostWebMessageAsString oder eine andere Methode verwenden, um Informationen an die WebView zu senden.</span><span class="sxs-lookup"><span data-stu-id="710d2-263">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="710d2-264">Die WebView kann über den Endbenutzer, der mit der Seite oder dem Skript auf der Seite interagiert, die Navigation verursacht hat, zu einer anderen Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="710d2-264">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="710d2-265">Achten Sie auf ähnliche Weise auf AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="710d2-265">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="710d2-266">Alle zukünftigen Navigationselemente führen dieses Skript aus, und wenn es Zugriff auf Informationen bietet, die nur für einen bestimmten Ursprung vorgesehen sind, kann jedes HTML-Dokumentzugriff haben.</span><span class="sxs-lookup"><span data-stu-id="710d2-266">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="710d2-267">Bei der Untersuchung des Ergebnisses eines executeScript-Methodenaufrufs, eines WebMessageReceived-Ereignisses, immer überprüfen der Quelle des Absenders oder eines anderen Mechanismus zum Empfangen von Informationen aus einem HTML-Dokument in einer WebView überprüfen Sie, ob der URI des HTML-Dokuments Ihren Erwartungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="710d2-267">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="710d2-268">Wenn Sie eine Nachricht erstellen, die Sie in eine WebView senden möchten, verwenden Sie PostWebMessageAsJson, und erstellen Sie den JSON-Zeichenfolgenparameter mithilfe einer JSON-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="710d2-268">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="710d2-269">Dadurch werden potenzielle Unfälle von Codierungsinformationen in eine JSON-Zeichenfolge oder ein Skript vermieden, und sichergestellt, dass keine von Angreifern gesteuerte Eingabe den restlichen Teil der JSON-Nachricht ändern oder ein beliebiges Skript ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="710d2-269">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="710d2-270">Zeichenfolgentypen</span><span class="sxs-lookup"><span data-stu-id="710d2-270">String types</span></span>

<span data-ttu-id="710d2-271">Zeichenfolgenparameter sind LPWSTR NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="710d2-271">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="710d2-272">Der aufgerufene ordnet die Zeichenfolge mithilfe von CoTaskMemAlloc zu.</span><span class="sxs-lookup"><span data-stu-id="710d2-272">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="710d2-273">Der Besitz wird an den Anrufer übertragen, und es ist dem Anrufer überlassen, den Speicher mit CoTaskMemFree zu befreien.</span><span class="sxs-lookup"><span data-stu-id="710d2-273">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="710d2-274">Zeichenfolge in Parametern sind LPCWSTR NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="710d2-274">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="710d2-275">Der Aufrufer stellt sicher, dass die Zeichenfolge für die Dauer des synchronen Funktionsaufrufs gültig ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-275">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="710d2-276">Wenn der aufgerufene diesen Wert nach Abschluss des Funktionsaufrufs bis zu einem gewissen Punkt beibehalten muss, muss der aufgerufene eine eigene Kopie des Zeichenfolgenwerts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="710d2-276">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="710d2-277">URI-und JSON-Analyse</span><span class="sxs-lookup"><span data-stu-id="710d2-277">URI and JSON parsing</span></span>

<span data-ttu-id="710d2-278">Verschiedene Methoden stellen URIs und JSON als Zeichenfolgen bereit oder akzeptieren Sie.</span><span class="sxs-lookup"><span data-stu-id="710d2-278">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="710d2-279">Verwenden Sie für die Analyse und Generierung dieser Zeichenfolgen ihre eigene bevorzugte Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="710d2-279">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="710d2-280">Wenn WinRT für Ihre app verfügbar ist, können Sie `RuntimeClass_Windows_Data_Json_JsonObject` JSON-Zeichenfolgen verwenden und erstellen oder URIs analysieren und `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` erstellen.</span><span class="sxs-lookup"><span data-stu-id="710d2-280">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="710d2-281">Beide arbeiten in Win32-apps.</span><span class="sxs-lookup"><span data-stu-id="710d2-281">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="710d2-282">Wenn Sie IUri und CreateUri zum Analysieren von URIs verwenden, sollten Sie möglicherweise die folgenden URI-Erstellungs Flags verwenden, damit CreateUri-Verhalten der URI-Analyse in der WebView genauer entspricht:</span><span class="sxs-lookup"><span data-stu-id="710d2-282">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="710d2-283">Debuggen</span><span class="sxs-lookup"><span data-stu-id="710d2-283">Debugging</span></span>

<span data-ttu-id="710d2-284">Öffnen Sie devtools mit den normalen Tastenkombinationen: `F12` oder `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="710d2-284">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="710d2-285">Sie können die `--auto-open-devtools-for-tabs` Befehlsargument Schalter verwenden, um das devtools-Fenster sofort zu öffnen, wenn Sie das erste Mal eine WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="710d2-285">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="710d2-286">Informationen zum Bereitstellen zusätzlicher Befehlszeilenargumente für den Browserprozess finden Sie in der CreateCoreWebView2Host-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="710d2-286">See CreateCoreWebView2Host documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="710d2-287">Schauen Sie sich den LoaderOverride-Registrierungsschlüssel an, um verschiedene Builds von WebView2 zu testen, ohne die Anwendung in der CreateCoreWebView2Host-Dokumentation zu ändern.</span><span class="sxs-lookup"><span data-stu-id="710d2-287">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Host documentation.</span></span>

## <span data-ttu-id="710d2-288">Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="710d2-288">Versioning</span></span>

<span data-ttu-id="710d2-289">Nachdem Sie eine bestimmte Version des SDK zum Erstellen Ihrer APP verwendet haben, wird Ihre APP möglicherweise mit einer älteren oder neueren Version der installierten Browser-Binärdateien ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710d2-289">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="710d2-290">Bis Version 1.0.0.0 von WebView2 können sich während der Updates Änderungen ändern, die verhindern, dass Ihr SDK mit unterschiedlichen Versionen der installierten Browser-Binärdateien funktioniert.</span><span class="sxs-lookup"><span data-stu-id="710d2-290">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="710d2-291">Nach der Version 1.0.0.0 können verschiedene Versionen des SDKs mit unterschiedlichen Versionen des installierten Browsers funktionieren, indem Sie die folgenden bewährten Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="710d2-291">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="710d2-292">Wenn Sie Änderungen an der API berücksichtigen möchten, müssen Sie sicherstellen, dass Sie beim Aufrufen der DLL-Export CreateCoreWebView2Environment und beim Aufrufen von QueryInterface für ein beliebiges CoreWebView2-Objekt auf Fehler überprüfen.</span><span class="sxs-lookup"><span data-stu-id="710d2-292">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="710d2-293">Ein Rückgabewert von E_NOINTERFACE kann darauf hindeuten, dass das SDK nicht mit den Binärdateien des Edge-Browsers kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-293">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="710d2-294">Das Überprüfen auf Fehler von QueryInterface berücksichtigt auch Fälle, in denen das SDK neuer als die Version des Edge-Browsers ist und Ihre APP versucht, eine Schnittstelle zu verwenden, von der der Edge-Browser nichts weiß.</span><span class="sxs-lookup"><span data-stu-id="710d2-294">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="710d2-295">Wenn eine Schnittstelle nicht zur Verfügung steht, können Sie das zugeordnete Feature nach Möglichkeit deaktivieren oder den Endbenutzer anderweitig darüber informieren, dass Sie den Browser aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="710d2-295">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="710d2-296">Member</span><span class="sxs-lookup"><span data-stu-id="710d2-296">Members</span></span>

#### <span data-ttu-id="710d2-297">get_Settings</span><span class="sxs-lookup"><span data-stu-id="710d2-297">get_Settings</span></span> 

<span data-ttu-id="710d2-298">Das ICoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-298">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="710d2-299">öffentliche HRESULT- [get_Settings](#get_settings)(ICoreWebView2Settings \* \*-Einstellungen)</span><span class="sxs-lookup"><span data-stu-id="710d2-299">public HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings \*\* settings)</span></span>

#### <span data-ttu-id="710d2-300">get_Source</span><span class="sxs-lookup"><span data-stu-id="710d2-300">get_Source</span></span> 

<span data-ttu-id="710d2-301">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="710d2-301">The URI of the current top level document.</span></span>

> <span data-ttu-id="710d2-302">Public HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="710d2-302">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="710d2-303">Dieser Wert ändert sich möglicherweise als Teil der Ereignis Befeuerungs Quelle für einige Fälle, beispielsweise das Navigieren zu einer anderen Website oder zu einer anderen Fragment-Navigation.</span><span class="sxs-lookup"><span data-stu-id="710d2-303">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="710d2-304">Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-304">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="710d2-305">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="710d2-305">Navigate</span></span> 

<span data-ttu-id="710d2-306">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="710d2-306">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="710d2-307">öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="710d2-307">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="710d2-308">Weitere Informationen finden Sie in den Navigations Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="710d2-308">See the navigation events for more information.</span></span> <span data-ttu-id="710d2-309">Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-309">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

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

#### <span data-ttu-id="710d2-310">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="710d2-310">NavigateToString</span></span> 

<span data-ttu-id="710d2-311">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="710d2-311">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="710d2-312">Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="710d2-312">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="710d2-313">Der htmlContent-Parameter darf nicht größer als 2 MB Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="710d2-313">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="710d2-314">Der Ursprung der neuen Seite lautet: leer.</span><span class="sxs-lookup"><span data-stu-id="710d2-314">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="710d2-315">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-315">add_NavigationStarting</span></span> 

<span data-ttu-id="710d2-316">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-316">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="710d2-317">Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-317">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-318">NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="710d2-318">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="710d2-319">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="710d2-319">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="710d2-320">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-320">remove_NavigationStarting</span></span> 

<span data-ttu-id="710d2-321">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-321">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="710d2-322">Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-322">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-323">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="710d2-323">add_ContentLoading</span></span> 

<span data-ttu-id="710d2-324">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-324">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="710d2-325">Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-325">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-326">ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden ContentLoading werden nicht ausgelöst, wenn dieselbe Seitennavigation erfolgt (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigation).</span><span class="sxs-lookup"><span data-stu-id="710d2-326">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="710d2-327">Dies folgt auf das NavigationStarting-Ereignis und das Source-Ereignis und steht vor den Ereignissen "History" und "NavigationCompleted".</span><span class="sxs-lookup"><span data-stu-id="710d2-327">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="710d2-328">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="710d2-328">remove_ContentLoading</span></span> 

<span data-ttu-id="710d2-329">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-329">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="710d2-330">Public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-330">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-331">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-331">add_SourceChanged</span></span> 

<span data-ttu-id="710d2-332">Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-332">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="710d2-333">Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-333">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-334">Die Quelle wird ausgelöst, um zu einer anderen Website oder zu einer anderen Fragment-Navigation zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="710d2-334">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="710d2-335">Sie wird nicht für andere Navigations Typen wie "Seiten-Reload" oder "History. pushState" mit der gleichen URL wie die aktuelle Seite ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="710d2-335">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="710d2-336">Die Quelle wird vor ContentLoading für die Navigation zu einem neuen Dokument ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="710d2-336">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="710d2-337">Fügen Sie einen Ereignishandler für das Quellpfad-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-337">Add an event handler for the SourceChanged event.</span></span> 

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
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="710d2-338">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-338">remove_SourceChanged</span></span> 

<span data-ttu-id="710d2-339">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-339">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="710d2-340">Public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-340">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-341">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-341">add_HistoryChanged</span></span> 

<span data-ttu-id="710d2-342">Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="710d2-342">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="710d2-343">Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-343">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-344">Verwenden Sie abrechnungshistorieändern, um zu überprüfen, ob sich get_CanGoBack/get_CanGoForward Wert geändert hat.</span><span class="sxs-lookup"><span data-stu-id="710d2-344">Use HistoryChange to check if get_CanGoBack/get_CanGoForward value has changed.</span></span> <span data-ttu-id="710d2-345">"History" wird auch für die Verwendung von GoBack/GoForward ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="710d2-345">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="710d2-346">"History" wird nach "sourcely" und "ContentLoading" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="710d2-346">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="710d2-347">Fügen Sie einen Ereignishandler für das History-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-347">Add an event handler for the HistoryChanged event.</span></span> 

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
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="710d2-348">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-348">remove_HistoryChanged</span></span> 

<span data-ttu-id="710d2-349">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-349">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="710d2-350">Public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-350">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-351">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="710d2-351">add_NavigationCompleted</span></span> 

<span data-ttu-id="710d2-352">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-352">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="710d2-353">Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-353">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-354">Das NavigationCompleted-Ereignis wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-354">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="710d2-355">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="710d2-355">remove_NavigationCompleted</span></span> 

<span data-ttu-id="710d2-356">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-356">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="710d2-357">Public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-357">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-358">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-358">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="710d2-359">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-359">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="710d2-360">Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-360">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-361">FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="710d2-361">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="710d2-362">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="710d2-362">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="710d2-363">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="710d2-363">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="710d2-364">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-364">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="710d2-365">Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-365">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-366">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="710d2-366">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="710d2-367">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-367">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="710d2-368">Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-368">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-369">Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung oder Eingabeaufforderung) für die WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-369">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="710d2-370">Dieses Ereignis wird nur ausgelöst, wenn die ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-370">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="710d2-371">Das ScriptDialogOpening-Ereignis kann verwendet werden, um Dialogfelder zu unterdrücken oder Standarddialogfelder durch benutzerdefinierte Dialogfelder zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="710d2-371">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
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

#### <span data-ttu-id="710d2-372">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="710d2-372">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="710d2-373">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-373">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="710d2-374">Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-374">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-375">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-375">add_PermissionRequested</span></span> 

<span data-ttu-id="710d2-376">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-376">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="710d2-377">Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-377">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-378">Wird ausgelöst, wenn Inhalt in einer WebView-Anforderung die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.</span><span class="sxs-lookup"><span data-stu-id="710d2-378">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
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

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="710d2-379">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-379">remove_PermissionRequested</span></span> 

<span data-ttu-id="710d2-380">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-380">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="710d2-381">Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-381">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-382">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="710d2-382">add_ProcessFailed</span></span> 

<span data-ttu-id="710d2-383">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-383">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="710d2-384">Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-384">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-385">Wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="710d2-385">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
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
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="710d2-386">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="710d2-386">remove_ProcessFailed</span></span> 

<span data-ttu-id="710d2-387">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-387">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="710d2-388">Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-388">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-389">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="710d2-389">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="710d2-390">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-390">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="710d2-391">Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="710d2-391">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="710d2-392">Das eingefügte Skript gilt für alle zukünftigen Dokumente und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie mit RemoveScriptToExecuteOnDocumentCreated entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-392">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="710d2-393">Diese wird asynchron angewendet, und Sie müssen warten, bis der vervollständigungshandler ausgeführt wird, bevor Sie sicher sein können, dass das Skript für zukünftige Navigationen ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="710d2-393">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="710d2-394">Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat.</span><span class="sxs-lookup"><span data-stu-id="710d2-394">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="710d2-395">Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.</span><span class="sxs-lookup"><span data-stu-id="710d2-395">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="710d2-396">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="710d2-396">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="710d2-397">Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-397">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="710d2-398">Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="710d2-398">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="710d2-399">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="710d2-399">ExecuteScript</span></span> 

<span data-ttu-id="710d2-400">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-400">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="710d2-401">Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="710d2-401">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="710d2-402">Dies wird asynchron ausgeführt, und wenn ein Handler im ExecuteScriptCompletedHandler-Parameter bereitgestellt wird, wird die Invoke-Methode mit dem Ergebnis der Auswertung des bereitgestellten JavaScript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="710d2-402">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="710d2-403">Der Ergebniswert ist eine JSON-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="710d2-403">The result value is a JSON encoded string.</span></span> <span data-ttu-id="710d2-404">Wenn das Ergebnis undefiniert ist, einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird der JSON-NULL-Wert als Zeichenfolge "Null" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="710d2-404">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="710d2-405">Beachten Sie, dass eine Funktion, die keinen expliziten Rückgabewert aufweist, undefined zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="710d2-405">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="710d2-406">Wenn das ausgeführte Skript eine nicht behandelte Ausnahme auslöst, ist das Ergebnis auch "Null".</span><span class="sxs-lookup"><span data-stu-id="710d2-406">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="710d2-407">Diese Methode wird asynchron angewendet.</span><span class="sxs-lookup"><span data-stu-id="710d2-407">This method is applied asynchronously.</span></span> <span data-ttu-id="710d2-408">Wenn der Aufruf erfolgt, während sich die WebView in einem Dokument befindet und eine Navigation nach dem Aufruf erfolgt, aber bevor das JavaScript ausgeführt wird, wird das Skript nicht ausgeführt, und der Handler wird mit E_FAIL für seinen errorCode-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="710d2-408">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="710d2-409">ExecuteScript funktioniert auch dann, wenn IsScriptEnabled auf "false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-409">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="710d2-410">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="710d2-410">CapturePreview</span></span> 

<span data-ttu-id="710d2-411">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-411">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="710d2-412">Public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) Image Format, IStream \* ImageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \*-Handler)</span><span class="sxs-lookup"><span data-stu-id="710d2-412">public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="710d2-413">Geben Sie das Format des Bilds mit dem ImageFormat-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="710d2-413">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="710d2-414">Die resultierenden Bild Binärdaten werden in den bereitgestellten ImageStream-Parameter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="710d2-414">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="710d2-415">Wenn CapturePreview den Schreibvorgang in den Datenstrom abgeschlossen hat, wird die Invoke-Methode für den bereitgestellten Handler-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="710d2-415">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
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

#### <span data-ttu-id="710d2-416">Laden</span><span class="sxs-lookup"><span data-stu-id="710d2-416">Reload</span></span> 

<span data-ttu-id="710d2-417">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="710d2-417">Reload the current page.</span></span>

> <span data-ttu-id="710d2-418">Public HRESULT [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="710d2-418">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="710d2-419">Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren.</span><span class="sxs-lookup"><span data-stu-id="710d2-419">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="710d2-420">Das zurück/weiter-Protokoll wird jedoch nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="710d2-420">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="710d2-421">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="710d2-421">PostWebMessageAsJson</span></span> 

<span data-ttu-id="710d2-422">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-422">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="710d2-423">Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="710d2-423">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="710d2-424">Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="710d2-424">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="710d2-425">JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen:</span><span class="sxs-lookup"><span data-stu-id="710d2-425">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="710d2-426">Das Ereignis args ist eine Instanz von `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="710d2-426">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="710d2-427">Die ICoreWebView2Settings:: IsWebMessageEnabled-Einstellung muss wahr sein, oder diese Methode schlägt mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="710d2-427">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="710d2-428">Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-428">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="710d2-429">Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt.</span><span class="sxs-lookup"><span data-stu-id="710d2-429">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="710d2-430">Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="710d2-430">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="710d2-431">Diese Nachricht wird asynchron gesendet.</span><span class="sxs-lookup"><span data-stu-id="710d2-431">This message is sent asynchronously.</span></span> <span data-ttu-id="710d2-432">Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="710d2-432">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="710d2-433">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="710d2-433">PostWebMessageAsString</span></span> 

<span data-ttu-id="710d2-434">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="710d2-434">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="710d2-435">Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="710d2-435">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="710d2-436">Dies verhält sich auf die gleiche Weise wie PostWebMessageAsJson, aber die `window.chrome.webview` Dateneigenschaft des Nachrichtenereignisses arg ist eine Zeichenfolge mit dem gleichen Wert wie webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="710d2-436">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="710d2-437">Verwenden Sie diese anstelle von PostWebMessageAsJson, wenn Sie über einfache Zeichenfolgen anstelle von JSON-Objekten kommunizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="710d2-437">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="710d2-438">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="710d2-438">add_WebMessageReceived</span></span> 

<span data-ttu-id="710d2-439">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="710d2-439">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="710d2-440">öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \*-Handler, EventRegistrationToken \*-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-440">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-441">Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-441">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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

 <span data-ttu-id="710d2-442">Wenn PostMessage aufgerufen wird, wird der [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) -Satz über diese SetWebMessageReceivedEventHandler-Methode aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-442">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="710d2-443">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="710d2-443">remove_WebMessageReceived</span></span> 

<span data-ttu-id="710d2-444">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-444">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="710d2-445">Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-445">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-446">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="710d2-446">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="710d2-447">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="710d2-447">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="710d2-448">Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="710d2-448">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="710d2-449">Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="710d2-449">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="710d2-450">Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="710d2-450">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="710d2-451">Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="710d2-451">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="710d2-452">Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-452">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="710d2-453">Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="710d2-453">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="710d2-454">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="710d2-454">get_BrowserProcessId</span></span> 

<span data-ttu-id="710d2-455">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="710d2-455">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="710d2-456">Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="710d2-456">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="710d2-457">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="710d2-457">get_CanGoBack</span></span> 

<span data-ttu-id="710d2-458">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="710d2-458">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="710d2-459">Public HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="710d2-459">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="710d2-460">Das History-Ereignis wird ausgelöst, wenn der Wert von get_CanGoBack geändert wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-460">The HistoryChanged event will fire if get_CanGoBack changes value.</span></span>

#### <span data-ttu-id="710d2-461">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="710d2-461">get_CanGoForward</span></span> 

<span data-ttu-id="710d2-462">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="710d2-462">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="710d2-463">Public HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="710d2-463">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="710d2-464">Das History-Ereignis wird ausgelöst, wenn der Wert von get_CanGoForward geändert wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-464">The HistoryChanged event will fire if get_CanGoForward changes value.</span></span>

#### <span data-ttu-id="710d2-465">GoBack</span><span class="sxs-lookup"><span data-stu-id="710d2-465">GoBack</span></span> 

<span data-ttu-id="710d2-466">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="710d2-466">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="710d2-467">Public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="710d2-467">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="710d2-468">GoForward</span><span class="sxs-lookup"><span data-stu-id="710d2-468">GoForward</span></span> 

<span data-ttu-id="710d2-469">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="710d2-469">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="710d2-470">Public HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="710d2-470">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="710d2-471">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="710d2-471">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="710d2-472">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="710d2-472">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="710d2-473">Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="710d2-473">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="710d2-474">Der eventName-Parameter ist der vollständige Name des Ereignisses im Format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="710d2-474">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="710d2-475">Eine Liste der Beschreibungen von devtools-Protokollereignissen und Ereignis args finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="710d2-475">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="710d2-476">Stop</span><span class="sxs-lookup"><span data-stu-id="710d2-476">Stop</span></span> 

<span data-ttu-id="710d2-477">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="710d2-477">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="710d2-478">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="710d2-478">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="710d2-479">Skripts werden nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="710d2-479">Does not stop scripts.</span></span>

#### <span data-ttu-id="710d2-480">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-480">add_NewWindowRequested</span></span> 

<span data-ttu-id="710d2-481">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-481">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="710d2-482">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-482">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-483">Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open.</span><span class="sxs-lookup"><span data-stu-id="710d2-483">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="710d2-484">Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-484">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
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

#### <span data-ttu-id="710d2-485">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-485">remove_NewWindowRequested</span></span> 

<span data-ttu-id="710d2-486">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-486">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="710d2-487">Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-487">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-488">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-488">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="710d2-489">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-489">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="710d2-490">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-490">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-491">Das Ereignis wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-491">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="710d2-492">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-492">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="710d2-493">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-493">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="710d2-494">Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-494">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-495">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="710d2-495">get_DocumentTitle</span></span> 

<span data-ttu-id="710d2-496">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="710d2-496">The title for the current top level document.</span></span>

> <span data-ttu-id="710d2-497">öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="710d2-497">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="710d2-498">Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="710d2-498">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="710d2-499">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="710d2-499">AddRemoteObject</span></span> 

<span data-ttu-id="710d2-500">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-500">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="710d2-501">Public HRESULT [addremoteobject](#addremoteobject)(LPCWSTR-Name, Variant \*-Objekt)</span><span class="sxs-lookup"><span data-stu-id="710d2-501">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="710d2-502">Host Objekte werden als Remoteobjekt Proxys über bereitgestellt `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="710d2-502">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="710d2-503">Remote Objektproxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="710d2-503">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="710d2-504">Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="710d2-504">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="710d2-505">Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="710d2-505">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="710d2-506">Wenn der Anwendungscode beispielsweise Folgendes durchführt:</span><span class="sxs-lookup"><span data-stu-id="710d2-506">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="710d2-507">JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen:</span><span class="sxs-lookup"><span data-stu-id="710d2-507">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="710d2-508">Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-508">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="710d2-509">Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt.</span><span class="sxs-lookup"><span data-stu-id="710d2-509">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="710d2-510">Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-510">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="710d2-511">Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="710d2-511">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="710d2-512">Arrays von nach Verweistypen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="710d2-512">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="710d2-513">VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="710d2-513">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="710d2-514">In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="710d2-514">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="710d2-515">Darüber hinaus werden alle Remoteobjekte als verfügbar gemacht `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="710d2-515">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="710d2-516">Hier werden die Hostobjekte als synchrone Remoteobjekt Proxys verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="710d2-516">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="710d2-517">Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="710d2-517">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="710d2-518">Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.remoteObjects.<name>` API verwenden.</span><span class="sxs-lookup"><span data-stu-id="710d2-518">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="710d2-519">Synchrone Remoteobjekt Proxys und asynchrone Remoteobjekt Proxys können sowohl Proxys für dasselbe Remoteobjekt als auch Proxys sein.</span><span class="sxs-lookup"><span data-stu-id="710d2-519">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="710d2-520">Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Remoteobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.</span><span class="sxs-lookup"><span data-stu-id="710d2-520">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="710d2-521">Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="710d2-521">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="710d2-522">Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.</span><span class="sxs-lookup"><span data-stu-id="710d2-522">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="710d2-523">Remote Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen.</span><span class="sxs-lookup"><span data-stu-id="710d2-523">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="710d2-524">Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710d2-524">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="710d2-525">Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.remoteObjects.options.forceLocalProperties` lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710d2-525">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="710d2-526">Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="710d2-526">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="710d2-527">Sie können diesem Array nach Bedarf weitere hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="710d2-527">You can add more to this array as required.</span></span>

<span data-ttu-id="710d2-528">Es gibt eine Methode `chrome.webview.remoteObjects.cleanupSome` , mit der die Garbage Collection von Remoteobjekt Proxys am besten abläuft.</span><span class="sxs-lookup"><span data-stu-id="710d2-528">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="710d2-529">Für Remote Objektproxys gibt es zusätzlich die folgenden Methoden, die lokal ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="710d2-529">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="710d2-530">applyRemote, getRemote, setremote: Durchführen eines Methodenaufrufs, eines Eigenschaften Abstands oder eines Eigenschaftssatzes für das Remoteobjekt.</span><span class="sxs-lookup"><span data-stu-id="710d2-530">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="710d2-531">Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-531">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="710d2-532">Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="710d2-532">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="710d2-533">`proxy.applyRemote('toString')`Wird aber `toString` stattdessen auf dem Remoteproxy Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710d2-533">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="710d2-534">getLocal, setlocal: führt Eigenschaften abrufen oder Eigenschaftssatz lokal aus.</span><span class="sxs-lookup"><span data-stu-id="710d2-534">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="710d2-535">Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Remoteobjekt Proxy selbst und nicht für das Remoteobjekt zu erzwingen, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="710d2-535">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="710d2-536">Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Remoteproxy Objekt benannt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-536">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="710d2-537">`proxy.getLocal('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.</span><span class="sxs-lookup"><span data-stu-id="710d2-537">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="710d2-538">Synchronisierung: asynchrone Remoteobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die ein Versprechen für einen synchronen Remoteobjekt Proxy für das gleiche Remoteobjekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="710d2-538">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="710d2-539">Gibt beispielsweise `chrome.webview.remoteObjects.sample.methodCall()` einen asynchronen Remoteobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="710d2-539">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="710d2-540">Sie können stattdessen die `sync` Methode zum Abrufen eines synchronen Remoteobjekt Proxys verwenden:</span><span class="sxs-lookup"><span data-stu-id="710d2-540">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="710d2-541">Async: synchrone Remoteobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Remoteobjekt Proxy für das gleiche Remoteobjekt blockiert und zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="710d2-541">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="710d2-542">Gibt beispielsweise `chrome.webview.remoteObjects.sync.sample.methodCall()` einen synchronen Remoteobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="710d2-542">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="710d2-543">Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Remoteobjekt Proxys für dasselbe Remoteobjekt:</span><span class="sxs-lookup"><span data-stu-id="710d2-543">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="710d2-544">dann: asynchrone Remoteobjekt Proxys verfügen über eine then-Methode.</span><span class="sxs-lookup"><span data-stu-id="710d2-544">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="710d2-545">Auf diese Weise können Sie warten.</span><span class="sxs-lookup"><span data-stu-id="710d2-545">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="710d2-546">gibt eine Verheißung zurück, die mit einer Darstellung des Remoteobjekts aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-546">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="710d2-547">Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="710d2-547">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="710d2-548">Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="710d2-548">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="710d2-549">Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Remoteobjekt Proxys zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="710d2-549">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="710d2-550">Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710d2-550">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="710d2-551">Asynchrone Remoteobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="710d2-551">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="710d2-552">Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-552">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="710d2-553">Synchrone Remoteobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-553">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="710d2-554">Das Festlegen einer Eigenschaft für einen asynchronen Remoteobjekt Proxy funktioniert etwas anders.</span><span class="sxs-lookup"><span data-stu-id="710d2-554">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="710d2-555">Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-555">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="710d2-556">Dies ist eine Anforderung des JavaScript-Proxy Objekts.</span><span class="sxs-lookup"><span data-stu-id="710d2-556">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="710d2-557">Wenn Sie asynchron warten müssen, bis die Eigenschaft auf Complete gesetzt ist, verwenden Sie die setremote-Methode, die eine Verheißung zurückgibt, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="710d2-557">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="710d2-558">Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-558">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="710d2-559">Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="710d2-559">For example, suppose you have a COM object with the following interface</span></span>

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="710d2-560">Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="710d2-560">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="710d2-561">In diesem Fall nennen wir `sample` Folgendes:</span><span class="sxs-lookup"><span data-stu-id="710d2-561">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="710d2-562">Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.remoteObjects.sample` Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="710d2-562">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="710d2-563">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="710d2-563">RemoveRemoteObject</span></span> 

<span data-ttu-id="710d2-564">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-564">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="710d2-565">Public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="710d2-565">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="710d2-566">Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="710d2-566">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="710d2-567">Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="710d2-567">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="710d2-568">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="710d2-568">OpenDevToolsWindow</span></span> 

<span data-ttu-id="710d2-569">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="710d2-569">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="710d2-570">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="710d2-570">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="710d2-571">Wenn das devtools-Fenster bereits geöffnet ist, wird nichts aufgerufen</span><span class="sxs-lookup"><span data-stu-id="710d2-571">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="710d2-572">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-572">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="710d2-573">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="710d2-573">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="710d2-574">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-574">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-575">Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt.</span><span class="sxs-lookup"><span data-stu-id="710d2-575">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="710d2-576">Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert.</span><span class="sxs-lookup"><span data-stu-id="710d2-576">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="710d2-577">Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.</span><span class="sxs-lookup"><span data-stu-id="710d2-577">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="710d2-578">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="710d2-578">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="710d2-579">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-579">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="710d2-580">Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-580">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-581">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="710d2-581">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="710d2-582">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="710d2-582">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="710d2-583">Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="710d2-583">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="710d2-584">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-584">add_WebResourceRequested</span></span> 

<span data-ttu-id="710d2-585">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-585">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="710d2-586">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-586">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-587">Wird ausgelöst, wenn die WebView eine HTTP-Anforderung an einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-587">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="710d2-588">Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-588">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### <span data-ttu-id="710d2-589">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-589">remove_WebResourceRequested</span></span> 

<span data-ttu-id="710d2-590">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-590">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="710d2-591">Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-591">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-592">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="710d2-592">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="710d2-593">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-593">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="710d2-594">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="710d2-594">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="710d2-595">Der URI-Parameter kann eine Platzhalterzeichenfolge (' ': 0 oder mehr; '? ': genau eins) sein.</span><span class="sxs-lookup"><span data-stu-id="710d2-595">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="710d2-596">nullptr entspricht L "".</span><span class="sxs-lookup"><span data-stu-id="710d2-596">nullptr is equivalent to L"".</span></span> <span data-ttu-id="710d2-597">Eine Beschreibung der Ressourcenkontext Filter finden Sie unter CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="710d2-597">See CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="710d2-598">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="710d2-598">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="710d2-599">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-599">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="710d2-600">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="710d2-600">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="710d2-601">Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-601">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="710d2-602">Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-602">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="710d2-603">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-603">add_WindowCloseRequested</span></span> 

<span data-ttu-id="710d2-604">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="710d2-604">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="710d2-605">Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-605">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="710d2-606">Wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close.</span><span class="sxs-lookup"><span data-stu-id="710d2-606">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="710d2-607">Die APP sollte das Fenster WebView und verwandte APP schließen, wenn dies für die APP sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="710d2-607">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="710d2-608">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="710d2-608">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="710d2-609">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-609">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="710d2-610">Public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="710d2-610">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="710d2-611">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="710d2-611">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="710d2-612">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-612">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="710d2-613">Enum- [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="710d2-613">enum [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="710d2-614">Werte</span><span class="sxs-lookup"><span data-stu-id="710d2-614">Values</span></span>                         | <span data-ttu-id="710d2-615">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-615">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="710d2-616">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="710d2-616">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="710d2-617">PNG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="710d2-617">PNG image format.</span></span>
<span data-ttu-id="710d2-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="710d2-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="710d2-619">JPEG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="710d2-619">JPEG image format.</span></span>

#### <span data-ttu-id="710d2-620">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="710d2-620">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="710d2-621">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="710d2-621">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="710d2-622">Enum- [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="710d2-622">enum [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="710d2-623">Werte</span><span class="sxs-lookup"><span data-stu-id="710d2-623">Values</span></span>                         | <span data-ttu-id="710d2-624">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-624">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="710d2-625">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="710d2-625">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="710d2-626">Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-626">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="710d2-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="710d2-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="710d2-628">Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-628">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="710d2-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="710d2-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="710d2-630">Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-630">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="710d2-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="710d2-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="710d2-632">Ein Dialogfeld, das über das beforeunload-JavaScript-Ereignis aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="710d2-632">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="710d2-633">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="710d2-633">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="710d2-634">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="710d2-634">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="710d2-635">Enum- [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="710d2-635">enum [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span></span>

 <span data-ttu-id="710d2-636">Werte</span><span class="sxs-lookup"><span data-stu-id="710d2-636">Values</span></span>                         | <span data-ttu-id="710d2-637">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-637">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="710d2-638">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="710d2-638">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="710d2-639">Gibt an, dass der Browserprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-639">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="710d2-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="710d2-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="710d2-641">Gibt an, dass der Renderprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="710d2-641">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="710d2-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="710d2-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="710d2-643">Gibt an, dass der Renderprozess nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="710d2-643">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="710d2-644">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="710d2-644">CORE_WEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="710d2-645">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="710d2-645">The type of a permission request.</span></span>

> <span data-ttu-id="710d2-646">Enum- [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="710d2-646">enum [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span></span>

 <span data-ttu-id="710d2-647">Werte</span><span class="sxs-lookup"><span data-stu-id="710d2-647">Values</span></span>                         | <span data-ttu-id="710d2-648">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-648">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="710d2-649">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="710d2-649">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="710d2-650">Unbekannte Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="710d2-650">Unknown permission.</span></span>
<span data-ttu-id="710d2-651">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="710d2-651">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="710d2-652">Berechtigung zum Aufzeichnen von Audio.</span><span class="sxs-lookup"><span data-stu-id="710d2-652">Permission to capture audio.</span></span>
<span data-ttu-id="710d2-653">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="710d2-653">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="710d2-654">Berechtigung zum Aufzeichnen von Videos.</span><span class="sxs-lookup"><span data-stu-id="710d2-654">Permission to capture video.</span></span>
<span data-ttu-id="710d2-655">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="710d2-655">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="710d2-656">Berechtigung für den Zugriff auf Geolocation.</span><span class="sxs-lookup"><span data-stu-id="710d2-656">Permission to access geolocation.</span></span>
<span data-ttu-id="710d2-657">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="710d2-657">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="710d2-658">Berechtigung zum Senden von webbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="710d2-658">Permission to send web notifications.</span></span>
<span data-ttu-id="710d2-659">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="710d2-659">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="710d2-660">Berechtigung für den Zugriff auf den generischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="710d2-660">Permission to access generic sensor.</span></span>
<span data-ttu-id="710d2-661">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="710d2-661">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="710d2-662">Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste</span><span class="sxs-lookup"><span data-stu-id="710d2-662">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="710d2-663">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="710d2-663">CORE_WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="710d2-664">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="710d2-664">Response to a permission request.</span></span>

> <span data-ttu-id="710d2-665">Enum- [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="710d2-665">enum [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span></span>

 <span data-ttu-id="710d2-666">Werte</span><span class="sxs-lookup"><span data-stu-id="710d2-666">Values</span></span>                         | <span data-ttu-id="710d2-667">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="710d2-668">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="710d2-668">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="710d2-669">Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.</span><span class="sxs-lookup"><span data-stu-id="710d2-669">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="710d2-670">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="710d2-670">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="710d2-671">Erteilen Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="710d2-671">Grant the permission request.</span></span>
<span data-ttu-id="710d2-672">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="710d2-672">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="710d2-673">Verweigern Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="710d2-673">Deny the permission request.</span></span>

#### <span data-ttu-id="710d2-674">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="710d2-674">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="710d2-675">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="710d2-675">Error status values for web navigations.</span></span>

> <span data-ttu-id="710d2-676">Enum- [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="710d2-676">enum [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span></span>

 <span data-ttu-id="710d2-677">Werte</span><span class="sxs-lookup"><span data-stu-id="710d2-677">Values</span></span>                         | <span data-ttu-id="710d2-678">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-678">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="710d2-679">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="710d2-679">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="710d2-680">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="710d2-680">An unknown error occurred.</span></span>
<span data-ttu-id="710d2-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="710d2-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="710d2-682">Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.</span><span class="sxs-lookup"><span data-stu-id="710d2-682">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="710d2-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="710d2-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="710d2-684">Das SSL-Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="710d2-684">The SSL certificate has expired.</span></span>
<span data-ttu-id="710d2-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="710d2-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="710d2-686">Das SSL-Clientzertifikat enthält Fehler.</span><span class="sxs-lookup"><span data-stu-id="710d2-686">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="710d2-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="710d2-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="710d2-688">Das SSL-Zertifikat wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="710d2-688">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="710d2-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="710d2-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="710d2-690">Das SSL-Zertifikat ist ungültig &ndash; Dies könnte bedeuten, dass das Zertifikat nicht mit den öffentlichen Schlüssel Pins für den Hostnamen übereinstimmte. das Zertifikat wird von einer nicht vertrauenswürdigen Zertifizierungsstelle signiert oder mit einem schwachen Vorzeichen Algorithmus, das Zertifikat behauptet, dass DNS-Namen gegen Namenseinschränkungen verstoßen, das Zertifikat einen schwachen Schlüssel enthält, der Gültigkeitszeitraum des Zertifikats zu lang ist, fehlender Sperrungsinformationen oder Sperrungs Mechanismus, nicht eindeutiger [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)Hostname, fehlender Zertifikat Transparenzinformationen oder das Zertifikat an</span><span class="sxs-lookup"><span data-stu-id="710d2-690">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="710d2-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="710d2-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="710d2-692">Der Host ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="710d2-692">The host is unreachable.</span></span>
<span data-ttu-id="710d2-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="710d2-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="710d2-694">Die Verbindung hat ein Zeitlimit überschritten.</span><span class="sxs-lookup"><span data-stu-id="710d2-694">The connection has timed out.</span></span>
<span data-ttu-id="710d2-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="710d2-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="710d2-696">Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="710d2-696">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="710d2-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="710d2-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="710d2-698">Die Verbindung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="710d2-698">The connection was aborted.</span></span>
<span data-ttu-id="710d2-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="710d2-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="710d2-700">Die Verbindung wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="710d2-700">The connection was reset.</span></span>
<span data-ttu-id="710d2-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="710d2-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="710d2-702">Die Internet Verbindung wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="710d2-702">The Internet connection has been lost.</span></span>
<span data-ttu-id="710d2-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="710d2-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="710d2-704">Verbindung mit Ziel kann nicht hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-704">Cannot connect to destination.</span></span>
<span data-ttu-id="710d2-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="710d2-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="710d2-706">Der angegebene Hostname konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="710d2-706">Could not resolve provided host name.</span></span>
<span data-ttu-id="710d2-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="710d2-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="710d2-708">Der Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="710d2-708">The operation was canceled.</span></span>
<span data-ttu-id="710d2-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="710d2-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="710d2-710">Die Anforderungs Umleitung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="710d2-710">The request redirect failed.</span></span>
<span data-ttu-id="710d2-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="710d2-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="710d2-712">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="710d2-712">An unexpected error occurred.</span></span>

#### <span data-ttu-id="710d2-713">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="710d2-713">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="710d2-714">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="710d2-714">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="710d2-715">Enum- [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="710d2-715">enum [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span></span>

 <span data-ttu-id="710d2-716">Werte</span><span class="sxs-lookup"><span data-stu-id="710d2-716">Values</span></span>                         | <span data-ttu-id="710d2-717">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="710d2-717">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="710d2-718">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="710d2-718">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="710d2-719">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-719">All resources.</span></span>
<span data-ttu-id="710d2-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="710d2-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="710d2-721">Dokument Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-721">Document resources.</span></span>
<span data-ttu-id="710d2-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="710d2-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="710d2-723">CSS-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-723">CSS resources.</span></span>
<span data-ttu-id="710d2-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="710d2-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="710d2-725">Bildressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-725">Image resources.</span></span>
<span data-ttu-id="710d2-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="710d2-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="710d2-727">Andere Medienressourcen wie Videos.</span><span class="sxs-lookup"><span data-stu-id="710d2-727">Other media resources such as videos.</span></span>
<span data-ttu-id="710d2-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="710d2-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="710d2-729">Schriftartressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-729">Font resources.</span></span>
<span data-ttu-id="710d2-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="710d2-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="710d2-731">Skriptressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-731">Script resources.</span></span>
<span data-ttu-id="710d2-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="710d2-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="710d2-733">XML-HTTP-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="710d2-733">XML HTTP requests.</span></span>
<span data-ttu-id="710d2-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="710d2-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="710d2-735">Abrufen der API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="710d2-735">Fetch API communication.</span></span>
<span data-ttu-id="710d2-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="710d2-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="710d2-737">Texttracking-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-737">TextTrack resources.</span></span>
<span data-ttu-id="710d2-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="710d2-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="710d2-739">EventSource-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="710d2-739">EventSource API communication.</span></span>
<span data-ttu-id="710d2-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="710d2-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="710d2-741">WebSocket-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="710d2-741">WebSocket API communication.</span></span>
<span data-ttu-id="710d2-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="710d2-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="710d2-743">Web App-Manifeste</span><span class="sxs-lookup"><span data-stu-id="710d2-743">Web App Manifests.</span></span>
<span data-ttu-id="710d2-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="710d2-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="710d2-745">Signierte http-Exchanges.</span><span class="sxs-lookup"><span data-stu-id="710d2-745">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="710d2-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="710d2-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="710d2-747">Ping-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="710d2-747">Ping requests.</span></span>
<span data-ttu-id="710d2-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="710d2-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="710d2-749">Berichte zu CSP-Verstößen</span><span class="sxs-lookup"><span data-stu-id="710d2-749">CSP Violation Reports.</span></span>
<span data-ttu-id="710d2-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="710d2-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="710d2-751">Andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="710d2-751">Other resources.</span></span>
