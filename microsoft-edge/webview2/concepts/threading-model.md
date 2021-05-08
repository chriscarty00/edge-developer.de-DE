---
description: Threadingmodell
title: Threadmodell| WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, Webview2, Webview, wpf-Apps, Wpf, Microsoft Edge, ICoreWebView2, ICoreWebView2Host, Browsersteuerung, Edge-HTML
ms.openlocfilehash: 9a7ce3d66e53b832d4430afb153e6539d97e5db7
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535608"
---
# <a name="threading-model"></a><span data-ttu-id="30057-104">Threadingmodell</span><span class="sxs-lookup"><span data-stu-id="30057-104">Threading model</span></span> 

:::row:::
   :::column span="1":::
      <span data-ttu-id="30057-105">Unterstützte Plattformen:</span><span class="sxs-lookup"><span data-stu-id="30057-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="30057-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="30057-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="30057-107">Das WebView2-Steuerelement basiert auf dem [Component Object Model (COM)][WindowsWin32ComTheComponentObjectModel] und muss in einem [Single Threaded Apartment (STA)-Thread ausgeführt][WindowsWin32ComSingleThreadedApartments] werden.</span><span class="sxs-lookup"><span data-stu-id="30057-107">The WebView2 control is based on the [Component Object Model (COM)][WindowsWin32ComTheComponentObjectModel] and must run on a [Single Threaded Apartments (STA)][WindowsWin32ComSingleThreadedApartments] thread.</span></span>  

## <a name="thread-safety"></a><span data-ttu-id="30057-108">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="30057-108">Thread safety</span></span>  

<span data-ttu-id="30057-109">WebView2 muss in einem Benutzeroberflächenthread erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="30057-109">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="30057-110">Insbesondere ein Thread mit einer Nachrichtenumpumpung.</span><span class="sxs-lookup"><span data-stu-id="30057-110">Specifically, a thread with a message pump.</span></span>  <span data-ttu-id="30057-111">Alle Rückrufe erfolgen in diesem Thread, und Anforderungen an WebView2 müssen in diesem Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="30057-111">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="30057-112">Es ist nicht sicher, WebView2 aus einem anderen Thread zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="30057-112">It isn't safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="30057-113">Die einzige Ausnahme gilt für die `Content` Eigenschaft von `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="30057-113">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="30057-114">Der `Content` Eigenschaftendatenstrom wird aus einem Hintergrundthread gelesen.</span><span class="sxs-lookup"><span data-stu-id="30057-114">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="30057-115">Der Datenstrom sollte agil sein oder aus einem Hintergrund-STA erstellt werden, um leistungsbeeinträchtigungen für den Benutzeroberflächenthread zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="30057-115">The stream should be agile or be created from a background STA to prevent performance degradation to the UI thread.</span></span>  

## <a name="re-entrancy"></a><span data-ttu-id="30057-116">Erneutes Entlocken</span><span class="sxs-lookup"><span data-stu-id="30057-116">Re-entrancy</span></span>  

<span data-ttu-id="30057-117">Rückrufe, einschließlich Ereignishandlern und Abschlusshandlern, werden seriell ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30057-117">Callbacks including event handlers and completion handlers run serially.</span></span>  
<span data-ttu-id="30057-118">Nachdem Sie einen Ereignishandler ausgeführt und eine Nachrichtenschleife begonnen haben, können Sie keinen Ereignishandler oder Abschlussrückruf erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="30057-118">After you run an event handler and begin a message loop, you're unable to run any event handler or completion callback in a re-entrant manner.</span></span>  

## <a name="deferrals"></a><span data-ttu-id="30057-119">Verschiebungen</span><span class="sxs-lookup"><span data-stu-id="30057-119">Deferrals</span></span>  

