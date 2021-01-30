---
description: Erste Schritte mit WebView2 für WinForms-Apps
title: Erste Schritte mit WebView2 für WinForms-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, Webview2, WebView, Webview, winforms apps, winforms, edge, CoreWebView2, browser control, edge html, getting started, .NET, windows forms
ms.openlocfilehash: 45a3b59733a57975e373df2e21258198645be2d4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306166"
---
# <span data-ttu-id="c981a-104">Erste Schritte mit WebView2 in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c981a-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="c981a-105">In diesem Artikel beginnen Sie mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Wichtigsten Features von [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="c981a-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="c981a-106">Weitere Informationen zu einzelnen APIs finden Sie in der [API-Referenz.][DotnetApiMicrosoftWebWebview2Winforms]</span><span class="sxs-lookup"><span data-stu-id="c981a-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span></span>  

## <span data-ttu-id="c981a-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c981a-107">Prerequisites</span></span>  

<span data-ttu-id="c981a-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="c981a-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="c981a-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen \(derzeit Windows 10, Windows 8.1 und Windows 7\ installiert ist).</span><span class="sxs-lookup"><span data-stu-id="c981a-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c981a-110">Das WebView-Team empfiehlt die Verwendung des Canarykanals, und die mindestens erforderliche Version ist 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="c981a-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="c981a-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c981a-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="c981a-112">WebView2 unterstützt derzeit keine .NET 5- und .NET Core-Designer.</span><span class="sxs-lookup"><span data-stu-id="c981a-112">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>

## <span data-ttu-id="c981a-113">Schritt 1: Erstellen einer App mit einem Fenster</span><span class="sxs-lookup"><span data-stu-id="c981a-113">Step 1 - Create a single-window app</span></span>

<span data-ttu-id="c981a-114">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="c981a-114">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="c981a-115">Wählen Visual Studio **"Windows Forms .NET Framework App**  >  **Next" aus.**</span><span class="sxs-lookup"><span data-stu-id="c981a-115">In Visual Studio, choose **Windows Forms .NET Framework App** > **Next**.</span></span>
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Neues Projekt" lightbox="./media/winforms-newproject.png":::
       <span data-ttu-id="c981a-117">Neues Projekt</span><span class="sxs-lookup"><span data-stu-id="c981a-117">New project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="c981a-118">Geben Sie Werte für **den Projektnamen und** den **Speicherort ein.**</span><span class="sxs-lookup"><span data-stu-id="c981a-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="c981a-119">Wählen **Sie .NET Framework 4.6.2** oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-119">Choose **.NET Framework 4.6.2** or later.</span></span>  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Projekt starten" lightbox="./media/winforms-startproj.png":::
       <span data-ttu-id="c981a-121">Projekt starten</span><span class="sxs-lookup"><span data-stu-id="c981a-121">Start project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="c981a-122">Um Ihr Projekt zu erstellen, wählen Sie **"Erstellen"** aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-122">To create your project, choose **Create**.</span></span>
    
## <span data-ttu-id="c981a-123">Schritt 2: Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="c981a-123">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="c981a-124">Verwenden Sie NuGet, um dem Projekt das WebView2 SDK hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c981a-124">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="c981a-125">Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **NuGet-Pakete verwalten... aus.**</span><span class="sxs-lookup"><span data-stu-id="c981a-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Verwalten von NuGet-Paketen":::
       <span data-ttu-id="c981a-127">Verwalten von NuGet-Paketen</span><span class="sxs-lookup"><span data-stu-id="c981a-127">Manage NuGet Packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="c981a-128">Geben Sie in der Suchleiste > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2 aus.**</span><span class="sxs-lookup"><span data-stu-id="c981a-128">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="c981a-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="c981a-130">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="c981a-131">Beginnen Sie mit der Entwicklung von Apps mithilfe der WebView2-API.</span><span class="sxs-lookup"><span data-stu-id="c981a-131">Start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="c981a-132">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-132">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="c981a-133">Das ausgeführte Projekt zeigt ein leeres Fenster an.</span><span class="sxs-lookup"><span data-stu-id="c981a-133">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Leere App" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="c981a-135">Leere App</span><span class="sxs-lookup"><span data-stu-id="c981a-135">Empty app</span></span>  
    :::image-end:::
    
