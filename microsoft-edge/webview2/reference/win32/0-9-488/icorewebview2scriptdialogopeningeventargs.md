---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: a0372e9319a3dd260092b8bc96c693976b7f1fec
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880320"
---
# <span data-ttu-id="56ac8-104">0.9.515-Interface-ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="56ac8-104">0.9.515 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="56ac8-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="56ac8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="56ac8-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="56ac8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="56ac8-107">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="56ac8-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="56ac8-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="56ac8-108">Summary</span></span>

 <span data-ttu-id="56ac8-109">Member</span><span class="sxs-lookup"><span data-stu-id="56ac8-109">Members</span></span>                        | <span data-ttu-id="56ac8-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="56ac8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56ac8-111">Annehmen</span><span class="sxs-lookup"><span data-stu-id="56ac8-111">Accept</span></span>](#accept) | <span data-ttu-id="56ac8-112">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="56ac8-112">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="56ac8-113">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="56ac8-113">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="56ac8-114">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="56ac8-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="56ac8-115">get_Kind</span><span class="sxs-lookup"><span data-stu-id="56ac8-115">get_Kind</span></span>](#get_kind) | <span data-ttu-id="56ac8-116">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="56ac8-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="56ac8-117">get_Message</span><span class="sxs-lookup"><span data-stu-id="56ac8-117">get_Message</span></span>](#get_message) | <span data-ttu-id="56ac8-118">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="56ac8-118">The message of the dialog box.</span></span>
[<span data-ttu-id="56ac8-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ac8-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="56ac8-120">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56ac8-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="56ac8-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="56ac8-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="56ac8-122">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="56ac8-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="56ac8-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="56ac8-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="56ac8-124">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="56ac8-124">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="56ac8-125">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ac8-125">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="56ac8-126">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56ac8-126">Set the ResultText property.</span></span>

## <span data-ttu-id="56ac8-127">Member</span><span class="sxs-lookup"><span data-stu-id="56ac8-127">Members</span></span>

#### <span data-ttu-id="56ac8-128">Annehmen</span><span class="sxs-lookup"><span data-stu-id="56ac8-128">Accept</span></span> 

<span data-ttu-id="56ac8-129">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="56ac8-129">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="56ac8-130">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="56ac8-130">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="56ac8-131">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56ac8-131">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="56ac8-132">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="56ac8-132">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="56ac8-133">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="56ac8-133">get_DefaultText</span></span> 

<span data-ttu-id="56ac8-134">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="56ac8-134">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="56ac8-135">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="56ac8-135">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="56ac8-136">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56ac8-136">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="56ac8-137">get_Kind</span><span class="sxs-lookup"><span data-stu-id="56ac8-137">get_Kind</span></span> 

<span data-ttu-id="56ac8-138">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="56ac8-138">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="56ac8-139">öffentliche HRESULT- [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="56ac8-139">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="56ac8-140">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="56ac8-140">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="56ac8-141">get_Message</span><span class="sxs-lookup"><span data-stu-id="56ac8-141">get_Message</span></span> 

<span data-ttu-id="56ac8-142">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="56ac8-142">The message of the dialog box.</span></span>

> <span data-ttu-id="56ac8-143">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="56ac8-143">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="56ac8-144">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="56ac8-144">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="56ac8-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ac8-145">get_ResultText</span></span> 

<span data-ttu-id="56ac8-146">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56ac8-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="56ac8-147">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="56ac8-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="56ac8-148">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="56ac8-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="56ac8-149">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56ac8-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="56ac8-150">get_Uri</span><span class="sxs-lookup"><span data-stu-id="56ac8-150">get_Uri</span></span> 

<span data-ttu-id="56ac8-151">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="56ac8-151">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="56ac8-152">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="56ac8-152">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="56ac8-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="56ac8-153">GetDeferral</span></span> 

<span data-ttu-id="56ac8-154">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="56ac8-154">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="56ac8-155">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="56ac8-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="56ac8-156">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="56ac8-156">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="56ac8-157">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ac8-157">put_ResultText</span></span> 

<span data-ttu-id="56ac8-158">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56ac8-158">Set the ResultText property.</span></span>

> <span data-ttu-id="56ac8-159">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="56ac8-159">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

