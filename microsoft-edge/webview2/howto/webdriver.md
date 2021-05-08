---
description: Automatisieren und Testen des WebView2-Steuerelements mithilfe Microsoft Edge Treibers
title: Automatisieren und Testen von WebView2 mit Microsoft Edge Treiber
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: c23d639582d4ce550406cf955c96171167bde7c8
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536484"
---
# <a name="automating-and-testing-webview2-with-microsoft-edge-driver"></a><span data-ttu-id="ec8bf-104">Automatisieren und Testen von WebView2 mit Microsoft Edge Treiber</span><span class="sxs-lookup"><span data-stu-id="ec8bf-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="ec8bf-105">Da WebView2 die Microsoft Edge \(Chromium\)-Webplattform verwendet, können WebView2-Entwickler \(Sie\) die Standardwebtools zum Debuggen und Automatisieren nutzen.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="ec8bf-106">Selen ist ein solches Tool.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-106">Selenium is one such tool.</span></span>  <span data-ttu-id="ec8bf-107">Es implementiert die W3C [WebDriver-API.][W3cWebdriver2]</span><span class="sxs-lookup"><span data-stu-id="ec8bf-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="ec8bf-108">Sie können Selenium verwenden, um automatisierte Tests zur Simulation von Benutzerinteraktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="ec8bf-109">Beginnen Sie mit den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-109">Get started with the following steps.</span></span>  

## <a name="step-1--download-webview2api-sample"></a><span data-ttu-id="ec8bf-110">Schritt 1: Herunterladen des WebView2API-Beispiels</span><span class="sxs-lookup"><span data-stu-id="ec8bf-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="ec8bf-111">Wenn Sie nicht über ein vorhandenes WebView2-Projekt verfügen, laden Sie die [WebView2API-Beispiel-App][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]herunter, ein umfassendes Beispiel für das neueste WebView2 SDK.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="ec8bf-112">Stellen Sie sicher, dass Sie die [Voraussetzungen für die WebView2API-Beispiel-App erfüllt haben.][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]</span><span class="sxs-lookup"><span data-stu-id="ec8bf-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="ec8bf-113">Nachdem Sie das Repository geklont haben, erstellen Sie das Projekt in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="ec8bf-114">Sie sollte wie die folgende Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="WebView2API-Beispiel-App" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="ec8bf-116">WebView2API-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="ec8bf-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <a name="step-2--install-microsoft-edge-driver"></a><span data-ttu-id="ec8bf-117">Schritt 2: Installieren Microsoft Edge Treibers</span><span class="sxs-lookup"><span data-stu-id="ec8bf-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="ec8bf-118">Befolgen Sie die Anweisungen zum Installieren [Microsoft Edge Treiber][WebdriverChromiumDownloadMicrosoftEdgeDriver] des browserspezifischen Treibers, der von Selenium zum Automatisieren und Testen von WebView2 erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="ec8bf-119">Stellen Sie sicher, dass die Version Microsoft Edge Treibers mit der von Der App verwendeten Version der WebView2-Runtime entspricht.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="ec8bf-120">Stellen Sie sicher, dass ihre Version von WebView2 Runtime größer oder gleich der unterstützten Version der neuesten WebView2 SDK-Version ist, damit das WebView2API-Beispiel funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="ec8bf-121">Um die neueste WebView2 SDK-Version zu finden, navigieren Sie zu [WebView2-Versionshinweise][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="ec8bf-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="ec8bf-122">Um herauszufinden, welche Version der WebView2-Runtime Sie aktuell haben, navigieren Sie zu `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="ec8bf-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a><span data-ttu-id="ec8bf-123">Schritt 3: Hinzufügen von Selen zum WebView2API-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec8bf-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="ec8bf-124">An diesem Punkt sollten Sie WebView2 Runtime installieren, ein WebView2-Projekt erstellen und Microsoft Edge installieren.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="ec8bf-125">Beginnen Sie nun mit selenium.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="ec8bf-126">Selenium unterstützt C\#, Java, Python, Javascript und Ruby.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="ec8bf-127">Die folgende Anleitung wird jedoch mit C\#geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="ec8bf-128">Erstellen Sie zunächst ein neues **C# .NET Framework** projekt in **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="ec8bf-129">Klicken **Sie in** der unteren rechten Ecke auf Weiter, um den Schritt fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Erstellen eines neuen Projekts" lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="ec8bf-131">Erstellen eines neuen Projekts</span><span class="sxs-lookup"><span data-stu-id="ec8bf-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec8bf-132">Geben Sie Ihrem Projekt **einen Namen,** speichern Sie es an Ihrem bevorzugten **Speicherort,** und wählen Sie **Erstellen aus.**</span><span class="sxs-lookup"><span data-stu-id="ec8bf-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Konfigurieren Des neuen Projekts" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="ec8bf-134">Konfigurieren Des neuen Projekts</span><span class="sxs-lookup"><span data-stu-id="ec8bf-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec8bf-135">Ein neues Projekt wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-135">A new project is created.</span></span>  <span data-ttu-id="ec8bf-136">In diesem Handbuch wird der ganze Code in die Datei `Program.cs` geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Neues Projekt" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="ec8bf-138">Neues Projekt</span><span class="sxs-lookup"><span data-stu-id="ec8bf-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec8bf-139">Fügen Sie dem Projekt nun **Selenium** hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="ec8bf-140">Installieren Sie Selenium mit dem **Selenium.WebDriver-NuGet Paket**.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="ec8bf-141">Wenn Sie **das Selenium.WebDriver-NuGet-Paket**herunterladen möchten, zeigen Sie in **Visual Studio**auf **Project**, und wählen Sie Verwalten NuGet **Paket aus.**</span><span class="sxs-lookup"><span data-stu-id="ec8bf-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover on **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="ec8bf-142">Der folgende Bildschirm sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Herunterladen NuGet Pakets" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="ec8bf-144">Herunterladen NuGet Pakets</span><span class="sxs-lookup"><span data-stu-id="ec8bf-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec8bf-145">Geben `Selenium.WebDriver` Sie in der Suchleiste ein, wählen Sie **Selenium.WebDriver** aus den Ergebnissen aus, und aktivieren Sie das Kontrollkästchen neben **pre-release**.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-145">Enter `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="ec8bf-146">Stellen Sie im rechten Fenster sicher, dass **version** auf **4.0.0-alpha04** oder höher installiert ist, und wählen Sie **Installieren aus.**</span><span class="sxs-lookup"><span data-stu-id="ec8bf-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="ec8bf-147">NuGet lädt Selenium auf Ihren Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="ec8bf-148">Weitere Informationen zum Selenium.WebDriver NuGet-Paket finden Sie unter [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="ec8bf-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Verwalten NuGet Pakets" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="ec8bf-150">Verwalten NuGet Pakets</span><span class="sxs-lookup"><span data-stu-id="ec8bf-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ec8bf-151">Verwenden `OpenQA.Selenium.Edge` Sie, indem Sie die folgende Anweisung hinzufügen:  `using OpenQA.Selenium.Edge;` am Anfang der `Program.cs` Datei.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a><span data-ttu-id="ec8bf-152">Schritt 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="ec8bf-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="ec8bf-153">Erstellen Sie zunächst das `EdgeOptions` Objekt, indem Sie den folgenden Codeausschnitt kopieren.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="ec8bf-154">Das `EdgeOptions` Objekt übernimmt die folgenden beiden Parameter.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="ec8bf-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec8bf-155">Parameter</span></span> | <span data-ttu-id="ec8bf-156">Details</span><span class="sxs-lookup"><span data-stu-id="ec8bf-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="ec8bf-157">Set to `false` , which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="ec8bf-158">Eine Zeichenfolge, die Selenium anteilt, dass Sie WebView2 fahren.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="ec8bf-159">Erstellen Sie als Nächstes auf den Dateipfad ihrer WebView2-Projektlaufzeit, erstellen Sie eine Zeichenfolge mit dem Namen, die den Dateipfad an den Ort angibt, an dem Sie Microsoft Edge Driver installiert haben, und erstellen Sie eine Zeichenfolge namens zum Speichern des Namens der `edgeOptions.BinaryLocation` `msedgedriverDir` Microsoft Edge [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Driver-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="ec8bf-160">Standardmäßig heißt die Laufzeit `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="ec8bf-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="ec8bf-161">Verwenden Sie diese beiden Zeichenfolgen, um das `EdgeDriverService` Objekt wie unten dargestellt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="ec8bf-162">Erstellen Sie schließlich das `EdgeDriver` Objekt mit `EdgeDriverService` und `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="ec8bf-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="ec8bf-163">Sie können den folgenden Code unter kopieren und `edgeOptions` einfügen.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="ec8bf-164">Stellen Sie sicher, dass Sie die richtigen Dateipfade zur Projektlaufzeit und die Microsoft Edge Treiberlaufzeit auf Ihrem Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
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
    
