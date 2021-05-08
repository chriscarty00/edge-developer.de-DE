---
description: Erfahren Sie, wie Sie die WebView2-Ladebibliothek statisch verknüpfen.
title: So verknüpfen Sie die WebView2-Ladebibliothek statisch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 8f48a4fde9e2960de6156fc14db8c84f87a49868
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535959"
---
# <a name="statically-link-the-webview2-loader-library"></a><span data-ttu-id="1d11e-104">Statische Verknüpfung der WebView2-Ladebibliothek</span><span class="sxs-lookup"><span data-stu-id="1d11e-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="1d11e-105">Möglicherweise möchten Sie Ihre Anwendung mit einer einzelnen ausführbaren Datei anstelle eines Pakets mit vielen Dateien verteilen.</span><span class="sxs-lookup"><span data-stu-id="1d11e-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="1d11e-106">Um eine einzelne ausführbare Datei zu erstellen oder die Größe Ihres Pakets zu reduzieren, sollten Sie die WebView2Loader-Dateien statisch verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1d11e-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="1d11e-107">Das WebView2 SDK enthält eine Headerdatei `WebView2Loader.dll` und die `IDL` Datei.</span><span class="sxs-lookup"><span data-stu-id="1d11e-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="1d11e-108">ist eine kleine Komponente, die Apps dabei hilft, die WebView2-Runtime oder nicht stabile Kanäle der Microsoft Edge auf dem Gerät zu finden.</span><span class="sxs-lookup"><span data-stu-id="1d11e-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="1d11e-109">Führen Sie die folgenden Schritte für Apps aus, die keines versenden `WebView2Loader.dll` möchten.</span><span class="sxs-lookup"><span data-stu-id="1d11e-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="1d11e-110">Öffnen Sie die Projektdatei für Ihre App in einem Texteditor, z. `.vcxproj` B. Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="1d11e-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1d11e-111">Die `.vcproj` Projektdatei kann eine ausgeblendete Datei sein, d. h. sie wird nicht in der Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1d11e-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="1d11e-112">Verwenden Sie die Befehlszeile, um nach ausgeblendeten Dateien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1d11e-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="1d11e-113">Suchen Sie den Abschnitt im Code, in den Sie die WebView2-NuGet Packzieldateien eingeben.</span><span class="sxs-lookup"><span data-stu-id="1d11e-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="1d11e-114">Die Position im Code wird in der folgenden Abbildung hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="1d11e-114">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/insert-here.png" alt-text="Project Codeausschnitt für Dateien" lightbox="./media/insert-here.png":::
       <span data-ttu-id="1d11e-116">Project Codeausschnitt für Dateien</span><span class="sxs-lookup"><span data-stu-id="1d11e-116">Project Files code snippet</span></span>   
    :::image-end:::  
    
1.  <span data-ttu-id="1d11e-117">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn dort ein, wo `Microsoft.Web.WebView2.targets` der enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1d11e-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  
    
    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```  
    
    :::image type="complex" source="./media/static-lib.png" alt-text="Eingefügter Codeausschnitt" lightbox="./media/static-lib.png":::
       <span data-ttu-id="1d11e-119">Eingefügter Codeausschnitt</span><span class="sxs-lookup"><span data-stu-id="1d11e-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1d11e-120">Bearbeiten Sie die zusätzlichen Abhängigkeiten der Buildkonfiguration für Ihre App.</span><span class="sxs-lookup"><span data-stu-id="1d11e-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="1d11e-121">Suchen Sie zunächst alle `<AdditionalDependencies>` Tags.</span><span class="sxs-lookup"><span data-stu-id="1d11e-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="1d11e-122">Fügen Sie jeweils als zusätzliche Abhängigkeit zu `version.lib` jeder anderen Buildkonfiguration in der Datei `.vcxproj` hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d11e-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/version-lib.png" alt-text="Hinzufügen von version.lib zu ItemDefinitionGroups" lightbox="./media/version-lib.png":::
       <span data-ttu-id="1d11e-124">Hinzufügen `version.lib` zu</span><span class="sxs-lookup"><span data-stu-id="1d11e-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="1d11e-125">Das WebView2-Team möchte das Hinzufügen der zusätzlichen Abhängigkeit in zukünftigen Versionen automatisieren.</span><span class="sxs-lookup"><span data-stu-id="1d11e-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1.  <span data-ttu-id="1d11e-126">Kompilieren und Ausführen Der App.</span><span class="sxs-lookup"><span data-stu-id="1d11e-126">Compile and run your app.</span></span>  
    
## <a name="getting-in-touch-with-the-webview2-team"></a><span data-ttu-id="1d11e-127">Kontakt mit dem WebView2-Team</span><span class="sxs-lookup"><span data-stu-id="1d11e-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

## <a name="see-also"></a><span data-ttu-id="1d11e-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1d11e-128">See also</span></span>  

*   <span data-ttu-id="1d11e-129">Um mit WebView2 zu beginnen, navigieren Sie zu [WebView2 Erste Schritte Guides][Webview2MainGetStarted].</span><span class="sxs-lookup"><span data-stu-id="1d11e-129">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span></span>  
*   <span data-ttu-id="1d11e-130">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="1d11e-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="1d11e-131">Weitere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="1d11e-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="1d11e-132">Weitere Informationen zu WebView2 finden Sie unter [WebView2 Resources][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="1d11e-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Vorschau) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? - JavaScript-Debugger für Visual Studio Code - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) WebView-Anwendungen - Visual Studio Code - Debugger für Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