## <span data-ttu-id="c981a-136">Schritt 3: Erstellen einer einzelnen WebView</span><span class="sxs-lookup"><span data-stu-id="c981a-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="c981a-137">Fügen Sie Ihrer App eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="c981a-137">Add a WebView to your app.</span></span>  

1.  <span data-ttu-id="c981a-138">Öffnen Sie **den Windows Forms Designer.**</span><span class="sxs-lookup"><span data-stu-id="c981a-138">Open the **Windows Forms Designer**.</span></span>  
1.  <span data-ttu-id="c981a-139">Suchen Sie in der **Toolbox**nach **WebView2.**</span><span class="sxs-lookup"><span data-stu-id="c981a-139">Search for **WebView2** in the **Toolbox**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c981a-140">Wenn Sie Visual Studio 2017 verwenden, wird **WebView2** standardmäßig nicht in der **Toolbox angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="c981a-140">If you are using Visual Studio 2017, by default **WebView2** may not display in the **Toolbox**.</span></span>  <span data-ttu-id="c981a-141">Um das Verhalten zu aktivieren, **wählen**Sie tools Options General > die Einstellung "Toolbox automatisch  >  \*\*\*\*  >  \*\*\*\* auffüllen" auf \*\*\*\* `True` .</span><span class="sxs-lookup"><span data-stu-id="c981a-141">To enable the behavior, choose **Tools** > **Options** > **General** > set the **Automatically Populate Toolbox** setting to `True`.</span></span>  
    
    <span data-ttu-id="c981a-142">Drag and drop the **WebView2** control into the Windows Forms App.</span><span class="sxs-lookup"><span data-stu-id="c981a-142">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Toolbox mit WebView2":::
       <span data-ttu-id="c981a-144">Toolbox mit WebView2</span><span class="sxs-lookup"><span data-stu-id="c981a-144">Toolbox displaying WebView2</span></span>
    :::image-end:::  

1.  <span data-ttu-id="c981a-145">Legen Sie die `(Name)`-Eigenschaft auf `webView` fest.</span><span class="sxs-lookup"><span data-stu-id="c981a-145">Set the `(Name)` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Eigenschaften des WebView2-Steuerelements":::
       <span data-ttu-id="c981a-147">Eigenschaften des WebView2-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="c981a-147">Properties of the WebView2 control</span></span>
    :::image-end:::

1.  <span data-ttu-id="c981a-148">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c981a-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  <span data-ttu-id="c981a-149">Legen Sie die `Source`-Eigenschaft auf `https://www.microsoft.com` fest.</span><span class="sxs-lookup"><span data-stu-id="c981a-149">Set the `Source` property to `https://www.microsoft.com`.</span></span>  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Die Eigenschaft "Source" des WebView2-Steuerelements":::
       <span data-ttu-id="c981a-151">Die **Eigenschaft "Source"** des WebView2-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="c981a-151">The **Source** property of the WebView2 control</span></span>
    :::image-end:::  

<span data-ttu-id="c981a-152">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-152">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="c981a-153">Stellen Sie sicher, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.</span><span class="sxs-lookup"><span data-stu-id="c981a-153">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   <span data-ttu-id="c981a-155">hello webview</span><span class="sxs-lookup"><span data-stu-id="c981a-155">hello webview</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c981a-156">Wenn Sie an einem Monitor mit hohem DPI arbeiten, müssen Sie Ihre [Windows Forms-App][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]möglicherweise für die Unterstützung hoher DPI konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c981a-156">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport].</span></span>  

