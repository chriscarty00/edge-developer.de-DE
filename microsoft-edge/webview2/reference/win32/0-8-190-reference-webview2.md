---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge WebView 2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ba3103037db60674d1d3887ac43a8fce5be02bdd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653917"
---
# 0.8.190-Reference (WebView2)  

> [!NOTE]
> Dieser Verweis kann für Versionen nach der SDK-Version 0.8.355 geändert oder nicht mehr zur Verfügung stehen.  Die neueste API-Referenz finden Sie unter [Referenz](../../webview2-api-reference.md) .

Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webinhalte in Ihrer Anwendung unter Verwendung von [Microsoft Edge \ (Chrom \)](https://www.microsoftedgeinsider.com) als Rendering-Modul hosten.  Weitere Informationen finden Sie unter [Übersicht über Microsoft Edge WebView2](../../index.md)) und [Erste Schritte mit WebView2](../../gettingstarted/win32.md).  [IWebView2WebView](0-8-190/IWebView2WebView.md) ist ein großartiger Ort, um mit dem Erlernen der Details der API zu beginnen.  

## Globals  

*   [Globals](0-8-190/webview2-idl.md)  

## Schnittstellen  
*   [IWebView2Deferral](0-8-190/IWebView2Deferral.md)
*   [IWebView2Environment](0-8-190/IWebView2Environment.md)
*   [IWebView2Environment2](0-8-190/IWebView2Environment2.md)
*   [IWebView2Environment3](0-8-190/IWebView2Environment3.md)
*   [IWebView2HttpHeadersCollectionIterator](0-8-190/IWebView2HttpHeadersCollectionIterator.md)
*   [IWebView2HttpRequestHeaders](0-8-190/IWebView2HttpRequestHeaders.md)
*   [IWebView2HttpResponseHeaders](0-8-190/IWebView2HttpResponseHeaders.md)
*   [IWebView2Settings](0-8-190/IWebView2Settings.md)
*   [IWebView2Settings2](0-8-190/IWebView2Settings2.md)
*   [IWebView2WebResourceRequest](0-8-190/IWebView2WebResourceRequest.md)
*   [IWebView2WebResourceRequestedEventArgs2](0-8-190/IWebView2WebResourceRequestedEventArgs2.md)
*   [IWebView2WebResourceResponse](0-8-190/IWebView2WebResourceResponse.md)
*   [IWebView2WebView](0-8-190/IWebView2WebView.md)
*   [IWebView2WebView2](0-8-190/IWebView2WebView2.md)
*   [IWebView2WebView3](0-8-190/IWebView2WebView3.md)
*   [IWebView2WebView4](0-8-190/IWebView2WebView4.md)
*   [IWebView2WebView5](0-8-190/IWebView2WebView5.md)

### Ereignisargument Schnittstellen

*   [IWebView2AcceleratorKeyPressedEventArgs](0-8-190/IWebView2AcceleratorKeyPressedEventArgs.md)
*   [IWebView2DevToolsProtocolEventReceivedEventArgs](0-8-190/IWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [IWebView2DocumentStateChangedEventArgs](0-8-190/IWebView2DocumentStateChangedEventArgs.md)
*   [IWebView2MoveFocusRequestedEventArgs](0-8-190/IWebView2MoveFocusRequestedEventArgs.md)
*   [IWebView2NavigationCompletedEventArgs](0-8-190/IWebView2NavigationCompletedEventArgs.md)
*   [IWebView2NavigationStartingEventArgs](0-8-190/IWebView2NavigationStartingEventArgs.md)
*   [IWebView2NewVersionAvailableEventArgs](0-8-190/IWebView2NewVersionAvailableEventArgs.md)
*   [IWebView2NewWindowRequestedEventArgs](0-8-190/IWebView2NewWindowRequestedEventArgs.md)
*   [IWebView2PermissionRequestedEventArgs](0-8-190/IWebView2PermissionRequestedEventArgs.md)
*   [IWebView2ProcessFailedEventArgs](0-8-190/IWebView2ProcessFailedEventArgs.md)
*   [IWebView2ScriptDialogOpeningEventArgs](0-8-190/IWebView2ScriptDialogOpeningEventArgs.md)
*   [IWebView2WebMessageReceivedEventArgs](0-8-190/IWebView2WebMessageReceivedEventArgs.md)
*   [IWebView2WebResourceRequestedEventArgs](0-8-190/IWebView2WebResourceRequestedEventArgs.md)

### Delegate-Schnittstellen

*   [IWebView2AcceleratorKeyPressedEventHandler](0-8-190/IWebView2AcceleratorKeyPressedEventHandler.md)
*   [IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-8-190/IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [IWebView2CallDevToolsProtocolMethodCompletedHandler](0-8-190/IWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [IWebView2CapturePreviewCompletedHandler](0-8-190/IWebView2CapturePreviewCompletedHandler.md)
*   [IWebView2ContainsFullScreenElementChangedEventHandler](0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [IWebView2CreateWebView2EnvironmentCompletedHandler](0-8-190/IWebView2CreateWebView2EnvironmentCompletedHandler.md)
*   [IWebView2CreateWebViewCompletedHandler](0-8-190/IWebView2CreateWebViewCompletedHandler.md)
*   [IWebView2DevToolsProtocolEventReceivedEventHandler](0-8-190/IWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [IWebView2DocumentStateChangedEventHandler](0-8-190/IWebView2DocumentStateChangedEventHandler.md)
*   [IWebView2DocumentTitleChangedEventHandler](0-8-190/IWebView2DocumentTitleChangedEventHandler.md)
*   [IWebView2ExecuteScriptCompletedHandler](0-8-190/IWebView2ExecuteScriptCompletedHandler.md)
*   [IWebView2FocusChangedEventHandler](0-8-190/IWebView2FocusChangedEventHandler.md)
*   [IWebView2MoveFocusRequestedEventHandler](0-8-190/IWebView2MoveFocusRequestedEventHandler.md)
*   [IWebView2NavigationCompletedEventHandler](0-8-190/IWebView2NavigationCompletedEventHandler.md)
*   [IWebView2NavigationStartingEventHandler](0-8-190/IWebView2NavigationStartingEventHandler.md)
*   [IWebView2NewVersionAvailableEventHandler](0-8-190/IWebView2NewVersionAvailableEventHandler.md)
*   [IWebView2NewWindowRequestedEventHandler](0-8-190/IWebView2NewWindowRequestedEventHandler.md)
*   [IWebView2PermissionRequestedEventHandler](0-8-190/IWebView2PermissionRequestedEventHandler.md)
*   [IWebView2ProcessFailedEventHandler](0-8-190/IWebView2ProcessFailedEventHandler.md)
*   [IWebView2ScriptDialogOpeningEventHandler](0-8-190/IWebView2ScriptDialogOpeningEventHandler.md)
*   [IWebView2WebMessageReceivedEventHandler](0-8-190/IWebView2WebMessageReceivedEventHandler.md)
*   [IWebView2WebResourceRequestedEventHandler](0-8-190/IWebView2WebResourceRequestedEventHandler.md)
*   [IWebView2ZoomFactorChangedEventHandler](0-8-190/IWebView2ZoomFactorChangedEventHandler.md)
