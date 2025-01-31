---
description: Erfahren Sie, wie Sie Ihre Website oder App in Microsoft Edge testen oder den Browser mit WebDriver automatisieren
title: Verwenden von WebDriver (Chromium) für die Testautomatisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, Javascript, Entwickler, WebDriver, Selenium, Tests, Tools, Automatisierung, Test
ms.openlocfilehash: 5d30fe14051ac8857c6ea4d64b8c8f1f8e8049ac
ms.sourcegitcommit: a7609b75a94755ed983111af7083a0d3bf64eeac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583587"
---
# <a name="use-webdriver-chromium-for-test-automation"></a>Verwenden von WebDriver (Chromium) für die Testautomatisierung  

Mit WebDriver können Entwickler automatisierte Tests erstellen, welche die Benutzerinteraktion simulieren.  WebDriver-Tests und -Simulationen unterscheiden sich in folgenden Punkten von JavaScript-Komponententests.  

*   Greift auf Funktionen und Informationen zu, die JavaScript in Browsern nicht zur Verfügung stehen.  
*   Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer.  
*   Verwaltet mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung.  
*   Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.  
    
Im folgenden Abschnitt wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \(Chromium\) beginnen.  

## <a name="install-microsoft-edge-chromium"></a>Installieren von Microsoft Edge (Chromium)  

Stellen Sie sicher, dass Sie [Microsoft Edge (Chromium)][MicrosoftEdge].  Um zu bestätigen, dass Microsoft Edge \(Chromium\) installiert ist, navigieren Sie zu `edge://settings/help`, und überprüfen Sie, ob die Versionsnummer Version 75 oder höher ist.  

## <a name="download-microsoft-edge-driver"></a>Herunterladen des Microsoft Edge-Treibers  

Führen Sie die folgenden Schritte aus, um die Automatisierung von Tests zu starten und sicherzustellen, dass die von Ihnen installierte WebDriver-Version mit Ihrer Browserversion übereinstimmt.  

1.  Suchen Sie nach Ihrer Microsoft Edge.  
    1.  Navigieren Sie zu `edge://settings/help`.  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Die Buildnummer für Microsoft Edge 15. April 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           Die Buildnummer für Microsoft Edge 15. April 2021  
        :::image-end:::  
        
