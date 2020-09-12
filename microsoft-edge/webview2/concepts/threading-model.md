---
description: Threadingmodell
title: Threadingmodell
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013737"
---
# <span data-ttu-id="3b049-104">Threadingmodell</span><span class="sxs-lookup"><span data-stu-id="3b049-104">Threading model</span></span> 

<span data-ttu-id="3b049-105">Das WebView2-Steuerelement basiert auf dem [Component-Objektmodell (com)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) und muss auf einem [Single Threaded Apartments (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) -Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3b049-105">The WebView2 control is based on the [Component Object Model (COM)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) and must run on a [Single Threaded Apartments (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) thread.</span></span>

## <span data-ttu-id="3b049-106">Thread Sicherheit</span><span class="sxs-lookup"><span data-stu-id="3b049-106">Thread safety</span></span>  

<span data-ttu-id="3b049-107">Der WebView2 muss in einem UI-Thread erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b049-107">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="3b049-108">Insbesondere ein Thread mit einer Nachrichten Pumpe.</span><span class="sxs-lookup"><span data-stu-id="3b049-108">Specifically a thread with a message pump.</span></span>  <span data-ttu-id="3b049-109">Alle Rückrufe treten für diesen Thread auf, und Anforderungen an die WebView2 müssen in diesem Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3b049-109">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="3b049-110">Es ist nicht sicher, die WebView2 aus einem anderen Thread zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b049-110">It is not safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="3b049-111">Die einzige Ausnahme ist die `Content` Eigenschaft von `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="3b049-111">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="3b049-112">Der `Content` Eigenschaftendaten Strom wird aus einem Hintergrundthread gelesen.</span><span class="sxs-lookup"><span data-stu-id="3b049-112">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="3b049-113">Der Datenstrom sollte agil sein oder aus einem background-STA erstellt werden, um die Auswirkungen auf die Leistung des UI-Threads zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="3b049-113">The stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span>  

## <span data-ttu-id="3b049-114">Reentranz</span><span class="sxs-lookup"><span data-stu-id="3b049-114">Reentrancy</span></span>  

<span data-ttu-id="3b049-115">Rückrufe, einschließlich Ereignishandlern und Vervollständigungs Handlern, werden seriell ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b049-115">Callbacks including event handlers and completion handlers run serially.</span></span>  <span data-ttu-id="3b049-116">Wenn Sie einen Ereignishandler ausführen und eine Nachrichtenschleife beginnen, können keine anderen Ereignishandler oder Abschluss Rückrufe auf eine Art und Weise gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3b049-116">If you have an event handler running and begin a message loop, no other event handlers or completion callbacks are able to begin running in a reentrant manner.</span></span>  

## <span data-ttu-id="3b049-117">Verzögerungen</span><span class="sxs-lookup"><span data-stu-id="3b049-117">Deferrals</span></span>  

<span data-ttu-id="3b049-118">Einige WebView2-Ereignisse lesen Werte, die für Ihre Ereignisargumente festgesetzt sind, oder führen nach Abschluss des Ereignishandlers eine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="3b049-118">Some WebView2 events read values set on their event args or perform some action after the event handler completes.</span></span>  <span data-ttu-id="3b049-119">Wenn Sie auch einen asynchronen Vorgang wie einen Ereignishandler ausführen müssen, können Sie die `GetDeferral` Methode für die Ereignisargumente der zugeordneten Ereignisse verwenden.</span><span class="sxs-lookup"><span data-stu-id="3b049-119">If you also need to run an asynchronous operation such an event handler, you may use the `GetDeferral` method on the event args of the associated events.</span></span>  <span data-ttu-id="3b049-120">Das zurückgegebene verzögerte Objekt stellt sicher, dass der Ereignishandler erst dann als abgeschlossen betrachtet wird, wenn die `Complete` Methode von `Deferral` angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="3b049-120">The returned Deferral object ensures the event handler is not considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="3b049-121">Beispielsweise können Sie das Ereignis verwenden `NewWindowRequested` , um eine `CoreWebView2` Verbindung als untergeordnetes Fenster bereitzustellen, wenn der Ereignishandler abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3b049-121">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="3b049-122">Wenn Sie das jedoch asynchron erstellen müssen `CoreWebView2` , fordern Sie die `GetDeferral` Methode für die `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="3b049-122">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="3b049-123">Nachdem Sie den asynchronen erstellt haben `CoreWebView2` und die `NewWindow` Eigenschaft für die-Eigenschaft festlegen `NewWindowRequestedEventArgs` , wird die Anforderung `Complete` für das `Deferral` Objekt mithilfe der Methode zurückgegeben `GetDeferral` .</span><span class="sxs-lookup"><span data-stu-id="3b049-123">After you have asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

<!-- links -->  
