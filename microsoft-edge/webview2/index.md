---
description: Hosten von Webinhalten in ihrer Win32-App mit dem Steuerelement "Microsoft Edge WebView 2"
title: Microsoft Edge-WebView2-Steuerelement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Win32-apps, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, Browser-Steuerelement, Edge-HTML, Windows Forms, WinForms, WPF, .net
ms.openlocfilehash: 4f28ef64bb2936bc6c9a089ea2574070738fc79d
ms.sourcegitcommit: 8f5c9255dadc2a9bb22c3201d15b57d84851fe64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "10671638"
---
# <span data-ttu-id="96eb5-104">Einführung in Microsoft Edge WebView2 (Preview)</span><span class="sxs-lookup"><span data-stu-id="96eb5-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="96eb5-105">Mit dem Microsoft Edge WebView2-Steuerelement können Sie Webtechnologien (HTML, CSS und JavaScript \) in ihre systemeigenen Anwendungen einbetten.</span><span class="sxs-lookup"><span data-stu-id="96eb5-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="96eb5-106">Das WebView2-Steuerelement verwendet [Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com) als Rendering-Modul, um die Webinhalte in systemeigenen Anwendungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-106">The WebView2 control uses [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com) as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="96eb5-107">Mit WebView2 können Sie Webcode in verschiedenen Teilen der systemeigenen Anwendung einbetten oder die gesamte systemeigene Anwendung in einem einzigen WebView-Webpart erstellen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="96eb5-108">Informationen zum Erstellen einer WebView2-Anwendung finden Sie unter [Erste Schritte](./index.md#getting-started).</span><span class="sxs-lookup"><span data-stu-id="96eb5-108">For information on how to start building a WebView2 application, see [Get Started](./index.md#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Was ist WebView":::
   <span data-ttu-id="96eb5-110">Was ist WebView</span><span class="sxs-lookup"><span data-stu-id="96eb5-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="96eb5-111">Die WebView2 Preview ist für frühzeitiges Prototyping vorgesehen, um Feedback zu sammeln, um die API zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="96eb5-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help to shape the API.</span></span>  <span data-ttu-id="96eb5-112">Das Microsoft Edge-WebView-Team rät davon ab, die Vorschau in ihren Produktions-apps zu verwenden, da möglicherweise [wichtige Änderungen](./releasenotes.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="96eb5-112">The Microsoft Edge WebView team does not recommend that you use the preview in your production apps because there may be [breaking changes](./releasenotes.md).</span></span>  

## <span data-ttu-id="96eb5-113">Ansatz der Hybrid Anwendung</span><span class="sxs-lookup"><span data-stu-id="96eb5-113">Hybrid Application Approach</span></span>  

<span data-ttu-id="96eb5-114">Entwickler müssen häufig zwischen dem Erstellen einer Webanwendung oder einer systemeigenen Anwendung auswählen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-114">Developers often have to choose between building a web application or a native application.</span></span>  <span data-ttu-id="96eb5-115">Die Entscheidung hängt vom Kompromiss zwischen Reichweite und macht ab.</span><span class="sxs-lookup"><span data-stu-id="96eb5-115">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="96eb5-116">Web-Anwendungen ermöglichen eine breite Reichweite.</span><span class="sxs-lookup"><span data-stu-id="96eb5-116">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="96eb5-117">Als Web-Entwickler können Sie die meisten, wenn nicht alle Ihren Code, auf allen verschiedenen Plattformen wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="96eb5-117">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="96eb5-118">Systemeigene Anwendungen nutzen jedoch die Funktionen der gesamten systemeigenen Plattform.</span><span class="sxs-lookup"><span data-stu-id="96eb5-118">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native":::
   <span data-ttu-id="96eb5-120">Web Native</span><span class="sxs-lookup"><span data-stu-id="96eb5-120">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="96eb5-121">Hybrid Anwendungen ermöglichen Entwicklern, das Beste aus beiden Welten zu genießen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-121">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="96eb5-122">Entwickler von Hybrid Anwendungen profitieren von der Allgegenwart und Stärke der Web-Plattform sowie von der Leistungsfähigkeit und den vollständigen Funktionen der systemeigenen Plattform.</span><span class="sxs-lookup"><span data-stu-id="96eb5-122">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="96eb5-123">WebView2-Vorteile</span><span class="sxs-lookup"><span data-stu-id="96eb5-123">WebView2 Benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView-Gründe":::
   <span data-ttu-id="96eb5-125">WebView-Gründe</span><span class="sxs-lookup"><span data-stu-id="96eb5-125">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-126">Web-Ökosystem \ & skillset</span><span class="sxs-lookup"><span data-stu-id="96eb5-126">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="96eb5-127">Verwenden Sie die gesamte Web-Plattform, Bibliotheken, Tools und Talente, die im Web-Ökosystem vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="96eb5-127">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-128">Schnelle Innovation</span><span class="sxs-lookup"><span data-stu-id="96eb5-128">Rapid Innovation</span></span>**  
      <span data-ttu-id="96eb5-129">Web-Entwicklung ermöglicht schnellere Bereitstellung und Iteration.</span><span class="sxs-lookup"><span data-stu-id="96eb5-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-130">Windows 7, 8, 10 Support</span><span class="sxs-lookup"><span data-stu-id="96eb5-130">Windows 7, 8, 10 Support</span></span>**  
      <span data-ttu-id="96eb5-131">Unterstützung für eine konsistente Benutzeroberfläche in Windows 7, 8 und 10.</span><span class="sxs-lookup"><span data-stu-id="96eb5-131">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-132">Systemeigene Funktionen</span><span class="sxs-lookup"><span data-stu-id="96eb5-132">Native capabilities</span></span>**  
      <span data-ttu-id="96eb5-133">Greifen Sie auf den vollständigen Satz nativer APIs zu.</span><span class="sxs-lookup"><span data-stu-id="96eb5-133">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-134">Code Freigabe</span><span class="sxs-lookup"><span data-stu-id="96eb5-134">Code-sharing</span></span>**  
      <span data-ttu-id="96eb5-135">Durch Hinzufügen von Webcode zu ihrer CodeBase können Sie die Wiederverwendung auf mehreren Plattformen erhöhen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-135">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-136">Microsoft-Support</span><span class="sxs-lookup"><span data-stu-id="96eb5-136">Microsoft support</span></span>**  
      <span data-ttu-id="96eb5-137">Microsoft bietet Support und fügt neue Funktionsanforderungen hinzu, wenn WebView2 als "ga" veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="96eb5-137">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-138">Immergrüne Verteilung</span><span class="sxs-lookup"><span data-stu-id="96eb5-138">Evergreen distribution</span></span>**  
      <span data-ttu-id="96eb5-139">Verlassen Sie sich auf eine aktuelle Version von Chromium mit regulären Plattformupdates und Sicherheitspatches.</span><span class="sxs-lookup"><span data-stu-id="96eb5-139">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="96eb5-140">**Behoben** \ (in Kürze verfügbar)</span><span class="sxs-lookup"><span data-stu-id="96eb5-140">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="96eb5-141">Wählen Sie aus, um die Chrom Bits in Ihrer Anwendung zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="96eb5-141">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="96eb5-142">Inkrementelle Einführung</span><span class="sxs-lookup"><span data-stu-id="96eb5-142">Incremental adoption</span></span>**  
      <span data-ttu-id="96eb5-143">Fügen Sie Ihrer Anwendung Stück für Stück Webkomponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="96eb5-143">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="96eb5-144">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="96eb5-144">Getting Started</span></span>  

<span data-ttu-id="96eb5-145">Wenn Sie Ihre Anwendung mithilfe des WebView2-Steuerelements erstellen und testen möchten, müssen Sie sowohl [Microsoft Edge (Chrom)](https://www.microsoftedgeinsider.com/download) als auch das [WebView2-SDK](https://aka.ms/webviewnuget) installiert haben.</span><span class="sxs-lookup"><span data-stu-id="96eb5-145">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download) and the [WebView2 SDK](https://aka.ms/webviewnuget) installed.</span></span>  <span data-ttu-id="96eb5-146">Wählen Sie eine der folgenden Optionen aus, um loszulegen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="96eb5-147">Erste Schritte mit Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="96eb5-147">Getting Started with Win32 C/C++</span></span>](./gettingstarted/win32.md)  
*   [<span data-ttu-id="96eb5-148">Erste Schritte mit WPF</span><span class="sxs-lookup"><span data-stu-id="96eb5-148">Getting Started with WPF</span></span>](./gettingstarted/wpf.md)  
*   [<span data-ttu-id="96eb5-149">Erste Schritte mit WinForms</span><span class="sxs-lookup"><span data-stu-id="96eb5-149">Getting Started with WinForms</span></span>](./gettingstarted/winforms.md)  

<span data-ttu-id="96eb5-150">Das [WebView2-Beispiel](https://github.com/MicrosoftEdge/WebView2Samples) -Repository enthält Beispiele, die alle WebView2-SDKs-Features und API-Verwendungsmuster veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-150">The [WebView2 Samples](https://github.com/MicrosoftEdge/WebView2Samples) repository contains samples that demonstrate all of the WebView2 SDKs features and API usage patterns.</span></span> <span data-ttu-id="96eb5-151">Wenn dem WebView2-SDK weitere Features hinzugefügt werden, werden die Beispielanwendungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="96eb5-151">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>   

## <span data-ttu-id="96eb5-152">Unterstützte Plattformen</span><span class="sxs-lookup"><span data-stu-id="96eb5-152">Supported Platforms</span></span>  

<span data-ttu-id="96eb5-153">Eine Entwicklervorschau steht in den folgenden Programmierumgebungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="96eb5-153">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="96eb5-154">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="96eb5-154">Win32 C/C++</span></span>  
*   <span data-ttu-id="96eb5-155">.NET Framework 4.6.2 oder höher</span><span class="sxs-lookup"><span data-stu-id="96eb5-155">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="96eb5-156">.Net Core 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="96eb5-156">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="96eb5-157">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="96eb5-157">WinUI 3.0</span></span>](/uwp/toolkits/winui3/)  

<span data-ttu-id="96eb5-158">Sie müssen Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2 oder Windows Server 2008 R2 ausführen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-158">You must run Windows 10, Windows 8.1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2, or Windows Server 2008 R2.</span></span>   

## <span data-ttu-id="96eb5-159">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="96eb5-159">Next Steps</span></span>  

<span data-ttu-id="96eb5-160">Ausführlichere Informationen zum Erstellen und Bereitstellen von WebView2-Anwendungen finden Sie in unserer konzeptionellen Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="96eb5-160">For more detailed information on how to build and deploy WebView2 applications, checkout our conceptual documentation</span></span><!-- and how-to guides--><span data-ttu-id="96eb5-161">.</span><span class="sxs-lookup"><span data-stu-id="96eb5-161">.</span></span>  

#### <span data-ttu-id="96eb5-162">Konzepte</span><span class="sxs-lookup"><span data-stu-id="96eb5-162">Concepts</span></span>  

*   [<span data-ttu-id="96eb5-163">WebView2 SDK und Microsoft Edge-Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="96eb5-163">WebView2 SDK and Microsoft Edge Versioning</span></span>](./concepts/versioning.md)
*   [<span data-ttu-id="96eb5-164">Verteilen von WebView2-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="96eb5-164">Distributing WebView2 Applications</span></span>](./concepts/distribution.md)  
 
#### <span data-ttu-id="96eb5-165">Anleitungen</span><span class="sxs-lookup"><span data-stu-id="96eb5-165">How-To Guides</span></span>  

*   [<span data-ttu-id="96eb5-166">Debuggen von WebView2 mit devtools und Visual Studio-Skriptdebugging</span><span class="sxs-lookup"><span data-stu-id="96eb5-166">Debugging WebView2 with DevTools and Visual Studio Script Debugging</span></span>](./howto/debug.md)  
*   [<span data-ttu-id="96eb5-167">Automatisieren und Debuggen von WebView2 mit Microsoft EdgeDriver</span><span class="sxs-lookup"><span data-stu-id="96eb5-167">Automating and Debugging WebView2 with Microsoft EdgeDriver</span></span>](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## <span data-ttu-id="96eb5-168">Kontakt mit dem WebView2-Team</span><span class="sxs-lookup"><span data-stu-id="96eb5-168">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="96eb5-169">Helfen Sie beim Aufbau einer reicheren WebView2-Erfahrung, indem Sie Ihr Feedback freigeben.</span><span class="sxs-lookup"><span data-stu-id="96eb5-169">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="96eb5-170">Besuchen Sie das WebView [Feedback Repo](https://aka.ms/webviewfeedback) , um Funktionsanforderungen oder Fehlerberichte zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="96eb5-170">Visit the WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  <span data-ttu-id="96eb5-171">Es ist auch ein guter Ort, um nach bekannten Problemen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-171">It is also a good place to search for known issues.</span></span>  

> [!NOTE]
> <span data-ttu-id="96eb5-172">Während der Entwicklervorschau sammelt das Microsoft Edge-WebView-Team auch Daten, die zum Erstellen einer besseren WebView beitragen.</span><span class="sxs-lookup"><span data-stu-id="96eb5-172">During developer preview, the Microsoft Edge WebView team also collects data to help build a better WebView.</span></span>  <span data-ttu-id="96eb5-173">Benutzer können WebView-Datensammlung deaktivieren, indem Sie `edge://settings/privacy` im Microsoft Edge-Browser navigieren und die Browserdaten Sammlung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="96eb5-173">Users may turn off WebView data collection by navigating to `edge://settings/privacy` in the Microsoft Edge browser and turning off browser data collection.</span></span>  
