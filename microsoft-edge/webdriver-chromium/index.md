---
description: Erfahren Sie, wie Sie Ihre Website oder App in Microsoft Edge testen oder den Browser mit WebDriver automatisieren.
title: Verwenden von WebDriver (Chromium) für die Testautomatisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, HTML, CSS, Javascript, Entwickler, Webdriver, Selenium, Testen, Tools, Automatisierung, Test
ms.openlocfilehash: b3b8a4ef2174c7f313fe9ee71bedbdf5e2f9b771
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343792"
---
# <span data-ttu-id="4b693-104">Verwenden von WebDriver (Chromium) für die Testautomatisierung</span><span class="sxs-lookup"><span data-stu-id="4b693-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="4b693-105">WebDriver ermöglicht Es Entwicklern, automatisierte Tests zu erstellen, die die Benutzerinteraktion simulieren.</span><span class="sxs-lookup"><span data-stu-id="4b693-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="4b693-106">#A0 und -Simulationen unterscheiden sich von #A1 auf folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="4b693-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="4b693-107">Accesses functionality and information not available to JavaScript running in browsers.</span><span class="sxs-lookup"><span data-stu-id="4b693-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="4b693-108">Simuliert Benutzerereignisse oder Ereignisse auf Betriebssystemebene präziser.</span><span class="sxs-lookup"><span data-stu-id="4b693-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="4b693-109">Verwaltet mehrere Fenster, Registerkarten und Webseiten in einer einzigen Testsitzung.</span><span class="sxs-lookup"><span data-stu-id="4b693-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="4b693-110">Führt mehrere Sitzungen von Microsoft Edge auf einem bestimmten Computer aus.</span><span class="sxs-lookup"><span data-stu-id="4b693-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="4b693-111">Im folgenden Abschnitt wird beschrieben, wie Sie mit WebDriver für Microsoft Edge \(Chromium\) beginnen.</span><span class="sxs-lookup"><span data-stu-id="4b693-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="4b693-112">Installieren von Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="4b693-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="4b693-113">Stellen Sie sicher, dass [Sie Microsoft Edge (Chromium) installieren.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="4b693-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="4b693-114">Um zu bestätigen, dass Sie Microsoft Edge \(Chromium\) installiert haben, navigieren Sie zu , und stellen Sie sicher, dass die Versionsnummer Version `edge://settings/help` 75 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="4b693-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <span data-ttu-id="4b693-115">Microsoft Edge Driver herunterladen</span><span class="sxs-lookup"><span data-stu-id="4b693-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="4b693-116">Um mit der Automatisierung von Tests zu beginnen, müssen Sie mit den folgenden Schritten sicherstellen, dass die installierte #A0 mit Ihrer Browserversion entspricht.</span><span class="sxs-lookup"><span data-stu-id="4b693-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="4b693-117">Zum Anzeigen der Version von Microsoft Edge navigieren Sie zu `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="4b693-117">To display the version of Microsoft Edge, navigate to `edge://settings/help`.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Die Buildnummer für Microsoft Edge Canary am 10. Februar 2021" lightbox="./media/microsoft-edge-version.msft.png":::
       <span data-ttu-id="4b693-119">Die Buildnummer für Microsoft Edge Canary am 10. Februar 2021</span><span class="sxs-lookup"><span data-stu-id="4b693-119">The build number for Microsoft Edge Canary on February 10, 2021</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4b693-120">Navigieren Sie im Abschnitt \*\*\*\* ["Downloads"][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]zu Microsoft Edge Driver, und laden Sie webDriver herunter, das der Versionsnummer von Microsoft Edge entspricht.</span><span class="sxs-lookup"><span data-stu-id="4b693-120">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver], under the **Downloads** section, and download the WebDriver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Der Abschnitt "Downloads" auf dem Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="4b693-122">Der **Abschnitt "Downloads"** auf [dem Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="4b693-122">The **Downloads** section on [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  

