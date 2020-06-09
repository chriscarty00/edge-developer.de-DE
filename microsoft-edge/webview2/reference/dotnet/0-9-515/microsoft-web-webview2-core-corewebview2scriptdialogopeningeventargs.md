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
ms.openlocfilehash: 1359e9472455acf2949cc329de4280ad970a3b68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697308"
---
# <span data-ttu-id="bd0c1-104">Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs Klasse</span><span class="sxs-lookup"><span data-stu-id="bd0c1-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="bd0c1-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bd0c1-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="bd0c1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="bd0c1-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="bd0c1-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="bd0c1-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="bd0c1-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="bd0c1-109">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-109">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="bd0c1-110">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bd0c1-110">Summary</span></span>

 <span data-ttu-id="bd0c1-111">Member</span><span class="sxs-lookup"><span data-stu-id="bd0c1-111">Members</span></span>                        | <span data-ttu-id="bd0c1-112">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="bd0c1-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bd0c1-113">DefaultText</span><span class="sxs-lookup"><span data-stu-id="bd0c1-113">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="bd0c1-114">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="bd0c1-115">Art</span><span class="sxs-lookup"><span data-stu-id="bd0c1-115">Kind</span></span>](#kind) | <span data-ttu-id="bd0c1-116">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="bd0c1-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="bd0c1-117">Meldung</span><span class="sxs-lookup"><span data-stu-id="bd0c1-117">Message</span></span>](#message) | <span data-ttu-id="bd0c1-118">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-118">The message of the dialog box.</span></span>
[<span data-ttu-id="bd0c1-119">ResultText</span><span class="sxs-lookup"><span data-stu-id="bd0c1-119">ResultText</span></span>](#resulttext) | <span data-ttu-id="bd0c1-120">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="bd0c1-121">URI</span><span class="sxs-lookup"><span data-stu-id="bd0c1-121">Uri</span></span>](#uri) | <span data-ttu-id="bd0c1-122">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="bd0c1-123">Annehmen</span><span class="sxs-lookup"><span data-stu-id="bd0c1-123">Accept</span></span>](#accept) | <span data-ttu-id="bd0c1-124">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-124">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="bd0c1-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bd0c1-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="bd0c1-126">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-126">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="bd0c1-127">Member</span><span class="sxs-lookup"><span data-stu-id="bd0c1-127">Members</span></span>

#### <span data-ttu-id="bd0c1-128">DefaultText</span><span class="sxs-lookup"><span data-stu-id="bd0c1-128">DefaultText</span></span> 

<span data-ttu-id="bd0c1-129">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-129">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="bd0c1-130">public String [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="bd0c1-130">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="bd0c1-131">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-131">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="bd0c1-132">Art</span><span class="sxs-lookup"><span data-stu-id="bd0c1-132">Kind</span></span> 

<span data-ttu-id="bd0c1-133">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="bd0c1-133">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="bd0c1-134">öffentliche CoreWebView2ScriptDialogKind- [Art](#kind)</span><span class="sxs-lookup"><span data-stu-id="bd0c1-134">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="bd0c1-135">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-135">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="bd0c1-136">Meldung</span><span class="sxs-lookup"><span data-stu-id="bd0c1-136">Message</span></span> 

<span data-ttu-id="bd0c1-137">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-137">The message of the dialog box.</span></span>

> <span data-ttu-id="bd0c1-138">[Nachricht](#message) für öffentliche Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bd0c1-138">public string [Message](#message)</span></span>

<span data-ttu-id="bd0c1-139">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-139">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="bd0c1-140">ResultText</span><span class="sxs-lookup"><span data-stu-id="bd0c1-140">ResultText</span></span> 

<span data-ttu-id="bd0c1-141">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-141">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="bd0c1-142">public String [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="bd0c1-142">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="bd0c1-143">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-143">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="bd0c1-144">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-144">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="bd0c1-145">URI</span><span class="sxs-lookup"><span data-stu-id="bd0c1-145">Uri</span></span> 

<span data-ttu-id="bd0c1-146">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-146">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="bd0c1-147">öffentlicher Zeichenfolgen- [URI](#uri)</span><span class="sxs-lookup"><span data-stu-id="bd0c1-147">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="bd0c1-148">Annehmen</span><span class="sxs-lookup"><span data-stu-id="bd0c1-148">Accept</span></span> 

<span data-ttu-id="bd0c1-149">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-149">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="bd0c1-150">public void [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="bd0c1-150">public void [Accept](#accept)()</span></span>

<span data-ttu-id="bd0c1-151">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-151">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="bd0c1-152">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-152">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="bd0c1-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bd0c1-153">GetDeferral</span></span> 

<span data-ttu-id="bd0c1-154">Getstundung kann aufgerufen werden, um ein CoreWebView2Deferral-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-154">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="bd0c1-155">Public CoreWebView2Deferral [getstundungal](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="bd0c1-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="bd0c1-156">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bd0c1-156">You can use this to complete the event at a later time.</span></span>

