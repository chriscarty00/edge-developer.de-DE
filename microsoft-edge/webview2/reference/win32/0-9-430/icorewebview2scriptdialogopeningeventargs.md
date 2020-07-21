---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: cd8f96787d289ab0fe649244ce665445efdbcecf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884043"
---
# <span data-ttu-id="2ccff-104">0.9.430-Interface-ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="2ccff-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="2ccff-105">Ereignis-args für das ScriptDialogOpening-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2ccff-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="2ccff-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2ccff-106">Summary</span></span>

 <span data-ttu-id="2ccff-107">Member</span><span class="sxs-lookup"><span data-stu-id="2ccff-107">Members</span></span>                        | <span data-ttu-id="2ccff-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2ccff-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ccff-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2ccff-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2ccff-110">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="2ccff-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="2ccff-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="2ccff-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="2ccff-112">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="2ccff-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="2ccff-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="2ccff-113">get_Message</span></span>](#get_message) | <span data-ttu-id="2ccff-114">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="2ccff-114">The message of the dialog box.</span></span>
[<span data-ttu-id="2ccff-115">Annehmen</span><span class="sxs-lookup"><span data-stu-id="2ccff-115">Accept</span></span>](#accept) | <span data-ttu-id="2ccff-116">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2ccff-116">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="2ccff-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="2ccff-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="2ccff-118">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ccff-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="2ccff-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="2ccff-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="2ccff-120">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2ccff-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="2ccff-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="2ccff-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="2ccff-122">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ccff-122">Set the ResultText property.</span></span>
[<span data-ttu-id="2ccff-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2ccff-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2ccff-124">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2ccff-124">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="2ccff-125">Member</span><span class="sxs-lookup"><span data-stu-id="2ccff-125">Members</span></span>

#### <span data-ttu-id="2ccff-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2ccff-126">get_Uri</span></span> 

<span data-ttu-id="2ccff-127">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="2ccff-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="2ccff-128">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2ccff-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2ccff-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="2ccff-129">get_Kind</span></span> 

<span data-ttu-id="2ccff-130">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="2ccff-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="2ccff-131">öffentliche HRESULT- [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="2ccff-131">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="2ccff-132">Akzeptieren, bestätigen, auffordern oder beforeunload.</span><span class="sxs-lookup"><span data-stu-id="2ccff-132">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="2ccff-133">get_Message</span><span class="sxs-lookup"><span data-stu-id="2ccff-133">get_Message</span></span> 

<span data-ttu-id="2ccff-134">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="2ccff-134">The message of the dialog box.</span></span>

> <span data-ttu-id="2ccff-135">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="2ccff-135">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="2ccff-136">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird und für beforeunload leer ist.</span><span class="sxs-lookup"><span data-stu-id="2ccff-136">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="2ccff-137">Annehmen</span><span class="sxs-lookup"><span data-stu-id="2ccff-137">Accept</span></span> 

<span data-ttu-id="2ccff-138">Der Host kann dies aufrufen, um mit OK zu antworten, um die Dialogfelder zu bestätigen, zu bestätigen und zu beforeunload, oder rufen Sie diese Methode nicht auf, um "Cancel" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2ccff-138">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="2ccff-139">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="2ccff-139">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="2ccff-140">Aus JavaScript bedeutet dies, dass die Funktion Confirm und beforeunload true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2ccff-140">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="2ccff-141">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="2ccff-141">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="2ccff-142">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="2ccff-142">get_DefaultText</span></span> 

<span data-ttu-id="2ccff-143">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ccff-143">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="2ccff-144">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="2ccff-144">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="2ccff-145">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2ccff-145">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="2ccff-146">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="2ccff-146">get_ResultText</span></span> 

<span data-ttu-id="2ccff-147">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2ccff-147">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="2ccff-148">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="2ccff-148">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="2ccff-149">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2ccff-149">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="2ccff-150">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2ccff-150">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="2ccff-151">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="2ccff-151">put_ResultText</span></span> 

<span data-ttu-id="2ccff-152">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ccff-152">Set the ResultText property.</span></span>

> <span data-ttu-id="2ccff-153">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="2ccff-153">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="2ccff-154">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2ccff-154">GetDeferral</span></span> 

<span data-ttu-id="2ccff-155">Getstundung kann aufgerufen werden, um ein [ICoreWebView2Deferral](ICoreWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="2ccff-155">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="2ccff-156">öffentliche HRESULT [getstundung](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="2ccff-156">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2ccff-157">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2ccff-157">You can use this to complete the event at a later time.</span></span>

