---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 4ba0299f3afbc6fc2846481f52c1000cd338ecd8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885786"
---
# <span data-ttu-id="8ad71-104">0.8.355-Interface-IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="8ad71-104">0.8.355 - interface IWebView2Settings2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="8ad71-105">Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.</span><span class="sxs-lookup"><span data-stu-id="8ad71-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="8ad71-106">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8ad71-106">Summary</span></span>

 <span data-ttu-id="8ad71-107">Member</span><span class="sxs-lookup"><span data-stu-id="8ad71-107">Members</span></span>                        | <span data-ttu-id="8ad71-108">Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8ad71-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8ad71-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8ad71-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="8ad71-110">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad71-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="8ad71-111">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8ad71-111">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="8ad71-112">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ad71-112">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="8ad71-113">Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.</span><span class="sxs-lookup"><span data-stu-id="8ad71-113">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="8ad71-114">Member</span><span class="sxs-lookup"><span data-stu-id="8ad71-114">Members</span></span>

#### <span data-ttu-id="8ad71-115">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8ad71-115">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="8ad71-116">Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad71-116">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="8ad71-117">öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool \* enabled)</span><span class="sxs-lookup"><span data-stu-id="8ad71-117">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="8ad71-118">Ist standardmäßig auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ad71-118">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="8ad71-119">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="8ad71-119">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="8ad71-120">Festlegen der AreDefaultContextMenusEnabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ad71-120">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="8ad71-121">öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)</span><span class="sxs-lookup"><span data-stu-id="8ad71-121">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

