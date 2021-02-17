---
description: Versionshinweise für Microsoft Edge WebView2 SDK
title: Versionshinweise für Microsoft Edge WebView2 für Win32, WPF und WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/16/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 58f96dda9c05cfc10790e3523a494e42cf33ec12
ms.sourcegitcommit: 988c9add287abd203acf1d5d51ef7146e6f0b351
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/16/2021
ms.locfileid: "11339920"
---
# Versionshinweise für WebView2 SDK  

Das WebView2-Team aktualisiert [das WebView2 SDK][NuGetGallery] in einer sechswöchigen Kadenz.  In den folgenden Inhalten finden Sie aktuelle Informationen zu Produktankündigungen, Ergänzungen, Änderungen und änderungen an den APIs.  

> [!NOTE]
> Stellen Sie sicher, dass Sie Ihre App nach dem Aktualisieren des NuGet-Pakets erneut kompilieren.  Das Team empfiehlt die Verwendung des Canarykanals bei der Entwicklung mit den Vorabversionspaketen und der immergrünen Laufzeit bei der Verwendung veröffentlichter Pakete.  Weitere Informationen finden Sie unter [Versionsinformationen.][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]  
 
## 1.0.790-prerelease  

Veröffentlichungsdatum: 10. Februar 2021  

[NuGet-Paket][NuGetGallery1.0.790-prerelease] \| Microsoft Edge Version 86.0.616.0 oder neuer  

### Allgemein  

> [!IMPORTANT]
> **Breaking Change**: WebView2 pre-release package 1.0.781 is deprecated.  Stellen Sie die Entwicklung mit Paket 1.0.781 ein.  

> [!IMPORTANT]
> WebView2 Pre-Release-Paket 0.9.430 ist veraltet und wird aus der kommenden Version entfernt.  Wenn Ihre WebView-App das Paket verwendet, wird empfohlen, auf ein neueres Paket zu aktualisieren.  

##### Features  

