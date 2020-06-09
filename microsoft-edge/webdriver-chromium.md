---
description: Erfahren Sie, wie Sie Ihre Website oder app in Microsoft Edge testen oder den Browser mit WebDriver automatisieren können.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, WebDriver, Selen, testen, Tools, Automatisierung, Test
ms.openlocfilehash: 14537943351db144bb4839d6befbfaa62894cd85
ms.sourcegitcommit: 3f8c8a5643e416b0851254833f9771192883ec45
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699507"
---
# <span data-ttu-id="c9811-104">Verwenden von WebDriver (Chrom) für die Testautomatisierung</span><span class="sxs-lookup"><span data-stu-id="c9811-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="c9811-105">WebDriver ermöglicht Entwicklern das Erstellen automatisierter Tests, die die Benutzerinteraktion simulieren.</span><span class="sxs-lookup"><span data-stu-id="c9811-105">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="c9811-106">WebDriver-Tests und-Simulationen unterscheiden sich von JavaScript-Komponententests aus folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="c9811-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span> 
*   <span data-ttu-id="c9811-107">Greift auf Funktionen und Informationen zu, die für JavaScript, das in Browsern ausgeführt wird, nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c9811-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="c9811-108">Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer.</span><span class="sxs-lookup"><span data-stu-id="c9811-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="c9811-109">Verwaltet Tests über mehrere Fenster, Registerkarten und Webseiten in einer einzelnen Testsitzung.</span><span class="sxs-lookup"><span data-stu-id="c9811-109">Manages testing across multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="c9811-110">Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.</span><span class="sxs-lookup"><span data-stu-id="c9811-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  

<span data-ttu-id="c9811-111">Im folgenden Abschnitt wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \ (Chrom \) beginnen.</span><span class="sxs-lookup"><span data-stu-id="c9811-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="c9811-112">Installieren von Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="c9811-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="c9811-113">Stellen Sie sicher, dass Sie [Microsoft Edge (Chrom)][MicrosoftEdge]installieren.</span><span class="sxs-lookup"><span data-stu-id="c9811-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="c9811-114">Um zu bestätigen, dass Sie Microsoft Edge (Chrom) installiert haben, wechseln Sie `edge://settings/help` im Browser zu, und überprüfen Sie, ob die Versionsnummer Version 75 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="c9811-114">To confirm that you have Microsoft Edge (Chromium) installed, go to `edge://settings/help` in the browser, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="c9811-115">Herunterladen von Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="c9811-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="c9811-116">Führen Sie die folgenden Schritte aus, um mit der Automatisierung von Tests zu beginnen, um sicherzustellen, dass die von Ihnen installierte WebDriver-Version Ihrer Browserversion entspricht.</span><span class="sxs-lookup"><span data-stu-id="c9811-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="c9811-117">Wechseln Sie zu `edge://settings/help` , um die Version von Edge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9811-117">Go to `edge://settings/help` to get the version of Edge.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020":::
       <span data-ttu-id="c9811-119">Abbildung1.</span><span class="sxs-lookup"><span data-stu-id="c9811-119">Figure 1.</span></span>  <span data-ttu-id="c9811-120">Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="c9811-120">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="c9811-121">Navigieren Sie zur Seite [Microsoft Edge Driver Downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] , und laden Sie den Treiber herunter, der der Edge-Versionsnummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="c9811-121">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the Edge version number.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Der Abschnitt "Downloads" auf der Seite "Microsoft Edge-Treiber"":::
       <span data-ttu-id="c9811-123">Abbildung2.</span><span class="sxs-lookup"><span data-stu-id="c9811-123">Figure 2.</span></span>  <span data-ttu-id="c9811-124">Der Abschnitt "Downloads" auf der Seite " [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver] "</span><span class="sxs-lookup"><span data-stu-id="c9811-124">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    > [!NOTE] 
    > <span data-ttu-id="c9811-125">Weitere Informationen zur Testautomatisierung mit Microsoft Edge (EdgeHTML) finden Sie unter [Microsoft WebDriver für Microsoft Edge (EdgeHTML)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="c9811-125">For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].</span></span>  

