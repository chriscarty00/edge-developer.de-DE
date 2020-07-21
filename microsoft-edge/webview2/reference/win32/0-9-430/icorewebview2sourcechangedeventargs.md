---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2eb2749b71cd9be9dfd25bb686b4ea57e728f179
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883981"
---
# <span data-ttu-id="866dc-104">0.9.430-Interface-ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="866dc-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="866dc-105">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="866dc-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="866dc-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="866dc-106">Summary</span></span>

 <span data-ttu-id="866dc-107">Member</span><span class="sxs-lookup"><span data-stu-id="866dc-107">Members</span></span>                        | <span data-ttu-id="866dc-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="866dc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="866dc-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="866dc-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="866dc-110">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="866dc-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="866dc-111">Member</span><span class="sxs-lookup"><span data-stu-id="866dc-111">Members</span></span>

#### <span data-ttu-id="866dc-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="866dc-112">get_IsNewDocument</span></span> 

<span data-ttu-id="866dc-113">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="866dc-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="866dc-114">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="866dc-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

