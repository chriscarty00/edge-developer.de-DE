---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8ea9437530a7f64cc045bfbaa1cc3cc55da77732
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698141"
---
# <span data-ttu-id="ea1b1-104">Schnittstellen ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ea1b1-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="ea1b1-105">Dieser Verweis kann für Versionen nach der SDK-Version 0.9.515 geändert oder nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ea1b1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ea1b1-106">Die neueste API-Referenz finden Sie in der [WebView2-API-Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ea1b1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="ea1b1-107">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ea1b1-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="ea1b1-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ea1b1-108">Summary</span></span>

 <span data-ttu-id="ea1b1-109">Member</span><span class="sxs-lookup"><span data-stu-id="ea1b1-109">Members</span></span>                        | <span data-ttu-id="ea1b1-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="ea1b1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea1b1-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="ea1b1-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="ea1b1-112">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="ea1b1-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="ea1b1-113">Member</span><span class="sxs-lookup"><span data-stu-id="ea1b1-113">Members</span></span>

#### <span data-ttu-id="ea1b1-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="ea1b1-114">get_IsNewDocument</span></span> 

<span data-ttu-id="ea1b1-115">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="ea1b1-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="ea1b1-116">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="ea1b1-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

