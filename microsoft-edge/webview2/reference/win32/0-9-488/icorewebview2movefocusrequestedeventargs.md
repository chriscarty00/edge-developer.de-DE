---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 8ca8de3c430eda3bde089ca53501d880f4d8e35e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653935"
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

