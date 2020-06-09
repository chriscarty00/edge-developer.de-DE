---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 576f54f2a7ecc2e1e99758719e80cc589c5bc791
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698935"
---
# Schnittstellen ICoreWebView2ExperimentalWindowFeatures 

> [!NOTE]
> Dies ist eine experimentelle API, die mit unserer Vorabversion SDK-Version 0.9.538 ausgeliefert wird.

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

Fenster Features für ein WebView-Popupfenster

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_Height](#get_height) | Die Höhe des Fensters.
[get_Left](#get_left) | Die linke Position des Fensters. Schlägt fehl, wenn HasPosition falsch ist.
[get_MenuBar](#get_menubar) | Gibt an, ob die Menüleiste angezeigt werden soll.
[get_ScrollBars](#get_scrollbars) | Gibt an, ob Bildlaufleisten angezeigt werden sollen.
[get_Status](#get_status) | Gibt an, ob eine Statusleiste hinzugefügt werden soll.
[get_Toolbar](#get_toolbar) | Gibt an, ob die Browsersymbolleiste angezeigt werden soll.
[get_Top](#get_top) | Die obere Position des Fensters. Schlägt fehl, wenn HasPosition falsch ist.
[get_Width](#get_width) | Die Breite des Fensters.
[HasPosition](#hasposition) | Hat den Wert für left und Top angegeben.
[HasSize](#hassize) | Hat die angegebenen Werte für Höhe und Breite.

Diese Felder entsprechen dem "windowFeatures", das an Window. Open übergeben wurde, wie in[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)

## Member

#### get_Height 

Die Höhe des Fensters.

> öffentliche HRESULT- [get_Height](#get_height)(UInt32 * Height)

Der Mindestwert ist 100. Schlägt fehl, wenn HasSize falsch ist.

#### get_Left 

Die linke Position des Fensters. Schlägt fehl, wenn HasPosition falsch ist.

> öffentliche HRESULT- [get_Left](#get_left)(UInt32 * Left)

#### get_MenuBar 

Gibt an, ob die Menüleiste angezeigt werden soll.

> öffentliche HRESULT- [get_MenuBar](#get_menubar)(bool * Menüleiste)

#### get_ScrollBars 

Gibt an, ob Bildlaufleisten angezeigt werden sollen.

> öffentliche HRESULT- [get_ScrollBars](#get_scrollbars)(bool * ScrollBars)

#### get_Status 

Gibt an, ob eine Statusleiste hinzugefügt werden soll.

> Public HRESULT [get_Status](#get_status)(bool * Status)

#### get_Toolbar 

Gibt an, ob die Browsersymbolleiste angezeigt werden soll.

> öffentliche HRESULT- [get_Toolbar](#get_toolbar)(bool * Toolbar)

#### get_Top 

Die obere Position des Fensters. Schlägt fehl, wenn HasPosition falsch ist.

> Public HRESULT [get_Top](#get_top)(UInt32 * Top)

#### get_Width 

Die Breite des Fensters.

> öffentliche HRESULT- [get_Width](#get_width)(UInt32 * Width)

Der Mindestwert ist 100. Schlägt fehl, wenn HasSize falsch ist.

#### HasPosition 

Hat den Wert für left und Top angegeben.

> Public HRESULT [HasPosition](#hasposition)(bool * HasPosition)

#### HasSize 

Hat die angegebenen Werte für Höhe und Breite.

> Public HRESULT [HasSize](#hassize)(bool * HasSize)

