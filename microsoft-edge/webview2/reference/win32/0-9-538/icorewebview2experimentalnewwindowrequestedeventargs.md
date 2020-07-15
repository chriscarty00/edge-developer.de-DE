---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 39d52b1231e767739b63b3759cdd08e4c9b26be3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879989"
---
# <span data-ttu-id="273f5-104">Schnittstellen ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="273f5-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="273f5-105">Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="273f5-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="273f5-106">Ereignis-args für das mswebviewnewwindowrequested-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="273f5-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="273f5-107">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="273f5-107">Summary</span></span>

 <span data-ttu-id="273f5-108">Member</span><span class="sxs-lookup"><span data-stu-id="273f5-108">Members</span></span>                        | <span data-ttu-id="273f5-109">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="273f5-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="273f5-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="273f5-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="273f5-111">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="273f5-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="273f5-112">Das Ereignis wird ausgelöst, wenn Inhalt in WebView zum Öffnen eines neuen Fensters angefordert wird (über Window. Open () usw.).</span><span class="sxs-lookup"><span data-stu-id="273f5-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="273f5-113">Member</span><span class="sxs-lookup"><span data-stu-id="273f5-113">Members</span></span>

#### <span data-ttu-id="273f5-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="273f5-114">get_WindowFeatures</span></span> 

<span data-ttu-id="273f5-115">Fenster Features, die vom Window. Open-Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="273f5-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="273f5-116">Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="273f5-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="273f5-117">Diese Features können beim Positionieren und Ändern der Größe von neuen WebView-Fenstern berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="273f5-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