## <span data-ttu-id="4b693-123">Auswählen einer #A0</span><span class="sxs-lookup"><span data-stu-id="4b693-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="4b693-124">Die letzte Komponente, die Sie herunterladen müssen, ist ein sprachspezifischer Clienttreiber, der Ihren Code \(Python, Java, C\#, Ruby, JavaScript\) in Befehle übersetzt, die der Microsoft #A0 in Microsoft Edge \(Chromium\) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b693-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="4b693-125">[Laden Sie die #A0 Ihrer Wahl herunter.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="4b693-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="4b693-126">Das Microsoft Edge Team empfiehlt [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] oder höher, da es Microsoft Edge \(Chromium\) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b693-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4b693-127">Sie können Microsoft Edge \(Chromium\) jedoch in allen älteren Versionen von Selenium steuern, einschließlich der aktuellen stabilen Selenium 3-Version.</span><span class="sxs-lookup"><span data-stu-id="4b693-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="4b693-128">Wenn Sie zuvor Microsoft Edge \(Chromium\) mit und Klassen automatisiert oder getestet haben, wird Ihr #A0 nicht unter `ChromeDriver` `ChromeOptions` Microsoft Edge Version 80 oder höher ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b693-128">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="4b693-129">Um das Problem zu beheben, aktualisieren Sie Ihre Tests so, dass sie `EdgeOptions` die Klasse verwenden, und laden [Sie Microsoft Edge Driver herunter.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="4b693-129">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="4b693-130">Verwenden von Selenium 3</span><span class="sxs-lookup"><span data-stu-id="4b693-130">Use Selenium 3</span></span>  

