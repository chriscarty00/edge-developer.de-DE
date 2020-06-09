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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698915"
---
# Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures Klasse 

> [!NOTE]
> Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Fenster Features für ein WebView-Popupfenster

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Höhe](#height) | Die Höhe des Fensters.
[Links](#left) | Die linke Position des Fensters.
[Menubar](#menubar) | Gibt an, ob die Menüleiste angezeigt werden soll.
[ScrollBars](#scrollbars) | Gibt an, ob Bildlaufleisten angezeigt werden sollen.
[Status](#status) | Gibt an, ob eine Statusleiste hinzugefügt werden soll.
[Symbolleiste](#toolbar) | Gibt an, ob die Browsersymbolleiste angezeigt werden soll.
[Oben](#top) | Die obere Position des Fensters.
[Breite](#width) | Die Breite des Fensters.
[HasPosition](#hasposition) | Hat den Wert für left und Top angegeben.
[HasSize](#hassize) | Hat die angegebenen Werte für Höhe und Breite.

## Member

#### Höhe 

Die Höhe des Fensters.

> öffentliche uint- [Höhe](#height)

#### Links 

Die linke Position des Fensters.

> public uint [Links](#left)

Schlägt fehl, wenn HasPosition falsch ist.

#### Menubar 

Gibt an, ob die Menüleiste angezeigt werden soll.

> öffentliche int- [Menüleiste](#menubar)

#### ScrollBars 

Gibt an, ob Bildlaufleisten angezeigt werden sollen.

> öffentliche int-Bild [Laufleisten](#scrollbars)

#### Status 

Gibt an, ob eine Statusleiste hinzugefügt werden soll.

> öffentlicher int- [Status](#status)

#### Symbolleiste 

Gibt an, ob die Browsersymbolleiste angezeigt werden soll.

> öffentliche int- [Symbolleiste](#toolbar)

#### Oben 

Die obere Position des Fensters.

> public uint [Top](#top)

Schlägt fehl, wenn HasPosition falsch ist.

#### Breite 

Die Breite des Fensters.

> öffentliche uint- [Breite](#width)

#### HasPosition 

Hat den Wert für left und Top angegeben.

> public int [HasPosition](#hasposition)()

#### HasSize 

Hat die angegebenen Werte für Höhe und Breite.

> public int [HasSize](#hassize)()

