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
ms.openlocfilehash: 69835f6fe22246f43e3df9c45a7fde7a674ac0e5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697644"
---
# <span data-ttu-id="ac95d-104">Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="ac95d-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="ac95d-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ac95d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ac95d-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ac95d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="ac95d-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ac95d-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ac95d-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="ac95d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ac95d-109">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ac95d-109">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="ac95d-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ac95d-110">Summary</span></span>

 <span data-ttu-id="ac95d-111">Member</span><span class="sxs-lookup"><span data-stu-id="ac95d-111">Members</span></span>                        | <span data-ttu-id="ac95d-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ac95d-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac95d-113">Handled</span><span class="sxs-lookup"><span data-stu-id="ac95d-113">Handled</span></span>](#handled) | <span data-ttu-id="ac95d-114">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="ac95d-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="ac95d-115">Grund</span><span class="sxs-lookup"><span data-stu-id="ac95d-115">Reason</span></span>](#reason) | <span data-ttu-id="ac95d-116">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="ac95d-116">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="ac95d-117">Member</span><span class="sxs-lookup"><span data-stu-id="ac95d-117">Members</span></span>

#### <span data-ttu-id="ac95d-118">Handled</span><span class="sxs-lookup"><span data-stu-id="ac95d-118">Handled</span></span> 

<span data-ttu-id="ac95d-119">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="ac95d-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="ac95d-120">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="ac95d-120">public bool [Handled](#handled)</span></span>

<span data-ttu-id="ac95d-121">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="ac95d-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="ac95d-122">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac95d-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="ac95d-123">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ac95d-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="ac95d-124">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ac95d-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="ac95d-125">Grund</span><span class="sxs-lookup"><span data-stu-id="ac95d-125">Reason</span></span> 

<span data-ttu-id="ac95d-126">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="ac95d-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="ac95d-127">[Grund](#reason) für öffentliche CoreWebView2MoveFocusReason</span><span class="sxs-lookup"><span data-stu-id="ac95d-127">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

