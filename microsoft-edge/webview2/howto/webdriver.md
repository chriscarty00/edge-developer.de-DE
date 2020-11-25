---
description: Automatisieren und Testen des WebView2-Steuerelements mit Microsoft Edge Driver
title: Automatisieren und Testen von WebView2 mit Microsoft Edge Driver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: 6f7f84fa88a57e54d7b5143a489d1138c7426d88
ms.sourcegitcommit: 652c345b46aae8b7e3723eb55a01b71a4ef76bf0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191450"
---
# Automatisieren und Testen von WebView2 mit Microsoft Edge Driver  

Da WebView2 die Microsoft Edge \ (Chromium \)-Webplattform verwendet, können WebView2-Entwickler \ (You \) standardmäßige Webtools für Debuggen und Automatisierung nutzen.  Selen ist ein solches Tool.  Sie implementiert die W3C- [WebDriver][W3cWebdriver2] -API.  Sie können Selen verwenden, um automatisierte Tests zum Simulieren von Benutzerinteraktionen zu erstellen.  

Beginnen Sie mit den folgenden Schritten.  

## Schritt 1: Herunterladen des WebView2API-Beispiels  

Wenn Sie nicht über ein vorhandenes WebView2-Projekt verfügen, laden Sie die [WebView2API-Beispiel-App][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]herunter, ein umfassendes Beispiel für das neueste WebView2-SDK.  Stellen Sie sicher, dass Sie die [Voraussetzungen für die WebView2API-Beispiel-App][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]erfüllt haben. 

Nachdem Sie das Repo geklont haben, erstellen Sie das Projekt in Visual Studio.  Es sollte wie in der folgenden Abbildung aussehen.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="WebView2API-Beispiel-App" lightbox="../media/webdriver/sample-app.png":::
   WebView2API-Beispiel-App  
:::image-end:::  

## Schritt 2: Installieren des Microsoft Edge-Treibers  

Befolgen Sie die Anweisungen zum Installieren des [Microsoft Edge-Treibers][WebdriverChromiumDownloadMicrosoftEdgeDriver] mit dem browserspezifischen Treiber, der von Selenium zum Automatisieren und Testen von WebView2 erforderlich ist.  

Stellen Sie sicher, dass die Version von Microsoft Edge Driver mit der Version der WebView2-Runtime übereinstimmt, die von der APP verwendet wird.  Damit das WebView2API-Beispiel funktioniert, stellen Sie sicher, dass Ihre Version der WebView2-Laufzeit größer oder gleich der unterstützten Version der neuesten WebView2 SDK-Version ist.  Navigieren Sie zu [WebView2][Webview2Releasenotes], um die neueste Version von WebView2 SDK zu finden.  Wenn Sie feststellen möchten, welche Version der WebView2-Laufzeit Sie zurzeit haben, navigieren Sie zu `edge://settings/help` .  

## Schritt 3: Hinzufügen von Selen zum WebView2API-Beispiel  

An diesem Punkt sollten Sie die WebView2-Runtime installiert haben, ein WebView2-Projekt erstellt und Microsoft Edge-Treiber installiert haben.  Beginnen Sie mit der Verwendung von Selen.  

> [!NOTE]
> Selen unterstützt C \ #, Java, Python, JavaScript und Ruby.  Das folgende Handbuch wird jedoch mit C \ # geschrieben.  

1.  Beginnen Sie mit dem Erstellen eines neuen **C# .NET Framework** -Projekts in **Visual Studio**.  Klicken Sie in der unteren rechten Ecke auf **weiter** , um fortzufahren.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Erstellen eines neuen Projekts" lightbox="../media/webdriver/new-project.png":::
       Erstellen eines neuen Projekts  
    :::image-end:::  
    
1.  Geben Sie Ihrem Projekt einen **Namen**, speichern Sie es an Ihrem bevorzugten **Speicherort**, und wählen Sie **Erstellen**aus.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Konfigurieren des neuen Projekts" lightbox="../media/webdriver/app-create.png":::
       Konfigurieren des neuen Projekts  
    :::image-end:::  
    
1.  Ein neues Projekt wird erstellt.  In diesem Leitfaden wird der gesamte Code in die `Program.cs` Datei geschrieben.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Neues Projekt" lightbox="../media/webdriver/start-app.png":::
       Neues Projekt  
    :::image-end:::  
    
1.  Fügen Sie dem Projekt nun **Selen** hinzu.  Installieren Sie Selen mithilfe des **Selen. WebDriver NuGet-Pakets**.  
    
    Wenn Sie das **Selen. WebDriver NuGet-Paket**herunterladen möchten, zeigen Sie in **Visual Studio**auf **Project**, und wählen Sie **NuGet-Paket verwalten**aus.  Der folgende Bildschirm sollte angezeigt werden.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="NuGet-Paket herunterladen" lightbox="../media/webdriver/download-nuget.png":::
       NuGet-Paket herunterladen  
    :::image-end:::  
    
