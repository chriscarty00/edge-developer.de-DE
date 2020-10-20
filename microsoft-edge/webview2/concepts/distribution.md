---
description: Verteilungsoptionen beim Freigeben einer APP mit Microsoft Edge WebView2
title: Verteilung von Microsoft Edge WebView2-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: bf0a79d41d9eddf39a31426db79d502c09b782ad
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120347"
---
# Verteilung von apps mithilfe von WebView2  

Stellen Sie beim Verteilen der WebView2-App sicher, dass die Backing-Webplattform, die [WebView2-Laufzeit][Webview2Installer], vorhanden ist, bevor die APP gestartet wird.  In diesem Artikel wird beschrieben, wie Sie die WebView2-Laufzeit installieren können, und wie Sie die beiden Verteilungs Modi für Ihre WebView2-App verwenden:  [immergrüne](#evergreen-distribution-mode) und [Feste Version](#fixed-version-distribution-mode).  

## Immergrüner Verteilungsmodus  

> [!NOTE]
> Der immergrüne Verteilungsmodus wird für die meisten Entwickler empfohlen.  

Der immergrüne Verteilungsmodus sorgt dafür, dass Ihre APP die neuesten Funktionen und Sicherheitsupdates nutzt.  Sie weist die folgenden Merkmale auf:  

*   Die zugrunde liegende Web-Plattform \ (WebView2 Runtime \) wird automatisch ohne zusätzlichen Aufwand von Ihnen aktualisiert.  
*   Alle apps, die den immergrünen Verteilungsmodus verwenden, verwenden eine freigegebene Kopie der immergrünen WebView2-Laufzeit, wodurch Speicherplatz gespart wird.  
    
### Grundlegendes zur WebView2-Laufzeit  

Die WebView2-Laufzeit ist eine verteilbare Laufzeit und dient als Sicherungs Webplattform für WebView2-apps.  Das Konzept ähnelt Visual c++ oder .NET Runtime für C++-/.net-apps.  Die Common Language Runtime enthält geänderte Microsoft Edge \ (Chromium \)-Binärdateien, die für apps optimiert und getestet wurden.  Bei der Installation wird die Laufzeit nicht als Benutzersicht barer Browser angezeigt.  Ein Benutzer verfügt beispielsweise nicht über eine Browser-Desktopverknüpfung oder ein Startmenü-Eintrag.  

Während der Entwicklung und Prüfung können Sie entweder als Hintergrund-Webplattform verwenden.  

*   Die WebView2-Laufzeit  
*   Any Insider \ (nicht-stable \) Microsoft Edge \ (Chrom \) Browser Kanal  

In Produktionsumgebungen müssen Sie sicherstellen, dass die Runtime auf Benutzergeräten vorhanden ist, bevor die APP gestartet wird.  Der Microsoft Edge stable-Kanal steht für die WebView2-Verwendung nicht zur Verfügung.  Die Entscheidung verhindert, dass apps eine Abhängigkeit vom Browser in der Produktion übernehmen.

Nehmen Sie keine Abhängigkeit vom Browser auf, da:  

*   Microsoft Edge \ (Chrom \) ist auf allen Benutzergeräten nicht garantiert vorhanden.  Geräte, die nicht mit Windows Update verbunden sind oder nicht direkt von Microsoft verwaltet werden \ (ein großer Teil des Enterprise-und edu-Marktes), haben möglicherweise nicht den Browser.  Durch das Verteilen der WebView2-Laufzeit wird verhindert, dass eine Abhängigkeit vom Browser als Voraussetzung für apps berücksichtigt wird.  
*   In Browsern und apps gibt es unterschiedliche Anwendungsfälle, und daher kann es vorkommen, dass eine Abhängigkeit von einem Browser unbeabsichtigte Nebeneffekte für Ihre apps hat.  So können IT-Administratoren beispielsweise den Browser für die interne Website Kompatibilität steuern.  Mit der WebView2-Laufzeit können apps immergrün bleiben, während Browser Updates aktiv verwaltet werden.  
*   Im Gegensatz zum Browser wird die Common Language Runtime für App-Szenarien entwickelt und getestet und kann in einigen Fällen Fehlerkorrekturen beinhalten, die im Browser noch nicht verfügbar sind.  
    
In Zukunft wird die Evergreen WebView2-Laufzeit in zukünftigen Versionen von Windows ausgeliefert.  Stellen Sie die Laufzeit mit der Produktions-App bereit, bis die Common Language Runtime universell verfügbar ist.  

### Bereitstellen der immergrünen WebView2-Laufzeit  

Für alle Evergreen-apps auf dem Gerät ist nur eine Installation der Evergreen WebView2-Laufzeit erforderlich.  Auf der [Download Seite der WebView2-Laufzeit][Webview2Installer]sind verschiedene Tools verfügbar.  Die folgenden Tools unterstützen Sie beim Bereitstellen der Evergreen-Laufzeit.  

*   WebView2 Runtime-Bootstrapper ist ein kleines (ca. 2 MB \)-Installationsprogramm.  WebView2-Runtime-Bootstrapper lädt die Evergreen-Laufzeit von Microsoft-Servern herunter und installiert Sie, die der Gerätearchitektur des Benutzers entspricht.  
*   Verwenden Sie einen Link, um den Bootstrapper programmgesteuert herunterzuladen.  
*   Das Standalone-Installationsprogramm von WebView2 Runtime ist ein vollständiges Installationsprogramm, das die immergrüne WebView2-Runtime in Offlineumgebungen installieren kann.  
    
Derzeit unterstützen sowohl der Bootstrapper als auch das Standalone-Installationsprogramm nur Installationen pro Computer, für die eine Anhebung erforderlich ist.  Wenn ein Installationsprogramm ohne Elevation ausgeführt wird, wird der Benutzer aufgefordert, Berechtigungen zu erhöhen.  

Wir empfehlen die folgenden Workflows, um sicherzustellen, dass die Laufzeit bereits installiert ist, bevor Ihre APP gestartet wird.  Sie können Ihren Workflow je nach Szenario anpassen.  Beispielcode steht in den [Beispielen Repo][InstallerSample]zur Verfügung.  

#### Nur Online Bereitstellung  

Führen Sie die folgenden Schritte aus, wenn Sie über ein Szenario für die Onlinebereitstellung verfügen, in dem Endbenutzer davon ausgegangen werden, dass Sie über einen Internetzugriff verfügen.  

1.  Stellen Sie während der APP-Einrichtung sicher, dass die Laufzeit bereits installiert ist.  Führen Sie eine der folgenden Aktionen aus, um dies zu überprüfen.  
    *   Überprüfen Sie `pv (REG_SZ)` , ob die der Registrierungsschlüssel vorhanden und nicht `null` oder leer ist.  Suchen Sie  `pv (REG_SZ)` an der folgenden Position.  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```
          
    *   Führen Sie [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] aus, und stellen Sie sicher, dass das `versionInfo` is `NULL` .  
1.  Wenn die Common Language Runtime nicht installiert ist, verwenden Sie den Link zum programmgesteuerten Download des Bootstrappers.  
1.  Rufen Sie den Bootstrapper über einen erhöhten Prozess oder eine Eingabeaufforderung mit `MicrosoftEdgeWebview2Setup.exe /silent /install` für die unbeaufsichtigte Installation auf.  
    
Der vorherige Workflow bietet die folgenden Vorteile.  

*   Installieren Sie die Laufzeit nur bei Bedarf, oder wenn Sie nicht zum Verpacken von Installationsprogrammen verpflichtet sind.  
*   Der Bootstrapper erkennt die Gerätearchitektur automatisch und installiert die übereinstimmende Laufzeit. 
*   Installieren Sie die Laufzeit automatisch.  
    
Sie können den Bootstrapper auch mit Ihrer APP Verpacken, anstatt ihn bei Bedarf programmgesteuert herunterzuladen.  

#### Offline Bereitstellung  

Führen Sie die folgenden Schritte aus, wenn Sie über ein Offline Bereitstellungsszenario verfügen, in dem die APP-Bereitstellung vollständig Offline funktionieren muss.  

1.  Laden Sie das [Standalone-Installationsprogramm][Webview2Installer]herunter.  
1.  Fügen Sie das Installationsprogramm in Ihr App-Installationsprogramm oder Updater ein.  
1.  Stellen Sie während der APP-Einrichtung sicher, dass die Laufzeit bereits installiert ist.  Führen Sie eine der folgenden Aktionen aus, um dies zu überprüfen.  
    *   Überprüfen Sie `pv (REG_SZ)` , ob die der Registrierungsschlüssel vorhanden und nicht `null` oder leer ist.  Suchen Sie  `pv (REG_SZ)` an der folgenden Position.  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```
          
    *   Führen Sie [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] aus, und stellen Sie sicher, dass das `versionInfo` is `NULL` .  
1.  Wenn die Common Language Runtime nicht installiert ist, führen Sie das eigenständige Installationsprogramm aus.  Wenn Sie eine unbeaufsichtigte Installation ausführen möchten, führen Sie das Installationsprogramm entweder über einen erhöhten Prozess aus, oder kopieren Sie den folgenden Befehl, und führen Sie ihn aus.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### Im Evergreen-Modus kompatibel bleiben

Das Web entwickelt sich ständig weiter. Die Evergreen WebView2-Laufzeit wird auf dem neuesten Stand gehalten, um Ihnen die neuesten Funktionen und Sicherheitsupdates zur Verfügung zu stellen.  Wenn Sie sicherstellen möchten, dass Ihre APP mit dem Web kompatibel bleibt, empfehlen wir, die Testinfrastruktur einzurichten.

Nicht stabile Microsoft Edge-Kanäle \ (Beta/dev/Canary \) bieten einen kleinen Einblick in das, was als nächstes in die WebView2-Laufzeit kommt.  Genau wie bei der Entwicklung von Websites für Microsoft Edge empfiehlt es sich, ihre WebView2-App regelmäßig zu testen.  Testen Sie Ihre WebView2-App mit einem der nicht stabilen Kanäle, und aktualisieren Sie Ihre APP, oder [melden Sie Probleme][GithubMicrosoftedgeWebviewfeedback] , wenn Probleme auftreten. In der Regel sind dev und Beta die empfohlenen Kanäle.  Navigieren Sie zur [Übersicht über die Microsoft Edge-Kanäle][DeployEdgeMicrosoftEdgeChannels], damit Sie entscheiden können, welcher Kanal richtig ist.  Sie können den [nicht stabilen Microsoft Edge-Kanal][DownloadNonstableEdge] in Ihrer Testumgebung herunterladen und mithilfe von `regkey` oder Umgebungsvariablen die Kanaleinstellungen für Ihre Test-App angeben.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  Sie können auch [WebDriver][HowtoWebdriver] verwenden, um WebView2-Tests zu automatisieren.

## Modus für feste Versions Verteilung  

> [!NOTE]
> Der Modus für die feste Versions Verteilung befindet sich in der öffentlichen Vorschau.  

Der Modus für die feste Versions Verteilung wurde zuvor mit "eigene Version" benannt.  

In Umgebungen mit eingeschränkter Kompatibilität, die strenge Kompatibilitätsanforderungen erfüllen, sollten Sie die Verwendung des festen Versions Verteilungsmodus in Frage stellen.  Wählen Sie eine bestimmte Version der WebView2-Runtime aus, und Verpacken Sie Sie mit dem Verteilungsmodus für feste Versionen.  Sie können die Anzeigedauer von Laufzeitupdates für Ihre APP angeben.  Der Modus für die feste Versions Verteilung erhält keine automatischen Updates. Sie sollten planen, Ihre APP und die Laufzeit zu aktualisieren.  

Wenn Sie den Modus "feste Version" verwenden möchten,  

*   [Laden][Webview2Installer] Sie das Paket mit fester Version herunter, und Dekomprimieren Sie das Paket.  
*   Fügen Sie die dekomprimierten Binärdateien der festen Version in Ihr Projekt ein.  
*   Geben Sie den Pfad zu den Binärdateien der festen Version an, wenn Sie die WebView2-Umgebung erstellen.  
    *   Für Win32 C/C++ können Sie die Umgebung mithilfe der Funktion [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions] erstellen.  Verwenden Sie den `browserExecutableFolder` Parameter, um den Pfad zu den Binärdateien fester Version anzugeben.  
    *   Für .net können Sie eine der folgenden Optionen ausführen, um die Umgebung anzugeben.  
        
        > [!NOTE]
        > Sie müssen die Umgebung angeben, bevor die WebView2 `Source` -Eigenschaft wirksam wird.  
        
        *   Setzen Sie die `CreationProperties` \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\)-Eigenschaft für das WebView2-Element.  Verwenden Sie das `BrowserExecutableFolder` Mitglied in der `CoreWebView2CreationProperties` \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\)-Klasse, um den Pfad zu den Binärdateien fester Version anzugeben.  
        *   Verwenden `EnsureCoreWebView2Async` Sie \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\), um die Umgebung anzugeben.  Verwenden Sie den `browserExecutableFolder` Parameter in [CoreWebView2Environment. createasync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] , um den Pfad zu den Binärdateien fester Version anzugeben.  
*   Verpacken und versenden Sie die Binärdateien der festen Version mit Ihrer APP.  Aktualisieren Sie die Binärdateien nach Bedarf.  
    
<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  

[HowtoWebdriver]: ../howto/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft docs"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "Createasync-Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse | Microsoft docs"  

[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WPF. WebView2 Klasse | Microsoft docs"  

[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WinForms. WebView2 Klasse | Microsoft docs"  

[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "CoreWebView2CreationProperties-Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties Klasse | Microsoft docs"  

[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft. Web. WebView2. WinForms Klasse | Microsoft docs"  

[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties-Microsoft. Web. WebView2. WPF. WebView2 Klasse | Microsoft docs"  

[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Microsoft. Web. WebView2. WinForms. WebView2 Klasse | Microsoft docs"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  

[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Microsoft docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm"  

[InstallerSample]: https://aka.ms/wv2installersample "Beispiel für ein WebView2-Installationsprogramm"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback | GitHub"  