## <span data-ttu-id="c981a-157">Schritt 4: Behandeln von Ereignissen für die Fenstergröße</span><span class="sxs-lookup"><span data-stu-id="c981a-157">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="c981a-158">Fügen Sie ein paar weitere Steuerelemente zu Ihren Windows Forms aus der Toolbox hinzu, und behandeln Sie die Ereignisse für die Fenstergröße entsprechend.</span><span class="sxs-lookup"><span data-stu-id="c981a-158">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1.  <span data-ttu-id="c981a-159">Öffnen Sie **im Windows Forms Designer**die **Toolbox**</span><span class="sxs-lookup"><span data-stu-id="c981a-159">In the **Windows Forms Designer**, open the **Toolbox**</span></span>
1.  <span data-ttu-id="c981a-160">Ziehen Sie ein **TextBox-Objekt per** Drag and Drop in die Windows Forms App.</span><span class="sxs-lookup"><span data-stu-id="c981a-160">Drag and drop a **TextBox** into the Windows Forms App.</span></span>  <span data-ttu-id="c981a-161">Geben Sie **auf der Registerkarte "Eigenschaften"** den Namen **"TextBox" ein.** `addressBar`</span><span class="sxs-lookup"><span data-stu-id="c981a-161">In the **Properties Tab**, name the **TextBox** `addressBar` .</span></span>
1.  <span data-ttu-id="c981a-162">Drag and drop a **Button** into the Windows Forms App.</span><span class="sxs-lookup"><span data-stu-id="c981a-162">Drag and drop a **Button** into the Windows Forms App.</span></span>  <span data-ttu-id="c981a-163">Ändern Sie den Text in der **Schaltfläche,** `Go!` und benennen Sie die **Schaltfläche** auf der `goButton` Registerkarte **"Eigenschaften".**</span><span class="sxs-lookup"><span data-stu-id="c981a-163">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="c981a-164">Die App sollte wie das folgende Bild im Designer aussehen.</span><span class="sxs-lookup"><span data-stu-id="c981a-164">The app should look like the following image in the designer.</span></span>
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Designer" lightbox="./media/winforms-designer.png":::
       <span data-ttu-id="c981a-166">Designer</span><span class="sxs-lookup"><span data-stu-id="c981a-166">designer</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="c981a-167">Definieren Sie in der Datei, dass die Steuerelemente bei der Größenänderung des `Form1.cs` `Form_Resize` App-Fensters weiterhin verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c981a-167">In the `Form1.cs` file, define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="c981a-168">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-168">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="c981a-169">Stellen Sie sicher, dass die App ähnlich wie im folgenden Screenshot angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c981a-169">Ensure the app displays similar to the following screenshot.</span></span>

:::image type="complex" source="./media/winforms-app.png" alt-text="App" lightbox="./media/winforms-app.png":::
   <span data-ttu-id="c981a-171">App</span><span class="sxs-lookup"><span data-stu-id="c981a-171">App</span></span>  
:::image-end:::

## <span data-ttu-id="c981a-172">Schritt 5: Navigation</span><span class="sxs-lookup"><span data-stu-id="c981a-172">Step 5 - Navigation</span></span>

<span data-ttu-id="c981a-173">Fügen Sie die Möglichkeit hinzu, Benutzern das Ändern der URL zu ermöglichen, die das WebView2-Steuerelement anzeigt, indem Sie der App eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c981a-173">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="c981a-174">Fügen Sie in der Datei den folgenden Codeausschnitt oben ein, um den `Form1.cs` `CoreWebView2` Namespace hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c981a-174">In the `Form1.cs`file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  <span data-ttu-id="c981a-175">Doppelklicken Sie **im Windows Forms Designer**auf die Schaltfläche, um die Methode in der Datei zu `Go!` `goButton_Click` `Form1.cs` erstellen.</span><span class="sxs-lookup"><span data-stu-id="c981a-175">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in the `Form1.cs` file.</span></span>  <span data-ttu-id="c981a-176">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="c981a-176">Copy and paste the following snippet inside the function.</span></span>  <span data-ttu-id="c981a-177">Nun navigiert die Funktion in der WebAnsicht zu `goButton_Click` der URL, die in der Adressleiste eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c981a-177">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="c981a-178">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-178">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="c981a-179">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **"Los" aus.**</span><span class="sxs-lookup"><span data-stu-id="c981a-179">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="c981a-180">Geben Sie z. `https://www.bing.com` B. .</span><span class="sxs-lookup"><span data-stu-id="c981a-180">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="c981a-181">Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="c981a-181">Ensure the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="c981a-182">Stellen Sie sicher, dass in der Adressleiste eine vollständige URL eingegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c981a-182">Ensure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="c981a-183">Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://`</span><span class="sxs-lookup"><span data-stu-id="c981a-183">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   <span data-ttu-id="c981a-185">bing.com</span><span class="sxs-lookup"><span data-stu-id="c981a-185">bing.com</span></span>  
:::image-end:::