1.  Geben Sie **Selen. WebDriver** in der Suchleiste ein, wählen Sie aus den Ergebnissen **Selen. WebDriver** aus, und stellen Sie sicher, dass Sie das Kontrollkästchen neben " **Pre-Release einbeziehen**" markieren. Stellen Sie im rechten Fenster sicher, dass die **Version** für die Installation von **4.0.0-alpha04** oder höher eingestellt ist, und wählen Sie **Installieren**aus.  Nuget downloadet Selen auf Ihren Computer.  
    
    Wenn Sie mehr über das Selen. WebDriver NuGet-Paket erfahren möchten, navigieren Sie zu [Selen. WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Verwalten des NuGet-Pakets" lightbox="../media/webdriver/nuget.png":::
       Verwalten des NuGet-Pakets  
    :::image-end:::  
    
1.  Verwenden Sie `OpenQA.Selenium.Edge` Diese Anweisung, indem Sie die folgende Anweisung  `using OpenQA.Selenium.Edge;` am Anfang der Datei hinzufügen `Program.cs` .  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## Schritt 4: Laufwerk WebView2 mit Selen und Microsoft Edge-Treiber  

1.  Erstellen Sie zunächst das `EdgeOptions` Objekt, indem Sie den folgenden Codeausschnitt kopieren.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    Das `EdgeOptions` Objekt akzeptiert die folgenden beiden Parameter.  
    
    | Parameter | Details |    
    |:--- |:--- |  
    | `is_legacy` | "Auf `false` " festzulegen, wodurch Selen mitgeteilt wird, dass Sie den neuen Chrom basierten Microsoft Edge-Browser antreiben. |  
    | `"webview2"` | Eine Zeichenfolge, die Selen anweist, dass Sie WebView2 fahren. |  
    
1.  Legen Sie als nächstes `edgeOptions.BinaryLocation` den Dateipfad der WebView2-Projektlaufzeit fest, erstellen Sie eine Zeichenfolge mit dem Namen `msedgedriverDir` , die den Dateipfad zum Speicherort des [Microsoft Edge-Treibers][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]enthält, und erstellen Sie eine Zeichenfolge, `msedgedriverExe` die den Namen der Microsoft Edge Driver-Laufzeit speichert.  Standardmäßig wird die Common Language Runtime benannt `msedgedriver.exe` . Verwenden Sie diese beiden Zeichenfolgen, um das Objekt zu konstruieren, `EdgeDriverService` wie unten dargestellt.  Erstellen Sie schließlich das `EdgeDriver` Objekt mit `EdgeDriverService` und `EdgeOptions` .  
    
    Sie können den folgenden Code darunter kopieren und einfügen `edgeOptions` .  Stellen Sie sicher, dass Sie die richtigen Dateipfade für Ihre Projektlaufzeit und die Microsoft Edge Driver-Laufzeit auf Ihrem Computer angeben.  
    
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
    
3.  Jetzt `EdgeDriver` ist die Konfiguration für das Laufwerk des WebView2 in Ihrem Projekt konfiguriert.  Wenn Sie beispielsweise das **WebView2API-Beispiel**verwenden, können Sie zu navigieren, `https://microsoft.com` indem Sie den `e.Url = @"https://www.microsoft.com";` Befehl ausführen.  Überprüfen Sie das Selen Drive-WebView2, indem Sie einen Haltepunkt in der Zeile festlegen und das Projekt ausführen.  
    
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

Herzlichen Glückwunsch.  Sie haben erfolgreich ein WebView2-Projekt und gesteuerte WebView2 mit Selen und Microsoft Edge Driver automatisiert.  

## Weitere Informationen  

*   Einen umfassenden Überblick darüber, wie die APIs Selenium WebView2 oder Microsoft Edge \ (Chrom \) steuert, navigieren Sie zu [WebDriver auf der Selenium-Dokumentation][SeleniumWebdriver] .   
*   Wenn Sie mehr über das WebView2-Steuerelement und seine Verwendung beim Einbetten von Webinhalten in Ihre systemeigene App erfahren möchten, navigieren Sie zu [Introduction to Microsoft Edge WebView2][WebViewIndex].  
*   Weitere Informationen zum Automatisieren von Microsoft Edge \ (Chrom \) finden Sie unter [Verwenden von WebDriver (Chrom) für die Testautomatisierung][WebdriverChromium] .   
    
## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium.md "Verwenden von WebDriver (Chrom) für die Testautomatisierung | Microsoft docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium.md#download-microsoft-edge-driver "Microsoft Edge Driver herunterladen – verwenden Sie WebDriver (Chrom) für die Testautomatisierung | Microsoft docs"  
[WebViewIndex]: ../index.md "Einführung in Microsoft Edge WebView2 – Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "WebDriver herunterladen | Microsoft Edge-Entwickler"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "WebView2-API-Beispiel-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Voraussetzungen – Beispiel für die WebView2-API | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selen. WebDriver 4.0.0-alpha04 | NuGet-Katalog"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selen"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  
