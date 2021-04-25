---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um Möglichkeiten zu finden, wie Sie Ihre Websites schneller laden können.
title: Optimieren der Websitegeschwindigkeit mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e3ddadcf37303a476f3a656696b00f121f079b69
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519611"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.  
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a><span data-ttu-id="576e6-104">Optimieren der Websitegeschwindigkeit mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="576e6-104">Optimize website speed with Microsoft Edge DevTools</span></span>  

## <a name="goal-of-tutorial"></a><span data-ttu-id="576e6-105">Ziel des Lernprogramms</span><span class="sxs-lookup"><span data-stu-id="576e6-105">Goal of tutorial</span></span>  

<span data-ttu-id="576e6-106">In diesem Lernprogramm erfahren Sie, wie Sie Microsoft Edge DevTools verwenden, um Möglichkeiten zu finden, wie Sie Ihre Websites schneller laden können.</span><span class="sxs-lookup"><span data-stu-id="576e6-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="576e6-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="576e6-107">Prerequisites</span></span>  

*   <span data-ttu-id="576e6-108">Sie sollten über grundlegende Webentwicklungserfahrungen verfügen, ähnlich wie in dieser Einführung in [die Webentwicklungsklasse][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="576e6-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="576e6-109">Sie müssen nichts über die Ladeleistung wissen.</span><span class="sxs-lookup"><span data-stu-id="576e6-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="576e6-110">In diesem Lernprogramm erfahren Sie mehr darüber.</span><span class="sxs-lookup"><span data-stu-id="576e6-110">You learn about it in this tutorial.</span></span>  

## <a name="introduction"></a><span data-ttu-id="576e6-111">Einführung</span><span class="sxs-lookup"><span data-stu-id="576e6-111">Introduction</span></span>  

<span data-ttu-id="576e6-112">Dies ist Tony.</span><span class="sxs-lookup"><span data-stu-id="576e6-112">This is Tony.</span></span>  <span data-ttu-id="576e6-113">Tony ist in der Katzengesellschaft sehr bekannt.</span><span class="sxs-lookup"><span data-stu-id="576e6-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="576e6-114">Er hat eine Website erstellt, damit seine Fans mehr über seine Lieblingsprodukte erfahren können.</span><span class="sxs-lookup"><span data-stu-id="576e6-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="576e6-115">Seine Fans lieben die Website, aber Tony hört immer wieder Beschwerden, dass die Website langsam geladen wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="576e6-116">Tony hat Sie gebeten, ihm bei der Beschleunigung der Website zu helfen.</span><span class="sxs-lookup"><span data-stu-id="576e6-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony, die Katze" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="576e6-118">Tony, die Katze</span><span class="sxs-lookup"><span data-stu-id="576e6-118">Tony the cat</span></span>  
:::image-end:::  

## <a name="step-1-audit-the-site"></a><span data-ttu-id="576e6-119">Schritt 1: Überwachen der Website</span><span class="sxs-lookup"><span data-stu-id="576e6-119">Step 1: Audit the site</span></span>  

<span data-ttu-id="576e6-120">Beginnen Sie immer mit einer Überwachung, wenn Sie die Lastleistung eines Standorts **verbessern möchten.**</span><span class="sxs-lookup"><span data-stu-id="576e6-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="576e6-121">Die Überwachung hat zwei wichtige Funktionen:</span><span class="sxs-lookup"><span data-stu-id="576e6-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="576e6-122">Es wird eine **Basislinie erstellt,** mit der Sie nachfolgende Änderungen messen können.</span><span class="sxs-lookup"><span data-stu-id="576e6-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="576e6-123">Sie erhalten praktische **Tipps dazu,** welche Änderungen die größten Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="576e6-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <a name="set-up"></a><span data-ttu-id="576e6-124">Einrichtung</span><span class="sxs-lookup"><span data-stu-id="576e6-124">Set up</span></span>  

<span data-ttu-id="576e6-125">Zunächst müssen Sie die Website so einrichten, dass Sie später Änderungen daran vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="576e6-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="576e6-126">[Öffnen Sie den Quellcode für die Website](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="576e6-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="576e6-127">Diese Registerkarte wird als **Editorregisterkarte bezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="576e6-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Die Registerkarte Editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="576e6-129">Die **Registerkarte Editor**</span><span class="sxs-lookup"><span data-stu-id="576e6-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-130">Wählen Sie **tony**aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-130">Choose **tony**.</span></span>  <span data-ttu-id="576e6-131">Es wird ein Menü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="576e6-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Das Menü, das nach der Auswahl von tony angezeigt wird" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="576e6-133">Das Menü, das nach der Auswahl von **tony angezeigt wird**</span><span class="sxs-lookup"><span data-stu-id="576e6-133">The menu that appears after choosing **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-134">Wählen Sie **#A0 aus.**</span><span class="sxs-lookup"><span data-stu-id="576e6-134">Choose **Remix Project**.</span></span>  <span data-ttu-id="576e6-135">Der Name des Projekts wird von **tony** in einen zufällig generierten Namen geändert.</span><span class="sxs-lookup"><span data-stu-id="576e6-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="576e6-136">Sie verfügen nun über eine eigene bearbeitbare Kopie des Codes.</span><span class="sxs-lookup"><span data-stu-id="576e6-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="576e6-137">Später können Sie Änderungen an diesem Code vornehmen.</span><span class="sxs-lookup"><span data-stu-id="576e6-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="576e6-138">Wählen **Sie Anzeigen** aus, und wählen Sie In einem neuen Fenster **aus.**</span><span class="sxs-lookup"><span data-stu-id="576e6-138">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="576e6-139">Die Demo wird auf einer neuen Registerkarte geöffnet.  Diese Registerkarte wird als Demoregisterkarte **bezeichnet.**  Es kann eine Weile dauern, bis die Website geladen ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Die Registerkarte Demo" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="576e6-141">Die Registerkarte Demo</span><span class="sxs-lookup"><span data-stu-id="576e6-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-142">Wählen `Control` + `Shift` + `J` Sie \(Windows, Linux\) oder `Command` + `Option` + `J` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-142">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="576e6-143">Microsoft Edge DevTools wird neben der Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="576e6-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools und die Demo" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="576e6-145">DevTools und die Demo</span><span class="sxs-lookup"><span data-stu-id="576e6-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="576e6-146">Für die restlichen Screenshots in diesem Lernprogramm wird DevTools in einem separaten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="576e6-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="576e6-147">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, `Undock` \*\*\*\* um das Befehlsmenü zu öffnen, und geben Sie ein, und wählen Sie dann Abdocken in ein separates Fenster aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Nicht gesockte DevTools" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="576e6-149">Nicht gesockte DevTools</span><span class="sxs-lookup"><span data-stu-id="576e6-149">Undocked DevTools</span></span>  
:::image-end:::  

### <a name="establish-a-baseline"></a><span data-ttu-id="576e6-150">Einrichten einer Basislinie</span><span class="sxs-lookup"><span data-stu-id="576e6-150">Establish a baseline</span></span>  

<span data-ttu-id="576e6-151">Die Basislinie ist eine Aufzeichnung der Leistung der Website, bevor Sie Leistungsverbesserungen vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="576e6-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="576e6-152">Wählen Sie das **Tool Überwachungen** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-152">Choose the **Audits** tool.</span></span>  <span data-ttu-id="576e6-153">Sie kann hinter der Schaltfläche **Weitere Bereiche** \( Weitere ![ Bereiche ](../media/more-panels-icon.msft.png) \) ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="576e6-153">It may be hidden behind the **More Panels** \(![More Panels](../media/more-panels-icon.msft.png)\) button.</span></span>  <span data-ttu-id="576e6-154">In diesem Panel befindet sich ein Leuchtturm, da das Projekt, das das Auditpanel unterstützt, den Namen **"Leuchtkraft" trägt.**</span><span class="sxs-lookup"><span data-stu-id="576e6-154">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Das Tool "Überwachungen"" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="576e6-156">Das **Tool "Überwachungen"**</span><span class="sxs-lookup"><span data-stu-id="576e6-156">The **Audits** tool</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="576e6-157">Passen Sie Ihre Überwachungskonfigurationseinstellungen den Einstellungen in der vorherigen Abbildung an.</span><span class="sxs-lookup"><span data-stu-id="576e6-157">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="576e6-158">Hier finden Sie eine Erläuterung der verschiedenen Optionen:</span><span class="sxs-lookup"><span data-stu-id="576e6-158">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="576e6-159">**Gerät**.</span><span class="sxs-lookup"><span data-stu-id="576e6-159">**Device**.</span></span>  <span data-ttu-id="576e6-160">Auf **Mobile festgelegt** ändert die Zeichenfolge des Benutzer-Agents und simuliert einen mobilen Viewport.</span><span class="sxs-lookup"><span data-stu-id="576e6-160">Set to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="576e6-161">Wenn Sie **auf Desktop** festlegen, werden die Mobile-Änderungen **einfach** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="576e6-161">Set to **Desktop** pretty much just turns off the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="576e6-162">**Überwachungen**.</span><span class="sxs-lookup"><span data-stu-id="576e6-162">**Audits**.</span></span>  <span data-ttu-id="576e6-163">Deaktivieren Sie eine Kategorie, um zu verhindern, dass diese Überwachungen vom Überwachungsbericht ausgeführt werden, und schließen Sie diese Überwachungen aus Ihrem Bericht aus. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="576e6-163">Turn off a category to prevent the **Audits** panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="576e6-164">Lassen Sie die anderen Kategorien aktiviert, wenn Sie die typen von Empfehlungen anzeigen möchten, die bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="576e6-164">Leave the other categories Turned on, if you want to display the types of recommendations that are provided.</span></span>  <span data-ttu-id="576e6-165">Deaktivieren Sie Kategorien, um den Überwachungsprozess geringfügig zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="576e6-165">Turn off categories to slightly speed up the auditing process.</span></span>  
    *   <span data-ttu-id="576e6-166">**Einschränkung**.</span><span class="sxs-lookup"><span data-stu-id="576e6-166">**Throttling**.</span></span>  <span data-ttu-id="576e6-167">Auf **Simulierte langsame 4G festgelegt, simuliert die 4-fache CPU-Verlangsamung** die typischen Bedingungen des Browsens auf einem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="576e6-167">Set to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="576e6-168">Er wird als "simuliert" bezeichnet, da der Überwachungsprozess während des Überwachungsprozesses nicht tatsächlich gedrosselt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-168">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="576e6-169">Stattdessen wird lediglich extrapoliert, wie lange die Seite unter mobilen Bedingungen geladen werden muss.</span><span class="sxs-lookup"><span data-stu-id="576e6-169">Instead, it just extrapolates how long the page takes to load under mobile conditions.</span></span>  <span data-ttu-id="576e6-170">Die **Einstellung Applied...** hingegen drosselt ihre CPU und Ihr Netzwerk, was zu einem längeren Überwachungsprozess beit.</span><span class="sxs-lookup"><span data-stu-id="576e6-170">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="576e6-171">**Speicher löschen**.</span><span class="sxs-lookup"><span data-stu-id="576e6-171">**Clear Storage**.</span></span>  <span data-ttu-id="576e6-172">Aktivieren Sie das Kontrollkästchen, um den speicher, der der Seite zugeordnet ist, vor jeder Überwachung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="576e6-172">Turn on the checkbox to clear all storage associated with the page before every audit.</span></span>  <span data-ttu-id="576e6-173">Lassen Sie diese Einstellung bei, wenn Sie überwachen möchten, wie Besucher Ihre Website beim ersten Mal erleben.</span><span class="sxs-lookup"><span data-stu-id="576e6-173">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="576e6-174">Deaktivieren Sie diese Einstellung, wenn Sie die Wiederholungsbesuchserfahrung wünschen.</span><span class="sxs-lookup"><span data-stu-id="576e6-174">Turn off this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="576e6-175">Wählen **Sie Überwachungen ausführen aus.**</span><span class="sxs-lookup"><span data-stu-id="576e6-175">Choose **Run Audits**.</span></span>  <span data-ttu-id="576e6-176">Nach 10 bis 30 \*\*\*\* Sekunden zeigt der Bereich Überwachungen einen Bericht über die Leistung der Website an.</span><span class="sxs-lookup"><span data-stu-id="576e6-176">After 10 to 30 seconds, the **Audits** panel displays a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Der Bericht für den Überwachungsbericht über die Leistung der Website" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="576e6-178">Der Bericht für den Überwachungsbericht über die Leistung der Website</span><span class="sxs-lookup"><span data-stu-id="576e6-178">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a><span data-ttu-id="576e6-179">Behandeln von Berichtsfehlern</span><span class="sxs-lookup"><span data-stu-id="576e6-179">Handling report errors</span></span>  

<span data-ttu-id="576e6-180">Wenn Sie jemals einen Fehler in Ihrem Bericht zum Überwachungsbericht erhalten, versuchen Sie, die Demoregisterkarte aus einem **InPrivate-Fenster** zu führen, ohne dass andere Registerkarten geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="576e6-180">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="576e6-181">Dadurch wird sichergestellt, dass Microsoft Edge in einem sauberen Zustand ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-181">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="576e6-182">Insbesondere Microsoft Edge Extensions stören häufig den Überwachungsprozess.</span><span class="sxs-lookup"><span data-stu-id="576e6-182">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a><span data-ttu-id="576e6-183">Verstehen Ihres Berichts</span><span class="sxs-lookup"><span data-stu-id="576e6-183">Understand your report</span></span>  

<span data-ttu-id="576e6-184">Die Nummer oben in Ihrem Bericht ist die Gesamtleistungsnote für die Website.</span><span class="sxs-lookup"><span data-stu-id="576e6-184">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="576e6-185">Wenn Sie später Änderungen am Code vornehmen, sollte die angezeigte Anzahl steigen.</span><span class="sxs-lookup"><span data-stu-id="576e6-185">Later, as you make changes to the code, the number displayed should rise.</span></span>  <span data-ttu-id="576e6-186">Eine höhere Punktzahl bedeutet eine bessere Leistung.</span><span class="sxs-lookup"><span data-stu-id="576e6-186">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Gesamtleistungsergebnis" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="576e6-188">Gesamtleistungsergebnis</span><span class="sxs-lookup"><span data-stu-id="576e6-188">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-189">Der **Abschnitt Metriken** enthält mengenmäßige Messungen der Leistung der Website.</span><span class="sxs-lookup"><span data-stu-id="576e6-189">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="576e6-190">Jede Metrik bietet Einblick in einen anderen Aspekt der Leistung.</span><span class="sxs-lookup"><span data-stu-id="576e6-190">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="576e6-191">Beispielsweise informiert **First Contentful Paint,** wann Inhalte zum ersten Mal auf den Bildschirm gefärbt werden. Dies ist ein wichtiger Meilenstein in der Wahrnehmung der Seitenlast durch den Benutzer, während **Time To Interactive** den Punkt markiert, an dem die Seite so bereit erscheint, dass Benutzerinteraktionen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="576e6-191">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Abschnitt "Metriken"" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="576e6-193">Abschnitt **"Metriken"**</span><span class="sxs-lookup"><span data-stu-id="576e6-193">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-194">Wählen Sie die hervorgehobene Umschaltfläche in der folgenden Abbildung aus, um eine Beschreibung für jede Metrik anzeigen zu können, und wählen Sie **Weitere** Informationen aus, um die Dokumentation dazu zu lesen.</span><span class="sxs-lookup"><span data-stu-id="576e6-194">Choose the highlighted toggle button in the following figure to display a description for each metric, and choose **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Wählen Sie die hervorgehobene Umschaltfläche aus, um die Metrikelemente zu erweitern." lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="576e6-196">Wählen Sie die hervorgehobene Umschaltfläche aus, um die Metrikelemente zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="576e6-196">Choose the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-197">Unter Metriken finden Sie eine Sammlung von Screenshots, die ihnen zeigen, wie die Seite wie geladen aussah.</span><span class="sxs-lookup"><span data-stu-id="576e6-197">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Screenshots, wie die Seite beim Laden aussah" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="576e6-199">Screenshots, wie die Seite beim Laden aussah</span><span class="sxs-lookup"><span data-stu-id="576e6-199">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-200">Der **Abschnitt Verkaufschancen** enthält spezifische Tipps zur Verbesserung der Ladeleistung dieser spezifischen Seite.</span><span class="sxs-lookup"><span data-stu-id="576e6-200">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Der Abschnitt Verkaufschancen" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="576e6-202">Der **Abschnitt Verkaufschancen**</span><span class="sxs-lookup"><span data-stu-id="576e6-202">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-203">Wählen Sie eine Gelegenheit aus, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="576e6-203">Choose an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminieren von Möglichkeiten zum Rendern blockierender Ressourcen" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="576e6-205">**Eliminieren von Möglichkeiten zum Rendern blockierender** Ressourcen</span><span class="sxs-lookup"><span data-stu-id="576e6-205">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-206">Wählen **Sie Weitere Informationen** aus, um Dokumentation darüber zu erhalten, warum eine Gelegenheit wichtig ist, und spezifische Empfehlungen zum Beheben dieser Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="576e6-206">Choose **Learn More** to display documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Dokumentation zur Möglichkeit zum Entfernen von Renderblockierungsressourcen" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="576e6-208">Dokumentation zur **Möglichkeit zum Entfernen von Renderblockierungsressourcen**</span><span class="sxs-lookup"><span data-stu-id="576e6-208">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-209">Der **Abschnitt Diagnose** enthält weitere Informationen zu Faktoren, die zur Ladezeit der Seite beitragen.</span><span class="sxs-lookup"><span data-stu-id="576e6-209">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Der Abschnitt "Diagnostics"" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="576e6-211">Der **Abschnitt "Diagnostics"**</span><span class="sxs-lookup"><span data-stu-id="576e6-211">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-212">Der **Abschnitt "Bestandene Prüfungen"** zeigt Ihnen, was die Website ordnungsgemäß macht.</span><span class="sxs-lookup"><span data-stu-id="576e6-212">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="576e6-213">Wählen Sie aus, um den Abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="576e6-213">Choose to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Der Abschnitt "Bestandene Überwachungen"" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="576e6-215">Der **Abschnitt "Bestandene Überwachungen"**</span><span class="sxs-lookup"><span data-stu-id="576e6-215">The **Passed Audits** section</span></span>  
:::image-end:::  

## <a name="step-2-experiment"></a><span data-ttu-id="576e6-216">Schritt 2: Experiment</span><span class="sxs-lookup"><span data-stu-id="576e6-216">Step 2: Experiment</span></span>  

<span data-ttu-id="576e6-217">Im Abschnitt Verkaufschancen Ihres Überwachungsberichts erhalten Sie Tipps zur Verbesserung der Leistung der Seite.</span><span class="sxs-lookup"><span data-stu-id="576e6-217">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="576e6-218">In diesem Abschnitt implementieren Sie die empfohlenen Änderungen an der Codebasis und überwachen die Website nach jeder Änderung, um zu messen, wie sich dies auf die Websitegeschwindigkeit auswirkt.</span><span class="sxs-lookup"><span data-stu-id="576e6-218">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <a name="enable-text-compression"></a><span data-ttu-id="576e6-219">Aktivieren der Textkomprimierung</span><span class="sxs-lookup"><span data-stu-id="576e6-219">Enable text compression</span></span>  

<span data-ttu-id="576e6-220">In Ihrem Bericht heißt es, dass die Vermeidung enormer Netzwerknutzlasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-220">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="576e6-221">Das Aktivieren der Textkomprimierung ist eine Möglichkeit, die Leistung der Seite zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="576e6-221">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="576e6-222">Die Textkomprimierung ist, wenn Sie die Größe einer Textdatei reduzieren oder komprimieren, bevor Sie sie über das Netzwerk senden.</span><span class="sxs-lookup"><span data-stu-id="576e6-222">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="576e6-223">Ähnlich wie Sie ein Verzeichnis archivieren können, bevor Sie es senden, um die Größe zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="576e6-223">Similar to how you may archive a directory before sending it to reduce the size.</span></span>  

<span data-ttu-id="576e6-224">Bevor Sie die Komprimierung aktivieren, finden Sie hier eine Reihe von Möglichkeiten, um manuell zu überprüfen, ob Textressourcen komprimiert sind.</span><span class="sxs-lookup"><span data-stu-id="576e6-224">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="576e6-225">Wählen Sie das **Netzwerktool** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-225">Choose the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Netzwerkbereich" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="576e6-227">Das **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="576e6-227">The **Network** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-228">Wählen Sie das **Symbol Netzwerkeinstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-228">Choose the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="576e6-229">Aktivieren Sie das **Kontrollkästchen Große Anforderungszeilen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="576e6-229">Choose the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="576e6-230">Die Höhe der Zeilen in der Tabelle der Netzwerkanforderungen nimmt zu.</span><span class="sxs-lookup"><span data-stu-id="576e6-230">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Große Zeilen in der Tabelle "Netzwerkanforderungen"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="576e6-232">Große Zeilen in der Tabelle "Netzwerkanforderungen"</span><span class="sxs-lookup"><span data-stu-id="576e6-232">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-233">Wenn die **Spalte Größe** in der Tabelle der Netzwerkanforderungen nicht angezeigt wird, wählen Sie die Tabellenkopfzeile > **Größe aus.**</span><span class="sxs-lookup"><span data-stu-id="576e6-233">If the **Size** column in the table of network requests is not displayed, choose the table header > **Size**.</span></span>  

<span data-ttu-id="576e6-234">Jede **Zelle Size** zeigt zwei Werte an.</span><span class="sxs-lookup"><span data-stu-id="576e6-234">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="576e6-235">Der höchste Wert ist die Größe der heruntergeladenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="576e6-235">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="576e6-236">Der untere Wert ist die Größe der nicht komprimierten Ressource.</span><span class="sxs-lookup"><span data-stu-id="576e6-236">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="576e6-237">Wenn die beiden Werte identisch sind, wird die Ressource nicht komprimiert, wenn sie über das Netzwerk gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-237">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="576e6-238">In der vorherigen Abbildung sind beispielsweise die oberen und unteren Werte `bundle.js` für und `1.2 MB` `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="576e6-238">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="576e6-239">Überprüfen Sie auf Komprimierung, indem Sie die HTTP-Header einer Ressource überprüfen:</span><span class="sxs-lookup"><span data-stu-id="576e6-239">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="576e6-240">Wählen Sie `bundle.js` aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-240">Choose `bundle.js`.</span></span>  
1.  <span data-ttu-id="576e6-241">Wählen Sie **den Bereich Kopfzeilen** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-241">Choose the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Der Kopfzeilenbereich" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="576e6-243">Der **Kopfzeilenbereich**</span><span class="sxs-lookup"><span data-stu-id="576e6-243">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-244">Durchsuchen Sie **den Abschnitt Antwortkopfzeilen** nach einer `content-encoding` Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="576e6-244">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="576e6-245">Eine `content-encoding` Überschrift wird nicht angezeigt, d. h. sie wurde nicht `bundle.js` komprimiert.</span><span class="sxs-lookup"><span data-stu-id="576e6-245">A `content-encoding` heading is not displayed, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="576e6-246">Wenn eine Ressource komprimiert wird, wird dieser Header in der Regel auf `gzip` , `deflate` oder `br` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="576e6-246">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="576e6-247">Eine Erläuterung der Werte finden Sie unter [Direktiven][MDNContentEncodingDirectives].</span><span class="sxs-lookup"><span data-stu-id="576e6-247">For an explanation of the values, navigate to [Directives][MDNContentEncodingDirectives].</span></span>  

<span data-ttu-id="576e6-248">Genug mit den Erläuterungen.</span><span class="sxs-lookup"><span data-stu-id="576e6-248">Enough with the explanations.</span></span>  <span data-ttu-id="576e6-249">Zeit für einige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="576e6-249">Time to make some changes.</span></span>  <span data-ttu-id="576e6-250">Aktivieren Sie die Textkomprimierung, indem Sie ein paar Codezeilen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="576e6-250">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="576e6-251">Wählen Sie auf der Registerkarte Editor \*\* die Optionserver.js\*\*.</span><span class="sxs-lookup"><span data-stu-id="576e6-251">In the editor tab, choose **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Bearbeiten server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="576e6-253">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="576e6-253">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-254">Fügen Sie den folgenden Code zu \*\*server.js. \*\*</span><span class="sxs-lookup"><span data-stu-id="576e6-254">Add the following code to **server.js**.</span></span>  <span data-ttu-id="576e6-255">Stellen Sie sicher, dass Sie vor `app.use(compression())` `app.use(express.static('build'))` setzen.</span><span class="sxs-lookup"><span data-stu-id="576e6-255">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="576e6-256">In der Regel müssen Sie das Paket über so etwas wie installieren, aber dies wurde `compression` bereits für Sie `npm i -S compression` durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="576e6-256">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="576e6-257">Warten Sie, bis Glitch den neuen Build der Website bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="576e6-257">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="576e6-258">Die ausgefallene Animation neben **Tools** bedeutet, dass die Website neu erstellt und erneut zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="576e6-258">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="576e6-259">Die Änderung ist bereit, wenn die Animation neben **Tools** nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-259">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="576e6-260">Wählen **Sie Anzeigen** aus, und wählen Sie erneut In einem neuen **Fenster** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-260">Choose **Show** and choose **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="576e6-261">Verwenden Sie die Workflows, die Sie zuvor gelernt haben, um manuell zu überprüfen, ob die Komprimierung funktioniert:</span><span class="sxs-lookup"><span data-stu-id="576e6-261">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="576e6-262">Wechseln Sie zurück zur Demoregisterkarte, und aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="576e6-262">Go back to the demo tab and refresh the page.</span></span>  <span data-ttu-id="576e6-263">In **der Spalte** Größe sollten nun 2 verschiedene Werte für Textressourcen wie angezeigt `bundle.js` werden.</span><span class="sxs-lookup"><span data-stu-id="576e6-263">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="576e6-264">In der Abbildung nach der folgenden Abbildung ist der oberste Wert für die Größe der Datei, die über das Netzwerk gesendet wurde, und der untere Wert ist die nicht komprimierte `256 KB` `bundle.js` `1.2 MB` Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="576e6-264">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="Die Spalte Größe zeigt jetzt 2 verschiedene Werte für Textressourcen an." lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="576e6-266">Die **Spalte Größe** zeigt jetzt 2 verschiedene Werte für Textressourcen an.</span><span class="sxs-lookup"><span data-stu-id="576e6-266">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-267">Der **Abschnitt Antwortkopfzeilen** für `bundle.js` sollte jetzt einen Header `content-encoding: gzip` enthalten.</span><span class="sxs-lookup"><span data-stu-id="576e6-267">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Der Abschnitt Antwortkopfzeilen enthält jetzt einen Header für die Inhaltscodierung." lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="576e6-269">Der **Abschnitt Antwortkopfzeilen** enthält jetzt einen Header für die Inhaltscodierung.</span><span class="sxs-lookup"><span data-stu-id="576e6-269">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="576e6-270">Überwachen Sie die Seite erneut, um zu messen, welche Art von Auswirkung die Textkomprimierung auf die Ladeleistung der Seite hat:</span><span class="sxs-lookup"><span data-stu-id="576e6-270">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="576e6-271">Wählen Sie das **Tool Überwachungen** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-271">Choose the **Audits** tool.</span></span>  
1.  <span data-ttu-id="576e6-272">Wählen **Sie Ausführen einer Überwachung** \( Ausführen einer Überwachung ![ ](../media/perform-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="576e6-272">Choose **Perform an audit** \(![Perform an audit](../media/perform-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="576e6-273">Lassen Sie die Einstellungen wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="576e6-273">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="576e6-274">Wählen **Sie Überwachung ausführen aus.**</span><span class="sxs-lookup"><span data-stu-id="576e6-274">Choose **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Aktivierung der Textkomprimierung" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="576e6-276">Ein Überwachungsbericht nach der Aktivierung der Textkomprimierung</span><span class="sxs-lookup"><span data-stu-id="576e6-276">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="576e6-277">Ihr Gesamtleistungsergebnis sollte erhöht sein, was bedeutet, dass die Website schneller wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-277">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <a name="text-compression-in-the-real-world"></a><span data-ttu-id="576e6-278">Textkomprimierung in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="576e6-278">Text compression in the real world</span></span>  

<span data-ttu-id="576e6-279">Die meisten Server verfügen tatsächlich über einfache Korrekturen wie dies zum Aktivieren der Komprimierung!</span><span class="sxs-lookup"><span data-stu-id="576e6-279">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="576e6-280">Suchen Sie einfach, wie Sie den Server konfigurieren, den Sie zum Komprimieren von Text verwenden.</span><span class="sxs-lookup"><span data-stu-id="576e6-280">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <a name="resize-images"></a><span data-ttu-id="576e6-281">Ändern der Größe von Bildern</span><span class="sxs-lookup"><span data-stu-id="576e6-281">Resize images</span></span>  

<span data-ttu-id="576e6-282">Ihr Bericht weist darauf hin, dass das Vermeiden enormer Netzwerknutzlasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-282">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="576e6-283">Die Größenänderung von Bildern trägt dazu bei, die Größe der Netzwerknutzlast zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="576e6-283">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="576e6-284">Wenn Ihr Benutzer Ihre Bilder auf einem 500 Pixel breiten Bildschirm des mobilen Geräts anschaut, hat es wirklich keinen Sinn, ein 1500 Pixel breites Bild zu senden.</span><span class="sxs-lookup"><span data-stu-id="576e6-284">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="576e6-285">Idealerweise senden Sie ein Bild mit einer Breite von 500 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="576e6-285">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="576e6-286">Wählen Sie in Ihrem Bericht **Enorme Netzwerknutzlast** vermeiden aus, um die Größe der Bilder anzeigen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="576e6-286">In your report, choose **Avoid enormous network payloads** to display which images should be resized.</span></span>  <span data-ttu-id="576e6-287">Es sieht so aus, als seien 2 der JPG-Dateien über 2000 KB, was größer als erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-287">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="576e6-288">Öffnen Sie zurück auf der Registerkarte Editor `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="576e6-288">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="576e6-289">Ersetzen Sie `const dir = 'big'` durch `const dir = 'small'`.</span><span class="sxs-lookup"><span data-stu-id="576e6-289">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="576e6-290">Dieses Verzeichnis enthält Kopien der gleichen Bilder, deren Größe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="576e6-290">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="576e6-291">Überwachen Sie die Seite erneut, um zu zeigen, wie sich die Änderung auf die Lastleistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="576e6-291">Audit the page again to display how the change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Größenänderung von Bildern" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="576e6-293">Ein Überwachungsbericht nach der Größenänderung von Bildern</span><span class="sxs-lookup"><span data-stu-id="576e6-293">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="576e6-294">Die angezeigte Änderung hat nur geringfügige Auswirkungen auf die Gesamtleistungsleistung.</span><span class="sxs-lookup"><span data-stu-id="576e6-294">The change displays only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="576e6-295">Die Bewertung zeigt jedoch nicht eindeutig, wie viele Netzwerkdaten Sie Ihre Benutzer speichern.</span><span class="sxs-lookup"><span data-stu-id="576e6-295">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="576e6-296">Die Gesamtgröße der alten Fotos lag bei etwa 5,3 Megabyte, jetzt sind es nur noch etwa 0,18 Megabyte.</span><span class="sxs-lookup"><span data-stu-id="576e6-296">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <a name="resizing-images-in-the-real-world"></a><span data-ttu-id="576e6-297">Ändern der Größe von Bildern in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="576e6-297">Resizing images in the real world</span></span>  

<span data-ttu-id="576e6-298">Für eine kleine App ist eine einmal angepasste Größe wie dies möglicherweise ausreichend.</span><span class="sxs-lookup"><span data-stu-id="576e6-298">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="576e6-299">Bei einer großen App ist dies jedoch offensichtlich nicht skalierbar.</span><span class="sxs-lookup"><span data-stu-id="576e6-299">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="576e6-300">Hier sind einige Strategien zum Verwalten von Bildern in großen Apps:</span><span class="sxs-lookup"><span data-stu-id="576e6-300">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="576e6-301">Ändern der Größe von Bildern während des Buildprozesses.</span><span class="sxs-lookup"><span data-stu-id="576e6-301">Resize images during your build process.</span></span>  
*   <span data-ttu-id="576e6-302">Erstellen Sie während des Erstellungsprozesses mehrere Größen der einzelnen Bilder, und verwenden Sie sie `srcset` dann in Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="576e6-302">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="576e6-303">Zur Laufzeit übernimmt der Browser die Auswahl, welche Größe für das Gerät am besten ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-303">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="576e6-304">Verwenden Sie ein Image-CDN, mit dem Sie die Größe eines Bilds dynamisch ändern können, wenn Sie es anfordern.</span><span class="sxs-lookup"><span data-stu-id="576e6-304">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="576e6-305">Optimieren Sie zumindest jedes Bild.</span><span class="sxs-lookup"><span data-stu-id="576e6-305">At the very least, optimize each image.</span></span>  <span data-ttu-id="576e6-306">Dies kann zu enormen Einsparungen führen.</span><span class="sxs-lookup"><span data-stu-id="576e6-306">This may create huge savings.</span></span>  
  <span data-ttu-id="576e6-307">Optimierung ist, wenn Sie ein Bild über ein spezielles Programm ausführen, das die Größe der Bilddatei reduziert.</span><span class="sxs-lookup"><span data-stu-id="576e6-307">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="576e6-308">Weitere Tipps finden Sie unter [Essential Image Optimization][EssentialImageOptimization].</span><span class="sxs-lookup"><span data-stu-id="576e6-308">For more tips, navigate to [Essential Image Optimization][EssentialImageOptimization].</span></span>  
    
### <a name="eliminate-render-blocking-resources"></a><span data-ttu-id="576e6-309">Eliminieren von render blockierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="576e6-309">Eliminate render-blocking resources</span></span>  

<span data-ttu-id="576e6-310">In Ihrem neuesten Bericht heißt es, dass das Eliminieren von Renderblockierressourcen jetzt die größte Möglichkeit ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-310">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="576e6-311">Eine Renderblockierressource ist eine externe JavaScript- oder CSS-Datei, die der Browser herunterladen, analysieren und ausführen muss, bevor die Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-311">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="576e6-312">Ziel ist es, nur den zentralen CSS- und JavaScript-Code ausführen, der zum ordnungsgemäßen Anzeigen der Seite erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-312">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="576e6-313">Die erste Aufgabe besteht also darin, Code zu finden, den Sie beim Laden der Seite nicht ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="576e6-313">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="576e6-314">Wählen **Sie Render blockierende Ressourcen entfernen aus,** um die blockierten Ressourcen anzeigen zu können:</span><span class="sxs-lookup"><span data-stu-id="576e6-314">Choose **Eliminate render-blocking resources** to display the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="576e6-315">und `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="576e6-315">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Weitere Informationen zur Gelegenheit Rendersperren von Ressourcen beseitigen" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="576e6-317">Weitere Informationen zur **Gelegenheit Rendersperren von Ressourcen** beseitigen</span><span class="sxs-lookup"><span data-stu-id="576e6-317">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-318">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, `Coverage` \*\*\*\* um das Befehlsmenü zu öffnen, mit der Eingabe zu beginnen, und wählen Sie dann Abdeckung anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-318">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then choose **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Öffnen des Befehlsmenüs im Überwachungbereich" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="576e6-320">Öffnen des Befehlsmenüs im **Überwachungbereich**</span><span class="sxs-lookup"><span data-stu-id="576e6-320">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Das Tool "Abdeckung"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="576e6-322">Das **Tool "Abdeckung"**</span><span class="sxs-lookup"><span data-stu-id="576e6-322">The **Coverage** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-323">Wählen **Sie Aktualisieren** \( Aktualisieren ![ ](../media/reload-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="576e6-323">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\).</span></span>  <span data-ttu-id="576e6-324">Das **Tool** Coverage bietet eine Übersicht darüber, wie viel Code in , und ausgeführt wird, während `bundle.js` die Seite geladen `jquery.js` `lodash.js` wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-324">The **Coverage** tool provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="576e6-325">In der Abbildung nach der folgenden Abbildung werden ca. 76 % bzw. 30 % der jQuery- und Lodash-Dateien nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="576e6-325">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Der Bericht "Abdeckung"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="576e6-327">Der Bericht "Abdeckung"</span><span class="sxs-lookup"><span data-stu-id="576e6-327">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-328">Wählen Sie die `jquery.js` Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-328">Choose the `jquery.js` row.</span></span>  <span data-ttu-id="576e6-329">DevTools öffnet die Datei im **Tool Quellen.**</span><span class="sxs-lookup"><span data-stu-id="576e6-329">DevTools opens the file in the **Sources** tool.</span></span>  <span data-ttu-id="576e6-330">Wenn eine Codezeile gelaufen ist, wird daneben ein blauer Balken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="576e6-330">If a line of code ran, a blue bar appears next to it.</span></span>  <span data-ttu-id="576e6-331">Ein roter Balken bedeutet, dass die Codezeile nicht ausgeführt wurde und bei der Auslastung der Webseite definitiv nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-331">A red bar means the line of code was not run, and is definitely not needed on load of the webpage.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Anzeigen der jQuery-Datei im Tool Quellen" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="576e6-333">Anzeigen der jQuery-Datei im **Tool Quellen**</span><span class="sxs-lookup"><span data-stu-id="576e6-333">Viewing the jQuery file in the **Sources** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-334">Scrollen Sie durch den jQuery-Code.</span><span class="sxs-lookup"><span data-stu-id="576e6-334">Scroll through the jQuery code.</span></span>  <span data-ttu-id="576e6-335">Einige der zeilen, die ausgeführt werden, sind eigentlich nur Kommentare.</span><span class="sxs-lookup"><span data-stu-id="576e6-335">Some of the lines that run are actually just comments.</span></span>  <span data-ttu-id="576e6-336">Um Kommentare zu löschen und die Größe der Datei zu reduzieren, führen Sie den Code über eine Minifier-App oder ein Miniskript aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-336">To strip comments and reduce the size of the file, run the code through a minifier app or script.</span></span>  

<span data-ttu-id="576e6-337">Kurz gesagt, wenn Sie mit Ihrem \*\*\*\* eigenen Code arbeiten, hilft Ihnen das Coverage-Tool dabei, Ihren Code zeiler zu analysieren und nur den Code zu versenden, der für das Laden von Seiten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-337">In short, when you are working with your own code, the **Coverage** tool helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="576e6-338">Sind die `jquery.js` `lodash.js` Und-Dateien sogar zum Laden der Seite erforderlich?</span><span class="sxs-lookup"><span data-stu-id="576e6-338">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="576e6-339">Das **Tool zum Blockieren** von Anfragen zeigt an, was geschieht, wenn Ressourcen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="576e6-339">The **Request blocking** tool displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="576e6-340">Wählen Sie das **Netzwerktool** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-340">Choose the **Network** tool.</span></span>  
1.  <span data-ttu-id="576e6-341">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das Befehlsmenü erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="576e6-341">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="576e6-342">Beginnen Sie mit der `blocking` Eingabe, und wählen Sie **Dann Anforderungsblockierung anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="576e6-342">Start typing `blocking` and then choose **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Das Tool zum Blockieren von Anfragen" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="576e6-344">Das **Tool zum Blockieren von** Anfragen</span><span class="sxs-lookup"><span data-stu-id="576e6-344">The **Request blocking** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-345">Wählen **Sie Muster hinzufügen** \( Muster hinzufügen \), geben Sie ![ ](../media/add-pattern-icon.msft.png) `/libs/*` ein, und wählen Sie dann `Enter` aus, um dies zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="576e6-345">Choose **Add Pattern** \(![Add Pattern](../media/add-pattern-icon.msft.png)\), type `/libs/*`, and then select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Hinzufügen eines Musters zum Blockieren jeder Anforderung zum libs-Verzeichnis" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="576e6-347">Hinzufügen eines Musters zum Blockieren einer Anforderung zum `libs` Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="576e6-347">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-348">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="576e6-348">Refresh the page.</span></span>  <span data-ttu-id="576e6-349">Die jQuery- und Lodash-Anforderungen sind rot, d. h., die Anforderungen wurden blockiert.</span><span class="sxs-lookup"><span data-stu-id="576e6-349">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="576e6-350">Die Seite wird weiterhin geladen und ist interaktiv, daher sieht es so aus, als ob diese Ressourcen überhaupt nicht benötigt werden!</span><span class="sxs-lookup"><span data-stu-id="576e6-350">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Der Netzwerkbereich zeigt an, dass die Anforderungen blockiert wurden" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="576e6-352">Das **Netzwerktool** zeigt, dass die Anforderungen blockiert wurden</span><span class="sxs-lookup"><span data-stu-id="576e6-352">The **Network** tool shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-353">Wählen **Sie Alle Muster entfernen** \( Alle Muster entfernen ![ ](../media/remove-icon.msft.png) \), um das `/libs/*` Blockierungsmuster zu löschen.</span><span class="sxs-lookup"><span data-stu-id="576e6-353">Choose **Remove all patterns** \(![Remove all patterns](../media/remove-icon.msft.png)\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="576e6-354">Im Allgemeinen ist das **Tool zum** Blockieren von Anforderungen hilfreich, um das Verhalten Ihrer Seite zu simulieren, wenn keine bestimmte Ressource verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-354">In general, the **Request blocking** tool is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="576e6-355">Entfernen Sie nun die Verweise auf diese Dateien aus dem Code, und überwachen Sie die Seite erneut:</span><span class="sxs-lookup"><span data-stu-id="576e6-355">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="576e6-356">Öffnen Sie zurück auf der Registerkarte Editor `template.html` .</span><span class="sxs-lookup"><span data-stu-id="576e6-356">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="576e6-357">Löschen Sie `<script src="/libs/lodash.js">` und `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="576e6-357">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="576e6-358">Warten Sie, bis die Website neu erstellen und erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-358">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="576e6-359">Überwachen Sie die Seite erneut über das **Überwachungstool.**</span><span class="sxs-lookup"><span data-stu-id="576e6-359">Audit the page again from the **Audits** tool.</span></span>  <span data-ttu-id="576e6-360">Ihr Gesamtergebnis sollte sich erneut verbessert haben.</span><span class="sxs-lookup"><span data-stu-id="576e6-360">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen der renderblocking-Ressourcen" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="576e6-362">Ein **Überwachungsbericht** nach dem Entfernen der renderblocking-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="576e6-362">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a><span data-ttu-id="576e6-363">Optimieren des kritischen Renderingpfads in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="576e6-363">Optimizing the Critical Rendering Path in the real-world</span></span>  

<span data-ttu-id="576e6-364">Der **Kritische Renderingpfad** bezieht sich auf den Code, den Sie zum Laden einer Seite benötigen.</span><span class="sxs-lookup"><span data-stu-id="576e6-364">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="576e6-365">Beschleunigen Sie im Allgemeinen das Laden der Seite, indem Sie während des Seitenladevorganges nur kritischen Code versenden und dann alles andere verzögert laden.</span><span class="sxs-lookup"><span data-stu-id="576e6-365">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="576e6-366">Es ist unwahrscheinlich, dass Sie Skripts finden können, die Sie ganz einfach entfernen können, aber möglicherweise finden Sie viele Skripts, die Sie während des Seitenlades nicht anfordern müssen, sondern möglicherweise asynchron angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="576e6-366">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--Navigate to [Using async or defer][async].  -->  
*   <span data-ttu-id="576e6-367">Wenn Sie ein Framework verwenden, überprüfen Sie, ob es über einen Produktionsmodus verfügt.</span><span class="sxs-lookup"><span data-stu-id="576e6-367">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="576e6-368">In diesem Modus kann [][WebpackTreeShaking] ein Feature wie z. B. das Baumschütteln verwendet werden, um unnötigen Code zu vermeiden, der das kritische Rendern blockiert.</span><span class="sxs-lookup"><span data-stu-id="576e6-368">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a><span data-ttu-id="576e6-369">Weniger Hauptthreadarbeit</span><span class="sxs-lookup"><span data-stu-id="576e6-369">Do less main thread work</span></span>  

<span data-ttu-id="576e6-370">Ihr aktueller Bericht zeigt einige geringfügige potenzielle Einsparungen im Abschnitt Verkaufschancen, aber wenn Sie im Abschnitt Diagnose nach unten schauen, sieht es so aus, als ob der größte Engpass zu viel Hauptthreadaktivität ist.</span><span class="sxs-lookup"><span data-stu-id="576e6-370">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="576e6-371">Der Hauptthread ist der Ort, an dem der Browser die meiste Arbeit zum Anzeigen einer Seite vor sich hat, z. B. die Analyse und Ausführung von HTML, CSS und JavaScript.</span><span class="sxs-lookup"><span data-stu-id="576e6-371">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="576e6-372">Das Ziel besteht in der Verwendung des Leistungsbereichs, um zu analysieren, welche Arbeit der Hauptthread während des Ladens der Seite macht, und Möglichkeiten zum Zurück- oder Entfernen unnötiger Arbeit zu finden.</span><span class="sxs-lookup"><span data-stu-id="576e6-372">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="576e6-373">Wählen Sie das **Tool Leistung** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-373">Choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="576e6-374">Wählen **Sie Aufnahmeeinstellungen** \( ![ Aufnahmeeinstellungen ](../media/capture-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="576e6-374">Choose **Capture Settings** \(![Capture Settings](../media/capture-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="576e6-375">Legen **Sie Netzwerk** auf **Langsame 3G** und CPU **auf** **6x Verlangsamung.**</span><span class="sxs-lookup"><span data-stu-id="576e6-375">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="576e6-376">Mobile Geräte haben in der Regel mehr Hardwareeinschränkungen als Laptops oder Desktops. Mit diesen Einstellungen können Sie die Seitenlast so erleben, als würden Sie ein weniger leistungsfähiges Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="576e6-376">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="576e6-377">Wählen **Sie Aktualisieren** \( Aktualisieren ![ ](../media/reload-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="576e6-377">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\).</span></span>  <span data-ttu-id="576e6-378">DevTools aktualisiert die Seite und erstellt dann eine Visualisierung aller Ausgeführten, um die Seite zu laden.</span><span class="sxs-lookup"><span data-stu-id="576e6-378">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="576e6-379">Diese Visualisierung wird als Ablaufverfolgung **bezeichnet.**</span><span class="sxs-lookup"><span data-stu-id="576e6-379">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Die Ablaufverfolgung des Leistungstools für die Seitenlast" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="576e6-381">Die **Ablaufverfolgung** des Leistungstools für die Seitenlast</span><span class="sxs-lookup"><span data-stu-id="576e6-381">The **Performance** tool trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="576e6-382">Die Ablaufverfolgung zeigt die Aktivität chronologisch von links nach rechts an.</span><span class="sxs-lookup"><span data-stu-id="576e6-382">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="576e6-383">Die FpS-, CPU- und #A0 oben bieten Ihnen eine Übersicht über Frames pro Sekunde, #A1 und Netzwerkaktivität.</span><span class="sxs-lookup"><span data-stu-id="576e6-383">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="576e6-384">Der gelbe Block, der in der Abbildung nach dem nächsten hervorgehoben ist, war die CPU vollständig mit Skriptaktivität beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="576e6-384">The block of yellow highlighted in the figure after the next, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="576e6-385">Dies ist ein Hinweis darauf, dass Sie möglicherweise die Seitenlast beschleunigen können, indem Sie weniger JavaScript-Arbeit tun.</span><span class="sxs-lookup"><span data-stu-id="576e6-385">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Der Abschnitt Übersicht der Ablaufverfolgung" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="576e6-387">Der Abschnitt Übersicht der Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="576e6-387">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="576e6-388">Untersuchen Sie die Ablaufverfolgung, um Möglichkeiten für weniger JavaScript-Arbeit zu finden:</span><span class="sxs-lookup"><span data-stu-id="576e6-388">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="576e6-389">Wählen Sie den **Abschnitt Timings** aus, um ihn zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="576e6-389">Choose the **Timings** section to expand it.</span></span>  <span data-ttu-id="576e6-390">Basierend auf der Tatsache, dass es eine Reihe von [Timings-Maßnahmen][MDNUserTimingApi] von React gibt, scheint es, als würde Tonys App den Entwicklungsmodus von React verwenden.</span><span class="sxs-lookup"><span data-stu-id="576e6-390">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="576e6-391">Der Wechsel in den Produktionsmodus von React kann zu einfachen Leistungsgewinnen führen.</span><span class="sxs-lookup"><span data-stu-id="576e6-391">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Der Abschnitt Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="576e6-393">Der **Abschnitt Timings**</span><span class="sxs-lookup"><span data-stu-id="576e6-393">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-394">Wählen **Sie Timings** erneut aus, um diesen Abschnitt zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="576e6-394">Choose **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="576e6-395">Durchsuchen Sie **den Abschnitt Main.**</span><span class="sxs-lookup"><span data-stu-id="576e6-395">Browse the **Main** section.</span></span>  <span data-ttu-id="576e6-396">Dieser Abschnitt zeigt ein chronologisches Protokoll der Hauptthreadaktivität von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="576e6-396">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="576e6-397">Die y-Achse (oben nach unten) zeigt, warum Ereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="576e6-397">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="576e6-398">Beispielsweise führte das Ereignis im Feigenblatt nach dem folgenden Ereignis dazu, dass die Funktion ausgeführt wurde, was zur Ausführung führte, was dazu führte, dass sie ausgeführt `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` wurde, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="576e6-398">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Der Abschnitt "Main"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="576e6-400">Der **Abschnitt "Main"**</span><span class="sxs-lookup"><span data-stu-id="576e6-400">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="576e6-401">Scrollen Sie nach unten im **Abschnitt Main.**</span><span class="sxs-lookup"><span data-stu-id="576e6-401">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="576e6-402">Wenn Sie ein Framework verwenden, wird der Großteil der oberen Aktivität durch das Framework verursacht, das in der Regel nicht in Ihrem Steuerelement liegt.</span><span class="sxs-lookup"><span data-stu-id="576e6-402">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="576e6-403">Die von Ihrer App verursachte Aktivität befindet sich in der Regel unten.</span><span class="sxs-lookup"><span data-stu-id="576e6-403">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="576e6-404">In dieser App scheint eine Funktion namens viele Anforderungen an `App` eine Funktion zu `mineBitcoin` verursachen.</span><span class="sxs-lookup"><span data-stu-id="576e6-404">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="576e6-405">Es klingt, als würde Tony die Geräte seiner Fans zum Minen von Kryptowährung verwenden...</span><span class="sxs-lookup"><span data-stu-id="576e6-405">It sounds like Tony may be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Zeigen auf die mineBitcoin-Aktivität" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="576e6-407">Zeigen auf die `mineBitcoin` Aktivität</span><span class="sxs-lookup"><span data-stu-id="576e6-407">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="576e6-408">Obwohl die Anforderungen, die Ihr Framework stellt, in der Regel nicht in Ihrem Steuerelement sind, können Sie Ihre App manchmal so strukturieren, dass das Framework ineffizient ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-408">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="576e6-409">Die Umstrukturierung Ihrer App zur effizienten Verwendung des Frameworks ist eine Möglichkeit, weniger Hauptthreadarbeit zu leisten.</span><span class="sxs-lookup"><span data-stu-id="576e6-409">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="576e6-410">Dies erfordert jedoch ein tiefes Verständnis der Funktionsweise Ihres Frameworks und der Art von Änderungen, die Sie in Ihrem eigenen Code vornehmen, um das Framework effizienter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="576e6-410">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="576e6-411">Erweitern Sie **den Abschnitt Bottom-Up.**</span><span class="sxs-lookup"><span data-stu-id="576e6-411">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="576e6-412">Diese Registerkarte bricht auf, welche Aktivitäten die meiste Zeit in Sich nahmen.</span><span class="sxs-lookup"><span data-stu-id="576e6-412">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="576e6-413">Wenn im Abschnitt "Bottom-Up" nichts angezeigt wird, wählen Sie die Bezeichnung für **den Abschnitt "Main"** aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-413">If nothing is displayed in the Bottom-Up section, choose the label for **Main** section.</span></span>  <span data-ttu-id="576e6-414">Im **Abschnitt Bottom-Up** werden nur Informationen zu den derzeit ausgewählten Aktivitäten oder Gruppen von Aktivitäten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="576e6-414">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="576e6-415">Wenn Sie beispielsweise eine der Aktivitäten ausgewählt haben, zeigt der `mineBitcoin` **Abschnitt Bottom-Up** nur Informationen für diese eine Aktivität an.</span><span class="sxs-lookup"><span data-stu-id="576e6-415">For example, if you chose one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Registerkarte Bottom-Up" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="576e6-417">Registerkarte **Unten nach** oben</span><span class="sxs-lookup"><span data-stu-id="576e6-417">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="576e6-418">In **der Spalte** Self Time wird angezeigt, wie viel Zeit direkt in jeder Aktivität verbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="576e6-418">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="576e6-419">In der folgenden Abbildung wurden beispielsweise ca. 63 % der Hauptthreadzeit für die Funktion `mineBitcoin` verwendet.</span><span class="sxs-lookup"><span data-stu-id="576e6-419">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="576e6-420">Zeit, um zu überprüfen, ob die Verwendung des Produktionsmodus und die Reduzierung der JavaScript-Aktivität die Seitenlast beschleunigen kann.</span><span class="sxs-lookup"><span data-stu-id="576e6-420">Time to review whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="576e6-421">Beginnen Sie mit dem Produktionsmodus:</span><span class="sxs-lookup"><span data-stu-id="576e6-421">Start with production mode:</span></span>  

1.  <span data-ttu-id="576e6-422">Öffnen Sie auf der Registerkarte Editor `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="576e6-422">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="576e6-423">Ändern Sie `"mode":"development"` in `"mode":"production"`.</span><span class="sxs-lookup"><span data-stu-id="576e6-423">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="576e6-424">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-424">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="576e6-425">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="576e6-425">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Konfiguration von Webpack für die Verwendung des Produktionsmodus" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="576e6-427">Ein Überwachungsbericht nach der Konfiguration von Webpack für die Verwendung des Produktionsmodus</span><span class="sxs-lookup"><span data-stu-id="576e6-427">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="576e6-428">Reduzieren Sie die JavaScript-Aktivität, indem Sie die Anforderung zu `mineBitcoin` entfernen:</span><span class="sxs-lookup"><span data-stu-id="576e6-428">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="576e6-429">Öffnen Sie auf der Registerkarte Editor `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="576e6-429">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="576e6-430">Kommentieren Sie die Anforderung `this.mineBitcoin(1500)` an in `constructor` aus.</span><span class="sxs-lookup"><span data-stu-id="576e6-430">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="576e6-431">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="576e6-431">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="576e6-432">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="576e6-432">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="576e6-434">Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit</span><span class="sxs-lookup"><span data-stu-id="576e6-434">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="576e6-435">Sieht so aus, als habe diese letzte Änderung einen enormen Leistungssprung verursacht!</span><span class="sxs-lookup"><span data-stu-id="576e6-435">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="576e6-436">Dieser Abschnitt bot eine ziemlich kurze Einführung in den Bereich "Leistung".</span><span class="sxs-lookup"><span data-stu-id="576e6-436">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="576e6-437">Weitere Informationen zum Analysieren der Seitenleistung finden Sie unter [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].</span><span class="sxs-lookup"><span data-stu-id="576e6-437">To learn more about how to analyze page performance, navigate to [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].</span></span>  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a><span data-ttu-id="576e6-438">Weniger Hauptthreadarbeit in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="576e6-438">Doing less main thread work in the real world</span></span>  

<span data-ttu-id="576e6-439">Im Allgemeinen ist das **Performance-Tool** die am häufigsten verwendeten Methoden, um zu verstehen, welche Aktivitäten Ihre Website beim Laden macht, und Wie Sie unnötige Aktivitäten entfernen können.</span><span class="sxs-lookup"><span data-stu-id="576e6-439">In general, the **Performance** tool is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="576e6-440">Wenn Sie einen Ansatz bevorzugen, der sich eher anfühlt, können Sie mit der `console.log()` [User Timing-API][MDNUserTimingApi] bestimmte Phasen ihres App-Lebenszyklus beliebig markieren, um nachverfolgt zu werden, wie lange jede dieser Phasen dauert.</span><span class="sxs-lookup"><span data-stu-id="576e6-440">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <a name="summary"></a><span data-ttu-id="576e6-441">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="576e6-441">Summary</span></span>  

*   <span data-ttu-id="576e6-442">Wenn Sie die Auslastungsleistung eines Standorts optimieren möchten, beginnen Sie immer mit einer Überwachung.</span><span class="sxs-lookup"><span data-stu-id="576e6-442">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="576e6-443">Die Überwachung legt eine Basislinie fest und gibt Ihnen Tipps zur Verbesserung.</span><span class="sxs-lookup"><span data-stu-id="576e6-443">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="576e6-444">Nehmen Sie jeweils eine Änderung vor, und überwachen Sie die Webseite nach jeder Änderung, um anzuzeigen, wie sich diese isolierte Änderung auf die Leistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="576e6-444">Make one change at a time, and audit the webpage after each change in order to display how that isolated change affects performance.</span></span>  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="576e6-445">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="576e6-445">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Leistungsanalysereferenz | Microsoft Docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Einführung in web development class | Coursera"  

[EssentialImageOptimization]: https://images.guide "Wesentliche Bildoptimierung"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Direktiven – Inhaltscodierungsrichtlinien | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Benutzer-Timing-API-| MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Baumschütteln | webpack"  

> [!NOTE]
> <span data-ttu-id="576e6-452">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="576e6-452">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="576e6-453">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="576e6-453">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="576e6-455">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="576e6-455">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
