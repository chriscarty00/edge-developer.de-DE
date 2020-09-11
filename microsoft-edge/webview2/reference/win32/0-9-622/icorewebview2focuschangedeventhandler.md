---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: f94e6f8323862d092bf9157061333f5e801db891
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012111"
---
# <span data-ttu-id="0dd26-104">Schnittstellen ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0dd26-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="0dd26-105">Der Aufrufer implementiert diese Methode, um das GotFocus-Ereignis und das LostFocus-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0dd26-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="0dd26-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0dd26-106">Summary</span></span>

 <span data-ttu-id="0dd26-107">Member</span><span class="sxs-lookup"><span data-stu-id="0dd26-107">Members</span></span>                        | <span data-ttu-id="0dd26-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0dd26-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0dd26-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0dd26-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0dd26-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0dd26-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="0dd26-111">Für dieses Ereignis sind keine Ereignisargumente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0dd26-111">There are no event args for this event.</span></span>

## <span data-ttu-id="0dd26-112">Member</span><span class="sxs-lookup"><span data-stu-id="0dd26-112">Members</span></span>

#### <span data-ttu-id="0dd26-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="0dd26-113">Invoke</span></span> 

<span data-ttu-id="0dd26-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0dd26-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0dd26-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="0dd26-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="0dd26-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="0dd26-116">There are no event args and the args parameter will be null.</span></span>

