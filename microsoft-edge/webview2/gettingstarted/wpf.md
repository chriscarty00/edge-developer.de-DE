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
# <span data-ttu-id="188af-104">Erste Schritte mit WebView2 in WPF</span><span class="sxs-lookup"><span data-stu-id="188af-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="188af-105">In diesem Artikel beginnen Sie mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Wichtigsten Features von [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="188af-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="188af-106">Weitere Informationen zu einzelnen APIs finden Sie in der [API-Referenz.][DotnetApiMicrosoftWebWebview2Wpf]</span><span class="sxs-lookup"><span data-stu-id="188af-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Wpf].</span></span>  

## <span data-ttu-id="188af-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="188af-107">Prerequisites</span></span>  

<span data-ttu-id="188af-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="188af-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="188af-109">[WebView2 Runtime][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen \(derzeit Windows 10, Windows 8.1 und Windows 7\ installiert ist).</span><span class="sxs-lookup"><span data-stu-id="188af-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
*   <span data-ttu-id="188af-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.</span><span class="sxs-lookup"><span data-stu-id="188af-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
## <span data-ttu-id="188af-111">Schritt 1: Erstellen einer App mit einem Fenster</span><span class="sxs-lookup"><span data-stu-id="188af-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="188af-112">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="188af-112">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="188af-113">Wählen Visual Studio **WPF .NET Core App** \(oder **WPF .NET Framework App**\) > Weiter **aus.**</span><span class="sxs-lookup"><span data-stu-id="188af-113">In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF Core":::
             <span data-ttu-id="188af-115">WPF Core</span><span class="sxs-lookup"><span data-stu-id="188af-115">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF Framework":::
             <span data-ttu-id="188af-117">WPF Framework</span><span class="sxs-lookup"><span data-stu-id="188af-117">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="188af-118">Geben Sie Werte für **den Projektnamen und** den **Speicherort ein.**</span><span class="sxs-lookup"><span data-stu-id="188af-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="188af-119">Wählen **Sie .NET Framework 4.6.2** oder höher \(oder **.NET Core 3.0** oder höher\) aus.</span><span class="sxs-lookup"><span data-stu-id="188af-119">Choose **.NET Framework 4.6.2** or later \(or **.NET Core 3.0** or later\).</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Kern erstellen":::
                 <span data-ttu-id="188af-121">Kern erstellen</span><span class="sxs-lookup"><span data-stu-id="188af-121">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Erstellen eines Frameworks":::
                 <span data-ttu-id="188af-123">Erstellen eines Frameworks</span><span class="sxs-lookup"><span data-stu-id="188af-123">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="188af-124">Um Ihr Projekt zu erstellen, wählen Sie **"Erstellen"** aus.</span><span class="sxs-lookup"><span data-stu-id="188af-124">To create your project, choose **Create**.</span></span>  
    
## <span data-ttu-id="188af-125">Schritt 2: Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="188af-125">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="188af-126">Verwenden Sie NuGet, um dem Projekt das WebView2 SDK hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="188af-126">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="188af-127">Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(Rechtsklick\), und wählen Sie **NuGet-Pakete verwalten...** aus.</span><span class="sxs-lookup"><span data-stu-id="188af-127">Hover on the projecty, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet-Pakete verwalten":::
       <span data-ttu-id="188af-129">NuGet-Pakete verwalten</span><span class="sxs-lookup"><span data-stu-id="188af-129">Manage NuGet packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="188af-130">Geben Sie in der Suchleiste > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2 aus.**</span><span class="sxs-lookup"><span data-stu-id="188af-130">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="188af-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="188af-132">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="188af-133">Bereit für die Entwicklung von Apps mithilfe der WebView2-API.</span><span class="sxs-lookup"><span data-stu-id="188af-133">Ready to start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="188af-134">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="188af-134">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="188af-135">Das ausgeführte Projekt zeigt ein leeres Fenster an.</span><span class="sxs-lookup"><span data-stu-id="188af-135">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Leere App":::
       <span data-ttu-id="188af-137">Leere App</span><span class="sxs-lookup"><span data-stu-id="188af-137">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="188af-138">Schritt 3: Erstellen einer einzelnen WebView in "MainWindow.xaml"</span><span class="sxs-lookup"><span data-stu-id="188af-138">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="188af-139">Fügen Sie als Nächstes Ihrer App eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="188af-139">Next add a WebView to your app.</span></span>  

1.  <span data-ttu-id="188af-140">Fügen Sie in der Datei die folgende Zeile in das Tag ein, um den `MainWindow.xaml` WebView2-XAML-Namespace `<Window/>` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="188af-140">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="188af-141">Stellen Sie sicher, dass der Code `MainWindow.xaml` in wie der folgende Codeausschnitt aussieht.</span><span class="sxs-lookup"><span data-stu-id="188af-141">Ensure the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="188af-142">Ersetzen Sie zum Hinzufügen des WebView2-Steuerelements die `<Grid>` Tags durch den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="188af-142">To add the WebView2 control, replace the `<Grid>` tags with the following code snippet.</span></span>  <span data-ttu-id="188af-143">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="188af-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="188af-144">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5`  "WebView2-Steuerelement anzeigen" [https://www.microsoft.com][|::ref1::|Main] aus.</span><span class="sxs-lookup"><span data-stu-id="188af-144">To build and run the project, select `F5`  Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="188af-146">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="188af-146">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="188af-147">Schritt 4: Navigation</span><span class="sxs-lookup"><span data-stu-id="188af-147">Step 4 - Navigation</span></span>  

<span data-ttu-id="188af-148">Fügen Sie die Möglichkeit hinzu, Benutzern das Ändern der URL zu ermöglichen, die das WebView2-Steuerelement anzeigt, indem Sie der App eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="188af-148">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="188af-149">Fügen Sie in der Datei eine Adressleiste hinzu, indem Sie den folgenden Codeausschnitt in den Codeausschnitt kopieren und einfügen, der `MainWindow.xaml` `<DockPanel>` die WebView enthält.</span><span class="sxs-lookup"><span data-stu-id="188af-149">In the `MainWindow.xaml` file, add an address bar by copying and pasting the following code snippet inside the `<DockPanel>` that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="188af-150">Stellen Sie `<DockPanel>` sicher, dass der Abschnitt `MainWindow.xaml` der Datei mit dem folgenden Codeausschnitt entspricht.</span><span class="sxs-lookup"><span data-stu-id="188af-150">Ensure the `<DockPanel>` section of the `MainWindow.xaml` file matches the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="188af-151">Fügen Visual Studio Codeausschnitt oben in die Datei ein, um den `MainWindow.xaml.cs` `CoreWebView2` Namespace hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="188af-151">In Visual Studio, in the `MainWindow.xaml.cs` file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="188af-152">Kopieren Sie in der Datei den folgenden Codeausschnitt, um die Methode zu erstellen, die die WebView zu der in der Adressleiste `MainWindow.xaml.cs` `ButtonGo_Click` eingegebenen URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="188af-152">In the `MainWindow.xaml.cs`file, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="188af-153">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="188af-153">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="188af-154">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **"Los" aus.**</span><span class="sxs-lookup"><span data-stu-id="188af-154">Type a new URL in the address bar and choose **Go**.</span></span>  <span data-ttu-id="188af-155">Geben Sie beispielsweise `https://www.bing.com` ein.</span><span class="sxs-lookup"><span data-stu-id="188af-155">For example, type `https://www.bing.com`.</span></span>  <span data-ttu-id="188af-156">Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="188af-156">Ensure the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="188af-157">Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="188af-157">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="188af-158">Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://` `https://` beginnt.</span><span class="sxs-lookup"><span data-stu-id="188af-158">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="188af-160">bing.com</span><span class="sxs-lookup"><span data-stu-id="188af-160">bing.com</span></span>
    :::image-end:::
    
## <span data-ttu-id="188af-161">Schritt 5: Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="188af-161">Step 5 - Navigation events</span></span>  

<span data-ttu-id="188af-162">Während der Webseitennavigation löst das WebView2-Steuerelement Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="188af-162">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="188af-163">Die App, die WebView2-Steuerelemente hostet, lauscht auf die folgenden Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="188af-163">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="188af-164">Navigieren Sie zu [Navigationsereignissen, um weitere Informationen zu erhalten.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="188af-164">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="188af-166">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="188af-166">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="188af-167">Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und sind möglicherweise von der Navigation zu einer Fehlerwebseite abhängig.</span><span class="sxs-lookup"><span data-stu-id="188af-167">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="188af-168">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="188af-168">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="188af-169">Um die Verwendung der Ereignisse zu veranschaulichen, registrieren Sie einen Handler, der alle `NavigationStarting` Nicht-HTTPS-Anforderungen abbricht.</span><span class="sxs-lookup"><span data-stu-id="188af-169">To demonstrate how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  

<span data-ttu-id="188af-170">Ändern Sie in der Datei den Konstruktor so, dass er mit dem `MainWindow.xaml.cs` folgenden Codeausschnitt übereinstimmen kann, und fügen Sie die Funktion `EnsureHttps` hinzu.</span><span class="sxs-lookup"><span data-stu-id="188af-170">In the `MainWindow.xaml.cs` file, modify the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="188af-171">Im Konstruktor wird EnsureHttps als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.</span><span class="sxs-lookup"><span data-stu-id="188af-171">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="188af-172">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="188af-172">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="188af-173">Stellen Sie sicher, dass die WebView beim Navigieren zu einer HTTP-Website unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="188af-173">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="188af-174">Die WebView navigiert jedoch zu HTTPS-Websites.</span><span class="sxs-lookup"><span data-stu-id="188af-174">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="188af-175">Schritt 6: Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="188af-175">Step 6 - Scripting</span></span>  

<span data-ttu-id="188af-176">Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.</span><span class="sxs-lookup"><span data-stu-id="188af-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="188af-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span><span class="sxs-lookup"><span data-stu-id="188af-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="188af-178">Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="188af-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="188af-179">Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="188af-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="188af-180">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="188af-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="188af-181">Führen Sie es aus, bevor ein anderes Im HTML-Dokument enthaltenes Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="188af-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="188af-182">Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="188af-182">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="188af-183">Ändern Sie die Funktion, um ein Skript in den Webinhalt zu injizieren, `EnsureHttps` der die [ExecuteScriptAsync-Methode](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) verwendet.</span><span class="sxs-lookup"><span data-stu-id="188af-183">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="188af-184">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="188af-184">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="188af-185">Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="188af-185">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="188af-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="188af-187">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="188af-188">Schritt 7: Kommunikation zwischen Host- und Webinhalt</span><span class="sxs-lookup"><span data-stu-id="188af-188">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="188af-189">Host- und Webinhalte können wie folgt miteinander `postMessage` kommunizieren:</span><span class="sxs-lookup"><span data-stu-id="188af-189">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="188af-190">Webinhalte in einem WebView2-Steuerelement können eine Nachricht mithilfe von . `window.chrome.webview.postMessage`</span><span class="sxs-lookup"><span data-stu-id="188af-190">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="188af-191">Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="188af-191">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="188af-192">Hostet Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="188af-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="188af-193">Diese Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` wurden.</span><span class="sxs-lookup"><span data-stu-id="188af-193">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="188af-194">Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.</span><span class="sxs-lookup"><span data-stu-id="188af-194">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="188af-195">Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, zeigt es die URL in der Adressleiste an und benachrichtigt den Benutzer über die im WebView2-Steuerelement angezeigte URL.</span><span class="sxs-lookup"><span data-stu-id="188af-195">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="188af-196">Aktualisieren Sie in der Datei den Konstruktor, und erstellen Sie eine `MainWindow.xaml.cs` `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="188af-196">In the `MainWindow.xaml.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="188af-197">Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) da die Initialisierung `CoreWebView2` asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="188af-197">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="188af-198">Nachdem **CoreWebView2** initialisiert wurde, registrieren Sie einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.</span><span class="sxs-lookup"><span data-stu-id="188af-198">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="188af-199">Aktualisieren `MainWindow.xaml.cs` und hinzufügen Sie in mithilfe des folgenden `InitializeAsync` `UpdateAddressBar` Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="188af-199">In `MainWindow.xaml.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="188af-200">Damit webView die Webnachricht senden und darauf antworten kann, wird nach der `CoreWebView2` Initialisierung der Host:</span><span class="sxs-lookup"><span data-stu-id="188af-200">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    1.  <span data-ttu-id="188af-201">Injects a script to the web content that registers a handler to print message from the host.</span><span class="sxs-lookup"><span data-stu-id="188af-201">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="188af-202">Injects a script to the web content that posts the URL to the host.</span><span class="sxs-lookup"><span data-stu-id="188af-202">Injects a script to the web content that posts the URL to the host.</span></span>  
        
    <span data-ttu-id="188af-203">Aktualisieren Sie `MainWindow.xaml.cs` in der Datei so, dass sie mit `InitializeAsync` dem folgenden Codeausschnitt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="188af-203">In the `MainWindow.xaml.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="188af-204">Wählen Sie zum Erstellen und Ausführen der App die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="188af-204">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="188af-205">Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="188af-205">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="188af-206">Wenn Sie erfolgreich zu einem neuen URI navigieren, warnt das WebView2-Steuerelement den Benutzer über den URI, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="188af-206">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="188af-208">addressBar</span><span class="sxs-lookup"><span data-stu-id="188af-208">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="188af-209">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="188af-209">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="188af-210">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="188af-210">Next steps</span></span>  

<span data-ttu-id="188af-211">Um weitere Informationen zu WebView2 zu erhalten, navigieren Sie zu den folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="188af-211">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="188af-212">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="188af-212">See also</span></span>  

*   <span data-ttu-id="188af-213">Ein umfassendes Beispiel der WebView2-Funktionen finden Sie im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samplesMain] auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="188af-213">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] on GitHub.</span></span>  
*   <span data-ttu-id="188af-214">Ausführlichere Informationen zur WebView2-API finden Sie in der [API-Referenz.](/dotnet/api/microsoft.web.webview2.wpf.webview2)</span><span class="sxs-lookup"><span data-stu-id="188af-214">For more detailed information about WebView2 API, navigate to [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="188af-215">Weitere Informationen zu WebView2 finden Sie unter ["WebView2-Ressourcen".](../index.md#next-steps)</span><span class="sxs-lookup"><span data-stu-id="188af-215">For more information about  WebView2, navigate to [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="188af-216">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="188af-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

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