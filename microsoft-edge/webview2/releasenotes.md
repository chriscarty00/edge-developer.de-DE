---
description: Anmerkungen zu dieser Version von Microsoft Edge WebView2 SDK
title: Anmerkungen zu dieser Version von Microsoft Edge WebView2 für Win32, WPF und WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 33b8280347d425eb1a02c1703a845ca31d4b314a
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052121"
---
# Anmerkungen zu dieser Version von WebView2 SDK  

Das WebView2-Team liefert Updates für das [WebView2-SDK][NuGetGallery] in einer sechswöchigen Kadenz.  Überprüfen Sie die folgenden Inhalte auf aktuelle Informationen zu Produktankündigungen, Ergänzungen und Änderungen an der API-Oberfläche sowie zu unterbrechenden Änderungen.  

> [!NOTE]
> Kompilieren Sie Ihre APP nach dem Aktualisieren des NuGet-Pakets erneut.  

> [!IMPORTANT]
> Während WebView2 eine Vorschau ist, befinden sich die .NET-APIs in der `prerelease package` .  

## 0.9.628-Vorabversion  

Veröffentlichungsdatum: 10. September, 2020  

[NuGet-Paket][NuGetGallery0.9.628-prerelease] \ | minimale Microsoft Edge-Version 87.0.628.0.  

> [!IMPORTANT]
> **Ankündigung**: Diese Vorabversion wird weiterhin basierend auf dem Microsoft Edge 87-Zweig veröffentlicht.  In Zukunft entspricht die Vorabversion des SDK-Release dem Microsoft Edge Canary Build, und die normale Version wird mit Microsoft Edge stable synchronisiert.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: Visual Hosting-APIs sind jetzt unter Vorschau.  WebView2 verwendet visuelles Hosting, um neben WinComp/DComp-visuellen Objekten im Gegensatz zu HWNDs zu laufen.  Die Schnittstellen sind in experimental.  Weitere Informationen finden Sie unter [ICoreWebView2ExperimentalEnvironment][ReferenceWin3209622Icorewebview2experimentalenvironment].  

#### .NET  

