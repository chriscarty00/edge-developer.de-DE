---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885793"
---
# <span data-ttu-id="8c325-104">0.8.355-Interface-IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="8c325-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="8c325-105">Ereignis-args für das [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8c325-105">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="8c325-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8c325-106">Summary</span></span>

 <span data-ttu-id="8c325-107">Member</span><span class="sxs-lookup"><span data-stu-id="8c325-107">Members</span></span>                        | <span data-ttu-id="8c325-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8c325-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8c325-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8c325-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="8c325-110">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="8c325-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="8c325-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="8c325-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="8c325-112">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="8c325-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="8c325-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="8c325-113">get_Message</span></span>](#get_message) | <span data-ttu-id="8c325-114">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="8c325-114">The message of the dialog box.</span></span>
[<span data-ttu-id="8c325-115">Annehmen</span><span class="sxs-lookup"><span data-stu-id="8c325-115">Accept</span></span>](#accept) | <span data-ttu-id="8c325-116">Der Host kann dies aufrufen, um mit OK zu antworten, um Dialogfelder zu bestätigen und anzufordern, oder diese Methode nicht aufrufen, um "Cancel" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8c325-116">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="8c325-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="8c325-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="8c325-118">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c325-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="8c325-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="8c325-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="8c325-120">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c325-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="8c325-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="8c325-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="8c325-122">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c325-122">Set the ResultText property.</span></span>
[<span data-ttu-id="8c325-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8c325-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="8c325-124">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8c325-124">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="8c325-125">Member</span><span class="sxs-lookup"><span data-stu-id="8c325-125">Members</span></span>

#### <span data-ttu-id="8c325-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8c325-126">get_Uri</span></span> 

<span data-ttu-id="8c325-127">Der URI der Seite, die das Dialogfeld angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="8c325-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="8c325-128">Public HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="8c325-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="8c325-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="8c325-129">get_Kind</span></span> 

<span data-ttu-id="8c325-130">Das Dialogfeld "JavaScript-Art"</span><span class="sxs-lookup"><span data-stu-id="8c325-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="8c325-131">öffentliche HRESULT- [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* Art)</span><span class="sxs-lookup"><span data-stu-id="8c325-131">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="8c325-132">get_Message</span><span class="sxs-lookup"><span data-stu-id="8c325-132">get_Message</span></span> 

<span data-ttu-id="8c325-133">Die Meldung des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="8c325-133">The message of the dialog box.</span></span>

> <span data-ttu-id="8c325-134">öffentliche HRESULT- [get_Message](#get_message)(LPWSTR \*-Meldung)</span><span class="sxs-lookup"><span data-stu-id="8c325-134">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="8c325-135">Von JavaScript Dies ist der erste Parameter, der an Alert, Confirm und prompt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c325-135">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="8c325-136">Annehmen</span><span class="sxs-lookup"><span data-stu-id="8c325-136">Accept</span></span> 

<span data-ttu-id="8c325-137">Der Host kann dies aufrufen, um mit OK zu antworten, um Dialogfelder zu bestätigen und anzufordern, oder diese Methode nicht aufrufen, um "Cancel" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8c325-137">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="8c325-138">öffentliche HRESULT- [Annahme](#accept)()</span><span class="sxs-lookup"><span data-stu-id="8c325-138">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="8c325-139">Aus JavaScript bedeutet dies, dass die Confirm-Funktion true zurückgibt, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c325-139">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="8c325-140">Und für die prompt-Funktion gibt Sie den Wert von ResultText zurück, wenn Accept aufgerufen wird, und gibt andernfalls false zurück.</span><span class="sxs-lookup"><span data-stu-id="8c325-140">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="8c325-141">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="8c325-141">get_DefaultText</span></span> 

<span data-ttu-id="8c325-142">Der zweite Parameter, der an das JavaScript-Eingabe Aufforderungsdialogfeld übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c325-142">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="8c325-143">Public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="8c325-143">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="8c325-144">Dies ist der Standardwert, der für das Ergebnis der Eingabeaufforderung JavaScript-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c325-144">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="8c325-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="8c325-145">get_ResultText</span></span> 

<span data-ttu-id="8c325-146">Der Rückgabewert der JavaScript-Aufforderungs Funktion, wenn Accept aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c325-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="8c325-147">Public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="8c325-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="8c325-148">Dies wird für Dialog Arten außer Eingabeaufforderung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8c325-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="8c325-149">Wenn Accept nicht aufgerufen wird, wird dieser Wert ignoriert, und von der Eingabeaufforderung wird false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c325-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="8c325-150">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="8c325-150">put_ResultText</span></span> 

<span data-ttu-id="8c325-151">Festlegen der ResultText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c325-151">Set the ResultText property.</span></span>

> <span data-ttu-id="8c325-152">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="8c325-152">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="8c325-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8c325-153">GetDeferral</span></span> 

<span data-ttu-id="8c325-154">Getstundung kann aufgerufen werden, um ein [IWebView2Deferral](IWebView2Deferral.md) -Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8c325-154">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="8c325-155">öffentliche HRESULT [getstundung](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Stundung)</span><span class="sxs-lookup"><span data-stu-id="8c325-155">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="8c325-156">Sie können dies verwenden, um das Ereignis zu einem späteren Zeitpunkt abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8c325-156">You can use this to complete the event at a later time.</span></span>

