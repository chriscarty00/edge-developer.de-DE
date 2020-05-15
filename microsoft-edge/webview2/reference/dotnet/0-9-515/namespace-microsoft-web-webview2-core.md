---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2 für Win32-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: f939f75aca7c89534914fbbaa2ef285564304f60
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654065"
---
# Microsoft. Web. WebView2. Core-Namespace 

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Bildformat, das von der CoreWebView2CapturePreview-Methode verwendet wird.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Grund für das Verschieben des Fokus
[CoreWebView2PermissionKind](#corewebview2permissionkind) | Der Typ einer Berechtigungsanforderung.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Antwort auf eine Berechtigungsanforderung.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Art des in der CoreWebView2ProcessFailedEventHandler-Klasse verwendeten Prozess Fehlers.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Art des in der CoreWebView2ScriptDialogOpeningEventHandler-Klasse verwendeten JavaScript-Dialogfelds.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Fehlerstatus Werte für Web-Navigationselemente.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Enum für Webressourcen-anforderungskontexte.
CoreWebView2 | WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.
CoreWebView2AcceleratorKeyPressedEventArgs | Ereignis-args für das AcceleratorKeyPressed-Ereignis.
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
CoreWebView2ProcessFailedEventArgs | Ereignis-args für das ProcessFailed-Ereignis.
CoreWebView2ScriptDialogOpeningEventArgs | Ereignis-args für das ScriptDialogOpening-Ereignis.
CoreWebView2Settings | Definiert Eigenschaften, die WebView-Features aktivieren, deaktivieren oder ändern.
CoreWebView2SourceChangedEventArgs | Ereignis-args für das Sourcecode-Ereignis.
CoreWebView2WebMessageReceivedEventArgs | Ereignis-args für das WebMessageReceived-Ereignis.
CoreWebView2WebResourceRequestedEventArgs | Ereignis-args für das WebResourceRequested-Ereignis.
EdgeNotFoundException | Diese Ausnahme wird ausgelöst, wenn eine Edge-Installation fehlt.
CoreWebView2PhysicalKeyStatus | Eine Struktur, die die Informationen darstellt, die in lParam verpackt sind, die einem Win32-Schlüsselereignis zugewiesen wurden.

## Member

#### CoreWebView2CapturePreviewImageFormat 

> Enum- [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
PNG            | PNG-Bildformat.
JPEG            | JPEG-Bildformat.

Bildformat, das von der CoreWebView2CapturePreview-Methode verwendet wird.

#### CoreWebView2KeyEventKind 

> Enum- [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
KeyDown            | Dem Fenster Nachrichten WM_KEYDOWN entsprechen.
KeyUp            | Dem Fenster Nachrichten WM_KEYUP entsprechen.
SystemKeyDown            | Dem Fenster Nachrichten WM_SYSKEYDOWN entsprechen.
SystemKeyUp            | Dem Fenster Nachrichten WM_SYSKEYUP entsprechen.

Der Typ des Schlüssel Ereignisses, das ein AcceleratorKeyPressed-Ereignis ausgelöst hat.

#### CoreWebView2MoveFocusReason 

> Enum- [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Programmatischen            | Der Fokus für die Code Einstellung in WebView.
Nächste            | Verschieben des Fokus aufgrund von Tabstopps vorwärts
Vorherige            | Verschieben des Fokus aufgrund von Tabstopps rückwärts

Grund für das Verschieben des Fokus

#### CoreWebView2PermissionKind 

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

Der Typ einer Berechtigungsanforderung.

#### CoreWebView2PermissionState 

> Enum- [CoreWebView2PermissionState](#corewebview2permissionstate)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Standard            | Verwenden Sie das Standardbrowser Verhalten, das die Benutzer normalerweise zur Entscheidung auffordert.
Zulassen            | Erteilen Sie die Berechtigungsanforderung.
Verweigern            | Verweigern Sie die Berechtigungsanforderung.

Antwort auf eine Berechtigungsanforderung.

#### CoreWebView2ProcessFailedKind 

> Enum- [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
BrowserProcessExited            | Es wurde angegeben, dass der Browserprozess unerwartet beendet wurde.
RenderProcessExited            | Der Renderprozess wurde unerwartet beendet.
RenderProcessUnresponsive            | Angezeigt, dass der Renderprozess nicht mehr reagiert.

Art des in der CoreWebView2ProcessFailedEventHandler-Klasse verwendeten Prozess Fehlers.

#### CoreWebView2ScriptDialogKind 

> Enum- [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Werte                         | Beschreibungen
--------------------------------|---------------------------------------------
Warnung            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. Alert" aufgerufen wird.
Bestätigen            | Ein Dialogfeld, das über die JavaScript-Funktion "Fenster. bestätigen" aufgerufen wird.
Aufforderung            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. prompt" aufgerufen wird.
Beforeunload            | Ein Dialogfeld, das über die JavaScript-Funktion "Window. beforeunload" aufgerufen wird.

Art des in der CoreWebView2ScriptDialogOpeningEventHandler-Klasse verwendeten JavaScript-Dialogfelds.

#### CoreWebView2WebErrorStatus 

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

Fehlerstatus Werte für Web-Navigationselemente.

#### CoreWebView2WebResourceContext 

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

Enum für Webressourcen-anforderungskontexte.

