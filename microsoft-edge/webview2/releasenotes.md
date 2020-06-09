---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Anmerkungen zu dieser Version von Microsoft Edge WebView2 für Win32, WPF und WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 4a1eb48270e062838fee9223d0a6e0e59505278e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697322"
---
# Anmerkungen zu dieser Version von WebView2 SDK  

Das WebView2-Team wird über eine 6-wöchige Kadenz Updates für das [WebView2-SDK][WebView2NuGetGallery] bereitstellen. Auf dieser Seite können Sie auf dem Laufenden bleiben: Produktankündigungen, Ergänzungen und Änderungen an der API-Oberfläche sowie wichtige Änderungen.

> [!IMPORTANT]
> Kompilieren Sie Ihre APP nach dem Aktualisieren des NuGet-Pakets erneut.

## 0.9.538

[NuGet-Paket][WebView2NuGetGallery0.9.538] | minimale Microsoft Edge-Version 85.0.538.0.

#### Allgemein

* Unterstützung für SDK-Version [0.8.149](#08149)wird gelöscht. Wir empfehlen, über die neueste Version von WebView2 auf dem Laufenden zu bleiben.
* Aktualisierte Gruppenrichtlinie für das Konto, wenn der Profilpfad des Microsoft Edge-Browsers geändert wird ([#179](https://github.com/MicrosoftEdge/WebViewFeedback/issues/179))

#### Win32 C/C++

* [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures](reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures) hinzugefügt, das ausgelöst wird, wenn "Window. Open ()" aufgerufen und zugeordnete [ICoreWebView2ExperimentalWindowFeatures](reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md). ([#70](https://github.com/MicrosoftEdge/WebViewFeedback/issues/70))
* **Aktuelle Änderung:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) wurde als veraltet markiert und durch [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions) ersetzt.
* **Aktuelle Änderung:** Um sicherzustellen, dass unsere API mit den Windows-API-Benennungskonventionen übereinstimmt, haben wir die folgenden Namen aktualisiert:
  * [AreRemoteObjectsAllowed](reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed) ist jetzt [AreHostObjectsAllowed](reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed)
* [AddHostObjectToScript](reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript) aktualisiert, um sicherzustellen, dass die ursprünglichen Hostobjekt-Serialisierungsprogramm-Marker auf die Proxyobjekte gesetzt und als Hostobjekt zurück serialisiert werden, wenn Sie als Parameter im JavaScript-Rückruf übergeben werden. ([#148](https://github.com/MicrosoftEdge/WebViewFeedback/issues/148))

#### .NET

* Freigegebene WinForms-und WPF-WebView2API-Beispiele, die umfassende Leitfäden für unser SDK sind. Schauen Sie sich das [WebView2 Samples Repo](https://github.com/MicrosoftEdge/WebView2Samples)an.
* Unterstützung für visuelles Hosting und Fenster Features, [experimentelle APIs](./concepts/versioning.md#experimental-apis) , hinzugefügt
* **Aktuelle Änderung:** Die folgenden Verzögerungen implementieren nun IDisposable: [ScriptDialogOpening](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening), [mswebviewnewwindowrequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested), [WebResourceRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested)und [PermissionRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested).
* [GetAvailableBrowserVersionString](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring) und [CompareBrowserVersions](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions) werden als [CoreWebView2Environment](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md) -Statik hinzugefügt.

## 0.9.515-Vorabversion

[NuGet-Paket][WebView2NuGetGallery0.9.515-prerelease] | minimale Microsoft Edge-Version 84.0.515.0.

* **Ankündigung:** WebView2 unterstützt jetzt Windows Forms und WPF unter .NET Framework 4.6.2 oder höher und .net Core 3,0 oder höher im **Pre-Release-Paket** .
* Auschecken des [WPF-Einführungsleitfadens](./gettingstarted/wpf.md) für die ersten Schritte beim Erstellen von WPF-Anwendungen und unserem [WPF-Verweis](./reference/wpf/0-9-515-reference-webview2.md) für WPF-spezifische APIs
* Auschecken des [Windows Forms-Einführungsleitfadens für erste](./gettingstarted/winforms.md) Schritte mit dem Erstellen von Windows Forms-Anwendungen und unserer [Windows Forms-Referenz](./reference/winforms/0-9-515-reference-webview2.md) für Windows Forms-spezifische APIs
* Checkout [.net Reference](./reference/dotnet/0-9-515-reference-webview2.md) für CoreWebView2-APIs
* **Bekannte Probleme:** Wir sind uns einiger Probleme in dieser Vorabversion bewusst, die wir in zukünftigen Versionen beheben werden.
  * **Dpi-Erkennung:** WebView2 für WPF ist derzeit nicht mit dpi vertraut. Bei der Initialisierung von WebView2 auf hochdpi-Monitoren gibt es ein bekanntes Problem, bei dem die WebView zunächst als Bruchteil des Fensters initialisiert wird, bis die Größe des Fensters geändert wird.
  * **WPF-Designer:** Diese Version unterstützt derzeit nicht den WPF-Designer. Platzieren Sie das WebView2-Steuerelement in Ihrer APP, indem Sie das entsprechende XAML direkt in einem Text-Editor ändern.

## 0.9.488

[NuGet-Paket][WebView2NuGetGallery0.9.488] | minimale Microsoft Edge-Version 84.0.488.0.

* **Ankündigung:** Beginnend mit der bevorstehenden Microsoft Edge-Version 83 wird Evergreen WebView nicht mehr auf den stabilen Browser Kanal ausgerichtet. Stattdessen wird Sie auf einen anderen Satz von Binärdateien (Branded [Microsoft Edge WebView2 Runtime](./concepts/distribution.md#microsoft-edge-webview2-runtime)) ausgerichtet, die über ein Installationsprogramm, das wir derzeit entwickeln, verkettet werden können. Weitere Informationen finden Sie unter [App-Verteilung](./concepts/distribution.md).
* **Ankündigung:** Wir werden zwei Pakete veröffentlichen: ein Pre-Release-Paket mit experimentellen APIs (das Sie ausprobieren können) und ein stabiles Release-Paket mit stabilen APIs (von dem Sie abhängig sind). Checkout [Microsoft Edge WebView2 SDK](./concepts/versioning.md) , um mehr über die Unterschiede zu erfahren.
* **Aktuelle Änderung:** Um sicherzustellen, dass unsere API mit den Windows-API-Benennungskonventionen übereinstimmt, haben wir die Namen der folgenden Schnittstellen aktualisiert:
  * CORE_WEBVIEW2_ * prefix ist nun COREWEBVIEW2_ *.
  * [GetCoreWebView2BrowserVersionInfo](reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo) ist jetzt [GetAvailableCoreWebView2BrowserVersionString](reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring)
  * [get_BrowserVersionInfo](reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo) ist jetzt [get_BrowserVersionString](reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring)
  * [Addremoteobject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) ist jetzt [AddHostObjectToScript](reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript)
  * [RemoveRemoteObject](reference/win32/0-9-430/icorewebview2.md#removeremoteobject) ist jetzt [RemoveHostObjectFromScript](reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript)
  * Chrome. WebView. remoteObjects ist jetzt Chrome. WebView. hostObjects
* **Aktuelle Änderung:** Die Proxy Methoden für addremoteobject JS wurden ebenfalls umbenannt.
  * getLocal ist jetzt getlocalproperty
  * setlocal ist jetzt setlocalproperty
  * getRemote ist jetzt gethostproperty
  * setremote ist jetzt sethostproperty
  * applyRemote ist jetzt applyHostFunction
* **Aktuelle Änderung:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) ist jetzt veraltet und wurde durch [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions)ersetzt.  
* [FrameNavigationCompleted](reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted) -Ereignis hinzugefügt. Wenn ein IFRAME nun die Navigation beendet, wird ein Ereignis ausgelöst und gibt den Erfolg der Navigation und der Navigations-ID zurück.
* [ICoreWebView2EnvironmentOptions](reference/win32/0-9-488/ICoreWebView2EnvironmentOptions.md) -Schnittstelle hinzugefügt, die verwendet werden kann, um die Version der WebView2-Laufzeit zu ermitteln, auf die die Anwendung ausgerichtet ist.
* [IsBuiltInErrorPageEnabled](reference/win32/0-9-488/ICoreWebView2Settings.md#get_isbuiltinerrorpageenabled) -Einstellung hinzugefügt. Nun können Sie auswählen, ob die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler aktiviert oder deaktiviert werden soll.
* Aktualisierte Remote Objekt Injektion zur Unterstützung von .net IDispatch-Implementierungen. ([#113](https://github.com/MicrosoftEdge/WebViewFeedback/issues/113))
* Das [mswebviewnewwindowrequested](reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested) -Ereignis wurde aktualisiert, um Anforderungen aus Kontextmenüs zu verarbeiten. ([#108](https://github.com/MicrosoftEdge/WebViewFeedback/issues/108))
* Hat unser erstes separates Pre-Release-Paket veröffentlicht, in dem Sie auf visuelle Hosting-APIs zugreifen können. Wir haben [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) aktualisiert, um diese neuen experimentellen APIs einzubeziehen.
  * [ICoreWebView2ExperimentalCompositionController](reference/win32/0-9-488/ICoreWebView2ExperimentalCompositionController.md) -Schnittstelle hinzugefügt, mit der eine Verbindung mit einer Kompositionsstruktur hergestellt und die Eingabe für die WebView bereitgestellt wird.
  * [ICoreWebView2ExperimentalPointerInfo](reference/win32/0-9-488/ICoreWebView2ExperimentalPointerInfo.md) hinzugefügt, das alle Informationen aus einem POINTER_INFO enthält. Sie wird an SendPointerInput übergeben, um zeigereingaben in die WebView einzufügen.
  * [ICoreWebView2ExperimentalCursorChangedEventHandler](reference/win32/0-9-488/ICoreWebView2ExperimentalCursorChangedEventHandler.md) hinzugefügt, das die APP anweist, wenn der Mauszeiger über der WebView geändert werden soll. Wenn sich die Maus über einem Textfeld in der WebView befindet, ändert sich der Cursor vom Pfeil zur Auswahl. Die Cursor-Eigenschaft für das CompositionController teilt der APP mit, was der Mauszeiger aktuell für die WebView sein soll.

## 0.9.430

[NuGet-Paket][WebView2NuGetGallery0.9.430] | minimale Microsoft Edge-Version 82.0.430.0.

Dieses SDK ist unsere offizielle Win32 C++-Beta Version, die verschiedene Funktionsanforderungen enthält, die wir erhalten haben. Wir haben versucht, die Anzahl der Freigaben mit aktuellen Änderungen zu begrenzen, aber während wir uns an unsere allgemeine Verfügbarkeit wenden, verwenden wir unsere Beta Version, um mehrere wichtige Änderungen in einem Schritt zu übernehmen.

* **Aktuelle Änderung:**  Während wir uns an unsere endgültige Version wenden, haben wir das Präfix *IWebView2WebView* zu *ICoreWebView2* umbenannt, um sicherzustellen, dass unsere API an die Windows-API-Benennungskonvention angeglichen wird. Darüber hinaus haben wir ICoreWebView2 in [ICoreWebView2](reference/win32/0-9-430/icorewebview2.md) und [ICoreWebView2Host](reference/win32/0-9-430/icorewebview2host.md)getrennt, um zu ermöglichen, dass unser SDK für die Verwendung durch UI-Frameworks erweiterbar ist. ICoreWebView2Host unterstützt das Ändern der Größe, ein-und ausblenden, die Fokussierung und andere Funktionen in Bezug auf Fenster und Komposition. ICoreWebView2 unterstützt alle anderen WebView2-Funktionen. Wenn Sie mehr über die Einbindung dieser Änderungen erfahren möchten, können Sie unsere [Pull-Anfrage](https://github.com/MicrosoftEdge/WebView2Samples/pull/17) in unserem [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) -Projekt Auschecken.
* **Aktuelle Änderung:** Teilen Sie [DocumentStateChanged](reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged) in drei Komponenten auf: [sourced](reference/win32/0-9-430/icorewebview2.md#add_sourcechanged), [ContentLoading](reference/win32/0-9-430/icorewebview2.md#add_contentloading)und [History](reference/win32/0-9-430/icorewebview2.md#add_historychanged). Wenn die Quell-URL nun geändert wird, wird das Sourcecode-Ereignis ausgelöst. Wenn der Verlaufszustand geändert wird, wird das History-Ereignis ausgelöst. Das ContentLoading-Ereignis wird vor dem anfänglichen Skript ausgelöst, wenn ein neues Dokument geladen wird.
* Unterstützung für ARM64-Architektur hinzugefügt
* Soft Input Panel (SIP)-Unterstützung für Touchscreen-Geräte hinzugefügt
* Unterstützung für `Windows Server 2008 R2` , `Windows Server 2012/2012 R2` und `Windows Server 2016`
* [NotifyParentWindowPositionChanged](reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged) hinzugefügt, der es der Statusleiste ermöglicht, dem Fenster im Fenstermodus zu folgen. Dies muss auch im Fenster freien Modus implementiert werden, damit Barrierefreiheitsfeatures funktionieren.
* [AreRemoteObjectsAllowed](reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed) -Einstellung hinzugefügt, um global zu steuern, ob von Remoteobjekten auf eine Seite zugegriffen werden kann. Standardmäßig ist AreRemoteObjectsAllowed aktiviert, was bedeutet, dass Remoteobjekte, die von [addremoteobject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) hinzugefügt wurden, von der Seite aus zugänglich sind. Wenn AreRemoteObjectsAllowed deaktiviert ist, können auf die Objekte nicht von der Seite aus zugegriffen werden. Änderungen werden beim nächsten Navigations Ereignis übernommen.
* [IsZoomControlEnabled](reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled) -Einstellung wurde hinzugefügt, um zu verhindern, dass Benutzer den Zoom des Webviews mit `ctrl`  +  `+` / `-` oder `ctrl` + Mausrad beeinflussen. Zoom kann weiterhin über [put_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor) festgelegt werden, wenn diese Einstellung deaktiviert ist.  
* ZoomFactor geändert, um nur auf die aktuelle WebView anzuwenden. Zoom Änderungen an der aktuellen WebView wirken sich nicht auf andere Webansichten aus, die sich gerade auf derselben Ursprungssite befinden. Weitere Informationen finden Sie unter [get_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor) .
* HID-zoomview-UI für WebView. ([#95](https://github.com/MicrosoftEdge/WebViewFeedback/issues/95))
* [SetBoundsAndZoomFactor](reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor)hinzugefügt. Nun können Sie den Zoomfaktor und die Begrenzungen eines Webviews gleichzeitig einstellen.
* [WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) -Ereignis hinzugefügt. Weitere Informationen finden Sie unter [add_WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) . ([#119](https://github.com/MicrosoftEdge/WebViewFeedback/issues/119))
* Unterstützung für das Dialogfeld "beforeunload" für JavaScript-Dialogfeldereignisse hinzugefügt und [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD](reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind) Enum-Eintrag hinzugefügt.
* [GetHeaders](reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders) zu HttpRequestHeaders, [GetHeader](reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader) zu HttpResponseHeaders und [get_HasCurrentHeader](reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader) -Eigenschaft zu HttpHeadersCollectionIterator hinzugefügt.
* **Aktuelle Änderung:** Geändertes DevToolsProtocolEventReceived-Verhalten. Nun können Sie einen [DevToolsProtocolEventReceiver](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md) für ein bestimmtes devtools-Protokollereignis erstellen und dieses Ereignis mithilfe [add_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived)remove_DevToolsProtocolEventReceived abonnieren/abbestellen / [remove_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived).
* **Aktuelle Änderung:** WebMessageReceivedEventArgs ' [get_WebMessageAsString](reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring) -Eigenschaft in eine [TryGetWebMessageAsString](reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring) -Methode geändert.
* **Aktuelle Änderung:** Die [handle](reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle) -Methode von AcceleratorKeyPressedEventArgs wurde in eine [get_Handled](reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled) -Eigenschaft geändert.

## 0.8.355

[NuGet-Paket][WebView2NuGetGallery0.8.355] | minimale Microsoft Edge-Version 80.0.355.0.

* Veröffentlichtes WebView2API-Beispiel – ein umfassender Leitfaden für unser SDK. Schauen Sie sich das [hier](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample)an!
* IME-Unterstützung für alle Sprachen außer Englisch wurde hinzugefügt. ([#30](https://github.com/MicrosoftEdge/WebViewFeedback/issues/30))
* Die API-Oberfläche des WebResourceRequested-Ereignisses wurde als Antwort auf Fehlerberichte aktualisiert.  Das gleichzeitige angeben eines Filters und eines Ereignisses bei der Erstellung ist jetzt veraltet.  Zum Erstellen eines angeforderten Webressource-Ereignisses verwenden Sie [add_WebResourceRequested](reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested) , um das Ereignis und [AddWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter) hinzuzufügen, um einen Filter hinzuzufügen.  [RemoveWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter) entfernt den Filter.  ([#36](https://github.com/MicrosoftEdge/WebViewFeedback/issues/36)) ([#74](https://github.com/MicrosoftEdge/WebViewFeedback/issues/74))  
* **Aktuelle Änderung:**  Geändertes Vollbild-Verhalten. Veraltete [IsFullScreenAllowed](reference/win32/0-8-190/IWebView2Settings.md#get_isfullscreenallowed_deprecated).  Wenn ein Element in einer WebView (wie einem Video) nun standardmäßig auf Vollbild eingestellt ist, füllt es die Begrenzungen der WebView-Ansicht aus.  Verwenden Sie das [ContainsFullScreenElementChanged](reference/win32/0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md#interface-iwebview2containsfullscreenelementchangedeventhandler) -Ereignis und [get_ContainsFullScreenElement](reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement) , um anzugeben, wie die APP die Größe der WebView ändern soll, wenn ein Element in den Vollbildmodus wechseln möchte.  

## 0.8.314

[NuGet-Paket][WebView2NuGetGallery0.8.314] | minimale Microsoft Edge-Version 80.0.314.0.

* Unterstützung für Windows 7, Windows 8/8.1 wurde hinzugefügt.
* Visual Studio-und Visual Studio-Code-Debug-Unterstützung für WebView2 hinzugefügt. Nun können Sie Ihr Skript in der WebView2 direkt aus Ihrer IDE Debuggen. Klicken Sie [hier](/microsoft-edge/hosting/webview2#debugging-webview2) , um weitere Informationen zu erhalten.  
* Hinzugefügt `Native Object Injection` , wodurch das in WebView2 ausgeführte Skript ein IDispatch-Objekt aus der Win32-Komponente der Anwendung übergeben und auf die Eigenschaften des IDispatch-Objekts zugreifen kann.  Weitere Informationen finden Sie unter [addremoteobject](reference/win32/0-8-190/iwebview2webview4.md#addremoteobject) .  ([#17](https://github.com/MicrosoftEdge/WebViewFeedback/issues/17)).  
* Ereignis hinzugefügt `AcceleratorKeyPressed` .  Weitere Informationen finden Sie unter [add_AcceleratorKeyPressed](reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed) .  ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Deaktiviert `Context Menus` .  Weitere Informationen finden Sie unter [put_AreDefaultContextMenusEnabled](reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled) ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Aktualisiert `DPI Awareness` . Das dpi-Bewusstsein der WebView-Ansicht ist nun mit der dpi-Erkennung der Hostanwendung identisch. Hinweis: Wenn eine andere Hybridanwendung mit einer anderen dpi-Sensibilisierung als die ursprüngliche WebView gestartet wird, wird die neue WebView nicht gestartet, wenn das Benutzerdatenverzeichnis identisch ist ([#1](https://github.com/MicrosoftEdge/WebViewFeedback/issues/1)).
* Aktualisiert `Notification Change Behavior` , damit WebView2 die Benachrichtigungs Berechtigungsanforderungen, die von Webinhalten, die in der WebView gehostet werden, automatisch ablehnen.

## 0.8.270  

[NuGet-Paket][WebView2NuGetGallery0.8.270] | minimale Microsoft Edge-Version 78.0.270.0.  

* Ereignis hinzugefügt `DocumentTitleChanged` , um die Änderung des Dokumenttitels anzugeben \ ([\ #27][MicrosoftEdgeWebViewFeedbackIssue27]\).  
* API hinzugefügt `GetWebView2BrowserVersionInfo` \ ([\ #18][MicrosoftEdgeWebViewFeedbackIssue18]\).  
* Ereignis hinzugefügt `NewWindowRequested` .  
* `CreateWebView2EnvironmentWithDetails`Zu entfernende zu aktualisierende Funktion `releaseChannelPreference` .  Weitere Informationen finden Sie unter [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] (Funktion).  Die Überschreibung der Registrierungs-und Umgebungsvariablen wird weiterhin unterstützt.  Die Standardkanal Einstellung wird nur verwendet, wenn Sie überschrieben wird.  
    Während der Kanalsuche überspringen wir alle älteren Kanal Versionen, die nicht mit dem WebView2 SDK kompatibel sind.  
    Wir wählen den stabileren Kanal aus, um die konsistentsten Verhaltensweisen für den Endbenutzer zu gewährleisten.  Wenn Sie mit den neuesten Canary-Builds testen, sollten Sie ein Skript erstellen, um die Umgebungsvariable `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` vor dem Starten der App festzulegen.  
* Aktualisierte `CreateWebView2EnvironmentWithDetails` Funktion mit Logik für Auswahl `userDataFolder` , wenn nicht angegeben.  Weitere Informationen finden Sie unter [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] (Funktion).  Wenn Sie zuvor den Standard `userDataFolder` Speicherort verwendet haben, wird beim Wechseln zum neuen SDK der Standardwert `userDataFolder` zurückgesetzt (auf einen neuen Speicherort im Host Codeverzeichnis festgesetzt), und ihr Zustand wird ebenfalls zurückgesetzt.  
    Wenn der Hostprozess nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis verfügt, `CreateWebView2EnvironmentWithDetails` kann ein Fehler auftreten.  Sie können die Daten aus dem alten Benutzerdatenverzeichnis in das neue Verzeichnis kopieren.  

## 0.8.230  

[NuGet-Paket][WebView2NuGetGallery0.8.230] | minimale Microsoft Edge-Version 77.0.230.0.  

* API hinzugefügt `Stop` , um alle Navigations-und ausstehenden Ressourcen Abrufe zu beenden \ ([\ #28][MicrosoftEdgeWebViewFeedbackIssue28]\).  
* TLB-Datei zum Nuget-Paket hinzugefügt \ ([\ #22][MicrosoftEdgeWebViewFeedbackIssue22]\).  
* .Net-Projekte wurden der Installationsliste im NuGet-Paket hinzugefügt \ ([\ #32][MicrosoftEdgeWebViewFeedbackIssue32]\).  

## 0.8.190  

[NuGet-Paket][WebView2NuGetGallery0.8.190] | minimale Microsoft Edge-Version 77.0.190.0.  

* Hinzugefügt `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` , um zu steuern, ob Benutzer devtools \ ([\ #16][MicrosoftEdgeWebViewFeedbackIssue16]\) öffnen können.  
* Hinzugefügt `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` , um zu steuern, ob die Statusleiste angezeigt wird \ ([\ #19][MicrosoftEdgeWebViewFeedbackIssue19]\).  
* Hinzugefügt `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` , um durch den Navigationsverlauf zurückzukehren.  
* Http-Headertypen ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` ) zum Anzeigen und Ändern von HTTP-Headern in WebView hinzugefügt.  
* Unterstützung für 32-Bit-WebView auf 64-Bit-Computern hinzugefügt \ ([\ #13][MicrosoftEdgeWebViewFeedbackIssue13]\).  
* WebView IDL zum SDK hinzugefügt \ ([\ #14][MicrosoftEdgeWebViewFeedbackIssue14]\).  
* Lib zur Unterstützung von IID\_\ *-Schnittstellen Kennungs Objekten hinzugefügt \ ([\ #12][MicrosoftEdgeWebViewFeedbackIssue12]\).  
* Hinzugefügt: Include-Pfad, Verknüpfung und Automatisches Kopieren von DLL-Dateien in NuGet-Ziel Datei im SDK.  
* `window.open`In Skript anfordern aktiviert.  

## 0.8.149  

[NuGet-Paket][WebView2NuGetGallery0.8.149] | minimale Microsoft Edge-Version 76.0.149.0.  

Erste Entwickler-Preview-Version.  

<!-- image links -->

<!-- Links -->
[MicrosoftEdgeWebViewFeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 12"  
[MicrosoftEdgeWebViewFeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 13"  
[MicrosoftEdgeWebViewFeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 14"  
[MicrosoftEdgeWebViewFeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Feedback-Repo für MicrosoftEdge/WebViewFeedback-Problem 16"  
[MicrosoftEdgeWebViewFeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 18"  
[MicrosoftEdgeWebViewFeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Feedback Repo für MicrosoftEdge/WebViewFeedback Ausgabe 19"  
[MicrosoftEdgeWebViewFeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Feedback-Repo für MicrosoftEdge/WebViewFeedback-Problem 22"  
[MicrosoftEdgeWebViewFeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Feedback-Repo für MicrosoftEdge/WebViewFeedback-Problem 27"  
[MicrosoftEdgeWebViewFeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 28"  
[MicrosoftEdgeWebViewFeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 32"  

[WebView2NuGetGallery]: https://aka.ms/webviewnuget "NuGet-Katalog | Microsoft. Web. WebView2"  
[WebView2NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.149"  
[WebView2NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.190"  
[WebView2NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.230"  
[WebView2NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.270"  
[WebView2NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.314"  
[WebView2NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.355"  
[WebView2NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.430"
[WebView2NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.488"
[WebView2NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.515-Vorabversion"
[WebView2NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.538"

[WebViewsGlobalsCreateWebView2EnvironmentWithDetails]: reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "WebView Globals-CreateWebView2EnvironmentWithDetails-Funktion"  
