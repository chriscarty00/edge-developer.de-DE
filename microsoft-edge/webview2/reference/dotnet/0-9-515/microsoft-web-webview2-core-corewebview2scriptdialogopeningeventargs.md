---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 4e7cd20b982d829be6d304eea1f3f60759cc503f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884855"
---
# <span data-ttu-id="4279c-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="4279c-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="4279c-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4279c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4279c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="4279c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4279c-107">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4279c-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="4279c-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4279c-108">Summary</span></span>

 <span data-ttu-id="4279c-109">Member</span><span class="sxs-lookup"><span data-stu-id="4279c-109">Members</span></span>                        | <span data-ttu-id="4279c-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4279c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4279c-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="4279c-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="4279c-112">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4279c-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="4279c-113">Art</span><span class="sxs-lookup"><span data-stu-id="4279c-113">Kind</span></span>](#kind) | <span data-ttu-id="4279c-114">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="4279c-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="4279c-115">Meldung</span><span class="sxs-lookup"><span data-stu-id="4279c-115">Message</span></span>](#message) | <span data-ttu-id="4279c-116">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="4279c-116">The message of the dialog box.</span></span>
[<span data-ttu-id="4279c-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="4279c-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="4279c-118">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4279c-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="4279c-119">URI</span><span class="sxs-lookup"><span data-stu-id="4279c-119">Uri</span></span>](#uri) | <span data-ttu-id="4279c-120">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="4279c-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="4279c-121">Annehmen</span><span class="sxs-lookup"><span data-stu-id="4279c-121">Accept</span></span>](#accept) | <span data-ttu-id="4279c-122">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4279c-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="4279c-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4279c-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4279c-124">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4279c-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="4279c-125">Member</span><span class="sxs-lookup"><span data-stu-id="4279c-125">Members</span></span>

#### <span data-ttu-id="4279c-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="4279c-126">DefaultText</span></span> 

<span data-ttu-id="4279c-127">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4279c-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="4279c-128">public String [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="4279c-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="4279c-129">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4279c-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="4279c-130">Art</span><span class="sxs-lookup"><span data-stu-id="4279c-130">Kind</span></span> 

<span data-ttu-id="4279c-131">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="4279c-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="4279c-132">öffentliche CoreWebView2ScriptDialogKind- [Art](#kind)</span><span class="sxs-lookup"><span data-stu-id="4279c-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="4279c-133">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="4279c-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="4279c-134">Meldung</span><span class="sxs-lookup"><span data-stu-id="4279c-134">Message</span></span> 

<span data-ttu-id="4279c-135">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="4279c-135">The message of the dialog box.</span></span>

> <span data-ttu-id="4279c-136">[Nachricht](#message) für öffentliche Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4279c-136">public string [Message](#message)</span></span>

<span data-ttu-id="4279c-137">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="4279c-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="4279c-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="4279c-138">ResultText</span></span> 

<span data-ttu-id="4279c-139">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4279c-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="4279c-140">public String [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="4279c-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="4279c-141">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4279c-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="4279c-142">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4279c-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="4279c-143">URI</span><span class="sxs-lookup"><span data-stu-id="4279c-143">Uri</span></span> 

<span data-ttu-id="4279c-144">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="4279c-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="4279c-145">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="4279c-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="4279c-146">Annehmen</span><span class="sxs-lookup"><span data-stu-id="4279c-146">Accept</span></span> 

<span data-ttu-id="4279c-147">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4279c-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="4279c-148">public void [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="4279c-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="4279c-149">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4279c-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="4279c-150">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="4279c-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="4279c-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4279c-151">GetDeferral</span></span> 

<span data-ttu-id="4279c-152">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4279c-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="4279c-153">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="4279c-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="4279c-154">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4279c-154">You can use this to complete the event at a later time.</span></span>

