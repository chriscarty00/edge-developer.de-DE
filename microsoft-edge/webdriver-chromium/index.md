---
description: Erfahren Sie, wie Sie Ihre Website oder app in Microsoft Edge testen oder den Browser mit WebDriver automatisieren können.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler, WebDriver, Selen, testen, Tools, Automatisierung, Test
ms.openlocfilehash: 5e881eec59c966fd4fa6d35118032a3a51e7b9e5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231131"
---
# <span data-ttu-id="71110-104">Verwenden von WebDriver (Chrom) zur Testautomatisierung (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="71110-104">Use WebDriver (Chromium) for test automation overview</span></span>  

<span data-ttu-id="71110-105">Mit WebDriver können Sie (Entwickler \) automatisierte Tests erstellen, die die Benutzerinteraktion simulieren.</span><span class="sxs-lookup"><span data-stu-id="71110-105">WebDriver enables you \(developers\) to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="71110-106">WebDriver-Tests und-Simulationen unterscheiden sich von JavaScript-Komponententests aus folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="71110-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span>  

*   <span data-ttu-id="71110-107">Greift auf Funktionen und Informationen zu, die für JavaScript, das in Browsern ausgeführt wird, nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="71110-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="71110-108">Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene genauer.</span><span class="sxs-lookup"><span data-stu-id="71110-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="71110-109">Verwaltet mehrere Fenster, Registerkarten und Webseiten in einer einzelnen Testsitzung.</span><span class="sxs-lookup"><span data-stu-id="71110-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="71110-110">Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.</span><span class="sxs-lookup"><span data-stu-id="71110-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="71110-111">Im folgenden Abschnitt wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \ (Chrom \) beginnen.</span><span class="sxs-lookup"><span data-stu-id="71110-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="71110-112">Installieren von Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="71110-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="71110-113">Stellen Sie sicher, dass Sie [Microsoft Edge (Chrom)][MicrosoftEdge]installieren.</span><span class="sxs-lookup"><span data-stu-id="71110-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="71110-114">Um zu bestätigen, dass Sie Microsoft Edge \ (Chrom \) installiert haben, navigieren Sie zu `edge://settings/help` , und überprüfen Sie, ob die Versionsnummer Version 75 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="71110-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="71110-115">Herunterladen von Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="71110-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="71110-116">Führen Sie die folgenden Schritte aus, um mit der Automatisierung von Tests zu beginnen, um sicherzustellen, dass die von Ihnen installierte WebDriver-Version Ihrer Browserversion entspricht.</span><span class="sxs-lookup"><span data-stu-id="71110-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="71110-117">Navigieren Sie zu `edge://settings/help` , um die Version von Microsoft Edge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="71110-117">Navigate to `edge://settings/help` to get the version of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020":::
       <span data-ttu-id="71110-119">Die Buildnummer für Microsoft Edge Canary am 14. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="71110-119">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="71110-120">Navigieren Sie zur Seite [Microsoft Edge Driver Downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] , und laden Sie den Treiber herunter, der der Versionsnummer von Microsoft Edge entspricht.</span><span class="sxs-lookup"><span data-stu-id="71110-120">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="Der Abschnitt "Downloads" auf der Seite "Microsoft Edge-Treiber"":::
       <span data-ttu-id="71110-122">Der Abschnitt "Downloads" auf der Seite " [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver] "</span><span class="sxs-lookup"><span data-stu-id="71110-122">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## <span data-ttu-id="71110-123">Auswählen einer WebDriver-Sprachbindung</span><span class="sxs-lookup"><span data-stu-id="71110-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="71110-124">Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Clienttreiber zum Übersetzen des Codes \ (python, Java, C \ #, Ruby, JavaScript \) in Befehle, die der Microsoft Edge-Treiber in Microsoft Edge \ (Chrom \) ausführt.</span><span class="sxs-lookup"><span data-stu-id="71110-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="71110-125">[Laden Sie die WebDriver-Sprachbindung Ihrer Wahl herunter][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="71110-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="71110-126">Das Microsoft Edge-Team empfiehlt [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] oder höher, da es Microsoft Edge (Chrom \) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71110-126">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="71110-127">Sie können jedoch Microsoft Edge (Chrom \) in allen älteren Versionen von Selen steuern, einschließlich der aktuellen stabilen Selenium 3-Version.</span><span class="sxs-lookup"><span data-stu-id="71110-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="71110-128">Wenn Sie zuvor Microsoft Edge (Chrom \) mit und-Klassen automatisiert oder getestet `ChromeDriver` haben `ChromeOptions` , wird Ihr WebDriver-Code nicht unter Microsoft Edge, Version 80 oder höher, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71110-128">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="71110-129">Um dieses Problem zu beheben, aktualisieren Sie Ihre Tests, um die Klasse zu verwenden `EdgeOptions` und [Microsoft Edge-Treiber][MicrosoftDeveloperEdgeToolsWebdriver]zu installieren.</span><span class="sxs-lookup"><span data-stu-id="71110-129">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="71110-130">Verwenden von Selen 3</span><span class="sxs-lookup"><span data-stu-id="71110-130">Use Selenium 3</span></span>  

