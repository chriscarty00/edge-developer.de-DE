---
description: Hosten von Webinhalten in ihren Win32-, .net-UWP-Anwendungen mit dem Microsoft Edge WebView2-Steuerelement
title: Microsoft Edge-WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML, Windows Forms, WinForms, WPF, .net, WinUI, Projekt-Wiedervereinigung
ms.openlocfilehash: d3294ce72237a323113ed9f7c8f31e37af43f5e6
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013744"
---
# <span data-ttu-id="ad8a0-104">Einführung in Microsoft Edge WebView2 (Preview)</span><span class="sxs-lookup"><span data-stu-id="ad8a0-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="ad8a0-105">Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien (HTML, CSS und JavaScript \) in ihre systemeigenen Anwendungen einbetten.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="ad8a0-106">Das WebView2-Steuerelement verwendet [Microsoft Edge (Chrom)][MicrosoftedgeinsiderMain] als Rendering-Modul, um die Webinhalte in systemeigenen Anwendungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="ad8a0-107">Mit WebView2 können Sie Webcode in verschiedenen Teilen der systemeigenen Anwendung einbetten oder die gesamte systemeigene Anwendung in einem einzigen WebView-Webpart erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="ad8a0-108">Informationen zum Erstellen einer WebView2-Anwendung finden Sie unter [Erste Schritte](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="ad8a0-108">For information on how to start building a WebView2 application, see [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Was ist WebView" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="ad8a0-110">Was ist WebView</span><span class="sxs-lookup"><span data-stu-id="ad8a0-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ad8a0-111">Die WebView2 Preview ist für frühzeitiges Prototyping vorgesehen, um Feedback zu sammeln, um die API zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help shape the API.</span></span>  <span data-ttu-id="ad8a0-112">Sie sollten die Vorschau in ihren Produktions-apps nicht verwenden, da möglicherweise wichtige Änderungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-112">You should not use the preview in your production apps because there may be breaking changes.</span></span>  <span data-ttu-id="ad8a0-113">Weitere Informationen finden Sie unter [Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="ad8a0-113">For more information, see [Webview2Releasenotes].</span></span>  

## <span data-ttu-id="ad8a0-114">Ansatz der Hybrid Anwendung</span><span class="sxs-lookup"><span data-stu-id="ad8a0-114">Hybrid application approach</span></span>  

