---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: da31478c18841084149e2775daa0a5f59a2543ea
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012054"
---
# <span data-ttu-id="3f680-104">Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="3f680-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

<span data-ttu-id="3f680-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3f680-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3f680-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3f680-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3f680-107">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="3f680-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="3f680-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3f680-108">Summary</span></span>

 <span data-ttu-id="3f680-109">Member</span><span class="sxs-lookup"><span data-stu-id="3f680-109">Members</span></span>                        | <span data-ttu-id="3f680-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3f680-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f680-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="3f680-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="3f680-112">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f680-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="3f680-113">Art</span><span class="sxs-lookup"><span data-stu-id="3f680-113">Kind</span></span>](#kind) | <span data-ttu-id="3f680-114">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="3f680-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="3f680-115">Meldung</span><span class="sxs-lookup"><span data-stu-id="3f680-115">Message</span></span>](#message) | <span data-ttu-id="3f680-116">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="3f680-116">The message of the dialog box.</span></span>
[<span data-ttu-id="3f680-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="3f680-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="3f680-118">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f680-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="3f680-119">URI</span><span class="sxs-lookup"><span data-stu-id="3f680-119">Uri</span></span>](#uri) | <span data-ttu-id="3f680-120">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="3f680-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="3f680-121">Annehmen</span><span class="sxs-lookup"><span data-stu-id="3f680-121">Accept</span></span>](#accept) | <span data-ttu-id="3f680-122">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3f680-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="3f680-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3f680-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="3f680-124">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3f680-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="3f680-125">Member</span><span class="sxs-lookup"><span data-stu-id="3f680-125">Members</span></span>

#### <span data-ttu-id="3f680-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="3f680-126">DefaultText</span></span> 

<span data-ttu-id="3f680-127">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f680-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="3f680-128">public String [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="3f680-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="3f680-129">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f680-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="3f680-130">Art</span><span class="sxs-lookup"><span data-stu-id="3f680-130">Kind</span></span> 

<span data-ttu-id="3f680-131">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="3f680-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="3f680-132">öffentliche CoreWebView2ScriptDialogKind- [Art](#kind)</span><span class="sxs-lookup"><span data-stu-id="3f680-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="3f680-133">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="3f680-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="3f680-134">Meldung</span><span class="sxs-lookup"><span data-stu-id="3f680-134">Message</span></span> 

<span data-ttu-id="3f680-135">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="3f680-135">The message of the dialog box.</span></span>

> <span data-ttu-id="3f680-136">[Nachricht](#message) für öffentliche Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3f680-136">public string [Message](#message)</span></span>

<span data-ttu-id="3f680-137">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="3f680-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="3f680-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="3f680-138">ResultText</span></span> 

<span data-ttu-id="3f680-139">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f680-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="3f680-140">public String [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="3f680-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="3f680-141">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f680-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="3f680-142">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f680-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="3f680-143">URI</span><span class="sxs-lookup"><span data-stu-id="3f680-143">Uri</span></span> 

<span data-ttu-id="3f680-144">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="3f680-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="3f680-145">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="3f680-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="3f680-146">Annehmen</span><span class="sxs-lookup"><span data-stu-id="3f680-146">Accept</span></span> 

<span data-ttu-id="3f680-147">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3f680-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="3f680-148">public void [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="3f680-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="3f680-149">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f680-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="3f680-150">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="3f680-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="3f680-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3f680-151">GetDeferral</span></span> 

<span data-ttu-id="3f680-152">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3f680-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="3f680-153">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="3f680-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="3f680-154">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3f680-154">You can use this to complete the event at a later time.</span></span>

