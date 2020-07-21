---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1982c6926d2ed8805433efc4d46ff6f3cac691ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885058"
---
# <span data-ttu-id="e4118-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver Klasse</span><span class="sxs-lookup"><span data-stu-id="e4118-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="e4118-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e4118-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e4118-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e4118-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e4118-107">Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt und ermöglicht Ihnen, dieses Ereignis zu abonnieren und abzubestellen.</span><span class="sxs-lookup"><span data-stu-id="e4118-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="e4118-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e4118-108">Summary</span></span>

 <span data-ttu-id="e4118-109">Member</span><span class="sxs-lookup"><span data-stu-id="e4118-109">Members</span></span>                        | <span data-ttu-id="e4118-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e4118-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4118-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="e4118-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="e4118-112">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="e4118-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="e4118-113">Abgerufen aus dem WebView-Objekt über GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="e4118-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="e4118-114">Member</span><span class="sxs-lookup"><span data-stu-id="e4118-114">Members</span></span>

#### <span data-ttu-id="e4118-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="e4118-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="e4118-116">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="e4118-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="e4118-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="e4118-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="e4118-118">Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e4118-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="e4118-119">Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter Objekt des devtools-Protokollereignisses als JSON-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="e4118-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

