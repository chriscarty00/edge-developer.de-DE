---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 7bccd93aeec2c5cfbc181ce5ab1cf58e29da48ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884295"
---
# 0.9.430-Interface-ICoreWebView2ContentLoadingEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

Ereignis-args für das ContentLoading-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsErrorPage](#get_iserrorpage) | "True", wenn der geladene Inhalt eine Fehlerseite ist.
[get_NavigationId](#get_navigationid) | Die ID der Navigation.

## Member

#### get_IsErrorPage 

"True", wenn der geladene Inhalt eine Fehlerseite ist.

> Public HRESULT [get_IsErrorPage](#get_iserrorpage)(bool * IsErrorPage)

#### get_NavigationId 

Die ID der Navigation.

> Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 * navigation_id)

