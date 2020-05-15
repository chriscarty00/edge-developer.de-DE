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
ms.openlocfilehash: 62daeaab702b431f787bc800ab79664fc183c4ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653706"
---
# <span data-ttu-id="1ad58-104">Schnittstellen IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="1ad58-104">interface IWebView2WebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="1ad58-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="1ad58-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1ad58-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="1ad58-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="1ad58-107">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ad58-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="1ad58-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1ad58-108">Summary</span></span>

 <span data-ttu-id="1ad58-109">Member</span><span class="sxs-lookup"><span data-stu-id="1ad58-109">Members</span></span>                        | <span data-ttu-id="1ad58-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="1ad58-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1ad58-111">Stop</span><span class="sxs-lookup"><span data-stu-id="1ad58-111">Stop</span></span>](#stop) | <span data-ttu-id="1ad58-112">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="1ad58-112">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="1ad58-113">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="1ad58-113">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="1ad58-114">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1ad58-114">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="1ad58-115">Member</span><span class="sxs-lookup"><span data-stu-id="1ad58-115">Members</span></span>

#### <span data-ttu-id="1ad58-116">Stop</span><span class="sxs-lookup"><span data-stu-id="1ad58-116">Stop</span></span> 

<span data-ttu-id="1ad58-117">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="1ad58-117">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="1ad58-118">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="1ad58-118">public HRESULT [Stop](#stop)()</span></span>

