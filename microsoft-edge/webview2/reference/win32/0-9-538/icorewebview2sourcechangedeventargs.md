---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 4ae58375f0158a3876b284e16a579149dc6db9a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698895"
---
# <span data-ttu-id="428f2-104">Schnittstellen ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="428f2-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="428f2-105">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="428f2-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="428f2-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="428f2-106">Summary</span></span>

 <span data-ttu-id="428f2-107">Member</span><span class="sxs-lookup"><span data-stu-id="428f2-107">Members</span></span>                        | <span data-ttu-id="428f2-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="428f2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="428f2-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="428f2-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="428f2-110">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="428f2-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="428f2-111">Member</span><span class="sxs-lookup"><span data-stu-id="428f2-111">Members</span></span>

#### <span data-ttu-id="428f2-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="428f2-112">get_IsNewDocument</span></span> 

<span data-ttu-id="428f2-113">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="428f2-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="428f2-114">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="428f2-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

