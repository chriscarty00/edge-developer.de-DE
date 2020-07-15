---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. WinForms. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. WinForms. WebView2
ms.openlocfilehash: 7d707c2a6ecb8127074735f06ba6d4f1f28eea0c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879450"
---
# <span data-ttu-id="2dc53-104">Microsoft. Web. WebView2. WinForms. WebView2 Klasse</span><span class="sxs-lookup"><span data-stu-id="2dc53-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="2dc53-105">Namespace: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="2dc53-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="2dc53-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span><span class="sxs-lookup"><span data-stu-id="2dc53-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="2dc53-107">Steuerelement zum Einbetten von WebView2 in WinForms</span><span class="sxs-lookup"><span data-stu-id="2dc53-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="2dc53-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2dc53-108">Summary</span></span>

 <span data-ttu-id="2dc53-109">Member</span><span class="sxs-lookup"><span data-stu-id="2dc53-109">Members</span></span>                        | <span data-ttu-id="2dc53-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2dc53-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2dc53-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="2dc53-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="2dc53-112">ContentLoading wird nach dem Beginn einer Navigation zu einem neuen URI und dem Rendern des Inhalts dieses URIs ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2dc53-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="2dc53-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="2dc53-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="2dc53-114">Dieses Ereignis wird ausgelöst, wenn die [CoreWebView2](#corewebview2) des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dc53-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="2dc53-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2dc53-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="2dc53-116">NavigationCompleted-nach einer Navigation im Dokument der obersten Ebene wird das Rendering erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2dc53-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="2dc53-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2dc53-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="2dc53-118">NavigationStarting versendet, bevor eine neue Navigate-Datei für das Dokument der obersten Ebene des WebView2 gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2dc53-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="2dc53-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="2dc53-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="2dc53-120">Die Quellcodeverteilung wird nach dem Ändern der Quelleigenschaft weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="2dc53-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="2dc53-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2dc53-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="2dc53-122">WebMessageReceived sendet nach dem Senden einer Nachricht an den App-Host per Webinhalt `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="2dc53-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="2dc53-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="2dc53-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="2dc53-124">Der zugrunde liegende CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="2dc53-125">Source</span><span class="sxs-lookup"><span data-stu-id="2dc53-125">Source</span></span>](#source) | <span data-ttu-id="2dc53-126">Die Source-Eigenschaft ist der URI des Dokuments der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="2dc53-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="2dc53-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="2dc53-128">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="2dc53-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="2dc53-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="2dc53-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="2dc53-130">Gibt "true" zurück, wenn die WebView über die GoBack-Methode zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="2dc53-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="2dc53-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="2dc53-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="2dc53-132">Gibt "true" zurück, wenn die WebView über die GoForward-Methode zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="2dc53-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="2dc53-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="2dc53-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="2dc53-134">Initialisierung der [CoreWebView2](#corewebview2)des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="2dc53-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="2dc53-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="2dc53-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="2dc53-136">Führt das bereitgestellte Skript im Dokument der obersten Ebene des WebView2 aus.</span><span class="sxs-lookup"><span data-stu-id="2dc53-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="2dc53-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="2dc53-137">GoBack</span></span>](#goback) | <span data-ttu-id="2dc53-138">Navigieren Sie im Navigationsverlauf zur vorherigen Seite.</span><span class="sxs-lookup"><span data-stu-id="2dc53-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="2dc53-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="2dc53-139">GoForward</span></span>](#goforward) | <span data-ttu-id="2dc53-140">Navigieren Sie im Navigationsverlauf zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="2dc53-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="2dc53-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="2dc53-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="2dc53-142">Rendern Sie den bereitgestellten HTML-Code als Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="2dc53-143">Laden</span><span class="sxs-lookup"><span data-stu-id="2dc53-143">Reload</span></span>](#reload) | <span data-ttu-id="2dc53-144">Laden Sie das Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="2dc53-145">Stop</span><span class="sxs-lookup"><span data-stu-id="2dc53-145">Stop</span></span>](#stop) | <span data-ttu-id="2dc53-146">Beenden Sie die Navigation in Progress in der WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="2dc53-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="2dc53-147">WebView2</span></span>](#webview2) | <span data-ttu-id="2dc53-148">Erstellen Sie ein neues WebView2 WinForms-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2dc53-148">Create a new WebView2 WinForms control.</span></span>

## <span data-ttu-id="2dc53-149">Member</span><span class="sxs-lookup"><span data-stu-id="2dc53-149">Members</span></span>

#### <span data-ttu-id="2dc53-150">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="2dc53-150">ContentLoading</span></span> 

<span data-ttu-id="2dc53-151">ContentLoading wird nach dem Beginn einer Navigation zu einem neuen URI und dem Rendern des Inhalts dieses URIs ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="2dc53-151">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="2dc53-152">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="2dc53-152">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="2dc53-153">Dies entspricht dem ContentLoading-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-153">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-154">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="2dc53-154">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-155">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="2dc53-155">CoreWebView2Ready</span></span> 

<span data-ttu-id="2dc53-156">Dieses Ereignis wird ausgelöst, wenn die [CoreWebView2](#corewebview2) des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dc53-156">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="2dc53-157">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="2dc53-157">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="2dc53-158">Sie sollten dieses Ereignis behandeln, wenn Sie eine einmalige Einrichtungs Operation für die CoreWebView2 durchführen müssen, für die Sie alle ihre Verwendungen beeinflussen möchten (beispielsweise das Hinzufügen von Ereignishandlern, das Konfigurieren von Einstellungen, das Installieren von Dokument Erstellungsskripts und das Hinzufügen von Host Objekten).</span><span class="sxs-lookup"><span data-stu-id="2dc53-158">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="2dc53-159">Dieses Ereignis stellt keine Argumente bereit, und der Absender ist das WebView2-Steuerelement, dessen CoreWebView2-Eigenschaft zum ersten Mal gültig (also ungleich null) ist.</span><span class="sxs-lookup"><span data-stu-id="2dc53-159">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="2dc53-160">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="2dc53-160">NavigationCompleted</span></span> 

<span data-ttu-id="2dc53-161">NavigationCompleted-nach einer Navigation im Dokument der obersten Ebene wird das Rendering erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2dc53-161">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="2dc53-162">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="2dc53-162">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="2dc53-163">Dies entspricht dem NavigationCompleted-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-163">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-164">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2dc53-164">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-165">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="2dc53-165">NavigationStarting</span></span> 

<span data-ttu-id="2dc53-166">NavigationStarting versendet, bevor eine neue Navigate-Datei für das Dokument der obersten Ebene des WebView2 gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2dc53-166">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="2dc53-167">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="2dc53-167">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="2dc53-168">Dies entspricht dem NavigationStarting-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-168">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-169">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2dc53-169">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-170">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="2dc53-170">SourceChanged</span></span> 

<span data-ttu-id="2dc53-171">Die Quellcodeverteilung wird nach dem Ändern der Quelleigenschaft weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="2dc53-171">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="2dc53-172">public event EventHandler< CoreWebView2SourceChangedEventArgs > [Quelle](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="2dc53-172">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="2dc53-173">Dies kann während einer Navigation auftreten, oder wenn andernfalls das Skript auf der Seite den URI des Dokuments ändert.</span><span class="sxs-lookup"><span data-stu-id="2dc53-173">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="2dc53-174">Dies entspricht dem CoreWebView2-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2dc53-174">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-175">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Quellcode.</span><span class="sxs-lookup"><span data-stu-id="2dc53-175">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-176">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="2dc53-176">WebMessageReceived</span></span> 

<span data-ttu-id="2dc53-177">WebMessageReceived sendet nach dem Senden einer Nachricht an den App-Host per Webinhalt `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="2dc53-177">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="2dc53-178">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="2dc53-178">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="2dc53-179">Dies entspricht dem WebMessageReceived-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-179">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-180">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="2dc53-180">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-181">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="2dc53-181">CoreWebView2</span></span> 

<span data-ttu-id="2dc53-182">Der zugrunde liegende CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-182">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="2dc53-183">öffentliche CoreWebView2- [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="2dc53-183">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="2dc53-184">Verwenden Sie diese Eigenschaft, um mehr Vorgänge für den WebView2-Inhalt durchzuführen, als auf dem WebView2 verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="2dc53-184">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="2dc53-185">Dieser Wert ist NULL, bis er initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2dc53-185">This value is null until it is initialized.</span></span> <span data-ttu-id="2dc53-186">Sie können erzwingen, dass der zugrunde liegende CoreWebView2 über die InitializeAsync-Methode initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2dc53-186">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="2dc53-187">Source</span><span class="sxs-lookup"><span data-stu-id="2dc53-187">Source</span></span> 

<span data-ttu-id="2dc53-188">Die Source-Eigenschaft ist der URI des Dokuments der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-188">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="2dc53-189">öffentliche URI- [Quelle](#source)</span><span class="sxs-lookup"><span data-stu-id="2dc53-189">public Uri [Source](#source)</span></span>

<span data-ttu-id="2dc53-190">Das Festlegen der Quelle entspricht dem Aufruf von CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="2dc53-190">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="2dc53-191">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, lautet diese Eigenschaft "about: blank".</span><span class="sxs-lookup"><span data-stu-id="2dc53-191">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="2dc53-192">Wenn die Eigenschaft auf einen nicht absoluten URI oder Null festgesetzt ist, bleibt die Eigenschaft unverändert.</span><span class="sxs-lookup"><span data-stu-id="2dc53-192">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="2dc53-193">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="2dc53-193">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-194">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="2dc53-194">ZoomFactor</span></span> 

<span data-ttu-id="2dc53-195">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="2dc53-195">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="2dc53-196">öffentliches Doppel [ZoomFactor](#zoomfactor)</span><span class="sxs-lookup"><span data-stu-id="2dc53-196">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="2dc53-197">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="2dc53-197">CanGoBack</span></span> 

<span data-ttu-id="2dc53-198">Gibt "true" zurück, wenn die WebView über die GoBack-Methode zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="2dc53-198">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="2dc53-199">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="2dc53-199">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="2dc53-200">Dies entspricht der CanGoBack-Eigenschaft für CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-200">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-201">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, ist diese Eigenschaft false.</span><span class="sxs-lookup"><span data-stu-id="2dc53-201">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="2dc53-202">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. CanGoBack.</span><span class="sxs-lookup"><span data-stu-id="2dc53-202">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-203">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="2dc53-203">CanGoForward</span></span> 

<span data-ttu-id="2dc53-204">Gibt "true" zurück, wenn die WebView über die GoForward-Methode zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="2dc53-204">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="2dc53-205">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="2dc53-205">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="2dc53-206">Dies entspricht der CanGoForward-Eigenschaft für CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-206">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-207">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, ist diese Eigenschaft false.</span><span class="sxs-lookup"><span data-stu-id="2dc53-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="2dc53-208">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="2dc53-208">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-209">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="2dc53-209">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="2dc53-210">Initialisierung der [CoreWebView2](#corewebview2)des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="2dc53-210">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="2dc53-211">öffentliche Aufgaben- [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="2dc53-211">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="2dc53-212">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dc53-212">Parameters</span></span>
* `environment` <span data-ttu-id="2dc53-213">Eine zuvor erstellte CoreWebView2Environment, die zum Erstellen des CoreWebView2 verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2dc53-213">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="2dc53-214">Durch das Erstellen einer eigenen Umgebung können Sie verschiedene Optionen steuern, die sich auf die Initialisierung des CoreWebView2 auswirken.</span><span class="sxs-lookup"><span data-stu-id="2dc53-214">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="2dc53-215">Wenn Sie NULL (den Standardwert) übergeben, wird eine Standardumgebung erstellt und automatisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dc53-215">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="2dc53-216">Gibt</span><span class="sxs-lookup"><span data-stu-id="2dc53-216">Returns</span></span>
<span data-ttu-id="2dc53-217">Eine Aufgabe, die den Hintergrund Initialisierungsprozess darstellt.</span><span class="sxs-lookup"><span data-stu-id="2dc53-217">A Task that represents the background initialization process.</span></span> <span data-ttu-id="2dc53-218">Wenn die Aufgabe abgeschlossen ist, steht die CoreWebView2-Eigenschaft zur Verwendung zur Verfügung (also nicht-null).</span><span class="sxs-lookup"><span data-stu-id="2dc53-218">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="2dc53-219">Beachten Sie, dass das [CoreWebView2Ready](#corewebview2ready) -Ereignis des Steuerelements aufgerufen wird, bevor die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2dc53-219">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="2dc53-220">Das zusätzliche Aufrufen dieser Methode hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt dieselbe Aufgabe wie beim ersten Aufruf zurück.</span><span class="sxs-lookup"><span data-stu-id="2dc53-220">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="2dc53-221">Das Aufrufen dieser Methode, nachdem die Initialisierung implizit ausgelöst wurde, indem die [Source](#source) -Eigenschaft festgelegt wird, hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt einfach eine Aufgabe zurück, die die bereits ausgeführte Initialisierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="2dc53-221">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="2dc53-222">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="2dc53-222">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="2dc53-223">Wird ausgelöst, wenn Sie von einem nicht-UI-Thread aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2dc53-223">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="2dc53-224">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="2dc53-224">ExecuteScriptAsync</span></span> 

<span data-ttu-id="2dc53-225">Führt das bereitgestellte Skript im Dokument der obersten Ebene des WebView2 aus.</span><span class="sxs-lookup"><span data-stu-id="2dc53-225">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="2dc53-226">Public Async Task< Zeichenfolge > [ExecuteScriptAsync](#executescriptasync)(Zeichenfolgen Skript)</span><span class="sxs-lookup"><span data-stu-id="2dc53-226">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="2dc53-227">Dies entspricht der ExecuteScriptAsync-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-227">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-228">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus.</span><span class="sxs-lookup"><span data-stu-id="2dc53-228">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="2dc53-229">Weitere Informationen finden Sie unter CoreWebView2.ExecuteScriptAsync-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2dc53-229">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-230">GoBack</span><span class="sxs-lookup"><span data-stu-id="2dc53-230">GoBack</span></span> 

<span data-ttu-id="2dc53-231">Navigieren Sie im Navigationsverlauf zur vorherigen Seite.</span><span class="sxs-lookup"><span data-stu-id="2dc53-231">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="2dc53-232">publicvoid [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="2dc53-232">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="2dc53-233">Dies entspricht der GoBack-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-233">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-234">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2dc53-234">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="2dc53-235">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. GoBack.</span><span class="sxs-lookup"><span data-stu-id="2dc53-235">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-236">GoForward</span><span class="sxs-lookup"><span data-stu-id="2dc53-236">GoForward</span></span> 

<span data-ttu-id="2dc53-237">Navigieren Sie im Navigationsverlauf zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="2dc53-237">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="2dc53-238">publicvoid [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="2dc53-238">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="2dc53-239">Dies entspricht der GoForward-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-239">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-240">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2dc53-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="2dc53-241">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. GoForward.</span><span class="sxs-lookup"><span data-stu-id="2dc53-241">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-242">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="2dc53-242">NavigateToString</span></span> 

<span data-ttu-id="2dc53-243">Rendern Sie den bereitgestellten HTML-Code als Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-243">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="2dc53-244">publicvoid [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="2dc53-244">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="2dc53-245">Dies entspricht der NavigateToString-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-245">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-246">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus.</span><span class="sxs-lookup"><span data-stu-id="2dc53-246">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="2dc53-247">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigateToString.</span><span class="sxs-lookup"><span data-stu-id="2dc53-247">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-248">Laden</span><span class="sxs-lookup"><span data-stu-id="2dc53-248">Reload</span></span> 

<span data-ttu-id="2dc53-249">Laden Sie das Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-249">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="2dc53-250">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="2dc53-250">public void [Reload](#reload)()</span></span>

<span data-ttu-id="2dc53-251">Dies entspricht der Reload-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-251">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-252">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus.</span><span class="sxs-lookup"><span data-stu-id="2dc53-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="2dc53-253">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Reload.</span><span class="sxs-lookup"><span data-stu-id="2dc53-253">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-254">Stop</span><span class="sxs-lookup"><span data-stu-id="2dc53-254">Stop</span></span> 

<span data-ttu-id="2dc53-255">Beenden Sie die Navigation in Progress in der WebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-255">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="2dc53-256">öffentlicher void- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="2dc53-256">public void [Stop](#stop)()</span></span>

<span data-ttu-id="2dc53-257">Dies entspricht der Stop-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="2dc53-257">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="2dc53-258">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2dc53-258">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="2dc53-259">Weitere Informationen finden Sie unter CoreWebView2. Stop-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2dc53-259">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="2dc53-260">WebView2</span><span class="sxs-lookup"><span data-stu-id="2dc53-260">WebView2</span></span> 

<span data-ttu-id="2dc53-261">Erstellen Sie ein neues WebView2 WinForms-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2dc53-261">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="2dc53-262">Public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="2dc53-262">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="2dc53-263">Nach der Erstellung ist die CoreWebView2-Eigenschaft NULL.</span><span class="sxs-lookup"><span data-stu-id="2dc53-263">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="2dc53-264">Rufen Sie [EnsureCoreWebView2Async](#ensurecorewebview2async) auf, um die zugrunde liegende CoreWebView2 zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="2dc53-264">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

