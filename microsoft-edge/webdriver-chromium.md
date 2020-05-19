---
description: Erfahren Sie, wie Sie Ihre Website oder app in Microsoft Edge testen oder den Browser mit WebDriver automatisieren können.
title: WebDriver (Chrom)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/18/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, WebDriver, Selen, testen, Tools, Automatisierung, Test
ms.openlocfilehash: 810c45e1e8d7fb5a6dbefee1c4ae6eccbe573326
ms.sourcegitcommit: f5dc9d3f1e6629120e036c4298f66de636688cb7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "10659380"
---
# <span data-ttu-id="f307d-104">WebDriver (Chrom)</span><span class="sxs-lookup"><span data-stu-id="f307d-104">WebDriver (Chromium)</span></span>  

<span data-ttu-id="f307d-105">Bei der W3C- [WebDriver][W3CWebdriver] -API handelt es sich um eine Plattform-und sprachneutrale Schnittstelle und ein Draht Protokoll, mit der Programme oder Skripts das Verhalten eines Webbrowsers steuern können, beispielsweise Microsoft Edge \ (Chrom \).</span><span class="sxs-lookup"><span data-stu-id="f307d-105">The W3C [WebDriver][W3CWebdriver] API is a platform and language-neutral interface and wire protocol allowing programs or scripts to control the behavior of a web browser, like Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="f307d-106">WebDriver ermöglicht Entwicklern das Erstellen automatisierter Tests, die die Benutzerinteraktion simulieren.</span><span class="sxs-lookup"><span data-stu-id="f307d-106">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="f307d-107">WebDriver-Tests und-Simulationen unterscheiden sich von JavaScript-Komponententests, da WebDriver Zugriff auf Funktionen und Informationen hat, die JavaScript im Browser nicht ausführt, und WebDrive ist in der Lage, Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="f307d-107">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver has access to functionality and information that JavaScript running in the browser does not, and WebDrive is able to more accurately simulate user events or OS-level events.</span></span>  <span data-ttu-id="f307d-108">WebDriver kann Tests über mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung verwalten.</span><span class="sxs-lookup"><span data-stu-id="f307d-108">WebDriver is able to manage testing across multiple windows, tabs and webpages in a single test session.</span></span>  

