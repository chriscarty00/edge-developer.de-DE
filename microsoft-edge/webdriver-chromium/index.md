---
description: Erfahren Sie, wie Sie Ihre Website oder app in Microsoft Edge testen oder den Browser mit WebDriver automatisieren können.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, WebDriver, Selen, testen, Tools, Automatisierung, Test
ms.openlocfilehash: 3c197a83dbf16c68102ff6e9a4ee6f33b0573af2
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192251"
---
# Verwenden von WebDriver (Chrom) für die Testautomatisierung  

Mit WebDriver können Sie (Entwickler \) automatisierte Tests erstellen, die die Benutzerinteraktion simulieren.  WebDriver-Tests und-Simulationen unterscheiden sich von JavaScript-Komponententests aus folgenden Gründen:  

*   Greift auf Funktionen und Informationen zu, die für JavaScript, das in Browsern ausgeführt wird, nicht verfügbar sind.  
*   Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer.  
*   Verwaltet mehrere Fenster, Registerkarten und Webseiten in einer einzelnen Testsitzung.  
*   Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.  
    
Im folgenden Abschnitt wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \ (Chrom \) beginnen.  

## Installieren von Microsoft Edge (Chrom)  

Stellen Sie sicher, dass Sie [Microsoft Edge (Chrom)][MicrosoftEdge]installieren.  Um zu bestätigen, dass Sie Microsoft Edge \ (Chrom \) installiert haben, navigieren Sie zu `edge://settings/help` , und überprüfen Sie, ob die Versionsnummer Version 75 oder höher ist.  

## Herunterladen von Microsoft Edge Driver  

Führen Sie die folgenden Schritte aus, um mit der Automatisierung von Tests zu beginnen, um sicherzustellen, dass die von Ihnen installierte WebDriver-Version Ihrer Browserversion entspricht.  

1.  Navigieren Sie zu `edge://settings/help` , um die Version von Microsoft Edge abzurufen.  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-version.png" alt-text="Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020" lightbox="../media/webdriver-chromium/edge-version.png":::
       Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020  
    :::image-end:::  
    
1.  Navigieren Sie zur Seite [Microsoft Edge Driver Downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] , und laden Sie den Treiber herunter, der der Versionsnummer von Microsoft Edge entspricht.  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-driver-install.png" alt-text="Der Abschnitt "Downloads" auf der Seite "Microsoft Edge-Treiber"" lightbox="../media/webdriver-chromium/edge-driver-install.png":::
       Der Abschnitt "Downloads" auf der Seite " [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver] "  
    :::image-end:::  
    
    > [!NOTE] 
    > Weitere Informationen zur Testautomatisierung mit Microsoft Edge \ (EdgeHTML \) finden Sie unter [Microsoft WebDriver für Microsoft Edge (EdgeHTML)][Webdriver].  
    
