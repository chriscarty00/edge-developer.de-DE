---
description: Leitfaden für erste Schritte mit WebView2 für WinUI-Apps
title: Erste Schritte mit WebView2 für WinUI-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, Webview2, WebView, Webview, Winui-Apps, Winui, Edge, CoreWebView2, Browsersteuerelement, Edge-HTML, erste Schritte, .NET
ms.openlocfilehash: 5188a735eaf635c3b3bc0eead6f4ee4f3a83f1c4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306152"
---
# Erste Schritte mit WebView2 in WinUI 3 (Vorschau)  

In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-App erstellen, und erfahren Sie mehr über die Wichtigsten Features [von WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Ihre erste WebView2-App verwendet WinUI3.  Weitere Informationen zu einzelnen APIs finden Sie in der [API-Referenz.][GithubMicrosoftUiXamlSpecsWebview2]  

## Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2 Runtime][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter Windows 10, Version 1803 \(Build 17134\) oder höher installiert ist.  Weitere Informationen zu Windows 10 finden Sie unter [Windows Update: Häufig][MicrosoftSupport12373]gestellte Fragen .  
    
    > [!NOTE]
    > Das WebView-Team empfiehlt die Verwendung des Canarykanals, und die mindestens erforderliche Version ist 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2019, Version 16.9 Preview.  Weitere Informationen finden Sie unter [Windows UI Library 3 Preview 3.][WindowsAppsWinui3ConfigureYourDevEnvironment]  
    
    *   Schließen Sie die folgenden Workloads ein, wenn Sie Visual Studio.  
        *   .NET Desktop Development \(Das Installationsprogramm installiert auch .NET 5\)  
        *   Entwicklung der universellen Windows-Plattform  
    *   Um C++-Apps zu erstellen, müssen Sie auch die folgenden Workloads hinzufügen.  
        *   Desktopentwicklung mit C++  
        *   Die optionale Komponente "C++ \(v142\) Universal Windows Platform" für die Arbeitsauslastung der universellen Windows-Plattform.  Weitere Informationen finden **** Sie im Abschnitt zur Entwicklung der universellen **Windows-Plattform** im rechten Bereich.  
        
## Schritt 0: Visual Studio Einstellungen  

1.  Stellen Sie sicher, dass auf Ihrem System eine NuGet-Paketquelle für [die][NugetHome]nuget.org.  Weitere Informationen finden Sie unter ["Allgemeine NuGet-Konfigurationen"][NugetConsumePackagesConfiguringNugetBehavior] und ["Windows Community Toolkit".][WindowsCommunitytoolkit]  
1.  Laden Sie das [WinUI 3 Preview 3 -VSIX-Paket herunter, und installieren Sie es.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]  Das Installationsprogramm fügt die WinUI 3-Projektvorlagen und das NuGet-Paket, das die WinUI 3-Bibliotheken enthält, zu Visual Studio 2019 hinzu.  
    
    Anweisungen zum Hinzufügen des Pakets zu Visual Studio finden Sie unter "Suchen und Verwenden von `VSIX` [Visual Studio Extensions".][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]
    
1.  Um auf alle entwicklerspezifischen Features Visual Studio, aktivieren Sie den [Entwicklermodus.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]  
    
## Schritt 1: Projekt erstellen  

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

1.  Wählen Visual Studio In diesem Fenster **"Neues Projekt erstellen" aus.**  
1.  Wählen Sie in der #A0 **C#**, **Windows**und **WinUI** aus.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Erstellen Sie ein neues WinUI-Projekt mithilfe Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Erstellen Sie ein neues WinUI-Projekt mithilfe Visual Studio
    :::image-end:::  
    
