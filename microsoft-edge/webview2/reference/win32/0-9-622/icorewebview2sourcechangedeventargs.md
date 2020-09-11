---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 7417b4790d327bbd5a415dc1237e0604963598e0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012167"
---
# <span data-ttu-id="b6d45-104">Schnittstellen ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b6d45-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="b6d45-105">Ereignis-args für das Sourcecode-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b6d45-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="b6d45-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b6d45-106">Summary</span></span>

 <span data-ttu-id="b6d45-107">Member</span><span class="sxs-lookup"><span data-stu-id="b6d45-107">Members</span></span>                        | <span data-ttu-id="b6d45-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="b6d45-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b6d45-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="b6d45-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="b6d45-110">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="b6d45-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="b6d45-111">Member</span><span class="sxs-lookup"><span data-stu-id="b6d45-111">Members</span></span>

#### <span data-ttu-id="b6d45-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="b6d45-112">get_IsNewDocument</span></span> 

<span data-ttu-id="b6d45-113">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="b6d45-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="b6d45-114">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="b6d45-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

