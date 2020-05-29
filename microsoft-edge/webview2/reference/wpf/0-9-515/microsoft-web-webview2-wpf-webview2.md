---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a0030e1a2a77d65963bd8333f2071485ab2fe308
ms.sourcegitcommit: 83efa259be89cc773a82751242495a0a919d54cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "10687797"
---
# <span data-ttu-id="c292e-104">Microsoft. Web. WebView2. WPF. WebView2 Klasse</span><span class="sxs-lookup"><span data-stu-id="c292e-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="c292e-105">Namespace: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="c292e-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="c292e-106">Assembly: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="c292e-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="c292e-107">Ein Steuerelement zum Einbetten von Webinhalten in eine WPF-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c292e-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="c292e-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c292e-108">Summary</span></span>

 <span data-ttu-id="c292e-109">Member</span><span class="sxs-lookup"><span data-stu-id="c292e-109">Members</span></span>                        | <span data-ttu-id="c292e-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c292e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c292e-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="c292e-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="c292e-112">Ein Wrapper um das CoreWebView2. ContentLoading-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="c292e-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="c292e-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="c292e-114">Dieses Ereignis wird ausgelöst, wenn die CoreWebView2 des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="c292e-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="c292e-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="c292e-116">Ein Wrapper um das CoreWebView2. NavigationCompleted-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="c292e-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="c292e-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="c292e-118">Ein Wrapper um das CoreWebView2. NavigationStarting-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="c292e-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="c292e-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="c292e-120">Ein Wrapper um das CoreWebView2. Sourcecode-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="c292e-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="c292e-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="c292e-122">Ein Wrapper um das CoreWebView2. WebMessageReceived-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="c292e-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="c292e-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="c292e-124">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="c292e-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="c292e-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="c292e-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="c292e-126">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="c292e-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="c292e-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="c292e-128">Greifen Sie auf die vollständige Funktionalität der zugrunde liegenden Core. CoreWebView2-com-API zu.</span><span class="sxs-lookup"><span data-stu-id="c292e-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="c292e-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="c292e-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="c292e-130">Ruft eine Sammlung von Optionen ab, die während der Initialisierung des CoreWebView2 des Steuerelements verwendet werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c292e-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="c292e-131">Source</span><span class="sxs-lookup"><span data-stu-id="c292e-131">Source</span></span>](#source) | <span data-ttu-id="c292e-132">Der URI der obersten Ebene, den die WebView aktuell anzeigt (oder wird angezeigt, sobald die Initialisierung des CoreWebView2-Endgeräts endet).</span><span class="sxs-lookup"><span data-stu-id="c292e-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="c292e-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="c292e-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="c292e-134">Initialisierung der CoreWebView2 des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="c292e-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="c292e-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="c292e-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="c292e-136">Führt JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="c292e-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="c292e-137">GoBack</span></span>](#goback) | <span data-ttu-id="c292e-138">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="c292e-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="c292e-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="c292e-139">GoForward</span></span>](#goforward) | <span data-ttu-id="c292e-140">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="c292e-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="c292e-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="c292e-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="c292e-142">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="c292e-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="c292e-143">Laden</span><span class="sxs-lookup"><span data-stu-id="c292e-143">Reload</span></span>](#reload) | <span data-ttu-id="c292e-144">Lädt die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="c292e-144">Reloads the current page.</span></span>
[<span data-ttu-id="c292e-145">Stop</span><span class="sxs-lookup"><span data-stu-id="c292e-145">Stop</span></span>](#stop) | <span data-ttu-id="c292e-146">Stoppt alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="c292e-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="c292e-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-147">WebView2</span></span>](#webview2) | <span data-ttu-id="c292e-148">Erstellt eine neue Instanz eines WebView2-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="c292e-148">Creates a new instance of a WebView2 control.</span></span>

<span data-ttu-id="c292e-149">Dieses Steuerelement ist effektiv ein Wrapper um die WebView2-com-API, in dem Sie die Dokumentation finden können: [https://aka.ms/webview2](https://aka.ms/webview2) Sie können direkt auf die zugrunde liegende ICoreWebView2-Schnittstelle und ihre gesamte Funktionalität zugreifen, indem Sie auf die CoreWebView2-Eigenschaft zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c292e-149">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="c292e-150">Einige der gängigsten com-Funktionen können auch direkt über Wrappermethoden/Eigenschaften/Ereignisse für das Steuerelement aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c292e-150">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="c292e-151">Bei der Erstellung ist die CoreWebView2-Eigenschaft des Steuerelements NULL.</span><span class="sxs-lookup"><span data-stu-id="c292e-151">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="c292e-152">Dies liegt daran, dass das Erstellen der CoreWebView2 eine kostspielige Operation ist, die Dinge wie das Starten von Edge-Browser-Prozessen umfasst.</span><span class="sxs-lookup"><span data-stu-id="c292e-152">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="c292e-153">Es gibt zwei Möglichkeiten, das Erstellen der CoreWebView2 zu veranlassen: 1) rufen Sie die EnsureCoreWebView2Async-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="c292e-153">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="c292e-154">Dies wird als explizite Initialisierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c292e-154">This is referred to as explicit initialization.</span></span> <span data-ttu-id="c292e-155">2) stellen Sie die Source-Eigenschaft ein, die beispielsweise über Markup erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="c292e-155">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="c292e-156">Dies wird als implizite Initialisierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c292e-156">This is referred to as implicit initialization.</span></span> <span data-ttu-id="c292e-157">Mit einer der beiden Optionen wird die Initialisierung im Hintergrund gestartet, und Sie kehren zum Aufrufer zurück, ohne darauf zu warten, dass er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-157">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="c292e-158">Wenn Sie Optionen für den Initialisierungsprozess angeben möchten, übergeben Sie entweder Ihr eigenes CoreWebView2Environment an EnsureCoreWebView2Async, oder legen Sie die CreationProperties-Eigenschaft des Steuerelements vor der Initialisierung fest.</span><span class="sxs-lookup"><span data-stu-id="c292e-158">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="c292e-159">Wenn die Initialisierung beendet wurde (unabhängig davon, wie Sie ausgelöst wurde), treten die folgenden Dinge in dieser Reihenfolge auf: 1) das CoreWebView2Ready-Ereignis des Steuerelements wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c292e-159">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="c292e-160">Wenn Sie vor der Verwendung eine einmalige Setup Operation für das CoreWebView2 durchführen müssen, sollten Sie dies in einem Handler für dieses Ereignis tun.</span><span class="sxs-lookup"><span data-stu-id="c292e-160">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="c292e-161">2) Wenn ein URI auf die Source-Eigenschaft gesetzt wurde, wird das Steuerelement im Hintergrund zu ihm navigieren (d. h., diese Schritte werden fortgesetzt, ohne darauf zu warten, dass die Navigation beendet wird).</span><span class="sxs-lookup"><span data-stu-id="c292e-161">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="c292e-162">3) die Aufgabe, die von EnsureCoreWebView2Async zurückgegeben wird, wird abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c292e-162">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="c292e-163">Weitere Informationen zu den Methoden/Eigenschaften/Ereignissen, die am Initialisierungsprozess beteiligt sind, finden Sie in der jeweiligen Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c292e-163">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="c292e-164">Da das CoreWebView2-Steuerelement ein sehr Schwergewichts Objekt ist (potenziell verantwortlich für mehrere ausgeführte Prozesse und Megabytes an Speicherplatz), implementiert das Steuerelement IDisposable, um eine explizite Möglichkeit zum Freigeben bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c292e-164">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="c292e-165">Durch Aufrufen von Dispose werden die CoreWebView2 und die zugrunde liegenden Ressourcen (mit Ausnahme der von anderen Webansichten verwendeten) freigegeben und CoreWebView2 auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c292e-165">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="c292e-166">Nachdem Dispose aufgerufen wurde, kann CoreWebView2 nicht erneut initialisiert werden, und jeder Versuch, die Funktionalität zu verwenden, die dies erfordert, löst eine ObjectDisposedException aus.</span><span class="sxs-lookup"><span data-stu-id="c292e-166">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="c292e-167">Beachten Sie, dass dieses Steuerelement HwndHost erweitert, um Fenster einzubetten, die außerhalb des WPF-Ökosystems Leben.</span><span class="sxs-lookup"><span data-stu-id="c292e-167">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="c292e-168">Dies hat Auswirkungen auf das Eingabe-und Ausgabeverhalten des Steuerelements sowie auf die Funktionalität, die es von UIElement und FrameworkElement erbt.</span><span class="sxs-lookup"><span data-stu-id="c292e-168">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="c292e-169">Weitere Informationen finden Sie in der HwndHost-und WPF/Win32-Interop-Dokumentation:</span><span class="sxs-lookup"><span data-stu-id="c292e-169">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="c292e-170">Member</span><span class="sxs-lookup"><span data-stu-id="c292e-170">Members</span></span>

#### <span data-ttu-id="c292e-171">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="c292e-171">ContentLoading</span></span> 

<span data-ttu-id="c292e-172">Ein Wrapper um das CoreWebView2. ContentLoading-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-172">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="c292e-173">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="c292e-173">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="c292e-174">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. ContentLoading ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-174">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="c292e-175">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. ContentLoading die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="c292e-175">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="c292e-176">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="c292e-176">CoreWebView2Ready</span></span> 

<span data-ttu-id="c292e-177">Dieses Ereignis wird ausgelöst, wenn die CoreWebView2 des Steuerelements initialisiert wurde (unabhängig davon, wie die Initialisierung ausgelöst wurde), aber bevor Sie für irgendetwas verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-177">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="c292e-178">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="c292e-178">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="c292e-179">Sie sollten dieses Ereignis behandeln, wenn Sie eine einmalige Einrichtungs Operation für die CoreWebView2 durchführen müssen, für die Sie alle ihre Verwendungen beeinflussen möchten (beispielsweise das Hinzufügen von Ereignishandlern, das Konfigurieren von Einstellungen, das Installieren von Dokument Erstellungsskripts und das Hinzufügen von Host Objekten).</span><span class="sxs-lookup"><span data-stu-id="c292e-179">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="c292e-180">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="c292e-180">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="c292e-181">Dieses Ereignis stellt keine Argumente bereit, und der Absender ist das WebView2-Steuerelement, dessen CoreWebView2-Eigenschaft zum ersten Mal gültig (also ungleich null) ist.</span><span class="sxs-lookup"><span data-stu-id="c292e-181">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="c292e-182">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="c292e-182">NavigationCompleted</span></span> 

<span data-ttu-id="c292e-183">Ein Wrapper um das CoreWebView2. NavigationCompleted-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-183">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="c292e-184">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="c292e-184">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="c292e-185">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. NavigationCompleted ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-185">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="c292e-186">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. NavigationCompleted die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="c292e-186">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="c292e-187">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="c292e-187">NavigationStarting</span></span> 

<span data-ttu-id="c292e-188">Ein Wrapper um das CoreWebView2. NavigationStarting-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-188">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="c292e-189">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="c292e-189">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="c292e-190">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. NavigationStarting ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-190">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="c292e-191">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. NavigationStarting die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="c292e-191">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="c292e-192">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="c292e-192">SourceChanged</span></span> 

<span data-ttu-id="c292e-193">Ein Wrapper um das CoreWebView2. Sourcecode-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-193">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="c292e-194">public event EventHandler< CoreWebView2SourceChangedEventArgs > [Quelle](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="c292e-194">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="c292e-195">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. Sourcecode ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-195">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="c292e-196">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. sourced die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="c292e-196">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="c292e-197">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="c292e-197">WebMessageReceived</span></span> 

<span data-ttu-id="c292e-198">Ein Wrapper um das CoreWebView2. WebMessageReceived-Ereignis von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-198">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="c292e-199">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="c292e-199">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="c292e-200">Der einzige Unterschied zwischen diesem Ereignis und CoreWebView2. WebMessageReceived ist der erste Parameter, der an Handler übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-200">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="c292e-201">Handler dieses Ereignisses empfangen das WebView2-Steuerelement, während Handler von CoreWebView2. WebMessageReceived die CoreWebView2-Instanz empfangen.</span><span class="sxs-lookup"><span data-stu-id="c292e-201">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="c292e-202">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="c292e-202">CanGoBack</span></span> 

<span data-ttu-id="c292e-203">Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="c292e-203">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="c292e-204">public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="c292e-204">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="c292e-205">Wrapper um die CoreWebView2. CanGoBack-Eigenschaft von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-205">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="c292e-206">Wenn CoreWebView2 noch nicht initialisiert ist, wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c292e-206">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="c292e-207">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="c292e-207">CanGoForward</span></span> 

<span data-ttu-id="c292e-208">Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="c292e-208">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="c292e-209">public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="c292e-209">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="c292e-210">Wrapper um die CoreWebView2. CanGoForward-Eigenschaft von CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-210">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="c292e-211">Wenn CoreWebView2 noch nicht initialisiert ist, wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c292e-211">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="c292e-212">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-212">CoreWebView2</span></span> 

<span data-ttu-id="c292e-213">Greifen Sie auf die vollständige Funktionalität der zugrunde liegenden Core. CoreWebView2-com-API zu.</span><span class="sxs-lookup"><span data-stu-id="c292e-213">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="c292e-214">öffentliche CoreWebView2- [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="c292e-214">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="c292e-215">Gibt NULL zurück, bis die Initialisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c292e-215">Returns null until initialization has completed.</span></span> <span data-ttu-id="c292e-216">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="c292e-216">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="c292e-217">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-217">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-218">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-218">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="c292e-219">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="c292e-219">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="c292e-220">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-220">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-221">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="c292e-221">CreationProperties</span></span> 

<span data-ttu-id="c292e-222">Ruft eine Sammlung von Optionen ab, die während der Initialisierung des CoreWebView2 des Steuerelements verwendet werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c292e-222">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="c292e-223">öffentliche CoreWebView2CreationProperties- [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="c292e-223">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="c292e-224">Das Festlegen dieser Eigenschaft funktioniert nicht, nachdem die Initialisierung des CoreWebView2 des Steuerelements begonnen hat (der alte Wert bleibt erhalten).</span><span class="sxs-lookup"><span data-stu-id="c292e-224">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="c292e-225">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="c292e-225">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="c292e-226">Source</span><span class="sxs-lookup"><span data-stu-id="c292e-226">Source</span></span> 

<span data-ttu-id="c292e-227">Der URI der obersten Ebene, den die WebView aktuell anzeigt (oder wird angezeigt, sobald die Initialisierung des CoreWebView2-Endgeräts endet).</span><span class="sxs-lookup"><span data-stu-id="c292e-227">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="c292e-228">öffentliche URI- [Quelle](#source)</span><span class="sxs-lookup"><span data-stu-id="c292e-228">public Uri [Source](#source)</span></span>

<span data-ttu-id="c292e-229">Im Allgemeinen entspricht das Abrufen dieser Eigenschaft dem Abrufen der CoreWebView2. Source-Eigenschaft von CoreWebView2, und das Festlegen dieser Eigenschaft entspricht dem Aufrufen der CoreWebView2. Navigate-Methode für CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="c292e-229">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="c292e-230">Wenn Sie diese Eigenschaft abrufen, bevor die CoreWebView2 initialisiert wurde, wird der letzte URI abgerufen, der auf ihn gesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-230">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="c292e-231">Wenn diese Eigenschaft vor dem Initialisieren der CoreWebView2-Eigenschaft festgelegt wurde, wird die Initialisierung im Hintergrund gestartet (falls Sie noch nicht ausgeführt wird), nachdem die WebView2 zum angegebenen URI navigiert.</span><span class="sxs-lookup"><span data-stu-id="c292e-231">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="c292e-232">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="c292e-232">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="c292e-233">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-233">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="c292e-234">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-234">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-235">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="c292e-235">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="c292e-236">Initialisierung der CoreWebView2 des Steuerelements explizit auslösen.</span><span class="sxs-lookup"><span data-stu-id="c292e-236">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="c292e-237">öffentliche Aufgaben- [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment-Umgebung)</span><span class="sxs-lookup"><span data-stu-id="c292e-237">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="c292e-238">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="c292e-238">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="c292e-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="c292e-239">Parameters</span></span>
* `environment` <span data-ttu-id="c292e-240">Eine zuvor erstellte CoreWebView2Environment, die zum Erstellen des CoreWebView2 verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c292e-240">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="c292e-241">Durch das Erstellen einer eigenen Umgebung können Sie verschiedene Optionen steuern, die sich auf die Initialisierung des CoreWebView2 auswirken.</span><span class="sxs-lookup"><span data-stu-id="c292e-241">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="c292e-242">Wenn Sie eine Umgebung an diese Methode übergeben, werden alle in der CreationProperties-Eigenschaft angegebenen Einstellungen außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="c292e-242">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="c292e-243">Wenn Sie NULL (den Standardwert) übergeben und kein Wert auf CreationProperties festgesetzt wurde, wird eine Standardumgebung erstellt und automatisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="c292e-243">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="c292e-244">Gibt</span><span class="sxs-lookup"><span data-stu-id="c292e-244">Returns</span></span>
<span data-ttu-id="c292e-245">Eine Aufgabe, die den Hintergrund Initialisierungsprozess darstellt.</span><span class="sxs-lookup"><span data-stu-id="c292e-245">A Task that represents the background initialization process.</span></span> <span data-ttu-id="c292e-246">Wenn die Aufgabe abgeschlossen ist, steht die CoreWebView2-Eigenschaft zur Verwendung zur Verfügung (also nicht-null).</span><span class="sxs-lookup"><span data-stu-id="c292e-246">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="c292e-247">Beachten Sie, dass das CoreWebView2Ready-Ereignis des Steuerelements aufgerufen wird, bevor die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c292e-247">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="c292e-248">Das zusätzliche Aufrufen dieser Methode hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt dieselbe Aufgabe wie beim ersten Aufruf zurück.</span><span class="sxs-lookup"><span data-stu-id="c292e-248">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="c292e-249">Das Aufrufen dieser Methode, nachdem die Initialisierung implizit ausgelöst wurde, indem die Source-Eigenschaft festgelegt wird, hat keine Auswirkungen (jede angegebene Umgebung wird ignoriert) und gibt einfach eine Aufgabe zurück, die die bereits ausgeführte Initialisierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="c292e-249">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="c292e-250">Beachten Sie, dass auch wenn diese Methode asynchron ist und eine Aufgabe zurückgibt, Sie dennoch im UI-Thread aufgerufen werden muss, wie die meisten öffentlichen Funktionen der meisten UI-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c292e-250">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="c292e-251">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-251">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-252">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-252">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="c292e-253">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="c292e-253">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="c292e-254">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-255">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="c292e-255">ExecuteScriptAsync</span></span> 

<span data-ttu-id="c292e-256">Führt JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-256">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="c292e-257">Public Async Task< String > [ExecuteScriptAsync](#executescriptasync)(String javaScript)</span><span class="sxs-lookup"><span data-stu-id="c292e-257">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="c292e-258">Entspricht dem Aufrufen von CoreWebView2. ExecuteScriptAsync auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-258">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="c292e-259">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-259">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-260">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-260">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="c292e-261">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-261">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="c292e-262">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="c292e-262">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="c292e-263">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-263">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-264">GoBack</span><span class="sxs-lookup"><span data-stu-id="c292e-264">GoBack</span></span> 

<span data-ttu-id="c292e-265">Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="c292e-265">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="c292e-266">publicvoid [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="c292e-266">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="c292e-267">Entspricht dem Aufrufen von CoreWebView2. GoBack auf CoreWebView2, wenn CoreWebView2 noch nicht initialisiert wurde, dann aber nichts tut.</span><span class="sxs-lookup"><span data-stu-id="c292e-267">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="c292e-268">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-268">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-269">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-269">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="c292e-270">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="c292e-270">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="c292e-271">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-271">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-272">GoForward</span><span class="sxs-lookup"><span data-stu-id="c292e-272">GoForward</span></span> 

<span data-ttu-id="c292e-273">Navigiert die WebView zur nächsten Seite im Navigationsverlauf.</span><span class="sxs-lookup"><span data-stu-id="c292e-273">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="c292e-274">publicvoid [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="c292e-274">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="c292e-275">Entspricht dem Aufrufen von CoreWebView2. GoForward auf CoreWebView2, wenn CoreWebView2 noch nicht initialisiert wurde, dann aber nichts tut.</span><span class="sxs-lookup"><span data-stu-id="c292e-275">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="c292e-276">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-276">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-277">Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-277">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="c292e-278">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="c292e-278">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="c292e-279">Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-279">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-280">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="c292e-280">NavigateToString</span></span> 

<span data-ttu-id="c292e-281">Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.</span><span class="sxs-lookup"><span data-stu-id="c292e-281">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="c292e-282">publicvoid [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="c292e-282">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="c292e-283">Entspricht dem Aufrufen von CoreWebView2. NavigateToString auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-283">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="c292e-284">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-284">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-285">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-285">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="c292e-286">" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-286">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="c292e-287">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-287">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-288">Laden</span><span class="sxs-lookup"><span data-stu-id="c292e-288">Reload</span></span> 

<span data-ttu-id="c292e-289">Lädt die aktuelle Seite neu.</span><span class="sxs-lookup"><span data-stu-id="c292e-289">Reloads the current page.</span></span>

> <span data-ttu-id="c292e-290">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="c292e-290">public void [Reload](#reload)()</span></span>

<span data-ttu-id="c292e-291">Entspricht dem Aufruf von CoreWebView2. Reload auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-291">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="c292e-292">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-292">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-293">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-293">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="c292e-294">" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-294">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="c292e-295">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-295">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-296">Stop</span><span class="sxs-lookup"><span data-stu-id="c292e-296">Stop</span></span> 

<span data-ttu-id="c292e-297">Stoppt alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="c292e-297">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="c292e-298">öffentlicher void- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="c292e-298">public void [Stop](#stop)()</span></span>

<span data-ttu-id="c292e-299">Entspricht dem Aufruf von CoreWebView2. Stop auf CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-299">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="c292e-300">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c292e-300">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="c292e-301">Wird ausgelöst, wenn CoreWebView2 noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-301">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="c292e-302">" <exception cref="InvalidOperationException"> Wird ausgelöst, wenn der aufrufende Thread nicht der Thread ist, der dieses Objekt erstellt hat (in der Regel der UI-Thread).</span><span class="sxs-lookup"><span data-stu-id="c292e-302">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="c292e-303">Weitere Informationen finden Sie unter DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Wird ausgelöst, wenn Dispose bereits für das Steuerelement aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c292e-303">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="c292e-304">WebView2</span><span class="sxs-lookup"><span data-stu-id="c292e-304">WebView2</span></span> 

<span data-ttu-id="c292e-305">Erstellt eine neue Instanz eines WebView2-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="c292e-305">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="c292e-306">Public [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="c292e-306">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="c292e-307">Beachten Sie, dass der CoreWebView2 des Steuerelements bis zur Initialisierung NULL ist.</span><span class="sxs-lookup"><span data-stu-id="c292e-307">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="c292e-308">Eine Initialisierungs Übersicht finden Sie in der Dokumentation zur WebView2-Klasse.</span><span class="sxs-lookup"><span data-stu-id="c292e-308">See the WebView2 class documentation for an initialization overview.</span></span>

