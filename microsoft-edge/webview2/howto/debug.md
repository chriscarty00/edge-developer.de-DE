---
description: Erfahren Sie, wie Sie WebView2-Steuerelemente Debuggen.
title: Debuggen von WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML
ms.openlocfilehash: 386bc237257be0ade8c48bc1c737b0151a882719
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659700"
---
# <span data-ttu-id="52bf5-104">Debuggen bei der Entwicklung mit WebView2-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="52bf5-104">How to Debug when developing with WebView2 controls</span></span>  

<span data-ttu-id="52bf5-105">Das Ziel des Microsoft Edge WebView2-Steuerelements ist die Kombination der besten Features der Web-und nativen Anwendungsentwicklung sowie der Entwicklertools.</span><span class="sxs-lookup"><span data-stu-id="52bf5-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="52bf5-106">In diesem Artikel werden die verschiedenen Tools erläutert, die bei der Entwicklung mit WebView2-Steuerelementen zu verwenden sind.</span><span class="sxs-lookup"><span data-stu-id="52bf5-106">This article outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="52bf5-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="52bf5-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="52bf5-108">Verwenden Sie die [Microsoft Edge (Chrom)-Entwickler Tools](/microsoft-edge/devtools-guide-chromium) zum Debuggen von Webinhalten, die in WebView2-Steuerelementen angezeigt werden, auf die gleiche Weise wie bei Verwendung von Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="52bf5-108">Use [Microsoft Edge (Chromium) Developer Tools](/microsoft-edge/devtools-guide-chromium) to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="52bf5-109">Um das devtools zu öffnen, setzen Sie den Fokus auf das WebView-Fenster, und verwenden Sie dann eine der folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="52bf5-109">To open the DevTools, set focus on the WebView window and then use any of the following options.</span></span>  
*   <span data-ttu-id="52bf5-110">Wählen Sie aus `F12` .</span><span class="sxs-lookup"><span data-stu-id="52bf5-110">Select `F12`.</span></span>  
*   <span data-ttu-id="52bf5-111">Wählen Sie aus `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="52bf5-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="52bf5-112">Öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \) > auswählen `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="52bf5-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   <span data-ttu-id="52bf5-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="52bf5-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="52bf5-115">Wenn Sie die Anwendung in Visual Studio debuggen, wobei der systemeigene Debugger angefügt ist, `F12` kann die Auswahl den systemeigenen Debugger anstelle der Entwickler Tools auslösen.</span><span class="sxs-lookup"><span data-stu-id="52bf5-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="52bf5-116">Verwenden Sie `Ctrl` + `Shift` + `I` das Kontextmenü, oder klicken Sie mit der rechten Maustaste auf \), um diese Situation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="52bf5-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid this situation.</span></span>  

## <span data-ttu-id="52bf5-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52bf5-117">Visual Studio</span></span>  

<span data-ttu-id="52bf5-118">Verwenden Sie den Skriptdebugger in Visual Studio 2019, Version 16,4 Preview 2 oder höher, um Ihr Skript in Visual Studio zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="52bf5-118">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="52bf5-119">Überprüfen Sie, ob die Komponente **JavaScript-Diagnose** in der **Desktop Entwicklung mit C++** -Arbeitsauslastung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="52bf5-119">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Visual Studio-JavaScript-Diagnose":::
   <span data-ttu-id="52bf5-121">Visual Studio-JavaScript-Diagnose</span><span class="sxs-lookup"><span data-stu-id="52bf5-121">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="52bf5-122">Zum Aktivieren des WebView2-Skript Debuggens öffnen Sie das Kontextmenü \ (mit der rechten Maustaste auf \) in Ihrem Projekt, > **Eigenschaften**auswählen.</span><span class="sxs-lookup"><span data-stu-id="52bf5-122">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  <span data-ttu-id="52bf5-123">Wählen Sie unter **Konfigurationseigenschaften**die Option **Debuggen**aus.</span><span class="sxs-lookup"><span data-stu-id="52bf5-123">On **Configuration Properties**, select **Debugging**.</span></span>  <span data-ttu-id="52bf5-124">Wählen Sie in der Eigenschaft **Debuggertyp** in der Liste der Optionen **JavaScript (WebView2)** aus.</span><span class="sxs-lookup"><span data-stu-id="52bf5-124">On the **Debugger Type** property, choose **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Visual Studio-JavaScript-Debugger":::
   <span data-ttu-id="52bf5-126">Visual Studio-JavaScript-Debugger</span><span class="sxs-lookup"><span data-stu-id="52bf5-126">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## <span data-ttu-id="52bf5-127">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="52bf5-127">Visual Studio Code</span></span>  

<span data-ttu-id="52bf5-128">Sie können Visual Studio-Code verwenden, um Skripts zu debuggen, die in WebView2-Steuerelementen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="52bf5-128">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="52bf5-129">Weitere Informationen finden Sie unter [Microsoft Edge (Chrom) WebView-Anwendungen](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span><span class="sxs-lookup"><span data-stu-id="52bf5-129">For more information, see [Microsoft Edge (Chromium) WebView Applications](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="52bf5-130">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="52bf5-130">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="52bf5-131">Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.</span><span class="sxs-lookup"><span data-stu-id="52bf5-131">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="52bf5-132">Besuchen Sie das [Feedback-Repo](https://aka.ms/webviewfeedback) , um Funktionsanforderungen oder Fehlerberichte einzureichen.</span><span class="sxs-lookup"><span data-stu-id="52bf5-132">Visit the [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  
