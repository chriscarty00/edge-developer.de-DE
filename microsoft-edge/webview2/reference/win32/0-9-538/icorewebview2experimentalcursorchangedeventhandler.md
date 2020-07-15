---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: f58279d1a3c404715be5aad8bf1be5ef120e1d94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880003"
---
# <span data-ttu-id="c7ee7-104">Schnittstellen ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c7ee7-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c7ee7-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c7ee7-106">Der Aufrufer implementiert diese Schnittstelle, um Cursor Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="c7ee7-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c7ee7-107">Summary</span></span>

 <span data-ttu-id="c7ee7-108">Member</span><span class="sxs-lookup"><span data-stu-id="c7ee7-108">Members</span></span>                        | <span data-ttu-id="c7ee7-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c7ee7-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c7ee7-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="c7ee7-110">Invoke</span></span>](#invoke) | <span data-ttu-id="c7ee7-111">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c7ee7-112">Verwenden Sie die Cursor-Eigenschaft, um den neuen Cursor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="c7ee7-113">Member</span><span class="sxs-lookup"><span data-stu-id="c7ee7-113">Members</span></span>

#### <span data-ttu-id="c7ee7-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c7ee7-114">Invoke</span></span> 

<span data-ttu-id="c7ee7-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c7ee7-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c7ee7-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c7ee7-117">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="c7ee7-117">There are no event args and the args parameter will be null.</span></span>

