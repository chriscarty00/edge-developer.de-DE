---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: 0.8.355-WebView2 Win32 C++-Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7ef060f17eb3e7c7bceef3084208de1a533c904a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879583"
---
# <span data-ttu-id="ef1bd-104">0.8.355-Reference (WebView2)</span><span class="sxs-lookup"><span data-stu-id="ef1bd-104">0.8.355 - Reference (WebView2)</span></span>  

> [!NOTE]
> <span data-ttu-id="ef1bd-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.8.355 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ef1bd-105">This reference may be altered or unavailable for releases after SDK version 0.8.355.</span></span>  <span data-ttu-id="ef1bd-106">Die neueste API-Referenz finden Sie unter [Referenz](../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ef1bd-106">Please refer to [Reference](../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="ef1bd-107">Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webinhalte in Ihrer Anwendung unter Verwendung von [Microsoft Edge \ (Chrom \)](https://www.microsoftedgeinsider.com) als Rendering-Modul hosten.</span><span class="sxs-lookup"><span data-stu-id="ef1bd-107">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="ef1bd-108">Weitere Informationen finden Sie unter [Übersicht über Microsoft Edge WebView2](../../index.md)) und [Erste Schritte mit WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="ef1bd-108">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="ef1bd-109">[IWebView2WebView](0-8-190/IWebView2WebView.md) ist ein großartiger Ort, um mit dem Erlernen der Details der API zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ef1bd-109">[IWebView2WebView](0-8-190/IWebView2WebView.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="ef1bd-110">Globals</span><span class="sxs-lookup"><span data-stu-id="ef1bd-110">Globals</span></span>  

*   [<span data-ttu-id="ef1bd-111">Globals</span><span class="sxs-lookup"><span data-stu-id="ef1bd-111">Globals</span></span>](0-8-190/webview2-idl.md)  

## <span data-ttu-id="ef1bd-112">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ef1bd-112">Interfaces</span></span>  
*   [<span data-ttu-id="ef1bd-113">IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="ef1bd-113">IWebView2Deferral</span></span>](0-8-190/IWebView2Deferral.md)
*   [<span data-ttu-id="ef1bd-114">IWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="ef1bd-114">IWebView2Environment</span></span>](0-8-190/IWebView2Environment.md)
*   [<span data-ttu-id="ef1bd-115">IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="ef1bd-115">IWebView2Environment2</span></span>](0-8-190/IWebView2Environment2.md)
*   [<span data-ttu-id="ef1bd-116">IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="ef1bd-116">IWebView2Environment3</span></span>](0-8-190/IWebView2Environment3.md)
*   [<span data-ttu-id="ef1bd-117">IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="ef1bd-117">IWebView2HttpHeadersCollectionIterator</span></span>](0-8-190/IWebView2HttpHeadersCollectionIterator.md)
*   [<span data-ttu-id="ef1bd-118">IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ef1bd-118">IWebView2HttpRequestHeaders</span></span>](0-8-190/IWebView2HttpRequestHeaders.md)
*   [<span data-ttu-id="ef1bd-119">IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="ef1bd-119">IWebView2HttpResponseHeaders</span></span>](0-8-190/IWebView2HttpResponseHeaders.md)
*   [<span data-ttu-id="ef1bd-120">IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="ef1bd-120">IWebView2Settings</span></span>](0-8-190/IWebView2Settings.md)
*   [<span data-ttu-id="ef1bd-121">IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="ef1bd-121">IWebView2Settings2</span></span>](0-8-190/IWebView2Settings2.md)
*   [<span data-ttu-id="ef1bd-122">IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="ef1bd-122">IWebView2WebResourceRequest</span></span>](0-8-190/IWebView2WebResourceRequest.md)
*   [<span data-ttu-id="ef1bd-123">IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="ef1bd-123">IWebView2WebResourceRequestedEventArgs2</span></span>](0-8-190/IWebView2WebResourceRequestedEventArgs2.md)
*   [<span data-ttu-id="ef1bd-124">IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="ef1bd-124">IWebView2WebResourceResponse</span></span>](0-8-190/IWebView2WebResourceResponse.md)
*   [<span data-ttu-id="ef1bd-125">IWebView2WebView</span><span class="sxs-lookup"><span data-stu-id="ef1bd-125">IWebView2WebView</span></span>](0-8-190/IWebView2WebView.md)
*   [<span data-ttu-id="ef1bd-126">IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="ef1bd-126">IWebView2WebView2</span></span>](0-8-190/IWebView2WebView2.md)
*   [<span data-ttu-id="ef1bd-127">IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="ef1bd-127">IWebView2WebView3</span></span>](0-8-190/IWebView2WebView3.md)
*   [<span data-ttu-id="ef1bd-128">IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="ef1bd-128">IWebView2WebView4</span></span>](0-8-190/IWebView2WebView4.md)
*   [<span data-ttu-id="ef1bd-129">IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="ef1bd-129">IWebView2WebView5</span></span>](0-8-190/IWebView2WebView5.md)

### <span data-ttu-id="ef1bd-130">Ereignisargument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ef1bd-130">Event argument interfaces</span></span>

*   [<span data-ttu-id="ef1bd-131">IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-131">IWebView2AcceleratorKeyPressedEventArgs</span></span>](0-8-190/IWebView2AcceleratorKeyPressedEventArgs.md)
*   [<span data-ttu-id="ef1bd-132">IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-132">IWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-8-190/IWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [<span data-ttu-id="ef1bd-133">IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-133">IWebView2DocumentStateChangedEventArgs</span></span>](0-8-190/IWebView2DocumentStateChangedEventArgs.md)
*   [<span data-ttu-id="ef1bd-134">IWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-134">IWebView2MoveFocusRequestedEventArgs</span></span>](0-8-190/IWebView2MoveFocusRequestedEventArgs.md)
*   [<span data-ttu-id="ef1bd-135">IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-135">IWebView2NavigationCompletedEventArgs</span></span>](0-8-190/IWebView2NavigationCompletedEventArgs.md)
*   [<span data-ttu-id="ef1bd-136">IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-136">IWebView2NavigationStartingEventArgs</span></span>](0-8-190/IWebView2NavigationStartingEventArgs.md)
*   [<span data-ttu-id="ef1bd-137">IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-137">IWebView2NewVersionAvailableEventArgs</span></span>](0-8-190/IWebView2NewVersionAvailableEventArgs.md)
*   [<span data-ttu-id="ef1bd-138">IWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-138">IWebView2NewWindowRequestedEventArgs</span></span>](0-8-190/IWebView2NewWindowRequestedEventArgs.md)
*   [<span data-ttu-id="ef1bd-139">IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-139">IWebView2PermissionRequestedEventArgs</span></span>](0-8-190/IWebView2PermissionRequestedEventArgs.md)
*   [<span data-ttu-id="ef1bd-140">IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-140">IWebView2ProcessFailedEventArgs</span></span>](0-8-190/IWebView2ProcessFailedEventArgs.md)
*   [<span data-ttu-id="ef1bd-141">IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-141">IWebView2ScriptDialogOpeningEventArgs</span></span>](0-8-190/IWebView2ScriptDialogOpeningEventArgs.md)
*   [<span data-ttu-id="ef1bd-142">IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-142">IWebView2WebMessageReceivedEventArgs</span></span>](0-8-190/IWebView2WebMessageReceivedEventArgs.md)
*   [<span data-ttu-id="ef1bd-143">IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ef1bd-143">IWebView2WebResourceRequestedEventArgs</span></span>](0-8-190/IWebView2WebResourceRequestedEventArgs.md)

### <span data-ttu-id="ef1bd-144">Delegate-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ef1bd-144">Delegate interfaces</span></span>

*   [<span data-ttu-id="ef1bd-145">IWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-145">IWebView2AcceleratorKeyPressedEventHandler</span></span>](0-8-190/IWebView2AcceleratorKeyPressedEventHandler.md)
*   [<span data-ttu-id="ef1bd-146">IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-146">IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-8-190/IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [<span data-ttu-id="ef1bd-147">IWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-147">IWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-8-190/IWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [<span data-ttu-id="ef1bd-148">IWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-148">IWebView2CapturePreviewCompletedHandler</span></span>](0-8-190/IWebView2CapturePreviewCompletedHandler.md)
*   [<span data-ttu-id="ef1bd-149">IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-149">IWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [<span data-ttu-id="ef1bd-150">IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-150">IWebView2CreateWebView2EnvironmentCompletedHandler</span></span>](0-8-190/IWebView2CreateWebView2EnvironmentCompletedHandler.md)
*   [<span data-ttu-id="ef1bd-151">IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-151">IWebView2CreateWebViewCompletedHandler</span></span>](0-8-190/IWebView2CreateWebViewCompletedHandler.md)
*   [<span data-ttu-id="ef1bd-152">IWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-152">IWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-8-190/IWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [<span data-ttu-id="ef1bd-153">IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-153">IWebView2DocumentStateChangedEventHandler</span></span>](0-8-190/IWebView2DocumentStateChangedEventHandler.md)
*   [<span data-ttu-id="ef1bd-154">IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-154">IWebView2DocumentTitleChangedEventHandler</span></span>](0-8-190/IWebView2DocumentTitleChangedEventHandler.md)
*   [<span data-ttu-id="ef1bd-155">IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-155">IWebView2ExecuteScriptCompletedHandler</span></span>](0-8-190/IWebView2ExecuteScriptCompletedHandler.md)
*   [<span data-ttu-id="ef1bd-156">IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-156">IWebView2FocusChangedEventHandler</span></span>](0-8-190/IWebView2FocusChangedEventHandler.md)
*   [<span data-ttu-id="ef1bd-157">IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-157">IWebView2MoveFocusRequestedEventHandler</span></span>](0-8-190/IWebView2MoveFocusRequestedEventHandler.md)
*   [<span data-ttu-id="ef1bd-158">IWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-158">IWebView2NavigationCompletedEventHandler</span></span>](0-8-190/IWebView2NavigationCompletedEventHandler.md)
*   [<span data-ttu-id="ef1bd-159">IWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-159">IWebView2NavigationStartingEventHandler</span></span>](0-8-190/IWebView2NavigationStartingEventHandler.md)
*   [<span data-ttu-id="ef1bd-160">IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-160">IWebView2NewVersionAvailableEventHandler</span></span>](0-8-190/IWebView2NewVersionAvailableEventHandler.md)
*   [<span data-ttu-id="ef1bd-161">IWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-161">IWebView2NewWindowRequestedEventHandler</span></span>](0-8-190/IWebView2NewWindowRequestedEventHandler.md)
*   [<span data-ttu-id="ef1bd-162">IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-162">IWebView2PermissionRequestedEventHandler</span></span>](0-8-190/IWebView2PermissionRequestedEventHandler.md)
*   [<span data-ttu-id="ef1bd-163">IWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-163">IWebView2ProcessFailedEventHandler</span></span>](0-8-190/IWebView2ProcessFailedEventHandler.md)
*   [<span data-ttu-id="ef1bd-164">IWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-164">IWebView2ScriptDialogOpeningEventHandler</span></span>](0-8-190/IWebView2ScriptDialogOpeningEventHandler.md)
*   [<span data-ttu-id="ef1bd-165">IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-165">IWebView2WebMessageReceivedEventHandler</span></span>](0-8-190/IWebView2WebMessageReceivedEventHandler.md)
*   [<span data-ttu-id="ef1bd-166">IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-166">IWebView2WebResourceRequestedEventHandler</span></span>](0-8-190/IWebView2WebResourceRequestedEventHandler.md)
*   [<span data-ttu-id="ef1bd-167">IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef1bd-167">IWebView2ZoomFactorChangedEventHandler</span></span>](0-8-190/IWebView2ZoomFactorChangedEventHandler.md)