<span data-ttu-id="71110-131">Wenn Sie bereits [Selen 3][|::ref1::|]verwenden, verfügen Sie möglicherweise über vorhandene Browser Tests und möchten eine Abdeckung für Microsoft Edge \ (Chrom \) hinzufügen, ohne Ihre Version von Selen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="71110-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="71110-132">Wenn Sie [Selen 3][|::ref2::|] zum Schreiben automatisierter Tests für Microsoft Edge \ (EdgeHTML \) und Microsoft Edge \ (Chrom \) verwenden möchten, installieren Sie das [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket, um den aktualisierten Treiber zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="71110-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="71110-133">Die `EdgeDriver` `EdgeDriverService` in den Tools enthaltenen und-Klassen sind vollständig mit den integrierten äquivalenten in Selenium 4 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="71110-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="71110-134">Führen Sie die folgenden Schritte aus, um Ihrem Projekt die [Selenium-Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] und [Selen 3][|::ref3::|] hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="71110-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<span data-ttu-id="71110-135">C#</span><span class="sxs-lookup"><span data-stu-id="71110-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="71110-136">Fügen Sie die [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] -und [Selen. WebDriver][NugetPackagesSeleniumWebdriver31410] -Pakete mithilfe der [NuGet-CLI][NugetCLI] oder [Visual Studio][VisualStudio]zu Ihrem .net-Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="71110-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="71110-137">Python</span><span class="sxs-lookup"><span data-stu-id="71110-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="71110-138">Verwenden Sie [PIP][PythonPip] , um die [msedge-Selenium-Tools][PythonSeleniumTools] und [Selen][PythonSelenium] -Pakete zu installieren.</span><span class="sxs-lookup"><span data-stu-id="71110-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="71110-139">JavaScript</span><span class="sxs-lookup"><span data-stu-id="71110-139">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="71110-140">Verwenden Sie [NPM][JavaScript|::ref4::|] , um die [Edge-Selenium-Tools][JavaScriptSeleniumTools] und [Selen-WebDriver][JavaScriptSelenium] -Pakete zu installieren.</span><span class="sxs-lookup"><span data-stu-id="71110-140">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="71110-141">Verwenden von Microsoft Edge (Chrom) mit WebDriver</span><span class="sxs-lookup"><span data-stu-id="71110-141">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="71110-142">Sie können die folgenden Beispiele entweder mit Selen 3 oder 4 ausführen.</span><span class="sxs-lookup"><span data-stu-id="71110-142">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="71110-143">Um mit Selen 3 zu verwenden, muss das [Selen Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] -Paket installiert sein.</span><span class="sxs-lookup"><span data-stu-id="71110-143">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="71110-144">Grundlegende Verwendung</span><span class="sxs-lookup"><span data-stu-id="71110-144">Basic Usage</span></span>  

<span data-ttu-id="71110-145">Wenn Sie mit Microsoft Edge \ (EdgeHTML \) verwenden möchten, erstellen Sie eine Standardinstanz der `EdgeDriver` Klasse.</span><span class="sxs-lookup"><span data-stu-id="71110-145">To use with Microsoft Edge \(EdgeHTML\), create a default instance of the `EdgeDriver` class.</span></span>  

