---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: 155b0ae414d03d7a062b1e3426331307457687ae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878911"
---
# <span data-ttu-id="3646a-104">Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver Klasse</span><span class="sxs-lookup"><span data-stu-id="3646a-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="3646a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3646a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3646a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3646a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3646a-107">Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt und ermöglicht Ihnen, dieses Ereignis zu abonnieren und abzubestellen.</span><span class="sxs-lookup"><span data-stu-id="3646a-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="3646a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3646a-108">Summary</span></span>

 <span data-ttu-id="3646a-109">Member</span><span class="sxs-lookup"><span data-stu-id="3646a-109">Members</span></span>                        | <span data-ttu-id="3646a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3646a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3646a-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="3646a-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="3646a-112">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="3646a-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="3646a-113">Abgerufen aus dem WebView-Objekt über GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="3646a-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="3646a-114">Member</span><span class="sxs-lookup"><span data-stu-id="3646a-114">Members</span></span>

#### <span data-ttu-id="3646a-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="3646a-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="3646a-116">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="3646a-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="3646a-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="3646a-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="3646a-118">Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3646a-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="3646a-119">Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter Objekt des devtools-Protokollereignisses als JSON-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="3646a-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

