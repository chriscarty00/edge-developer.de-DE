---
description: Erste Schritte mit WebView2 für WPF-Apps
title: Erste Schritte mit WebView2 für WPF-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, Webview2, WebView, Webview, wpf apps, wpf, edge, CoreWebView2, Browsersteuerelement, Edge-HTML, erste Schritte, .NET
ms.openlocfilehash: de67b8a2da8cda0339b5e8d0b96cf4c3df260ec6
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306145"
---
# Erste Schritte mit WebView2 in WPF

In diesem Artikel beginnen Sie mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Wichtigsten Features von [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Weitere Informationen zu einzelnen APIs finden Sie in der [API-Referenz.][DotnetApiMicrosoftWebWebview2Wpf]  

## Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2 Runtime][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen \(derzeit Windows 10, Windows 8.1 und Windows 7\ installiert ist).  
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.  
    
## Schritt 1: Erstellen einer App mit einem Fenster  

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
    
1.  Geben Sie Werte für **den Projektnamen und** den **Speicherort ein.**  Wählen **Sie .NET Framework 4.6.2** oder höher \(oder **.NET Core 3.0** oder höher\) aus.  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Kern erstellen":::
                 Kern erstellen :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Erstellen eines Frameworks":::
                 Erstellen eines Frameworks :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  Um Ihr Projekt zu erstellen, wählen Sie **"Erstellen"** aus.  
    
## Schritt 2: Installieren des WebView2 SDK  

Verwenden Sie NuGet, um dem Projekt das WebView2 SDK hinzuzufügen.  

1.  Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **NuGet-Pakete verwalten...** aus.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet-Pakete verwalten":::
       NuGet-Pakete verwalten
    :::image-end:::
    
1.  Geben Sie in der Suchleiste > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2 aus.**  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Bereit für die Entwicklung von Apps mithilfe der WebView2-API.  Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Das ausgeführte Projekt zeigt ein leeres Fenster an.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Leere App":::
       Leere App
    :::image-end:::  
    
## Schritt 3: Erstellen einer einzelnen WebView in "MainWindow.xaml"  

Fügen Sie als Nächstes Ihrer App eine WebView hinzu.  

1.  Fügen Sie in der Datei die folgende Zeile in das Tag ein, um den `MainWindow.xaml` WebView2-XAML-Namespace `<Window/>` hinzuzufügen.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Stellen Sie sicher, dass der Code `MainWindow.xaml` in wie der folgende Codeausschnitt aussieht.  
    
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
    
1.  Ersetzen Sie zum Hinzufügen des WebView2-Steuerelements die `<Grid>` Tags durch den folgenden Codeausschnitt.  Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5`  "WebView2-Steuerelement anzeigen" [https://www.microsoft.com][|::ref1::|Main] aus.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## Schritt 4: Navigation  

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
    
1.  Fügen Visual Studio Codeausschnitt oben in die Datei ein, um den `MainWindow.xaml.cs` `CoreWebView2` Namespace hinzuzufügen.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  Kopieren Sie in der Datei den folgenden Codeausschnitt, um die Methode zu erstellen, die die WebView zu der in der Adressleiste `MainWindow.xaml.cs` `ButtonGo_Click` eingegebenen URL navigiert.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **"Los" aus.**  Geben Sie beispielsweise `https://www.bing.com` ein.  Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.  
    
    > [!NOTE]
    > Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben wird.  Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://` `https://` beginnt.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       bing.com
    :::image-end:::
    
## Schritt 5: Navigationsereignisse  

Während der Webseitennavigation löst das WebView2-Steuerelement Ereignisse aus.  Die App, die WebView2-Steuerelemente hostet, lauscht auf die folgenden Ereignisse.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Navigieren Sie zu [Navigationsereignissen, um weitere Informationen zu erhalten.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   Navigationsereignisse
:::image-end:::  

Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und sind möglicherweise von der Navigation zu einer Fehlerwebseite abhängig.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.  

Um die Verwendung der Ereignisse zu veranschaulichen, registrieren Sie einen Handler, der alle `NavigationStarting` Nicht-HTTPS-Anforderungen abbricht.  

Ändern Sie in der Datei den Konstruktor so, dass er mit dem `MainWindow.xaml.cs` folgenden Codeausschnitt übereinstimmen kann, und fügen Sie die Funktion `EnsureHttps` hinzu.  

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

Im Konstruktor wird EnsureHttps als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.  

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass die WebView beim Navigieren zu einer HTTP-Website unverändert bleibt.  Die WebView navigiert jedoch zu HTTPS-Websites.  

## Schritt 6: Skripterstellung  

Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.  You may task WebView to run arbitrary JavaScript or add initialization scripts.  Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.  Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes Im HTML-Dokument enthaltenes Skript ausgeführt wird.  

Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.  Ändern Sie die Funktion, um ein Skript in den Webinhalt zu injizieren, `EnsureHttps` der die [ExecuteScriptAsync-Methode](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) verwendet.  

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

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## Schritt 7: Kommunikation zwischen Host- und Webinhalt  

Host- und Webinhalte können wie folgt miteinander `postMessage` kommunizieren:  

*   Webinhalte in einem WebView2-Steuerelement können eine Nachricht mithilfe von . `window.chrome.webview.postMessage`  Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.  
*   Hostet Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .  Diese Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` wurden.  

Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.  

Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, zeigt es die URL in der Adressleiste an und benachrichtigt den Benutzer über die im WebView2-Steuerelement angezeigte URL.  

1.  Aktualisieren Sie in der Datei den Konstruktor, und erstellen Sie eine `MainWindow.xaml.cs` `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.  Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) da die Initialisierung `CoreWebView2` asynchron ist.  
    
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
    
1.  Nachdem **CoreWebView2** initialisiert wurde, registrieren Sie einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.  Aktualisieren `MainWindow.xaml.cs` und hinzufügen Sie in mithilfe des folgenden `InitializeAsync` `UpdateAddressBar` Codeausschnitts.  
    
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
    
1.  Damit webView die Webnachricht senden und darauf antworten kann, wird nach der `CoreWebView2` Initialisierung der Host:  
    1.  Injects a script to the web content that registers a handler to print message from the host.  
    1.  Injects a script to the web content that posts the URL to the host.  
        
    Aktualisieren Sie `MainWindow.xaml.cs` in der Datei so, dass sie mit `InitializeAsync` dem folgenden Codeausschnitt übereinstimmen.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Wählen Sie zum Erstellen und Ausführen der App die Option `F5` aus.  Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.  Wenn Sie erfolgreich zu einem neuen URI navigieren, warnt das WebView2-Steuerelement den Benutzer über den URI, der im WebView2-Steuerelement angezeigt wird.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## Nächste Schritte  

Um weitere Informationen zu WebView2 zu erhalten, navigieren Sie zu den folgenden Ressourcen.  

### Weitere Informationen  

*   Ein umfassendes Beispiel der WebView2-Funktionen finden Sie im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samplesMain] auf GitHub.  
*   Ausführlichere Informationen zur WebView2-API finden Sie in der [API-Referenz.](/dotnet/api/microsoft.web.webview2.wpf.webview2)  
*   Weitere Informationen zu WebView2 finden Sie unter ["WebView2-Ressourcen".](../index.md#next-steps)  

## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Microsoft.Web.WebView2.Wpf Namespace-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "WebView2.EnsureCoreWebView2Async(CoreWebView2Environment)-Methode | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String)-Methode | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples-| GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2-| Microsoft Edge Developer"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer" 