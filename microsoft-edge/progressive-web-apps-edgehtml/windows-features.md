---
description: Progressives verbessern ihrer PWA für Windows mit nativen App-Features
title: Anpassen von PWA für Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.openlocfilehash: 5bad708db5b13517fd1887214a5e1d5457796ee2
ms.sourcegitcommit: e07de36ee9fbe20422ffc2c62b98839851e1b02b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2020
ms.locfileid: "10604011"
---
# Anpassen der PWA-EdgeHTML für Windows  

PWAs, die unter Windows 10 installiert sind, [nutzen alle Vorteile][PwaIndexWindows10] der Ausführung als [universelle Windows-Plattform \ (UWP \)][WindowsUWPGetStartedGuide] -apps, einschließlich Schutz durch die Sicherheit der Windows-App-Sandbox und Vollzugriff auf die [Windows-Runtime \ (WinRT \))][UwpApiIndex] -APIs, einschließlich der folgenden:  

*   Steuern von Gerätefunktionen \ (wie Kamera, Mikrofon, GPS \)  
*   Zugriff auf Benutzer Ressourcen \ (wie Kalender, Kontakte, Dokumente, Musik \)  
*   Starten/Navigieren in ihrer App mithilfe von Cortana-Sprachbefehlen  
*   Integration in das Windows-Betriebssystem \ (über das Windows-Aktions Center, die Desktop-Taskleiste und Kontextmenüs \)  

... und dies sind nur einige der zusätzlichen Möglichkeiten für Ihre PWA \ (EdgeHTML \) unter Windows!  

In diesem Leitfaden wird gezeigt, wie Sie Ihre PWA \ (EdgeHTML \) als Windows 10-App installieren, ausführen und verbessern und gleichzeitig die browserübergreifende und plattformübergreifende Kompatibilität sicherstellen.  

## Voraussetzungen  

*   Eine vorhandene PWA \ (oder gehostete Web-App \), entweder eine Live-oder eine localhost-Website.  In diesem Leitfaden wird das Beispiel PWA aus [Erste Schritte mit progressiven Web-Apps][PwaGetStarted]verwendet.  
*   Laden Sie die \ (Free \) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].  Sie können auch die Editionen Professional, Enterprise oder [Preview][MicrosoftVisualStudioPreview] verwenden.  Wählen Sie im Visual Studio-Installationsprogramm die folgenden Arbeitsauslastungen aus:  
    *   **Entwicklung der universellen Windows-Plattform**  

## Einrichten und Ausführen der universellen Windows-App  

Eine PWA \ (EdgeHTML \), die als Windows 10-App installiert ist, wird unabhängig vom Browser in einem eigenständigen \ ( `WWAHost.exe` Prozess \)-Fenster ausgeführt.  Für die Aktivierung wird einfach ein einfacher app-Wrapper benötigt, der Ihre gehostete Web-App enthält, die Sie mit der Visual Studio-Projektvorlage schnell einrichten können `Progressive Web App (Universal Windows)` .  \ (Alle Ihre APP-Logik, einschließlich des Sendens von systemeigenen Windows-Runtime-API-Anforderungen, erfolgt weiterhin in Ihrem ursprünglichen Web App-Code. \)  

Richten Sie Ihre Entwicklungsumgebung für die Windows-app in Visual Studio ein.  

1.  Aktivieren Sie in den Windows-Einstellungen den [Entwicklermodus][WindowsUWPGetStartedEnable].  \ (Geben `developer mode` Sie die Windows-Suchfunktion ein, um Sie zu finden. \)  
1.  Starten Sie Visual Studio, und **Erstellen Sie ein neues Projekt...**  
1.  Wählen Sie die Projektvorlage für die C#- **Windows-Anwendungsverpackung** aus.  Wenn Sie eine frühere Version von Visual Studio verwenden, suchen Sie die entsprechende Vorlage unter **Hosted Web App (Universal Windows)** oder **Progressive Web App (universelle Windows)**.  
1.  Wählen Sie die standardmäßige Windows 10 `Target version` \ (neueste Version) und `Minimum version` \ (Build 10586 oder höher \) aus, und klicken Sie auf **OK**.  

    ![Visual Studio-Auswahldialogfeld für UWP-Projektziel-Builds](media/vs-target-min-version.png)  

    Das neue Projekt wird geladen, wenn der Paket-appxmanifest-Designer geöffnet wird.  Hier konfigurieren Sie die Details Ihrer APP, einschließlich Paketidentität, Paketabhängigkeiten, erforderliche Funktionen, visuelle Elemente und Erweiterbarkeitspunkte.  Hierbei handelt es sich um eine leicht konfigurierbare, temporäre Version des App-paketmanifests, das während der APP-Entwicklung verwendet wird.  
    Wenn Sie Ihr App-Projekt erstellen, [generiert Visual Studio eine AppxManifest. XML-][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] Datei aus diesen Metadaten, die zum Installieren und Ausführen der APP verwendet wird.  Wenn Sie Ihre Datei aktualisieren, müssen Sie `package.appxmanifest` das Projekt neu erstellen, damit beide in ihrer zur Laufzeit wiedergegeben werden `AppxManifest.xml` .  

