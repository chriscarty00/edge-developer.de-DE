---
description: Erste Schritte mit WebView2 für WPF-Apps
title: Erste Schritte mit WebView2 für WPF-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, Webview, wpf apps, wpf, edge, CoreWebView2, browser control, edge html, getting started, Getting Started, .NET
ms.openlocfilehash: 1ced88ebd80d663ac2bd25840174d8505729bf32
ms.sourcegitcommit: b51df5036642060525e03cd744b7d35726326abe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526080"
---
# <a name="getting-started-with-webview2-in-wpf"></a>Erste Schritte mit WebView2 in WPF

Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Weitere Informationen zu einzelnen APIs finden Sie unter [API reference][DotnetApiMicrosoftWebWebview2Wpf].  

## <a name="prerequisites"></a>Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2-Laufzeit][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen installiert ist \(derzeit Windows 10, Windows 8.1 und Windows 7\).  
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.  
    
## <a name="step-1---create-a-single-window-app"></a>Schritt 1 : Erstellen einer App mit einem Fenster  

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

1.  Wählen Visual Studio **WPF .NET Core App** \(oder **WPF .NET Framework App**\) > Weiter **aus.**  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF Core":::
             WPF Core :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF Framework":::
             WPF Framework :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Geben Sie Werte für **Projektname und** **Standort ein.**  Wählen **.NET Framework 4.6.2** oder höher \(oder **.NET Core 3.0** oder höher\) aus.  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Erstellen eines Kerns":::
                 Erstellen eines Kerns :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Create Framework":::
                 Create Framework :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  Wählen Sie Erstellen aus, um Ihr Projekt **zu erstellen.**  
    
## <a name="step-2---install-webview2-sdk"></a>Schritt 2 : Installieren des WebView2 SDK  

Verwenden Sie NuGet, um das WebView2 SDK zum Projekt hinzuzufügen.  

1.  Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **NuGet-Pakete verwalten...** aus.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet-Pakete verwalten":::
       NuGet-Pakete verwalten
    :::image-end:::
    
1.  Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > Wählen Sie **Microsoft.Web.WebView2 aus.**  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Bereit zum Entwickeln von Apps mithilfe der WebView2-API.  Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.  Das ausgeführte Projekt zeigt ein leeres Fenster an.  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Leere App" lightbox="./media/winforms-emptyapp.png":::
       Leere App  
    :::image-end:::  
    
## <a name="step-3---create-a-single-webview"></a>Schritt 3 : Erstellen einer einzelnen WebView 

Fügen Sie als Nächstes Ihrer App eine WebView hinzu.  

1.  Fügen Sie in der Datei die folgende Zeile in das Tag ein, um den `MainWindow.xaml` WebView2-XAML-Namespace `<Window/>` hinzuzufügen.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Stellen Sie sicher, dass der Code in `MainWindow.xaml` wie der folgende Codeausschnitt aussieht.  
    
    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
    >
        <Grid>
        
        </Grid>
    </Window>
    ```  
    
1.  Zum Hinzufügen des WebView2-Steuerelements ersetzen Sie die `<Grid>` Tags durch den folgenden Codeausschnitt.  Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Zum Erstellen und Ausführen des Projekts wählen Sie `F5`  Sicherstellen, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## <a name="step-4---navigation"></a>Schritt 4 – Navigation  

Fügen Sie die Möglichkeit hinzu, Benutzern das Ändern der URL zu ermöglichen, die das WebView2-Steuerelement anzeigt, indem Sie der App eine Adressleiste hinzufügen.

1.  Fügen Sie in der Datei eine Adressleiste hinzu, indem Sie den folgenden Codeausschnitt in den Codeausschnitt kopieren und einfügen, der `MainWindow.xaml` `<DockPanel>` die WebView enthält.  
    
    ```xml
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo"
                DockPanel.Dock="Right"
                Click="ButtonGo_Click"
                Content="Go"
        />
        <TextBox Name="addressBar"/>
    </DockPanel>
    ```  
    
    Stellen Sie `<DockPanel>` sicher, dass der Abschnitt `MainWindow.xaml` der Datei mit dem folgenden Codeausschnitt entspricht.  
    
    ```xml
    <DockPanel>
        <DockPanel DockPanel.Dock="Top">
            <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
            <TextBox Name = "addressBar"/>
        </DockPanel>
        <wv2:WebView2 Name = "webView"
                      Source = "https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Fügen Visual Studio in der Datei den folgenden Codeausschnitt oben ein, um den `MainWindow.xaml.cs` `CoreWebView2` Namespace hinzuzufügen.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  Kopieren Sie in der Datei den folgenden Codeausschnitt, um die Methode zu erstellen, die im WebView zu der URL navigiert, die in der `MainWindow.xaml.cs` `ButtonGo_Click` Adressleiste eingegeben wurde.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **Los**aus.  Geben Sie beispielsweise `https://www.bing.com` ein.  Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.  
    
    > [!NOTE]
    > Stellen Sie sicher, dass eine vollständige URL in der Adressleiste eingegeben wird.  Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://` `https://` beginnt.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       bing.com
    :::image-end:::
    
