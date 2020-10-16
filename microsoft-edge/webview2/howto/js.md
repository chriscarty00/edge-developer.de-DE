---
description: Informationen zur Verwendung von JavaScript in komplexen Szenarien in WebView2-apps
title: Verwenden von JavaScript in WebView2-apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 0fd4e33b7cfc16dcd19a850147b6efbca8922a8e
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120069"
---
# <span data-ttu-id="20d3a-104">Verwenden von JavaScript in WebView für erweiterte Szenarien</span><span class="sxs-lookup"><span data-stu-id="20d3a-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="20d3a-105">Durch die Verwendung von JavaScript in WebView2-Steuerelementen können Sie systemeigene apps an Ihre Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="20d3a-106">In diesem Artikel wird erläutert, wie Sie JavaScript in WebView2 verwenden, und es wird erläutert, wie Sie mithilfe der erweiterten WebView2-Features und-Funktionen entwickeln können.</span><span class="sxs-lookup"><span data-stu-id="20d3a-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <span data-ttu-id="20d3a-107">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="20d3a-107">Before you begin</span></span>  

<span data-ttu-id="20d3a-108">In diesem Artikel wird davon ausgegangen, dass Sie bereits über ein funktionierendes Projekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="20d3a-109">Wenn Sie nicht über ein Projekt verfügen und folgen möchten, navigieren Sie zum [WebView2-Leitfaden für erste Schritte][Webview2GettingstartedWpf].</span><span class="sxs-lookup"><span data-stu-id="20d3a-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <span data-ttu-id="20d3a-110">Grundlegende WebView2-Funktionen</span><span class="sxs-lookup"><span data-stu-id="20d3a-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="20d3a-111">Verwenden Sie die folgenden Funktionen, um mit der Einbettung von JavaScript in Ihre WebView-APP zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="20d3a-112">API</span><span class="sxs-lookup"><span data-stu-id="20d3a-112">API</span></span>  | <span data-ttu-id="20d3a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20d3a-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="20d3a-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="20d3a-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="20d3a-115">Führen Sie JavaScript in einem WebView-Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="20d3a-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="20d3a-116">Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zum Lernprogramm "erste Schritte".</span><span class="sxs-lookup"><span data-stu-id="20d3a-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="20d3a-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="20d3a-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="20d3a-118">Wird ausgeführt, wenn das Dokumentobjektmodell \ (DOM \) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="20d3a-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <span data-ttu-id="20d3a-119">Szenario: Ausführen einer dedizierten Skriptdatei</span><span class="sxs-lookup"><span data-stu-id="20d3a-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="20d3a-120">Greifen Sie in diesem Abschnitt auf eine dedizierte JavaScript-Datei über Ihr WebView2-Steuerelement zu.</span><span class="sxs-lookup"><span data-stu-id="20d3a-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="20d3a-121">Obwohl das Schreiben von JavaScript Inline für schnelle JavaScript-Befehle effizient sein kann, verlieren Sie JavaScript-Farbdesigns und die Zeilenformatierung, wodurch große Codeabschnitte in Visual Studio schwierig zu schreiben sind.</span><span class="sxs-lookup"><span data-stu-id="20d3a-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="20d3a-122">Um das Problem zu beheben, erstellen Sie eine separate JavaScript-Datei mit Ihrem Code, und übergeben Sie dann mithilfe der Parameter einen Verweis auf diese Datei `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="20d3a-123">Erstellen Sie eine `.js` Datei in Ihrem Projekt, und fügen Sie den JavaScript-Code hinzu, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="20d3a-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="20d3a-124">Erstellen Sie beispielsweise eine Datei mit dem Namen `script.js` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="20d3a-125">Konvertieren Sie die JavaScript-Datei in eine Zeichenfolge, die übergeben wird `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="20d3a-126">Wenn Sie Ihre JavaScript-Datei in eine Zeichenfolge konvertieren möchten, kopieren Sie den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="20d3a-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="20d3a-127">Fügen Sie den Code in ein `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="20d3a-128">Übergeben Sie die Textvariable mit `ExecuteScriptAsync` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <span data-ttu-id="20d3a-129">Szenario: Entfernen von Drag & Drop-Funktionen</span><span class="sxs-lookup"><span data-stu-id="20d3a-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="20d3a-130">Verwenden Sie in diesem Abschnitt JavaScript, um die Drag & Drop-Funktion aus Ihrem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="20d3a-131">Erkunden Sie zunächst die aktuelle Drag & Drop-Funktion.</span><span class="sxs-lookup"><span data-stu-id="20d3a-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="20d3a-132">Erstellen `.txt` Sie eine Datei, um Sie zu ziehen und abzulegen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="20d3a-133">Erstellen Sie beispielsweise eine Datei mit dem Namen, `contoso.txt` und fügen Sie Text hinzu.</span><span class="sxs-lookup"><span data-stu-id="20d3a-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="20d3a-134">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="20d3a-134">Run your project.</span></span>  
1.  <span data-ttu-id="20d3a-135">Ziehen Sie die `contoso.txt` Datei auf das WebView-Steuerelement, und legen Sie Sie ab.</span><span class="sxs-lookup"><span data-stu-id="20d3a-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="20d3a-136">Es wird ein neues Fenster geöffnet, das das Ergebnis des Codes in Ihrem Beispielprojekt ist.</span><span class="sxs-lookup"><span data-stu-id="20d3a-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Ergebnis beim Ziehen und Ablegen von contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="20d3a-138">Ergebnis beim Ziehen und Ablegen von contoso.txt</span><span class="sxs-lookup"><span data-stu-id="20d3a-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="20d3a-139">Fügen Sie jetzt Code hinzu, um die Drag & Drop-Funktion aus dem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="20d3a-140">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in ein `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="20d3a-141">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="20d3a-141">Run your project.</span></span>  
1.  <span data-ttu-id="20d3a-142">Ziehen und ablegen versuchen `contoso.txt` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="20d3a-143">Vergewissern Sie sich, dass Sie nicht in der Lage sind, Drag & Drop zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <span data-ttu-id="20d3a-144">Szenario: Entfernen des Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="20d3a-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="20d3a-145">Entfernen Sie in diesem Abschnitt das Standardkontextmenü aus Ihrem WebView2-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="20d3a-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="20d3a-146">Erkunden Sie zunächst die aktuelle Kontextmenü Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="20d3a-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="20d3a-147">Führen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="20d3a-147">Run your project.</span></span>  
1.  <span data-ttu-id="20d3a-148">Zeigen Sie auf das WebView2-Steuerelement, und öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \).</span><span class="sxs-lookup"><span data-stu-id="20d3a-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="20d3a-149">Das Kontextmenü zeigt die Standardauswahl an.</span><span class="sxs-lookup"><span data-stu-id="20d3a-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Ergebnis beim Ziehen und Ablegen von contoso.txt" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="20d3a-151">Das Kontextmenü mit den Standardoptionen</span><span class="sxs-lookup"><span data-stu-id="20d3a-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="20d3a-152">Fügen Sie nun Code hinzu, um die Kontextmenü Funktionalität des WebView2-Steuerelements zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="20d3a-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="20d3a-153">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in ein `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="20d3a-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="20d3a-154">Führen Sie den Code erneut aus.</span><span class="sxs-lookup"><span data-stu-id="20d3a-154">Run the code again.</span></span>  <span data-ttu-id="20d3a-155">Vergewissern Sie sich, dass Sie nicht in der Lage sind, ein Kontextmenü zu öffnen \ (Klicken Sie mit der rechten Maustaste auf \).</span><span class="sxs-lookup"><span data-stu-id="20d3a-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <span data-ttu-id="20d3a-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="20d3a-156">See also</span></span>  

*   <span data-ttu-id="20d3a-157">Weitere Informationen zu den ersten Schritten mit WebView2 finden Sie unter [Erste Schritte mit WebView2][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="20d3a-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="20d3a-158">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] Repo auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="20d3a-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="20d3a-159">Detaillierte Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="20d3a-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="20d3a-160">Wenn Sie weitere Informationen zu WebView2 möchten, navigieren Sie zu [WebView2-Ressourcen][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="20d3a-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <span data-ttu-id="20d3a-161">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="20d3a-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated-0.9.579-Interface ICoreWebView2 | Microsoft docs"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync (String)-Methode (Microsoft. Web. WebView2. WPF) | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
