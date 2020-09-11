---
description: Einbetten von Webtechnologien (HTML, CSS und JavaScript) in ihre systemeigenen Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft. Web. WebView2. Core. CoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, DotNet, WPF, WinForms, APP, Edge, CoreWebView2, CoreWebView2Controller, Browser Control, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2
ms.openlocfilehash: 3a728ad32647a3d74eda7b36b947e335bf4a1e80
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012108"
---
# Microsoft. Web. WebView2. Core. CoreWebView2 Klasse 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

WebView2 ermöglicht Ihnen das Hosten von Webinhalten mithilfe der neuesten Edge-Webbrowser Technologie.

## Zusammenfassung

 Member                        | Beschreibungen
--------------------------------|---------------------------------------------
[BrowserProcessId](#browserprocessid) | Die Prozess-ID des Browser Prozesses, der die WebView hostet.
[CanGoBack](#cangoback) | Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.
[CanGoForward](#cangoforward) | Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.
[ContainsFullScreenElement](#containsfullscreenelement) | Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.
[ContainsFullScreenElementChanged](#containsfullscreenelementchanged) | ContainsFullScreenElementChanged wird ausgelöst, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.
[ContentLoading](#contentloading) | ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden.
[DocumentTitle](#documenttitle) | Der Titel für das aktuelle Dokument der obersten Ebene.
[DocumentTitleChanged](#documenttitlechanged) | DocumentTitleChanged wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.
[FrameNavigationCompleted](#framenavigationcompleted) | FrameNavigationCompleted wird ausgelöst, wenn ein untergeordneter Frame vollständig geladen wurde (Body. OnLoad hat ausgelöst) oder das Laden mit Fehler beendet wurde.
[FrameNavigationStarting](#framenavigationstarting) | FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert.
[History](#historychanged) | Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wird.
[NavigationStarting](#navigationstarting) | NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert.
[Mswebviewnewwindowrequested](#newwindowrequested) | Mswebviewnewwindowrequested wird ausgelöst, wenn der Inhalt in der WebView-Anforderung zum Öffnen eines neuen Fensters, beispielsweisedurch Window. Open, anfordert.
[PermissionRequested](#permissionrequested) | PermissionRequested wird ausgelöst, wenn Inhalt in einer WebView die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.
[ProcessFailed](#processfailed) | ProcessFailed wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.
[ScriptDialogOpening](#scriptdialogopening) | Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung, Eingabeaufforderung oder beforeunload) für die WebView angezeigt wird.
[Einstellungen](#settings) | Das CoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für die Ausführung
[Source](#source) | Der URI des aktuellen Dokuments auf oberster Ebene.
[SourceChanged](#sourcechanged) | Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived wird ausgelöst, wenn die CoreWebView2Settings. IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .
[WebResourceRequested](#webresourcerequested) | WebResourceRequested wird ausgelöst, wenn eine URL-Anforderung (über das Netzwerk, die Datei usw.) in der WebView für einen Ressourcenkontext Filter und eine in AddWebResourceRequestedFilter angegebene URL-URL angefordert wird.
[WebResourceResponseReceived](#webresourceresponsereceived) | Das WebResourceResponseReceived-Ereignis wird ausgelöst, nachdem die WebView die Antwort für eine Webressourcen Anforderung empfangen und verarbeitet hat.
[WindowCloseRequested](#windowcloserequested) | WindowCloseRequested wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close.
[AddHostObjectToScript](#addhostobjecttoscript) | Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.
[AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync) | Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.
[CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync) | Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.
[CapturePreviewAsync](#capturepreviewasync) | Erfassen Sie ein Bild von der Anzeige von WebView.
[ExecuteScriptAsync](#executescriptasync) | Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.
[GoBack](#goback) | Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.
[GoForward](#goforward) | Navigiert die WebView zur nächsten Seite im Navigationsverlauf.
[%%amp;quot;Navigate%%amp;quot;
](#navigate) | Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.
[NavigateToString](#navigatetostring) | Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.
[OpenDevToolsWindow](#opendevtoolswindow) | Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.
[PostWebMessageAsJson](#postwebmessageasjson) | Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.
[Laden](#reload) | Laden Sie die aktuelle Seite neu.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated mit der angegebenen Skript-ID hinzugefügt wurde.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.
[Stop](#stop) | Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

## Member

#### BrowserProcessId 

Die Prozess-ID des Browser Prozesses, der die WebView hostet.

> public uint [BrowserProcessId](#browserprocessid)

#### CanGoBack 

Gibt "true" zurück, wenn die WebView zu einer vorherigen Seite im Navigationsverlauf navigieren kann.

> public bool [CanGoBack](#cangoback)

Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoBack geändert wird.

#### CanGoForward 

Gibt "true" zurück, wenn die WebView zu einer nächsten Seite im Navigationsverlauf navigieren kann.

> public bool [CanGoForward](#cangoforward)

Das History-Ereignis wird ausgelöst, wenn der Wert von CanGoForward geändert wird.

#### ContainsFullScreenElement 

Gibt an, ob die WebView ein HTML-Vollbild-Element enthält.

> public bool [ContainsFullScreenElement](#containsfullscreenelement)

#### ContainsFullScreenElementChanged 

ContainsFullScreenElementChanged wird ausgelöst, wenn sich die ContainsFullScreenElement-Eigenschaft ändert.

> public event EventHandler<-Objekt > [ContainsFullScreenElementChanged](#containsfullscreenelementchanged)

Dies bedeutet, dass ein HTML-Element in der WebView Vollbild auf die Größe des WebView-Elements eingibt oder den Fullscreen-Eintrag verlässt. Dieses Ereignis ist nützlich, wenn beispielsweise ein Video Element den Fullscreen-Modus anfordert. Der Listener von ContainsFullScreenElementChanged kann die WebView-Ansicht dann als Antwort ändern.

#### ContentLoading 

ContentLoading wird ausgelöst, bevor Inhalte geladen werden, einschließlich Skripten, die mit AddScriptToExecuteOnDocumentCreated hinzugefügt wurden.

> public event EventHandler< [CoreWebView2ContentLoadingEventArgs](microsoft-web-webview2-core-corewebview2contentloadingeventargs.md)  >  [ContentLoading](#contentloading)

ContentLoading wird nicht ausgelöst, wenn dieselbe Seitennavigation ausgeführt wird (beispielsweisedurch Fragment-Navigation oder History. pushState-Navigationselemente).

Dies folgt auf das NavigationStarting-Ereignis und das Source-Ereignis und steht vor den Ereignissen "History" und "NavigationCompleted".

#### DocumentTitle 

Der Titel für das aktuelle Dokument der obersten Ebene.

> public String [DocumentTitle](#documenttitle)

Wenn das Dokument keinen expliziten Titel hat oder sonst leer ist, wird ein Standardwert verwendet, der möglicherweise nicht mit dem URI des Dokuments übereinstimmt.

#### DocumentTitleChanged 

DocumentTitleChanged wird ausgelöst, wenn die DocumentTitle-Eigenschaft des WebView-Ereignisses geändert wird und möglicherweise vor oder nach dem NavigationCompleted-Ereignis ausgelöst wird.

> public event EventHandler<-Objekt > [DocumentTitleChanged](#documenttitlechanged)

#### FrameNavigationCompleted 

FrameNavigationCompleted wird ausgelöst, wenn ein untergeordneter Frame vollständig geladen wurde (Body. OnLoad hat ausgelöst) oder das Laden mit Fehler beendet wurde.

> public event EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [FrameNavigationCompleted](#framenavigationcompleted)

#### FrameNavigationStarting 

FrameNavigationStarting wird ausgelöst, wenn ein untergeordneter Frame in der WebView die Berechtigung zum Navigieren zu einem anderen URI anfordert.

> public event EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [FrameNavigationStarting](#framenavigationstarting)

Dies wird auch für Umleitungen ausgelöst. Entsprechende Navigationselemente können blockiert werden, bis der Ereignishandler zurückgegeben wird.

#### History 

Abrechnungshistorieändern hören Sie sich die Änderung des Navigationsverlaufs für das Dokument der obersten Ebene an.

> public event EventHandler<-Objekt > [History](#historychanged)

Verwenden Sie abrechnungshistorieändern, um zu überprüfen, ob sich CanGoBack/CanGoForward-Wert geändert hat. "History" wird auch für die Verwendung von GoBack/GoForward ausgelöst. "History" wird nach "sourcely" und "ContentLoading" ausgelöst.

#### NavigationCompleted 

NavigationCompleted wird ausgelöst, wenn die WebView vollständig geladen wurde (Body. OnLoad wurde ausgelöst) oder das Laden mit einem Fehler beendet wird.

> public event EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [NavigationCompleted](#navigationcompleted)

#### NavigationStarting 

NavigationStarting wird ausgelöst, wenn der WebView-Hauptframe die Berechtigung zum Navigieren zu einem anderen URI anfordert.

> public event EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [NavigationStarting](#navigationstarting)

Dies wird auch für Umleitungen ausgelöst. Entsprechende Navigationselemente können blockiert werden, bis der Ereignishandler zurückgegeben wird.

#### Mswebviewnewwindowrequested 

Mswebviewnewwindowrequested wird ausgelöst, wenn der Inhalt in der WebView-Anforderung zum Öffnen eines neuen Fensters, beispielsweisedurch Window. Open, anfordert.

> public event EventHandler< [CoreWebView2NewWindowRequestedEventArgs](microsoft-web-webview2-core-corewebview2newwindowrequestedeventargs.md)  >  [mswebviewnewwindowrequested](#newwindowrequested)

Die APP kann eine Ziel-WebView übergeben, die als das geöffnete Fenster angesehen wird. Skripts, die im neuen Fenster angefordert wurden, können blockiert werden, bis der Ereignishandler zurückgegeben wird, wenn keine Verzögerung für die Ereignis args übernommen wird. Wenn eine Verzögerung durchgeführt wird, werden Skripts blockiert, bis der Verzögerungs Vorgang abgeschlossen ist.

#### PermissionRequested 

PermissionRequested wird ausgelöst, wenn Inhalt in einer WebView die Berechtigung für den Zugriff auf einige Privilegierte Ressourcen anfordert.

> public event EventHandler< [CoreWebView2PermissionRequestedEventArgs](microsoft-web-webview2-core-corewebview2permissionrequestedeventargs.md)  >  [PermissionRequested](#permissionrequested)

Wenn für die Ereignis-args keine Verzögerung übernommen wird, können die nachfolgenden Skripts blockiert werden, bis der Ereignishandler zurückgegeben wird. Wenn eine Verzögerung durchgeführt wird, werden die Skripts blockiert, bis der Verzögerungs Vorgang abgeschlossen ist.

#### ProcessFailed 

ProcessFailed wird ausgelöst, wenn ein WebView-Prozess unerwartet beendet wird oder nicht mehr reagiert.

> public event EventHandler< [CoreWebView2ProcessFailedEventArgs](microsoft-web-webview2-core-corewebview2processfailedeventargs.md)  >  [ProcessFailed](#processfailed)

#### ScriptDialogOpening 

Das Ereignis wird ausgelöst, wenn ein JavaScript-Dialogfeld (Benachrichtigung, Bestätigung, Eingabeaufforderung oder beforeunload) für die WebView angezeigt wird.

> public event EventHandler< [CoreWebView2ScriptDialogOpeningEventArgs](microsoft-web-webview2-core-corewebview2scriptdialogopeningeventargs.md)  >  [ScriptDialogOpening](#scriptdialogopening)

Dieses Ereignis wird nur ausgelöst, wenn die CoreWebView2Settings. AreDefaultScriptDialogsEnabled-Eigenschaft auf false festgelegt ist. Das ScriptDialogOpening-Ereignis kann verwendet werden, um Dialogfelder zu unterdrücken oder Standarddialogfelder durch benutzerdefinierte Dialogfelder zu ersetzen. Wenn für die Ereignis-args keine Verzögerung übernommen wird, können die nachfolgenden Skripts blockiert werden, bis der Ereignishandler zurückgegeben wird. Wenn eine Verzögerung durchgeführt wird, werden die Skripts blockiert, bis der Verzögerungs Vorgang abgeschlossen ist.

#### Einstellungen 

Das CoreWebView2Settings-Objekt enthält verschiedene änderbare Einstellungen für die Ausführung

> [Einstellungen](#settings) für öffentliche [CoreWebView2Settings](microsoft-web-webview2-core-corewebview2settings.md)

#### Source 

Der URI des aktuellen Dokuments auf oberster Ebene.

> öffentliche Zeichenfolgen [Quelle](#source)

Dieser Wert ändert sich möglicherweise als Teil der Ereignis Befeuerungs Quelle für einige Fälle, beispielsweise das Navigieren zu einer anderen Website oder zu einer anderen Fragment-Navigation. Sie bleibt bei anderen Navigations Typen wie "Seiten-Reload" oder "History. pushState" unverändert, wobei dieselbe URL wie die aktuelle Seite angezeigt wird.

#### SourceChanged 

Die Quelle wird ausgelöst, wenn die Quelleigenschaft geändert wird.

> public event EventHandler< [CoreWebView2SourceChangedEventArgs](microsoft-web-webview2-core-corewebview2sourcechangedeventargs.md)-  >  [Quelle](#sourcechanged)

Die Quelle wird ausgelöst, um zu einer anderen Website oder zu einer anderen Fragment-Navigation zu navigieren. Sie wird nicht für andere Navigationsarten wie "Seiten-Reload" oder "History. pushState" mit der gleichen URL wie die aktuelle Seite ausgelöst. Die Quelle wird vor ContentLoading für die Navigation zu einem neuen Dokument ausgelöst.

#### WebMessageReceived 

WebMessageReceived wird ausgelöst, wenn die CoreWebView2Settings. IsWebMessageEnabled-Einstellung festgelegt ist, und das Dokument auf oberster Ebene des WebView-Anrufs `window.chrome.webview.postMessage` .

> public event EventHandler< [CoreWebView2WebMessageReceivedEventArgs](microsoft-web-webview2-core-corewebview2webmessagereceivedeventargs.md)  >  [WebMessageReceived](#webmessagereceived)

Bei der Funktion PostMessage handelt es sich um `void postMessage(object)` ein Objekt, das von der JSON-Konvertierung unterstützt wird. Wenn PostMessage aufgerufen wird, wird die Invoke-Methode des Handlers aufgerufen, wobei der Objektparameter der PostMessage in eine JSON-Zeichenfolge konvertiert wird.

#### WebResourceRequested 

WebResourceRequested wird ausgelöst, wenn eine URL-Anforderung (über das Netzwerk, die Datei usw.) in der WebView für einen Ressourcenkontext Filter und eine in AddWebResourceRequestedFilter angegebene URL-URL angefordert wird.

> public event EventHandler< [CoreWebView2WebResourceRequestedEventArgs](microsoft-web-webview2-core-corewebview2webresourcerequestedeventargs.md)  >  [WebResourceRequested](#webresourcerequested)

Der Host kann die Anforderung anzeigen und ändern oder eine Antwort in einem ähnlichen Muster wie http bereitstellen, in diesem Fall ist die Anforderung sofort abgeschlossen. Dieser enthält möglicherweise keine Anforderungs Kopfzeilen, die vom Netzwerkstapel hinzugefügt werden, wie Autorisierungs Kopfzeilen. Die angeforderte Webressource kann blockiert werden, bis der Ereignishandler zurückgegeben wird, wenn keine Verzögerung für die Ereignis args übernommen wird. Wenn eine Verzögerung durchgeführt wird, wird die angeforderte Webressource blockiert, bis die Verzögerung abgeschlossen ist.

#### WebResourceResponseReceived 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Das WebResourceResponseReceived-Ereignis wird ausgelöst, nachdem die WebView die Antwort für eine Webressourcen Anforderung empfangen und verarbeitet hat.

> public event EventHandler< [CoreWebView2WebResourceResponseReceivedEventArgs](microsoft-web-webview2-core-corewebview2webresourceresponsereceivedeventargs.md)  >  [WebResourceResponseReceived](#webresourceresponsereceived)

Zu den Ereignis-args gehören die vom WebResourceRequest gesendeten und empfangenen WebResourceResponse, einschließlich aller zusätzlichen Überschriften, die vom Netzwerkstapel hinzugefügt wurden, die nicht als Teil des zugeordneten WebResourceRequested-Ereignisses, wie etwa Authentifizierungs Kopfzeilen, aufgenommen wurden.

#### WindowCloseRequested 

WindowCloseRequested wird ausgelöst, wenn der Inhalt in der WebView zum Schließen des Fensters angefordert wird, beispielsweise nach dem Aufruf von Window. Close.

> public event EventHandler<-Objekt > [WindowCloseRequested](#windowcloserequested)

Die APP sollte das Fenster WebView und verwandte APP schließen, wenn dies für die APP sinnvoll ist.

#### AddHostObjectToScript 

Fügen Sie das bereitgestellte Hostobjekt zu Skript hinzu, das in der WebView mit dem angegebenen Namen ausgeführt wird.

> publicvoid [AddHostObjectToScript](#addhostobjecttoscript)(String Name, Object rawObject)

Hostobjekte werden als Hostobjekt Proxys über `window.chrome.webview.hostObjects.{name}` . Hostobjekt Proxys sind Versprechungen und werden in ein Objekt aufgelöst, das das Hostobjekt darstellt. JavaScript-Code in der WebView kann auf appObject wie folgt zugreifen und dann auf Attribute und Methoden von appObject zugreifen.

Verwenden Sie zum Erstellen einer IDispatch-Implementierungsklasse in C# die folgenden Attribute für jede Klasse, die Sie verfügbar machen möchten. 
```
// Bridge and BridgeAnotherClass are C# classes that implement IDispatch and works with AddRemoteObject.
[ClassInterface(ClassInterfaceType.AutoDual)]
[ComVisible(true)]
public class BridgeAnotherClass
{
    // Sample property.
    public string Prop { get; set; } = "Example";
}

[ClassInterface(ClassInterfaceType.AutoDual)]
[ComVisible(true)]
public class Bridge
{
    public string Func(string param)
    {
        return "Example: " + param;
    }

    public BridgeAnotherClass AnotherObject { get; set; } = new BridgeAnotherClass();

    // Sample indexed property.
    [System.Runtime.CompilerServices.IndexerName("Items")]
    public string this[int index]
    {
        get { return m_dictionary[index]; }
        set { m_dictionary[index] = value; }
    }
    private Dictionary<int, string> m_dictionary = new Dictionary<int, string>();
}
```
 Fügen Sie dann Instanzen dieser Klassen über `AddHostObjectToScript` Folgendes hinzu: 
```
webView.CoreWebView2.AddHostObjectToScript("bridge", new Bridge());
```
 Und dann im Skript können Sie die Methoden aufrufen und auf die Eigenschaften der Objekte zugreifen, die über AddHostObjectToScript hinzugefügt wurden: 
```
// Find added objects on the hostObjects property
const bridge = chrome.webview.hostObjects.bridge;

// Call a method and pass in a parameter.
// The result is another proxy promise so you must await to get the result.
console.log(await bridge.Func("testing..."));

// A property may be another object as long as its class also implements
// IDispatch.
// Getting a property also gets a proxy promise you must await.
const propValue = await bridge.AnotherObject.Prop;
console.log(propValue);

// Indexed properties
let index = 123;
bridge[index] = "test";
let result = await bridge[index];
console.log(result);
```

Beachten Sie, dass einfache Typen, IDispatch und Array unterstützt werden, generische IUnknown, VT_DECIMAL oder VT_RECORD Variant nicht unterstützt werden. Remote-JavaScript-Objekte wie Rückruffunktionen werden als VT_DISPATCH Variante mit dem Object-Implementierungs-IDispatch dargestellt. Die JavaScript-Rückrufmethode kann mit DISPID_VALUE für die DISPID aufgerufen werden. Geschachtelte Arrays werden bis zu einer Tiefe von 3 unterstützt. Arrays von nach Verweistypen werden nicht unterstützt. VT_EMPTY und VT_NULL werden JavaScript als NULL zugeordnet. In JavaScript werden NULL und undefined VT_EMPTY zugeordnet.

Darüber hinaus werden alle Hostobjekte als verfügbar gemacht `window.chrome.webview.hostObjects.sync.{name}` . Hier werden die Hostobjekte als synchrone Hostobjekt Proxys verfügbar gemacht. Hierbei handelt es sich nicht um Versprechungen und Aufrufe von Funktionen oder des Eigenschafts Zugriffs, die ein synchrones Blockieren des ausgeführten Skripts warten, um die Ausführung des Host Codes zu kommunizieren. Dementsprechend kann dies zu Zuverlässigkeitsproblemen führen, und es wird empfohlen, dass Sie die oben beschriebene Versprechen-basierte asynchrone `window.chrome.webview.hostObjects.{name}` API verwenden.

Synchrone Hostobjekt Proxys und asynchrone Hostobjekt Proxys können beide Proxys für dasselbe Hostobjekt bereithalten. Remote Änderungen, die von einem Proxy durchgeführt werden, werden in jedem anderen Proxy desselben Hostobjekts widergespiegelt, unabhängig davon, ob die anderen Proxys synchron oder asynchron sind.

Während JavaScript bei einem synchronen Aufruf von systemeigenem Code blockiert wird, kann dieser systemeigene Code nicht mehr in JavaScript zurückrufen. Der Versuch, dies zu tun, schlägt mit HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK) fehl.

Host Objektproxys sind JavaScript-Proxy Objekte, die alle Eigenschaften abrufen, Eigenschaftensätze und Methodenaufrufe abfangen. Eigenschaften oder Methoden, die Teil des Funktions-oder Objekt Prototyps sind, werden lokal ausgeführt. Darüber hinaus werden alle Eigenschaften oder Methoden im Array `chrome.webview.hostObjects.options.forceLocalProperties` lokal ausgeführt. Diese Option enthält standardmäßig optionale Methoden, die in JavaScript wie und in Bedeutung sind `toJSON` `Symbol.toPrimitive` . Sie können diesem Array nach Bedarf weitere hinzufügen.

Es gibt eine Methode `chrome.webview.hostObjects.cleanupSome` , mit der die Garbage Collection von Hostobjekt Proxys am besten abläuft.

Host Objektproxys verfügen zusätzlich über die folgenden Methoden, die lokal ausgeführt werden:

* applyHostFunction, gethostproperty, sethostproperty: führen Sie einen Methodenaufruf, eine Eigenschaft Get oder einen Eigenschaftssatz für das Hostobjekt aus. Mit diesen können Sie explizit erzwingen, dass eine Methode oder Eigenschaft Remote ausgeführt wird, wenn eine in Konflikt stehende lokale Methode oder Eigenschaft vorhanden ist. Beispielsweise führt `proxy.toString()` die lokale ToString-Methode für das Proxyobjekt aus. `proxy.applyHostFunction('toString')`Wird aber `toString` stattdessen auf dem Host Proxyobjekt ausgeführt.

* getlocalproperty, setlocalproperty: Ausführen von Eigenschaften abrufen oder Eigenschaftssatz lokal. Sie können diese Methoden verwenden, um das Abrufen oder Festlegen einer Eigenschaft für den Hostobjekt Proxy selbst zu erzwingen, anstatt auf das Hostobjekt, das es darstellt. Beispielsweise `proxy.unknownProperty` wird die Eigenschaft abgerufen, die `unknownProperty` aus dem Host Proxyobjekt benannt wurde. `proxy.getLocalProperty('unknownProperty')`Der Wert der Eigenschaft wird jedoch `unknownProperty` für das Proxyobjekt selbst abgerufen.

* Synchronisierung: asynchrone Hostobjekt Proxys machen eine Synchronisierungsmethode verfügbar, die eine Versprechung für einen synchronen Hostobjekt Proxy für dasselbe Hostobjekt zurückgibt. Gibt beispielsweise `chrome.webview.hostObjects.sample.methodCall()` einen asynchronen Hostobjekt Proxy zurück. Stattdessen können Sie die `sync` Methode zum Abrufen eines synchronen Hostobjekt Proxys verwenden: `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* Async: synchrone Hostobjekt Proxys machen eine asynchrone Methode verfügbar, die einen asynchronen Hostobjekt Proxy für dasselbe Hostobjekt blockiert und zurückgibt. Gibt beispielsweise `chrome.webview.hostObjects.sync.sample.methodCall()` einen synchronen Hostobjekt Proxy zurück. Aufruf der `async` Methode für diesen Block und anschließendes zurückgeben eines asynchronen Hostobjekt Proxys für dasselbe Hostobjekt: `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* dann: asynchrone Hostobjekt Proxys verfügen über eine then-Methode. Auf diese Weise können Sie warten. `then` gibt eine Verheißung zurück, die mit einer Darstellung des Hostobjekts aufgelöst wird. Wenn der Proxy ein JavaScript-Literal darstellt, wird eine Kopie davon lokal zurückgegeben. Wenn der Proxy eine Funktion darstellt, wird ein nicht erwarteter Proxy zurückgegeben. Wenn der Proxy ein JavaScript-Objekt mit einer Kombination aus Literalen Eigenschaften und Funktionseigenschaften darstellt, wird eine Kopie des Objekts mit einigen Eigenschaften als Hostobjekt Proxys zurückgegeben.

Alle anderen Eigenschaften-und Methodenaufrufe (außer den oben genannten Methoden für Remote Objektproxy, forceLocalProperties-Liste und Eigenschaften für Funktions-und Objekt Prototypen) werden Remote ausgeführt. Asynchrone Hostobjekt Proxys geben eine Versprechung zurück, die den asynchronen Abschluss des Remoteaufrufs der Methode oder das Abrufen der Eigenschaft darstellt. Das Versprechen wird aufgelöst, nachdem die Remotevorgänge abgeschlossen sind und die Zusagen in den resultierenden Wert des Vorgangs aufgelöst werden. Synchrone Hostobjekt Proxys funktionieren ähnlich, blockieren aber die JavaScript-Ausführung und warten, bis der Remotevorgang abgeschlossen ist.

Das Festlegen einer Eigenschaft für einen asynchronen Hostobjekt Proxy funktioniert etwas anders. Der Satz wird sofort zurückgegeben, und der Rückgabewert ist der Wert, der festgesetzt wird. Dies ist eine Anforderung des JavaScript-Proxy Objekts. Wenn Sie asynchron warten müssen, bis der Eigenschaftssatz abgeschlossen ist, verwenden Sie die sethostproperty-Methode, die eine Verheißung zurückgibt, wie oben beschrieben. Eigenschaft für synchrone Objekteigenschaft festlegen synchron blockiert, bis die Eigenschaft gesetzt ist.

#### AddScriptToExecuteOnDocumentCreatedAsync 

Fügen Sie das bereitgestellte JavaScript einer Liste von Skripts hinzu, die ausgeführt werden sollen, nachdem das globale Objekt erstellt wurde, aber bevor das HTML-Dokument analysiert wurde und bevor ein anderes Skript ausgeführt wird, das vom HTML-Dokument eingeschlossen ist.

> Public Async Task< String > [AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync)(String javaScript)

##### Gibt
Gibt eine Skript-ID zurück, die beim Aufrufen von [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)übergeben werden kann. 

Das eingefügte Skript gilt für alle zukünftigen Dokumente und untergeordneten Frame-Navigationselemente auf oberster Ebene, bis Sie mit RemoveScriptToExecuteOnDocumentCreated entfernt werden. Diese wird asynchron angewendet, und Sie müssen warten, bis der vervollständigungshandler ausgeführt wird, bevor Sie sicher sein können, dass das Skript für zukünftige Navigationen ausgeführt werden kann.

Beachten Sie, dass sich dies auf das hier ausgeführte Skript auswirkt, wenn ein HTML-Dokument über Sandbox [-Eigenschaften oder über den](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [Content-Security-Policy-HTTP-Header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) eine Art Sandbox hat. Wenn also beispielsweise das Schlüsselwort "Allow-modals" nicht festgesetzt ist, werden Aufrufe der `alert` Funktion ignoriert.

#### AddWebResourceRequestedFilter 

Fügt dem WebResourceRequested-Ereignis einen URI-und Ressourcenkontext Filter hinzu.

> publicvoid [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(String URI, CoreWebView2WebResourceContext resourcecontext)

Der URI-Parameter kann eine Platzhalterzeichenfolge (' * ': 0 oder mehr; "?": genau eins) sein. nullptr entspricht L "". Eine Beschreibung der Ressourcenkontext Filter finden Sie unter CoreWebView2WebResourceContext-Enumeration.

#### CallDevToolsProtocolMethodAsync 

Rufen Sie eine asynchrone DevToolsProtocol-Methode auf.

> Public Async Task< String > [CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync)(String MethodName, String parametersAsJson)

##### Gibt
Eine JSON-Zeichenfolge, die das Rückgabeobjekt der Methode darstellt. 

Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) . Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` . Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält. Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird. Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.

#### CapturePreviewAsync 

Erfassen Sie ein Bild von der Anzeige von WebView.

> Public Async Task [CapturePreviewAsync](#capturepreviewasync)(CoreWebView2CapturePreviewImageFormat ImageFormat, Stream ImageStream)

Geben Sie das Format des Bilds mit dem ImageFormat-Parameter an. Die resultierenden Bild Binärdaten werden in den bereitgestellten ImageStream-Parameter geschrieben. Wenn CapturePreview den Schreibvorgang in den Datenstrom abgeschlossen hat, wird die Invoke-Methode für den bereitgestellten Handler-Parameter aufgerufen.

#### ExecuteScriptAsync 

Führen Sie JavaScript-Code aus dem JavaScript-Parameter im aktuellen Dokument der obersten Ebene aus, das in der WebView gerendert wird.

> Public Async Task< String > [ExecuteScriptAsync](#executescriptasync)(String javaScript)

##### Gibt
Gibt eine JSON-codierte Zeichenfolge zurück, die das Ergebnis der Ausführung des bereitgestellten JavaScript darstellt. 

Diese Methode führt das bereitgestellte JavaScript asynchron aus und gibt das Ergebnis des bereitgestellten JavaScript zurück. Wenn das Ergebnis des bereitgestellten Javascripts `undefined` einen Referenz Zyklus enthält oder in JSON nicht codiert werden kann, wird die Zeichenfolge "Null" zurückgegeben. Wenn eine aufgerufene Funktion im bereitgestellten JavaScript keinen expliziten Rückgabewert aufweist, `undefined` wird zurückgegeben. Wenn das bereitgestellte JavaScript eine nicht behandelte Ausnahme auslöst, wird "Null" zurückgegeben. Wenn diese Methode nach einem NavigationStarting-Ereignis aufgerufen wird, wird das bereitgestellte JavaScript beim Laden des neuen Dokuments um die gleiche Zeit ausgeführt, zu der ContentLoading ausgelöst wird. ExecuteScriptAsync wird auch dann funktionieren, wenn CoreWebView2Settings. IsScriptEnabled auf gesetzt ist `FALSE` .

#### GetDevToolsProtocolEventReceiver 

Rufen Sie einen devtools-Protokollereignis Empfänger ab, mit dem Sie ein devtools-Protokollereignis abonnieren können.

> Public CoreWebView2DevToolsProtocolEventReceiver [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(String EventName)

Eine Liste und eine Beschreibung der verfügbaren Methoden finden Sie im [devtools-Protokoll-Viewer](https://aka.ms/DevToolsProtocolDocs) . Der MethodName-Parameter ist der vollständige Name der Methode im Format `{domain}.{method}` . Der parametersAsJson-Parameter ist eine JSON-formatierte Zeichenfolge, die die Parameter für die entsprechende Methode enthält. Die Invoke-Methode des Handlers wird aufgerufen, wenn die Methode asynchron abgeschlossen wird. Invoke wird mit dem Rückgabeobjekt der Methode als JSON-Zeichenfolge aufgerufen.

#### GoBack 

Navigiert die WebView zur vorherigen Seite im Navigationsverlauf.

> publicvoid [GoBack](#goback)()

#### GoForward 

Navigiert die WebView zur nächsten Seite im Navigationsverlauf.

> publicvoid [GoForward](#goforward)()

#### %%amp;quot;Navigate%%amp;quot;
 

Führen Sie eine Navigation des Dokuments auf oberster Ebene zum angegebenen URI.

> public void [Navigate](#navigate)(Zeichenfolgen-URI)

Weitere Informationen finden Sie in den Navigations Ereignissen. Beachten Sie, dass dadurch eine Navigation gestartet wird und das entsprechende NavigationStarting-Ereignis irgendwann ausgelöst wird, nachdem dieser Navigate-Aufruf abgeschlossen ist.

#### NavigateToString 

Initiiert eine Navigation zu htmlContent als HTML-Code für ein neues Dokument.

> publicvoid [NavigateToString](#navigatetostring)(String htmlContent)

Der htmlContent-Parameter darf nicht größer als 2 MB in der Gesamtgröße sein. Der Ursprung der neuen Seite lautet: leer.

#### OpenDevToolsWindow 

Öffnet das devtools-Fenster für das aktuelle Dokument in der WebView.

> publicvoid [OpenDevToolsWindow](#opendevtoolswindow)()

Wenn das devtools-Fenster bereits geöffnet ist, wird Nothing aufgerufen.

#### PostWebMessageAsJson 

Posten Sie die angegebene Webnachricht im Dokument der obersten Ebene in dieser WebView.

> publicvoid [PostWebMessageAsJson](#postwebmessageasjson)(String webMessageAsJson)

Das Nachrichtenereignis des Fensters "Window. Chrome. WebView" des obersten Dokuments wird ausgelöst. JavaScript in diesem Dokument kann das Ereignis über Folgendes abonnieren und kündigen:

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

Das Ereignis args ist eine Instanz von `MessageEvent` . Die CoreWebView2Settings. IsWebMessageEnabled-Einstellung muss true sein, oder diese Methode schlägt mit E_INVALIDARG fehl. Die Dateneigenschaft des Ereignisses arg ist der webmessage-Zeichenfolgenparameter, der als JSON-Zeichenfolge in ein JavaScript-Objekt analysiert wurde. Die Source-Eigenschaft des Ereignisses arg ist ein Verweis auf das `window.chrome.webview` Objekt. Informationen zum Senden von Nachrichten aus dem HTML-Dokument in der WebView an den Host finden Sie unter WebMessageReceived-Ereignis. Diese Nachricht wird asynchron gesendet. Wenn eine Navigation erfolgt, bevor die Nachricht auf der Seite veröffentlicht wird, wird die Nachricht nicht gesendet.

#### PostWebMessageAsString 

Dies ist ein Helfer zum Posten einer Nachricht, bei der es sich um eine einfache Zeichenfolge und nicht um eine JSON-Zeichenfolgendarstellung eines JavaScript-Objekts handelt.

> publicvoid [PostWebMessageAsString](#postwebmessageasstring)(String webMessageAsString)

Dies verhält sich auf die gleiche Weise wie PostWebMessageAsJson, aber die `window.chrome.webview` Dateneigenschaft des Nachrichtenereignisses arg ist eine Zeichenfolge mit dem gleichen Wert wie webMessageAsString. Verwenden Sie diese anstelle von PostWebMessageAsJson, wenn Sie über einfache Zeichenfolgen anstelle von JSON-Objekten kommunizieren möchten.

#### Laden 

Laden Sie die aktuelle Seite neu.

> public void [Reload](#reload)()

Dies ähnelt der Navigation zum URI des aktuellen Dokuments auf oberster Ebene, einschließlich aller Navigationsereignisse, die alle Einträge im HTTP-Cache auslösen und respektieren. Das zurück/weiter-Protokoll wird jedoch nicht geändert.

#### RemoveHostObjectFromScript 

Entfernen Sie das vom Namen angegebene Hostobjekt, damit es nicht mehr über JavaScript-Code in der WebView zugänglich ist.

> publicvoid [RemoveHostObjectFromScript](#removehostobjectfromscript)(String Name)

Während neue Zugriffsversuche verweigert werden, wenn das Objekt bereits durch JavaScript-Code in der WebView abgerufen wird, hat der JavaScript-Code weiterhin Zugriff auf das Objekt. Das Aufrufen dieser Methode für einen Namen, der bereits entfernt oder nie hinzugefügt wird, schlägt fehl.

#### RemoveScriptToExecuteOnDocumentCreated 

Entfernen Sie das entsprechende JavaScript, das über AddScriptToExecuteOnDocumentCreated mit der angegebenen Skript-ID hinzugefügt wurde.

> publicvoid [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(String-ID)

#### RemoveWebResourceRequestedFilter 

Entfernt einen übereinstimmenden Webressourcen Filter, der zuvor für das WebResourceRequested-Ereignis hinzugefügt wurde.

> publicvoid [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(String URI, [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) resourcecontext)

Wenn derselbe Filter mehrmals hinzugefügt wurde, muss er so oft entfernt werden, wie er hinzugefügt wurde, damit er wirksam wird. Gibt E_INVALIDARG für einen Filter zurück, der nie hinzugefügt wurde.

#### Stop 

Beenden Sie alle Navigations-und ausstehenden Ressourcen Abrufe.

> öffentlicher void- [Stopp](#stop)()

Skripts werden nicht angehalten.

