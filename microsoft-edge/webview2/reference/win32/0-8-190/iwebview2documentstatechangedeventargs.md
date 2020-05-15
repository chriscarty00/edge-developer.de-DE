---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 342716da2cded9c903f1edd13fb3400c779a9b39
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653954"
---
# <span data-ttu-id="a7273-104">Schnittstellen IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a7273-104">interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a7273-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a7273-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a7273-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="a7273-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="a7273-107">Ereignis-args für das DocumentStateChanged-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a7273-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="a7273-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="a7273-108">Summary</span></span>

 <span data-ttu-id="a7273-109">Member</span><span class="sxs-lookup"><span data-stu-id="a7273-109">Members</span></span>                        | <span data-ttu-id="a7273-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="a7273-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a7273-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="a7273-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="a7273-112">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="a7273-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="a7273-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a7273-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="a7273-114">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="a7273-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="a7273-115">Member</span><span class="sxs-lookup"><span data-stu-id="a7273-115">Members</span></span>

#### <span data-ttu-id="a7273-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="a7273-116">get_IsNewDocument</span></span> 

<span data-ttu-id="a7273-117">"True", wenn die zu navigierende Seite ein neues Dokument ist.</span><span class="sxs-lookup"><span data-stu-id="a7273-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="a7273-118">Public HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="a7273-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="a7273-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a7273-119">get_IsErrorPage</span></span> 

<span data-ttu-id="a7273-120">"True", wenn der geladene Inhalt eine Fehlerseite ist.</span><span class="sxs-lookup"><span data-stu-id="a7273-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="a7273-121">Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="a7273-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