#### [<span data-ttu-id="71110-146">C#</span><span class="sxs-lookup"><span data-stu-id="71110-146">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="71110-147">Python</span><span class="sxs-lookup"><span data-stu-id="71110-147">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="71110-148">JavaScript</span><span class="sxs-lookup"><span data-stu-id="71110-148">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="71110-149">Driving Microsoft Edge (Chrom)</span><span class="sxs-lookup"><span data-stu-id="71110-149">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="71110-150">Wenn Sie mit Microsoft Edge \ (Chrom \) verwenden möchten, erstellen `EdgeDriver` Sie eine neue Klasse, und übergeben Sie Sie an das `EdgeOptions` Objekt, auf das die `UseChromium` Eigenschaft gesetzt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="71110-150">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="71110-151">C#</span><span class="sxs-lookup"><span data-stu-id="71110-151">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="71110-152">Python</span><span class="sxs-lookup"><span data-stu-id="71110-152">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="71110-153">JavaScript</span><span class="sxs-lookup"><span data-stu-id="71110-153">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="71110-154">Wenn Ihr IT-Administrator die [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] -Richtlinie auf festgesetzt hat `2` , ist [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] nicht in der Lage, [Microsoft Edge (Chrom)][MicrosoftEdge] zu steuern, da der Treiber die [Microsoft Edge-devtools][DevToolsMain]verwendet.</span><span class="sxs-lookup"><span data-stu-id="71110-154">If your IT admin has set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="71110-155">Stellen Sie sicher, dass die [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] -Richtlinie auf `0` oder `1` zum Automatisieren von [Microsoft Edge (Chrom)][MicrosoftEdge]eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="71110-155">Ensure the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="71110-156">Auswählen bestimmter Browser-Binärdateien (nur Chrom)</span><span class="sxs-lookup"><span data-stu-id="71110-156">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="71110-157">Sie können die `EdgeOptions` Klasse mit bestimmten Binärdateien von Microsoft Edge \ (Chrom \) verwenden.</span><span class="sxs-lookup"><span data-stu-id="71110-157">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="71110-158">So können Sie beispielsweise Tests mit den [Microsoft Edge Preview-Kanälen][MicrosoftedgeinsiderDownload] wie Microsoft Edge Beta ausführen.</span><span class="sxs-lookup"><span data-stu-id="71110-158">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="71110-159">C#</span><span class="sxs-lookup"><span data-stu-id="71110-159">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="71110-160">Python</span><span class="sxs-lookup"><span data-stu-id="71110-160">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="71110-161">JavaScript</span><span class="sxs-lookup"><span data-stu-id="71110-161">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="71110-162">Anpassen des Microsoft Edge-Treiber Diensts</span><span class="sxs-lookup"><span data-stu-id="71110-162">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="71110-163">C#</span><span class="sxs-lookup"><span data-stu-id="71110-163">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="71110-164">Wenn eine `EdgeDriver` Klasseninstanz mithilfe von Class erstellt wird `EdgeOptions` , wird die entsprechende `EdgeDriverService` Klasse für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \) erstellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="71110-164">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="71110-165">Wenn Sie einen erstellen möchten `EdgeDriverService` , erstellen Sie einen für Microsoft Edge (Chrom \) konfigurierten unter Verwendung der `CreateChromiumService()` Methode.</span><span class="sxs-lookup"><span data-stu-id="71110-165">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="71110-166">Sie finden es möglicherweise hilfreich für zusätzliche Anpassungen wie das Aktivieren der ausführlichen Protokollausgabe im folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="71110-166">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="71110-167">Sie müssen das Objekt nicht angeben `EdgeOptions` , wenn Sie `EdgeDriverService` an die Instanz übergeben werden `EdgeDriver` .</span><span class="sxs-lookup"><span data-stu-id="71110-167">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="71110-168">`EdgeDriver`Je nach dem von Ihnen bereitgestellten Dienst verwendet die Klasse die Standardoptionen für Microsoft Edge \ (EdgeHTML \) oder Microsoft Edge \ (Chrom \).</span><span class="sxs-lookup"><span data-stu-id="71110-168">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="71110-169">Wenn Sie jedoch beide und Klassen bereitstellen `EdgeDriverService` möchten `EdgeOptions` , stellen Sie sicher, dass beide für dieselbe Version von Microsoft Edge konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="71110-169">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="71110-170">Es ist beispielsweise nicht möglich, eine standardmäßige Microsoft Edge \ (EdgeHTML \)- `EdgeDriverService` Klasse und Chrom-Eigenschaften in der Klasse zu verwenden `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="71110-170">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="71110-171">Die `EdgeDriver` Klasse löst einen Fehler aus, um die Verwendung unterschiedlicher Versionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="71110-171">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="71110-172">Python</span><span class="sxs-lookup"><span data-stu-id="71110-172">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="71110-173">Bei Verwendung von Python `Edge` erstellt und verwaltet das Objekt die `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="71110-173">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="71110-174">Um das zu konfigurieren `EdgeService` , übergeben Sie zusätzliche Argumente an das `Edge` Objekt, wie im folgenden Code angegeben.</span><span class="sxs-lookup"><span data-stu-id="71110-174">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="71110-175">JavaScript</span><span class="sxs-lookup"><span data-stu-id="71110-175">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="71110-176">Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie a `Service` mit der `ServiceBuilder` Klasse.</span><span class="sxs-lookup"><span data-stu-id="71110-176">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="71110-177">Optional können Sie das `Service` Objekt an das Objekt übergeben `Driver` , das \ (und stoppt \) den Dienst für Sie startet.</span><span class="sxs-lookup"><span data-stu-id="71110-177">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="71110-178">Um das zu konfigurieren `Service` , führen Sie weitere Methoden in der Klasse aus, `ServiceBuilder` bevor Sie die `build()` Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="71110-178">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="71110-179">Übergeben Sie dann den `service` als Parameter in der `Driver.createSession()` Methode.</span><span class="sxs-lookup"><span data-stu-id="71110-179">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="71110-180">Verwenden von Chromium-Specific Optionen</span><span class="sxs-lookup"><span data-stu-id="71110-180">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="71110-181">Wenn Sie die `UseChromium` Eigenschaft auf festlegen `true` , können Sie die Klasse verwenden, `EdgeOptions` um auf die gleichen [Chrom spezifischen Eigenschaften und Methoden][SeleniumWebDriverChromeoptionsClass] zuzugreifen, wie bei der Automatisierung anderer Chrom-Browser.</span><span class="sxs-lookup"><span data-stu-id="71110-181">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="71110-182">C#</span><span class="sxs-lookup"><span data-stu-id="71110-182">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="71110-183">Python</span><span class="sxs-lookup"><span data-stu-id="71110-183">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="71110-184">JavaScript</span><span class="sxs-lookup"><span data-stu-id="71110-184">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  

