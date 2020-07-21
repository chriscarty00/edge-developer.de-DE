---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883728"
---
# 0.9.430-Interface-ICoreWebView2NavigationCompletedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

Ereignis-args für das NavigationCompleted-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsSuccess](#get_issuccess) | "True", wenn die Navigation erfolgreich ist.
[get_WebErrorStatus](#get_weberrorstatus) | Der Fehlercode, wenn die Navigation fehlgeschlagen ist.
[get_NavigationId](#get_navigationid) | Die ID der Navigation.

## Member

#### get_IsSuccess 

"True", wenn die Navigation erfolgreich ist.

> öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool * issuccess)

Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.

#### get_WebErrorStatus 

Der Fehlercode, wenn die Navigation fehlgeschlagen ist.

> öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS * CORE_WEBVIEW2_WEB_ERROR_STATUS)

#### get_NavigationId 

Die ID der Navigation.

> Public HRESULT [get_NavigationId](#get_navigationid)(UINT64 * navigation_id)

