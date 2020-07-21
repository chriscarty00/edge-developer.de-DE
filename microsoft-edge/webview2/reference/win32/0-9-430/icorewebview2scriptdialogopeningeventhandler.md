---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 31fea451b377b86eda0055a1074706ea12d9538e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884022"
---
# <span data-ttu-id="c76eb-104">0.9.430-Interface-ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="c76eb-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="c76eb-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c76eb-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="c76eb-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c76eb-106">Summary</span></span>

 <span data-ttu-id="c76eb-107">Member</span><span class="sxs-lookup"><span data-stu-id="c76eb-107">Members</span></span>                        | <span data-ttu-id="c76eb-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="c76eb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c76eb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c76eb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c76eb-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c76eb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c76eb-111">Member</span><span class="sxs-lookup"><span data-stu-id="c76eb-111">Members</span></span>

#### <span data-ttu-id="c76eb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c76eb-112">Invoke</span></span> 

<span data-ttu-id="c76eb-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c76eb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c76eb-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender;[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c76eb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

