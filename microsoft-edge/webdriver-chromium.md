---
description: Erfahren Sie, wie Sie Ihre Website oder app in Microsoft Edge testen oder den Browser mit WebDriver automatisieren können.
title: WebDriver (Chrom)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, WebDriver, Selen, testen, Tools, Automatisierung, Test
ms.openlocfilehash: 1ce30ec13a4def2da67cffc80b0cc7c92845f22b
ms.sourcegitcommit: a78e285e8d0d9c570169b4e86bc4a2c2bb17871d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2020
ms.locfileid: "10668186"
---
# WebDriver (Chrom)  

Bei der W3C- [WebDriver][W3CWebdriver] -API handelt es sich um eine Plattform-und sprachneutrale Schnittstelle und ein Draht Protokoll, mit der Programme oder Skripts das Verhalten eines Webbrowsers steuern können, beispielsweise Microsoft Edge \ (Chrom \).  

WebDriver ermöglicht Entwicklern das Erstellen automatisierter Tests, die die Benutzerinteraktion simulieren.  WebDriver-Tests und-Simulationen unterscheiden sich von JavaScript-Komponententests, da WebDriver Zugriff auf Funktionen und Informationen hat, die JavaScript im Browser nicht ausführt, und WebDrive ist in der Lage, Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer zu simulieren.  WebDriver kann Tests über mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung verwalten.  

Hier erfahren Sie, wie Sie mit WebDriver für Microsoft Edge \ (Chrom \) beginnen.  

## Installieren von Microsoft Edge (Chrom)  

Wenn Sie dies noch nicht getan haben, [Installieren Sie Microsoft Edge (Chrom)][MicrosoftEdge].  Wenn Sie eine vorinstallierte Version von Microsoft Edge auf Ihrem Computer verwenden, stellen Sie sicher, dass Sie über Microsoft Edge \ (Chrom \) und nicht über Microsoft Edge \ (EdgeHTML \) verfügen.  Eine schnelle Möglichkeit zur Überprüfung besteht darin, `edge://settings/help` im Browser zu laden und zu bestätigen, dass die Versionsnummer V75 oder höher ist.  

## Herunterladen von Microsoft Edge Driver  

Für WebDriver ist ein browserspezifischer Treiber erforderlich, um jeden Browser zu automatisieren.  Für Microsoft Edge \ (Chromium \) benötigt WebDriver den entsprechenden [Microsoft-Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver] für den Build von Microsoft Edge, den Sie testen oder automatisieren möchten.  

Führen Sie die folgenden Schritte aus, um die richtige Buildnummer zu finden.  

1.  Starten von Microsoft Edge 
1.  Zeigen Sie die Microsoft Edge \ (Chrom \)-Version an.  
    *   Navigieren Sie zu `edge://settings/help`  
    *   Auswählen `...`  >  **Settings**  >   **von Einstellungen zu Microsoft Edge**  
1.  Überprüfen Sie, ob die richtige Version von WebDriver für Ihren Build sicher ist, damit Sie ordnungsgemäß ausgeführt wird.  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020":::
   Abbildung1.  Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020  
:::image-end:::  

Laden Sie jetzt [die passende Version von Microsoft Edge Driver herunter][MicrosoftDeveloperEdgeToolsWebdriverDownloads].  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Der Abschnitt "Downloads" auf der Seite "Microsoft Edge-Treiber"":::
   Abbildung2.  Der Abschnitt "Downloads" auf der Seite " [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriverDownloads] "  
:::image-end:::  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) funktioniert nicht mit dem [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriverDownloads].  Zum Automatisieren von Microsoft Edge \ (EdgeHTML \) müssen Sie [Microsoft WebDriver für Microsoft Edge \ (EdgeHTML \)][Webdriver]herunterladen.  

## Auswählen einer WebDriver-Sprachbindung  

Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Clienttreiber.  Die Sprachbindung übersetzt den Code, den Sie in Python, Java, C \ #, Ruby und JavaScript schreiben, in Befehle, die der Microsoft Edge-Treiber, den Sie [im vorherigen Abschnitt heruntergeladen](#download-microsoft-edge-driver) haben, in Microsoft Edge \ (Chrom \) ausführen kann.  

[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter][SeleniumDownloads].  Das Microsoft Edge-Team empfiehlt [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] oder höher, da es eine integrierte Unterstützung für Microsoft Edge \ (Chrom \) bietet.  Sie können jedoch Microsoft Edge \ (Chrom \) in allen älteren Versionen von Selen, einschließlich der aktuellen stabilen Selenium 3-Version, Steuern.  

