---
description: Versionshinweise für Microsoft Edge WebView2 SDK
title: Versionshinweise für Microsoft Edge WebView2 für Win32, WPF und WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 63a81baed1f4b67cf37b95fa88abd0b6f67b1e4d
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536489"
---
# <a name="release-notes-for-webview2-sdk"></a>Versionshinweise für WebView2 SDK  

Das WebView2-Team aktualisiert das [WebView2 SDK][NuGetGallery] auf sechs Wochen.  In den folgenden Inhalten finden Sie aktuelle Informationen zu Produktansagen, Ergänzungen, Änderungen und Änderungen an den APIs.  

> [!NOTE]
> Stellen Sie sicher, dass Sie Ihre App nach dem Aktualisieren des NuGet kompilieren.  Das WebView-Team empfiehlt, den Canary-Kanal bei der Entwicklung mit den Vorabpaketen und die Evergreen WebView2-Runtime zu verwenden, wenn Sie die Veröffentlichungspakete verwenden.  Weitere Informationen finden Sie unter [Matching WebView2 Runtime versions][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions].  

> [!NOTE]
> WebView2-Fehlerkorrekturen sind entweder Runtime- oder SDK-spezifisch.  

## <a name="10865-prerelease"></a>1.0.865-prerelease  

Veröffentlichungsdatum: 26. April 2021  

[NuGet -Paket][NuGetGallery1.0.865-prerelease] \| Mindestens Microsoft Edge zu ladende Version: 86.0.616.0 oder neuer \| Vollständige API-Kompatibilität: 91.0.865.0 oder neuer  

### <a name="general"></a>Allgemein  

#### <a name="experimental-features"></a>Experimentelle Features  

