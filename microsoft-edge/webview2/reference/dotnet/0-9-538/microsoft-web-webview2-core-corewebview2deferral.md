---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: 62cd86772d45e1bf9eee7d1821a90b723e1af7db
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011048"
---
# <span data-ttu-id="4435b-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral Klasse</span><span class="sxs-lookup"><span data-stu-id="4435b-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="4435b-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4435b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4435b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="4435b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4435b-107">Diese Klasse wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4435b-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="4435b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4435b-108">Summary</span></span>

 <span data-ttu-id="4435b-109">Member</span><span class="sxs-lookup"><span data-stu-id="4435b-109">Members</span></span>                        | <span data-ttu-id="4435b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4435b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4435b-111">Complete</span><span class="sxs-lookup"><span data-stu-id="4435b-111">Complete</span></span>](#complete) | <span data-ttu-id="4435b-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="4435b-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="4435b-113">Member</span><span class="sxs-lookup"><span data-stu-id="4435b-113">Members</span></span>

#### <span data-ttu-id="4435b-114">Complete</span><span class="sxs-lookup"><span data-stu-id="4435b-114">Complete</span></span> 

<span data-ttu-id="4435b-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="4435b-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="4435b-116">publicvoid [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="4435b-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="4435b-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4435b-117">Complete should only be called once for each deferral taken.</span></span>

