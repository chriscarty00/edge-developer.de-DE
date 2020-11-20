---
description: Hosten von Webinhalten in ihren Win32-, .net-UWP-Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML, Windows Forms, WinForms, WPF, .net, WinUI, Projekt-Wiedervereinigung
ms.openlocfilehash: 9e5cc3a26f07a11c9fd5c21d62ecafc3ed5103f4
ms.sourcegitcommit: c619168deea44cdec8ebc80ef9ddf1d91d5f726d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "11182183"
---
# <span data-ttu-id="d1157-104">Einführung in Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="d1157-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="d1157-105">Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien (HTML, CSS und JavaScript \) in ihre systemeigenen Anwendungen einbetten.</span><span class="sxs-lookup"><span data-stu-id="d1157-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="d1157-106">Das WebView2-Steuerelement verwendet [Microsoft Edge (Chrom)][MicrosoftedgeinsiderMain] als Rendering-Modul, um die Webinhalte in systemeigenen Anwendungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d1157-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="d1157-107">Mit WebView2 können Sie Webcode in verschiedenen Teilen der systemeigenen Anwendung einbetten oder die gesamte systemeigene Anwendung in einem einzigen WebView-Webpart erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1157-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="d1157-108">Informationen dazu, wie Sie mit dem Erstellen einer WebView2-Anwendung beginnen, finden [Sie unter Erste Schritte](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="d1157-108">For information on how to start building a WebView2 application, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Was ist WebView" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="d1157-110">Was ist WebView</span><span class="sxs-lookup"><span data-stu-id="d1157-110">What is WebView</span></span>  
:::image-end:::  

## <span data-ttu-id="d1157-111">Ansatz der Hybrid Anwendung</span><span class="sxs-lookup"><span data-stu-id="d1157-111">Hybrid application approach</span></span>  

