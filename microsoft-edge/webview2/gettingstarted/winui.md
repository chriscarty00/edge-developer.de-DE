---
description: Hosten von Webinhalten in ihrer WinUI-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge-WebView2 für WinUI-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinUI-apps, WinUI, Edge, CoreWebView2, Browser-Steuerelement, Edge-HTML, erste Schritte, erste Schritte, .net
ms.openlocfilehash: 805655fd27c0b654e1ccb41c615aa21797d6ddf7
ms.sourcegitcommit: ef6d6adae1f4d18a219fa3e17f91b95b40367a40
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/18/2020
ms.locfileid: "10934898"
---
# <span data-ttu-id="54760-104">Erste Schritte mit WebView2 in WinUI3 (Preview)</span><span class="sxs-lookup"><span data-stu-id="54760-104">Getting started with WebView2 in WinUI3 (Preview)</span></span>  

<span data-ttu-id="54760-105">In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-App mit WinUI3 erstellen, und erfahren Sie mehr über die wichtigsten Features der [Einführung in Microsoft Edge WebView2 (Preview)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="54760-105">In this article, get started creating your first WebView2 app with WinUI3 and learn about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="54760-106">Weitere Informationen zu einzelnen APIs finden Sie unter [API-Referenz][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="54760-106">For more information on individual APIs, see [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="54760-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="54760-107">Prerequisites</span></span>  

<span data-ttu-id="54760-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie mit dem folgenden Artikel fortfahren.</span><span class="sxs-lookup"><span data-stu-id="54760-108">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

*   <span data-ttu-id="54760-109">Windows 10-Version 1803 \ (Build 17134 \) oder höher</span><span class="sxs-lookup"><span data-stu-id="54760-109">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="54760-110">Weitere Informationen finden Sie unter [Windows Update: häufig gestellte Fragen (FAQ][MicrosoftSupport12373]).</span><span class="sxs-lookup"><span data-stu-id="54760-110">For more information, see [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
*   <span data-ttu-id="54760-111">[Microsoft Edge (Chrom) Canary Channel][MicrosoftedgeinsiderDownload] unter Windows 10, Windows 8,1 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54760-111">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
*   <span data-ttu-id="54760-112">Visual Studio 2019, Version 16,7 Preview 1</span><span class="sxs-lookup"><span data-stu-id="54760-112">Visual Studio 2019, version 16.7 Preview 1.</span></span>  <span data-ttu-id="54760-113">Weitere Informationen finden Sie unter [Windows-UI-Bibliothek 3 Preview 2 (Juli 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="54760-113">For more information, see [Windows UI Library 3 Preview 2 (July 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
*   <span data-ttu-id="54760-114">Sowohl die [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] -als auch die [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] -Version von .net 5 Preview 4.</span><span class="sxs-lookup"><span data-stu-id="54760-114">Both the [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] and [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] versions of .NET 5 Preview 4.</span></span>  
*   <span data-ttu-id="54760-115">[WinUI 3-Projektvorlagen][VisualstudioMarketplaceWinUiprojecttemplates] Erweiterung für Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="54760-115">[WinUI 3 Project Templates][VisualstudioMarketplaceWinUiprojecttemplates] extension for Visual Studio 2019.</span></span>  
<span data-ttu-id="54760-116">Stellen Sie sicher, dass Sie den [Entwicklermodus aktivieren][WindowsUwpGetStartedEnableYourDeviceForDevelopment] , um sicherzustellen, dass Sie auf alle Features von Visual Studio zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="54760-116">Ensure you [Enable Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all Visual Studio features.</span></span>  

## <span data-ttu-id="54760-117">Schritt 1: Erstellen eines Projekts</span><span class="sxs-lookup"><span data-stu-id="54760-117">Step 1 - Create Project</span></span>  

<span data-ttu-id="54760-118">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="54760-118">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="54760-119">Wählen Sie in Visual Studio **ein neues Projekt erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="54760-119">In Visual Studio, select **Create a new project**.</span></span>  
1.  <span data-ttu-id="54760-120">Wählen Sie in der Dropdownliste Projekt den Eintrag **C#**, **Windows**und **WinUI** aus.</span><span class="sxs-lookup"><span data-stu-id="54760-120">In the project drop-down, select **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Dialogfeld zum Erstellen von Visual Studio-Projekten für WinUI" lightbox="./media/winui-gettingstarted-selections.png":::
       <span data-ttu-id="54760-122">Dialogfeld zum Erstellen von Visual Studio-Projekten für WinUI</span><span class="sxs-lookup"><span data-stu-id="54760-122">Visual studio project creation dialog for WinUI</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="54760-123">Wählen Sie **leere APP, verpackt (WinUI im Desktop)** aus, und wählen Sie dann **weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="54760-123">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="54760-124">Geben Sie einen Projektnamen ein, wählen Sie bei Bedarf weitere Optionen aus, und wählen Sie dann **Erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="54760-124">Enter a project name, choose other options as needed, and then select **Create**.</span></span>  
1.  <span data-ttu-id="54760-125">Wählen Sie in der **neuen universellen Windows-Plattform Project**die folgenden Werte aus, und wählen Sie dann **OK**aus:</span><span class="sxs-lookup"><span data-stu-id="54760-125">In **New Universal Windows Platform Project**, select the following values, and then choose **OK**:</span></span>  
    *   <span data-ttu-id="54760-126">Zielversion: **Windows 10, Version 1903 (Build 18362)** oder höher</span><span class="sxs-lookup"><span data-stu-id="54760-126">Target version: **Windows 10, version 1903 (build 18362)** or later.</span></span>  
    *   <span data-ttu-id="54760-127">Minimale Version: **Windows 10, Version 1803 (Build 17134)**.</span><span class="sxs-lookup"><span data-stu-id="54760-127">Minimum version: **Windows 10, version 1803 (build 17134)**.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Dialogfeld zum Erstellen von Visual Studio-Projekten für WinUI" lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="54760-129">Das neue Dialogfeld "universelle Windows-Plattform" mit ausgewählten Werten für Zielversion und Mindestversion.</span><span class="sxs-lookup"><span data-stu-id="54760-129">The New Universal Windows Platform Project dialog with selected values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="54760-130">Im Projektmappen-Explorer werden zwei Projekte generiert.</span><span class="sxs-lookup"><span data-stu-id="54760-130">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="54760-131">**Ihr Projektname (Desktop)**.</span><span class="sxs-lookup"><span data-stu-id="54760-131">**Your project name(Desktop)**.</span></span> <span data-ttu-id="54760-132">Dieses Projekt enthält den Code für Ihre APP.</span><span class="sxs-lookup"><span data-stu-id="54760-132">This project contains the code for your app.</span></span>  <span data-ttu-id="54760-133">**App.XAML.cs** definiert eine `Application` Klasse, die ihre app-Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="54760-133">**App.xaml.cs** defines an`Application`class that represents your app instance.</span></span> <span data-ttu-id="54760-134">**MainWindow.XAML.cs** definiert eine `MainWindow` Klasse, die das von der app-Instanz angezeigte Hauptfenster darstellt.</span><span class="sxs-lookup"><span data-stu-id="54760-134">**MainWindow.xaml.cs** defines a`MainWindow`class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="54760-135">Diese Klassen werden von Typen im `Microsoft.UI.Xaml` Namespace von WinUI abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="54760-135">These classes derive from types in the`Microsoft.UI.Xaml`namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="54760-136">**Ihr Projektname (Paket)**.</span><span class="sxs-lookup"><span data-stu-id="54760-136">**Your project name(Package)**.</span></span>  <span data-ttu-id="54760-137">Bei diesem Projekt handelt es sich um aWindows Application Packaging Projectthat, das so konfiguriert ist, dass die app in einem MSIX-Paket für die Bereitstellung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="54760-137">This project is aWindows Application Packaging Projectthat is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="54760-138">Das Projekt enthält thepackage-manifestfor Ihrer APP, und es ist standardmäßig das Startprojekt für Ihre Lösung.</span><span class="sxs-lookup"><span data-stu-id="54760-138">The project contains thepackage manifestfor your app, and it is the startup project for your solution by default.</span></span> <span data-ttu-id="54760-139">Weitere Informationen finden Sie unter [Einrichten Ihrer Desktopanwendung für MSIX-Verpackungen in Visual Studio und in][WindowsMsixDesktopToUwpPackagingDotNet] der [Paketmanifest-Schemareferenz für Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="54760-139">For more information, see [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="54760-140">Öffnen Sie im Projektmappen-Explorer die Datei "Hauptfeld **. XAML** ", um den Code anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="54760-140">In the Solution Explorer, open **MainWindow.xaml** to display the code.</span></span>  <span data-ttu-id="54760-141">Wählen Sie aus `F5` , um Ihr Projekt auszuführen und ein Fenster mit einer Schaltfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="54760-141">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="54760-142">Schritt 2 – Hinzufügen eines WebView2-Steuerelements zum Projekt</span><span class="sxs-lookup"><span data-stu-id="54760-142">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="54760-143">Fügen Sie dem Projekt als nächstes ein WebView2-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="54760-143">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="54760-144">Öffnen Sie `MainWindow.xaml`.</span><span class="sxs-lookup"><span data-stu-id="54760-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="54760-145">Fügen Sie den WebView2-XAML-Namespace hinzu, indem Sie die folgende Zeile innerhalb der `<Window/>` Kategorie einfügen.</span><span class="sxs-lookup"><span data-stu-id="54760-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="54760-146">Vergewissern Sie sich, dass Ihr Code in `MainWindow.xaml` mit dem folgenden Codeausschnitt vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="54760-146">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="54760-147">Wenn Sie das WebView2-Steuerelement hinzufügen möchten, ersetzen Sie die `<StackPanel>` Tags durch den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="54760-147">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="54760-148">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="54760-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="54760-149">Öffnen `MainWindow.xaml.cs` Sie die folgende Zeile, und kommentieren Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="54760-149">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="54760-150">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="54760-150">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="54760-151">Vergewissern Sie sich, dass Ihr WebView2-Steuerelement angezeigt wird [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="54760-151">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Dialogfeld zum Erstellen von Visual Studio-Projekten für WinUI" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="54760-153">Ein WebView2-Steuerelement, das die Microsoft.com-Website anzeigt.</span><span class="sxs-lookup"><span data-stu-id="54760-153">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="54760-154">Schritt 3: Hinzufügen von Navigationssteuerelementen</span><span class="sxs-lookup"><span data-stu-id="54760-154">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="54760-155">Ermöglichen Sie Benutzern, die Webseite zu steuern, die in Ihrem WebView2-Steuerelement angezeigt wird, indem Sie Ihrer APP eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="54760-155">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span> 

1.  <span data-ttu-id="54760-156">Kopieren Sie in "Datei" **. XAML**den folgenden Codeausschnitt in das `Grid` Element, das das Element enthält, und fügen Sie ihn ein `WebView2` .</span><span class="sxs-lookup"><span data-stu-id="54760-156">In **MainWindow.xaml**, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="54760-157">Vergewissern Sie sich, dass das `Grid` Element von `MainWindow.xaml` mit dem folgenden Codeausschnitt vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="54760-157">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="54760-158">Kopieren Sie in **MainWindow.XAML.cs**den folgenden Codeausschnitt in `myButton_Click` , der das WebView2-Steuerelement zu der in der Adressleiste eingegebenen URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="54760-158">In **MainWindow.xaml.cs**, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="54760-159">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="54760-159">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="54760-160">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie dann **Gehe**zu aus.</span><span class="sxs-lookup"><span data-stu-id="54760-160">Enter a new URL in the address bar, and then select **Go**.</span></span>  <span data-ttu-id="54760-161">Geben Sie beispielsweise ein `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="54760-161">For example, enter `https://www.bing.com`.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="54760-162">Stellen Sie sicher, dass Sie vollständige URLs in der Adressleiste verwenden.</span><span class="sxs-lookup"><span data-stu-id="54760-162">Ensure you use complete URLs in the address bar.</span></span> `ArgumentException` <span data-ttu-id="54760-163">Ausnahmen werden ausgelöst, wenn die URL nicht mit `http://` oder beginnt `https://` .</span><span class="sxs-lookup"><span data-stu-id="54760-163">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Dialogfeld zum Erstellen von Visual Studio-Projekten für WinUI" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="54760-165">„Bing.com“</span><span class="sxs-lookup"><span data-stu-id="54760-165">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="54760-166">Schritt 4 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="54760-166">Step 4 - Navigation events</span></span>  

<span data-ttu-id="54760-167">Anwendungen, die WebView2-Steuerelemente hosten, lauschen den folgenden Ereignissen, die von WebView2-Steuerelementen während der Webseiten Navigation ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="54760-167">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="54760-168">HTTP-Umleitungen lösen mehrere `NavigationStarting` Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="54760-168">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="54760-169">Weitere Informationen finden Sie unter [Navigationsereignisse][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="54760-169">For more information, see [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="54760-170">Wenn Fehler auftreten, werden die folgenden Ereignisse ausgelöst und möglicherweise zu einer Fehlerseite navigiert.</span><span class="sxs-lookup"><span data-stu-id="54760-170">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="54760-171">Als ein Beispiel für die Verwendung der Ereignisse registrieren Sie einen Handler, der `NavigationStarting` alle Anforderungen abbricht, die kein HTTPS verwenden.</span><span class="sxs-lookup"><span data-stu-id="54760-171">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span> <span data-ttu-id="54760-172">Ändern Sie in `MainWindow.xaml.cs` den Konstruktor, um `EnsureHttps` ihn zu registrieren, und fügen Sie die `EnsureHttps` Funktion so hinzu, dass Sie dem folgenden Codeausschnitt entspricht.</span><span class="sxs-lookup"><span data-stu-id="54760-172">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="54760-173">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="54760-173">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="54760-174">Vergewissern Sie sich, dass die Navigation für HTTP-Websites blockiert und für HTTPS-Websites zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="54760-174">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="54760-175">Schritt 5 – Skripting</span><span class="sxs-lookup"><span data-stu-id="54760-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="54760-176">Host-Anwendungen können JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einfügen.</span><span class="sxs-lookup"><span data-stu-id="54760-176">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="54760-177">Das eingefügte JavaScript gilt für alle neuen Dokumente auf oberster Ebene und für alle untergeordneten Frames, bis das JavaScript entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="54760-177">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="54760-178">Das eingefügte JavaScript wird nach der Erstellung des globalen Objekts und vor dem Ausführen eines anderen im HTML-Dokument enthaltenen Skripts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54760-178">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="54760-179">Ein Beispiel: beim Hinzufügen von Skripts wird eine Benachrichtigung gesendet, wenn ein Benutzer zu nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="54760-179">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="54760-180">Ändern `EnsureHttps` Sie die Funktion, um ein Skript mit [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync]in den Webinhalt einzufügen.</span><span class="sxs-lookup"><span data-stu-id="54760-180">Modify the `EnsureHttps` function to inject a script into the web content using [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="54760-181">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="54760-181">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="54760-182">Vergewissern Sie sich, dass Ihre Anwendung eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die kein HTTPS verwendet.</span><span class="sxs-lookup"><span data-stu-id="54760-182">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Dialogfeld zum Erstellen von Visual Studio-Projekten für WinUI" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="54760-184">WebView2-Steuerelement mit einem Warnungsdialogfeld</span><span class="sxs-lookup"><span data-stu-id="54760-184">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="54760-185">Herzlichen Glückwunsch, Sie haben ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="54760-185">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="54760-186">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="54760-186">Next Steps</span></span>  

<span data-ttu-id="54760-187">Unser Team erstellt derzeit mehr WebView2-APIs.</span><span class="sxs-lookup"><span data-stu-id="54760-187">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="54760-188">Weitere Informationen zum aktuellen Zustand von WebView2-APIs finden Sie in der [WebView2-Spezifikation][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="54760-188">For more information on the current state of WebView2 APIs, see the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="54760-189">Das WinRT-CoreWebView2-Objekt steht möglicherweise nicht zur Verfügung, wenn die WebView2-APIs ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="54760-189">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span> <span data-ttu-id="54760-190">Wenn Sie wissen möchten, welche APIs für WebView2-Steuerelemente verfügbar sind, finden Sie unter [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] eine Liste der verfügbaren APIs.</span><span class="sxs-lookup"><span data-stu-id="54760-190">To understand which APIs are available to WebView2 controls, see [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span> 

<span data-ttu-id="54760-191">Weitere Informationen zu den WebView2-Funktionen finden Sie unter [WebView2-Konzepte und Anleitungen][Webview2IndexNextSteps]sowie im [WebView2-Beispiel-Repo][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="54760-191">For more information about WebView2 capabilities, see [WebView2 Concepts and How-To guides][Webview2IndexNextSteps], and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="54760-192">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="54760-192">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft docs"  
[Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 Klasse | Microsoft docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Paketmanifest-Schemareferenz für Windows 10 | Microsoft docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Konfigurieren der dev-Umgebung-Windows-UI-Bibliothek 3,0 Preview 1 (Mai 2020) | Microsoft docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Einrichten Ihrer Desktopanwendung für MSIX-Verpackungen in Visual Studio | Microsoft docs"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Aktivieren Ihres Geräts für die Entwicklung | Microsoft docs"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec-Microsoft/Microsoft-UI-XAML-Specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: häufig gestellte Fragen"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge-Insider Kanälen"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exeherunterladen "  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceWinUiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "WinUI 3-Projektvorlagen"  
