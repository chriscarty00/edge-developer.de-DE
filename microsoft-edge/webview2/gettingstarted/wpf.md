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
# <a name="getting-started-with-webview2-in-wpf"></a><span data-ttu-id="15869-104">Erste Schritte mit WebView2 in WPF</span><span class="sxs-lookup"><span data-stu-id="15869-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="15869-105">Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="15869-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="15869-106">Weitere Informationen zu einzelnen APIs finden Sie unter [API reference][DotnetApiMicrosoftWebWebview2Wpf].</span><span class="sxs-lookup"><span data-stu-id="15869-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Wpf].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="15869-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="15869-107">Prerequisites</span></span>  

<span data-ttu-id="15869-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="15869-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="15869-109">[WebView2-Laufzeit][Webview2Installer] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen installiert ist \(derzeit Windows 10, Windows 8.1 und Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="15869-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
*   <span data-ttu-id="15869-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.</span><span class="sxs-lookup"><span data-stu-id="15869-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="15869-111">Schritt 1 : Erstellen einer App mit einem Fenster</span><span class="sxs-lookup"><span data-stu-id="15869-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="15869-112">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="15869-112">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="15869-113">Wählen Visual Studio **WPF .NET Core App** \(oder **WPF .NET Framework App**\) > Weiter **aus.**</span><span class="sxs-lookup"><span data-stu-id="15869-113">In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF Core":::
             <span data-ttu-id="15869-115">WPF Core</span><span class="sxs-lookup"><span data-stu-id="15869-115">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF Framework":::
             <span data-ttu-id="15869-117">WPF Framework</span><span class="sxs-lookup"><span data-stu-id="15869-117">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="15869-118">Geben Sie Werte für **Projektname und** **Standort ein.**</span><span class="sxs-lookup"><span data-stu-id="15869-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="15869-119">Wählen **.NET Framework 4.6.2** oder höher \(oder **.NET Core 3.0** oder höher\) aus.</span><span class="sxs-lookup"><span data-stu-id="15869-119">Choose **.NET Framework 4.6.2** or later \(or **.NET Core 3.0** or later\).</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Erstellen eines Kerns":::
                 <span data-ttu-id="15869-121">Erstellen eines Kerns</span><span class="sxs-lookup"><span data-stu-id="15869-121">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Create Framework":::
                 <span data-ttu-id="15869-123">Create Framework</span><span class="sxs-lookup"><span data-stu-id="15869-123">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="15869-124">Wählen Sie Erstellen aus, um Ihr Projekt **zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="15869-124">To create your project, choose **Create**.</span></span>  
    
## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="15869-125">Schritt 2 : Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="15869-125">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="15869-126">Verwenden Sie NuGet, um das WebView2 SDK zum Projekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="15869-126">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="15869-127">Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **NuGet-Pakete verwalten...** aus.</span><span class="sxs-lookup"><span data-stu-id="15869-127">Hover on the projecty, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet-Pakete verwalten":::
       <span data-ttu-id="15869-129">NuGet-Pakete verwalten</span><span class="sxs-lookup"><span data-stu-id="15869-129">Manage NuGet packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="15869-130">Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > Wählen Sie **Microsoft.Web.WebView2 aus.**</span><span class="sxs-lookup"><span data-stu-id="15869-130">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="15869-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="15869-132">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="15869-133">Bereit zum Entwickeln von Apps mithilfe der WebView2-API.</span><span class="sxs-lookup"><span data-stu-id="15869-133">Ready to start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="15869-134">Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="15869-134">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="15869-135">Das ausgeführte Projekt zeigt ein leeres Fenster an.</span><span class="sxs-lookup"><span data-stu-id="15869-135">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Leere App" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="15869-137">Leere App</span><span class="sxs-lookup"><span data-stu-id="15869-137">Empty app</span></span>  
    :::image-end:::  
    
## <a name="step-3---create-a-single-webview"></a><span data-ttu-id="15869-138">Schritt 3 : Erstellen einer einzelnen WebView</span><span class="sxs-lookup"><span data-stu-id="15869-138">Step 3 - Create a single WebView</span></span> 

<span data-ttu-id="15869-139">Fügen Sie als Nächstes Ihrer App eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="15869-139">Next add a WebView to your app.</span></span>  

1.  <span data-ttu-id="15869-140">Fügen Sie in der Datei die folgende Zeile in das Tag ein, um den `MainWindow.xaml` WebView2-XAML-Namespace `<Window/>` hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="15869-140">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="15869-141">Stellen Sie sicher, dass der Code in `MainWindow.xaml` wie der folgende Codeausschnitt aussieht.</span><span class="sxs-lookup"><span data-stu-id="15869-141">Ensure the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="15869-142">Zum Hinzufügen des WebView2-Steuerelements ersetzen Sie die `<Grid>` Tags durch den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="15869-142">To add the WebView2 control, replace the `<Grid>` tags with the following code snippet.</span></span>  <span data-ttu-id="15869-143">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="15869-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="15869-144">Zum Erstellen und Ausführen des Projekts wählen Sie `F5`  Sicherstellen, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.</span><span class="sxs-lookup"><span data-stu-id="15869-144">To build and run the project, select `F5`  Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="15869-146">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="15869-146">Microsoft.com</span></span>
    :::image-end:::  
    
## <a name="step-4---navigation"></a><span data-ttu-id="15869-147">Schritt 4 – Navigation</span><span class="sxs-lookup"><span data-stu-id="15869-147">Step 4 - Navigation</span></span>  

<span data-ttu-id="15869-148">Fügen Sie die Möglichkeit hinzu, Benutzern das Ändern der URL zu ermöglichen, die das WebView2-Steuerelement anzeigt, indem Sie der App eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="15869-148">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="15869-149">Fügen Sie in der Datei eine Adressleiste hinzu, indem Sie den folgenden Codeausschnitt in den Codeausschnitt kopieren und einfügen, der `MainWindow.xaml` `<DockPanel>` die WebView enthält.</span><span class="sxs-lookup"><span data-stu-id="15869-149">In the `MainWindow.xaml` file, add an address bar by copying and pasting the following code snippet inside the `<DockPanel>` that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="15869-150">Stellen Sie `<DockPanel>` sicher, dass der Abschnitt `MainWindow.xaml` der Datei mit dem folgenden Codeausschnitt entspricht.</span><span class="sxs-lookup"><span data-stu-id="15869-150">Ensure the `<DockPanel>` section of the `MainWindow.xaml` file matches the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="15869-151">Fügen Visual Studio in der Datei den folgenden Codeausschnitt oben ein, um den `MainWindow.xaml.cs` `CoreWebView2` Namespace hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="15869-151">In Visual Studio, in the `MainWindow.xaml.cs` file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="15869-152">Kopieren Sie in der Datei den folgenden Codeausschnitt, um die Methode zu erstellen, die im WebView zu der URL navigiert, die in der `MainWindow.xaml.cs` `ButtonGo_Click` Adressleiste eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="15869-152">In the `MainWindow.xaml.cs`file, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="15869-153">Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="15869-153">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="15869-154">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **Los**aus.</span><span class="sxs-lookup"><span data-stu-id="15869-154">Type a new URL in the address bar and choose **Go**.</span></span>  <span data-ttu-id="15869-155">Geben Sie beispielsweise `https://www.bing.com` ein.</span><span class="sxs-lookup"><span data-stu-id="15869-155">For example, type `https://www.bing.com`.</span></span>  <span data-ttu-id="15869-156">Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="15869-156">Ensure the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="15869-157">Stellen Sie sicher, dass eine vollständige URL in der Adressleiste eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="15869-157">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="15869-158">Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://` `https://` beginnt.</span><span class="sxs-lookup"><span data-stu-id="15869-158">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="15869-160">bing.com</span><span class="sxs-lookup"><span data-stu-id="15869-160">bing.com</span></span>
    :::image-end:::
    
## <a name="step-5---navigation-events"></a><span data-ttu-id="15869-161">Schritt 5 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="15869-161">Step 5 - Navigation events</span></span>  

<span data-ttu-id="15869-162">Während der Webseitennavigation löst das WebView2-Steuerelement Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="15869-162">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="15869-163">Die App, die WebView2-Steuerelemente hostet, lauscht auf die folgenden Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="15869-163">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="15869-164">Weitere Informationen finden Sie unter [Navigationsereignisse][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="15869-164">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="15869-166">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="15869-166">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="15869-167">Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und hängen möglicherweise von der Navigation zu einer Fehlerwebseite ab.</span><span class="sxs-lookup"><span data-stu-id="15869-167">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="15869-168">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="15869-168">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="15869-169">Um die Verwendung der Ereignisse zu veranschaulichen, registrieren Sie einen Handler, `NavigationStarting` der alle Nicht-HTTPS-Anforderungen abbricht.</span><span class="sxs-lookup"><span data-stu-id="15869-169">To demonstrate how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  

<span data-ttu-id="15869-170">Ändern Sie `MainWindow.xaml.cs` in der Datei den Konstruktor, um dem folgenden Codeausschnitt zu entsprechen, und fügen Sie die Funktion `EnsureHttps` hinzu.</span><span class="sxs-lookup"><span data-stu-id="15869-170">In the `MainWindow.xaml.cs` file, modify the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="15869-171">Wird im `EnsureHttps` Konstruktor als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.</span><span class="sxs-lookup"><span data-stu-id="15869-171">In the constructor, `EnsureHttps` is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="15869-172">Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="15869-172">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="15869-173">Stellen Sie sicher, dass beim Navigieren zu einer HTTP-Website die WebView unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="15869-173">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="15869-174">Die WebView navigiert jedoch zu HTTPS-Websites.</span><span class="sxs-lookup"><span data-stu-id="15869-174">However, the WebView navigates to HTTPS sites.</span></span>  

## <a name="step-6---scripting"></a><span data-ttu-id="15869-175">Schritt 6 – Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="15869-175">Step 6 - Scripting</span></span>  

<span data-ttu-id="15869-176">Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.</span><span class="sxs-lookup"><span data-stu-id="15869-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="15869-177">Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.</span><span class="sxs-lookup"><span data-stu-id="15869-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="15869-178">Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="15869-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="15869-179">Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15869-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="15869-180">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="15869-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="15869-181">Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="15869-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="15869-182">Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="15869-182">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="15869-183">Ändern Sie `EnsureHttps` die Funktion, um ein Skript in den Webinhalt zu injizieren, der [die ExecuteScriptAsync-Methode](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) verwendet.</span><span class="sxs-lookup"><span data-stu-id="15869-183">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="15869-184">Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="15869-184">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="15869-185">Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="15869-185">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="15869-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="15869-187">HTTPS</span></span>
:::image-end:::  

## <a name="step-7---communication-between-host-and-web-content"></a><span data-ttu-id="15869-188">Schritt 7 – Kommunikation zwischen Host- und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="15869-188">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="15869-189">Host- und Webinhalte können auf folgende Weise mithilfe von `postMessage` kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="15869-189">The host and web content may communicate in the following ways using `postMessage`.</span></span>  

*   <span data-ttu-id="15869-190">Webinhalte in einem WebView2-Steuerelement können eine Nachricht mithilfe von an den Host `window.chrome.webview.postMessage` senden.</span><span class="sxs-lookup"><span data-stu-id="15869-190">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="15869-191">Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="15869-191">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="15869-192">Hosts posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="15869-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="15869-193">Die Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` werden.</span><span class="sxs-lookup"><span data-stu-id="15869-193">The messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="15869-194">Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.</span><span class="sxs-lookup"><span data-stu-id="15869-194">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="15869-195">Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt und der Benutzer über die im WebView2-Steuerelement angezeigte URL benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="15869-195">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="15869-196">Aktualisieren Sie `MainWindow.xaml.cs` in der Datei den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="15869-196">In the `MainWindow.xaml.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="15869-197">Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) da die Initialisierung `CoreWebView2` von asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="15869-197">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="15869-198">Registrieren Sie nach der Initialisierung von **CoreWebView2** einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.</span><span class="sxs-lookup"><span data-stu-id="15869-198">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="15869-199">Aktualisieren `MainWindow.xaml.cs` und hinzufügen Sie in mithilfe des folgenden `InitializeAsync` `UpdateAddressBar` Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="15869-199">In `MainWindow.xaml.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="15869-200">Damit webView die Webnachricht sendet und auf sie antwortet, wird der Host nach der `CoreWebView2` Initialisierung:</span><span class="sxs-lookup"><span data-stu-id="15869-200">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    1.  <span data-ttu-id="15869-201">Injects a script to the web content that registers a handler to print message from the host.</span><span class="sxs-lookup"><span data-stu-id="15869-201">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="15869-202">Injects a script to the web content that posts the URL to the host.</span><span class="sxs-lookup"><span data-stu-id="15869-202">Injects a script to the web content that posts the URL to the host.</span></span>  
        
    <span data-ttu-id="15869-203">Aktualisieren Sie `MainWindow.xaml.cs` in der Datei `InitializeAsync` so, dass sie mit dem folgenden Codeausschnitt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="15869-203">In the `MainWindow.xaml.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="15869-204">Wählen Sie zum Erstellen und Ausführen der App `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="15869-204">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="15869-205">Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="15869-205">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="15869-206">Wenn Sie erfolgreich zu einem neuen URI navigieren, benachrichtigt das WebView2-Steuerelement den Benutzer über den URI, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="15869-206">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="15869-208">addressBar</span><span class="sxs-lookup"><span data-stu-id="15869-208">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="15869-209">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="15869-209">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="15869-210">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="15869-210">Next steps</span></span>  

<span data-ttu-id="15869-211">Navigieren Sie zu den folgenden Ressourcen, um weitere Informationen zu WebView2 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15869-211">To continue learning more about WebView2, navigate to the following resources.</span></span>  

*   <span data-ttu-id="15869-212">Weitere Informationen zum Erstellen von WebView2-Anwendungen finden Sie unter Bewährte Methoden für [die WebView2-Entwicklung.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="15869-212">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="15869-213">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samplesMain] auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="15869-213">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] on GitHub.</span></span>  
*   <span data-ttu-id="15869-214">Weitere Informationen zur WebView2-API finden Sie unter [API-Referenz](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span><span class="sxs-lookup"><span data-stu-id="15869-214">For more detailed information about WebView2 API, navigate to [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="15869-215">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="15869-215">For more information about  WebView2, navigate to [WebView2 Resources](../index.md#next-steps).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="15869-216">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="15869-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
