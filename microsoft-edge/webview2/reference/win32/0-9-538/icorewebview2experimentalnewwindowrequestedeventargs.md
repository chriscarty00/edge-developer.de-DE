---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 855425e5cbdd594c7a4bca12efe1827035ca2f3a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011104"
---
# <span data-ttu-id="51ec3-104">0.9.579-Interface-ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="51ec3-104">0.9.579 - interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="51ec3-105">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="51ec3-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="51ec3-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="51ec3-106">Summary</span></span>

 <span data-ttu-id="51ec3-107">Member</span><span class="sxs-lookup"><span data-stu-id="51ec3-107">Members</span></span>                        | <span data-ttu-id="51ec3-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="51ec3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="51ec3-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="51ec3-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="51ec3-110">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51ec3-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="51ec3-111">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="51ec3-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="51ec3-112">Member</span><span class="sxs-lookup"><span data-stu-id="51ec3-112">Members</span></span>

#### <span data-ttu-id="51ec3-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="51ec3-113">get_WindowFeatures</span></span> 

<span data-ttu-id="51ec3-114">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51ec3-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="51ec3-115">Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="51ec3-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="51ec3-116">Diese Features können beim Positionieren und Ändern der Größe von neuen WebView-Fenstern berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="51ec3-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

