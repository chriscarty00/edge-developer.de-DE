---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: d127af61bfdc9bf692fa48489d7982bf2c6cad86
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878547"
---
# <span data-ttu-id="975aa-104">0.8.355-Interface-IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="975aa-104">0.8.355 - interface IWebView2Environment2</span></span> 

> [!NOTE]
> <span data-ttu-id="975aa-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="975aa-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="975aa-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="975aa-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="975aa-107">Zusätzliche vom Environment-Objekt implementierte Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="975aa-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="975aa-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="975aa-108">Summary</span></span>

 <span data-ttu-id="975aa-109">Member</span><span class="sxs-lookup"><span data-stu-id="975aa-109">Members</span></span>                        | <span data-ttu-id="975aa-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="975aa-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="975aa-111">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="975aa-111">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="975aa-112">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="975aa-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="975aa-113">Weitere Informationen finden Sie auf der [IWebView2Environment](IWebView2Environment.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="975aa-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="975aa-114">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2Environment](IWebView2Environment.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="975aa-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="975aa-115">Member</span><span class="sxs-lookup"><span data-stu-id="975aa-115">Members</span></span>

#### <span data-ttu-id="975aa-116">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="975aa-116">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="975aa-117">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="975aa-117">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="975aa-118">Public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="975aa-118">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="975aa-119">Dies entspricht dem Format der GetWebView2BrowserVersionInfo-API.</span><span class="sxs-lookup"><span data-stu-id="975aa-119">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="975aa-120">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="975aa-120">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

