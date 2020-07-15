---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 7c10e669b4caf13f43f858e343c9bad3da155518
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878414"
---
# 0.8.355-Interface-IWebView2NavigationCompletedEventArgs 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

Ereignis-args für das NavigationCompleted-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsSuccess](#get_issuccess) | "True", wenn die Navigation erfolgreich ist.
[get_WebErrorStatus](#get_weberrorstatus) | Der Fehlercode, wenn die Navigation fehlgeschlagen ist.

## Member

#### get_IsSuccess 

"True", wenn die Navigation erfolgreich ist.

> öffentliche HRESULT- [get_IsSuccess](#get_issuccess)(bool * issuccess)

Dies ist falsch für eine Navigation, die auf einer Fehlerseite endete (Fehler aufgrund fehlender Netzwerk-, DNS-Suchfehler, http-Server antwortet mit 4xx), kann aber auch falsch sein, wenn zusätzliche Elemente wie Window. Stop () auf navigierten Seite aufgerufen werden.

#### get_WebErrorStatus 

Der Fehlercode, wenn die Navigation fehlgeschlagen ist.

> öffentliche HRESULT- [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS * WEBVIEW2_WEB_ERROR_STATUS)