1.  Geben Sie im Manifest-Designer- **Anwendungs** Bereich die URL ihrer PWA als `Start page` .

    > [!NOTE]
    > Dienstmitarbeiter werden für alle HTTPS \ (Secure, Remote \)-URLs unterstützt, die als `StartPage` .  Dienstmitarbeiter werden standardmäßig nicht für Webanwendungen unterstützt, die eine lokale Startseite angeben.  Um die Unterstützung der Dienstmitarbeiter für diese Fälle zu aktivieren, fügen Sie dem Manifest einen expliziten [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) -Eintrag hinzu, beispielsweise: `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Anwendungsbereich des Pakets. appxmanifest-Designer](media/vs-manifest-application.png)  
    
    Sie können auch das `Display name` und `Description` nach Belieben ändern.  
1.  Speichern Sie diese Datei \ (oder ein anderes 512x512-Bild Ihrer Wahl) auf dem Desktop.  
    Klicken Sie dann im Manifest-Designer **Visual Assets** Panel auf die `Source` Schaltfläche Feld **...** , wählen Sie Sie als Quelldatei aus, und klicken Sie auf **generieren**.  \ (Klicken Sie dann auf **OK** , um die Standardplatzhalter-Bilder zu überschreiben \).  
    
    ![Bereich "visuelle Objekte" des Pakets. appxmanifest-Designer](media/vs-manifest-visual-assets.png)  
    
    Dadurch werden die grundlegenden visuellen Ressourcen zum Installieren, ausführen, starten und Verteilen Ihrer APP im Store generiert.  
    Wenn rote `X` Fehlermeldungen angezeigt werden, die auf fehlende Bilder hindeuten, können Sie auf die Schaltfläche.. **.** klicken, um eine Datei aus den generierten Bildern manuell auszuwählen.  
1.  Ersetzen Sie im Bereich Manifest-Designer- **Inhalts-URIs** `http://example.com` durch den Speicherort Ihrer PWA \ (so `Rule`  =  `include` und `WinRT Access`  =  `All` \).  
    Dadurch wird Ihre PWA-Berechtigung zum Senden systemeigener Windows-Runtime \ (WinRT \)-API-Anforderungen gewährt, wenn Sie als Windows 10-app ausgeführt wird, die ein wenig später abgedeckt wird.   Wenn für ihre eigentliche PWA kein WinRT-Zugriff erforderlich ist, können Sie den `WinRT Access` Wert auf ändern `None` .  Achten Sie auf jeden Fall darauf, die Standard `http://example.com` Zeichenfolge mit dem URI ihrer PWA zu unterteilen, oder die APP kann zur Laufzeit nicht ordnungsgemäß geladen werden.  
    Sie können Ihre PWA als Windows 10-app ausführen und Debuggen.  Wenn Sie eine localhost-Website verwenden, um diesen Leitfaden zu durchlaufen, stellen Sie sicher, dass Sie ausgeführt wird.  Dann  
1.  Erstellen Sie \ ( `Ctrl` + `Shift` + `F5` \), und führen `F5` Sie das PWA-Projekt aus.  Ihre Website sollte nun in einem eigenständigen App-Fenster gestartet werden.  Es handelt sich nicht nur um eine gehostete Web-App; Sie wird als Progressive Web-App auf Windows 10 ausgeführt.  

    ![PWA wird in einem WWAHost. exe-Fenster ausgeführt](media/wwahost.png)  

## Debuggen Ihrer PWA \ (EdgeHTML \) als Windows-App  

