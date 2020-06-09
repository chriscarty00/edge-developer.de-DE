---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 33450805c7f5117806feb1fb561cd7e0c364f00e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698099"
---
# <span data-ttu-id="817f9-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="817f9-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="817f9-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="817f9-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="817f9-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="817f9-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="817f9-107">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="817f9-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="817f9-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="817f9-108">Summary</span></span>

 <span data-ttu-id="817f9-109">Member</span><span class="sxs-lookup"><span data-stu-id="817f9-109">Members</span></span>                        | <span data-ttu-id="817f9-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="817f9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="817f9-111">Annehmen</span><span class="sxs-lookup"><span data-stu-id="817f9-111">Accept</span></span>](#accept) | <span data-ttu-id="817f9-112">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="817f9-112">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="817f9-113">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="817f9-113">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="817f9-114">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="817f9-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="817f9-115">get_Kind</span><span class="sxs-lookup"><span data-stu-id="817f9-115">get_Kind</span></span>](#get_kind) | <span data-ttu-id="817f9-116">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="817f9-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="817f9-117">get_Message</span><span class="sxs-lookup"><span data-stu-id="817f9-117">get_Message</span></span>](#get_message) | <span data-ttu-id="817f9-118">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="817f9-118">The message of the dialog box.</span></span>
[<span data-ttu-id="817f9-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="817f9-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="817f9-120">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="817f9-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="817f9-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="817f9-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="817f9-122">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="817f9-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="817f9-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="817f9-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="817f9-124">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="817f9-124">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="817f9-125">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="817f9-125">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="817f9-126">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="817f9-126">Set the ResultText property.</span></span>

## <span data-ttu-id="817f9-127">Member</span><span class="sxs-lookup"><span data-stu-id="817f9-127">Members</span></span>

#### <span data-ttu-id="817f9-128">Annehmen</span><span class="sxs-lookup"><span data-stu-id="817f9-128">Accept</span></span> 

<span data-ttu-id="817f9-129">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="817f9-129">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="817f9-130">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="817f9-130">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="817f9-131">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="817f9-131">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="817f9-132">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="817f9-132">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="817f9-133">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="817f9-133">get_DefaultText</span></span> 

<span data-ttu-id="817f9-134">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="817f9-134">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="817f9-135">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="817f9-135">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="817f9-136">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="817f9-136">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="817f9-137">get_Kind</span><span class="sxs-lookup"><span data-stu-id="817f9-137">get_Kind</span></span> 

<span data-ttu-id="817f9-138">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="817f9-138">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="817f9-139">öffentliche HRESULT- [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="817f9-139">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="817f9-140">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="817f9-140">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="817f9-141">get_Message</span><span class="sxs-lookup"><span data-stu-id="817f9-141">get_Message</span></span> 

<span data-ttu-id="817f9-142">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="817f9-142">The message of the dialog box.</span></span>

> <span data-ttu-id="817f9-143">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="817f9-143">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="817f9-144">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="817f9-144">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="817f9-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="817f9-145">get_ResultText</span></span> 

<span data-ttu-id="817f9-146">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="817f9-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="817f9-147">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="817f9-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="817f9-148">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="817f9-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="817f9-149">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="817f9-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="817f9-150">get_Uri</span><span class="sxs-lookup"><span data-stu-id="817f9-150">get_Uri</span></span> 

<span data-ttu-id="817f9-151">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="817f9-151">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="817f9-152">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="817f9-152">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="817f9-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="817f9-153">GetDeferral</span></span> 

<span data-ttu-id="817f9-154">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](icorewebview2deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="817f9-154">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="817f9-155">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="817f9-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="817f9-156">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="817f9-156">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="817f9-157">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="817f9-157">put_ResultText</span></span> 

<span data-ttu-id="817f9-158">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="817f9-158">Set the ResultText property.</span></span>

> <span data-ttu-id="817f9-159">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="817f9-159">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