<span data-ttu-id="f307d-109">Hier erfahren Sie, wie Sie mit WebDriver für Microsoft Edge \ (Chrom \) beginnen.</span><span class="sxs-lookup"><span data-stu-id="f307d-109">Here is how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="f307d-110">Installieren von Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="f307d-110">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="f307d-111">Wenn Sie dies noch nicht getan haben, [Installieren Sie Microsoft Edge (Chrom)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="f307d-111">If you have not already, [install Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="f307d-112">Wenn Sie eine vorinstallierte Version von Microsoft Edge auf Ihrem Computer verwenden, stellen Sie sicher, dass Sie über Microsoft Edge \ (Chrom \) und nicht über Microsoft Edge \ (EdgeHTML \) verfügen.</span><span class="sxs-lookup"><span data-stu-id="f307d-112">If you are using a pre-installed version of Microsoft Edge on your machine, verify that you have Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="f307d-113">Eine schnelle Möglichkeit zur Überprüfung besteht darin, `edge://settings/help` im Browser zu laden und zu bestätigen, dass die Versionsnummer V75 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="f307d-113">A quick way to check is to load `edge://settings/help` in the browser and confirm that the version number is v75 or later.</span></span>  

## <span data-ttu-id="f307d-114">Herunterladen von Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="f307d-114">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="f307d-115">Für WebDriver ist ein browserspezifischer Treiber erforderlich, um jeden Browser zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="f307d-115">WebDriver requires a browser-specific driver to automate each browser.</span></span>  <span data-ttu-id="f307d-116">Für Microsoft Edge \ (Chromium \) benötigt WebDriver den entsprechenden [Microsoft-Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver] für den Build von Microsoft Edge, den Sie testen oder automatisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f307d-116">For Microsoft Edge \(Chromium\), WebDriver requires the appropriate [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] for the build of Microsoft Edge you want to test or automate.</span></span>  

<span data-ttu-id="f307d-117">Führen Sie die folgenden Schritte aus, um die richtige Buildnummer zu finden.</span><span class="sxs-lookup"><span data-stu-id="f307d-117">To find your correct build number, use the following steps.</span></span>  

1.  <span data-ttu-id="f307d-118">Starten von Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f307d-118">Launch Microsoft Edge</span></span> 
1.  <span data-ttu-id="f307d-119">Zeigen Sie die Microsoft Edge \ (Chrom \)-Version an.</span><span class="sxs-lookup"><span data-stu-id="f307d-119">View the Microsoft Edge \(Chromium\) version.</span></span>  
    *   <span data-ttu-id="f307d-120">Navigieren Sie zu</span><span class="sxs-lookup"><span data-stu-id="f307d-120">Navigate to</span></span> `edge://settings/help`  
    *   <span data-ttu-id="f307d-121">Auswählen `...`  >  **Settings**  >   **von Einstellungen zu Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="f307d-121">Select `...` > **Settings** >  **About Microsoft Edge**</span></span>  
1.  <span data-ttu-id="f307d-122">Überprüfen Sie, ob die richtige Version von WebDriver für Ihren Build sicher ist, damit Sie ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f307d-122">Verify the correct version of WebDriver for your build ensures, so it runs correctly.</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020":::
   <span data-ttu-id="f307d-124">Abbildung1.</span><span class="sxs-lookup"><span data-stu-id="f307d-124">Figure 1.</span></span>  <span data-ttu-id="f307d-125">Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="f307d-125">The build number for Microsoft Edge Canary on January 14, 2020</span></span>  
:::image-end:::  

<span data-ttu-id="f307d-126">Laden Sie jetzt [die passende Version von Microsoft Edge Driver herunter][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="f307d-126">Now, [download the matching version of Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Der Abschnitt "Downloads" auf der Seite "Microsoft Edge-Treiber"":::
   <span data-ttu-id="f307d-128">Abbildung2.</span><span class="sxs-lookup"><span data-stu-id="f307d-128">Figure 2.</span></span>  <span data-ttu-id="f307d-129">Der Abschnitt "Downloads" auf der Seite " [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriverDownloads] "</span><span class="sxs-lookup"><span data-stu-id="f307d-129">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="f307d-130">Microsoft Edge \ (EdgeHTML \) funktioniert nicht mit dem [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="f307d-130">Microsoft Edge \(EdgeHTML\) does not work with [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="f307d-131">Zum Automatisieren von Microsoft Edge \ (EdgeHTML \) müssen Sie [Microsoft WebDriver für Microsoft Edge \ (EdgeHTML \)][Webdriver]herunterladen.</span><span class="sxs-lookup"><span data-stu-id="f307d-131">To automate Microsoft Edge \(EdgeHTML\), you must download [Microsoft WebDriver for Microsoft Edge \(EdgeHTML\)][Webdriver].</span></span>  

## <span data-ttu-id="f307d-132">Auswählen einer WebDriver-Sprachbindung</span><span class="sxs-lookup"><span data-stu-id="f307d-132">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="f307d-133">Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Clienttreiber.</span><span class="sxs-lookup"><span data-stu-id="f307d-133">The last component you must download is a language-specific client driver.</span></span>  <span data-ttu-id="f307d-134">Die Sprachbindung übersetzt den Code, den Sie in Python, Java, C \ #, Ruby und JavaScript schreiben, in Befehle, die der Microsoft Edge-Treiber, den Sie [im vorherigen Abschnitt heruntergeladen](#download-microsoft-edge-driver) haben, in Microsoft Edge \ (Chrom \) ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="f307d-134">The language binding translates the code you write in Python, Java, C\#, Ruby, and JavaScript into commands that the Microsoft Edge Driver you [downloaded in the previous section](#download-microsoft-edge-driver) is able to run in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="f307d-135">[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="f307d-135">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="f307d-136">Das Microsoft Edge-Team empfiehlt [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] oder höher, da es eine integrierte Unterstützung für Microsoft Edge \ (Chrom \) bietet.</span><span class="sxs-lookup"><span data-stu-id="f307d-136">The Microsoft Edge team highly recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, since it has built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="f307d-137">Sie können jedoch Microsoft Edge \ (Chrom \) in allen älteren Versionen von Selen, einschließlich der aktuellen stabilen Selenium 3-Version, Steuern.</span><span class="sxs-lookup"><span data-stu-id="f307d-137">However, you are able to drive Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f307d-138">Wenn Sie zuvor Microsoft Edge (Chrom \) mithilfe von und getestet haben `ChromeDriver` `ChromeOptions` , wird Ihr WebDriver-Code nicht erfolgreich mit Microsoft Edge V80 oder höher ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f307d-138">If you were previously automating or testing Microsoft Edge \(Chromium\) by using `ChromeDriver` and `ChromeOptions`, your WebDriver code does not run successfully against Microsoft Edge v80 or later.</span></span>  <span data-ttu-id="f307d-139">Hierbei handelt es sich um eine unterbrechende Änderung, und Microsoft Edge \ (Chrom \) akzeptiert die Befehle nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="f307d-139">This is a breaking change and Microsoft Edge \(Chromium\) no longer accepts the commands.</span></span>  <span data-ttu-id="f307d-140">Sie müssen Ihre Tests so ändern, dass Sie den `EdgeOptions` Kurs-und [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver]verwenden.</span><span class="sxs-lookup"><span data-stu-id="f307d-140">You must change your tests to use the `EdgeOptions` class and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="f307d-141">Verwenden von Selen 3</span><span class="sxs-lookup"><span data-stu-id="f307d-141">Using Selenium 3</span></span>  

<span data-ttu-id="f307d-142">[Selen 3][|::ref1::|] ist die neueste stabile Selen-Version.</span><span class="sxs-lookup"><span data-stu-id="f307d-142">[Selenium 3][|::ref1::|] is the latest stable Selenium release.</span></span>  <span data-ttu-id="f307d-143">Selen 3 steuert standardmäßig den alten Microsoft Edge \ (EdgeHTML \) und verfügt nicht über eine integrierte Unterstützung für Microsoft Edge \ (Chrom \).</span><span class="sxs-lookup"><span data-stu-id="f307d-143">By default, Selenium 3 drives the old Microsoft Edge \(EdgeHTML\), and does not have built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="f307d-144">Wenn Sie Selen 3 mit Microsoft Edge \ (Chrom \) verwenden möchten, installieren Sie das [Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket.</span><span class="sxs-lookup"><span data-stu-id="f307d-144">To use Selenium 3 with Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package.</span></span>  <span data-ttu-id="f307d-145">Die Selenium Tools für Microsoft Edge erweitern Selen 3 mit einem aktualisierten Treiber, damit Sie automatisierte Tests für die Microsoft Edge \ (EdgeHTML \) und die neuen Microsoft Edge \ (Chromium \)-Browser erstellen können.</span><span class="sxs-lookup"><span data-stu-id="f307d-145">The Selenium Tools for Microsoft Edge extend Selenium 3 with an updated driver to help you write automated tests for both the Microsoft Edge \(EdgeHTML\) and new Microsoft Edge \(Chromium\) browsers.</span></span>  

<span data-ttu-id="f307d-146">Selenium Tools für Microsoft Edge ist eine Lösung für Entwickler, die es vorziehen, auf Selen 3 und Entwickler zu bleiben, die über vorhandene Browser Tests verfügen und die Abdeckung für den neuen Microsoft Edge \ (Chromium \)-Browser hinzufügen möchten, ohne die Selen-Versionen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f307d-146">Selenium Tools for Microsoft Edge is a solution for developers who prefer to remain on Selenium 3 and developers who have existing browser tests and want to add coverage for the new Microsoft Edge \(Chromium\) browser without changing Selenium versions.</span></span>  <span data-ttu-id="f307d-147">Die `EdgeDriver` `EdgeDriverService` in den Tools enthaltenen und-Klassen sind vollständig mit den integrierten äquivalenten in Selen kompatibel und führen Microsoft Edge \ (EdgeHTML \) standardmäßig aus, damit die Tools als nahtloser Ersatz für die vorhandenen Edge-Klassen in Selen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f307d-147">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium, and run Microsoft Edge \(EdgeHTML\) by default so the tools may be used as a seamless drop-in replacement for the existing Edge classes in Selenium.</span></span>  

<span data-ttu-id="f307d-148">[Installieren Sie Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] , um mit Ihrem Selenium 3-Projekt Microsoft Edge zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f307d-148">[Install Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] to begin using Microsoft Edge \(Chromium\) with your Selenium 3 project.</span></span>  

## <span data-ttu-id="f307d-149">Verwenden von Microsoft Edge (Chrom) mit WebDriver</span><span class="sxs-lookup"><span data-stu-id="f307d-149">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="f307d-150">Die folgenden Beispiele können mit Selen 3 oder 4 ausführbar sein.</span><span class="sxs-lookup"><span data-stu-id="f307d-150">The following examples are runnable using either Selenium 3 or 4.</span></span>  <span data-ttu-id="f307d-151">Um mit Selen 3 zu verwenden, müssen die [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] installiert sein.</span><span class="sxs-lookup"><span data-stu-id="f307d-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] must be installed.</span></span>  

### <span data-ttu-id="f307d-152">Grundlegende Verwendung</span><span class="sxs-lookup"><span data-stu-id="f307d-152">Basic Usage</span></span>  

<span data-ttu-id="f307d-153">Um mit Microsoft Edge \ (EdgeHTML \) zu verwenden, erstellen Sie einfach eine Standardinstanz der `EdgeDriver` Klasse.</span><span class="sxs-lookup"><span data-stu-id="f307d-153">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="f307d-154">C#</span><span class="sxs-lookup"><span data-stu-id="f307d-154">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code" />  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="f307d-155">Python</span><span class="sxs-lookup"><span data-stu-id="f307d-155">Python</span></span>](#tab/python/)  

<a id="basic-usage-code" />  

```python
driver = Edge()
```  

* * *  

### <span data-ttu-id="f307d-156">Driving Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="f307d-156">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="f307d-157">Wenn Sie stattdessen mit Microsoft Edge \ (Chrom \) verwenden möchten, erstellen `EdgeDriver` Sie eine neue Klasse, und übergeben Sie Sie an das `EdgeOptions` Objekt, auf das die `UseChromium` Eigenschaft gesetzt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="f307d-157">To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="f307d-158">C#</span><span class="sxs-lookup"><span data-stu-id="f307d-158">C#</span></span>](#tab/c-sharp/)  

<a id="diving-microsoft-edge-chromium-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="f307d-159">Python</span><span class="sxs-lookup"><span data-stu-id="f307d-159">Python</span></span>](#tab/python/)  

<a id="diving-microsoft-edge-chromium-code" />  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

* * *  

### <span data-ttu-id="f307d-160">Auswählen bestimmter Browser-Binärdateien (nur Chrom)</span><span class="sxs-lookup"><span data-stu-id="f307d-160">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="f307d-161">Verwenden `EdgeOptions` Sie die Klasse, um eine bestimmte Binärdatei zu wählen.</span><span class="sxs-lookup"><span data-stu-id="f307d-161">Use the `EdgeOptions` class to choose a specific binary.</span></span>  <span data-ttu-id="f307d-162">Sie eignet sich zum Testen von [Microsoft Edge Preview-Kanälen][MicrosoftedgeinsiderDownload] wie Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="f307d-162">It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="f307d-163">C#</span><span class="sxs-lookup"><span data-stu-id="f307d-163">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="f307d-164">Python</span><span class="sxs-lookup"><span data-stu-id="f307d-164">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

* * *  

### <span data-ttu-id="f307d-165">Anpassen des Microsoft Edge-Treiber Diensts</span><span class="sxs-lookup"><span data-stu-id="f307d-165">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="f307d-166">C#</span><span class="sxs-lookup"><span data-stu-id="f307d-166">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

<span data-ttu-id="f307d-167">Wenn eine `EdgeDriver` Klasseninstanz mithilfe von Class erstellt wird `EdgeOptions` , wird automatisch die geeignete `EdgeDriverService` Klasse für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \) erstellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="f307d-167">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="f307d-168">Wenn Sie einen erstellen möchten `EdgeDriverService` , erstellen Sie einen für Microsoft Edge (Chrom \) konfigurierten unter Verwendung der `CreateChromiumService()` Methode.</span><span class="sxs-lookup"><span data-stu-id="f307d-168">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="f307d-169">Sie finden es möglicherweise hilfreich für zusätzliche Anpassungen wie das Aktivieren der ausführlichen Protokollausgabe im folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="f307d-169">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> <span data-ttu-id="f307d-170">Sie müssen das Objekt nicht angeben, `EdgeOptions` Wenn Sie die `EdgeDriver` Klasseninstanz `EdgeDriverService` .</span><span class="sxs-lookup"><span data-stu-id="f307d-170">You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.</span></span>  <span data-ttu-id="f307d-171">Die `EdgeDriver` Klasse verwendet die Standardoptionen für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \), je nachdem, welche Art von Dienst Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f307d-171">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.</span></span>  
> 
> <span data-ttu-id="f307d-172">Wenn Sie jedoch sowohl eine als auch eine Klasse bereitstellen möchten `EdgeDriverService` `EdgeOptions` , müssen Sie sicherstellen, dass beide für dieselbe Version von Microsoft Edge konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="f307d-172">However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="f307d-173">Es ist beispielsweise nicht möglich, eine standardmäßige Microsoft Edge \ (EdgeHTML \)- `EdgeDriverService` Klasse und Chrom-Eigenschaften in der Klasse zu verwenden `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="f307d-173">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="f307d-174">Die `EdgeDriver` Klasse löst einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f307d-174">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="f307d-175">Python</span><span class="sxs-lookup"><span data-stu-id="f307d-175">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

<span data-ttu-id="f307d-176">Bei Verwendung von Python `Edge` erstellt und verwaltet das Objekt die `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="f307d-176">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="f307d-177">Um das zu konfigurieren `EdgeService` , übergeben Sie zusätzliche Argumente an das `Edge` Objekt:</span><span class="sxs-lookup"><span data-stu-id="f307d-177">To configure the `EdgeService`, pass additional arguments to the `Edge` object:</span></span>

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

* * *  

### <span data-ttu-id="f307d-178">Verwenden von Chrom spezifischen Optionen</span><span class="sxs-lookup"><span data-stu-id="f307d-178">Using Chromium-Specific Options</span></span>  

<span data-ttu-id="f307d-179">Mithilfe der `EdgeOptions` Klasse mit dem `UseChromium` festgelegten Eigenschaften `true` Zugriff erhalten Sie Zugriff auf alle Methoden und Eigenschaften, die in der [chromeoptions][SeleniumWebDriverChromeoptionsClass] -Klasse in Selen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f307d-179">Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.</span></span>  <span data-ttu-id="f307d-180">Verwenden Sie beispielsweise wie bei anderen Chromium-Browsern die `EdgeOptions.AddArguments()` Methode zum Ausführen von Microsoft Edge \ (Chromium \) im [Headless-Modus][WikiHeadlessBrowser] im folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="f307d-180">For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.</span></span>  

#### [<span data-ttu-id="f307d-181">C#</span><span class="sxs-lookup"><span data-stu-id="f307d-181">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="f307d-182">Python</span><span class="sxs-lookup"><span data-stu-id="f307d-182">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

* * *  

> [!NOTE]
> <span data-ttu-id="f307d-183">Die [Chrom spezifischen Eigenschaften und Methoden][SeleniumWebDriverChromeoptionsClass] sind immer verfügbar, haben jedoch keine Auswirkungen, wenn die `UseChromium` Eigenschaft nicht auf gesetzt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="f307d-183">The [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.</span></span>  <span data-ttu-id="f307d-184">Ebenso haben vorhandene Eigenschaften und Methoden, die für Microsoft Edge \ (EdgeHTML \) vorgesehen sind, keine Auswirkungen, wenn `UseChromium` Property auf gesetzt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="f307d-184">Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.</span></span>  

## <span data-ttu-id="f307d-185">Weitere Möglichkeiten zum Einrichten von WebDriver</span><span class="sxs-lookup"><span data-stu-id="f307d-185">Other ways to set up WebDriver</span></span>  

### <span data-ttu-id="f307d-186">Schokoladig</span><span class="sxs-lookup"><span data-stu-id="f307d-186">Chocolatey</span></span>  

<span data-ttu-id="f307d-187">Wenn Sie [Chocolaty][Chocolatey] als Paket-Manager verwenden, installieren Sie den Microsoft Edge-Treiber, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="f307d-187">If you are using [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="f307d-188">Weitere Informationen finden Sie unter [Selen Chrom-Kanten Treiber auf Chocolaty][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="f307d-188">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="f307d-189">Docker</span><span class="sxs-lookup"><span data-stu-id="f307d-189">Docker</span></span>  

<span data-ttu-id="f307d-190">Wenn Sie [docker][DockerHub]verwenden, laden Sie ein vorkonfiguriertes Bild herunter, wobei Microsoft Edge \ (Chrom \) und [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] bereits installiert ist, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="f307d-190">If you are using [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] already installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="f307d-191">Weitere Informationen finden Sie unter [Container im docker-Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="f307d-191">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="f307d-192">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="f307d-192">Getting in touch with the Microsoft Edge DevTools team</span></span>    

<span data-ttu-id="f307d-193">Das Microsoft Edge-Team ist begierig, Ihr Feedback zur Verwendung von WebDriver, Selen und Microsoft Edge zu hören!</span><span class="sxs-lookup"><span data-stu-id="f307d-193">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge!</span></span>  <span data-ttu-id="f307d-194">Verwenden Sie das **Feedback** -Symbol in der Microsoft Edge devtools-oder Tweet- [@EdgeDevTools][TwitterTweetEdgeDevTools] , damit das Team weiß, was Sie denken.</span><span class="sxs-lookup"><span data-stu-id="f307d-194">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Das Feedback Symbol in der Microsoft Edge-devtools":::
   <span data-ttu-id="f307d-196">Das **Feedback** Symbol in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="f307d-196">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
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
