---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: dbcc5b10ce1973df61554f3f27174f600fb25280
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885981"
---
# 0.8.355-Interface-IWebView2HttpHeadersCollectionIterator 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Iterator für eine Sammlung von HTTP-Headern.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.
[MoveNext](#movenext) | Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.

Siehe [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) und [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).

## Member

#### GetCurrentHeader 

Rufen Sie den Namen und den Wert des aktuellen HTTP-Headers des Iterators ab.

> Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * Name, LPWSTR *-Wert)

Diese Methode schlägt fehl, wenn der letzte Aufruf von MoveNext has_next auf "false" festgelegt hat.

#### MoveNext 

Verschieben Sie den Iterator in den nächsten HTTP-Header in der Sammlung.

> Public HRESULT [MoveNext](#movenext)(bool * has_next)

Der has_next-Parameter wird auf "false" festgelegt, wenn keine weiteren HTTP-Header vorhanden sind. Nachdem dies erfolgt ist, schlägt die GetCurrentHeader-Methode fehl, wenn Sie aufgerufen wird.

