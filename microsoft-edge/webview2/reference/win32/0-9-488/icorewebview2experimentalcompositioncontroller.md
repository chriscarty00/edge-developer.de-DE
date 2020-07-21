---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: ddb3fce4f3f9799bcfaf8a9aa297c3207392f916
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884540"
---
# 0.9.515-Interface-ICoreWebView2ExperimentalCompositionController 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

Diese Schnittstelle ist eine Erweiterung der ICoreWebView2Controller-Schnittstelle, um visuelles Hosting zu unterstützen.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[add_CursorChanged](#add_cursorchanged) | Fügen Sie einen Ereignishandler für das Cursor Ereignis hinzu.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).
[get_Cursor](#get_cursor) | Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.
[get_RootVisualTarget](#get_rootvisualtarget) | Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.
[get_UIAProvider](#get_uiaprovider) | Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.
[put_RootVisualTarget](#put_rootvisualtarget) | Festlegen der RootVisualTarget-Eigenschaft
[remove_CursorChanged](#remove_cursorchanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_CursorChanged hinzugefügt wurde.
[SendMouseInput](#sendmouseinput) | Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL oder COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL ist, gibt mouseData den Umfang der Mausradbewegung an.
[SendPointerInput](#sendpointerinput) | SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in COREWEBVIEW2_POINTER_EVENT_KIND definiert sind.
[COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4) | Matrix, die eine 3D-Transformation darstellt.
[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) | Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.
[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) | Virtuelle Mausereignis Tasten, die einem COREWEBVIEW2_MOUSE_EVENT_KIND für SendMouseInput zugeordnet sind.
[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) | Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.

Ein Objekt, das die ICoreWebView2ExperimentalCompositionController-Schnittstelle implementiert, implementiert auch ICoreWebView2Controller. Anrufern wird erwartet, dass Sie ICoreWebView2Controller für die Größenänderung, Sichtbarkeit, Fokus usw. verwenden, und verwenden Sie dann ICoreWebView2ExperimentalCompositionController, um eine Verbindung mit einer Kompositionsstruktur herzustellen und die Eingabe für die WebView bereitzustellen.

## Member

#### add_CursorChanged 

Fügen Sie einen Ereignishandler für das Cursor Ereignis hinzu.

> Public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) * EventHandler, EventRegistrationToken * Token)

Das Ereignis wird ausgelöst, wenn WebView glaubt, dass der Cursor geändert werden soll. Wenn beispielsweise der Mauszeiger aktuell der Standardcursor ist, aber dann über Text verschoben wird, kann er versuchen, zum IBeam-Cursor zu wechseln.

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                       IUnknown* args) -> HRESULT {
                    HCURSOR cursor;
                    CHECK_FAILURE(sender->get_Cursor(&cursor));
                    SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    return S_OK;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### CreateCoreWebView2PointerInfoFromPointerId 

Eine Hilfsfunktion zum Konvertieren einer vom System empfangenen Zeiger-Nr in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).

> öffentliche HRESULT- [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint-Zeiger-Nr., HWND-ParentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

ParentWindow ist das HWND, das die WebView enthält. Dies kann ein beliebiges HWND in der HWND-Struktur sein, das die WebView enthält. Die COREWEBVIEW2_MATRIX_4X4 ist die Transformation aus diesem HWND in die WebView. Der zurückgegebene [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) wird in SendPointerInfo verwendet. Der Zeigertyp muss entweder Stift oder Fingereingabe sein, oder die Funktion schlägt fehl.



#### get_Cursor 

Der aktuelle Cursor, der von WebView als vorgesehen erachtet wird.

> öffentliche HRESULT- [get_Cursor](#get_cursor)(HCURSOR * Cursor)

Der Cursor sollte in WM_SETCURSOR durch:: SetCursor festzulegen oder für das entsprechende übergeordnete/Ancestor-HWND des Webviews über:: SetClassLongPtr festzulegen. Die HCURSOR kann freigegeben werden, damit CopyCursor/DestroyCursor empfohlen wird, ihre eigene Kopie beizubehalten, wenn Sie mehr als das sofortige Festlegen des Cursors tun.

#### get_RootVisualTarget 

Die RootVisualTarget ist ein visuelles Element in der visuellen Struktur der Host-app.

> öffentliche HRESULT- [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown * *-Ziel)

In diesem visuellen Element wird die WebView-Struktur mit der visuellen Struktur verbunden. Die APP verwendet dieses visuelle Element, um die WebView in der APP zu positionieren. Die APP muss weiterhin die Bounds-Eigenschaft verwenden, um die Größe von WebView zu ändern. Die RootVisualTarget-Eigenschaft kann ein IDCompositionVisual oder ein Windows:: UI:: Composition:: ContainerVisual sein. WebView verbindet die visuelle Struktur mit dem bereitgestellten visuellen Element, bevor es vom Eigenschaftensetter zurückgegeben wird. Die APP muss auf Ihrem Gerät einen Commit für die RootVisualTarget-Eigenschaft festlegen. Die RootVisualTarget-Eigenschaft unterstützt die Einstellung auf nullptr, um die WebView aus der visuellen Struktur der APP zu trennen. 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### get_UIAProvider 

Gibt den Benutzeroberflächenautomatisierungs-Anbieter für die WebView zurück.

> öffentliche HRESULT- [get_UIAProvider](#get_uiaprovider)(IUnknown * *-Anbieter)

#### put_RootVisualTarget 

Festlegen der RootVisualTarget-Eigenschaft

> öffentliche HRESULT- [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown *-Ziel)

#### remove_CursorChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_CursorChanged hinzugefügt wurde.

> Public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken-Token)

#### SendMouseInput 

Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL oder COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL ist, gibt mouseData den Umfang der Mausradbewegung an.

> Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UInt32 mouseData, Point Point)

Ein positiver Wert gibt an, dass das Rad nach vorne gedreht wurde, vom Benutzer entfernt; ein negativer Wert gibt an, dass das Rad nach hinten gedreht wurde, in Richtung des Benutzers. Ein Mausrad Klick ist als WHEEL_DELTA definiert, was 120 ist. Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN oder COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP ist, gibt mouseData an, welche X-Schaltflächen gedrückt oder freigegeben wurden. Dieser Wert sollte 1 sein, wenn die erste x-Taste gedrückt/freigegeben wird, und 2, wenn die zweite x-Taste gedrückt/freigegeben wird. Wenn eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE ist, sollten virtualKeys, mouseData und Point alle NULL sein. Wenn eventKind ein beliebiger anderer Wert ist, sollte mouseData NULL sein. Point wird im Client Koordinatensystem der WebView erwartet. Zum nachvollziehen von Mausereignissen, die in der WebView beginnen und potenziell außerhalb der WebView-und Hostanwendung verschoben werden können, wird der Aufruf von SetCapture und ReleaseCapture empfohlen. Wenn Sie Hover-Popups schließen möchten, empfiehlt es sich auch, WM_MOUSELEAVE Nachrichten zu senden. 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### SendPointerInput 

SendPointerInput akzeptiert Fingereingabe-oder Stiftzeiger Eingaben von Typen, die in COREWEBVIEW2_POINTER_EVENT_KIND definiert sind.

> Public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * pointerInfo)

Alle zeigereingaben aus dem System müssen zuerst in eine [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) konvertiert werden.

#### COREWEBVIEW2_MATRIX_4X4 

Matrix, die eine 3D-Transformation darstellt.

> typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)

Diese Transformation wird verwendet, um korrekte Koordinaten beim Aufrufen von CreateCoreWebView2PointerInfoFromPointerId zu berechnen. Dies entspricht einer D2D1_MATRIX_4X4_F

#### COREWEBVIEW2_MOUSE_EVENT_KIND 

Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.

> Enum- [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL            | Mausrad Scroll-Ereignis, WM_MOUSEHWHEEL
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK            | Klicken Sie mit der linken Maustaste auf das Mausereignis, WM_LBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN            | Linke Maustaste-Maustaste-Ereignis, WM_LBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP            | Linke Maustaste, Mausereignis, WM_LBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE            | Maus-Leave-Ereignis, WM_MOUSELEAVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK            | Klicken Sie auf die mittlere Schaltfläche, und klicken Sie auf Mausereignis WM_MBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN            | Klicken Sie auf der mittleren Maustaste auf das Mausereignis, WM_MBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP            | Mittlere Maustaste auf Mausereignis, WM_MBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE            | Maus Bewegungs Ereignis, WM_MOUSEMOVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK            | Klicken Sie mit der rechten Maustaste auf Mausereignis, WM_RBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN            | Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP            | Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL            | Mausrad Scroll-Ereignis, WM_MOUSEWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK            | Erste oder zweite X-Taste Doppelklick-Mausereignis, WM_XBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN            | Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP            | Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONUP.

Die Werte dieser Enumeration sind an die übereinstimmenden WM_ *-Fenster Meldungen ausgerichtet.

#### COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS 

Virtuelle Mausereignis Tasten, die einem COREWEBVIEW2_MOUSE_EVENT_KIND für SendMouseInput zugeordnet sind.

> Enum- [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE            | Keine weiteren Tasten gedrückt.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON            | Linke Maustaste gedrückt, MK_LBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON            | Klicken Sie mit der rechten Maustaste auf die MK_RBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT            | Die UMSCHALTTASTE ist MK_SHIFT.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL            | Die STRG-Taste ist MK_CONTROL.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON            | Mittlere Maustaste gedrückt, MK_MBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1            | Die erste X-Taste ist unten, MK_XBUTTON1.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2            | Die zweite X-Taste ist unten, MK_XBUTTON2.

Diese Werte können in ein Bitflags-Flag kombiniert werden, wenn mehr als eine virtuelle Taste für das Ereignis gedrückt wird. Die Werte dieser Enumeration werden an die übereinstimmenden MK_ *-Maustasten angeglichen.

#### COREWEBVIEW2_POINTER_EVENT_KIND 

Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.

> Enum- [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE            | Entspricht WM_POINTERACTIVATE.
COREWEBVIEW2_POINTER_EVENT_KIND_DOWN            | Entspricht WM_POINTERDOWN.
COREWEBVIEW2_POINTER_EVENT_KIND_ENTER            | Entspricht WM_POINTERENTER.
COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE            | Entspricht WM_POINTERLEAVE.
COREWEBVIEW2_POINTER_EVENT_KIND_UP            | Entspricht WM_POINTERUP.
COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE            | Entspricht WM_POINTERUPDATE.

Die Werte dieser Enumeration sind an die übereinstimmenden WM_POINTER *-Fenster Meldungen ausgerichtet.

