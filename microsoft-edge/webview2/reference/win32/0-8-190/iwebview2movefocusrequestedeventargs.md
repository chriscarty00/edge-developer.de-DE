---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge
ms.openlocfilehash: 5d8d447bced6bbbb51ae33220e74ebcf47f11ce5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885927"
---
# 0.8.355-Interface-IWebView2MoveFocusRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das MoveFocusRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Reason](#get_reason) | Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.
[get_Handled](#get_handled) | Geben Sie an, ob das Ereignis von der APP behandelt wurde.
[put_Handled](#put_handled) | Festlegen der Handled-Eigenschaft

## Member

#### get_Reason 

Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.

> Public HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON *-Wert)

#### get_Handled 

Geben Sie an, ob das Ereignis von der APP behandelt wurde.

> Public HRESULT [get_Handled](#get_handled)(bool * value)

Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen. Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt. Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben. Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.

#### put_Handled 

Festlegen der Handled-Eigenschaft

> Public HRESULT [put_Handled](#put_handled)(bool-Wert)

