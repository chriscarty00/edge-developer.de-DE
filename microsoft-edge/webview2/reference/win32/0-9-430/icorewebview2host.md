---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Host
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 39566c867c28739d21dd99c369d161d29a308946
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885618"
---
# 0.9.430-Interface-ICoreWebView2Host 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Host
  : public IUnknown
```

Diese Schnittstelle ist der Besitzer des CoreWebView2-Objekts und bietet Unterstützung für die Größenänderung, das ein-und ausblenden, die Fokussierung und andere Funktionen im Zusammenhang mit Fenster und Komposition.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[get_IsVisible](#get_isvisible) | Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.
[put_IsVisible](#put_isvisible) | Festlegen der IsVisible-Eigenschaft
[get_Bounds](#get_bounds) | Die WebView-Begrenzungen.
[put_Bounds](#put_bounds) | Die Bounds-Eigenschaft festlegen.
[get_ZoomFactor](#get_zoomfactor) | Der Zoomfaktor für die WebView.
[put_ZoomFactor](#put_zoomfactor) | Festlegen der ZoomFactor-Eigenschaft
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften
[MoveFocus](#movefocus) | Verschieben des Fokus in WebView
[add_MoveFocusRequested](#add_movefocusrequested) | Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.
[add_GotFocus](#add_gotfocus) | Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.
[remove_GotFocus](#remove_gotfocus) | Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.
[add_LostFocus](#add_lostfocus) | Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.
[remove_LostFocus](#remove_lostfocus) | Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.
[get_ParentWindow](#get_parentwindow) | Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.
[put_ParentWindow](#put_parentwindow) | Das übergeordnete Fenster für die WebView-Ansicht einrichten
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Hierbei handelt es sich um eine von put_Bounds getrennte Benachrichtigung, in der WebView das übergeordnete HWND (oder ein Vorgänger) verschoben wird.
[Schließen](#close) | Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.
[get_CoreWebView2](#get_corewebview2) | Ruft das CoreWebView2 ab, das diesem CoreWebView2Host zugeordnet ist.
[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) | Grund für das Verschieben des Fokus
[CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) | Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.
[CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status) | Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

Die CoreWebView2Host besitzt den CoreWebView2, und wenn alle Verweise auf die CoreWebView2Host verschwindet, wird die WebView geschlossen.

## Member

#### get_IsVisible 

Die IsVisible-Eigenschaft bestimmt, ob die WebView angezeigt oder ausgeblendet werden soll.

> öffentliche HRESULT- [get_IsVisible](#get_isvisible)(bool * isVisible)

Wenn IsVisible auf "false" festgelegt ist, ist die WebView transparent und wird nicht gerendert. Dies wirkt sich jedoch nicht auf das Fenster aus, das die WebView enthält (den HWND-Parameter, der an CreateCoreWebView2Host übergeben wurde). Wenn Sie möchten, dass das Fenster ebenfalls ausgeblendet wird, rufen Sie ShowWindow direkt zusätzlich zum Ändern der IsVisible-Eigenschaft auf. WebView als untergeordnetes Fenster ruft keine Fenster Meldungen ab, wenn das oberste Fenster minimiert oder wiederhergestellt wird. Aus Leistungsgründen sollte Entwickler die IsVisible-Eigenschaft der WebView-Eigenschaft auf "false" festlegen, wenn das App-Fenster minimiert wird, und zurück zu "true", wenn das App-Fenster wiederhergestellt wird. Das App-Fenster kann dies tun, indem SC_MINIMIZE und SC_RESTORE Befehl beim empfangen WM_SYSCOMMAND Nachricht behandelt werden.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### put_IsVisible 

Festlegen der IsVisible-Eigenschaft

> öffentliche HRESULT- [put_IsVisible](#put_isvisible)(bool isVisible)

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_host->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_host->put_IsVisible(TRUE);
            }
        }
    }
```

#### get_Bounds 

Die WebView-Begrenzungen.

