---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 34ffa5fe0eabfe8e822db2792d2b25ab5106442a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012057"
---
# Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[ButtonChangeKind](#buttonchangekind) | Die ButtonChangeKind des Zeiger Ereignisses.
[DisplayRect](#displayrect) | Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).
[Frame-Nr](#frameid) | Die Frame-Nr des Pointer-Ereignisses.
[HimetricLocation](#himetriclocation) | Die HimetricLocation des Zeiger Ereignisses.
[HimetricLocationRaw](#himetriclocationraw) | Die HimetricLocationRaw des Zeiger Ereignisses.
[HistoryCount](#historycount) | Die HistoryCount des Zeiger Ereignisses.
[InputData](#inputdata) | Die inputData des Zeiger Ereignisses.
[KeyStates](#keystates) | Die KeyStates des Pointer-Ereignisses.
[PenFlags](#penflags) | Die PenFlags des Zeiger Ereignisses.
[PenMask](#penmask) | Die PenMask des Zeiger Ereignisses.
[PenPressure](#penpressure) | Die PenPressure des Zeiger Ereignisses.
[PenRotation](#penrotation) | Die PenRotation des Zeiger Ereignisses.
[PenTiltX](#pentiltx) | Die PenTiltX des Zeiger Ereignisses.
[PenTiltY](#pentilty) | Die PenTiltY des Zeiger Ereignisses.
[PerformanceCount](#performancecount) | Die PerformanceCount des Zeiger Ereignisses.
[PixelLocation](#pixellocation) | Die PixelLocation des Zeiger Ereignisses.
[PixelLocationRaw](#pixellocationraw) | Die PixelLocationRaw des Zeiger Ereignisses.
[PointerDeviceRect](#pointerdevicerect) | Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).
[PointerFlags](#pointerflags) | Die PointerFlags des Zeiger Ereignisses.
[Zeiger-Nr](#pointerid) | Die Zeiger-Nr des Zeiger Ereignisses.
[PointerKind](#pointerkind) | Die PointerKind des Zeiger Ereignisses.
[Zeit](#time) | Die Uhrzeit des Zeiger Ereignisses.
[TouchContact](#touchcontact) | Die TouchContact des Zeiger Ereignisses.
[TouchContactRaw](#touchcontactraw) | Die TouchContactRaw des Zeiger Ereignisses.
[TouchFlags](#touchflags) | Die TouchFlags des Zeiger Ereignisses.
[TouchMask](#touchmask) | Die TouchMask des Zeiger Ereignisses.
[TouchOrientation](#touchorientation) | Die TouchOrientation des Zeiger Ereignisses.
[TouchPressure](#touchpressure) | Die TouchPressure des Zeiger Ereignisses.

## Member

#### ButtonChangeKind 

Die ButtonChangeKind des Zeiger Ereignisses.

> public int [ButtonChangeKind](#buttonchangekind)

Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.

#### DisplayRect 

Die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

> öffentliches Rechteck [DisplayRect](#displayrect)

#### Frame-Nr 

Die Frame-Nr des Pointer-Ereignisses.

> öffentliche uint- [Frame](#frameid) -Nr

Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).

#### HimetricLocation 

Die HimetricLocation des Zeiger Ereignisses.

> öffentlicher Punkt [HimetricLocation](#himetriclocation)

Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### HimetricLocationRaw 

Die HimetricLocationRaw des Zeiger Ereignisses.

> öffentlicher Punkt [HimetricLocationRaw](#himetriclocationraw)

Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### HistoryCount 

Die HistoryCount des Zeiger Ereignisses.

> public uint [HistoryCount](#historycount)

Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### InputData 

Die inputData des Zeiger Ereignisses.

> public int [inputData](#inputdata)

Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### KeyStates 

Die KeyStates des Pointer-Ereignisses.

> öffentliche uint- [KeyStates](#keystates)

Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PenFlags 

Die PenFlags des Zeiger Ereignisses.

> public uint [PenFlags](#penflags)

Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur. Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### PenMask 

Die PenMask des Zeiger Ereignisses.

> public uint [PenMask](#penmask)

Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur. Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.

#### PenPressure 

Die PenPressure des Zeiger Ereignisses.

> public uint [PenPressure](#penpressure)

Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PenRotation 

Die PenRotation des Zeiger Ereignisses.

> public uint [PenRotation](#penrotation)

Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PenTiltX 

Die PenTiltX des Zeiger Ereignisses.

> public int [PenTiltX](#pentiltx)

Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PenTiltY 

Die PenTiltY des Zeiger Ereignisses.

> public int [PenTiltY](#pentilty)

Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PerformanceCount 

Die PerformanceCount des Zeiger Ereignisses.

> Public ULONG [PerformanceCount](#performancecount)

Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PixelLocation 

Die PixelLocation des Zeiger Ereignisses.

> öffentlicher Punkt [PixelLocation](#pixellocation)

Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PixelLocationRaw 

Die PixelLocationRaw des Zeiger Ereignisses.

> öffentlicher Punkt [PixelLocationRaw](#pixellocationraw)

Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PointerDeviceRect 

Die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

> öffentliches Rechteck [PointerDeviceRect](#pointerdevicerect)

#### PointerFlags 

Die PointerFlags des Zeiger Ereignisses.

> public uint [PointerFlags](#pointerflags)

Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### Zeiger-Nr 

Die Zeiger-Nr des Zeiger Ereignisses.

> öffentliche uint- [Zeiger](#pointerid) -Nr

Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).

#### PointerKind 

Die PointerKind des Zeiger Ereignisses.

> public uint [PointerKind](#pointerkind)

Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert. Unterstützt PT_PEN und PT_TOUCH.

#### Zeit 

Die Uhrzeit des Zeiger Ereignisses.

> öffentliche uint- [Zeit](#time)

Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### TouchContact 

Die TouchContact des Zeiger Ereignisses.

> öffentliches Rechteck [TouchContact](#touchcontact)

Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### TouchContactRaw 

Die TouchContactRaw des Zeiger Ereignisses.

> öffentliches Rechteck [TouchContactRaw](#touchcontactraw)

Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### TouchFlags 

Die TouchFlags des Zeiger Ereignisses.

> public uint [TouchFlags](#touchflags)

Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur. Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### TouchMask 

Die TouchMask des Zeiger Ereignisses.

> public uint [TouchMask](#touchmask)

Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur. Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.

#### TouchOrientation 

Die TouchOrientation des Zeiger Ereignisses.

> public uint [TouchOrientation](#touchorientation)

Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### TouchPressure 

Die TouchPressure des Zeiger Ereignisses.

> public uint [TouchPressure](#touchpressure)

Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

