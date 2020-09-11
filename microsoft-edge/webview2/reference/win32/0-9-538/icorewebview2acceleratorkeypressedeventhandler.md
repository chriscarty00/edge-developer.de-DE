---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 104291f2bbf285737311a205188a1b549906becf
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011216"
---
# <span data-ttu-id="faf38-104">0.9.579-Interface-ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="faf38-104">0.9.579 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="faf38-105">Der Aufrufer implementiert diese Schnittstelle, um das AcceleratorKeyPressed-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="faf38-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="faf38-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="faf38-106">Summary</span></span>

 <span data-ttu-id="faf38-107">Member</span><span class="sxs-lookup"><span data-stu-id="faf38-107">Members</span></span>                        | <span data-ttu-id="faf38-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="faf38-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="faf38-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="faf38-109">Invoke</span></span>](#invoke) | <span data-ttu-id="faf38-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="faf38-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="faf38-111">Member</span><span class="sxs-lookup"><span data-stu-id="faf38-111">Members</span></span>

#### <span data-ttu-id="faf38-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="faf38-112">Invoke</span></span> 

<span data-ttu-id="faf38-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="faf38-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="faf38-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="faf38-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

