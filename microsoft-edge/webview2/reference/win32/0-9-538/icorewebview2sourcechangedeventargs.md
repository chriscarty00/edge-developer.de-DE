---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 3e622a8fb5b8ed43e5a23eaab8bd0aa61ed7d193
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879401"
---
# <span data-ttu-id="bb709-104">Schnittstellen ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bb709-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="bb709-105">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="bb709-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="bb709-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="bb709-106">Summary</span></span>

 <span data-ttu-id="bb709-107">Member</span><span class="sxs-lookup"><span data-stu-id="bb709-107">Members</span></span>                        | <span data-ttu-id="bb709-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="bb709-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bb709-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bb709-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="bb709-110">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="bb709-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="bb709-111">Member</span><span class="sxs-lookup"><span data-stu-id="bb709-111">Members</span></span>

#### <span data-ttu-id="bb709-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bb709-112">get_IsNewDocument</span></span> 

<span data-ttu-id="bb709-113">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="bb709-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="bb709-114">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="bb709-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

