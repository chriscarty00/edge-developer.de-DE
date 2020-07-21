---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: d18ccc91d16213cf0a915420b406b65823b3f9d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886451"
---
# <span data-ttu-id="69341-104">Schnittstellen ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="69341-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="69341-105">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="69341-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="69341-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="69341-106">Summary</span></span>

 <span data-ttu-id="69341-107">Member</span><span class="sxs-lookup"><span data-stu-id="69341-107">Members</span></span>                        | <span data-ttu-id="69341-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="69341-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="69341-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="69341-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="69341-110">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="69341-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="69341-111">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="69341-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="69341-112">Member</span><span class="sxs-lookup"><span data-stu-id="69341-112">Members</span></span>

#### <span data-ttu-id="69341-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="69341-113">get_WindowFeatures</span></span> 

<span data-ttu-id="69341-114">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="69341-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="69341-115">Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="69341-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="69341-116">Diese Features können beim Positionieren und Ändern der Größe von neuen WebView-Fenstern berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="69341-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