> [!NOTE]
> <span data-ttu-id="71110-185">Wenn die `UseChromium` Eigenschaft auf eingestellt ist `true` , können Sie keine Eigenschaften und Methoden für Microsoft Edge \ (EdgeHTML \) verwenden.</span><span class="sxs-lookup"><span data-stu-id="71110-185">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="71110-186">Weitere Installationsoptionen für WebDriver</span><span class="sxs-lookup"><span data-stu-id="71110-186">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="71110-187">Schokoladig</span><span class="sxs-lookup"><span data-stu-id="71110-187">Chocolatey</span></span>  

<span data-ttu-id="71110-188">Wenn Sie [Chocolaty][Chocolatey] als Paket-Manager verwenden, installieren Sie den Microsoft Edge-Treiber, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="71110-188">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="71110-189">Weitere Informationen finden Sie unter [Selen Chrom-Kanten Treiber auf Chocolaty][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="71110-189">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="71110-190">Docker</span><span class="sxs-lookup"><span data-stu-id="71110-190">Docker</span></span>  

<span data-ttu-id="71110-191">Wenn Sie [docker][DockerHub]verwenden, laden Sie ein vorkonfiguriertes Bild mit Microsoft Edge \ (Chrom \) und [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] vorinstalliert herunter, indem Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="71110-191">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="71110-192">Weitere Informationen finden Sie unter [Container im docker-Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="71110-192">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="71110-193">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="71110-193">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="71110-194">Das Microsoft Edge-Team ist begierig, Ihr Feedback zur Verwendung von WebDriver, Selen und Microsoft Edge zu hören.</span><span class="sxs-lookup"><span data-stu-id="71110-194">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="71110-195">Um das Team zu informieren, was Sie denken, wählen Sie das Symbol **Feedback senden** in der Microsoft Edge-devtools aus, oder senden Sie eine Tweet- [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="71110-195">To let the team know what you think, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol „Feedback senden“ in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="71110-197">Das Symbol " **Feedback senden** " im Microsoft Edge-devtools</span><span class="sxs-lookup"><span data-stu-id="71110-197">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevToolsMain]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"
[Webdriver]: ../webdriver/index.md "WebDriver (EdgeHTML) | Microsoft docs"  

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

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

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
