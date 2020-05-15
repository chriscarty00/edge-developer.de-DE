---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8ed1a10a65a07fc359deea18b8aadd4df3a7b055
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654141"
---
# <span data-ttu-id="9ebc2-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="9ebc2-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9ebc2-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9ebc2-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9ebc2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="9ebc2-107">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="9ebc2-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9ebc2-108">Summary</span></span>

 <span data-ttu-id="9ebc2-109">Member</span><span class="sxs-lookup"><span data-stu-id="9ebc2-109">Members</span></span>                        | <span data-ttu-id="9ebc2-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9ebc2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ebc2-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9ebc2-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="9ebc2-112">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="9ebc2-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="9ebc2-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="9ebc2-114">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="9ebc2-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="9ebc2-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="9ebc2-115">get_Message</span></span>](#get_message) | <span data-ttu-id="9ebc2-116">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-116">The message of the dialog box.</span></span>
[<span data-ttu-id="9ebc2-117">Annehmen</span><span class="sxs-lookup"><span data-stu-id="9ebc2-117">Accept</span></span>](#accept) | <span data-ttu-id="9ebc2-118">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="9ebc2-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="9ebc2-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="9ebc2-120">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="9ebc2-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="9ebc2-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="9ebc2-122">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="9ebc2-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="9ebc2-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="9ebc2-124">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9ebc2-124">Set the ResultText property.</span></span>
[<span data-ttu-id="9ebc2-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9ebc2-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9ebc2-126">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="9ebc2-127">Member</span><span class="sxs-lookup"><span data-stu-id="9ebc2-127">Members</span></span>

#### <span data-ttu-id="9ebc2-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9ebc2-128">get_Uri</span></span> 

<span data-ttu-id="9ebc2-129">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="9ebc2-130">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="9ebc2-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="9ebc2-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="9ebc2-131">get_Kind</span></span> 

<span data-ttu-id="9ebc2-132">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="9ebc2-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="9ebc2-133">öffentliche HRESULT- [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="9ebc2-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="9ebc2-134">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="9ebc2-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="9ebc2-135">get_Message</span></span> 

<span data-ttu-id="9ebc2-136">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-136">The message of the dialog box.</span></span>

> <span data-ttu-id="9ebc2-137">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="9ebc2-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="9ebc2-138">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="9ebc2-139">Annehmen</span><span class="sxs-lookup"><span data-stu-id="9ebc2-139">Accept</span></span> 

<span data-ttu-id="9ebc2-140">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="9ebc2-141">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="9ebc2-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="9ebc2-142">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="9ebc2-143">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="9ebc2-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="9ebc2-144">get_DefaultText</span></span> 

<span data-ttu-id="9ebc2-145">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="9ebc2-146">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="9ebc2-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="9ebc2-147">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="9ebc2-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="9ebc2-148">get_ResultText</span></span> 

<span data-ttu-id="9ebc2-149">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="9ebc2-150">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="9ebc2-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="9ebc2-151">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="9ebc2-152">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="9ebc2-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="9ebc2-153">put_ResultText</span></span> 

<span data-ttu-id="9ebc2-154">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9ebc2-154">Set the ResultText property.</span></span>

> <span data-ttu-id="9ebc2-155">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="9ebc2-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="9ebc2-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9ebc2-156">GetDeferral</span></span> 

<span data-ttu-id="9ebc2-157">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="9ebc2-158">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="9ebc2-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="9ebc2-159">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-159">You can use this to complete the event at a later time.</span></span>

