---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8a9f1b1e44353796c6d3b57d3f4c6f3d4997aad5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880199"
---
# <span data-ttu-id="745bc-104">0.9.430-Interface-ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="745bc-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="745bc-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="745bc-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="745bc-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="745bc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="745bc-107">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="745bc-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="745bc-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="745bc-108">Summary</span></span>

 <span data-ttu-id="745bc-109">Member</span><span class="sxs-lookup"><span data-stu-id="745bc-109">Members</span></span>                        | <span data-ttu-id="745bc-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="745bc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="745bc-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="745bc-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="745bc-112">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="745bc-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="745bc-113">Member</span><span class="sxs-lookup"><span data-stu-id="745bc-113">Members</span></span>

#### <span data-ttu-id="745bc-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="745bc-114">get_IsNewDocument</span></span> 

<span data-ttu-id="745bc-115">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="745bc-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="745bc-116">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="745bc-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

