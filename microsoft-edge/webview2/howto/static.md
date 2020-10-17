---
description: Hier erfahren Sie, wie Sie die WebView2-Loader-Bibliothek statisch verknüpfen.
title: So verknüpfen Sie die WebView2-Ladeprogramm Bibliothek statisch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 880e9ed809dc268ee0b30b6ee3b5996711f54300
ms.sourcegitcommit: 0ded671914aae231493f418dd7645a04361dca1b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120124"
---
# <span data-ttu-id="6aef2-104">Statische Verknüpfung der WebView2-Loader-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6aef2-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="6aef2-105">Möglicherweise möchten Sie Ihre Anwendung mit einer einzelnen ausführbaren Datei anstelle eines Pakets von vielen Dateien verteilen.</span><span class="sxs-lookup"><span data-stu-id="6aef2-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="6aef2-106">Wenn Sie eine einzelne ausführbare Datei erstellen oder die Größe Ihres Pakets verkleinern möchten, sollten Sie die WebView2Loader-Dateien statisch verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6aef2-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="6aef2-107">Das WebView2-SDK enthält eine Headerdatei `WebView2Loader.dll` und die `IDL` Datei.</span><span class="sxs-lookup"><span data-stu-id="6aef2-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="6aef2-108">ist eine kleine Komponente, die apps dabei hilft, die WebView2-Runtime oder nicht-stable-Kanäle von Microsoft Edge auf dem Gerät zu finden.</span><span class="sxs-lookup"><span data-stu-id="6aef2-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="6aef2-109">Führen Sie die folgenden Schritte aus, wenn Sie keine apps senden möchten `WebView2Loader.dll` .</span><span class="sxs-lookup"><span data-stu-id="6aef2-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="6aef2-110">Öffnen `.vcxproj` Sie die Projektdatei für Ihre APP in einem Text-Editor wie Visual Studio-Code.</span><span class="sxs-lookup"><span data-stu-id="6aef2-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6aef2-111">Die `.vcproj` Projektdatei kann eine versteckte Datei sein, was bedeutet, dass Sie in Visual Studio nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6aef2-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="6aef2-112">Verwenden Sie die Befehlszeile, um ausgeblendete Dateien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6aef2-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="6aef2-113">Suchen Sie den Abschnitt im Code, in den Sie die WebView2 NuGet-Paket Zieldateien einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="6aef2-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="6aef2-114">Die Position im Code ist in der folgenden Abbildung hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="6aef2-114">The location in the code is highlighted in the following figure.</span></span>  

    :::image type="complex" source="./media/inserthere.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/inserthere.png":::
       <span data-ttu-id="6aef2-116">Codeausschnitt für Projektdateien</span><span class="sxs-lookup"><span data-stu-id="6aef2-116">Project Files code snippet</span></span>   
    :::image-end:::  
  
1.  <span data-ttu-id="6aef2-117">Kopieren Sie den folgenden Codeausschnitt, und fügen Sie ihn dort ein, wo er `Microsoft.Web.WebView2.targets` enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6aef2-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/staticlib.png":::
       <span data-ttu-id="6aef2-119">Eingefügter Codeausschnitt</span><span class="sxs-lookup"><span data-stu-id="6aef2-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6aef2-120">Bearbeiten Sie die zusätzlichen Abhängigkeiten der Buildkonfiguration für Ihre APP.</span><span class="sxs-lookup"><span data-stu-id="6aef2-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="6aef2-121">Suchen Sie zunächst alle `<AdditionalDependencies>` Kategorien.</span><span class="sxs-lookup"><span data-stu-id="6aef2-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="6aef2-122">Fügen Sie für jede `version.lib` eine weitere Abhängigkeit zu jeder anderen Buildkonfiguration in der Datei hinzu `.vcxproj` .</span><span class="sxs-lookup"><span data-stu-id="6aef2-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Codeausschnitt für Projektdateien" lightbox="./media/versionlib.png":::
       <span data-ttu-id="6aef2-124">Hinzufügen `version.lib` zu</span><span class="sxs-lookup"><span data-stu-id="6aef2-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6aef2-125">Das WebView2-Team zielt darauf ab, das Hinzufügen der zusätzlichen Abhängigkeit in zukünftigen Versionen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="6aef2-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1. <span data-ttu-id="6aef2-126">Kompilieren Sie Ihre APP, und führen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="6aef2-126">Compile and run your app.</span></span>

### <span data-ttu-id="6aef2-127">Kontakt mit dem WebView2-Team</span><span class="sxs-lookup"><span data-stu-id="6aef2-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <span data-ttu-id="6aef2-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6aef2-128">See also</span></span>  

*   <span data-ttu-id="6aef2-129">Um mit der Verwendung von WebView2 zu beginnen, navigieren Sie zu [WebView2 Anleitungen für erste Schritte][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="6aef2-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="6aef2-130">Ein umfassendes Beispiel für WebView2-Funktionen finden Sie unter [WebView2Samples][GithubMicrosoftedgeWebview2samples] auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="6aef2-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="6aef2-131">Ausführlichere Informationen zu WebView2-APIs finden Sie unter [API-Referenz][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="6aef2-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="6aef2-132">Wenn Sie weitere Informationen zu WebView2 möchten, navigieren Sie zu [WebView2-Ressourcen][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="6aef2-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2-API-Referenz | Microsoft docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Nächste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Erste Schritte – Einführung in Microsoft Edge WebView2 (Preview) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Was ist neu? -JavaScript-Debugger für Visual Studio-Code – Microsoft/vscode-js – Debuggen | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chrom) WebView-Anwendungen – Visual Studio-Code – Debugger für Microsoft Edge – Microsoft/vscode-Edge-debug2 | GitHub"  
