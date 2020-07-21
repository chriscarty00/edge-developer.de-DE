---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2ed75f2a12387b6b8de628ac27ef536cf43fb8b1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885408"
---
# 0.9.515-Interface-ICoreWebView2DevToolsProtocolEventReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_ParameterObjectAsJson](#get_parameterobjectasjson) | Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.

## Member

#### get_ParameterObjectAsJson 

Das Parameter Objekt des entsprechenden DevToolsProtocol-Ereignisses, das als JSON-Zeichenfolge dargestellt wird.

> Public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR * ParameterObjectAsJson)

