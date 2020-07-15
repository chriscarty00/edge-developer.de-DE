---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 6fce29c2df69abc8d55d91c267b282702e567453
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881207"
---
# <span data-ttu-id="b5f25-104">0.9.430-Interface-ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="b5f25-104">0.9.430 - interface ICoreWebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="b5f25-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="b5f25-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b5f25-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="b5f25-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="b5f25-107">WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.</span><span class="sxs-lookup"><span data-stu-id="b5f25-107">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="b5f25-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b5f25-108">Summary</span></span>

 <span data-ttu-id="b5f25-109">Member</span><span class="sxs-lookup"><span data-stu-id="b5f25-109">Members</span></span>                        | <span data-ttu-id="b5f25-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b5f25-111">get_Settings</span><span class="sxs-lookup"><span data-stu-id="b5f25-111">get_Settings</span></span>](#get_settings) | <span data-ttu-id="b5f25-112">Das ICoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-112">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="b5f25-113">get_Source</span><span class="sxs-lookup"><span data-stu-id="b5f25-113">get_Source</span></span>](#get_source) | <span data-ttu-id="b5f25-114">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="b5f25-114">The URI of the current top level document.</span></span>
[<span data-ttu-id="b5f25-115">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="b5f25-115">Navigate</span></span>](#navigate) | <span data-ttu-id="b5f25-116">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="b5f25-116">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="b5f25-117">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="b5f25-117">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="b5f25-118">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="b5f25-118">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="b5f25-119">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-119">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="b5f25-120">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-120">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="b5f25-121">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-121">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="b5f25-122">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-122">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="b5f25-123">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="b5f25-123">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="b5f25-124">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-124">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="b5f25-125">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="b5f25-125">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="b5f25-126">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-126">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="b5f25-127">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-127">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="b5f25-128">Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-128">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="b5f25-129">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-129">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="b5f25-130">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-130">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="b5f25-131">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-131">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="b5f25-132">Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="b5f25-132">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="b5f25-133">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-133">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="b5f25-134">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-134">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="b5f25-135">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="b5f25-135">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="b5f25-136">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-136">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="b5f25-137">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="b5f25-137">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="b5f25-138">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-138">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="b5f25-139">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-139">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="b5f25-140">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-140">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="b5f25-141">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-141">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="b5f25-142">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-142">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="b5f25-143">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="b5f25-143">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="b5f25-144">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-144">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="b5f25-145">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="b5f25-145">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="b5f25-146">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-146">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="b5f25-147">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-147">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="b5f25-148">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-148">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="b5f25-149">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-149">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="b5f25-150">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-150">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="b5f25-151">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="b5f25-151">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="b5f25-152">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-152">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="b5f25-153">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="b5f25-153">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="b5f25-154">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-154">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="b5f25-155">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="b5f25-155">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="b5f25-156">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-156">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="b5f25-157">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="b5f25-157">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="b5f25-158">Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-158">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="b5f25-159">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="b5f25-159">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="b5f25-160">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-160">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="b5f25-161">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="b5f25-161">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="b5f25-162">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-162">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="b5f25-163">Laden</span><span class="sxs-lookup"><span data-stu-id="b5f25-163">Reload</span></span>](#reload) | <span data-ttu-id="b5f25-164">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-164">Reload the current page.</span></span>
[<span data-ttu-id="b5f25-165">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="b5f25-165">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="b5f25-166">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-166">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="b5f25-167">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="b5f25-167">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="b5f25-168">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-168">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="b5f25-169">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="b5f25-169">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="b5f25-170">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-170">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="b5f25-171">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="b5f25-171">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="b5f25-172">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-172">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="b5f25-173">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="b5f25-173">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="b5f25-174">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b5f25-174">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="b5f25-175">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="b5f25-175">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="b5f25-176">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-176">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="b5f25-177">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="b5f25-177">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="b5f25-178">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="b5f25-178">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="b5f25-179">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="b5f25-179">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="b5f25-180">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="b5f25-180">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="b5f25-181">GoBack</span><span class="sxs-lookup"><span data-stu-id="b5f25-181">GoBack</span></span>](#goback) | <span data-ttu-id="b5f25-182">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="b5f25-182">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="b5f25-183">GoForward</span><span class="sxs-lookup"><span data-stu-id="b5f25-183">GoForward</span></span>](#goforward) | <span data-ttu-id="b5f25-184">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="b5f25-184">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="b5f25-185">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="b5f25-185">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="b5f25-186">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="b5f25-186">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="b5f25-187">Stop</span><span class="sxs-lookup"><span data-stu-id="b5f25-187">Stop</span></span>](#stop) | <span data-ttu-id="b5f25-188">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="b5f25-188">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="b5f25-189">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-189">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="b5f25-190">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-190">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="b5f25-191">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-191">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="b5f25-192">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-192">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="b5f25-193">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-193">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="b5f25-194">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-194">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="b5f25-195">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-195">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="b5f25-196">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-196">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="b5f25-197">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="b5f25-197">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="b5f25-198">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="b5f25-198">The title for the current top level document.</span></span>
[<span data-ttu-id="b5f25-199">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="b5f25-199">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="b5f25-200">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-200">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="b5f25-201">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="b5f25-201">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="b5f25-202">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-202">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="b5f25-203">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="b5f25-203">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="b5f25-204">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-204">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="b5f25-205">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-205">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="b5f25-206">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-206">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="b5f25-207">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-207">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="b5f25-208">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-208">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="b5f25-209">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="b5f25-209">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="b5f25-210">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="b5f25-210">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="b5f25-211">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-211">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="b5f25-212">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-212">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="b5f25-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="b5f25-214">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="b5f25-215">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="b5f25-215">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="b5f25-216">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-216">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="b5f25-217">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="b5f25-217">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="b5f25-218">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-218">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="b5f25-219">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-219">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="b5f25-220">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-220">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="b5f25-221">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-221">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="b5f25-222">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-222">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="b5f25-223">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="b5f25-223">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#core_webview2_capture_preview_image_format) | <span data-ttu-id="b5f25-224">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-224">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="b5f25-225">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="b5f25-225">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#core_webview2_script_dialog_kind) | <span data-ttu-id="b5f25-226">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="b5f25-226">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="b5f25-227">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="b5f25-227">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#core_webview2_process_failed_kind) | <span data-ttu-id="b5f25-228">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="b5f25-228">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="b5f25-229">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="b5f25-229">CORE_WEBVIEW2_PERMISSION_KIND</span></span>](#core_webview2_permission_kind) | <span data-ttu-id="b5f25-230">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b5f25-230">The type of a permission request.</span></span>
[<span data-ttu-id="b5f25-231">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="b5f25-231">CORE_WEBVIEW2_PERMISSION_STATE</span></span>](#core_webview2_permission_state) | <span data-ttu-id="b5f25-232">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b5f25-232">Response to a permission request.</span></span>
[<span data-ttu-id="b5f25-233">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="b5f25-233">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span>](#core_webview2_web_error_status) | <span data-ttu-id="b5f25-234">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="b5f25-234">Error status values for web navigations.</span></span>
[<span data-ttu-id="b5f25-235">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="b5f25-235">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#core_webview2_web_resource_context) | <span data-ttu-id="b5f25-236">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="b5f25-236">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="b5f25-237">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="b5f25-237">Navigation events</span></span>

<span data-ttu-id="b5f25-238">Die normale Abfolge von Navigations Ereignissen lautet NavigationStarting, sourced, ContentLoading und dann NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="b5f25-238">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="b5f25-240">Beachten Sie, dass dies für Navigationsereignisse mit dem gleichen Navigations-Event-arg gilt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-240">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="b5f25-241">Navigationsereignisse mit unterschiedlichen Navigations-Event-args können sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-241">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="b5f25-242">Wenn Sie beispielsweise eine Navigation auf das NavigationStarting-Ereignis warten und dann eine andere Navigation starten, sehen Sie die NavigationStarting für die erste Navigation, gefolgt von der NavigationStarting der zweiten Navigation, gefolgt von der NavigationCompleted für die erste Navigation und dann allen anderen geeigneten Navigations Ereignissen für die zweite Navigation.</span><span class="sxs-lookup"><span data-stu-id="b5f25-242">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="b5f25-243">In Fehlerfällen kann es sich um ein ContentLoading-Ereignis handeln, das davon abhängt, ob die Navigation auf einer Fehlerseite fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-243">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="b5f25-244">Im Fall einer HTTP-Umleitung gibt es mehrere NavigationStarting-Ereignisse in einer Zeile, wobei für diejenigen, die dem ersten Folgen, das isredirect-Flag festzulegen ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-244">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="b5f25-245">Verwenden Sie FrameNavigationStarting, um die Navigation innerhalb von unter Frames in der WebView zu überwachen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-245">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="b5f25-246">Prozessmodell</span><span class="sxs-lookup"><span data-stu-id="b5f25-246">Process model</span></span>

<span data-ttu-id="b5f25-247">WebView2 verwendet das gleiche Prozessmodell wie der Edge-Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="b5f25-247">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="b5f25-248">Es gibt einen Edge-Browserprozess pro angegebenen Benutzerdatenverzeichnis in einer Benutzersitzung, die jedem WebView2-Aufrufprozess dient, der das Benutzerdatenverzeichnis angibt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-248">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="b5f25-249">Dies bedeutet, dass ein Edge-Browser-Prozess möglicherweise mehrere Anruf Prozesse bedient, und ein Aufrufprozess möglicherweise mehrere Edge-Browser-Prozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-249">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="b5f25-251">In einem Browserprozess gibt es eine Reihe von Renderer-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-251">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="b5f25-252">Diese werden nach Bedarf erstellt, um potenziell mehrere Frames in verschiedenen Webansichten zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-252">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="b5f25-253">Die Anzahl der Renderer-Prozesse variiert basierend auf dem Feature "Website Isolierungs Browser" und der Anzahl der unterschiedlichen getrennten Ursprünge, die in verknüpften Webansichten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-253">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="b5f25-255">Mithilfe des ProcessFailure-Ereignisses können Sie auf Abstürze reagieren und in diesen Browser-und Renderer-Prozessen hängen bleiben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-255">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="b5f25-256">Sie können zugeordnete Browser-und Renderer-Prozesse mit der Close-Methode sicher Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="b5f25-256">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="b5f25-257">Threadingmodell</span><span class="sxs-lookup"><span data-stu-id="b5f25-257">Threading model</span></span>

<span data-ttu-id="b5f25-258">Der WebView2 muss in einem UI-Thread erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-258">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="b5f25-259">Insbesondere ein Thread mit einer Nachrichten Pumpe.</span><span class="sxs-lookup"><span data-stu-id="b5f25-259">Specifically a thread with a message pump.</span></span> <span data-ttu-id="b5f25-260">Alle Rückrufe werden in diesem Thread ausgeführt, und Aufrufe an die WebView müssen in diesem Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-260">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="b5f25-261">Es ist nicht sicher, die WebView aus einem anderen Thread zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-261">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="b5f25-262">Rückrufe, einschließlich Ereignishandlern und Vervollständigungs Handlern, werden seriell ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-262">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="b5f25-263">Das heißt, wenn Sie einen Ereignishandler ausführen und eine Nachrichtenschleife beginnen, werden keine anderen Ereignishandler oder Abschluss Rückrufe erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-263">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="b5f25-264">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="b5f25-264">Security</span></span>

<span data-ttu-id="b5f25-265">Überprüfen Sie immer die Source-Eigenschaft von WebView, bevor Sie executeScript, PostWebMessageAsJson, PostWebMessageAsString oder eine andere Methode verwenden, um Informationen an die WebView zu senden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-265">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="b5f25-266">Die WebView kann über den Endbenutzer, der mit der Seite oder dem Skript auf der Seite interagiert, die Navigation verursacht hat, zu einer anderen Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="b5f25-266">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="b5f25-267">Achten Sie auf ähnliche Weise auf AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="b5f25-267">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="b5f25-268">Alle zukünftigen Navigationselemente führen dieses Skript aus, und wenn es Zugriff auf Informationen bietet, die nur für einen bestimmten Ursprung vorgesehen sind, kann jedes HTML-Dokumentzugriff haben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-268">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="b5f25-269">Bei der Untersuchung des Ergebnisses eines executeScript-Methodenaufrufs, eines WebMessageReceived-Ereignisses, immer überprüfen der Quelle des Absenders oder eines anderen Mechanismus zum Empfangen von Informationen aus einem HTML-Dokument in einer WebView überprüfen Sie, ob der URI des HTML-Dokuments Ihren Erwartungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b5f25-269">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="b5f25-270">Wenn Sie eine Nachricht erstellen, die Sie in eine WebView senden möchten, verwenden Sie PostWebMessageAsJson, und erstellen Sie den JSON-Zeichenfolgenparameter mithilfe einer JSON-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b5f25-270">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="b5f25-271">Dadurch werden potenzielle Unfälle von Codierungsinformationen in eine JSON-Zeichenfolge oder ein Skript vermieden, und sichergestellt, dass keine von Angreifern gesteuerte Eingabe den restlichen Teil der JSON-Nachricht ändern oder ein beliebiges Skript ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="b5f25-271">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="b5f25-272">Zeichenfolgentypen</span><span class="sxs-lookup"><span data-stu-id="b5f25-272">String types</span></span>

<span data-ttu-id="b5f25-273">Zeichenfolgenparameter sind LPWSTR NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-273">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="b5f25-274">Der aufgerufene ordnet die Zeichenfolge mithilfe von CoTaskMemAlloc zu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-274">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="b5f25-275">Der Besitz wird an den Anrufer übertragen, und es ist dem Anrufer überlassen, den Speicher mit CoTaskMemFree zu befreien.</span><span class="sxs-lookup"><span data-stu-id="b5f25-275">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="b5f25-276">Zeichenfolge in Parametern sind LPCWSTR NULL-terminierte Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-276">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="b5f25-277">Der Aufrufer stellt sicher, dass die Zeichenfolge für die Dauer des synchronen Funktionsaufrufs gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-277">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="b5f25-278">Wenn der aufgerufene diesen Wert nach Abschluss des Funktionsaufrufs bis zu einem gewissen Punkt beibehalten muss, muss der aufgerufene eine eigene Kopie des Zeichenfolgenwerts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-278">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="b5f25-279">URI-und JSON-Analyse</span><span class="sxs-lookup"><span data-stu-id="b5f25-279">URI and JSON parsing</span></span>

<span data-ttu-id="b5f25-280">Verschiedene Methoden stellen URIs und JSON als Zeichenfolgen bereit oder akzeptieren Sie.</span><span class="sxs-lookup"><span data-stu-id="b5f25-280">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="b5f25-281">Verwenden Sie für die Analyse und Generierung dieser Zeichenfolgen ihre eigene bevorzugte Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b5f25-281">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="b5f25-282">Wenn WinRT für Ihre app verfügbar ist, können Sie `RuntimeClass_Windows_Data_Json_JsonObject` JSON-Zeichenfolgen verwenden und erstellen oder URIs analysieren und `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` erstellen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-282">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="b5f25-283">Beide arbeiten in Win32-apps.</span><span class="sxs-lookup"><span data-stu-id="b5f25-283">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="b5f25-284">Wenn Sie IUri und CreateUri zum Analysieren von URIs verwenden, sollten Sie möglicherweise die folgenden URI-Erstellungs Flags verwenden, damit CreateUri-Verhalten der URI-Analyse in der WebView genauer entspricht:</span><span class="sxs-lookup"><span data-stu-id="b5f25-284">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="b5f25-285">Debuggen</span><span class="sxs-lookup"><span data-stu-id="b5f25-285">Debugging</span></span>

<span data-ttu-id="b5f25-286">Öffnen Sie devtools mit den normalen Tastenkombinationen: `F12` oder `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-286">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="b5f25-287">Sie können die `--auto-open-devtools-for-tabs` Befehlsargument Schalter verwenden, um das devtools-Fenster sofort zu öffnen, wenn Sie das erste Mal eine WebView erstellen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-287">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="b5f25-288">Informationen zum Bereitstellen zusätzlicher Befehlszeilenargumente für den Browserprozess finden Sie in der CreateCoreWebView2Host-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b5f25-288">See CreateCoreWebView2Host documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="b5f25-289">Schauen Sie sich den LoaderOverride-Registrierungsschlüssel an, um verschiedene Builds von WebView2 zu testen, ohne die Anwendung in der CreateCoreWebView2Host-Dokumentation zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b5f25-289">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Host documentation.</span></span>

## <span data-ttu-id="b5f25-290">Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="b5f25-290">Versioning</span></span>

<span data-ttu-id="b5f25-291">Nachdem Sie eine bestimmte Version des SDK zum Erstellen Ihrer APP verwendet haben, wird Ihre APP möglicherweise mit einer älteren oder neueren Version der installierten Browser-Binärdateien ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-291">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="b5f25-292">Bis Version 1.0.0.0 von WebView2 können sich während der Updates Änderungen ändern, die verhindern, dass Ihr SDK mit unterschiedlichen Versionen der installierten Browser-Binärdateien funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-292">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="b5f25-293">Nach der Version 1.0.0.0 können verschiedene Versionen des SDKs mit unterschiedlichen Versionen des installierten Browsers funktionieren, indem Sie die folgenden bewährten Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="b5f25-293">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="b5f25-294">Wenn Sie Änderungen an der API berücksichtigen möchten, müssen Sie sicherstellen, dass Sie beim Aufrufen der DLL-Export CreateCoreWebView2Environment und beim Aufrufen von QueryInterface für ein beliebiges CoreWebView2-Objekt auf Fehler überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-294">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="b5f25-295">Ein Rückgabewert von E_NOINTERFACE kann darauf hindeuten, dass das SDK nicht mit den Binärdateien des Edge-Browsers kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-295">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="b5f25-296">Das Überprüfen auf Fehler von QueryInterface berücksichtigt auch Fälle, in denen das SDK neuer als die Version des Edge-Browsers ist und Ihre APP versucht, eine Schnittstelle zu verwenden, von der der Edge-Browser nichts weiß.</span><span class="sxs-lookup"><span data-stu-id="b5f25-296">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="b5f25-297">Wenn eine Schnittstelle nicht zur Verfügung steht, können Sie das zugeordnete Feature nach Möglichkeit deaktivieren oder den Endbenutzer anderweitig darüber informieren, dass Sie den Browser aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-297">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="b5f25-298">Member</span><span class="sxs-lookup"><span data-stu-id="b5f25-298">Members</span></span>

#### <span data-ttu-id="b5f25-299">get_Settings</span><span class="sxs-lookup"><span data-stu-id="b5f25-299">get_Settings</span></span> 

<span data-ttu-id="b5f25-300">Das ICoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für den ausgeführten WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-300">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="b5f25-301">öffentliche HRESULT- [get_Settings](#get_settings)(ICoreWebView2Settings \* \*-Einstellungen)</span><span class="sxs-lookup"><span data-stu-id="b5f25-301">public HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings \*\* settings)</span></span>

#### <span data-ttu-id="b5f25-302">get_Source</span><span class="sxs-lookup"><span data-stu-id="b5f25-302">get_Source</span></span> 

<span data-ttu-id="b5f25-303">Der URI des aktuellen Dokuments auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="b5f25-303">The URI of the current top level document.</span></span>

> <span data-ttu-id="b5f25-304">Public HRESULT [get_Source](#get_source)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="b5f25-304">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="b5f25-305">Dieser Wert ändert sich möglicherweise als Teil der Ereignis Befeuerungs Quelle für einige Fälle, beispielsweise das Navigieren zu einer anderen Website oder zu einer anderen Fragment-Navigation.</span><span class="sxs-lookup"><span data-stu-id="b5f25-305">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="b5f25-306">Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-306">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="b5f25-307">%%amp;quot;Navigate%%amp;quot;
</span><span class="sxs-lookup"><span data-stu-id="b5f25-307">Navigate</span></span> 

<span data-ttu-id="b5f25-308">Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.</span><span class="sxs-lookup"><span data-stu-id="b5f25-308">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="b5f25-309">öffentliche HRESULT- [Navigation](#navigate)(LPCWSTR-URI)</span><span class="sxs-lookup"><span data-stu-id="b5f25-309">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="b5f25-310">Weitere Informationen finden Sie in den Navigations Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-310">See the navigation events for more information.</span></span> <span data-ttu-id="b5f25-311">Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-311">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

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

#### <span data-ttu-id="b5f25-312">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="b5f25-312">NavigateToString</span></span> 

<span data-ttu-id="b5f25-313">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="b5f25-313">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="b5f25-314">Public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="b5f25-314">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="b5f25-315">Der htmlContent-Parameter darf nicht größer als 2 MB Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="b5f25-315">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="b5f25-316">Der Ursprung der neuen Seite lautet: leer.</span><span class="sxs-lookup"><span data-stu-id="b5f25-316">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="b5f25-317">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-317">add_NavigationStarting</span></span> 

<span data-ttu-id="b5f25-318">Fügen Sie einen Ereignishandler für das NavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-318">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="b5f25-319">Public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-319">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-320">NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-320">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="b5f25-321">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b5f25-321">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="b5f25-322">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-322">remove_NavigationStarting</span></span> 

<span data-ttu-id="b5f25-323">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-323">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="b5f25-324">Public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-324">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-325">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="b5f25-325">add_ContentLoading</span></span> 

<span data-ttu-id="b5f25-326">Fügen Sie einen Ereignishandler für das ContentLoading-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-326">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="b5f25-327">Public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-327">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-328">ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden ContentLoading werden nicht ausgelöst, wenn dieselbe Seitennavigation erfolgt (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigation).</span><span class="sxs-lookup"><span data-stu-id="b5f25-328">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="b5f25-329">Dies folgt auf das NavigationStarting-Ereignis und das Source-Ereignis und steht vor den Ereignissen "History" und "NavigationCompleted".</span><span class="sxs-lookup"><span data-stu-id="b5f25-329">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="b5f25-330">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="b5f25-330">remove_ContentLoading</span></span> 

<span data-ttu-id="b5f25-331">Entfernen Sie einen Ereignishandler, der zuvor mit add_ContentLoading hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-331">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="b5f25-332">Public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-332">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-333">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-333">add_SourceChanged</span></span> 

<span data-ttu-id="b5f25-334">Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-334">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="b5f25-335">Public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-335">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-336">Die Quelle wird ausgelöst, um zu einer anderen Website oder zu einer anderen Fragment-Navigation zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="b5f25-336">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="b5f25-337">Sie wird nicht für andere Navigations Typen wie "Seiten-Reload" oder "History. pushState" mit der gleichen URL wie die aktuelle Seite ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b5f25-337">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="b5f25-338">Die Quelle wird vor ContentLoading für die Navigation zu einem neuen Dokument ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b5f25-338">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="b5f25-339">Fügen Sie einen Ereignishandler für das Quellpfad-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-339">Add an event handler for the SourceChanged event.</span></span> 

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

#### <span data-ttu-id="b5f25-340">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-340">remove_SourceChanged</span></span> 

<span data-ttu-id="b5f25-341">Entfernen Sie einen Ereignishandler, der zuvor mit add_SourceChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-341">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="b5f25-342">Public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-342">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-343">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-343">add_HistoryChanged</span></span> 

<span data-ttu-id="b5f25-344">Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="b5f25-344">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="b5f25-345">Public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-345">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-346">Verwenden Sie abrechnungshistorieändern, um zu überprüfen, ob sich get_CanGoBack/get_CanGoForward Wert geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b5f25-346">Use HistoryChange to check if get_CanGoBack/get_CanGoForward value has changed.</span></span> <span data-ttu-id="b5f25-347">"History" wird auch für die Verwendung von GoBack/GoForward ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b5f25-347">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="b5f25-348">"History" wird nach "sourcely" und "ContentLoading" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b5f25-348">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="b5f25-349">Fügen Sie einen Ereignishandler für das History-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-349">Add an event handler for the HistoryChanged event.</span></span> 

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

#### <span data-ttu-id="b5f25-350">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-350">remove_HistoryChanged</span></span> 

<span data-ttu-id="b5f25-351">Entfernen Sie einen Ereignishandler, der zuvor mit add_HistoryChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-351">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="b5f25-352">Public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-352">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-353">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="b5f25-353">add_NavigationCompleted</span></span> 

<span data-ttu-id="b5f25-354">Fügen Sie einen Ereignishandler für das NavigationCompleted-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-354">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="b5f25-355">Public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-355">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-356">Das NavigationCompleted-Ereignis wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-356">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="b5f25-357">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="b5f25-357">remove_NavigationCompleted</span></span> 

<span data-ttu-id="b5f25-358">Entfernen Sie einen Ereignishandler, der zuvor mit add_NavigationCompleted hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-358">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="b5f25-359">Public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-359">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-360">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-360">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="b5f25-361">Fügen Sie einen Ereignishandler für das FrameNavigationStarting-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-361">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="b5f25-362">Public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-362">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-363">FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-363">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="b5f25-364">Dies wird auch für Umleitungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b5f25-364">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="b5f25-365">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="b5f25-365">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="b5f25-366">Entfernen Sie einen Ereignishandler, der zuvor mit add_FrameNavigationStarting hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-366">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="b5f25-367">Public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-367">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-368">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="b5f25-368">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="b5f25-369">Fügen Sie einen Ereignishandler für das ScriptDialogOpening-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-369">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="b5f25-370">Public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-370">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-371">Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung oder Eingabeaufforderung) für die WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-371">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="b5f25-372">Dieses Ereignis wird nur ausgelöst, wenn die ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-372">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="b5f25-373">Das ScriptDialogOpening-Ereignis kann verwendet werden, um Dialogfelder zu unterdrücken oder Standarddialogfelder durch benutzerdefinierte Dialogfelder zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-373">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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

#### <span data-ttu-id="b5f25-374">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="b5f25-374">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="b5f25-375">Entfernen Sie einen Ereignishandler, der zuvor mit add_ScriptDialogOpening hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-375">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="b5f25-376">Public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-376">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-377">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-377">add_PermissionRequested</span></span> 

<span data-ttu-id="b5f25-378">Fügen Sie einen Ereignishandler für das PermissionRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-378">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="b5f25-379">Public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-379">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-380">Wird ausgelöst, wenn Inhalt in einer WebView-Anforderung die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-380">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="b5f25-381">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-381">remove_PermissionRequested</span></span> 

<span data-ttu-id="b5f25-382">Entfernen Sie einen Ereignishandler, der zuvor mit add_PermissionRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-382">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="b5f25-383">Public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-383">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-384">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="b5f25-384">add_ProcessFailed</span></span> 

<span data-ttu-id="b5f25-385">Fügen Sie einen Ereignishandler für das ProcessFailed-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-385">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="b5f25-386">Public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-386">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-387">Wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-387">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="b5f25-388">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="b5f25-388">remove_ProcessFailed</span></span> 

<span data-ttu-id="b5f25-389">Entfernen Sie einen Ereignishandler, der zuvor mit add_ProcessFailed hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-389">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="b5f25-390">Public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-390">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-391">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="b5f25-391">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="b5f25-392">Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-392">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="b5f25-393">Public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="b5f25-393">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="b5f25-394">Das eingefügte Skript gilt für alle zukünftigen Dokumente und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie mit RemoveScriptToExecuteOnDocumentCreated entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-394">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="b5f25-395">Diese wird asynchron angewendet, und Sie müssen warten, bis der vervollständigungshandler ausgeführt wird, bevor Sie sicher sein können, dass das Skript für zukünftige Navigationen ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5f25-395">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="b5f25-396">Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat.</span><span class="sxs-lookup"><span data-stu-id="b5f25-396">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="b5f25-397">Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-397">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="b5f25-398">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="b5f25-398">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="b5f25-399">Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-399">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="b5f25-400">Public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR-ID)</span><span class="sxs-lookup"><span data-stu-id="b5f25-400">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="b5f25-401">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="b5f25-401">ExecuteScript</span></span> 

<span data-ttu-id="b5f25-402">Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-402">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="b5f25-403">Public HRESULT [executeScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="b5f25-403">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="b5f25-404">Dies wird asynchron ausgeführt, und wenn ein Handler im ExecuteScriptCompletedHandler-Parameter bereitgestellt wird, wird die Invoke-Methode mit dem Ergebnis der Auswertung des bereitgestellten JavaScript aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-404">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="b5f25-405">Der Ergebniswert ist eine JSON-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b5f25-405">The result value is a JSON encoded string.</span></span> <span data-ttu-id="b5f25-406">Wenn das Ergebnis undefiniert ist, einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird der JSON-NULL-Wert als Zeichenfolge "Null" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-406">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="b5f25-407">Beachten Sie, dass eine Funktion, die keinen expliziten Rückgabewert aufweist, undefined zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-407">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="b5f25-408">Wenn das ausgeführte Skript eine nicht behandelte Ausnahme auslöst, ist das Ergebnis auch "Null".</span><span class="sxs-lookup"><span data-stu-id="b5f25-408">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="b5f25-409">Diese Methode wird asynchron angewendet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-409">This method is applied asynchronously.</span></span> <span data-ttu-id="b5f25-410">Wenn der Aufruf erfolgt, während sich die WebView in einem Dokument befindet und eine Navigation nach dem Aufruf erfolgt, aber bevor das JavaScript ausgeführt wird, wird das Skript nicht ausgeführt, und der Handler wird mit E_FAIL für seinen errorCode-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-410">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="b5f25-411">ExecuteScript funktioniert auch dann, wenn IsScriptEnabled auf "false" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-411">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="b5f25-412">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="b5f25-412">CapturePreview</span></span> 

<span data-ttu-id="b5f25-413">Erfassen Sie ein Bild von der Anzeige von WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-413">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="b5f25-414">Public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) Image Format, IStream \* ImageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \*-Handler)</span><span class="sxs-lookup"><span data-stu-id="b5f25-414">public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="b5f25-415">Geben Sie das Format des Bilds mit dem ImageFormat-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="b5f25-415">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="b5f25-416">Die resultierenden Bild Binärdaten werden in den bereitgestellten ImageStream-Parameter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-416">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="b5f25-417">Wenn CapturePreview den Schreibvorgang in den Datenstrom abgeschlossen hat, wird die Invoke-Methode für den bereitgestellten Handler-Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-417">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="b5f25-418">Laden</span><span class="sxs-lookup"><span data-stu-id="b5f25-418">Reload</span></span> 

<span data-ttu-id="b5f25-419">Laden Sie die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-419">Reload the current page.</span></span>

> <span data-ttu-id="b5f25-420">Public HRESULT [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="b5f25-420">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="b5f25-421">Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren.</span><span class="sxs-lookup"><span data-stu-id="b5f25-421">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="b5f25-422">Das zurück/weiter-Protokoll wird jedoch nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-422">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="b5f25-423">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="b5f25-423">PostWebMessageAsJson</span></span> 

<span data-ttu-id="b5f25-424">Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-424">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="b5f25-425">Public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="b5f25-425">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="b5f25-426">Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b5f25-426">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="b5f25-427">JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen:</span><span class="sxs-lookup"><span data-stu-id="b5f25-427">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="b5f25-428">Das Ereignis args ist eine Instanz von `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-428">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="b5f25-429">Die ICoreWebView2Settings:: IsWebMessageEnabled-Einstellung muss wahr sein, oder diese Methode schlägt mit E_INVALIDARG fehl.</span><span class="sxs-lookup"><span data-stu-id="b5f25-429">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="b5f25-430">Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-430">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="b5f25-431">Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-431">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="b5f25-432">Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter SetWebMessageReceivedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="b5f25-432">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="b5f25-433">Diese Nachricht wird asynchron gesendet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-433">This message is sent asynchronously.</span></span> <span data-ttu-id="b5f25-434">Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-434">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="b5f25-435">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="b5f25-435">PostWebMessageAsString</span></span> 

<span data-ttu-id="b5f25-436">Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-436">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="b5f25-437">Public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="b5f25-437">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="b5f25-438">Dies verhält sich auf die gleiche Weise wie PostWebMessageAsJson, aber die `window.chrome.webview` Dateneigenschaft des Nachrichtenereignisses arg ist eine Zeichenfolge mit dem gleichen Wert wie webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="b5f25-438">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="b5f25-439">Verwenden Sie diese anstelle von PostWebMessageAsJson, wenn Sie über einfache Zeichenfolgen anstelle von JSON-Objekten kommunizieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b5f25-439">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="b5f25-440">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="b5f25-440">add_WebMessageReceived</span></span> 

<span data-ttu-id="b5f25-441">Dieses Ereignis wird ausgelöst, wenn die IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-441">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="b5f25-442">öffentliche HRESULT- [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \*-Handler, EventRegistrationToken \*-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-442">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-443">Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-443">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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

 <span data-ttu-id="b5f25-444">Wenn PostMessage aufgerufen wird, wird der [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) -Satz über diese SetWebMessageReceivedEventHandler-Methode aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-444">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="b5f25-445">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="b5f25-445">remove_WebMessageReceived</span></span> 

<span data-ttu-id="b5f25-446">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebMessageReceived hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-446">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="b5f25-447">Public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-447">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-448">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="b5f25-448">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="b5f25-449">Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b5f25-449">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="b5f25-450">Public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR MethodName, LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* Handler)</span><span class="sxs-lookup"><span data-stu-id="b5f25-450">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="b5f25-451">Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="b5f25-451">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="b5f25-452">Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-452">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="b5f25-453">Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="b5f25-453">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="b5f25-454">Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-454">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="b5f25-455">Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-455">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="b5f25-456">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="b5f25-456">get_BrowserProcessId</span></span> 

<span data-ttu-id="b5f25-457">Die Prozess-ID des Browser Prozesses, der die WebView hostet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-457">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="b5f25-458">Public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UInt32 \*-Wert)</span><span class="sxs-lookup"><span data-stu-id="b5f25-458">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="b5f25-459">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="b5f25-459">get_CanGoBack</span></span> 

<span data-ttu-id="b5f25-460">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="b5f25-460">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="b5f25-461">Public HRESULT [get_CanGoBack](#get_cangoback)(bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="b5f25-461">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="b5f25-462">Das History-Ereignis wird ausgelöst, wenn der Wert von get_CanGoBack geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-462">The HistoryChanged event will fire if get_CanGoBack changes value.</span></span>

#### <span data-ttu-id="b5f25-463">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="b5f25-463">get_CanGoForward</span></span> 

<span data-ttu-id="b5f25-464">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="b5f25-464">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="b5f25-465">Public HRESULT [get_CanGoForward](#get_cangoforward)(bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="b5f25-465">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="b5f25-466">Das History-Ereignis wird ausgelöst, wenn der Wert von get_CanGoForward geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-466">The HistoryChanged event will fire if get_CanGoForward changes value.</span></span>

#### <span data-ttu-id="b5f25-467">GoBack</span><span class="sxs-lookup"><span data-stu-id="b5f25-467">GoBack</span></span> 

<span data-ttu-id="b5f25-468">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="b5f25-468">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="b5f25-469">Public HRESULT [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="b5f25-469">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="b5f25-470">GoForward</span><span class="sxs-lookup"><span data-stu-id="b5f25-470">GoForward</span></span> 

<span data-ttu-id="b5f25-471">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="b5f25-471">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="b5f25-472">Public HRESULT [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="b5f25-472">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="b5f25-473">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="b5f25-473">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="b5f25-474">Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="b5f25-474">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="b5f25-475">Public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR EventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="b5f25-475">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="b5f25-476">Der eventName-Parameter ist der vollständige Name des Ereignisses im Format `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-476">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="b5f25-477">Eine Liste der Beschreibungen von devtools-Protokollereignissen und Ereignis args finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) .</span><span class="sxs-lookup"><span data-stu-id="b5f25-477">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="b5f25-478">Stop</span><span class="sxs-lookup"><span data-stu-id="b5f25-478">Stop</span></span> 

<span data-ttu-id="b5f25-479">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="b5f25-479">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="b5f25-480">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="b5f25-480">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="b5f25-481">Skripts werden nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="b5f25-481">Does not stop scripts.</span></span>

#### <span data-ttu-id="b5f25-482">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-482">add_NewWindowRequested</span></span> 

<span data-ttu-id="b5f25-483">Fügen Sie einen Ereignishandler für das mswebviewnewwindowrequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-483">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="b5f25-484">Public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-484">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-485">Wird ausgelöst, wenn der Inhalt in der WebView zum Öffnen eines neuen Fensters angefordert wird, beispielsweisedurch Window. Open.</span><span class="sxs-lookup"><span data-stu-id="b5f25-485">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="b5f25-486">Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-486">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="b5f25-487">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-487">remove_NewWindowRequested</span></span> 

<span data-ttu-id="b5f25-488">Entfernen Sie einen Ereignishandler, der zuvor mit add_NewWindowRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-488">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="b5f25-489">Public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-489">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-490">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-490">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="b5f25-491">Fügen Sie einen Ereignishandler für das DocumentTitleChanged-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-491">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="b5f25-492">Public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-492">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-493">Das Ereignis wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-493">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="b5f25-494">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-494">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="b5f25-495">Entfernen Sie einen Ereignishandler, der zuvor mit add_DocumentTitleChanged hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-495">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="b5f25-496">Public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-496">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-497">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="b5f25-497">get_DocumentTitle</span></span> 

<span data-ttu-id="b5f25-498">Der Titel für das aktuelle Dokument der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="b5f25-498">The title for the current top level document.</span></span>

> <span data-ttu-id="b5f25-499">öffentliche HRESULT- [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="b5f25-499">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="b5f25-500">Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-500">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="b5f25-501">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="b5f25-501">AddRemoteObject</span></span> 

<span data-ttu-id="b5f25-502">Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-502">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="b5f25-503">Public HRESULT [addremoteobject](#addremoteobject)(LPCWSTR-Name, Variant \*-Objekt)</span><span class="sxs-lookup"><span data-stu-id="b5f25-503">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="b5f25-504">Host Objekte werden als Remoteobjekt Proxys über bereitgestellt `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-504">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="b5f25-505">Remote Objektproxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-505">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="b5f25-506">Das Versprechen wird abgelehnt, wenn die APP kein Objekt mit dem Namen hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="b5f25-506">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="b5f25-507">Wenn JavaScript-Code auf eine Eigenschaft oder Methode des Objekts zugreift, wird eine Zusage zurückgegeben, die in den Wert aufgelöst wird, der vom Host für die Eigenschaft oder Methode zurückgegeben wird, oder im Fall eines Fehlers abgelehnt wird, beispielsweise wenn keine solche Eigenschaft oder Methode für das Objekt vorhanden ist oder Parameter ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="b5f25-507">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="b5f25-508">Wenn der Anwendungscode beispielsweise Folgendes durchführt:</span><span class="sxs-lookup"><span data-stu-id="b5f25-508">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="b5f25-509">JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen:</span><span class="sxs-lookup"><span data-stu-id="b5f25-509">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="b5f25-510">Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-510">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="b5f25-511">Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-511">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="b5f25-512">Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-512">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="b5f25-513">Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-513">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="b5f25-514">Arrays von nach Verweistypen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-514">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="b5f25-515">VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-515">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="b5f25-516">In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b5f25-516">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="b5f25-517">Darüber hinaus werden alle Remoteobjekte als verfügbar gemacht `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-517">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="b5f25-518">Hier werden die Hostobjekte als synchrone Remoteobjekt Proxys verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b5f25-518">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="b5f25-519">Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="b5f25-519">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="b5f25-520">Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.remoteObjects.<name>` API verwenden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-520">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="b5f25-521">Synchrone Remoteobjekt Proxys und asynchrone Remoteobjekt Proxys können sowohl Proxys für dasselbe Remoteobjekt als auch Proxys sein.</span><span class="sxs-lookup"><span data-stu-id="b5f25-521">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="b5f25-522">Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Remoteobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.</span><span class="sxs-lookup"><span data-stu-id="b5f25-522">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="b5f25-523">Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-523">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="b5f25-524">Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.</span><span class="sxs-lookup"><span data-stu-id="b5f25-524">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="b5f25-525">Remote Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-525">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="b5f25-526">Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-526">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="b5f25-527">Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.remoteObjects.options.forceLocalProperties` lokal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-527">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="b5f25-528">Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-528">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="b5f25-529">Sie können diesem Array nach Bedarf weitere hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-529">You can add more to this array as required.</span></span>

<span data-ttu-id="b5f25-530">Es gibt eine Methode `chrome.webview.remoteObjects.cleanupSome` , mit der die Garbage Collection von Remoteobjekt Proxys am besten abläuft.</span><span class="sxs-lookup"><span data-stu-id="b5f25-530">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="b5f25-531">Für Remote Objektproxys gibt es zusätzlich die folgenden Methoden, die lokal ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b5f25-531">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="b5f25-532">applyRemote, getRemote, setremote: Durchführen eines Methodenaufrufs, eines Eigenschaften Abstands oder eines Eigenschaftssatzes für das Remoteobjekt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-532">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="b5f25-533">Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-533">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="b5f25-534">Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="b5f25-534">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="b5f25-535">`proxy.applyRemote('toString')`Wird aber `toString` stattdessen auf dem Remoteproxy Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-535">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="b5f25-536">getLocal, setlocal: führt Eigenschaften abrufen oder Eigenschaftssatz lokal aus.</span><span class="sxs-lookup"><span data-stu-id="b5f25-536">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="b5f25-537">Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Remoteobjekt Proxy selbst und nicht für das Remoteobjekt zu erzwingen, das es darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-537">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="b5f25-538">Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Remoteproxy Objekt benannt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-538">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="b5f25-539">`proxy.getLocal('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-539">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="b5f25-540">Synchronisierung: asynchrone Remoteobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die ein Versprechen für einen synchronen Remoteobjekt Proxy für das gleiche Remoteobjekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-540">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="b5f25-541">Gibt beispielsweise `chrome.webview.remoteObjects.sample.methodCall()` einen asynchronen Remoteobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="b5f25-541">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="b5f25-542">Sie können stattdessen die `sync` Methode zum Abrufen eines synchronen Remoteobjekt Proxys verwenden:</span><span class="sxs-lookup"><span data-stu-id="b5f25-542">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="b5f25-543">Async: synchrone Remoteobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Remoteobjekt Proxy für das gleiche Remoteobjekt blockiert und zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-543">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="b5f25-544">Gibt beispielsweise `chrome.webview.remoteObjects.sync.sample.methodCall()` einen synchronen Remoteobjekt Proxy zurück.</span><span class="sxs-lookup"><span data-stu-id="b5f25-544">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="b5f25-545">Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Remoteobjekt Proxys für dasselbe Remoteobjekt:</span><span class="sxs-lookup"><span data-stu-id="b5f25-545">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="b5f25-546">dann: asynchrone Remoteobjekt Proxys verfügen über eine then-Methode.</span><span class="sxs-lookup"><span data-stu-id="b5f25-546">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="b5f25-547">Auf diese Weise können Sie warten.</span><span class="sxs-lookup"><span data-stu-id="b5f25-547">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="b5f25-548">gibt eine Verheißung zurück, die mit einer Darstellung des Remoteobjekts aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-548">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="b5f25-549">Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-549">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="b5f25-550">Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-550">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="b5f25-551">Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Remoteobjekt Proxys zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-551">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="b5f25-552">Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-552">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="b5f25-553">Asynchrone Remoteobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-553">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="b5f25-554">Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-554">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="b5f25-555">Synchrone Remoteobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-555">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="b5f25-556">Das Festlegen einer Eigenschaft für einen asynchronen Remoteobjekt Proxy funktioniert etwas anders.</span><span class="sxs-lookup"><span data-stu-id="b5f25-556">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="b5f25-557">Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-557">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="b5f25-558">Dies ist eine Anforderung des JavaScript-Proxy Objekts.</span><span class="sxs-lookup"><span data-stu-id="b5f25-558">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="b5f25-559">Wenn Sie asynchron warten müssen, bis die Eigenschaft auf Complete gesetzt ist, verwenden Sie die setremote-Methode, die eine Verheißung zurückgibt, wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-559">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="b5f25-560">Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-560">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="b5f25-561">Angenommen, Sie verfügen über ein COM-Objekt mit der folgenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5f25-561">For example, suppose you have a COM object with the following interface</span></span>

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

 <span data-ttu-id="b5f25-562">Wir können eine Instanz dieser Schnittstelle in unserem JavaScript mit hinzufügen `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="b5f25-562">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="b5f25-563">In diesem Fall nennen wir `sample` Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b5f25-563">In this case we name it `sample`:</span></span>

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

 <span data-ttu-id="b5f25-564">Im HTML-Dokument können wir dieses COM-Objekt dann über `chrome.webview.remoteObjects.sample` Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="b5f25-564">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

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

#### <span data-ttu-id="b5f25-565">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="b5f25-565">RemoveRemoteObject</span></span> 

<span data-ttu-id="b5f25-566">Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-566">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="b5f25-567">Public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="b5f25-567">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="b5f25-568">Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-568">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="b5f25-569">Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="b5f25-569">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="b5f25-570">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="b5f25-570">OpenDevToolsWindow</span></span> 

<span data-ttu-id="b5f25-571">Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.</span><span class="sxs-lookup"><span data-stu-id="b5f25-571">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="b5f25-572">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="b5f25-572">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="b5f25-573">Wenn das devtools-Fenster bereits geöffnet ist, wird nichts aufgerufen</span><span class="sxs-lookup"><span data-stu-id="b5f25-573">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="b5f25-574">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-574">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="b5f25-575">Benachrichtigt, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-575">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="b5f25-576">Public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-576">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-577">Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-577">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="b5f25-578">Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-578">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="b5f25-579">Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.</span><span class="sxs-lookup"><span data-stu-id="b5f25-579">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="b5f25-580">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="b5f25-580">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="b5f25-581">Entfernen Sie einen Ereignishandler, der zuvor mit der entsprechenden add_-Ereignismethode hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-581">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="b5f25-582">Public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-582">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-583">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="b5f25-583">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="b5f25-584">Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="b5f25-584">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="b5f25-585">Public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="b5f25-585">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="b5f25-586">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-586">add_WebResourceRequested</span></span> 

<span data-ttu-id="b5f25-587">Fügen Sie einen Ereignishandler für das WebResourceRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-587">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="b5f25-588">Public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-588">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-589">Wird ausgelöst, wenn die WebView eine HTTP-Anforderung an einen übereinstimmenden URL-und Ressourcenkontext Filter ausführt, der mit AddWebResourceRequestedFilter hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-589">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="b5f25-590">Es muss mindestens ein Filter hinzugefügt werden, damit das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-590">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="b5f25-591">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-591">remove_WebResourceRequested</span></span> 

<span data-ttu-id="b5f25-592">Entfernen Sie einen Ereignishandler, der zuvor mit add_WebResourceRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-592">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="b5f25-593">Public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-593">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-594">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="b5f25-594">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="b5f25-595">Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-595">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="b5f25-596">Public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const URI,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="b5f25-596">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="b5f25-597">Der URI-Parameter kann eine Platzhalterzeichenfolge (' ': 0 oder mehr; '? ': genau eins) sein.</span><span class="sxs-lookup"><span data-stu-id="b5f25-597">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="b5f25-598">nullptr entspricht L "".</span><span class="sxs-lookup"><span data-stu-id="b5f25-598">nullptr is equivalent to L"".</span></span> <span data-ttu-id="b5f25-599">Eine Beschreibung der Ressourcenkontext Filter finden Sie unter CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="b5f25-599">See CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="b5f25-600">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="b5f25-600">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="b5f25-601">Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-601">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="b5f25-602">Public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const URI,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="b5f25-602">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="b5f25-603">Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-603">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="b5f25-604">Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-604">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="b5f25-605">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-605">add_WindowCloseRequested</span></span> 

<span data-ttu-id="b5f25-606">Fügen Sie einen Ereignishandler für das WindowCloseRequested-Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5f25-606">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="b5f25-607">Public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-607">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="b5f25-608">Wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close.</span><span class="sxs-lookup"><span data-stu-id="b5f25-608">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="b5f25-609">Die APP sollte das Fenster WebView und verwandte APP schließen, wenn dies für die APP sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="b5f25-609">The app should close the WebView and related app window if that makes sense to the app.</span></span>

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

#### <span data-ttu-id="b5f25-610">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="b5f25-610">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="b5f25-611">Entfernen Sie einen Ereignishandler, der zuvor mit add_WindowCloseRequested hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-611">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="b5f25-612">Public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken-Token)</span><span class="sxs-lookup"><span data-stu-id="b5f25-612">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="b5f25-613">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="b5f25-613">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="b5f25-614">Bildformat, das von der ICoreWebView2:: CapturePreview-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-614">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="b5f25-615">Enum- [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span><span class="sxs-lookup"><span data-stu-id="b5f25-615">enum [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="b5f25-616">Werte</span><span class="sxs-lookup"><span data-stu-id="b5f25-616">Values</span></span>                         | <span data-ttu-id="b5f25-617">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-617">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b5f25-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="b5f25-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="b5f25-619">PNG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="b5f25-619">PNG image format.</span></span>
<span data-ttu-id="b5f25-620">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="b5f25-620">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="b5f25-621">JPEG-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="b5f25-621">JPEG image format.</span></span>

#### <span data-ttu-id="b5f25-622">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="b5f25-622">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="b5f25-623">Art des in der ICoreWebView2ScriptDialogOpeningEventHandler-Schnittstelle verwendeten JavaScript-Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="b5f25-623">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="b5f25-624">Enum- [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span><span class="sxs-lookup"><span data-stu-id="b5f25-624">enum [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="b5f25-625">Werte</span><span class="sxs-lookup"><span data-stu-id="b5f25-625">Values</span></span>                         | <span data-ttu-id="b5f25-626">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-626">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b5f25-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="b5f25-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="b5f25-628">Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-628">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="b5f25-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="b5f25-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="b5f25-630">Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-630">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="b5f25-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="b5f25-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="b5f25-632">Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-632">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="b5f25-633">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="b5f25-633">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="b5f25-634">Ein Dialogfeld, das über das beforeunload-JavaScript-Ereignis aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5f25-634">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="b5f25-635">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="b5f25-635">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="b5f25-636">Art des in der ICoreWebView2ProcessFailedEventHandler-Schnittstelle verwendeten Prozess Fehlers.</span><span class="sxs-lookup"><span data-stu-id="b5f25-636">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="b5f25-637">Enum- [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span><span class="sxs-lookup"><span data-stu-id="b5f25-637">enum [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span></span>

 <span data-ttu-id="b5f25-638">Werte</span><span class="sxs-lookup"><span data-stu-id="b5f25-638">Values</span></span>                         | <span data-ttu-id="b5f25-639">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-639">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b5f25-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="b5f25-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="b5f25-641">Gibt an, dass der Browserprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-641">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="b5f25-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="b5f25-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="b5f25-643">Gibt an, dass der Renderprozess unerwartet beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b5f25-643">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="b5f25-644">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="b5f25-644">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="b5f25-645">Gibt an, dass der Renderprozess nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-645">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="b5f25-646">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="b5f25-646">CORE_WEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="b5f25-647">Der Typ einer Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b5f25-647">The type of a permission request.</span></span>

> <span data-ttu-id="b5f25-648">Enum- [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span><span class="sxs-lookup"><span data-stu-id="b5f25-648">enum [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span></span>

 <span data-ttu-id="b5f25-649">Werte</span><span class="sxs-lookup"><span data-stu-id="b5f25-649">Values</span></span>                         | <span data-ttu-id="b5f25-650">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-650">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b5f25-651">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="b5f25-651">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="b5f25-652">Unbekannte Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="b5f25-652">Unknown permission.</span></span>
<span data-ttu-id="b5f25-653">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="b5f25-653">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="b5f25-654">Berechtigung zum Aufzeichnen von Audio.</span><span class="sxs-lookup"><span data-stu-id="b5f25-654">Permission to capture audio.</span></span>
<span data-ttu-id="b5f25-655">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="b5f25-655">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="b5f25-656">Berechtigung zum Aufzeichnen von Videos.</span><span class="sxs-lookup"><span data-stu-id="b5f25-656">Permission to capture video.</span></span>
<span data-ttu-id="b5f25-657">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="b5f25-657">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="b5f25-658">Berechtigung für den Zugriff auf Geolocation.</span><span class="sxs-lookup"><span data-stu-id="b5f25-658">Permission to access geolocation.</span></span>
<span data-ttu-id="b5f25-659">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="b5f25-659">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="b5f25-660">Berechtigung zum Senden von webbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-660">Permission to send web notifications.</span></span>
<span data-ttu-id="b5f25-661">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="b5f25-661">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="b5f25-662">Berechtigung für den Zugriff auf den generischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="b5f25-662">Permission to access generic sensor.</span></span>
<span data-ttu-id="b5f25-663">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="b5f25-663">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="b5f25-664">Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste</span><span class="sxs-lookup"><span data-stu-id="b5f25-664">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="b5f25-665">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="b5f25-665">CORE_WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="b5f25-666">Antwort auf eine Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b5f25-666">Response to a permission request.</span></span>

> <span data-ttu-id="b5f25-667">Enum- [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span><span class="sxs-lookup"><span data-stu-id="b5f25-667">enum [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span></span>

 <span data-ttu-id="b5f25-668">Werte</span><span class="sxs-lookup"><span data-stu-id="b5f25-668">Values</span></span>                         | <span data-ttu-id="b5f25-669">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-669">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b5f25-670">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b5f25-670">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="b5f25-671">Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.</span><span class="sxs-lookup"><span data-stu-id="b5f25-671">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="b5f25-672">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="b5f25-672">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="b5f25-673">Erteilen Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b5f25-673">Grant the permission request.</span></span>
<span data-ttu-id="b5f25-674">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="b5f25-674">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="b5f25-675">Verweigern Sie die Berechtigungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b5f25-675">Deny the permission request.</span></span>

#### <span data-ttu-id="b5f25-676">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="b5f25-676">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="b5f25-677">Fehlerstatus Werte für Web-Navigationselemente.</span><span class="sxs-lookup"><span data-stu-id="b5f25-677">Error status values for web navigations.</span></span>

> <span data-ttu-id="b5f25-678">Enum- [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span><span class="sxs-lookup"><span data-stu-id="b5f25-678">enum [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span></span>

 <span data-ttu-id="b5f25-679">Werte</span><span class="sxs-lookup"><span data-stu-id="b5f25-679">Values</span></span>                         | <span data-ttu-id="b5f25-680">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-680">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b5f25-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="b5f25-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="b5f25-682">Ein unbekannter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b5f25-682">An unknown error occurred.</span></span>
<span data-ttu-id="b5f25-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="b5f25-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="b5f25-684">Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.</span><span class="sxs-lookup"><span data-stu-id="b5f25-684">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="b5f25-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="b5f25-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="b5f25-686">Das SSL-Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-686">The SSL certificate has expired.</span></span>
<span data-ttu-id="b5f25-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b5f25-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="b5f25-688">Das SSL-Clientzertifikat enthält Fehler.</span><span class="sxs-lookup"><span data-stu-id="b5f25-688">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="b5f25-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="b5f25-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="b5f25-690">Das SSL-Zertifikat wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-690">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="b5f25-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="b5f25-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="b5f25-692">Das SSL-Zertifikat ist ungültig &ndash; Dies könnte bedeuten, dass das Zertifikat nicht mit den öffentlichen Schlüssel Pins für den Hostnamen übereinstimmte. das Zertifikat wird von einer nicht vertrauenswürdigen Zertifizierungsstelle signiert oder mit einem schwachen Vorzeichen Algorithmus, das Zertifikat behauptet, dass DNS-Namen gegen Namenseinschränkungen verstoßen, das Zertifikat einen schwachen Schlüssel enthält, der Gültigkeitszeitraum des Zertifikats zu lang ist, fehlender Sperrungsinformationen oder Sperrungs Mechanismus, nicht eindeutiger [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)Hostname, fehlender Zertifikat Transparenzinformationen oder das Zertifikat an</span><span class="sxs-lookup"><span data-stu-id="b5f25-692">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="b5f25-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="b5f25-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="b5f25-694">Der Host ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="b5f25-694">The host is unreachable.</span></span>
<span data-ttu-id="b5f25-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b5f25-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="b5f25-696">Die Verbindung hat ein Zeitlimit überschritten.</span><span class="sxs-lookup"><span data-stu-id="b5f25-696">The connection has timed out.</span></span>
<span data-ttu-id="b5f25-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="b5f25-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="b5f25-698">Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5f25-698">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="b5f25-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="b5f25-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="b5f25-700">Die Verbindung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-700">The connection was aborted.</span></span>
<span data-ttu-id="b5f25-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="b5f25-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="b5f25-702">Die Verbindung wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b5f25-702">The connection was reset.</span></span>
<span data-ttu-id="b5f25-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="b5f25-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="b5f25-704">Die Internet Verbindung wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-704">The Internet connection has been lost.</span></span>
<span data-ttu-id="b5f25-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="b5f25-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="b5f25-706">Verbindung mit Ziel kann nicht hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-706">Cannot connect to destination.</span></span>
<span data-ttu-id="b5f25-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="b5f25-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="b5f25-708">Der angegebene Hostname konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="b5f25-708">Could not resolve provided host name.</span></span>
<span data-ttu-id="b5f25-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="b5f25-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="b5f25-710">Der Vorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-710">The operation was canceled.</span></span>
<span data-ttu-id="b5f25-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="b5f25-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="b5f25-712">Die Anforderungs Umleitung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-712">The request redirect failed.</span></span>
<span data-ttu-id="b5f25-713">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="b5f25-713">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="b5f25-714">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b5f25-714">An unexpected error occurred.</span></span>

#### <span data-ttu-id="b5f25-715">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="b5f25-715">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="b5f25-716">Enum für Webressourcen-anforderungskontexte.</span><span class="sxs-lookup"><span data-stu-id="b5f25-716">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="b5f25-717">Enum- [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span><span class="sxs-lookup"><span data-stu-id="b5f25-717">enum [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span></span>

 <span data-ttu-id="b5f25-718">Werte</span><span class="sxs-lookup"><span data-stu-id="b5f25-718">Values</span></span>                         | <span data-ttu-id="b5f25-719">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b5f25-719">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="b5f25-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="b5f25-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="b5f25-721">Alle Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-721">All resources.</span></span>
<span data-ttu-id="b5f25-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="b5f25-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="b5f25-723">Dokument Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-723">Document resources.</span></span>
<span data-ttu-id="b5f25-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="b5f25-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="b5f25-725">CSS-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-725">CSS resources.</span></span>
<span data-ttu-id="b5f25-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="b5f25-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="b5f25-727">Bildressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-727">Image resources.</span></span>
<span data-ttu-id="b5f25-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="b5f25-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="b5f25-729">Andere Medienressourcen wie Videos.</span><span class="sxs-lookup"><span data-stu-id="b5f25-729">Other media resources such as videos.</span></span>
<span data-ttu-id="b5f25-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="b5f25-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="b5f25-731">Schriftartressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-731">Font resources.</span></span>
<span data-ttu-id="b5f25-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="b5f25-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="b5f25-733">Skriptressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-733">Script resources.</span></span>
<span data-ttu-id="b5f25-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="b5f25-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="b5f25-735">XML-HTTP-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-735">XML HTTP requests.</span></span>
<span data-ttu-id="b5f25-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="b5f25-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="b5f25-737">Abrufen der API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="b5f25-737">Fetch API communication.</span></span>
<span data-ttu-id="b5f25-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="b5f25-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="b5f25-739">Texttracking-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-739">TextTrack resources.</span></span>
<span data-ttu-id="b5f25-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b5f25-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="b5f25-741">EventSource-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="b5f25-741">EventSource API communication.</span></span>
<span data-ttu-id="b5f25-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="b5f25-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="b5f25-743">WebSocket-API-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="b5f25-743">WebSocket API communication.</span></span>
<span data-ttu-id="b5f25-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="b5f25-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="b5f25-745">Web App-Manifeste</span><span class="sxs-lookup"><span data-stu-id="b5f25-745">Web App Manifests.</span></span>
<span data-ttu-id="b5f25-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="b5f25-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="b5f25-747">Signierte http-Exchanges.</span><span class="sxs-lookup"><span data-stu-id="b5f25-747">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="b5f25-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="b5f25-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="b5f25-749">Ping-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-749">Ping requests.</span></span>
<span data-ttu-id="b5f25-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="b5f25-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="b5f25-751">Berichte zu CSP-Verstößen</span><span class="sxs-lookup"><span data-stu-id="b5f25-751">CSP Violation Reports.</span></span>
<span data-ttu-id="b5f25-752">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="b5f25-752">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="b5f25-753">Andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5f25-753">Other resources.</span></span>
