---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9c8cd627275a98382f079bc4f64dd7f565d46630
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654093"
---
# <span data-ttu-id="67885-104">Schnittstellen ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="67885-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="67885-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.488 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="67885-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="67885-106">Der Aufrufer implementiert diese Schnittstelle, um Cursor Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="67885-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="67885-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="67885-107">Summary</span></span>

 <span data-ttu-id="67885-108">Member</span><span class="sxs-lookup"><span data-stu-id="67885-108">Members</span></span>                        | <span data-ttu-id="67885-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="67885-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67885-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="67885-110">Invoke</span></span>](#invoke) | <span data-ttu-id="67885-111">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="67885-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="67885-112">Verwenden Sie die Cursor-Eigenschaft, um den neuen Cursor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="67885-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="67885-113">Member</span><span class="sxs-lookup"><span data-stu-id="67885-113">Members</span></span>

#### <span data-ttu-id="67885-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="67885-114">Invoke</span></span> 

<span data-ttu-id="67885-115">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="67885-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="67885-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="67885-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="67885-117">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="67885-117">There are no event args and the args parameter will be null.</span></span>

