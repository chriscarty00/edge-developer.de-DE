---
description: Erfahren Sie, wie Sie Ihre Website oder App in Microsoft Edge testen oder den Browser mit WebDriver automatisieren.
title: Verwenden von WebDriver (Chromium) für die Testautomatisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, html, css, javascript, developer, webdriver, selenium, testing, tools, automation, test
ms.openlocfilehash: 87855fad02243a9d86053e43b5523013644f7e35
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398833"
---
# <a name="use-webdriver-chromium-for-test-automation"></a>Verwenden von WebDriver (Chromium) für die Testautomatisierung  

Mit WebDriver können Entwickler automatisierte Tests erstellen, die die Benutzerinteraktion simulieren.  WebDriver-Tests und -Simulationen unterscheiden sich auf folgende Weise von #A0 .  

*   Zugrifft auf Funktionen und Informationen, die für JavaScript, das in Browsern ausgeführt wird, nicht verfügbar sind.  
*   Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer.  
*   Verwaltet mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung.  
*   Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.  
    
Im folgenden Abschnitt wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \(Chromium\) beginnen.  

## <a name="install-microsoft-edge-chromium"></a>Installieren von Microsoft Edge (Chromium)  

Stellen Sie sicher, [dass Sie Microsoft Edge (Chromium) installieren.][MicrosoftEdge]  Um zu bestätigen, dass Microsoft Edge \(Chromium\) installiert ist, navigieren Sie zu , und überprüfen Sie, ob die Versionsnummer Version `edge://settings/help` 75 oder höher ist.  

## <a name="download-microsoft-edge-driver"></a>Microsoft Edge Driver herunterladen  

Um mit der Automatisierung von Tests zu beginnen, verwenden Sie die folgenden Schritte, um sicherzustellen, dass die von Ihnen installierte WebDriver-Version mit Ihrer Browserversion entspricht.  

1.  Navigieren Sie zum Anzeigen der Version von Microsoft Edge zu `edge://settings/help` .  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Die Buildnummer für Microsoft Edge Canary am 10. Februar 2021" lightbox="./media/microsoft-edge-version.msft.png":::
       Die Buildnummer für Microsoft Edge Canary am 10. Februar 2021  
    :::image-end:::  
    