## Auswählen einer WebDriver-Sprachbindung  

Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Clienttreiber zum Übersetzen des Codes \ (python, Java, C \ #, Ruby, JavaScript \) in Befehle, die der Microsoft Edge-Treiber in Microsoft Edge \ (Chrom \) ausführt.  

[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter][SeleniumDownloads].  Das Microsoft Edge-Team empfiehlt [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] oder höher, da es Microsoft Edge (Chrom \) unterstützt.  Sie können jedoch Microsoft Edge (Chrom \) in allen älteren Versionen von Selen steuern, einschließlich der aktuellen stabilen Selenium 3-Version.  

> [!IMPORTANT]
> Wenn Sie zuvor Microsoft Edge (Chrom \) mit und-Klassen automatisiert oder getestet `ChromeDriver` haben `ChromeOptions` , wird Ihr WebDriver-Code nicht unter Microsoft Edge, Version 80 oder höher, ausgeführt.  Um dieses Problem zu beheben, aktualisieren Sie Ihre Tests, um die Klasse zu verwenden `EdgeOptions` und [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver]zu installieren.  

### Verwenden von Selen 3  

Wenn Sie bereits [Selen 3][|::ref1::|]verwenden, verfügen Sie möglicherweise über vorhandene Browser Tests und möchten eine Abdeckung für Microsoft Edge \ (Chrom \) hinzufügen, ohne Ihre Version von Selen zu ändern.  Wenn Sie [Selen 3][|::ref2::|] zum Schreiben automatisierter Tests für Microsoft Edge \ (EdgeHTML \) und Microsoft Edge \ (Chrom \) verwenden möchten, installieren Sie das [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket, um den aktualisierten Treiber zu verwenden.  Die `EdgeDriver` `EdgeDriverService` in den Tools enthaltenen und-Klassen sind vollständig mit den integrierten äquivalenten in Selenium 4 kompatibel.  

Führen Sie die folgenden Schritte aus, um Ihrem Projekt die [Selenium-Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] und [Selen 3][|::ref3::|] hinzuzufügen.

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Fügen Sie die [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] -und [Selen. WebDriver][NugetPackagesSeleniumWebdriver31410] -Pakete mithilfe der [NuGet-CLI][NugetCLI] oder [Visual Studio][VisualStudio]zu Ihrem .net-Projekt hinzu.  

#### [Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Verwenden Sie [PIP][PythonPip] , um die [msedge-Selenium-Tools][PythonSeleniumTools] und [Selen][PythonSelenium] -Pakete zu installieren.  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Verwenden Sie [NPM][JavaScript|::ref4::|] , um die [Edge-Selenium-Tools][JavaScriptSeleniumTools] und [Selen-WebDriver][JavaScriptSelenium] -Pakete zu installieren.  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Verwenden von Microsoft Edge (Chrom) mit WebDriver

Sie können die folgenden Beispiele entweder mit Selen 3 oder 4 ausführen.  Um mit Selen 3 zu verwenden, muss das [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket installiert sein.  

### Grundlegende Verwendung  

Wenn Sie mit Microsoft Edge \ (EdgeHTML \) verwenden möchten, erstellen Sie eine Standardinstanz der `EdgeDriver` Klasse.  

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [Python](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [JavaScript](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### Driving Microsoft Edge (Chrom)  

Wenn Sie mit Microsoft Edge \ (Chrom \) verwenden möchten, erstellen `EdgeDriver` Sie eine neue Klasse, und übergeben Sie Sie an das `EdgeOptions` Objekt, auf das die `UseChromium` Eigenschaft gesetzt ist `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Wenn Ihr IT-Administrator die [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] -Richtlinie auf festgesetzt hat `2` , ist [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] nicht in der Lage, [Microsoft Edge (Chrom)][MicrosoftEdge] zu steuern, da der Treiber die [Microsoft Edge-devtools][DevToolsMain]verwendet.  Stellen Sie sicher, dass die [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] -Richtlinie auf `0` oder `1` zum Automatisieren von [Microsoft Edge (Chrom)][MicrosoftEdge]eingestellt ist.  

### Auswählen bestimmter Browser-Binärdateien (nur Chrom)  

Sie können die `EdgeOptions` Klasse mit bestimmten Binärdateien von Microsoft Edge \ (Chrom \) verwenden.  So können Sie beispielsweise Tests mit den [Microsoft Edge Preview-Kanälen][MicrosoftedgeinsiderDownload] wie Microsoft Edge Beta ausführen.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Anpassen des Microsoft Edge-Treiber Diensts  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Wenn eine `EdgeDriver` Klasseninstanz mithilfe von Class erstellt wird `EdgeOptions` , wird die entsprechende `EdgeDriverService` Klasse für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \) erstellt und gestartet.  

Wenn Sie einen erstellen möchten `EdgeDriverService` , erstellen Sie einen für Microsoft Edge (Chrom \) konfigurierten unter Verwendung der `CreateChromiumService()` Methode.  Sie finden es möglicherweise hilfreich für zusätzliche Anpassungen wie das Aktivieren der ausführlichen Protokollausgabe im folgenden Code.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Sie müssen das Objekt nicht angeben `EdgeOptions` , wenn Sie `EdgeDriverService` an die Instanz übergeben werden `EdgeDriver` . `EdgeDriver`Je nach dem von Ihnen bereitgestellten Dienst verwendet die Klasse die Standardoptionen für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \).  
> Wenn Sie jedoch beide und Klassen bereitstellen `EdgeDriverService` möchten `EdgeOptions` , stellen Sie sicher, dass beide für dieselbe Version von Microsoft Edge konfiguriert sind.  Es ist beispielsweise nicht möglich, eine standardmäßige Microsoft Edge \ (EdgeHTML \)- `EdgeDriverService` Klasse und Chrom-Eigenschaften in der Klasse zu verwenden `EdgeOptions` .  Die `EdgeDriver` Klasse löst einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.  

#### [Python](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Bei Verwendung von Python `Edge` erstellt und verwaltet das Objekt die `EdgeService` .  Um das zu konfigurieren `EdgeService` , übergeben Sie zusätzliche Argumente an das `Edge` Objekt, wie im folgenden Code angegeben.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie a `Service` mit der `ServiceBuilder` Klasse.  Optional können Sie das `Service` Objekt an das Objekt übergeben `Driver` , das \ (und stoppt \) den Dienst für Sie startet.  
Um das zu konfigurieren `Service` , führen Sie weitere Methoden in der Klasse aus, `ServiceBuilder` bevor Sie die `build()` Methode verwenden.  Übergeben Sie dann den `service` als Parameter in der `Driver.createSession()` Methode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Verwenden von Chromium-Specific Optionen  

Wenn Sie die `UseChromium` Eigenschaft auf festlegen `true` , können Sie die Klasse verwenden, `EdgeOptions` um auf die gleichen [Chrom spezifischen Eigenschaften und Methoden][SeleniumWebDriverChromeoptionsClass] zuzugreifen, wie bei der Automatisierung anderer Chrom-Browser.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [JavaScript](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  

> [!NOTE]
> Wenn die `UseChromium` Eigenschaft auf eingestellt ist `true` , können Sie keine Eigenschaften und Methoden für Microsoft Edge \ (EdgeHTML \) verwenden.  

## Weitere Installationsoptionen für WebDriver  

### Schokoladig  

Wenn Sie [Chocolaty][Chocolatey] als Paket-Manager verwenden, installieren Sie den Microsoft Edge-Treiber, indem Sie den folgenden Befehl ausführen.  

```console
choco install selenium-chromium-edge-driver
```  

Weitere Informationen finden Sie unter [Selen Chrom-Kanten Treiber auf Chocolaty][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Wenn Sie [docker][DockerHub]verwenden, laden Sie ein vorkonfiguriertes Bild mit Microsoft Edge \ (Chrom \) und [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] vorinstalliert herunter, indem Sie den folgenden Befehl ausführen.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Weitere Informationen finden Sie unter [Container im docker-Hub][DockerHubMsedgedriver].  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

Das Microsoft Edge-Team ist begierig, Ihr Feedback zur Verwendung von WebDriver, Selen und Microsoft Edge zu hören.  Um das Team zu informieren, was Sie denken, wählen Sie das Symbol **Feedback senden** in der Microsoft Edge-devtools aus, oder senden Sie eine Tweet- [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol "Feedback senden" im Microsoft Edge-devtools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Das Symbol " **Feedback senden** " im Microsoft Edge-devtools  
:::image-end:::  

<!-- links -->  

[DevToolsMain]: ../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"
[Webdriver]: ../webdriver.md "WebDriver (EdgeHTML) | Microsoft docs"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability – Microsoft Edge – Richtlinien | Microsoft docs"  

[Chocolatey]: https://chocolatey.org "Chocolaty | Schokoladen Software"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selen Chrom-Kanten Treiber | Schokoladig"  

[DockerHub]: https://hub.docker.com "Docker-Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker-Hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selen | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "NPM"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@Microsoft/Edge-Selenium-Tools | NPM"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "Selen-WebDriver | NPM"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Microsoft-Entwickler"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Downloads-WebDriver | Microsoft-Entwickler"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | NuGet-Katalog"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | NuGet-Katalog"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selen. WebDriver 3.141.0 | NuGet-Katalog"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selen. WebDriver 4.0.0-alpha05 | NuGet-Katalog"  

[PythonPip]: https://pypi.org/project/pip/ "PIP | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-Selenium-Tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "Selen | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selen"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Chromeoptions-Klasse-WebDriver | Selen"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Einen Tweet Posten"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless-Browser | Wikipedia"  
