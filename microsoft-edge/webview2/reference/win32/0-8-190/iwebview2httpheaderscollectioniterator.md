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
ms.openlocfilehash: 4b9ad48d9b09343bad04d4acbe7c49750e76427d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654071"
---
# Schnittstellen IWebView2HttpHeadersCollectionIterator 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.8.355 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

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