<span data-ttu-id="d1157-112">Entwickler müssen sich häufig zwischen dem Erstellen einer Webanwendung oder einer systemeigenen Anwendung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="d1157-112">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="d1157-113">Die Entscheidung hängt vom Kompromiss zwischen Reichweite und macht ab.</span><span class="sxs-lookup"><span data-stu-id="d1157-113">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="d1157-114">Web-Anwendungen ermöglichen eine breite Reichweite.</span><span class="sxs-lookup"><span data-stu-id="d1157-114">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="d1157-115">Als Web-Entwickler können Sie die meisten, wenn nicht alle Ihren Code, auf allen verschiedenen Plattformen wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1157-115">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="d1157-116">Systemeigene Anwendungen nutzen jedoch die Funktionen der gesamten systemeigenen Plattform.</span><span class="sxs-lookup"><span data-stu-id="d1157-116">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="d1157-118">Web Native</span><span class="sxs-lookup"><span data-stu-id="d1157-118">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="d1157-119">Hybrid Anwendungen ermöglichen Entwicklern, das Beste aus beiden Welten zu genießen.</span><span class="sxs-lookup"><span data-stu-id="d1157-119">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="d1157-120">Entwickler von Hybrid Anwendungen profitieren von der Allgegenwart und Stärke der Web-Plattform sowie von der Leistungsfähigkeit und den vollständigen Funktionen der systemeigenen Plattform.</span><span class="sxs-lookup"><span data-stu-id="d1157-120">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="d1157-121">WebView2-Vorteile</span><span class="sxs-lookup"><span data-stu-id="d1157-121">WebView2 benefits</span></span>  

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView-Gründe" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="d1157-123">WebView-Gründe</span><span class="sxs-lookup"><span data-stu-id="d1157-123">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="d1157-124">Web-Ökosystem \ & skillset</span><span class="sxs-lookup"><span data-stu-id="d1157-124">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="d1157-125">Verwenden Sie die gesamte Web-Plattform, Bibliotheken, Tools und Talente, die im Web-Ökosystem vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d1157-125">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d1157-126">Schnelle Innovation</span><span class="sxs-lookup"><span data-stu-id="d1157-126">Rapid innovation</span></span>**  
      <span data-ttu-id="d1157-127">Web-Entwicklung ermöglicht schnellere Bereitstellung und Iteration.</span><span class="sxs-lookup"><span data-stu-id="d1157-127">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d1157-128">Windows 7, 8, 10 Support</span><span class="sxs-lookup"><span data-stu-id="d1157-128">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="d1157-129">Unterstützung für eine konsistente Benutzeroberfläche in Windows 7, 8 und 10.</span><span class="sxs-lookup"><span data-stu-id="d1157-129">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d1157-130">Systemeigene Funktionen</span><span class="sxs-lookup"><span data-stu-id="d1157-130">Native capabilities</span></span>**  
      <span data-ttu-id="d1157-131">Greifen Sie auf den vollständigen Satz nativer APIs zu.</span><span class="sxs-lookup"><span data-stu-id="d1157-131">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d1157-132">Code Freigabe</span><span class="sxs-lookup"><span data-stu-id="d1157-132">Code-sharing</span></span>**  
      <span data-ttu-id="d1157-133">Durch Hinzufügen von Webcode zu ihrer CodeBase können Sie die Wiederverwendung auf mehreren Plattformen erhöhen.</span><span class="sxs-lookup"><span data-stu-id="d1157-133">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d1157-134">Microsoft-Support</span><span class="sxs-lookup"><span data-stu-id="d1157-134">Microsoft support</span></span>**  
      <span data-ttu-id="d1157-135">Microsoft bietet Support und fügt neue Funktionsanforderungen hinzu, wenn WebView2 als "ga" veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="d1157-135">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d1157-136">Immergrüne Verteilung</span><span class="sxs-lookup"><span data-stu-id="d1157-136">Evergreen distribution</span></span>**  
      <span data-ttu-id="d1157-137">Verlassen Sie sich auf eine aktuelle Version von Chromium mit regulären Plattformupdates und Sicherheitspatches.</span><span class="sxs-lookup"><span data-stu-id="d1157-137">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="d1157-138">**Behoben** \ (in Kürze verfügbar)</span><span class="sxs-lookup"><span data-stu-id="d1157-138">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="d1157-139">Wählen Sie aus, um die Chrom Bits in Ihrer Anwendung zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="d1157-139">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d1157-140">Inkrementelle Einführung</span><span class="sxs-lookup"><span data-stu-id="d1157-140">Incremental adoption</span></span>**  
      <span data-ttu-id="d1157-141">Fügen Sie Ihrer Anwendung Stück für Stück Webkomponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="d1157-141">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="d1157-142">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="d1157-142">Getting started</span></span>  

<span data-ttu-id="d1157-143">Wenn Sie Ihre Anwendung mithilfe des WebView2-Steuerelements erstellen und testen möchten, müssen Sie sowohl [Microsoft Edge (Chrom)][MicrosoftedgeinsiderDownload] als auch das [WebView2-SDK][NugetPackagesMicrosoftWebWebView2] installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d1157-143">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="d1157-144">Wählen Sie eine der folgenden Optionen aus, um loszulegen.</span><span class="sxs-lookup"><span data-stu-id="d1157-144">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="d1157-145">Erste Schritte mit Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="d1157-145">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="d1157-146">Erste Schritte mit WPF</span><span class="sxs-lookup"><span data-stu-id="d1157-146">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="d1157-147">Erste Schritte mit WinForms</span><span class="sxs-lookup"><span data-stu-id="d1157-147">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="d1157-148">Erste Schritte mit WinUI3</span><span class="sxs-lookup"><span data-stu-id="d1157-148">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="d1157-149">Das [WebView2-Beispiel][GithubMicrosoftedgeWebview2samples] -Repository enthält Beispiele, die alle WebView2-SDK-Features und API-Verwendungsmuster veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="d1157-149">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="d1157-150">Wenn dem WebView2-SDK weitere Features hinzugefügt werden, werden die Beispielanwendungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d1157-150">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="d1157-151">Unterstützte Plattformen</span><span class="sxs-lookup"><span data-stu-id="d1157-151">Supported platforms</span></span>  