> öffentliche HRESULT- [get_Bounds](#get_bounds)(Rect * bounds)

Begrenzungen sind relativ zum übergeordneten HWND. Die APP hat zwei Möglichkeiten, um eine WebView-Position zu positionieren:

1. Erstellen Sie ein untergeordnetes HWND, das das übergeordnete HWND von WebView ist. Positionieren Sie dieses Fenster, in dem sich die WebView befinden soll. Verwenden Sie in diesem Fall (0, 0) für die Bound's obere linke Ecke des Webviews (den Offset).

1. Verwenden Sie das oberste Fenster der App als übergeordnetes WebView-HWND. Stellen Sie die Bound's-obere linke Ecke der WebView so ein, dass die WebView in der APP richtig positioniert ist. Die Werte der Bounds befinden sich im Koordinatenbereich des Hosts.

#### put_Bounds 

Die Bounds-Eigenschaft festlegen.

> öffentliche HRESULT- [put_Bounds](#put_bounds)(Rect-Begrenzungen)

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_host->put_Bounds(desiredBounds);
}
```

#### get_ZoomFactor 

Der Zoomfaktor für die WebView.

> öffentliche HRESULT- [get_ZoomFactor](#get_zoomfactor)(Double * ZoomFactor)

Beachten Sie, dass das Ändern des Zoomfaktors `window.innerWidth/innerHeight` zu einer Änderung des Seitenlayouts führen kann. Ein Zoomfaktor, der vom Host angewendet wird, indem put_ZoomFactor aufgerufen wird, wird zum neuen Standardzoom für die WebView. Dieser Zoomfaktor gilt für alle Navigationselemente und der Zoomfaktor WebView wird zurückgegeben, wenn der Benutzer STRG + 0 drückt. Wenn der Zoomfaktor vom Benutzer geändert wird (was im App-Empfang ZoomFactorChanged), gilt dieser Zoom nur für die aktuelle Seite. Der Zoom eines Benutzers, der angewendet wird, ist nur für die aktuelle Seite vorgesehen und wird in einer Navigation zurückgesetzt. Die Angabe einer ZoomFactor kleiner oder gleich 0 ist nicht zulässig. WebView verfügt auch über einen internen unterstützten Zoomfaktor Bereich. Wenn sich ein angegebener Zoomfaktor außerhalb dieses Bereichs befindet, wird er normalisiert, sodass er innerhalb des Bereichs liegt, und ein ZoomFactorChanged-Ereignis wird für den tatsächlich angewendeten Zoomfaktor ausgelöst. Wenn diese Bereichs Normalisierung erfolgt, meldet die ZoomFactor-Eigenschaft den Zoomfaktor, der während der vorherigen Änderung der ZoomFactor-Eigenschaft angegeben wird, bis das ZoomFactorChanged-Ereignis empfangen wird, nachdem WebView den normalisierten Zoomfaktor angewendet hat.

#### put_ZoomFactor 

Festlegen der ZoomFactor-Eigenschaft

> öffentliche HRESULT- [put_ZoomFactor](#put_zoomfactor)(Double ZoomFactor)

#### add_ZoomFactorChanged 

Fügen Sie einen Ereignishandler für das ZoomFactorChanged-Ereignis hinzu.

> Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

Das Ereignis wird ausgelöst, wenn die ZoomFactor-Eigenschaft des WebView geändert wird. Das Ereignis konnte ausgelöst werden, weil der Aufrufer die ZoomFactor-Eigenschaft geändert hat, oder weil der Benutzer den Zoom manuell geändert hat. Wenn Sie vom Aufrufer über die ZoomFactor-Eigenschaft geändert wird, wird der interne Zoomfaktor sofort aktualisiert, und es gibt kein ZoomFactorChanged-Ereignis. WebView ordnet den zuletzt verwendeten Zoomfaktor für jede Website zu. Daher ist es möglich, dass sich der Zoomfaktor ändert, wenn Sie zu einer anderen Seite navigieren. Wenn sich der Zoomfaktor aufgrund dieser Änderung ändert, wird das ZoomFactorChanged-Ereignis direkt hinter dem ContentLoading-Ereignis ausgelöst.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_host->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Host* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### remove_ZoomFactorChanged 

Entfernen Sie einen Ereignishandler, der zuvor mit add_ZoomFactorChanged hinzugefügt wurde.

> Public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken-Token)

#### SetBoundsAndZoomFactor 

Gleichzeitiges Aktualisieren von Begrenzungen und ZoomFactor-Eigenschaften

> öffentliche HRESULT- [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(Rect-Begrenzungen, Doppel ZoomFactor)

Dieser Vorgang ist vom Perspecive des Hosts atomar. Nach der Rückgabe von dieser Funktion werden die Bounds-Eigenschaft und die ZoomFactor-Eigenschaft beide aktualisiert, wenn die Funktion erfolgreich ist, oder keine wird aktualisiert, wenn die Funktion fehlschlägt. Wenn Grenz-und ZoomFactor sowohl auf der gleichen Skala aktualisiert werden (d. h., dass die Begrenzungen und ZoomFactor beide verdoppelt werden), wird der Seite keine Änderung in Window. InnereBreite/InnereHoehe angezeigt, und die WebView rendert den Inhalt mit der neuen Größe und zoomt ohne zwischen Renderings. Diese Funktion kann auch verwendet werden, um nur eine von ZoomFactor oder Begrenzungen zu aktualisieren, indem der neue Wert für einen und der aktuelle Wert für den anderen übergeben wird.

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_host->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_host->SetBoundsAndZoomFactor(bounds, scale);
}
```

#### MoveFocus 

Verschieben des Fokus in WebView

> öffentliche HRESULT- [MoveFocus](#movefocus)([CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) Grund)

WebView erhält den Fokus, und der Fokus wird auf das korrespondierende Element auf der Seite gesetzt, die in der WebView gehostet wird. Aus Programm Gründen wird der Fokus auf das zuvor fokussierte Element oder auf das Standardelement gesetzt, wenn kein zuvor fokussiertes Element vorhanden ist. Aus dem nächsten Grund wird der Fokus auf das erste Element gesetzt. Aus vorherigen Gründen wird der Fokus auf das letzte Element gesetzt. WebView kann auch den Fokus über die Benutzerinteraktion erhalten, wie das Klicken in WebView oder die Tab-Taste. Für die Tab-Taste kann die APP MoveFocus mit der nächsten oder vorherigen aufrufen, um mit Tab und UMSCHALT + TAB auszurichten, wenn Sie beschließt, dass die WebView das nächste Tabbed-Element ist. Oder die APP kann IsDialogMessage als Teil der Nachrichtenschleife aufrufen, damit die Plattform die Tab-Funktion automatisch verarbeiten kann. Die Plattform wird durch alle Fenster mit WS_TABSTOP gedreht. Wenn die WebView den Fokus von IsDialogMessage erhält, wird der Fokus intern auf das erste oder letzte Element für Tab und UMSCHALT + TAB gesetzt.

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (int i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### add_MoveFocusRequested 

Fügen Sie einen Ereignishandler für das MoveFocusRequested-Ereignis hinzu.

> Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

MoveFocusRequested wird ausgelöst, wenn der Benutzer versucht, die Tab-Taste aus der WebView zu ziehen. Der Fokus der WebView wurde nicht geändert, wenn dieses Ereignis ausgelöst wird.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_host->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    CORE_WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### remove_MoveFocusRequested 

Entfernen Sie einen Ereignishandler, der zuvor mit add_MoveFocusRequested hinzugefügt wurde.

> Public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken-Token)

#### add_GotFocus 

Fügen Sie einen Ereignishandler für das GotFocus-Ereignis hinzu.

> Public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

GotFocus wird ausgelöst, wenn WebView den Fokus erhält.

#### remove_GotFocus 

Entfernen Sie einen Ereignishandler, der zuvor mit add_GotFocus hinzugefügt wurde.

> Public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken-Token)

#### add_LostFocus 

Fügen Sie einen Ereignishandler für das LostFocus-Ereignis hinzu.

> Public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

LostFocus wird ausgelöst, wenn WebView den Fokus verloren hat. In dem Fall, in dem das MoveFocusRequested-Ereignis ausgelöst wird, liegt der Fokus weiterhin auf WebView, wenn das MoveFocusRequested-Ereignis ausgelöst wird. Der verlorene Fokus wird erst dann ausgelöst, wenn der app-Code oder die Standardaktion des MoveFocusRequested-Ereignisses den Fokus von WebView absetzen.

#### remove_LostFocus 

Entfernen Sie einen Ereignishandler, der zuvor mit add_LostFocus hinzugefügt wurde.

> Public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken-Token)

