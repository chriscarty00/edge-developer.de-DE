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
ms.openlocfilehash: 8451620cc819a6c2934efe80b241e7127861d48e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654110"
---
# <span data-ttu-id="01158-104">Schnittstellen ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="01158-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="01158-105">Der Aufrufer implementiert diese Schnittstelle, um das ScriptDialogOpening-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="01158-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="01158-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="01158-106">Summary</span></span>

 <span data-ttu-id="01158-107">Member</span><span class="sxs-lookup"><span data-stu-id="01158-107">Members</span></span>                        | <span data-ttu-id="01158-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="01158-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="01158-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="01158-109">Invoke</span></span>](#invoke) | <span data-ttu-id="01158-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="01158-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="01158-111">Member</span><span class="sxs-lookup"><span data-stu-id="01158-111">Members</span></span>

#### <span data-ttu-id="01158-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="01158-112">Invoke</span></span> 

<span data-ttu-id="01158-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="01158-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="01158-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="01158-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

