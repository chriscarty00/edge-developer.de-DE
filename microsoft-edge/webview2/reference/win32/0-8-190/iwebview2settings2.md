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
# Schnittstellen IWebView2Settings2 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2Settings2
  : public IWebView2Settings
```

Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Festlegen der AreDefaultContextMenusEnabled-Eigenschaft

Das Festlegen von Änderungen, die nach dem NavigationStarting-Ereignis vorgenommen wurden, wird erst nach der nächsten Navigation auf oberster Ebene übernommen.

## Member

#### get_AreDefaultContextMenusEnabled 

Die AreDefaultContextMenusEnabled-Eigenschaft wird verwendet, um zu verhindern, dass Standardkontextmenüs Benutzern in WebView angezeigt werden.

> öffentliche HRESULT- [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(bool * enabled)

Ist standardmäßig auf true festgelegt.

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

#### put_AreDefaultContextMenusEnabled 

Festlegen der AreDefaultContextMenusEnabled-Eigenschaft

> öffentliche HRESULT- [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(bool enabled)

