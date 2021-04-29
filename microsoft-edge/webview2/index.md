---
description: Hosten von Webinhalten in Ihren Win32-, .NET- und UWP-Apps mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, browser control, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Reunion
ms.openlocfilehash: ec22edbc838f57c2f9c591a0f48298d61dce484c
ms.sourcegitcommit: b51df5036642060525e03cd744b7d35726326abe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526073"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="66663-104">Einführung in Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="66663-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="66663-105">Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien \(HTML, CSS und JavaScript\) in Ihre systemeigenen Apps einbetten.</span><span class="sxs-lookup"><span data-stu-id="66663-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="66663-106">Das WebView2-Steuerelement verwendet [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] als Renderingmodul, um die Webinhalte in systemeigenen Apps anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="66663-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="66663-107">Mit WebView2 können Sie Webcode in verschiedene Teile Ihrer systemeigenen App einbetten.</span><span class="sxs-lookup"><span data-stu-id="66663-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="66663-108">Erstellen Sie alle systemeigenen Apps in einer einzelnen WebView-Instanz.</span><span class="sxs-lookup"><span data-stu-id="66663-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="66663-109">Informationen zum Erstellen einer WebView2-App finden Sie unter [Erste Schritte.](#getting-started)</span><span class="sxs-lookup"><span data-stu-id="66663-109">For information on how to start building a WebView2 app, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Was ist WebView?" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="66663-111">Was ist WebView?</span><span class="sxs-lookup"><span data-stu-id="66663-111">What is WebView?</span></span>  
:::image-end:::  

## <a name="hybrid-app-approach"></a><span data-ttu-id="66663-112">Hybrid-App-Ansatz</span><span class="sxs-lookup"><span data-stu-id="66663-112">Hybrid app approach</span></span>  

<span data-ttu-id="66663-113">Entwickler müssen häufig zwischen dem Erstellen einer Web-App oder einer nativen App entscheiden.</span><span class="sxs-lookup"><span data-stu-id="66663-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="66663-114">Die Entscheidung hängt vom Abhandeln zwischen Reichweite und Energie ab.</span><span class="sxs-lookup"><span data-stu-id="66663-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="66663-115">Web-Apps ermöglichen eine breite Reichweite.</span><span class="sxs-lookup"><span data-stu-id="66663-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="66663-116">Als Webentwickler können Sie den Großteil Ihres Codes auf verschiedenen Plattformen wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="66663-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="66663-117">Verwenden Sie eine systemeigene App, um auf alle Funktionen einer systemeigenen Plattform zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="66663-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web native" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="66663-119">Web native</span><span class="sxs-lookup"><span data-stu-id="66663-119">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="66663-120">Hybrid-Apps ermöglichen Entwicklern, das Beste aus beiden Welten zu genießen.</span><span class="sxs-lookup"><span data-stu-id="66663-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="66663-121">Entwickler von Hybrid-Apps profitieren von den folgenden Vorteilen.</span><span class="sxs-lookup"><span data-stu-id="66663-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="66663-122">Die Ubiquitie und Stärke der Webplattform.</span><span class="sxs-lookup"><span data-stu-id="66663-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="66663-123">Die Leistungsfähigkeit und die vollständigen Funktionen der systemeigenen Plattform.</span><span class="sxs-lookup"><span data-stu-id="66663-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="66663-124">WebView2-Vorteile</span><span class="sxs-lookup"><span data-stu-id="66663-124">WebView2 benefits</span></span>   

<!--  
:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webviewreasons.png":::
   WebView reasons  
:::image-end:::  
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **<span data-ttu-id="66663-125">Web ecosystem \& Skillset</span><span class="sxs-lookup"><span data-stu-id="66663-125">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="66663-126">Nutzen Sie die gesamte Webplattform, Bibliotheken, Tools und Talente, die innerhalb des Webökosystems vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="66663-126">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **<span data-ttu-id="66663-127">Schnelle Innovation</span><span class="sxs-lookup"><span data-stu-id="66663-127">Rapid innovation</span></span>**  
      <span data-ttu-id="66663-128">Die Webentwicklung ermöglicht eine schnellere Bereitstellung und Iteration.</span><span class="sxs-lookup"><span data-stu-id="66663-128">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **<span data-ttu-id="66663-129">Unterstützung für Windows 7, 8 und 10</span><span class="sxs-lookup"><span data-stu-id="66663-129">Windows 7, 8, and 10 support</span></span>**  
      <span data-ttu-id="66663-130">Unterstützung für eine konsistente Benutzeroberfläche in Windows 7, Windows 8 und Windows 10.</span><span class="sxs-lookup"><span data-stu-id="66663-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **<span data-ttu-id="66663-131">Systemeigene Funktionen</span><span class="sxs-lookup"><span data-stu-id="66663-131">Native capabilities</span></span>**  
      <span data-ttu-id="66663-132">Greifen Sie auf den vollständigen Satz systemeigener APIs zu.</span><span class="sxs-lookup"><span data-stu-id="66663-132">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **<span data-ttu-id="66663-133">Codefreigabe</span><span class="sxs-lookup"><span data-stu-id="66663-133">Code-sharing</span></span>**  
      <span data-ttu-id="66663-134">Das Hinzufügen von Webcode zu Ihrer Codebasis ermöglicht eine höhere Wiederverwendung auf mehreren Plattformen.</span><span class="sxs-lookup"><span data-stu-id="66663-134">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **<span data-ttu-id="66663-135">Microsoft-Support</span><span class="sxs-lookup"><span data-stu-id="66663-135">Microsoft support</span></span>**  
      <span data-ttu-id="66663-136">Microsoft bietet Unterstützung und fügt neue Featureanforderungen hinzu, wenn WebView2 unter Allgemeinverfügbarkeit \(GA\) veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="66663-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **<span data-ttu-id="66663-137">Immergrüne Verteilung</span><span class="sxs-lookup"><span data-stu-id="66663-137">Evergreen distribution</span></span>**  
      <span data-ttu-id="66663-138">Verlassen Sie sich auf eine aktuelle Version von Chromium mit regelmäßigen Plattformupdates und Sicherheitspatches.</span><span class="sxs-lookup"><span data-stu-id="66663-138">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **<span data-ttu-id="66663-139">Behoben</span><span class="sxs-lookup"><span data-stu-id="66663-139">Fixed</span></span>**  
      <span data-ttu-id="66663-140">\(in Kürze\) Wählen Sie aus, um die Chromium-Bits in Ihrer App zu packen.</span><span class="sxs-lookup"><span data-stu-id="66663-140">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **<span data-ttu-id="66663-141">Inkrementelle Einführung</span><span class="sxs-lookup"><span data-stu-id="66663-141">Incremental adoption</span></span>**  
      <span data-ttu-id="66663-142">Fügen Sie Ihrer App Stück für Stück Webkomponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="66663-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="getting-started"></a><span data-ttu-id="66663-143">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="66663-143">Getting started</span></span>  

<span data-ttu-id="66663-144">Zum Erstellen und Testen Ihrer App mithilfe des WebView2-Steuerelements benötigen Sie</span><span class="sxs-lookup"><span data-stu-id="66663-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="66663-145">das [installierte WebView2 SDK.][NugetPackagesMicrosoftWebWebView2]</span><span class="sxs-lookup"><span data-stu-id="66663-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="66663-146">Wählen Sie eine der folgenden Optionen für die ersten Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="66663-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="66663-147">Erste Schritte mit Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="66663-147">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="66663-148">Erste Schritte mit WPF</span><span class="sxs-lookup"><span data-stu-id="66663-148">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="66663-149">Erste Schritte mit WinForms</span><span class="sxs-lookup"><span data-stu-id="66663-149">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="66663-150">Erste Schritte mit WinUI3</span><span class="sxs-lookup"><span data-stu-id="66663-150">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="66663-151">Das [WebView2 Samples-Repository][GithubMicrosoftedgeWebview2samples] enthält Beispiele, die alle WebView2 SDK-Features und API-Verwendungsmuster veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="66663-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="66663-152">Wenn dem WebView2 SDK weitere Features hinzugefügt werden, werden die Beispiel-Apps aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="66663-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="66663-153">Unterstützte Plattformen</span><span class="sxs-lookup"><span data-stu-id="66663-153">Supported platforms</span></span>  

<span data-ttu-id="66663-154">Eine Allgemeine Verfügbarkeit \(GA\) oder Vorschauversion ist in den folgenden Programmierumgebungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66663-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="66663-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="66663-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="66663-156">.NET Framework 4.5 oder höher</span><span class="sxs-lookup"><span data-stu-id="66663-156">.NET Framework 4.5 or later</span></span>  
*   <span data-ttu-id="66663-157">.NET Core 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="66663-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="66663-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="66663-158">.NET 5</span></span>  
*   <span data-ttu-id="66663-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="66663-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="66663-160">Sie können WebView2-Apps unter den folgenden Versionen von Windows ausführen.</span><span class="sxs-lookup"><span data-stu-id="66663-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="66663-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="66663-161">Windows 10</span></span>  
*   <span data-ttu-id="66663-162">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="66663-162">Windows 8.1</span></span>  
*   <span data-ttu-id="66663-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="66663-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="66663-164">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="66663-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="66663-165">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="66663-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="66663-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66663-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="66663-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="66663-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="66663-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="66663-168">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="66663-169">\*\* WebView2-Unterstützung für Windows 7 und Windows Server 2008 R2 hat den gleichen Supportzyklus wie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="66663-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="66663-170">Weitere Informationen finden Sie unter [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span><span class="sxs-lookup"><span data-stu-id="66663-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="66663-171">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="66663-171">Next steps</span></span>  

<span data-ttu-id="66663-172">Weitere Informationen zum Erstellen und Bereitstellen von WebView2-Apps finden Sie in der konzeptionellen Dokumentation und anleitungen.</span><span class="sxs-lookup"><span data-stu-id="66663-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

#### <a name="concepts"></a><span data-ttu-id="66663-173">Konzepte</span><span class="sxs-lookup"><span data-stu-id="66663-173">Concepts</span></span>  

*   [<span data-ttu-id="66663-174">Verstehen von WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="66663-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="66663-175">Verteilung von Apps mit WebView2</span><span class="sxs-lookup"><span data-stu-id="66663-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="66663-176">Bewährte Methoden für die Entwicklung sicherer WebView2-Apps</span><span class="sxs-lookup"><span data-stu-id="66663-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="66663-177">Verwalten des Benutzerdatenordners in WebView2-Apps</span><span class="sxs-lookup"><span data-stu-id="66663-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserdatafolder]  
 
#### <a name="how-to-guides"></a><span data-ttu-id="66663-178">How-To Anleitungen</span><span class="sxs-lookup"><span data-stu-id="66663-178">How-To guides</span></span>  

*   [<span data-ttu-id="66663-179">Debuggen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="66663-179">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="66663-180">Automatisieren und Testen von WebView2 mit Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="66663-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="66663-181">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="66663-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Apps mithilfe von WebView2-| Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-Apps | Microsoft Docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Verwalten des Benutzerdatenordners | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Verstehen der WebView2 SDK-| Microsoft Docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Erste Schritte mit WebView2 | Microsoft Docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps (Vorschau) | Microsoft Docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Erste Schritte mit WebView2 in WinUI3 (Vorschau) | Microsoft Docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft Docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Debuggen mit WebView2-| Microsoft Docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft Docs"  
[Webview2Releasenotes]: ./releasenotes.md "Versionshinweise für WebView2 SDK | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (July 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge unterstützte Betriebssysteme | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele – MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback – MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Insider herunterladen"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Gallery"  
