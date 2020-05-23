---
description: Hosten von Webinhalten in Ihrer WPF-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge WebView 2 für WPF-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WPF-apps, WPF, Edge, CoreWebView2, Browser-Steuerelement, Edge-HTML, erste Schritte, erste Schritte, .net
ms.openlocfilehash: 6e66d90c3b821ee3656466ccaf3c9a079dda5030
ms.sourcegitcommit: e00e783926877090116e650da25242498173a7fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2020
ms.locfileid: "10673956"
---
# <span data-ttu-id="ae4b4-104">Erste Schritte mit WebView2 in WPF (Preview)</span><span class="sxs-lookup"><span data-stu-id="ae4b4-104">Getting Started with WebView2 in WPF (Preview)</span></span>  

<span data-ttu-id="ae4b4-105">In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-app erstellen und die wichtigsten Features von [WebView2 (Preview)](/microsoft-edge/hosting/webview2/index)kennenlernen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="ae4b4-106">Weitere Informationen zu einzelnen APIs finden Sie unter [API-Referenz](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="ae4b4-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="ae4b4-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ae4b4-107">Prerequisites</span></span>  

<span data-ttu-id="ae4b4-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installiert haben, bevor Sie fortfahren:</span><span class="sxs-lookup"><span data-stu-id="ae4b4-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="ae4b4-109">[Microsoft Edge (Chrom) Canary Channel](https://www.microsoftedgeinsider.com/download/) , installiert unter Windows 10, Windows 8,1 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="ae4b4-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 oder höher</span><span class="sxs-lookup"><span data-stu-id="ae4b4-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later.</span></span>  

## <span data-ttu-id="ae4b4-111">Schritt 1 – Erstellen einer einzelnen Fenster Anwendung</span><span class="sxs-lookup"><span data-stu-id="ae4b4-111">Step 1 - Create a single window application</span></span>

<span data-ttu-id="ae4b4-112">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-112">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="ae4b4-113">Öffnen Sie **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="ae4b4-113">Open **Visual Studio.**</span></span>
2. <span data-ttu-id="ae4b4-114">Wählen Sie **WPF .net Core-App** oder **WPF .NET Framework-App**aus, und wählen Sie dann **weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-114">Choose **WPF .NET Core App** or **WPF .NET Framework App**, and then choose **Next**.</span></span>  

    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF-Kern":::
             <span data-ttu-id="ae4b4-116">WPF-Kern</span><span class="sxs-lookup"><span data-stu-id="ae4b4-116">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF-Framework":::
             <span data-ttu-id="ae4b4-118">WPF-Framework</span><span class="sxs-lookup"><span data-stu-id="ae4b4-118">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

3. <span data-ttu-id="ae4b4-119">Geben Sie Werte für **Projektname** und **Speicherort**ein.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-119">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="ae4b4-120">Wählen Sie .NET Framework 4.6.2 oder höher oder .net Core 3,0 oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-120">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  

:::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Erstellen eines Kerns":::
             <span data-ttu-id="ae4b4-122">Erstellen eines Kerns</span><span class="sxs-lookup"><span data-stu-id="ae4b4-122">Create core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Erstellen eines Frameworks":::
             <span data-ttu-id="ae4b4-124">Erstellen eines Frameworks</span><span class="sxs-lookup"><span data-stu-id="ae4b4-124">Create Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

4. <span data-ttu-id="ae4b4-125">Wählen Sie **Erstellen** aus, um Ihr Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-125">Choose **Create** to create your project.</span></span>  

## <span data-ttu-id="ae4b4-126">Schritt 2 – Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="ae4b4-126">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="ae4b4-127">Fügen Sie als nächstes das WebView2-SDK zum Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-127">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="ae4b4-128">Installieren Sie für die Vorschau das WebView2-SDK mithilfe von Nuget.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-128">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="ae4b4-129">Öffnen Sie das Kontextmenü im Projekt \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **NuGet-Pakete verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-129">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Nuget":::
       <span data-ttu-id="ae4b4-131">Nuget</span><span class="sxs-lookup"><span data-stu-id="ae4b4-131">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="ae4b4-132">Geben Sie `Microsoft.Web.WebView2` in die Suchleiste ein.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-132">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="ae4b4-133">Wählen Sie in den Suchergebnissen **Microsoft. Web. WebView2** aus.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-133">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="ae4b4-134">Legen Sie die Paketversion auf **Pre-Release**, und wählen Sie dann **Installieren**aus.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-134">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

     ![nuget](./media/installnuget.PNG)

<span data-ttu-id="ae4b4-136">Sie können mit der WebView2-API beginnen, Anwendungen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-136">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="ae4b4-137">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-137">Press `F5` to build and run the project.</span></span>  <span data-ttu-id="ae4b4-138">Im laufenden Projekt wird ein leeres Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-138">The running project displays an empty window.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Leere App":::
   <span data-ttu-id="ae4b4-140">Leere App</span><span class="sxs-lookup"><span data-stu-id="ae4b4-140">Empty app</span></span>
:::image-end:::

## <span data-ttu-id="ae4b4-141">Schritt 3 – Erstellen einer einzelnen WebView in "" "" ". XAML"</span><span class="sxs-lookup"><span data-stu-id="ae4b4-141">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="ae4b4-142">Fügen Sie Ihrer Anwendung als nächstes eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-142">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="ae4b4-143">Öffnen Sie `MainWindow.xaml`.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-143">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="ae4b4-144">Fügen Sie den WebView2-XAML-Namespace hinzu, indem Sie die folgende Zeile innerhalb der `<Window/>` Kategorie einfügen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-144">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  

    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  

    <span data-ttu-id="ae4b4-145">Vergewissern Sie sich, dass der Code in `MainWindow.xaml` wie im folgenden Codeausschnitt aussieht.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-145">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  

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
        />
        <Grid>

                </Grid>
    </Window>
    ```  

2. <span data-ttu-id="ae4b4-146">Fügen Sie das WebView2-Steuerelement hinzu, indem Sie die `<Grid>` Tags mit dem folgenden Codeausschnitt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-146">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="ae4b4-147">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-147">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  

    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  

3. <span data-ttu-id="ae4b4-148">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-148">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="ae4b4-149">Vergewissern Sie sich, dass Ihr WebView2-Steuerelement angezeigt wird [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-149">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="ae4b4-151">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ae4b4-151">Microsoft.com</span></span> :::image-end:::

## <span data-ttu-id="ae4b4-152">Schritt 4 – Navigation</span><span class="sxs-lookup"><span data-stu-id="ae4b4-152">Step 4 - Navigation</span></span>  

<span data-ttu-id="ae4b4-153">Hinzufügen der Möglichkeit, dass Benutzer die vom WebView2-Steuerelement angezeigte URL ändern können, indem Sie der App eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-153">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="ae4b4-154">Fügen Sie in "Hauptfeld **. XAML**" eine Adressleiste hinzu, indem Sie den folgenden Codeausschnitt innerhalb der DockPanel-Datei, die die WebView enthält, kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-154">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  

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

<span data-ttu-id="ae4b4-155">Vergewissern Sie sich, dass der `DockPanel` Abschnitt `MainWindow.xaml` wie im folgenden Codeausschnitt aussieht.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-155">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  

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

2. <span data-ttu-id="ae4b4-156">`MainWindow.xaml.cs`In Visual Studio öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-156">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="ae4b4-157">Fügen Sie den `CoreWebView2` Namespace hinzu, indem Sie am oberen Rand des folgenden Codeausschnitts einfügen `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-157">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

3. <span data-ttu-id="ae4b4-158">Kopieren Sie in **MainWindow.XAML.cs**den folgenden Codeausschnitt, um die `ButtonGo_Click` Methode zu erstellen, die die WebView zu der in der Adressleiste eingegebenen URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-158">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  

    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="ae4b4-159">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-159">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="ae4b4-160">Geben Sie in der Adressleiste eine neue URL ein, und klicken Sie auf **Gehe**zu.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-160">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="ae4b4-161">Geben Sie beispielsweise ein `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-161">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="ae4b4-162">Überprüfen Sie, ob das WebView2-Steuerelement zur URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-162">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="ae4b4-163">Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-163">Make sure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="ae4b4-164">Eine `ArgumentException` wird ausgelöst, wenn die URL nicht mit gestartet wird `http://` oder</span><span class="sxs-lookup"><span data-stu-id="ae4b4-164">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
   <span data-ttu-id="ae4b4-166">Bing</span><span class="sxs-lookup"><span data-stu-id="ae4b4-166">Bing</span></span>
:::image-end:::

## <span data-ttu-id="ae4b4-167">Schritt 5 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="ae4b4-167">Step 5 - Navigation events</span></span>  

<span data-ttu-id="ae4b4-168">Die Anwendung, die WebView2-Steuerelemente hostet, überwacht die folgenden Ereignisse, die vom WebView2-Steuerelement während der Navigation zu Webseiten ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-168">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="ae4b4-169">Weitere Informationen finden Sie unter [Navigationsereignisse](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="ae4b4-169">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="ae4b4-171">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="ae4b4-171">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="ae4b4-172">Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und können von der Navigation zu einer Fehlerseite abhängen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-172">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="ae4b4-173">Wenn eine HTTP-Umleitung vorhanden ist, gibt es mehrere `NavigationStarting` Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-173">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="ae4b4-174">Um zu veranschaulichen, wie diese Ereignisse verwendet werden, müssen Sie zunächst einen Handler registrieren, der `NavigationStarting` alle Anforderungen abbricht, die nicht HTTPS verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-174">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="ae4b4-175">`MainWindow.xaml.cs`Ändern Sie in den Konstruktor wie unten dargestellt, und fügen Sie die `EnsureHttps` Funktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-175">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="ae4b4-176">Im Konstruktor wird EnsureHttps als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-176">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="ae4b4-177">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-177">Press `F5` to build and run your project.</span></span> <span data-ttu-id="ae4b4-178">Vergewissern Sie sich, dass die WebView-Ansicht beim Navigieren zu einer HTTP-Website **unverändert bleibt**.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-178">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span> <span data-ttu-id="ae4b4-179">Die WebView wird jedoch zu HTTPS-Websites navigieren.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-179">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="ae4b4-180">Schritt 6 – Skripting</span><span class="sxs-lookup"><span data-stu-id="ae4b4-180">Step 6 - Scripting</span></span>  

<span data-ttu-id="ae4b4-181">Sie können Host-Anwendungen verwenden, um JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einzufügen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-181">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="ae4b4-182">Das eingefügte JavaScript gilt für alle neuen Dokumente auf oberster Ebene und für alle untergeordneten Frames, bis das JavaScript entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-182">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="ae4b4-183">Das eingefügte JavaScript wird nach der Erstellung des globalen Objekts und vor dem Ausführen eines anderen im HTML-Dokument enthaltenen Skripts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-183">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="ae4b4-184">Sie können Skripting verwenden, um den Benutzer zu benachrichtigen, wenn Sie zu einer nicht-HTTPS-Website navigieren.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-184">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="ae4b4-185">Ändern `EnsureHttps` Sie die Funktion so, dass Sie mit der [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) -Methode Skripts in den Webinhalt einfügt.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-185">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) method.</span></span>  

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

<span data-ttu-id="ae4b4-186">Drücken Sie `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-186">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="ae4b4-187">Vergewissern Sie sich, dass die Anwendung eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die nicht HTTPS verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-187">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="ae4b4-189">HTTPS</span><span class="sxs-lookup"><span data-stu-id="ae4b4-189">HTTPS</span></span>
:::image-end:::

## <span data-ttu-id="ae4b4-190">Schritt 7 – Kommunikation zwischen Host-und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="ae4b4-190">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="ae4b4-191">Die Host-und Webinhalte können mithilfe der folgenden Informationen miteinander kommunizieren `postMessage` :</span><span class="sxs-lookup"><span data-stu-id="ae4b4-191">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="ae4b4-192">Webinhalte in einem WebView2-Steuerelement senden möglicherweise eine Nachricht mithilfe von an den Host `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-192">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="ae4b4-193">Der Host verarbeitet die Nachricht mit einem `WebMessageReceived` auf dem Host registrierten Namen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-193">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="ae4b4-194">Hosts Posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mit `CoreWebView2.PostWebMessageAsString` oder `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-194">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="ae4b4-195">Diese Nachrichten werden von Handlern abgefangen, denen Sie hinzugefügt wurden `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-195">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="ae4b4-196">Mit diesem Kommunikationsmechanismus können Webinhalte Nachrichten mithilfe von systemeigenen Funktionen an den Host weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-196">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="ae4b4-197">Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt, und der Benutzer wird benachrichtigt, dass die URL im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-197">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="ae4b4-198">Aktualisieren Sie in **MainWindow.XAML.cs**den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, wie im folgenden Codeausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-198">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="ae4b4-199">Die `InitializeAsync` Funktion wartet [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) auf, da die Initialisierung von `CoreWebView2` asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-199">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

2. <span data-ttu-id="ae4b4-200">Nachdem **CoreWebView2** initialisiert wurde, registrieren Sie einen Ereignishandler, auf den Sie Antworten können `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-200">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="ae4b4-201">In **MainWindow.XAML.cs** Update `InitializeAsync` und Add `UpdateAddressBar` mit dem folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-201">In **MainWindow.xaml.cs** update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="ae4b4-202">Damit die WebView die Webnachricht senden und beantworten kann, `CoreWebView2` wird nach der Initialisierung der Host:</span><span class="sxs-lookup"><span data-stu-id="ae4b4-202">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  

    1. <span data-ttu-id="ae4b4-203">Fügt dem Webinhalt ein Skript ein, das einen Handler registriert, um eine Nachricht vom Host zu drucken.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-203">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    2. <span data-ttu-id="ae4b4-204">Fügt dem Webinhalt ein Skript hinzu, das die URL an den Host sendet.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-204">Injects a script to the web content that posts the URL to the host.</span></span>  

<span data-ttu-id="ae4b4-205">In `MainWindow.xaml.cs` , aktualisieren Sie `InitializeAsync` wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ae4b4-205">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="ae4b4-206">Drücken Sie `F5` , um die APP zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-206">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="ae4b4-207">Die Adressleiste zeigt nun den URI in der WebView an, und wenn Sie erfolgreich zu einem neuen URI navigieren, benachrichtigt die WebView den Benutzer des in der WebView angezeigten URIs.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-207">Now the address bar displays the URI in the WebView and when you successfully navigate to a new URI, the WebView alerts the user of the URI displayed in the WebView.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
   <span data-ttu-id="ae4b4-209">addressBar</span><span class="sxs-lookup"><span data-stu-id="ae4b4-209">addressBar</span></span>
:::image-end:::

<span data-ttu-id="ae4b4-210">Herzlichen Glückwunsch, Sie haben ihre erste WebView2-App erstellt!</span><span class="sxs-lookup"><span data-stu-id="ae4b4-210">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="ae4b4-211">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ae4b4-211">Next Steps</span></span>  

<span data-ttu-id="ae4b4-212">Es gibt viele WebView2-Funktionen, die in dieser exemplarischen Vorgehensweise nicht behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-212">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>  

<span data-ttu-id="ae4b4-213">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ae4b4-213">To learn more:</span></span>  

* <span data-ttu-id="ae4b4-214">Detaillierte Informationen zu den einzelnen APIs finden Sie unter [API-Referenz](../reference/dotnet/0-9-515-reference-webview2.md) .</span><span class="sxs-lookup"><span data-stu-id="ae4b4-214">Please explore [API reference](../reference/dotnet/0-9-515-reference-webview2.md) for detailed information about each API.</span></span>  

## <span data-ttu-id="ae4b4-215">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="ae4b4-215">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="ae4b4-216">Helfen Sie, ein reicheres WebView2-Erlebnis zu schaffen, indem Sie Ihr Feedback austauschen!</span><span class="sxs-lookup"><span data-stu-id="ae4b4-216">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="ae4b4-217">Besuchen Sie das Feedback- [Repo](https://aka.ms/webviewfeedback) von Microsoft Edge WebView, um Funktionsanforderungen oder Fehlerberichte zu übermitteln oder nach bekannten Problemen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ae4b4-217">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
