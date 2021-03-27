---
description: Erste Schritte mit WebView2 für WinUI-Apps
title: Erste Schritte mit WebView2 für WinUI-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, Webview, winui apps, winui, edge, CoreWebView2, browser control, edge html, getting started, .NET
ms.openlocfilehash: 52d84afb6f9fe1e120f75525b2669a797309fdfe
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461206"
---
# <a name="getting-started-with-webview2-in-winui-3-preview"></a><span data-ttu-id="38330-104">Erste Schritte mit WebView2 in WinUI 3 (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="38330-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="38330-105">Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="38330-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="38330-106">Ihre erste WebView2-App verwendet WinUI3.</span><span class="sxs-lookup"><span data-stu-id="38330-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="38330-107">Weitere Informationen zu einzelnen APIs finden Sie unter [API reference][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="38330-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="38330-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="38330-108">Prerequisites</span></span>  

<span data-ttu-id="38330-109">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="38330-109">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="38330-110">[WebView2-Laufzeit][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter Windows 10, Version 1803 \(Build 17134\) oder höher installiert ist.</span><span class="sxs-lookup"><span data-stu-id="38330-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="38330-111">Weitere Informationen zu Windows 10 finden Sie unter [Windows Update: FAQ][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="38330-111">For more information about Windows 10, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="38330-112">Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="38330-112">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="38330-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, Version 16.9 Preview.</span><span class="sxs-lookup"><span data-stu-id="38330-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="38330-114">Weitere Informationen finden Sie unter [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="38330-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    *   <span data-ttu-id="38330-115">Schließen Sie die folgenden Workloads ein, wenn Sie Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38330-115">Include the following workloads when you install Visual Studio.</span></span>  
        *   <span data-ttu-id="38330-116">.NET Desktop Development \(Das Installationsprogramm installiert auch .NET 5\)</span><span class="sxs-lookup"><span data-stu-id="38330-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
        *   <span data-ttu-id="38330-117">Entwicklung der universellen Windows-Plattform</span><span class="sxs-lookup"><span data-stu-id="38330-117">Universal Windows Platform development</span></span>  
    *   <span data-ttu-id="38330-118">Zum Erstellen von C++-Apps müssen Sie auch die folgenden Workloads hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="38330-118">To build C++ apps, you must also include the following workloads.</span></span>  
        *   <span data-ttu-id="38330-119">Desktopentwicklung mit C++</span><span class="sxs-lookup"><span data-stu-id="38330-119">Desktop development with C++</span></span>  
        *   <span data-ttu-id="38330-120">Die optionale Komponente C++ \(v142\) Universelle #A0 für die Arbeitsauslastung der universellen Windows-Plattform.</span><span class="sxs-lookup"><span data-stu-id="38330-120">The C++ \(v142\) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="38330-121">Weitere Informationen finden Sie unter **Installationsdetails** im Abschnitt Entwicklung der universellen **Windows-Plattform** im rechten Bereich.</span><span class="sxs-lookup"><span data-stu-id="38330-121">For more information,  navigate to **Installation Details** under the **Universal Windows Platform development** section, on the right pane.</span></span>  
        
## <a name="step-0---visual-studio-settings"></a><span data-ttu-id="38330-122">Schritt 0 – Visual Studio Einstellungen</span><span class="sxs-lookup"><span data-stu-id="38330-122">Step 0 - Visual Studio settings</span></span>  

1.  <span data-ttu-id="38330-123">Stellen Sie sicher, dass auf Ihrem System eine NuGet-Paketquelle für [die][NugetHome]nuget.org.  Weitere Informationen finden Sie unter [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] und [Windows Community Toolkit][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="38330-123">Ensure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="38330-124">Laden Sie das [WinUI 3 Preview 3 VSIX-Paket herunter, und installieren Sie es.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]</span><span class="sxs-lookup"><span data-stu-id="38330-124">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="38330-125">Das Installationsprogramm fügt sowohl die WinUI 3-Projektvorlagen als auch das NuGet-Paket mit den WinUI 3-Bibliotheken zu Visual Studio 2019 hinzu.</span><span class="sxs-lookup"><span data-stu-id="38330-125">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="38330-126">Anweisungen zum Hinzufügen des Pakets zu Visual Studio navigieren Sie zu Suchen und Verwenden Visual Studio `VSIX` [Erweiterungen][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="38330-126">For instructions on how to add the `VSIX` package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="38330-127">Um auf alle entwicklerspezifischen Visual Studio zu zugreifen, aktivieren Sie den [Entwicklermodus][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span><span class="sxs-lookup"><span data-stu-id="38330-127">To access all developer-specific Visual Studio features, turn on [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span></span>  
    
## <a name="step-1---create-project"></a><span data-ttu-id="38330-128">Schritt 1 – Projekt erstellen</span><span class="sxs-lookup"><span data-stu-id="38330-128">Step 1 - Create Project</span></span>  

<span data-ttu-id="38330-129">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="38330-129">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="38330-130">Wählen Visual Studio sie ein **neues Projekt erstellen aus.**</span><span class="sxs-lookup"><span data-stu-id="38330-130">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="38330-131">Wählen Sie in der Dropdownliste des Projekts **C#**, **Windows**und **WinUI** aus.</span><span class="sxs-lookup"><span data-stu-id="38330-131">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Erstellen eines neuen WinUI-Projekts mithilfe Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="38330-133">Erstellen eines neuen WinUI-Projekts mithilfe Visual Studio</span><span class="sxs-lookup"><span data-stu-id="38330-133">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="38330-134">Wählen **Sie Leere App, Verpackt (WinUI in Desktop)**  >  **Weiter aus.**</span><span class="sxs-lookup"><span data-stu-id="38330-134">Choose **Blank App, Packaged (WinUI in Desktop)** > **Next**.</span></span>  
1.  <span data-ttu-id="38330-135">Geben Sie einen Projektnamen ein.</span><span class="sxs-lookup"><span data-stu-id="38330-135">Enter a project name.</span></span>
1.  <span data-ttu-id="38330-136">Wählen Sie nach Bedarf Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="38330-136">Choose options as needed.</span></span>  
1.  <span data-ttu-id="38330-137">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="38330-137">Choose **Create**.</span></span>  
1.  <span data-ttu-id="38330-138">Wählen **Sie in New Universal Windows Platform Project**die folgenden Werte aus, und wählen Sie dann OK **aus.**</span><span class="sxs-lookup"><span data-stu-id="38330-138">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="38330-139">**Zielversion**:  **Windows 10, Version 1903 (Build 18362)** oder höher</span><span class="sxs-lookup"><span data-stu-id="38330-139">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="38330-140">**Mindestversion**:  **Windows 10, Version 1803 (Build 17134)**</span><span class="sxs-lookup"><span data-stu-id="38330-140">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Das Dialogfeld Neues universelles Windows-Plattformprojekt mit den ausgewählten Werten für die Zielversion und die Mindestversion." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="38330-142">Das Dialogfeld Neues universelles Windows-Plattformprojekt mit den ausgewählten Werten für die Zielversion und die Mindestversion.</span><span class="sxs-lookup"><span data-stu-id="38330-142">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="38330-143">Im Projektmappen-Explorer werden zwei Projekte generiert.</span><span class="sxs-lookup"><span data-stu-id="38330-143">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="38330-144">**Ihr Projektname (Desktop)**.</span><span class="sxs-lookup"><span data-stu-id="38330-144">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="38330-145">Das Desktop-Projekt enthält den Code für Ihre App.</span><span class="sxs-lookup"><span data-stu-id="38330-145">The Desktop project contains the code for your app.</span></span>  <span data-ttu-id="38330-146">Die `App.xaml.cs` Datei definiert eine `Application` Klasse, die Ihre App-Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="38330-146">The `App.xaml.cs` file defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="38330-147">Die `MainWindow.xaml.cs` Datei definiert eine `MainWindow` Klasse, die das Hauptfenster darstellt, das von Ihrer App-Instanz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38330-147">The `MainWindow.xaml.cs` file defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="38330-148">Die Klassen leiten sich von Typen im `Microsoft.UI.Xaml` Namespace von WinUI ab.</span><span class="sxs-lookup"><span data-stu-id="38330-148">The classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    *   <span data-ttu-id="38330-149">**Ihr Projektname (Package)**.</span><span class="sxs-lookup"><span data-stu-id="38330-149">**Your project name (Package)**.</span></span>  <span data-ttu-id="38330-150">Das Paketprojekt ist ein Windows-Anwendungspaketprojekt, das für die Erstellung der App in ein MSIX-Paket für die Bereitstellung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="38330-150">The Package project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="38330-151">Das Projekt enthält das Paketmanifest für Ihre App und ist standardmäßig das Startprojekt für Ihre Lösung.</span><span class="sxs-lookup"><span data-stu-id="38330-151">The project contains the package manifest for your app, and is the startup project for your solution by default.</span></span>  <span data-ttu-id="38330-152">Weitere Informationen finden Sie unter Einrichten Der Desktopanwendung für [die MSIX-Verpackung in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] und [Paketmanifestschemareferenz für Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="38330-152">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>  
1.  <span data-ttu-id="38330-153">Öffnen Sie zum Anzeigen des Codes im Projektmappen-Explorer die `MainWindow.xaml` Datei.</span><span class="sxs-lookup"><span data-stu-id="38330-153">In the Solution Explorer, to display the code, open the `MainWindow.xaml` file.</span></span>  <span data-ttu-id="38330-154">Wählen Sie aus, um Ihr Projekt zu ausführen und ein Fenster mit einer Schaltfläche `F5` anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="38330-154">To run your project and display a window with a button, select `F5`.</span></span>  
    
## <a name="step-2---add-a-webview2-control-to-your-project"></a><span data-ttu-id="38330-155">Schritt 2 : Hinzufügen eines WebView2-Steuerelements zu Ihrem Projekt</span><span class="sxs-lookup"><span data-stu-id="38330-155">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="38330-156">Fügen Sie Ihrem Projekt ein WebView2-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="38330-156">Add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="38330-157">Fügen Sie in der Datei die folgende Zeile in das Tag ein, um den `MainWindow.xaml` WebView2-XAML-Namespace `<Window/>` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="38330-157">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="38330-158">Stellen Sie sicher, dass Ihr Code in `MainWindow.xaml` dem folgenden Codeausschnitt ähnelt.</span><span class="sxs-lookup"><span data-stu-id="38330-158">Ensure your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="38330-159">Zum Hinzufügen des WebView2-Steuerelements ersetzen Sie die `<StackPanel>` Tags durch den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="38330-159">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="38330-160">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38330-160">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="38330-161">Kommentieren `MainWindow.xaml.cs` Sie in der Datei die folgende Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="38330-161">In the `MainWindow.xaml.cs` file, comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="38330-162">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="38330-162">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="38330-163">Stellen Sie sicher, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.</span><span class="sxs-lookup"><span data-stu-id="38330-163">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="WebView2-Steuerelement zeigt microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="38330-165">WebView2-Steuerelement zeigt microsoft.com</span><span class="sxs-lookup"><span data-stu-id="38330-165">WebView2 control displays microsoft.com</span></span>  
    :::image-end:::  
    
## <a name="step-3---add-navigation-controls"></a><span data-ttu-id="38330-166">Schritt 3 : Hinzufügen von Navigationssteuerelementen</span><span class="sxs-lookup"><span data-stu-id="38330-166">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="38330-167">Damit Benutzer die Webseite steuern können, die in Ihrem WebView2-Steuerelement angezeigt wird, fügen Sie Ihrer App eine Adressleiste hinzu.</span><span class="sxs-lookup"><span data-stu-id="38330-167">To allow users to control the webpage that is displayed in your WebView2 control, add an address bar to your app.</span></span>  

1.  <span data-ttu-id="38330-168">Kopieren Und fügen Sie in der Datei den folgenden Codeausschnitt in das `MainWindow.xaml` Element `<Grid>` ein, das das Element `WebView2` enthält.</span><span class="sxs-lookup"><span data-stu-id="38330-168">In the `MainWindow.xaml` file, copy and paste the following code snippet inside the `<Grid>` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="38330-169">Stellen Sie `<Grid>` sicher, dass das Element in `MainWindow.xaml` der Datei dem folgenden Codeausschnitt ähnelt.</span><span class="sxs-lookup"><span data-stu-id="38330-169">Ensure your `<Grid>` element in the `MainWindow.xaml` file is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="38330-170">Kopieren Sie in der Datei den folgenden Codeausschnitt in , der das WebView2-Steuerelement zu der in der `MainWindow.xaml.cs` `myButton_Click` Adressleiste eingegebenen URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="38330-170">In the `MainWindow.xaml.cs` file, copy the following code snippet into `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="38330-171">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="38330-171">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="38330-172">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie dann **Go aus.**</span><span class="sxs-lookup"><span data-stu-id="38330-172">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="38330-173">Geben Sie z. B. `https://www.bing.com` ein.</span><span class="sxs-lookup"><span data-stu-id="38330-173">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="38330-174">Stellen Sie sicher, dass Sie vollständige URLs in der Adressleiste eingeben.</span><span class="sxs-lookup"><span data-stu-id="38330-174">Ensure you enter complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="38330-175">Ausnahmen werden ausgelöst, wenn die URL nicht mit oder `http://` `https://` beginnt.</span><span class="sxs-lookup"><span data-stu-id="38330-175">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="38330-177">bing.com</span><span class="sxs-lookup"><span data-stu-id="38330-177">bing.com</span></span>  
    :::image-end:::  
    
## <a name="step-4---navigation-events"></a><span data-ttu-id="38330-178">Schritt 4 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="38330-178">Step 4 - Navigation events</span></span>  

<span data-ttu-id="38330-179">Apps, die WebView2-Steuerelemente hosten, lauschen auf die folgenden Ereignisse, die von WebView2-Steuerelementen während der Webseitennavigation ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="38330-179">Apps that host WebView2 controls listen for the following events that are raised by WebView2 controls during webpage navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="38330-180">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="38330-180">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="38330-181">Weitere Informationen finden Sie unter [Navigationsereignisse][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="38330-181">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="38330-182">Wenn Fehler auftreten, werden die folgenden Ereignisse ausgelöst und können zu einer Fehlerwebseite navigieren.</span><span class="sxs-lookup"><span data-stu-id="38330-182">When errors occur, the following events are raised and may navigate to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="38330-183">Als Beispiel für die Verwendung der Ereignisse registrieren Sie einen Handler, `NavigationStarting` der alle Nicht-HTTPS-Anforderungen abbricht.</span><span class="sxs-lookup"><span data-stu-id="38330-183">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  <span data-ttu-id="38330-184">Ändern `MainWindow.xaml.cs` Sie in den Konstruktor so, dass er registriert wird, und fügen Sie die Funktion so hinzu, dass sie dem folgenden `EnsureHttps` `EnsureHttps` Codeausschnitt entspricht.</span><span class="sxs-lookup"><span data-stu-id="38330-184">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="38330-185">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="38330-185">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="38330-186">Stellen Sie sicher, dass die Navigation für HTTP-Websites blockiert ist und für HTTPS-Websites zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="38330-186">Ensure navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <a name="step-5---scripting"></a><span data-ttu-id="38330-187">Schritt 5 – Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="38330-187">Step 5 - Scripting</span></span>  

<span data-ttu-id="38330-188">Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.</span><span class="sxs-lookup"><span data-stu-id="38330-188">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="38330-189">Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.</span><span class="sxs-lookup"><span data-stu-id="38330-189">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="38330-190">Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="38330-190">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="38330-191">Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38330-191">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="38330-192">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="38330-192">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="38330-193">Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="38330-193">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="38330-194">Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="38330-194">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="38330-195">Ändern Sie `EnsureHttps` die Funktion, um ein Skript in den Webinhalt zu injizieren, der [ExecuteScriptAsync verwendet.][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]</span><span class="sxs-lookup"><span data-stu-id="38330-195">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="38330-196">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="38330-196">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="38330-197">Stellen Sie sicher, dass Ihre App eine Warnung anzeigt, wenn Sie zu websites navigieren, die keine HTTPS-Websites sind.</span><span class="sxs-lookup"><span data-stu-id="38330-197">Ensure your app displays an alert when you navigate to any non-HTTPS websites.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="WebView2-Steuerelement zeigt ein Warnungsdialogfeld an" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="38330-199">WebView2-Steuerelement zeigt ein Warnungsdialogfeld an</span><span class="sxs-lookup"><span data-stu-id="38330-199">WebView2 control displays an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="38330-200">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="38330-200">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="38330-201">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="38330-201">Next steps</span></span>  

<span data-ttu-id="38330-202">Navigieren Sie zu den folgenden Ressourcen, um weitere Informationen zu WebView2 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38330-202">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <a name="see-also"></a><span data-ttu-id="38330-203">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="38330-203">See also</span></span>  

*   <span data-ttu-id="38330-204">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="38330-204">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="38330-205">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="38330-205">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="38330-206">Das WinRT CoreWebView2-Objekt ist möglicherweise nicht mit der Version der WebView2-API verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38330-206">The WinRT CoreWebView2 object may not be available with the release of the WebView2 API.</span></span>  <span data-ttu-id="38330-207">Um zu verstehen, welche APIs für WebView2-Steuerelemente verfügbar sind, navigieren Sie zu [WebView2 Spec,][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] um eine Liste der verfügbaren APIs zu finden.</span><span class="sxs-lookup"><span data-stu-id="38330-207">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  
    
*   <span data-ttu-id="38330-208">Ausführliche Informationen zur WebView2-API finden Sie unter [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="38330-208">For detailed information about the WebView2 API, navigate to [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="38330-209">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="38330-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<span data-ttu-id="38330-210">Um Ihre WinUI-spezifischen Featureanforderungen oder Fehler zu senden, navigieren Sie zu [Probleme - microsoft/microsoft-ui-xaml,][GithubMicrosoftMicrosoftUiXamlIssues] und wählen Sie **Neues Problem aus.**</span><span class="sxs-lookup"><span data-stu-id="38330-210">To send your WinUI-specific feature requests or bugs, navigate to [Issues - microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] and choose **New issue**.</span></span>  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Allgemeine NuGet-Konfigurationen | Microsoft Docs"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Paketmanifestschemareferenz für Windows 10-| Microsoft Docs"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installieren ohne Verwenden des Dialogfelds Erweiterungen verwalten – Verwalten von Erweiterungen für Visual Studio | Microsoft Docs"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Konfigurieren Ihrer Entwicklungsumgebung – Windows UI Library 3.0 Preview 1 (Mai 2020) | Microsoft Docs"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Dokumentation zu Windows Community Toolkit | Microsoft Docs"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Richten Sie Ihre Desktopanwendung für die MSIX-Verpackung in Visual Studio | Microsoft Docs"  
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

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "WinUI 3 Project Templates | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer" 
