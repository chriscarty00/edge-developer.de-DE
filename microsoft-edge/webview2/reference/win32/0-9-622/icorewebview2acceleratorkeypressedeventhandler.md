---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 15ad3a4afb76ea8068066097340af204b45fe416
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012161"
---
# <span data-ttu-id="38573-104">Schnittstellen ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="38573-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="38573-105">Der Aufrufer implementiert diese Schnittstelle, um das AcceleratorKeyPressed-Ereignis zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="38573-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="38573-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="38573-106">Summary</span></span>

 <span data-ttu-id="38573-107">Member</span><span class="sxs-lookup"><span data-stu-id="38573-107">Members</span></span>                        | <span data-ttu-id="38573-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="38573-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="38573-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="38573-109">Invoke</span></span>](#invoke) | <span data-ttu-id="38573-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="38573-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="38573-111">Member</span><span class="sxs-lookup"><span data-stu-id="38573-111">Members</span></span>

#### <span data-ttu-id="38573-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="38573-112">Invoke</span></span> 

<span data-ttu-id="38573-113">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="38573-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="38573-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender; [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="38573-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

