---
description: Automatisieren und Testen des WebView2-Steuerelements mithilfe Microsoft Edge Treibers
title: Automatisieren und Testen von WebView2 mit Microsoft Edge Treiber
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: 37c0e41e11693c8a21b7240bf9370fd658834cff
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535957"
---
# <a name="automate-and-test-webview2-with-microsoft-edge-driver"></a>Automatisieren und Testen von WebView2 mit Microsoft Edge Treiber  

Da WebView2 die Microsoft Edge \(Chromium\)-Webplattform verwendet, können WebView2-Entwickler \(Sie\) die Standardwebtools zum Debuggen und Automatisieren nutzen.  Selen ist ein solches Tool.  Es implementiert die W3C [WebDriver-API.][W3cWebdriver2]  Sie können Selenium verwenden, um automatisierte Tests zur Simulation von Benutzerinteraktionen zu erstellen.  

Beginnen Sie mit den folgenden Schritten.  

## <a name="step-1--download-webview2api-sample"></a>Schritt 1: Herunterladen des WebView2API-Beispiels  

Wenn Sie nicht über ein vorhandenes WebView2-Projekt verfügen, laden Sie die [WebView2API-Beispiel-App][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]herunter, ein umfassendes Beispiel für das neueste WebView2 SDK.  Stellen Sie sicher, dass Sie die [Voraussetzungen für die WebView2API-Beispiel-App erfüllt haben.][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]  

Nachdem Sie das Repository geklont haben, erstellen Sie das Projekt in Visual Studio.  Sie sollte wie die folgende Abbildung aussehen.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="WebView2API-Beispiel-App" lightbox="../media/webdriver/sample-app.png":::
   WebView2API-Beispiel-App  
:::image-end:::    

## <a name="step-2--install-microsoft-edge-driver"></a>Schritt 2: Installieren Microsoft Edge Treibers  

Befolgen Sie die Anweisungen zum Installieren [Microsoft Edge Treiber][WebdriverChromiumDownloadMicrosoftEdgeDriver] des browserspezifischen Treibers, der von Selenium zum Automatisieren und Testen von WebView2 erforderlich ist.  

Stellen Sie sicher, dass die Version Microsoft Edge Treibers mit der von Der App verwendeten Version der WebView2-Runtime entspricht.  Stellen Sie sicher, dass ihre Version von WebView2 Runtime größer oder gleich der unterstützten Version der neuesten WebView2 SDK-Version ist, damit das WebView2API-Beispiel funktioniert.  Um die neueste WebView2 SDK-Version zu finden, navigieren Sie zu [WebView2-Versionshinweise][Webview2ReleaseNotes].  Um herauszufinden, welche Version der WebView2-Runtime Sie aktuell haben, navigieren Sie zu `edge://settings/help` .  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a>Schritt 3: Hinzufügen von Selen zum WebView2API-Beispiel  

An diesem Punkt sollten Sie WebView2 Runtime installieren, ein WebView2-Projekt erstellen und Microsoft Edge installieren.  Beginnen Sie nun mit selenium.  

> [!NOTE]
> Selenium unterstützt C\#, Java, Python, Javascript und Ruby.  Die folgende Anleitung wird jedoch mit C\#geschrieben.  

1.  Erstellen Sie zunächst ein neues **C# .NET Framework** projekt in **Visual Studio**.  Klicken **Sie in** der unteren rechten Ecke auf Weiter, um den Schritt fortzufahren.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Erstellen eines neuen Projekts" lightbox="../media/webdriver/new-project.png":::
       Erstellen eines neuen Projekts  
    :::image-end:::  
    
1.  Geben Sie Ihrem Projekt **einen Namen,** speichern Sie es an Ihrem bevorzugten **Speicherort,** und wählen Sie **Erstellen aus.**  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Konfigurieren Des neuen Projekts" lightbox="../media/webdriver/app-create.png":::
       Konfigurieren Des neuen Projekts  
    :::image-end:::  
    
1.  Ein neues Projekt wird erstellt.  In diesem Handbuch wird der ganze Code in die Datei `Program.cs` geschrieben.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Neues Projekt" lightbox="../media/webdriver/start-app.png":::
       Neues Projekt  
    :::image-end:::  
    
1.  Fügen Sie dem Projekt nun **Selenium** hinzu.  Installieren Sie Selenium mit dem **Selenium.WebDriver-NuGet Paket**.  
    
    Wenn Sie **das Selenium.WebDriver-NuGet-Paket**herunterladen möchten, zeigen Sie in **Visual Studio**auf **Project**, und wählen Sie Verwalten NuGet **Paket aus.**  Der folgende Bildschirm sollte angezeigt werden.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Herunterladen NuGet Pakets" lightbox="../media/webdriver/download-nuget.png":::
       Herunterladen NuGet Pakets  
    :::image-end:::  
    
