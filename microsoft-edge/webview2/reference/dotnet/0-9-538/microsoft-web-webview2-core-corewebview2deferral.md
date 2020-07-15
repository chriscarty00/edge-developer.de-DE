---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: 77a3540a64c9894f10cb0c03998dafda90e4f15b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878932"
---
# <span data-ttu-id="4d8ca-104">Microsoft. Web. WebView2. Core. CoreWebView2Deferral Klasse</span><span class="sxs-lookup"><span data-stu-id="4d8ca-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="4d8ca-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4d8ca-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4d8ca-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="4d8ca-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4d8ca-107">Diese Klasse wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4d8ca-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="4d8ca-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4d8ca-108">Summary</span></span>

 <span data-ttu-id="4d8ca-109">Member</span><span class="sxs-lookup"><span data-stu-id="4d8ca-109">Members</span></span>                        | <span data-ttu-id="4d8ca-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4d8ca-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d8ca-111">Complete</span><span class="sxs-lookup"><span data-stu-id="4d8ca-111">Complete</span></span>](#complete) | <span data-ttu-id="4d8ca-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="4d8ca-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="4d8ca-113">Member</span><span class="sxs-lookup"><span data-stu-id="4d8ca-113">Members</span></span>

#### <span data-ttu-id="4d8ca-114">Complete</span><span class="sxs-lookup"><span data-stu-id="4d8ca-114">Complete</span></span> 

<span data-ttu-id="4d8ca-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="4d8ca-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="4d8ca-116">publicvoid [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="4d8ca-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="4d8ca-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ca-117">Complete should only be called once for each deferral taken.</span></span>

