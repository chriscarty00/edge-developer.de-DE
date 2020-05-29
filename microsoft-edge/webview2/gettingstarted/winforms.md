---
description: Hosten von Webinhalten in Ihrer Windows Forms-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge WebView 2 für Windows Forms-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinForms-apps, WinForms, Edge, CoreWebView2, Browser Control, Edge HTML, erste Schritte, erste Schritte, .net, Windows Forms
ms.openlocfilehash: 6c53b66dd9f849384f24c2ae879f28231a25f481
ms.sourcegitcommit: 799fe63d961a37ada455bb36ef3ef0d8076e70bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "10685687"
---
# <span data-ttu-id="02163-104">Erste Schritte mit WebView2 in Windows Forms-Apps (Preview)</span><span class="sxs-lookup"><span data-stu-id="02163-104">Getting Started with WebView2 in Windows Forms apps (Preview)</span></span>  

<span data-ttu-id="02163-105">In diesem Artikel erfahren Sie, wie Sie Ihre erste WebView2-app erstellen und die wichtigsten Features von [WebView2 (Preview)](/microsoft-edge/hosting/webview2/index)kennenlernen.</span><span class="sxs-lookup"><span data-stu-id="02163-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="02163-106">Weitere Informationen zu einzelnen APIs finden Sie unter [API-Referenz](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="02163-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="02163-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="02163-107">Prerequisites</span></span>  

