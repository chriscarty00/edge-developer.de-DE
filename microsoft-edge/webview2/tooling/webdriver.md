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
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653747"
---
# Automatisieren und Testen von WebView2 mit Microsoft Edge Driver

Da WebView2 die Chrom-Webplattform nutzt, können WebView2-Entwickler standardmäßige Webtools für Debugging und Automatisierung nutzen. Ein solches Tool ist Selen, das die W3C- [WebDriver](https://www.w3.org/TR/webdriver2/) -API implementiert, mit der automatisierte Tests erstellt werden können, mit denen Benutzerinteraktionen simuliert werden.

Dies sind die ersten Schritte:

## Schritt 1: Herunterladen des WebView2API-Beispiels

Wenn Sie nicht über ein vorhandenes WebView2-Projekt verfügen, laden Sie unsere [WebView2API-Beispielanwendung](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample)herunter, ein umfassendes Beispiel für das neueste WebView2-SDK. Bitte überprüfen Sie, ob Sie diese [Voraussetzungen](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites)erfüllt haben.

Nachdem Sie das Repo geklont haben, erstellen Sie das Projekt in Visual Studio. Es sollte wie folgt aussehen:

![Alternativer Text](../media/webdriver/sample-app.png)

## Schritt 2: Installieren des Microsoft Edge-Treibers

Befolgen Sie die Anweisungen zum Installieren des [Microsoft Edge-Treibers](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) mit dem browserspezifischen Treiber, der von Selenium zum Automatisieren und Testen von WebView2 erforderlich ist.

Es ist wichtig, sicherzustellen, dass die Version von Microsoft Edge Driver mit der Version von Microsoft Edge übereinstimmt, die von der Anwendung verwendet wird. Damit das WebView2API-Beispiel funktioniert, stellen Sie sicher, dass Ihre Version von Microsoft Edge größer oder gleich der unterstützten Version unserer neuesten SDK-Version ist, die [in unseren Versions](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes)hinweisen zu finden ist. Wenn Sie wissen möchten, welche Version von Microsoft Edge Sie derzeit haben, laden Sie `edge://settings/help` den Browser.

## Schritt 3: Hinzufügen von Selen zum WebView2API-Beispiel

An diesem Punkt sollten Sie Microsoft Edge installiert haben, ein WebView2-Projekt erstellt und Microsoft Edge-Treiber installiert haben. Nun beginnen wir mit der Verwendung von Selen.

> [!NOTE]
> Selen unterstützt C#, Java, Python, JavaScript und Ruby. Dieses Handbuch befindet sich jedoch in C#.

1. Beginnen Sie mit dem Erstellen eines neuen **C# .NET Framework** -Projekts in **Visual Studio**. Klicken Sie in der unteren rechten Ecke auf **weiter** , um fortzufahren.

![Alternativer Text](../media/webdriver/new-project.png)

2. Geben Sie Ihrem Projekt einen **Namen**, speichern Sie es an Ihrem bevorzugten **Speicherort**, und klicken Sie auf **Erstellen**.

![Alternativer Text](../media/webdriver/app-create.png)

3. Es wird ein neues Projekt erstellt. In diesem Leitfaden wird der gesamte Code in die **Program.cs** -Datei geschrieben.

![Alternativer Text](../media/webdriver/start-app.png)

4. Nun fügen wir **Selen** zum Projekt hinzu. Sie können Selen über das **Selen. WebDriver NuGet-Paket**installieren.

Wenn Sie das **Selen. WebDriver NuGet-Paket**herunterladen möchten, zeigen Sie in **Visual Studio**auf **Project** , und wählen Sie **NuGet-Paket verwalten**aus. Der folgende Bildschirm sollte angezeigt werden:

![Alternativer Text](../media/webdriver/download-nuget.png)

5. Geben Sie **Selen. WebDriver** in der Suchleiste ein, klicken Sie auf **Selen. WebDriver** aus den Ergebnissen, und stellen Sie sicher, dass Sie das Kontrollkästchen neben " **Pre-Release einbeziehen**" markieren. Stellen Sie im rechten Fenster sicher, dass die **Version** für die Installation von **4.0.0-alpha04** oder höher eingestellt ist, und klicken Sie auf **Installieren**. Nuget wird Selen auf Ihren Computer herunterladen.

[Weitere Informationen zum Selen. WebDriver NuGet-Paket.](https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04)

![Alternativer Text](../media/webdriver/nuget.png)

6. Verwenden Sie **OpenQA. Selenium. Edge** , indem Sie die folgende Anweisung hinzufügen: ```using OpenQA.Selenium.Edge;``` am Anfang von **Program.cs**

```csharp
using OpenQA.Selenium.Edge;

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Schritt 4: Laufwerk WebView2 mit Selen und Microsoft EdgeDriver

1. Erstellen Sie zunächst das `EdgeOptions` Objekt, indem Sie den folgenden Code kopieren:

```csharp
static void Main(string[] args)
{
    // EdgeOptions() requires using OpenQA.Selenium.Edge
    // Construct EdgeOptions with is_legacy = false and the string "webview2"
    EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
```

Das `EdgeOptions` Objekt hat zwei Parameter:
\
    **Parameter**
    1. `is_legacy`: auf `false` , der angibt, dass Selen den neuen Chrom basierten Microsoft Edge-Browser steuert.
    2. `"webview2"`: eine Zeichenfolge, die Selen angibt, dass Sie **WebView2** fahren

2. Legen Sie als nächstes `edgeOptions.BinaryLocation` den Dateipfad der ausführbaren Datei Ihres WebView2-Projekts fest, erstellen Sie eine Zeichenfolge namens `msedgedriverDir` , die den Dateipfad zum Speicherort der [Microsoft Edge-Treiber](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads)bereitstellt, und erstellen Sie eine Zeichenfolge, die aufgerufen wird, `msedgedriverExe` um den Namen der ausführbaren Datei des Microsoft Edge-Treibers zu speichern. Standardmäßig wird die ausführbare Datei aufgerufen `"msedgedriver.exe"` . Verwenden Sie diese beiden Zeichenfolgen, um das Objekt zu konstruieren, `EdgeDriverService` wie unten dargestellt. Erstellen Sie schließlich das `EdgeDriver` Objekt mit `EdgeDriverService` und `EdgeOptions` .

Sie können den folgenden Code darunter kopieren und einfügen `edgeOptions` . Stellen Sie sicher, dass Sie die korrekten Dateipfade zur ausführbaren Datei des Projekts und zur ausführbaren Datei des Microsoft Edge-Treibers auf Ihrem Computer angeben.

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

3. **EdgeDriver** ist nun so konfiguriert, dass es die **WebView2** in Ihrem Projekt fährt. Wenn Sie beispielsweise das **WebView2API-Beispiel**verwenden, können Sie durch einen Anruf zu **Navigieren** <https://microsoft.com> ```e.Url = @"https://www.microsoft.com";``` . Sie können **Selenium** Drive **WebView2** beobachten, indem Sie in dieser Zeile einen Haltepunkt festlegen und das Projekt ausführen.

```csharp
    //The following will Navigate the WebView2API Sample from bing.com to microsoft.com
    e.Url = @"https://www.microsoft.com";

    //This exits the edge driver
    e.Quit();
}
```

![Alternativer Text](../media/webdriver/microsoft.png)

Herzlichen Glückwunsch! Sie haben erfolgreich ein WebView2-Projekt und gesteuerte WebView2 mit Selen und Microsoft Edge Driver automatisiert.

## Nächste Schritte

Weitere Informationen finden Sie unter:

- Schauen Sie sich die [Dokumentation zu Selen](https://www.selenium.dev/documentation/en/webdriver/) an, um einen umfassenden Überblick über die APIs zu erhalten, die Selen für das fahren von WebView2 oder Microsoft Edge (Chrom) zur Verfügung hat.
- Weitere Informationen zum [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) -Steuerelement und zur Verwendung beim Einbetten von Webinhalten in Ihre systemeigene App
- Lesen Sie [Dokumentation zu Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) , um mehr über die Automatisierung von Microsoft Edge (Chrom) zu erfahren.

## Kontakt mit dem WebView2-Team  

Helfen Sie uns, ein reicheres WebView2-Erlebnis zu schaffen, indem Sie Ihr Feedback austauschen! Besuchen Sie unser [Feedback-Repo](https://github.com/MicrosoftEdge/WebViewFeedback) , um Funktionsanforderungen oder Fehlerberichte zu übermitteln oder nach bekannten Problemen zu suchen.
