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
ms.openlocfilehash: 6d4c5e7893f9be78baca25e8976ca889ef9826c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654057"
---
# <span data-ttu-id="bdf2d-104">Schnittstellen ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bdf2d-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="bdf2d-105">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="bdf2d-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="bdf2d-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bdf2d-106">Summary</span></span>

 <span data-ttu-id="bdf2d-107">Member</span><span class="sxs-lookup"><span data-stu-id="bdf2d-107">Members</span></span>                        | <span data-ttu-id="bdf2d-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="bdf2d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bdf2d-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bdf2d-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="bdf2d-110">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="bdf2d-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="bdf2d-111">Member</span><span class="sxs-lookup"><span data-stu-id="bdf2d-111">Members</span></span>

#### <span data-ttu-id="bdf2d-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bdf2d-112">get_IsNewDocument</span></span> 

<span data-ttu-id="bdf2d-113">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="bdf2d-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="bdf2d-114">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="bdf2d-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

