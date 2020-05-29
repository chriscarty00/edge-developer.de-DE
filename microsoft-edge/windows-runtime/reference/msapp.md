---
title: MSApp-API-Referenz
description: Stellt Hilfsfunktionen bereit, mit deren Hilfe Sie BLOB-und MSStream-Objekte erstellen können. MSApp-Objekte und-Member werden für Windows-apps mit JavaScript unterstützt.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, Dateiupload, Blog, MSStream, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 0ed8cefa918bd44f3b2c4e8312d2c1d3b4ace8fc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10568720"
---
# MSApp

Das MSApp-Objekt und seine Member werden nur für Windows-Apps unterstützt, die JavaScript verwenden (einschließlich PWAs Zugriff auf Windows-API-Features). Das MSApp-Objekt ist nur im lokalen Kontext eines HTML-Dokuments in einer Windows-app vorhanden, die über das URI-Schema "MS-AppX" geladen wird. Andernfalls ist das Objekt nicht vorhanden (und daher sind keine seiner Methoden und Eigenschaften verfügbar).

Sie stellt Hilfsfunktionen bereit, mit deren Hilfe Sie [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) -und [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) -Objekte erstellen können.

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**Methoden**](#msapp-methods) | [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getviewl](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp). |

| | |
| :--- | :--- |
| [**Konstanten**](#msapp-constants) | [aktuell](#current), [groß](#high), [inaktiv](#idle), [Normal](#normal).|

| | |
| :--- | :--- |
| [**MSAppAsyncOperation** -Schnittstelle](#msappasyncoperation) | [start](#start) |

## MSApp-Methoden

### clearTemporaryWebDataAsync 
Löscht Cache-und indexedDB-Daten für die APP oder [WebView](../../webview.md).

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
Geben[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)

Stellt eine asynchrone Aktion dar.

### createBlobFromRandomAccessStream
Erstellt ein [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) aus einem [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Objekt. Diese Methode sollte beim Umgang mit `IRandomAccessStream` Objekten in Apps verwendet werden, um ein W3C-basiertes Objekt aus dem Datenstrom zu erstellen. Nachdem das BLOB erstellt wurde, kann es mit [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL-APIs](https://developer.mozilla.org/docs/Web/API/URL)und [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)verwendet werden. 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### Parameter

`type` in

|Typ | Beschreibung |
|:---- |:--- |
|Zeichenfolge | Inhaltstyp der Daten. Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist.

`stream` in

|Typ | Beschreibung |
|:---- |:--- |
|Any | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) , der im BLOB gespeichert werden soll.

#### Rückgabewert
|Typ | Beschreibung |
|:---- |:--- |
|BLOB | Neues BLOB-Objekt, das den Datenstrom enthält.

#### Ausnahmen
|Ausnahme | Bedingung |
|:---- |:--- |
|TypeMismatchError | Der Knotentyp ist mit dem erwarteten Parametertyp nicht kompatibel. Bei älteren Versionen als Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.

#### Hinweise
Erstellt ein BLOB aus Windows-Runtime-Typen über den MSApp-Namespace für das Window-Objekt. Diese Methode erstellt ein BLOB, das im Wesentlichen ein Licht Wrapper über dem Objekt ist, das [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) ihm bereitgestellt wird. Das BLOB besitzt die Lebensdauer dieses Streams, und der Datenstrom wird geschlossen, wenn das BLOB zerstört wird. 

#### Beispiel

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### createDataPackage
Wandelt den angegebenen Bereich des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### Parameter
`object` in

|Typ | Beschreibung |
|:---- |:--- |
|Any | Dieser Bereich kann entweder aus einem Selection-Objekt, beispielsweise: `window.selection.getRangeAt(0)` oder manuell, erstellt werden.

#### Rückgabewert
|Typ | Beschreibung |
|:---- |:--- |
|Any | Enthält das HTML-Markup für den angegebenen Bereich.

#### Hinweise
Diese Methode unterstützt nur den [DOM-Bereich (Document Object Model)](https://developer.mozilla.org/docs/Web/API/Range), nicht [TextRange](/uwp/api/windows.ui.xaml.documents.textrange). Das zurückgegebene Datenpaket für den angegebenen Bereich enthält HTML-Markup im Zwischenablageformat.

Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.

### createDataPackageFromSelection 
Wandelt die Auswahl des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### Parameter
Diese Methode hat keine Parameter.

#### Rückgabewert
|Typ | Beschreibung |
|:---- |:--- |
|Any | Enthält das HTML-Markup für den angegebenen Bereich.

#### Hinweise
Das zurückgegebene Datenpaket für die Auswahl enthält HTML-Markup im Zwischenablageformat. Wenn keine Benutzerauswahl an einer beliebigen Stelle auf der Benutzeroberfläche der Anwendung vorhanden ist, wird `createDataPackageFromSelection` NULL zurückgegeben.

Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.
 
### createFileFromStorageFile 
Konvertiert eine [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) in ein Standard [`File`](https://developer.mozilla.org/docs/Web/API/File) -W3C-Objekt.

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### Parameter
`storageFile` in

|Typ | Beschreibung |
|:---- |:--- |
|Any | Enthält die Speicherdatei.

#### Ausnahmen
|Ausnahme | Bedingung |
|:---- |:--- |
|TypeMismatchError | Der angegebene W3C-Dateiverweis ist ungültig. Bei älteren Versionen als Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.

### createStreamFromInputStream  

Erstellt eine [`MSStream`](https://msdn.microsoft.com/library/hh772328) von einer [`InputStream`](https://msdn.microsoft.com/library/hh772327) .  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### Parameter
`type` in

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Inhaltstyp der Daten. Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist. ([Siehe MIME-Typen,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. Text/Plain, Text/HTML, Bild/JPEG, Bild/PNG, Audio/MPEG, Audio/OGG, Audio/*, Video/MP4 usw.). 

`inputStream` in

|Typ | Beschreibung |
|:---- |:--- |
|Any | Die [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) in der gespeichert werden soll `MSStream` .

#### Hinweise
Diese Methode verwendet einen Inhaltstyp und den `IInputStream` Verweis. Die Methode überprüft dann, ob es sich bei dem übergebenen Datenstrom Verweis um eine Instanz von Type handelt `IInputStream` , und wenn dies nicht der Fall ist, wird ausgelöst `DOMException TYPE_MISMATCH_ERR` . Wenn kein Fehler auftritt, wird `createStreamFromInputStream` ein `MSStream` (aus seinen Eingaben) erstellt.

#### Beispiel
Eine `IInputStream` kann verwendet werden, um eine zu erstellen `MSStream` . Da `MSStreams` es sich um eigenständige Objekte mit einmaliger Verwendung handelt, werden alle von Ihnen erstellten URLs `URL.createObjectURL` beim erstmaligen lösen durch das Image-Element aufgehoben. Darüber hinaus schlägt die Anforderung einer zweiten URL für dieses Objekt, nachdem der Datenstrom verwendet wurde, fehl.

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### execAsyncAtPriority 
Plant einen Rückruf, der zu einem späteren Zeitpunkt entsprechend der angegebenen Priorität ausgeführt werden soll. 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### Parameter
`asynchronousCallback` in

|Typ | Beschreibung |
|:---- |:--- |
|Funktion | Die Rückruffunktion, die asynchron ausgeführt werden soll, wird mit der angegebenen Prioritäts Priorität verteilt.

`priority` in

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Der kontextbezogene Prioritätswert, in dem der asynchronousCallback-Rückruf ausgeführt wird. Siehe [MSApp-Konstanten](#msapp-constants).

`args` in

|Typ | Beschreibung |
|:---- |:--- |
|Any | Eine optionale Reihe von Argumenten, die an die synchronousCallback-Rückruffunktion übergeben werden (als Parameter 1 und ein).

#### Rückgabewert
Diese Methode gibt keinen Wert zurück.

#### Hinweise
Die bereitgestellte `asynchronousCallback` Rückruffunktion wird später asynchron ausgeführt. `asynchronousCallback` wird entsprechend der angegebenen Priorität versandt. Die normale Priorität entspricht der vorhandenen [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) Methode. Wenn der Rückruf ausgeführt wird, wird die aktuelle kontextbezogene Priorität für die Dauer der Ausführung des Rückrufs auf den angegebenen Prioritäts Parameterwert gesetzt.

Der `asynchronousCallback` Rückrufparameter kann eine beliebige Funktion sein. Wenn Argumente nach dem Parameter bereitgestellt werden `priority` , werden Sie alle an die Rückruffunktion übergeben.

Im Gegensatz dazu `execAtPriority` wird jedes von der Rückruffunktion zurückgegebene Objekt `asynchronousCallback` ignoriert (und nicht über) zurückgegeben `execAsyncAtPriority` .

### execAtPriority 
Führt die angegebene Rückruffunktion unter der angegebenen Kontext Priorität aus.

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### Parameter
`synchronousCallback` in

|Typ | Beschreibung |
|:---- |:--- |
|Funktion | Die Rückruffunktion, die mit der angegebenen Prioritäts Kontext Priorität synchron ausgeführt werden soll.

`priority` in

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Der angegebene Prioritätswert, auf den der aktuelle kontextabhängige Prioritätswert festgelegt wird, wenn die `synchronousCallback` Rückruffunktion ausgeführt wird. Siehe [MSApp-Konstanten](#msapp-constants).

`args` in

|Typ | Beschreibung |
|:---- |:--- |
|Any | Eine optionale Reihe von Argumenten, die an die `synchronousCallback` Rückruffunktion übergeben werden (als Parameter 1 und ein).

#### Rückgabewert
|Typ | Beschreibung |
|:---- |:--- |
|Any | Gibt den Rückgabewert des `synchronousCallback` Rückrufs (falls zutreffend) zurück.

#### Hinweise
Die bereitgestellte `synchronousCallback` Rückrufmethode wird synchron ausgeführt. Die aktuelle kontextbezogene Priorität wird für die Dauer der bereitgestellten Rückruffunktion in den angegebenen Prioritätswert (angegeben durch das Prioritäts Argument) geändert. Sobald die Rückruffunktion die Ausführung beendet hat, wird die Priorität vor dem Aufruf an den vorherigen Wert zurückgegeben `execAtPriority` . Der Rückgabewert von `execAtPriority` ist der Rückgabewert der Rückrufmethode (wie angegeben).
 
Der `synchronousCallback` Rückrufparameter kann eine beliebige Funktion sein. Wenn nach dem Priority-Parameter Argumente bereitgestellt werden, werden Sie an die bereitgestellte Rückrufmethode übergeben. Wenn der Rückrufparameter einen Wert zurückgibt, wird dieser Wert ebenfalls zum Rückgabewert `execAtPriority` .

#### Beispiel

```javascript
var user = Windows.System.UserProfile.UserInformation;

MSApp.execAtPriority(function () { // This callback executes synchronously.
  user.getFirstNameAsync().then(function () { // Dispatches at high priority.
    return user.getLastNameAsync();
  }).done(function () { // Dispatches at high priority.
    // USEFUL CODE HERE
  });
}, MSApp.HIGH); // The second argument of the execAtPriority method.
```

### getCurrentPriority 
Gibt die aktuelle kontextbezogene Priorität zurück.

```javascript
var retval = MSApp.getCurrentPriority();
```

#### Parameter
Keine 

#### Rückgabewert
|Typ | Beschreibung |
|:---- |:--- |
|Dom | Der Rückgabewert ist eine der Zeichenfolgen `MSApp.HIGH` , `MSApp.NORMAL` oder `MSApp.IDLE` .

#### Hinweise
Diese Methode gibt die aktuelle kontextbezogene Priorität zurück (siehe [`MSApp Constants`](#msapp-constants) ), die über und geändert werden kann `execAtPriority` `execAsyncAtPriority` .

#### Beispiel

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### getHtmlPrintDocumentSource  

Synchrone API, die als veraltet markiert wurde. Informationen zu Windows 10 finden Sie unter `getHtmlPrintDocumentSourceAsync` . Informationen zu Windows 8-und 8,1-apps finden Sie im MSDN-Eintrag für [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync
Gibt den Quellinhalt zurück, der gedruckt werden soll.

#### Parameter
`htmlDoc` in

|Typ | Beschreibung |
|:---- |:--- |
|Dokument | Das HTML-Dokument, das gedruckt werden soll. Dies kann das Stammdokument, das Dokument in einem IFRAME, ein Dokument Fragment oder ein SVG-Dokument sein. Beachten Sie, dass htmlDoc ein Dokument und kein Element sein muss.

#### Beispiel 1

```javascript
var printTask = event.request.createPrintTask(title, function (args) {
                var deferral = args.getDeferral();
                var getPrintDocumentSourceAsync;
                if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                    getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
                } else {
                    getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
                }
                getPrintDocumentSourceAsync.then(function (source) {
                    args.setSource(source);
                    deferral.complete();
                }, function (error) {
                    console.error(error);
                    deferral.complete();
                });
            });
```

#### Beispiel 2

```javascript
    function registerForPrintContract() {
            var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
            printManager.onprinttaskrequested = onPrintTaskRequested;
            console.log("Print Contract registered. Use the Print button to print.", "sample", "status");
    }
    
    // Variable to hold the document source to print
    var gHtmlPrintDocumentSource = null;
    
    // Print event handler for printing via the PrintManager API.
    function onPrintTaskRequested(printEvent) {
        var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
            args.setSource(gHtmlPrintDocumentSource);
    
            // Register the handler for print task completion event
            printTask.oncompleted = onPrintTaskCompleted;
        });
    }
    
    // Print Task event handler is invoked when the print job is completed.
    function onPrintTaskCompleted(printTaskCompletionEvent) {
        // Notify the user about the failure
        if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
            console.log("Failed to print.", "sample", "error");
        }
    }
    
    // Executed just before printing.
    var beforePrint = function () {
        // Replace with code to be executed just before printing the current document:
    };
    
    // Executed immediately after printing.
    var afterPrint = function () {
        // Replace with code to be executed immediately after printing the current document:
    };
    
    function printButtonHandler() {
        // Optionally, functions to be executed immediately before and after printing can be configured as following:
        window.document.body.onbeforeprint = beforePrint;
        window.document.body.onafterprint = afterPrint;
    
        // Get document source to print
        MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
            gHtmlPrintDocumentSource = htmlPrintDocumentSource;
    
            // If the print contract is registered, the print experience is invoked.
            Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
        });
    }
```

### GetView-Nr. 
Unterstützung für mehrere Fenster. 

> [!NOTE] 
> In Win 8.1 JavaScript UWP-apps wurden mehrere Fenster unterstützt, die MSApp-DOM-APIs verwenden, die jetzt depricated sind. Verwenden Sie für Windows 10 `window.open` `window` und das neue `MSApp.getViewId` .

| Beschreibung |Windows 10 | Windows8.1 |  
|:---- |:---- |:--- |  
| Neues Fenster erstellen | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|Neues Fensterobjekt | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### Parameter
`window`

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Ein Objekt, das ein Fenster darstellt, das ein DOM-Dokument enthält. | 

#### Rückgabewert

`viewId`

|Typ | Beschreibung |
|:---- |:--- |
|Zahl | Kann mit den verschiedenen APIs verwendet werden [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) . 

#### Hinweise
Verwenden Sie [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) und [`window`](https://developer.mozilla.org/docs/Web/API/Window) zum Erstellen neuer Fenster, und fügen Sie dann die API hinzu, um mit WinRT-APIs zu interagieren `MSApp.getViewId` . Sie akzeptiert ein `window` Objekt als Parameter und gibt eine `viewId` Zahl zurück, die mit den verschiedenen APIs verwendet werden kann [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) . 

##### Verzögern der Sichtbarkeit 
Ansichten in WinRT werden normalerweise ausgeblendet, und der endentwickler verwendet so etwas wie `TryShowAsStandaloneAsync` , um die Ansicht anzuzeigen, sobald Sie vollständig vorbereitet ist. In der Web-Welt wird `window.open` sofort ein Fenster angezeigt, und der Endbenutzer kann beobachten, wie Inhalte geladen und gerendert werden. Damit Ihre neuen Windows-Ansichten in WinRT und nicht sofort angezeigt werden, haben wir eine Option hinzugefügt `window.open` . Beispiel:
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### Unterschiede im primären Fenster
Das primäre Fenster, das zunächst vom Betriebssystem geöffnet wird, fungiert anders als das von ihm geöffnete sekundäre Fenster: 

|Beschreibung | Primär | Sekundärer |
|:---- |:--- |:--- |
|Window. Open | Zugelassen | Disallowed |
|Fenster. Schließen | APP schließen | Fenster schließen |
| Navigations Einschränkungen | Nur ACUR | Keine Einschränkungen |

Die Einschränkung, dass sekundäre Fenster nicht geöffnet werden können, kann sich in Zukunft je nach [Feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)ändern.

##### Kommunikationseinschränkungen für denselben Ursprung 
Es gibt ein schwieriges technisches Problem, das die korrekte Unterstützung für synchrone, identische Ursprungs-, Fenster-und Skriptaufrufe verhindert. Wenn Sie ein Fenster öffnen, das denselben Ursprung hat, kann das Skript in einem Fensterfunktionen direkt im anderen Fenster aufrufen, und einige dieser Aufrufe können nicht ausgeführt werden. `postMessage` Anrufe funktionieren prima und sind die empfohlene Vorgehensweise, wenn es möglich ist. Arbeiten zur Verbesserung dieses Problems sind in Bearbeitung.


### isTaskScheduledAtPriorityOrHigher 
Gibt einen booleschen Wert zurück, der angibt, ob die Arbeit auf der angegebenen Prioritätsstufe oder höher aussteht.

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### Parameter
`priority` in

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Ein Prioritätswert (siehe [MSApp-Konstanten](#msapp-constants)), der die Prioritätsstufe und höher angibt, um nach ausstehender in der Warteschlange befindlicher Arbeit zu Fragen.

#### Rückgabewert
|Typ | Beschreibung |
|:---- |:--- |
|Boolesch | Gibt zurück `true` , wenn Warteschlangen Arbeit auf der angegebenen Prioritätsstufe oder höher vorhanden ist, `false` andernfalls.

#### Hinweise
Die `isTaskScheduledAtPriorityOrHigher` Methode bietet eine Möglichkeit für JavaScript-Code, um festzustellen, ob die Arbeit auf den verschiedenen Prioritätsebenen (oder höher) aussteht, mit der Absicht, dass sich der aufrufende JavaScript-Code dann entscheiden kann, die Arbeit mit höherer Priorität zu erzielen.

#### Beispiel

```javascript
function performIdleWork(array_in) {
  var idx = 0;

  function performIdleWorkHelper() {
    for (; idx < array_in.length; ++idx) {

      // USEFUL CODE HERE 

      if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
        MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
        break;
      } // if
    } // for
  } // performIdleWorkHelper

  performIdleWorkHelper();
} // performIdleWork
```

### pageHandlesAllApplicationActivations
Wird verwendet, um eine Aktualisierung des Start Pfads (Page Reload) vor jedem Activate-Ereignis (also klicken auf eine Benachrichtigung oder eine angeheftete Kachel) zu vermeiden. 

#### Parameter

|Typ | Beschreibung |
|:---- |:--- |
Boolesch | Verwenden Sie `MSApp.pageHandlesAllApplicationActivations(true)` diese Option, um die Aktualisierung des startpfads (Seite neu laden) immer zu überspringen und stattdessen direkt zum Auslösen des Activated-Ereignisses zu springen `WebUIApplication` . Erfordert, dass alle Seiten Aktivierungsereignisse separat behandeln. Wenn Sie diese Methode definieren `true` , wird durch Klicken auf ein Activated-Ereignis (wie ein Benachrichtigung gesendet) das erneute Laden nicht ausgelöst, was ein wesentlicher Faktor für einzelne Seiten-Apps ist, die das erneute Laden von Seiten vermeiden möchten.

#### Beispiel 

```javascript
// Without this, the app will first refresh to the start path before every activate event
window.MSApp.pageHandlesAllApplicationActivations(true); 

// This must not be deffered so that it can receive the initial `activated` event in time
window.Windows.UI.WebUI.WebUIApplication.addEventListener(
    `activated`,
    e =>
        microsoftInterface.handleActivatedEvent(e);
    }),
    false
);
```

### suppressSubdownloadCredentialPrompts 
Steuert, ob eine APP während des Downloads von Ressourcen mögliche Authentifizierungs Aufforderungen unterdrückt.

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### Parameter
`suppress` in

|Typ | Beschreibung |
|:---- |:--- |
|Boolesch | Der Wert true unterdrückt potenzielle Authentifizierungs Aufforderungen. Der Wert false unterdrückt keine potenziellen Authentifizierungs Aufforderungen des Benutzers.

#### Returan-Wert
Keine

#### Hinweise
Die `suppressSubdownloadCredentialPrompts` Methode steuert, ob eine APP potenzielle Authentifizierungs Aufforderungen während des Downloads von Ressourcen unterdrückt. Das Standardverhalten besteht darin, Anmeldeinformationen nicht zu unterdrücken.

`suppressSubdownloadCredentialPrompts` ist für die Verwendung durch Apps vorgesehen, die eine übermäßige Anzahl von Ressourcen laden können, die eine Authentifizierung erfordern, beispielsweise eine Mail-app (die einen Newsletter mit einer Reihe von Bildern enthalten kann, bei denen für jedes Bild eine Authentifizierung erforderlich ist).

Wenn Sie Anmeldeinformationen unterdrücken, werden Dialogfelder für die Authentifizierung bei Servern beim Zugriff auf Ressourcen, die eine Authentifizierung erfordern, nicht angezeigt, und die Ressource wird nicht heruntergeladen. Beachten Sie, dass dies `suppressSubdownloadCredentialPrompts` keine Auswirkungen auf andere mögliche Eingabeaufforderungen wie Proxyauthentifizierung oder Client Zertifizierungs Anforderungs Dialogfelder hat und sich auch nicht auf XMLHttpRequest auswirkt.

Beachten Sie, dass `suppressSubdownloadCredentialPrompts` alle Inhalte in der Anwendung, einschließlich der Inhalte, die im Element gehostet werden, beeinträchtigt werden `webview` .
 
**Wichtig:**  Entscheidungen für Anmeldeinformationen werden zwischengespeichert. Daher wird die Unterdrückung von Anmeldeinformationen für Anmeldeinformationen sofort wirksam, sodass die Eingabeaufforderung für Anmeldeinformationen nach dem unterdrücken möglicherweise ein erneutes Laden des Dokuments benötigt, damit es wirksam wird.

#### Beispiel

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### terminateApp
Beendet die aktuelle Anwendung und generiert einen Fehlerbericht. 

```javascript
MSApp.terminateApp(error); 
```

#### Parameter
`error` in

Typ | Beschreibung |
|:---- |:--- |
|Fehler | Ein `Error` Objekt, das Sie verwenden können, um den Fehler zu beschreiben, der die Kündigung ausgelöst hat. Das `Error` Objekt muss die Eigenschaften Number, Description und Stack enthalten; es wird kein Fehlerbericht generiert, wenn das Objekt diese Eigenschaften nicht enthält.

#### Rückgabewert
Keine

#### Hinweise
Wenn das gemeldete Problem zu `terminateApp` einem der 5 häufigsten Probleme Ihrer APP wird, wird es auf der Qualitätsseite der App angezeigt.

#### Beispiel
In diesem Beispiel `terminateApp` wird aufgerufen, wenn eine Ausnahme auftritt. Sie verwendet das `Error` Objekt, das beim Abfangen einer Ausnahme bereitgestellt wird. 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### MSApp-Konstanten
Zulässige Prioritätswerte, die mit `execAsyncAtPriority` , `execAtPriority` , und verknüpft sind `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .

#### Aktuell
`current`

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Wenn die `current` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die aktuelle kontextbezogene Priorität.

#### Hoch 
`high`

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Wenn die `high` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs eine höhere Priorität als normal, und die Operation wird vor jeder vorhandenen normalen Priorität ausgeführt.

#### Leerlauf
`idle`

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Wenn `ideal` mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs eine niedrigere Priorität als normal, und die Operation wird nach jeder vorhandenen normalen Priorität ausgeführt.

#### Normal
`normal`

|Typ | Beschreibung |
|:---- |:--- |
|Dom | Wenn die `normal` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die normale vorhandene Priorität.

#### Beispiel

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### Anforderungen
|IDL | MSHTML. idl |
|:---- |:--- |

## MSAppAsyncOperation

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### start
Startet das `MSAppAsyncOperation` .

```javascript
var retval = MSAppAsyncOperation.start();
```

#### Parameter
Keine

#### Rückgabewert
Keine

#### Eigenschaften
`error` Eigenschaft

|Typ | Beschreibung |
|:---- |:--- |
|DOMError | Stellt einen Fehler in dar `MSAppAsyncOperation` .

```javascript
p = object.error
```

`oncomplete` Eigenschaft

|Typ | Beschreibung |
|:---- |:--- |
|EventHandler | Eigenschaft zum Festlegen eines Ereignishandlers nach Abschluss von `MSAppAsyncOperation` .

```javascript
p = object.oncomplete
```

`onerror` Eigenschaft

|Typ | Beschreibung |
|:---- |:--- |
|EventHandler | Eigenschaft zum Festlegen eines Ereignishandlers bei einem Fehler `MSAppAsyncOperation` .

```javascript
p = object.onerror
```

`readyState` Eigenschaft

|Typ | Beschreibung |
|:---- |:--- |
|Zahl | Stellt den Zustand des asynchronen Vorgangs in der Windows-App mit JavaScript dar. Zu den Werten zählen: gestartet [0], abgeschlossen [1], Fehler [2].

```javascript
p = object.readyState
```

`result` Eigenschaft

|Typ | Beschreibung |
|:---- |:--- |
|Any |Stellt das Ergebnis von dar `MSAppAsyncOperation` .

```javascript
p = object.result
```
