---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: b9350db7d59c0369bfb16d10e30a23ef3f6bffa5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010460"
---
# <span data-ttu-id="9e831-104">0.9.579-Interface-ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9e831-104">0.9.579 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="9e831-105">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9e831-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="9e831-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9e831-106">Summary</span></span>

 <span data-ttu-id="9e831-107">Member</span><span class="sxs-lookup"><span data-stu-id="9e831-107">Members</span></span>                        | <span data-ttu-id="9e831-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="9e831-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e831-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="9e831-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="9e831-110">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="9e831-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="9e831-111">Member</span><span class="sxs-lookup"><span data-stu-id="9e831-111">Members</span></span>

#### <span data-ttu-id="9e831-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="9e831-112">get_IsNewDocument</span></span> 

<span data-ttu-id="9e831-113">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="9e831-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="9e831-114">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="9e831-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