1.  Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.  
1.  Geben Sie einen Projektnamen ein.
1.  Wählen Sie nach Bedarf Optionen aus.  
1.  Wählen Sie **Erstellen** aus.  
1.  Wählen **Sie in "Neues Projekt für die universelle Windows-Plattform"** die folgenden Werte aus, und wählen Sie dann **"OK" aus.**  
    *   **Zielversion:**  **Windows 10, Version 1903 (Build 18362)** oder höher  
    *   **Mindestversion:**  **Windows 10, Version 1803 (Build 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Das Dialogfeld "Neues Projekt für die universelle Windows-Plattform" mit den ausgewählten Werten für die Zielversion und die Mindestversion." lightbox="./media/winui-gettingstarted-projecttype.png":::
       Das Dialogfeld "Neues Projekt für die universelle Windows-Plattform" mit ausgewählten Werten für die Zielversion und die Mindestversion.
    :::image-end:::  
    
1.  Im Projektmappen-Explorer werden zwei Projekte generiert.  
    *   **Ihr Projektname (Desktop)**.  Das Desktopprojekt enthält den Code für Ihre App.  Die `App.xaml.cs` Datei definiert eine `Application` Klasse, die Ihre App-Instanz darstellt.  Die `MainWindow.xaml.cs` Datei definiert eine `MainWindow` Klasse, die das Hauptfenster darstellt, das von Ihrer App-Instanz angezeigt wird.  Die Klassen werden von Typen im `Microsoft.UI.Xaml` Namespace von WinUI ab.  
    *   **Ihr Projektname (Paket)**.  Das Paketprojekt ist ein Projekt zum Packen von Windows-Anwendungen, das so konfiguriert ist, dass die App in ein MSIX-Paket für die Bereitstellung verpackt wird.  Das Projekt enthält das Paketmanifest für Ihre App und ist standardmäßig das Startprojekt für Ihre Lösung.  Weitere Informationen finden Sie unter "Einrichten Der Desktopanwendung für das Packen von [MSIX in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] und der Schemareferenz für das Paketmanifest [für Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]  
1.  Öffnen Sie die Datei im Projektmappen-Explorer, um den Code anzeigen zu `MainWindow.xaml` können.  Wählen Sie zum Ausführen des Projekts und Anzeigen eines Fensters mit einer Schaltfläche die Option `F5` aus.  
    
## Schritt 2: Hinzufügen eines WebView2-Steuerelements zu Ihrem Projekt  

Fügen Sie Ihrem Projekt ein WebView2-Steuerelement hinzu.  

1.  Fügen Sie in der Datei die folgende Zeile in das Tag ein, um den `MainWindow.xaml` WebView2-XAML-Namespace `<Window/>` hinzuzufügen.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Stellen Sie sicher, dass `MainWindow.xaml` ihr Code dem folgenden Codeausschnitt ähnelt.  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  Ersetzen Sie zum Hinzufügen des WebView2-Steuerelements die `<StackPanel>` Tags durch den folgenden Codeausschnitt.  Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Kommentieren Sie `MainWindow.xaml.cs` in der Datei die folgende Zeile aus.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="WebView2-Steuerelement zeigt microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       WebView2-Steuerelement zeigt microsoft.com  
    :::image-end:::  
    
## Schritt 3: Hinzufügen von Navigationssteuerelementen  

Damit Benutzer die Webseite steuern können, die in Ihrem WebView2-Steuerelement angezeigt wird, fügen Sie Ihrer App eine Adressleiste hinzu.  

1.  Kopieren Sie in der Datei den folgenden Codeausschnitt, und fügen Sie ihn in das `MainWindow.xaml` `<Grid>` Element ein, das das Element `WebView2` enthält.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Stellen Sie `<Grid>` sicher, dass das Element in `MainWindow.xaml` der Datei dem folgenden Codeausschnitt ähnelt.  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Kopieren Sie in der Datei den folgenden Codeausschnitt in das WebView2-Steuerelement, das zu der in der Adressleiste `MainWindow.xaml.cs` `myButton_Click` eingegebenen URL navigiert.  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie dann **"Los" aus.**  Geben Sie z. `https://www.bing.com` B. .  
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie vollständige URLs in die Adressleiste eingeben.  `ArgumentException` Ausnahmen werden ausgelöst, wenn die URL nicht mit oder `http://` `https://` beginnt.  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       bing.com  
    :::image-end:::  
    
## Schritt 4: Navigationsereignisse  

Apps, die WebView2-Steuerelemente hosten, lauschen auf die folgenden Ereignisse, die von WebView2-Steuerelementen während der Webseitennavigation ausgelöst werden.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Wenn eine HTTP-Umleitung stattfindet, gibt es `NavigationStarting` mehrere Ereignisse in einer Zeile.  

Navigieren Sie zu [Navigationsereignissen, um weitere Informationen zu erhalten.][Webviews2ConceptsNavigationEvents]  

Wenn Fehler auftreten, werden die folgenden Ereignisse ausgelöst und können zu einer Fehlerwebseite navigieren.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Registrieren Sie als Beispiel für die Verwendung der Ereignisse einen Handler, der alle `NavigationStarting` Nicht-HTTPS-Anforderungen abbricht.  Ändern `MainWindow.xaml.cs` Sie in den Konstruktor, um ihn zu registrieren, und fügen Sie die Funktion so hinzu, dass sie dem folgenden `EnsureHttps` `EnsureHttps` Codeausschnitt entspricht.  

```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass die Navigation zu den HTTP-Websites blockiert ist und für HTTPS-Websites zulässig ist.  

## Schritt 5: Skripterstellung  

Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.  You may task WebView to run arbitrary JavaScript or add initialization scripts.  Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.  Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes Im HTML-Dokument enthaltenes Skript ausgeführt wird.  

Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.  Ändern Sie die Funktion, um ein Skript in den Webinhalt zu injizieren, `EnsureHttps` der [ExecuteScriptAsync verwendet.][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.  Stellen Sie sicher, dass Ihre App eine Warnung anzeigt, wenn Sie zu nicht-HTTPS-Websites navigieren.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="WebView2-Steuerelement zeigt ein Warnungsdialogfeld an" lightbox="./media/winui-gettingstarted-script.png":::
   WebView2-Steuerelement zeigt ein Warnungsdialogfeld an
:::image-end:::  

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## Nächste Schritte  

Um weitere Informationen zu WebView2 zu erhalten, navigieren Sie zu den folgenden Ressourcen.  

### Weitere Informationen  

*   Ein umfassendes Beispiel der WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Weitere Informationen zu WebView2 finden Sie unter ["WebView2-Ressourcen".][Webview2IndexNextSteps]  
    
    > [!NOTE]
    > Das WinRT CoreWebView2 -Objekt ist mit der Veröffentlichung der WebView2-API möglicherweise nicht verfügbar.  Um zu verstehen, welche APIs für WebView2-Steuerelemente verfügbar sind, navigieren Sie zu [WebView2 Spec,][GithubMicrosoftUiXamlSpecsWebview2] um eine Liste der verfügbaren APIs zu finden.  
    
*   Ausführliche Informationen zur WebView2-API finden Sie in der [WebView2-Spezifikation.][GithubMicrosoftUiXamlSpecsWebview2]  
    
## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String)-Methode (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Allgemeine | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Paketmanifestschemareferenz für Windows 10-| Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installation ohne Verwendung des Dialogfelds "Erweiterungen verwalten" – Verwalten von Erweiterungen für Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Konfigurieren Der Entwicklungsumgebung – Windows UI Library 3.0 Preview 1 (Mai 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Dokumentation zum Windows Community Toolkit | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Einrichten der Desktopanwendung für das Packen von MSIX in Visual Studio | Microsoft Docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Aktivieren Sie Ihr Gerät für | Microsoft Docs"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec - microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback-| GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: Häufig gestellte Fragen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Home | NuGet Gallery"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Herunterladen dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "WinUI 3-Projektvorlagen-| Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer" 
