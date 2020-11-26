---
description: Automatisieren und Testen des WebView2-Steuerelements mit Microsoft Edge Driver
title: Automatisieren und Testen von WebView2 mit Microsoft Edge Driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: 2af1ce222abb1dc7a279afc05e87e7e42a45fe9e
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191617"
---
# <span data-ttu-id="f21ba-104">Automatisieren und Testen von WebView2 mit Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="f21ba-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="f21ba-105">Da WebView2 die Microsoft Edge \ (Chromium \)-Webplattform verwendet, können WebView2-Entwickler \ (You \) standardmäßige Webtools für Debuggen und Automatisierung nutzen.</span><span class="sxs-lookup"><span data-stu-id="f21ba-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="f21ba-106">Selen ist ein solches Tool.</span><span class="sxs-lookup"><span data-stu-id="f21ba-106">Selenium is one such tool.</span></span>  <span data-ttu-id="f21ba-107">Sie implementiert die W3C- [WebDriver][W3cWebdriver2] -API.</span><span class="sxs-lookup"><span data-stu-id="f21ba-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="f21ba-108">Sie können Selen verwenden, um automatisierte Tests zum Simulieren von Benutzerinteraktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f21ba-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="f21ba-109">Beginnen Sie mit den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="f21ba-109">Get started with the following steps.</span></span>  