1.  Navigieren Sie zu [Microsoft Edge Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].  
1.  Navigieren Sie zu **Rufen Sie die neueste Version ab.**  
1.  Wählen Sie den Build des Kanals aus, der Ihrer Versionsnummer des Microsoft Edge.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Der Abschnitt Aktuelle Version auf der Webseite Microsoft Edge Treibers" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       Der **Abschnitt Aktuelle Version auf der** Webseite Microsoft Edge [Treibers][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a>Auswählen einer WebDriver-Sprachbindung  

Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Client-Treiber, um Ihren Code \(Python, Java, C\#, Ruby, JavaScript\) in Befehle zu übersetzen, die der Microsoft Edge-Treiber in Microsoft Edge \(Chromium\) ausführt.  

[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter][SeleniumDownloads].  Das Microsoft Edge empfiehlt [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] oder höher, da es Microsoft Edge \(Chromium\) unterstützt.  Sie können jedoch Microsoft Edge \(Chromium\) in allen älteren Versionen von Selenium steuern, einschließlich der aktuellen stabilen Selenium 3-Version.  

> [!IMPORTANT]
> Wenn Sie zuvor Microsoft Edge \(Chromium\) mit `ChromeDriver` und `ChromeOptions` Klassen automatisiert oder getestet haben, automatisiert oder getestet haben, wird Ihr WebDriver-Code nicht unter Microsoft Edge Version 80 oder höher ausgeführt.  Um das Problem zu beheben, aktualisieren Sie Ihre Tests, um die Klasse `EdgeOptions` verwenden, und laden Sie [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunter.  

### <a name="using-selenium-4"></a>Verwenden von Selenium 4

Selenium 4 bietet integrierte Unterstützung für Microsoft Edge (Chromium).  Navigieren Sie zum Installieren von Selenium 4 zu [Installieren von Seleniumbibliotheken][SeleniumInstallingLibraries].

Wenn Sie Selenium 4 verwenden, müssen Sie keine Selenium Tools für Microsoft Edge.  Selen tools for Microsoft Edge is for Selenium 3 only.  Wenn Sie versuchen, Selenium 4 mit Selenium Tools für Microsoft Edge zu verwenden und versuchen, eine neue Instanz zu erstellen, erhalten Sie den `EdgeDriver` folgenden Fehler: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .  

Wenn Sie Selenium 4 verwenden und diesen Fehler erhalten, entfernen Sie aus Ihrem Projekt, und stellen Sie sicher, dass Sie die offiziellen Und Klassen aus dem `Microsoft.Edge.SeleniumTools` `EdgeOptions` `EdgeDriver` `OpenQA.Selenium.Edge` Namespace verwenden.

### <a name="using-selenium-3"></a>Verwenden von Selenium 3  

Wenn Sie [Selenium 3][|::ref1::|]bereits verwenden, verfügen Sie möglicherweise über vorhandene Browsertests und möchten die Abdeckung für Microsoft Edge \(Chromium\) hinzufügen, ohne Ihre Selenium-Version zu ändern.  Um mit [Selenium 3][|::ref2::|] automatisierte Tests für Microsoft Edge \(EdgeHTML\) und Microsoft Edge \(Chromium\) zu schreiben, installieren Sie das Paket [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools], um den aktualisierten Treiber zu verwenden.  Die in den Tools enthaltenen Klassen `EdgeDriver` und `EdgeDriverService` sind vollständig mit den in Selenium 4 integrierten Äquivalenten kompatibel.  

Führen Sie die folgenden Schritte aus, um die [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] und [Selenium 3][|::ref3::|] zu Ihrem Projekt hinzuzufügen.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Fügen Sie die Pakete [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] und [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] mithilfe der [NuGet CLI][NugetCLI] oder [Visual Studio][VisualStudio] zu Ihrem .NET-Projekt hinzu.  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Verwenden Sie [pip][PythonPip], um die [msedge-selenium-tools][PythonSeleniumTools] und [selenium][PythonSelenium]-Pakete zu installieren.  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Wenn Ihr Java Maven verwendet, kopieren Sie die folgende Abhängigkeit und fügen Sie diese in Ihre Datei ein, um `pom.xml` [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] hinzuzufügen.  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

Das Java-Paket kann auch direkt auf der Seite [Selenium Tools für Microsoft Edge-Versionen][GithubMicrosoftEdgeSeleniumToolsReleases] heruntergeladen werden.  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Verwenden Sie [npm][JavaScript|::ref4::|], um die Pakete [edge-selenium-tools][JavaScriptSeleniumTools] und [selenium-webdriver][JavaScriptSelenium] zu installieren.  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a>Automatisieren von Microsoft Edge (Chromium) mit WebDriver  

Um einen Browser mit WebDriver zu automatisieren, müssen Sie zuerst eine WebDriver-Sitzung mit Ihrer bevorzugten WebDriver-Sprachbindung starten.  Eine Sitzung ist eine einzelne ausgeführte Instanz eines Browsers, die mithilfe von WebDriver-Befehlen gesteuert wird.  Starten Sie eine WebDriver-Sitzung, um eine neue Browserinstanz zu beginnen.  Die gestartete Browserinstanz bleibt geöffnet, bis Sie die WebDriver-Sitzung schließen.  

Der folgende Inhalt führt Sie durch die Verwendung von Selenium zum Starten einer WebDriver-Sitzung mit Microsoft Edge \(Chromium\).  Sie können die Beispiele entweder mit Selenium 3 oder 4 ausführen.  Zur Verwendung mit Selenium 3 muss das Paket [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] installiert sein.  

### <a name="automate-microsoft-edge-chromium"></a>Automatisieren von Microsoft Edge (Chromium)  

Selenium verwendet die Klasse `EdgeDriver`, zum Verwalten einer Microsoft Edge \(Chromium\)-Sitzung.  Um eine Sitzung zu starten und Microsoft Edge \(Chromium\) zu automatisieren, erstellen Sie ein neues `EdgeDriver` Objekt, und übergeben Sie es an ein `EdgeOptions` mit der festgelegten Eigenschaft `true`.  

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

Die Klasse `EdgeDriver` unterstützt nur Microsoft Edge \(Chromium\), Microsoft Edge \(EdgeHTML\) wird nicht unterstützt.  Für die grundlegende Verwendung können Sie eine erstellen, `EdgeDriver` ohne . `EdgeOptions`  

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
> Wenn Ihr IT-Administrator die [DeveloperToolsAvailability-Richtlinie][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] auf `2` festgelegt hat, kann der [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] Microsoft Edge \(Chromium\) nicht steuern, da der Treiber die [Microsoft Edge DevTools][DevtoolsIndex] verwendet.  Stellen Sie sicher, dass die [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]-Richtlinie auf `0` oder `1` festgelegt ist, um Microsoft Edge (Chromium) zu automatisieren.  

### <a name="choose-specific-browser-binaries-chromium-only"></a>Auswählen bestimmter Browser-Binärdateien (nur Chromium)  

Sie können eine #A0 mit bestimmten Microsoft Edge \(Chromium\) starten.  Sie können z. B. Tests mit den Microsoft Edge [wie z.][MicrosoftedgeinsiderDownload] B. Microsoft Edge Beta.  

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

Wenn Sie die `EdgeOptions` Klasse zum Erstellen einer `EdgeDriver` Klasseninstanz verwenden, wird die entsprechende `EdgeDriverService` Klasse entweder für Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\) erstellt und gestartet.  

Wenn Sie einen `EdgeDriverService` erstellen möchten, verwenden Sie die `CreateChromiumService()`-Methode, um eine für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.  Die `CreateChromiumService()` Methode ist nützlich, wenn Sie Anpassungen hinzufügen müssen.  Der folgende Code startet beispielsweise die ausführliche Protokollausgabe.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Sie müssen das `EdgeOptions` Objekt nicht bereitstellen, wenn Sie `EdgeDriverService` an die Instanz `EdgeDriver` übergeben.  Die `EdgeDriver` Klasse verwendet die Standardoptionen für Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\), basierend auf dem von Ihnen angebotenen Dienst.  
> Wenn Sie jedoch sowohl `EdgeDriverService` als auch `EdgeOptions` Klassen bereitstellen möchten, stellen Sie sicher, dass beide für die gleiche Version von Microsoft Edge konfiguriert sind.  Beispielsweise können Sie eine `EdgeDriverService` Standardklasse für Microsoft Edge \(EdgeHTML\) Chromium-Eigenschaften in der `EdgeOptions` Klasse verwenden.  Die `EdgeDriver` Klasse gibt einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Wenn Sie Python verwenden, erstellt und verwaltet das `Edge` Objekt das `EdgeService`.  Um das `EdgeService` zu konfigurieren, übergeben Sie zusätzliche Argumente an das `Edge` Objekt, wie im folgenden Code angegeben.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Verwenden Sie die `createDefaultService()` Methode, um eine `EdgeDriverService` für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.  Verwenden Sie die Java-Systemeigenschaften, um die Treiberdienste in Java anzupassen.  Der folgende Code verwendet beispielsweise die `"webdriver.edge.verboseLogging"` Eigenschaft, um die ausführliche Protokollausgabe zu aktivieren.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie eine `Service` mit der `ServiceBuilder` Klasse.  Optional können Sie das Objekt an das Objekt übergeben, das `Service` `Driver` \(und beendet\) den Dienst für Sie startet.  
Führen Sie zum Konfigurieren der `Service` eine andere Methode in der `ServiceBuilder` Klasse aus, bevor Sie die `build()` Methode verwenden.  Übergeben Sie dann `service` als Parameter in der `Driver.createSession()`-Methode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a>Verwenden von Chromium-spezifischer Optionen  