*   .NET-Binärdateien sind jetzt [stark benannt][DotnetStandardAssemblyStrongNamed].  \ ([\ #181][GithubMicrosoftedgeWebviewfeedbackIssue181]\).  
*   Das NuGet-Ziel wurde aktualisiert `WebViewLoader2.dll` .  \ ([\ #228][GithubMicrosoftedgeWebviewfeedbackIssue228]\) und \ ([\ #183][GithubMicrosoftedgeWebviewfeedbackIssue183]\).  
*   Aktualisiert `WebResourceRequested` , um [HttpRequestHeaders][ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httprequestheaders] -und [HttpResponseHeaders][ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httpresponseheaders] -APIs in .net verfügbar zu machen.  \ ([\ #131][GithubMicrosoftedgeWebviewfeedbackIssue131]\).  

## 0.9.622  

Veröffentlichungsdatum: 10. September, 2020  

[NuGet-Paket][NuGetGallery0.9.622.11] \ | minimale WebView2-Runtime-Version 86.0.622.11.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: dieses SDK ist der Veröffentlichungskandidat für WebView2 Win32 C/C++ GA.  Die GA-Version sollte dieselbe API-Schnittstelle und-Funktionalität verwenden.  

*   Getrennte [Browser Richtlinien][DeployedgeMicrosoftEdgePolicies].  
*   [AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin3209622Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount] -Eigenschaft für WebView2-Umgebungsoptionen hinzugefügt, um bedingten Zugriff für WebView zu ermöglichen.  
*   Aktualisiert `ICoreWebView2NewWindowRequestedEventArgs` , um die [WindowFeatures][ReferenceWin3209622Icorewebview2newwindowrequestedeventargsGetWindowfeatures] -Eigenschaft und die zugehörige [ICoreWebView2WindowFeatures][ReferenceWin3209622Icorewebview2windowfeatures]einzubeziehen.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   `System.Windows.Rect`Die Verwendung wird `System.Drawing.Rectangle` anstelle von `System.Windows.Rect` \ ([\ #235][GithubMicrosoftedgeWebviewfeedbackIssue235]\) aktualisiert.  
*   Das mswebviewnewwindowrequested-Ereignis wurde aktualisiert, um die `window.open()` Anforderung ohne Parameter zu behandeln.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][ReferenceWin3209622Icorewebview2environmentoptionsPutAdditionalbrowserarguments] -Satz using `ICoreWebView2EnvironmentOptions` werden nicht mit Umgebungsvariablen oder Registrierungswert überschrieben.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209622IdlCreatecorewebview2environmentwithoptions].  

## 0.9.579  

Veröffentlichungsdatum: 20. Juli 2020  

[NuGet-Paket][NuGetGallery0.9.579] \ | minimale Microsoft Edge-Version 86.0.579.0.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: Evergreen WebView2-Laufzeit und-Installationsprogramm werden für die Vorschau veröffentlicht.  Weitere Informationen finden Sie unter [Verteilung von WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview].  
*   > [!IMPORTANT]
    > **Ankündigung**: die folgenden WebView2-SDK-Versionen werden nach der nächsten SDK-Version nicht mehr unterstützt.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Die WebView2-SDK-Versionen sind auch in nuget.org als veraltet markiert.  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem Laufenden zu bleiben.  

*   Verbesserungen des WebView-Worker-Threads.  \ ([\ #318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Popup-Blocker deaktiviert in WebView.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu der [IsUserInitiated][ReferenceWin3209538Icorewebview2newwindowrequestedeventargsGetIsuserinitiated] -Eigenschaft des `NewWindowRequested` Ereignisses.  
*   Sichergestellt, dass das Startereignis für WebView-Navigation ausgelöst wird `about:blank` .  Nun `NavigationStarting` werden Ereignisse für die gesamte Navigation ausgelöst, aber Abbruch `about:blank` -oder IFRAME-srcdoc werden nicht unterstützt und ignoriert.  
*   Blockiertes `edge:// URI` Schema in WebView.  
*   Experimentelle [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin3209538Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled] -Eigenschaft für WebView2-Umgebungsoptionen hinzugefügt, um bedingten Zugriff für WebView zu ermöglichen.  
*   Experimentelles [WebResourceResponseReceived][ReferenceWin3209538Icorewebview2experimentalAddWebresourceresponsereceived] -Ereignis wurde hinzugefügt, das ausgelöst wird, nachdem die WebView die Antwort für eine Webressourcen Anforderung empfangen und verarbeitet hat.  Authentifizierungsheader (sofern vorhanden) sind im Response-Objekt enthalten.  

#### .NET  

*   Verbesserte WPF-Fokus Behandlung  \ ([\ #185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   `ZoomFactor`Eigenschaft auf WPF-Webview2-Controller hinzugefügt.  

## 0.9.538  

[NuGet-Paket][NuGetGallery0.9.538] \ | minimale Microsoft Edge-Version 85.0.538.0.  

#### Allgemein  

*   Unterstützung für WebView2 SDK-Version [0.8.149](#08149)wird gelöscht.  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem Laufenden zu bleiben.  
*   Die Gruppenrichtlinie wurde aktualisiert, um zu berücksichtigen, wenn der Profilpfad des Microsoft Edge-Browsers geändert wird \ ([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  

#### Win32 C/C++  

*   [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures]hinzugefügt, das ausgelöst wird, wenn `window.open()` ausgeführt wird und [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin3209538Icorewebview2experimentalwindowfeatures] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\) zugeordnet ist.  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] ist veraltet und wird durch [CreateCoreWebView2EnvironmentWithOptions] [[ReferenceWin3209538IdlCreatecorewebview2environmentwithoptions]] ersetzt.  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: um sicherzustellen, dass die WebView2-API mit den Windows-API-Benennungskonventionen übereinstimmt, hat das WebView-Team die Namen der folgenden aktualisiert.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed] ist jetzt [AreHostObjectsAllowed][ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed].  
*   [AddHostObjectToScript][ReferenceWin3209538Icorewebview2Addhostobjecttoscript] aktualisiert, um sicherzustellen, dass die ursprünglichen Hostobjekt-Serialisierungsprogramme-Marker auf die Proxyobjekte gesetzt und als Hostobjekt zurück serialisiert werden, wenn Sie als Parameter im JavaScript-Rückruf \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\) übergeben werden.  

#### .Net (0.9.538 Pre-Release)  

*   Freigegebene WinForms-und WPF-WebView2API-Beispiele, die umfassende Leitfäden des WebView2-SDK sind.  Wenn Sie weitere Informationen wünschen, navigieren Sie zu [Samples Repo][GithubMicrosoftedgeWebview2samplesMain].  
*   Unterstützung für visuelles Hosting und Fenster Features, [experimentelle APIs][ConceptsVersioningExperimentalApis], wurde hinzugefügt.  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: die folgenden Verzögerungen implementieren nun IDisposable:  [ScriptDialogOpening][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [mswebviewnewwindowrequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]und [PermissionRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   [GetAvailableBrowserVersionString][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] und [CompareBrowserVersions][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] werden als [CoreWebView2Environment][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment] -Statik hinzugefügt.  

## 0.9.515-Vorabversion  

[NuGet-Paket][NuGetGallery0.9.515-prerelease] \ | minimale Microsoft Edge-Version 84.0.515.0.  

*   > [!IMPORTANT]
    > **Ankündigung**: WebView2 unterstützt jetzt Windows Forms und WPF unter .NET Framework 4.6.2 oder höher und .net Core 3,0 oder höher im **Pre-Release-Paket**.  
*   Weitere Informationen zum Erstellen von WPF-Anwendungen und zum WPF- [Referenz][ReferenceWpf09515Reference] WebView2 für WPF-spezifische APIs finden Sie unter [WPF-Leitfaden für erste Schritte][GettingstartedWpf].  
*   Weitere Informationen zum Erstellen von Windows Forms-Anwendungen und der WebView2 [Windows Forms-Referenz][ReferenceWinforms09515Reference] für Windows Forms-spezifische APIs finden Sie unter [Windows Forms-Leitfaden für erste Schritte][GettingstartedWinforms].  
*   Wenn Sie weitere Informationen zu den CoreWebView2-APIs erhalten möchten, navigieren Sie zu [.net Reference][ReferenceDotnet09515Reference].  
*   > [!CAUTION]
    > **Bekannte Probleme**: das WebView-Team kennt einige Probleme in der Vorabversion, die in zukünftigen Versionen aufgelöst werden.  
    > *   **Dpi-Erkennung**: WebView2 für WPF ist derzeit nicht mit dpi vertraut.  Bei der Initialisierung von WebView2 auf hochdpi-Monitoren gibt es ein bekanntes Problem, bei dem die WebView zunächst als Bruchteil des Fensters initialisiert wird, bis die Größe des Fensters geändert wird.  
    > *   **WPF-Designer**: der WPF-Designer wird derzeit nicht unterstützt.  Fügen Sie das WebView2-Steuerelement in Ihrer APP hinzu, indem Sie den entsprechenden XAML-Code in einem Text-Editor direkt ändern.  

## 0.9.488  

[NuGet-Paket][NuGetGallery0.9.488] \ | minimale Microsoft Edge-Version 84.0.488.0.  

*   > [!IMPORTANT]
    > **Ankündigung**: beginnend mit der bevorstehenden Microsoft Edge-Version 83, ist Evergreen WebView nicht mehr auf den stabilen Browser Kanal ausgerichtet.  Stattdessen zielt Sie auf einen anderen Satz von Binärdateien ab, der Marken- [Evergreen-WebView2-Laufzeit][ConceptsDistributionEvergreenMode], die Sie möglicherweise durch einen Installer verketten, den das WebView-Team zurzeit entwickelt.  Weitere Informationen finden Sie unter [App-Verteilung][ConceptsDistribution].  
*   > [!IMPORTANT]
    > **Ankündigung**: das WebView-Team gibt zwei Pakete frei: ein Pre-Release-Paket mit experimentellen APIs \ (für Sie zu testen \) und ein stabiles Release-Paket mit stabilen APIs \ (für Ihr Vertrauen).  Informationen zu den Unterschieden finden Sie unter [Grundlegendes zu Browserversionen und WebView2][ConceptsVersioning].  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: um sicherzustellen, dass die WebView2-API mit den Windows-API-Benennungskonventionen übereinstimmt, hat das WebView-Team die Namen der folgenden Schnittstellen aktualisiert.  
    > *   `CORE_WEBVIEW2_*` prefix ist jetzt `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo] ist jetzt [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo] ist nun [get_BrowserVersionString][ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring].  
    > *   [Addremoteobject][ReferenceWin3209430Icorewebview2Addremoteobject] ist jetzt [AddHostObjectToScript][ReferenceWin3209488Icorewebview2Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][ReferenceWin3209430Icorewebview2Removeremoteobject] ist jetzt [RemoveHostObjectFromScript][ReferenceWin3209488Icorewebview2Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` ist jetzt `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: die `AddRemoteObject` js-Proxy Methoden werden ebenfalls umbenannt.  
    > *   `getLocal` ist jetzt `getLocalProperty` .  
    > *   `setLocal` ist jetzt `setLocalProperty` .  
    > *   `getRemote` ist jetzt `getHostProperty` .  
    > *   `setRemote` ist jetzt `setHostProperty` .  
    > *   `applyRemote` ist jetzt `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] ist veraltet und durch [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions]ersetzt.  
*   [FrameNavigationCompleted][ReferenceWin3209488Icorewebview2AddFramenavigationcompleted] -Ereignis hinzugefügt.  Wenn ein IFRAME nun die Navigation beendet, wird ein Ereignis ausgelöst und gibt den Erfolg der Navigation und der Navigations-ID zurück.  
*   [ICoreWebView2EnvironmentOptions][ReferenceWin3209488Icorewebview2environmentoptions] -Schnittstelle hinzugefügt, die verwendet werden kann, um die Version der WebView2-Laufzeit zu ermitteln, auf die die Anwendung ausgerichtet ist.  
*   [IsBuiltInErrorPageEnabled][ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled] -Einstellung hinzugefügt.  Nun können Sie die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler aktivieren oder deaktivieren.  
*   Aktualisierte Remote Objekt Injektion zur Unterstützung von .net IDispatch-Implementierungen \ ([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Das [mswebviewnewwindowrequested][ReferenceWin3209488Icorewebview2AddNewwindowrequested] -Ereignis wurde aktualisiert, um Anforderungen aus Kontextmenüs zu behandeln \ ([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Hat das erste separate WebView2-Pre-Release-Paket veröffentlicht, in dem Sie auf visuelle Hosting-APIs zugreifen können.  Das WebView-Team hat [APISample][GithubMicrosoftedgeWebview2samplesMain] aktualisiert, um die neuen experimentellen APIs einzubeziehen.  
    *   [ICoreWebView2ExperimentalCompositionController][ReferenceWin3209488Icorewebview2experimentalcompositioncontroller] -Schnittstelle hinzugefügt, um eine Verbindung mit einer Kompositionsstruktur herzustellen und Eingaben für die WebView bereitzustellen.  
    *   [ICoreWebView2ExperimentalPointerInfo][ReferenceWin3209488Icorewebview2experimentalpointerinfo]hinzugefügt, das alle Informationen aus einer enthält `POINTER_INFO` .  Dieses Objekt wird an SendPointerInput übergeben, um zeigereingaben in die WebView einzufügen.  
    *   [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler]hinzugefügt, das die APP anweist, wenn der Mauszeiger über der WebView geändert werden soll.  Wenn sich die Maus über einem Textfeld in der WebView befindet, ändert sich der Cursor vom Pfeil zur Auswahl.  Die `cursor` Eigenschaft in der `CompositionController` teilt der APP mit, was der Mauszeiger aktuell für die WebView sein sollte.  

## 0.9.430  

[NuGet-Paket][NuGetGallery0.9.430] \ | minimale Microsoft Edge-Version 82.0.430.0.  

Das WebView2-SDK ist die offizielle Win32 C++-Beta Version, die mehrere Funktionsanforderungen aus Feedback enthält.  Das WebView-Team versucht, die Anzahl der Versionen mit Unterbrechungen zu begrenzen, aber da die allgemeine Verfügbarkeit angesprochen wird, wird die Beta Version verwendet, um mehrere wichtige wichtige Änderungen in einem Schritt einzubeziehen.  

*   > [!IMPORTANT]
    > **Aktuelle Änderung**: Wenn sich die endgültige Version nähert, wird das WebView-Team das Präfix *IWebView2WebView*   zu *ICoreWebView2*   umbenannt, um sicherzustellen, dass die WebView2-API mit der Windows-API-Benennungskonvention ausgerichtet wird.  Um das WebView2-SDK aus UI-Frameworks zu nutzen, wurde das WebView-Team außerdem `ICoreWebView2` in [ICoreWebView2][ReferenceWin3209430Icorewebview2] und [ICoreWebView2Host][ReferenceWin3209430Icorewebview2host]getrennt.  `ICoreWebView2Host` unterstützt das Ändern der Größe, ein-und ausblenden, die Fokussierung und andere Funktionen im Zusammenhang mit Fenster und Komposition.  ICoreWebView2 unterstützt alle anderen WebView2-Funktionen.  Wenn Sie mehr über das Integrieren der Änderungen erfahren möchten, navigieren Sie im WebView2 [APISample][GithubMicrosoftedgeWebview2samplesMain] -Projekt zur WebView2- [Pull-Anforderung][GithubMicrosoftedgeWebview2samplesPr17] .  
*   > [!IMPORTANT]
    > Unter **brechende Änderung**: Teilen Sie [DocumentStateChanged][ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged] in drei Komponenten auf: [sourced][ReferenceWin3209430Icorewebview2AddSourcechanged], [ContentLoading][ReferenceWin3209430Icorewebview2AddContentloading]und [History][ReferenceWin3209430Icorewebview2AddHistorychanged].  Wenn die Quell-URL nun geändert `SourceChanged` wird, wird das Ereignis ausgelöst.  Wenn der Verlaufszustand geändert wird `HistoryChanged` , wird das Ereignis ausgelöst.  Das `ContentLoading` Ereignis wird vor dem anfänglichen Skript ausgelöst, wenn ein neues Dokument geladen wird.  
*   Unterstützung für die ARM64-Architektur wurde hinzugefügt.  
*   Soft Input Panel (SIP \)-Unterstützung für Touchscreen-Geräte hinzugefügt.  
*   Unterstützung für Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 und Windows Server 2016 wurde hinzugefügt.  
*   [NotifyParentWindowPositionChanged][ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged] hinzugefügt, der es der Statusleiste ermöglicht, dem Fenster im Fenstermodus zu folgen.  Die Änderung muss auch im Fenster freien Modus implementiert werden, damit Barrierefreiheitsfeatures funktionieren.  
*   [AreRemoteObjectsAllowed][ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed] -Einstellung hinzugefügt, um global zu steuern, ob von Remoteobjekten auf eine Seite zugegriffen werden kann.  Standardmäßig `AreRemoteObjectsAllowed` ist aktiviert, was bedeutet, dass Remoteobjekte, die von [addremoteobject][ReferenceWin3209430Icorewebview2Addremoteobject] hinzugefügt wurden, von der Seite aus zugänglich sind.  Wenn `AreRemoteObjectsAllowed` deaktiviert ist, kann auf die Objekte nicht über die Seite zugegriffen werden.  Änderungen werden beim nächsten Navigations Ereignis übernommen.  
*   [IsZoomControlEnabled][ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled] -Einstellung wurde hinzugefügt, um zu verhindern, dass Benutzer den Zoom der WebView mithilfe von `ctrl` + `+` und `ctrl` + `-` \ (oder `ctrl` + Mausrad \) beeinflussen.  Zoom kann weiterhin mithilfe von [put_ZoomFactor][ReferenceWin3209430Icorewebview2hostPutZoomfactor] festgelegt werden, wenn die Einstellung deaktiviert ist.  
*   ZoomFactor geändert, um nur auf die aktuelle WebView anzuwenden.  Zoom Änderungen an der aktuellen WebView wirken sich nicht auf andere Webansichten aus, die Sie zur gleichen Ursprungssite navigiert haben.  Wenn Sie weitere Informationen wünschen, navigieren Sie zu [get_ZoomFactor][ReferenceWin3209430Icorewebview2hostGetZoomfactor].  
*   HID-zoomview-UI für WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   [SetBoundsAndZoomFactor][ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor]hinzugefügt.  Nun können Sie den Zoomfaktor und die Grenzen eines Webviews gleichzeitig einstellen.  
*   [WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] -Ereignis hinzugefügt.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [add_WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] \ ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Unterstützung für den `beforeunload` Dialogfeldtyp für JavaScript-Dialog Ereignisse hinzugefügt und [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind] Enum-Eintrag hinzugefügt.  
*   [GetHeaders][ReferenceWin3209430Icorewebview2httprequestheadersGetheaders] zu HttpRequestHeaders, [GetHeader][ReferenceWin3209430Icorewebview2httpresponseheadersGetheader] zu HttpResponseHeaders und [get_HasCurrentHeader][ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader] -Eigenschaft zu HttpHeadersCollectionIterator hinzugefügt.  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: geändertes `DevToolsProtocolEventReceived` Verhalten.  Nun können Sie einen [DevToolsProtocolEventReceiver][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver] für ein bestimmtes devtools-Protokollereignis erstellen und dieses Ereignis mithilfe [add_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived]remove_DevToolsProtocolEventReceived abonnieren/abbestellen / [remove_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived].
*   > [!IMPORTANT]
    > Unter **brechende Änderung**: Changed WebMessageReceivedEventArgs ' [get_WebMessageAsString][ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring] -Eigenschaft in eine [TryGetWebMessageAsString][ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring] -Methode.  
*   > [!IMPORTANT]
    > **Umbruch Änderung**: geänderte `AcceleratorKeyPressedEventArgs` [handle][ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle] -Methode in eine [get_Handled][ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled] -Eigenschaft.  

## 0.8.355

[NuGet-Paket][NuGetGallery0.8.355] \ | minimale Microsoft Edge-Version 80.0.355.0.

*   Veröffentlichtes WebView2API-Beispiel, eine umfassende Anleitung zum WebView2-SDK.  Weitere Informationen finden Sie unter [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   IME-Unterstützung für alle Sprachen außer Englisch ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\) hinzugefügt.  
*   Die API-Oberfläche des `WebResourceRequested` Ereignisses wurde als Reaktion auf Fehlerberichte aktualisiert.  Das gleichzeitige angeben eines Filters und eines Ereignisses bei der Erstellung ist jetzt veraltet.  Zum Erstellen eines angeforderten Webressource-Ereignisses verwenden Sie [add_WebResourceRequested][ReferenceWin3208190Iwebview2webview5AddWebresourcerequested] , um das Ereignis und [AddWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter] hinzuzufügen, um einen Filter hinzuzufügen.  [RemoveWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter] entfernt den Filter \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > Unter **brechende Änderung**: geändertes Vollbild-Verhalten.  Veraltete [IsFullScreenAllowed][ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated].  Wenn ein Element innerhalb einer WebView-Datei (beispielsweise ein Video) auf Vollbild eingestellt ist, wird nun standardmäßig die Begrenzungen der WebView-Ansicht ausgefüllt.  Verwenden Sie das [ContainsFullScreenElementChanged][ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler] -Ereignis und [get_ContainsFullScreenElement][ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement] , um anzugeben, wie die APP die Größe der WebView ändern soll, wenn ein Element in den Vollbildmodus wechseln möchte.  

## 0.8.314  

[NuGet-Paket][NuGetGallery0.8.314] \ | minimale Microsoft Edge-Version 80.0.314.0.  

*   Unterstützung für Windows 7, Windows 8 und Windows 8,1 wurde hinzugefügt.  
*   Visual Studio-und Visual Studio-Code-Debug-Unterstützung für WebView2 hinzugefügt.  Debuggen Sie nun Ihr Skript in der WebView2 direkt von der IDE aus.  Weitere Informationen finden Sie unter [Debuggen bei der Entwicklung mit WebView2-Steuerelementen][HowtoDebug].  
*   Hinzugefügt `Native Object Injection` , wodurch das in WebView2 ausgeführte Skript auf ein IDispatch-Objekt aus der Win32-Komponente der Anwendung zugreifen und auf die Eigenschaften des IDispatch-Objekts zugreifen kann.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [addremoteobject][ReferenceWin3208190Iwebview2webview4Addremoteobject] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Ereignis hinzugefügt `AcceleratorKeyPressed` .  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [add_AcceleratorKeyPressed][ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Deaktiviert `Context Menus` .  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [put_AreDefaultContextMenusEnabled][ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Aktualisiert `DPI Awareness` .  Die dpi-Bekanntheit von WebView ist nun identisch mit der dpi-Bekanntheit der Hostanwendung.  
    
    > [!NOTE]
    > Wenn eine andere Hybridanwendung mit einer anderen dpi-Sensibilisierung als die ursprüngliche WebView gestartet wird, wird die neue WebView nicht gestartet, wenn das Benutzerdatenverzeichnis identisch ist \ ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Aktualisiert `Notification Change Behavior` , damit WebView2 die Benachrichtigungs Berechtigungsanforderungen, die von Webinhalten, die in der WebView gehostet werden, automatisch ablehnen.  

## 0.8.270  

[NuGet-Paket][NuGetGallery0.8.270] \ | minimale Microsoft Edge-Version 78.0.270.0.  

*   Ereignis hinzugefügt `DocumentTitleChanged` , um die Änderung des Dokumenttitels anzugeben \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   API hinzugefügt `GetWebView2BrowserVersionInfo` \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Ereignis hinzugefügt `NewWindowRequested` .  
*   `CreateWebView2EnvironmentWithDetails`Zu entfernende zu aktualisierende Funktion `releaseChannelPreference` .  Weitere Informationen zur `CreateWebView2EnvironmentWithDetails` Funktion finden Sie unter [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails].  Die Überschreibung der Registrierungs-und Umgebungsvariablen wird weiterhin unterstützt.  Die Standardkanal Einstellung wird nur verwendet, wenn Sie überschrieben wird.  
    Während der Kanalsuche überspringt das WebView-Team alle älteren Kanal Versionen, die nicht mit dem WebView2-SDK kompatibel sind.  
    Das WebView-Team wählt den stabileren Kanal aus, um die konsistentsten Verhaltensweisen für den Endbenutzer zu gewährleisten.  Wenn Sie mit den neuesten Canary-Builds testen, sollten Sie ein Skript erstellen, um die `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` Umgebungsvariable `1` vor dem Starten der App festzulegen.  
*   Die `CreateWebView2EnvironmentWithDetails` Funktion wurde mit der Logik für die Auswahl aktualisiert `userDataFolder` , wenn nicht angegeben.  Weitere Informationen zur `CreateWebView2EnvironmentWithDetails` Funktion finden Sie unter [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails].  Wenn Sie zuvor den Standard `userDataFolder` Speicherort verwendet haben, wird beim Wechseln zum neuen SDK der Standardwert `userDataFolder` zurückgesetzt \ (auf einen neuen Speicherort im Host Codeverzeichnis festgesetzt \), und ihr Zustand wird ebenfalls zurückgesetzt.  
    Wenn der Hostprozess nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis verfügt, `CreateWebView2EnvironmentWithDetails` schlägt die Funktion möglicherweise fehl.  Sie können die Daten aus dem alten Benutzerdatenverzeichnis in das neue Verzeichnis kopieren.  

## 0.8.230  

[NuGet-Paket][NuGetGallery0.8.230] \ | minimale Microsoft Edge-Version 77.0.230.0.  

*   API hinzugefügt `Stop` , um alle Navigations-und ausstehenden Ressourcen Abrufe zu beenden \ ([\ #28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   `.tlb`Datei zum NuGet-Paket hinzugefügt \ ([\ #22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   .Net-Projekte wurden der Installationsliste im NuGet-Paket hinzugefügt \ ([\ #32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  

## 0.8.190  

[NuGet-Paket][NuGetGallery0.8.190] \ | minimale Microsoft Edge-Version 77.0.190.0.  

*   Hinzugefügt `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` , um zu steuern, ob Benutzer devtools \ ([\ #16][GithubMicrosoftedgeWebviewfeedbackIssue16]\) öffnen können.  
*   Hinzugefügt `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` , um zu steuern, ob die Statusleiste angezeigt wird \ ([\ #19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Hinzugefügt `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` , um durch den Navigationsverlauf zurückzukehren.  
*   Http-Headertypen hinzugefügt \ ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) zum Anzeigen und Ändern von HTTP-Headern in WebView.  
*   Unterstützung für 32-Bit-WebView auf 64-Bit-Computern hinzugefügt \ ([\ #13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   WebView IDL zum SDK hinzugefügt \ ([\ #14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Lib zur Unterstützung von `IID\_\*` Schnittstellen-ID-Objekten hinzugefügt \ ([\ #12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Hinzugefügt: Pfad, Verknüpfung und Automatisches Kopieren von DLL-Dateien in NuGet- `TARGET` Datei im SDK.  
*   `window.open()`In Skript anfordern aktiviert.  

## 0.8.149  

[NuGet-Paket][NuGetGallery0.8.149] \ | minimale Microsoft Edge-Version 76.0.149.0.  

Erste Entwickler-Preview-Version.  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./concepts/distribution.md#understanding-the-webview2-runtime "Grundlegendes zur WebView2-Laufzeit und zum Installationsprogramm (Preview) – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft docs"  
[ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Experimentelle APIs – Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-apps | Microsoft docs"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF | Microsoft docs"  
[HowtoDebug]: ./howto/debug.md "Debuggen bei der Entwicklung mit WebView2-Steuerelementen | Microsoft docs"  

[ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle]: ./reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle "Handle-Interface-IWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler]: ./reference/win32/0-8-190/iwebview2containsfullscreenelementchangedeventhandler.md "Schnittstelle IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft docs"  
[ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled]: ./reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled-Interface IWebView2Settings2 | Microsoft docs"  
[ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]: ./reference/win32/0-8-190/iwebview2settings.md#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated-Interface IWebView2Settings | Microsoft docs"  
[ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring]: ./reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring "get_WebMessageAsString-Interface IWebView2WebMessageReceivedEventArgs | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed]: ./reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed "add_AcceleratorKeyPressed-Interface IWebView2WebView4 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged]: ./reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged "add_DocumentStateChanged-Interface IWebView2WebView | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview4Addremoteobject]: ./reference/win32/0-8-190/iwebview2webview4.md#addremoteobject "Addremoteobject-Schnittstelle IWebView2WebView4 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5AddWebresourcerequested]: ./reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested "add_WebResourceRequested-Interface IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter "AddWebResourceRequestedFilter-Interface-IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement]: ./reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement "get_ContainsFullScreenElement-Interface IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter-Interface-IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails]:  ./reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-Globals | Microsoft docs"  

[ReferenceWin3209430Icorewebview2]: ./reference/win32/0-9-430/icorewebview2.md "Schnittstelle ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled]: ./reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled "get_Handled-Interface ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddContentloading]: ./reference/win32/0-9-430/icorewebview2.md#add_contentloading "add_ContentLoading-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddHistorychanged]: ./reference/win32/0-9-430/icorewebview2.md#add_historychanged "add_HistoryChanged-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2Addremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#addremoteobject "Addremoteobject-Schnittstelle ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddSourcechanged]: ./reference/win32/0-9-430/icorewebview2.md#add_sourcechanged "add_SourceChanged-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddWindowcloserequested]: ./reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested "add_WindowCloseRequested-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind]: ./reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md "Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived-Interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived-Interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo]: ./reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo "get_BrowserVersionInfo-Interface ICoreWebView2Environment | Microsoft docs"  
[ReferenceWin3209430Icorewebview2host]: ./reference/win32/0-9-430/icorewebview2host.md "Schnittstelle ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo]: ./reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-Globals | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostGetZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor "get_ZoomFactor-Interface ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged]: ./reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged-Interface-ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostPutZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor "put_ZoomFactor-Interface ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor "SetBoundsAndZoomFactor-Interface-ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader]: ./reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader "get_HasCurrentHeader-Interface ICoreWebView2HttpHeadersCollectionIterator | Microsoft docs"  
[ReferenceWin3209430Icorewebview2httprequestheadersGetheaders]: ./reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders "GetHeaders-Interface ICoreWebView2HttpRequestHeaders | Microsoft docs"  
[ReferenceWin3209430Icorewebview2httpresponseheadersGetheader]: ./reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader "GetHeader-Interface ICoreWebView2HttpResponseHeaders | Microsoft docs"  
[ReferenceWin3209430Icorewebview2Removeremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#removeremoteobject "RemoveRemoteObject-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled]: ./reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled "get_IsZoomControlEnabled-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring]: ./reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring "TryGetWebMessageAsString-Interface-ICoreWebView2WebMessageReceivedEventArgs | Microsoft docs"  

[ReferenceWin3209488Icorewebview2AddFramenavigationcompleted]: ./reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted "add_FrameNavigationCompleted-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2AddNewwindowrequested]: ./reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested "add_NewWindowRequested-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring]: ./reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring " | Microsoft docs"  
[ReferenceWin3209488Icorewebview2environmentoptions]: ./reference/win32/0-9-488/icorewebview2environmentoptions.md "Schnittstelle ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin3209488Icorewebview2experimentalcompositioncontroller]: ./reference/win32/0-9-488/icorewebview2experimentalcompositioncontroller.md "Schnittstelle ICoreWebView2ExperimentalCompositionController | Microsoft docs"  
[ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler]: ./reference/win32/0-9-488/icorewebview2experimentalcursorchangedeventhandler.md "Schnittstelle ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft docs"  
[ReferenceWin3209488Icorewebview2experimentalpointerinfo]: ./reference/win32/0-9-488/icorewebview2experimentalpointerinfo.md "Schnittstelle ICoreWebView2ExperimentalPointerInfo | Microsoft docs"  
[ReferenceWin3209488Icorewebview2Removehostobjectfromscript]: ./reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript "RemoveHostObjectFromScript-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled]: ./reference/win32/0-9-488/icorewebview2settings.md#get_isbuiltinerrorpageenabled " | Microsoft docs"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-Globals | Microsoft docs"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  
[ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring]: ./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Microsoft docs"  

[ReferenceDotnet09515Reference]: ./reference/dotnet/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWinforms09515Reference]: ./reference/winforms/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  
[ReferenceWpf09515Reference]: ./reference/wpf/0-9-515-reference-webview2.md "Referenz (WebView2) | Microsoft docs"  


[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md "Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions "CompareBrowserVersions-Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse | Microsoft docs"
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring "GetAvailableBrowserVersionString-Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested "Mswebviewnewwindowrequested-Microsoft. Web. WebView2. Core. CoreWebView2 Klasse | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested "PermissionRequested-Microsoft. Web. WebView2. Core. CoreWebView2 Klasse | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening "ScriptDialogOpening-Microsoft. Web. WebView2. Core. CoreWebView2 Klasse | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested "WebResourceRequested-Microsoft. Web. WebView2. Core. CoreWebView2 Klasse | Microsoft docs"  
[ReferenceWin3209538Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209538Icorewebview2experimentalAddWebresourceresponsereceived]: ./reference/win32/0-9-538/icorewebview2experimental.md#add_webresourceresponsereceived "add_WebResourceResponseReceived-Interface ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin3209538Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled]: ./reference/win32/0-9-538/icorewebview2experimentalenvironmentoptions.md#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled-Interface ICoreWebView2ExperimentalEnvironmentOptions | Microsoft docs"  
[ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures "get_WindowFeatures-Interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin3209538Icorewebview2experimentalwindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md "Schnittstelle ICoreWebView2ExperimentalWindowFeatures | Microsoft docs"  
[ReferenceWin3209538Icorewebview2newwindowrequestedeventargsGetIsuserinitiated]: ./reference/win32/0-9-538/icorewebview2newwindowrequestedeventargs.md#get_isuserinitiated "get_IsUserInitiated-Schnittstelle ICoreWebView2NewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed]: ./reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed "get_AreHostObjectsAllowed-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209538IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  

[ReferenceWin3209622Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount]: ./reference/win32/0-9-622/icorewebview2environmentoptions.md#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount-Interface ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin3209622Icorewebview2environmentoptionsPutAdditionalbrowserarguments]: ./reference/win32/0-9-622/icorewebview2environmentoptions.md#put_additionalbrowserarguments "put_AdditionalBrowserArguments-Interface ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin3209622Icorewebview2experimentalenvironment]: ./reference/win32/0-9-622/icorewebview2experimentalenvironment.md "Schnittstelle ICoreWebView2ExperimentalEnvironment | Microsoft docs"  
[ReferenceWin3209622Icorewebview2newwindowrequestedeventargsGetWindowfeatures]: ./reference/win32/0-9-622/icorewebview2newwindowrequestedeventargs.md#get_windowfeatures "get_WindowFeatures-Interface ICoreWebView2NewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin3209622Icorewebview2windowfeatures]: ./reference/win32/0-9-622/icorewebview2windowfeatures.md "Schnittstelle ICoreWebView2WindowFeatures | Microsoft docs"  
[ReferenceWin3209622IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-622/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft Edge"  

[ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httprequestheaders]: ./reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2httprequestheaders.md "Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders Klasse | Microsoft docs"  
[ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: ./reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2httpresponseheaders.md "Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders Klasse | Microsoft docs"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Richtlinien | Microsoft docs"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblys mit starkem Namen | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Feedback-Repo für MicrosoftEdge/WebViewFeedback-Problem 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Feedback Repo für MicrosoftEdge/WebViewFeedback Ausgabe 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Feedback-Repo für MicrosoftEdge/WebViewFeedback-Problem 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Feedback-Repo für MicrosoftEdge/WebViewFeedback-Problem 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 108"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 119"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 131"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 185"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 235"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 318"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Verschieben eines Projekts zur Verwendung der neuesten WebView2 SDK-0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel-MicrosoftEdge/WebView2Samples | GitHub"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "NuGet-Katalog | Microsoft. Web. WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.515-Vorabversion"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.622.11"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.628-Vorabversion"  
