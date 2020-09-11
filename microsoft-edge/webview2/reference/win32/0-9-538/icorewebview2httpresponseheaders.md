---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 6278f29f983503916e0015ab4bbac44f79ffe3d9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011307"
---
# 0.9.579-Interface-ICoreWebView2HttpResponseHeaders 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

HTTP-Antwortheader.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Fügt Headerzeile mit Name und Wert an.
[Contains](#contains) | Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.
[GetHeader](#getheader) | Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.
[GetHeaders](#getheaders) | Ruft die Überschriften Werte ab, die dem Namen entsprechen.
[GetIterator](#getiterator) | Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.

Wird zum Erstellen eines WebResourceResponse für das WebResourceRequested-Ereignis verwendet.

## Member

#### AppendHeader 

Fügt Headerzeile mit Name und Wert an.

> Public HRESULT [Appendheader](#appendheader)(LPCWSTR-Name; LPCWSTR-Wert)

#### Contains 

Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.

> Public HRESULT [Contains](#contains)(LPCWSTR Name, bool * Contains)

#### GetHeader 

Ruft den ersten Headerwert in der Sammlung ab, die mit dem Namen übereinstimmt.

> Public HRESULT [GetHeader](#getheader)(LPCWSTR-Name, LPWSTR *-Wert)

#### GetHeaders 

Ruft die Überschriften Werte ab, die dem Namen entsprechen.

> öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *-Iterator)

#### GetIterator 

Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.

> öffentlicher HRESULT- [getIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *-Iterator)

