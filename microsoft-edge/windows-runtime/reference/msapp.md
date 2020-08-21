---
title: MSApp-API-Referenz
description: Stellt Hilfsfunktionen bereit, mit deren Hilfe Sie BLOB-und MSStream-Objekte erstellen können.  MSApp-Objekte und-Member werden für Windows-apps mit JavaScript unterstützt.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, Dateiupload, Blog, MSStream, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 4966f6afbe4e971d6a366de7e9b4f5a6cd2305e0
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942168"
---
# MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Das MSApp-Objekt und seine Member werden nur für Windows-Apps unterstützt, die JavaScript verwenden \ (einschließlich PWAs Zugriff auf die Windows-API-Funktionen).  Das MSApp-Objekt ist nur im lokalen Kontext eines HTML-Dokuments in einer Windows-app vorhanden, die über das URI-Schema "MS-AppX" geladen wird. Andernfalls ist das Objekt nicht vorhanden (und daher sind keine seiner Methoden und Eigenschaften verfügbar).  

Sie stellt Hilfsfunktionen bereit, mit deren Hilfe Sie [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) -und [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) -Objekte erstellen können.  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Methoden](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getviewl](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Konstanten](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [aktuell](#current), [groß](#high), [inaktiv](#idle), [Normal](#normal).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [MSAppAsyncOperation-Schnittstelle](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [start](#start)  
   :::column-end:::
:::row-end:::  

## MSApp-Methoden  

### clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Löscht Cache-und indexedDB-Daten für die APP oder [WebView](../../webview.md).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      Diese Methode hat keine Parameter.  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      Geben Sie Folgendes ein: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
      Stellt eine asynchrone Aktion dar.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Erstellt ein [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) aus einem [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) -Objekt.  Diese Methode sollte beim Umgang mit `IRandomAccessStream` Objekten in Apps verwendet werden, um ein W3C-basiertes Objekt aus dem Datenstrom zu erstellen.  Nachdem das BLOB erstellt wurde, kann es mit [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL-APIs](https://developer.mozilla.org/docs/Web/API/URL)und [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)verwendet werden.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `type` in  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Zeichenfolge | Inhaltstyp der Daten.  Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist.  |  
      
      `stream` in  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) , der im BLOB gespeichert werden soll.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | BLOB | Neues BLOB-Objekt, das den Datenstrom enthält.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      | Ausnahme | Bedingung |  
      |:---- |:--- |  
      | TypeMismatchError | Der Knotentyp ist mit dem erwarteten Parametertyp nicht kompatibel.  Bei älteren Versionen als Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.  |  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Erstellt ein BLOB aus Windows-Runtime-Typen über den MSApp-Namespace für das Window-Objekt.  Diese Methode erstellt ein BLOB, das im Wesentlichen ein Licht Wrapper über dem [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) -Objekt ist, das ihm bereitgestellt wird.  Das BLOB besitzt die Lebensdauer dieses Streams, und der Datenstrom wird geschlossen, wenn das BLOB zerstört wird.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackage  

:::row:::
   :::column span="":::
      Wandelt den angegebenen Bereich des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `object` in  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Dieser Bereich kann entweder aus einem Selection-Objekt, beispielsweise: `window.selection.getRangeAt(0)` oder manuell, erstellt werden.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Enthält das HTML-Markup für den angegebenen Bereich.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Diese Methode unterstützt nur den [DOM-Bereich (Document Object Model)](https://developer.mozilla.org/docs/Web/API/Range), nicht [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).  Das zurückgegebene Datenpaket für den angegebenen Bereich enthält HTML-Markup im Zwischenablageformat.  
      
      Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Wandelt die Auswahl des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      Diese Methode hat keine Parameter.  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Enthält das HTML-Markup für den angegebenen Bereich.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Das zurückgegebene Datenpaket für die Auswahl enthält HTML-Markup im Zwischenablageformat.  Wenn keine Benutzerauswahl an einer beliebigen Stelle auf der Benutzeroberfläche der Anwendung vorhanden ist, wird der Wert `createDataPackageFromSelection` zurückgegeben `null` .  
      
      Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### createFileFromStorageFile  

:::row:::
   :::column span="":::
      Konvertiert eine [WinRT](/uwp/api/) - [Speicher](/uwp/api/windows.storage.storagefile) Datei in ein Standard-W3C- [Datei](https://developer.mozilla.org/docs/Web/API/File) Objekt.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `storageFile` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Enthält die Speicherdatei.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**
      
      Keine    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      | Ausnahme | Bedingung |  
      |:---- |:--- |  
      | TypeMismatchError | Der angegebene W3C-Dateiverweis ist ungültig.  Für Versionen, die älter als Internet Explorer 10 sind, `TYPE_MISMATCH_ERR` wird zurückgegeben.  |  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createStreamFromInputStream  

:::row:::
   :::column span="":::
      Erstellt eine [MSStream](https://msdn.microsoft.com/library/hh772328) aus einem [InputStream](https://msdn.microsoft.com/library/hh772327).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `type` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Inhaltstyp der Daten.  Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist.  \ ([Siehe MIME-Typen] (wie,,,,,,,, usw https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` `text/html` `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` . \).  
      
      `inputStream` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Die [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) , die in der gespeichert werden soll `MSStream` .  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Diese Methode verwendet einen Inhaltstyp und den `IInputStream` Verweis.  Die Methode überprüft dann, ob es sich bei dem übergebenen Datenstrom Verweis um eine Instanz von Type handelt `IInputStream` , und wenn dies nicht der Fall ist, wird ausgelöst `DOMException TYPE_MISMATCH_ERR` .  Wenn kein Fehler auftritt, wird `createStreamFromInputStream` ein `MSStream` \ (aus seinen Eingaben \) erstellt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      Eine `IInputStream` kann verwendet werden, um eine zu erstellen `MSStream` .  Da `MSStreams` es sich um eigenständige Objekte mit einmaliger Verwendung handelt, werden alle von Ihnen erstellten URLs `URL.createObjectURL` beim erstmaligen lösen durch das Image-Element aufgehoben.  Darüber hinaus schlägt die Anforderung einer zweiten URL für dieses Objekt, nachdem der Datenstrom verwendet wurde, fehl.  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAsyncAtPriority  

:::row:::
   :::column span="":::
      Plant einen Rückruf, der zu einem späteren Zeitpunkt entsprechend der angegebenen Priorität ausgeführt werden soll.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `asynchronousCallback` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Funktion | Die Rückruffunktion, die asynchron ausgeführt werden soll, wird mit der angegebenen Prioritäts Priorität verteilt.  |  
      
      `priority` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Der kontextbezogene Prioritätswert, in dem der asynchronousCallback-Rückruf ausgeführt wird.  Siehe [MSApp-Konstanten](#msapp-constants).  |  
      
      `args` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |   
      | Any | Eine optionale Reihe von Argumenten, die an die synchronousCallback-Rückruffunktion \ (als Parameter 1 usw. \) übergeben werden.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      Diese Methode gibt keinen Wert zurück.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Die bereitgestellte `asynchronousCallback` Rückruffunktion wird später asynchron ausgeführt.  `asynchronousCallback` wird entsprechend der angegebenen Priorität versandt.  Die normale Priorität entspricht der vorhandenen [setimmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) -Methode.  Wenn der Rückruf ausgeführt wird, wird die aktuelle kontextbezogene Priorität für die Dauer der Ausführung des Rückrufs auf den angegebenen Prioritäts Parameterwert gesetzt.  
      
      Der `asynchronousCallback` Rückrufparameter kann eine beliebige Funktion sein.  Wenn Argumente nach dem Parameter bereitgestellt werden `priority` , werden Sie alle an die Rückruffunktion übergeben.  
      
      Im Gegensatz dazu `execAtPriority` wird jedes von der Rückruffunktion zurückgegebene Objekt `asynchronousCallback` ignoriert \ (und nicht über `execAsyncAtPriority` \) zurückgegeben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAtPriority  

:::row:::
   :::column span="":::
      Führt die angegebene Rückruffunktion unter der angegebenen Kontext Priorität aus.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `synchronousCallback` in  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Funktion | Die Rückruffunktion, die mit der angegebenen Prioritäts Kontext Priorität synchron ausgeführt werden soll.  |  
      
      `priority` in  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Der angegebene Prioritätswert, auf den der aktuelle kontextabhängige Prioritätswert festgelegt wird, wenn die `synchronousCallback` Rückruffunktion ausgeführt wird.  Siehe [MSApp-Konstanten](#msapp-constants).  |  
      
      `args` in  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Eine optionale Reihe von Argumenten, die an die `synchronousCallback` Rückruffunktion \ (als Parameter 1 usw. \) übergeben werden.  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Gibt den Rückgabewert des `synchronousCallback` Rückrufs zurück \ (sofern zutreffend \).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Die bereitgestellte `synchronousCallback` Rückrufmethode wird synchron ausgeführt.  Die aktuelle kontextbezogene Priorität wird für die Dauer der bereitgestellten Rückruffunktion in den angegebenen Prioritätswert (angegeben durch das Prioritäts Argument) geändert.  Sobald die Rückruffunktion die Ausführung beendet hat, wird die Priorität vor dem Aufruf an den vorherigen Wert zurückgegeben `execAtPriority` .  Der Rückgabewert von `execAtPriority` ist der Rückgabewert der Rückrufmethode \ (wie angegeben \).  
      
      Der `synchronousCallback` Rückrufparameter kann eine beliebige Funktion sein.  Wenn nach dem Priority-Parameter Argumente bereitgestellt werden, werden Sie an die bereitgestellte Rückrufmethode übergeben.  Wenn der Rückrufparameter einen Wert zurückgibt, wird dieser Wert ebenfalls zum Rückgabewert `execAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getCurrentPriority  

:::row:::
   :::column span="":::
      Gibt die aktuelle kontextbezogene Priorität zurück.  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Der Rückgabewert ist eine der Zeichenfolgen `MSApp.HIGH` , `MSApp.NORMAL` oder `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Diese Methode gibt die aktuelle kontextbezogene Priorität zurück (siehe [MSApp-Konstanten](#msapp-constants)\), die über und geändert werden kann `execAtPriority` `execAsyncAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getHtmlPrintDocumentSource  

Synchrone API, die als veraltet markiert wurde.  Informationen zu Windows 10 finden Sie unter `getHtmlPrintDocumentSourceAsync` .  Informationen zu Windows 8-und 8,1-apps finden Sie im MSDN-Eintrag für [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync  

:::row:::
   :::column span="":::
      Gibt den Quellinhalt zurück, der gedruckt werden soll.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `htmlDoc` in  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dokument | Das HTML-Dokument, das gedruckt werden soll.  Dies kann das Stammdokument, das Dokument in einem IFRAME, ein Dokument Fragment oder ein SVG-Dokument sein.  Beachten Sie, dass htmlDoc ein Dokument und kein Element sein muss.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel 1**  
      
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
   :::column-end:::
   :::column span="":::
      **Beispiel 2**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
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
   :::column-end:::
:::row-end:::  

### GetView-Nr.  

:::row:::
   :::column span="":::
      Unterstützung für mehrere Fenster.  
      
      > [!NOTE] 
      > In Win 8.1 JavaScript UWP-apps wurden mehrere Fenster unterstützt, die MSApp-DOM-APIs verwenden, die jetzt depricated sind.  Verwenden Sie für Windows 10 `window.open` `window` und das neue `MSApp.getViewId` .  
      
      | Beschreibung |Windows 10 | Windows8.1 |  
      |:---- |:---- |:--- |  
      | Neues Fenster erstellen | [Window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp. createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Neues Fensterobjekt | [Fenster](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `window`
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Ein Objekt, das ein Fenster darstellt, das ein DOM-Dokument enthält.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      `viewId`
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Zahl | Kann mit den verschiedenen [Windows. UI. ViewManagement. ApplicationViewSwitcher-](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs verwendet werden.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Verwenden Sie [Window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) und [Window](https://developer.mozilla.org/docs/Web/API/Window) zum Erstellen neuer Fenster, aber um dann mit WinRT-APIs zu interagieren, fügen Sie die `MSApp.getViewId` API hinzu.  Sie nimmt ein `window` Objekt als Parameter an und gibt eine `viewId` Zahl zurück, die mit den verschiedenen [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) -APIs verwendet werden kann.  
      
      *   Verzögern der Sichtbarkeit  
          
          Ansichten in WinRT werden normalerweise ausgeblendet, und der endentwickler verwendet so etwas wie `TryShowAsStandaloneAsync` , um die Ansicht anzuzeigen, sobald Sie vollständig vorbereitet ist.  In der Web-Welt wird `window.open` sofort ein Fenster angezeigt, und der Endbenutzer kann beobachten, wie Inhalte geladen und gerendert werden.  Damit Ihre neuen Windows-Ansichten in WinRT und nicht sofort angezeigt werden, haben wir eine Option hinzugefügt `window.open` .  Zum Beispiel:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Unterschiede im primären Fenster  
          
          Das primäre Fenster, das zunächst vom Betriebssystem geöffnet wird, fungiert anders als das von ihm geöffnete sekundäre Fenster:  
          
          | Beschreibung | Primär | Sekundärer |  
          |:---- |:--- |:--- |  
          | Window. Open | Zugelassen | Disallowed |  
          | Fenster. Schließen | APP schließen | Fenster schließen |  
          | Navigations Einschränkungen | Nur ACUR | Keine Einschränkungen |  
          
          Die Einschränkung, dass sekundäre Fenster nicht geöffnet werden können, kann sich in Zukunft je nach [Feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)ändern.  
      
      *   Kommunikationseinschränkungen für denselben Ursprung  
          
          Es gibt ein schwieriges technisches Problem, das die korrekte Unterstützung für synchrone, identische Ursprungs-, Fenster-und Skriptaufrufe verhindert.  Wenn Sie ein Fenster öffnen, das denselben Ursprung hat, kann das Skript in einem Fensterfunktionen direkt im anderen Fenster aufrufen, und einige dieser Aufrufe können nicht ausgeführt werden.  `postMessage` Anrufe funktionieren prima und sind die empfohlene Vorgehensweise, wenn es möglich ist.  Arbeiten zur Verbesserung dieses Problems sind in Bearbeitung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Gibt einen booleschen Wert zurück, der angibt, ob die Arbeit auf der angegebenen Prioritätsstufe oder höher aussteht.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `priority` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Ein Prioritätswert \ (siehe [MSApp-Konstanten](#msapp-constants)\), der die Prioritätsstufe und höher angibt, um nach ausstehender in der Warteschlange befindlicher Arbeit zu Fragen.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Boolesch | Gibt zurück `true` , wenn Warteschlangen Arbeit auf der angegebenen Prioritätsstufe oder höher vorhanden ist, `false` andernfalls.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Die `isTaskScheduledAtPriorityOrHigher` Methode bietet eine Möglichkeit für JavaScript-Code, um festzustellen, ob die Arbeit auf den verschiedenen Prioritätsebenen \ (oder darüber \) aussteht, mit der Absicht, dass der aufrufende JavaScript-Code dann beschließen kann, der Arbeit mit höherer Priorität nachzugeben.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Wird verwendet, um eine Aktualisierung des Start Pfads (Seiten neu laden) vor jedem Activate-Ereignis zu vermeiden \ (wie klicken auf eine Benachrichtigung oder auf eine angeheftete Kachel).  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Boolesch | Verwenden Sie `MSApp.pageHandlesAllApplicationActivations(true)` diese Option, um die Aktualisierung des startpfads (Seite neu laden) immer zu überspringen und stattdessen direkt zum Auslösen des Activated-Ereignisses zu springen `WebUIApplication` .  Erfordert, dass alle Seiten Aktivierungsereignisse separat behandeln.  Wenn Sie diese Methode definieren `true` , wird beim Klicken auf ein aktiviertes Ereignis \ (wie eine Benachrichtigung \) das erneute Laden nicht ausgelöst, was ein wesentlicher Faktor für einzelne Seiten-Apps ist, die das erneute Laden von Seiten vermeiden möchten.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Steuert, ob eine APP während des Downloads von Ressourcen mögliche Authentifizierungs Aufforderungen unterdrückt.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
     
      `suppress` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Boolesch | Der Wert true unterdrückt potenzielle Authentifizierungs Aufforderungen.  Der Wert false unterdrückt keine potenziellen Authentifizierungs Aufforderungen des Benutzers.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Die `suppressSubdownloadCredentialPrompts` Methode steuert, ob eine APP potenzielle Authentifizierungs Aufforderungen während des Downloads von Ressourcen unterdrückt.  Das Standardverhalten besteht darin, Anmeldeinformationen nicht zu unterdrücken.  
      
      `suppressSubdownloadCredentialPrompts` ist für die Verwendung durch Apps vorgesehen, die möglicherweise eine übermäßige Anzahl von Ressourcen laden, die eine Authentifizierung erfordern, wie etwa eine e-Mail-App \ (die einen Newsletter mit einer Reihe von Bildern enthalten kann, in denen jedes Bild eine Authentifizierung erfordert \).  
      
      Wenn Sie Anmeldeinformationen unterdrücken, werden Dialogfelder für die Authentifizierung bei Servern beim Zugriff auf Ressourcen, die eine Authentifizierung erfordern, nicht angezeigt, und die Ressource wird nicht heruntergeladen.  Beachten Sie, dass dies `suppressSubdownloadCredentialPrompts` keine Auswirkungen auf andere mögliche Eingabeaufforderungen wie Proxyauthentifizierung oder Client Zertifizierungs Anforderungs Dialogfelder hat und sich auch nicht auf XMLHttpRequest auswirkt.  
      
      Beachten Sie, dass `suppressSubdownloadCredentialPrompts` alle Inhalte in der Anwendung, einschließlich der Inhalte, die im Element gehostet werden, beeinträchtigt werden `webview` .  
      
      > [!IMPORTANT]
      > Entscheidungen für Anmeldeinformationen werden zwischengespeichert.  Daher wird die Unterdrückung von Anmeldeinformationen für Anmeldeinformationen sofort wirksam, sodass die Eingabeaufforderung für Anmeldeinformationen nach dem unterdrücken möglicherweise ein erneutes Laden des Dokuments benötigt, damit es wirksam wird.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### terminateApp  


:::row:::
   :::column span="":::
      Beendet die aktuelle Anwendung und generiert einen Fehlerbericht.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      `error` in
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Fehler | Ein `Error` Objekt, das Sie verwenden können, um den Fehler zu beschreiben, der die Kündigung ausgelöst hat.  Das `Error` Objekt muss die Eigenschaften Number, Description und Stack enthalten; es wird kein Fehlerbericht generiert, wenn das Objekt diese Eigenschaften nicht enthält.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Wenn das gemeldete Problem zu `terminateApp` einem der 5 häufigsten Probleme Ihrer APP wird, wird es auf der Qualitätsseite der App angezeigt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      In diesem Beispiel `terminateApp` wird aufgerufen, wenn eine Ausnahme auftritt.  Sie verwendet das `Error` Objekt, das beim Abfangen einer Ausnahme bereitgestellt wird.  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### MSApp-Konstanten  

:::row:::
   :::column span="":::
      Zulässige Prioritätswerte, die mit `execAsyncAtPriority` , `execAtPriority` , und verknüpft sind `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### Aktuell  
      
      `current`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Bei `current` Verwendung mit der entsprechenden Methode \ (siehe auch Abschnitt \) verwendet die Methode die aktuelle kontextbezogene Priorität, wenn der angeforderte Vorgang ausgeführt wird.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Hoch   
      
      `high`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Wenn `high` mit der entsprechenden Methode \ (siehe auch Abschnitt \) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine höhere Priorität als normal, und die Operation wird vor jeder vorhandenen normalen Priorität ausgeführt.  |  
   :::column-end:::
   :::column span="":::
      #### Leerlauf  
      
      `idle`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Wenn `ideal` mit der entsprechenden Methode \ (siehe auch Abschnitt \) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine niedrigere Priorität als normal, und die Operation wird nach jeder vorhandenen normalen Priorität ausgeführt.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Normal  
      
      `normal`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dom | Wenn die `normal` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die normale vorhandene Priorität.  |  
   :::column-end:::
   :::column span="":::
      **Beispiel**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Anforderungen**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | IDL | MSHTML. idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### start  

:::row:::
   :::column span="":::
      Startet das `MSAppAsyncOperation` .  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameter**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**
      
      Keine  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **Eigenschaften**  
      
      `error` Eigenschaft  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMError | Stellt einen Fehler in dar `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` Eigenschaft  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | EventHandler | Eigenschaft zum Festlegen eines Ereignishandlers nach Abschluss von `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` Eigenschaft  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | EventHandler | Eigenschaft zum Festlegen eines Ereignishandlers bei einem Fehler `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` Eigenschaft  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Zahl | Stellt den Zustand des asynchronen Vorgangs in der Windows-App mit JavaScript dar.  Zu den Werten gehören: `Started[0]` , `Completed[1]` , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` Eigenschaft  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any |Stellt das Ergebnis von dar `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
