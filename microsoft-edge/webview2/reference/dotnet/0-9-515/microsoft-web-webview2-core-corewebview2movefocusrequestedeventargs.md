---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 1d3cae59c0906a94414ff135ef8d84fac7cc89b4
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885072"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs Klasse 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Ereignis-args für das MoveFocusRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Handled](#handled) | Geben Sie an, ob das Ereignis von der APP behandelt wurde.
[Grund](#reason) | Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.

## Member

#### Handled 

Geben Sie an, ob das Ereignis von der APP behandelt wurde.

> öffentliche bool- [Behandlung](#handled)

Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen. Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt. Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben. Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.

#### Grund 

Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.

> [Grund](#reason) für öffentliche CoreWebView2MoveFocusReason

