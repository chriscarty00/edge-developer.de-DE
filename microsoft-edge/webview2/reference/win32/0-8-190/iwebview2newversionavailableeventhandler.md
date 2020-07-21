---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 3a9af31477e7b4155bece55ec2faef85efccbd0d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884981"
---
# <span data-ttu-id="87c35-104">0.8.355-Interface-IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="87c35-104">0.8.355 - interface IWebView2NewVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="87c35-105">Der Aufrufer implementiert diese Schnittstelle zum Empfangen von NewVersionAvailable-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="87c35-105">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="87c35-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="87c35-106">Summary</span></span>

 <span data-ttu-id="87c35-107">Member</span><span class="sxs-lookup"><span data-stu-id="87c35-107">Members</span></span>                        | <span data-ttu-id="87c35-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="87c35-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="87c35-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="87c35-109">Invoke</span></span>](#invoke) | <span data-ttu-id="87c35-110">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="87c35-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="87c35-111">Verwenden Sie die get_NewVersion-Methode von [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) , um die neue Versionsnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87c35-111">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="87c35-112">Member</span><span class="sxs-lookup"><span data-stu-id="87c35-112">Members</span></span>

#### <span data-ttu-id="87c35-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="87c35-113">Invoke</span></span> 

<span data-ttu-id="87c35-114">Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="87c35-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="87c35-115">Public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="87c35-115">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