#### add_AcceleratorKeyPressed 

Fügen Sie einen Ereignishandler für das AcceleratorKeyPressed-Ereignis hinzu.

> Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) * EventHandler, EventRegistrationToken * Token)

AcceleratorKeyPressed wird ausgelöst, wenn eine Zugriffstasten-oder Tastenkombination gedrückt oder freigegeben wird, während die WebView fokussiert ist. Ein Schlüssel wird in folgenden Fällen als Beschleuniger betrachtet:

1. STRG oder alt wird derzeit gehalten, oder

1. die Taste gedrückt wird einem Zeichen nicht zugeordnet. Einige bestimmte Tasten gelten nie als Beschleuniger, wie etwa die UMSCHALTTASTE. Die Escape-Taste wird immer als Beschleuniger angesehen.

Durch automatisch wiederholte Tastenereignisse, die durch das Drücken der Taste nach unten verursacht werden, wird dieses Ereignis ebenfalls ausgelöst. Sie können diese filtern, indem Sie das Ereignis args ' KeyEventLParam oder PhysicalKeyStatus.

Im Fenstermodus wird dieser Ereignishandler synchron aufgerufen. Bis Sie Handle () für die Ereignis-args aufrufen oder der Ereignishandler zurückgibt, wird der Browserprozess blockiert, und ausgehende prozessübergreifende com-Aufrufe schlagen mit RPC_E_CANTCALLOUT_ININPUTSYNCCALL fehl. Allerdings funktionieren alle CoreWebView2-API-Methoden.