<span data-ttu-id="ad8a0-115">Entwickler müssen sich häufig zwischen dem Erstellen einer Webanwendung oder einer systemeigenen Anwendung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-115">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="ad8a0-116">Die Entscheidung hängt vom Kompromiss zwischen Reichweite und macht ab.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-116">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="ad8a0-117">Web-Anwendungen ermöglichen eine breite Reichweite.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-117">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="ad8a0-118">Als Web-Entwickler können Sie die meisten, wenn nicht alle Ihren Code, auf allen verschiedenen Plattformen wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-118">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="ad8a0-119">Systemeigene Anwendungen nutzen jedoch die Funktionen der gesamten systemeigenen Plattform.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-119">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="ad8a0-121">Web Native</span><span class="sxs-lookup"><span data-stu-id="ad8a0-121">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="ad8a0-122">Hybrid Anwendungen ermöglichen Entwicklern, das Beste aus beiden Welten zu genießen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-122">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="ad8a0-123">Entwickler von Hybrid Anwendungen profitieren von der Allgegenwart und Stärke der Web-Plattform sowie von der Leistungsfähigkeit und den vollständigen Funktionen der systemeigenen Plattform.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-123">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="ad8a0-124">WebView2-Vorteile</span><span class="sxs-lookup"><span data-stu-id="ad8a0-124">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView-Gründe" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="ad8a0-126">WebView-Gründe</span><span class="sxs-lookup"><span data-stu-id="ad8a0-126">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-127">Web-Ökosystem \ & skillset</span><span class="sxs-lookup"><span data-stu-id="ad8a0-127">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="ad8a0-128">Verwenden Sie die gesamte Web-Plattform, Bibliotheken, Tools und Talente, die im Web-Ökosystem vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-129">Schnelle Innovation</span><span class="sxs-lookup"><span data-stu-id="ad8a0-129">Rapid innovation</span></span>**  
      <span data-ttu-id="ad8a0-130">Web-Entwicklung ermöglicht schnellere Bereitstellung und Iteration.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-130">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-131">Windows 7, 8, 10 Support</span><span class="sxs-lookup"><span data-stu-id="ad8a0-131">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="ad8a0-132">Unterstützung für eine konsistente Benutzeroberfläche in Windows 7, 8 und 10.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-132">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-133">Systemeigene Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad8a0-133">Native capabilities</span></span>**  
      <span data-ttu-id="ad8a0-134">Greifen Sie auf den vollständigen Satz nativer APIs zu.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-135">Code Freigabe</span><span class="sxs-lookup"><span data-stu-id="ad8a0-135">Code-sharing</span></span>**  
      <span data-ttu-id="ad8a0-136">Durch Hinzufügen von Webcode zu ihrer CodeBase können Sie die Wiederverwendung auf mehreren Plattformen erhöhen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-136">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-137">Microsoft-Support</span><span class="sxs-lookup"><span data-stu-id="ad8a0-137">Microsoft support</span></span>**  
      <span data-ttu-id="ad8a0-138">Microsoft bietet Support und fügt neue Funktionsanforderungen hinzu, wenn WebView2 als "ga" veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-138">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-139">Immergrüne Verteilung</span><span class="sxs-lookup"><span data-stu-id="ad8a0-139">Evergreen distribution</span></span>**  
      <span data-ttu-id="ad8a0-140">Verlassen Sie sich auf eine aktuelle Version von Chromium mit regulären Plattformupdates und Sicherheitspatches.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="ad8a0-141">**Behoben** \ (in Kürze verfügbar)</span><span class="sxs-lookup"><span data-stu-id="ad8a0-141">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="ad8a0-142">Wählen Sie aus, um die Chrom Bits in Ihrer Anwendung zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-142">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="ad8a0-143">Inkrementelle Einführung</span><span class="sxs-lookup"><span data-stu-id="ad8a0-143">Incremental adoption</span></span>**  
      <span data-ttu-id="ad8a0-144">Fügen Sie Ihrer Anwendung Stück für Stück Webkomponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-144">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="ad8a0-145">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="ad8a0-145">Getting started</span></span>  

<span data-ttu-id="ad8a0-146">Wenn Sie Ihre Anwendung mithilfe des WebView2-Steuerelements erstellen und testen möchten, müssen Sie sowohl [Microsoft Edge (Chrom)][MicrosoftedgeinsiderDownload] als auch das [WebView2-SDK][NugetPackagesMicrosoftWebWebView2] installiert haben.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-146">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="ad8a0-147">Wählen Sie eine der folgenden Optionen aus, um loszulegen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-147">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="ad8a0-148">Erste Schritte mit Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="ad8a0-148">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="ad8a0-149">Erste Schritte mit WPF</span><span class="sxs-lookup"><span data-stu-id="ad8a0-149">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="ad8a0-150">Erste Schritte mit WinForms</span><span class="sxs-lookup"><span data-stu-id="ad8a0-150">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="ad8a0-151">Erste Schritte mit WinUI3</span><span class="sxs-lookup"><span data-stu-id="ad8a0-151">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="ad8a0-152">Das [WebView2-Beispiel][GithubMicrosoftedgeWebview2samples] -Repository enthält Beispiele, die alle WebView2-SDK-Features und API-Verwendungsmuster veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-152">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="ad8a0-153">Wenn dem WebView2-SDK weitere Features hinzugefügt werden, werden die Beispielanwendungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-153">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="ad8a0-154">Unterstützte Plattformen</span><span class="sxs-lookup"><span data-stu-id="ad8a0-154">Supported platforms</span></span>  

<span data-ttu-id="ad8a0-155">Eine Entwicklervorschau steht in den folgenden Programmierumgebungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-155">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="ad8a0-156">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="ad8a0-156">Win32 C/C++</span></span>  
*   <span data-ttu-id="ad8a0-157">.NET Framework 4.6.2 oder höher</span><span class="sxs-lookup"><span data-stu-id="ad8a0-157">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="ad8a0-158">.Net Core 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ad8a0-158">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="ad8a0-159">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="ad8a0-159">WinUI 3.0</span></span>][UwpToolkitsWinui3]  

