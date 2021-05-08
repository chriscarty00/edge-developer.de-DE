---
description: Informationen zur Verwendung von JavaScript in komplexen Szenarien in WebView2-Apps
title: Verwenden von JavaScript in WebView2-Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: da04d1e24b95dfa7ea477bbd228fd46b64727ec3
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536524"
---
# <a name="use-javascript-in-webview-for-extended-scenarios"></a><span data-ttu-id="c767d-104">Verwenden von JavaScript in WebView für erweiterte Szenarien</span><span class="sxs-lookup"><span data-stu-id="c767d-104">Use JavaScript in WebView for extended scenarios</span></span>  

<span data-ttu-id="c767d-105">Mithilfe von JavaScript in WebView2-Steuerelementen können Sie systemeigene Apps an Ihre Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="c767d-105">Using JavaScript in WebView2 controls allows you to customize native apps to meet your requirements.</span></span>  <span data-ttu-id="c767d-106">In diesem Artikel wird die Verwendung von JavaScript in WebView2 und die Entwicklung mit erweiterten WebView2-Features und -Funktionen erläutert.</span><span class="sxs-lookup"><span data-stu-id="c767d-106">This article explores how to use JavaScript in WebView2, and reviews how to develop using advanced WebView2 features and functionality.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="c767d-107">Vorbemerkungen</span><span class="sxs-lookup"><span data-stu-id="c767d-107">Before you begin</span></span>  