## <span data-ttu-id="c981a-186">Schritt 6: Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="c981a-186">Step 6 - Navigation events</span></span>  

<span data-ttu-id="c981a-187">Während der Webseitennavigation löst das WebView2-Steuerelement Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-187">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="c981a-188">Die App, die WebView2-Steuerelemente hostet, lauscht auf die folgenden Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c981a-188">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="c981a-189">Navigieren Sie zu [Navigationsereignissen, um weitere Informationen zu erhalten.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="c981a-189">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="c981a-191">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="c981a-191">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="c981a-192">Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und sind möglicherweise von der Navigation zu einer Fehlerwebseite abhängig.</span><span class="sxs-lookup"><span data-stu-id="c981a-192">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="c981a-193">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="c981a-193">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="c981a-194">Um die Verwendung dieser Ereignisse zu veranschaulichen, registrieren Sie zunächst einen Handler, der alle Anforderungen abbricht, die HTTPS `NavigationStarting` nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="c981a-194">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="c981a-195">Aktualisieren Sie in der Datei den Konstruktor so, dass er mit dem `Form1.cs` folgenden Codeausschnitt übereinstimmen kann, und fügen Sie die Funktion `EnsureHttps` hinzu.</span><span class="sxs-lookup"><span data-stu-id="c981a-195">In the `Form1.cs` file, update the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="c981a-196">Im Konstruktor wird EnsureHttps als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.</span><span class="sxs-lookup"><span data-stu-id="c981a-196">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="c981a-197">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-197">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="c981a-198">Stellen Sie sicher, dass die WebView beim Navigieren zu einer HTTP-Website unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="c981a-198">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="c981a-199">Die WebView navigiert jedoch zu HTTPS-Websites.</span><span class="sxs-lookup"><span data-stu-id="c981a-199">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="c981a-200">Schritt 7: Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="c981a-200">Step 7 - Scripting</span></span>  

<span data-ttu-id="c981a-201">Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.</span><span class="sxs-lookup"><span data-stu-id="c981a-201">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="c981a-202">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span><span class="sxs-lookup"><span data-stu-id="c981a-202">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="c981a-203">Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c981a-203">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="c981a-204">Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c981a-204">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="c981a-205">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-205">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="c981a-206">Führen Sie es aus, bevor ein anderes Im HTML-Dokument enthaltenes Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c981a-206">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="c981a-207">Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="c981a-207">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="c981a-208">Ändern Sie die Funktion, um ein Skript in den Webinhalt zu injizieren, `EnsureHttps` der die [ExecuteScriptAsync-Methode][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] verwendet.</span><span class="sxs-lookup"><span data-stu-id="c981a-208">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] method.</span></span>  

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

<span data-ttu-id="c981a-209">Wählen Sie zum Erstellen und Ausführen des Projekts die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-209">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="c981a-210">Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c981a-210">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   <span data-ttu-id="c981a-212">https</span><span class="sxs-lookup"><span data-stu-id="c981a-212">https</span></span>  
:::image-end:::

## <span data-ttu-id="c981a-213">Schritt 8: Kommunikation zwischen Host- und Webinhalt</span><span class="sxs-lookup"><span data-stu-id="c981a-213">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="c981a-214">Host- und Webinhalte können für `postMessage` die Kommunikation miteinander wie folgt verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="c981a-214">The host and web content may use `postMessage` to communicate with each other as follows:</span></span>  

