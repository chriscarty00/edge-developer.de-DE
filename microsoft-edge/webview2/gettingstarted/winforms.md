---
description: Erste Schritte mit WebView2 für WinForms-Apps
title: Erste Schritte mit WebView2 für WinForms-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, Webview, winforms apps, winforms, edge, CoreWebView2, browser control, edge html, getting started, Getting Started, .NET, windows forms
ms.openlocfilehash: 408d225c6c0abe54483226e7004a386d367d65ab
ms.sourcegitcommit: b51df5036642060525e03cd744b7d35726326abe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526087"
---
# <a name="getting-started-with-webview2-in-windows-forms"></a><span data-ttu-id="8829a-104">Erste Schritte mit WebView2 in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8829a-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="8829a-105">Beginnen Sie in diesem Artikel mit dem Erstellen Ihrer ersten WebView2-App, und erfahren Sie mehr über die Hauptfeatures von [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="8829a-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="8829a-106">Weitere Informationen zu einzelnen APIs finden Sie unter [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span><span class="sxs-lookup"><span data-stu-id="8829a-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="8829a-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8829a-107">Prerequisites</span></span>  

<span data-ttu-id="8829a-108">Stellen Sie sicher, dass Sie die folgende Liste der Voraussetzungen installieren, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="8829a-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="8829a-109">[WebView2-Laufzeit][MicrosoftDeveloperMicrosoftEdgeWebview2] oder ein nicht stabiler [Microsoft Edge (Chromium)-Kanal,][MicrosoftedgeinsiderDownload] der unter unterstützten Betriebssystemen installiert ist \(derzeit Windows 10, Windows 8.1 und Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="8829a-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8829a-110">Das WebView-Team empfiehlt die Verwendung des Canary-Kanals, und die erforderliche Mindestversion ist 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="8829a-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="8829a-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 oder höher.</span><span class="sxs-lookup"><span data-stu-id="8829a-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="8829a-112">WebView2 unterstützt derzeit keine .NET 5- und .NET Core-Designer.</span><span class="sxs-lookup"><span data-stu-id="8829a-112">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>  

## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="8829a-113">Schritt 1 : Erstellen einer App mit einem Fenster</span><span class="sxs-lookup"><span data-stu-id="8829a-113">Step 1 - Create a single-window app</span></span>

<span data-ttu-id="8829a-114">Beginnen Sie mit einem einfachen Desktopprojekt, das ein einzelnes Hauptfenster enthält.</span><span class="sxs-lookup"><span data-stu-id="8829a-114">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="8829a-115">Wählen Visual Studio Windows **Forms .NET Framework App**  >  **Next aus.**</span><span class="sxs-lookup"><span data-stu-id="8829a-115">In Visual Studio, choose **Windows Forms .NET Framework App** > **Next**.</span></span>
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Neues Projekt" lightbox="./media/winforms-newproject.png":::
       <span data-ttu-id="8829a-117">Neues Projekt</span><span class="sxs-lookup"><span data-stu-id="8829a-117">New project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="8829a-118">Geben Sie Werte für **Projektname und** **Standort ein.**</span><span class="sxs-lookup"><span data-stu-id="8829a-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="8829a-119">Wählen **.NET Framework 4.6.2** oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="8829a-119">Choose **.NET Framework 4.6.2** or later.</span></span>  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Projekt starten" lightbox="./media/winforms-startproj.png":::
       <span data-ttu-id="8829a-121">Projekt starten</span><span class="sxs-lookup"><span data-stu-id="8829a-121">Start project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="8829a-122">Wählen Sie Erstellen aus, um Ihr Projekt **zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="8829a-122">To create your project, choose **Create**.</span></span>
    
## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="8829a-123">Schritt 2 : Installieren des WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="8829a-123">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="8829a-124">Verwenden Sie NuGet, um das WebView2 SDK zum Projekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8829a-124">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="8829a-125">Zeigen Sie auf das Projekt, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **NuGet-Pakete verwalten...** aus.</span><span class="sxs-lookup"><span data-stu-id="8829a-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Verwalten von NuGet-Paketen":::
       <span data-ttu-id="8829a-127">Verwalten von NuGet-Paketen</span><span class="sxs-lookup"><span data-stu-id="8829a-127">Manage NuGet Packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="8829a-128">Geben Sie in der Suchleiste `Microsoft.Web.WebView2` > Wählen Sie **Microsoft.Web.WebView2 aus.**</span><span class="sxs-lookup"><span data-stu-id="8829a-128">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="8829a-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="8829a-130">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="8829a-131">Beginnen Sie mit der Entwicklung von Apps mithilfe der WebView2-API.</span><span class="sxs-lookup"><span data-stu-id="8829a-131">Start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="8829a-132">Wählen Sie aus, um das Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="8829a-132">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="8829a-133">Das ausgeführte Projekt zeigt ein leeres Fenster an.</span><span class="sxs-lookup"><span data-stu-id="8829a-133">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Leere App" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="8829a-135">Leere App</span><span class="sxs-lookup"><span data-stu-id="8829a-135">Empty app</span></span>  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a><span data-ttu-id="8829a-136">Schritt 3 : Erstellen einer einzelnen WebView</span><span class="sxs-lookup"><span data-stu-id="8829a-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="8829a-137">Fügen Sie Ihrer App eine WebView hinzu.</span><span class="sxs-lookup"><span data-stu-id="8829a-137">Add a WebView to your app.</span></span>  

1.  <span data-ttu-id="8829a-138">Öffnen Sie **den Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="8829a-138">Open the **Windows Forms Designer**.</span></span>  
1.  <span data-ttu-id="8829a-139">Suchen Sie in der **Toolbox**nach **WebView2.**</span><span class="sxs-lookup"><span data-stu-id="8829a-139">Search for **WebView2** in the **Toolbox**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8829a-140">Wenn Sie Visual Studio 2017 verwenden, wird **WebView2** standardmäßig nicht in der **Toolbox angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="8829a-140">If you are using Visual Studio 2017, by default **WebView2** may not display in the **Toolbox**.</span></span>  <span data-ttu-id="8829a-141">Um das Verhalten zu aktivieren, wählen Sie **Tools**  >  **Options**  >  **General** > legen Sie die **Einstellung** Toolbox automatisch auf auf . `True`</span><span class="sxs-lookup"><span data-stu-id="8829a-141">To enable the behavior, choose **Tools** > **Options** > **General** > set the **Automatically Populate Toolbox** setting to `True`.</span></span>  
    
    <span data-ttu-id="8829a-142">Ziehen Sie das **WebView2-Steuerelement** in die Windows Forms App, und legen Sie es ab.</span><span class="sxs-lookup"><span data-stu-id="8829a-142">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Toolbox mit WebView2":::
       <span data-ttu-id="8829a-144">Toolbox mit WebView2</span><span class="sxs-lookup"><span data-stu-id="8829a-144">Toolbox displaying WebView2</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="8829a-145">Legen Sie die `(Name)`-Eigenschaft auf `webView` fest.</span><span class="sxs-lookup"><span data-stu-id="8829a-145">Set the `(Name)` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Eigenschaften des WebView2-Steuerelements":::
       <span data-ttu-id="8829a-147">Eigenschaften des WebView2-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="8829a-147">Properties of the WebView2 control</span></span>
    :::image-end:::

1.  <span data-ttu-id="8829a-148">Die `Source` Eigenschaft legt den anfänglichen URI fest, der im WebView2-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8829a-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  <span data-ttu-id="8829a-149">Legen Sie die `Source`-Eigenschaft auf `https://www.microsoft.com` fest.</span><span class="sxs-lookup"><span data-stu-id="8829a-149">Set the `Source` property to `https://www.microsoft.com`.</span></span>  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Die Source-Eigenschaft des WebView2-Steuerelements":::
       <span data-ttu-id="8829a-151">Die **Source-Eigenschaft** des WebView2-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="8829a-151">The **Source** property of the WebView2 control</span></span>
    :::image-end:::  

