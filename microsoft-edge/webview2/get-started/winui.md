---
description: Erste Schritte mit WebView2 für WinUI-Apps
title: Erste Schritte mit WebView2 für WinUI-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, Webview, winui apps, winui, edge, CoreWebView2, browser control, edge html, get started, Erste Schritte, .NET
ms.openlocfilehash: e334e8e7aec5fff4c57700a99de5cde906242e4f
ms.sourcegitcommit: bbbf722067f1d255f59ab384e66798f8b77ef609
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "11574582"
---
# <a name="get-started-with-webview2-in-winui-3-preview"></a>Erste Schritte mit WebView2 in WinUI 3 (Vorschau)  

Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Ihre erste WebView2-App verwendet WinUI3.  Weitere Informationen zu einzelnen APIs finden Sie unter [API reference][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].  

## <a name="prerequisites"></a>Voraussetzungen  

Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.  

*   [WebView2 Runtime][Webview2Installer] oder Microsoft Edge [(Chromium)][MicrosoftedgeinsiderDownload] nicht stabilen Kanal, der auf Windows 10 Version 1803 \(Build 17134\) oder höher installiert ist.  Weitere Informationen zu Windows 10 finden Sie unter [Windows Update: FAQ][MicrosoftSupport12373].  
    
    > [!NOTE]
    > Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2019, Version 16.9 Preview.  Weitere Informationen finden Sie unter [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    *   Schließen Sie die folgenden Workloads ein, wenn Sie Visual Studio.  
        *   .NET Desktop Development \(Das Installationsprogramm installiert auch .NET 5\)  
        *   Universelle Windows-Plattformentwicklung  
    *   Zum Erstellen von C++-Apps müssen Sie auch die folgenden Workloads hinzufügen.  
        *   Desktopentwicklung mit C++  
        *   Die optionale Komponente C++ \(v142\) Universal Windows Platform tools für die universelle Windows Plattformarbeitsauslastung.  Weitere Informationen finden Sie unter **Installationsdetails** im Abschnitt Entwicklung der universellen **Windows-Plattform** im rechten Bereich.  
        
## <a name="step-0---visual-studio-settings"></a>Schritt 0 – Visual Studio Einstellungen  

1.  Stellen Sie sicher, dass auf Ihrem NuGet eine Paketquelle [für][NugetHome]die nuget.org.  Weitere Informationen finden Sie unter [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] und [Windows Community Toolkit][WindowsCommunitytoolkit].  
1.  Laden Sie das Project [VsIX-Paket "Reunion" herunter,][VisualstudioMarketplaceProjectreunionMicrosoftprojectreunion]und installieren Sie es.  Das Installationsprogramm fügt die WinUI 3-Projektvorlagen und das NuGet-Paket mit den WinUI 3-Bibliotheken zu Visual Studio 2019 hinzu.  
    
    Anweisungen zum Hinzufügen des Pakets zu Visual Studio navigieren Sie zu Suchen und Verwenden `VSIX` [Visual Studio Erweiterungen][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].
    
1.  Um auf alle entwicklerspezifischen Features Visual Studio, aktivieren Sie den [Entwicklermodus][WindowsUwpGetStartedEnableYourDeviceForDevelopment].  
    
## <a name="step-1---create-project"></a>Schritt 1 : Erstellen Project  

Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.  

1.  Wählen Visual Studio Sie erstellen **ein neues Projekt aus.**  
1.  Wählen Sie in der Dropdownliste des **Projekts C#**, **Windows**und **WinUI** aus.  
    
    :::image type="complex" source="./media/winui-getting-started-selections.png" alt-text="Erstellen Eines neuen WinUI-Projekts mithilfe Visual Studio" lightbox="./media/winui-getting-started-selections.png":::
        Erstellen Eines neuen WinUI-Projekts mithilfe Visual Studio
    :::image-end:::  
    
1.  Wählen **Sie Leere App, Verpackt (WinUI in Desktop)**  >  **Weiter aus.**  
1.  Geben Sie einen Projektnamen ein.
1.  Wählen Sie nach Bedarf Optionen aus.  
1.  Wählen Sie **Erstellen** aus.  
1.  Wählen Sie in New **Universal Windows Platform Project**die folgenden Werte aus, und wählen Sie dann OK **aus.**  
    *   **Zielversion**: **Windows 10, Version 1903 (Build 18362)** oder höher  
    *   **Mindestversion**: **Windows 10, Version 1803 (Build 17134)**  
        
    :::image type="complex" source="./media/winui-getting-started-project-type.png" alt-text="Das Dialogfeld Neue universelle Windows-Project mit ausgewählten Werten für die Zielversion und die Mindestversion." lightbox="./media/winui-getting-started-project-type.png":::
       Das Dialogfeld Neue universelle Windows-Project mit ausgewählten Werten für die Zielversion und die Mindestversion.
    :::image-end:::  
    
1.  Im Projektmappen-Explorer werden zwei Projekte generiert.  
    *   **Ihr Projektname (Desktop)**.  Das Desktop-Projekt enthält den Code für Ihre App.  Die `App.xaml.cs` Datei definiert eine `Application` Klasse, die Ihre App-Instanz darstellt.  Die `MainWindow.xaml.cs` Datei definiert eine `MainWindow` Klasse, die das Hauptfenster darstellt, das von Ihrer App-Instanz angezeigt wird.  Die Klassen leiten sich von Typen im `Microsoft.UI.Xaml` Namespace von WinUI ab.  
    *   **Ihr Projektname (Package)**.  Das Paketprojekt ist eine Windows Application Packaging-Project, die für die Erstellung der App in ein MSIX-Paket für die Bereitstellung konfiguriert ist.  Das Projekt enthält das Paketmanifest für Ihre App und ist standardmäßig das Startprojekt für Ihre Lösung.  Weitere Informationen finden Sie unter Einrichten der Desktopanwendung für [die MSIX-Verpackung in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] und [Paketmanifestschemareferenz für Windows 10][UwpSchemasAppxpackageUapmanifestRoot].  
1.  Öffnen Sie zum Anzeigen des Codes im Projektmappen-Explorer die `MainWindow.xaml` Datei.  Wählen Sie aus, um Ihr Projekt zu ausführen und ein Fenster mit einer Schaltfläche `F5` anzuzeigen.  
    
## <a name="step-2---add-a-webview2-control-to-your-project"></a>Schritt 2 : Hinzufügen eines WebView2-Steuerelements zu Ihrem Projekt  

Fügen Sie Ihrem Projekt ein WebView2-Steuerelement hinzu.  

1.  Fügen Sie in der Datei die folgende Zeile in das Tag ein, um den `MainWindow.xaml` WebView2-XAML-Namespace `<Window/>` hinzuzufügen.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Stellen Sie sicher, dass Ihr Code in `MainWindow.xaml` dem folgenden Codeausschnitt ähnelt.  
    
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
    
1.  Zum Hinzufügen des WebView2-Steuerelements ersetzen Sie die `<StackPanel>` Tags durch den folgenden Codeausschnitt.  Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.  
    
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
    
1.  Kommentieren `MainWindow.xaml.cs` Sie in der Datei die folgende Zeile aus.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.  
    
    :::image type="complex" source="./media/winui-getting-started-part-3.png" alt-text="WebView2-Steuerelement zeigt microsoft.com" lightbox="./media/winui-getting-started-part-3.png":::
       WebView2-Steuerelement zeigt microsoft.com  
    :::image-end:::  
    
## <a name="step-3---add-navigation-controls"></a>Schritt 3 : Hinzufügen von Navigationssteuerelementen  

Damit Benutzer die Webseite steuern können, die in Ihrem WebView2-Steuerelement angezeigt wird, fügen Sie Ihrer App eine Adressleiste hinzu.  

1.  Kopieren Und fügen Sie in der Datei den folgenden Codeausschnitt in das `MainWindow.xaml` Element `<Grid>` ein, das das Element `WebView2` enthält.  
    
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
    
1.  Kopieren Sie in der Datei den folgenden Codeausschnitt in , der das WebView2-Steuerelement zu der in der `MainWindow.xaml.cs` `myButton_Click` Adressleiste eingegebenen URL navigiert.  
    
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
    
    Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie dann **Go aus.**  Geben Sie z. B. `https://www.bing.com` ein.  
    
    > [!NOTE]
    > Stellen Sie sicher, dass Sie vollständige URLs in der Adressleiste eingeben.  `ArgumentException` Ausnahmen werden ausgelöst, wenn die URL nicht mit oder `http://` `https://` beginnt.  
    
    :::image type="complex" source="./media/winui-getting-started-bing.png" alt-text="bing.com" lightbox="./media/winui-getting-started-bing.png":::
       bing.com  
    :::image-end:::  
    
## <a name="step-4---navigation-events"></a>Schritt 4 – Navigationsereignisse  

Apps, die WebView2-Steuerelemente hosten, lauschen auf die folgenden Ereignisse, die von WebView2-Steuerelementen während der Webseitennavigation ausgelöst werden.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
> [!NOTE]
> Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.  

Weitere Informationen finden Sie unter [Navigationsereignisse][Webviews2ConceptsNavigationEvents].  

Wenn Fehler auftreten, werden die folgenden Ereignisse ausgelöst und können zu einer Fehlerwebseite navigieren.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
Als Beispiel für die Verwendung der Ereignisse registrieren Sie einen Handler, `NavigationStarting` der alle Nicht-HTTPS-Anforderungen abbricht.  Ändern `MainWindow.xaml.cs` Sie in den Konstruktor so, dass er registriert wird, und fügen Sie die Funktion so hinzu, dass sie dem folgenden `EnsureHttps` `EnsureHttps` Codeausschnitt entspricht.  

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

Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass die Navigation für HTTP-Websites blockiert ist und für HTTPS-Websites zulässig ist.  

## <a name="step-5---scripting"></a>Schritt 5 – Skripterstellung  

Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.  Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.  Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.  Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.  

*   Führen Sie es nach der Erstellung des globalen Objekts aus.  
*   Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.  
    
Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.  Ändern Sie `EnsureHttps` die Funktion, um ein Skript in den Webinhalt zu injizieren, der [ExecuteScriptAsync verwendet.][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]  

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

Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.  Stellen Sie sicher, dass Ihre App eine Warnung anzeigt, wenn Sie zu websites navigieren, die keine HTTPS-Websites sind.  

:::image type="complex" source="./media/winui-getting-started-script.png" alt-text="WebView2-Steuerelement zeigt ein Warnungsdialogfeld an" lightbox="./media/winui-getting-started-script.png":::
   WebView2-Steuerelement zeigt ein Warnungsdialogfeld an
:::image-end:::  

Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.  

## <a name="next-steps"></a>Nächste Schritte  

Navigieren Sie zu den folgenden Ressourcen, um weitere Informationen zu WebView2 zu erhalten.  

*   Weitere Informationen zum Erstellen von WebView2-Anwendungen finden Sie unter Bewährte Methoden für [die WebView2-Entwicklung.][WV2BestPractices]  
*   Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].  
    
    > [!NOTE]
    > Das WinRT CoreWebView2-Objekt ist möglicherweise nicht mit der Version der WebView2-API verfügbar.  Um zu verstehen, welche APIs für WebView2-Steuerelemente verfügbar sind, navigieren Sie zu [WebView2 Spec,][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] um eine Liste der verfügbaren APIs zu finden.  
    
