---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: eda4d00db8e8c52f9ce0b6511acb3d89b497fb1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878736"
---
# Schnittstellen ICoreWebView2MoveFocusRequestedEventArgs 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Ereignis-args für das MoveFocusRequested-Ereignis.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Geben Sie an, ob das Ereignis von der APP behandelt wurde.
[get_Reason](#get_reason) | Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.
[put_Handled](#put_handled) | Festlegen der Handled-Eigenschaft

## Member

#### get_Handled 

Geben Sie an, ob das Ereignis von der APP behandelt wurde.

> Public HRESULT [get_Handled](#get_handled)(bool * value)

Wenn die APP den Fokus an die gewünschte Position verschoben hat, sollte Sie die Handled-Eigenschaft auf true festlegen. Wenn Handled-Eigenschaft auf false festgelegt ist, nachdem der Ereignishandler zurückgegeben wurde, wird Standardaktion ausgeführt. Die Standardaktion besteht darin, das nächste Tabstopp-untergeordnete Fenster in der APP zu finden und zu versuchen, den Fokus auf dieses Fenster zu verschieben. Wenn kein anderes Fenster zum Verschieben des Fokus vorhanden ist, wird der Fokus innerhalb des Webinhalts der WebView-Webinhalte durchlaufen.

#### get_Reason 

Der Grund, warum WebView das angeforderte MoveFocus-Ereignis ausgelöst hat.

> Public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON *-Wert)

#### put_Handled 

Festlegen der Handled-Eigenschaft

> Public HRESULT [put_Handled](#put_handled)(bool-Wert)

