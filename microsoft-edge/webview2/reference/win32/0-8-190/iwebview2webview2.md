---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884736"
---
# <span data-ttu-id="e001e-104">0.8.355-Interface-IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="e001e-104">0.8.355 - interface IWebView2WebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="e001e-105">Zusätzliche Funktionen, die vom primären WebView-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e001e-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="e001e-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e001e-106">Summary</span></span>

 <span data-ttu-id="e001e-107">Member</span><span class="sxs-lookup"><span data-stu-id="e001e-107">Members</span></span>                        | <span data-ttu-id="e001e-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e001e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e001e-109">Stop</span><span class="sxs-lookup"><span data-stu-id="e001e-109">Stop</span></span>](#stop) | <span data-ttu-id="e001e-110">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="e001e-110">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="e001e-111">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2WebView](IWebView2WebView.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="e001e-111">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="e001e-112">Weitere Informationen finden Sie auf der [IWebView2WebView](IWebView2WebView.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="e001e-112">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="e001e-113">Member</span><span class="sxs-lookup"><span data-stu-id="e001e-113">Members</span></span>

#### <span data-ttu-id="e001e-114">Stop</span><span class="sxs-lookup"><span data-stu-id="e001e-114">Stop</span></span> 

<span data-ttu-id="e001e-115">Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.</span><span class="sxs-lookup"><span data-stu-id="e001e-115">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="e001e-116">öffentlicher HRESULT- [Stopp](#stop)()</span><span class="sxs-lookup"><span data-stu-id="e001e-116">public HRESULT [Stop](#stop)()</span></span>

