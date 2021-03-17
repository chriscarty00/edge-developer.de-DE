---
title: MSApp-API-Referenz
description: Stellt Hilfsfunktionen zur Verfügung, mit denen Sie Blob- und MSStream-Objekte erstellen können.  MSApp-Objekte und -Member werden für Windows-Apps mithilfe von JavaScript unterstützt.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, Dateiupload, Blog, MSStream, Windows 10-Apps, UWP, Edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0607929971b1dd2956571304230f69f756497e32
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439724"
---
# <a name="msapp"></a>MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Das MSApp-Objekt und seine Member werden nur für Windows-Apps unterstützt, die JavaScript \(einschließlich PWAs, die auf Windows-API-Features zugreifen\).  Das #A0 ist nur im lokalen Kontext eines #A1 in einer #A1 vorhanden, die über das ms-appx-URI-Schema geladen wird. Andernfalls ist das Objekt nicht vorhanden (und folglich sind keine seiner Methoden und Eigenschaften verfügbar).  

Es bietet Hilfsfunktionen, mit denen Sie [Blob-](https://developer.mozilla.org/docs/Web/API/Blob) und [MSStream-Objekte erstellen](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) können.  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Methoden](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Konstanten](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [current](#current), [high](#high), [idle](#idle), [normal](#normal).  
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

## <a name="msapp-methods"></a>MSApp-Methoden  

### <a name="cleartemporarywebdataasync"></a>clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Entfernt Cache- und indexierteDB-Daten für die App oder [WebView](../../hosting/webview/index.md).  
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
      
      Diese Methode verfügt über keine Parameter.  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      Typ: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
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

### <a name="createblobfromrandomaccessstream"></a>createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Erstellt ein [Blob](https://developer.mozilla.org/docs/Web/API/Blob) aus einem [IRandomAccessStream-Objekt.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)  Diese Methode sollte beim Umgang mit Objekten in Apps verwendet werden, um ein W3C-basiertes Objekt aus `IRandomAccessStream` dem Datenstrom zu erstellen.  Nachdem das Blob erstellt wurde, kann es mit [den FileReader-,](https://developer.mozilla.org/docs/Web/API/FileReader) [URL-APIs](https://developer.mozilla.org/docs/Web/API/URL)und [XMLHttpRequest verwendet werden.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)  
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
      
      `type` [in]  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Zeichenfolge | Inhaltstyp der Daten.  Diese Zeichenfolge sollte das im Medientyptoken in Abschnitt 3.7 von RFC 2616 definierte Format haben.  |  
      
      `stream` [in]  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | [IRandomAccessStream,](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) das im Blob gespeichert werden soll.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Blob | Neues Blob-Objekt, das den Datenstrom enthält.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      | Ausnahme | Bedingung |  
      |:---- |:--- |  
      | TypeMismatchError | Der Knotentyp ist mit dem erwarteten Parametertyp nicht kompatibel.  Für Versionen vor Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.  |  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Erstellt einen Blob aus Windows-Runtime-Typen über den MSApp-Namespace im Window-Objekt.  Mit dieser Methode wird ein Blob erstellt, das im Wesentlichen ein leichter Wrapper über das [bereitgestellte RandomAccessStream-Objekt](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) ist.  Das Blob besitzt die Lebensdauer dieses Datenstroms, und der Datenstrom wird geschlossen, wenn das Blob zerstört wird.  
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

### <a name="createdatapackage"></a>createDataPackage  

:::row:::
   :::column span="":::
      Konvertiert den angegebenen Bereich des Benutzers oder der Anwendung in ein HTML-Fragment, das freigegeben werden kann.  
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
      
      `object` [in]  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Dieser Bereich kann entweder aus einem Auswahlobjekt erstellt werden, z. B.: `window.selection.getRangeAt(0)` oder manuell.  |  
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
      
      Diese Methode unterstützt nur [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), nicht [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).  Das zurückgegebene Datenpaket für den angegebenen Bereich enthält HTML-Markup im Zwischenablageformat.  
      
      Für das zurückgegebene Datenpaket sind keine Eigenschaften verfügbar.  
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

### <a name="createdatapackagefromselection"></a>createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Konvertiert die Auswahl des Benutzers oder der Anwendung in ein HTML-Fragment, das freigegeben werden kann.  
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
      
      Diese Methode verfügt über keine Parameter.  
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
      
      Das zurückgegebene Datenpaket für die Auswahl enthält HTML-Markup im Zwischenablageformat.  Wenn innerhalb der Benutzeroberfläche der Anwendung keine Benutzerauswahl vorkommt, gibt der `createDataPackageFromSelection` `null` zurück.  
      
      Für das zurückgegebene Datenpaket sind keine Eigenschaften verfügbar.  
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
 
### <a name="createfilefromstoragefile"></a>createFileFromStorageFile  

:::row:::
   :::column span="":::
      Konvertiert ein [WinRT](/uwp/api/) [StorageFile-Objekt](/uwp/api/windows.storage.storagefile) in ein standard W3C [File-Objekt.](https://developer.mozilla.org/docs/Web/API/File)  
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
      
      `storageFile` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Enthält die Speicherdatei.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**
      
      Keiner    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      | Ausnahme | Bedingung |  
      |:---- |:--- |  
      | TypeMismatchError | Der angegebene W3C-Dateiverweis ist ungültig.  Für Versionen vor Internet Explorer 10 wird `TYPE_MISMATCH_ERR` zurückgegeben.  |  
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

### <a name="createstreamfrominputstream"></a>createStreamFromInputStream  

:::row:::
   :::column span="":::
      Erstellt einen [MSStream aus](https://msdn.microsoft.com/library/hh772328) einem [InputStream -Objekt.](https://msdn.microsoft.com/library/hh772327)  
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
      
      `type` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Inhaltstyp der Daten.  Diese Zeichenfolge sollte das im Medientyptoken in Abschnitt 3.7 von RFC 2616 definierte Format haben.  \([Siehe MIME-Typen,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) z. B. `text/plain` , , , , , , , , `text/html` und so `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` weiter\).  
      
      `inputStream` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Der [IInputStream,](/uwp/api/Windows.Storage.Streams.IInputStream) der in gespeichert werden `MSStream` soll.  |  
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
      
      Diese Methode verwendet einen Inhaltstyp und den `IInputStream` Verweis.  Die Methode überprüft dann, ob der übergebene Streamverweis eine Instanz des Typs ist und, falls `IInputStream` nicht, ausgelöst `DOMException TYPE_MISMATCH_ERR` wird.  Wenn kein Fehler auftritt, `createStreamFromInputStream` wird `MSStream` ein \(aus den Eingaben\) erstellt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      Ein `IInputStream` kann zum Erstellen eines verwendet `MSStream` werden.  Wie bei Objekten mit einmaler Verwendung werden alle von erstellten URLs beim ersten Auflösen durch das `MSStreams` `URL.createObjectURL` Image-Element widerrufen.  Darüber hinaus werden Anforderungen für eine zweite URL für dieses Objekt nach der Verwendung des Datenstroms fehlschlagen.  
      
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

### <a name="execasyncatpriority"></a>execAsyncAtPriority  

:::row:::
   :::column span="":::
      Plant einen Rückruf, der zu einem späteren Zeitpunkt gemäß der angegebenen Priorität ausgeführt wird.  
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
      
      `asynchronousCallback` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Funktion | Die Rückruffunktion, die asynchron ausgeführt werden soll, wird mit der angegebenen Prioritätspriorität ausgelöst.  |  
      
      `priority` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Der Kontextprioritätswert, mit dem der asynchroneCallback-Rückruf ausgeführt wird.  Weitere Informationen finden Sie unter [MSApp Constants](#msapp-constants).  |  
      
      `args` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |   
      | Any | Eine optionale Reihe von Argumenten, die an die synchroneCallback-Rückruffunktion \(als Parameter 1 und so weiter\) übergeben werden.  |  
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
      
      Die `asynchronousCallback` bereitgestellte Rückruffunktion wird später asynchron ausgeführt.  `asynchronousCallback` wird entsprechend der angegebenen Priorität versendet.  Die normale Priorität entspricht der vorhandenen [setImmediate-Methode.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)  Wenn der Rückruf ausgeführt wird, wird die aktuelle Kontextpriorität für die Dauer der Ausführung des Rückrufs auf den angegebenen Prioritätsparameterwert festgelegt.  
      
      Der `asynchronousCallback` Callbackparameter kann eine beliebige Funktion sein.  Wenn Argumente nach dem Parameter angegeben werden, werden sie `priority` alle an die Rückruffunktion übergeben.  
      
      Im Gegensatz zu wird jedes von der Rückruffunktion zurückgegebene Objekt `execAtPriority` `asynchronousCallback` ignoriert \(und nicht über `execAsyncAtPriority` \zurückgegeben).  
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

### <a name="execatpriority"></a>execAtPriority  

:::row:::
   :::column span="":::
      Führt die angegebene Rückruffunktion mit der angegebenen Kontextpriorität aus.  
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
      
      `synchronousCallback` [in]  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Funktion | Die Rückruffunktion, die synchron mit der angegebenen Kontextpriorität der Priorität ausgeführt werden soll.  |  
      
      `priority` [in]  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Der angegebene Prioritätswert, auf den der aktuelle Kontextprioritätswert festgelegt wird, wenn die `synchronousCallback` Rückruffunktion ausgeführt wird.  Weitere Informationen finden Sie unter [MSApp Constants](#msapp-constants).  |  
      
      `args` [in]  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Eine optionale Reihe von Argumenten, die an die `synchronousCallback` Rückruffunktion \(als Parameter 1 und so weiter\) übergeben werden.  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any | Gibt den Rückgabewert des `synchronousCallback` Rückrufs \(wie zutreffend\) zurück.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Die `synchronousCallback` bereitgestellte Rückrufmethode wird synchron ausgeführt.  Die aktuelle Kontextpriorität wird für die Dauer der bereitgestellten Rückruffunktion in den angegebenen Prioritätswert (angegeben durch das Prioritätsargument) geändert.  Sobald die Ausführung der Rückruffunktion abgeschlossen ist, wird die Priorität auf den vorherigen Wert vor dem Aufruf `execAtPriority` zurückgegeben.  Der Rückgabewert von `execAtPriority` ist der Rückgabewert der Rückrufmethode \(wie angegeben\).  
      
      Der `synchronousCallback` Callbackparameter kann eine beliebige Funktion sein.  Wenn Argumente nach dem Priority-Parameter angegeben werden, werden sie an die bereitgestellte Rückrufmethode übergeben.  Wenn der Rückrufparameter einen Wert zurückgibt, wird dieser Wert auch zum `execAtPriority` Rückgabewert.  
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

### <a name="getcurrentpriority"></a>getCurrentPriority  

:::row:::
   :::column span="":::
      Gibt die aktuelle Kontextpriorität zurück.  

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
      | DOMString | Der Rückgabewert ist eine der Zeichenfolgen `MSApp.HIGH` , `MSApp.NORMAL` oder `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Diese Methode gibt die aktuelle Kontextpriorität \(siehe [MSApp-Konstanten](#msapp-constants)\) zurück, die über und geändert werden `execAtPriority` `execAsyncAtPriority` kann.  
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

### <a name="gethtmlprintdocumentsource"></a>getHtmlPrintDocumentSource  

Synchrone API, die veraltet ist.  Informationen zu Windows 10 finden Sie unter `getHtmlPrintDocumentSourceAsync` .  Informationen Windows 8 und 8.1-Apps finden Sie im MSDN-Eintrag für [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### <a name="gethtmlprintdocumentsourceasync"></a>getHtmlPrintDocumentSourceAsync  

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
      
      `htmlDoc` [in]  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Dokument | Das zu druckde HTML-Dokument.  Dies kann das Stammdokument, das Dokument in einem iframe, ein Dokumentfragment oder ein SVG-Dokument sein.  Beachten Sie, dass htmlDoc ein Dokument und kein Element sein muss.  |  
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

### <a name="getviewid"></a>getViewId  

:::row:::
   :::column span="":::
      Unterstützung für mehrere Fenster.  
      
      > [!NOTE] 
      > In Win8.1 unterstützten JavaScript-UWP-Apps mehrere Fenster mithilfe von MSApp-DOM-APIs, die nun enteignet sind.  Verwenden Sie für Windows 10 `window.open` , und das neue `window` `MSApp.getViewId` .  
      
      | Beschreibung |Windows 10 | Windows8.1 |  
      |:---- |:---- |:--- |  
      | Erstellen eines neuen Fensters | [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Neues Window-Objekt | [Fenster](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
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
      | DOMString | Ein Objekt, das ein Fenster mit einem DOM-Dokument darstellt.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      `viewId`
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Zahl | Kann mit den verschiedenen [Windows.UI.ViewManagement.ApplicationViewSwitcher-APIs verwendet](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) werden.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Verwenden [Sie window.open](https://developer.mozilla.org/docs/Web/API/Window/open) und [window](https://developer.mozilla.org/docs/Web/API/Window) zum Erstellen neuer Fenster, fügen Sie dann jedoch die API hinzu, um mit WinRT-APIs zu `MSApp.getViewId` interagieren.  Es verwendet ein Objekt als Parameter und gibt eine Zahl zurück, die mit den verschiedenen `window` `viewId` [Windows.UI.ViewManagement.ApplicationViewSwitcher-APIs verwendet werden](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) kann.  
      
      *   Verzögern der Sichtbarkeit  
          
          Ansichten in WinRT beginnen normalerweise ausgeblendet, und der Endentwickler verwendet so etwas wie zum Anzeigen der `TryShowAsStandaloneAsync` Ansicht, sobald sie vollständig vorbereitet ist.  Zeigt in der Webwelt sofort ein Fenster an, und der Endbenutzer kann beobachten, wie Inhalte `window.open` geladen und gerendert werden.  Damit Ihre neuen Fenster wie Ansichten in WinRT agieren und nicht sofort angezeigt werden, haben wir eine Option `window.open` hinzugefügt.  Zum Beispiel:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Primäre Fensterunterschiede  
          
          Das primäre Fenster, das zunächst vom Betriebssystem geöffnet wird, verhält sich anders als die sekundären Fenster, die geöffnet werden:  
          
          | Beschreibung | Primär | Sekundärer |  
          |:---- |:--- |:--- |  
          | window.open | Zugelassen | Disallowed |  
          | window.close | Schließen der App | Fenster schließen |  
          | Navigationseinschränkungen | Nur ACUR | Keine Einschränkungen |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   Kommunikationseinschränkungen für den gleichen Ursprung  
          
          Es gibt ein schwieriges technisches Problem, das die ordnungsgemäße Unterstützung synchroner, identischer, fensterübergreifender Skriptaufrufe verhindert.  Wenn Sie ein Fenster mit demselben Ursprung öffnen, kann skript in einem Fenster direkt Funktionen im anderen Fenster aufrufen, und einige dieser Aufrufe werden fehlschlagen.  `postMessage` Anrufe funktionieren einfach gut, und es wird empfohlen, dies nach Möglichkeit zu tun.  Es werden Arbeiten zur Verbesserung dieses Problems ausgeführt.  
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
    
### <a name="istaskscheduledatpriorityorhigher"></a>isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Gibt einen booleschen Wert zurück, der angibt, ob ausstehende Arbeit auf der angegebenen Prioritätsebene oder höher ist.  
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
      
      `priority` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Ein Prioritätswert \(siehe [MSApp-Konstanten](#msapp-constants)\), der die Prioritätsstufe und höher an gibt, um nach ausstehenden Arbeiten in der Warteschlange zu fragen.  |  
   :::column-end:::
   :::column span="":::
      **Rückgabewert**  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Boolesch | Gibt zurück, wenn Arbeit in der Warteschlange auf der angegebenen Prioritätsebene oder höher `true` liegt, `false` andernfalls.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ausnahmen**  
      
      Keine  
   :::column-end:::
   :::column span="":::
      **Hinweise**  
      
      Die -Methode bietet eine Möglichkeit für JavaScript-Code, um zu bestimmen, ob ausstehende Arbeit auf den verschiedenen Prioritätsebenen \(oder höher\) mit der Absicht, dass der aufrufende JavaScript-Code dann entscheiden kann, arbeit mit höherer Priorität zu `isTaskScheduledAtPriorityOrHigher` ergeben.  
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

### <a name="pagehandlesallapplicationactivations"></a>pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Wird verwendet, um eine Aktualisierung des Startpfads (Seitenladen) vor jedem Aktivierungsereignis \(z. B. klicken auf eine Benachrichtigung oder eine angeheftet Kachel\) zu vermeiden.  
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
      | Boolesch | Verwenden Sie diese Option, um das Aktualisieren des Startpfads (Seitenladen) immer zu überspringen und stattdessen direkt zum Starten `MSApp.pageHandlesAllApplicationActivations(true)` des `WebUIApplication` aktivierten Ereignisses zu springen.  Erfordert, dass alle Seiten Aktivierungsereignisse separat behandeln.  Wenn Sie diese Methode als definieren, löst das Klicken auf ein aktiviertes Ereignis \(wie eine Benachrichtigung\) das Erneute laden nicht aus, was für Apps mit einer einzelnen Seite unerlässlich ist, die Seiten neu laden `true` möchten.  |  
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

### <a name="suppresssubdownloadcredentialprompts"></a>suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Steuert, ob eine App mögliche Authentifizierungsaufforderungen während des Downloads von Ressourcen unterdrückt.  
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
     
      `suppress` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Boolesch | Der Wert true unterdrückt potenzielle Authentifizierungsaufforderungen.  Der Wert false unterdrückt keine potenziellen Authentifizierungsaufforderungen des Benutzers.  |  
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
      
      Die `suppressSubdownloadCredentialPrompts` Methode steuert, ob eine App potenzielle Authentifizierungsaufforderungen während des Downloads von Ressourcen unterdrückt.  Das Standardverhalten besteht im Nicht unterdrücken von Anmeldeinformationsaufforderungen.  
      
      `suppressSubdownloadCredentialPrompts` ist für die Verwendung durch Apps vorgesehen, die eine übermäßig große Anzahl von Ressourcen laden können, die eine Authentifizierung erfordern, z. B. eine E-Mail-App \(die einen Newsletter enthalten kann, der eine Reihe von Bildern enthält, für die für jedes Bild eine Authentifizierung erforderlich ist\).  
      
      Beim Unterdrücken von Anmeldeinformationen werden beim Zugriff auf Ressourcen, die eine Authentifizierung erfordern, keine Dialogfelder für die Authentifizierung auf Servern angezeigt, und die Ressource wird nicht heruntergeladen.  Beachten Sie, dass sich dies weder auf andere mögliche Aufforderungen wie Proxyauthentifizierung oder Clientzertifizierungsanforderungsdialogfelder noch auf `suppressSubdownloadCredentialPrompts` XHR auswirken kann.  
      
      Beachten Sie, `suppressSubdownloadCredentialPrompts` dass sich dies auf alle Inhalte in der Anwendung aus wirkt, einschließlich der inhalte, die im Element gehostet `webview` werden.  
      
      > [!IMPORTANT]
      > Entscheidungen zur Eingabeaufforderung von Anmeldeinformationen werden zwischengespeichert.  Daher wird das Unterdrücken von Anmeldeinformationsaufforderungen sofort wirksam, wenn Anmeldeinformationsaufforderungen nach dem Unterdrücken der Eingabeaufforderungen jedoch möglicherweise ein erneutes Laden des Dokuments wirksam werden müssen.  
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

### <a name="terminateapp"></a>terminateApp  


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
      
      `error` [in]
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Fehler | Ein Objekt, mit dem Sie den Fehler `Error` beschreiben können, der die Beendigung ausgelöst hat.  Das Objekt muss die Zahlen-, Beschreibungs- und Stapeleigenschaften enthalten. Ein Fehlerbericht wird nicht generiert, wenn das Objekt diese Eigenschaften `Error` nicht enthält.  |  
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
      
      Wenn das von gemeldete Problem zu einem der 5 obersten Probleme Ihrer App wird, wird es auf der Seite `terminateApp` Qualität der App angezeigt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Beispiel**  
      
      Dieses Beispiel ruft `terminateApp` auf, wenn eine Ausnahme auftritt.  Es verwendet das `Error` bereitgestellte Objekt, wenn Sie eine Ausnahme abfangen.  
      
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

### <a name="msapp-constants"></a>MSApp-Konstanten  

:::row:::
   :::column span="":::
      Zulässige Prioritätswerte, die `execAsyncAtPriority` mit , , und verknüpft `execAtPriority` `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` sind.  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a>Aktuell  
      
      `current`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Wenn die Methode mit der entsprechenden Methode \(Siehe auch Abschnitt\) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs die aktuelle `current` Kontextpriorität.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a>Hoch   
      
      `high`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Wenn die Methode mit der entsprechenden Methode \(Siehe auch Abschnitt\) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine höhere Priorität als die normale Priorität und löst den Vorgang vor jeder vorhandenen normalen `high` Prioritätsarbeit aus.  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a>Leerlauf  
      
      `idle`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Wenn die Methode mit der entsprechenden Methode \(Siehe auch Abschnitt\) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine niedrigere Priorität als die normale Priorität, und der Vorgang wird nach jeder vorhandenen normalen `ideal` Prioritätsarbeit ausgelöst.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a>Normal  
      
      `normal`  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMString | Wenn die Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die normale vorhandene `normal` Priorität.  |  
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
      | IDL | Mshtml.idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a>MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a>start  

:::row:::
   :::column span="":::
      Startet die `MSAppAsyncOperation` .  
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
      
      `error` property  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | DOMError | Stellt einen Fehler in `MSAppAsyncOperation` dar.  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` property  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | EventHandler | Eigenschaft zum Festlegen eines Ereignishandlers nach Abschluss von `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` property  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | EventHandler | Eigenschaft zum Festlegen eines Ereignishandlers auf einen Fehler während `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` property  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Zahl | Stellt den Status des asynchronen Vorgangs in der Windows-App mithilfe von JavaScript dar.  Werte sind: `Started[0]` , `Completed[1]` , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` property  
      
      | Typ | Beschreibung |  
      |:---- |:--- |  
      | Any |Stellt das Ergebnis von `MSAppAsyncOperation` dar.  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
