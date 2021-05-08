---
description: Erste Schritte mit WebView2 für WinForms-Apps
title: Erste Schritte mit WebView2 für WinForms-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, Webview, winforms apps, winforms, edge, CoreWebView2, browser control, edge html, get started, Get Started, .NET, windows forms
ms.openlocfilehash: 704e5732ddcff02e56f49bec37a5d1ad5f11c2b5
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536022"
---
# <a name="get-started-with-webview2-in-windows-forms"></a>Erste Schritte mit WebView2 in Windows Forms

Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Weitere Informationen zu einzelnen APIs finden Sie unter [API reference][DotnetApiMicrosoftWebWebview2Winforms].  

## <a name="prerequisites"></a>Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2-Laufzeit][MicrosoftDeveloperMicrosoftEdgeWebview2] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen installiert ist \(derzeit Windows 10, Windows 8.1 und Windows 7\).  
    
    > [!NOTE]
    > Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.  
    
> [!NOTE]
> WebView2 unterstützt derzeit keine .NET 5- und .NET Core-Designer.  

## <a name="step-1---create-a-single-window-app"></a>Schritt 1 : Erstellen einer App mit einem Fenster

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

1.  Wählen Visual Studio Windows **Forms .NET Framework App**  >  **Next aus.**
    
    :::image type="complex" source="./media/winforms-new-project.png" alt-text="Neues Projekt" lightbox="./media/winforms-new-project.png":::
       Neues Projekt  
    :::image-end:::
    
1.  Geben Sie Werte für **Projektname und** **Standort ein.**  Wählen **.NET Framework 4.6.2** oder höher aus.  
    
    :::image type="complex" source="./media/winforms-start-proj.png" alt-text="Projekt starten" lightbox="./media/winforms-start-proj.png":::
       Projekt starten  
    :::image-end:::
    
1.  Wählen Sie Erstellen aus, um Ihr Projekt **zu erstellen.**
    
## <a name="step-2---install-webview2-sdk"></a>Schritt 2 : Installieren des WebView2 SDK

Verwenden Sie NuGet, um das WebView2 SDK zum Projekt hinzuzufügen.  

1.  Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **NuGet-Pakete verwalten...** aus.  
    
    :::image type="complex" source="./media/wpf-getting-started-mng-nuget.png" alt-text="Verwalten von NuGet-Paketen":::
       Verwalten von NuGet-Paketen
    :::image-end:::
    
1.  Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > Wählen Sie **Microsoft.Web.WebView2 aus.**  
    
    :::image type="complex" source="./media/install-nuget.png" alt-text="NuGet" lightbox="./media/install-nuget.png":::
       NuGet  
    :::image-end:::
    
    Beginnen Sie mit der Entwicklung von Apps mithilfe der WebView2-API.  Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.  Das ausgeführte Projekt zeigt ein leeres Fenster an.  
    
    :::image type="complex" source="./media/winforms-empty-app.png" alt-text="Leere App" lightbox="./media/winforms-empty-app.png":::
       Leere App  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a>Schritt 3 : Erstellen einer einzelnen WebView  

Fügen Sie Ihrer App eine WebView hinzu.  

1.  Öffnen Sie **den Windows Forms Designer**.  
1.  Suchen Sie in der **Toolbox**nach **WebView2.**  
    
    > [!NOTE]
    > Wenn Sie Visual Studio 2017 verwenden, wird **WebView2** standardmäßig nicht in der **Toolbox angezeigt.**  Um das Verhalten zu aktivieren, wählen Sie **Tools**  >  **Options**  >  **General** > legen Sie die **Einstellung** Toolbox automatisch auf auf . `True`  
    
    Ziehen Sie das **WebView2-Steuerelement** in die Windows Forms App, und legen Sie es ab.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Toolbox mit WebView2":::
       Toolbox mit WebView2  
    :::image-end:::  
    
1.  Legen Sie die `(Name)`-Eigenschaft auf `webView` fest.
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Eigenschaften des WebView2-Steuerelements":::
       Eigenschaften des WebView2-Steuerelements
    :::image-end:::
    