> [!IMPORTANT]
> Wenn Sie zuvor Microsoft Edge (Chrom \) mithilfe von und getestet haben `ChromeDriver` `ChromeOptions` , wird Ihr WebDriver-Code nicht erfolgreich mit Microsoft Edge V80 oder höher ausgeführt.  Hierbei handelt es sich um eine unterbrechende Änderung, und Microsoft Edge \ (Chrom \) akzeptiert die Befehle nicht mehr.  Sie müssen Ihre Tests so ändern, dass Sie den `EdgeOptions` Kurs-und [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver]verwenden.  

### Verwenden von Selen 3  

[Selen 3][|::ref1::|] ist die neueste stabile Selen-Version.  Selen 3 steuert standardmäßig den alten Microsoft Edge \ (EdgeHTML \) und verfügt nicht über eine integrierte Unterstützung für Microsoft Edge \ (Chrom \).  Wenn Sie Selen 3 mit Microsoft Edge \ (Chrom \) verwenden möchten, installieren Sie das [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket.  Die Selenium Tools für Microsoft Edge erweitern Selen 3 mit einem aktualisierten Treiber, damit Sie automatisierte Tests für die Microsoft Edge \ (EdgeHTML \) und die neuen Microsoft Edge \ (Chromium \)-Browser erstellen können.  

Selenium Tools für Microsoft Edge ist eine Lösung für Entwickler, die es vorziehen, auf Selen 3 und Entwickler zu bleiben, die über vorhandene Browser Tests verfügen und die Abdeckung für den neuen Microsoft Edge \ (Chromium \)-Browser hinzufügen möchten, ohne die Selen-Versionen zu ändern.  Die `EdgeDriver` `EdgeDriverService` in den Tools enthaltenen und-Klassen sind vollständig mit den integrierten äquivalenten in Selen kompatibel und führen Microsoft Edge \ (EdgeHTML \) standardmäßig aus, damit die Tools als nahtloser Ersatz für die vorhandenen Edge-Klassen in Selen verwendet werden können.  

[Installieren Sie Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] , um mit Ihrem Selenium 3-Projekt Microsoft Edge zu verwenden.  

## Verwenden von Microsoft Edge (Chrom) mit WebDriver

Die folgenden Beispiele können mit Selen 3 oder 4 ausführbar sein.  Um mit Selen 3 zu verwenden, müssen die [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] installiert sein.  

### Grundlegende Verwendung  

Um mit Microsoft Edge \ (EdgeHTML \) zu verwenden, erstellen Sie einfach eine Standardinstanz der `EdgeDriver` Klasse.

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code" />  

```csharp
var driver = new EdgeDriver();
```  

#### [Python](#tab/python/)  

<a id="basic-usage-code" />  

```python
driver = Edge()
```  

#### [JavaScript](#tab/javascript/)  

<a id="basic-usage-code" />  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### Driving Microsoft Edge (Chrom)  

Wenn Sie stattdessen mit Microsoft Edge \ (Chrom \) verwenden möchten, erstellen `EdgeDriver` Sie eine neue Klasse, und übergeben Sie Sie an das `EdgeOptions` Objekt, auf das die `UseChromium` Eigenschaft gesetzt ist `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code" />  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code" />  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

### Auswählen bestimmter Browser-Binärdateien (nur Chrom)  

Verwenden `EdgeOptions` Sie die Klasse, um eine bestimmte Binärdatei zu wählen.  Sie eignet sich zum Testen von [Microsoft Edge Preview-Kanälen][MicrosoftedgeinsiderDownload] wie Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Anpassen des Microsoft Edge-Treiber Diensts  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

Wenn eine `EdgeDriver` Klasseninstanz mithilfe von Class erstellt wird `EdgeOptions` , wird automatisch die geeignete `EdgeDriverService` Klasse für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \) erstellt und gestartet.  

Wenn Sie einen erstellen möchten `EdgeDriverService` , erstellen Sie einen für Microsoft Edge (Chrom \) konfigurierten unter Verwendung der `CreateChromiumService()` Methode.  Sie finden es möglicherweise hilfreich für zusätzliche Anpassungen wie das Aktivieren der ausführlichen Protokollausgabe im folgenden Code.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> Sie müssen das Objekt nicht angeben, `EdgeOptions` Wenn Sie die `EdgeDriver` Klasseninstanz `EdgeDriverService` .  Die `EdgeDriver` Klasse verwendet die Standardoptionen für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \), je nachdem, welche Art von Dienst Sie bereitstellen.  
> 
> Wenn Sie jedoch sowohl eine als auch eine Klasse bereitstellen möchten `EdgeDriverService` `EdgeOptions` , müssen Sie sicherstellen, dass beide für dieselbe Version von Microsoft Edge konfiguriert sind.  Es ist beispielsweise nicht möglich, eine standardmäßige Microsoft Edge \ (EdgeHTML \)- `EdgeDriverService` Klasse und Chrom-Eigenschaften in der Klasse zu verwenden `EdgeOptions` .  Die `EdgeDriver` Klasse löst einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.  

#### [Python](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

Bei Verwendung von Python `Edge` erstellt und verwaltet das Objekt die `EdgeService` .  Um das zu konfigurieren `EdgeService` , übergeben Sie zusätzliche Argumente an das `Edge` Objekt:

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie a `Service` mit der `ServiceBuilder` Klasse.  Sie können das Objekt optional `Service` an das Objekt übergeben, das `Driver` den Dienst für Sie startet und beendet.  

Um das zu konfigurieren `Service` , führen Sie weitere Methoden in der Klasse aus, `ServiceBuilder` bevor Sie die Methode verwenden, `build()` und übergeben Sie dann den `service` als Parameter in der `Driver.createSession()` Methode.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Verwenden von Chrom spezifischen Optionen  

Mithilfe der `EdgeOptions` Klasse mit dem `UseChromium` festgelegten Eigenschaften `true` Zugriff erhalten Sie Zugriff auf alle Methoden und Eigenschaften, die in der [chromeoptions][SeleniumWebDriverChromeoptionsClass] -Klasse in Selen verfügbar sind.  Verwenden Sie beispielsweise wie bei anderen Chromium-Browsern die `EdgeOptions.AddArguments()` Methode zum Ausführen von Microsoft Edge \ (Chromium \) im [Headless-Modus][WikiHeadlessBrowser] im folgenden Code.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="using-chromium-specific-options-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [JavaScript](#tab/javascript/)  

<a id="using-chromium-specific-options-code" />  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```
* * *  

> [!NOTE]
> Die [Chrom spezifischen Eigenschaften und Methoden][SeleniumWebDriverChromeoptionsClass] sind immer verfügbar, haben jedoch keine Auswirkungen, wenn die `UseChromium` Eigenschaft nicht auf gesetzt ist `true` .  Ebenso haben vorhandene Eigenschaften und Methoden, die für Microsoft Edge \ (EdgeHTML \) vorgesehen sind, keine Auswirkungen, wenn `UseChromium` Property auf gesetzt ist `true` .  

## Weitere Möglichkeiten zum Einrichten von WebDriver  

### Schokoladig  

Wenn Sie [Chocolaty][Chocolatey] als Paket-Manager verwenden, installieren Sie den Microsoft Edge-Treiber, indem Sie den folgenden Befehl ausführen.  

```console
choco install selenium-chromium-edge-driver
```  

Weitere Informationen finden Sie unter [Selen Chrom-Kanten Treiber auf Chocolaty][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Wenn Sie [docker][DockerHub]verwenden, laden Sie ein vorkonfiguriertes Bild herunter, wobei Microsoft Edge \ (Chrom \) und [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] bereits installiert ist, indem Sie den folgenden Befehl ausführen.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Weitere Informationen finden Sie unter [Container im docker-Hub][DockerHubMsedgedriver].  

## Kontakt mit dem Microsoft Edge devtools-Team    

Das Microsoft Edge-Team ist begierig, Ihr Feedback zur Verwendung von WebDriver, Selen und Microsoft Edge zu hören!  Verwenden Sie das **Feedback** -Symbol in der Microsoft Edge devtools-oder Tweet- [@EdgeDevTools][TwitterTweetEdgeDevTools] , damit das Team weiß, was Sie denken.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Das Feedback Symbol in der Microsoft Edge-devtools":::
   Das **Feedback** Symbol in der Microsoft Edge-devtools  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[Webdriver]: ./webdriver.md "WebDriver (EdgeHTML) | Microsoft docs"  

[Chocolatey]: https://chocolatey.org "Chocolaty | Schokoladen Software"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selen Chrom-Kanten Treiber | Schokoladig"  

[DockerHub]: https://hub.docker.com "Docker-Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker-Hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selen | GitHub"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Microsoft-Entwickler"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Downloads-WebDriver | Microsoft-Entwickler"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Neuen Microsoft Edge-Browser herunterladen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | NuGet-Katalog"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selen. WebDriver 3.141.0 | NuGet-Katalog"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selen. WebDriver 4.0.0-alpha05 | NuGet-Katalog"  

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selen"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Chromeoptions-Klasse-WebDriver | Selen"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Einen Tweet Posten"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless-Browser | Wikipedia"  
