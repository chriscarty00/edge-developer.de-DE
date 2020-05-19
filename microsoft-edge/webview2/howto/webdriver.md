---
description: Automatisieren und Testen des WebView2-Steuerelements mit Microsoft Edge Driver
title: Automatisieren und Testen von WebView2 mit Microsoft Edge Driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: acee8c1f791fdd4a2604b8f3bfa7664548a164d1
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659701"
---
# <span data-ttu-id="797e3-104">Automatisieren und Testen von WebView2 mit Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="797e3-104">Automating and Testing WebView2 with Microsoft Edge Driver</span></span>

<span data-ttu-id="797e3-105">Da WebView2 die Chrom-Webplattform nutzt, können WebView2-Entwickler standardmäßige Webtools für Debugging und Automatisierung nutzen.</span><span class="sxs-lookup"><span data-stu-id="797e3-105">Because WebView2 utilizes the Chromium web platform, WebView2 developers can take advantage of standard web tooling for debugging and automation.</span></span> <span data-ttu-id="797e3-106">Ein solches Tool ist Selen, das die W3C- [WebDriver](https://www.w3.org/TR/webdriver2/) -API implementiert, mit der automatisierte Tests erstellt werden können, mit denen Benutzerinteraktionen simuliert werden.</span><span class="sxs-lookup"><span data-stu-id="797e3-106">One such tool is Selenium, which implements the W3C [WebDriver](https://www.w3.org/TR/webdriver2/) API, which can be used to create automated tests that simulate user interactions.</span></span>

<span data-ttu-id="797e3-107">Dies sind die ersten Schritte:</span><span class="sxs-lookup"><span data-stu-id="797e3-107">Here's how to get started:</span></span>

## <span data-ttu-id="797e3-108">Schritt 1: Herunterladen des WebView2API-Beispiels</span><span class="sxs-lookup"><span data-stu-id="797e3-108">Step 1: Download WebView2API Sample</span></span>

<span data-ttu-id="797e3-109">Wenn Sie nicht über ein vorhandenes WebView2-Projekt verfügen, laden Sie unsere [WebView2API-Beispielanwendung](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample)herunter, ein umfassendes Beispiel für das neueste WebView2-SDK.</span><span class="sxs-lookup"><span data-stu-id="797e3-109">If you do not have an existing WebView2 project, download our [WebView2API Sample application](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), a comprehensive sample of the latest WebView2 SDK.</span></span> <span data-ttu-id="797e3-110">Bitte überprüfen Sie, ob Sie diese [Voraussetzungen](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites)erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="797e3-110">Please double check that you have satisfied these [prerequisites](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).</span></span>

<span data-ttu-id="797e3-111">Nachdem Sie das Repo geklont haben, erstellen Sie das Projekt in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="797e3-111">Once you have cloned the repo, build the project in Visual Studio.</span></span> <span data-ttu-id="797e3-112">Es sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="797e3-112">It should look like the following:</span></span>

![Alternativer Text](../media/webdriver/sample-app.png)

## <span data-ttu-id="797e3-114">Schritt 2: Installieren des Microsoft Edge-Treibers</span><span class="sxs-lookup"><span data-stu-id="797e3-114">Step 2: Install Microsoft Edge Driver</span></span>

<span data-ttu-id="797e3-115">Befolgen Sie die Anweisungen zum Installieren des [Microsoft Edge-Treibers](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) mit dem browserspezifischen Treiber, der von Selenium zum Automatisieren und Testen von WebView2 erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="797e3-115">Follow the instructions to install [Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) the browser-specific driver required by Selenium to automate and test WebView2.</span></span>

<span data-ttu-id="797e3-116">Es ist wichtig, sicherzustellen, dass die Version von Microsoft Edge Driver mit der Version von Microsoft Edge übereinstimmt, die von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="797e3-116">It is important to make sure that the version of Microsoft Edge Driver matches the version of Microsoft Edge that the application uses.</span></span> <span data-ttu-id="797e3-117">Damit das WebView2API-Beispiel funktioniert, stellen Sie sicher, dass Ihre Version von Microsoft Edge größer oder gleich der unterstützten Version unserer neuesten SDK-Version ist, die [in unseren Versions](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes)hinweisen zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="797e3-117">For the WebView2API Sample to work, make sure that your version of Microsoft Edge is greater than or equal to the supported version of our latest SDK release found [in our Release Notes](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes).</span></span> <span data-ttu-id="797e3-118">Wenn Sie wissen möchten, welche Version von Microsoft Edge Sie derzeit haben, laden Sie `edge://settings/help` den Browser.</span><span class="sxs-lookup"><span data-stu-id="797e3-118">To find out what version of Microsoft Edge you currently have, load `edge://settings/help` in the browser.</span></span>

## <span data-ttu-id="797e3-119">Schritt 3: Hinzufügen von Selen zum WebView2API-Beispiel</span><span class="sxs-lookup"><span data-stu-id="797e3-119">Step 3: Add Selenium to the WebView2API Sample</span></span>

<span data-ttu-id="797e3-120">An diesem Punkt sollten Sie Microsoft Edge installiert haben, ein WebView2-Projekt erstellt und Microsoft Edge-Treiber installiert haben.</span><span class="sxs-lookup"><span data-stu-id="797e3-120">At this point you should have Microsoft Edge installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span> <span data-ttu-id="797e3-121">Nun beginnen wir mit der Verwendung von Selen.</span><span class="sxs-lookup"><span data-stu-id="797e3-121">Now, let's get started using Selenium.</span></span>

> [!NOTE]
> <span data-ttu-id="797e3-122">Selen unterstützt C#, Java, Python, JavaScript und Ruby.</span><span class="sxs-lookup"><span data-stu-id="797e3-122">Selenium supports C#, Java, Python, Javascript, and Ruby.</span></span> <span data-ttu-id="797e3-123">Dieses Handbuch befindet sich jedoch in C#.</span><span class="sxs-lookup"><span data-stu-id="797e3-123">However, this guide will be in C#.</span></span>

1. <span data-ttu-id="797e3-124">Beginnen Sie mit dem Erstellen eines neuen **C# .NET Framework** -Projekts in **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="797e3-124">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span> <span data-ttu-id="797e3-125">Klicken Sie in der unteren rechten Ecke auf **weiter** , um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="797e3-125">Click **Next** on the bottom right-hand corner to continue.</span></span>

![Alternativer Text](../media/webdriver/new-project.png)

2. <span data-ttu-id="797e3-127">Geben Sie Ihrem Projekt einen **Namen**, speichern Sie es an Ihrem bevorzugten **Speicherort**, und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="797e3-127">Give your project a **name**, save it to your preferred **location**, and click **Create**.</span></span>

![Alternativer Text](../media/webdriver/app-create.png)

3. <span data-ttu-id="797e3-129">Es wird ein neues Projekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="797e3-129">A new project will be created.</span></span> <span data-ttu-id="797e3-130">In diesem Leitfaden wird der gesamte Code in die **Program.cs** -Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="797e3-130">In this guide, all code will be written in the **Program.cs** file.</span></span>

![Alternativer Text](../media/webdriver/start-app.png)

4. <span data-ttu-id="797e3-132">Nun fügen wir **Selen** zum Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="797e3-132">Now let's add **Selenium** to the project.</span></span> <span data-ttu-id="797e3-133">Sie können Selen über das **Selen. WebDriver NuGet-Paket**installieren.</span><span class="sxs-lookup"><span data-stu-id="797e3-133">You can install Selenium via the **Selenium.WebDriver NuGet package**.</span></span>

<span data-ttu-id="797e3-134">Wenn Sie das **Selen. WebDriver NuGet-Paket**herunterladen möchten, zeigen Sie in **Visual Studio**auf **Project** , und wählen Sie **NuGet-Paket verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="797e3-134">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project** and select **Manage NuGet Package**.</span></span> <span data-ttu-id="797e3-135">Der folgende Bildschirm sollte angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="797e3-135">The following screen should appear:</span></span>

![Alternativer Text](../media/webdriver/download-nuget.png)

5. <span data-ttu-id="797e3-137">Geben Sie **Selen. WebDriver** in der Suchleiste ein, klicken Sie auf **Selen. WebDriver** aus den Ergebnissen, und stellen Sie sicher, dass Sie das Kontrollkästchen neben " **Pre-Release einbeziehen**" markieren.</span><span class="sxs-lookup"><span data-stu-id="797e3-137">Enter **Selenium.WebDriver** in the search bar, click **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span> <span data-ttu-id="797e3-138">Stellen Sie im rechten Fenster sicher, dass die **Version** für die Installation von **4.0.0-alpha04** oder höher eingestellt ist, und klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="797e3-138">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and click **Install**.</span></span> <span data-ttu-id="797e3-139">Nuget wird Selen auf Ihren Computer herunterladen.</span><span class="sxs-lookup"><span data-stu-id="797e3-139">Nuget will download Selenium to your machine.</span></span>

[<span data-ttu-id="797e3-140">Weitere Informationen zum Selen. WebDriver NuGet-Paket.</span><span class="sxs-lookup"><span data-stu-id="797e3-140">Learn more about the Selenium.WebDriver NuGet package.</span></span>](https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04)

![Alternativer Text](../media/webdriver/nuget.png)

6. <span data-ttu-id="797e3-142">Verwenden Sie **OpenQA. Selenium. Edge** , indem Sie die folgende Anweisung hinzufügen: ```using OpenQA.Selenium.Edge;``` am Anfang von **Program.cs**</span><span class="sxs-lookup"><span data-stu-id="797e3-142">Use **OpenQA.Selenium.Edge** by adding the following statement:```using OpenQA.Selenium.Edge;``` at the beginning of **Program.cs**</span></span>

```csharp
using OpenQA.Selenium.Edge;

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## <span data-ttu-id="797e3-143">Schritt 4: Laufwerk WebView2 mit Selen und Microsoft EdgeDriver</span><span class="sxs-lookup"><span data-stu-id="797e3-143">Step 4: Drive WebView2 with Selenium and Microsoft EdgeDriver</span></span>

1. <span data-ttu-id="797e3-144">Erstellen Sie zunächst das `EdgeOptions` Objekt, indem Sie den folgenden Code kopieren:</span><span class="sxs-lookup"><span data-stu-id="797e3-144">First, create the `EdgeOptions` object, by copying the code below:</span></span>

```csharp
static void Main(string[] args)
{
    // EdgeOptions() requires using OpenQA.Selenium.Edge
    // Construct EdgeOptions with is_legacy = false and the string "webview2"
    EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
```

<span data-ttu-id="797e3-145">Das `EdgeOptions` Objekt hat zwei Parameter:</span><span class="sxs-lookup"><span data-stu-id="797e3-145">The `EdgeOptions` object takes in two parameters:</span></span>
\
    **<span data-ttu-id="797e3-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="797e3-146">Parameters:</span></span>**
    1. `is_legacy`<span data-ttu-id="797e3-147">: auf `false` , der angibt, dass Selen den neuen Chrom basierten Microsoft Edge-Browser steuert.</span><span class="sxs-lookup"><span data-stu-id="797e3-147">: set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span>
    2. `"webview2"`<span data-ttu-id="797e3-148">: eine Zeichenfolge, die Selen angibt, dass Sie **WebView2** fahren</span><span class="sxs-lookup"><span data-stu-id="797e3-148">: a string that tell Selenium you are driving **WebView2**</span></span>

2. <span data-ttu-id="797e3-149">Legen Sie als nächstes `edgeOptions.BinaryLocation` den Dateipfad der ausführbaren Datei Ihres WebView2-Projekts fest, erstellen Sie eine Zeichenfolge namens `msedgedriverDir` , die den Dateipfad zum Speicherort der [Microsoft Edge-Treiber](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads)bereitstellt, und erstellen Sie eine Zeichenfolge, die aufgerufen wird, `msedgedriverExe` um den Namen der ausführbaren Datei des Microsoft Edge-Treibers zu speichern.</span><span class="sxs-lookup"><span data-stu-id="797e3-149">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project's executable, create a string called `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads), and create a string called `msedgedriverExe` to store the name of the Microsoft Edge Driver executable.</span></span> <span data-ttu-id="797e3-150">Standardmäßig wird die ausführbare Datei aufgerufen `"msedgedriver.exe"` .</span><span class="sxs-lookup"><span data-stu-id="797e3-150">By default, the executable is called `"msedgedriver.exe"`.</span></span> <span data-ttu-id="797e3-151">Verwenden Sie diese beiden Zeichenfolgen, um das Objekt zu konstruieren, `EdgeDriverService` wie unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="797e3-151">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span> <span data-ttu-id="797e3-152">Erstellen Sie schließlich das `EdgeDriver` Objekt mit `EdgeDriverService` und `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="797e3-152">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>

<span data-ttu-id="797e3-153">Sie können den folgenden Code darunter kopieren und einfügen `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="797e3-153">You can copy and paste the following code underneath `edgeOptions`.</span></span> <span data-ttu-id="797e3-154">Stellen Sie sicher, dass Sie die korrekten Dateipfade zur ausführbaren Datei des Projekts und zur ausführbaren Datei des Microsoft Edge-Treibers auf Ihrem Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="797e3-154">Make sure to specify the correct file paths to your project's executable and the Microsoft Edge Driver's executable on your machine.</span></span>

```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample's executable
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";

    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";

    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";

    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);

    EdgeDriver e = new EdgeDriver(service, edgeOptions);
```

3. <span data-ttu-id="797e3-155">**EdgeDriver** ist nun so konfiguriert, dass es die **WebView2** in Ihrem Projekt fährt.</span><span class="sxs-lookup"><span data-stu-id="797e3-155">Now, **EdgeDriver** is configured to drive the **WebView2** in your project.</span></span> <span data-ttu-id="797e3-156">Wenn Sie beispielsweise das **WebView2API-Beispiel**verwenden, können Sie durch einen Anruf zu **Navigieren** <https://microsoft.com> ```e.Url = @"https://www.microsoft.com";``` .</span><span class="sxs-lookup"><span data-stu-id="797e3-156">For example, if you are using the **WebView2API Sample**, you can **Navigate** to <https://microsoft.com> by calling ```e.Url = @"https://www.microsoft.com";```.</span></span> <span data-ttu-id="797e3-157">Sie können **Selenium** Drive **WebView2** beobachten, indem Sie in dieser Zeile einen Haltepunkt festlegen und das Projekt ausführen.</span><span class="sxs-lookup"><span data-stu-id="797e3-157">You can watch **Selenium** drive **WebView2** by setting a breakpoint on this line and running the project.</span></span>

```csharp
    //The following will Navigate the WebView2API Sample from bing.com to microsoft.com
    e.Url = @"https://www.microsoft.com";

    //This exits the edge driver
    e.Quit();
}
```

![Alternativer Text](../media/webdriver/microsoft.png)

<span data-ttu-id="797e3-159">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="797e3-159">Congratulations!</span></span> <span data-ttu-id="797e3-160">Sie haben erfolgreich ein WebView2-Projekt und gesteuerte WebView2 mit Selen und Microsoft Edge Driver automatisiert.</span><span class="sxs-lookup"><span data-stu-id="797e3-160">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>

## <span data-ttu-id="797e3-161">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="797e3-161">Next Steps</span></span>

<span data-ttu-id="797e3-162">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="797e3-162">To learn more:</span></span>

- <span data-ttu-id="797e3-163">Schauen Sie sich die [Dokumentation zu Selen](https://www.selenium.dev/documentation/en/webdriver/) an, um einen umfassenden Überblick über die APIs zu erhalten, die Selen für das fahren von WebView2 oder Microsoft Edge (Chrom) zur Verfügung hat.</span><span class="sxs-lookup"><span data-stu-id="797e3-163">Check out [Selenium's documentation](https://www.selenium.dev/documentation/en/webdriver/) for a comprehensive look at the APIs Selenium has available for driving WebView2 or Microsoft Edge (Chromium)</span></span>
- <span data-ttu-id="797e3-164">Weitere Informationen zum [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) -Steuerelement und zur Verwendung beim Einbetten von Webinhalten in Ihre systemeigene App</span><span class="sxs-lookup"><span data-stu-id="797e3-164">Learn more about [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) control and how to use it when embedding web content in your native app</span></span>
- <span data-ttu-id="797e3-165">Lesen Sie [Dokumentation zu Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) , um mehr über die Automatisierung von Microsoft Edge (Chrom) zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="797e3-165">Check out [documentation for Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) to learn more about automating Microsoft Edge (Chromium)</span></span>

## <span data-ttu-id="797e3-166">Kontakt mit dem WebView2-Team</span><span class="sxs-lookup"><span data-stu-id="797e3-166">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="797e3-167">Helfen Sie uns, ein reicheres WebView2-Erlebnis zu schaffen, indem Sie Ihr Feedback austauschen!</span><span class="sxs-lookup"><span data-stu-id="797e3-167">Help us build a richer WebView2 experience by sharing your feedback!</span></span> <span data-ttu-id="797e3-168">Besuchen Sie unser [Feedback-Repo](https://github.com/MicrosoftEdge/WebViewFeedback) , um Funktionsanforderungen oder Fehlerberichte zu übermitteln oder nach bekannten Problemen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="797e3-168">Visit our [feedback repo](https://github.com/MicrosoftEdge/WebViewFeedback) to submit feature requests or bug reports or to search for known issues.</span></span>
