---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: d99349ec763796bd6b1ea242abbe5c2219c221c2
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698786"
---
# <span data-ttu-id="4ddfe-104">Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver Klasse</span><span class="sxs-lookup"><span data-stu-id="4ddfe-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="4ddfe-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4ddfe-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4ddfe-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="4ddfe-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4ddfe-107">Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt und ermöglicht Ihnen, dieses Ereignis zu abonnieren und abzubestellen.</span><span class="sxs-lookup"><span data-stu-id="4ddfe-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="4ddfe-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4ddfe-108">Summary</span></span>

 <span data-ttu-id="4ddfe-109">Member</span><span class="sxs-lookup"><span data-stu-id="4ddfe-109">Members</span></span>                        | <span data-ttu-id="4ddfe-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4ddfe-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4ddfe-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="4ddfe-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="4ddfe-112">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="4ddfe-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="4ddfe-113">Abgerufen aus dem WebView-Objekt über GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="4ddfe-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="4ddfe-114">Member</span><span class="sxs-lookup"><span data-stu-id="4ddfe-114">Members</span></span>

#### <span data-ttu-id="4ddfe-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="4ddfe-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="4ddfe-116">Abonnieren eines DevToolsProtocol-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="4ddfe-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="4ddfe-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="4ddfe-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="4ddfe-118">Die Invoke-Methode des Handlers wird aufgerufen, wenn das entsprechende DevToolsProtocol-Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="4ddfe-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="4ddfe-119">Invoke wird mit dem Ereignis args-Objekt aufgerufen, das das Parameter Objekt des devtools-Protokollereignisses als JSON-Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="4ddfe-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

