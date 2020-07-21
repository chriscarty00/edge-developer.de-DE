---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 077c85b2458c2cf843c4d2f0548d17ec01ba4751
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885961"
---
# 0.8.355-Interface-IWebView2HttpResponseHeaders 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

HTTP-Antwortheader.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Fügt Headerzeile mit Name und Wert an.
[Contains](#contains) | Überprüft, ob die Kopfzeilen Einträge enthalten, die dem Headernamen entsprechen.
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

#### GetHeaders 

Ruft die Überschriften Werte ab, die dem Namen entsprechen.

> öffentliche HRESULT [GetHeaders](#getheaders)(LPCWSTR-Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) * *-Iterator)

#### GetIterator 

Ruft einen Iterator über die Auflistung der gesamten Antwortheader ab.

> öffentlicher HRESULT- [getIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) * *-Iterator)

