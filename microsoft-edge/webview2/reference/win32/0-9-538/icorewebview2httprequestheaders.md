---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 903355ff04463ad86f1e25771f5f321f7d0df479
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879163"
---
# Schnittstellen ICoreWebView2HttpRequestHeaders 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

HTTP-Anforderungsheader.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Contains](#contains) | Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.
[GetHeader](#getheader) | Ruft den Headerwert ab, der dem Namen entspricht.
[GetHeaders](#getheaders) | Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.
[GetIterator](#getiterator) | Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.
[RemoveHeader](#removeheader) | Entfernt den Header, der dem Namen entspricht.
[SetHeader](#setheader) | Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.

Wird verwendet, um die HTTP-Anforderung für das WebResourceRequested-Ereignis und das NavigationStarting-Ereignis zu überprüfen. Beachten Sie, dass Sie die HTTP-Anforderungs Kopfzeilen aus einem WebResourceRequested-Ereignis, aber nicht aus einem NavigationStarting-Ereignis ändern können.

## Member

#### Contains 

Überprüft, ob die Kopfzeilen einen Eintrag enthalten, der dem Headernamen entspricht.

> Public HRESULT [Contains](#contains)(LPCWSTR Name, bool * Contains)

#### GetHeader 

Ruft den Headerwert ab, der dem Namen entspricht.

> Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR *-Wert)

#### GetHeaders 

Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.

> öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *-Iterator)

#### GetIterator 

Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.

> öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *-Iterator)

#### RemoveHeader 

Entfernt den Header, der dem Namen entspricht.

> Public HRESULT [RemoveHeader](#removeheader)(LPCWSTR Name)

#### SetHeader 

Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.

> Public HRESULT [setHeader](#setheader)(LPCWSTR-Name, LPCWSTR-Wert)