## <span data-ttu-id="c9811-126">Auswählen einer WebDriver-Sprachbindung</span><span class="sxs-lookup"><span data-stu-id="c9811-126">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="c9811-127">Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Clienttreiber zum Übersetzen des Codes \ (python, Java, C \ #, Ruby, JavaScript \) in Befehle, die der Microsoft Edge-Treiber in Microsoft Edge \ (Chrom \) ausführt.</span><span class="sxs-lookup"><span data-stu-id="c9811-127">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="c9811-128">[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="c9811-128">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="c9811-129">Das Microsoft Edge-Team empfiehlt [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] oder höher, da es Microsoft Edge (Chrom \) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9811-129">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c9811-130">Sie können jedoch Microsoft Edge (Chrom \) in allen älteren Versionen von Selen steuern, einschließlich der aktuellen stabilen Selenium 3-Version.</span><span class="sxs-lookup"><span data-stu-id="c9811-130">However, you are able to control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c9811-131">Wenn Sie zuvor Microsoft Edge (Chrom \) mit und-Klassen automatisiert oder getestet `ChromeDriver` haben `ChromeOptions` , wird Ihr WebDriver-Code nicht unter Microsoft Edge, Version 80 oder höher, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9811-131">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="c9811-132">Um dieses Problem zu beheben, aktualisieren Sie Ihre Tests, um die Klasse zu verwenden `EdgeOptions` und [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver]zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c9811-132">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="c9811-133">Verwenden von Selen 3</span><span class="sxs-lookup"><span data-stu-id="c9811-133">Use Selenium 3</span></span>  

<span data-ttu-id="c9811-134">Wenn Sie bereits [Selen 3][|::ref1::|]verwenden, verfügen Sie möglicherweise über vorhandene Browser Tests und möchten eine Abdeckung für Microsoft Edge \ (Chrom \) hinzufügen, ohne Ihre Version von Selen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c9811-134">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="c9811-135">Wenn Sie [Selen 3][|::ref2::|] zum Schreiben automatisierter Tests für Microsoft Edge \ (EdgeHTML \) und Microsoft Edge \ (Chrom \) verwenden möchten, installieren Sie das [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket, um den aktualisierten Treiber zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9811-135">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="c9811-136">Die `EdgeDriver` `EdgeDriverService` in den Tools enthaltenen und-Klassen sind vollständig mit den integrierten äquivalenten in Selenium 4 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c9811-136">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

## <span data-ttu-id="c9811-137">Verwenden von Microsoft Edge (Chrom) mit WebDriver</span><span class="sxs-lookup"><span data-stu-id="c9811-137">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="c9811-138">Sie können die folgenden Beispiele entweder mit Selen 3 oder 4 ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9811-138">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="c9811-139">Um mit Selen 3 zu verwenden, muss das [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket installiert sein.</span><span class="sxs-lookup"><span data-stu-id="c9811-139">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="c9811-140">Grundlegende Verwendung</span><span class="sxs-lookup"><span data-stu-id="c9811-140">Basic Usage</span></span>  

