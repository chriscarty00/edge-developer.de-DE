---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 9332786935ba79adfd6ef215c9e11afa24c5ceb2
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012007"
---
# <span data-ttu-id="9d63c-104">Schnittstellen ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9d63c-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9d63c-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="9d63c-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="9d63c-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9d63c-106">Summary</span></span>

 <span data-ttu-id="9d63c-107">Member</span><span class="sxs-lookup"><span data-stu-id="9d63c-107">Members</span></span>                        | <span data-ttu-id="9d63c-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9d63c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d63c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d63c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9d63c-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d63c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="9d63c-111">Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9d63c-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="9d63c-112">Member</span><span class="sxs-lookup"><span data-stu-id="9d63c-112">Members</span></span>

#### <span data-ttu-id="9d63c-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="9d63c-113">Invoke</span></span> 

<span data-ttu-id="9d63c-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d63c-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9d63c-115">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender; IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9d63c-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="9d63c-116">Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9d63c-116">There are no event args and the args parameter will be null.</span></span>

