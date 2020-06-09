---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b44bd47f5352179abcc06ef5fd5b8f613bde455e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698815"
---
# <span data-ttu-id="4b958-104">Schnittstellen ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4b958-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4b958-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="4b958-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4b958-106">Der Aufrufer implementiert diese Schnittstelle, um Cursor Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="4b958-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="4b958-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4b958-107">Summary</span></span>

 <span data-ttu-id="4b958-108">Member</span><span class="sxs-lookup"><span data-stu-id="4b958-108">Members</span></span>                        | <span data-ttu-id="4b958-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="4b958-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4b958-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="4b958-110">Invoke</span></span>](#invoke) | <span data-ttu-id="4b958-111">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4b958-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4b958-112">Verwenden Sie die Cursor-Eigenschaft, um den neuen Cursor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b958-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="4b958-113">Member</span><span class="sxs-lookup"><span data-stu-id="4b958-113">Members</span></span>

#### <span data-ttu-id="4b958-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="4b958-114">Invoke</span></span> 

<span data-ttu-id="4b958-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4b958-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4b958-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4b958-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="4b958-117">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="4b958-117">There are no event args and the args parameter will be null.</span></span>

