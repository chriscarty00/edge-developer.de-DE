---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 77cf5ffce5eb6fbb6d310968c998a3f65c08b11a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884218"
---
# 0.9.430-Interface-ICoreWebView2DocumentTitleChangedEventHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

Der Aufrufer implementiert diese Schnittstelle zum Empfangen von DocumentTitleChanged-Ereignissen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

Verwenden Sie die DocumentTitle-Eigenschaft, um den geänderten Titel abzurufen.

## Member

#### Invoke 

Wird aufgerufen, um dem Implementierer die Ereignis args für das entsprechende Ereignis bereitzustellen.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) * Sender; IUnknown * args)

Es gibt keine Ereignisargumente, und der args-Parameter ist NULL.