Im Fenstermodus wird der Ereignishandler asynchron aufgerufen. Eine weitere Eingabe erreicht den Browser erst, wenn der Ereignishandler zurückgegeben oder Handle () aufgerufen wird, der Browserprozess selbst jedoch nicht blockiert wird und ausgehende com-Aufrufe normal funktionieren.

Es wird empfohlen, handle (true) so früh wie möglich aufzurufen, wenn Sie wissen, dass Sie die Zugriffstasten Taste behandeln möchten.

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_host->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                CORE_WEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        CORE_WEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### remove_AcceleratorKeyPressed 

Entfernen Sie einen Ereignishandler, der zuvor mit add_AcceleratorKeyPressed hinzugefügt wurde.

> Public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken-Token)

#### get_ParentWindow 

Das übergeordnete Fenster, das von der APP bereitgestellt wird, die von dieser WebView zum Rendern von Inhalten verwendet wird.

> öffentliche HRESULT- [get_ParentWindow](#get_parentwindow)(HWND * topLevelWindow)

Diese API gibt zunächst das Fenster zurück, das an CreateCoreWebView2Host übergeben wurde.

#### put_ParentWindow 

Das übergeordnete Fenster für die WebView-Ansicht einrichten

> Public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)

Dies bewirkt, dass die WebView das Fenster des neu bereitgestellten Fensters erneut übermittelt.

#### NotifyParentWindowPositionChanged 

Hierbei handelt es sich um eine von put_Bounds getrennte Benachrichtigung, in der WebView das übergeordnete HWND (oder ein Vorgänger) verschoben wird.

> Public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Dies ist für die Barrierefreiheit und bestimmte Dialogfelder in WebView erforderlich, um ordnungsgemäß zu funktionieren. 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### Schließen 

Schließt die WebView und bereinigt die zugrunde liegende Browserinstanz.

> Public HRESULT [Close](#close)()

Durch Bereinigen des Browsers Instanz werden die Ressourcen freigegeben, die die WebView-Ansicht einschalten. Die Browserinstanz wird heruntergefahren, wenn keine anderen Webansichten verwendet werden.

Nach dem Aufruf von Close werden alle Methodenaufrufe fehlschlagen, und die Ereignishandler werden nicht mehr ausgelöst. Insbesondere gibt die WebView Ihre Verweise auf die Ereignishandler frei, wenn Close aufgerufen wird.

Close wird implizit aufgerufen, wenn die CoreWebView2Host den endgültigen Bezug verliert und zerstört wird. Es empfiehlt sich jedoch, explizit Close aufzurufen, um einen zufälligen Zyklus von Verweisen zwischen WebView und app-Code zu vermeiden. Insbesondere wenn Sie einen Verweis auf die WebView in einem Ereignishandler aufzeichnen, erstellen Sie einen Referenz Zyklus zwischen WebView und dem Ereignishandler. Durch das Aufrufen von Close wird dieser Zyklus unterbrochen, indem alle Ereignishandler freigegeben werden. Um dies zu vermeiden, empfiehlt es sich, sowohl explizit Close für die WebView zu verwenden als auch einen Verweis auf die WebView zu erfassen, um sicherzustellen, dass die WebView ordnungsgemäß bereinigt werden kann.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_host)
    {
        m_host->Close();
        m_host = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2.idl#createwebview2environmentwithdetails
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instnaces.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### get_CoreWebView2 

Ruft das CoreWebView2 ab, das diesem CoreWebView2Host zugeordnet ist.

> Public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) * * CoreWebView2)

#### CORE_WEBVIEW2_MOVE_FOCUS_REASON 

Grund für das Verschieben des Fokus

> Enum- [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Der Fokus für die Code Einstellung in WebView.
CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Verschieben des Fokus aufgrund von Tabstopps vorwärts
CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Verschieben des Fokus aufgrund von Tabstopps rückwärts

#### CORE_WEBVIEW2_KEY_EVENT_KIND 

Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.

> Enum- [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN            | Dem Fenster Nachrichten WM_KEYDOWN entsprechen.
CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP            | Dem Fenster Nachrichten WM_KEYUP entsprechen.
CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN            | Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.
CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP            | Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.

#### CORE_WEBVIEW2_PHYSICAL_KEY_STATUS 

Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

> typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)

Weitere Informationen finden Sie in der Dokumentation zu WM_KEYDOWN.[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

