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
ms.openlocfilehash: cb317e9078e48ed14091eb2eda6ff9d59a19c6ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653853"
---
# <span data-ttu-id="e1f0b-104">Schnittstellen IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="e1f0b-104">interface IWebView2Settings2</span></span> 

> [!NOTE]
> <span data-ttu-id="e1f0b-105">Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e1f0b-106">Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e1f0b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="e1f0b-107">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="e1f0b-108">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e1f0b-108">Summary</span></span>

 <span data-ttu-id="e1f0b-109">Member</span><span class="sxs-lookup"><span data-stu-id="e1f0b-109">Members</span></span>                        | <span data-ttu-id="e1f0b-110">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e1f0b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1f0b-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f0b-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="e1f0b-112">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="e1f0b-113">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f0b-113">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="e1f0b-114">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1f0b-114">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="e1f0b-115">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-115">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="e1f0b-116">Member</span><span class="sxs-lookup"><span data-stu-id="e1f0b-116">Members</span></span>

#### <span data-ttu-id="e1f0b-117">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f0b-117">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="e1f0b-118">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-118">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="e1f0b-119">öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="e1f0b-119">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="e1f0b-120">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1f0b-120">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="e1f0b-121">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="e1f0b-121">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="e1f0b-122">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e1f0b-122">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="e1f0b-123">öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="e1f0b-123">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