Wenn Sie die Eigenschaft auf festlegen, können Sie mit der Klasse auf die gleichen `UseChromium` `true` `EdgeOptions` [Chromium-spezifischen][WebdriverCapabilitiesEdgeOptions] Eigenschaften und Methoden zugreifen, die beim Automatisieren anderer Browser Chromium werden.  

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
> Wenn die `UseChromium` Eigenschaft auf `true` festgelegt ist, können Sie keine Eigenschaften und Methoden für Microsoft Edge \(EdgeHTML\) verwenden.  

## <a name="other-webdriver-installation-options"></a>Andere WebDriver-Installationsoptionen  

### <a name="docker"></a>Docker  

Wenn Sie [Docker][DockerHub] verwenden, führen Sie den folgenden Befehl aus, um ein vorkonfiguriertes Image mit vorinstalliertem Microsoft Edge \(Chromium\) und [Microsoft Edge-Treiber][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunterzuladen.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Weitere Informationen finden Sie im [msedgedriver-Container auf Docker Hub][DockerHubMsedgedriver].  

## <a name="next-steps"></a>Nächste Schritte  

Weitere Informationen zu WebDriver und zum Schreiben automatisierter WebDriver-Tests mithilfe von Selenium finden Sie in der [Selenium-Dokumentation.][SeleniumDocumentation]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge-Team freut sich über Ihr Feedback zur Verwendung von WebDriver, Selenium und Microsoft Edge.  Um dem Team Ihre Fragen und Kommentare zu senden, wählen Sie das Symbol **Feedback senden** in den Microsoft Edge DevTools aus, oder senden Sie einen Tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol Feedback senden in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Das Symbol **Feedback senden** in den Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funktionen und EdgeOptions | Microsoft Docs"  

<!--[Webdriver]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability – Microsoft Edge – Richtlinien | Microsoft Docs"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Microsoft Edge Treiber | Microsoft Edge Entwickler"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | NuGet Gallery"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver400beta02]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta2 "Selenium.WebDriver 4.0.0-beta2 | NuGet Gallery"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Das Selenium Browser Automation Project | Dokumentation für Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selenium"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Installieren von Seleniumbibliotheken | Selenium"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Veröffentlichen eines Tweets"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Monitorlose Browser-| Wikipedia"  