1.  Navigieren Sie [zu Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver], unter dem Abschnitt **Downloads,** und laden Sie webDriver herunter, das der Versionsnummer von Microsoft Edge entspricht.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Der Abschnitt Downloads unter Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       Der **Abschnitt Downloads** unter Microsoft Edge [Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a>Auswählen einer WebDriver-Sprachbindung  

Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Clienttreiber, um Ihren Code \(Python, Java, C\#, Ruby, JavaScript\) in Befehle zu übersetzen, die der Microsoft #A0 in Microsoft Edge \(Chromium\) ausgeführt wird.  

[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter.][SeleniumDownloads]  Das Microsoft Edge-Team empfiehlt [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] oder höher, da es Microsoft Edge \(Chromium\) unterstützt.  Sie können Microsoft Edge \(Chromium\) jedoch in allen älteren Versionen von Selenium steuern, einschließlich der aktuellen stabilen Selenium 3-Version.  

> [!IMPORTANT]
> Wenn Sie zuvor Microsoft Edge \(Chromium\) mit und Klassen automatisiert oder getestet haben, wird Ihr `ChromeDriver` `ChromeOptions` WebDriver-Code nicht unter Microsoft Edge Version 80 oder höher ausgeführt.  Um das Problem zu beheben, aktualisieren Sie Ihre Tests so, dass sie die Klasse `EdgeOptions` verwenden, und laden [Sie Microsoft Edge Driver herunter.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  

### <a name="use-selenium-3"></a>Verwenden von Selenium 3  

Wenn Sie [Selenium 3][|::ref1::|]bereits verwenden, verfügen Sie möglicherweise über vorhandene Browsertests und möchten die Abdeckung für Microsoft Edge \(Chromium\) hinzufügen, ohne Ihre Version von Selenium zu ändern.  Um [Selenium 3][|::ref2::|] zum Schreiben automatisierter Tests für Microsoft Edge \(EdgeHTML\) und Microsoft Edge \(Chromium\) zu verwenden, installieren Sie das [Selenium Tools for Microsoft][GithubMicrosoftEdgeSeleniumTools] Edge-Paket, um den aktualisierten Treiber zu verwenden.  Die in den Tools enthaltenen Klassen und sind vollständig mit den integrierten `EdgeDriver` `EdgeDriverService` Entsprechungen in Selenium 4 kompatibel.  

Verwenden Sie die folgenden Schritte, um ihrem Projekt die [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] und [Selenium 3][|::ref3::|] hinzuzufügen.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Fügen Sie [die Pakete Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] und [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] zu Ihrem .NET-Projekt hinzu, indem Sie die [NuGet CLI][NugetCLI] oder [Visual Studio.][VisualStudio]  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Verwenden [Sie pip,][PythonPip] um [die msedge-selenium-tools][PythonSeleniumTools] und [selenium-Pakete][PythonSelenium] zu installieren.  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Wenn Ihr Java Maven verwendet, kopieren Und fügen Sie die folgende Abhängigkeit zu Ihrer Datei ein, um `pom.xml` [msedge-selenium-tools-java hinzuzufügen.][SonatypeMavenRepositorySearch]  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

Das Java-Paket steht auch direkt auf der Seite [Selenium Tools for Microsoft Edge Releases zum Download bereit.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Verwenden [Sie npm,][JavaScript|::ref4::|] um [die edge-selenium-tools][JavaScriptSeleniumTools] und [selenium-webdriver-Pakete zu][JavaScriptSelenium] installieren.  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a>Automatisieren von Microsoft Edge (Chromium) mit WebDriver  

Um einen Browser mithilfe von WebDriver zu automatisieren, müssen Sie zunächst eine WebDriver-Sitzung mit Ihrer bevorzugten WebDriver-Sprachbindung starten.  Eine Sitzung ist eine einzelne ausgeführte Instanz eines Browsers, die mithilfe von WebDriver-Befehlen gesteuert wird.  Starten Sie eine WebDriver-Sitzung, um eine neue Browserinstanz zu starten.  Die gestartete Browserinstanz bleibt geöffnet, bis Sie die WebDriver-Sitzung schließen.  

Der folgende Inhalt führt Sie durch die Verwendung von Selenium, um eine WebDriver-Sitzung mit Microsoft Edge \(Chromium\) zu starten.  Sie können die Beispiele entweder mit Selenium 3 oder 4 ausführen.  Für die Verwendung mit Selenium 3 muss das [Selenium Tools for Microsoft Edge-Paket][GithubMicrosoftEdgeSeleniumTools] installiert sein.  

### <a name="automate-microsoft-edge-chromium"></a>Automatisieren von Microsoft Edge (Chromium)  

Selenium verwendet die `EdgeDriver` Klasse, um eine Microsoft Edge \(Chromium\)-Sitzung zu verwalten.  Um eine Sitzung zu starten und Microsoft Edge \(Chromium\) zu automatisieren, erstellen Sie ein neues Objekt, und übergeben Sie es mit der auf `EdgeDriver` `EdgeOptions` `UseChromium` festgelegten Eigenschaft ein `true` Objekt.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

Die `EdgeDriver` Klasse unterstützt nur Microsoft Edge \(Chromium\), und Microsoft Edge \(EdgeHTML\) wird nicht unterstützt.  Für die grundlegende Verwendung können Sie eine erstellen, `EdgeDriver` ohne . `EdgeOptions`  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Wenn Ihr IT-Administrator die [DeveloperToolsAvailability-Richtlinie][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] auf festgelegt hat, wird Microsoft Edge Driver am Fahren von `2` Microsoft Edge \(Chromium\) blockiert, da der Treiber die [Microsoft Edge DevTools verwendet.][DevtoolsIndex] [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  Stellen Sie sicher, dass die [DeveloperToolsAvailability-Richtlinie][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] auf `0` Microsoft Edge (Chromium) festgelegt ist oder `1` diese automatisiert.  

### <a name="choose-specific-browser-binaries-chromium-only"></a>Auswählen bestimmter Browser-Binärdateien (nur Chromium)  

Sie können eine WebDriver-Sitzung mit bestimmten Microsoft Edge\(Chromium\)-Binärdateien starten.  Beispielsweise können Sie Tests mit den [Microsoft Edge-Vorschaukanälen wie][MicrosoftedgeinsiderDownload] Microsoft Edge Beta ausführen.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a>Anpassen des Microsoft Edge-Treiberdiensts  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Wenn Sie die Klasse zum Erstellen einer Klasseninstanz verwenden, erstellt und startet sie die entsprechende Klasse für `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) oder Microsoft Edge \(Chromium\).  

Wenn Sie einen erstellen möchten, verwenden Sie die -Methode, um eine für `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.  Die `CreateChromiumService()` Methode ist nützlich, wenn Sie Anpassungen hinzufügen müssen.  Der folgende Code startet beispielsweise die ausführliche Protokollausgabe.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Sie müssen das Objekt nicht bereitstellen, `EdgeOptions` wenn Sie an die Instanz `EdgeDriverService` `EdgeDriver` übergeben.  Die Klasse verwendet die Standardoptionen für `EdgeDriver` Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\) basierend auf dem von Ihnen angebotenen Dienst.  
> Wenn Sie jedoch sowohl als auch Klassen bereitstellen möchten, stellen Sie sicher, dass beide für die gleiche Version von `EdgeDriverService` `EdgeOptions` Microsoft Edge konfiguriert sind.  Sie können z. B. die Standardeigenschaften Microsoft Edge \(EdgeHTML\) und `EdgeDriverService` Chromium in der Klasse `EdgeOptions` verwenden.  Die `EdgeDriver` Klasse gibt einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Wenn Sie Python verwenden, erstellt und verwaltet `Edge` das Objekt das `EdgeService` .  Um das `EdgeService` zu konfigurieren, übergeben Sie zusätzliche Argumente an das `Edge` Objekt, wie im folgenden Code angegeben.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Verwenden Sie `createDefaultService()` die -Methode, um `EdgeDriverService` eine für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.  Verwenden Java Systemeigenschaften zum Anpassen von Treiberdiensten in Java.  Der folgende Code verwendet beispielsweise die Eigenschaft, um die ausführliche `"webdriver.edge.verboseLogging"` Protokollausgabe zu aktivieren.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie eine `Service` mit der `ServiceBuilder` Klasse.  Optional können Sie das Objekt an das Objekt übergeben, das `Service` `Driver` \(und beendet\) den Dienst für Sie startet.  
Führen Sie zum `Service` Konfigurieren der eine andere Methode in der Klasse `ServiceBuilder` aus, bevor Sie die Methode `build()` verwenden.  Übergeben Sie dann `service` den als -Parameter in der `Driver.createSession()` -Methode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a>Verwenden Chromium-Specific Optionen  

Wenn Sie die Eigenschaft auf festlegen, können Sie die Klasse verwenden, um auf dieselben Chromium-spezifischen Eigenschaften und Methoden zu zugreifen, die beim Automatisieren anderer `UseChromium` `true` `EdgeOptions` [Chromium-Browser][WebdriverCapabilitiesEdgeOptions] verwendet werden.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> Wenn die Eigenschaft auf festgelegt ist, können Sie keine Eigenschaften und Methoden für `UseChromium` `true` Microsoft Edge \(EdgeHTML\) verwenden.  

## <a name="other-webdriver-installation-options"></a>Andere WebDriver-Installationsoptionen  

### <a name="chocolatey"></a>Praline  

Wenn Sie [Schokoline][Chocolatey] als Paketmanager verwenden, führen Sie den folgenden Befehl aus, um den Microsoft Edge Driver zu installieren.  

```console
choco install selenium-chromium-edge-driver
```  

Weitere Informationen finden Sie unter [Selenium Chromium Edge Driver auf Schokoline][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### <a name="docker"></a>Docker  

Wenn Sie [Docker verwenden,][DockerHub]führen Sie den folgenden Befehl aus, um ein vorkonfiguriertes Image mit vorinstalliertem Microsoft Edge \(Chromium\) und [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunterzuladen.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Weitere Informationen finden Sie im [msedgedriver-Container auf Docker Hub][DockerHubMsedgedriver].  

## <a name="next-steps"></a>Nächste Schritte  

Weitere Informationen zu WebDriver und zum Schreiben automatisierter WebDriver-Tests mithilfe von Selenium finden Sie in der [Selenium-Dokumentation.][SeleniumDocumentation]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft #A0 ist gespannt auf Ihr Feedback zur Verwendung von WebDriver, Selenium und Microsoft Edge.  Um dem Team Ihre Fragen und **** Kommentare zu senden, wählen Sie das Symbol Feedback senden in den Microsoft Edge DevTools aus, oder senden Sie einen [Tweet @EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol „Feedback senden“ in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Das **Symbol Feedback senden** in den Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funktionen und EdgeOptions | Microsoft Docs"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability – Microsoft Edge – Richtlinien | Microsoft Docs"  

[Chocolatey]: https://chocolatey.org "Praline | Praline Software"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge Driver | Praline"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | NuGet Gallery"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Selenium.WebDriver 4.0.0-alpha07 | NuGet Gallery"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Das Selenium Browser Automation Project | Dokumentation für Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selenium"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Veröffentlichen eines Tweets"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Kopflose Browser-| Wikipedia"  
