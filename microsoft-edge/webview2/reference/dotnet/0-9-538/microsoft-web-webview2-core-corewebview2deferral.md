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
ms.openlocfilehash: 935e8edb4db54e7bbb707cb2dc704ba312ed3196
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698788"
---
# <span data-ttu-id="ca427-104">Microsoft. Web. WebView2. Core. CoreWebView2Deferral Klasse</span><span class="sxs-lookup"><span data-stu-id="ca427-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="ca427-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ca427-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ca427-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="ca427-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ca427-107">Diese Klasse wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ca427-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="ca427-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ca427-108">Summary</span></span>

 <span data-ttu-id="ca427-109">Member</span><span class="sxs-lookup"><span data-stu-id="ca427-109">Members</span></span>                        | <span data-ttu-id="ca427-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ca427-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca427-111">Complete</span><span class="sxs-lookup"><span data-stu-id="ca427-111">Complete</span></span>](#complete) | <span data-ttu-id="ca427-112">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="ca427-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="ca427-113">Member</span><span class="sxs-lookup"><span data-stu-id="ca427-113">Members</span></span>

#### <span data-ttu-id="ca427-114">Complete</span><span class="sxs-lookup"><span data-stu-id="ca427-114">Complete</span></span> 

<span data-ttu-id="ca427-115">Schließt das zugeordnete verzögerte Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="ca427-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="ca427-116">publicvoid [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="ca427-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="ca427-117">Complete sollte nur einmal für jede verzögerte Verzögerung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ca427-117">Complete should only be called once for each deferral taken.</span></span>