## <span data-ttu-id="f21ba-110">Schritt 1: Herunterladen des WebView2API-Beispiels</span><span class="sxs-lookup"><span data-stu-id="f21ba-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="f21ba-111">Wenn Sie nicht über ein vorhandenes WebView2-Projekt verfügen, laden Sie die [WebView2API-Beispiel-App][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]herunter, ein umfassendes Beispiel für das neueste WebView2-SDK.</span><span class="sxs-lookup"><span data-stu-id="f21ba-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="f21ba-112">Stellen Sie sicher, dass Sie die [Voraussetzungen für die WebView2API-Beispiel-App][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="f21ba-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="f21ba-113">Nachdem Sie das Repo geklont haben, erstellen Sie das Projekt in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f21ba-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="f21ba-114">Es sollte wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="f21ba-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="WebView2API-Beispiel-App" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="f21ba-116">WebView2API-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="f21ba-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <span data-ttu-id="f21ba-117">Schritt 2: Installieren des Microsoft Edge-Treibers</span><span class="sxs-lookup"><span data-stu-id="f21ba-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="f21ba-118">Befolgen Sie die Anweisungen zum Installieren des [Microsoft Edge-Treibers][WebdriverChromiumDownloadMicrosoftEdgeDriver] mit dem browserspezifischen Treiber, der von Selenium zum Automatisieren und Testen von WebView2 erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f21ba-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="f21ba-119">Stellen Sie sicher, dass die Version von Microsoft Edge Driver mit der Version der WebView2-Runtime übereinstimmt, die von der APP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f21ba-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="f21ba-120">Damit das WebView2API-Beispiel funktioniert, stellen Sie sicher, dass Ihre Version der WebView2-Laufzeit größer oder gleich der unterstützten Version der neuesten WebView2 SDK-Version ist.</span><span class="sxs-lookup"><span data-stu-id="f21ba-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="f21ba-121">Navigieren Sie zu [WebView2][Webview2Releasenotes], um die neueste Version von WebView2 SDK zu finden.</span><span class="sxs-lookup"><span data-stu-id="f21ba-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="f21ba-122">Wenn Sie feststellen möchten, welche Version der WebView2-Laufzeit Sie zurzeit haben, navigieren Sie zu `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="f21ba-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <span data-ttu-id="f21ba-123">Schritt 3: Hinzufügen von Selen zum WebView2API-Beispiel</span><span class="sxs-lookup"><span data-stu-id="f21ba-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="f21ba-124">An diesem Punkt sollten Sie die WebView2-Runtime installiert haben, ein WebView2-Projekt erstellt und Microsoft Edge-Treiber installiert haben.</span><span class="sxs-lookup"><span data-stu-id="f21ba-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="f21ba-125">Beginnen Sie mit der Verwendung von Selen.</span><span class="sxs-lookup"><span data-stu-id="f21ba-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="f21ba-126">Selen unterstützt C \ #, Java, Python, JavaScript und Ruby.</span><span class="sxs-lookup"><span data-stu-id="f21ba-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="f21ba-127">Das folgende Handbuch wird jedoch mit C \ # geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f21ba-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="f21ba-128">Beginnen Sie mit dem Erstellen eines neuen **C# .NET Framework** -Projekts in **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="f21ba-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="f21ba-129">Klicken Sie in der unteren rechten Ecke auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="f21ba-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Erstellen eines neuen Projekts" lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="f21ba-131">Erstellen eines neuen Projekts</span><span class="sxs-lookup"><span data-stu-id="f21ba-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f21ba-132">Geben Sie Ihrem Projekt einen **Namen**, speichern Sie es an Ihrem bevorzugten **Speicherort**, und wählen Sie **Erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="f21ba-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Konfigurieren des neuen Projekts" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="f21ba-134">Konfigurieren des neuen Projekts</span><span class="sxs-lookup"><span data-stu-id="f21ba-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f21ba-135">Ein neues Projekt wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="f21ba-135">A new project is created.</span></span>  <span data-ttu-id="f21ba-136">In diesem Leitfaden wird der gesamte Code in die `Program.cs` Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f21ba-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Neues Projekt" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="f21ba-138">Neues Projekt</span><span class="sxs-lookup"><span data-stu-id="f21ba-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f21ba-139">Fügen Sie dem Projekt nun **Selen** hinzu.</span><span class="sxs-lookup"><span data-stu-id="f21ba-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="f21ba-140">Installieren Sie Selen mithilfe des **Selen. WebDriver NuGet-Pakets**.</span><span class="sxs-lookup"><span data-stu-id="f21ba-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="f21ba-141">Wenn Sie das **Selen. WebDriver NuGet-Paket**herunterladen möchten, zeigen Sie in **Visual Studio**auf **Project**, und wählen Sie **NuGet-Paket verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="f21ba-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="f21ba-142">Der folgende Bildschirm sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f21ba-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="NuGet-Paket herunterladen" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="f21ba-144">NuGet-Paket herunterladen</span><span class="sxs-lookup"><span data-stu-id="f21ba-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f21ba-145">Geben Sie `Selenium.WebDriver` in die Suchleiste ein, wählen Sie **Selen. WebDriver** aus den Ergebnissen aus, und stellen Sie sicher, dass Sie das Kontrollkästchen neben " **Pre-Release einbeziehen**" markieren.</span><span class="sxs-lookup"><span data-stu-id="f21ba-145">Enter `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="f21ba-146">Stellen Sie im rechten Fenster sicher, dass die **Version** für die Installation von **4.0.0-alpha04** oder höher eingestellt ist, und wählen Sie **Installieren**aus.</span><span class="sxs-lookup"><span data-stu-id="f21ba-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="f21ba-147">NuGet downloadet Selen auf Ihren Computer.</span><span class="sxs-lookup"><span data-stu-id="f21ba-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="f21ba-148">Wenn Sie mehr über das Selen. WebDriver NuGet-Paket erfahren möchten, navigieren Sie zu [Selen. WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="f21ba-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Verwalten des NuGet-Pakets" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="f21ba-150">Verwalten des NuGet-Pakets</span><span class="sxs-lookup"><span data-stu-id="f21ba-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f21ba-151">Verwenden Sie `OpenQA.Selenium.Edge` Diese Anweisung, indem Sie die folgende Anweisung  `using OpenQA.Selenium.Edge;` am Anfang der Datei hinzufügen `Program.cs` .</span><span class="sxs-lookup"><span data-stu-id="f21ba-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <span data-ttu-id="f21ba-152">Schritt 4: Laufwerk WebView2 mit Selen und Microsoft Edge-Treiber</span><span class="sxs-lookup"><span data-stu-id="f21ba-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="f21ba-153">Erstellen Sie zunächst das `EdgeOptions` Objekt, indem Sie den folgenden Codeausschnitt kopieren.</span><span class="sxs-lookup"><span data-stu-id="f21ba-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="f21ba-154">Das `EdgeOptions` Objekt akzeptiert die folgenden beiden Parameter.</span><span class="sxs-lookup"><span data-stu-id="f21ba-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="f21ba-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="f21ba-155">Parameter</span></span> | <span data-ttu-id="f21ba-156">Details</span><span class="sxs-lookup"><span data-stu-id="f21ba-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="f21ba-157">"Auf `false` " festzulegen, wodurch Selen mitgeteilt wird, dass Sie den neuen Chrom basierten Microsoft Edge-Browser antreiben.</span><span class="sxs-lookup"><span data-stu-id="f21ba-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="f21ba-158">Eine Zeichenfolge, die Selen anweist, dass Sie WebView2 fahren.</span><span class="sxs-lookup"><span data-stu-id="f21ba-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="f21ba-159">Legen Sie als nächstes `edgeOptions.BinaryLocation` den Dateipfad der WebView2-Projektlaufzeit fest, erstellen Sie eine Zeichenfolge mit dem Namen `msedgedriverDir` , die den Dateipfad zum Speicherort des [Microsoft Edge-Treibers][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]enthält, und erstellen Sie eine Zeichenfolge, `msedgedriverExe` die den Namen der Microsoft Edge Driver-Laufzeit speichert.</span><span class="sxs-lookup"><span data-stu-id="f21ba-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="f21ba-160">Standardmäßig wird die Common Language Runtime benannt `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="f21ba-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="f21ba-161">Verwenden Sie diese beiden Zeichenfolgen, um das Objekt zu konstruieren, `EdgeDriverService` wie unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f21ba-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="f21ba-162">Erstellen Sie schließlich das `EdgeDriver` Objekt mit `EdgeDriverService` und `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="f21ba-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="f21ba-163">Sie können den folgenden Code darunter kopieren und einfügen `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="f21ba-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="f21ba-164">Stellen Sie sicher, dass Sie die richtigen Dateipfade für Ihre Projektlaufzeit und die Microsoft Edge Driver-Laufzeit auf Ihrem Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="f21ba-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
    ```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample runtime
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";
    
    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";
    
    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";
    
    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);
    
    EdgeDriver e = new EdgeDriver(service, edgeOptions);
    ```
    
