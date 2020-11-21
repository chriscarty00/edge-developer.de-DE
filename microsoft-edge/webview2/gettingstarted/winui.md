---
description: Leitfaden für erste Schritte mit WebView2 für WinUI-apps
title: Erste Schritte mit WebView2 für WinUI-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinUI-apps, WinUI, Edge, CoreWebView2, Browser-Steuerelement, Edge-HTML, erste Schritte, erste Schritte, .net
ms.openlocfilehash: a1ccffe332f71ee9d53ff267e8cca6bdbda81703
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182721"
---
# Erste Schritte mit WebView2 in WinUI 3 (Preview)  

In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-APP und die wichtigsten Features der [Einführung in Microsoft Edge WebView2 (Preview)][Webview2Index]erstellen.  Ihre erste WebView2-App verwendet WinUI3.  Wenn Sie weitere Informationen zu einzelnen APIs erhalten möchten, navigieren Sie zu [API-Referenz][GithubMicrosoftUiXamlSpecsWebview2].  

## Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie mit dem folgenden Artikel fortfahren.  

1.  Windows 10-Version 1803 \ (Build 17134 \) oder höher  Wenn Sie weitere Informationen wünschen, navigieren Sie zu [Windows Update: häufig gestellte Fragen][MicrosoftSupport12373].  
1.  [Microsoft Edge (Chrom) Canary Channel][MicrosoftedgeinsiderDownload] unter Windows 10, Windows 8,1 oder Windows 7.  
1.  Visual Studio 2019, Version 16,9 Preview.  Weitere Informationen finden Sie unter [Windows-UI-Bibliothek 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    
    Berücksichtigen Sie bei der Installation von Visual Studio die folgenden Arbeitsauslastungen.  
    
    *   .Net Desktop-Entwicklung \ (das Installationsprogramm installiert auch .net 5 \)  
    *   Entwicklung der universellen Windows-Plattform  
        
    Zum Erstellen von C++-apps müssen Sie auch die folgenden Arbeitsauslastungen einbeziehen.  
    
    *   Desktop Entwicklung mit C++  
    *   Die optionale Komponente für die universelle Windows-Plattform (v142) (C++) für die universelle Windows-Plattform-Arbeitsauslastung.  Weitere Informationen finden Sie im Abschnitt "Entwicklung der universellen Windows-Plattform" im rechten Bereich zu Installations Details.  
        
1.  Stellen Sie sicher, dass auf Ihrem System eine NuGet-Paketquelle für [nuget.org][NugetHome]aktiviert ist.  Weitere Informationen finden Sie unter [Allgemeine NuGet-Konfigurationen][NugetConsumePackagesConfiguringNugetBehavior] und [Windows Community Toolkit][WindowsCommunitytoolkit].  
1.  Laden Sie das [WinUI 3 Preview 3 VSIX-Paket][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]herunter, und installieren Sie es.  Das Installationsprogramm fügt sowohl die WinUI 3-Projektvorlagen als auch das NuGet-Paket, das die WinUI 3-Bibliotheken enthält, zu Visual Studio 2019 hinzu.  
    
    Anweisungen zum Hinzufügen des VSIX-Pakets zu Visual Studio finden Sie unter [Suchen und Verwenden von Visual Studio-Erweiterungen][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].
    
1.  Aktivieren Sie den [Entwicklermodus][WindowsUwpGetStartedEnableYourDeviceForDevelopment] , um sicherzustellen, dass Sie auf alle entwicklerspezifischen Visual Studio-Features zugreifen können.  
    
## Schritt 1: Erstellen eines Projekts  

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

1.  Wählen Sie in Visual Studio **Neues Projekt erstellen**aus.  
1.  Wählen Sie in der Dropdownliste Projekt den Eintrag **C#**, **Windows**und **WinUI** aus.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Erstellen eines neuen WinUI-Projekts mit Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Erstellen eines neuen WinUI-Projekts mit Visual Studio
    :::image-end:::  
    
1.  Wählen Sie **leere APP, verpackt (WinUI im Desktop)** aus, und wählen Sie dann **weiter**aus.  
1.  Geben Sie einen Projektnamen ein, wählen Sie bei Bedarf weitere Optionen aus, und wählen Sie dann **Erstellen**aus.  
1.  Wählen Sie in der **neuen universellen Windows-Plattform Project**die folgenden Werte aus, und wählen Sie dann **OK**aus.  
    *   **Zielversion**:  **Windows 10, Version 1903 (Build 18362)** oder höher  
    *   **Minimale Version**:  **Windows 10, Version 1803 (Build 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Das neue Dialogfeld "universelle Windows-Plattform" mit ausgewählten Werten für Zielversion und Mindestversion." lightbox="./media/winui-gettingstarted-projecttype.png":::
       Das neue Dialogfeld "universelle Windows-Plattform" mit ausgewählten Werten für Zielversion und Mindestversion.
    :::image-end:::  
    
1.  Im Projektmappen-Explorer werden zwei Projekte generiert.  
    *   **Ihr Projektname (Desktop)**.  Dieses Projekt enthält den Code für Ihre APP.  **App.XAML.cs** definiert eine `Application` Klasse, die ihre app-Instanz darstellt.  **MainWindow.XAML.cs** definiert eine `MainWindow` Klasse, die das von der app-Instanz angezeigte Hauptfenster darstellt.  Diese Klassen werden von Typen im `Microsoft.UI.Xaml` Namespace von WinUI abgeleitet.  
    
    *   **Ihr Projektname (Paket)**.  Bei diesem Projekt handelt es sich um ein Projekt für die Windows-Anwendungsverpackung, das zum Erstellen der app in einem MSIX-Paket für die Bereitstellung konfiguriert ist.  Das Projekt enthält das Paketmanifest für Ihre APP, und es ist standardmäßig das Startprojekt für Ihre Lösung.  Weitere Informationen finden Sie unter [Einrichten Ihrer Desktopanwendung für MSIX-Verpackungen in Visual Studio und in][WindowsMsixDesktopToUwpPackagingDotNet] der [Paketmanifest-Schemareferenz für Windows 10][UwpSchemasAppxpackageUapmanifestRoot].
    
1.  Öffnen Sie im Projektmappen-Explorer die Datei, um den Code anzuzeigen `MainWindow.xaml` .  Wählen Sie aus `F5` , um Ihr Projekt auszuführen und ein Fenster mit einer Schaltfläche anzuzeigen.  
    
## Schritt 2 – Hinzufügen eines WebView2-Steuerelements zum Projekt  

Fügen Sie dem Projekt als nächstes ein WebView2-Steuerelement hinzu.  

1.  Öffnen Sie `MainWindow.xaml`.  Fügen Sie den WebView2-XAML-Namespace hinzu, indem Sie die folgende Zeile innerhalb der `<Window/>` Kategorie einfügen.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Vergewissern Sie sich, dass Ihr Code in `MainWindow.xaml` mit dem folgenden Codeausschnitt vergleichbar ist.  
    
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
    
1.  Wenn Sie das WebView2-Steuerelement hinzufügen möchten, ersetzen Sie die `<StackPanel>` Tags durch den folgenden Codeausschnitt.  Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.  
    
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
    
1.  Öffnen `MainWindow.xaml.cs` Sie die folgende Zeile, und kommentieren Sie Sie aus.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Vergewissern Sie sich, dass Ihr WebView2-Steuerelement angezeigt wird [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Ein WebView2-Steuerelement, das die Microsoft.com-Website anzeigt" lightbox="./media/winui-gettingstarted-part3.png":::
       Ein WebView2-Steuerelement, das die Microsoft.com-Website anzeigt.  
    :::image-end:::  
    
## Schritt 3: Hinzufügen von Navigationssteuerelementen  

Ermöglichen Sie Benutzern, die Webseite zu steuern, die in Ihrem WebView2-Steuerelement angezeigt wird, indem Sie Ihrer APP eine Adressleiste hinzufügen.  

1.  `MainWindow.xaml`Kopieren Sie den folgenden Codeausschnitt in das Element, das `Grid` das Element enthält, und fügen Sie es ein `WebView2` .  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Vergewissern Sie sich, dass das `Grid` Element von `MainWindow.xaml` mit dem folgenden Codeausschnitt vergleichbar ist.  
    
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
    
1.  `MainWindow.xaml.cs`Kopieren Sie in den folgenden Codeausschnitt in `myButton_Click` , der durch das WebView2-Steuerelement zur URL wechselt, die in der Adressleiste eingegeben wurde.  
    
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
    
    Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie dann **Gehe**zu aus.  Geben Sie beispielsweise ein `https://www.bing.com` .  
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie vollständige URLs in der Adressleiste verwenden.  `ArgumentException` Ausnahmen werden ausgelöst, wenn die URL nicht mit `http://` oder beginnt `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="„Bing.com“" lightbox="./media/winui-gettingstarted-bing.png":::
       „Bing.com“  
    :::image-end:::  
    
## Schritt 4 – Navigationsereignisse  

Anwendungen, die WebView2-Steuerelemente hosten, lauschen den folgenden Ereignissen, die von WebView2-Steuerelementen während der Webseiten Navigation ausgelöst werden.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> HTTP-Umleitungen lösen mehrere `NavigationStarting` Ereignisse aus.  

Wenn Sie weitere Informationen wünschen, navigieren Sie zu [Navigations Ereignissen][Webviews2ConceptsNavigationEvents].  

Wenn Fehler auftreten, werden die folgenden Ereignisse ausgelöst und möglicherweise zu einer Fehlerseite navigiert.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
Als Beispiel für die Verwendung der Ereignisse registrieren Sie einen Handler für `NavigationStarting` diesen Vorgang, der jede Anforderung abbricht, die kein HTTPS verwendet.  Ändern Sie in `MainWindow.xaml.cs` den Konstruktor, um `EnsureHttps` ihn zu registrieren, und fügen Sie die `EnsureHttps` Funktion so hinzu, dass Sie dem folgenden Codeausschnitt entspricht.  

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

Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Vergewissern Sie sich, dass die Navigation für HTTP-Websites blockiert und für HTTPS-Websites zulässig ist.  

## Schritt 5 – Skripting  

Host-Anwendungen können JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einfügen.  Das eingefügte JavaScript gilt für alle neuen Dokumente auf oberster Ebene und für alle untergeordneten Frames, bis das JavaScript entfernt wurde.  Das eingefügte JavaScript wird mit einer bestimmten Anzeigedauer ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie die Datei aus, bevor alle anderen Skripts, die im HTML-Dokument enthalten sind, ausgeführt werden.  

Ein Beispiel: beim Hinzufügen von Skripts wird eine Benachrichtigung gesendet, wenn ein Benutzer zu nicht-HTTPS-Websites navigiert.  Ändern `EnsureHttps` Sie die Funktion, um ein Skript in den Webinhalt einzufügen, der [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]verwendet.  

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

Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.  Vergewissern Sie sich, dass Ihre Anwendung eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die kein HTTPS verwendet.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="WebView2-Steuerelement mit einem Warnungsdialogfeld" lightbox="./media/winui-gettingstarted-script.png":::
   WebView2-Steuerelement mit einem Warnungsdialogfeld
:::image-end:::  

Herzlichen Glückwunsch, Sie haben ihre erste WebView2-App erstellt.  

## Nächste Schritte  

Unser Team erstellt derzeit mehr WebView2-APIs.  Weitere Informationen zum aktuellen Zustand von WebView2-APIs finden Sie unter WebView2- [Spezifikation][GithubMicrosoftUiXamlSpecsWebview2].  

> [!NOTE]
> Das WinRT-CoreWebView2-Objekt steht möglicherweise nicht zur Verfügung, wenn die WebView2-APIs ausgeliefert werden.  Wenn Sie wissen möchten, welche APIs für WebView2-Steuerelemente verfügbar sind, navigieren Sie zu [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] , um eine Liste der verfügbaren APIs anzuzeigen.  

Weitere Informationen zu den WebView2-Funktionen finden Sie unter [WebView2-Konzepte und How-To-Leitfäden][Webview2IndexNextSteps] sowie WebView2-Beispiele für [Repo][GithubMicrosoftedgeWebview2samplesMain].  

## Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync (String)-Methode (Microsoft. Web. WebView2. WPF) | Microsoft docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Allgemeine NuGet-Konfigurationen | Microsoft docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Paketmanifest-Schemareferenz für Windows 10 | Microsoft docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installieren ohne Verwendung des Dialogfelds "Erweiterungen verwalten" – Verwalten von Erweiterungen für Visual Studio | Microsoft docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Konfigurieren der dev-Umgebung-Windows-UI-Bibliothek 3,0 Preview 1 (Mai 2020) | Microsoft docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Windows Community Toolkit-Dokumentation | Microsoft docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Einrichten Ihrer Desktopanwendung für MSIX-Verpackungen in Visual Studio | Microsoft docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Aktivieren Ihres Geräts für die Entwicklung | Microsoft docs"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec-Microsoft/Microsoft-UI-XAML-Specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: häufig gestellte Fragen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[NugetHome]: https://nuget.org "Startseite | NuGet-Katalog"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exeherunterladen "  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "WinUI 3-Projektvorlagen | Visual Studio Marketplace"  
