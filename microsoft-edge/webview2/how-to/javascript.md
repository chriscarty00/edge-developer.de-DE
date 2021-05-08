---
description: Informationen zur Verwendung von JavaScript in komplexen Szenarien in WebView2-Apps
title: Verwenden von JavaScript in WebView2-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 8db5c4a5b3709c144240fe88e6f8480445c1659f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535966"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a><span data-ttu-id="164e8-104">Verwenden von JavaScript in WebView für erweiterte Szenarien</span><span class="sxs-lookup"><span data-stu-id="164e8-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="164e8-105">Mithilfe von JavaScript in WebView2-Steuerelementen können Sie systemeigene Apps an Ihre Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="164e8-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="164e8-106">In diesem Artikel wird die Verwendung von JavaScript in WebView2 und die Entwicklung mit erweiterten WebView2-Features und -Funktionen erläutert.</span><span class="sxs-lookup"><span data-stu-id="164e8-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="164e8-107">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="164e8-107">Before you begin</span></span>  

<span data-ttu-id="164e8-108">In diesem Artikel wird davon ausgegangen, dass Sie bereits über ein funktionierendes Projekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="164e8-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="164e8-109">Wenn Sie kein Projekt haben und folgen möchten, navigieren Sie zu [WebView2 Erste Schritte Guide][Webview2GetStartedWpf].</span><span class="sxs-lookup"><span data-stu-id="164e8-109">If you do not have a project and want to follow along, navigate to the [WebView2 Get Started Guide][Webview2GetStartedWpf].</span></span>  

