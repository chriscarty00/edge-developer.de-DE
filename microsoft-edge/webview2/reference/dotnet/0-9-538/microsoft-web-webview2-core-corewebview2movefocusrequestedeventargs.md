---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: 098ca5199d6797510cdc0535a02a58c795b5ce54
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010957"
---
# <span data-ttu-id="af016-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="af016-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="af016-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="af016-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="af016-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="af016-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="af016-107">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="af016-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="af016-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="af016-108">Summary</span></span>

 <span data-ttu-id="af016-109">Member</span><span class="sxs-lookup"><span data-stu-id="af016-109">Members</span></span>                        | <span data-ttu-id="af016-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="af016-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af016-111">Handled</span><span class="sxs-lookup"><span data-stu-id="af016-111">Handled</span></span>](#handled) | <span data-ttu-id="af016-112">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="af016-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="af016-113">Grund</span><span class="sxs-lookup"><span data-stu-id="af016-113">Reason</span></span>](#reason) | <span data-ttu-id="af016-114">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="af016-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="af016-115">Member</span><span class="sxs-lookup"><span data-stu-id="af016-115">Members</span></span>

#### <span data-ttu-id="af016-116">Handled</span><span class="sxs-lookup"><span data-stu-id="af016-116">Handled</span></span> 

<span data-ttu-id="af016-117">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="af016-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="af016-118">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="af016-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="af016-119">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="af016-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="af016-120">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af016-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="af016-121">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="af016-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="af016-122">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="af016-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="af016-123">Grund</span><span class="sxs-lookup"><span data-stu-id="af016-123">Reason</span></span> 

<span data-ttu-id="af016-124">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="af016-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="af016-125">[Grund](#reason) für öffentliche CoreWebView2MoveFocusReason</span><span class="sxs-lookup"><span data-stu-id="af016-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

