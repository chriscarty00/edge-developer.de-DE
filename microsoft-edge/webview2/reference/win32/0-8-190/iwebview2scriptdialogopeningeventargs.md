---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 867a8f3656b04a566708fc6fc1a24e80b967c1e2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653730"
---
# <span data-ttu-id="fdfa8-104">Schnittstellen IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="fdfa8-104">interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="fdfa8-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="fdfa8-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="fdfa8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="fdfa8-107">Ereignis-args für das [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-107">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="fdfa8-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fdfa8-108">Summary</span></span>

 <span data-ttu-id="fdfa8-109">Member</span><span class="sxs-lookup"><span data-stu-id="fdfa8-109">Members</span></span>                        | <span data-ttu-id="fdfa8-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="fdfa8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fdfa8-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fdfa8-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="fdfa8-112">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="fdfa8-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="fdfa8-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="fdfa8-114">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="fdfa8-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="fdfa8-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="fdfa8-115">get_Message</span></span>](#get_message) | <span data-ttu-id="fdfa8-116">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-116">The message of the dialog box.</span></span>
[<span data-ttu-id="fdfa8-117">Annehmen</span><span class="sxs-lookup"><span data-stu-id="fdfa8-117">Accept</span></span>](#accept) | <span data-ttu-id="fdfa8-118">Der Host kann dies aufrufen, um mit OK zu antworten, um Dialogfelder zu bestätigen und anzufordern, oder diese Methode nicht aufrufen, um "Cancel" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-118">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="fdfa8-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="fdfa8-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="fdfa8-120">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="fdfa8-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="fdfa8-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="fdfa8-122">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="fdfa8-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="fdfa8-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="fdfa8-124">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fdfa8-124">Set the ResultText property.</span></span>
[<span data-ttu-id="fdfa8-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="fdfa8-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="fdfa8-126">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-126">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="fdfa8-127">Member</span><span class="sxs-lookup"><span data-stu-id="fdfa8-127">Members</span></span>

#### <span data-ttu-id="fdfa8-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fdfa8-128">get_Uri</span></span> 

<span data-ttu-id="fdfa8-129">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="fdfa8-130">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="fdfa8-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="fdfa8-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="fdfa8-131">get_Kind</span></span> 

<span data-ttu-id="fdfa8-132">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="fdfa8-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="fdfa8-133">öffentliche HRESULT- [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="fdfa8-133">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="fdfa8-134">get_Message</span><span class="sxs-lookup"><span data-stu-id="fdfa8-134">get_Message</span></span> 

<span data-ttu-id="fdfa8-135">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-135">The message of the dialog box.</span></span>

> <span data-ttu-id="fdfa8-136">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="fdfa8-136">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="fdfa8-137">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="fdfa8-138">Annehmen</span><span class="sxs-lookup"><span data-stu-id="fdfa8-138">Accept</span></span> 

<span data-ttu-id="fdfa8-139">Der Host kann dies aufrufen, um mit OK zu antworten, um Dialogfelder zu bestätigen und anzufordern, oder diese Methode nicht aufrufen, um "Cancel" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-139">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="fdfa8-140">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="fdfa8-140">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="fdfa8-141">Aus JavaScript bedeutet dies, dass die Confirm-Funktion true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-141">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="fdfa8-142">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-142">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="fdfa8-143">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="fdfa8-143">get_DefaultText</span></span> 

<span data-ttu-id="fdfa8-144">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-144">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="fdfa8-145">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="fdfa8-145">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="fdfa8-146">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-146">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="fdfa8-147">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="fdfa8-147">get_ResultText</span></span> 

<span data-ttu-id="fdfa8-148">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-148">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="fdfa8-149">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="fdfa8-149">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="fdfa8-150">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-150">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="fdfa8-151">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-151">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="fdfa8-152">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="fdfa8-152">put_ResultText</span></span> 

<span data-ttu-id="fdfa8-153">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fdfa8-153">Set the ResultText property.</span></span>

> <span data-ttu-id="fdfa8-154">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="fdfa8-154">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="fdfa8-155">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="fdfa8-155">GetDeferral</span></span> 

<span data-ttu-id="fdfa8-156">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-156">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="fdfa8-157">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="fdfa8-157">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="fdfa8-158">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fdfa8-158">You can use this to complete the event at a later time.</span></span>

