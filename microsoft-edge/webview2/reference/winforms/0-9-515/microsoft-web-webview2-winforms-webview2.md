---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 25ea8367aa9d64d0a1066cf8c1564f4d9c9f05ed
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653714"
---
# <span data-ttu-id="ab984-104">Microsoft. Web. WebView2. WinForms. WebView2 Klasse</span><span class="sxs-lookup"><span data-stu-id="ab984-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="ab984-105">Namespace: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="ab984-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="ab984-106">Assembly: Microsoft. Web. WebView2. WinForms. dll</span><span class="sxs-lookup"><span data-stu-id="ab984-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="ab984-107">Steuerelement zum Einbetten von WebView2 in WinForms</span><span class="sxs-lookup"><span data-stu-id="ab984-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="ab984-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ab984-108">Summary</span></span>

 <span data-ttu-id="ab984-109">Member</span><span class="sxs-lookup"><span data-stu-id="ab984-109">Members</span></span>                        | <span data-ttu-id="ab984-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ab984-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ab984-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="ab984-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="ab984-112">ContentLoading wird nach dem Beginn einer Navigation zu einem neuen URI und dem Rendern des Inhalts dieses URIs ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ab984-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="ab984-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="ab984-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="ab984-114">Dieses Ereignis wird ausgelöst, wenn die [CoreWebView2](#corewebview2) des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab984-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="ab984-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="ab984-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="ab984-116">NavigationCompleted-nach einer Navigation im Dokument der obersten Ebene wird das Rendering erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ab984-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="ab984-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="ab984-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="ab984-118">NavigationStarting versendet, bevor eine neue Navigate-Datei für das Dokument der obersten Ebene des WebView2 gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ab984-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="ab984-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="ab984-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="ab984-120">Die Quellcodeverteilung wird nach dem Ändern der Quelleigenschaft weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="ab984-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="ab984-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="ab984-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="ab984-122">WebMessageReceived sendet nach dem Senden einer Nachricht an den App-Host per Webinhalt `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ab984-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="ab984-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="ab984-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="ab984-124">Der zugrunde liegende CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="ab984-125">Source</span><span class="sxs-lookup"><span data-stu-id="ab984-125">Source</span></span>](#source) | <span data-ttu-id="ab984-126">Die Source-Eigenschaft ist der URI des Dokuments der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="ab984-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ab984-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="ab984-128">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="ab984-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="ab984-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="ab984-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="ab984-130">Gibt "true" zurück, wenn die WebView über die GoBack-Methode zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="ab984-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="ab984-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="ab984-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="ab984-132">Gibt "true" zurück, wenn die WebView über die GoForward-Methode zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="ab984-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="ab984-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="ab984-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="ab984-134">Initialisierung der [CoreWebView2](#corewebview2)des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="ab984-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="ab984-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="ab984-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="ab984-136">Führt das bereitgestellte Skript im Dokument der obersten Ebene des WebView2 aus.</span><span class="sxs-lookup"><span data-stu-id="ab984-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="ab984-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="ab984-137">GoBack</span></span>](#goback) | <span data-ttu-id="ab984-138">Navigieren Sie im Navigationsverlauf zur vorherigen Seite.</span><span class="sxs-lookup"><span data-stu-id="ab984-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="ab984-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="ab984-139">GoForward</span></span>](#goforward) | <span data-ttu-id="ab984-140">Navigieren Sie im Navigationsverlauf zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="ab984-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="ab984-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="ab984-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="ab984-142">Rendern Sie den bereitgestellten HTML-Code als Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="ab984-143">Laden</span><span class="sxs-lookup"><span data-stu-id="ab984-143">Reload</span></span>](#reload) | <span data-ttu-id="ab984-144">Laden Sie das Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="ab984-145">Stop</span><span class="sxs-lookup"><span data-stu-id="ab984-145">Stop</span></span>](#stop) | <span data-ttu-id="ab984-146">Beenden Sie die Navigation in Progress in der WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="ab984-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="ab984-147">WebView2</span></span>](#webview2) | <span data-ttu-id="ab984-148">Erstellen Sie ein neues WebView2 WinForms-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ab984-148">Create a new WebView2 WinForms control.</span></span>
[<span data-ttu-id="ab984-149">OnEnter</span><span class="sxs-lookup"><span data-stu-id="ab984-149">OnEnter</span></span>](#onenter) | <span data-ttu-id="ab984-150">Geschützter Fokus Handler.</span><span class="sxs-lookup"><span data-stu-id="ab984-150">Protected focus handler.</span></span>
[<span data-ttu-id="ab984-151">OnSizeChanged</span><span class="sxs-lookup"><span data-stu-id="ab984-151">OnSizeChanged</span></span>](#onsizechanged) | <span data-ttu-id="ab984-152">Geschützter SizeChanged-Handler.</span><span class="sxs-lookup"><span data-stu-id="ab984-152">Protected SizeChanged handler.</span></span>
[<span data-ttu-id="ab984-153">OnVisibleChanged</span><span class="sxs-lookup"><span data-stu-id="ab984-153">OnVisibleChanged</span></span>](#onvisiblechanged) | <span data-ttu-id="ab984-154">Geschützter Sichtbarkeits Handler.</span><span class="sxs-lookup"><span data-stu-id="ab984-154">Protected VisibilityChanged handler.</span></span>

## <span data-ttu-id="ab984-155">Member</span><span class="sxs-lookup"><span data-stu-id="ab984-155">Members</span></span>

#### <span data-ttu-id="ab984-156">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="ab984-156">ContentLoading</span></span> 

<span data-ttu-id="ab984-157">ContentLoading wird nach dem Beginn einer Navigation zu einem neuen URI und dem Rendern des Inhalts dieses URIs ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ab984-157">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="ab984-158">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="ab984-158">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="ab984-159">Dies entspricht dem ContentLoading-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-159">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="ab984-160">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="ab984-160">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="ab984-161">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="ab984-161">CoreWebView2Ready</span></span> 

<span data-ttu-id="ab984-162">Dieses Ereignis wird ausgelöst, wenn die [CoreWebView2](#corewebview2) des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab984-162">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="ab984-163">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="ab984-163">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="ab984-164">Sie sollten dieses Ereignis behandeln, wenn Sie eine einmalige Einrichtungs Operation für die CoreWebView2 durchführen müssen, für die Sie alle ihre Verwendungen beeinflussen möchten (beispielsweise das Hinzufügen von Ereignishandlern, das Konfigurieren von Einstellungen, das Installieren von Dokument Erstellungsskripts und das Hinzufügen von Host Objekten).</span><span class="sxs-lookup"><span data-stu-id="ab984-164">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="ab984-165">Dieses Ereignis stellt keine Argumente bereit, und der Absender ist das WebView2-Steuerelement, dessen CoreWebView2-Eigenschaft zum ersten Mal gültig (also ungleich null) ist.</span><span class="sxs-lookup"><span data-stu-id="ab984-165">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="ab984-166">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="ab984-166">NavigationCompleted</span></span> 

<span data-ttu-id="ab984-167">NavigationCompleted-nach einer Navigation im Dokument der obersten Ebene wird das Rendering erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ab984-167">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="ab984-168">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="ab984-168">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="ab984-169">Dies entspricht dem NavigationCompleted-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-169">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="ab984-170">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="ab984-170">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="ab984-171">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="ab984-171">NavigationStarting</span></span> 

<span data-ttu-id="ab984-172">NavigationStarting versendet, bevor eine neue Navigate-Datei für das Dokument der obersten Ebene des WebView2 gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ab984-172">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="ab984-173">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="ab984-173">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="ab984-174">Dies entspricht dem NavigationStarting-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-174">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="ab984-175">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ab984-175">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="ab984-176">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="ab984-176">SourceChanged</span></span> 

<span data-ttu-id="ab984-177">Die Quellcodeverteilung wird nach dem Ändern der Quelleigenschaft weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="ab984-177">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="ab984-178">public event EventHandler< CoreWebView2SourceChangedEventArgs > [Quelle](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="ab984-178">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="ab984-179">Dies kann während einer Navigation auftreten, oder wenn andernfalls das Skript auf der Seite den URI des Dokuments ändert.</span><span class="sxs-lookup"><span data-stu-id="ab984-179">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="ab984-180">Dies entspricht dem CoreWebView2-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ab984-180">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="ab984-181">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Quellcode.</span><span class="sxs-lookup"><span data-stu-id="ab984-181">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="ab984-182">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="ab984-182">WebMessageReceived</span></span> 

<span data-ttu-id="ab984-183">WebMessageReceived sendet nach dem Senden einer Nachricht an den App-Host per Webinhalt `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ab984-183">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="ab984-184">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="ab984-184">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="ab984-185">Dies entspricht dem WebMessageReceived-Ereignis im CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-185">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="ab984-186">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="ab984-186">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="ab984-187">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="ab984-187">CoreWebView2</span></span> 

<span data-ttu-id="ab984-188">Der zugrunde liegende CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-188">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="ab984-189">öffentliche CoreWebView2- [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="ab984-189">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="ab984-190">Verwenden Sie diese Eigenschaft, um mehr Vorgänge für den WebView2-Inhalt durchzuführen, als auf dem WebView2 verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="ab984-190">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="ab984-191">Dieser Wert ist NULL, bis er initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab984-191">This value is null until it is initialized.</span></span> <span data-ttu-id="ab984-192">Sie können erzwingen, dass der zugrunde liegende CoreWebView2 über die InitializeAsync-Methode initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab984-192">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="ab984-193">Source</span><span class="sxs-lookup"><span data-stu-id="ab984-193">Source</span></span> 

<span data-ttu-id="ab984-194">Die Source-Eigenschaft ist der URI des Dokuments der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-194">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="ab984-195">öffentliche URI- [Quelle](#source)</span><span class="sxs-lookup"><span data-stu-id="ab984-195">public Uri [Source](#source)</span></span>

<span data-ttu-id="ab984-196">Das Festlegen der Quelle entspricht dem Aufruf von CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="ab984-196">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="ab984-197">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, lautet diese Eigenschaft "about: blank".</span><span class="sxs-lookup"><span data-stu-id="ab984-197">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="ab984-198">Wenn die Eigenschaft auf einen nicht absoluten URI oder Null festgesetzt ist, bleibt die Eigenschaft unverändert.</span><span class="sxs-lookup"><span data-stu-id="ab984-198">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="ab984-199">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="ab984-199">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="ab984-200">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="ab984-200">ZoomFactor</span></span> 

<span data-ttu-id="ab984-201">Der Zoomfaktor für die WebView.</span><span class="sxs-lookup"><span data-stu-id="ab984-201">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="ab984-202">öffentliches Doppel [ZoomFactor](#zoomfactor)</span><span class="sxs-lookup"><span data-stu-id="ab984-202">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="ab984-203">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="ab984-203">CanGoBack</span></span> 

<span data-ttu-id="ab984-204">Gibt "true" zurück, wenn die WebView über die GoBack-Methode zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="ab984-204">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="ab984-205">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="ab984-205">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="ab984-206">Dies entspricht der CanGoBack-Eigenschaft für CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-206">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="ab984-207">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, ist diese Eigenschaft false.</span><span class="sxs-lookup"><span data-stu-id="ab984-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="ab984-208">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. CanGoBack.</span><span class="sxs-lookup"><span data-stu-id="ab984-208">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="ab984-209">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="ab984-209">CanGoForward</span></span> 

<span data-ttu-id="ab984-210">Gibt "true" zurück, wenn die WebView über die GoForward-Methode zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="ab984-210">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="ab984-211">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="ab984-211">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="ab984-212">Dies entspricht der CanGoForward-Eigenschaft für CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-212">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="ab984-213">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, ist diese Eigenschaft false.</span><span class="sxs-lookup"><span data-stu-id="ab984-213">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="ab984-214">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="ab984-214">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="ab984-215">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="ab984-215">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="ab984-216">Initialisierung der [CoreWebView2](#corewebview2)des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="ab984-216">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="ab984-217">öffentliche Aufgaben- [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="ab984-217">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="ab984-218">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab984-218">Parameters</span></span>
* `environment` <span data-ttu-id="ab984-219">Eine zuvor erstellte CoreWebView2Environment, die zum Erstellen des CoreWebView2 verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab984-219">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="ab984-220">Durch das Erstellen einer eigenen Umgebung können Sie verschiedene Optionen steuern, die sich auf die Initialisierung des CoreWebView2 auswirken.</span><span class="sxs-lookup"><span data-stu-id="ab984-220">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="ab984-221">Wenn Sie NULL (den Standardwert) übergeben, wird eine Standardumgebung erstellt und automatisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab984-221">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="ab984-222">Gibt</span><span class="sxs-lookup"><span data-stu-id="ab984-222">Returns</span></span>
<span data-ttu-id="ab984-223">Eine Aufgabe, die den Hintergrund Initialisierungsprozess darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab984-223">A Task that represents the background initialization process.</span></span> <span data-ttu-id="ab984-224">Wenn die Aufgabe abgeschlossen ist, steht die CoreWebView2-Eigenschaft zur Verwendung zur Verfügung (also nicht-null).</span><span class="sxs-lookup"><span data-stu-id="ab984-224">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="ab984-225">Beachten Sie, dass das [CoreWebView2Ready](#corewebview2ready) -Ereignis des Steuerelements aufgerufen wird, bevor die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ab984-225">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="ab984-226">Das zusätzliche Aufrufen dieser Methode hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt dieselbe Aufgabe wie beim ersten Aufruf zurück.</span><span class="sxs-lookup"><span data-stu-id="ab984-226">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="ab984-227">Das Aufrufen dieser Methode, nachdem die Initialisierung implizit ausgelöst wurde, indem die [Source](#source) -Eigenschaft festgelegt wird, hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt einfach eine Aufgabe zurück, die die bereits ausgeführte Initialisierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab984-227">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="ab984-228">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="ab984-228">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="ab984-229">Wird ausgelöst, wenn Sie von einem nicht-UI-Thread aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ab984-229">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="ab984-230">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="ab984-230">ExecuteScriptAsync</span></span> 

<span data-ttu-id="ab984-231">Führt das bereitgestellte Skript im Dokument der obersten Ebene des WebView2 aus.</span><span class="sxs-lookup"><span data-stu-id="ab984-231">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="ab984-232">Public Async Task< Zeichenfolge > [ExecuteScriptAsync](#executescriptasync)(Zeichenfolgen Skript)</span><span class="sxs-lookup"><span data-stu-id="ab984-232">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="ab984-233">Dies entspricht der ExecuteScriptAsync-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-233">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="ab984-234">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus.</span><span class="sxs-lookup"><span data-stu-id="ab984-234">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="ab984-235">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. ExecuteScriptAsync.</span><span class="sxs-lookup"><span data-stu-id="ab984-235">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="ab984-236">GoBack</span><span class="sxs-lookup"><span data-stu-id="ab984-236">GoBack</span></span> 

<span data-ttu-id="ab984-237">Navigieren Sie im Navigationsverlauf zur vorherigen Seite.</span><span class="sxs-lookup"><span data-stu-id="ab984-237">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="ab984-238">publicvoid [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="ab984-238">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="ab984-239">Dies entspricht der GoBack-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-239">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="ab984-240">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="ab984-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="ab984-241">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. GoBack.</span><span class="sxs-lookup"><span data-stu-id="ab984-241">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="ab984-242">GoForward</span><span class="sxs-lookup"><span data-stu-id="ab984-242">GoForward</span></span> 

<span data-ttu-id="ab984-243">Navigieren Sie im Navigationsverlauf zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="ab984-243">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="ab984-244">publicvoid [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="ab984-244">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="ab984-245">Dies entspricht der GoForward-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-245">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="ab984-246">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="ab984-246">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="ab984-247">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. GoForward.</span><span class="sxs-lookup"><span data-stu-id="ab984-247">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="ab984-248">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="ab984-248">NavigateToString</span></span> 

<span data-ttu-id="ab984-249">Rendern Sie den bereitgestellten HTML-Code als Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-249">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="ab984-250">publicvoid [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="ab984-250">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="ab984-251">Dies entspricht der NavigateToString-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-251">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="ab984-252">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus.</span><span class="sxs-lookup"><span data-stu-id="ab984-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="ab984-253">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. NavigateToString.</span><span class="sxs-lookup"><span data-stu-id="ab984-253">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="ab984-254">Laden</span><span class="sxs-lookup"><span data-stu-id="ab984-254">Reload</span></span> 

<span data-ttu-id="ab984-255">Laden Sie das Dokument der obersten Ebene des WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-255">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="ab984-256">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="ab984-256">public void [Reload](#reload)()</span></span>

<span data-ttu-id="ab984-257">Dies entspricht der Reload-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-257">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="ab984-258">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, löst diese Methode eine InvalidOperationException aus.</span><span class="sxs-lookup"><span data-stu-id="ab984-258">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="ab984-259">Weitere Informationen finden Sie unter Dokumentation zu CoreWebView2. Reload.</span><span class="sxs-lookup"><span data-stu-id="ab984-259">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="ab984-260">Stop</span><span class="sxs-lookup"><span data-stu-id="ab984-260">Stop</span></span> 

<span data-ttu-id="ab984-261">Beenden Sie die Navigation in Progress in der WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-261">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="ab984-262">öffentlicher void- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="ab984-262">public void [Stop](#stop)()</span></span>

<span data-ttu-id="ab984-263">Dies entspricht der Stop-Methode auf der CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="ab984-263">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="ab984-264">Wenn der zugrunde liegende CoreWebView2 noch nicht initialisiert ist, hat diese Methode keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="ab984-264">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="ab984-265">Weitere Informationen finden Sie unter CoreWebView2. Stop-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ab984-265">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="ab984-266">WebView2</span><span class="sxs-lookup"><span data-stu-id="ab984-266">WebView2</span></span> 

<span data-ttu-id="ab984-267">Erstellen Sie ein neues WebView2 WinForms-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ab984-267">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="ab984-268">Public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="ab984-268">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="ab984-269">Nach der Erstellung ist die CoreWebView2-Eigenschaft NULL.</span><span class="sxs-lookup"><span data-stu-id="ab984-269">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="ab984-270">Rufen Sie [EnsureCoreWebView2Async](#ensurecorewebview2async) auf, um die zugrunde liegende CoreWebView2 zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="ab984-270">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

#### <span data-ttu-id="ab984-271">OnEnter</span><span class="sxs-lookup"><span data-stu-id="ab984-271">OnEnter</span></span> 

<span data-ttu-id="ab984-272">Geschützter Fokus Handler.</span><span class="sxs-lookup"><span data-stu-id="ab984-272">Protected focus handler.</span></span>

> <span data-ttu-id="ab984-273">protected override void [OnEnter](#onenter)(EventArgs e)</span><span class="sxs-lookup"><span data-stu-id="ab984-273">protected override void [OnEnter](#onenter)(EventArgs e)</span></span>

#### <span data-ttu-id="ab984-274">OnSizeChanged</span><span class="sxs-lookup"><span data-stu-id="ab984-274">OnSizeChanged</span></span> 

<span data-ttu-id="ab984-275">Geschützter SizeChanged-Handler.</span><span class="sxs-lookup"><span data-stu-id="ab984-275">Protected SizeChanged handler.</span></span>

> <span data-ttu-id="ab984-276">protected override void [onsized](#onsizechanged)(EventArgs e)</span><span class="sxs-lookup"><span data-stu-id="ab984-276">protected override void [OnSizeChanged](#onsizechanged)(EventArgs e)</span></span>

#### <span data-ttu-id="ab984-277">OnVisibleChanged</span><span class="sxs-lookup"><span data-stu-id="ab984-277">OnVisibleChanged</span></span> 

<span data-ttu-id="ab984-278">Geschützter Sichtbarkeits Handler.</span><span class="sxs-lookup"><span data-stu-id="ab984-278">Protected VisibilityChanged handler.</span></span>

> <span data-ttu-id="ab984-279">protected override void [onvisibled](#onvisiblechanged)(EventArgs e)</span><span class="sxs-lookup"><span data-stu-id="ab984-279">protected override void [OnVisibleChanged](#onvisiblechanged)(EventArgs e)</span></span>