<span data-ttu-id="ad8a0-160">Sie können WebView2-Anwendungen unter den folgenden Windows-Versionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-160">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="ad8a0-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ad8a0-161">Windows 10</span></span>  
*   <span data-ttu-id="ad8a0-162">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="ad8a0-162">Windows 8.1</span></span>  
*   <span data-ttu-id="ad8a0-163">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ad8a0-163">Windows 8</span></span>  
*   <span data-ttu-id="ad8a0-164">Windows7</span><span class="sxs-lookup"><span data-stu-id="ad8a0-164">Windows 7</span></span>  
*   <span data-ttu-id="ad8a0-165">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="ad8a0-165">Windows Server 2019</span></span>  
*   <span data-ttu-id="ad8a0-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ad8a0-166">Windows Server 2016</span></span>  
*   <span data-ttu-id="ad8a0-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad8a0-167">Windows Server 2012</span></span>  
*   <span data-ttu-id="ad8a0-168">Windows Server-2012R2</span><span class="sxs-lookup"><span data-stu-id="ad8a0-168">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="ad8a0-169">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad8a0-169">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="ad8a0-170">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ad8a0-170">Next steps</span></span>  

<span data-ttu-id="ad8a0-171">Weitere Informationen zum Erstellen und Bereitstellen von WebView2-Anwendungen finden Sie in den konzeptionellen Dokumentationen und Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-171">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="ad8a0-172">Konzepte</span><span class="sxs-lookup"><span data-stu-id="ad8a0-172">Concepts</span></span>  

*   [<span data-ttu-id="ad8a0-173">Grundlegendes zu WebView2 SDK-Versionen</span><span class="sxs-lookup"><span data-stu-id="ad8a0-173">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="ad8a0-174">Verteilung von Anwendungen mithilfe von WebView2</span><span class="sxs-lookup"><span data-stu-id="ad8a0-174">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="ad8a0-175">Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ad8a0-175">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="ad8a0-176">Verwalten von benutzerdatenordnern in WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ad8a0-176">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="ad8a0-177">Anleitungen</span><span class="sxs-lookup"><span data-stu-id="ad8a0-177">How-To guides</span></span>  

*   [<span data-ttu-id="ad8a0-178">Debuggen mit WebView2</span><span class="sxs-lookup"><span data-stu-id="ad8a0-178">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="ad8a0-179">Automatisieren und Testen von WebView2 mit Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="ad8a0-179">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="ad8a0-180">Kontakt mit dem Microsoft Edge WebView-Team</span><span class="sxs-lookup"><span data-stu-id="ad8a0-180">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

> [!NOTE]
> <span data-ttu-id="ad8a0-181">Während der Vorschau unterstützt die gesammelten Daten das Erstellen eines besseren Produkts.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-181">During the preview, the collected data helps build a better product.</span></span>  <span data-ttu-id="ad8a0-182">Wenn Sie die WebView2-Datensammlung deaktivieren möchten, wechseln Sie zu `edge://settings/privacy` und deaktivieren Sie die Browserdaten Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ad8a0-182">To turn off WebView2 data collection, go to `edge://settings/privacy` and turn off browser data collection.</span></span>  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Verteilung von Anwendungen mit WebView2 | Microsoft docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-Anwendungen | Microsoft docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Verwalten des Benutzerdatenordners | Microsoft docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Grundlegendes zu WebView2 SDK-Versionen | Microsoft docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Erste Schritte mit WebView2 (Developer Preview) | Microsoft docs"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms-Apps (Preview) | Microsoft docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Erste Schritte mit WebView2 in WinUI3 (Preview) | Microsoft docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF (Preview) | Microsoft docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Debuggen mit WebView2 | Microsoft docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatisieren und Testen von WebView2 mit Microsoft Edge Driver | Microsoft docs"  
[Webview2Releasenotes]: ./releasenotes.md "Anmerkungen zu dieser Version von Webview2Releasenotes für WebView2 SDK | Microsoft docs"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Windows-UI-Bibliothek 3 Preview 2 (Juli 2020) | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2-Beispiele-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView-Feedback-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge-Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Insider herunterladen"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | NuGet-Katalog"  
