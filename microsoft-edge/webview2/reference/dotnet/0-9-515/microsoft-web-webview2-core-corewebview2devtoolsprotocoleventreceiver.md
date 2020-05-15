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
ms.openlocfilehash: 23ee363fd90416d07c76644879a5f4b6cc2acabe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654027"
---
# <span data-ttu-id="2e21a-104">Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver Klasse</span><span class="sxs-lookup"><span data-stu-id="2e21a-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="2e21a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2e21a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2e21a-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="2e21a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2e21a-107">Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt und ermöglicht Ihnen, dieses Ereignis zu abonnieren und abzubestellen.</span><span class="sxs-lookup"><span data-stu-id="2e21a-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="2e21a-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2e21a-108">Summary</span></span>

 <span data-ttu-id="2e21a-109">Member</span><span class="sxs-lookup"><span data-stu-id="2e21a-109">Members</span></span>                        | <span data-ttu-id="2e21a-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2e21a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2e21a-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="2e21a-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="2e21a-112">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2e21a-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="2e21a-113">Abgerufen aus dem WebView-Objekt über GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="2e21a-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="2e21a-114">Member</span><span class="sxs-lookup"><span data-stu-id="2e21a-114">Members</span></span>

#### <span data-ttu-id="2e21a-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="2e21a-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="2e21a-116">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2e21a-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="2e21a-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="2e21a-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="2e21a-118">Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="2e21a-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="2e21a-119">Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter Objekt des devtools-Protokollereignisses als JSON-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="2e21a-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