<span data-ttu-id="c9811-141">Um mit Microsoft Edge \ (EdgeHTML \) zu verwenden, erstellen Sie einfach eine Standardinstanz der `EdgeDriver` Klasse.</span><span class="sxs-lookup"><span data-stu-id="c9811-141">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="c9811-142">C#</span><span class="sxs-lookup"><span data-stu-id="c9811-142">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="c9811-143">Python</span><span class="sxs-lookup"><span data-stu-id="c9811-143">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="c9811-144">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9811-144">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="c9811-145">Driving Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="c9811-145">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="c9811-146">Wenn Sie mit Microsoft Edge \ (Chrom \) verwenden möchten, erstellen `EdgeDriver` Sie eine neue Klasse, und übergeben Sie Sie an das `EdgeOptions` Objekt, auf das die `UseChromium` Eigenschaft gesetzt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="c9811-146">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="c9811-147">C#</span><span class="sxs-lookup"><span data-stu-id="c9811-147">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="c9811-148">Python</span><span class="sxs-lookup"><span data-stu-id="c9811-148">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="c9811-149">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9811-149">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="c9811-150">Wenn die [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] -Richtlinie auf festgesetzt ist `2` , ist [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] nicht in der Lage, [Microsoft Edge (Chrom)][MicrosoftEdge] zu steuern, da der Treiber die [Microsoft Edge-devtools][DevToolsMain]verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9811-150">If the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="c9811-151">Stellen Sie sicher, dass Sie die [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] -Richtlinie auf `0` oder `1` zum Automatisieren von [Microsoft Edge (Chrom)][MicrosoftEdge]festlegen.</span><span class="sxs-lookup"><span data-stu-id="c9811-151">Ensure you set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="c9811-152">Auswählen bestimmter Browser-Binärdateien (nur Chrom)</span><span class="sxs-lookup"><span data-stu-id="c9811-152">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="c9811-153">Sie können die `EdgeOptions` Klasse mit bestimmten Binärdateien von Microsoft Edge (Chrom) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9811-153">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="c9811-154">So können Sie beispielsweise Tests mit den [Microsoft Edge Preview-Kanälen][MicrosoftedgeinsiderDownload] wie Microsoft Edge Beta ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9811-154">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="c9811-155">C#</span><span class="sxs-lookup"><span data-stu-id="c9811-155">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="c9811-156">Python</span><span class="sxs-lookup"><span data-stu-id="c9811-156">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="c9811-157">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9811-157">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="c9811-158">Anpassen des Microsoft Edge-Treiber Diensts</span><span class="sxs-lookup"><span data-stu-id="c9811-158">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="c9811-159">C#</span><span class="sxs-lookup"><span data-stu-id="c9811-159">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="c9811-160">Wenn eine `EdgeDriver` Klasseninstanz mithilfe von Class erstellt wird `EdgeOptions` , wird die entsprechende `EdgeDriverService` Klasse für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \) erstellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="c9811-160">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="c9811-161">Wenn Sie einen erstellen möchten `EdgeDriverService` , erstellen Sie einen für Microsoft Edge (Chrom \) konfigurierten unter Verwendung der `CreateChromiumService()` Methode.</span><span class="sxs-lookup"><span data-stu-id="c9811-161">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="c9811-162">Sie finden es möglicherweise hilfreich für zusätzliche Anpassungen wie das Aktivieren der ausführlichen Protokollausgabe im folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="c9811-162">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="c9811-163">Sie müssen das Objekt nicht angeben `EdgeOptions` , wenn Sie `EdgeDriverService` an die Instanz übergeben werden `EdgeDriver` .</span><span class="sxs-lookup"><span data-stu-id="c9811-163">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="c9811-164">`EdgeDriver`Je nach dem von Ihnen bereitgestellten Dienst verwendet die Klasse die Standardoptionen für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \).</span><span class="sxs-lookup"><span data-stu-id="c9811-164">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="c9811-165">Wenn Sie jedoch beide und Klassen bereitstellen `EdgeDriverService` möchten `EdgeOptions` , stellen Sie sicher, dass beide für dieselbe Version von Microsoft Edge konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="c9811-165">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="c9811-166">Es ist beispielsweise nicht möglich, eine standardmäßige Microsoft Edge (EdgeHTML)- `EdgeDriverService` Klasse und Chrom-Eigenschaften in der Klasse zu verwenden `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="c9811-166">For example, it is not possible to use a default Microsoft Edge (EdgeHTML) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="c9811-167">Die `EdgeDriver` Klasse löst einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c9811-167">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="c9811-168">Python</span><span class="sxs-lookup"><span data-stu-id="c9811-168">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="c9811-169">Bei Verwendung von Python `Edge` erstellt und verwaltet das Objekt die `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="c9811-169">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="c9811-170">Um das zu konfigurieren `EdgeService` , übergeben Sie zusätzliche Argumente an das `Edge` Objekt, wie im folgenden Code angegeben.</span><span class="sxs-lookup"><span data-stu-id="c9811-170">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="c9811-171">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9811-171">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="c9811-172">Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie a `Service` mit der `ServiceBuilder` Klasse.</span><span class="sxs-lookup"><span data-stu-id="c9811-172">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="c9811-173">Sie können das Objekt optional `Service` an das Objekt übergeben, das `Driver` den Dienst für Sie startet und beendet.</span><span class="sxs-lookup"><span data-stu-id="c9811-173">You may optionally pass the `Service` object to the `Driver` object which starts and stops the service for you.</span></span>  
<span data-ttu-id="c9811-174">Um das zu konfigurieren `Service` , führen Sie weitere Methoden in der Klasse aus, `ServiceBuilder` bevor Sie die `build()` Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9811-174">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="c9811-175">Übergeben Sie dann den `service` als Parameter in der `Driver.createSession()` Methode.</span><span class="sxs-lookup"><span data-stu-id="c9811-175">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * * 

