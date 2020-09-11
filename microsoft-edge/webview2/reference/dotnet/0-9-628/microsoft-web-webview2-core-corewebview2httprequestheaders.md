---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012024"
---
# Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

> public bool [Contains](#contains)(Zeichenfolgenname)

#### GetHeader 

Ruft den Headerwert ab, der dem Namen entspricht.

> öffentliche Zeichenfolge [GetHeader](#getheader)(Zeichenfolgenname)

#### GetHeaders 

Ruft den Headerwert ab, der dem Namen über einen Iterator entspricht.

> öffentliche CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(Zeichenfolgenname)

#### GetIterator 

Ruft einen Iterator über der Auflistung von Anforderungsheadern ab.

> Public CoreWebView2HttpHeadersCollectionIterator [getIterator](#getiterator)()

#### RemoveHeader 

Entfernt den Header, der dem Namen entspricht.

> publicvoid [RemoveHeader](#removeheader)(String Name)

#### SetHeader 

Fügt den Header hinzu oder aktualisiert ihn, der dem Namen entspricht.

> publicvoid [setHeader](#setheader)(Zeichenfolgenname, Zeichenfolgenwert)

