---
description: Verteilungsoptionen beim Freigeben einer APP mit Microsoft Edge WebView2
title: Verteilung von Microsoft Edge WebView2-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, WPF-apps, WPF, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 0cbaaeade03feac766647c55bb5edabfe8e8456e
ms.sourcegitcommit: 7b16c3e6eb458e0b2458279c2498597fb227bc8c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182909"
---
# Verteilung von apps mithilfe von WebView2  

Stellen Sie beim Verteilen Ihrer WebView2-App sicher, dass die Sicherungs-Webplattform, die [WebView2-Laufzeit][Webview2Installer], vor dem Start der app vorhanden ist.  In diesem Artikel wird beschrieben, wie Sie die WebView2-Runtime installieren \ (der Entwickler \) und die beiden Verteilungs Modi für Ihre WebView2-App verwenden:  [immergrüne](#evergreen-distribution-mode) und [Feste Version](#fixed-version-distribution-mode).  

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

*   Microsoft Edge \ (Chrom \) wird nicht garantiert auf allen Benutzergeräten vorhanden sein.  Geräte, die nicht mit Windows Update verbunden sind oder nicht direkt von Microsoft verwaltet werden \ (ein großer Teil des Enterprise-und edu-Marktes), haben möglicherweise nicht den Browser.  Durch das Verteilen der WebView2-Laufzeit wird verhindert, dass eine Abhängigkeit vom Browser als Voraussetzung für apps berücksichtigt wird.  
*   In Browsern und apps gibt es unterschiedliche Anwendungsfälle, und daher kann es vorkommen, dass eine Abhängigkeit von einem Browser unbeabsichtigte Nebeneffekte für Ihre apps hat.  So können IT-Administratoren beispielsweise den Browser für die interne Website Kompatibilität steuern.  Mit der WebView2-Laufzeit können apps immergrün bleiben, während Browser Updates aktiv verwaltet werden.  
*   Im Gegensatz zum Browser wird die Common Language Runtime für App-Szenarien entwickelt und getestet und kann in einigen Fällen Fehlerkorrekturen beinhalten, die im Browser noch nicht verfügbar sind.  
    
In Zukunft plant die Evergreen WebView2-Laufzeit, mit zukünftigen Versionen von Windows ausgeliefert zu werden.  Stellen Sie die Laufzeit mit der Produktions-App bereit, bis die Common Language Runtime universell verfügbar ist.  

### Bereitstellen der immergrünen WebView2-Laufzeit  

Für alle Evergreen-apps auf dem Gerät ist nur eine Installation der Evergreen WebView2-Laufzeit erforderlich.  Auf der [Download Seite der WebView2-Laufzeit][Webview2Installer]sind verschiedene Tools verfügbar.  Die folgenden Tools unterstützen Sie beim Bereitstellen der Evergreen-Laufzeit.  

*   WebView2 Runtime-Bootstrapper ist ein kleines (ca. 2 MB \)-Installationsprogramm.  WebView2-Runtime-Bootstrapper lädt die Evergreen-Laufzeit von Microsoft-Servern herunter und installiert Sie, die der Gerätearchitektur des Benutzers entspricht.  
*   Verwenden Sie einen Link, um den Bootstrapper programmgesteuert herunterzuladen.  
*   Das Standalone-Installationsprogramm von WebView2 Runtime ist ein vollständiges Installationsprogramm, das die immergrüne WebView2-Runtime in Offlineumgebungen installiert.  
    
Derzeit unterstützen sowohl der Bootstrapper als auch das Standalone-Installationsprogramm nur Installationen pro Computer, für die eine Anhebung erforderlich ist.  Wenn ein Installationsprogramm ohne Elevation ausgeführt wird, wird der Benutzer aufgefordert, Berechtigungen zu erhöhen.  

Verwenden Sie die folgenden Workflows, um sicherzustellen, dass die Laufzeit bereits installiert ist, bevor Ihre APP gestartet wird.  Sie können Ihren Workflow je nach Szenario anpassen.  Beispielcode steht in den [Beispielen Repo][GitHubMicrosoftedgeWebView2samplesWebview2Deployment]zur Verfügung.  

#### Nur Online Bereitstellung  

Führen Sie die folgenden Schritte aus, wenn Sie über ein Online Bereitstellungsszenario verfügen, in dem Benutzer davon ausgehen, dass Sie über einen Internetzugriff verfügen.  

1.  Stellen Sie während der APP-Einrichtung sicher, dass die Laufzeit bereits installiert ist.  Führen Sie eine der folgenden Aktionen aus, um dies zu überprüfen.  
    *   Überprüfen Sie `pv (REG_SZ)` , ob die der Registrierungsschlüssel vorhanden und nicht `null` oder leer ist.  Suchen Sie  `pv (REG_SZ)` an der folgenden Position.  
        
        Unter 64-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Unter 32-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Führen Sie [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] aus, und stellen Sie sicher, dass das `versionInfo` is `NULL` .  
1.  Wenn die Laufzeit nicht installiert ist, verwenden Sie den Link zum programmgesteuerten herunterladen des Bootstrappers.  
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
        
        Unter 64-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Unter 32-Bit-Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Führen Sie [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] aus, und stellen Sie sicher, dass das `versionInfo` is `NULL` .  
1.  Wenn die Laufzeit nicht installiert ist, führen Sie das eigenständige Installationsprogramm aus.  Wenn Sie eine unbeaufsichtigte Installation ausführen möchten, führen Sie das Installationsprogramm entweder über einen erhöhten Prozess aus, oder kopieren Sie den folgenden Befehl, und führen Sie ihn aus.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### Im Evergreen-Modus kompatibel bleiben  

Das Web entwickelt sich ständig weiter.  Die Evergreen WebView2-Laufzeit wird auf dem neuesten Stand gehalten, um Ihnen die neuesten Funktionen und Sicherheitsupdates zur Verfügung zu stellen.  Wenn Sie sicherstellen möchten, dass Ihre APP mit dem Web kompatibel bleibt, sollten Sie die Testinfrastruktur einrichten.  

Nicht stabile Microsoft Edge-Kanäle \ (Beta/dev/Canary \) bieten einen kleinen Einblick in das, was als nächstes in die WebView2-Laufzeit kommt.  Genau wie bei der Entwicklung von Websites für Microsoft Edge sollten Sie Ihre WebView2-App regelmäßig testen.  Testen Sie Ihre WebView2-App mit einem der nicht stabilen Kanäle, und aktualisieren Sie Ihre APP, oder [melden Sie Probleme][GithubMicrosoftedgeWebviewfeedback] , wenn Probleme auftreten. In der Regel sind dev und Beta die empfohlenen Kanäle.  Navigieren Sie zur [Übersicht über die Microsoft Edge-Kanäle][DeployEdgeMicrosoftEdgeChannels], damit Sie entscheiden können, welcher Kanal richtig ist.  Sie können den [nicht stabilen Microsoft Edge-Kanal][DownloadNonstableEdge] in Ihrer Testumgebung herunterladen und mithilfe von `regkey` oder Umgebungsvariablen die Kanaleinstellungen für Ihre Test-App angeben.  Weitere Informationen finden Sie unter [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  Sie können auch [WebDriver][HowtoWebdriver] verwenden, um WebView2-Tests zu automatisieren.

## Modus für feste Versions Verteilung   

In Umgebungen mit eingeschränkter Kompatibilität, die strenge Kompatibilitätsanforderungen erfüllen, sollten Sie die Verwendung des festen Versions Verteilungsmodus in Frage stellen.  Wählen Sie eine bestimmte Version der WebView2-Runtime aus, und Verpacken Sie Sie mit dem Verteilungsmodus für feste Versionen.  Sie können die Anzeigedauer von Laufzeitupdates für Ihre APP angeben.  Der Modus für die feste Versions Verteilung erhält keine automatischen Updates. Planen Sie, Ihre APP und die Laufzeit zu aktualisieren.  

> [!NOTE] 
> Der Modus für die feste Versions Verteilung wurde zuvor als "eigene Version" bezeichnet.  

Führen Sie die folgenden Aktionen aus, um den Modus "feste Version" zu verwenden:

1.  [Herunterladen][Webview2Installer] des Pakets für die feste Version. 
1.  Dekomprimieren Sie das Paket mithilfe der Befehlszeile `expand {path to the package} -F:* {path to the destination folder}` oder mit Tools wie WinRAR. Vermeiden Sie eine Dekomprimierung über den Datei-Explorer, da Sie möglicherweise nicht die richtige Ordnerstruktur generiert.  
1.  Fügen Sie die dekomprimierten Binärdateien der festen Version in Ihr Projekt ein.  
1.  Geben Sie den Pfad zu den Binärdateien der festen Version an, wenn Sie die WebView2-Umgebung erstellen.  
    *   Für Win32 C/C++ können Sie die Umgebung mithilfe der Funktion [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions] erstellen.  Verwenden Sie den `browserExecutableFolder` Parameter, um den Pfad zu dem Ordner mit anzugeben `msedgewebview2.exe` .  
    *   Für .net können Sie eine der folgenden Optionen ausführen, um die Umgebung anzugeben.  
        
        > [!NOTE]
        > Sie müssen die Umgebung angeben, bevor die WebView2 `Source` -Eigenschaft wirksam wird.  
        
        *   Setzen Sie die `CreationProperties` \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\)-Eigenschaft für das WebView2-Element.  Verwenden Sie das `BrowserExecutableFolder` Mitglied in der `CoreWebView2CreationProperties` \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\)-Klasse, um den Pfad zu den Binärdateien fester Version anzugeben.  
        *   Verwenden `EnsureCoreWebView2Async` Sie \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\), um die Umgebung anzugeben.  Verwenden Sie den `browserExecutableFolder` Parameter in [CoreWebView2Environment. createasync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] , um den Pfad zu den Binärdateien fester Version anzugeben.  