3.  <span data-ttu-id="f21ba-165">Jetzt `EdgeDriver` ist die Konfiguration für das Laufwerk des WebView2 in Ihrem Projekt konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f21ba-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="f21ba-166">Wenn Sie beispielsweise das **WebView2API-Beispiel**verwenden, können Sie zu navigieren, `https://microsoft.com` indem Sie den `e.Url = @"https://www.microsoft.com";` Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="f21ba-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="f21ba-167">Überprüfen Sie das Selen Drive-WebView2, indem Sie einen Haltepunkt in der Zeile festlegen und das Projekt ausführen.</span><span class="sxs-lookup"><span data-stu-id="f21ba-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selen mit WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="f21ba-169">Selen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="f21ba-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="f21ba-170">Herzlichen Glückwunsch.</span><span class="sxs-lookup"><span data-stu-id="f21ba-170">Congratulations.</span></span>  <span data-ttu-id="f21ba-171">Sie haben erfolgreich ein WebView2-Projekt und gesteuerte WebView2 mit Selen und Microsoft Edge Driver automatisiert.</span><span class="sxs-lookup"><span data-stu-id="f21ba-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <span data-ttu-id="f21ba-172">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f21ba-172">See also</span></span>  

*   <span data-ttu-id="f21ba-173">Einen umfassenden Überblick darüber, wie die APIs Selenium WebView2 oder Microsoft Edge \ (Chrom \) steuert, navigieren Sie zu [WebDriver auf der Selenium-Dokumentation][SeleniumWebdriver] .</span><span class="sxs-lookup"><span data-stu-id="f21ba-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="f21ba-174">Wenn Sie mehr über das WebView2-Steuerelement und seine Verwendung beim Einbetten von Webinhalten in Ihre systemeigene App erfahren möchten, navigieren Sie zu [Introduction to Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="f21ba-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="f21ba-175">Weitere Informationen zum Automatisieren von Microsoft Edge \ (Chrom \) finden Sie unter [Verwenden von WebDriver (Chrom) für die Testautomatisierung][WebdriverChromium] .</span><span class="sxs-lookup"><span data-stu-id="f21ba-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <span data-ttu-id="f21ba-176">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="f21ba-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Verwenden von WebDriver (Chrom) für die Testautomatisierung | Microsoft docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Microsoft Edge Driver herunterladen – verwenden Sie WebDriver (Chrom) für die Testautomatisierung | Microsoft docs"  
[WebViewIndex]: ../index.md "Einführung in Microsoft Edge WebView2 – Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "WebDriver herunterladen | Microsoft Edge-Entwickler"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Voraussetzungen – Beispiel für die WebView2-API | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selen. WebDriver 4.0.0-alpha04 | NuGet-Katalog"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selen"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