## <a name="basic-webview2-functions"></a><span data-ttu-id="164e8-110">Grundlegende WebView2-Funktionen</span><span class="sxs-lookup"><span data-stu-id="164e8-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="164e8-111">Verwenden Sie die folgenden Funktionen, um mit dem Einbetten von JavaScript in Ihre WebView-App zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="164e8-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="164e8-112">API</span><span class="sxs-lookup"><span data-stu-id="164e8-112">API</span></span>  | <span data-ttu-id="164e8-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="164e8-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="164e8-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="164e8-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="164e8-115">Führen Sie JavaScript in einem WebView-Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="164e8-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="164e8-116">Weitere Informationen finden Sie im Erste Schritte Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="164e8-116">For more information, navigate to the Get Started tutorial.</span></span> |
| [<span data-ttu-id="164e8-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="164e8-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="164e8-118">Wird ausgeführt, wenn das Dokumentobjektmodell \(DOM\) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="164e8-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <a name="scenario--running-a-dedicated-script-file"></a><span data-ttu-id="164e8-119">Szenario: Ausführen einer dedizierten Skriptdatei</span><span class="sxs-lookup"><span data-stu-id="164e8-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="164e8-120">Greifen Sie in diesem Abschnitt über Ihr WebView2-Steuerelement auf eine dedizierte JavaScript-Datei zu.</span><span class="sxs-lookup"><span data-stu-id="164e8-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="164e8-121">Obwohl das Schreiben von JavaScript-Inline für schnelle JavaScript-Befehle effizient sein kann, gehen JavaScript-Farbthemen und Zeilenformatierungen verloren, was das Schreiben großer Codeabschnitte in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="164e8-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="164e8-122">Um das Problem zu lösen, erstellen Sie eine separate JavaScript-Datei mit Ihrem Code, und übergeben Sie dann einen Verweis auf diese Datei mithilfe der `ExecuteScriptAsync` Parameter.</span><span class="sxs-lookup"><span data-stu-id="164e8-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="164e8-123">Erstellen Sie `.js` eine Datei in Ihrem Projekt, und fügen Sie den JavaScript-Code hinzu, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="164e8-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="164e8-124">Erstellen Sie beispielsweise eine Datei namens `script.js` .</span><span class="sxs-lookup"><span data-stu-id="164e8-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="164e8-125">Konvertieren Sie die JavaScript-Datei in eine Zeichenfolge, die an übergeben `ExecuteScriptAsync` wird.</span><span class="sxs-lookup"><span data-stu-id="164e8-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="164e8-126">Um Ihre JavaScript-Datei in eine Zeichenfolge zu konvertieren, kopieren Sie den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="164e8-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="164e8-127">Fügen Sie den Code in `MainWindow.xaml.cs` ein.</span><span class="sxs-lookup"><span data-stu-id="164e8-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="164e8-128">Übergeben Sie Ihre Textvariable mithilfe `ExecuteScriptAsync` von .</span><span class="sxs-lookup"><span data-stu-id="164e8-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  
    
## <a name="scenario--remove-drag-and-drop-functionality"></a><span data-ttu-id="164e8-129">Szenario: Entfernen der Drag -and-Drop-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="164e8-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="164e8-130">Verwenden Sie in diesem Abschnitt JavaScript, um die Drag -and-Drop-Funktionalität aus Ihrem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="164e8-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="164e8-131">Erkunden Sie zunächst die aktuelle Drag -and-Drop-Funktion.</span><span class="sxs-lookup"><span data-stu-id="164e8-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="164e8-132">Erstellen Sie `.txt` eine Datei, um drag-and-drop zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="164e8-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="164e8-133">Erstellen Sie z. B. eine Datei mit `contoso.txt` dem Namen, und fügen Sie ihr Text hinzu.</span><span class="sxs-lookup"><span data-stu-id="164e8-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="164e8-134">Führen Sie Ihr Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="164e8-134">Run your project.</span></span>  
1.  <span data-ttu-id="164e8-135">Ziehen Sie die Datei per Drag -and-Drop `contoso.txt` in das WebView-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="164e8-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="164e8-136">Es wird ein neues Fenster geöffnet, das das Ergebnis des Codes in Ihrem Beispielprojekt ist.</span><span class="sxs-lookup"><span data-stu-id="164e8-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/drag-text.png" alt-text="Ergebnis des Ziehens und Ablegens contoso.txt" lightbox="./media/drag-text.png":::
       <span data-ttu-id="164e8-138">Ergebnis des Ziehens und Ablegens contoso.txt</span><span class="sxs-lookup"><span data-stu-id="164e8-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  
    
<span data-ttu-id="164e8-139">Fügen Sie nun Code hinzu, um die Drag -and-Drop-Funktion aus dem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="164e8-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="164e8-140">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in `MainWindow.xaml.cs` ein.</span><span class="sxs-lookup"><span data-stu-id="164e8-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
    
1.  <span data-ttu-id="164e8-141">Führen Sie Ihr Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="164e8-141">Run your project.</span></span>  
1.  <span data-ttu-id="164e8-142">Versuchen Sie, drag-and-drop `contoso.txt` zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="164e8-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="164e8-143">Vergewissern Sie sich, dass Drag -and-Drop nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="164e8-143">Confirm that you are not able to drag-and-drop.</span></span>  
    
## <a name="scenario--removing-the-context-menu"></a><span data-ttu-id="164e8-144">Szenario: Entfernen des Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="164e8-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="164e8-145">Entfernen Sie in diesem Abschnitt das Standardkontextmenü aus Ihrem WebView2-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="164e8-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="164e8-146">Erkunden Sie zunächst die aktuelle Kontextmenüfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="164e8-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="164e8-147">Führen Sie Ihr Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="164e8-147">Run your project.</span></span>  
1.  <span data-ttu-id="164e8-148">Zeigen Sie auf eine beliebige Stelle im WebView2-Steuerelement, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="164e8-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="164e8-149">Im Kontextmenü werden die Standardoptionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="164e8-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/context-menu.png" alt-text="Das Kontextmenü mit den Standardauswahlmöglichkeiten" lightbox="./media/context-menu.png":::
       <span data-ttu-id="164e8-151">Das Kontextmenü mit den Standardauswahlmöglichkeiten</span><span class="sxs-lookup"><span data-stu-id="164e8-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="164e8-152">Fügen Sie nun Code hinzu, um die kontextbezogene Menüfunktionalität aus dem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="164e8-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="164e8-153">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in `MainWindow.xaml.cs` ein.</span><span class="sxs-lookup"><span data-stu-id="164e8-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
    
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  
    
1.  <span data-ttu-id="164e8-154">Führen Sie den Code erneut aus.</span><span class="sxs-lookup"><span data-stu-id="164e8-154">Run the code again.</span></span>  <span data-ttu-id="164e8-155">Vergewissern Sie sich, dass Sie kein Kontextmenü öffnen können \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="164e8-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="164e8-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="164e8-156">See also</span></span>  

*   <span data-ttu-id="164e8-157">Um mit WebView2 zu beginnen, navigieren Sie zu [WebView2 Erste Schritte Guides][Webview2MainGetStarted].</span><span class="sxs-lookup"><span data-stu-id="164e8-157">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span></span>  
*   <span data-ttu-id="164e8-158">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="164e8-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="164e8-159">Ausführliche Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="164e8-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="164e8-160">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="164e8-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="164e8-161">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="164e8-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft Docs"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 - interface ICoreWebView2 | Microsoft Docs"  

[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