<span data-ttu-id="30057-120">Einige WebView2-Ereignisse lesen Werte, die für die zugehörigen Ereignisargumente festgelegt sind, oder starten eine Aktion, nachdem der Ereignishandler abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="30057-120">Some WebView2 events read values set on the related event arguments or start some action after the event handler completes.</span></span>  <span data-ttu-id="30057-121">Wenn Sie auch einen asynchronen Vorgang wie einen Ereignishandler ausführen müssen, verwenden Sie die -Methode für die Ereignisargumente `GetDeferral` der zugeordneten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="30057-121">If you also need to run an asynchronous operation such an event handler, use the `GetDeferral` method on the event arguments of the associated events.</span></span>  <span data-ttu-id="30057-122">Das zurückgegebene Objekt stellt sicher, dass der Ereignishandler erst als abgeschlossen betrachtet wird, wenn `Deferral` `Complete` die -Methode angefordert `Deferral` wird.</span><span class="sxs-lookup"><span data-stu-id="30057-122">The returned `Deferral` object ensures the event handler isn't considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="30057-123">Sie können das Ereignis z. B. verwenden, um eine Verbindung als untergeordnetes Fenster herzustellen, wenn `NewWindowRequested` `CoreWebView2` der Ereignishandler abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="30057-123">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="30057-124">Wenn Sie jedoch asynchron das erstellen `CoreWebView2` müssen, fordern Sie die `GetDeferral` -Methode für `NewWindowRequestedEventArgs` an.</span><span class="sxs-lookup"><span data-stu-id="30057-124">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="30057-125">Nachdem Sie die -Eigenschaft asynchron erstellt und für die festgelegt haben, wird die Anforderung für das Objekt mithilfe `CoreWebView2` `NewWindow` der `NewWindowRequestedEventArgs` `Complete` `Deferral` -Methode `GetDeferral` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30057-125">After you've asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

## <a name="block-the-ui-thread"></a><span data-ttu-id="30057-126">Blockieren des Benutzeroberflächenthreads</span><span class="sxs-lookup"><span data-stu-id="30057-126">Block the UI thread</span></span>  

<span data-ttu-id="30057-127">WebView2 verwendet die Nachrichtenumpumpung des Benutzeroberflächenthreads, um Ereignishandlerrückrufe und Async-Methodenabschlussrückrufe ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="30057-127">The WebView2 relies on the message pump of the UI thread to run event handler callbacks and async method completion callbacks.</span></span>  <span data-ttu-id="30057-128">Wenn Sie Methoden verwenden, die die Nachrichtenumpumpung blockieren, z. B. oder, werden die WebView2-Ereignishandler und `Task.Result` async-Methodenentvollständigungshandler `WaitForSingleObject` nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30057-128">If you use methods that block the message pump such as `Task.Result` or `WaitForSingleObject`, then your WebView2 event handlers and async method completion handlers don't run.</span></span>  <span data-ttu-id="30057-129">Der folgende Code ist beispielsweise nicht vollständig, da die Nachrichtenumpumpung angehalten wird, während sie `Task.Result` wartet, `ExecuteScriptAsync` bis sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="30057-129">For example, the following code doesn't complete, because `Task.Result` stops the message pump while it waits for `ExecuteScriptAsync` to complete.</span></span>  <span data-ttu-id="30057-130">Da die Nachrichtenumpumpung blockiert ist, kann der Vorgang `ExecuteScriptAsync` nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="30057-130">Since the message pump is blocked, the `ExecuteScriptAsync` isn't able to complete.</span></span>   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

<span data-ttu-id="30057-131">Verwenden Sie einen asynchronen Mechanismus wie and , der die Nachrichtenummpung oder den `await` `async` Benutzeroberflächenthread nicht `await` blockiert.</span><span class="sxs-lookup"><span data-stu-id="30057-131">Use an asynchronous `await` mechanism such as `async` and `await`, which doesn't block the message pump or the UI thread.</span></span>  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a><span data-ttu-id="30057-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="30057-132">See also</span></span>  

*   <span data-ttu-id="30057-133">Navigieren Sie zu [WebView2 Get Started Guides,][Webview2IndexGetStarted] um mit WebView2 zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="30057-133">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="30057-134">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="30057-134">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="30057-135">Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="30057-135">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="30057-136">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="30057-136">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="30057-137">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="30057-137">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Erste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Single-Threaded-| Microsoft Docs"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "Das Component-Objektmodell | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
