---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: e9bf743f9417645bee7a5692f5ef9ca9b646e7ab
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010222"
---
# <span data-ttu-id="2e130-104">0.9.579-Interface-ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2e130-104">0.9.579 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="2e130-105">Der Aufrufer implementiert diese Schnittstelle, um Cursor Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2e130-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="2e130-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2e130-106">Summary</span></span>

 <span data-ttu-id="2e130-107">Member</span><span class="sxs-lookup"><span data-stu-id="2e130-107">Members</span></span>                        | <span data-ttu-id="2e130-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2e130-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2e130-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2e130-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2e130-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2e130-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2e130-111">Verwenden Sie die Cursor-Eigenschaft, um den neuen Cursor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2e130-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="2e130-112">Member</span><span class="sxs-lookup"><span data-stu-id="2e130-112">Members</span></span>

#### <span data-ttu-id="2e130-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="2e130-113">Invoke</span></span> 

<span data-ttu-id="2e130-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2e130-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2e130-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2e130-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="2e130-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="2e130-116">There are no event args and the args parameter will be null.</span></span>