*   <span data-ttu-id="c981a-215">Webinhalte in einem WebView2-Steuerelement können zum Veröffentlichen `window.chrome.webview.postMessage` einer Nachricht an den Host verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c981a-215">Web content in a WebView2 control may use `window.chrome.webview.postMessage` to post a message to the host.</span></span>  <span data-ttu-id="c981a-216">Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c981a-216">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="c981a-217">Hostet Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="c981a-217">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="c981a-218">Diese Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` wurden.</span><span class="sxs-lookup"><span data-stu-id="c981a-218">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="c981a-219">Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.</span><span class="sxs-lookup"><span data-stu-id="c981a-219">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="c981a-220">Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, zeigt es die URL in der Adressleiste an und benachrichtigt den Benutzer über die im WebView2-Steuerelement angezeigte URL.</span><span class="sxs-lookup"><span data-stu-id="c981a-220">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="c981a-221">Aktualisieren Sie in der Datei den Konstruktor, und erstellen Sie eine `Form1.cs` `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="c981a-221">In the `Form1.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="c981a-222">Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] da die Initialisierung `CoreWebView2` asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="c981a-222">The `InitializeAsync` function awaits [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1.  <span data-ttu-id="c981a-223">Registrieren `CoreWebView2` Sie nach der Initialisierung einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.</span><span class="sxs-lookup"><span data-stu-id="c981a-223">After `CoreWebView2` is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="c981a-224">Aktualisieren und `Form1.cs` fügen Sie in der Datei mithilfe des folgenden `InitializeAsync` `UpdateAddressBar` Codeausschnitts hinzu.</span><span class="sxs-lookup"><span data-stu-id="c981a-224">In the `Form1.cs` file, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1.  <span data-ttu-id="c981a-225">Damit WebView die Webnachricht sendet und darauf antwortet, wird nach der Initialisierung ein Skript in den `CoreWebView2` Webinhalt eingef?nkt, um:</span><span class="sxs-lookup"><span data-stu-id="c981a-225">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1.  <span data-ttu-id="c981a-226">Senden Sie die URL mithilfe von `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="c981a-226">Send the URL to the host using `postMessage`.</span></span>
    1.  <span data-ttu-id="c981a-227">Registrieren Sie einen Ereignishandler, um eine vom Host gesendete Nachricht zu drucken.</span><span class="sxs-lookup"><span data-stu-id="c981a-227">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="c981a-228">Aktualisieren Sie `Form1.cs` in der Datei so, dass sie mit `InitializeAsync` dem folgenden Codeausschnitt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c981a-228">In the `Form1.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="c981a-229">Wählen Sie zum Erstellen und Ausführen der App die Option `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="c981a-229">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="c981a-230">Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="c981a-230">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="c981a-231">Wenn Sie erfolgreich zu einer neuen URL navigieren, wird der Benutzer außerdem von WebView über die url benachrichtigt, die in der WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c981a-231">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Endgültige App" lightbox="./media/winforms-finalapp.png":::
   <span data-ttu-id="c981a-233">Endgültige App</span><span class="sxs-lookup"><span data-stu-id="c981a-233">Final app</span></span>  
:::image-end:::

<span data-ttu-id="c981a-234">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="c981a-234">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="c981a-235">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c981a-235">Next steps</span></span>  

<span data-ttu-id="c981a-236">Um weitere Informationen zu WebView2 zu erhalten, navigieren Sie zu den folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c981a-236">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="c981a-237">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c981a-237">See also</span></span>  

*   <span data-ttu-id="c981a-238">Ein umfassendes Beispiel der WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="c981a-238">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="c981a-239">Weitere Informationen zu WebView2 finden Sie unter ["WebView2-Ressourcen".][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="c981a-239">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
*   <span data-ttu-id="c981a-240">Ausführliche Informationen zur WebView2-API finden Sie in der [API-Referenz.][DotnetApiMicrosoftWebWebview2WinformsWebview2]</span><span class="sxs-lookup"><span data-stu-id="c981a-240">For detailed information about the WebView2 API, navigate to [API reference][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span></span>  

## <span data-ttu-id="c981a-241">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="c981a-241">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Namespace-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "WebView2-| Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "WebView2.EnsureCoreWebView2Async(CoreWebView2Environment)-Methode | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String)-Methode | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Konfigurieren der Windows Forms-App für hohe DPI-Unterstützung – Unterstützung für hohe DPI in Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2| Microsoft Edge Developer"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  