1.  Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.  Legen Sie die `Source`-Eigenschaft auf `https://www.microsoft.com` fest.  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Die Source-Eigenschaft des WebView2-Steuerelements":::
       Die **Source-Eigenschaft** des WebView2-Steuerelements
    :::image-end:::  

Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.

:::image type="complex" source="./media/winforms-hello-webview.png" alt-text="hello webview" lightbox="./media/winforms-hello-webview.png":::
   hello webview  
:::image-end:::    

> [!NOTE]
> Wenn Sie an einem Monitor mit hohem DPI arbeiten, müssen Sie Ihre [Windows Forms-App][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]möglicherweise für die Unterstützung mit hohem DPI konfigurieren.  

## <a name="step-4---handle-window-resize-events"></a>Schritt 4 – Behandeln von Ereignissen für die Fenstergröße  

Fügen Sie ihren Windows Forms aus der Toolbox ein paar weitere Steuerelemente hinzu, und behandeln Sie die Ereignisse für die Fenstergröße entsprechend.  

1.  Öffnen Sie **im Windows Forms Designer**die **Toolbox**.  
1.  Ziehen und ablegen Sie **ein TextBox-Objekt** in die Windows Forms App.  Benennen Sie **das TextBox-Postfach** `addressBar` auf der Registerkarte **Eigenschaften**.  
1.  Ziehen und Ablegen einer **Schaltfläche** in die Windows Forms App.  Ändern Sie den Text in **der Schaltfläche** in und nennen Sie `Go!` die **Schaltfläche** auf der `goButton` Registerkarte **Eigenschaften**.  
    
    Die App sollte wie das folgende Bild im Designer aussehen.  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="WinForms-Designer" lightbox="./media/winforms-designer.png":::
       WinForms-Designer  
    :::image-end:::  

1.  Definieren Sie in der Datei, dass die Steuerelemente bei der Größenänderung des `Form1.cs` `Form_Resize` App-Fensters an Ort und Stelle bleiben.
    
```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```  

Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass die App ähnlich dem folgenden Screenshot angezeigt wird.

:::image type="complex" source="./media/winforms-app.png" alt-text="App" lightbox="./media/winforms-app.png":::
   App  
:::image-end:::  

## <a name="step-5---navigation"></a>Schritt 5 – Navigation

Fügen Sie die Möglichkeit hinzu, Benutzern das Ändern der URL zu ermöglichen, die das WebView2-Steuerelement anzeigt, indem Sie der App eine Adressleiste hinzufügen.  

1.  Wählen `F5` Sie aus, um Ihr Projekt zu erstellen und ausführen.  Vergewissern Sie sich, dass die App ähnlich dem folgenden Screenshot angezeigt wird.  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="WinForms App" lightbox="./media/winforms-app.png":::
       WinForms App  
    :::image-end:::  
    
1.  Fügen Sie in der Datei den folgenden Codeausschnitt oben ein, um den `Form1.cs` `CoreWebView2` Namespace hinzuzufügen.  
1.  Fügen `Form1.cs` Sie den `CoreWebView2` Namespace hinzu, indem Sie den folgenden Codeausschnitt oben in `Form1.cs` einfügen.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  **Doppelklicken Sie im Windows Forms Designer**auf die `Go!` Schaltfläche, um die Methode in der Datei `goButton_Click` zu `Form1.cs` erstellen.  Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die Funktion ein.  Nun navigiert `goButton_Click` die Funktion in der WebView zu der URL, die in der Adressleiste eingegeben wurde.
    
    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **Los**aus.  Geben Sie z. B. `https://www.bing.com` ein.  Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.  

> [!NOTE]
> Stellen Sie sicher, dass eine vollständige URL in der Adressleiste eingegeben wird.  Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://` `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::  

## <a name="step-6---navigation-events"></a>Schritt 6 – Navigationsereignisse  

