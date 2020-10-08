---
description: Hier erfahren Sie, wie Sie die WebView2-Loader-Bibliothek statisch verknüpfen.
title: So verknüpfen Sie die WebView2-Ladeprogramm Bibliothek statisch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: b7e0ec70cb00f318d4eb67254f37fcec79a5fcf6
ms.sourcegitcommit: 903524ab85321ade278facd741d6487e8cabe33f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100307"
---
# <span data-ttu-id="6c268-104">So verknüpfen Sie die WebView2-Ladeprogramm Bibliothek statisch</span><span class="sxs-lookup"><span data-stu-id="6c268-104">How to Statically link the WebView2 loader library</span></span>  

## <span data-ttu-id="6c268-105">Kontext</span><span class="sxs-lookup"><span data-stu-id="6c268-105">Context</span></span>  

<span data-ttu-id="6c268-106">Was ist der WebView2Loader.dll?</span><span class="sxs-lookup"><span data-stu-id="6c268-106">What is the WebView2Loader.dll?</span></span>  

*   <span data-ttu-id="6c268-107">Das WebView2-SDK enthält eine Headerdatei `WebView2Loader.dll.` und die `IDL` Datei.</span><span class="sxs-lookup"><span data-stu-id="6c268-107">The WebView2 SDK contains a header file, `WebView2Loader.dll.`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="6c268-108">ist eine kleine Komponente, die apps bei der Suche nach der WebView2-Runtime (oder nicht stabilen Microsoft Edge-Kanälen) auf dem Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c268-108">is a small component that helps apps locate the WebView2 Runtime (or non-stable Microsoft Edge channels) on the device.</span></span>  

<span data-ttu-id="6c268-109">Führen Sie die folgenden Schritte aus, wenn apps, die über eine einzige Laufzeit verfügen und keine senden möchten `WebView2Loader.dll` , die folgenden Schritte **Ausführen** .</span><span class="sxs-lookup"><span data-stu-id="6c268-109">For apps that have a single runtime, and do not want to ship a `WebView2Loader.dll`, complete the following **Procedure** steps.</span></span>  

## <span data-ttu-id="6c268-110">Verfahren</span><span class="sxs-lookup"><span data-stu-id="6c268-110">Procedure</span></span>  

1.  <span data-ttu-id="6c268-111">Öffnen `.vcxproj` Sie die Projektdatei für Ihre APP in einem Text-Editor wie Visual Studio-Code.</span><span class="sxs-lookup"><span data-stu-id="6c268-111">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6c268-112">Die `.vcproj` Projektdatei kann eine versteckte Datei sein, was bedeutet, dass Sie in Visual Studio nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c268-112">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="6c268-113">Verwenden Sie die Befehlszeile, um eine versteckte Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6c268-113">Use the command-line to find a hidden file.</span></span>  
    
1.  <span data-ttu-id="6c268-114">Suchen Sie den Abschnitt im Code, in den Sie die WebView2 NuGet-Paket Zieldateien einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="6c268-114">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="6c268-115">Die Position im Code ist in der folgenden Abbildung hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="6c268-115">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/inserthere.png"::: 
       <span data-ttu-id="6c268-117">Codeausschnitt für Projektdateien</span><span class="sxs-lookup"><span data-stu-id="6c268-117">Project Files code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6c268-118">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn überall im `Microsoft.Web.WebView2.targets` Lieferumfang ein.</span><span class="sxs-lookup"><span data-stu-id="6c268-118">Copy the following code snippet and paste it everywhere the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="6c268-119">Fügen Sie den Codebeispiels Weise nach dem folgenden Codeblock ein.</span><span class="sxs-lookup"><span data-stu-id="6c268-119">For example, include it after the following code block.</span></span>  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/staticlib.png"::: 
       <span data-ttu-id="6c268-121">Eingefügter Codeausschnitt</span><span class="sxs-lookup"><span data-stu-id="6c268-121">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6c268-122">Bearbeiten Sie die zusätzlichen Abhängigkeiten der Buildkonfiguration für Ihre APP.</span><span class="sxs-lookup"><span data-stu-id="6c268-122">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="6c268-123">Suchen Sie zunächst alle `<AdditionalDependencies>` Kategorien.</span><span class="sxs-lookup"><span data-stu-id="6c268-123">To begin, find all of the `<AdditionalDependencies>` tags.</span></span>  
1.  <span data-ttu-id="6c268-124">Fügen Sie `version.lib` jeder anderen Buildkonfiguration in der `.vcxproj` Datei für Ihre APP eine zusätzliche Abhängigkeit hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c268-124">Add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file for your app.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/versionlib.png"::: 
       <span data-ttu-id="6c268-126">Hinzufügen `version.lib` zu</span><span class="sxs-lookup"><span data-stu-id="6c268-126">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6c268-127">Das WebView2-Team zielt darauf ab, den zusätzlichen Abhängigkeits Schritt in zukünftigen Versionen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="6c268-127">The WebView2 team aims to automate the additional dependency step in future releases.</span></span>  
    
<span data-ttu-id="6c268-128">Kompilieren und Bereitstellen Ihrer APP</span><span class="sxs-lookup"><span data-stu-id="6c268-128">Compile and deploy your app.</span></span>  <span data-ttu-id="6c268-129">Erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6c268-129">Success.</span></span>  

## <span data-ttu-id="6c268-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c268-130">See also</span></span>  

*   <span data-ttu-id="6c268-131">Um mit der Verwendung von WebView2 zu beginnen, navigieren Sie zu [WebView2 Anleitungen für erste Schritte][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="6c268-131">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="6c268-132">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="6c268-132">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="6c268-133">Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="6c268-133">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="6c268-134">Wenn Sie weitere Informationen zu WebView2 möchten, navigieren Sie zu [WebView2-Ressourcen][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="6c268-134">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="6c268-135">Kontakt mit dem WebView2-Team</span><span class="sxs-lookup"><span data-stu-id="6c268-135">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions Klasse | Microsoft docs"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Microsoft docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? -JavaScript-Debugger für Visual Studio-Code – Microsoft/vscode-js – Debuggen | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – Visual Studio-Code – Debugger für Microsoft Edge – Microsoft/vscode-Edge-debug2 | GitHub"  