<span data-ttu-id="8829a-152">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="8829a-152">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="8829a-153">Stellen Sie sicher, dass Ihr WebView2-Steuerelement angezeigt [https://www.microsoft.com][|::ref1::|Main] wird.</span><span class="sxs-lookup"><span data-stu-id="8829a-153">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   <span data-ttu-id="8829a-155">hello webview</span><span class="sxs-lookup"><span data-stu-id="8829a-155">hello webview</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8829a-156">Wenn Sie an einem Monitor mit hohem DPI arbeiten, müssen Sie Ihre [Windows Forms-App][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]möglicherweise für die Unterstützung mit hohem DPI konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8829a-156">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport].</span></span>  

## <a name="step-4---handle-window-resize-events"></a><span data-ttu-id="8829a-157">Schritt 4 – Behandeln von Ereignissen für die Fenstergröße</span><span class="sxs-lookup"><span data-stu-id="8829a-157">Step 4 - Handle Window Resize Events</span></span>  

<span data-ttu-id="8829a-158">Fügen Sie ihren Windows Forms aus der Toolbox ein paar weitere Steuerelemente hinzu, und behandeln Sie die Ereignisse für die Fenstergröße entsprechend.</span><span class="sxs-lookup"><span data-stu-id="8829a-158">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>  

1.  <span data-ttu-id="8829a-159">Öffnen Sie **im Windows Forms Designer**die **Toolbox**.</span><span class="sxs-lookup"><span data-stu-id="8829a-159">In the **Windows Forms Designer**, open the **Toolbox**.</span></span>  
1.  <span data-ttu-id="8829a-160">Ziehen und ablegen Sie **ein TextBox-Objekt** in die Windows Forms App.</span><span class="sxs-lookup"><span data-stu-id="8829a-160">Drag and Drop a **TextBox** into the Windows Forms App.</span></span>  <span data-ttu-id="8829a-161">Benennen Sie **das TextBox-Postfach** `addressBar` auf der Registerkarte **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="8829a-161">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>  
1.  <span data-ttu-id="8829a-162">Ziehen und Ablegen einer **Schaltfläche** in die Windows Forms App.</span><span class="sxs-lookup"><span data-stu-id="8829a-162">Drag and Drop a **Button** into the Windows Forms App.</span></span>  <span data-ttu-id="8829a-163">Ändern Sie den Text in **der Schaltfläche** in und nennen Sie `Go!` die **Schaltfläche** auf der `goButton` Registerkarte **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="8829a-163">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>  
    
    <span data-ttu-id="8829a-164">Die App sollte wie das folgende Bild im Designer aussehen.</span><span class="sxs-lookup"><span data-stu-id="8829a-164">The app should look like the following image in the designer.</span></span>  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="WinForms-Designer" lightbox="./media/winforms-designer.png":::
       <span data-ttu-id="8829a-166">WinForms-Designer</span><span class="sxs-lookup"><span data-stu-id="8829a-166">WinForms designer</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="8829a-167">Definieren Sie in der Datei, dass die Steuerelemente bei der Größenänderung des `Form1.cs` `Form_Resize` App-Fensters an Ort und Stelle bleiben.</span><span class="sxs-lookup"><span data-stu-id="8829a-167">In the `Form1.cs` file, define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="8829a-168">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="8829a-168">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="8829a-169">Stellen Sie sicher, dass die App ähnlich dem folgenden Screenshot angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8829a-169">Ensure the app displays similar to the following screenshot.</span></span>

:::image type="complex" source="./media/winforms-app.png" alt-text="App" lightbox="./media/winforms-app.png":::
   <span data-ttu-id="8829a-171">App</span><span class="sxs-lookup"><span data-stu-id="8829a-171">App</span></span>  
:::image-end:::

## <a name="step-5---navigation"></a><span data-ttu-id="8829a-172">Schritt 5 – Navigation</span><span class="sxs-lookup"><span data-stu-id="8829a-172">Step 5 - Navigation</span></span>

<span data-ttu-id="8829a-173">Fügen Sie die Möglichkeit hinzu, Benutzern das Ändern der URL zu ermöglichen, die das WebView2-Steuerelement anzeigt, indem Sie der App eine Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8829a-173">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>  

1.  <span data-ttu-id="8829a-174">Wählen `F5` Sie aus, um Ihr Projekt zu erstellen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="8829a-174">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="8829a-175">Vergewissern Sie sich, dass die App ähnlich dem folgenden Screenshot angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8829a-175">Confirm that the app displays similar to the following screenshot.</span></span>  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="WinForms App" lightbox="./media/winforms-app.png":::
       <span data-ttu-id="8829a-177">WinForms App</span><span class="sxs-lookup"><span data-stu-id="8829a-177">WinForms App</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8829a-178">Fügen Sie in der Datei den folgenden Codeausschnitt oben ein, um den `Form1.cs` `CoreWebView2` Namespace hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8829a-178">In the `Form1.cs`file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  

1.  <span data-ttu-id="8829a-179">Fügen `Form1.cs` Sie den `CoreWebView2` Namespace hinzu, indem Sie den folgenden Codeausschnitt oben in `Form1.cs` einfügen.</span><span class="sxs-lookup"><span data-stu-id="8829a-179">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  <span data-ttu-id="8829a-180">**Doppelklicken Sie im Windows Forms Designer**auf die `Go!` Schaltfläche, um die Methode in der Datei `goButton_Click` zu `Form1.cs` erstellen.</span><span class="sxs-lookup"><span data-stu-id="8829a-180">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in the `Form1.cs` file.</span></span>  <span data-ttu-id="8829a-181">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn in die Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="8829a-181">Copy and paste the following snippet inside the function.</span></span>  <span data-ttu-id="8829a-182">Nun navigiert `goButton_Click` die Funktion in der WebView zu der URL, die in der Adressleiste eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8829a-182">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="8829a-183">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="8829a-183">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="8829a-184">Geben Sie in der Adressleiste eine neue URL ein, und wählen Sie **Los**aus.</span><span class="sxs-lookup"><span data-stu-id="8829a-184">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="8829a-185">Geben Sie z. B. `https://www.bing.com` ein.</span><span class="sxs-lookup"><span data-stu-id="8829a-185">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="8829a-186">Stellen Sie sicher, dass das WebView2-Steuerelement zur URL navigiert.</span><span class="sxs-lookup"><span data-stu-id="8829a-186">Ensure the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="8829a-187">Stellen Sie sicher, dass eine vollständige URL in der Adressleiste eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8829a-187">Ensure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="8829a-188">Ein `ArgumentException` wird ausgelöst, wenn die URL nicht mit oder `http://`</span><span class="sxs-lookup"><span data-stu-id="8829a-188">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   <span data-ttu-id="8829a-190">bing.com</span><span class="sxs-lookup"><span data-stu-id="8829a-190">bing.com</span></span>  
:::image-end:::

## <a name="step-6---navigation-events"></a><span data-ttu-id="8829a-191">Schritt 6 – Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="8829a-191">Step 6 - Navigation events</span></span>  

<span data-ttu-id="8829a-192">Während der Webseitennavigation löst das WebView2-Steuerelement Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="8829a-192">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="8829a-193">Die App, die WebView2-Steuerelemente hostet, lauscht auf die folgenden Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8829a-193">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="8829a-194">Weitere Informationen finden Sie unter [Navigationsereignisse][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="8829a-194">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Navigationsereignisse":::
   <span data-ttu-id="8829a-196">Navigationsereignisse</span><span class="sxs-lookup"><span data-stu-id="8829a-196">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="8829a-197">Wenn ein Fehler auftritt, werden die folgenden Ereignisse ausgelöst und hängen möglicherweise von der Navigation zu einer Fehlerwebseite ab.</span><span class="sxs-lookup"><span data-stu-id="8829a-197">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="8829a-198">Wenn eine HTTP-Umleitung auftritt, gibt es mehrere `NavigationStarting` Ereignisse in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="8829a-198">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="8829a-199">Um die Verwendung der Ereignisse zu veranschaulichen, registrieren Sie zunächst einen Handler, der alle Anforderungen abbricht, die https `NavigationStarting` nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="8829a-199">To demonstrate how to use the events, start by registering a handler for `NavigationStarting` that cancels any requests not using HTTPS.</span></span>  

<span data-ttu-id="8829a-200">Aktualisieren Sie `Form1.cs` in der Datei den Konstruktor, um dem folgenden Codeausschnitt zu entsprechen, und fügen Sie die Funktion `EnsureHttps` hinzu.</span><span class="sxs-lookup"><span data-stu-id="8829a-200">In the `Form1.cs` file, update the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="8829a-201">Wird im `EnsureHttps` Konstruktor als Ereignishandler für das `NavigationStarting` Ereignis im WebView2-Steuerelement registriert.</span><span class="sxs-lookup"><span data-stu-id="8829a-201">In the constructor, `EnsureHttps` is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="8829a-202">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="8829a-202">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="8829a-203">Stellen Sie sicher, dass beim Navigieren zu einer HTTP-Website die WebView unverändert bleibt.</span><span class="sxs-lookup"><span data-stu-id="8829a-203">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="8829a-204">Die WebView navigiert jedoch zu HTTPS-Websites.</span><span class="sxs-lookup"><span data-stu-id="8829a-204">However, the WebView will navigate to HTTPS sites.</span></span>

## <a name="step-7---scripting"></a><span data-ttu-id="8829a-205">Schritt 7 – Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="8829a-205">Step 7 - Scripting</span></span>  

<span data-ttu-id="8829a-206">Sie können Host-Apps verwenden, um Zur Laufzeit JavaScript-Code in WebView2-Steuerelemente zu injizieren.</span><span class="sxs-lookup"><span data-stu-id="8829a-206">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="8829a-207">Sie können WebView zum Ausführen beliebiger JavaScript- oder Initialisierungsskripts aufgaben.</span><span class="sxs-lookup"><span data-stu-id="8829a-207">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="8829a-208">Das injizierte JavaScript gilt für alle neuen Dokumente der obersten Ebene und alle untergeordneten Frames, bis das JavaScript entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8829a-208">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="8829a-209">Das injizierte JavaScript wird mit einem bestimmten Timing ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8829a-209">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="8829a-210">Führen Sie es nach der Erstellung des globalen Objekts aus.</span><span class="sxs-lookup"><span data-stu-id="8829a-210">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="8829a-211">Führen Sie es aus, bevor ein anderes Skript ausgeführt wird, das im HTML-Dokument enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8829a-211">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="8829a-212">Fügen Sie beispielsweise Skripts hinzu, die eine Warnung senden, wenn ein Benutzer zu Nicht-HTTPS-Websites navigiert.</span><span class="sxs-lookup"><span data-stu-id="8829a-212">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="8829a-213">Ändern Sie `EnsureHttps` die Funktion, um ein Skript in den Webinhalt zu injizieren, der [die ExecuteScriptAsync-Methode][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] verwendet.</span><span class="sxs-lookup"><span data-stu-id="8829a-213">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] method.</span></span>  

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

<span data-ttu-id="8829a-214">Wählen Sie aus, um Ihr Projekt zu erstellen und `F5` ausführen.</span><span class="sxs-lookup"><span data-stu-id="8829a-214">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="8829a-215">Stellen Sie sicher, dass die App eine Warnung anzeigt, wenn Sie zu einer Website navigieren, die https nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8829a-215">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   <span data-ttu-id="8829a-217">https</span><span class="sxs-lookup"><span data-stu-id="8829a-217">https</span></span>  
:::image-end:::

## <a name="step-8---communication-between-host-and-web-content"></a><span data-ttu-id="8829a-218">Schritt 8 – Kommunikation zwischen Host- und Webinhalten</span><span class="sxs-lookup"><span data-stu-id="8829a-218">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="8829a-219">Host- und Webinhalte können für die `postMessage` Kommunikation miteinander wie folgt verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="8829a-219">The host and web content may use `postMessage` to communicate with each other as follows:</span></span>  

*   <span data-ttu-id="8829a-220">Webinhalte in einem WebView2-Steuerelement können verwendet werden, um eine `window.chrome.webview.postMessage` Nachricht an den Host zu posten.</span><span class="sxs-lookup"><span data-stu-id="8829a-220">Web content in a WebView2 control may use `window.chrome.webview.postMessage` to post a message to the host.</span></span>  <span data-ttu-id="8829a-221">Der Host verarbeitet die Nachricht mit allen auf dem `WebMessageReceived` Host registrierten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="8829a-221">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="8829a-222">Hosts posten Nachrichten an Webinhalte in einem WebView2-Steuerelement mithilfe oder `CoreWebView2.PostWebMessageAsString` `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="8829a-222">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="8829a-223">Diese Nachrichten werden von Handlern erfasst, die zu hinzugefügt `window.chrome.webview.addEventListener` werden.</span><span class="sxs-lookup"><span data-stu-id="8829a-223">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="8829a-224">Der Kommunikationsmechanismus übergibt Nachrichten von Webinhalten mithilfe systemeigener Funktionen an den Host.</span><span class="sxs-lookup"><span data-stu-id="8829a-224">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="8829a-225">Wenn das WebView2-Steuerelement in Ihrem Projekt zu einer URL navigiert, wird die URL in der Adressleiste angezeigt und der Benutzer über die im WebView2-Steuerelement angezeigte URL benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="8829a-225">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="8829a-226">Aktualisieren Sie `Form1.cs` in der Datei den Konstruktor, und erstellen Sie eine `InitializeAsync` Funktion, die mit dem folgenden Codeausschnitt übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="8829a-226">In the `Form1.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="8829a-227">Die `InitializeAsync` Funktion wartet auf [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] da die Initialisierung `CoreWebView2` von asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="8829a-227">The `InitializeAsync` function awaits [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1.  <span data-ttu-id="8829a-228">Registrieren `CoreWebView2` Sie nach der Initialisierung einen Ereignishandler, um auf zu `WebMessageReceived` reagieren.</span><span class="sxs-lookup"><span data-stu-id="8829a-228">After `CoreWebView2` is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="8829a-229">Aktualisieren `Form1.cs` und hinzufügen Sie `InitializeAsync` in der Datei mithilfe des folgenden `UpdateAddressBar` Codeausschnitts.</span><span class="sxs-lookup"><span data-stu-id="8829a-229">In the `Form1.cs` file, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1.  <span data-ttu-id="8829a-230">Damit webView die Webnachricht sendet und darauf antwortet, wird nach der Initialisierung ein Skript in den `CoreWebView2` Webinhalt eingesenkt:</span><span class="sxs-lookup"><span data-stu-id="8829a-230">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1.  <span data-ttu-id="8829a-231">Senden Sie die URL mithilfe von an den `postMessage` Host.</span><span class="sxs-lookup"><span data-stu-id="8829a-231">Send the URL to the host using `postMessage`.</span></span>
    1.  <span data-ttu-id="8829a-232">Registrieren Sie einen Ereignishandler, um eine vom Host gesendete Nachricht zu drucken.</span><span class="sxs-lookup"><span data-stu-id="8829a-232">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="8829a-233">Aktualisieren Sie `Form1.cs` in der Datei `InitializeAsync` so, dass sie mit dem folgenden Codeausschnitt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8829a-233">In the `Form1.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="8829a-234">Wählen Sie zum Erstellen und Ausführen der App `F5` aus.</span><span class="sxs-lookup"><span data-stu-id="8829a-234">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="8829a-235">Jetzt zeigt die Adressleiste den URI im WebView2-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="8829a-235">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="8829a-236">Wenn Sie außerdem erfolgreich zu einer neuen URL navigieren, benachrichtigt webView den Benutzer über die url, die in der WebView angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8829a-236">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Letzte App" lightbox="./media/winforms-finalapp.png":::
   <span data-ttu-id="8829a-238">Letzte App</span><span class="sxs-lookup"><span data-stu-id="8829a-238">Final app</span></span>  
:::image-end:::

<span data-ttu-id="8829a-239">Herzlichen Glückwunsch, Sie haben Ihre erste WebView2-App erstellt.</span><span class="sxs-lookup"><span data-stu-id="8829a-239">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="8829a-240">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8829a-240">Next steps</span></span>  

<span data-ttu-id="8829a-241">Navigieren Sie zu den folgenden Ressourcen, um weitere Informationen zu WebView2 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8829a-241">To continue learning more about WebView2, navigate to the following resources.</span></span>  

*   <span data-ttu-id="8829a-242">Weitere Informationen zum Erstellen von WebView2-Anwendungen finden Sie unter Bewährte Methoden für [die WebView2-Entwicklung.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="8829a-242">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="8829a-243">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="8829a-243">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="8829a-244">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="8829a-244">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
*   <span data-ttu-id="8829a-245">Ausführliche Informationen zur WebView2-API finden Sie unter [API-Referenz][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span><span class="sxs-lookup"><span data-stu-id="8829a-245">For detailed information about the WebView2 API, navigate to [API reference][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="8829a-246">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="8829a-246">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Bewährte Methoden für die WebView2-| Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Navigationsereignisse | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Microsoft.Web.WebView2.WinForms Namespace | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "WebView2-Klasse | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) Method | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Konfigurieren Ihrer Windows Forms-App für hohe DPI-Unterstützung – Unterstützung mit hohem DPI in Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Herunterladen von Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2-| Microsoft Edge Developer"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