<span data-ttu-id="02163-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installiert haben, bevor Sie fortfahren:</span><span class="sxs-lookup"><span data-stu-id="02163-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="02163-109">[Microsoft Edge (Chrom) Canary Channel](https://www.microsoftedgeinsider.com/download/) , installiert unter Windows 10, Windows 8,1 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02163-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="02163-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 oder höher</span><span class="sxs-lookup"><span data-stu-id="02163-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="02163-111">Wenn Sie mit **Windows Forms .net Core 3,0 oder .net 5**entwickeln, laden Sie [Visual Studio (Preview)](https://visualstudio.microsoft.com/vs/preview/) herunter.</span><span class="sxs-lookup"><span data-stu-id="02163-111">If developing with **Windows Forms .NET Core 3.0 or .NET 5**, download [Visual Studio (Preview)](https://visualstudio.microsoft.com/vs/preview/)</span></span>

## <span data-ttu-id="02163-112">Schritt 1 – Erstellen einer einzelnen Fenster Anwendung</span><span class="sxs-lookup"><span data-stu-id="02163-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="02163-113">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="02163-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="02163-114">Öffnen Sie **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="02163-114">Open **Visual Studio.**</span></span>

2. <span data-ttu-id="02163-115">Wählen Sie **Windows Forms .NET Framework-App** oder **Windows Forms .net Core-App**aus, und wählen Sie dann **weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="02163-115">Choose **Windows Forms .NET Framework App** or **Windows Forms .NET Core App**, and then choose **Next**.</span></span>

    ![NewProject](./media/winforms-newproject.png)

3. <span data-ttu-id="02163-117">Geben Sie Werte für **Projektname** und **Speicherort**ein.</span><span class="sxs-lookup"><span data-stu-id="02163-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="02163-118">Wählen Sie **.NET Framework 4.6.2** oder höher oder **.net Core 3,0** oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="02163-118">Select **.NET Framework 4.6.2** or later, or **.NET Core 3.0** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

4. <span data-ttu-id="02163-120">Wählen Sie **Erstellen** aus, um Ihr Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02163-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="02163-121">Schritt 2 – Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="02163-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="02163-122">Fügen Sie als nächstes das WebView2-SDK zum Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="02163-122">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="02163-123">Installieren Sie für die Vorschau das WebView2-SDK mithilfe von Nuget.</span><span class="sxs-lookup"><span data-stu-id="02163-123">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="02163-124">Öffnen Sie das Kontextmenü im Projekt \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **NuGet-Pakete verwalten**aus.</span><span class="sxs-lookup"><span data-stu-id="02163-124">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Nuget":::
       <span data-ttu-id="02163-126">Nuget</span><span class="sxs-lookup"><span data-stu-id="02163-126">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="02163-127">Geben Sie `Microsoft.Web.WebView2` in die Suchleiste ein.</span><span class="sxs-lookup"><span data-stu-id="02163-127">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="02163-128">Wählen Sie in den Suchergebnissen **Microsoft. Web. WebView2** aus.</span><span class="sxs-lookup"><span data-stu-id="02163-128">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="02163-129">Legen Sie die Paketversion auf **Pre-Release**, und wählen Sie dann **Installieren**aus.</span><span class="sxs-lookup"><span data-stu-id="02163-129">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

    ![nuget](./media/installnuget.png)

<span data-ttu-id="02163-131">Sie können mit der WebView2-API beginnen, Anwendungen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="02163-131">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="02163-132">Wählen Sie aus `F5` , um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="02163-132">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="02163-133">Im laufenden Projekt wird ein leeres Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02163-133">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="02163-135">Schritt 3 – Erstellen einer einzelnen WebView</span><span class="sxs-lookup"><span data-stu-id="02163-135">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="02163-136">Fügen Sie Ihrer Anwendung als nächstes eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="02163-136">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="02163-137">Öffnen Sie den **Windows Forms-Designer**.</span><span class="sxs-lookup"><span data-stu-id="02163-137">Open the **Windows Forms Designer**.</span></span>  
2. <span data-ttu-id="02163-138">Suchen Sie in der **Toolbox**nach **WebView2** .</span><span class="sxs-lookup"><span data-stu-id="02163-138">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="02163-139">Ziehen und Ablegen des **WebView2** -Steuerelements in die Windows Forms-App</span><span class="sxs-lookup"><span data-stu-id="02163-139">Drag and drop the **WebView2** control into the Windows Forms App</span></span>

    ![Toolbox](./media/winforms-toolbox.png)

3. <span data-ttu-id="02163-141">Ändern Sie die `Name`-Eigenschaft in `webView`.</span><span class="sxs-lookup"><span data-stu-id="02163-141">Change the `Name` property to `webView`.</span></span>

    ![Toolbox](./media/winforms-properties.png)

4. <span data-ttu-id="02163-143">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="02163-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="02163-144">Setzen Sie die Source-Eigenschaft auf</span><span class="sxs-lookup"><span data-stu-id="02163-144">Set the Source property to</span></span> <https://www.microsoft.com>

    ![Toolbox](./media/winforms-source.png)

<span data-ttu-id="02163-146">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="02163-146">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="02163-147">Vergewissern Sie sich, dass Ihr WebView2-Steuerelement angezeigt wird [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="02163-147">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="02163-149">Wenn Sie mit einem HD-Monitor arbeiten, müssen Sie möglicherweise [Ihre Windows Forms-App für die Unterstützung mit höherer dpi-Auflösung konfigurieren](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="02163-149">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="02163-150">Schritt 4: Behandeln von Fenstergrößen Ereignissen</span><span class="sxs-lookup"><span data-stu-id="02163-150">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="02163-151">Fügen Sie Ihren Windows Forms einige weitere Steuerelemente aus der Toolbox hinzu, und behandeln Sie die Ereignisse für die Fenstergröße entsprechend.</span><span class="sxs-lookup"><span data-stu-id="02163-151">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="02163-152">Öffnen der **Toolbox** im **Windows Forms-Designer**</span><span class="sxs-lookup"><span data-stu-id="02163-152">In the **Windows Forms Designer** open the **Toolbox**</span></span>
2. <span data-ttu-id="02163-153">Ziehen Sie ein **Textfeld** in die Windows Forms-APP, und legen Sie es ab.</span><span class="sxs-lookup"><span data-stu-id="02163-153">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="02163-154">Benennen Sie das **Textfeld** `addressBar` auf der **Registerkarte Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="02163-154">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
3. <span data-ttu-id="02163-155">Ziehen Sie eine **Schaltfläche** in die Windows Forms-APP, und legen Sie Sie ab.</span><span class="sxs-lookup"><span data-stu-id="02163-155">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="02163-156">Ändern Sie den Text in der **Schaltfläche** , `Go!` und benennen Sie die **Schaltfläche** auf `goButton` der **Registerkarte Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="02163-156">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

<span data-ttu-id="02163-157">Die APP sollte im Designer wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="02163-157">The app should look like the following in the designer:</span></span>

![-Designer](./media/winforms-designer.png)

4. <span data-ttu-id="02163-159">In **Form1.cs** definieren `Form_Resize` , um die Steuerelemente beizubehalten, wenn die Größe des App-Fensters geändert wird.</span><span class="sxs-lookup"><span data-stu-id="02163-159">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

<span data-ttu-id="02163-160">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="02163-160">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="02163-161">Vergewissern Sie sich, dass die APP ähnlich wie der folgende Screenshot angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="02163-161">Confirm that the app displays similar to the following screenshot.</span></span>

![App](./media/winforms-app.png)

## <span data-ttu-id="02163-163">Schritt 5 – Navigation</span><span class="sxs-lookup"><span data-stu-id="02163-163">Step 5 - Navigation</span></span>

<span data-ttu-id="02163-164">Hinzufügen der Möglichkeit, dass Benutzer die vom WebView2-Steuerelement angezeigte URL ändern können, indem Sie der App eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="02163-164">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="02163-165">`Form1.cs`Fügen Sie den `CoreWebView2` Namespace hinzu, indem Sie den folgenden Codeausschnitt oben auf Einfügen `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="02163-165">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

2. <span data-ttu-id="02163-166">Doppelklicken Sie im **Windows Forms-Designer**auf die `Go!` Schaltfläche, um die `goButton_Click` Methode in zu erstellen `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="02163-166">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="02163-167">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="02163-167">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="02163-168">Nun `goButton_Click` navigiert die Funktion in der WebView zu der URL, die in der Adressleiste eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="02163-168">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="02163-169">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="02163-169">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="02163-170">Geben Sie in der Adressleiste eine neue URL ein, und klicken Sie auf **Gehe**zu.</span><span class="sxs-lookup"><span data-stu-id="02163-170">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="02163-171">Geben Sie beispielsweise ein `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="02163-171">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="02163-172">Überprüfen Sie, ob das WebView2-Steuerelement zur URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="02163-172">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="02163-173">Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="02163-173">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="02163-174">Eine `ArgumentException` wird ausgelöst, wenn die URL nicht mit gestartet wird `http://` oder</span><span class="sxs-lookup"><span data-stu-id="02163-174">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="02163-176">Schritt 6 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="02163-176">Step 6 - Navigation events</span></span>  

<span data-ttu-id="02163-177">Die Anwendung, die WebView2-Steuerelemente hostet, überwacht die folgenden Ereignisse, die vom WebView2-Steuerelement während der Navigation zu Webseiten ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="02163-177">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="02163-178">Weitere Informationen finden Sie unter [Navigationsereignisse](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="02163-178">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="02163-180">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="02163-180">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="02163-181">Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und können von der Navigation zu einer Fehlerseite abhängen.</span><span class="sxs-lookup"><span data-stu-id="02163-181">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="02163-182">Wenn eine HTTP-Umleitung vorhanden ist, gibt es mehrere `NavigationStarting` Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="02163-182">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="02163-183">Um zu veranschaulichen, wie diese Ereignisse verwendet werden, müssen Sie zunächst einen Handler registrieren, der `NavigationStarting` alle Anforderungen abbricht, die nicht HTTPS verwenden.</span><span class="sxs-lookup"><span data-stu-id="02163-183">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="02163-184">`Form1.cs`Ändern Sie in den Konstruktor wie unten dargestellt, und fügen Sie die `EnsureHttps` Funktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="02163-184">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

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

<span data-ttu-id="02163-185">Im Konstruktor wird EnsureHttps als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.</span><span class="sxs-lookup"><span data-stu-id="02163-185">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="02163-186">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="02163-186">Select `F5` to build and run your project.</span></span> <span data-ttu-id="02163-187">Vergewissern Sie sich, dass die WebView-Ansicht beim Navigieren zu einer HTTP-Website unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="02163-187">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="02163-188">Die WebView wird jedoch zu HTTPS-Websites navigieren.</span><span class="sxs-lookup"><span data-stu-id="02163-188">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="02163-189">Schritt 7 – Skripting</span><span class="sxs-lookup"><span data-stu-id="02163-189">Step 7 - Scripting</span></span>  

<span data-ttu-id="02163-190">Sie können Host-Anwendungen verwenden, um JavaScript-Code zur Laufzeit in WebView2-Steuerelemente einzufügen.</span><span class="sxs-lookup"><span data-stu-id="02163-190">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="02163-191">Das eingefügte JavaScript gilt für alle neuen Dokumente auf oberster Ebene und für alle untergeordneten Frames, bis das JavaScript entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="02163-191">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="02163-192">Das eingefügte JavaScript wird nach der Erstellung des globalen Objekts und vor dem Ausführen eines anderen im HTML-Dokument enthaltenen Skripts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02163-192">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="02163-193">Sie können Skripting verwenden, um den Benutzer zu benachrichtigen, wenn Sie zu einer nicht-HTTPS-Website navigieren.</span><span class="sxs-lookup"><span data-stu-id="02163-193">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="02163-194">Ändern `EnsureHttps` Sie die Funktion so, dass Sie mit der [ExecuteScriptAsync]() -Methode Skripts in den Webinhalt einfügt.</span><span class="sxs-lookup"><span data-stu-id="02163-194">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="02163-195">Wählen Sie aus `F5` , um Ihr Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="02163-195">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="02163-196">Vergewissern Sie sich, dass die Anwendung eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die nicht HTTPS verwendet.</span><span class="sxs-lookup"><span data-stu-id="02163-196">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="02163-198">Schritt 8 – Kommunikation zwischen Host-und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="02163-198">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="02163-199">Die Host-und Webinhalte können mithilfe der folgenden Informationen miteinander kommunizieren `postMessage` :</span><span class="sxs-lookup"><span data-stu-id="02163-199">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="02163-200">Webinhalte in einem WebView2-Steuerelement senden möglicherweise eine Nachricht mithilfe von an den Host `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="02163-200">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="02163-201">Der Host verarbeitet die Nachricht mit einem `WebMessageReceived` auf dem Host registrierten Namen.</span><span class="sxs-lookup"><span data-stu-id="02163-201">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="02163-202">Hosts Posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mit `CoreWebView2.PostWebMessageAsString` oder `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="02163-202">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="02163-203">Diese Nachrichten werden von Handlern abgefangen, denen Sie hinzugefügt wurden `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="02163-203">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="02163-204">Mit diesem Kommunikationsmechanismus können Webinhalte Nachrichten mithilfe von systemeigenen Funktionen an den Host weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="02163-204">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="02163-205">Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt, und der Benutzer wird benachrichtigt, dass die URL im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="02163-205">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="02163-206">Aktualisieren Sie in **Form1.cs**den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, wie im folgenden Codeausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="02163-206">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="02163-207">Die `InitializeAsync` Funktion wartet [EnsureCoreWebView2Async]() auf, da die Initialisierung von `CoreWebView2` asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="02163-207">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

2. <span data-ttu-id="02163-208">Nachdem **CoreWebView2** initialisiert wurde, registrieren Sie einen Ereignishandler, auf den Sie Antworten können `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="02163-208">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="02163-209">In `Form1.cs` Update `InitializeAsync` und Add `UpdateAddressBar` mithilfe des folgenden Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="02163-209">In `Form1.cs` update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="02163-210">Damit die WebView die Webnachricht senden und beantworten kann, wird nach der `CoreWebView2` Initialisierung der Host ein Skript in den Webinhalt eingefügt, um:</span><span class="sxs-lookup"><span data-stu-id="02163-210">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="02163-211">Senden Sie die URL an den Host mit `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="02163-211">Send the URL to the host using `postMessage`.</span></span>
    2. <span data-ttu-id="02163-212">Registrieren Sie einen Ereignishandler, um eine vom Host gesendete Nachricht zu drucken.</span><span class="sxs-lookup"><span data-stu-id="02163-212">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="02163-213">In `Form1.cs` , aktualisieren Sie, `InitializeAsync` wie im folgenden Codeausschnitt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="02163-213">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="02163-214">Wählen Sie aus `F5` , um die APP zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="02163-214">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="02163-215">Vergewissern Sie sich, dass auf der Adressleiste die URL der Website angezeigt wird, die in der WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="02163-215">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="02163-216">Wenn Sie erfolgreich zu einer neuen URL navigieren, benachrichtigt die WebView den Benutzer auch über die URL, die in der WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="02163-216">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="02163-218">Herzlichen Glückwunsch, Sie haben ihre erste WebView2-App erstellt!</span><span class="sxs-lookup"><span data-stu-id="02163-218">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="02163-219">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="02163-219">Next Steps</span></span> 

* <span data-ttu-id="02163-220">Auschecken des [WebView2Samples Repo](https://github.com/MicrosoftEdge/WebView2Samples) für ein umfassendes Beispiel für WebView2's-Funktionen</span><span class="sxs-lookup"><span data-stu-id="02163-220">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="02163-221">Checkout [-API-Referenz](../reference/winforms/0-9-515/microsoft-web-webview2-winforms-webview2.md) für detailliertere Informationen zu unseren APIs</span><span class="sxs-lookup"><span data-stu-id="02163-221">Checkout [API reference](../reference/winforms/0-9-515/microsoft-web-webview2-winforms-webview2.md) for more detailed information about our APIs</span></span>
* <span data-ttu-id="02163-222">Auschecken einer Liste mit [WebView2-Ressourcen](../index.md#next-steps) , um mehr über WebView2 zu erfahren</span><span class="sxs-lookup"><span data-stu-id="02163-222">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>


## <span data-ttu-id="02163-223">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="02163-223">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="02163-224">Helfen Sie, ein reicheres WebView2-Erlebnis zu schaffen, indem Sie Ihr Feedback austauschen!</span><span class="sxs-lookup"><span data-stu-id="02163-224">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="02163-225">Besuchen Sie das Feedback- [Repo](https://aka.ms/webviewfeedback) von Microsoft Edge WebView, um Funktionsanforderungen oder Fehlerberichte zu übermitteln oder nach bekannten Problemen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="02163-225">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
