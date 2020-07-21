---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: e3177f159ff397ee9d4781936aa32f2715d4af02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886087"
---
# <span data-ttu-id="3f9a1-104">0.8.355-Interface-IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="3f9a1-104">0.8.355 - interface IWebView2Environment2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="3f9a1-105">Zusätzliche vom Environment-Objekt implementierte Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="3f9a1-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="3f9a1-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="3f9a1-106">Summary</span></span>

 <span data-ttu-id="3f9a1-107">Member</span><span class="sxs-lookup"><span data-stu-id="3f9a1-107">Members</span></span>                        | <span data-ttu-id="3f9a1-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="3f9a1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f9a1-109">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3f9a1-109">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="3f9a1-110">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="3f9a1-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="3f9a1-111">Weitere Informationen finden Sie auf der [IWebView2Environment](IWebView2Environment.md) -Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="3f9a1-111">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="3f9a1-112">Sie können QueryInterface für diese Schnittstelle aus dem Objekt, das [IWebView2Environment](IWebView2Environment.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="3f9a1-112">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="3f9a1-113">Member</span><span class="sxs-lookup"><span data-stu-id="3f9a1-113">Members</span></span>

#### <span data-ttu-id="3f9a1-114">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3f9a1-114">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="3f9a1-115">Die Browser Versionsinformationen des aktuellen [IWebView2Environment](IWebView2Environment.md), einschließlich des Kanal namens, wenn es sich nicht um den stabilen Kanal handelt.</span><span class="sxs-lookup"><span data-stu-id="3f9a1-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="3f9a1-116">Public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="3f9a1-116">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="3f9a1-117">Dies entspricht dem Format der GetWebView2BrowserVersionInfo-API.</span><span class="sxs-lookup"><span data-stu-id="3f9a1-117">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="3f9a1-118">Kanalnamen sind "Beta", "dev" und "Canary".</span><span class="sxs-lookup"><span data-stu-id="3f9a1-118">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