<span data-ttu-id="c767d-108">In diesem Artikel wird davon ausgegangen, dass Sie bereits über ein funktionierendes Projekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="c767d-108">This article assumes that you already have a working project.</span></span>  <span data-ttu-id="c767d-109">Wenn Sie kein Projekt haben und mit folgen möchten, navigieren Sie zum [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span><span class="sxs-lookup"><span data-stu-id="c767d-109">If you do not have a project and want to follow along, navigate to the [WebView2 Getting Started Guide][Webview2GettingstartedWpf].</span></span>  

## <a name="basic-webview2-functions"></a><span data-ttu-id="c767d-110">Grundlegende WebView2-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c767d-110">Basic WebView2 Functions</span></span>  

<span data-ttu-id="c767d-111">Verwenden Sie die folgenden Funktionen, um mit dem Einbetten von JavaScript in Ihre WebView-App zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="c767d-111">Use the following functions to begin embedding JavaScript in your WebView app.</span></span>  

| <span data-ttu-id="c767d-112">API</span><span class="sxs-lookup"><span data-stu-id="c767d-112">API</span></span>  | <span data-ttu-id="c767d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c767d-113">Description</span></span>  |
|:--- |:--- |  
| [<span data-ttu-id="c767d-114">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="c767d-114">ExecuteScriptAsync</span></span>][Webview2ReferenceWpfMicrosoftWebExecutescriptasync] | <span data-ttu-id="c767d-115">Führen Sie JavaScript in einem WebView-Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="c767d-115">Run JavaScript in a WebView control.</span></span> <span data-ttu-id="c767d-116">Weitere Informationen finden Sie im Lernprogramm Erste Schritte.</span><span class="sxs-lookup"><span data-stu-id="c767d-116">For more information, navigate to the Getting Started tutorial.</span></span> |
| [<span data-ttu-id="c767d-117">OnDocumentCreatedAsync</span><span class="sxs-lookup"><span data-stu-id="c767d-117">OnDocumentCreatedAsync</span></span>][Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated] | <span data-ttu-id="c767d-118">Wird ausgeführt, wenn das Dokumentobjektmodell \(DOM\) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c767d-118">Runs when the Document Object Model \(DOM\) is created.</span></span> |
      
## <a name="scenario--running-a-dedicated-script-file"></a><span data-ttu-id="c767d-119">Szenario: Ausführen einer dedizierten Skriptdatei</span><span class="sxs-lookup"><span data-stu-id="c767d-119">Scenario:  Running a dedicated script file</span></span>  

<span data-ttu-id="c767d-120">Greifen Sie in diesem Abschnitt über Ihr WebView2-Steuerelement auf eine dedizierte JavaScript-Datei zu.</span><span class="sxs-lookup"><span data-stu-id="c767d-120">In this section, access a dedicated JavaScript file from your WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="c767d-121">Obwohl das Schreiben von JavaScript-Inline für schnelle JavaScript-Befehle effizient sein kann, gehen JavaScript-Farbthemen und Zeilenformatierungen verloren, was das Schreiben großer Codeabschnitte in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c767d-121">Although writing JavaScript inline may be efficient for quick JavaScript commands, you lose JavaScript color themes and line formatting that makes it difficult to write large sections of code in Visual Studio.</span></span>  

<span data-ttu-id="c767d-122">Um das Problem zu lösen, erstellen Sie eine separate JavaScript-Datei mit Ihrem Code, und übergeben Sie dann einen Verweis auf diese Datei mithilfe der `ExecuteScriptAsync` Parameter.</span><span class="sxs-lookup"><span data-stu-id="c767d-122">To solve the problem, create a separate JavaScript file with your code, and then pass a reference to that file using the `ExecuteScriptAsync` parameters.</span></span>  

1.  <span data-ttu-id="c767d-123">Erstellen Sie `.js` eine Datei in Ihrem Projekt, und fügen Sie den JavaScript-Code hinzu, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="c767d-123">Create a `.js` file in your project, and add the JavaScript code that you want to run.</span></span>  <span data-ttu-id="c767d-124">Erstellen Sie beispielsweise eine Datei namens `script.js` .</span><span class="sxs-lookup"><span data-stu-id="c767d-124">For example, create a file called `script.js`.</span></span>  
1.  <span data-ttu-id="c767d-125">Konvertieren Sie die JavaScript-Datei in eine Zeichenfolge, die an übergeben `ExecuteScriptAsync` wird.</span><span class="sxs-lookup"><span data-stu-id="c767d-125">Convert the JavaScript file to a string that is passed to `ExecuteScriptAsync`.</span></span>  
    1.  <span data-ttu-id="c767d-126">Um Ihre JavaScript-Datei in eine Zeichenfolge zu konvertieren, kopieren Sie den folgenden Codeausschnitt.</span><span class="sxs-lookup"><span data-stu-id="c767d-126">To convert your JavaScript file into a string, copy the following code snippet.</span></span>  
        
        ```csharp
        string text = System.IO.File.ReadAllText(@"C:\PATH_TO_YOUR_FILE\script.js");
        ```  
        
    1.  <span data-ttu-id="c767d-127">Fügen Sie den Code in `MainWindow.xaml.cs` ein.</span><span class="sxs-lookup"><span data-stu-id="c767d-127">Paste the code into `MainWindow.xaml.cs`.</span></span>  
1.  <span data-ttu-id="c767d-128">Übergeben Sie Ihre Textvariable mithilfe `ExecuteScriptAsync` von .</span><span class="sxs-lookup"><span data-stu-id="c767d-128">Pass your text variable using `ExecuteScriptAsync`.</span></span>  
    
    ```csharp
    await webView.CoreWebView2.ExecuteScriptAsync(text);
    ```  

## <a name="scenario--remove-drag-and-drop-functionality"></a><span data-ttu-id="c767d-129">Szenario: Entfernen der Drag -and-Drop-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="c767d-129">Scenario:  Remove drag-and-drop functionality</span></span>  

<span data-ttu-id="c767d-130">Verwenden Sie in diesem Abschnitt JavaScript, um die Drag -and-Drop-Funktionalität aus Ihrem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c767d-130">In this section, use JavaScript to remove the drag-and-drop functionality from your WebView2 control.</span></span>  

<span data-ttu-id="c767d-131">Erkunden Sie zunächst die aktuelle Drag -and-Drop-Funktion.</span><span class="sxs-lookup"><span data-stu-id="c767d-131">To begin, explore the current drag-and-drop functionality.</span></span>  

1.  <span data-ttu-id="c767d-132">Erstellen Sie `.txt` eine Datei, um drag-and-drop zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c767d-132">Create a `.txt` file in order to drag-and-drop.</span></span>  <span data-ttu-id="c767d-133">Erstellen Sie z. B. eine Datei mit `contoso.txt` dem Namen, und fügen Sie ihr Text hinzu.</span><span class="sxs-lookup"><span data-stu-id="c767d-133">For example, create a file named `contoso.txt` and add text to it.</span></span>  
1.  <span data-ttu-id="c767d-134">Führen Sie Ihr Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c767d-134">Run your project.</span></span>  
1.  <span data-ttu-id="c767d-135">Ziehen Sie die Datei per Drag -and-Drop `contoso.txt` in das WebView-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c767d-135">Drag-and-drop the `contoso.txt` file onto the WebView control.</span></span>  <span data-ttu-id="c767d-136">Es wird ein neues Fenster geöffnet, das das Ergebnis des Codes in Ihrem Beispielprojekt ist.</span><span class="sxs-lookup"><span data-stu-id="c767d-136">A new window opens, which is the result of the code in your sample project.</span></span>  
    
    :::image type="complex" source="./media/dragtext.png" alt-text="Ergebnis des Ziehens und Ablegens contoso.txt" lightbox="./media/dragtext.png":::
       <span data-ttu-id="c767d-138">Ergebnis des Ziehens und Ablegens contoso.txt</span><span class="sxs-lookup"><span data-stu-id="c767d-138">Result of dragging and dropping contoso.txt</span></span>  
    :::image-end:::  

<span data-ttu-id="c767d-139">Fügen Sie nun Code hinzu, um die Drag -and-Drop-Funktion aus dem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c767d-139">Now, add code to remove the drag-and-drop functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="c767d-140">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in `MainWindow.xaml.cs` ein.</span><span class="sxs-lookup"><span data-stu-id="c767d-140">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>   
            
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('dragover',function(e){e.preventDefault();},false);");
    
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('drop',function(e){" +
    "e.preventDefault();" +
    "console.log(e.dataTransfer);" +
    "console.log(e.dataTransfer.files[0])" +
    "}, false);");
    ```  
          
1.  <span data-ttu-id="c767d-141">Führen Sie Ihr Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c767d-141">Run your project.</span></span>  
1.  <span data-ttu-id="c767d-142">Versuchen Sie, drag-and-drop `contoso.txt` zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="c767d-142">Try to drag-and-drop `contoso.txt`.</span></span>  <span data-ttu-id="c767d-143">Vergewissern Sie sich, dass Drag -and-Drop nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="c767d-143">Confirm that you are not able to drag-and-drop.</span></span>  

## <a name="scenario--removing-the-context-menu"></a><span data-ttu-id="c767d-144">Szenario: Entfernen des Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="c767d-144">Scenario:  Removing the Context Menu</span></span>  

<span data-ttu-id="c767d-145">Entfernen Sie in diesem Abschnitt das Standardkontextmenü aus Ihrem WebView2-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c767d-145">In this section, remove the default context menu from your WebView2 control.</span></span>  

<span data-ttu-id="c767d-146">Erkunden Sie zunächst die aktuelle Kontextmenüfunktionalität.</span><span class="sxs-lookup"><span data-stu-id="c767d-146">To begin, explore the current contextual menu functionality.</span></span>  

1.  <span data-ttu-id="c767d-147">Führen Sie Ihr Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c767d-147">Run your project.</span></span>  
1.  <span data-ttu-id="c767d-148">Zeigen Sie auf eine beliebige Stelle im WebView2-Steuerelement, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="c767d-148">Hover anywhere on the WebView2 control and open the context menu \(right-click\).</span></span>  <span data-ttu-id="c767d-149">Im Kontextmenü werden die Standardoptionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c767d-149">The context menu displays the default choices.</span></span>  
    
    :::image type="complex" source="./media/contextmenu.png" alt-text="Das Kontextmenü mit den Standardauswahlmöglichkeiten" lightbox="./media/contextmenu.png":::
       <span data-ttu-id="c767d-151">Das Kontextmenü mit den Standardauswahlmöglichkeiten</span><span class="sxs-lookup"><span data-stu-id="c767d-151">The context menu showing the default choices</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c767d-152">Fügen Sie nun Code hinzu, um die kontextbezogene Menüfunktionalität aus dem WebView2-Steuerelement zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c767d-152">Now add code to remove the contextual menu functionality from the WebView2 control.</span></span>  

1.  <span data-ttu-id="c767d-153">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn `InitializeAsync()` in `MainWindow.xaml.cs` ein.</span><span class="sxs-lookup"><span data-stu-id="c767d-153">Copy and paste the following code snippet into `InitializeAsync()` in `MainWindow.xaml.cs`.</span></span>    
        
    ```csharp   
    await webView.CoreWebView2.ExecuteScriptAsync("window.addEventListener('contextmenu', window => {window.preventDefault();});");
    ```  

1.  <span data-ttu-id="c767d-154">Führen Sie den Code erneut aus.</span><span class="sxs-lookup"><span data-stu-id="c767d-154">Run the code again.</span></span>  <span data-ttu-id="c767d-155">Vergewissern Sie sich, dass Sie kein Kontextmenü öffnen können \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="c767d-155">Confirm that you're not able to open a context menu \(right-click\).</span></span>  
   
## <a name="see-also"></a><span data-ttu-id="c767d-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c767d-156">See also</span></span>  

*   <span data-ttu-id="c767d-157">Weitere Informationen zu den ersten Schritte mit WebView2 finden Sie unter [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="c767d-157">For more information on getting started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="c767d-158">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie im [WebView2Samples-Repository][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="c767d-158">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>  
*   <span data-ttu-id="c767d-159">Ausführliche Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="c767d-159">For detailed information on WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>  
*   <span data-ttu-id="c767d-160">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="c767d-160">For more information on WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="c767d-161">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="c767d-161">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  


[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft Docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2Addscripttoexecuteondocumentcreated]: /microsoft-edge/webview2/reference/win32/icorewebview2#addscripttoexecuteondocumentcreated "AddScriptToExecuteOnDocumentCreated - 0.9.579 - interface ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
