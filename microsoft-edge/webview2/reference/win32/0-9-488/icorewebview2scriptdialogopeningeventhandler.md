---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 90721fff94948c632c1bb19d861ffc7d4911faff
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884764"
---
# <span data-ttu-id="52092-104">0.9.515-Interface-ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="52092-104">0.9.515 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="52092-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="52092-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="52092-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="52092-106">Summary</span></span>

 <span data-ttu-id="52092-107">Member</span><span class="sxs-lookup"><span data-stu-id="52092-107">Members</span></span>                        | <span data-ttu-id="52092-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="52092-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52092-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="52092-109">Invoke</span></span>](#invoke) | <span data-ttu-id="52092-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52092-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="52092-111">Member</span><span class="sxs-lookup"><span data-stu-id="52092-111">Members</span></span>

#### <span data-ttu-id="52092-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="52092-112">Invoke</span></span> 

<span data-ttu-id="52092-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="52092-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="52092-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="52092-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