1.  Verpacken und versenden Sie die Binärdateien der festen Version mit Ihrer APP.  Aktualisieren Sie die Binärdateien nach Bedarf.  
    
### Bekannte Probleme bei einer festen Version  

Im Vergleich zur Evergreen-Laufzeit verfügt die feste Version nicht über einen Installationsvorgang, der dazu führt, dass [Microsoft PlayReady][MicrosoftPlayReady] nicht ohne Änderungen funktioniert.  Sie können das Problem verringern, indem Sie die folgenden Aktionen ausführen.  

1.  Suchen Sie den Pfad, in dem Sie das Paket mit fester Version auf dem Gerät des Benutzers bereitstellen, beispielsweise den folgenden Speicherort.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Führen Sie die folgenden Befehle auf dem Gerät des Benutzers aus.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady sollte jetzt auf dem Gerät des Benutzers funktionieren.  Auf der Registerkarte " **Sicherheit** " des Ordners " **Feste Version** " sollte Sie Berechtigungen für `ALL APPLICATION PACKAGES` und verwenden `ALL RESTRICTED APPLICATION PACKAGES` .  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Berechtigung für PlayReady" lightbox="../media/play-ready-permission.png":::
        Berechtigung für PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Grundlegendes zu Browserversionen und WebView2 | Microsoft docs"  
[HowtoWebdriver]: ../howto/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft docs"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Microsoft docs"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Übersicht über die Microsoft Edge-Kanäle | Microsoft docs"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "Createasync-Microsoft. Web. WebView2. Core. CoreWebView2Environment Klasse | Microsoft docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WPF. WebView2 Klasse | Microsoft docs"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WinForms. WebView2 Klasse | Microsoft docs"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "CoreWebView2CreationProperties-Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties Klasse | Microsoft docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft. Web. WebView2. WinForms Klasse | Microsoft docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties-Microsoft. Web. WebView2. WPF. WebView2 Klasse | Microsoft docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Microsoft. Web. WebView2. WinForms. WebView2 Klasse | Microsoft docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm | Microsoft-Entwickler"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback | GitHub"  

[GitHubMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "WebView2-Bereitstellung – MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  
