---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 4866626111908eae9800da0baabec0356d5d4bf8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879653"
---
# Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures Klasse 

> [!NOTE]
> Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

