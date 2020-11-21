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
# <span data-ttu-id="64659-104">Erste Schritte mit WebView2 in WinUI 3 (Preview)</span><span class="sxs-lookup"><span data-stu-id="64659-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="64659-105">In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-APP und die wichtigsten Features der [Einführung in Microsoft Edge WebView2 (Preview)][Webview2Index]erstellen.</span><span class="sxs-lookup"><span data-stu-id="64659-105">In this article, learn how to create your first WebView2 app and about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="64659-106">Ihre erste WebView2-App verwendet WinUI3.</span><span class="sxs-lookup"><span data-stu-id="64659-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="64659-107">Wenn Sie weitere Informationen zu einzelnen APIs erhalten möchten, navigieren Sie zu [API-Referenz][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="64659-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="64659-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="64659-108">Prerequisites</span></span>  

<span data-ttu-id="64659-109">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie mit dem folgenden Artikel fortfahren.</span><span class="sxs-lookup"><span data-stu-id="64659-109">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

1.  <span data-ttu-id="64659-110">Windows 10-Version 1803 \ (Build 17134 \) oder höher</span><span class="sxs-lookup"><span data-stu-id="64659-110">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="64659-111">Wenn Sie weitere Informationen wünschen, navigieren Sie zu [Windows Update: häufig gestellte Fragen][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="64659-111">For more information, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
1.  <span data-ttu-id="64659-112">[Microsoft Edge (Chrom) Canary Channel][MicrosoftedgeinsiderDownload] unter Windows 10, Windows 8,1 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64659-112">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
1.  <span data-ttu-id="64659-113">Visual Studio 2019, Version 16,9 Preview.</span><span class="sxs-lookup"><span data-stu-id="64659-113">Visual Studio 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="64659-114">Weitere Informationen finden Sie unter [Windows-UI-Bibliothek 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="64659-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    <span data-ttu-id="64659-115">Berücksichtigen Sie bei der Installation von Visual Studio die folgenden Arbeitsauslastungen.</span><span class="sxs-lookup"><span data-stu-id="64659-115">Include the following workloads when you install Visual Studio.</span></span>  
    
    *   <span data-ttu-id="64659-116">.Net Desktop-Entwicklung \ (das Installationsprogramm installiert auch .net 5 \)</span><span class="sxs-lookup"><span data-stu-id="64659-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
    *   <span data-ttu-id="64659-117">Entwicklung der universellen Windows-Plattform</span><span class="sxs-lookup"><span data-stu-id="64659-117">Universal Windows Platform development</span></span>  
        
    <span data-ttu-id="64659-118">Zum Erstellen von C++-apps müssen Sie auch die folgenden Arbeitsauslastungen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="64659-118">To build C++ apps, you must also include the following workloads.</span></span>  
    
    *   <span data-ttu-id="64659-119">Desktop Entwicklung mit C++</span><span class="sxs-lookup"><span data-stu-id="64659-119">Desktop development with C++</span></span>  
    *   <span data-ttu-id="64659-120">Die optionale Komponente für die universelle Windows-Plattform (v142) (C++) für die universelle Windows-Plattform-Arbeitsauslastung.</span><span class="sxs-lookup"><span data-stu-id="64659-120">The C++ (v142) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="64659-121">Weitere Informationen finden Sie im Abschnitt "Entwicklung der universellen Windows-Plattform" im rechten Bereich zu Installations Details.</span><span class="sxs-lookup"><span data-stu-id="64659-121">For more information,  navigate to Installation Details under the Universal Windows Platform development section, on the right pane.</span></span>  
        
1.  <span data-ttu-id="64659-122">Stellen Sie sicher, dass auf Ihrem System eine NuGet-Paketquelle für [nuget.org][NugetHome]aktiviert ist.  Weitere Informationen finden Sie unter [Allgemeine NuGet-Konfigurationen][NugetConsumePackagesConfiguringNugetBehavior] und [Windows Community Toolkit][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="64659-122">Make sure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="64659-123">Laden Sie das [WinUI 3 Preview 3 VSIX-Paket][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="64659-123">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="64659-124">Das Installationsprogramm fügt sowohl die WinUI 3-Projektvorlagen als auch das NuGet-Paket, das die WinUI 3-Bibliotheken enthält, zu Visual Studio 2019 hinzu.</span><span class="sxs-lookup"><span data-stu-id="64659-124">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="64659-125">Anweisungen zum Hinzufügen des VSIX-Pakets zu Visual Studio finden Sie unter [Suchen und Verwenden von Visual Studio-Erweiterungen][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="64659-125">For instructions on how to add the VSIX package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="64659-126">Aktivieren Sie den [Entwicklermodus][WindowsUwpGetStartedEnableYourDeviceForDevelopment] , um sicherzustellen, dass Sie auf alle entwicklerspezifischen Visual Studio-Features zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="64659-126">Enable [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all developer-specific Visual Studio features.</span></span>  
    
## <span data-ttu-id="64659-127">Schritt 1: Erstellen eines Projekts</span><span class="sxs-lookup"><span data-stu-id="64659-127">Step 1 - Create Project</span></span>  

<span data-ttu-id="64659-128">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="64659-128">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="64659-129">Wählen Sie in Visual Studio **Neues Projekt erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="64659-129">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="64659-130">Wählen Sie in der Dropdownliste Projekt den Eintrag **C#**, **Windows**und **WinUI** aus.</span><span class="sxs-lookup"><span data-stu-id="64659-130">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Erstellen eines neuen WinUI-Projekts mit Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="64659-132">Erstellen eines neuen WinUI-Projekts mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="64659-132">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="64659-133">Wählen Sie **leere APP, verpackt (WinUI im Desktop)** aus, und wählen Sie dann **weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="64659-133">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="64659-134">Geben Sie einen Projektnamen ein, wählen Sie bei Bedarf weitere Optionen aus, und wählen Sie dann **Erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="64659-134">Enter a project name, choose other options as needed, and then choose **Create**.</span></span>  
1.  <span data-ttu-id="64659-135">Wählen Sie in der **neuen universellen Windows-Plattform Project**die folgenden Werte aus, und wählen Sie dann **OK**aus.</span><span class="sxs-lookup"><span data-stu-id="64659-135">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="64659-136">**Zielversion**:  **Windows 10, Version 1903 (Build 18362)** oder höher</span><span class="sxs-lookup"><span data-stu-id="64659-136">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="64659-137">**Minimale Version**:  **Windows 10, Version 1803 (Build 17134)**</span><span class="sxs-lookup"><span data-stu-id="64659-137">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Das neue Dialogfeld "universelle Windows-Plattform" mit ausgewählten Werten für Zielversion und Mindestversion." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="64659-139">Das neue Dialogfeld "universelle Windows-Plattform" mit ausgewählten Werten für Zielversion und Mindestversion.</span><span class="sxs-lookup"><span data-stu-id="64659-139">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="64659-140">Im Projektmappen-Explorer werden zwei Projekte generiert.</span><span class="sxs-lookup"><span data-stu-id="64659-140">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="64659-141">**Ihr Projektname (Desktop)**.</span><span class="sxs-lookup"><span data-stu-id="64659-141">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="64659-142">Dieses Projekt enthält den Code für Ihre APP.</span><span class="sxs-lookup"><span data-stu-id="64659-142">This project contains the code for your app.</span></span>  <span data-ttu-id="64659-143">**App.XAML.cs** definiert eine `Application` Klasse, die ihre app-Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="64659-143">**App.xaml.cs** defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="64659-144">**MainWindow.XAML.cs** definiert eine `MainWindow` Klasse, die das von der app-Instanz angezeigte Hauptfenster darstellt.</span><span class="sxs-lookup"><span data-stu-id="64659-144">**MainWindow.xaml.cs** defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="64659-145">Diese Klassen werden von Typen im `Microsoft.UI.Xaml` Namespace von WinUI abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="64659-145">These classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="64659-146">**Ihr Projektname (Paket)**.</span><span class="sxs-lookup"><span data-stu-id="64659-146">**Your project name (Package)**.</span></span>  <span data-ttu-id="64659-147">Bei diesem Projekt handelt es sich um ein Projekt für die Windows-Anwendungsverpackung, das zum Erstellen der app in einem MSIX-Paket für die Bereitstellung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="64659-147">This project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="64659-148">Das Projekt enthält das Paketmanifest für Ihre APP, und es ist standardmäßig das Startprojekt für Ihre Lösung.</span><span class="sxs-lookup"><span data-stu-id="64659-148">The project contains the package manifest for your app, and it is the startup project for your solution by default.</span></span>  <span data-ttu-id="64659-149">Weitere Informationen finden Sie unter [Einrichten Ihrer Desktopanwendung für MSIX-Verpackungen in Visual Studio und in][WindowsMsixDesktopToUwpPackagingDotNet] der [Paketmanifest-Schemareferenz für Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="64659-149">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="64659-150">Öffnen Sie im Projektmappen-Explorer die Datei, um den Code anzuzeigen `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="64659-150">In the Solution Explorer, to display the code, open `MainWindow.xaml` file.</span></span>  <span data-ttu-id="64659-151">Wählen Sie aus `F5` , um Ihr Projekt auszuführen und ein Fenster mit einer Schaltfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64659-151">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="64659-152">Schritt 2 – Hinzufügen eines WebView2-Steuerelements zum Projekt</span><span class="sxs-lookup"><span data-stu-id="64659-152">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="64659-153">Fügen Sie dem Projekt als nächstes ein WebView2-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="64659-153">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="64659-154">Öffnen Sie `MainWindow.xaml`.</span><span class="sxs-lookup"><span data-stu-id="64659-154">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="64659-155">Fügen Sie den WebView2-XAML-Namespace hinzu, indem Sie die folgende Zeile innerhalb der `<Window/>` Kategorie einfügen.</span><span class="sxs-lookup"><span data-stu-id="64659-155">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="64659-156">Vergewissern Sie sich, dass Ihr Code in `MainWindow.xaml` mit dem folgenden Codeausschnitt vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="64659-156">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="64659-157">Wenn Sie das WebView2-Steuerelement hinzufügen möchten, ersetzen Sie die `<StackPanel>` Tags durch den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="64659-157">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="64659-158">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="64659-158">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="64659-159">Öffnen `MainWindow.xaml.cs` Sie die folgende Zeile, und kommentieren Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="64659-159">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="64659-160">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="64659-160">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="64659-161">Vergewissern Sie sich, dass Ihr WebView2-Steuerelement angezeigt wird [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="64659-161">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Ein WebView2-Steuerelement, das die Microsoft.com-Website anzeigt" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="64659-163">Ein WebView2-Steuerelement, das die Microsoft.com-Website anzeigt.</span><span class="sxs-lookup"><span data-stu-id="64659-163">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="64659-164">Schritt 3: Hinzufügen von Navigationssteuerelementen</span><span class="sxs-lookup"><span data-stu-id="64659-164">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="64659-165">Ermöglichen Sie Benutzern, die Webseite zu steuern, die in Ihrem WebView2-Steuerelement angezeigt wird, indem Sie Ihrer APP eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="64659-165">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span>  

1.  <span data-ttu-id="64659-166">`MainWindow.xaml`Kopieren Sie den folgenden Codeausschnitt in das Element, das `Grid` das Element enthält, und fügen Sie es ein `WebView2` .</span><span class="sxs-lookup"><span data-stu-id="64659-166">In `MainWindow.xaml`, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="64659-167">Vergewissern Sie sich, dass das `Grid` Element von `MainWindow.xaml` mit dem folgenden Codeausschnitt vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="64659-167">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="64659-168">`MainWindow.xaml.cs`Kopieren Sie in den folgenden Codeausschnitt in `myButton_Click` , der durch das WebView2-Steuerelement zur URL wechselt, die in der Adressleiste eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="64659-168">In `MainWindow.xaml.cs`, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="64659-169">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="64659-169">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="64659-170">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie dann **Gehe**zu aus.</span><span class="sxs-lookup"><span data-stu-id="64659-170">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="64659-171">Geben Sie beispielsweise ein `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="64659-171">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="64659-172">Stellen Sie sicher, dass Sie vollständige URLs in der Adressleiste verwenden.</span><span class="sxs-lookup"><span data-stu-id="64659-172">Ensure you use complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="64659-173">Ausnahmen werden ausgelöst, wenn die URL nicht mit `http://` oder beginnt `https://` .</span><span class="sxs-lookup"><span data-stu-id="64659-173">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="„Bing.com“" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="64659-175">„Bing.com“</span><span class="sxs-lookup"><span data-stu-id="64659-175">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="64659-176">Schritt 4 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="64659-176">Step 4 - Navigation events</span></span>  

<span data-ttu-id="64659-177">Anwendungen, die WebView2-Steuerelemente hosten, lauschen den folgenden Ereignissen, die von WebView2-Steuerelementen während der Webseiten Navigation ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="64659-177">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="64659-178">HTTP-Umleitungen lösen mehrere `NavigationStarting` Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="64659-178">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="64659-179">Wenn Sie weitere Informationen wünschen, navigieren Sie zu [Navigations Ereignissen][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="64659-179">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="64659-180">Wenn Fehler auftreten, werden die folgenden Ereignisse ausgelöst und möglicherweise zu einer Fehlerseite navigiert.</span><span class="sxs-lookup"><span data-stu-id="64659-180">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="64659-181">Als Beispiel für die Verwendung der Ereignisse registrieren Sie einen Handler für `NavigationStarting` diesen Vorgang, der jede Anforderung abbricht, die kein HTTPS verwendet.</span><span class="sxs-lookup"><span data-stu-id="64659-181">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any request that does not use HTTPS.</span></span>  <span data-ttu-id="64659-182">Ändern Sie in `MainWindow.xaml.cs` den Konstruktor, um `EnsureHttps` ihn zu registrieren, und fügen Sie die `EnsureHttps` Funktion so hinzu, dass Sie dem folgenden Codeausschnitt entspricht.</span><span class="sxs-lookup"><span data-stu-id="64659-182">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="64659-183">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="64659-183">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="64659-184">Vergewissern Sie sich, dass die Navigation für HTTP-Websites blockiert und für HTTPS-Websites zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="64659-184">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="64659-185">Schritt 5 – Skripting</span><span class="sxs-lookup"><span data-stu-id="64659-185">Step 5 - Scripting</span></span>  

<span data-ttu-id="64659-186">Host-Anwendungen können JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einfügen.</span><span class="sxs-lookup"><span data-stu-id="64659-186">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="64659-187">Das eingefügte JavaScript gilt für alle neuen Dokumente auf oberster Ebene und für alle untergeordneten Frames, bis das JavaScript entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="64659-187">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="64659-188">Das eingefügte JavaScript wird mit einer bestimmten Anzeigedauer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64659-188">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="64659-189">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="64659-189">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="64659-190">Führen Sie die Datei aus, bevor alle anderen Skripts, die im HTML-Dokument enthalten sind, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="64659-190">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="64659-191">Ein Beispiel: beim Hinzufügen von Skripts wird eine Benachrichtigung gesendet, wenn ein Benutzer zu nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="64659-191">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="64659-192">Ändern `EnsureHttps` Sie die Funktion, um ein Skript in den Webinhalt einzufügen, der [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]verwendet.</span><span class="sxs-lookup"><span data-stu-id="64659-192">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="64659-193">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="64659-193">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="64659-194">Vergewissern Sie sich, dass Ihre Anwendung eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die kein HTTPS verwendet.</span><span class="sxs-lookup"><span data-stu-id="64659-194">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="WebView2-Steuerelement mit einem Warnungsdialogfeld" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="64659-196">WebView2-Steuerelement mit einem Warnungsdialogfeld</span><span class="sxs-lookup"><span data-stu-id="64659-196">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="64659-197">Herzlichen Glückwunsch, Sie haben ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="64659-197">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="64659-198">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="64659-198">Next Steps</span></span>  

<span data-ttu-id="64659-199">Unser Team erstellt derzeit mehr WebView2-APIs.</span><span class="sxs-lookup"><span data-stu-id="64659-199">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="64659-200">Weitere Informationen zum aktuellen Zustand von WebView2-APIs finden Sie unter WebView2- [Spezifikation][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="64659-200">For more information on the current state of WebView2 APIs, navigate to the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="64659-201">Das WinRT-CoreWebView2-Objekt steht möglicherweise nicht zur Verfügung, wenn die WebView2-APIs ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="64659-201">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span>  <span data-ttu-id="64659-202">Wenn Sie wissen möchten, welche APIs für WebView2-Steuerelemente verfügbar sind, navigieren Sie zu [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] , um eine Liste der verfügbaren APIs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64659-202">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  

<span data-ttu-id="64659-203">Weitere Informationen zu den WebView2-Funktionen finden Sie unter [WebView2-Konzepte und How-To-Leitfäden][Webview2IndexNextSteps] sowie WebView2-Beispiele für [Repo][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="64659-203">For more information about WebView2 capabilities, navigate to [WebView2 Concepts and How-To guides][Webview2IndexNextSteps] and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="64659-204">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="64659-204">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
