---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: e12809d1db7e8c7764ad75e9a10f44ac3f445fa4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653865"
---
# Schnittstellen ICoreWebView2HttpRequestHeaders 

> [!NOTE]
> Diese Schnittstelle kann nach der SDK-Version 0.9.430 geändert oder für Versionen nicht verfügbar sein. Die neueste API-Referenz finden Sie unter [Referenz](../../../webview2-api-reference.md) .

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

HTTP-Anforderungsheader.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[GetHeader](#getheader) | Ruft den Headerwert ab, der dem Namen entspricht.
[GetHeaders](#getheaders) | Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.
[Contains](#contains) | Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.
[SetHeader](#setheader) | Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.
[RemoveHeader](#removeheader) | Entfernt den Header, der dem Namen entspricht.
[GetIterator](#getiterator) | Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.

Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen. Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.

## Member

#### GetHeader 

Ruft den Headerwert ab, der dem Namen entspricht.

> Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR *-Wert)

#### GetHeaders 

Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.

> öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * *-Iterator)

#### Contains 

Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.

> Public HRESULT [Contains](#contains)(LPCWSTR Name, bool * Contains)

#### SetHeader 

Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.

> Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)

#### RemoveHeader 

Entfernt den Header, der dem Namen entspricht.

> Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)

#### GetIterator 

Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.

> öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * *-Iterator)