## <a name="step-5---navigation-events"></a>Schritt 5 – Navigationsereignisse  

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

Um die Verwendung der Ereignisse zu veranschaulichen, registrieren Sie einen Handler, `NavigationStarting` der alle Nicht-HTTPS-Anforderungen abbricht.  

Ändern Sie `MainWindow.xaml.cs` in der Datei den Konstruktor, um dem folgenden Codeausschnitt zu entsprechen, und fügen Sie die Funktion `EnsureHttps` hinzu.  

```csharp
public MainWindow()
{
    InitializeComponent();
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

Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass beim Navigieren zu einer HTTP-Website die WebView unverändert bleibt.  Die WebView navigiert jedoch zu HTTPS-Websites.  

## <a name="step-6---scripting"></a>Schritt 6 – Skripterstellung  

Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.  Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.  Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.  Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.  

Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.  Ändern Sie `EnsureHttps` die Funktion, um ein Skript in den Webinhalt zu injizieren, der [die ExecuteScriptAsync-Methode](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) verwendet.  

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

Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## <a name="step-7---communication-between-host-and-web-content"></a>Schritt 7 – Kommunikation zwischen Host- und Webinhalten  

Host- und Webinhalte können auf folgende Weise mithilfe von `postMessage` kommunizieren.  

*   Webinhalte in einem WebView2-Steuerelement können eine Nachricht mithilfe von an den Host `window.chrome.webview.postMessage` senden.  Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.  
*   Hosts posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .  Die Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` werden.  

Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.  

Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt und der Benutzer über die im WebView2-Steuerelement angezeigte URL benachrichtigt.  

1.  Aktualisieren Sie `MainWindow.xaml.cs` in der Datei den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.  Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) da die Initialisierung `CoreWebView2` von asynchron ist.  
    
    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }
    
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  Registrieren Sie nach der Initialisierung von **CoreWebView2** einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.  Aktualisieren `MainWindow.xaml.cs` und hinzufügen Sie in mithilfe des folgenden `InitializeAsync` `UpdateAddressBar` Codeausschnitts.  
    
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
    
1.  Damit webView die Webnachricht sendet und auf sie antwortet, wird der Host nach der `CoreWebView2` Initialisierung:  
    1.  Injects a script to the web content that registers a handler to print message from the host.  
    1.  Injects a script to the web content that posts the URL to the host.  
        
    Aktualisieren Sie `MainWindow.xaml.cs` in der Datei `InitializeAsync` so, dass sie mit dem folgenden Codeausschnitt übereinstimmen.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Wählen Sie zum Erstellen und Ausführen der App `F5` aus.  Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.  Wenn Sie erfolgreich zu einem neuen URI navigieren, benachrichtigt das WebView2-Steuerelement den Benutzer über den URI, der im WebView2-Steuerelement angezeigt wird.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## <a name="next-steps"></a>Nächste Schritte  

Navigieren Sie zu den folgenden Ressourcen, um weitere Informationen zu WebView2 zu erhalten.  

*   Weitere Informationen zum Erstellen von WebView2-Anwendungen finden Sie unter Bewährte Methoden für [die WebView2-Entwicklung.][WV2BestPractices]  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samplesMain] auf GitHub.  
*   Weitere Informationen zur WebView2-API finden Sie unter [API-Referenz](/dotnet/api/microsoft.web.webview2.wpf.webview2).  
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources](../index.md#next-steps).  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[WV2BestPractices]: ../concepts/developer-guide.md "Bewährte Methoden für die WebView2-| Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft.Web.WebView2.Wpf Namespace | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-Klasse | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) Method | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2-| Microsoft Edge Developer"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer" 
