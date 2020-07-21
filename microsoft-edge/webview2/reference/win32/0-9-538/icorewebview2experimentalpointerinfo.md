---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML, ICoreWebView2ExperimentalPointerInfo
ms.openlocfilehash: 6a5727fbcae24f7fd65c6c4a7a49b1a0b4746eb3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883717"
---
# Schnittstellen ICoreWebView2ExperimentalPointerInfo 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_ButtonChangeKind](#get_buttonchangekind) | Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.
[get_DisplayRect](#get_displayrect) | Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.
[get_FrameId](#get_frameid) | Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.
[get_HimetricLocation](#get_himetriclocation) | Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.
[get_HimetricLocationRaw](#get_himetriclocationraw) | Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.
[get_HistoryCount](#get_historycount) | Rufen Sie die HistoryCount des Pointer-Ereignisses ab.
[get_InputData](#get_inputdata) | Rufen Sie die inputData des Pointer-Ereignisses ab.
[get_KeyStates](#get_keystates) | Rufen Sie die KeyStates des Pointer-Ereignisses ab.
[get_PenFlags](#get_penflags) | Rufen Sie die PenFlags des Pointer-Ereignisses ab.
[get_PenMask](#get_penmask) | Rufen Sie die PenMask des Pointer-Ereignisses ab.
[get_PenPressure](#get_penpressure) | Rufen Sie die PenPressure des Pointer-Ereignisses ab.
[get_PenRotation](#get_penrotation) | Rufen Sie die PenRotation des Pointer-Ereignisses ab.
[get_PenTiltX](#get_pentiltx) | Rufen Sie die PenTiltX des Pointer-Ereignisses ab.
[get_PenTiltY](#get_pentilty) | Rufen Sie die PenTiltY des Pointer-Ereignisses ab.
[get_PerformanceCount](#get_performancecount) | Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.
[get_PixelLocation](#get_pixellocation) | Rufen Sie die PixelLocation des Pointer-Ereignisses ab.
[get_PixelLocationRaw](#get_pixellocationraw) | Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.
[get_PointerDeviceRect](#get_pointerdevicerect) | Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.
[get_PointerFlags](#get_pointerflags) | Rufen Sie die PointerFlags des Pointer-Ereignisses ab.
[get_PointerId](#get_pointerid) | Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.
[get_PointerKind](#get_pointerkind) | Rufen Sie die PointerKind des Pointer-Ereignisses ab.
[get_Time](#get_time) | Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.
[get_TouchContact](#get_touchcontact) | Rufen Sie die TouchContact des Pointer-Ereignisses ab.
[get_TouchContactRaw](#get_touchcontactraw) | Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.
[get_TouchFlags](#get_touchflags) | Rufen Sie die TouchFlags des Pointer-Ereignisses ab.
[get_TouchMask](#get_touchmask) | Rufen Sie die TouchMask des Pointer-Ereignisses ab.
[get_TouchOrientation](#get_touchorientation) | Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.
[get_TouchPressure](#get_touchpressure) | Rufen Sie die TouchPressure des Pointer-Ereignisses ab.
[put_ButtonChangeKind](#put_buttonchangekind) | Legt die ButtonChangeKind des Zeiger Ereignisses fest.
[put_DisplayRect](#put_displayrect) | Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).
[put_FrameId](#put_frameid) | Legt die Frame-Nr des Zeiger Ereignisses fest.
[put_HimetricLocation](#put_himetriclocation) | Legt die HimetricLocation des Zeiger Ereignisses fest.
[put_HimetricLocationRaw](#put_himetriclocationraw) | Legt die HimetricLocationRaw des Zeiger Ereignisses fest.
[put_HistoryCount](#put_historycount) | Legt die HistoryCount des Zeiger Ereignisses fest.
[put_InputData](#put_inputdata) | Legt die inputData des Zeiger Ereignisses fest.
[put_KeyStates](#put_keystates) | Die KeyStates des Pointer-Ereignisses festzulegen.
[put_PenFlags](#put_penflags) | Legt die PenFlags des Zeiger Ereignisses fest.
[put_PenMask](#put_penmask) | Legt die PenMask des Zeiger Ereignisses fest.
[put_PenPressure](#put_penpressure) | Legt die PenPressure des Zeiger Ereignisses fest.
[put_PenRotation](#put_penrotation) | Legt die PenRotation des Zeiger Ereignisses fest.
[put_PenTiltX](#put_pentiltx) | Legt die PenTiltX des Zeiger Ereignisses fest.
[put_PenTiltY](#put_pentilty) | Legt die PenTiltY des Zeiger Ereignisses fest.
[put_PerformanceCount](#put_performancecount) | Legt die PerformanceCount des Zeiger Ereignisses fest.
[put_PixelLocation](#put_pixellocation) | Legt die PixelLocation des Zeiger Ereignisses fest.
[put_PixelLocationRaw](#put_pixellocationraw) | Legt die PixelLocationRaw des Zeiger Ereignisses fest.
[put_PointerDeviceRect](#put_pointerdevicerect) | Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).
[put_PointerFlags](#put_pointerflags) | Legt die PointerFlags des Zeiger Ereignisses fest.
[put_PointerId](#put_pointerid) | Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.
[put_PointerKind](#put_pointerkind) | Legt die PointerKind des Zeiger Ereignisses fest.
[put_Time](#put_time) | Legt die Uhrzeit des Zeiger Ereignisses fest.
[put_TouchContact](#put_touchcontact) | Legt die TouchContact des Zeiger Ereignisses fest.
[put_TouchContactRaw](#put_touchcontactraw) | Legt die TouchContactRaw des Zeiger Ereignisses fest.
[put_TouchFlags](#put_touchflags) | Legt die TouchFlags des Zeiger Ereignisses fest.
[put_TouchMask](#put_touchmask) | Legt die TouchMask des Zeiger Ereignisses fest.
[put_TouchOrientation](#put_touchorientation) | Legt die TouchOrientation des Zeiger Ereignisses fest.
[put_TouchPressure](#put_touchpressure) | Legt die TouchPressure des Zeiger Ereignisses fest.

Sie nimmt Felder aus allen dreien auf und schließt einige Win32-spezifische Datentypen wie HWND und handle aus. Beachten Sie, dass sourceDevice herausgenommen wird, aber wir erwarten, dass PointerDeviceRect und DisplayRect die vorhandenen Anwendungsfälle von sourceDevice abdecken. Ein weiterer großer Unterschied besteht darin, dass eine der Punkt-oder Rect-Positionen in WebView-physikalischen Koordinaten erwartet wird. Das heißt, Koordinaten relativ zum WebView und keine DPI-Skalierung angewendet.

## Member

#### get_ButtonChangeKind 

Rufen Sie die ButtonChangeKind des Pointer-Ereignisses ab.

> Public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 * ButtonChangeKind)

Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.

#### get_DisplayRect 

Rufen Sie die DisplayRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.

> Public HRESULT [get_DisplayRect](#get_displayrect)(Rect * DisplayRect)

#### get_FrameId 

Rufen Sie die Frame-Nr des Pointer-Ereignisses ab.

> Public HRESULT [get_FrameId](#get_frameid)(UInt32 * Frame-Nr)

Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_HimetricLocation 

Rufen Sie die HimetricLocation des Pointer-Ereignisses ab.

> öffentliche HRESULT- [get_HimetricLocation](#get_himetriclocation)(Point * HimetricLocation)

Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_HimetricLocationRaw 

Rufen Sie die HimetricLocationRaw des Pointer-Ereignisses ab.

> öffentliche HRESULT- [get_HimetricLocationRaw](#get_himetriclocationraw)(Point * HimetricLocationRaw)

Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_HistoryCount 

Rufen Sie die HistoryCount des Pointer-Ereignisses ab.

> Public HRESULT [get_HistoryCount](#get_historycount)(UInt32 * HistoryCount)

Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_InputData 

Rufen Sie die inputData des Pointer-Ereignisses ab.

> Public HRESULT [get_InputData](#get_inputdata)(Int32 * inputData)

Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_KeyStates 

Rufen Sie die KeyStates des Pointer-Ereignisses ab.

> öffentliche HRESULT- [get_KeyStates](#get_keystates)(DWORD *-KeyStates)

Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PenFlags 

Rufen Sie die PenFlags des Pointer-Ereignisses ab.

> Public HRESULT [get_PenFlags](#get_penflags)(UInt32 * PenFlags)

Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur. Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### get_PenMask 

Rufen Sie die PenMask des Pointer-Ereignisses ab.

> Public HRESULT [get_PenMask](#get_penmask)(UInt32 * PenMask)

Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur. Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.

#### get_PenPressure 

Rufen Sie die PenPressure des Pointer-Ereignisses ab.

> Public HRESULT [get_PenPressure](#get_penpressure)(UInt32 * PenPressure)

Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PenRotation 

Rufen Sie die PenRotation des Pointer-Ereignisses ab.

> Public HRESULT [get_PenRotation](#get_penrotation)(UInt32 * PenRotation)

Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PenTiltX 

Rufen Sie die PenTiltX des Pointer-Ereignisses ab.

> Public HRESULT [get_PenTiltX](#get_pentiltx)(Int32 * PenTiltX)

Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PenTiltY 

Rufen Sie die PenTiltY des Pointer-Ereignisses ab.

> Public HRESULT [get_PenTiltY](#get_pentilty)(Int32 * PenTiltY)

Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PerformanceCount 

Rufen Sie die PerformanceCount des Pointer-Ereignisses ab.

> Public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 * PerformanceCount)

Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PixelLocation 

Rufen Sie die PixelLocation des Pointer-Ereignisses ab.

> öffentliche HRESULT- [get_PixelLocation](#get_pixellocation)(Point * PixelLocation)

Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PixelLocationRaw 

Rufen Sie die PixelLocationRaw des Pointer-Ereignisses ab.

> öffentliche HRESULT- [get_PixelLocationRaw](#get_pixellocationraw)(Point * PixelLocationRaw)

Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PointerDeviceRect 

Rufen Sie die PointerDeviceRect-Eigenschaft der sourceDevice-Eigenschaft der POINTER_INFO-Struktur ab, wie im Windows SDK (Winuser. h) definiert.

> Public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect * PointerDeviceRect)

#### get_PointerFlags 

Rufen Sie die PointerFlags des Pointer-Ereignisses ab.

> Public HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 * PointerFlags)

Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### get_PointerId 

Rufen Sie die Zeiger-Nr. des Pointer-Ereignisses ab.

> öffentliche HRESULT- [get_PointerId](#get_pointerid)(UInt32 * Pointer-Nr.)

Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_PointerKind 

Rufen Sie die PointerKind des Pointer-Ereignisses ab.

> Public HRESULT [get_PointerKind](#get_pointerkind)(DWORD * PointerKind)

Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert. Unterstützt PT_PEN und PT_TOUCH.

#### get_Time 

Rufen Sie die Uhrzeit des Zeiger Ereignisses ab.

> öffentliche HRESULT- [get_Time](#get_time)(DWORD * Zeit)

Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_TouchContact 

Rufen Sie die TouchContact des Pointer-Ereignisses ab.

> Public HRESULT [get_TouchContact](#get_touchcontact)(Rect * TouchContact)

Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_TouchContactRaw 

Rufen Sie die TouchContactRaw des Pointer-Ereignisses ab.

> Public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect * TouchContactRaw)

Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_TouchFlags 

Rufen Sie die TouchFlags des Pointer-Ereignisses ab.

> Public HRESULT [get_TouchFlags](#get_touchflags)(UInt32 * TouchFlags)

Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur. Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### get_TouchMask 

Rufen Sie die TouchMask des Pointer-Ereignisses ab.

> Public HRESULT [get_TouchMask](#get_touchmask)(UInt32 * TouchMask)

Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur. Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.

#### get_TouchOrientation 

Rufen Sie die TouchOrientation des Pointer-Ereignisses ab.

> Public HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 * TouchOrientation)

Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### get_TouchPressure 

Rufen Sie die TouchPressure des Pointer-Ereignisses ab.

> Public HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 * TouchPressure)

Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_ButtonChangeKind 

Legt die ButtonChangeKind des Zeiger Ereignisses fest.

> Public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)

Dies entspricht der ButtonChangeKind-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_BUTTON_CHANGE_KIND Enum im Windows SDK (Winuser. h) definiert.

#### put_DisplayRect 

Setzen Sie die DisplayRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).

> Public HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)

#### put_FrameId 

Legt die Frame-Nr des Zeiger Ereignisses fest.

> Public HRESULT [put_FrameId](#put_frameid)(UInt32-Frame-Nr)

Dies entspricht der Frame-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_HimetricLocation 

Legt die HimetricLocation des Zeiger Ereignisses fest.

> öffentliche HRESULT- [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)

Dies entspricht der ptHimetricLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_HimetricLocationRaw 

Legt die HimetricLocationRaw des Zeiger Ereignisses fest.

> öffentliche HRESULT- [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)

Dies entspricht der ptHimetricLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_HistoryCount 

Legt die HistoryCount des Zeiger Ereignisses fest.

> Public HRESULT [put_HistoryCount](#put_historycount)(UInt32 HistoryCount)

Dies entspricht der historyCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_InputData 

Legt die inputData des Zeiger Ereignisses fest.

> Public HRESULT [put_InputData](#put_inputdata)(Int32 inputData)

Dies entspricht der inputData-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_KeyStates 

Die KeyStates des Pointer-Ereignisses festzulegen.

> Public HRESULT [put_KeyStates](#put_keystates)(DWORD-KeyStates)

Dies entspricht der dwKeyStates-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PenFlags 

Legt die PenFlags des Zeiger Ereignisses fest.

> Public HRESULT [put_PenFlags](#put_penflags)(UInt32 PenFlags)

Dies entspricht der penFlags-Eigenschaft der POINTER_PEN_INFO-Struktur. Die Werte werden durch die PEN_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### put_PenMask 

Legt die PenMask des Zeiger Ereignisses fest.

> Public HRESULT [put_PenMask](#put_penmask)(UInt32 PenMask)

Dies entspricht der penMask-Eigenschaft der POINTER_PEN_INFO-Struktur. Die Werte werden durch die PEN_MASK Konstanten im Windows SDK (Winuser. h) definiert.

#### put_PenPressure 

Legt die PenPressure des Zeiger Ereignisses fest.

> Public HRESULT [put_PenPressure](#put_penpressure)(UInt32 PenPressure)

Dies entspricht der Pressure-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PenRotation 

Legt die PenRotation des Zeiger Ereignisses fest.

> Public HRESULT [put_PenRotation](#put_penrotation)(UInt32 PenRotation)

Dies entspricht der Rotation-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PenTiltX 

Legt die PenTiltX des Zeiger Ereignisses fest.

> Public HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)

Dies entspricht der tiltX-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PenTiltY 

Legt die PenTiltY des Zeiger Ereignisses fest.

> Public HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)

Dies entspricht der TiltY-Eigenschaft der POINTER_PEN_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PerformanceCount 

Legt die PerformanceCount des Zeiger Ereignisses fest.

> Public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)

Dies entspricht der PerformanceCount-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PixelLocation 

Legt die PixelLocation des Zeiger Ereignisses fest.

> öffentliche HRESULT- [put_PixelLocation](#put_pixellocation)(Point PixelLocation)

Dies entspricht der ptPixelLocation-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PixelLocationRaw 

Legt die PixelLocationRaw des Zeiger Ereignisses fest.

> öffentliche HRESULT- [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)

Dies entspricht der ptPixelLocationRaw-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PointerDeviceRect 

Setzen Sie die PointerDeviceRect der sourceDevice-Eigenschaft der POINTER_INFO-Struktur entsprechend der Definition im Windows SDK (Winuser. h).

> Public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)

#### put_PointerFlags 

Legt die PointerFlags des Zeiger Ereignisses fest.

> Public HRESULT [put_PointerFlags](#put_pointerflags)(UInt32 PointerFlags)

Dies entspricht der pointerFlags-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### put_PointerId 

Die Zeiger-Nr. des Pointer-Ereignisses festzulegen.

> Public HRESULT [put_PointerId](#put_pointerid)(UInt32-Zeiger-Nr.)

Dies entspricht der Pointer-Eigenschaft der POINTER_INFO Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_PointerKind 

Legt die PointerKind des Zeiger Ereignisses fest.

> Public HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)

Dies entspricht der pointerKind-Eigenschaft der POINTER_INFO-Struktur. Die Werte werden durch die POINTER_INPUT_KIND Enum im Windows SDK (Winuser. h) definiert. Unterstützt PT_PEN und PT_TOUCH.

#### put_Time 

Legt die Uhrzeit des Zeiger Ereignisses fest.

> Public HRESULT [put_Time](#put_time)(DWORD-Zeit)

Dies entspricht der dwTime-Eigenschaft der POINTER_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_TouchContact 

Legt die TouchContact des Zeiger Ereignisses fest.

> Public HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)

Dies entspricht der rcContact-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_TouchContactRaw 

Legt die TouchContactRaw des Zeiger Ereignisses fest.

> Public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)

Dies entspricht der rcContactRaw-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_TouchFlags 

Legt die TouchFlags des Zeiger Ereignisses fest.

> Public HRESULT [put_TouchFlags](#put_touchflags)(UInt32 TouchFlags)

Dies entspricht der touchFlags-Eigenschaft der POINTER_TOUCH_INFO-Struktur. Die Werte werden durch die TOUCH_FLAGS Konstanten im Windows SDK (Winuser. h) definiert.

#### put_TouchMask 

Legt die TouchMask des Zeiger Ereignisses fest.

> Public HRESULT [put_TouchMask](#put_touchmask)(UInt32 TouchMask)

Dies entspricht der touchMask-Eigenschaft der POINTER_TOUCH_INFO-Struktur. Die Werte werden durch die TOUCH_MASK Konstanten im Windows SDK (Winuser. h) definiert.

#### put_TouchOrientation 

Legt die TouchOrientation des Zeiger Ereignisses fest.

> Public HRESULT [put_TouchOrientation](#put_touchorientation)(UInt32 TouchOrientation)

Dies entspricht der Orientation-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

#### put_TouchPressure 

Legt die TouchPressure des Zeiger Ereignisses fest.

> Public HRESULT [put_TouchPressure](#put_touchpressure)(UInt32 TouchPressure)

Dies entspricht der Pressure-Eigenschaft der POINTER_TOUCH_INFO-Struktur gemäß Definition im Windows SDK (Winuser. h).