*   [IsPinchZoomEnabled-Einstellung hinzugefügt.][Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled] Sie können das Zoomsteuerelement für die Seitenskala in einer Einstellung aktivieren oder deaktivieren.  
*   Benutzerdefinierte [add_DownloadStarting-API][Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting] hinzugefügt.  Sie können Downloads blockieren, in einem anderen Pfad speichern und auf die erforderlichen Metadaten zugreifen, um eine benutzerdefinierte Downloadbenutzeroberfläche zu erstellen.  
*   Elementunterstützung `iframe` von [AddHostObjectToScriptWithOrigins hinzugefügt.][Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins]  
*   Beispielcode für [die WPF-Beispiel-App hinzugefügt, um][GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser] die API zum Deaktivieren von Browserfunktionsschlüsseln zu verwenden.  
*   Die [UpdateRuntime-API][Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime] wurde hinzugefügt, um die WebView2-Runtime auf einfache Weise zu aktualisieren.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Der Handler für eine `Chromium DevTools Protocol` Nachricht mit `POST` Binärdaten in WebView2 wurde behoben.  
*   Die `OpenSaveAsAwareness` Downloadbenutzeroberfläche wurde deaktiviert, da sie Links zu `edge://settings` enthielt.  \([\#1120][GithubMicrosoftedgeWebviewfeedbackIssue1120]\).  
*   Branding aus dem Bildschirmfreigabedialogfeld entfernt.  \([\#940][GithubMicrosoftedgeWebviewfeedbackIssue940]\).  
*   Fehler behoben, bei dem [die SetWindowDisplayAffinity-Funktion][WindowsWin32ApiWinuserSetWindowDisplayAffinity] WebView2 abgebrochen hat, als sie die Bildschirmaufnahme in einer WebView2-App beendete.  \([\#841][GithubMicrosoftedgeWebviewfeedbackIssue841]\).
*   Fehler beim Kompositionshosting behoben, bei dem die Mauseingabe nicht mehr funktionierte, wenn stifteingaben an WebView2 gesendet wurden.  
*   Fehler behoben, bei dem die Mauseingabe nach jeder Stifteingabe nicht mehr eingegeben wurde.  Diese Änderung ist laufzeitspezifisch.  
    
### <a name="net"></a>.NET  

#### <a name="experimental-features"></a>Experimentelle Features  

*   WebView2-Designertool zur WPF Toolbox hinzugefügt.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   WebView2-UI-Element im .NET-Designermodus hinzugefügt.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Beschreibungen der COM-Ausnahme wurden verbessert, indem jeweils eine ausführlichere .NET-Ausnahme umhüllt wurde.  \([\#338][GithubMicrosoftedgeWebviewfeedbackIssue338]\).  Diese Änderung ist laufzeitspezifisch.  
*   Fehler behoben, der beim Auswählen der Fokusverschiebung verursacht wurde, führte dazu, dass das #A0 in Microsoft Visual Studio `tab` Tools for Office.  \([\#589][GithubMicrosoftedgeWebviewfeedbackIssue589] und [\#933][GithubMicrosoftedgeWebviewfeedbackIssue933]\).  Diese Änderung ist laufzeitspezifisch.  
*   Verbesserte .NET-Framework-Ladeebene, um robuster zu sein.  \([\#946][GithubMicrosoftedgeWebviewfeedbackIssue946]\).
*   Fehler behoben, der den Absturz verursachte, als Sie versuchen, die Aktualisierung zu wiederholen, bevor die erste Navigation abgeschlossen wurde.  \([\#1011][GithubMicrosoftedgeWebviewfeedbackIssue1011]\).
*   Initialisierung wurde behoben, sodass die Navigation während `CoreWebView2InitializationCompleted` erfolgt.  \([\#1050][GithubMicrosoftedgeWebviewfeedbackIssue1050]\).
*   Verbesserte Behandlung von Absturzfehlern beim .NET-Browserprozess.  Sie können Steuerelemente jetzt neu erstellen, nachdem Sie ein `ProcessFailed` Ereignis ohne Absturz behandeln.  \([\#996][GithubMicrosoftedgeWebviewfeedbackIssue996]\).  

## <a name="1081841"></a>1.0.818.41  

Veröffentlichungsdatum: 21. April 2021  

[NuGet -Paket][NuGetGallery1.0.818.41] \| Mindestens zu ladende Laufzeitversion: 86.0.616.0 oder neuer \| Vollständige API-Kompatibilität: 90.0.818.41 oder neuer  

### <a name="general"></a>Allgemein  

#### <a name="features"></a>Features  

*   Verbesserter WebView2-Code, um ausfallsicherer für Anwendungsdateien mit `.exe` falsch formatierten Versionsinformationen zu sein.  \([\#850][GithubMicrosoftedgeWebviewfeedbackIssue850]\).  
*   Aus `--winhttp-proxy-resolver` der Befehlszeile des WebView-Browserprozesses entfernt und andere Proxybefehlszeilenoptionen für WebView2 aktiviert.  
  
## <a name="10824-prerelease"></a>1.0.824-prerelease  

Veröffentlichungsdatum: 8. März 2021  

[NuGet -Paket][NuGetGallery1.0.824-prerelease] \| Mindestens Microsoft Edge zu ladende Version: 86.0.616.0 oder neuer \| Vollständige API-Kompatibilität: 91.0.824.0 oder neuer  

### <a name="general"></a>Allgemein  

#### <a name="features"></a>Features  

*   Das Ereignis `ProcessFailed` wurde erweitert.  Es wird jetzt für untergeordnete Prozesse und Framerenderer, die nicht rendern, erhöht.  
*   Experimentelle [AreBrowserAcceleratorKeysEnabled-Einstellung][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled] hinzugefügt.  Sie können verhindern, dass der Browser auf Tastenkombinationen im Zusammenhang mit Navigation, Drucken, Speichern und anderen browserspezifischen Funktionen reagiert.  
*   Elementunterstützung `iframe` für `AddScriptToExecuteOnDocumentCreated` hinzugefügt.  
    
#### <a name="promotion"></a>Promotion  

*   [UserAgent][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] DIE API wird jetzt zu Stable heraufgestuft.  
*   Rasterization Scale APIs \([RasterizationScale][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] property,  [RasterizationScaleChanged][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] event, [BoundsMode property][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode], and [ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] property\) are now promoted to Stable.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Erweiterte unterstützte C++- und .NET-Projekttypen wie MFC und ATL.  \([\#506][GithubMicrosoftedgeWebviewfeedbackIssue506], [\#669][GithubMicrosoftedgeWebviewfeedbackIssue669]und [\#851][GithubMicrosoftedgeWebviewfeedbackIssue851]\).  
*   Es wurde ein Fehler behoben, bei dem die Evergreen WebView2-Laufzeit den Eingehenden Firewalleintrag nicht mehr zusickert.  
*   Einstellung Antwort während des Ereignisses `WebResourceRequested` behoben.  \([\#568][GithubMicrosoftedgeWebviewfeedbackIssue568]\).  
*   Es wurde ein Fehler behoben, der dazu führt, dass der `edge://` Browserprozess beendet wurde.  \([\#604][GithubMicrosoftedgeWebviewfeedbackIssue604]\).  
*   Es wurde ein Fehler behoben, der webView2 auf die Bildschirmgröße im visuellen Hostingmodus beschränkte.  

## <a name="1077444"></a>1.0.774.44  

Veröffentlichungsdatum: 8. März 2021  

[NuGet -Paket][NuGetGallery1.0.774.44] \| Mindestens zu ladende Laufzeitversion: 86.0.616.0 oder neuer \| Vollständige API-Kompatibilität: 89.0.774.44 oder neuer  

### <a name="general"></a>Allgemein  

#### <a name="features"></a>Features  

*   Verschiedene Browserdienste Microsoft Edge WebView2 deaktiviert.  
*   Visuelle Hosting-APIs sind jetzt allgemein verfügbar.  

#### <a name="promotions"></a>Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable heraufgestuft.  
    *   [DPI-Unterstützungs-APIs][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   Visuelle Hosting-APIs  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend und Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
        
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Es wurde ein Fehler behoben, der webView2 auf die Bildschirmgröße im visuellen Hostingmodus beschränkte.  
    
## <a name="10790-prerelease"></a>1.0.790-prerelease  

Veröffentlichungsdatum: 10. Februar 2021  

[NuGet -Paket][NuGetGallery1.0.790-prerelease] \| Microsoft Edge Version 86.0.616.0 oder neuer  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Breaking Change**: Das WebView2-Vorabversionspaket 1.0.781 ist veraltet.  Beenden Sie die Entwicklung mit Paket 1.0.781.  

> [!IMPORTANT]
> Das WebView2-Vorabversionspaket 0.9.430 ist veraltet und wird mit der nächsten Version entfernt.  Wenn Ihre WebView-App das Paket verwendet, empfiehlt das WebView-Team, zu einem neueren Paket zu wechseln.  

#### <a name="features"></a>Features  

*   [TrySuspend- und Resume-Methode][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] zum Anhalten und Fortsetzen von WebViews hinzugefügt.  
*   [SetVirtualHostNameToFolderMapping-Methode][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] hinzugefügt, die einen virtuellen Hostnamen einem Verzeichnispfad zu ordnet.  \([\#37][GithubMicrosoftedgeWebviewfeedbackIssue37], [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]und [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Die [DefaultBackgroundColor-Eigenschaft][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] wurde hinzugefügt, um die Farbe und den Alphakanal des Hintergrunds festlegen.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Die [UserAgent-Eigenschaft wurde][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] hinzugefügt, um den Benutzer-Agent zu erhalten oder zu festlegen.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Die Methode `CreateCookieWithCookie` wurde durch die Methode `CopyCookie` ersetzt.  
*   Unterstützung für visuelles Hosting mithilfe der [ICoreWebView2CompositionController-Schnittstelle][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] hinzugefügt, die mit der neuen `CreateCoreWebView2CompositionController` Methode von erstellt `ICoreWebView2Environment3` wird.  
    
#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Das Feature Microsoft Edge Shopping in WebView2 wurde deaktiviert.  
*   Das Kontextmenü im PDF-Viewer wurde deaktiviert, wenn `AreDefaultContextMenusEnabled` `false` .  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Ein Fehler wurde behoben, der beim Abfragen von zurückgegeben `E_NOINTERFACE` `ICoreWebView2` `ICoreWebView2Experimental` wurde.  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Es wurde ein Fehler behoben, der die Navigation mit falsch formatierten URIs erlaubte, wenn `CoreWebView2NavigationStartingEventArgs.Cancel` dieser auf festgelegt `false` wurde.  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Es wurde ein Fehler behoben, der in Popupfenstern mit Ereignishandlern blockiert wurde, die `window.print()` an Ereignisse angefügt `NewWindowRequested` waren.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Problem mit dynamischem DPI beim Verschieben von Apps zwischen verschiedenen Monitoren behoben.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Die `HRESULT` Instanzen, die von [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke übergeben wurden, wurden verbessert.][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]  
*   Schaltfläche "Automatisches Ausfüllen verwalten" deaktiviert.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Fehler Visual Studio während der Ausführung behoben, `WebView2.Dispose` wenn sie in mehreren Fenstern gehostet werden.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\) und [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Fehler zum Anzeigen des WebView2-Steuerelements in der toolbox Visual Studio behoben.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Reduzierte Probleme mit der hohen CPU-Auslastung.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Probleme mit dem veralteten 1.0.781-prerelease-Paket wurden behoben.  \([\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] und [\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
#### <a name="promotions"></a>Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable heraufgestuft.  
    *   Visuelle Hosting-APIs  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
        
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   Fehler behoben, bei dem WebView-Apps abgestürzt sind, die das WPF SDK verwenden.  Der Absturz ist aufgetreten, als Sie `F4` ausgewählt haben, ein Fenster zu schließen.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   Der WebView2-Initialisierungsbildschirm ist nun transparent statt grau.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## <a name="1070550"></a>1.0.705.50  

Veröffentlichungsdatum: 25. Januar 2021  

[NuGet -Paket][NuGetGallery1.0.705.50] \| WebView2 Runtime Version 86.0.616.0 oder neuer  

### <a name="general"></a>Allgemein  

#### <a name="promotions"></a>Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable heraufgestuft.  
    *   [WebResourceResponseReceived-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest-API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [Cookieverwaltungs-API][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [WebView Environment-Eigenschaft][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  

## <a name="10721-prerelease"></a>1.0.721-prerelease  

Veröffentlichungsdatum: 8. Dezember 2020  

[NuGet -Paket][NuGetGallery1.0.721-prerelease] \| Microsoft Edge Version 86.0.616.0 oder neuer  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Breaking Change**: WebView2-Vorabversionspaket 1.0.707 und Paket 0.9.628 sind veraltet.  Beenden Sie die Entwicklung mit Paket 1.0.707 und package0.9.628.  

#### <a name="features"></a>Features  

*   [WebView2-Gruppenrichtlinien hinzugefügt.][DeployedgeMicrosoftEdgeWebviewPolicies]  Weitere Informationen zu empfohlenen Methoden finden Sie unter [Gruppenrichtlinien für WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Breaking Change**: Veralteter alter Registrierungsspeicherort.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Unterstützung für [Drag and Drop][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] in WebView2 hinzugefügt.  
*   APIs zur Verarbeitung der DPI-Unterstützung hinzugefügt.  
    *   Die [RasterizationScale-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] wurde hinzugefügt, um die DPI-Skalierung für WebView-Inhalte und Benutzeroberflächenpopups und das zugehörige [RasterizationScaleChanged-Ereignis zu][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] ändern.  
    *   Die [ShouldDetectMonitorScaleChanges-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] wurde hinzugefügt, um die Eigenschaft bei `RasterizationScale` Bedarf automatisch zu aktualisieren.  
    *   [BoundsMode-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] hinzugefügt, um anzugeben, dass es sich bei den Begrenzungen um Logikpixel handelt und WebView für die WebView2-Pixelanzeige verwendet werden kann, und WebView verwendet das mit, um die physische Größe `RasterizationScale` `RasterizationScale` zu `Bounds` erhalten.  
*   Zu `NewWindowRequested` behandelnde und `Ctrl` + `click` aktualisiertes `Shift` + `click` Ereignis.  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] und [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Die folgenden experimentellen APIs werden nun zu Stable heraufgestuft.  
    *   [WebResourceResponseReceived-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest-API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [Cookieverwaltungs-API][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [WebView Environment-Eigenschaft][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
### <a name="net"></a>.NET  

#### <a name="features"></a>Features  

*   Aktivierter WinForms-Designer in .NET Core 3.1+ und .NET 5.  
*   Verbesserte .NET-Cookieverwaltung.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Ersetzt `CoreWebView2Ready` durch [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  

#### <a name="bug-fixes"></a>Fehlerbehebungen

*   [AcceleratorKeyPressed-Ereignis][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] zur Unterstützung der `AcceleratorKey` Auswahl in WebView2 hinzugefügt.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Unnötige Dateien wurden aus der Ausgabe in WebView2-Ordner entfernt.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   Verbesserte Hostobjekt-API.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] und [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## <a name="1066437"></a>1.0.664.37  

Veröffentlichungsdatum: 20. November 2020  

[NuGet -Paket][NuGetGallery1.0.664.37] \| WebView2 Runtime Version 86.0.616.0 oder neuer  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Ankündigung**: .NET WPF/WinForms WebView2 SDKs sind jetzt allgemein verfügbar \(GA\).  Ab dieser Version sind Release-SDKs vorwärtskompatibel.  Weitere Informationen finden Sie im Blogbeitrag [zur GA-Ankündigung.][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]  

#### <a name="features"></a>Features  

*   .NET WPF/WinForms WebView2 ist jetzt allgemein verfügbar \(GA\).  
*   Fixed Distribution \(Bring-your-own\) mode reached GA.  
    
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Fehlerbehebungen  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` verhindert, dass ein neues Fenster geöffnet wird.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] und [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## <a name="10674-prerelease"></a>1.0.674-prerelease  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet -Paket][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime Version 86.0.616.0 oder neuer  

### <a name="general"></a>Allgemein  

*   Die [NavigateWithWebResourceRequest-Methode][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] wurde hinzugefügt, um während der Navigation Postdaten oder andere Anforderungsheader zur Verfügung zu stellen.  
*   [DOMContentLoaded-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] hinzugefügt, das ausgeführt wird, wenn das ursprüngliche HTML-Dokument geladen und analysiert wird.  
*   Die [Environment-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] wurde in WebView2 hinzugefügt.  Diese Eigenschaft macht die WebView2-Umgebung verfügbar, in der eine Instanz von WebView2 erstellt wurde.  
*   [Hinzugefügte][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] Cookieverwaltungs-APIs, mit denen Entwickler die WebView2-Sitzung authentifizieren oder Cookies aus WebView abrufen können, um andere Tools zu authentifizieren.  Das Webview-Team plant, sprach- oder frameworkspezifische Verbesserungen vorzunehmen.  Weitere Informationen finden Sie unter [API Review: Cookie Management][GithubMicrosoftedgeWebview2AnnouncementIssue2].  
*   Das [WebResourceResponseReceived-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] wurde aktualisiert und unveränderliche [WebResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] und [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] zu [WebResourceResponseView::GetContent hinzugefügt.][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]  
*   Deaktivierte [Microsoft Defender Application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] in WebView2.  
*   [SystemCursorId für][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] visuelles Hosting hinzugefügt.  
*   Fehler wurde für die Input-Methode in Visual Hosting behoben.  
*   Entfernt enthält die Anforderung `version.lib` für die Verwendung der statischen WebView2-Bibliothek.  
    
### <a name="net"></a>.NET  

*   Die [CoreWebView2-Klasse][DotnetApiMicrosoftWebWebview2CoreCorewebview2] wurde aktualisiert, um die Variable `CoreWebView2Environment` verfügbar zu machen.  
*   Implementierungen benutzerdefinierter EventArgs-Klassen im Namespace wurden in Unterklassen von `Microsoft.Web.WebView2.Core` [System.EventArgs][DotnetApiSystemEventargs] oder [System.ComponentModel.CancelEventArgs geändert.][DotnetApiSystemComponentmodelCancelEventargs]  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Unterstützung für [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] in WinForms hinzugefügt.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET-APIs hinzugefügt.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Die WinForms Designer [Source-Eigenschaft][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] wurde standardmäßig aktualisiert oder auf NULL zurückgesetzt.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   WebView2-Grenzen in WebView2.Init() aktualisiert, um DPI-Modi zu unterstützen, die weniger als 100 % sind.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   [BuildWindowCore und][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [DestroyWindowCore wurden][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] aktualisiert, um die Robustheit zu erhöhen.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Die .NET Loader-Basis wurde aktualisiert, um das Prozessbit anstelle der Betriebssystemarchitektur zu laden.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Umbenannt `EdgeNotFoundException` in [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## <a name="1062222"></a>1.0.622.22  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet -Paket][NuGetGallery1.0.622.22] \| WebView2 Runtime Version 86.0.616.0 oder neuer  

### <a name="general"></a>Allgemein  

> [!IMPORTANT]
> **Ankündigung**: Win32 C/C++ WebView2 ist jetzt allgemein verfügbar \(GA\).  Ab dieser Version sind Release-SDKs vorwärtskompatibel.  Weitere Informationen finden Sie im Blogbeitrag [zur GA-Ankündigung.][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]  

*   [Evergreen WebView2 Runtime und Installer][Webview2ConceptsDistributionUnderstandRuntimeInstaller] sind GA.  Bootstrapper, Downlinklink für den Bootstrapper und eigenständiges Installationsprogramm für die Evergreen WebView2 Runtime sind unter [Microsoft Edge WebView2 verfügbar.][MicrosoftDeveloperMicrosoftEdgeWebView2]  Beispielcode für den Installationsworkflow ist auch im [WebView2Samples-Repository verfügbar.][GithubMicrosoftedgeWebview2samplesMain]  
*   [Der Modus "Feste Version"][Webview2ConceptsDistributionFixedVersionDistributionMode] ist für die Entwicklervorschau verfügbar.  
    
## <a name="0962211"></a>0.9.622.11  

Veröffentlichungsdatum: 10. September 2020  

[NuGet -Paket][NuGetGallery0.9.622.11] \| WebView2 Runtime Version 86.0.616.0 oder neuer  

### <a name="general"></a>Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: This SDK is the Release Candidate for WebView2 Win32 C/C++ GA.  Die GA-Version sollte dieselbe API-Schnittstelle und -Funktionalität verwenden.  
    
*   Getrennte [Browserrichtlinien][DeployedgeMicrosoftEdgePolicies].  
*   [AllowSingleSignOnUsingOSPrimaryAccount-Eigenschaft][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] wurde zu WebView2-Umgebungsoptionen hinzugefügt, um den bedingten Zugriff für WebView zu aktivieren.  
*   Wird `ICoreWebView2NewWindowRequestedEventArgs` aktualisiert, [um die WindowFeatures-Eigenschaft][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] und die zugeordneten [ICoreWebView2WindowFeatures -Eigenschaften zu enthalten.][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Wird `System.Windows.Rect`  für die Verwendung anstelle von `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\) aktualisiert.  
*   Das NewWindowRequested-Ereignis wurde aktualisiert, um `window.open()` die Anforderung ohne Parameter zu verarbeiten.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] specified with `ICoreWebView2EnvironmentOptions` aren't overridden with environment variables or registry values.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions].  
    
## <a name="09579"></a>0.9.579  

Veröffentlichungsdatum: 20. Juli 2020  

[NuGet -Paket][NuGetGallery0.9.579] \| Microsoft Edge Version 86.0.579.0.  

### <a name="general"></a>Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: Evergreen WebView2 Runtime and installer is released for preview.  Weitere Informationen finden Sie unter [Verteilung von WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller].  
    
*   > [!IMPORTANT]
    > **Ankündigung**: Die folgenden WebView2 SDK-Versionen werden nach der nächsten SDK-Version nicht mehr unterstützt.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Die WebView2-SDK-Versionen werden auch als veraltet gekennzeichnet, wenn nuget.org.  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem neuesten Stand zu bleiben.  
    
*   Verbesserungen des WebView-Arbeitsthreads hinzugefügt.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Popupblocker in WebView deaktiviert.  Weitere Informationen finden Sie im Ereignis zur [IsUserInitiated-Eigenschaft.][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] `NewWindowRequested`  
*   Sichergestellt, dass das Startereignis für die WebView-Navigation für ausgeführt `about:blank` wird.  Jetzt werden Ereignisse für alle Navigationen ausgeführt, aber Absagen für oder des Elements werden nicht unterstützt `NavigationStarting` `about:blank` und `srcdoc` `iframe` ignoriert.  
*   Blockierte `edge://` einige URI-Schemas in WebView.  
*   Experimentelle [IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] zu WebView2-Umgebungsoptionen hinzugefügt, um den bedingten Zugriff für WebView zu aktivieren.  
*   Es wurde ein experimentelles [WebResourceResponseReceived-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] hinzugefügt, das ausgeführt wird, nachdem WebView die Antwort einer WebResource-Anforderung empfängt und verarbeitet.  Authentifizierungsheader sind, falls vorhanden, im Antwortobjekt enthalten.  
    
### <a name="net"></a>.NET  

*   Verbesserte Behandlung des WPF-Fokus.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Eigenschaft `ZoomFactor` auf dem WPF Webview2 Controller hinzugefügt.  
    
## <a name="09538"></a>0.9.538  

[NuGet -Paket][NuGetGallery0.9.538] \| Microsoft Edge Version 85.0.538.0.  

### <a name="general"></a>Allgemein  

*   Unterstützung für WebView2 SDK, Version [0.8.149, wird nicht mehr unterstützt.](#08149)  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem neuesten Stand zu bleiben.  
*   Die Gruppenrichtlinie wurde aktualisiert, um zu berücksichtigen, wann der Profilpfad des Microsoft Edge geändert wird \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
### <a name="win32-cc"></a>Win32 C/C++  

*   [ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]hinzugefügt, das ausgeführt wird und `window.open()` [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\) zugeordnet wird.  
*   > [!IMPORTANT]
    > **Breaking Change**: Veraltete [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] und ersetzt durch [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Um sicherzustellen, dass die WebView2-API den Windows-API-Benennungskonventionen entspricht, hat das WebView-Team die Folgenden aktualisiert.  
    > 
    > *   [AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] ist jetzt [AreHostObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed].  
    
*   [AddHostObjectToScript wurde aktualisiert.][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]  Die ursprünglichen Serialisierungsmarkierungen des Hostobjekts werden nun auf die Proxyobjekte festgelegt.  Anschließend werden Die Serialisierungsmarker des Hostobjekts als Hostobjekt serialisiert, wenn sie als Parameter im[JavaScript-Rückruf][GithubMicrosoftedgeWebviewfeedbackIssue148]\( #148 \) übergeben werden.  
    
### <a name="net-09538-pre-release"></a>.NET (0.9.538 Pre-Release)  

*   Veröffentlichte WinForms- und WPF WebView2API-Beispiele, die umfassende Anleitungen des WebView2 SDK sind.  Weitere Informationen finden Sie unter [Samples Repo][GithubMicrosoftedgeWebview2samplesMain].  
*   Unterstützung für visuelle Hosting- und Fensterfeatures für [experimentelle APIs hinzugefügt.][Webview2ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Breaking Change**: Die folgenden Verschiebungen implementieren jetzt IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]und [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] und [CompareBrowserVersions wurden][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] als [CoreWebView2Environment-Statik][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] hinzugefügt.  
    
## <a name="09515-prerelease"></a>0.9.515-prerelease  

[NuGet -Paket][NuGetGallery0.9.515-prerelease] \| Microsoft Edge Version 84.0.515.0.  

*   > [!IMPORTANT]
    > **Ankündigung**: WebView2 unterstützt jetzt Windows Formulare und WPF auf .NET Framework 4.6.2 oder höher und .NET Core 3.0 oder höher im **Vorabversionspaket**.  
    
*   Weitere Informationen zum Erstellen von WPF-Apps finden Sie im [WPF Getting Started Guide][Webview2GettingstartedWpf] und in der WebView2-WPF-Referenz für WPF-spezifische APIs. [][DotnetApiMicrosoftWebWebview2Wpf]  
*   Weitere Informationen zum Erstellen von Windows Forms-Apps finden Sie im [Windows Forms Getting Started Guide][Webview2GettingstartedWinforms] und im WebView2 Windows Forms [Reference][DotnetApiMicrosoftWebWebview2Winforms] for Windows Forms specific APIs.  
*   Weitere Informationen zu den CoreWebView2-APIs finden Sie unter [.NET Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Bekannte Probleme:** Das WebView-Team ist sich einiger Probleme in der Vorabversion bewusst, die in zukünftigen Versionen behoben werden.  
    > 
    > *   **DPI-Bewusstsein:** WebView2 für WPF ist derzeit nicht DPI-bewusst.  Beim Initialisieren von WebView2 auf Monitoren mit hohem DPI gibt es ein bekanntes Problem, bei dem die WebView zunächst als Bruchteil des Fensters initialisiert wird, bis die Größe des Fensters geändert wird.  
    > *   **WPF Designer**: Der WPF-Designer wird derzeit nicht unterstützt.  Fügen Sie das WebView2-Steuerelement in Ihrer App hinzu, indem Sie das entsprechende XAML direkt in einem Texteditor ändern.  
    
## <a name="09488"></a>0.9.488  

[NuGet -Paket][NuGetGallery0.9.488] \| Microsoft Edge Version 84.0.488.0.  

*   > [!IMPORTANT]
    > **Ankündigung**: Ab der bevorstehenden Microsoft Edge Version 83 zielt Evergreen WebView nicht mehr auf den Stable-Browserkanal ab.  Stattdessen richtet sie sich an eine andere Reihe von Binärdateien, [die als Evergreen WebView2 Runtime][Webview2ConceptsDistributionEvergreenDistributionMode]bezeichnet werden, die Sie über ein Installationsprogramm, das das WebView-Team derzeit entwickelt, verketten können.  Weitere Informationen finden Sie unter [App-Distribution][Webview2ConceptsDistribution].  
    
*   > [!IMPORTANT]
    > **Ankündigung**: Das WebView-Team veröffentlicht zwei Pakete: ein Pre-Release-Paket mit experimentellen APIs \(damit Sie testen können\) und ein stabiles Releasepaket mit stabilen APIs \(für Ihre Sicherheit\).  Um mehr über die Unterschiede zu erfahren, navigieren Sie zu [Grundlegendes zu Browserversionen und WebView2][Webview2ConceptsVersioning].  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Um sicherzustellen, dass die WebView2-API den Windows-API-Benennungskonventionen entspricht, hat das WebView-Team die Namen der folgenden Schnittstellen aktualisiert.  
    > 
    > *   `CORE_WEBVIEW2_*` Präfix ist jetzt `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] ist jetzt [GetAvailableCoreWebView2BrowserVersionString][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] ist jetzt [get_BrowserVersionString][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring].  
    > *   [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] ist jetzt [AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] ist jetzt [RemoveHostObjectFromScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` ist jetzt `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Die `AddRemoteObject` JS-Proxymethoden werden ebenfalls umbenannt.  
    > 
    > *   `getLocal` ist jetzt `getLocalProperty` .  
    > *   `setLocal` ist jetzt `setLocalProperty` .  
    > *   `getRemote` ist jetzt `getHostProperty` .  
    > *   `setRemote` ist jetzt `setHostProperty` .  
    > *   `applyRemote` ist jetzt `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Veraltete [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] und ersetzt durch [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   [FrameNavigationCompleted-Ereignis][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted] hinzugefügt.  Wenn nun ein Element die Navigation abgeschlossen hat, wird ein Ereignis ausgeführt und gibt den Erfolg der Navigation und `iframe` der Navigations-ID zurück.  
*   [ICoreWebView2EnvironmentOptions-Schnittstelle][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] hinzugefügt, die verwendet werden kann, um die Version der Evergreen WebView2 Runtime zu bestimmen, die von Ihrer App bestimmt wird.  
*   [IsBuiltInErrorPageEnabled-Einstellung][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled] hinzugefügt.  Jetzt können Sie die integrierte Fehlerwebseite für Navigationsfehler und Renderprozessfehler aktivieren oder deaktivieren.  
*   Die Remoteobjektinjektion wurde aktualisiert, um `IDispatch` .NET-Implementierungen \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\) zu unterstützen.  
*   Das [NewWindowRequested-Ereignis][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] wurde aktualisiert, um Anforderungen aus Kontextmenüs \( #108 \)[zu][GithubMicrosoftedgeWebviewfeedbackIssue108]verarbeiten.  
*   Das erste separate WebView2-Vorabversionspaket wurde veröffentlicht, in dem Sie auf visuelle Hosting-APIs zugreifen können.  Das WebView-Team hat [APISample aktualisiert,][GithubMicrosoftedgeWebview2samplesMain] um die neuen experimentellen APIs zu integrieren.  
    *   [ICoreWebView2ExperimentalCompositionController-Schnittstelle][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] hinzugefügt, um eine Verbindung mit einer Kompositionsstruktur herzustellen und Eingaben für webView zu liefern.  
    *   [ICoreWebView2ExperimentalPointerInfo][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]hinzugefügt, die alle Informationen aus einem `POINTER_INFO` enthält.  Dieses Objekt wird an SendPointerInput übergeben, um Zeigereingaben in die WebView zu injizieren.  
    *   [ICoreWebView2ExperimentalCursorChangedEventHandler][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]hinzugefügt, das der App mitteilt, wann der Mauszeiger über der WebView geändert werden soll.  Wenn sich die Maus über einem Textfeld in der WebView befindet, wechselt der Cursor vom Pfeil zum Auswahlfeld.  Die Eigenschaft auf der teilt der App mit, was der Mauszeiger `cursor` `CompositionController` derzeit für die WebView sein soll.  
        
## <a name="09430"></a>0.9.430  

[NuGet -Paket][NuGetGallery0.9.430] \| Microsoft Edge Version 82.0.430.0.  

Das WebView2 SDK ist die offizielle Win32 C++-Betaversion, die mehrere Featureanforderungen aus Feedback enthält.  Das WebView-Team versucht, die Anzahl der Versionen mit änderungen zu begrenzen.  Wenn sich die allgemeine Verfügbarkeit nähert, werden in die Betaversion einige wichtige wichtige Änderungen einbezogen.  

*   > [!IMPORTANT]
    > **Breaking Change**: Wenn sich die endgültige Version nähert, hat das WebView-Team das Präfix in umbenannt, um sicherzustellen, dass die `IWebView2WebView` `ICoreWebView2` WebView2-API mit der Windows-API-Benennungskonvention in Einklang steht.  Um das WebView2 SDK aus Benutzeroberflächenframeworks nutzen zu können, wurde das WebView-Team in `ICoreWebView2` [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] und [ICoreWebView2Host getrennt.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430]  `ICoreWebView2Host` unterstützt die Größenänderung, das Ein- und Ausblenden, das Fokussieren und andere Funktionen im Zusammenhang mit Fenstern und Komposition.  ICoreWebView2 unterstützt alle anderen WebView2-Funktionen.  Um mehr über das Integrieren der Änderungen zu [][GithubMicrosoftedgeWebview2samplesPr17] erfahren, navigieren Sie zur WebView2-Pullanforderung im WebView2-APISample-Projekt. [][GithubMicrosoftedgeWebview2samplesMain]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Teilen [Sie DocumentStateChanged][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] in drei Komponenten auf:  [SourceChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged], [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]und [HistoryChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged].  Wenn sich nun die Quell-URL ändert, `SourceChanged` wird das Ereignis ausgeführt.  Wenn der Verlaufsstatus geändert wird, `HistoryChanged` wird das Ereignis ausgeführt.  Das `ContentLoading` Ereignis wird vor dem ersten Skript ausgeführt, wenn ein neues Dokument geladen wird.  
    
*   Unterstützung für die ARM64-Architektur hinzugefügt.  
*   Unterstützung des Soft Input Panels \(SIP\) für Touchscreengeräte hinzugefügt.  
*   Unterstützung für Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 und Windows Server 2016.  
*   [NotifyParentWindowPositionChanged][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] wurde hinzugefügt, damit die Statusleiste dem Fenster im Fenstermodus folgt.  Implementieren Sie außerdem die Änderung im fensterlosen Modus, damit Barrierefreiheitsfunktionen funktionieren.  
*   Einstellung [AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] hinzugefügt, um global zu steuern, ob auf eine Webseite von Remoteobjekten zugegriffen werden kann.  Standardmäßig ist `AreRemoteObjectsAllowed` dies aktiviert, sodass von [AddRemoteObject hinzugefügte Remoteobjekte][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] von der Webseite aus zugänglich sind.  Wenn die Objekt deaktiviert sind, kann `AreRemoteObjectsAllowed` nicht über die Webseite auf die Objekte zugegriffen werden.  Änderungen werden für das nächste Navigationsereignis angewendet.  
*   Die [IsZoomControlEnabled-Einstellung][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] wurde hinzugefügt, um zu verhindern, dass Benutzer den Zoom der WebView mithilfe von `ctrl` + `+` `ctrl` + `-` und `ctrl` \(oder + Mausrad\) auswirken.  Der Zoom kann weiterhin mithilfe von put_ZoomFactor [festgelegt][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] werden, wenn die Einstellung deaktiviert ist.  
*   ZoomFactor wurde geändert, um nur auf die aktuelle WebView anzuwenden.  Zoomänderungen an der aktuellen WebView wirken sich nicht auf andere WebViews aus, zu der Sie mit derselben Ursprungswebsite navigiert haben.  Weitere Informationen finden Sie unter [get_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor].  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   [SetBoundsAndZoomFactor wurde hinzugefügt.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]  Jetzt können Sie den Zoomfaktor und die Grenzen einer WebView gleichzeitig festlegen.  
*   [WindowCloseRequested-Ereignis][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] hinzugefügt.  Weitere Informationen finden Sie unter [add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Unterstützung für den `beforeunload` Dialogfeldtyp für [][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind] JavaScript-Dialogereignisse hinzugefügt und CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD Enumerationseintrag hinzugefügt.  
*   [GetHeaders][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] zu HttpRequestHeaders, [][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] [GetHeader][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] zu HttpResponseHeaders und get_HasCurrentHeader httpHeadersCollectionIterator hinzugefügt.  
*   > [!IMPORTANT]
    > **Breaking Change**: Geändertes `DevToolsProtocolEventReceived` Verhalten.  Jetzt können Sie ein [DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] für ein bestimmtes DevTools-Protokollereignis [][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]erstellen und ein solches Ereignis mithilfe von add_DevToolsProtocolEventReceived / [remove_DevToolsProtocolEventReceived.][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: `WebMessageReceivedEventArgs` [][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] Get_WebMessageAsString-Eigenschaft in eine [TryGetWebMessageAsString-Methode][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring] geändert.  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Die `AcceleratorKeyPressedEventArgs` [Handle-Methode][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] wurde in eine [get_Handled][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled] geändert.  
    
## <a name="08355"></a>0.8.355  

[NuGet -Paket][NuGetGallery0.8.355] \| Microsoft Edge Version 80.0.355.0.  

*   Veröffentlichtes WebView2API-Beispiel, ein umfassendes Handbuch des WebView2 SDK.  Weitere Informationen finden Sie unter [API Sample][GithubMicrosoftedgeWebview2samplesApisample].  
*   ImE-Unterstützung für alle Sprachen neben Englisch \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\) hinzugefügt.  
*   Die #A0 des `WebResourceRequested` Ereignisses wurde als Reaktion auf Fehlerberichte aktualisiert.  Das gleichzeitige Angeben eines Filters und eines Ereignisses bei der Erstellung ist nun veraltet.  Verwenden Sie zum Erstellen eines [angeforderten][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] Webressource-Ereignisses add_WebResourceRequested, um das Ereignis hinzuzufügen, und [addWebResourceRequestedFilter,][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] um einen Filter hinzuzufügen.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] entfernt den Filter \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Breaking Change**: Geändertes Vollbildverhalten.  Veraltet [isFullScreenAllowed][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated].  Wenn ein Element in einer WebView \(z. B. einem Video\) auf Vollbild festgelegt ist, werden nun standardmäßig die Grenzen der WebView gefüllt.  Verwenden Sie [das ContainsFullScreenElementChanged-Ereignis][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] und [get_ContainsFullScreenElement,][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement] um anzugeben, wie die App die WebView-Größe ändern soll, wenn ein Element in den Vollbildmodus wechseln soll.  
    
## <a name="08314"></a>0.8.314  

[NuGet -Paket][NuGetGallery0.8.314] \| Microsoft Edge Version 80.0.314.0.  

*   Unterstützung für Windows 7, Windows 8 und Windows 8.1.  
*   Unterstützung Visual Studio und Visual Studio Code für WebView2 hinzugefügt.  Debuggen Sie nun Ihr Skript in WebView2 direkt von Ihrer IDE aus.  Weitere Informationen finden Sie unter [How to debug when developing with WebView2 controls][Webview2HowtoDebug].  
*   Für das ausgeführte Skript in WebView2 hinzugefügt, um über die Win32-Komponente der App auf ein IDispatch-Objekt zu zugreifen und auf die Eigenschaften des `Native Object Injection` IDispatch-Objekts zu zugreifen.  Weitere Informationen finden Sie unter [AddRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Ereignis `AcceleratorKeyPressed` hinzugefügt.  Weitere Informationen finden Sie unter [add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Deaktiviert die `Context Menus` .  Weitere Informationen finden Sie unter [put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Aktualisiert `DPI Awareness` .  Jetzt ist das DPI-Bewusstsein von WebView mit dem DPI-Bewusstsein der Host-App identisch.  
    
    > [!NOTE]
    > Wenn eine andere Hybrid-App mit einer anderen DPI-Sensibilisierung als die ursprüngliche WebView gestartet wird, wird die neue WebView nicht gestartet, wenn die `user data folder` identisch ist \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Aktualisiert, `Notification Change Behavior` damit WebView2 automatisch Benachrichtigungsberechtigungsanforderungen ablehnt, die von Webinhalten, die in WebView gehostet werden, aufgefordert werden.  
    
## <a name="08270"></a>0.8.270  

[NuGet -Paket][NuGetGallery0.8.270] \| Microsoft Edge Version 78.0.270.0.  

*   Ereignis `DocumentTitleChanged` zum Angeben der Dokumenttiteländerung \([\#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\) hinzugefügt.  
*   API `GetWebView2BrowserVersionInfo` \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\) hinzugefügt.  
*   Ereignis `NewWindowRequested` hinzugefügt.  
*   Die `CreateWebView2EnvironmentWithDetails` Funktion wurde aktualisiert, um zu `releaseChannelPreference` entfernen.  Weitere Informationen zur Funktion `CreateWebView2EnvironmentWithDetails` finden Sie unter [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Die Außerkraftsetzung der Registrierungs- und Umgebungsvariablen wird weiterhin unterstützt.  Die Standardkanaleinstellung wird verwendet, es sei denn, sie wird überschrieben.  
    Während der Kanalsuche überspringt das WebView-Team alle vorherigen Kanalversion, die nicht mit dem WebView2 SDK kompatibel ist.  
    Das WebView-Team wählt den stabileren Kanal aus, um das konsistenteste Verhalten für den Endbenutzer sicherzustellen.  Wenn Sie mit den neuesten Canary-Builds testen, sollten Sie ein Skript zum Festlegen der Umgebungsvariablen erstellen, `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` bevor Sie die App `1` starten.  
*   Die Funktion `CreateWebView2EnvironmentWithDetails` wurde mit Logik für die Auswahl `userDataFolder` aktualisiert, wenn sie nicht angegeben wurde.  Weitere Informationen zur Funktion `CreateWebView2EnvironmentWithDetails` finden Sie unter [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Wenn Sie zuvor den Standardspeicherort verwendet haben, wird beim Wechseln zum neuen SDK die Standardeinstellung \(auf einen neuen Speicherort im Hostcodeverzeichnis\) zurückgesetzt, und ihr Status wird ebenfalls `userDataFolder` `userDataFolder` zurückgesetzt.  Wenn der Hostprozess nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis verfügt, kann `CreateWebView2EnvironmentWithDetails` die Funktion fehlschlagen.  Sie können die Daten aus dem alten in `user data folder` das neue Verzeichnis kopieren.  
    
## <a name="08230"></a>0.8.230  

[NuGet -Paket][NuGetGallery0.8.230] \| Microsoft Edge Version 77.0.230.0.  

*   API `Stop` hinzugefügt, um alle Navigations- und ausstehenden Ressourcen abruft \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Datei `.tlb` zum NuGet -Paket \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\) hinzugefügt.  
*   .NET-Projekte wurden der Installerliste im NuGet-Paket \([\#32 \)][GithubMicrosoftedgeWebviewfeedbackIssue32]hinzugefügt.  
    
## <a name="08190"></a>0.8.190  

[NuGet -Paket][NuGetGallery0.8.190] \| Microsoft Edge Version 77.0.190.0.  

*   Hinzugefügt, `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` um zu steuern, ob Benutzer DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\) öffnen können.  
*   Hinzugefügt, `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` um zu steuern, ob die Statusleiste angezeigt wird \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Hinzugefügt, `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` um zurück und vorwärts durch den Navigationsverlauf zu gehen.  
*   HTTP-Headertypen \( \) zum Anzeigen und Ändern von `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` HTTP-Headern in WebView hinzugefügt.  
*   32-Bit-WebView-Unterstützung auf 64-Bit-Computern \([\#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\) hinzugefügt.  
*   WebView IDL zum SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\) hinzugefügt.  
*   Lib zur Unterstützung von `IID\_\*` Schnittstellen-ID-Objekten \([\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\) hinzugefügt.  
*   Hinzugefügt: Pfad, Verknüpfung und automatisches Kopieren von DLL-Dateien in NuGet `TARGET` SDK.  
*   Die Anforderung wurde `window.open()` im Skript aktiviert.  
    
## <a name="08149"></a>0.8.149  

[NuGet -Paket][NuGetGallery0.8.149] \| Microsoft Edge Version 76.0.149.0.  

Erste Entwicklervorschauversion.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Immergrüner Verteilungsmodus – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Fester Versionsverteilungsmodus – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Verstehen der WebView2-Runtime und des Installationsprogramms – Verteilung von Anwendungen mithilfe von WebView2-| Microsoft Docs"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Gruppenrichtlinien für WebView2 – Verwalten von WebView2-Anwendungen | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft-Dokumentation"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Experimentelle APIs – Grundlegendes zu Browserversionen und WebView2-| Microsoft Docs"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Übereinstimmende WebView2-Laufzeitversionen – Verstehen der WebView2 SDK-| Microsoft Docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps | Microsoft Docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF | Microsoft Docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Debuggen bei der Entwicklung mit WebView2-Steuerelementen | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental2?view=webview2-1.0.865-prerelease&preserve-view=true#add_downloadstarting  "add_DownloadStarting - Schnittstelle ICoreWebView2Experimental2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment3?view=webview2-1.0.865-prerelease&preserve-view=true#updateruntime  "UpdateRuntime – Schnittstelle ICoreWebView2ExperimentalEnvironment3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalframe?view=webview2-1.0.865-prerelease&preserve-view=true#addhostobjecttoscriptwithorigins  "AddHostObjectToScriptWithOrigins - Schnittstelle ICoreWebView2ExperimentalFrame | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings4?view=webview2-1.0.865-prerelease&preserve-view=true#ispinchzoomenabled  "IsPinchZoomEnabled - Schnittstelle ICoreWebView2ExperimentalSettings4 | Microsoft Docs" 

[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings2?view=webview2-1.0.824&preserve-view=true#get_arebrowseracceleratorkeysenabled "get_AreBrowserAcceleratorKeyPressed - Schnittstelle ICoreWebView2ExperimentalSettings | Microsoft Docs" 

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - ICoreWebView2_2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping – ICoreWebView2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend – ICoreWebview2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled - Schnittstelle ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "Schnittstelle ICoreWebView2CompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor - Schnittstelle ICoreWebView2Controller2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived - Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived - Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest – Schnittstelle ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "schnittstelle ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount - Schnittstelle ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments - Schnittstelle ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo - Schnittstelle ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString - Schnittstelle ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "Schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalCompositionController3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalCompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged - Schnittstelle ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode - Schnittstelle ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale - Schnittstelle ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges - Schnittstelle ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled - Schnittstelle ICoreWebView2ExperimentalEnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures - Schnittstelle ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalPointerInfo | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent - Schnittstelle ICoreWebView2ExperimentalSettings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - Schnittstelle ICoreWebView2Experimentale | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - Schnittstelle ICoreWebView2Experimentale | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - Schnittstelle ICoreWebView2Experimentale | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager - Schnittstelle ICoreWebView2Experimentale | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment - Schnittstelle ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest – Schnittstelle ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent – Schnittstelle ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent – Schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalWindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "Schnittstelle ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor - Schnittstelle ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged – Schnittstelle ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor - Schnittstelle ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor - Schnittstelle ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader - Schnittstelle ICoreWebView2HttpHeadersCollectionIterator | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders – Schnittstelle ICoreWebView2HttpRequestHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader – Schnittstelle ICoreWebView2HttpResponseHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated-Schnittstelle ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures - Schnittstelle ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - Schnittstelle ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled - Schnittstelle ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - Schnittstelle ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled "get_IsBuiltInErrorPageEnabled - Schnittstelle ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed - Schnittstelle ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject – Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject – Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript – Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript - Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString - Schnittstelle ICoreWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke – Schnittstelle ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "Schnittstelle ICoreWebView2WindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle – Schnittstelle IWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "Schnittstelle IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled - Schnittstelle IWebView2Settings2 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated - Schnittstelle IWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString - Schnittstelle IWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed - Schnittstelle IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject – Schnittstelle IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested - Schnittstelle IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter - Schnittstelle IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement - Schnittstelle IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter – Schnittstelle IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged - Schnittstelle IWebView2WebView | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails – Globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo – Globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails – Globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – Globals | Microsoft-Dokumentation" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString – Globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – Globals | Microsoft-Dokumentation" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – Globals | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 – Richtlinien | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Microsoft.Web.WebView2.Core Namespace | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "CoreWebView2-Klasse (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "CoreWebView2Environment Class (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment.CompareBrowserVersions(String, String) Method (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "CoreWebView2Environment.GetAvailableBrowserVersionString(String) Method (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "CoreWebView2HttpRequestHeaders Class (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "CoreWebView2HttpResponseHeaders Class (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "CoreWebView2.NewWindowRequested Event (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "CoreWebView2.PermissionRequested Event (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "CoreWebView2.ScriptDialogOpening Event (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "CoreWebView2.WebResourceRequested Event (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "CoreWebView2InitializationCompletedEventArgs Class | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Namespace | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "CoreWebView2CreationProperties Class (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Webview2.Source Class (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft.Web.WebView2.Wpf Namespace | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "WebView2.BuildWindowCore(HandleRef) Method (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "WebView2.DestroyWindowCore(HandleRef) Method (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "CancelEventArgs Class (System.ComponentModel) | Microsoft Docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "EventArgs Class (System) | Microsoft Docs"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblys mit starkem | Microsoft Docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender Application Guard (Windows 10) – Windows Sicherheit | Microsoft Docs"  
[WindowsWin32ApiWinuserSetWindowDisplayAffinity]: /windows/win32/api/winuser/nf-winuser-setwindowdisplayaffinity "SetWindowDisplayAffinity-Funktion (winuser.h) – Win32-Apps | Microsoft Docs"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Ankündigungs-Repository für MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2WpfBrowser "WebView2WpfBrowser – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Verschieben des Projekts zur Verwendung der neuesten WebView2 SDK 0.9.430 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue506]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/506 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 506"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue568]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/568 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 568"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue604]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/604 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 604"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue669]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/669 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 669"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue851]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/851 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 851"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 878"  
[GithubMicrosoftedgeWebviewfeedbackIssue1120]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1120 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 1120"
[GithubMicrosoftedgeWebviewfeedbackIssue940]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/940 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 940"
[GithubMicrosoftedgeWebviewfeedbackIssue841]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/841 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 841"
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 210"
[GithubMicrosoftedgeWebviewfeedbackIssue338]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/338 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 338"
[GithubMicrosoftedgeWebviewfeedbackIssue589]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/589 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 589"
[GithubMicrosoftedgeWebviewfeedbackIssue933]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/933 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 933"
[GithubMicrosoftedgeWebviewfeedbackIssue946]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/946 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 946"
[GithubMicrosoftedgeWebviewfeedbackIssue1011]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1011 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 1011"
[GithubMicrosoftedgeWebviewfeedbackIssue1050]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1050 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 1050"
[GithubMicrosoftedgeWebviewfeedbackIssue996]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/996 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 996"
[GithubMicrosoftedgeWebviewfeedbackIssue850]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/850 "Feedback-Repository für MicrosoftEdge/WebViewFeedback Issue 850"

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Ankündigung der allgemeinen Verfügbarkeit Microsoft Edge WebView2 für .NET und Fixed Distribution Method | .NET Blog"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2-| Microsoft Edge Entwickler"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "NuGet Katalog | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "NuGet Katalog | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v0.9.515-Vorabversion"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "NuGet Katalog | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v0.9.628-Vorabversion"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.674-Vorabrelease"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.721-Vorabversion"  
[NuGetGallery1.0.774.44]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.774.44 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.774.44"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.790 prerelease"  
[NuGetGallery1.0.818.41]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.818.41 "NuGet Katalog | Microsoft.Web.WebView2 v1.0.818.41"  
[NuGetGallery1.0.824-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.824-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.824-Vorabversion"  
[NuGetGallery1.0.865-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.865-prerelease "NuGet Katalog | Microsoft.Web.WebView2 v1.0.865-Vorabversion"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Ankündigung Microsoft Edge WebView2 General Availability | Microsoft Edge Blog"  
