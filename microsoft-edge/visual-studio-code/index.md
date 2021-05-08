---
description: Microsoft Edge (Chromium) und Visual Studio Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs code, visual studio code, debugger, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230691"
---
# <span data-ttu-id="5070d-104">Visual Studio Code – Übersicht</span><span class="sxs-lookup"><span data-stu-id="5070d-104">Visual Studio Code overview</span></span>  

<span data-ttu-id="5070d-105">[Visual Studio Code][VisualStudioCodeDocs] ist ein einfacher, aber leistungsstarker Quellcode-Editor.</span><span class="sxs-lookup"><span data-stu-id="5070d-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="5070d-106">[Visual Studio Code][VisualStudioCodeDocs] ist für Windows, Linux und macOS verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5070d-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="5070d-107">Es umfasst integrierte Unterstützung für JavaScript, TypeScript und Node.js, daher ist es ein großartiges Tool für Webentwickler, bevor Sie es anpassen.</span><span class="sxs-lookup"><span data-stu-id="5070d-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="5070d-108">Wenn Sie es noch nicht verwenden, laden Sie [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="5070d-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="5070d-109">Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="5070d-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="5070d-110">Um eine der unten hervorgehobenen Erweiterungen zu erwerben, navigieren Sie zu Erweiterungen \(wählen Sie `Ctrl` + `Shift` + `X` unter Windows/Linux oder `Command` + `Shift` + `X` unter macOS\) in Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="5070d-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="5070d-111">Suchen Sie im Marketplace nach der spezifischen Erweiterung, und wählen Sie **Installieren aus.**</span><span class="sxs-lookup"><span data-stu-id="5070d-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Installieren des Debuggers für Microsoft Edge Visual Studio Code Erweiterung" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="5070d-113">Installieren des **Debuggers für Microsoft Edge** Visual Studio Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5070d-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Debugger für Microsoft Edge Visual Studio Code Erweiterung" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="5070d-115">**Debugger für Microsoft Edge** Visual Studio Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5070d-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="5070d-116">Debugger für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5070d-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Tools für Visual Studio Code Visual Studio Code Erweiterung" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="5070d-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="5070d-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="5070d-119">Microsoft Edge Tools für Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="5070d-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="webhint Visual Studio Code Erweiterung" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="5070d-121">**webhint** Visual Studio Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5070d-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="5070d-122">Webhint</span><span class="sxs-lookup"><span data-stu-id="5070d-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="5070d-123">Debugger für Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5070d-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="5070d-124">Debugger for [Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debuggen Sie Ihren Front-End-JavaScript-Code Zeile für Zeile, und sehen Sie anweisungen direkt aus `console.log()` [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="5070d-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="5070d-125">Mithilfe des Debuggertools können Sie sowohl Microsoft Edge \(EdgeHTML\) als auch Microsoft Edge \(Chromium\) starten oder anfügen.</span><span class="sxs-lookup"><span data-stu-id="5070d-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="5070d-126">Eine exemplarische Vorgehensweise zum Debuggen Microsoft Edge von Visual Studio Code und Beispielkonfigurationen finden Sie unter `launch.json` [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span><span class="sxs-lookup"><span data-stu-id="5070d-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="5070d-127">Wählen Sie die folgende Abbildung aus, um die Erweiterung in Aktion zu sehen.</span><span class="sxs-lookup"><span data-stu-id="5070d-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Debugger für Edge-Visual Studio Code in Aktion" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="5070d-129">**Debugger für Microsoft Edge** Visual Studio Code erweiterung in Aktion</span><span class="sxs-lookup"><span data-stu-id="5070d-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="5070d-130">Microsoft Edge Tools für Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="5070d-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="5070d-131">Verwenden Sie [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code das **Element-Tool** des Microsoft Edge in Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="5070d-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="5070d-132">Verwenden Sie es für die folgenden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="5070d-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="5070d-133">Fügen Sie eine Instanz an, oder starten Sie eine Instanz Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5070d-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="5070d-134">Zeigt die Laufzeit-HTML-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="5070d-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="5070d-135">Aktualisieren Sie das Layout.</span><span class="sxs-lookup"><span data-stu-id="5070d-135">Update the layout.</span></span>  
*   <span data-ttu-id="5070d-136">Behebung von Formatierungsproblemen.</span><span class="sxs-lookup"><span data-stu-id="5070d-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="5070d-137">Weitere Informationen finden Sie unter [Microsoft Edge Tools for Visual Studio Code Visual Studio Code Extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span><span class="sxs-lookup"><span data-stu-id="5070d-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Tools für Visual Studio Code Visual Studio Code erweiterung in Aktion" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="5070d-139">**Microsoft Edge tools for Visual Studio Code** Visual Studio Code extension in action</span><span class="sxs-lookup"><span data-stu-id="5070d-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="5070d-140">Webhint</span><span class="sxs-lookup"><span data-stu-id="5070d-140">webhint</span></span>  
      
<span data-ttu-id="5070d-141">Verwenden [Sie webhint][WebhintMain], ein anpassbares Lintingtool, um die folgenden Funktionen Ihrer Website zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="5070d-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="5070d-142">Barrierefreiheit</span><span class="sxs-lookup"><span data-stu-id="5070d-142">Accessibility</span></span>
*   <span data-ttu-id="5070d-143">Leistung</span><span class="sxs-lookup"><span data-stu-id="5070d-143">Performance</span></span>
*   <span data-ttu-id="5070d-144">Browserübergreifende Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="5070d-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="5070d-145">PWA Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="5070d-145">PWA compatibility</span></span>
*   <span data-ttu-id="5070d-146">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="5070d-146">Security</span></span>

<span data-ttu-id="5070d-147">Der Code wird auf Codierungsmethoden und häufige Fehler überprüft.</span><span class="sxs-lookup"><span data-stu-id="5070d-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="5070d-148">Das webhint-Open-Source-Projekt, das ursprünglich vom Microsoft Edge-Team entwickelt wurde, ist jetzt Teil der [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="5070d-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="5070d-149">Das Microsoft Edge-Team arbeitet weiterhin zusammen mit Webentwicklern in der Community am Webhint mit.</span><span class="sxs-lookup"><span data-stu-id="5070d-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Screenshot der Webhint-Visual Studio Code-Erweiterung" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="5070d-151">Screenshot der **Webhint-Visual Studio Code-Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="5070d-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="5070d-152">Identifizieren und beheben Sie Probleme auf Ihrer Website, indem Sie die [Webhint-Erweiterung für Visual Studio Code.][VisualstudioMarketplaceWebhint]</span><span class="sxs-lookup"><span data-stu-id="5070d-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="5070d-153">Hinweise untersuchen HTML, CSS, JavaScript, TypeScript und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="5070d-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="5070d-154">Hinweise werden als Inline unterstreicht angezeigt und im Bereich **Probleme zusammengefasst.**</span><span class="sxs-lookup"><span data-stu-id="5070d-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="5070d-155">Weitere Informationen finden Sie unter [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="5070d-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Debugger Für Microsoft Edge Visual Studio Code Erweiterung | Microsoft Docs"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools für Visual Studio Code Erweiterung | Microsoft Docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio Code Extension | Microsoft Docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Dokumentation | Visual Studio Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