*   Ausführliche Informationen zur WebView2-API finden Sie unter [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Kontakt mit dem Microsoft Edge WebView-Team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

Um Ihre WinUI-spezifischen Featureanforderungen oder Fehler zu senden, navigieren Sie zu [Probleme - microsoft/microsoft-ui-xaml,][GithubMicrosoftMicrosoftUiXamlIssues] und wählen Sie **Neues Problem aus.**  

<!-- links -->  
[WV2BestPractices]: ../concepts/developer-guide.md "Bewährte Methoden für die WebView2-| Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  
[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  

[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Häufig NuGet Konfigurationen | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Paketmanifestschemareferenz für Windows 10 | Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installieren ohne Verwenden des Dialogfelds Erweiterungen verwalten – Verwalten von Erweiterungen für Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Konfigurieren Der Entwicklungsumgebung : Windows Ui Library 3.0 Preview 1 (Mai 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Windows Community Toolkit Documentation | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Richten Sie Ihre Desktopanwendung für die MSIX-Verpackung in einem Visual Studio | Microsoft Docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Aktivieren Sie Ihr Gerät für | Microsoft Docs"  

[GithubMicrosoftMicrosoftUiXamlIssues]: https://github.com/microsoft/microsoft-ui-xaml/issues "Probleme – microsoft/microsoft-ui-xaml | GitHub"  
[GithubMicrosoftMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec – microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: Häufig gestellte Fragen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Startseite | NuGet Gallery"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Download dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceProjectreunionMicrosoftprojectreunion]: https://marketplace.visualstudio.com/items?itemName=ProjectReunion.MicrosoftProjectReunion "Project Reunion-| Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer" 
