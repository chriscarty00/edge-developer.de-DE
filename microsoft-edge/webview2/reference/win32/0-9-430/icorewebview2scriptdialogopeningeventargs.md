---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: dfd3383318daf94e8060ba62ef1511c9944efe54
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880213"
---
# <span data-ttu-id="a5b67-104">0.9.430-Interface-ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="a5b67-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a5b67-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a5b67-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a5b67-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b67-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="a5b67-107">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a5b67-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="a5b67-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a5b67-108">Summary</span></span>

 <span data-ttu-id="a5b67-109">Member</span><span class="sxs-lookup"><span data-stu-id="a5b67-109">Members</span></span>                        | <span data-ttu-id="a5b67-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a5b67-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a5b67-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a5b67-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="a5b67-112">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="a5b67-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="a5b67-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="a5b67-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="a5b67-114">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="a5b67-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="a5b67-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="a5b67-115">get_Message</span></span>](#get_message) | <span data-ttu-id="a5b67-116">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="a5b67-116">The message of the dialog box.</span></span>
[<span data-ttu-id="a5b67-117">Annehmen</span><span class="sxs-lookup"><span data-stu-id="a5b67-117">Accept</span></span>](#accept) | <span data-ttu-id="a5b67-118">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a5b67-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="a5b67-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="a5b67-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="a5b67-120">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5b67-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="a5b67-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="a5b67-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="a5b67-122">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a5b67-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="a5b67-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="a5b67-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="a5b67-124">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a5b67-124">Set the ResultText property.</span></span>
[<span data-ttu-id="a5b67-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a5b67-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a5b67-126">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a5b67-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="a5b67-127">Member</span><span class="sxs-lookup"><span data-stu-id="a5b67-127">Members</span></span>

#### <span data-ttu-id="a5b67-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a5b67-128">get_Uri</span></span> 

<span data-ttu-id="a5b67-129">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="a5b67-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="a5b67-130">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="a5b67-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="a5b67-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="a5b67-131">get_Kind</span></span> 

<span data-ttu-id="a5b67-132">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="a5b67-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="a5b67-133">öffentliche HRESULT- [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="a5b67-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="a5b67-134">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="a5b67-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="a5b67-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="a5b67-135">get_Message</span></span> 

<span data-ttu-id="a5b67-136">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="a5b67-136">The message of the dialog box.</span></span>

> <span data-ttu-id="a5b67-137">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="a5b67-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="a5b67-138">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="a5b67-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="a5b67-139">Annehmen</span><span class="sxs-lookup"><span data-stu-id="a5b67-139">Accept</span></span> 

<span data-ttu-id="a5b67-140">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a5b67-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="a5b67-141">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="a5b67-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="a5b67-142">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a5b67-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="a5b67-143">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="a5b67-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="a5b67-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="a5b67-144">get_DefaultText</span></span> 

<span data-ttu-id="a5b67-145">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5b67-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="a5b67-146">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="a5b67-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="a5b67-147">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5b67-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="a5b67-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="a5b67-148">get_ResultText</span></span> 

<span data-ttu-id="a5b67-149">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a5b67-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="a5b67-150">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="a5b67-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="a5b67-151">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a5b67-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="a5b67-152">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5b67-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="a5b67-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="a5b67-153">put_ResultText</span></span> 

<span data-ttu-id="a5b67-154">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a5b67-154">Set the ResultText property.</span></span>

> <span data-ttu-id="a5b67-155">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="a5b67-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="a5b67-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a5b67-156">GetDeferral</span></span> 

<span data-ttu-id="a5b67-157">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a5b67-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="a5b67-158">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="a5b67-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="a5b67-159">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a5b67-159">You can use this to complete the event at a later time.</span></span>