Während der Webseitennavigation löst das WebView2-Steuerelement Ereignisse aus.  Die App, die WebView2-Steuerelemente hostet, lauscht auf die folgenden Ereignisse.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
Weitere Informationen finden Sie unter [Navigationsereignisse][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   Navigationsereignisse
:::image-end:::

Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und hängen möglicherweise von der Navigation zu einer Fehlerwebseite ab.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
> [!NOTE]
> Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.  

Um die Verwendung der Ereignisse zu veranschaulichen, registrieren Sie zunächst einen Handler, der alle Anforderungen abbricht, die https `NavigationStarting` nicht verwenden.  

Aktualisieren Sie `Form1.cs` in der Datei den Konstruktor, um dem folgenden Codeausschnitt zu entsprechen, und fügen Sie die Funktion `EnsureHttps` hinzu.  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```  

Wird im `EnsureHttps` Konstruktor als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.  

Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass beim Navigieren zu einer HTTP-Website die WebView unverändert bleibt.  Die WebView navigiert jedoch zu HTTPS-Websites.

## <a name="step-7---scripting"></a>Schritt 7 – Skripterstellung  

Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.  Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.  Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.  Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.  
    
Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.  Ändern Sie `EnsureHttps` die Funktion, um ein Skript in den Webinhalt zu injizieren, der [die ExecuteScriptAsync-Methode][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] verwendet.  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   https  
:::image-end:::  

## <a name="step-8---communication-between-host-and-web-content"></a>Schritt 8 – Kommunikation zwischen Host- und Webinhalten  

Host- und Webinhalte können für die `postMessage` Kommunikation miteinander wie folgt verwendet werden:  

*   Webinhalte in einem WebView2-Steuerelement können verwendet werden, um eine `window.chrome.webview.postMessage` Nachricht an den Host zu posten.  Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.  
*   Hosts posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .  Diese Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` werden.  
    
Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.  

Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt und der Benutzer über die im WebView2-Steuerelement angezeigte URL benachrichtigt.  

1.  Aktualisieren Sie `Form1.cs` in der Datei den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.  Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] da die Initialisierung `CoreWebView2` von asynchron ist.  
    
    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  Registrieren `CoreWebView2` Sie nach der Initialisierung einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.  Aktualisieren `Form1.cs` und hinzufügen Sie `InitializeAsync` in der Datei mithilfe des folgenden `UpdateAddressBar` Codeausschnitts.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }

    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  
    
1.  Damit webView die Webnachricht sendet und darauf antwortet, wird nach der Initialisierung ein Skript in den `CoreWebView2` Webinhalt eingesenkt:  
    1.  Senden Sie die URL mithilfe von an den `postMessage` Host.
    1.  Registrieren Sie einen Ereignishandler, um eine vom Host gesendete Nachricht zu drucken.  
        
Aktualisieren Sie `Form1.cs` in der Datei `InitializeAsync` so, dass sie mit dem folgenden Codeausschnitt übereinstimmen.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Wählen Sie zum Erstellen und Ausführen der App `F5` aus.  Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.  Wenn Sie außerdem erfolgreich zu einer neuen URL navigieren, benachrichtigt webView den Benutzer über die url, die in der WebView angezeigt wird.  

:::image type="complex" source="./media/winforms-final-app.png" alt-text="Letzte App" lightbox="./media/winforms-final-app.png":::
   Letzte App  
:::image-end:::  

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## <a name="next-steps"></a>Nächste Schritte  

Navigieren Sie zu den folgenden Ressourcen, um weitere Informationen zu WebView2 zu erhalten.  

*   Weitere Informationen zum Erstellen von WebView2-Anwendungen finden Sie unter Bewährte Methoden für [die WebView2-Entwicklung.][WV2BestPractices]  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].  
*   Ausführliche Informationen zur WebView2-API finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WinformsWebview2].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Bewährte Methoden für die WebView2-| Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Namespace | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "WebView2-Klasse | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) Method | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Konfigurieren Ihrer Windows Forms-App für hohe DPI-Unterstützung – Unterstützung mit hohem DPI in Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2-| Microsoft Edge Developer"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