Da es sich bei einer PWA \ (EdgeHTML \) einfach um eine progressiv erweiterte gehostete Web-App handelt, können Sie Ihren serverseitigen Code wie jede andere Web-App mit der üblichen IDE und dem normalen Workflow Debuggen.  Die von Ihnen bereitgestellten Änderungen werden in Ihrer installierten PWA-Version wiedergegeben, wenn Sie Sie das nächste Mal starten \ (Sie müssen das universelle Windows-App-Paket nicht erneut bereitstellen).

Für das clientseitige Debuggen in Ihrer Windows 10-App müssen Sie über die `Microsoft Edge DevTools Preview` App verfügen.  Diese eigenständige App umfasst die gesamte Funktionalität des ursprünglichen in-Browser- [Microsoft Edge-devtools][DevToolsGuide] \ (einschließlich [PWA-Tools][DevToolsGuideServiceWorkers]\) sowie die grundlegende Unterstützung für [Remotedebuggen][DevToolsProtocol01ClientsEdgePreview] sowie eine [Debug-Zielauswahl][DevToolsGuideMicrosoftStoreApp] zum Anfügen an eine beliebige ausgeführte Instanz des EdgeHTML-Moduls, einschließlich Add-Ins für Office, Cortana, App-Webansichten und natürlich PWAs, die unter Windows ausgeführt werden.  

Hier erfahren Sie, wie Sie das Debuggen für Ihre PWA \ (EdgeHTML \) einrichten.  

1.  Installieren Sie die [Microsoft Edge devtools Preview][MicrosoftStoreEdgeDevtoolsPreview] -App aus dem Microsoft Store, wenn Sie Sie nicht bereits haben.  
1.  Starten Sie die devtools-APP, während ihre PWA-Website ausgeführt wird.  
1.  Starten Sie in Visual Studio Ihre Windows 10-App mit `Start Without Debugging` dem `Ctrl` + `F5` Befehl ().  \ (Die devtools-APP wird nicht ordnungsgemäß angefügt, wenn der Visual Studio-Debugger aktiv ist. \)  
1.  Klicken Sie in der devtools-app in der lokalen Debug-Zielauswahl auf die Schaltfläche **Aktualisieren** .  Ihre PWA \ (EdgeHTML \)-Website sollte nun aufgelistet sein.  \ (Wenn Sie auch in einem Browserfenster ausgeführt wird, handelt es sich um die letzte Instanz dieser Website in der Liste. \)  
1.  Klicken Sie auf Ihren PWA \ (EdgeHTML \)-Website Eintrag, um eine neue Registerkarte für devtools-Instanzen zu öffnen und das Debuggen zu starten.  
    
    ![Lokale Debug-Zielauswahl in der Microsoft Edge devtools-App](media/devtools-local.png)  
    
