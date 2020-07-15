---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 26bbc2a5c55ebe5a9b7519a87b01c4dd17af375c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879562"
---
# <span data-ttu-id="dcb3f-104">Schnittstellen ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="dcb3f-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="dcb3f-105">Der Aufrufer implementiert diese Schnittstelle, um das AcceleratorKeyPressed-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="dcb3f-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="dcb3f-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="dcb3f-106">Summary</span></span>

 <span data-ttu-id="dcb3f-107">Member</span><span class="sxs-lookup"><span data-stu-id="dcb3f-107">Members</span></span>                        | <span data-ttu-id="dcb3f-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="dcb3f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dcb3f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="dcb3f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dcb3f-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dcb3f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="dcb3f-111">Member</span><span class="sxs-lookup"><span data-stu-id="dcb3f-111">Members</span></span>

#### <span data-ttu-id="dcb3f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="dcb3f-112">Invoke</span></span> 

<span data-ttu-id="dcb3f-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dcb3f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dcb3f-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="dcb3f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

