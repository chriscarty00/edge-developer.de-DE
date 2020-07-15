---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: dd141e135275d815458ce66a93dfc9ef3e7b33a8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878862"
---
# <span data-ttu-id="47b75-104">Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="47b75-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

<span data-ttu-id="47b75-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="47b75-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="47b75-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="47b75-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="47b75-107">Ereignis-args für das MoveFocusRequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="47b75-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="47b75-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="47b75-108">Summary</span></span>

 <span data-ttu-id="47b75-109">Member</span><span class="sxs-lookup"><span data-stu-id="47b75-109">Members</span></span>                        | <span data-ttu-id="47b75-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="47b75-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47b75-111">Handled</span><span class="sxs-lookup"><span data-stu-id="47b75-111">Handled</span></span>](#handled) | <span data-ttu-id="47b75-112">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="47b75-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="47b75-113">Grund</span><span class="sxs-lookup"><span data-stu-id="47b75-113">Reason</span></span>](#reason) | <span data-ttu-id="47b75-114">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="47b75-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="47b75-115">Member</span><span class="sxs-lookup"><span data-stu-id="47b75-115">Members</span></span>

#### <span data-ttu-id="47b75-116">Handled</span><span class="sxs-lookup"><span data-stu-id="47b75-116">Handled</span></span> 

<span data-ttu-id="47b75-117">Geben Sie an, ob das Ereignis von der APP behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="47b75-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="47b75-118">öffentliche bool- [Behandlung](#handled)</span><span class="sxs-lookup"><span data-stu-id="47b75-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="47b75-119">Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen.</span><span class="sxs-lookup"><span data-stu-id="47b75-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="47b75-120">Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47b75-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="47b75-121">Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="47b75-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="47b75-122">Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="47b75-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="47b75-123">Grund</span><span class="sxs-lookup"><span data-stu-id="47b75-123">Reason</span></span> 

<span data-ttu-id="47b75-124">Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="47b75-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="47b75-125">[Grund](#reason) für öffentliche CoreWebView2MoveFocusReason</span><span class="sxs-lookup"><span data-stu-id="47b75-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

