---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 9ea8f860d637c5d9e49e68917d167380c0418b87
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877371"
---
# <span data-ttu-id="2aa86-104">0.9.515-Interface-ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2aa86-104">0.9.515 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2aa86-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="2aa86-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="2aa86-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="2aa86-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="2aa86-107">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2aa86-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="2aa86-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2aa86-108">Summary</span></span>

 <span data-ttu-id="2aa86-109">Member</span><span class="sxs-lookup"><span data-stu-id="2aa86-109">Members</span></span>                        | <span data-ttu-id="2aa86-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="2aa86-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2aa86-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="2aa86-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="2aa86-112">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="2aa86-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="2aa86-113">Member</span><span class="sxs-lookup"><span data-stu-id="2aa86-113">Members</span></span>

#### <span data-ttu-id="2aa86-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="2aa86-114">get_IsNewDocument</span></span> 

<span data-ttu-id="2aa86-115">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="2aa86-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="2aa86-116">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="2aa86-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

