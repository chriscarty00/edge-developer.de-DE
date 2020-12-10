---
description: Anmerkungen zu dieser Version von Microsoft Edge WebView2 SDK
title: Anmerkungen zu dieser Version von Microsoft Edge WebView2 für Win32, WPF und WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 2859f931aea8963e8a50835110914a216811c191
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204019"
---
# Anmerkungen zu dieser Version von WebView2 SDK  

Das WebView2-Team aktualisiert das [WebView2-SDK][NuGetGallery] in einer sechswöchigen Kadenz.  Überprüfen Sie die folgenden Inhalte auf aktuelle Informationen zu Produktankündigungen, Ergänzungen, Änderungen und unterbrechen von Änderungen an den APIs.  

> [!NOTE]
> Kompilieren Sie Ihre APP nach dem Aktualisieren des NuGet-Pakets erneut.  

## 1.0.721-Vorabversion  

Veröffentlichungsdatum: 8. Dezember 2020  

[NuGet-Paket][NuGetGallery1.0.721-prerelease] \ | minimale Microsoft Edge-Version 86.0.616.0.  

#### Allgemein  

###### Features  

*   [WebView2-Gruppenrichtlinien][DeployedgeMicrosoftEdgeWebviewPolicies]wurden hinzugefügt.  Weitere Informationen zu empfohlenen Methoden finden Sie unter [Gruppenrichtlinien für WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: der alte Registrierungsspeicherort wurde als veraltet markiert.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
     
*   Unterstützung für [Drag & Drop][ReferenceWin32Icorewebview2experimentalcompositioncontroller3] in WebView2 hinzugefügt.  
*   APIs zur Behandlung der dpi-Unterstützung hinzugefügt.  
    *   [RasterizationScale][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] -Eigenschaft hinzugefügt, um die DPI-Skalierung für WebView-Inhalte und UI-Popups sowie zugeordnete [RasterizationScaleChanged][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] -Ereignisse zu ändern.  
    *   [ShouldDetectMonitorScaleChanges][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges] -Eigenschaft hinzugefügt, um die `RasterizationScale` Eigenschaft bei Bedarf automatisch zu aktualisieren.  
    *   [BoundsMode-Eigenschaft][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode] hinzugefügt, um anzugeben, dass die Begrenzungen logische Pixel sind, und WebView die Verwendung der `RasterizationScale` für WebView2-Pixel Anzeige ermöglichen, und WebView die `RasterizationScale` auf den anwenden, `Bounds` um die physikalische Größe zu erhalten.
*   Aktualisiertes `NewWindowRequested` Ereignis, das verarbeitet werden soll, `Ctrl` + `click` und `Shift` + `click` .  \ ([\ #168][GithubMicrosoftedgeWebviewfeedbackIssue168] und [\ #371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  

#### .NET  

###### Features  

*   Aktivierter WinForms-Designer in .net Core 3.1 + und .net 5.  
*   Verbesserte .net Cookie-Verwaltung.  \ ([\ #611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   `CoreWebView2Ready`Durch [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]ersetzt.  

###### Fehlerbehebungen

*   [AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] -Ereignis hinzugefügt, das AcceleratorKey drücken in WebView2 unterstützt.  \ ([\ #288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Unnötige Dateien werden von der Ausgabe in WebView2-Ordner entfernt.  \ ([\ #461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   Verbesserte Hostobjekt-API.  \ ([\ #335][GithubMicrosoftedgeWebviewfeedbackIssue335] und [\ #525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  

## 1.0.664.37  

Veröffentlichungsdatum: 20. November 2020  

[NuGet-Paket][NuGetGallery1.0.664.37] \ | minimale WebView2-Runtime-Version 86.0.616.0.  

#### Allgemein  

> [!IMPORTANT]
> **Ankündigung**: .net WPF/WinForms WebView2 ist jetzt im allgemeinen verfügbar \ (GA \).  Ab dieser Version sind die Release-SDKs Forward-kompatibel.  Weitere Informationen finden Sie im [Blogbeitrag zur GA-Ankündigung][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod].  

###### Features  

*   .Net WPF/WinForms WebView2 ist jetzt im allgemeinen verfügbar \ (GA \).  
*   Die feste Verteilung \ (bringen-eigene \)-Modus hat GA erreicht.  

#### .NET  

###### Fehlerbehebungen  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` verhindert, dass neues Fenster geöffnet wird \ ([\ #549][GithubMicrosoftedgeWebviewfeedbackIssue549]\) und \ ([\ #560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  


## 1.0.674-Vorabversion  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet-Paket][NuGetGallery1.0.674-prerelease] \ | minimale WebView2-Runtime-Version 86.0.616.0.  

#### Allgemein  

*   [NavigateWithWebResourceRequest][ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674] -Methode hinzugefügt, mit der Sie während der Navigation Postdaten oder zusätzliche Anforderungs Kopfzeilen bereitstellen können.
*   Das [DOMContentLoaded][ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674] -Ereignis, das beim Laden und Analysieren des ersten HTML-Dokuments ausgeführt wird, wurde hinzugefügt.
*   Die [Umgebungs][ReferenceWin32Icorewebview2experimentalGetEnvironment10674] Eigenschaft für WebView2 wurde hinzugefügt.  Diese Eigenschaft macht die WebView2-Umgebung verfügbar, in der eine Instanz von WebView2 erstellt wurde.
*   Hinzugefügte [Cookie-Verwaltungs][ReferenceWin32Icorewebview2experimentalGetCookiemanager10674] -APIs, die es Entwicklern ermöglichen, die WebView2-Sitzung zu authentifizieren oder Cookies aus WebView abzurufen, um andere Tools zu authentifizieren.  Wir planen, Sprache/Framework-spezifische Verbesserungen vorzunehmen.  Weitere Informationen finden Sie unter [API-Überprüfung: Cookieverwaltung][GithubMicrosoftedgeWebview2AnnouncementIssue2].
*   Das [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674] -Ereignis wurde aktualisiert, und es wurden unveränderliche [WebResourceResponseView][ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674] und [WebResourceResponseReceivedEventArgs::P opulateresponsecontent][ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628] zu [WebResourceResponseView:: getContent][ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]hinzugefügt.
*   [Microsoft Defender Application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] in WebView2 deaktiviert.
*   [SystemCursorId][ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674] für visuelles Hosting hinzugefügt.
*   Der Fehler wurde für die Eingabemethode im visuellen Hosting behoben.
*   Entwickler müssen Version. lib nicht mehr einbeziehen, wenn Sie die statische WebView2-Bibliothek verwenden.

#### .NET  

*   [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] -Klasse aktualisiert, um die CoreWebView2Environment-Variable verfügbar zu machen.  
*   Implementierungen von benutzerdefinierten EventArgs-Klassen in Namespace wurden als unter `Microsoft.Web.WebView2.Core` Klassen von [System. EventArgs][DotnetApiSystemEventargs] oder [System. ComponentModel. CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs]geändert.  \ ([\ #250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Unterstützung für [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] in WinForms wurde hinzugefügt.  \ ([\ #204][GithubMicrosoftedgeWebviewfeedbackIssue204]\)
*   .Net [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] -APIs wurden hinzugefügt.  \ ([\ #219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Die [Quell][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] Eigenschaft des WinForms-Designers wurde auf Standard aktualisiert oder auf Null zurückgesetzt.  \ ([\ #177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   WebView2-Begrenzungen in WebView2.Init () wurden aktualisiert, um dpi-Modi mit weniger als 100% zu unterstützen.  \ ([\ #432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   [BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] und [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] wurden aktualisiert, um robuster zu sein.  \ ([\ #382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Die .net Loader-Basis wurde aktualisiert, um den Prozess-Bit anstelle der Betriebssystemarchitektur zu laden.  \ ([\ #431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   `EdgeNotFoundExpection`In [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]umbenannt.
 
## 1.0.622.22  

Veröffentlichungsdatum: 19. Oktober 2020  

[NuGet-Paket][NuGetGallery1.0.622.22] \ | minimale WebView2-Runtime-Version 86.0.616.0.  

#### Allgemein  

> [!IMPORTANT]
> **Ankündigung**: Win32 C/C++ WebView2 ist jetzt im allgemeinen verfügbar \ (GA \).  Ab dieser Version sind die Release-SDKs Forward-kompatibel.  Weitere Informationen finden Sie im [Blogbeitrag zur GA-Ankündigung][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability].  

*  [Evergreen-WebView2-Laufzeit und-Installer][Webview2ConceptsDistributionUnderstandRuntimeInstaller] sind GA.  Bootstrapper, Downlink-Link für den Bootstrapper und Standalone-Installationsprogramm für die Evergreen-Laufzeit sind auf [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2]verfügbar.  Der Beispielcode für den Installations Workflow steht auch im [WebView2Samples Repo][GithubMicrosoftedgeWebview2samplesMain]zur Verfügung.  
*  Der [Modus für feste Versionen][Webview2ConceptsDistributionFixedVersionMode] steht für Entwicklervorschau zur Verfügung.  

## 0.9.628-Vorabversion  

Veröffentlichungsdatum: 10. September 2020  

[NuGet-Paket][NuGetGallery0.9.628-prerelease] \ | minimale Microsoft Edge-Version 86.0.616.0.  

> [!IMPORTANT]
> **Ankündigung**: Diese Vorabversion wird weiterhin basierend auf dem Microsoft Edge 87-Zweig veröffentlicht.  In Zukunft entspricht die Vorabversion des SDK-Release dem Microsoft Edge Canary Build, und die normale Version wird mit Microsoft Edge stable synchronisiert.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: Visual Hosting-APIs sind jetzt unter Vorschau.  WebView2 verwendet visuelles Hosting, um neben WinComp/DComp-visuellen Objekten im Gegensatz zu HWNDs zu laufen.  Die Schnittstellen sind in experimental.  Weitere Informationen finden Sie unter [ICoreWebView2ExperimentalEnvironment][ReferenceWin32Icorewebview2experimentalenvironment09628].  

#### .NET  

*   .NET-Binärdateien sind jetzt [stark benannt][DotnetStandardAssemblyStrongNamed].  \ ([\ #181][GithubMicrosoftedgeWebviewfeedbackIssue181]\).  
*   Das NuGet-Ziel wurde aktualisiert `WebViewLoader2.dll` .  \ ([\ #228][GithubMicrosoftedgeWebviewfeedbackIssue228]\) und \ ([\ #183][GithubMicrosoftedgeWebviewfeedbackIssue183]\).  
*   Aktualisiert `WebResourceRequested` , um [HttpRequestHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders] -und [HttpResponseHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders] -APIs in .net verfügbar zu machen.  \ ([\ #131][GithubMicrosoftedgeWebviewfeedbackIssue131]\).  

## 0.9.622.11  

Veröffentlichungsdatum: 10. September 2020  

[NuGet-Paket][NuGetGallery0.9.622.11] \ | minimale WebView2-Runtime-Version 86.0.616.0.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: dieses SDK ist der Veröffentlichungskandidat für WebView2 Win32 C/C++ GA.  Die GA-Version sollte dieselbe API-Schnittstelle und-Funktionalität verwenden.  

*   Getrennte [Browser Richtlinien][DeployedgeMicrosoftEdgePolicies].  
*   [AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622] -Eigenschaft für WebView2-Umgebungsoptionen hinzugefügt, um bedingten Zugriff für WebView zu ermöglichen.  
*   Aktualisiert `ICoreWebView2NewWindowRequestedEventArgs` , um die [WindowFeatures][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622] -Eigenschaft und die zugehörige [ICoreWebView2WindowFeatures][ReferenceWin32Icorewebview2windowfeatures09622]einzubeziehen.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   `System.Windows.Rect`Die Verwendung wird `System.Drawing.Rectangle` anstelle von `System.Windows.Rect` \ ([\ #235][GithubMicrosoftedgeWebviewfeedbackIssue235]\) aktualisiert.  
*   Das mswebviewnewwindowrequested-Ereignis wurde aktualisiert, um die `window.open()` Anforderung ohne Parameter zu behandeln.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622] -Satz using werden `ICoreWebView2EnvironmentOptions` nicht mit Umgebungsvariablen oder Registrierungswerten überschrieben.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622].  

## 0.9.579  

Veröffentlichungsdatum: 20. Juli 2020  

[NuGet-Paket][NuGetGallery0.9.579] \ | minimale Microsoft Edge-Version 86.0.579.0.  

#### Allgemein  

*   > [!IMPORTANT]
    > **Ankündigung**: Evergreen WebView2-Laufzeit und-Installationsprogramm werden für die Vorschau veröffentlicht.  Weitere Informationen finden Sie unter [Verteilung von WebView2] [Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview].  
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
*   Popup-Blocker deaktiviert in WebView.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu der [IsUserInitiated][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538] -Eigenschaft des `NewWindowRequested` Ereignisses.  
*   Sichergestellt, dass das Startereignis für WebView-Navigation ausgelöst wird `about:blank` .  Nun `NavigationStarting` werden Ereignisse für die gesamte Navigation ausgelöst, aber Stornierungen für `about:blank` oder IFRAME-srcdoc werden nicht unterstützt und ignoriert.  
*   Blockiertes `edge:// URI` Schema in WebView.  
*   Experimentelle [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538] -Eigenschaft für WebView2-Umgebungsoptionen hinzugefügt, um bedingten Zugriff für WebView zu ermöglichen.  
*   Experimentelles [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538] -Ereignis wurde hinzugefügt, das ausgelöst wird, nachdem die WebView die Antwort für eine Webressourcen Anforderung empfangen und verarbeitet hat.  Authentifizierungsheader (sofern vorhanden) sind im Response-Objekt enthalten.  

#### .NET  

*   Verbesserte WPF-Fokus Behandlung  \ ([\ #185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   `ZoomFactor`Eigenschaft auf WPF-Webview2-Controller hinzugefügt.  

## 0.9.538  

[NuGet-Paket][NuGetGallery0.9.538] \ | minimale Microsoft Edge-Version 85.0.538.0.  

#### Allgemein  

*   Unterstützung für WebView2 SDK-Version [0.8.149](#08149)wird gelöscht.  WebView2 empfiehlt, mit der neuesten Version von WebView2 auf dem Laufenden zu bleiben.  
*   Die Gruppenrichtlinie wurde aktualisiert, um zu berücksichtigen, wenn der Profilpfad des Microsoft Edge-Browsers geändert wird \ ([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  

#### Win32 C/C++  

*   [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]hinzugefügt, das ausgelöst wird, wenn `window.open()` ausgeführt wird und [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin32Icorewebview2experimentalwindowfeatures09538] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\) zugeordnet ist.  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: veralteter [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] und ersetzt durch [CreateCoreWebView2EnvironmentWithOptions] [[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538].  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: um sicherzustellen, dass die WebView2-API mit den Windows-API-Benennungskonventionen übereinstimmt, hat das WebView-Team die Namen der folgenden aktualisiert.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488] ist jetzt [AreHostObjectsAllowed][ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538].  
*   [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09538] aktualisiert, um sicherzustellen, dass die ursprünglichen Hostobjekt-Serialisierungsprogramm-Marker auf die Proxyobjekte gesetzt und als Hostobjekt zurück serialisiert werden, wenn Sie als Parameter im JavaScript-Rückruf \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\) übergeben werden.  

#### .Net (0.9.538 Pre-Release)  

*   Freigegebene WinForms-und WPF-WebView2API-Beispiele, die umfassende Leitfäden des WebView2-SDK sind.  Wenn Sie weitere Informationen wünschen, navigieren Sie zu [Samples Repo][GithubMicrosoftedgeWebview2samplesMain].  
*   Unterstützung für visuelles Hosting und Fenster Features, [experimentelle APIs][ConceptsVersioningExperimentalApis], wurde hinzugefügt.  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: die folgenden Verzögerungen implementieren nun IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [mswebviewnewwindowrequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]und [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] und [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] werden als [CoreWebView2Environment][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] -Statik hinzugefügt.  

## 0.9.515-Vorabversion  

[NuGet-Paket][NuGetGallery0.9.515-prerelease] \ | minimale Microsoft Edge-Version 84.0.515.0.  

*   > [!IMPORTANT]
    > **Ankündigung**: WebView2 unterstützt jetzt Windows Forms und WPF unter .NET Framework 4.6.2 oder höher und .net Core 3,0 oder höher im **Pre-Release-Paket**.  
*   Weitere Informationen zum Erstellen von WPF-Anwendungen finden Sie unter [WPF-Handbuch für erste Schritte][GettingstartedWpf] und WebView2 [WPF-Referenz][DotnetApiMicrosoftWebWebview2Wpf] für WPF-spezifische APIs.  
*   Weitere Informationen zum Erstellen von Windows Forms-Anwendungen finden Sie unter [Windows Forms-Handbuch für erste Schritte][GettingstartedWinforms] und WebView2 Windows Forms- [Referenz][DotnetApiMicrosoftWebWebview2Winforms] für Windows Forms-spezifische APIs.  
*   Wenn Sie weitere Informationen zu den CoreWebView2-APIs erhalten möchten, navigieren Sie zu [.net Reference][DotnetApiMicrosoftWebWebview2Core].  
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
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430] ist jetzt [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488].  
    > *   [get_BrowserVersionInfo][ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430] ist nun [get_BrowserVersionString][ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488].  
    > *   [Addremoteobject][ReferenceWin32Icorewebview2Addremoteobject09430] ist jetzt [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09488].  
    > *   [RemoveRemoteObject][ReferenceWin32Icorewebview2Removeremoteobject09430] ist jetzt [RemoveHostObjectFromScript][ReferenceWin32Icorewebview2Removehostobjectfromscript09488].  
    > *   `chrome.webview.remoteObjects` ist jetzt `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: die `AddRemoteObject` js-Proxy Methoden werden ebenfalls umbenannt.  
    > *   `getLocal` ist jetzt `getLocalProperty` .  
    > *   `setLocal` ist jetzt `setLocalProperty` .  
    > *   `getRemote` ist jetzt `getHostProperty` .  
    > *   `setRemote` ist jetzt `setHostProperty` .  
    > *   `applyRemote` ist jetzt `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: veralteter [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] und durch [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]ersetzt.  
*   [FrameNavigationCompleted][ReferenceWin32Icorewebview2AddFramenavigationcompleted09488] -Ereignis hinzugefügt.  Wenn ein IFRAME nun die Navigation beendet, wird ein Ereignis ausgelöst und gibt den Erfolg der Navigation und der Navigations-ID zurück.  
*   [ICoreWebView2EnvironmentOptions][ReferenceWin32Icorewebview2environmentoptions09488] -Schnittstelle hinzugefügt, die verwendet werden kann, um die Version der WebView2-Laufzeit zu ermitteln, auf die die Anwendung ausgerichtet ist.  
*   [IsBuiltInErrorPageEnabled][ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488] -Einstellung hinzugefügt.  Nun können Sie die integrierte Fehlerseite für Navigationsfehler und Renderprozess-Fehler aktivieren oder deaktivieren.  
*   Aktualisierte Remote Objekt Injektion zur Unterstützung von .net `IDispatch` -Implementierungen \ ([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Das [mswebviewnewwindowrequested][ReferenceWin32Icorewebview2AddNewwindowrequested09488] -Ereignis wurde aktualisiert, um Anforderungen aus Kontextmenüs zu behandeln \ ([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Hat das erste separate WebView2-Pre-Release-Paket veröffentlicht, in dem Sie auf visuelle Hosting-APIs zugreifen können.  Das WebView-Team hat [APISample][GithubMicrosoftedgeWebview2samplesMain] aktualisiert, um die neuen experimentellen APIs einzubeziehen.  
    *   [ICoreWebView2ExperimentalCompositionController][ReferenceWin32Icorewebview2experimentalcompositioncontroller09488] -Schnittstelle hinzugefügt, um eine Verbindung mit einer Kompositionsstruktur herzustellen und Eingaben für die WebView bereitzustellen.  
    *   [ICoreWebView2ExperimentalPointerInfo][ReferenceWin32Icorewebview2experimentalpointerinfo09488]hinzugefügt, das alle Informationen aus einer enthält `POINTER_INFO` .  Dieses Objekt wird an SendPointerInput übergeben, um zeigereingaben in die WebView einzufügen.  
    *   [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]hinzugefügt, das die APP anweist, wenn der Mauszeiger über der WebView geändert werden soll.  Wenn sich die Maus über einem Textfeld in der WebView befindet, ändert sich der Cursor vom Pfeil zur Auswahl.  Die `cursor` Eigenschaft in der `CompositionController` teilt der APP mit, was der Mauszeiger aktuell für die WebView sein sollte.  

## 0.9.430  

[NuGet-Paket][NuGetGallery0.9.430] \ | minimale Microsoft Edge-Version 82.0.430.0.  

Das WebView2-SDK ist die offizielle Win32 C++-Beta Version, die mehrere Funktionsanforderungen aus Feedback enthält.  Das WebView-Team versucht, die Anzahl der Versionen mit unter brechenden Änderungen zu begrenzen.  Während wir uns der allgemeinen Verfügbarkeit nähern, werden einige wichtige Änderungen in die Beta Version integriert.  

*   > [!IMPORTANT]
    > **Aktuelle Änderung**: Wenn sich die endgültige Version nähert, wird das WebView-Team das Präfix *IWebView2WebView*   zu *ICoreWebView2*   umbenannt, um sicherzustellen, dass die WebView2-API mit der Windows-API-Benennungskonvention ausgerichtet wird.  Um das WebView2-SDK aus UI-Frameworks zu nutzen, wurde das WebView-Team außerdem `ICoreWebView2` in [ICoreWebView2][ReferenceWin32Icorewebview209430] und [ICoreWebView2Host][ReferenceWin32Icorewebview2host09430]getrennt.  `ICoreWebView2Host` unterstützt das Ändern der Größe, ein-und ausblenden, die Fokussierung und andere Funktionen im Zusammenhang mit Fenster und Komposition.  ICoreWebView2 unterstützt alle anderen WebView2-Funktionen.  Wenn Sie mehr über das Integrieren der Änderungen erfahren möchten, navigieren Sie im WebView2 [APISample][GithubMicrosoftedgeWebview2samplesMain] -Projekt zur WebView2- [Pull-Anforderung][GithubMicrosoftedgeWebview2samplesPr17] .  
*   > [!IMPORTANT]
    > Unter **brechende Änderung**: Teilen Sie [DocumentStateChanged][ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190] in drei Komponenten auf: [sourced][ReferenceWin32Icorewebview2AddSourcechanged09430], [ContentLoading][ReferenceWin32Icorewebview2AddContentloading09430]und [History][ReferenceWin32Icorewebview2AddHistorychanged09430].  Wenn die Quell-URL nun geändert `SourceChanged` wird, wird das Ereignis ausgelöst.  Wenn der Verlaufszustand geändert wird `HistoryChanged` , wird das Ereignis ausgelöst.  Das `ContentLoading` Ereignis wird vor dem anfänglichen Skript ausgelöst, wenn ein neues Dokument geladen wird.  
*   Unterstützung für die ARM64-Architektur wurde hinzugefügt.  
*   Soft Input Panel (SIP \)-Unterstützung für Touchscreen-Geräte hinzugefügt.  
*   Unterstützung für Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 und Windows Server 2016 wurde hinzugefügt.  
*   [NotifyParentWindowPositionChanged][ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]hinzugefügt, mit dem die Statusleiste dem Fenster im Fenstermodus folgen kann.  Implementieren Sie diese Änderung auch im Fenster freien Modus, damit die Barrierefreiheitsfeatures funktionieren.  
*   [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430] -Einstellung hinzugefügt, um global zu steuern, ob von Remoteobjekten auf eine Seite zugegriffen werden kann.  Standardmäßig `AreRemoteObjectsAllowed` ist aktiviert, was bedeutet, dass Remoteobjekte, die von [addremoteobject][ReferenceWin32Icorewebview2Addremoteobject09430] hinzugefügt wurden, von der Seite aus zugänglich sind.  Wenn `AreRemoteObjectsAllowed` deaktiviert ist, kann auf die Objekte nicht von der Seite aus zugegriffen werden.  Änderungen werden beim nächsten Navigations Ereignis übernommen.  
*   [IsZoomControlEnabled][ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430] -Einstellung wurde hinzugefügt, um zu verhindern, dass Benutzer den Zoom der WebView mithilfe von `ctrl` + `+` und `ctrl` + `-` \ (oder `ctrl` + Mausrad \) beeinflussen.  Zoom kann weiterhin mithilfe von [put_ZoomFactor][ReferenceWin32Icorewebview2hostPutZoomfactor09430] festgelegt werden, wenn die Einstellung deaktiviert ist.  
*   ZoomFactor geändert, um nur auf die aktuelle WebView anzuwenden.  Zoom Änderungen an der aktuellen WebView wirken sich nicht auf andere Webansichten aus, die Sie zur gleichen Ursprungssite navigiert haben.  Wenn Sie weitere Informationen wünschen, navigieren Sie zu [get_ZoomFactor][ReferenceWin32Icorewebview2hostGetZoomfactor09430].  
*   HID-zoomview-UI für WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   [SetBoundsAndZoomFactor][ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]hinzugefügt.  Nun können Sie den Zoomfaktor und die Grenzen eines Webviews gleichzeitig einstellen.  
*   [WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] -Ereignis hinzugefügt.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [add_WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] \ ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Unterstützung für den `beforeunload` Dialogfeldtyp für JavaScript-Dialog Ereignisse hinzugefügt und [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430] Enum-Eintrag hinzugefügt.  
*   [GetHeaders][ReferenceWin32Icorewebview2httprequestheadersGetheaders09430] zu HttpRequestHeaders, [GetHeader][ReferenceWin32Icorewebview2httpresponseheadersGetheader09430] zu HttpResponseHeaders und [get_HasCurrentHeader][ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430] -Eigenschaft zu HttpHeadersCollectionIterator hinzugefügt.  
*   > [!IMPORTANT]
    > **Aktuelle Änderung**: geändertes `DevToolsProtocolEventReceived` Verhalten.  Nun können Sie einen [DevToolsProtocolEventReceiver][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430] für ein bestimmtes devtools-Protokollereignis erstellen und dieses Ereignis mithilfe [add_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]remove_DevToolsProtocolEventReceived abonnieren/abbestellen / [][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430].
*   > [!IMPORTANT]
    > Unter **brechende Änderung**: `WebMessageReceivedEventArgs` [get_WebMessageAsString][ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190] -Eigenschaft in eine [TryGetWebMessageAsString][ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430] -Methode geändert.  
*   > [!IMPORTANT]
    > **Umbruch Änderung**: geänderte `AcceleratorKeyPressedEventArgs` [handle][ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190] -Methode in eine [get_Handled][ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430] -Eigenschaft.  

## 0.8.355

[NuGet-Paket][NuGetGallery0.8.355] \ | minimale Microsoft Edge-Version 80.0.355.0.

*   Veröffentlichtes WebView2API-Beispiel, eine umfassende Anleitung zum WebView2-SDK.  Weitere Informationen finden Sie unter [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   IME-Unterstützung für alle Sprachen außer Englisch ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\) hinzugefügt.  
*   Die API-Oberfläche des `WebResourceRequested` Ereignisses wurde als Reaktion auf Fehlerberichte aktualisiert.  Das gleichzeitige angeben eines Filters und eines Ereignisses bei der Erstellung ist jetzt veraltet.  Zum Erstellen eines angeforderten Webressource-Ereignisses verwenden Sie [add_WebResourceRequested][ReferenceWin32Iwebview2webview5AddWebresourcerequested08190] , um das Ereignis und [AddWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190] hinzuzufügen, um einen Filter hinzuzufügen.  [RemoveWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190] entfernt den Filter \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > Unter **brechende Änderung**: geändertes Vollbild-Verhalten.  Veraltete [IsFullScreenAllowed][ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190].  Wenn ein Element innerhalb einer WebView-Datei (beispielsweise ein Video) auf Vollbild eingestellt ist, wird nun standardmäßig die Begrenzungen der WebView-Ansicht ausgefüllt.  Verwenden Sie das [ContainsFullScreenElementChanged][ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190] -Ereignis und [get_ContainsFullScreenElement][ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190] , um anzugeben, wie die APP die Größe der WebView ändern soll, wenn ein Element in den Vollbildmodus wechseln möchte.  

## 0.8.314  

[NuGet-Paket][NuGetGallery0.8.314] \ | minimale Microsoft Edge-Version 80.0.314.0.  

*   Unterstützung für Windows 7, Windows 8 und Windows 8,1 wurde hinzugefügt.  
*   Visual Studio-und Visual Studio-Code-Debug-Unterstützung für WebView2 hinzugefügt.  Debuggen Sie nun Ihr Skript in der WebView2 direkt von der IDE aus.  Weitere Informationen finden Sie unter [Debuggen bei der Entwicklung mit WebView2-Steuerelementen][HowtoDebug].  
*   Hinzugefügt `Native Object Injection` , wodurch das in WebView2 ausgeführte Skript auf ein IDispatch-Objekt aus der Win32-Komponente der Anwendung zugreifen und auf die Eigenschaften des IDispatch-Objekts zugreifen kann.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [addremoteobject][ReferenceWin32Iwebview2webview4Addremoteobject08190] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Ereignis hinzugefügt `AcceleratorKeyPressed` .  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [add_AcceleratorKeyPressed][ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Deaktiviert `Context Menus` .  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zu [put_AreDefaultContextMenusEnabled][ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Aktualisiert `DPI Awareness` .  Die dpi-Bekanntheit von WebView ist nun identisch mit der dpi-Bekanntheit der Hostanwendung.  
    
    > [!NOTE]
    > Wenn eine andere Hybridanwendung mit einer anderen dpi-Sensibilisierung als die ursprüngliche WebView gestartet wird, wird die neue WebView nicht gestartet, wenn das Benutzerdatenverzeichnis identisch ist \ ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Aktualisiert `Notification Change Behavior` , damit WebView2 die Benachrichtigungs Berechtigungsanforderungen, die von Webinhalten, die in der WebView gehostet werden, automatisch ablehnen.  

## 0.8.270  

[NuGet-Paket][NuGetGallery0.8.270] \ | minimale Microsoft Edge-Version 78.0.270.0.  

*   Ereignis hinzugefügt `DocumentTitleChanged` , um die Änderung des Dokumenttitels anzugeben \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   API hinzugefügt `GetWebView2BrowserVersionInfo` \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Ereignis hinzugefügt `NewWindowRequested` .  
*   `CreateWebView2EnvironmentWithDetails`Zu entfernende zu aktualisierende Funktion `releaseChannelPreference` .  Weitere Informationen zur `CreateWebView2EnvironmentWithDetails` Funktion finden Sie unter [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Die Überschreibung der Registrierungs-und Umgebungsvariablen wird weiterhin unterstützt.  Die Standardkanal Einstellung wird nur verwendet, wenn Sie überschrieben wird.  
    Während der Kanalsuche überspringt das WebView-Team jede vorherige Kanalversion, die nicht mit dem WebView2-SDK kompatibel ist.  
    Das WebView-Team wählt den stabileren Kanal aus, um die konsistentsten Verhaltensweisen für den Endbenutzer zu gewährleisten.  Wenn Sie mit den neuesten Canary-Builds testen, sollten Sie ein Skript erstellen, um die `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` Umgebungsvariable `1` vor dem Starten der App festzulegen.  
*   Die `CreateWebView2EnvironmentWithDetails` Funktion wurde mit der Logik für die Auswahl aktualisiert `userDataFolder` , wenn nicht angegeben.  Weitere Informationen zur `CreateWebView2EnvironmentWithDetails` Funktion finden Sie unter [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Wenn Sie zuvor den Standard `userDataFolder` Speicherort verwendet haben, wird beim Wechseln zum neuen SDK der Standardwert `userDataFolder` zurückgesetzt \ (auf einen neuen Speicherort im Host Codeverzeichnis festgesetzt \), und ihr Zustand wird ebenfalls zurückgesetzt.  
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
*   Hinzugefügt: include Path, Linking und autocopying von DLL-Dateien in NuGet- `TARGET` Datei im SDK.  
*   `window.open()`In Skript anfordern aktiviert.  

## 0.8.149  

[NuGet-Paket][NuGetGallery0.8.149] \ | minimale Microsoft Edge-Version 76.0.149.0.  

Erste Entwickler-Preview-Version.  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Evergreen-Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[Webview2ConceptsDistributionFixedVersionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Fester Versions Verteilungsmodus – Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Grundlegendes zur WebView2-Laufzeit und zum Installationsprogramm – Verteilung von Anwendungen mithilfe von WebView2 | Microsoft docs"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Gruppenrichtlinien für WebView2-Verwalten von WebView2-Anwendungen | Microsoft docs"  
[ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Experimentelle APIs – Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-apps | Microsoft docs"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF | Microsoft docs"  
[HowtoDebug]: ./howto/debug.md "Debuggen bei der Entwicklung mit WebView2-Steuerelementen | Microsoft docs"  

[ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle-Interface-IWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "Schnittstelle IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft docs"  
[ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled-Interface IWebView2Settings2 | Microsoft docs"  
[ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated-Interface IWebView2Settings | Microsoft docs"  
[ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString-Interface IWebView2WebMessageReceivedEventArgs | Microsoft docs"  
[ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed-Interface IWebView2WebView4 | Microsoft docs"  
[ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged-Interface IWebView2WebView | Microsoft docs"  
[ReferenceWin32Iwebview2webview4Addremoteobject08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "Addremoteobject-Schnittstelle IWebView2WebView4 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5AddWebresourcerequested08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested-Interface IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter-Interface-IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement-Interface IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter-Interface-IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-Globals | Microsoft docs"  

[ReferenceWin32Icorewebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "Schnittstelle ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled-Interface ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2AddContentloading09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddHistorychanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2Addremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "Addremoteobject-Schnittstelle ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddSourcechanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddWindowcloserequested09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "Schnittstelle ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived-Interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived-Interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo-Interface ICoreWebView2Environment | Microsoft docs"  
[ReferenceWin32Icorewebview2host09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "Schnittstelle ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-Globals | Microsoft docs"  
[ReferenceWin32Icorewebview2hostGetZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor-Interface ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged-Interface-ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2hostPutZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor-Interface ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor-Interface-ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader-Interface ICoreWebView2HttpHeadersCollectionIterator | Microsoft docs"  
[ReferenceWin32Icorewebview2httprequestheadersGetheaders09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders-Interface ICoreWebView2HttpRequestHeaders | Microsoft docs"  
[ReferenceWin32Icorewebview2httpresponseheadersGetheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader-Interface ICoreWebView2HttpResponseHeaders | Microsoft docs"  
[ReferenceWin32Icorewebview2Removeremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString-Interface-ICoreWebView2WebMessageReceivedEventArgs | Microsoft docs"  

[ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2Addhostobjecttoscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddNewwindowrequested09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested-Interface ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentoptions09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "Schnittstelle ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalCompositionController | Microsoft docs"
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalCompositionController | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalpointerinfo09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalPointerInfo | Microsoft docs"  
[ReferenceWin32Icorewebview2Removehostobjectfromscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Microsoft docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-Globals | Microsoft docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Microsoft docs"  

[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged-Interface ICoreWebView2ExperimentalController | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode-Interface ICoreWebView2ExperimentalController | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale-Interface ICoreWebView2ExperimentalController | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges-Interface ICoreWebView2ExperimentalController | Microsoft docs"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Microsoft. Web. WebView2. Core-Namespace | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft. Web. WebView2. WPF-Namespace | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft. Web. WebView2. WinForms-Namespace | Microsoft docs"  

[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2. WebView2RuntimeNotFound (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "CoreWebView2-Klasse (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "CoreWebView2Environment-Klasse (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment. CompareBrowserVersions (String, String)-Methode (Microsoft. Web. WebView2. Core) | Microsoft docs"
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "CoreWebView2Environment. GetAvailableBrowserVersionString (String)-Methode (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "CoreWebView2. mswebviewnewwindowrequested-Ereignis (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "CoreWebView2. PermissionRequested-Ereignis (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "CoreWebView2. ScriptDialogOpening-Ereignis (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "CoreWebView2. WebResourceRequested-Ereignis (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "CoreWebView2HttpRequestHeaders-Klasse (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "CoreWebView2HttpResponseHeaders-Klasse (Microsoft. Web. WebView2. Core) | Microsoft docs"  

[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "CoreWebView2CreationProperties-Klasse (Microsoft. Web. WebView2. WinForms) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Webview2. Source-Klasse (Microsoft. Web. Webview2. WinForms) | Microsoft docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "WebView2. BuildWindowCore (HandleRef)-Methode (Microsoft. Web. WebView2. WPF) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "WebView2. DestroyWindowCore (HandleRef)-Methode (Microsoft. Web. WebView2. WPF) | Microsoft docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "Microsoft. Web. webview2. WPF. webview2. acceleratorkeypressed | Microsoft docs"  

[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "CoreWebView2InitializationCompletedEventArgs Klasse | Microsoft docs"  

[ReferenceWin32Icorewebview2Addhostobjecttoscript09538]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript-Interface-ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived-Interface ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled-Interface ICoreWebView2ExperimentalEnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures-Interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalWindowFeatures | Microsoft docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated-Schnittstelle ICoreWebView2NewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed-Interface ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  

[ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount-Interface ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments-Interface ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures-Interface ICoreWebView2NewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2windowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "Schnittstelle ICoreWebView2WindowFeatures | Microsoft docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft Edge"  
[ReferenceWin32Icorewebview2experimentalenvironment09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.628-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalEnvironment | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent-Interface-ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft docs"  

[ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded-Interface ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived-Interface ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalGetCookiemanager10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager-Interface ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalGetEnvironment10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment-Interface ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest-Interface-ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2#get_systemcursorid?view=webview2-1.0.674-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent-Schnittstelle ICoreWebView2ExperimentalWebResourceResponseView | Microsoft docs"  

[ReferenceWin32Icorewebview2experimentalcompositioncontroller3]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "Schnittstelle ICoreWebView2ExperimentalCompositionController3 | Microsoft docs"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge – Richtlinien | Microsoft docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2-Richtlinien | Microsoft docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender Application Guard (Windows 10) – Windows-Sicherheit | Microsoft docs"

[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "CancelEventArgs-Klasse (System. ComponentModel) | Microsoft docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "EventArgs-Klasse (System) | Microsoft docs"  
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
[GithubMicrosoftedgeWebviewfeedbackIssue168]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 177"
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 185"
[GithubMicrosoftedgeWebviewfeedbackIssue204]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 204"
[GithubMicrosoftedgeWebviewfeedbackIssue219]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 219"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 235"
[GithubMicrosoftedgeWebviewfeedbackIssue250]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 250"
[GithubMicrosoftedgeWebviewfeedbackIssue288]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 288"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Feedback Repo für MicrosoftEdge/WebViewFeedback Issue 611"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]:  https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Ankündigungs-Repo für MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Verschieben eines Projekts zur Verwendung der neuesten WebView2 SDK-0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Ankündigung der allgemeinen Verfügbarkeit für Microsoft Edge WebView2 für .net und feste Verteilungsmethode | .net-Blog"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge-WebView2 | Microsoft Edge-Entwickler"  

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
[NuGetGallery1.0.622.22]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "NuGet-Katalog | Microsoft. Web. WebView2 v 1.0.622.22"
[NuGetGallery1.0.664.34]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "NuGet-Katalog | Microsoft. Web. WebView2 v 1.0.664.34"
[NuGetGallery1.0.664.37]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "NuGet-Katalog | Microsoft. Web. WebView2 v 1.0.664.37"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "NuGet-Katalog | Microsoft. Web. WebView2 v 0.9.628-Vorabversion"  
[NuGetGallery1.0.674-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "NuGet-Katalog | Microsoft. Web. WebView2 v 1.0.674-Vorabversion"  
[NuGetGallery1.0.721-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "NuGet-Katalog | Microsoft. Web. WebView2 v 1.0.721-Vorabversion"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Ankündigung der allgemeinen Verfügbarkeit von Microsoft Edge WebView2 | Microsoft Edge-Blog"  