*   [TrySuspend- und Resume-Methode][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] zum Anhalten und Fortsetzen von WebViews hinzugefügt.  
*   [SetVirtualHostNameToFolderMapping-Methode][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] hinzugefügt, die einen virtuellen Hostnamen einem Verzeichnispfad zu ordnet.  \([\#37][GithubMicrosoftedgeWebviewfeedbackIssue37], [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]und [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Die [DefaultBackgroundColor -Eigenschaft][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] wurde hinzugefügt, um die Farbe und den Alphakanal des Hintergrunds festlegen.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Die Eigenschaft ["UserAgent" wurde][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] hinzugefügt, um den Benutzer-Agent zu erhalten oder zu festlegen.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Die Methode `CreateCookieWithCookie` wurde durch die Methode `CopyCookie` ersetzt.  
*   Unterstützung für visuelles Hosting mithilfe der [ICoreWebView2CompositionController-Schnittstelle][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] hinzugefügt, die mit der neuen `CreateCoreWebView2CompositionController` Methode von erstellt `ICoreWebView2Environment3` wird.  

    
##### Fehlerbehebungen  

*   Das Microsoft Edge -Einkaufsfeature in WebView2 wurde deaktiviert.  
*   Das Kontextmenü im PDF-Viewer wurde deaktiviert, wenn `AreDefaultContextMenusEnabled` dies der Format `false` ist.  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Behebung eines Fehlers, der beim Abfragen von zurückgegeben `E_NOINTERFACE` `ICoreWebView2` `ICoreWebView2Experimental` wurde.  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Es wurde ein Fehler behoben, der die Navigation mit falsch formatierten URIs erlaubte, wenn `CoreWebView2NavigationStartingEventArgs.Cancel` dieser auf festgelegt `false` wurde.  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Behebung eines Fehlers, der in Popupfenstern blockiert wurde, bei dem `window.print()` Ereignishandler an Ereignisse angefügt `NewWindowRequested` waren.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Es wurde ein Dynamisches DPI-Problem beim Verschieben von Apps zwischen verschiedenen Monitoren behoben.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Die von `HRESULT` [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]übergebenen Instanzen wurden verbessert.  
*   Schaltfläche "Automatisches Ausfüllen verwalten" deaktiviert.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Behebung Visual Studio, die abstürzte, während `WebView2.Dispose` sie ausgeführt wird, wenn sie in mehreren Fenstern gehostet wurde.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\ und [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Behebung eines Fehlers zum Anzeigen des #A0 in Visual Studio Toolbox.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Reduzierte Hohe CPU-Auslastung.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Es wurden Probleme mit veraltetem 1.0.781-Vorabversionspaket behoben. [\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] und [\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
##### Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable heraufgestuft.  
    *   Visual Hosting-APIs.  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend und Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
    
#### .NET  

##### Fehlerbehebungen  

*   Behebung eines Fehlers, durch den #A0 abgestürzt sind, die das WPF SDK verwenden.  Der Absturz ist aufgetreten, als die Fenster mit der F4-TASTE geschlossen wurden.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   Der Initialisierungsbildschirm von WebView2 ist jetzt transparent statt grau.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## 1.0.705.50  

Veröffentlichungsdatum: 25. Januar 2021  

[NuGet-Paket][NuGetGallery1.0.705.50] \| WebView2 Runtime Version 86.0.616.0 oder neuer  

##### Promotions  

*   Die folgenden experimentellen APIs werden nun zu Stable heraufgestuft.  
    *   [WebResourceResponseReceived-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest-API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [Cookieverwaltungs-API][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [WebView Environment (Eigenschaft)][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  

## 1.0.721-prerelease  

Veröffentlichungsdatum: 8. Dezember 2020  

[NuGet-Paket][NuGetGallery1.0.721-prerelease] \| Microsoft Edge Version 86.0.616.0 oder neuer  

#### Allgemein  

> [!IMPORTANT]
> **Breaking Change**: WebView2 pre-release package 1.0.707 and package 0.9.628 are deprecated.  Stellen Sie die Entwicklung mit Paket 1.0.707 und package0.9.628 ein.  

###### Features  

*   [WebView2-Gruppenrichtlinien hinzugefügt.][DeployedgeMicrosoftEdgeWebviewPolicies]  Weitere Informationen zu empfohlenen Vorgehensweisen finden Sie unter ["Gruppenrichtlinien für WebView2".][Webview2ConceptsEnterpriseGroupPoliciesForWebview2]  
*   > [!IMPORTANT]
    > **Breaking Change**: Veralteter Registrierungsspeicherort.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Unterstützung für Drag [and Drop][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] in WebView2 hinzugefügt.  
*   APIs zum Behandeln der DPI-Unterstützung hinzugefügt.  
    *   Die [Eigenschaft "RasterizationScale"][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] wurde hinzugefügt, um die DPI-Skalierung für WebView-Inhalte und Benutzeroberflächenpopups und das zugehörige [RasterizationScaleChanged-Ereignis zu][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] ändern.  
    *   Die [Eigenschaft ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] wurde hinzugefügt, um die Eigenschaft bei Bedarf `RasterizationScale` automatisch zu aktualisieren.  
    *   Eigenschaft [BoundsMode hinzugefügt,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] um anzugeben, dass es sich bei den Grenzen um Logische Pixel handelt und WebView für die WebView2-Pixelanzeige verwendet werden kann, und WebView die mit der verwendet, um die physische Größe `RasterizationScale` `RasterizationScale` zu `Bounds` erhalten.  
*   Ereignis `NewWindowRequested` wurde aktualisiert, das zu behandeln `Ctrl` + `click` ist, und `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] und [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Die folgenden experimentellen APIs werden nun zu Stable heraufgestuft.  
    *   [WebResourceResponseReceived-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest-API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [Cookieverwaltungs-API][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded-API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [WebView Environment (Eigenschaft)][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
#### .NET  

###### Features  

*   Aktivierter WinForms Designer in .NET Core 3.1+ und .NET 5.  
*   Verbesserte .NET-Cookieverwaltung.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Ersetzt `CoreWebView2Ready` durch [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  

###### Fehlerbehebungen

*   Das [AcceleratorKeyPressed-Ereignis wurde][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] hinzugefügt, um die Tastendrucktaste in WebView2 zu unterstützen.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Unnötige Dateien wurden aus der Ausgabe in WebView2-Ordner entfernt.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   Verbesserte Hostobjekt-API.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] und [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## 1.0.664.37  

Veröffentlichungsdatum: 20. November 2020  

[NuGet-Paket][NuGetGallery1.0.664.37] \| WebView2 Runtime Version 86.0.616.0 oder neuer.  

#### Allgemein  

> [!IMPORTANT]
> **Ankündigung:**.NET WPF/WinForms WebView2-SDKs sind jetzt allgemein verfügbar \(GA\).  Ab dieser Version sind Release-SDKs vorwärtskompatibel.  Weitere Informationen finden Sie im Blogbeitrag zur [GA-Ankündigung.][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]  

###### Features  

*   .NET WPF/WinForms WebView2 ist jetzt allgemein verfügbar \(GA\).  
*   Der Feste Verteilungsmodus \(Bring-your-own\) hat den ga-Modus erreicht.  
    
#### .NET  

###### Fehlerbehebungen  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` verhindert, dass ein neues Fenster geöffnet wird.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] und [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## 1.0.674-prerelease  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet-Paket][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime Version 86.0.616.0 oder neuer.  

#### Allgemein  

*   Die [Methode NavigateWithWebResourceRequest wurde][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] hinzugefügt, um während der Navigation Postdaten oder andere Anforderungsheader zur Verfügung zu stellen.  
*   [DomContentLoaded-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] hinzugefügt, das ausgeführt wird, wenn das erste HTML-Dokument geladen und analysiert wird.  
*   Die Eigenschaft ["Environment"][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] wurde zu WebView2 hinzugefügt.  Diese Eigenschaft macht die WebView2-Umgebung verfügbar, in der eine Instanz von WebView2 erstellt wurde.  
*   [Cookieverwaltungs-APIs][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] hinzugefügt, mit denen Entwickler die WebView2-Sitzung authentifizieren oder Cookies aus WebView abrufen können, um andere Tools zu authentifizieren.  Das Webview-Team plant sprach- oder frameworkspezifische Verbesserungen.  Weitere Informationen finden Sie unter [API Review: Cookie Management][GithubMicrosoftedgeWebview2AnnouncementIssue2].  
*   Das [WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] -Ereignis wurde aktualisiert und unveränderliche [WebResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] und [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] zu [WebResourceResponseView::GetContent hinzugefügt.][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]  
*   Microsoft [Defender Application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] in WebView2 deaktiviert.  
*   [SystemCursorId für visuelles][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] Hosting hinzugefügt.  
*   Fehler für #A0 im visuellen Hosting wurde behoben.  
*   Zu den entfernten Informationen gehört die `version.lib` Anforderung für die Verwendung der statischen WebView2-Bibliothek.  
    
#### .NET  

*   Die [CoreWebView2-Klasse][DotnetApiMicrosoftWebWebview2CoreCorewebview2] wurde aktualisiert, um die Variable verfügbar zu `CoreWebView2Environment` machen.  
*   Implementierungen von benutzerdefinierten EventArgs -Klassen im Namespace in Unterklassen von `Microsoft.Web.WebView2.Core` [System.EventArgs][DotnetApiSystemEventargs] oder [System.ComponentModel.CancelEventArgs geändert.][DotnetApiSystemComponentmodelCancelEventargs]  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Unterstützung für [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] in WinForms hinzugefügt.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET-APIs hinzugefügt.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   WinForms Designer [Source-Eigenschaft][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] wurde auf "default" aktualisiert oder auf NULL zurückgesetzt.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Die Grenzen von WebView2 in WebView2.Init() wurden aktualisiert, um DPI-Modi zu unterstützen, die kleiner als 100 % sind.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   [BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] und [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] wurden aktualisiert, um die Robustheit zu erhöhen.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Die .NET Loader-Basis wurde aktualisiert, um das Prozessbit anstelle der Betriebssystemarchitektur zu laden.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Umbenannt `EdgeNotFoundExpection` in [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## 1.0.622.22  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet-Paket][NuGetGallery1.0.622.22] \| WebView2 Runtime Version 86.0.616.0 oder neuer.  

#### Allgemein  

> [!IMPORTANT]
> **Ankündigung**: Win32 C/C++ WebView2 ist jetzt allgemein verfügbar \(GA\).  Ab dieser Version sind Release-SDKs vorwärtskompatibel.  Weitere Informationen finden Sie im Blogbeitrag [zur GA-Ankündigung.][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]  

*   [Immergrüne WebView2 Runtime und Installer][Webview2ConceptsDistributionUnderstandRuntimeInstaller] sind GA.  Bootstrapper, downlink link for the Bootstrapper, and Standalone Installer for the Evergreen WebView2 Runtime are available on [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  Beispielcode für den Installationsworkflow ist auch im [WebView2Samples-Repository verfügbar.][GithubMicrosoftedgeWebview2samplesMain]  
*   [Der Modus "Feste Version"][Webview2ConceptsDistributionFixedVersionDistributionMode] ist für die Entwicklervorschau verfügbar.  
    
## 0.9.622.11  

Veröffentlichungsdatum: 10. September 2020  

[NuGet-Paket][NuGetGallery0.9.622.11] \| WebView2 Runtime Version 86.0.616.0 oder neuer.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung:** Dieses SDK ist der Release Candidate für WebView2 Win32 C/C++ GA.  Die ga-Version sollte dieselbe API-Schnittstelle und -Funktionalität verwenden.  
    
*   Getrennte [Browserrichtlinien][DeployedgeMicrosoftEdgePolicies].  
*   Die [Eigenschaft "AllowSingleSignOnUsingOSPrimaryAccount"][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] wurde zu den WebView2-Umgebungsoptionen hinzugefügt, um den bedingten Zugriff für WebView zu aktivieren.  
*   Aktualisiert `ICoreWebView2NewWindowRequestedEventArgs` mit [der WindowFeatures-Eigenschaft][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] und den zugeordneten [ICoreWebView2WindowFeatures][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622].  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Die `System.Windows.Rect`  Verwendung anstelle von `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\) wurde aktualisiert.  
*   Das Ereignis "NewWindowRequested" wurde aktualisiert, um die `window.open()` Anforderung ohne Parameter zu verarbeiten.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [Mit "AdditionalBrowserArguments"][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] angegebene Argumente werden nicht mit `ICoreWebView2EnvironmentOptions` Umgebungsvariablen oder Registrierungswerten überschrieben.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions].  
    
## 0.9.579  

Veröffentlichungsdatum: 20. Juli 2020  

[NuGet-Paket][NuGetGallery0.9.579] \| Microsoft Edge, Version 86.0.579.0.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung:** Immergrüne WebView2 Runtime und Installer werden für die Vorschau veröffentlicht.  Weitere Informationen finden Sie unter ["Verteilung von WebView2".][Webview2ConceptsDistributionUnderstandRuntimeInstaller]  
    
*   > [!IMPORTANT]
    > **Ankündigung:** Die folgenden WebView2 -SDK-Versionen werden nach der nächsten VERSION des SDK nicht mehr unterstützt.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Die WebView2 -SDK-Versionen sind auch auf der Website als veraltet nuget.org.  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem neuesten Stand zu bleiben.  
    
*   Verbesserungen des WebView-Arbeitsthreads hinzugefügt.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Der Popupblocker in WebView wurde deaktiviert.  Navigieren Sie für das Ereignis zur [IsUserInitiated-Eigenschaft,][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] um weitere Informationen `NewWindowRequested` zu erhalten.  
*   Sicherstellen, dass das Startereignis der WebView-Navigation für ausgeführt `about:blank` wird.  Jetzt werden Ereignisse für alle Navigationen ausgeführt, aber Absagen für oder iframe werden `NavigationStarting` `about:blank` nicht unterstützt und `srcdoc` ignoriert.  
*   Einige `edge://` URI-Schemas in WebView blockiert.  
*   Experimentelle [IsSingleSignOnUsingOSPrimaryAccountEnabled-Eigenschaft][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] zu WebView2-Umgebungsoptionen hinzugefügt, um den bedingten Zugriff für WebView zu aktivieren.  
*   Experimentelles [WebResourceResponseReceived-Ereignis][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] hinzugefügt, das ausgeführt wird, nachdem WebView die Antwort von einer WebResource-Anforderung empfängt und verarbeitet.  Authentifizierungsheader sind, falls vorhanden, im Antwortobjekt enthalten.  
    
#### .NET  

*   Verbesserte Behandlung des WPF-Fokus.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Eigenschaft `ZoomFactor` für WPF Webview2 Controller hinzugefügt.  
    
## 0.9.538  

[NuGet-Paket][NuGetGallery0.9.538] \| Microsoft Edge, Version 85.0.538.0.  

#### Allgemein  

*   Unterstützung für WebView2 SDK Version [0.8.149](#08149)wird nicht mehr unterstützt.  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem neuesten Stand zu bleiben.  
*   Gruppenrichtlinie so aktualisiert, dass berücksichtigt wird, wann der Profilpfad des Microsoft Edge-Browsers geändert wird \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
#### Win32 C/C++  

*   [ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]hinzugefügt, das ausgeführt wird und `window.open()` [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\) zugeordnet wird.  
*   > [!IMPORTANT]
    > **Breaking Change**: Veraltete [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] und ersetzt durch [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Breaking Change:** Um sicherzustellen, dass die WebView2-API den Benennungskonventionen der Windows-API entspricht, hat das WebView-Team die folgenden Namen aktualisiert.  
    > 
    > *   [AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] ist jetzt [AreHostObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed].  
    
*   [AddHostObjectToScript aktualisiert.][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]  Die Serialisierungsmarkierungen des ursprünglichen Hostobjekts werden jetzt auf die Proxyobjekte festgelegt.  Anschließend werden Die Serialisierungsmarkierungen des Hostobjekts als Hostobjekt serialisiert, wenn sie als Parameter im JavaScript-Rückruf \( #148 \)[übergeben][GithubMicrosoftedgeWebviewfeedbackIssue148]werden.  
    
#### .NET (0.9.538 Vorabversion)  

*   Es wurden WinForms und WPF WebView2API-Beispiele veröffentlicht, die umfassende Anleitungen des WebView2 SDK sind.  Weitere Informationen finden Sie im [Beispiel-Repository.][GithubMicrosoftedgeWebview2samplesMain]  
*   Unterstützung für experimentelle APIs für visuelles Hosting und [Fensterfeatures hinzugefügt.][Webview2ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Breaking Change**: Die folgenden Zurückdrängungen implementieren jetzt IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]und [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] und [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] als ["CoreWebView2Environment"-Statik][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] hinzugefügt.  
    
## 0.9.515-prerelease  

[NuGet-Paket][NuGetGallery0.9.515-prerelease] \| Microsoft Edge, Version 84.0.515.0.  

*   > [!IMPORTANT]
    > **Ankündigung:** WebView2 unterstützt jetzt Windows Forms und WPF unter .NET Framework 4.6.2 oder höher und .NET Core 3.0 oder höher im **Vorabversionspaket.**  
    
*   Weitere Informationen zum Erstellen von WPF-Apps finden Sie im [WPF-Leitfaden][Webview2GettingstartedWpf] für erste Schritte und in der WebView2-WPF-Referenz für WPF-spezifische APIs. [][DotnetApiMicrosoftWebWebview2Wpf]  
*   Weitere Informationen zum Erstellen von Windows Forms-Apps finden Sie im Windows [Forms Getting Started Guide][Webview2GettingstartedWinforms] und in der WebView2 Windows Forms [Reference][DotnetApiMicrosoftWebWebview2Winforms] für Windows Forms-spezifische APIs.  
*   Weitere Informationen zu den CoreWebView2-APIs finden Sie in [der .NET-Referenz.][DotnetApiMicrosoftWebWebview2Core]  
*   > [!CAUTION]
    > **Bekannte Probleme:** Das WebView-Team ist sich einiger Probleme in der Vorabversion bewusst, die in zukünftigen Versionen behoben werden.  
    > 
    > *   **DPI-Bewusstsein:** WebView2 für WPF ist derzeit nicht DPI-enthbar.  Bei der Initialisierung von WebView2 auf Monitoren mit hohem DPI liegt ein bekanntes Problem vor, bei dem WebView zunächst als Bruchteil des Fensters initialisiert wird, bis die Fenstergröße geändert wird.  
    > *   **WPF Designer:** Der WPF Designer wird derzeit nicht unterstützt.  Fügen Sie das WebView2-Steuerelement in Ihrer App hinzu, indem Sie den entsprechenden XAML direkt in einem Texteditor ändern.  
    
## 0.9.488  

[NuGet-Paket][NuGetGallery0.9.488] \| Microsoft Edge, Version 84.0.488.0.  

*   > [!IMPORTANT]
    > **Ankündigung:** Ab der anstehenden Microsoft Edge-Version 83 zielt Immergrün WebView nicht mehr auf den Browserkanal Stable ab.  Stattdessen zielt sie auf eine andere Gruppe von Binärdateien ab, die als ["Evergreen WebView2 Runtime"][Webview2ConceptsDistributionEvergreenDistributionMode]bezeichnet wird und die Sie über ein Installationsprogramm verketten können, das das WebView-Team derzeit entwickelt.  Weitere Informationen finden Sie unter ["App-Distribution".][Webview2ConceptsDistribution]  
    
*   > [!IMPORTANT]
    > **Ankündigung:** In Zukunft veröffentlicht das WebView-Team zwei Pakete: ein Vorabversionspaket mit experimentellen APIs \(für Sie zum Testen\) und ein stabiles Releasepaket mit stabilen APIs \(für Ihre Konfidenz\).  Um mehr über die Unterschiede zu erfahren, navigieren Sie zu ["Grundlegendes zu Browserversionen und WebView2".][Webview2ConceptsVersioning]  
    
*   > [!IMPORTANT]
    > **Breaking Change:** Um sicherzustellen, dass die WebView2-API den Benennungskonventionen der Windows-API entspricht, hat das WebView-Team die Namen der folgenden Schnittstellen aktualisiert.  
    > 
    > *   `CORE_WEBVIEW2_*` Präfix ist jetzt `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo ist][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] jetzt [GetAvailableCoreWebView2BrowserVersionString][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] ist jetzt [get_BrowserVersionString][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring].  
    > *   [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] ist jetzt [AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] ist jetzt [RemoveHostObjectFromScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` ist jetzt `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Breaking Change:** Die `AddRemoteObject` JS-Proxymethoden werden ebenfalls umbenannt.  
    > 
    > *   `getLocal` ist jetzt `getLocalProperty` .  
    > *   `setLocal` ist jetzt `setLocalProperty` .  
    > *   `getRemote` ist jetzt `getHostProperty` .  
    > *   `setRemote` ist jetzt `setHostProperty` .  
    > *   `applyRemote` ist jetzt `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Veraltete [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] und ersetzt durch [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   [FrameNavigationCompleted-Ereignis][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted] hinzugefügt.  Wenn nun ein iframe die Navigation abgeschlossen hat, wird ein Ereignis ausgeführt und gibt den Erfolg der Navigation und die Navigations-ID zurück.  
*   Die [ICoreWebView2EnvironmentOptions-Schnittstelle][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] wurde hinzugefügt, die verwendet werden kann, um die Version der WebView2-Runtime zu ermitteln, die auf Ihre App ausgerichtet ist.  
*   [IsBuiltInErrorPageEnabled-Einstellung hinzugefügt.][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]  Jetzt können Sie die integrierte Fehlerwebseite für Navigationsfehler und Renderprozessfehler aktivieren oder deaktivieren.  
*   Remoteobjektinjektion zur Unterstützung von `IDispatch` .NET-Implementierungen \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\) aktualisiert.  
*   Das [Ereignis "NewWindowRequested"][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] wurde aktualisiert, um Anforderungen aus Kontextmenüs zu verarbeiten \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Das erste separate WebView2-Vorabversionspaket wurde veröffentlicht, in dem Sie auf visuelle Hosting-APIs zugreifen können.  Das WebView-Team hat [APISample aktualisiert,][GithubMicrosoftedgeWebview2samplesMain] um die neuen experimentellen APIs zu enthalten.  
    
    *   Die [ICoreWebView2ExperimentalCompositionController-Schnittstelle][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] wurde hinzugefügt, um eine Verbindung mit einer Kompositionsstruktur herzustellen und Eingaben für webView zu ermöglichen.  
    *   [ICoreWebView2ExperimentalPointerInfo hinzugefügt,][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]das alle Informationen aus einem `POINTER_INFO` enthält.  Dieses Objekt wird an SendPointerInput übergeben, um Zeigereingaben in die WebView zu injizieren.  
    *   [ICoreWebView2ExperimentalCursorChangedEventHandler][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]hinzugefügt, das der App mitteilt, wann der Mauszeiger über webView geändert werden soll.  Wenn die Maus über einem Textfeld in der WebView bewegt wird, wechselt der Cursor vom Pfeil zum Selektor.  Die Eigenschaft auf der gibt der App an, was der Mauszeiger für die `cursor` `CompositionController` WebView sein soll.  
    
## 0.9.430  

[NuGet-Paket][NuGetGallery0.9.430] \| Microsoft Edge, Version 82.0.430.0.  

Das WebView2 SDK ist die offizielle Win32 C++-Betaversion, die mehrere Featureanforderungen von Feedback enthält.  Das WebView-Team versucht, die Anzahl der Veröffentlichungen mit änderungen zu begrenzen.  Bei der allgemeinen Verfügbarkeit sind einige wichtige wichtige Änderungen in die Betaversion integriert.  

*   > [!IMPORTANT]
    > **Breaking Change:** Während sich die endgültige Version nähert, hat das WebView-Team das Präfix *"IWebView2WebView"*   in *"ICoreWebView2"*   umbenannt, um sicherzustellen, dass die WebView2-API der Benennungskonvention der Windows-API entspricht.  Um das WebView2 SDK aus Benutzeroberflächenframework nutzen zu können, wurde das WebView-Team außerdem in `ICoreWebView2` [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] und [ICoreWebView2Host getrennt.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430]  `ICoreWebView2Host` Unterstützt die Größenänderung, das Ein- und Ausblenden, Fokussieren und andere Funktionen im Zusammenhang mit Fenstern und Kompositionen.  ICoreWebView2 unterstützt alle anderen WebView2-Funktionen.  Um mehr über das Einbinden der Änderungen zu [][GithubMicrosoftedgeWebview2samplesPr17] erfahren, navigieren Sie zur WebView2-Pullanforderung im WebView2-APISample-Projekt. [][GithubMicrosoftedgeWebview2samplesMain]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: [DocumentStateChanged in][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] drei Komponenten aufteilen:  [SourceChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged], [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]und [HistoryChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged].  Wenn sich nun die Quell-URL ändert, `SourceChanged` wird das Ereignis ausgeführt.  Wenn der Verlaufsstatus geändert wird, `HistoryChanged` wird das Ereignis ausgeführt.  Das `ContentLoading` Ereignis wird vor dem ersten Skript ausgeführt, wenn ein neues Dokument geladen wird.  
    
*   Unterstützung für die ARM64-Architektur hinzugefügt.  
*   Unterstützung für den Soft Input Panel \(SIP\) für Touchscreengeräte hinzugefügt.  
*   Unterstützung für Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 und Windows Server 2016 hinzugefügt.  
*   [NotifyParentWindowPositionChanged][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] wurde hinzugefügt, damit die Statusleiste dem Fenster im Fenstermodus folgen kann.  Implementieren Sie außerdem die Änderung im fensterlosen Modus, damit Barrierefreiheitsfunktionen funktionieren.  
*   Die [Einstellung "AreRemoteObjectsAllowed" wurde][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] hinzugefügt, um global zu steuern, ob von Remoteobjekten auf eine Webseite zugegriffen werden kann.  Standardmäßig ist `AreRemoteObjectsAllowed` dies aktiviert, sodass von [AddRemoteObject hinzugefügte][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] Remoteobjekte von der Webseite aus zugänglich sind.  Wenn dies deaktiviert ist, ist der Zugriff auf die Objekte `AreRemoteObjectsAllowed` von der Webseite aus nicht möglich.  Änderungen werden auf das nächste Navigationsereignis angewendet.  
*   Die [Einstellung "IsZoomControlEnabled"][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] wurde hinzugefügt, um zu verhindern, dass Benutzer den Zoom der WebView mit und `ctrl` + `+` `ctrl` + `-` \(oder `ctrl` + Mausrad\) ändern.  Der Zoom kann weiterhin mithilfe von [put_ZoomFactor,][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] wenn die Einstellung deaktiviert ist.  
*   ZoomFactor wurde geändert, um nur auf die aktuelle WebView anzuwenden.  Zoomänderungen an der aktuellen WebView wirken sich nicht auf andere WebViews aus, zu der Sie mit derselben Website des Ursprungs navigiert haben.  Weitere Informationen finden Sie unter [get_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor].  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   [SetBoundsAndZoomFactor hinzugefügt.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]  Jetzt können Sie den Zoomfaktor und die Grenzen einer WebView gleichzeitig festlegen.  
*   [WindowCloseRequested-Ereignis][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] hinzugefügt.  Weitere Informationen finden Sie unter [add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Unterstützung für den Dialogtyp für Dialogfeldereignisse in JavaScript hinzugefügt und `beforeunload` CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD Enumerationseintrag [][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind] hinzugefügt.  
*   [GetHeaders zu][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] "HttpRequestHeaders", ["GetHeader"][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] zu "HttpResponseHeaders" und [get_HasCurrentHeader][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] "HttpHeadersCollectionIterator" hinzugefügt.  
*   > [!IMPORTANT]
    > **Breaking Change:** Geändertes `DevToolsProtocolEventReceived` Verhalten.  Jetzt können Sie ein [DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] für ein bestimmtes DevTools -Protokoll-Ereignis erstellen und ein Abonnement/Abonnement für ein solches Ereignis mit add_DevToolsProtocolEventReceived [][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived].  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Get_WebMessageAsString `WebMessageReceivedEventArgs` [][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] eigenschaft in eine [TryGetWebMessageAsString -Methode][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring] geändert.  
    
*   > [!IMPORTANT]
    > **Breaking Change:** Die Methode `AcceleratorKeyPressedEventArgs` ["Handle"][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] wurde in eine [get_Handled][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled] geändert.  
    
## 0.8.355  

[NuGet-Paket][NuGetGallery0.8.355] \| Microsoft Edge, Version 80.0.355.0.  

*   Veröffentlichtes WebView2API-Beispiel, ein umfassendes Handbuch des WebView2 SDK.  Weitere Informationen finden Sie im [API-Beispiel.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Unterstützung für IME für alle Sprachen neben Englisch \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\) hinzugefügt.  
*   Die #A0 des `WebResourceRequested` Ereignisses wurde als Reaktion auf Fehlerberichte aktualisiert.  Die gleichzeitige Angabe eines Filters und eines Ereignisses bei der Erstellung ist nun veraltet.  Verwenden Sie zum Erstellen eines von einer [Webressource angeforderten][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] Ereignisses add_WebResourceRequested, um das Ereignis hinzuzufügen, und fügen Sie ["AddWebResourceRequestedFilter"][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] einen Filter hinzu.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] entfernt den Filter \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Breaking Change**: Geändertes Vollbildverhalten.  Veraltet [isFullScreenAllowed][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated].  Wenn ein Element in einer WebView \(z. B. ein Video\) auf Vollbild festgelegt ist, füllt es jetzt standardmäßig die Grenzen der WebView.  Verwenden Sie [das ContainsFullScreenElementChanged-Ereignis][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] und [get_ContainsFullScreenElement,][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement] um anzugeben, wie die Größe der WebView von der App geändert werden soll, wenn ein Element in den Vollbildmodus wechseln soll.  
    
## 0.8.314  

[NuGet-Paket][NuGetGallery0.8.314] \| Microsoft Edge, Version 80.0.314.0.  

*   Unterstützung für Windows 7, Windows 8 und Windows 8.1 hinzugefügt.  
*   Unterstützung Visual Studio und Visual Studio Codedebugger für WebView2 hinzugefügt.  Debuggen Sie nun das Skript in WebView2 direkt von Ihrer IDE aus.  Weitere Informationen finden Sie unter ["Debuggen" bei der Entwicklung mit WebView2-Steuerelementen.][Webview2HowtoDebug]  
*   Für das ausgeführte Skript in WebView2 hinzugefügt, um von der Win32-Komponente der App auf ein IDispatch-Objekt zu zugreifen und auf die Eigenschaften des `Native Object Injection` IDispatch -Objekts zu zugreifen.  Weitere Informationen finden Sie unter [AddRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Ereignis `AcceleratorKeyPressed` hinzugefügt.  Weitere Informationen finden Sie unter [add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Deaktiviert die `Context Menus` .  Weitere Informationen finden Sie unter [put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   `DPI Awareness`Aktualisiert.  Jetzt ist das DPI-Bewusstsein von WebView mit dem DPI-Bewusstsein der Host-App identisch.  
    
    > [!NOTE]
    > Wenn eine andere Hybrid-App mit einem anderen DPI-Bewusstsein als die ursprüngliche WebView gestartet wird, wird die neue WebView nicht gestartet, wenn die \( #1 \) identisch `user data folder` ist.[][GithubMicrosoftedgeWebviewfeedbackIssue1]  
    
*   Aktualisiert, `Notification Change Behavior` sodass WebView2 automatisch Benachrichtigungsberechtigungsanforderungen ablehnt, die von Webinhalten, die in WebView gehostet werden, aufgefordert werden.  
    
## 0.8.270  

[NuGet-Paket][NuGetGallery0.8.270] \| Microsoft Edge, Version 78.0.270.0.  

*   Ereignis `DocumentTitleChanged` zum Angeben der Änderung des Dokumenttitels \([\#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\) hinzugefügt.  
*   API `GetWebView2BrowserVersionInfo` \( \#18 \)[hinzugefügt.][GithubMicrosoftedgeWebviewfeedbackIssue18]  
*   Ereignis `NewWindowRequested` hinzugefügt.  
*   Funktion `CreateWebView2EnvironmentWithDetails` zum Entfernen `releaseChannelPreference` aktualisiert.  Weitere Informationen zu der Funktion `CreateWebView2EnvironmentWithDetails` finden Sie unter [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Die Außerkraftsetzung von Registrierungs- und Umgebungsvariablen wird weiterhin unterstützt.  Die Standardkanaleinstellung wird verwendet, es sei denn, sie wird außer Kraft gesetzt.  
    Während der Kanalsuche überspringt das WebView-Team alle vorherigen Kanalversion, die nicht mit dem WebView2 SDK kompatibel ist.  
    Das WebView-Team wählt den stabileren Kanal aus, um das konsistenteste Verhalten für den Endbenutzer sicherzustellen.  Wenn Sie mit den neuesten Canary-Builds testen, sollten Sie ein Skript zum Festlegen der Umgebungsvariablen `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` erstellen, bevor Sie die App starten.  
*   Die Funktion `CreateWebView2EnvironmentWithDetails` wurde mit logik für die Auswahl aktualisiert, wenn nicht `userDataFolder` angegeben.  Weitere Informationen zu der Funktion `CreateWebView2EnvironmentWithDetails` finden Sie unter [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Wenn Sie zuvor den Standardspeicherort verwendet haben, wird beim Wechsel zum neuen SDK der Standardwert zurückgesetzt \(auf einen neuen Speicherort im Hostcodeverzeichnis festgelegt\), und der Status wird ebenfalls `userDataFolder` `userDataFolder` zurückgesetzt.  Wenn der Hostprozess nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis verfügt, kann die `CreateWebView2EnvironmentWithDetails` Funktion fehlschlagen.  Sie können die Daten aus dem alten in `user data folder` das neue Verzeichnis kopieren.  
    
## 0.8.230  

[NuGet-Paket][NuGetGallery0.8.230] \| Microsoft Edge, Version 77.0.230.0.  

*   `Stop`API hinzugefügt, um alle Navigations- und ausstehenden Ressourcenrufe zu beenden \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Datei `.tlb` zum NuGet-Paket \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\) hinzugefügt.  
*   .NET-Projekte zur Installerliste im NuGet-Paket \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\) hinzugefügt.  
    
## 0.8.190  

[NuGet-Paket][NuGetGallery0.8.190] \| Microsoft Edge, Version 77.0.190.0.  

*   Hinzugefügt, `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` um zu steuern, ob Benutzer DevTools \([\#16 \) öffnen][GithubMicrosoftedgeWebviewfeedbackIssue16]können.  
*   Hinzugefügt, `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` um zu steuern, ob die Statusleiste angezeigt wird \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Für `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` das Zurück- und Vorwärtsschalten des Navigationsverlaufs hinzugefügt.  
*   HTTP-Headertypen \( \) zum Anzeigen und Ändern von HTTP-Headern `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` in WebView hinzugefügt.  
*   32-Bit-WebView-Unterstützung auf 64-Bit-Computern \([\#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\) hinzugefügt.  
*   WebView-IDL zum SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\) hinzugefügt.  
*   Lib zur Unterstützung von `IID\_\*` Schnittstellen-ID-Objekten \([\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\) hinzugefügt.  
*   Hinzugefügt: Pfad, Verknüpfung und automatisches Kopieren von DLL-Dateien in die NuGet-Datei `TARGET` im SDK.  
*   Das Anfordern im `window.open()` Skript wurde aktiviert.  
    
## 0.8.149  

[NuGet-Paket][NuGetGallery0.8.149] \| Microsoft Edge, Version 76.0.149.0.  

Erste Entwicklervorschauversion.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Immergrüner Verteilungsmodus – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Fester Versionsverteilungsmodus – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Verstehen der WebView2-Laufzeit und des Installationsprogramms – Verteilung von Anwendungen mithilfe von WebView2-| Microsoft Docs"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Gruppenrichtlinien für WebView2 – Verwalten von WebView2-| Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu Browserversionen und WebView2-| Microsoft Docs"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Experimentelle APIs – Grundlegendes zu Browserversionen und WebView2-| Microsoft Docs"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Übereinstimmende WebView2-Runtime-Versionen – Verstehen der WebView2 -SDK-| Microsoft Docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps | Microsoft Docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF | Microsoft Docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Debuggen bei der Entwicklung mit WebView2-Steuerelementen | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded : Schnittstellen-ICoreWebView2_2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping – ICoreWebView2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend – ICoreWebview2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled - Interface ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "interface ICoreWebView2CompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor - Interface ICoreWebView2Controller2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived - Interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived - Interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest – Schnittstelle ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount - Interface ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments - interface ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo - Interface ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString - Interface ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged - Interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode - Interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale - interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges - Interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled - interface ICoreWebView2ExperimentalEnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures - interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalPointerInfo | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent - Interface ICoreWebView2ExperimentalSettings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - Interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - Interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - Interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager - interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment - Interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest – Schnittstelle ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent - interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor - Interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged – Schnittstelle ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor - Interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor – Schnittstelle ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader - Interface ICoreWebView2HttpHeadersCollectionIterator | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders – Schnittstelle ICoreWebView2HttpRequestHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader – Schnittstelle ICoreWebView2HttpResponseHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated -Schnittstelle ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures - Interface ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - Interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled - Interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - Interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed - Interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject – Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject – Schnittstelle ICoreWebView2-| Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript – Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested - Interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript – Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript – Schnittstelle ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString – Schnittstelle ICoreWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke - interface ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interface ICoreWebView2WindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle – Schnittstelle IWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interface IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled - Interface IWebView2Settings2 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated - Interface IWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString - interface IWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed - Interface IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject – Schnittstelle IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested - Interface IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter – Schnittstelle IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement - Interface IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter – Schnittstelle IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged - Interface IWebView2WebView | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails – globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo – globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails – globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString – globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – globale | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions – globale | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Richtlinien | Microsoft Docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 – Richtlinien | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Microsoft.Web.WebView2.Core-Namespace-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "CoreWebView2-Klasse (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "CoreWebView2Environment-Klasse (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment.CompareBrowserVersions(String, String) Method (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "CoreWebView2Environment.GetAvailableBrowserVersionString(String)-Methode (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "CoreWebView2HttpRequestHeaders-Klasse (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "CoreWebView2HttpResponseHeaders-Klasse (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "CoreWebView2.NewWindowRequested-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "CoreWebView2.PermissionRequested-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "CoreWebView2.ScriptDialogOpening-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "CoreWebView2.WebResourceRequested-Ereignis (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "CoreWebView2InitializationCompletedEventArgs-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Namespace-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "CoreWebView2CreationProperties-Klasse (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Webview2.Source-Klasse (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft.Web.WebView2.Wpf Namespace-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "WebView2.BuildWindowCore(HandleRef)-Methode (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "WebView2.DestroyWindowCore(HandleRef)-Methode (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "CancelEventArgs-Klasse (System.ComponentModel) | Microsoft Docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "EventArgs Class (System) | Microsoft Docs"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblys mit starkem | Microsoft Docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender Application Guard (Windows 10) – Sicherheitseinstellungen für Windows | Microsoft Docs"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Ankündigungs-Repository für MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Verschieben des Projekts zur Verwendung der neuesten WebView2 SDK 0.9.430 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 878"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Ankündigung der allgemeinen Verfügbarkeit für Microsoft Edge WebView2 für .NET und feste Verteilungsmethode | .NET-Blog"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Edge Developer"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "NuGet Gallery | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "NuGet Gallery | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "NuGet Gallery | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "NuGet Gallery | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "NuGet Gallery | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "NuGet Gallery | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "NuGet Gallery | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "NuGet Gallery | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "NuGet Gallery | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "NuGet Gallery | Microsoft.Web.WebView2 v0.9.515 Prerelease"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "NuGet Gallery | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "NuGet Gallery | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "NuGet Gallery | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "NuGet Gallery | Microsoft.Web.WebView2 v0.9.628 Prerelease"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "NuGet Gallery | Microsoft.Web.WebView2 v1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "NuGet Gallery | Microsoft.Web.WebView2 v1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "NuGet Gallery | Microsoft.Web.WebView2 v1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "NuGet Gallery | Microsoft.Web.WebView2 v1.0.674 Prerelease"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "NuGet Gallery | Microsoft.Web.WebView2 v1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "NuGet Gallery | Microsoft.Web.WebView2 v1.0.721 Prerelease"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "NuGet Gallery | Microsoft.Web.WebView2 v1.0.790 Prerelease"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Ankündigung der allgemeinen Verfügbarkeit von Microsoft Edge WebView2 | Microsoft Edge Blog"  
