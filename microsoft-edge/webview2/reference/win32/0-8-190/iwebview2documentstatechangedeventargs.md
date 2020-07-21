---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 75741c1ba1d835d1c26c7d1db0845071216e0705
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886122"
---
# <span data-ttu-id="27738-104">0.8.355-Interface-IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="27738-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="27738-105">Ereignis-args für das DocumentStateChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="27738-105">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="27738-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="27738-106">Summary</span></span>

 <span data-ttu-id="27738-107">Member</span><span class="sxs-lookup"><span data-stu-id="27738-107">Members</span></span>                        | <span data-ttu-id="27738-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="27738-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="27738-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="27738-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="27738-110">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="27738-110">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="27738-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="27738-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="27738-112">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="27738-112">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="27738-113">Member</span><span class="sxs-lookup"><span data-stu-id="27738-113">Members</span></span>

#### <span data-ttu-id="27738-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="27738-114">get_IsNewDocument</span></span> 

<span data-ttu-id="27738-115">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="27738-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="27738-116">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="27738-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="27738-117">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="27738-117">get_IsErrorPage</span></span> 

<span data-ttu-id="27738-118">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="27738-118">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="27738-119">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="27738-119">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

