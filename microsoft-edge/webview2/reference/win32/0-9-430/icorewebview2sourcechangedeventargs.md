---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 69c569be7e712d0f5cfddbaa180419be8d475ad0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654097"
---
# <span data-ttu-id="239f4-104">Schnittstellen ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="239f4-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="239f4-105">Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="239f4-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="239f4-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="239f4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="239f4-107">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="239f4-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="239f4-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="239f4-108">Summary</span></span>

 <span data-ttu-id="239f4-109">Member</span><span class="sxs-lookup"><span data-stu-id="239f4-109">Members</span></span>                        | <span data-ttu-id="239f4-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="239f4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="239f4-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="239f4-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="239f4-112">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="239f4-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="239f4-113">Member</span><span class="sxs-lookup"><span data-stu-id="239f4-113">Members</span></span>

#### <span data-ttu-id="239f4-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="239f4-114">get_IsNewDocument</span></span> 

<span data-ttu-id="239f4-115">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="239f4-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="239f4-116">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="239f4-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