<span data-ttu-id="4b693-131">Wenn Sie [Selenium 3][|::ref1::|]bereits verwenden, verfügen Sie möglicherweise über vorhandene Browsertests und möchten die Abdeckung für Microsoft Edge \(Chromium\) hinzufügen, ohne Ihre Version von Selenium zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4b693-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="4b693-132">Um [Selenium 3][|::ref2::|] zum Schreiben automatisierter Tests für Microsoft Edge \(EdgeHTML\) und Microsoft Edge \(Chromium\) zu verwenden, installieren Sie das [Paket "Selenium Tools für Microsoft Edge",][GithubMicrosoftEdgeSeleniumTools] um den aktualisierten Treiber zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b693-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="4b693-133">Die in den Tools enthaltenen Klassen und Klassen sind vollständig kompatibel mit den `EdgeDriver` `EdgeDriverService` integrierten Entsprechungen in Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="4b693-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="4b693-134">Verwenden Sie die folgenden Schritte, um ihrem Projekt [die Selenium Tools für Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] und [Selenium 3][|::ref3::|] hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4b693-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<span data-ttu-id="4b693-135">C#</span><span class="sxs-lookup"><span data-stu-id="4b693-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="4b693-136">Fügen Sie ihrem .NET-Projekt die Pakete ["Microsoft.Edge.SeleniumTools"][NugetPackagesMicrosoftEdgeSeleniumtools] und ["Selenium.WebDriver"][NugetPackagesSeleniumWebdriver31410] mithilfe der [NuGet CLI][NugetCLI] oder Visual Studio [.][VisualStudio]</span><span class="sxs-lookup"><span data-stu-id="4b693-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="4b693-137">Python</span><span class="sxs-lookup"><span data-stu-id="4b693-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="4b693-138">Verwenden [Sie pip,][PythonPip] um [die msedge-selenium-tools und][PythonSeleniumTools] [selenium-Pakete zu][PythonSelenium] installieren.</span><span class="sxs-lookup"><span data-stu-id="4b693-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="4b693-139">Java</span><span class="sxs-lookup"><span data-stu-id="4b693-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="4b693-140">Wenn Ihr Java Maven verwendet, kopieren Sie die folgende Abhängigkeit, und fügen Sie sie in Ihre Datei ein, um `pom.xml` [msedge-selenium-tools-java hinzuzufügen.][SonatypeMavenRepositorySearch]</span><span class="sxs-lookup"><span data-stu-id="4b693-140">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="4b693-141">Das Java ist auch direkt auf der Seite ["Selenium Tools for Microsoft Edge Releases" zum Download verfügbar.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="4b693-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<span data-ttu-id="4b693-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b693-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="4b693-143">Verwenden [Sie npm,][JavaScript|::ref4::|] um [die Edge-selenium-tools und][JavaScriptSeleniumTools] [selenium-webdriver-Pakete zu][JavaScriptSelenium] installieren.</span><span class="sxs-lookup"><span data-stu-id="4b693-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="4b693-144">Automatisieren von Microsoft Edge (Chromium) mit WebDriver</span><span class="sxs-lookup"><span data-stu-id="4b693-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="4b693-145">Um einen Browser mithilfe von WebDriver zu automatisieren, müssen Sie zunächst eine #A0 mit Ihrer bevorzugten #A1 starten.</span><span class="sxs-lookup"><span data-stu-id="4b693-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="4b693-146">Eine Sitzung ist eine einzelne ausgeführte Instanz eines Browsers, die mithilfe von #A0 gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="4b693-146">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="4b693-147">Starten Sie eine WebDriver-Sitzung, um eine neue Browserinstanz zu starten.</span><span class="sxs-lookup"><span data-stu-id="4b693-147">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="4b693-148">Die gestartete Browserinstanz bleibt geöffnet, bis Sie die #A0 schließen.</span><span class="sxs-lookup"><span data-stu-id="4b693-148">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="4b693-149">Der folgende Inhalt führt Sie durch die Verwendung von Selenium zum Starten einer #A0 mit Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="4b693-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4b693-150">Sie können die Beispiele mit Selenium 3 oder 4 ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b693-150">You may run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="4b693-151">Für die Verwendung mit Selenium 3 muss das [Paket "Selenium Tools for Microsoft Edge"][GithubMicrosoftEdgeSeleniumTools] installiert sein.</span><span class="sxs-lookup"><span data-stu-id="4b693-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="4b693-152">Automatisieren von Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="4b693-152">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="4b693-153">Selenium verwendet die `EdgeDriver` Klasse zum Verwalten einer Microsoft Edge \(Chromium\)-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4b693-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="4b693-154">Um eine Sitzung zu starten und Microsoft Edge \(Chromium\) zu automatisieren, erstellen Sie ein neues Objekt, und übergeben Sie es an ein Objekt, auf das `EdgeDriver` `EdgeOptions` die Eigenschaft festgelegt `UseChromium` `true` ist.</span><span class="sxs-lookup"><span data-stu-id="4b693-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="4b693-155">C#</span><span class="sxs-lookup"><span data-stu-id="4b693-155">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="4b693-156">Python</span><span class="sxs-lookup"><span data-stu-id="4b693-156">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="4b693-157">Java</span><span class="sxs-lookup"><span data-stu-id="4b693-157">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="4b693-158">Die `EdgeDriver` Klasse unterstützt nur Microsoft Edge \(Chromium\), und Microsoft Edge \(EdgeHTML\) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b693-158">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="4b693-159">Für die grundlegende Verwendung können Sie eine erstellen, `EdgeDriver` ohne eine Angabe zu `EdgeOptions` erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b693-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<span data-ttu-id="4b693-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b693-160">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="4b693-161">Wenn Ihr IT-Administrator die [Richtlinie "DeveloperToolsAvailability" auf "DeveloperToolsAvailability"][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] festgelegt hat, wird microsoft Edge Driver am Fahren von `2` Microsoft Edge \(Chromium\) blockiert, da der Treiber [die Microsoft Edge DevTools verwendet.][DevtoolsIndex] [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="4b693-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="4b693-162">Stellen Sie [sicher, dass die Richtlinie "DeveloperToolsAvailability"][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] auf `0` Microsoft Edge (Chromium) festgelegt oder automatisiert `1` ist.</span><span class="sxs-lookup"><span data-stu-id="4b693-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <span data-ttu-id="4b693-163">Auswählen bestimmter Browser-Binärdateien (nur Chromium)</span><span class="sxs-lookup"><span data-stu-id="4b693-163">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="4b693-164">Sie können eine #A0 mit bestimmten Microsoft Edge \(Chromium\)-Binärdateien starten.</span><span class="sxs-lookup"><span data-stu-id="4b693-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="4b693-165">Sie können z. B. Tests mit den [Microsoft Edge-Vorschaukanälen wie][MicrosoftedgeinsiderDownload] Microsoft Edge Beta ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b693-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="4b693-166">C#</span><span class="sxs-lookup"><span data-stu-id="4b693-166">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="4b693-167">Python</span><span class="sxs-lookup"><span data-stu-id="4b693-167">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="4b693-168">Java</span><span class="sxs-lookup"><span data-stu-id="4b693-168">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="4b693-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b693-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="4b693-170">Anpassen des Microsoft Edge-Treiberdiensts</span><span class="sxs-lookup"><span data-stu-id="4b693-170">Customize the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="4b693-171">C#</span><span class="sxs-lookup"><span data-stu-id="4b693-171">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="4b693-172">Wenn Sie die Klasse zum Erstellen einer Klasseninstanz verwenden, wird die entsprechende Klasse für `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) oder Microsoft Edge \(Chromium\) erstellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="4b693-172">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="4b693-173">Wenn Sie eine erstellen möchten, verwenden Sie die Methode, um eine für `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b693-173">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4b693-174">Die `CreateChromiumService()` Methode ist hilfreich, wenn Sie Anpassungen hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="4b693-174">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="4b693-175">Der folgende Code startet beispielsweise die ausführliche Protokollausgabe.</span><span class="sxs-lookup"><span data-stu-id="4b693-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="4b693-176">Sie müssen das Objekt nicht bereitstellen, `EdgeOptions` wenn Sie es an die Instanz `EdgeDriverService` `EdgeDriver` übergeben.</span><span class="sxs-lookup"><span data-stu-id="4b693-176">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="4b693-177">Die Klasse verwendet die Standardoptionen für `EdgeDriver` Microsoft Edge \(EdgeHTML\) oder Microsoft Edge \(Chromium\) basierend auf dem von Ihnen angebotenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="4b693-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="4b693-178">Wenn Sie jedoch sowohl Klassen als auch Klassen bereitstellen möchten, stellen Sie sicher, dass beide für die gleiche `EdgeDriverService` Version von Microsoft Edge konfiguriert `EdgeOptions` sind.</span><span class="sxs-lookup"><span data-stu-id="4b693-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="4b693-179">Sie können z. B. eine Standardmäßige Microsoft Edge \(EdgeHTML\)-Klasse und `EdgeDriverService` Chromium-Eigenschaften in der Klasse `EdgeOptions` verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b693-179">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="4b693-180">Die `EdgeDriver` Klasse gibt einen Fehler aus, um die Verwendung verschiedener Versionen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4b693-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="4b693-181">Python</span><span class="sxs-lookup"><span data-stu-id="4b693-181">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="4b693-182">Wenn Sie Python verwenden, erstellt und verwaltet `Edge` das Objekt das `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="4b693-182">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="4b693-183">Übergeben Sie zum `EdgeService` Konfigurieren der zusätzlichen Argumente an `Edge` das Objekt, wie im folgenden Code angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b693-183">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="4b693-184">Java</span><span class="sxs-lookup"><span data-stu-id="4b693-184">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="4b693-185">Verwenden Sie `createDefaultService()` die Methode, um eine `EdgeDriverService` für Microsoft Edge \(Chromium\) konfigurierte Methode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b693-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4b693-186">Verwenden Java Systemeigenschaften zum Anpassen von Treiberdiensten in Java.</span><span class="sxs-lookup"><span data-stu-id="4b693-186">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="4b693-187">Der folgende Code verwendet beispielsweise die Eigenschaft, `"webdriver.edge.verboseLogging"` um die ausführliche Protokollausgabe zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4b693-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<span data-ttu-id="4b693-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b693-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="4b693-189">Wenn Sie JavaScript verwenden, erstellen und konfigurieren Sie eine `Service` mit der `ServiceBuilder` Klasse.</span><span class="sxs-lookup"><span data-stu-id="4b693-189">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="4b693-190">Optional können Sie das Objekt an das Objekt übergeben, das `Service` `Driver` \(und beendet\) den Dienst für Sie startet.</span><span class="sxs-lookup"><span data-stu-id="4b693-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="4b693-191">Führen Sie zum `Service` Konfigurieren der Eine andere Methode in der Klasse `ServiceBuilder` aus, bevor Sie die Methode `build()` verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b693-191">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="4b693-192">Übergeben Sie dann `service` den Parameter als Parameter in der `Driver.createSession()` Methode.</span><span class="sxs-lookup"><span data-stu-id="4b693-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="4b693-193">Verwenden Chromium-Specific Optionen</span><span class="sxs-lookup"><span data-stu-id="4b693-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="4b693-194">Wenn Sie die Eigenschaft auf festlegen, können Sie die Klasse verwenden, um auf die gleichen Chromium-spezifischen Eigenschaften und Methoden zu zugreifen, die beim Automatisieren anderer `UseChromium` `true` `EdgeOptions` [Chromium-Browser][WebdriverCapabilitiesEdgeOptions] verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b693-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="4b693-195">C#</span><span class="sxs-lookup"><span data-stu-id="4b693-195">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="4b693-196">Python</span><span class="sxs-lookup"><span data-stu-id="4b693-196">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="4b693-197">Java</span><span class="sxs-lookup"><span data-stu-id="4b693-197">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<span data-ttu-id="4b693-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4b693-198">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="4b693-199">Wenn die Eigenschaft auf festgelegt ist, können Sie keine Eigenschaften und Methoden für `UseChromium` `true` Microsoft Edge \(EdgeHTML\) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b693-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="4b693-200">Andere #A0</span><span class="sxs-lookup"><span data-stu-id="4b693-200">Other WebDriver installation options</span></span>  

### <span data-ttu-id="4b693-201">Heiter</span><span class="sxs-lookup"><span data-stu-id="4b693-201">Chocolatey</span></span>  

<span data-ttu-id="4b693-202">Wenn Sie [Indy als][Chocolatey] Paketmanager verwenden, führen Sie den folgenden Befehl aus, um den Microsoft Edge Driver zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4b693-202">If you use [Chocolatey][Chocolatey] as your package manager, run the following command to install the Microsoft Edge Driver.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="4b693-203">Weitere Informationen finden Sie unter ["Selenium Chromium-Edgetreiber" auf "Indy".][ChocolateyPackagesSeleniumChromiumEdgeDriver]</span><span class="sxs-lookup"><span data-stu-id="4b693-203">For more information, navigate to [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="4b693-204">Docker</span><span class="sxs-lookup"><span data-stu-id="4b693-204">Docker</span></span>  

<span data-ttu-id="4b693-205">Wenn Sie [Docker][DockerHub]verwenden, führen Sie den folgenden Befehl aus, um ein vorkonfiguriertes Image mit vorinstalliertem Microsoft Edge \(Chromium\) und [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4b693-205">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="4b693-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="4b693-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="4b693-207">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="4b693-207">Next steps</span></span>  

<span data-ttu-id="4b693-208">Weitere Informationen zu WebDriver und zum Schreiben automatisierter #A0 mithilfe von Selenium finden Sie in der [Selenium-Dokumentation.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="4b693-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <span data-ttu-id="4b693-209">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="4b693-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="4b693-210">Das Microsoft #A0 ist bestrebt, Ihr Feedback zur Verwendung von WebDriver, Selenium und Microsoft Edge zu hören.</span><span class="sxs-lookup"><span data-stu-id="4b693-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="4b693-211">Um dem Team Ihre Fragen und \*\*\*\* Kommentare zu senden, wählen Sie das Symbol "Feedback senden" in den Microsoft Edge DevTools aus, oder senden Sie einen Tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="4b693-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Das Symbol „Feedback senden“ in den Microsoft Edge-Entwicklungstools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="4b693-213">Das **Symbol "Feedback senden"** in den Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4b693-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium)-Entwicklertools | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funktionen und EdgeOptions | Microsoft Docs"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability – Microsoft Edge – Richtlinien | Microsoft Docs"  

[Chocolatey]: https://chocolatey.org "Sehr | Unerginglich Software"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge Driver | Heiter"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker Hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver-| Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine-| NuGet Gallery"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Gallery"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Selenium.WebDriver 4.0.0-alpha07 | NuGet Gallery"  

[PythonPip]: https://pypi.org/project/pip/ "Pip-| PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Das Selenium Browser Automation Project | Dokumentation für Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Downloads | Selenium"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Posten eines Tweets"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver-| W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Headless browser | Wikipedia"  
