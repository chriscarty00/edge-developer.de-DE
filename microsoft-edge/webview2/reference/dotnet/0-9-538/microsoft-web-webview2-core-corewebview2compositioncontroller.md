---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2CompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2CompositionController
ms.openlocfilehash: 45ac5406cea804aa5b5db748cecaae7104dccb00
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878988"
---
# Microsoft. Web. WebView2. Core. CoreWebView2CompositionController Klasse 

> [!NOTE]
> Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Diese Klasse ist eine Erweiterung der CoreWebView2Controller-Klasse, um das visuelle Hosting zu unterstützen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[Cursor](#cursor) | Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.
[CursorChanged](#cursorchanged) | Das Ereignis wird ausgelöst, wenn WebView glaubt, dass der Cursor geändert werden soll.
[RootVisualTarget](#rootvisualtarget) | Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.
[UIAProvider](#uiaprovider) | Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine CoreWebView2ExperimentalPointerInfo.
[SendMouseInput](#sendmouseinput) | Wenn eventKind CoreWebView2MouseEventKind. HorizontalWheel oder CoreWebView2MouseEventKind. Wheel ist, gibt mouseData den Umfang der Mausradbewegung an.
[SendPointerInput](#sendpointerinput) | SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in CoreWebView2PointerEventKind definiert sind.

## Member

#### Cursor 

Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.

> öffentlicher IntPtr- [Cursor](#cursor)

Der Cursor sollte in WM_SETCURSOR über Mouse. SetCursor festzulegen oder auf das entsprechende übergeordnete/Ancestor-HWND der WebView-über SetClassLongPtr festzulegen. Die HCURSOR kann freigegeben werden, damit CopyCursor/DestroyCursor empfohlen wird, ihre eigene Kopie beizubehalten, wenn Sie mehr als das sofortige Festlegen des Cursors tun.

#### CursorChanged 

Das Ereignis wird ausgelöst, wenn WebView glaubt, dass der Cursor geändert werden soll.

> public event EventHandler<-Objekt > [Cursor](#cursorchanged)

Wenn beispielsweise der Mauszeiger aktuell der Standardcursor ist, aber dann über Text verschoben wird, kann er versuchen, zum IBeam-Cursor zu wechseln.

#### RootVisualTarget 

Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.

> öffentliches Objekt [RootVisualTarget](#rootvisualtarget)

In diesem visuellen Element wird die WebView-Struktur mit der visuellen Struktur verbunden. Die APP verwendet dieses visuelle Element, um die WebView in der APP zu positionieren. Die APP muss weiterhin die Bounds-Eigenschaft verwenden, um die Größe von WebView zu ändern. Die RootVisualTarget-Eigenschaft kann ein IDCompositionVisual oder ein Windows:: UI:: Composition:: ContainerVisual sein. WebView verbindet die visuelle Struktur mit dem bereitgestellten visuellen Element, bevor es vom Eigenschaftensetter zurückgegeben wird. Die APP muss auf Ihrem Gerät einen Commit für die RootVisualTarget-Eigenschaft festlegen. Die RootVisualTarget-Eigenschaft unterstützt die Einstellung auf nullptr, um die WebView aus der visuellen Struktur der APP zu trennen.

#### UIAProvider 

Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.

> öffentliches Objekt [UIAProvider](#uiaprovider)

#### CreateCoreWebView2PointerInfoFromPointerId 

Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine CoreWebView2ExperimentalPointerInfo.

> öffentliche [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) - [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint-Zeiger-Nr., IntPtr-ParentWindow, Matrix4x4-Transformation)

ParentWindow ist das HWND, das die WebView enthält. Dies kann ein beliebiges HWND in der HWND-Struktur sein, das die WebView enthält. Die CoreWebView2Matrix4x4 ist die Transformation aus diesem HWND in die WebView-Ansicht. Der zurückgegebene CoreWebView2ExperimentalPointerInfo wird in SendPointerInfo verwendet. Der Zeigertyp muss entweder Stift oder Fingereingabe sein, oder die Funktion schlägt fehl.

#### SendMouseInput 

Wenn eventKind CoreWebView2MouseEventKind. HorizontalWheel oder CoreWebView2MouseEventKind. Wheel ist, gibt mouseData den Umfang der Mausradbewegung an.

> publicvoid [SendMouseInput](#sendmouseinput)([CoreWebView2MouseEventKind](./namespace-microsoft-web-webview2-core.md) eventKind, [CoreWebView2MouseEventVirtualKeys](./namespace-microsoft-web-webview2-core.md) virtualKeys, uint mouseData, Point Point)

Ein positiver Wert gibt an, dass das Rad nach vorne gedreht wurde, vom Benutzer entfernt; ein negativer Wert gibt an, dass das Rad nach hinten gedreht wurde, in Richtung des Benutzers. Ein Mausrad Klick ist als WHEEL_DELTA definiert, was 120 ist. Wenn eventKind CoreWebView2MouseEventKind. XButtonDoubleClick CoreWebView2MouseEventKind. XButtonDown oder CoreWebView2MouseEventKind. XButtonUp ist, gibt mouseData an, welche X-Schaltflächen gedrückt oder freigegeben wurden. Dieser Wert sollte 1 sein, wenn die erste x-Taste gedrückt/freigegeben wird, und 2, wenn die zweite x-Taste gedrückt/freigegeben wird. Wenn eventKind CoreWebView2MouseEventKind. Leave ist, sollten virtualKeys, mouseData und Point alle NULL sein. Wenn eventKind ein beliebiger anderer Wert ist, sollte mouseData NULL sein. Point wird im Client Koordinatensystem der WebView erwartet. Zum nachvollziehen von Mausereignissen, die in der WebView beginnen und potenziell außerhalb der WebView-und Hostanwendung verschoben werden können, wird der Aufruf von SetCapture und ReleaseCapture empfohlen. Wenn Sie Hover-Popups schließen möchten, empfiehlt es sich auch, WM_MOUSELEAVE Nachrichten zu senden.

#### SendPointerInput 

SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in CoreWebView2PointerEventKind definiert sind.

> publicvoid [SendPointerInput](#sendpointerinput)([CoreWebView2PointerEventKind](./namespace-microsoft-web-webview2-core.md) EventType, [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) pointerInfo)

Alle zeigereingaben aus dem System müssen zuerst in eine CoreWebView2ExperimentalPointerInfo konvertiert werden.