<span data-ttu-id="d1157-152">Eine allgemeine Verfügbarkeit \ (GA \) oder Preview-Version steht in den folgenden Programmierumgebungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d1157-152">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="d1157-153">Win32 C/C++ \ (GA \)</span><span class="sxs-lookup"><span data-stu-id="d1157-153">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="d1157-154">.NET Framework 4.6.2 oder höher \ (Vorschau \)</span><span class="sxs-lookup"><span data-stu-id="d1157-154">.NET Framework 4.6.2 or later \(Preview\)</span></span>  
*   <span data-ttu-id="d1157-155">.Net Core 3,0 oder höher \ (Vorschau \)</span><span class="sxs-lookup"><span data-stu-id="d1157-155">.NET Core 3.0 or later \(Preview\)</span></span>  
*   <span data-ttu-id="d1157-156">[WinUI 3,0][UwpToolkitsWinui3] \ (Vorschau \)</span><span class="sxs-lookup"><span data-stu-id="d1157-156">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="d1157-157">Sie können WebView2-Anwendungen unter den folgenden Windows-Versionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1157-157">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="d1157-158">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d1157-158">Windows 10</span></span>  
*   <span data-ttu-id="d1157-159">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="d1157-159">Windows 8.1</span></span>  
*   <span data-ttu-id="d1157-160">Windows 7 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="d1157-160">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="d1157-161">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="d1157-161">Windows Server 2019</span></span>  
*   <span data-ttu-id="d1157-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d1157-162">Windows Server 2016</span></span>  
*   <span data-ttu-id="d1157-163">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1157-163">Windows Server 2012</span></span>  
*   <span data-ttu-id="d1157-164">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d1157-164">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="d1157-165">Windows Server 2008 R2 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="d1157-165">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d1157-166">\ \* \ \* WebView2-Unterstützung für Windows 7 und Windows Server 2008 R2 hat denselben Support Zyklus wie Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d1157-166">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="d1157-167">Weitere Informationen finden Sie [unter Unterstützte Microsoft Edge-Betriebssysteme][DeployedgeMicrosoftEdgeSupportedOS].</span><span class="sxs-lookup"><span data-stu-id="d1157-167">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <span data-ttu-id="d1157-168">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d1157-168">Next steps</span></span>  

<span data-ttu-id="d1157-169">Weitere Informationen zum Erstellen und Bereitstellen von WebView2-Anwendungen finden Sie in den konzeptionellen Dokumentationen und Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="d1157-169">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="d1157-170">Konzepte</span><span class="sxs-lookup"><span data-stu-id="d1157-170">Concepts</span></span>  

*   [<span data-ttu-id="d1157-171">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="d1157-171">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="d1157-172">Verteilung von Anwendungen mithilfe von WebView2</span><span class="sxs-lookup"><span data-stu-id="d1157-172">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="d1157-173">Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d1157-173">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="d1157-174">Verwalten von benutzerdatenordnern in WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d1157-174">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="d1157-175">How-To Führungslinien</span><span class="sxs-lookup"><span data-stu-id="d1157-175">How-To guides</span></span>  

*   [<span data-ttu-id="d1157-176">Debuggen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="d1157-176">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="d1157-177">Automatisieren und Testen von WebView2 mit Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="d1157-177">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="d1157-178">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="d1157-178">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen | Microsoft docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Verwalten des Benutzerdatenordners | Microsoft docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu WebView2 SDK-Versionen | Microsoft docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Erste Schritte mit WebView2 | Microsoft docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps (Preview) | Microsoft docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Erste Schritte mit WebView2 in WinUI3 (Preview) | Microsoft docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Debuggen mit WebView2 | Microsoft docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft docs"  
[Webview2Releasenotes]: ./releasenotes.md "Anmerkungen zu dieser Version von WebView2 SDK | Microsoft docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows-UI-Bibliothek 3 Preview 2 (Juli 2020) | Microsoft docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge-unterstützte Betriebssysteme | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Insider herunterladen"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | NuGet-Katalog"  