1.  Geben Sie in die Suchleiste ein, wählen Sie `Selenium.WebDriver` **Selenium.WebDriver** aus den Ergebnissen aus, und aktivieren Sie das Kontrollkästchen neben **pre-release**.  Stellen Sie im rechten Fenster sicher, dass **version** auf **4.0.0-alpha04** oder höher installiert ist, und wählen Sie **Installieren aus.**  NuGet lädt Selenium auf Ihren Computer herunter.  
    
    Weitere Informationen zum Selenium.WebDriver NuGet-Paket finden Sie unter [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Verwalten NuGet Pakets" lightbox="../media/webdriver/nuget.png":::
       Verwalten NuGet Pakets  
    :::image-end:::  
    
1.  Verwenden `OpenQA.Selenium.Edge` Sie, indem Sie die folgende Anweisung hinzufügen:  `using OpenQA.Selenium.Edge;` am Anfang der `Program.cs` Datei.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a>Schritt 4: Drive WebView2 with Selenium and Microsoft Edge Driver  

1.  Erstellen Sie zunächst das `EdgeOptions` Objekt, indem Sie den folgenden Codeausschnitt kopieren.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    Das `EdgeOptions` Objekt übernimmt die folgenden beiden Parameter.  
    
    | Parameter | Details |    
    |:--- |:--- |  
    | `is_legacy` | Set to `false` , which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser. |  
    | `"webview2"` | Eine Zeichenfolge, die Selenium anteilt, dass Sie WebView2 fahren. |  
    
1.  Erstellen Sie als Nächstes auf den Dateipfad ihrer WebView2-Projektlaufzeit, erstellen Sie eine Zeichenfolge mit dem Namen, die den Dateipfad an den Ort angibt, an dem Sie Microsoft Edge Driver installiert haben, und erstellen Sie eine Zeichenfolge namens zum Speichern des Namens der `edgeOptions.BinaryLocation` `msedgedriverDir` Microsoft Edge [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Driver-Laufzeit.  Standardmäßig heißt die Laufzeit `msedgedriver.exe` . Verwenden Sie diese beiden Zeichenfolgen, um das `EdgeDriverService` Objekt wie unten dargestellt zu erstellen.  Erstellen Sie schließlich das `EdgeDriver` Objekt mit `EdgeDriverService` und `EdgeOptions` .  
    
    Sie können den folgenden Code unter kopieren und `edgeOptions` einfügen.  Stellen Sie sicher, dass Sie die richtigen Dateipfade zur Projektlaufzeit und die Microsoft Edge Treiberlaufzeit auf Ihrem Computer angeben.  
    
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
    
3.  Ist nun `EdgeDriver` so konfiguriert, dass WebView2 in Ihrem Projekt unterstützt wird.  Wenn Sie beispielsweise das **WebView2API-Beispiel verwenden,** können Sie zu navigieren, `https://microsoft.com` indem Sie den Befehl `e.Url = @"https://www.microsoft.com";` ausführen.  Überprüfen Sie das Selenium-Laufwerk WebView2, indem Sie einen Haltepunkt in der Zeile festlegen und das Projekt ausführen.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selen mit WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selen mit WebView2  
    :::image-end:::
    
Herzlichen Glückwunsch.  Sie haben ein WebView2-Projekt erfolgreich automatisiert und WebView2 mithilfe von Selenium und Microsoft Edge gesteuert.  

## <a name="see-also"></a>Weitere Informationen  

*   Einen umfassenden Überblick darüber, wie die APIs Selenium WebView2 oder Microsoft Edge \(Chromium\) steuert, finden Sie in der Dokumentation zu [WebDriver on Selenium.][SeleniumWebdriver]   
*   Weitere Informationen zum WebView2-Steuerelement und deren Verwendung beim Einbetten von Webinhalten in Ihre systemeigene App finden Sie unter [Einführung in Microsoft Edge WebView2][WebViewIndex].  
*   Weitere Informationen zum Automatisieren von Microsoft Edge \(Chromium\) finden Sie unter Verwenden von [WebDriver (Chromium) für die Testautomatisierung.][WebdriverChromium]   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Verwenden von WebDriver (Chromium) für Testautomatisierungstests | Microsoft Docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Download Microsoft Edge Driver – Verwenden von WebDriver (Chromium) für die Testautomatisierung | Microsoft Docs"  
[WebViewIndex]: ../index.md "Einführung in Microsoft Edge WebView2 – Microsoft Docs"  
[Webview2ReleaseNotes]: ../release-notes.md "Versionshinweise für WebView2 SDK | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Herunterladen von WebDriver | Microsoft Edge Entwickler"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Voraussetzungen – WebView2-API-| GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | NuGet Gallery"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
