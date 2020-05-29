---
description: Hosten von Webinhalten in Ihrer Windows 10-App mit dem WebView (EdgeHTML)-Steuerelement
title: Microsoft Edge WebView für Windows 10-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: x-ms-WebView, MSHTMLWebViewElement, WebView, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 08efb1bb87877e0b11cbc3bee1061f9be6c9ab3f
ms.sourcegitcommit: 831fc41ea347e2d1160b1804fb5e5a427dc3070d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629549"
---
# WebView (EdgeHTML) für Windows 10-apps

Das WebView (EdgeHTML)-Steuerelement ermöglicht das Hosten von Webinhalten in Ihrer Windows 10-app. 

Sie können es als XAML-Element (für [universelle Windows-Plattform (UWP)-apps](/uwp/api/Windows.UI.Xaml.Controls.WebView) und [Windows Forms-und WPF-Desktopanwendungen](/windows/communitytoolkit/controls/wpf-winforms/webview)) oder als HTML-Element (x-ms-WebView)-/DOM-Objekt (MSHTMLWebViewElement) für JavaScript-basierte Windows 10-Apps verwenden, wie hier beschrieben.

| | |
|-|-|
| [**Ereignisse**](#events) | [departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)
| [**Methoden**](#methods) | [addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [GoBack](#goback), [GoForward](#goforward), [Navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Aktualisieren](#refresh), [Beenden](#stop) |
| [**Eigenschaften**](#properties) | [canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [Process](#process), [Settings](#settings), [src](#src), [Width](#width) |

## Syntax

```js
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```

## Hinweise

### WebView versus IFRAME

Wie bei einem standardmäßigen HTML- [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) -Element können Sie WebView verwenden, um Remote Seiten über HTTP und lokale Seiten (*MS-AppX-Web:///*) aus Ihrem App-Paket zu laden. Die WebView-Ansicht kann aber auch:

 - Laden von Seiten und Ressourcen aus Ihren [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) -Ordnern (lokal, Roaming, Temp) (*MS-APPDATA:///*) und [in-Memory-Streams](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)

 - Bereitstellen von Browser ähnlichen Steuerelementen: für das [zurück](#goback) gehen und [weiterleiten](#goforward) im Navigationsverlauf sowie zum [Beenden](#stop) oder [Aktualisieren](#refresh) der aktuellen Seite. 

 - [Erfassen Sie Screenshots von Webinhalten](#capturepreviewtoblobasync) , wodurch die Implementierung des Windows 10-APP- [Freigabe](/windows/uwp/app-to-app/share-data) Vertrags einfach ist.

 - Ermöglichen Sie JavaScript-Code, der in einer WebView ausgeführt wird, um benutzerdefinierte Ereignisse ([MSWebViewScriptNotify](#mswebviewscriptnotify)) für Ihre APP auszulösen, und ermöglichen Sie Ihrer APP das Ausführen von JavaScript innerhalb der WebView ([invokeScriptAsync](#invokescriptasync)).

 - Bereitstellen von optimierten WebView-Inhalts Ereignissen:
    
    WebView-DOM-Ereignis | Beschreibung
    --------- | ------
    [MSWebViewNavigationStarting](#mswebviewnavigationstarting) | Gibt an, dass die WebView mit der Navigation beginnt
    [MSWebViewContentLoading](#mswebviewcontentloading) | Der HTML-Inhalt wird heruntergeladen und in das Steuerelement geladen.
    [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded) | Gibt an, dass die wichtigsten DOM-Elemente das Laden beenden
    [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted) | Gibt an, dass die Navigation abgeschlossen ist und alle Medienelemente gerendert werden.
    [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) | Die WebView hat festgestellt, dass der Inhalt nicht HTML war
    [UnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying) | Die WebView zeigt eine Warnungsseite für Inhalte, die vom Windows-SmartScreen- *Filter*als unsicher gemeldet wurden.

    ... einschließen entsprechender [Ereignisse](#events) für iframe-Inhalte, die in einer WebView geladen wurden (beispielsweise [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) usw.)

### Drucken

Wenn eine Windows-App mit JavaScript gedruckt wird, `<x-ms-webview>` werden die Tags `<iframe>` vor dem Drucken in Tags umgewandelt. Neben dem normalen Unterschied zwischen der Anzeige auf dem Bildschirm und dem gerenderten Ausdruck für den Druck gelten die auf Elemente angewendeten CSS-Formatvorlagen `<iframe>` dann für die `<iframe>` Transformation von `<x-ms-webview>` .

### Dienstmitarbeiter

Beginnend mit dem [2018-Update für Windows 10 Oktober](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18) [werden Dienstmitarbeiter im WebView-Steuerelement](/microsoft-edge/dev-guide#service-workers) (zusätzlich zum Microsoft Edge-Browser und Windows 10-apps mit JavaScript) unterstützt.

x64-App-Architekturen erfordern neutrale (Any CPU)-oder x64-Pakete, da Dienstmitarbeiter in WOW64-Prozessen nicht unterstützt werden. (Um Speicherplatz zu sparen, ist die WoW-Version der erforderlichen DLLs nicht nativ in Windows enthalten.)

### Threadingmodell und Zuverlässigkeit

Durch das Erstellen einer WebView über `document.createElement("x-ms-webview")` oder über `<x-ms-webview>` Markup wird ein WebView für einen neuen eindeutigen Thread im App-Prozess erstellt. Die Ausführung auf einem neuen eindeutigen Thread bedeutet, dass die APP oder andere Webansichten von einem WebView-Skript mit langer Laufzeit nicht hängen können. Durch das Erstellen einer WebView über den `new MSWebView()` Konstruktor wird eine WebView in einem separaten WebView-Prozess erstellt. Die Ausführung in einem eindeutigen Prozess bedeutet, dass die APP neben dem Schutz vor Skripts mit langer Ausführungszeit auch vor Webinhalten geschützt ist, die den WebView-Prozess abstürzen. Durch das Erstellen einer WebView über die [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) Methode wird auch eine WebView in einem separaten Prozess erstellt, die dem Aufrufer jedoch mehr Kontrolle über Prozesseinstellungen und das Gruppieren von Webansichten in WebView-Prozessen ermöglicht. Weitere Informationen finden Sie unter `MSWebViewProcess`. 

### WinRT-API-Zugriff

Eine UWP-App kann HTML-Dokumenten in Webviews den Zugriff auf WinRT-APIs ermöglichen. Dies erfolgt über das WindowsRuntimeAccess-Attribut der untergeordneten Rule-Elemente des ApplicationContentUriRules-Elements der AppxManifest. XML der UWP-app. Wenn Sie WindowsRuntimeAccess auf "alle" und HTML-Dokumente mit übereinstimmenden URIs setzen, ist die Verwendung von WinRT zulässig. Dies entspricht dem Bereitstellen von WinRT-Zugriff auf HTML-Inhalte in JavaScript-UWP-apps, daher finden Sie weitere Informationen unter [Aufrufen von WinRT-APIs aus ihrer PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) .

UI-bezogene WinRT-APIs funktionieren möglicherweise nicht, wenn Sie von einer WebView aufgerufen werden, die in einem eigenen Thread ausgeführt wird, aber möglicherweise funktioniert, wenn Sie von einer WebView aufgerufen wird, die in einem Bei Verwendung einer WebView in einem eigenen eindeutigen Thread ist dieser Thread nicht der Ansicht-Thread der app. Einige UI-bezogene WinRT-APIs müssen aus dem Ansicht-Thread der app aufgerufen werden. Webansichten, die in einem separaten WebView-Prozess erstellt wurden, werden in einem Ansicht-Thread ausgeführt und sollten daher nicht den gleichen Einschränkungen unterliegen, wie die WebView-Ausführung in einem eigenen eindeutigen Thread. Wenn Sie Probleme mit UI-bezogenen WinRT-APIs in einer WebView haben, stellen Sie sicher, dass Sie eine WebView in einem eigenen WebView-Prozess verwenden, wie oben beschrieben.

### AppCache-Speichereinschränkungen

Anwendungen, die JavaScript-Unterstützung der Anwendungs Cache-API (oder AppCache) verwenden, wie in der [HTML5-Spezifikation](https://go.microsoft.com/fwlink/p/?LinkId=228542)definiert, um Offline-Webanwendungen zu erstellen, müssen die verfügbaren Speichereinschränkungen beachten. Dies gilt insbesondere für Geräte mit wenig Speicherplatz. Die praktischen Grenzwerte für die Größe der AppCache sind immer eine Funktion des verfügbaren Speicherplatzes. Nachfolgend sind die allgemeinen Richtlinien aufgeführt.

| Datenträgergröße         |AppCache pro Domäne | AppCache pro Benutzer   | 
|---------------|---------------|-------------------------|
Bis zu 4 GB | 10MB | 50 MB |
4GB bis 16GB | 50 MB | 500MB | 
16GB bis 32 GB | 50 MB | 1 GB |

Da alle Windows10-apps das gleiche AppCache-Kontingent Modell verwenden sollen, gilt die verfügbare Festplattenspeicher Beschränkung sowohl für Desktop-als auch für Telefon-apps. Das ist auch eine harte Grenze, nachdem Seiten, die in **WebView** geladen wurden, 1 GB *AppCache* Speicherplatz verbraucht haben. Anforderungen für zusätzlichen *AppCache* -Speicher oberhalb dieser Grenze werden verweigert. 

Weitere Informationen finden Sie unter Beispiel für ein [HTML-WebView-Steuerelement](https://go.microsoft.com/fwlink/p/?linkid=309825) und die JSBrowser, die [die WebView-Steuerelement Dokumentation nutzbar](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) macht.

## Ereignisse

### departingFocus

Gibt an, dass der Fokus vom **WebView** in die APP abgeht. Wird ausgelöst, wenn das Dokument der obersten Ebene des Webviews Window. departFocus aufruft. Die FocusNavigationEvent-args im departingFocus-Ereignis entsprechen den Parametern, die für departFocus bereitgestellt werden, mit der Ausnahme, dass die Ursprungs Parameter aus dem Benutzers-Koordinatenraum des Webviews in den Koordinatenbereich des WebView-Host Dokuments übersetzt werden. Weitere Informationen finden Sie unter WebView. navigateFocus-Methode und entsprechendes Window-navigatingFocus-Ereignis zum Übertragen des Fokus vom Host auf WebView. Ein Beispiel für eine Implementierung der Fokusnavigation über die Tastatur oder das Gamepad, die dieses Ereignis behandelt, finden Sie in der [TVJS-Navigations Bibliothek](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [FocusNavigationEvent](./webview/FocusNavigationEvent.md) |
|**Synchron** |Ja |    
|**Blasen**     |Ja |   
|**Abbrechbar**  |Nein |            

### MSWebViewContainsFullScreenElementChanged

Tritt auf, wenn sich der Status ändert, ob die **WebView** derzeit ein voll Bildelement enthält. Verwenden Sie die containsFullScreenElement-Eigenschaft auf den aktuellen Wert. Vollbild-Element hier bezieht sich auf den [Fullscreen-DOM-APIs](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) -Begriff eines Vollbild-Elements über die Funktionen "Element. requestFullScreen" und "Document. exitFullScreen Dom".

```js
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | **Ereignis** |
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |  

### MSWebViewContentLoading

Gibt an, dass der HTML-Inhalt heruntergeladen und in das Steuerelement geladen wird.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |    

### MSWebViewDOMContentLoaded

Gibt an, dass die wichtigsten DOM-Elemente geladen wurden.


```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |                 

### MSWebViewFrameContentLoading

Gibt an, dass der HTML-Inhalt heruntergeladen und in das `<iframe>` Steuerelement geladen wird.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |                 

### MSWebViewFrameDOMContentLoaded

Gibt an, dass die wichtigsten DOM-Elemente das Laden in `<iframe>` .

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |    


### MSWebViewFrameNavigationCompleted

Gibt an, dass die Navigation abgeschlossen ist und alle Medienelemente in der gerendert werden `<iframe>` .

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |       

### MSWebViewFrameNavigationStarting

Gibt an `<iframe>` , dass eine innerhalb einer **WebView** beginnt, zu navigieren. Dieser wird ausgelöst, bevor Ressourcen aus dem Netzwerk für die Navigation abgerufen werden. Die Navigation wird erst gestartet, wenn alle MSWebViewFrameNavigationStarting-Ereignishandler abgeschlossen sind. Dieses Ereignis kann über einen Anruf abgebrochen werden `eventArgs.preventDefault()` . Wenn die Ansicht abgebrochen wird, wird die Navigation nicht durch die WebView ausgeführt.


```js
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Ja |                 
          
### MSWebViewLongRunningScriptDetected

Tritt in regelmäßigen Abständen während einer unterbrechungsfreien Skriptausführung in der **WebView**auf, sodass Sie das Skript anhalten können.

```js
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [LongRunningScriptDetectedEvent](./webview/LongRunningScriptDetectedEvent.md) |
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |            

### MSWebViewNavigationCompleted

Gibt an, dass die Navigation abgeschlossen ist und alle Medienelemente gerendert werden oder ein Navigationsfehler aufgetreten ist. Überprüfen Sie die Eigenschaft Event args issuccess, um zu ermitteln, ob die Navigation erfolgreich war, und die webErrorStatus-Eigenschaft, um Details zum Navigationsfehler anzuzeigen. Navigationsfehler können auftreten, bevor Inhalte aus dem Netzwerk abgerufen werden, beispielsweise, wenn der Hostname eines URIs nicht aufgelöst wird, wobei das MSWebViewNavigationStarted-Ereignis ausgelöst wird, gefolgt vom MSWebViewNavigationCompleted-Ereignis. Navigationsfehler können auch auftreten, nachdem eine Fehlerseite von einem Webserver empfangen wurde, beispielsweise eine 404-Seite von einem HTTP-Server, in dem alle Navigationsereignisse ausgelöst werden, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded und dann MSWebViewNavigationCompleted. Wenn Sie eine Fehlerseite für die APP-Navigation für Fälle bereitstellen möchten, in denen der Webserver keine Fehlerseite bereitgestellt hat, müssen Sie überprüfen, ob MSWebViewContentLoading nicht für eine fehlerhafte Navigation ausgelöst wurde, die angibt, dass keine Fehlerseite für den Server bereitgestellt wurde.

```js
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |                 
         

### MSWebViewNavigationStarting

Gibt an, dass die **WebView** mit der Navigation beginnt. Dieser wird ausgelöst, bevor Ressourcen aus dem Netzwerk für die Navigation abgerufen werden. Die Navigation wird erst gestartet, wenn alle MSWebViewNavigationStarting-Ereignishandler abgeschlossen sind. Dieses Ereignis kann über einen Anruf abgebrochen werden `eventArgs.preventDefault()` . Wenn die Ansicht abgebrochen wird, wird die Navigation nicht durch die WebView ausgeführt.


```js
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchron** |Nein  |    
|**Blasen**     |Ja |   
|**Abbrechbar**  |Ja |      

### MSWebViewNewWindowRequested

Wird ausgelöst, wenn der Inhalt in **WebView** versucht, ein neues Fenster zu öffnen. Wenn das Ereignis nicht abgebrochen wird, startet WebView den URI der neuen Fenster Anforderung im Standardbrowser des Benutzers.

```js
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEventWithReferrer](./webview/NavigationEventWithReferrer.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Ja |                 
           

### MSWebViewPermissionRequested

Gibt an, dass der Inhalt in der **WebView** auf Funktionen (wie Geolocation oder Pointer Lock Access) zugreifen soll, für die normalerweise Endbenutzerberechtigungen erforderlich sind. Wenn kein Ereignishandler registriert ist oder der Ereignishandler EventArgs. permissionRequest. allow (), verzögern () oder DENY () nicht aufruft, wird standardmäßig die Berechtigungsanforderung abgelehnt. Wenn Sie entscheiden müssen, ob die Berechtigung zum Beispiel asynchron zugelassen oder verweigert wird, wenn Sie den Benutzer auffordern müssen, verwenden Sie EventArgs. permissionRequest. verzögern (). Die Berechtigungsanforderung wird verzögert, bis Sie WebView. getDeferredPermissionRequestById oder WebView. getDeferredPermissionRequests verwenden und Allow () oder DENY () auf dem DeferredPermissionRequest mit dem entsprechenden ID-Wert aufrufen.

```js
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [PermissionRequestedEvent](./webview/PermissionRequestedEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |    


### MSWebViewProcessExited

Gibt an, dass der **WebView** -Komponenten Prozess abstürzte. Dies ist nur für eine Out-of-Process-WebView relevant. Im Abschnitt "Hinweise" finden Sie Informationen zum Erstellen einer Out-of-Process-WebView im Gegensatz zu einer in-Process-WebView. Nachdem dieses Ereignis ausgelöst wurde, wird die entsprechende WebView in einen abgestürzten Zustand versetzt. Beim Aufrufen der meisten WebView-spezifischen Methoden oder beim Zugriff auf die meisten WebView-spezifischen Eigenschaften einer abgestürzten WebView wird eine Ausnahme ausgelöst. Wenn Sie dieses Ereignis wiederherstellen möchten, entfernen Sie den abgestürzten WebView aus dem Dom, und ersetzen Sie ihn durch einen neuen WebView.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | **Ereignis** |
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |      


### MSWebViewWebResourceRequested

Wird ausgelöst, wenn eine Seite im **WebView** -Element eine Ressource anfordert.

```js
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [WebResourceRequestedEvent](./webview/WebResourceRequestedEvent.md) |
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |      


### MSWebViewScriptNotify

Wird ausgelöst, wenn eine Seite im **WebView** -Element die **Window. external. Notify** -Methode aufruft. Die Window. external. Notify-Methode steht nur für Dokumente mit URIs zur Verfügung, die den Regeln im manifest's-ApplicationContentUriRules der App entsprechen oder durch Festlegen von WebView. Settings. isScriptNotifyAllowed auf true xxxxxxxxxxxxxxx zugelassen wurden. Darüber hinaus steht Window. external. Notify nur für das Dokument der obersten Ebene von WebView zur Verfügung.

```js
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [ScriptNotifyEvent](./webview/ScriptNotifyEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |      

### MSWebViewUnsafeContentWarningDisplaying

Tritt auf, wenn die **WebView** eine Warnungsseite für Inhalte anzeigt, die vom SmartScreen-Filter als unsicher gemeldet wurden.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | **Ereignis** |
|**Synchron** |Ja |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |    

### MSWebViewUnsupportedUriSchemeIdentified

Wird ausgelöst, wenn die Navigation zu einem Uniform Resource Identifier (URI) erfolgt, den die **WebView** nicht unterstützt.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [NavigationEvent](./webview/NavigationEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Ja |     

### MSWebViewUnviewableContentIdentified

Wird ausgelöst, wenn die **WebView** versucht, zu Webinhalten mit einem nicht unterstützten Inhaltstyp zu navigieren. Beispielsweise werden PDF-Dateien zurzeit nicht von WebView unterstützt, und die Navigation zu PDF-Dokumenten wird nicht durch navigiert und stattdessen dieses Ereignis ausgelöst.

```js
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```

#### Ereignisinformationen

|            |      |
|------------|------|
|**Schnittstelle** | [UnviewableContentIdentifiedEvent](./webview/UnviewableContentIdentifiedEvent.md) |
|**Synchron** |Ja  |    
|**Blasen**     |Nein |   
|**Abbrechbar**  |Nein |                 
         

## Methoden

### addWebAllowedObject

Fügt ein systemeigenes Windows-Runtime-Objekt als globalen Parameter zum Dokument auf oberster Ebene innerhalb einer **WebView**hinzu.

Das Objekt wird nicht in das aktuelle Dokument eingefügt, sondern eher auf das nächste Dokument der obersten Ebene, in das die WebView navigiert. Das Objekt wird eingefügt, bevor ein Skript aus dem HTML-Dokument ausgeführt wird, damit Sie sich auf das Objekt im globalen Skript Ihres Dokuments verlassen können.

Sie sollten addWebAllowedObject entweder während eines MSWebViewNavigationStarting-Ereignisses oder vor dem expliziten Aufrufen einer Navigate-Methode verwenden. In diesen Fällen wird das Objekt in das Dokument der entsprechenden Navigation eingefügt. Wenn Sie es in einem anderen Kontext aufrufen, können Sie nicht sicher sein, in welches Dokument Sie Ihr Objekt einfügen möchten.

Wenn Sie addWebAllowedObject mehrmals hintereinander aufrufen, werden mehrere Objekte in das Dokument eingefügt. Wenn Sie beide vor einem expliziten Navigate-Aufruf und dann erneut während des entsprechenden MSWebViewNavigationStarting-Ereignisses aufrufen, sind beide Aufrufe erfolgreich, und es werden mehrere Objekte eingefügt. Wenn Sie mehrere Male mit dem gleichen Namen-Parameter anrufen, werden der letzte Anruf WINS und die vorherigen Anrufe mit diesem Namen ignoriert.

Wenn ein Navigate fehlschlägt oder umgeleitet wird, werden die addWebAllowedObject-Aufrufe für diese Navigation ignoriert. Wenn Sie Umleitungen behandeln möchten, können Sie die MSWebViewNavigationStarting-Ereignisüberwachung für Umleitungen abonnieren und addWebAllowedObject entsprechend den für Ihre Anwendung geeigneten Kriterien wieder aufrufen. Auch wenn ein Dokument alle Objekte, die über addWebAllowedObject für dieses Dokument injiziert wurden, entfernt, wird es nicht zum nächsten Dokument weitergeleitet, und Sie müssen addWebAllowedObject explizit aufrufen, wenn Sie diese übertragen möchten.

Wenn Sie addWebAllowedObject für ein Dokument aufrufen, das ansonsten keinen WinRT-Zugriff hat, oder wenn es [AllowForWebOnly Zugriff über ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) hat, wird das Objekt nur injiziert, wenn das Objekt das Windows. Foundation. Metadata. AllowForWeb-Metadatenattribute-Attribut aufweist. Andernfalls schlägt die Injektion fehl, und ein Fehler wird an die JavaScript-Entwicklerkonsole gemeldet. Wenn Sie für ein Dokument mit voll WinRT Zugriff aufgerufen wird, wird das Objekt unabhängig vom AllowForWeb-Attribut eingefügt. 

Darüber hinaus muss das Objekt die IAgileObject-Schnittstelle implementieren. Dies liegt daran, dass die XAML-und HTML-WebView-Elemente in den AStA-Ansicht-Threads Ihrer app ausgeführt werden und der JavaScript-Thread der WebView ein anderer Asta-Thread ist, und wir möchten App-Entwickler ermutigen, sicherzustellen, dass Ihr Objekt auf dem JavaScript-Thread ausgeführt werden kann, ohne den App-Ansichts Thread nach Möglichkeit zu blockieren

Der Name-Parameter muss ein gültiger JavaScript-Eigenschaftsname sein, da andernfalls der Aufruf automatisch fehlschlägt. Wenn der Name einer Eigenschaft entspricht, die bereits im globalen Objekt vorhanden ist, wird diese Eigenschaft überschrieben, wenn die Eigenschaft konfiguriert werden kann. Nicht konfigurierbare Eigenschaften für das globale Objekt werden nicht überschrieben, und der addWebAllowedObject-Aufruf verfällt automatisch. JavaScript-Eigenschaften, die über addWebAllowedObject erstellt wurden, sind beschreibbar, konfigurierbar und aufzählbar.

```js
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```

#### Parameter
*name*
* Typ: **Zeichenfolge**
* Der Name des Objekts, das für das Dokument in der **WebView**verfügbar gemacht werden soll.

*applicationObject*
* Typ: **Object**
* Das Objekt, das für das Dokument in der **WebView**verfügbar gemacht werden soll.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

#### Zusätzliche Features und Anforderungen

|            |      |
|------------|------|
|**Unterstützte Mindestversion (Client)** |Windows10 [nur Windows Store-Apps] |    
|**Unterstützte Mindestversion (Server)** |Nicht unterstützt |   
|**Unterstützte Mindestversion (Telefon)**  |Nicht unterstützt |  

### buildLocalStreamUri

Erstellt einen URI, den Sie an [navigateToLocalStreamUri](#methods)übergeben können.

```js
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```

#### Parameter
*contentIdentifier*
* Typ: **Zeichenfolge**
* Ein eindeutiger Bezeichner für den Inhalt, auf den der URI verweist. Damit wird der Stamm des URIs definiert.

*relativePath*
* Typ: **Zeichenfolge**
* Der Pfad zur Ressource relativ zum Stamm.

#### Rückgabewert
Typ: **Zeichenfolge**

Der URI, der durch kombinieren und Normalisieren von *contentIdentifier* und *relativePath*erstellt wird.

#### Beispiel

Im folgenden Beispiel wird ein typischer Anwendungsfall veranschaulicht. 

```js
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### capturePreviewToBlobAsync

Erstellt ein Bild des aktuellen [WebView-Elements](./webview.md) und schreibt es in das angegebene Image-Element.

```js
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Geben Sie Folgendes ein: **MSWebViewAsyncOperation**

Ein **MSWebViewAsyncOperation** -Objekt, das nach Abschluss ein **BLOB** -Objekt bereitstellt, das das Bild enthält. Bei Verwendung von **capturePreviewToBlobAsync**müssen Sie nach dem Definieren des Vorgangs Erfolgs-und Fehlerhandler definieren. Nachdem Sie die Ereignishandler angewendet haben, rufen Sie die Start-Methode für das [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) -Objekt auf, um den Vorgang auszuführen.

### captureSelectedContentToDataPackageAsync 

> [!IMPORTANT]
> Diese Methode ist veraltet und hat ein bekanntes Problem. Vermeiden Sie es, diese Methode in Ihrem Produktionscode zu verwenden. 

Ruft asynchron ein [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) ab, das den ausgewählten Inhalt in der **WebView**enthält.

```js
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Geben Sie Folgendes ein: **MSWebViewAsyncOperation**

Ein **MSWebViewAsyncOperation** -Objekt, das nach Abschluss ein [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) -Objekt bereitstellt, das das Bild enthält. Bei Verwendung von **captureSelectedContentToDataPackageAsync**müssen Sie nach dem Definieren des Vorgangs Erfolgs-und Fehlerhandler definieren. Nachdem Sie die Ereignishandler angewendet haben, rufen Sie die Start-Methode für das MSWebViewAsyncOperation-Objekt auf, um den Vorgang auszuführen.

```js
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();  

```

### invokeScriptAsync

Führt als asynchrone Aktion die angegebene Skriptfunktion aus dem aktuell geladenen HTML-Code mit bestimmten Argumenten aus.

```js
webview.invokeScriptAsync(functionName, ...args)
```

#### Parameter

**FunctionName**
* Typ: **Zeichenfolge**
* Der Name der aufzurufenden Funktion. Hierbei handelt es sich um einen Eigenschaftsnamen im globalen Fensterobjekt im Dokument der obersten Ebene von WebView. Dies kann eine integrierte globale Funktion wie eval oder Open sein, oder es kann sich um eine Skript definierte Funktion für das globale Window-Objekt handeln. Es können nur Funktionen im Dokument der obersten Ebene der WebView aufgerufen werden.

**args**
* Typ: **Zeichenfolge**
* Optionale Zeichenfolgenparameter, die an die aufgerufene Funktion übergeben werden sollen. Nach Funktionsname sind alle zusätzlichen Parameter für invokeScriptAsync Zeichenfolgen, die an die aufgerufene Funktion übergeben werden.

#### Rückgabewert
Geben Sie Folgendes ein: **MSWebViewAsyncOperation**

Bei Verwendung von **invokeScriptAsync**müssen Sie nach dem Definieren des Vorgangs Erfolgs-und Fehlerhandler definieren. Nachdem Sie die Ereignishandler angewendet haben, rufen Sie **MSWebViewAsyncOperation. Start** auf, um den Vorgang auszuführen. Wenn das Complete-Ereignis des MSWebViewAsyncOperation ausgelöst wird, ist die Ergebniseigenschaft des MSWebViewAsyncOperation der Zeichenfolgen Rückgabewert aus dem Aufrufen der Funktion. Die Verwendung des Rückgabewerts der aufgerufenen Funktion ermöglicht es dem WebView-Inhalt, synchron zurück zum WebView-Host zu kommunizieren. Wenn die WebView-Inhalte stattdessen asynchron an den WebView-Host weitergeleitet werden sollen, lesen Sie das MSWebViewScriptNotify-Ereignis. Wenn die aufgerufene Funktion eine nicht behandelte Ausnahme auslöst, wird das MSWebViewAsyncOperation-Fehlerereignis ausgelöst. 

```js
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```

### getDeferredPermissionRequests

Gibt eine Liste der verzögerten Berechtigungsanforderungen zurück, die von Inhalten im **WebView** -Steuerelement ausgegeben werden.

```js
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Geben Sie Folgendes ein: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)

Die angegebene verzögerte Berechtigungsanforderung.

#### Zusätzliche Features und Anforderungen

|            |      |
|------------|------|
|**Unterstützte Mindestversion (Client)** |Windows10 [nur Windows Store-Apps] |    
|**Unterstützte Mindestversion (Server)** |Nicht unterstützt|   
|**Unterstützte Mindestversion (Telefon)**  |Nicht unterstützt |    


### getDeferredPermissionRequestById

Gibt die angegebene verzögerte Berechtigungsanforderung zurück. 

```js
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```

#### Parameter
*id*
* Typ: **unsigned long**
* Die ID der verzögerten Berechtigungsanforderung, die Sie abrufen möchten.

#### Rückgabewert
Geben Sie Folgendes ein: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)

Die angegebene verzögerte Berechtigungsanforderung.

#### Zusätzliche Features und Anforderungen

|            |      |
|------------|------|
|**Unterstützte Mindestversion (Client)** |Windows10 [nur Windows Store-Apps] |    
|**Unterstützte Mindestversion (Server)** |Nicht unterstützt|   
|**Unterstützte Mindestversion (Telefon)**  |Nicht unterstützt | 

### GoBack

Navigiert die **WebView** zur vorherigen Seite im Navigationsverlauf. 

```js
webview.goBack();
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

### GoForward

Navigiert die **WebView** zur nächsten Seite im Navigationsverlauf. 

```js
webview.goForward();
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

### Navigieren

Lädt den HTML-Inhalt mit dem angegebenen URI (Uniform Resource Identifier). 

```js
webview.navigate(uri);
```

#### Parameter

**Uri**
* Typ: **Zeichenfolge**
* Der URI, der geladen werden soll.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

### navigateFocus

Navigiert den Fokus auf die **WebView**. Löst das window's-navigatingfocus-Ereignis des WebView-Dokuments auf oberster Ebene aus. Die im navigatingfocus-Ereignis verwendeten FocusNavigationEvent-Argumente entsprechen den Parametern für navigateFocus, mit der Ausnahme, dass die Ursprungs Parameter aus dem Koordinatenraum des Host Dokuments in den Koordinatenbereich des obersten Dokuments der WebView-Ebene übersetzt werden. Weitere Informationen finden Sie unter WebView departingFocus-Ereignis und entsprechende Window. departFocus-Methode zum Übertragen des Fokus vom WebView auf den Host. Ein Beispiel für eine Implementierung der Fokusnavigation über die Tastatur oder das Gamepad, die diese Methode verwendet, finden Sie in der [TVJS-Navigations Bibliothek](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .

```js
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```

#### Parameter
*navigationReason*
* Typ: **Zeichenfolge**
* Der Grund für die Navigation. Der Wert sollte entweder "Left", "up", "Right" oder "Down" sein. Es ist die Richtung, in der sich der Fokus von dem aktuell fokussierten Element entfernt.

*Ursprung*
* Typ: **Object**
* Der Ursprung der Navigation. Hierbei handelt es sich um ein JavaScript-Objekt mit den Eigenschaften "originLeft", "originTop", "originWidth" und "originHeight". Diese Werte sollten die Position und Größe des aktuell fokussierten Elements beschreiben, von dem der Fokus verschoben wird.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

### navigateToLocalStreamUri

Lädt lokalen Webinhalt am angegebenen URI mithilfe eines [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).

```js
webview.navigateToLocalStreamUri(source, streamResolver); 
```

#### Parameter

*Quelle*
* Typ: **Zeichenfolge**
* Ein MS-local-Stream-URI, der den zu ladenden lokalen HTML-Inhalt identifiziert. Erstellen Sie diese Zeichenfolge mithilfe von [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).

*streamResolver*
* Geben Sie Folgendes ein:
* Ein Resolver, der den URI in einen zu ladenden Stream konvertiert.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

### navigateToString

Lädt den angegebenen HTML-Inhalt als neues Dokument. 

```js
webview.navigateToString(contents);
```

#### Parameter

*Inhalt*
* Typ: **Zeichenfolge**
* Der anzuzeigende HTML-Inhalt.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

### navigateWithHttpRequestMessage

Navigiert die WebView zu einem Uniform Resource Identifier (URI) mit einer POST-Anforderung und HTTP-Headern. 

```js
webview.navigateWithHttpRequestMessage(requestMessage);
```

#### Parameter

*RequestMessage*
* Geben Sie Folgendes ein: **HttpRequestMessage**
* Die Details der HTTP-Anforderung. 

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

#### Hinweise

> [!WARNING]
> Wenn Sie dieser Anforderung zusätzliche Kopfzeilen wie Authentifizierungsanmeldeinformationen hinzufügen, denken Sie daran, dass diese Überschriften auch bei nachfolgenden untergeordneten Anforderungen enthalten sind. Verwenden Sie Vorsicht, um eine versehentliche Offenlegung vertraulicher oder personenbezogener Informationen zu verhindern. 


### Aktualisieren 

Lädt den aktuellen Inhalt in der **WebView**erneut. 

```js
webview.refresh();
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.


### stop

Hält die aktuelle **WebView** -Navigation oder den Download an. 

```js
webview.stop();
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.


## Eigenschaften

### canGoBack

Ruft einen Wert ab, der angibt, ob die **WebView** rückwärts navigieren kann.

Diese Eigenschaft ist schreibgeschützt.

```js
var canGoBack = webview.canGoBack;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**

" **True** ", wenn die **WebView** rückwärts navigieren kann; andernfalls **false**.

### canGoForward

Ruft einen Wert ab, der angibt, ob die **WebView** vorwärts navigieren kann.

Diese Eigenschaft ist schreibgeschützt.

```js
var canGoForward = webview.canGoForward;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**

" **True** ", wenn die **WebView** vorwärts navigieren kann; andernfalls **false**.

### containsFullScreenElement

Ruft einen Wert ab, der angibt, ob die **WebView** ein Element enthält, das den Vollbildmodus unterstützt. Weitere Informationen finden Sie im MSWebViewContainsFullScreenElementChanged-Ereignis.

Diese Eigenschaft ist schreibgeschützt.

```js
var containsFullScreenElement = webview.containsFullScreenElement;
```

#### Eigenschaftenwert
Typ: **boolescher Wert**

" **True** ", wenn die **WebView** ein Element enthält, das Vollbild unterstützt; andernfalls **false**.


### documentTitle

Ruft den Titel der Seite ab, die derzeit in der **WebView**angezeigt wird. 

Diese Eigenschaft ist schreibgeschützt.

```js
var documentTitle = webview.documentTitle;
```

#### Eigenschaftenwert
Typ: **Zeichenfolge**

Der Seitentitel

### height

Ruft die Höhe von **WebView**ab oder legt diese fest. 

```js
var height = webview.height;
webview.height = height;

```

#### Eigenschaftenwert
Typ: **Zahl**

Die Höhe von **WebView**. 


### Prozess manipuliert wird.

Ruft den **WebView** -Prozess ab.

Diese Eigenschaft ist schreibgeschützt.

```js
var process = webview.process;
webview.process = process;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: [MSWebViewProcess](./webview/MSWebViewProcess.md)


### settings

Ruft ein [MSWebViewSettings](./webview/MSWebViewSettings.md) -Objekt ab, das Eigenschaften zum Aktivieren oder Deaktivieren von **WebView** -Features enthält.

Diese Eigenschaft ist schreibgeschützt.

```js
var settings = webview.settings;
webview.settings = settings;
```

#### Eigenschaftenwert
Geben Sie Folgendes ein: [MSWebViewSettings](./webview/MSWebViewSettings.md)

Ein [MSWebViewSettings](./webview/MSWebViewSettings.md) -Objekt, das Eigenschaften zum Aktivieren oder Deaktivieren von **WebView** -Features enthält.

### src

Ruft die URI-Quelle (Uniform Resource Identifier) des HTML-Inhalts ab, der im **WebView** -Steuerelement angezeigt werden soll, oder legt diese fest. 

```js
var src = webview.src;
webview.src = src;
```

#### Eigenschaftenwert
Typ: **Zeichenfolge**

Die URI-Quelle des HTML-Inhalts, der im **WebView** -Steuerelement angezeigt werden soll. 


### width

Ruft die Breite von **WebView**ab oder legt diese fest.

```js
var width = webview.width;
webview.width = width;
```

#### Eigenschaftenwert
Typ: **Zahl**

Die Breite von **WebView**.
