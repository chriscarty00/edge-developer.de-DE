---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f2c3bcb5334abc907a838971ebc1773b6485194f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653787"
---
# <span data-ttu-id="a56cb-104">Microsoft. Web. WebView2. WPF. WebView2 Klasse</span><span class="sxs-lookup"><span data-stu-id="a56cb-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="a56cb-105">Namespace: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="a56cb-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="a56cb-106">Assembly: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="a56cb-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="a56cb-107">Ein Steuerelement zum Einbetten von Webinhalten in eine WPF-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a56cb-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="a56cb-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a56cb-108">Summary</span></span>

 <span data-ttu-id="a56cb-109">Member</span><span class="sxs-lookup"><span data-stu-id="a56cb-109">Members</span></span>                        | <span data-ttu-id="a56cb-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a56cb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a56cb-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="a56cb-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="a56cb-112">Ein Wrapper um das CoreWebView2. ContentLoading-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="a56cb-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="a56cb-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="a56cb-114">Dieses Ereignis wird ausgelöst, wenn die CoreWebView2 des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="a56cb-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="a56cb-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="a56cb-116">Ein Wrapper um das CoreWebView2. NavigationCompleted-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="a56cb-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="a56cb-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="a56cb-118">Ein Wrapper um das CoreWebView2. NavigationStarting-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="a56cb-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="a56cb-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="a56cb-120">Ein Wrapper um das CoreWebView2. Sourcecode-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="a56cb-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="a56cb-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="a56cb-122">Ein Wrapper um das CoreWebView2. WebMessageReceived-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="a56cb-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="a56cb-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="a56cb-124">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="a56cb-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="a56cb-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="a56cb-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="a56cb-126">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="a56cb-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="a56cb-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="a56cb-128">Greifen Sie auf die vollständige Funktionalität der zugrunde liegenden Core. CoreWebView2-com-API zu.</span><span class="sxs-lookup"><span data-stu-id="a56cb-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="a56cb-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="a56cb-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="a56cb-130">Ruft eine Sammlung von Optionen ab, die während der Initialisierung des CoreWebView2 des Steuerelements verwendet werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a56cb-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="a56cb-131">Source</span><span class="sxs-lookup"><span data-stu-id="a56cb-131">Source</span></span>](#source) | <span data-ttu-id="a56cb-132">Der URI der obersten Ebene, den die WebView aktuell anzeigt (oder wird angezeigt, sobald die Initialisierung des CoreWebView2-Endgeräts endet).</span><span class="sxs-lookup"><span data-stu-id="a56cb-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="a56cb-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="a56cb-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="a56cb-134">Initialisierung der CoreWebView2 des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="a56cb-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="a56cb-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="a56cb-136">Führt JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="a56cb-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="a56cb-137">GoBack</span></span>](#goback) | <span data-ttu-id="a56cb-138">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="a56cb-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="a56cb-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="a56cb-139">GoForward</span></span>](#goforward) | <span data-ttu-id="a56cb-140">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="a56cb-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="a56cb-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="a56cb-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="a56cb-142">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="a56cb-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="a56cb-143">Laden</span><span class="sxs-lookup"><span data-stu-id="a56cb-143">Reload</span></span>](#reload) | <span data-ttu-id="a56cb-144">Lädt die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="a56cb-144">Reloads the current page.</span></span>
[<span data-ttu-id="a56cb-145">Stop</span><span class="sxs-lookup"><span data-stu-id="a56cb-145">Stop</span></span>](#stop) | <span data-ttu-id="a56cb-146">Stoppt alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="a56cb-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="a56cb-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-147">WebView2</span></span>](#webview2) | <span data-ttu-id="a56cb-148">Erstellt eine neue Instanz eines WebView2-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="a56cb-148">Creates a new instance of a WebView2 control.</span></span>
[<span data-ttu-id="a56cb-149">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-149">BuildWindowCore</span></span>](#buildwindowcore) | <span data-ttu-id="a56cb-150">Dies wird von HwndHost überschrieben und aufgerufen, um uns zu beauftragen, unser HWND zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-150">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>
[<span data-ttu-id="a56cb-151">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-151">DestroyWindowCore</span></span>](#destroywindowcore) | <span data-ttu-id="a56cb-152">Dies wird von HwndHost überschrieben und aufgerufen, um uns anzuweisen, unser HWND zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="a56cb-152">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>
[<span data-ttu-id="a56cb-153">Löschen</span><span class="sxs-lookup"><span data-stu-id="a56cb-153">Dispose</span></span>](#dispose) | <span data-ttu-id="a56cb-154">Dies wird von unserer Basisklasse entsprechend der typischen Implementierung des IDispose-Musters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-154">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>
[<span data-ttu-id="a56cb-155">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-155">HasFocusWithinCore</span></span>](#hasfocuswithincore) | <span data-ttu-id="a56cb-156">Dies wird von HwndHost überschrieben und aufgerufen, wenn WPF wissen muss, ob sich der Fokus in unserem Steuerelement/Fenster befindet.</span><span class="sxs-lookup"><span data-stu-id="a56cb-156">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>
[<span data-ttu-id="a56cb-157">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="a56cb-157">OnKeyDown</span></span>](#onkeydown) | <span data-ttu-id="a56cb-158">Dies wird von UIElement überschrieben und aufgerufen, damit wir die Eingabe von Tasten drücken verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a56cb-158">This is overridden from UIElement and called to allow us to handle key press input.</span></span>
[<span data-ttu-id="a56cb-159">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="a56cb-159">OnKeyUp</span></span>](#onkeyup) | <span data-ttu-id="a56cb-160">Siehe OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="a56cb-160">See OnKeyDown.</span></span>
[<span data-ttu-id="a56cb-161">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="a56cb-161">OnPreviewKeyDown</span></span>](#onpreviewkeydown) | <span data-ttu-id="a56cb-162">Dies ist die "Vorschau" (also</span><span class="sxs-lookup"><span data-stu-id="a56cb-162">This is the "Preview" (i.e.</span></span>
[<span data-ttu-id="a56cb-163">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="a56cb-163">OnPreviewKeyUp</span></span>](#onpreviewkeyup) | <span data-ttu-id="a56cb-164">Siehe OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="a56cb-164">See OnPreviewKeyDown.</span></span>
[<span data-ttu-id="a56cb-165">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="a56cb-165">OnWindowPositionChanged</span></span>](#onwindowpositionchanged) | <span data-ttu-id="a56cb-166">Dieser wird von HwndHost überschrieben und aufgerufen, wenn sich der Standort des Steuerelements geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a56cb-166">This is overridden from HwndHost and called when our control's location has changed.</span></span>
[<span data-ttu-id="a56cb-167">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-167">TabIntoCore</span></span>](#tabintocore) | <span data-ttu-id="a56cb-168">Dies wird von HwndHost überschrieben und wird aufgerufen, um uns mitzuteilen, dass die Tab-Taste dazu geführt hat, dass der Fokus in unser Control/Window verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-168">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

<span data-ttu-id="a56cb-169">Dieses Steuerelement ist effektiv ein Wrapper um die WebView2-com-API, in dem Sie die Dokumentation finden können: [https://aka.ms/webview2](https://aka.ms/webview2) Sie können direkt auf die zugrunde liegende ICoreWebView2-Schnittstelle und ihre gesamte Funktionalität zugreifen, indem Sie auf die CoreWebView2-Eigenschaft zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-169">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="a56cb-170">Einige der gängigsten com-Funktionen können auch direkt über Wrappermethoden/Eigenschaften/Ereignisse für das Steuerelement aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a56cb-170">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="a56cb-171">Bei der Erstellung ist die CoreWebView2-Eigenschaft des Steuerelements NULL.</span><span class="sxs-lookup"><span data-stu-id="a56cb-171">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="a56cb-172">Dies liegt daran, dass das Erstellen der CoreWebView2 eine kostspielige Operation ist, die Dinge wie das Starten von Edge-Browser-Prozessen umfasst.</span><span class="sxs-lookup"><span data-stu-id="a56cb-172">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="a56cb-173">Es gibt zwei Möglichkeiten, das Erstellen der CoreWebView2 zu veranlassen: 1) rufen Sie die EnsureCoreWebView2Async-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a56cb-173">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="a56cb-174">Dies wird als explizite Initialisierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a56cb-174">This is referred to as explicit initialization.</span></span> <span data-ttu-id="a56cb-175">2) stellen Sie die Source-Eigenschaft ein, die beispielsweise über Markup erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="a56cb-175">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="a56cb-176">Dies wird als implizite Initialisierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a56cb-176">This is referred to as implicit initialization.</span></span> <span data-ttu-id="a56cb-177">Mit einer der beiden Optionen wird die Initialisierung im Hintergrund gestartet, und Sie kehren zum Aufrufer zurück, ohne darauf zu warten, dass er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-177">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="a56cb-178">Wenn Sie Optionen für den Initialisierungsprozess angeben möchten, übergeben Sie entweder Ihr eigenes CoreWebView2Environment an EnsureCoreWebView2Async, oder legen Sie die CreationProperties-Eigenschaft des Steuerelements vor der Initialisierung fest.</span><span class="sxs-lookup"><span data-stu-id="a56cb-178">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="a56cb-179">Wenn die Initialisierung beendet wurde (unabhängig davon, wie Sie ausgelöst wurde), treten die folgenden Dinge in dieser Reihenfolge auf: 1) das CoreWebView2Ready-Ereignis des Steuerelements wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-179">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="a56cb-180">Wenn Sie vor der Verwendung eine einmalige Setup Operation für das CoreWebView2 durchführen müssen, sollten Sie dies in einem Handler für dieses Ereignis tun.</span><span class="sxs-lookup"><span data-stu-id="a56cb-180">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="a56cb-181">2) Wenn ein URI auf die Source-Eigenschaft gesetzt wurde, wird das Steuerelement im Hintergrund zu ihm navigieren (d. h., diese Schritte werden fortgesetzt, ohne darauf zu warten, dass die Navigation beendet wird).</span><span class="sxs-lookup"><span data-stu-id="a56cb-181">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="a56cb-182">3) die Aufgabe, die von EnsureCoreWebView2Async zurückgegeben wird, wird abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-182">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="a56cb-183">Weitere Informationen zu den Methoden/Eigenschaften/Ereignissen, die am Initialisierungsprozess beteiligt sind, finden Sie in der jeweiligen Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a56cb-183">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="a56cb-184">Da das CoreWebView2-Steuerelement ein sehr Schwergewichts Objekt ist (potenziell verantwortlich für mehrere ausgeführte Prozesse und Megabytes an Speicherplatz), implementiert das Steuerelement IDisposable, um eine explizite Möglichkeit zum Freigeben bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-184">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="a56cb-185">Durch Aufrufen von Dispose werden die CoreWebView2 und die zugrunde liegenden Ressourcen (mit Ausnahme der von anderen Webansichten verwendeten) freigegeben und CoreWebView2 auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a56cb-185">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="a56cb-186">Nachdem Dispose aufgerufen wurde, kann CoreWebView2 nicht erneut initialisiert werden, und jeder Versuch, die Funktionalität zu verwenden, die dies erfordert, löst eine ObjectDisposedException aus.</span><span class="sxs-lookup"><span data-stu-id="a56cb-186">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="a56cb-187">Beachten Sie, dass dieses Steuerelement HwndHost erweitert, um Fenster einzubetten, die außerhalb des WPF-Ökosystems Leben.</span><span class="sxs-lookup"><span data-stu-id="a56cb-187">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="a56cb-188">Dies hat Auswirkungen auf das Eingabe-und Ausgabeverhalten des Steuerelements sowie auf die Funktionalität, die es von UIElement und FrameworkElement erbt.</span><span class="sxs-lookup"><span data-stu-id="a56cb-188">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="a56cb-189">Weitere Informationen finden Sie in der HwndHost-und WPF/Win32-Interop-Dokumentation:</span><span class="sxs-lookup"><span data-stu-id="a56cb-189">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="a56cb-190">Member</span><span class="sxs-lookup"><span data-stu-id="a56cb-190">Members</span></span>

#### <span data-ttu-id="a56cb-191">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="a56cb-191">ContentLoading</span></span> 

<span data-ttu-id="a56cb-192">Ein Wrapper um das CoreWebView2. ContentLoading-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-192">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="a56cb-193">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="a56cb-193">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="a56cb-194">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. ContentLoading ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-194">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="a56cb-195">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. ContentLoading die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-195">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="a56cb-196">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="a56cb-196">CoreWebView2Ready</span></span> 

<span data-ttu-id="a56cb-197">Dieses Ereignis wird ausgelöst, wenn die CoreWebView2 des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-197">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="a56cb-198">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="a56cb-198">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="a56cb-199">Sie sollten dieses Ereignis behandeln, wenn Sie eine einmalige Einrichtungs Operation für die CoreWebView2 durchführen müssen, für die Sie alle ihre Verwendungen beeinflussen möchten (beispielsweise das Hinzufügen von Ereignishandlern, das Konfigurieren von Einstellungen, das Installieren von Dokument Erstellungsskripts und das Hinzufügen von Host Objekten).</span><span class="sxs-lookup"><span data-stu-id="a56cb-199">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="a56cb-200">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a56cb-200">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="a56cb-201">Dieses Ereignis stellt keine Argumente bereit, und der Absender ist das WebView2-Steuerelement, dessen CoreWebView2-Eigenschaft zum ersten Mal gültig (also ungleich null) ist.</span><span class="sxs-lookup"><span data-stu-id="a56cb-201">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="a56cb-202">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="a56cb-202">NavigationCompleted</span></span> 

<span data-ttu-id="a56cb-203">Ein Wrapper um das CoreWebView2. NavigationCompleted-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-203">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="a56cb-204">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="a56cb-204">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="a56cb-205">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. NavigationCompleted ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-205">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="a56cb-206">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. NavigationCompleted die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-206">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="a56cb-207">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="a56cb-207">NavigationStarting</span></span> 

<span data-ttu-id="a56cb-208">Ein Wrapper um das CoreWebView2. NavigationStarting-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-208">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="a56cb-209">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="a56cb-209">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="a56cb-210">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. NavigationStarting ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-210">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="a56cb-211">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. NavigationStarting die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-211">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="a56cb-212">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="a56cb-212">SourceChanged</span></span> 

<span data-ttu-id="a56cb-213">Ein Wrapper um das CoreWebView2. Sourcecode-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-213">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="a56cb-214">public event EventHandler< CoreWebView2SourceChangedEventArgs > [Quelle](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="a56cb-214">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="a56cb-215">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. Sourcecode ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-215">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="a56cb-216">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. sourced die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-216">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="a56cb-217">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="a56cb-217">WebMessageReceived</span></span> 

<span data-ttu-id="a56cb-218">Ein Wrapper um das CoreWebView2. WebMessageReceived-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-218">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="a56cb-219">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="a56cb-219">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="a56cb-220">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. WebMessageReceived ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-220">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="a56cb-221">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. WebMessageReceived die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-221">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="a56cb-222">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="a56cb-222">CanGoBack</span></span> 

<span data-ttu-id="a56cb-223">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="a56cb-223">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="a56cb-224">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="a56cb-224">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="a56cb-225">Wrapper um die CoreWebView2. CanGoBack-Eigenschaft von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-225">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="a56cb-226">Wenn CoreWebView2 noch nicht initialisiert ist, wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a56cb-226">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="a56cb-227">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="a56cb-227">CanGoForward</span></span> 

<span data-ttu-id="a56cb-228">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="a56cb-228">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="a56cb-229">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="a56cb-229">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="a56cb-230">Wrapper um die CoreWebView2. CanGoForward-Eigenschaft von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-230">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="a56cb-231">Wenn CoreWebView2 noch nicht initialisiert ist, wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a56cb-231">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="a56cb-232">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-232">CoreWebView2</span></span> 

<span data-ttu-id="a56cb-233">Greifen Sie auf die vollständige Funktionalität der zugrunde liegenden Core. CoreWebView2-com-API zu.</span><span class="sxs-lookup"><span data-stu-id="a56cb-233">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="a56cb-234">öffentliche CoreWebView2- [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="a56cb-234">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="a56cb-235">Gibt NULL zurück, bis die Initialisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a56cb-235">Returns null until initialization has completed.</span></span> <span data-ttu-id="a56cb-236">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a56cb-236">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="a56cb-237">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-237">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-238">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-238">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="a56cb-239">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="a56cb-239">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="a56cb-240">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-240">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-241">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="a56cb-241">CreationProperties</span></span> 

<span data-ttu-id="a56cb-242">Ruft eine Sammlung von Optionen ab, die während der Initialisierung des CoreWebView2 des Steuerelements verwendet werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a56cb-242">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="a56cb-243">öffentliche CoreWebView2CreationProperties- [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="a56cb-243">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="a56cb-244">Das Festlegen dieser Eigenschaft funktioniert nicht, nachdem die Initialisierung des CoreWebView2 des Steuerelements begonnen hat (der alte Wert bleibt erhalten).</span><span class="sxs-lookup"><span data-stu-id="a56cb-244">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="a56cb-245">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a56cb-245">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="a56cb-246">Source</span><span class="sxs-lookup"><span data-stu-id="a56cb-246">Source</span></span> 

<span data-ttu-id="a56cb-247">Der URI der obersten Ebene, den die WebView aktuell anzeigt (oder wird angezeigt, sobald die Initialisierung des CoreWebView2-Endgeräts endet).</span><span class="sxs-lookup"><span data-stu-id="a56cb-247">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="a56cb-248">öffentliche URI- [Quelle](#source)</span><span class="sxs-lookup"><span data-stu-id="a56cb-248">public Uri [Source](#source)</span></span>

<span data-ttu-id="a56cb-249">Im Allgemeinen entspricht das Abrufen dieser Eigenschaft dem Abrufen der CoreWebView2. Source-Eigenschaft von CoreWebView2, und das Festlegen dieser Eigenschaft entspricht dem Aufrufen der CoreWebView2. Navigate-Methode für CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-249">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="a56cb-250">Wenn Sie diese Eigenschaft abrufen, bevor die CoreWebView2 initialisiert wurde, wird der letzte URI abgerufen, der auf ihn gesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-250">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="a56cb-251">Wenn diese Eigenschaft vor dem Initialisieren der CoreWebView2-Eigenschaft festgelegt wurde, wird die Initialisierung im Hintergrund gestartet (falls Sie noch nicht ausgeführt wird), nachdem die WebView2 zum angegebenen URI navigiert.</span><span class="sxs-lookup"><span data-stu-id="a56cb-251">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="a56cb-252">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a56cb-252">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="a56cb-253">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-253">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="a56cb-254">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-255">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="a56cb-255">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="a56cb-256">Initialisierung der CoreWebView2 des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-256">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="a56cb-257">öffentliche Aufgaben- [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="a56cb-257">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="a56cb-258">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a56cb-258">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="a56cb-259">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56cb-259">Parameters</span></span>
* `environment` <span data-ttu-id="a56cb-260">Eine zuvor erstellte CoreWebView2Environment, die zum Erstellen des CoreWebView2 verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a56cb-260">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="a56cb-261">Durch das Erstellen einer eigenen Umgebung können Sie verschiedene Optionen steuern, die sich auf die Initialisierung des CoreWebView2 auswirken.</span><span class="sxs-lookup"><span data-stu-id="a56cb-261">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="a56cb-262">Wenn Sie eine Umgebung an diese Methode übergeben, werden alle in der CreationProperties-Eigenschaft angegebenen Einstellungen außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="a56cb-262">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="a56cb-263">Wenn Sie NULL (den Standardwert) übergeben und kein Wert auf CreationProperties festgesetzt wurde, wird eine Standardumgebung erstellt und automatisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="a56cb-263">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="a56cb-264">Gibt</span><span class="sxs-lookup"><span data-stu-id="a56cb-264">Returns</span></span>
<span data-ttu-id="a56cb-265">Eine Aufgabe, die den Hintergrund Initialisierungsprozess darstellt.</span><span class="sxs-lookup"><span data-stu-id="a56cb-265">A Task that represents the background initialization process.</span></span> <span data-ttu-id="a56cb-266">Wenn die Aufgabe abgeschlossen ist, steht die CoreWebView2-Eigenschaft zur Verwendung zur Verfügung (also nicht-null).</span><span class="sxs-lookup"><span data-stu-id="a56cb-266">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="a56cb-267">Beachten Sie, dass das CoreWebView2Ready-Ereignis des Steuerelements aufgerufen wird, bevor die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a56cb-267">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="a56cb-268">Das zusätzliche Aufrufen dieser Methode hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt dieselbe Aufgabe wie beim ersten Aufruf zurück.</span><span class="sxs-lookup"><span data-stu-id="a56cb-268">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="a56cb-269">Das Aufrufen dieser Methode, nachdem die Initialisierung implizit ausgelöst wurde, indem die Source-Eigenschaft festgelegt wird, hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt einfach eine Aufgabe zurück, die die bereits ausgeführte Initialisierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="a56cb-269">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="a56cb-270">Beachten Sie, dass auch wenn diese Methode asynchron ist und eine Aufgabe zurückgibt, Sie dennoch im UI-Thread aufgerufen werden muss, wie die meisten öffentlichen Funktionen der meisten UI-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a56cb-270">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="a56cb-271">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-271">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-272">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-272">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="a56cb-273">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="a56cb-273">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="a56cb-274">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-274">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-275">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="a56cb-275">ExecuteScriptAsync</span></span> 

<span data-ttu-id="a56cb-276">Führt JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-276">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="a56cb-277">Public Async Task< String > [ExecuteScriptAsync](#executescriptasync)(String javaScript)</span><span class="sxs-lookup"><span data-stu-id="a56cb-277">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="a56cb-278">Entspricht dem Aufrufen von CoreWebView2. ExecuteScriptAsync auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-278">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="a56cb-279">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-279">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-280">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-280">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="a56cb-281">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-281">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="a56cb-282">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="a56cb-282">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="a56cb-283">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-283">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-284">GoBack</span><span class="sxs-lookup"><span data-stu-id="a56cb-284">GoBack</span></span> 

<span data-ttu-id="a56cb-285">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="a56cb-285">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="a56cb-286">publicvoid [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="a56cb-286">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="a56cb-287">Entspricht dem Aufrufen von CoreWebView2. GoBack auf CoreWebView2, wenn CoreWebView2 noch nicht initialisiert wurde, dann aber nichts tut.</span><span class="sxs-lookup"><span data-stu-id="a56cb-287">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="a56cb-288">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-288">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-289">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-289">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="a56cb-290">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="a56cb-290">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="a56cb-291">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-291">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-292">GoForward</span><span class="sxs-lookup"><span data-stu-id="a56cb-292">GoForward</span></span> 

<span data-ttu-id="a56cb-293">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="a56cb-293">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="a56cb-294">publicvoid [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="a56cb-294">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="a56cb-295">Entspricht dem Aufrufen von CoreWebView2. GoForward auf CoreWebView2, wenn CoreWebView2 noch nicht initialisiert wurde, dann aber nichts tut.</span><span class="sxs-lookup"><span data-stu-id="a56cb-295">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="a56cb-296">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-296">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-297">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-297">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="a56cb-298">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="a56cb-298">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="a56cb-299">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-299">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-300">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="a56cb-300">NavigateToString</span></span> 

<span data-ttu-id="a56cb-301">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="a56cb-301">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="a56cb-302">publicvoid [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="a56cb-302">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="a56cb-303">Entspricht dem Aufrufen von CoreWebView2. NavigateToString auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-303">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="a56cb-304">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-304">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-305">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-305">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="a56cb-306">" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-306">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="a56cb-307">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-307">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-308">Laden</span><span class="sxs-lookup"><span data-stu-id="a56cb-308">Reload</span></span> 

<span data-ttu-id="a56cb-309">Lädt die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="a56cb-309">Reloads the current page.</span></span>

> <span data-ttu-id="a56cb-310">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="a56cb-310">public void [Reload](#reload)()</span></span>

<span data-ttu-id="a56cb-311">Entspricht dem Aufruf von CoreWebView2. Reload auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-311">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="a56cb-312">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-312">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-313">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-313">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="a56cb-314">" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-314">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="a56cb-315">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-315">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-316">Stop</span><span class="sxs-lookup"><span data-stu-id="a56cb-316">Stop</span></span> 

<span data-ttu-id="a56cb-317">Stoppt alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="a56cb-317">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="a56cb-318">öffentlicher void- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="a56cb-318">public void [Stop](#stop)()</span></span>

<span data-ttu-id="a56cb-319">Entspricht dem Aufruf von CoreWebView2. Stop auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-319">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="a56cb-320">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a56cb-320">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="a56cb-321">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-321">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="a56cb-322">" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="a56cb-322">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="a56cb-323">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-323">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="a56cb-324">WebView2</span><span class="sxs-lookup"><span data-stu-id="a56cb-324">WebView2</span></span> 

<span data-ttu-id="a56cb-325">Erstellt eine neue Instanz eines WebView2-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="a56cb-325">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="a56cb-326">Public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="a56cb-326">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="a56cb-327">Beachten Sie, dass der CoreWebView2 des Steuerelements bis zur Initialisierung NULL ist.</span><span class="sxs-lookup"><span data-stu-id="a56cb-327">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="a56cb-328">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a56cb-328">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="a56cb-329">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-329">BuildWindowCore</span></span> 

<span data-ttu-id="a56cb-330">Dies wird von HwndHost überschrieben und aufgerufen, um uns zu beauftragen, unser HWND zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-330">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>

> <span data-ttu-id="a56cb-331">protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span><span class="sxs-lookup"><span data-stu-id="a56cb-331">protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span></span>

##### <span data-ttu-id="a56cb-332">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56cb-332">Parameters</span></span>
* `hwndParent` <span data-ttu-id="a56cb-333">Das HWND, das wir als übergeordnetes Element des erstellten verwenden sollen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-333">The HWND that we should use as the parent of the one we create.</span></span>

##### <span data-ttu-id="a56cb-334">Gibt</span><span class="sxs-lookup"><span data-stu-id="a56cb-334">Returns</span></span>
<span data-ttu-id="a56cb-335">Das von uns erstellte HWND.</span><span class="sxs-lookup"><span data-stu-id="a56cb-335">The HWND that we created.</span></span>

#### <span data-ttu-id="a56cb-336">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-336">DestroyWindowCore</span></span> 

<span data-ttu-id="a56cb-337">Dies wird von HwndHost überschrieben und aufgerufen, um uns anzuweisen, unser HWND zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="a56cb-337">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>

> <span data-ttu-id="a56cb-338">protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef HWND)</span><span class="sxs-lookup"><span data-stu-id="a56cb-338">protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef hwnd)</span></span>

##### <span data-ttu-id="a56cb-339">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56cb-339">Parameters</span></span>
* `hwnd` <span data-ttu-id="a56cb-340">Unser HWND, das wir zerstören müssen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-340">Our HWND that we need to destroy.</span></span>

#### <span data-ttu-id="a56cb-341">Löschen</span><span class="sxs-lookup"><span data-stu-id="a56cb-341">Dispose</span></span> 

<span data-ttu-id="a56cb-342">Dies wird von unserer Basisklasse entsprechend der typischen Implementierung des IDispose-Musters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-342">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>

> <span data-ttu-id="a56cb-343">protected override void [Dispose](#dispose)(bool disposing)</span><span class="sxs-lookup"><span data-stu-id="a56cb-343">protected override void [Dispose](#dispose)(bool disposing)</span></span>

<span data-ttu-id="a56cb-344">Wir implementieren es durch die Freigabe aller zugrunde liegenden com-Ressourcen, einschließlich unserer CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a56cb-344">We implement it by releasing all of our underlying COM resources, including our CoreWebView2.</span></span>

##### <span data-ttu-id="a56cb-345">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56cb-345">Parameters</span></span>
* `disposing` <span data-ttu-id="a56cb-346">True, wenn ein Aufrufer explizit Dispose aufruft, false, wenn wir finalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a56cb-346">True if a caller is explicitly calling Dispose, false if we're being finalized.</span></span>

#### <span data-ttu-id="a56cb-347">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-347">HasFocusWithinCore</span></span> 

<span data-ttu-id="a56cb-348">Dies wird von HwndHost überschrieben und aufgerufen, wenn WPF wissen muss, ob sich der Fokus in unserem Steuerelement/Fenster befindet.</span><span class="sxs-lookup"><span data-stu-id="a56cb-348">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>

> <span data-ttu-id="a56cb-349">protected override bool [HasFocusWithinCore](#hasfocuswithincore)()</span><span class="sxs-lookup"><span data-stu-id="a56cb-349">protected override bool [HasFocusWithinCore](#hasfocuswithincore)()</span></span>

<span data-ttu-id="a56cb-350">WPF kann nicht alleine wissen, da wir ein nicht-WPF-Fenster hosten, stattdessen fragt es uns, indem wir dies aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-350">WPF can't know on its own since we're hosting a non-WPF window, so instead it asks us by calling this.</span></span> <span data-ttu-id="a56cb-351">Zur Beantwortung wird der Zustand auf der Grundlage von CoreWebView2-Ereignissen, die ausgelöst werden, wenn er den Fokus erhält oder verliert, einfach nach vollführt.</span><span class="sxs-lookup"><span data-stu-id="a56cb-351">To answer, we just track state based on CoreWebView2 events that fire when it gains or loses focus.</span></span>

##### <span data-ttu-id="a56cb-352">Gibt</span><span class="sxs-lookup"><span data-stu-id="a56cb-352">Returns</span></span>
<span data-ttu-id="a56cb-353">True, wenn sich der Fokus in unserem Control/Window befindet, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="a56cb-353">True if the focus is in our control/window, false if it isn't.</span></span>

#### <span data-ttu-id="a56cb-354">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="a56cb-354">OnKeyDown</span></span> 

<span data-ttu-id="a56cb-355">Dies wird von UIElement überschrieben und aufgerufen, damit wir die Eingabe von Tasten drücken verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a56cb-355">This is overridden from UIElement and called to allow us to handle key press input.</span></span>

> <span data-ttu-id="a56cb-356">protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="a56cb-356">protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="a56cb-357">WPF sollte diesen Anruf eigentlich nie als Antwort auf Tastaturereignisse aufrufen, da wir ein nicht-WPF-Fenster hosten.</span><span class="sxs-lookup"><span data-stu-id="a56cb-357">WPF should never actually call this in response to keyboard events because we're hosting a non-WPF window.</span></span> <span data-ttu-id="a56cb-358">Wenn unser Fenster den Fokus hat, sendet Windows die Eingabe direkt an Sie, anstatt an das WPF-Fenster auf oberster Ebene und an das Eingabesystem.</span><span class="sxs-lookup"><span data-stu-id="a56cb-358">When our window has focus Windows will send the input directly to it rather than to WPF's top-level window and input system.</span></span> <span data-ttu-id="a56cb-359">Diese Außerkraftsetzung sollte nur aufgerufen werden, wenn wir die Zugriffstasten Eingabe aus dem CoreWebView2 explizit an WPF (in CoreWebView2Controller_AcceleratorKeyPressed) weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="a56cb-359">This override should only be called when we're explicitly forwarding accelerator key input from the CoreWebView2 to WPF (in CoreWebView2Controller_AcceleratorKeyPressed).</span></span> <span data-ttu-id="a56cb-360">Selbst dann wird diese KeyDownEvent nur ausgelöst, weil Sie von unserer PreviewKeyDownEvent-Implementierung explizit ausgelöst wird, die dem normalen WPF-System entspricht.</span><span class="sxs-lookup"><span data-stu-id="a56cb-360">Even then, this KeyDownEvent is only triggered because our PreviewKeyDownEvent implementation explicitly triggers it, matching WPF's usual system.</span></span> <span data-ttu-id="a56cb-361">Der Prozess lautet also: CoreWebView2Controller_AcceleratorKeyPressed > Raise PreviewKeyDownEvent-> OnPreviewKeyDown-> Raise KeyDownEvent-> OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="a56cb-361">So the process is: CoreWebView2Controller_AcceleratorKeyPressed -> raise PreviewKeyDownEvent -> OnPreviewKeyDown -> raise KeyDownEvent -> OnKeyDown</span></span>

#### <span data-ttu-id="a56cb-362">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="a56cb-362">OnKeyUp</span></span> 

<span data-ttu-id="a56cb-363">Siehe OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="a56cb-363">See OnKeyDown.</span></span>

> <span data-ttu-id="a56cb-364">protected override void [onkeyup](#onkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="a56cb-364">protected override void [OnKeyUp](#onkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="a56cb-365">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="a56cb-365">OnPreviewKeyDown</span></span> 

<span data-ttu-id="a56cb-366">Dies ist die "Vorschau" (also</span><span class="sxs-lookup"><span data-stu-id="a56cb-366">This is the "Preview" (i.e.</span></span>

> <span data-ttu-id="a56cb-367">protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="a56cb-367">protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="a56cb-368">Tunneling)-Version von OnKeyDown aus, sodass dies zunächst geschieht.</span><span class="sxs-lookup"><span data-stu-id="a56cb-368">tunneling) version of OnKeyDown, so it actually happens first.</span></span> <span data-ttu-id="a56cb-369">Wie OnKeyDown wird dies immer nur aufgerufen, wenn wir die Schlüsselpressen explizit aus dem CoreWebView2 weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="a56cb-369">Like OnKeyDown, this will only ever be called if we're explicitly forwarding key presses from the CoreWebView2.</span></span> <span data-ttu-id="a56cb-370">Um die Standardeingabe Behandlung von WPF nachzuahmen, wenn wir dies erhalten, drehen wir den standardmäßigen sprudelnden KeyDownEvent um und zünden ihn an.</span><span class="sxs-lookup"><span data-stu-id="a56cb-370">In order to mimic WPF's standard input handling, when we receive this we turn around and fire off the standard bubbling KeyDownEvent.</span></span> <span data-ttu-id="a56cb-371">Auf diese Weise sehen andere in der WPF-Struktur dasselbe Standardpaar von Eingabeereignissen, die von WPF selbst ausgelöst wurden, wenn Sie die Tastenkombination verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a56cb-371">That way others in the WPF tree see the same standard pair of input events that WPF itself would have triggered if it were handling the key press.</span></span>

#### <span data-ttu-id="a56cb-372">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="a56cb-372">OnPreviewKeyUp</span></span> 

<span data-ttu-id="a56cb-373">Siehe OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="a56cb-373">See OnPreviewKeyDown.</span></span>

> <span data-ttu-id="a56cb-374">protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="a56cb-374">protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="a56cb-375">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="a56cb-375">OnWindowPositionChanged</span></span> 

<span data-ttu-id="a56cb-376">Dieser wird von HwndHost überschrieben und aufgerufen, wenn sich der Standort des Steuerelements geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a56cb-376">This is overridden from HwndHost and called when our control's location has changed.</span></span>

> <span data-ttu-id="a56cb-377">protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span><span class="sxs-lookup"><span data-stu-id="a56cb-377">protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span></span>

<span data-ttu-id="a56cb-378">HwndHost sorgt für die Aktualisierung des von uns erstellten HWNDs.</span><span class="sxs-lookup"><span data-stu-id="a56cb-378">The HwndHost takes care of updating the HWND we created.</span></span> <span data-ttu-id="a56cb-379">Wir müssen unsere CoreWebView2 so verschieben, dass Sie dem neuen Standort entspricht.</span><span class="sxs-lookup"><span data-stu-id="a56cb-379">What we need to do is move our CoreWebView2 to match the new location.</span></span>

#### <span data-ttu-id="a56cb-380">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="a56cb-380">TabIntoCore</span></span> 

<span data-ttu-id="a56cb-381">Dies wird von HwndHost überschrieben und wird aufgerufen, um uns mitzuteilen, dass die Tab-Taste dazu geführt hat, dass der Fokus in unser Control/Window verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="a56cb-381">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

> <span data-ttu-id="a56cb-382">protected override bool [TabIntoCore](#tabintocore)(TraversalRequest Request)</span><span class="sxs-lookup"><span data-stu-id="a56cb-382">protected override bool [TabIntoCore](#tabintocore)(TraversalRequest request)</span></span>

<span data-ttu-id="a56cb-383">Da WPF den Übergang des Fokus nicht in ein nicht-WPF-HWND verwalten kann, wird hier der Übergang an uns delegiert.</span><span class="sxs-lookup"><span data-stu-id="a56cb-383">Since WPF can't manage the transition of focus to a non-WPF HWND, it delegates the transition to us here.</span></span> <span data-ttu-id="a56cb-384">Unsere Aufgabe ist es also, den Fokus auf unser externes HWND zu legen.</span><span class="sxs-lookup"><span data-stu-id="a56cb-384">So our job is just to place the focus in our external HWND.</span></span>

##### <span data-ttu-id="a56cb-385">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56cb-385">Parameters</span></span>
* `request` <span data-ttu-id="a56cb-386">Informationen dazu, wie der Fokus verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a56cb-386">Information about how the focus is moving.</span></span>

##### <span data-ttu-id="a56cb-387">Gibt</span><span class="sxs-lookup"><span data-stu-id="a56cb-387">Returns</span></span>
<span data-ttu-id="a56cb-388">"True", um anzugeben, dass die Navigation gehandhabt wurde, oder "false", um anzugeben, dass dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="a56cb-388">True to indicate that we handled the navigation, or false to indicate that we didn't.</span></span>