1.  Sie können überprüfen, ob devtools an Ihre PWA-running-as-Windows-App angefügt ist.  Geben Sie in der devtools- **Konsole**Folgendes ein:  
    
    ```shell
    window.Windows
    ```  
    
    Dadurch wird das globale `Windows Runtime` Objekt zurückgegeben, das alle [WinRT-Namespaces der obersten Ebene](#find-windows-runtime-winrt-apis)enthält.  Hierbei handelt es sich um Ihren PWA \ (EdgeHTML \)-Einstiegsbereich für die [universelle Windows-Plattform][WindowsUWPIndex], der nur für Web-Apps verfügbar gemacht wird, die als Windows 10-apps ausgeführt werden (die außerhalb des Browsers ausgeführt werden, in einem `WWAHost.exe` Prozess).  
    
## Suchen von Windows-Runtime \ (WinRT \)-APIs  

Als installierte Windows-App verfügt Ihre [PWA \ (EdgeHTML \) über vollen Zugriff auf systemeigene Windows-Runtime-APIs][WindowsRuntime]. Ermitteln Sie, was Sie verwenden müssen, rufen Sie die erforderlichen Berechtigungen ab, und verwenden Sie die Feature-Erkennung, um diese API-Anforderung in unterstützten Umgebungen zu senden.  Gehen Sie durch diesen Vorgang, um eine progressive Verbesserung für Windows-Desktopbenutzer ihrer PWA hinzuzufügen.  

Es gibt eine Reihe von Möglichkeiten, die universellen Windows-Plattform-APIs zu identifizieren, die Sie für Ihre Windows-PWA benötigen, einschließlich Durchsuchen der umfassenden [UWP-Dokumente auf Windows dev Center] [UWP/API/], herunterladen und Ausführen von [UWP-Codebeispielen](#uwp-code-samples) in Visual Studio und Durchsuchen von Codeausschnitten für allgemeine Aufgaben für PWAs unter Windows.

Es gibt eine Reihe von Möglichkeiten, die für Ihre Windows-PWA benötigten APIs für die universelle Windows-Plattform zu identifizieren, einschließlich Durchsuchen der umfassenden [UWP-Dokumente auf Windows dev Center] [UWP/API/], herunterladen und Ausführen von [UWP-Codebeispielen](#uwp-code-samples) in Visual Studio und Durchsuchen von Codeausschnitten für allgemeine Aufgaben für [PWAs unter Windows 10 (EdgeHTML)][PwaIndexWindows10].  

Insgesamt arbeiten WinRT-APIs in JavaScript auf die gleiche Weise wie in C#, daher können Sie die allgemeine [Dokumentation zur universellen Windows-Plattform][WindowsUWPIndex] und die [API-Referenz][UwpApiIndex] für die Verwendung befolgen.  Beachten Sie jedoch die folgenden Unterschiede:  

*   WinRT-Features in JavaScript verwenden [unterschiedliche Konventionen][ScriptingJsinrtUsingWinRTCasingConventions] für die Groß-/Kleinschreibung  
*   [Ereignisse werden als Zeichenfolgenbezeichner dargestellt][ScriptingJsinrtHandlingWinRTEvents] , die an Klassen `addEventListener` / `removeEventListener` Methoden übergeben werden.  
*   [Asynchrone Methoden][ScriptingJsinrtUsingWinRT] verwenden das JavaScript-Promise-Modell  
*   APIs im `Windows.UI.Xaml` Namespace werden für JavaScript-apps nicht unterstützt, die stattdessen den [EdgeHTML][DevGuideWhatsNew] Engine Web Rendering Stack \ (HTML, CSS \) verwenden.  

Weitere Informationen finden Sie unter [Verwenden der Windows-Runtime in JavaScript][WindowRuntimeUsingJavascript].  

### UWP-Codebeispiele  

Schauen Sie sich die [universelle Windows-Plattform \ (UWP \) Code Beispiele][MicrosoftDeveloperWindowsSamples] Repo an, um JavaScript-Beispiele für allgemeine Windows 10-App-Szenarien zu durchsuchen.  Obwohl die JS-Versionen dieser Beispiele die [WinJS][GithubWinjsWinjs] -Bibliothek verwenden, um die Beispielvorlage zu strukturieren, ist WinJS für das Senden der WinRT-API-Anforderungen, die in diesen Beispielen demonstriert werden, nicht erforderlich.  

> [!NOTE]
> Wenn Sie das [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] Ereignis für die APP Abhören müssen, können Sie dies mit der folgenden systemeigenen WinRT-API tun:  
> 
> **Verwenden Sie diese**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> ... im Gegensatz zu dieser Art von WinJS-Anforderung, die in den Beispielen verwendet wird:  
> 
> **Nicht so**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## Senden von WinRT-API-Anforderungen aus ihrer PWA (EdgeHTML)  

Nehmen Sie an diesem Punkt an, dass Sie ein benutzerdefiniertes Kontextmenü für Windows-Benutzer unserer PWA \ (EdgeHTML \) hinzufügen und die benötigten APIs im [Windows. UI. Popups][UwpApiWindowsUiPopups] -Namespace identifiziert haben möchten.  

Um alle WinRT-APIs-Anforderungen aus unserer PWA \ (EdgeHTML \) zu senden, müssen Sie zuerst [die erforderlichen Berechtigungen](#set-application-content-uri-rules-acurs) \ (oder Anwendungsinhalts-URI-Regeln \) in Ihrer Windows-App-Paketmanifest \ ( `.appxmanifest` \)-Datei erstellen.  

Wenn eine dieser API-Anforderungen den Zugriff auf Benutzer Ressourcen wie Bilder oder Musik oder auf Gerätefeatures wie die Kamera oder das Mikrofon beinhaltet, müssen Sie dem App-Paketmanifest auch [App-Funktionsdeklarationen](#app-capability-declarations) hinzufügen, damit Windows den Benutzer zur Genehmigung auffordert.  Wenn Sie später Ihre PWA \ (EdgeHTML \) im Microsoft Store veröffentlichen, werden diese erforderlichen [App-Berechtigungen][MicrosoftSupportWindowsAppPermissions] auch in Ihrem Store-Eintrag angegeben.  

#### Einrichten von Anwendungsinhalts-URI-Regeln (ACURs)  

Über ACURs (auch als URL-Zulassungsliste bezeichnet) können Sie die URLs Ihres PWA \ (EdgeHTML \) direkten Zugriffs auf Windows-Runtime-APIs angeben.  Auf der Windows-Betriebssystemebene sind die richtigen Richtlinien Grenzen so eingestellt, dass Code, der auf Ihrem Webserver gehostet wird, direkt Platt Form-API-Anforderungen senden kann.  Sie definieren diese Grenzen in der APP-Paket Manifestdatei, wenn Sie Ihre PWA-URLs als angeben `ApplicationContentUriRules` .  

Ihre Regeln sollten die Startseite für Ihre APP und alle anderen Seiten enthalten, die als App-Seiten enthalten sein sollen.  Wenn der Benutzer zu einer URL navigiert, die nicht in ihren Regeln enthalten ist, öffnet Windows die Ziel-URL im Microsoft Edge-Browser und nicht das eigenständige PWA \ (EdgeHTML \)-Fenster \ ( `WWAHost.exe` Prozess \).  Sie können auch bestimmte URLs ausschließen.  

Es gibt mehrere Möglichkeiten, eine URL `Match` in ihren Regeln anzugeben:  

*   Ein exakter Hostname  
*   Ein Hostname, für den ein URI mit einer Unterdomäne dieses Hostnamens einbezogen oder ausgeschlossen wird  
*   Ein exakter URI  
*   Ein exakter URI mit einer Abfrageeigenschaft  
*   Ein Teilpfad und ein Platzhalter für die Angabe einer bestimmten Dateierweiterung für eine Einbeziehungsregel  
*   Relative Pfade für Ausschlussregeln  

Hier sind einige Beispiele für ACURs in einer `.appxmanifest` Datei:  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

In der ACURs für Ihre APP definierte URLs können über das `WindowsRuntimeAccess` Attribut, das die folgenden Werte akzeptiert, die Berechtigung für die Windows-Runtime erhalten:  

*   `all`: Remote-JavaScript-Code hat Zugriff auf alle WinRT-APIs und alle lokalen Paketkomponenten.  Der [Windows \ (WinRT \))-][UwpApiIndex] Namespace wird injiziert und im Skriptmodul dargestellt.  
*   `allowForWeb`: Der Remote Zugriff auf JavaScript-Code ist auf lokale verpackte Komponenten, einschließlich benutzerdefinierter C++/c #-Komponenten, limitiert.  
*   `none`Standard.  Die angegebene URL hat keinen Plattformzugriff.  

In diesem Lernprogramm haben Sie bereits die einzige ACUR-Version festgesetzt, die Sie benötigen \ (Schritt 6 des vorherigen [Einrichten und Ausführen des App](#set-up-and-run-your-universal-windows-app) -Abschnitts \) für ihre Einzelseiten-app.  Sie können dies über den Bereich " **Inhalts-URIs** " des Visual Studio- `package.appxmanifest` Designers bestätigen.  

![Bereich ' Inhalts-URI ' im Visual Studio-appxmanifest-Designer](media/vs-appxmanifest-editor-acurs.png)  

Sie können auch den unformatierten XML-Code ihres Manifests anzeigen, indem Sie `package.appxmanifest` im Visual Studio-Projektmappen-Explorer mit der rechten Maustaste auf die Datei klicken und " **Code anzeigen** \ ( `F7` \)" auswählen.  Wenn Sie wieder zur Entwurfsansicht wechseln möchten, wählen Sie **Ansicht-Designer** \ ( `Shift` + `F7` \) aus.  

#### Deklarationen von App-Funktionen  

Wenn Ihre APP programmgesteuerten Zugriff auf Benutzer Ressourcen wie Bilder oder Musik oder auf Geräte wie eine Kamera oder ein Mikrofon benötigt, müssen Sie die entsprechenden [Deklarationen][WindowsUwpPackagingAppCapabilities] für die App-Funktion in Ihre APP-Paket Manifestdatei aufnehmen.  Es gibt drei Kategorien von App Funktionsdeklarationen:  

*   [Funktionen zur allgemeinen Verwendung][WindowsUwpPackagingAppCapabilitiesGeneralUse], die auf die meisten allgemeinen App-Szenarien zutreffen.  
*   [Gerätefunktionen][WindowsUwpPackagingAppCapabilitiesDevice], die Ihrer App den Zugriff auf Peripheriegeräte und interne Geräte ermöglichen.  
*   [Funktionen zur Sondernutzung][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] , die Unternehmensszenarien unterstützen und ein Microsoft Store-Unternehmenskonto erfordern.  Weitere Informationen zu Unternehmenskonten finden Sie unter [Kontotypen, Standorte und Gebühren][WindowsUwpPublishAccountTypesLocationsFees].

Auf der Microsoft Store-App-Seite werden alle Funktionen aufgeführt, die Sie in Ihrem App-Paketmanifest deklarieren, daher müssen Sie unbedingt nur die Funktionen angeben, die Ihre APP tatsächlich verwendet.

Einige Funktionen bieten apps Zugriff auf vertrauliche Ressourcen.  Diese Ressourcen gelten als vertraulich, weil jede Person auf die persönlichen Daten des Benutzers zugreifen oder dem Nutzer Geld kosten kann.  Mit den Datenschutzeinstellungen, die von der Windows 10- [Einstellungs][BingResultsWindows10Settings] -App verwaltet werden, können Benutzer den Zugriff auf vertrauliche Ressourcen dynamisch steuern.  Daher ist es wichtig, dass Ihre APP nicht davon ausgeht, dass eine vertrauliche Ressource immer verfügbar ist.  Weitere Informationen zum Zugriff auf sensible Ressourcen finden Sie unter [Richtlinien für Apps mit Berücksichtigung von Datenschutz][WindowsUwp|::ref2::|Index].  

Sie fordern Zugriff an, indem Sie Funktionen im Paketmanifest für Ihre APP deklarieren.  In Visual Studio können Sie dies über den Bereich " **Funktionen** " des Package. appxmanifest-Designers tun.  

![Bereich "Funktionen" im Visual Studio-appxmanifest-Designer](media/vs-appxmanifest-editor-capabilities.png)  

In diesem Lernprogramm ist nur die standardmäßige Internet-Funktion \ (Client \) erforderlich, daher ist keine weitere Aktion erforderlich.  

### Verwenden der Feature-Erkennung zum Aufrufen von WinRT  

Damit Sie für Ihre PWA-Zielgruppe auf allen Plattformen eine qualitativ hochwertige Baseline erzielen können, verbessern Sie mit der WinRT-Feature-Erkennung schrittweise ihre PWA-Funktionalität für Windows.  Auf diese Weise können Sie sicherstellen, dass Ihr Windows-spezifischer Code nur in einem Kontext ausgeführt wird, in dem WinRT-APIs verfügbar und anwendbar sind.  

Die Funktionserkennung kann so einfach sein wie die Suche nach dem `Windows` Objekt \ (dem EntryPoint zum [WinRT-Namespace][UwpApiIndex]\) wie unten:  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

Da jedoch nicht alle Windows-APIs für alle [Windows 10-Gerätetypen][UwpExtensionSdkDeviceFamiliesOverview]verfügbar sind, ist es im Allgemeinen nützlich, eine spezifischere Funktionserkennung zu verwenden, um den Namespace der API-Anforderung, die Sie senden, weiter zu qualifizieren:  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

Mit diesem Hintergrund können Sie einige WinRT-Code hinzufügen, um ein benutzerdefiniertes Kontextmenü zu implementieren.  Wenn Sie das Beispiel PWA aus [Erste Schritte mit Progressive Web Apps][PwaGetStarted]verwenden:

1.  Öffnen Sie Visual Studio für Ihr PWA-Websiteprojekt.

1.  Öffnen Sie im Projektmappen-Explorer die `views\layout.pug` Datei, und fügen Sie die folgende Zeile direkt unter dem `script` Verweis für Ihren Dienstmitarbeiter hinzu:
    
    ```xml
    script(src='/javascripts/site.js')
    ```  

1.  Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf den `javascripts` Ordner, und **fügen**Sie  >  **neue Datei hinzu.**

1.  Benennen Sie Ihre Datei: `site.js` , und kopieren Sie den folgenden Code:
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```

1.  Vergleichen Sie das Verhalten des Kontextmenüs, wenn Sie Ihre PWA im Browser ausführen \ ( `F5` aus dem PWA-Websiteprojekt \) versus im Windows-App-Fenster \ ( `F5` aus ihrem universellen Windows-App-Projekt \).  Klicken Sie im Browser mit der rechten Maustaste auf das Standardkontextmenü von Microsoft Edge, während während des `WWAHost.exe` Prozesses das benutzerdefinierte Menü nun angezeigt wird.  

    | Microsoft Edge | Windows 10-App |  
    |:--- |:---- |  
    | ![Browser-Standardkontextmenü](media/browser-context-menu.png) | ![Benutzerdefiniertes App-Kontextmenü](media/app-context-menu.png) |  

Wir hoffen, dass Sie jetzt ein solides Fundament haben, um Ihre PWAs unter Windows schrittweise zu verbessern.  Wenn Sie auf Fragen stoßen oder etwas unklar ist, senden Sie uns bitte einen Kommentar!  

## Vertiefung

Das [Windows dev Center][MicrosoftDeveloperWindowsApps] ist Ihre vollständige Referenz für alle Phasen des Windows-App-Aufbaus, von den [ersten Schritten][MicrosoftDeveloperWindowsAppsGetStarted]bis zum [entwerfen][MicrosoftDeveloperWindowsAppsDesign], [entwickeln][MicrosoftDeveloperWindowsAppsDevelop]und [veröffentlichen][MicrosoftDeveloperStorePublishApps] im Microsoft Store.  

Eine allgemeine Übersicht über die universelle Windows-Plattform \ (UWP \) und wie Sie auf unterschiedliche Windows 10-Gerätefamilien abzielen, finden Sie unter [Einführung in die universelle Windows-Plattform][WindowsUWPGetStartedGuide].  

Und wenn Sie fertig sind, gehen Sie wie folgt vor, um [Ihre PWA an den Microsoft Store](./microsoft-store.md)zu übermitteln.  

<!-- image links -->  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Erste Schritte mit Progressive Web-Apps"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs unter Windows 10 (EdgeHTML) – Progressive Web-Apps unter Windows"  
[DevToolsGuide]: ../devtools-guide.md "Microsoft Edge (EdgeHTML)-Entwickler Tools"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide.md#microsoft-store-app "Microsoft Store-App – Microsoft Edge (EdgeHTML)-Entwickler Tools"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Dienstmitarbeiter"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge devtools Preview – devtools-Protokoll Clients"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Neuerungen in EdgeHTML"  
[WindowsRuntime]: ../windows-runtime/index.md "Windows-Runtime (WinRT) für JavaScript"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Verwenden der Windows-Runtime in JavaScript"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Behandeln von Windows-Runtime-Ereignissen in JavaScript"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Verwenden von asynchronen Windows-Runtime-Methoden"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Konventionen für die Groß-/Kleinschreibung mit Windows-Runtime-Features – verwenden der Windows-Runtime in JavaScript"  
[UwpApiIndex]: /uwp/api/index "Windows UWP-Namespaces"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Windows. UI. Popups-Namespace"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "WebUIApplication. Activated-Ereignis"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Übersicht über Gerätefamilien"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "So generiert Visual Studio ein App-Paketmanifest"  
[WindowsUWPIndex]: /windows/uwp/index "Dokumentation zur universellen Windows-Plattform"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "Was ist eine APP für die universelle Windows-Plattform (UWP)?"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Aktivieren Ihres Geräts für die Entwicklung"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Sicherheits"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Kontotypen, Standorte und Gebühren"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Eingeschränkte Funktionen"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Gerätefunktionen"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Funktionen zur allgemeinen Nutzung"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "App-Funktionsdeklarationen"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "Windows 10-Einstellungen – Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "winjs/winjs | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Veröffentlichen von Windows-apps und-spielen"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Dokumentation zur universellen Windows-Plattform"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Entwerfen und Codieren von Windows-apps"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Entwickeln von UWP-apps"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Erste Schritte mit Windows 10-apps"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Code Beispiele"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge devtools Preview"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "App-Berechtigungen"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Downloads"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Visual Studio Preview"  
