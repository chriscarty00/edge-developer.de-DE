---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core
ms.openlocfilehash: e45cb4c6a6fdd01680abc59691a0e0c34a64af15
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881193"
---
# Microsoft.Web.WebView2.Core namespace 

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Bildformat, das von der CoreWebView2CapturePreview-Methode verwendet wird.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.
[CoreWebView2MouseEventKind](#corewebview2mouseeventkind) | Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.
[CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys) | Virtuelle Mausereignis Tasten, die einem CoreWebView2MouseEventKind für SendMouseInput zugeordnet sind.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Grund für das Verschieben des Fokus
[CoreWebView2PermissionKind](#corewebview2permissionkind) | Der Typ einer Berechtigungsanforderung.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Antwort auf eine Berechtigungsanforderung.
[CoreWebView2PointerEventKind](#corewebview2pointereventkind) | Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Art des in der CoreWebView2ProcessFailedEventHandler-Klasse verwendeten Prozess Fehlers.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Art des in der CoreWebView2ScriptDialogOpeningEventHandler-Klasse verwendeten JavaScript-Dialogfelds.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Fehlerstatus Werte für Web-Navigationselemente.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Enum für Webressourcen-anforderungskontexte.
CoreWebView2 | WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.
CoreWebView2AcceleratorKeyPressedEventArgs | Ereignis-args für das AcceleratorKeyPressed-Ereignis.
CoreWebView2CompositionController | Diese Klasse ist eine Erweiterung der CoreWebView2Controller-Klasse, um das visuelle Hosting zu unterstützen.
CoreWebView2ContentLoadingEventArgs | Ereignis-args für das ContentLoading-Ereignis.
CoreWebView2Controller | Diese Klasse ist der Besitzer des CoreWebView2-Objekts und bietet Unterstützung für die Größenänderung, das ein-und ausblenden, die Fokussierung und andere Funktionen im Zusammenhang mit Fenster und Komposition.
CoreWebView2Deferral | Diese Klasse wird verwendet, um Verzögerungen für Ereignis-args abzuschließen, die das Abrufen von Verzögerungen über Ihre getstundung-Methode unterstützen.
CoreWebView2DevToolsProtocolEventReceivedEventArgs | Ereignis-args für das DevToolsProtocolEventReceived-Ereignis.
CoreWebView2DevToolsProtocolEventReceiver | Ein Empfänger wird für ein bestimmtes devtools-Protokollereignis erstellt und ermöglicht Ihnen, dieses Ereignis zu abonnieren und abzubestellen.
CoreWebView2Environment | Dies stellt die WebView2-Umgebung dar.
CoreWebView2EnvironmentOptions | Optionen zum Erstellen der WebView2-Umgebung
CoreWebView2MoveFocusRequestedEventArgs | Ereignis-args für das MoveFocusRequested-Ereignis.
CoreWebView2NavigationCompletedEventArgs | Ereignis-args für das NavigationCompleted-Ereignis.
CoreWebView2NavigationStartingEventArgs | Ereignis-args für das NavigationStarting-Ereignis.
CoreWebView2NewWindowRequestedEventArgs | Ereignis-args für das mswebviewnewwindowrequested-Ereignis.
CoreWebView2PermissionRequestedEventArgs | Ereignis-args für das PermissionRequested-Ereignis.
CoreWebView2PointerInfo | Dies stellt in erster Linie ein kombiniertes Win32-POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO-Objekt dar.
CoreWebView2ProcessFailedEventArgs | Ereignis-args für das ProcessFailed-Ereignis.
CoreWebView2ScriptDialogOpeningEventArgs | Ereignis-args für das ScriptDialogOpening-Ereignis.
CoreWebView2Settings | Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.
CoreWebView2SourceChangedEventArgs | Ereignis-args für das Sourcecode-Ereignis.
CoreWebView2WebMessageReceivedEventArgs | Ereignis-args für das WebMessageReceived-Ereignis.
CoreWebView2WebResourceRequestedEventArgs | Ereignis-args für das WebResourceRequested-Ereignis.
CoreWebView2WindowFeatures | Fenster Features für ein WebView-Popupfenster
EdgeNotFoundException | Diese Ausnahme wird ausgelöst, wenn eine Edge-Installation fehlt.
CoreWebView2Matrix4x4 | Diese Transformation wird verwendet, um korrekte Koordinaten beim Aufrufen von CreateCoreWebView2PointerInfoFromPointerId zu berechnen.
CoreWebView2PhysicalKeyStatus | Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

## Member

#### CoreWebView2CapturePreviewImageFormat 

Bildformat, das von der CoreWebView2CapturePreview-Methode verwendet wird.

> Enum- [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
PNG            | PNG-Bildformat.
JPEG            | JPEG-Bildformat.

#### CoreWebView2KeyEventKind 

Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.

> Enum- [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
KeyDown            | Dem Fenster Nachrichten WM_KEYDOWN entsprechen.
KeyUp            | Dem Fenster Nachrichten WM_KEYUP entsprechen.
SystemKeyDown            | Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.
SystemKeyUp            | Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.

#### CoreWebView2MouseEventKind 

> [!NOTE]
> Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.

Maus Ereignistyp, der von SendMouseInput verwendet wird, um den Typ des Mausereignisses zu übermitteln, das an WebView gesendet wird.

> Enum- [CoreWebView2MouseEventKind](#corewebview2mouseeventkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
HorizontalWheel            | Mausrad Scroll-Ereignis, WM_MOUSEHWHEEL
LeftButtonDoubleClick            | Klicken Sie mit der linken Maustaste auf das Mausereignis, WM_LBUTTONDBLCLK.
LeftButtonDown            | Linke Maustaste-Maustaste-Ereignis, WM_LBUTTONDOWN.
LeftButtonUp            | Linke Maustaste, Mausereignis, WM_LBUTTONUP.
Verlassen            | Maus-Leave-Ereignis, WM_MOUSELEAVE.
MiddleButtonDoubleClick            | Klicken Sie auf die mittlere Schaltfläche, und klicken Sie auf Mausereignis WM_MBUTTONDBLCLK.
MiddleButtonDown            | Klicken Sie auf der mittleren Maustaste auf das Mausereignis, WM_MBUTTONDOWN.
MiddleButtonUp            | Mittlere Maustaste auf Mausereignis, WM_MBUTTONUP.
Move            | Maus Bewegungs Ereignis, WM_MOUSEMOVE.
RightButtonDoubleClick            | Klicken Sie mit der rechten Maustaste auf Mausereignis, WM_RBUTTONDBLCLK.
RightButtonDown            | Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONDOWN.
RightButtonUp            | Klicken Sie mit der rechten Maustaste auf das Mausereignis, WM_RBUTTONUP.
Rad            | Mausrad Scroll-Ereignis, WM_MOUSEWHEEL.
XButtonDoubleClick            | Erste oder zweite X-Taste Doppelklick-Mausereignis, WM_XBUTTONDBLCLK.
XButtonDown            | Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONDOWN.
XButtonUp            | Erstes oder zweites X-Schaltflächen-Mausereignis, WM_XBUTTONUP.

#### CoreWebView2MouseEventVirtualKeys 

> [!NOTE]
> Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.

Virtuelle Mausereignis Tasten, die einem CoreWebView2MouseEventKind für SendMouseInput zugeordnet sind.

> Enum- [CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Keine            | Keine weiteren Tasten gedrückt.
LeftButton            | Linke Maustaste gedrückt, MK_LBUTTON.
RightButton            | Klicken Sie mit der rechten Maustaste auf die MK_RBUTTON.
UMSCHALTTASTE            | Die UMSCHALTTASTE ist MK_SHIFT.
Steuerelement            | Die STRG-Taste ist MK_CONTROL.
MiddleButton            | Mittlere Maustaste gedrückt, MK_MBUTTON.
XButton1            | Die erste X-Taste ist unten, MK_XBUTTON1.
XButton2            | Die zweite X-Taste ist unten, MK_XBUTTON2.

#### CoreWebView2MoveFocusReason 

Grund für das Verschieben des Fokus

> Enum- [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Programmatischen            | Der Fokus für die Code Einstellung in WebView.
Nächste            | Verschieben des Fokus aufgrund von Tabstopps vorwärts
Vorherige            | Verschieben des Fokus aufgrund von Tabstopps rückwärts

#### CoreWebView2PermissionKind 

Der Typ einer Berechtigungsanforderung.

> Enum- [CoreWebView2PermissionKind](#corewebview2permissionkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
UnknownPermission            | Unbekannte Berechtigung.
Mikrofon            | Berechtigung zum Aufzeichnen von Audio.
Kamera            | Berechtigung zum Aufzeichnen von Videos.
Geolocation            | Berechtigung für den Zugriff auf Geolocation.
Benachrichtigungen            | Berechtigung zum Senden von webbenachrichtigungen.
OtherSensors            | Berechtigung für den Zugriff auf den generischen Sensor.
ClipboardRead            | Berechtigung zum Lesen der Systemzwischenablage ohne Benutzergeste

#### CoreWebView2PermissionState 

Antwort auf eine Berechtigungsanforderung.

> Enum- [CoreWebView2PermissionState](#corewebview2permissionstate)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Standard            | Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.
Zulassen            | Erteilen Sie die Berechtigungsanforderung.
Verweigern            | Verweigern Sie die Berechtigungsanforderung.

#### CoreWebView2PointerEventKind 

> [!NOTE]
> Hierbei handelt es sich um eine [experimentelle API](../../../concepts/versioning.md#experimental-apis) , die mit unserer SDK [-Version 0.9.538-Prerelease](../../../releasenotes.md#09538)ausgeliefert wurde.

Zeiger Ereignistyp, der von SendPointerInput verwendet wird, um den Typ des Zeiger Ereignisses zu vermitteln, das an WebView gesendet wird.

> Enum- [CoreWebView2PointerEventKind](#corewebview2pointereventkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Aktivieren            | Entspricht WM_POINTERACTIVATE.
Unten            | Entspricht WM_POINTERDOWN.
Eingabe            | Entspricht WM_POINTERENTER.
Verlassen            | Entspricht WM_POINTERLEAVE.
Oben            | Entspricht WM_POINTERUP.
Update            | Entspricht WM_POINTERUPDATE.

#### CoreWebView2ProcessFailedKind 

Art des in der CoreWebView2ProcessFailedEventHandler-Klasse verwendeten Prozess Fehlers.

> Enum- [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
BrowserProcessExited            | Es wurde angegeben, dass der Browserprozess unerwartet beendet wurde.
RenderProcessExited            | Der Renderprozess wurde unerwartet beendet.
RenderProcessUnresponsive            | Angezeigt, dass der Renderprozess nicht mehr reagiert.

#### CoreWebView2ScriptDialogKind 

Art des in der CoreWebView2ScriptDialogOpeningEventHandler-Klasse verwendeten JavaScript-Dialogfelds.

> Enum- [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Warnung            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.
Bestätigen            | Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.
Aufforderung            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.
Beforeunload            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. beforeunload" aufgerufen wird.

#### CoreWebView2WebErrorStatus 

Fehlerstatus Werte für Web-Navigationselemente.

> Enum- [CoreWebView2WebErrorStatus](#corewebview2weberrorstatus)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Unknown            | Ein unbekannter Fehler ist aufgetreten.
CertificateCommonNameIsIncorrect            | Der allgemeine Name des SSL-Zertifikats entspricht nicht der Webadresse.
CertificateExpired            | Das SSL-Zertifikat ist abgelaufen.
ClientCertificateContainsErrors            | Das SSL-Clientzertifikat enthält Fehler.
CertificateRevoked            | Das SSL-Zertifikat wurde gesperrt.
CertificateIsInvalid            | Das SSL-Zertifikat ist ungültig &ndash; Dies könnte bedeuten, dass das Zertifikat nicht mit den öffentlichen Schlüssel Pins für den Hostnamen übereinstimmte. das Zertifikat wird von einer nicht vertrauenswürdigen Zertifizierungsstelle signiert oder mit einem schwachen Vorzeichen Algorithmus, das Zertifikat behauptet, dass DNS-Namen gegen Namenseinschränkungen verstoßen, das Zertifikat einen schwachen Schlüssel enthält, der Gültigkeitszeitraum des Zertifikats zu lang ist, fehlender Sperrungsinformationen oder Sperrungs Mechanismus, nicht eindeutiger [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)Hostname, fehlender Zertifikat Transparenzinformationen oder das Zertifikat an
ServerUnreachable            | Der Host ist nicht erreichbar.
Timeout            | Die Verbindung hat ein Zeitlimit überschritten.
ErrorHttpInvalidServerResponse            | Der Server hat eine ungültige oder unbekannte Antwort zurückgegeben.
ConnectionAborted            | Die Verbindung wurde abgebrochen.
ConnectionReset            | Die Verbindung wurde zurückgesetzt.
Getrennt            | Die Internet Verbindung wurde unterbrochen.
CannotConnect            | Verbindung mit Ziel kann nicht hergestellt werden.
HostNameNotResolved            | Der angegebene Hostname konnte nicht aufgelöst werden.
OperationCanceled            | Der Vorgang wurde abgebrochen.
RedirectFailed            | Die Anforderungs Umleitung ist fehlgeschlagen.
UnexpectedError            | Ein unerwarteter Fehler ist aufgetreten.

#### CoreWebView2WebResourceContext 

Enum für Webressourcen-anforderungskontexte.

> Enum- [CoreWebView2WebResourceContext](#corewebview2webresourcecontext)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Alle            | Alle Ressourcen.
Dokument            | Dokument Ressourcen.
Stylesheet            | CSS-Ressourcen.
Bild            | Bildressourcen.
Medien            | Andere Medienressourcen wie Videos.
Font            | Schriftartressourcen.
Skript            | Skriptressourcen.
XHR            | XML-HTTP-Anforderungen.
Holen            | Abrufen der API-Kommunikation.
TextTrack            | Texttracking-Ressourcen.
EventSource            | EventSource-API-Kommunikation.
Websocket            | WebSocket-API-Kommunikation.
Manifest            | Web App-Manifeste
SignedExchange            | Signierte http-Exchanges.
Ping            | Ping-Anforderungen.
CspViolationReport            | Berichte zu CSP-Verstößen
Other            | Andere Ressourcen.