3.  <span data-ttu-id="ec8bf-165">Ist nun `EdgeDriver` so konfiguriert, dass WebView2 in Ihrem Projekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="ec8bf-166">Wenn Sie beispielsweise das **WebView2API-Beispiel verwenden,** können Sie zu navigieren, `https://microsoft.com` indem Sie den Befehl `e.Url = @"https://www.microsoft.com";` ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="ec8bf-167">Überprüfen Sie das Selenium-Laufwerk WebView2, indem Sie einen Haltepunkt in der Zeile festlegen und das Projekt ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selen mit WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="ec8bf-169">Selen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="ec8bf-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="ec8bf-170">Herzlichen Glückwunsch.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-170">Congratulations.</span></span>  <span data-ttu-id="ec8bf-171">Sie haben ein WebView2-Projekt erfolgreich automatisiert und WebView2 mithilfe von Selenium und Microsoft Edge gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ec8bf-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ec8bf-172">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec8bf-172">See also</span></span>  

*   <span data-ttu-id="ec8bf-173">Einen umfassenden Überblick darüber, wie die APIs Selenium WebView2 oder Microsoft Edge \(Chromium\) steuert, finden Sie in der Dokumentation zu [WebDriver on Selenium.][SeleniumWebdriver]</span><span class="sxs-lookup"><span data-stu-id="ec8bf-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="ec8bf-174">Weitere Informationen zum WebView2-Steuerelement und deren Verwendung beim Einbetten von Webinhalten in Ihre systemeigene App finden Sie unter [Einführung in Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="ec8bf-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="ec8bf-175">Weitere Informationen zum Automatisieren von Microsoft Edge \(Chromium\) finden Sie unter Verwenden von [WebDriver (Chromium) für die Testautomatisierung.][WebdriverChromium]</span><span class="sxs-lookup"><span data-stu-id="ec8bf-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="ec8bf-176">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="ec8bf-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Verwenden von WebDriver (Chromium) für Testautomatisierungstests | Microsoft Docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Download Microsoft Edge Driver – Verwenden von WebDriver (Chromium) für die Testautomatisierung | Microsoft Docs"  
[WebViewIndex]: ../index.md "Einführung in Microsoft Edge WebView2 – Microsoft Docs"  
[Webview2Releasenotes]: ../releasenotes.md "Versionshinweise für WebView2 SDK | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Herunterladen von WebDriver | Microsoft Edge Entwickler"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Voraussetzungen – WebView2-API-| GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | NuGet Gallery"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
