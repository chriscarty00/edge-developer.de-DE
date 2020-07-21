---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 67d0e6e05fb3640e141ec1ae7193746a1200bbd0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884883"
---
# <span data-ttu-id="50d29-104">Schnittstellen ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="50d29-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="50d29-105">Der Aufrufer implementiert diese Schnittstelle, um Cursor Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="50d29-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="50d29-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="50d29-106">Summary</span></span>

 <span data-ttu-id="50d29-107">Member</span><span class="sxs-lookup"><span data-stu-id="50d29-107">Members</span></span>                        | <span data-ttu-id="50d29-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="50d29-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="50d29-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="50d29-109">Invoke</span></span>](#invoke) | <span data-ttu-id="50d29-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="50d29-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="50d29-111">Verwenden Sie die Cursor-Eigenschaft, um den neuen Cursor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50d29-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="50d29-112">Member</span><span class="sxs-lookup"><span data-stu-id="50d29-112">Members</span></span>

#### <span data-ttu-id="50d29-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="50d29-113">Invoke</span></span> 

<span data-ttu-id="50d29-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="50d29-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="50d29-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="50d29-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="50d29-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="50d29-116">There are no event args and the args parameter will be null.</span></span>