### <span data-ttu-id="c9811-176">Verwenden von Chrom spezifischen Optionen</span><span class="sxs-lookup"><span data-stu-id="c9811-176">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="c9811-177">Wenn Sie die `UseChromium` Eigenschaft auf festlegen `true` , können Sie die Klasse verwenden, `EdgeOptions` um auf die gleichen [Chrom spezifischen Eigenschaften und Methoden][SeleniumWebDriverChromeoptionsClass] zuzugreifen, wie bei der Automatisierung anderer Chrom-Browser.</span><span class="sxs-lookup"><span data-stu-id="c9811-177">If you set the `UseChromium` property to `true`, you are able to use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="c9811-178">C#</span><span class="sxs-lookup"><span data-stu-id="c9811-178">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="c9811-179">Python</span><span class="sxs-lookup"><span data-stu-id="c9811-179">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="c9811-180">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c9811-180">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  
> [!NOTE]
> <span data-ttu-id="c9811-181">Wenn die `UseChromium` Eigenschaft auf eingestellt ist `true` , können Sie keine Eigenschaften und Methoden für Microsoft Edge \ (EdgeHTML \) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9811-181">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="c9811-182">Weitere Installationsoptionen für WebDriver</span><span class="sxs-lookup"><span data-stu-id="c9811-182">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="c9811-183">Schokoladig</span><span class="sxs-lookup"><span data-stu-id="c9811-183">Chocolatey</span></span>  

<span data-ttu-id="c9811-184">Wenn Sie [Chocolaty][Chocolatey] als Paket-Manager verwenden, installieren Sie den Microsoft Edge-Treiber, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9811-184">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="c9811-185">Weitere Informationen finden Sie unter [Selen Chrom-Kanten Treiber auf Chocolaty][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="c9811-185">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="c9811-186">Docker</span><span class="sxs-lookup"><span data-stu-id="c9811-186">Docker</span></span>  

<span data-ttu-id="c9811-187">Wenn Sie [docker][DockerHub]verwenden, laden Sie ein vorkonfiguriertes Bild mit Microsoft Edge \ (Chrom \) und [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] vorinstalliert herunter, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9811-187">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="c9811-188">Weitere Informationen finden Sie unter [Container im docker-Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="c9811-188">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="c9811-189">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="c9811-189">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="c9811-190">Das Microsoft Edge-Team ist begierig, Ihr Feedback zur Verwendung von WebDriver, Selen und Microsoft Edge zu hören.</span><span class="sxs-lookup"><span data-stu-id="c9811-190">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="c9811-191">Verwenden Sie das **Feedback** -Symbol in der Microsoft Edge devtools-oder Tweet- [@EdgeDevTools][TwitterTweetEdgeDevTools] , damit das Team weiß, was Sie denken.</span><span class="sxs-lookup"><span data-stu-id="c9811-191">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Das Feedback Symbol in der Microsoft Edge-devtools":::
   <span data-ttu-id="c9811-193">Das **Feedback** Symbol in der Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="c9811-193">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[DevToolsMain]: ./devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"
[Webdriver]: ./webdriver.md "WebDriver (EdgeHTML) | Microsoft docs"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability – Microsoft Edge – Richtlinien | Microsoft docs"  

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
