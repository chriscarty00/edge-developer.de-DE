---
description: Leitfaden für erste Schritte mit WebView2 für WPF-apps
title: Erste Schritte mit WebView2 für WPF-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WPF-apps, WPF, Edge, CoreWebView2, Browser-Steuerelement, Edge-HTML, erste Schritte, erste Schritte, .net
ms.openlocfilehash: e928dae0aa63f15ca5fa21860c83fa5529e905df
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182374"
---
# <span data-ttu-id="38a9e-104">Erste Schritte mit WebView2 in WPF</span><span class="sxs-lookup"><span data-stu-id="38a9e-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="38a9e-105">In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-app erstellen und Informationen zu den Hauptfeatures von [WebView2](../index.md)erhalten.</span><span class="sxs-lookup"><span data-stu-id="38a9e-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2](../index.md).</span></span>  <span data-ttu-id="38a9e-106">Weitere Informationen zu einzelnen APIs finden Sie unter [API-Referenz](/dotnet/api/microsoft.web.webview2.wpf).</span><span class="sxs-lookup"><span data-stu-id="38a9e-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf).</span></span>  

## <span data-ttu-id="38a9e-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="38a9e-107">Prerequisites</span></span>  

<span data-ttu-id="38a9e-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installiert haben, bevor Sie fortfahren:</span><span class="sxs-lookup"><span data-stu-id="38a9e-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="38a9e-109">[WebView2-Runtime][Webview2Installer] oder ein [nicht stabiler Microsoft Edge (Chrom) Canary-Kanal](https://www.microsoftedgeinsider.com/download) , der unter Windows 10, Windows 8,1 oder Windows 7 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="38a9e-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span>  
* <span data-ttu-id="38a9e-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 oder höher</span><span class="sxs-lookup"><span data-stu-id="38a9e-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>  

## <span data-ttu-id="38a9e-111">Schritt 1 – Erstellen einer einzelnen Fenster Anwendung</span><span class="sxs-lookup"><span data-stu-id="38a9e-111">Step 1 - Create a single window application</span></span>  

<span data-ttu-id="38a9e-112">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="38a9e-112">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="38a9e-113">Öffnen Sie **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="38a9e-113">Open **Visual Studio**.</span></span>  
1.  <span data-ttu-id="38a9e-114">Wählen Sie **WPF .net Core-App** oder **WPF .NET Framework-App**aus, und wählen Sie dann **weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="38a9e-114">Select **WPF .NET Core App** or **WPF .NET Framework App**, and then select **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF-Kern":::
             <span data-ttu-id="38a9e-116">WPF-Kern</span><span class="sxs-lookup"><span data-stu-id="38a9e-116">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF-Framework":::
             <span data-ttu-id="38a9e-118">WPF-Framework</span><span class="sxs-lookup"><span data-stu-id="38a9e-118">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="38a9e-119">Geben Sie Werte für **Projektname** und **Speicherort**ein.</span><span class="sxs-lookup"><span data-stu-id="38a9e-119">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="38a9e-120">Wählen Sie .NET Framework 4.6.2 oder höher oder .net Core 3,0 oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="38a9e-120">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Erstellen eines Kerns":::
                 <span data-ttu-id="38a9e-122">Erstellen eines Kerns</span><span class="sxs-lookup"><span data-stu-id="38a9e-122">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Erstellen eines Frameworks":::
                 <span data-ttu-id="38a9e-124">Erstellen eines Frameworks</span><span class="sxs-lookup"><span data-stu-id="38a9e-124">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="38a9e-125">Wählen Sie **Erstellen** aus, um Ihr Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-125">Select **Create** to create your project.</span></span>  
    
## <span data-ttu-id="38a9e-126">Schritt 2 – Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="38a9e-126">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="38a9e-127">Als Nächstes fügen Sie das WebView2-SDK mit NuGet zum Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="38a9e-127">Next add the WebView2 SDK to the project using NuGet.</span></span>  

1.  <span data-ttu-id="38a9e-128">Öffnen Sie das Kontextmenü im Projekt \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **NuGet-Pakete verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="38a9e-128">Open the context menu on the project \(right-click\), and select **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="38a9e-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="38a9e-130">NuGet</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="38a9e-131">Geben Sie `Microsoft.Web.WebView2` in die Suchleiste ein.</span><span class="sxs-lookup"><span data-stu-id="38a9e-131">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="38a9e-132">Wählen Sie in den Suchergebnissen **Microsoft. Web. WebView2** aus.</span><span class="sxs-lookup"><span data-stu-id="38a9e-132">Select **Microsoft.Web.WebView2** from the search results.</span></span>  
   
     ![nuget](./media/installnuget.PNG)
    
    <span data-ttu-id="38a9e-134">Mit der WebView2-API können Sie nun mit der Entwicklung von Anwendungen beginnen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-134">You're all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="38a9e-135">Wählen Sie aus `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-135">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="38a9e-136">Im laufenden Projekt wird ein leeres Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38a9e-136">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Leere App":::
       <span data-ttu-id="38a9e-138">Leere App</span><span class="sxs-lookup"><span data-stu-id="38a9e-138">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="38a9e-139">Schritt 3 – Erstellen einer einzelnen WebView in "" "" ". XAML"</span><span class="sxs-lookup"><span data-stu-id="38a9e-139">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="38a9e-140">Fügen Sie Ihrer Anwendung als nächstes eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="38a9e-140">Next add a WebView to your application.</span></span>  

1.  <span data-ttu-id="38a9e-141">Öffnen Sie `MainWindow.xaml`.</span><span class="sxs-lookup"><span data-stu-id="38a9e-141">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="38a9e-142">Fügen Sie den WebView2-XAML-Namespace hinzu, indem Sie die folgende Zeile innerhalb der `<Window/>` Kategorie einfügen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-142">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="38a9e-143">Vergewissern Sie sich, dass der Code in `MainWindow.xaml` wie im folgenden Codeausschnitt aussieht.</span><span class="sxs-lookup"><span data-stu-id="38a9e-143">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="38a9e-144">Fügen Sie das WebView2-Steuerelement hinzu, indem Sie die `<Grid>` Tags mit dem folgenden Codeausschnitt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-144">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="38a9e-145">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38a9e-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="38a9e-146">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-146">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="38a9e-147">Vergewissern Sie sich, dass Ihr WebView2-Steuerelement angezeigt wird [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="38a9e-147">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="38a9e-149">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="38a9e-149">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="38a9e-150">Schritt 4 – Navigation</span><span class="sxs-lookup"><span data-stu-id="38a9e-150">Step 4 - Navigation</span></span>  

<span data-ttu-id="38a9e-151">Hinzufügen der Möglichkeit, dass Benutzer die vom WebView2-Steuerelement angezeigte URL ändern können, indem Sie der App eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-151">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="38a9e-152">Fügen Sie in "Hauptfeld **. XAML**" eine Adressleiste hinzu, indem Sie den folgenden Codeausschnitt innerhalb der DockPanel-Datei, die die WebView enthält, kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-152">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="38a9e-153">Vergewissern Sie sich, dass der `DockPanel` Abschnitt `MainWindow.xaml` wie im folgenden Codeausschnitt aussieht.</span><span class="sxs-lookup"><span data-stu-id="38a9e-153">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="38a9e-154">`MainWindow.xaml.cs`In Visual Studio öffnen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-154">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="38a9e-155">Fügen Sie den `CoreWebView2` Namespace hinzu, indem Sie am oberen Rand des folgenden Codeausschnitts einfügen `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="38a9e-155">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="38a9e-156">Kopieren Sie in **MainWindow.XAML.cs**den folgenden Codeausschnitt, um die `ButtonGo_Click` Methode zu erstellen, die die WebView zu der in der Adressleiste eingegebenen URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="38a9e-156">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="38a9e-157">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-157">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="38a9e-158">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **dann gehe**zu aus.</span><span class="sxs-lookup"><span data-stu-id="38a9e-158">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="38a9e-159">Geben Sie beispielsweise ein `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="38a9e-159">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="38a9e-160">Überprüfen Sie, ob das WebView2-Steuerelement zur URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="38a9e-160">Confirm that the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="38a9e-161">Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="38a9e-161">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="38a9e-162">Eine `ArgumentException` wird ausgelöst, wenn die URL nicht mit `http://` oder beginnt `https://` .</span><span class="sxs-lookup"><span data-stu-id="38a9e-162">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="38a9e-164">Bing</span><span class="sxs-lookup"><span data-stu-id="38a9e-164">Bing</span></span>
    :::image-end:::
    
## <span data-ttu-id="38a9e-165">Schritt 5 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="38a9e-165">Step 5 - Navigation events</span></span>  

<span data-ttu-id="38a9e-166">Während der Webseiten Navigation löst das WebView2-Steuerelementereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="38a9e-166">During webpage navigation, the WebView2 control raises events.</span></span> <span data-ttu-id="38a9e-167">Die Anwendung, die WebView2-Steuerelemente hostet, überwacht die folgenden Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="38a9e-167">The application that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="38a9e-168">Weitere Informationen finden Sie unter [Navigationsereignisse](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="38a9e-168">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="38a9e-170">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="38a9e-170">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="38a9e-171">Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und können von der Navigation zu einer Fehlerseite abhängen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-171">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

<span data-ttu-id="38a9e-172">Wenn eine HTTP-Umleitung vorhanden ist, gibt es mehrere `NavigationStarting` Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="38a9e-172">When there's an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="38a9e-173">Um zu veranschaulichen, wie diese Ereignisse verwendet werden, müssen Sie zunächst einen Handler registrieren, der `NavigationStarting` alle Anforderungen abbricht, die kein HTTPS verwenden.</span><span class="sxs-lookup"><span data-stu-id="38a9e-173">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="38a9e-174">`MainWindow.xaml.cs`Ändern Sie in den Konstruktor wie unten dargestellt, und fügen Sie die `EnsureHttps` Funktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="38a9e-174">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="38a9e-175">Im Konstruktor wird EnsureHttps als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.</span><span class="sxs-lookup"><span data-stu-id="38a9e-175">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="38a9e-176">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-176">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="38a9e-177">Vergewissern Sie sich, dass die WebView-Ansicht beim Navigieren zu einer HTTP-Website **unverändert bleibt**.</span><span class="sxs-lookup"><span data-stu-id="38a9e-177">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span>  <span data-ttu-id="38a9e-178">Die WebView navigiert jedoch zu HTTPS-Websites.</span><span class="sxs-lookup"><span data-stu-id="38a9e-178">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="38a9e-179">Schritt 6 – Skripting</span><span class="sxs-lookup"><span data-stu-id="38a9e-179">Step 6 - Scripting</span></span>  

<span data-ttu-id="38a9e-180">Sie können Host-Anwendungen verwenden, um JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einzufügen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-180">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="38a9e-181">Das eingefügte JavaScript gilt für alle neuen Dokumente auf oberster Ebene und für alle untergeordneten Frames, bis das JavaScript entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="38a9e-181">The injected JavaScript applies to all new top-level documents and any child frames, until the JavaScript is removed.</span></span>  <span data-ttu-id="38a9e-182">Das eingefügte JavaScript wird nach der Erstellung des globalen Objekts und vor den Skripts, die im HTML-Dokument enthalten sind, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38a9e-182">The injected JavaScript is run after creation of the global object, and before any scripts included in the HTML document.</span></span>  

<span data-ttu-id="38a9e-183">Sie können Skripting verwenden, um den Benutzer zu benachrichtigen, wenn Sie zu einer nicht-HTTPS-Website navigieren.</span><span class="sxs-lookup"><span data-stu-id="38a9e-183">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="38a9e-184">Ändern `EnsureHttps` Sie die Funktion so, dass Sie mit der [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) -Methode Skripts in den Webinhalt einfügt.</span><span class="sxs-lookup"><span data-stu-id="38a9e-184">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="38a9e-185">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-185">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="38a9e-186">Vergewissern Sie sich, dass die Anwendung eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die nicht HTTPS verwendet.</span><span class="sxs-lookup"><span data-stu-id="38a9e-186">Confirm that the application displays an alert when you navigate to a site that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="38a9e-188">HTTPS</span><span class="sxs-lookup"><span data-stu-id="38a9e-188">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="38a9e-189">Schritt 7 – Kommunikation zwischen Host-und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="38a9e-189">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="38a9e-190">Die Host-und Webinhalte können mithilfe der folgenden Informationen miteinander kommunizieren `postMessage` :</span><span class="sxs-lookup"><span data-stu-id="38a9e-190">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="38a9e-191">Webinhalte in einem WebView2-Steuerelement senden möglicherweise eine Nachricht mithilfe von an den Host `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="38a9e-191">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="38a9e-192">Der Host verarbeitet die Nachricht mit einem `WebMessageReceived` auf dem Host registrierten Namen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-192">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="38a9e-193">Hosts Posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mit `CoreWebView2.PostWebMessageAsString` oder `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="38a9e-193">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="38a9e-194">Diese Nachrichten werden von Handlern abgefangen, denen Sie hinzugefügt wurden `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="38a9e-194">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="38a9e-195">Mit diesem Kommunikationsmechanismus können Webinhalte Nachrichten mithilfe von systemeigenen Funktionen an den Host weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="38a9e-195">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="38a9e-196">Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt, und der Benutzer wird benachrichtigt, dass die URL im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38a9e-196">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="38a9e-197">Aktualisieren Sie in **MainWindow.XAML.cs**den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, wie im folgenden Codeausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="38a9e-197">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="38a9e-198">Die `InitializeAsync` Funktion wartet [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) auf, da die Initialisierung von `CoreWebView2` asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="38a9e-198">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="38a9e-199">Nachdem **CoreWebView2** initialisiert wurde, registrieren Sie einen Ereignishandler, auf den Sie Antworten können `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="38a9e-199">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="38a9e-200">Aktualisieren Sie in **MainWindow.XAML.cs**, `InitializeAsync` und fügen Sie es `UpdateAddressBar` mithilfe des folgenden Codeausschnitts hinzu.</span><span class="sxs-lookup"><span data-stu-id="38a9e-200">In **MainWindow.xaml.cs**, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="38a9e-201">Damit die WebView die Webnachricht senden und beantworten kann, `CoreWebView2` wird nach der Initialisierung der Host:</span><span class="sxs-lookup"><span data-stu-id="38a9e-201">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    
    1.  <span data-ttu-id="38a9e-202">Fügt dem Webinhalt ein Skript ein, das einen Handler registriert, um eine Nachricht vom Host zu drucken.</span><span class="sxs-lookup"><span data-stu-id="38a9e-202">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="38a9e-203">Fügt dem Webinhalt ein Skript hinzu, das die URL an den Host sendet.</span><span class="sxs-lookup"><span data-stu-id="38a9e-203">Injects a script to the web content that posts the URL to the host.</span></span>  
    
    <span data-ttu-id="38a9e-204">In `MainWindow.xaml.cs` , aktualisieren Sie `InitializeAsync` wie folgt:</span><span class="sxs-lookup"><span data-stu-id="38a9e-204">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="38a9e-205">Drücken Sie `F5` , um die APP zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38a9e-205">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="38a9e-206">Nun zeigt die Adressleiste den URI im WebView2-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="38a9e-206">Now, the address bar displays the URI in the WebView2 control.</span></span> <span data-ttu-id="38a9e-207">Wenn Sie erfolgreich zu einem neuen URI navigieren, benachrichtigt das WebView2-Steuerelement den Benutzer über den URI, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38a9e-207">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="38a9e-209">addressBar</span><span class="sxs-lookup"><span data-stu-id="38a9e-209">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="38a9e-210">Herzlichen Glückwunsch, Sie haben ihre erste WebView2-App erstellt!</span><span class="sxs-lookup"><span data-stu-id="38a9e-210">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="38a9e-211">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="38a9e-211">Next steps</span></span>  

*   <span data-ttu-id="38a9e-212">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples Repo](https://github.com/MicrosoftEdge/WebView2Samples) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="38a9e-212">For a comprehensive example of WebView2 capabilities, see [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) on GitHub.</span></span>  
*   <span data-ttu-id="38a9e-213">Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span><span class="sxs-lookup"><span data-stu-id="38a9e-213">For more detailed information about WebView2 APIs, see [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="38a9e-214">Weitere Informationen zu WebView2 finden Sie unter [WebView2-Ressourcen](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="38a9e-214">For more information about  WebView2, see [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="38a9e-215">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="38a9e-215">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2-Installationsprogramm" 
