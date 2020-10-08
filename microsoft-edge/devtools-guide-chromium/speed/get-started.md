---
description: Erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um Wege zu finden, wie Sie Ihre Websites schneller laden können.
title: Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: dafcb9c4d1194239baed7507e505d74d2b4ce1c8
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993440"
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





# <span data-ttu-id="d02f9-104">Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="d02f9-104">Optimize website speed with Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="d02f9-105">Ziel des Lernprogramms</span><span class="sxs-lookup"><span data-stu-id="d02f9-105">Goal of tutorial</span></span>  

<span data-ttu-id="d02f9-106">In diesem Lernprogramm erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um Wege zu finden, wie Sie Ihre Websites schneller laden können.</span><span class="sxs-lookup"><span data-stu-id="d02f9-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="d02f9-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d02f9-107">Prerequisites</span></span>  

*   <span data-ttu-id="d02f9-108">Sie sollten über grundlegende Webentwicklungsfunktionen verfügen, ähnlich wie in dieser [Einführung in die Webentwicklungs Klasse][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="d02f9-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="d02f9-109">Sie müssen nichts über die Ladeleistung wissen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="d02f9-110">In diesem Lernprogramm erfahren Sie mehr darüber!</span><span class="sxs-lookup"><span data-stu-id="d02f9-110">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="d02f9-111">Einführung</span><span class="sxs-lookup"><span data-stu-id="d02f9-111">Introduction</span></span>   

<span data-ttu-id="d02f9-112">Das ist Tony.</span><span class="sxs-lookup"><span data-stu-id="d02f9-112">This is Tony.</span></span>  <span data-ttu-id="d02f9-113">Tony ist in der Cat Society sehr bekannt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="d02f9-114">Er hat eine Website entwickelt, damit seine Fans mehr über seine bevorzugten Lebensmittel erfahren können.</span><span class="sxs-lookup"><span data-stu-id="d02f9-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="d02f9-115">Seine Fans lieben die Website, aber Tony hört immer wieder Beschwerden, dass die Website langsam geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="d02f9-116">Tony hat Sie gebeten, ihm beim Beschleunigen der Website zu helfen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="d02f9-118">Tony the Cat</span><span class="sxs-lookup"><span data-stu-id="d02f9-118">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="d02f9-119">Schritt 1: Überwachen der Website</span><span class="sxs-lookup"><span data-stu-id="d02f9-119">Step 1: Audit the site</span></span>   

<span data-ttu-id="d02f9-120">Wenn Sie die Ladeleistung einer Website verbessern möchten, **beginnen Sie immer mit einer Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="d02f9-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="d02f9-121">Das Audit hat zwei wichtige Funktionen:</span><span class="sxs-lookup"><span data-stu-id="d02f9-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="d02f9-122">Sie erstellt einen **Basisplan** , in dem Sie nachfolgende Änderungen messen können.</span><span class="sxs-lookup"><span data-stu-id="d02f9-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="d02f9-123">Es gibt Ihnen **umsetzbare Tipps** , welche Änderungen die meisten Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="d02f9-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="d02f9-124">Einrichtung</span><span class="sxs-lookup"><span data-stu-id="d02f9-124">Set up</span></span>   

<span data-ttu-id="d02f9-125">Zunächst müssen Sie die Website so einrichten, dass Sie später Änderungen daran vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="d02f9-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="d02f9-126">[Öffnen Sie den Quellcode für die Website](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="d02f9-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="d02f9-127">Diese Registerkarte wird als **Registerkarte "Editor"** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d02f9-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="d02f9-129">Die **Registerkarte "Editor"**</span><span class="sxs-lookup"><span data-stu-id="d02f9-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-130">Wählen Sie **Tony**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-130">Select **tony**.</span></span>  <span data-ttu-id="d02f9-131">Ein Menü wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="d02f9-133">Das Menü, das nach dem Klicken auf " **Tony** " angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="d02f9-133">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-134">Wählen Sie **Remix Project**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-134">Select **Remix Project**.</span></span>  <span data-ttu-id="d02f9-135">Der Name des Projekts wechselt von **Tony** zu einem zufällig generierten Namen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="d02f9-136">Sie haben jetzt eine eigene bearbeitbare Kopie des Codes.</span><span class="sxs-lookup"><span data-stu-id="d02f9-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="d02f9-137">Später können Sie Änderungen an diesem Code vornehmen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="d02f9-138">Wählen Sie **in einem neuen Fenster** **anzeigen** und auswählen aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-138">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="d02f9-139">Die Demo wird in einer neuen Registerkarte geöffnet.  Diese Registerkarte wird als **Registerkarte Demo**bezeichnet.  Das Laden der Website kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="d02f9-141">Die Registerkarte "Demo"</span><span class="sxs-lookup"><span data-stu-id="d02f9-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-142">Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="d02f9-142">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="d02f9-143">Microsoft Edge devtools wird parallel zur Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d02f9-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="d02f9-145">DevTools und die Demo</span><span class="sxs-lookup"><span data-stu-id="d02f9-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d02f9-146">Für die restlichen Screenshots in diesem Lernprogramm wird devtools in einem separaten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="d02f9-147">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, einzugeben `Undock` , und wählen Sie dann **in separates Fenster Abdocken**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-147">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="d02f9-149">Nicht angedockte devtools</span><span class="sxs-lookup"><span data-stu-id="d02f9-149">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="d02f9-150">Festlegen eines Basisplans</span><span class="sxs-lookup"><span data-stu-id="d02f9-150">Establish a baseline</span></span>   

<span data-ttu-id="d02f9-151">Der Basisplan ist eine Aufzeichnung der Vorgehensweise der Website, bevor Sie Leistungsverbesserungen durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="d02f9-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="d02f9-152">Wählen Sie die Registerkarte **Audits** aus.  Sie ist möglicherweise hinter der Schaltfläche " **Weitere Panels** \ ![ ][ImageMorePanelsIcon] " verborgen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-152">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="d02f9-153">Auf diesem Panel befindet sich ein Leuchtturm, weil das Projekt, das das Audit Panel anbietet, den Namen **Lighthouse**trägt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-153">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="d02f9-155">**Überwachungs** Panel</span><span class="sxs-lookup"><span data-stu-id="d02f9-155">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="d02f9-156">Vergleichen Sie Ihre Überwachungs Konfigurationseinstellungen mit denen in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="d02f9-156">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="d02f9-157">Nachfolgend finden Sie eine Erläuterung der verschiedenen Optionen:</span><span class="sxs-lookup"><span data-stu-id="d02f9-157">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="d02f9-158">**Gerät**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-158">**Device**.</span></span>  <span data-ttu-id="d02f9-159">Wenn Sie auf **Mobile** festlegen, ändert sich die Zeichenfolge des Benutzer-Agents und simuliert ein mobiles Viewport.</span><span class="sxs-lookup"><span data-stu-id="d02f9-159">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="d02f9-160">Durch die Einstellung auf den **Desktop** werden die **mobilen** Änderungen so ziemlich deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d02f9-160">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="d02f9-161">**Audits**.</span><span class="sxs-lookup"><span data-stu-id="d02f9-161">**Audits**.</span></span>  <span data-ttu-id="d02f9-162">Durch das Deaktivieren einer Kategorie wird verhindert, dass der Überwachungsbereich diese Audits ausführt, und diese Audits werden aus dem Bericht ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-162">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="d02f9-163">Lassen Sie die anderen Kategorien aktiviert, wenn Sie die Typen von Empfehlungen anzeigen möchten, die bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-163">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="d02f9-164">Das Deaktivieren von Kategorien beschleunigt den Überwachungsvorgang etwas.</span><span class="sxs-lookup"><span data-stu-id="d02f9-164">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="d02f9-165">**Einschränkung**.</span><span class="sxs-lookup"><span data-stu-id="d02f9-165">**Throttling**.</span></span>  <span data-ttu-id="d02f9-166">Einstellung auf **simulierte langsame 4G, vierfache CPU-Verlangsamung** simuliert die typischen Bedingungen für das Browsen auf einem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="d02f9-166">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="d02f9-167">Sie wird als "simuliert" bezeichnet, da das Überwachungs Panel während des Überwachungsprozesses nicht tatsächlich gedrosselt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-167">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="d02f9-168">Stattdessen wird nur extrapoliert, wie lange es dauert, bis die Seite unter mobilen Bedingungen geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="d02f9-168">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="d02f9-169">Mit der Einstellung " **angewendet...** " wird dagegen Ihre CPU und Ihr Netzwerk tatsächlich gedrosselt, mit dem Kompromiss eines längeren Überwachungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="d02f9-169">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="d02f9-170">**Speicher löschen**.</span><span class="sxs-lookup"><span data-stu-id="d02f9-170">**Clear Storage**.</span></span>  <span data-ttu-id="d02f9-171">Wenn Sie dieses Kontrollkästchen aktivieren, wird vor jeder Überwachung der gesamte Speicherplatz gelöscht, der der Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d02f9-171">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="d02f9-172">Belasse diese Einstellung, wenn Sie überprüfen möchten, wie die Besucher Ihrer Website erst einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="d02f9-172">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="d02f9-173">Deaktivieren Sie diese Einstellung, wenn Sie die Wiederholungs Besuchs Erfahrung wünschen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-173">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="d02f9-174">Wählen Sie **Audits ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-174">Select **Run Audits**.</span></span>  <span data-ttu-id="d02f9-175">Nach 10 bis 30 Sekunden wird im Überwachungs Panel ein Bericht über die Leistung der Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-175">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="d02f9-177">Der Bericht für das Audits-Panel über die Leistung der Website</span><span class="sxs-lookup"><span data-stu-id="d02f9-177">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="d02f9-178">Behandeln von Berichts Fehlern</span><span class="sxs-lookup"><span data-stu-id="d02f9-178">Handling report errors</span></span>   

<span data-ttu-id="d02f9-179">Wenn Sie in Ihrem Audits-Panel-Bericht jemals eine Fehlermeldung erhalten, versuchen Sie, die Registerkarte Demo in einem **InPrivate** -Fenster auszuführen, ohne dass weitere Registerkarten geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="d02f9-179">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="d02f9-180">Dadurch wird sichergestellt, dass Sie Microsoft Edge in einem sauberen Zustand ausführen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-180">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="d02f9-181">Insbesondere Microsoft-Edge-Erweiterungen stören häufig den Überwachungsprozess.</span><span class="sxs-lookup"><span data-stu-id="d02f9-181">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="d02f9-182">Grundlegendes zu Ihrem Bericht</span><span class="sxs-lookup"><span data-stu-id="d02f9-182">Understand your report</span></span>   

<span data-ttu-id="d02f9-183">Die Zahl am oberen Rand des Berichts entspricht dem Gesamtleistungsfaktor für die Website.</span><span class="sxs-lookup"><span data-stu-id="d02f9-183">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="d02f9-184">Wenn Sie später Änderungen am Code vornehmen, sollte diese Zahl steigen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-184">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="d02f9-185">Eine höhere Punktzahl bedeutet eine bessere Leistung.</span><span class="sxs-lookup"><span data-stu-id="d02f9-185">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="d02f9-187">Der Gesamtleistungsfaktor</span><span class="sxs-lookup"><span data-stu-id="d02f9-187">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-188">Der Abschnitt **Metriken** bietet quantitative Maße für die Leistung der Website.</span><span class="sxs-lookup"><span data-stu-id="d02f9-188">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="d02f9-189">Jede Metrik bietet Einblicke in einen anderen Aspekt der Leistung.</span><span class="sxs-lookup"><span data-stu-id="d02f9-189">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="d02f9-190">Beispielsweise erfahren Sie in der **ersten Inhaltsfarbe** , wann Inhalte zuerst auf dem Bildschirm gemalt werden, was ein wichtiger Meilenstein für die Wahrnehmung der Seitenauslastung durch den Benutzer ist, während die **Zeit für interaktive** Kennzeichnung den Punkt angibt, an dem die Seite für die Behandlung von Benutzerinteraktionen bereit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-190">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="d02f9-192">Abschnitt " **Metriken** "</span><span class="sxs-lookup"><span data-stu-id="d02f9-192">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-193">Wählen Sie die hervorgehobene Umschaltfläche in der folgenden Abbildung aus, um eine Beschreibung für jede Metrik anzuzeigen, und klicken Sie auf **Weitere Informationen** , um die Dokumentation dazu zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-193">Select the highlighted toggle button in the following figure to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="d02f9-195">Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der Metriken Elemente</span><span class="sxs-lookup"><span data-stu-id="d02f9-195">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-196">Unter Metriken finden Sie eine Sammlung von Screenshots, die Ihnen zeigen, wie die Seite beim Laden aussah.</span><span class="sxs-lookup"><span data-stu-id="d02f9-196">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="d02f9-198">Screenshots, wie die Seite beim Laden aussah</span><span class="sxs-lookup"><span data-stu-id="d02f9-198">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-199">Im Abschnitt " **Verkaufschancen** " finden Sie spezielle Tipps zum Verbessern der Auslastungs Leistung dieser bestimmten Seite.</span><span class="sxs-lookup"><span data-stu-id="d02f9-199">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="d02f9-201">Der Abschnitt " **Verkaufschancen** "</span><span class="sxs-lookup"><span data-stu-id="d02f9-201">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-202">Wählen Sie eine Gelegenheit aus, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="d02f9-202">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="d02f9-204">**Eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d02f9-204">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-205">Wählen Sie **Weitere Informationen** aus, um die Dokumentation dazu anzuzeigen, warum eine Verkaufschance wichtig ist, und spezifische Empfehlungen zur Behebung.</span><span class="sxs-lookup"><span data-stu-id="d02f9-205">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="d02f9-207">Dokumentation für die Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d02f9-207">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-208">Der Abschnitt **Diagnostics** enthält weitere Informationen zu Faktoren, die zur Ladezeit der Seite beitragen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-208">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="d02f9-210">Abschnitt " **Diagnose** "</span><span class="sxs-lookup"><span data-stu-id="d02f9-210">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-211">Im Abschnitt "übertragene **Prüfungen** " wird gezeigt, was die Website richtig macht.</span><span class="sxs-lookup"><span data-stu-id="d02f9-211">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="d02f9-212">Wählen Sie diese Option aus, um den Abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-212">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="d02f9-214">Abschnitt " **übergebene Überprüfungen** "</span><span class="sxs-lookup"><span data-stu-id="d02f9-214">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="d02f9-215">Schritt 2: experimentieren</span><span class="sxs-lookup"><span data-stu-id="d02f9-215">Step 2: Experiment</span></span>   

<span data-ttu-id="d02f9-216">Im Abschnitt "Verkaufschancen" Ihres Überwachungsberichts erhalten Sie Tipps, wie Sie die Leistung der Seite verbessern können.</span><span class="sxs-lookup"><span data-stu-id="d02f9-216">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="d02f9-217">In diesem Abschnitt implementieren Sie die empfohlenen Änderungen an der CodeBase, indem Sie die Website nach jeder Änderung überwachen, um zu messen, wie sich dies auf die Geschwindigkeit der Website auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-217">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="d02f9-218">Aktivieren der Text Komprimierung</span><span class="sxs-lookup"><span data-stu-id="d02f9-218">Enable text compression</span></span>   

<span data-ttu-id="d02f9-219">Ihr Bericht besagt, dass die Vermeidung von enormen Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-219">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="d02f9-220">Das Aktivieren der Text Komprimierung bietet die Möglichkeit, die Leistung der Seite zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-220">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="d02f9-221">Die Text Komprimierung erfolgt, wenn Sie die Größe einer Textdatei reduzieren oder komprimieren, bevor Sie Sie über das Netzwerk senden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-221">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="d02f9-222">Eine Art gefällt Ihnen, wie Sie einen Ordner komprimieren können, bevor Sie ihn per e-Mail senden, um die Größe zu verringern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-222">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="d02f9-223">Bevor Sie die Komprimierung aktivieren, gibt es eine Reihe von Möglichkeiten, um manuell zu überprüfen, ob Textressourcen komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-223">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="d02f9-224">Wählen Sie die Registerkarte **Netzwerk** aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-224">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="d02f9-226">**Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="d02f9-226">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-227">Wählen Sie das Symbol **Netzwerkeinstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-227">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="d02f9-228">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** .</span><span class="sxs-lookup"><span data-stu-id="d02f9-228">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="d02f9-229">Die Höhe der Zeilen in der Tabelle der Netzwerkanforderungen nimmt zu.</span><span class="sxs-lookup"><span data-stu-id="d02f9-229">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="d02f9-231">Große Zeilen in der Tabelle "Netzwerkanforderungen"</span><span class="sxs-lookup"><span data-stu-id="d02f9-231">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-232">Wenn die Spalte **Größe** in der Tabelle der Netzwerkanforderungen nicht angezeigt wird, klicken Sie auf die Tabellenüberschrift, und wählen Sie dann **Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-232">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="d02f9-233">Jede **Größen** Zelle enthält zwei Werte.</span><span class="sxs-lookup"><span data-stu-id="d02f9-233">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="d02f9-234">Der oberste Wert ist die Größe der heruntergeladenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="d02f9-234">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="d02f9-235">Der untere Wert gibt die Größe der unkomprimierten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d02f9-235">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="d02f9-236">Wenn die beiden Werte identisch sind, wird die Ressource nicht komprimiert, wenn Sie über das Netzwerk gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-236">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="d02f9-237">In der vorhergehenden Abbildung sind die oberen und unteren Werte für " `bundle.js` sind" `1.2 MB` und " `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-237">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="d02f9-238">Überprüfen Sie auf Komprimierung, indem Sie die HTTP-Header einer Ressource prüfen:</span><span class="sxs-lookup"><span data-stu-id="d02f9-238">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="d02f9-239">Wählen Sie **bundle.js**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-239">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="d02f9-240">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-240">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="d02f9-242">Die Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="d02f9-242">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-243">Durchsuchen Sie den Abschnitt **Antwort Kopfzeilen** nach einer `content-encoding` Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="d02f9-243">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="d02f9-244">Sie sollten keines sehen, was bedeutet, dass es sich nicht um eine `bundle.js` Komprimierung handelt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-244">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="d02f9-245">Wenn eine Ressource komprimiert ist, wird in der Regel dieser Header auf `gzip` , `deflate` oder gesetzt `br` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-245">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="d02f9-246">Eine Erläuterung dieser Werte finden Sie unter [Direktiven][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="d02f9-246">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="d02f9-247">Genug mit den Erläuterungen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-247">Enough with the explanations.</span></span>  <span data-ttu-id="d02f9-248">Zeit, einige Änderungen vorzunehmen!</span><span class="sxs-lookup"><span data-stu-id="d02f9-248">Time to make some changes!</span></span>  <span data-ttu-id="d02f9-249">Aktivieren Sie die Text Komprimierung, indem Sie ein paar Codezeilen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="d02f9-249">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="d02f9-250">Klicken Sie auf der Registerkarte Editor auf **server.js**.</span><span class="sxs-lookup"><span data-stu-id="d02f9-250">In the editor tab, click **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="d02f9-252">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="d02f9-252">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-253">Fügen Sie **server.js**den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="d02f9-253">Add the following code to **server.js**.</span></span>  <span data-ttu-id="d02f9-254">Stellen Sie sicher, dass Sie dies tun `app.use(compression())` `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-254">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="d02f9-255">In der Regel müssen Sie das `compression` Paket über einen ähnlichen `npm i -S compression` Vorgang installieren, dies wurde aber bereits für Sie erledigt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-255">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="d02f9-256">Warten Sie, bis glitch den neuen Build der Website bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="d02f9-256">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="d02f9-257">Die raffinierte Animation neben **Tools** bedeutet, dass die Website neu erstellt und erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-257">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="d02f9-258">Die Änderung ist fertig, wenn die Animation neben **Tools** verschwindet.</span><span class="sxs-lookup"><span data-stu-id="d02f9-258">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="d02f9-259">Wählen Sie wieder **in einem neuen Fenster** **anzeigen** und auswählen aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-259">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="d02f9-260">Verwenden Sie die zuvor gelernten Workflows, um manuell zu überprüfen, ob die Komprimierung funktioniert:</span><span class="sxs-lookup"><span data-stu-id="d02f9-260">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="d02f9-261">Wechseln Sie zur Registerkarte Demo zurück, und laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="d02f9-261">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="d02f9-262">In der Spalte **Größe** sollten nun zwei unterschiedliche Werte für Textressourcen wie angezeigt werden `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-262">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="d02f9-263">In der folgenden Abbildung ist der oberste Wert von für die `256 KB` Größe der Datei, die `bundle.js` über das Netzwerk gesendet wurde, und der untere Wert von `1.2 MB` ist die unkomprimierte Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="d02f9-263">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="d02f9-265">In der Spalte " **Größe** " werden nun zwei unterschiedliche Werte für Textressourcen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-265">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-266">Im Abschnitt " **Antwort Kopfzeilen** " `bundle.js` sollte nun eine `content-encoding: gzip` Kopfzeile enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="d02f9-266">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="d02f9-268">Der Abschnitt " **Antwort Kopfzeilen** " enthält jetzt einen Inhalts Codierungs Header.</span><span class="sxs-lookup"><span data-stu-id="d02f9-268">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d02f9-269">Überwachen Sie die Seite erneut, um zu messen, welche Art von Auswirkungen die Text Komprimierung auf die Ladeleistung der Seite hat:</span><span class="sxs-lookup"><span data-stu-id="d02f9-269">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="d02f9-270">Wählen Sie die Registerkarte **Audits** aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-270">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="d02f9-271">Wählen Sie **Audit durchführen** \ ( ![ Audit durchführen ][ImagePerformIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-271">Select **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="d02f9-272">Belasse die Einstellungen wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="d02f9-272">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="d02f9-273">Wählen Sie **Audit ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-273">Select **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="d02f9-275">Ein Überwachungsbericht nach der Aktivierung der Text Komprimierung</span><span class="sxs-lookup"><span data-stu-id="d02f9-275">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="d02f9-276">Ihr Gesamtleistungsfaktor sollte zugenommen haben, was bedeutet, dass die Website schneller wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-276">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="d02f9-277">Text Komprimierung in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="d02f9-277">Text compression in the real world</span></span>   

<span data-ttu-id="d02f9-278">Bei den meisten Servern gibt es wirklich einfache Fehlerbehebungen wie diese zum Aktivieren von Komprimierung!</span><span class="sxs-lookup"><span data-stu-id="d02f9-278">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="d02f9-279">Führen Sie einfach eine Suche durch, um zu konfigurieren, welcher Server zum Komprimieren von Text verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-279">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="d02f9-280">Ändern der Größe von Bildern</span><span class="sxs-lookup"><span data-stu-id="d02f9-280">Resize images</span></span>   

<span data-ttu-id="d02f9-281">Ihr Bericht weist darauf hin, dass die Vermeidung enormer Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-281">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="d02f9-282">Durch Ändern der Größe von Bildern kann die Größe der Netzwerk Nutzlast verringert werden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-282">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="d02f9-283">Wenn der Benutzer Ihre Bilder auf einem Bildschirm mit einem mobilen Gerät anzeigt, der 500 Pixel breit ist, ist es wirklich unwichtig, ein 1500-Pixel breites Bild zu senden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-283">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="d02f9-284">Im Idealfall senden Sie höchstens ein Bild mit einer Breite von 500 Pixel.</span><span class="sxs-lookup"><span data-stu-id="d02f9-284">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="d02f9-285">Klicken Sie in Ihrem Bericht auf **enorme Netzwerk Nutzlasten vermeiden** , um festzustellen, welche Bilder geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-285">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="d02f9-286">Es sieht so aus, als ob 2 der JPG-Dateien über 2000 KB liegen, was größer als notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="d02f9-286">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="d02f9-287">Zurück auf der Registerkarte "Editor" Öffnen `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-287">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="d02f9-288">Ersetzen Sie `const dir = 'big'` durch `const dir = 'small'`.</span><span class="sxs-lookup"><span data-stu-id="d02f9-288">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="d02f9-289">Dieses Verzeichnis enthält Kopien der gleichen Bilder, deren Größe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d02f9-289">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="d02f9-290">Überprüfen Sie die Seite erneut, um zu sehen, wie sich diese Änderung auf die Ladeleistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-290">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="d02f9-292">Ein Überwachungsbericht nach dem Ändern der Größe von Bildern</span><span class="sxs-lookup"><span data-stu-id="d02f9-292">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d02f9-293">Sieht so aus, als ob die Änderung nur eine geringfügige Auswirkung auf den Gesamtleistungsfaktor hat.</span><span class="sxs-lookup"><span data-stu-id="d02f9-293">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="d02f9-294">Die Punktzahl zeigt jedoch nicht eindeutig, wie viel Netzwerkdaten Sie für Ihre Benutzer speichern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-294">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="d02f9-295">Die Gesamtgröße der alten Fotos betrug etwa 5,3 Megabyte, während es jetzt nur noch etwa 0,18 Megabytes gibt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-295">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="d02f9-296">Ändern der Größe von Bildern in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="d02f9-296">Resizing images in the real world</span></span>   

<span data-ttu-id="d02f9-297">Bei einer kleinen app kann eine einmalige Größenänderung so gut wie möglich sein.</span><span class="sxs-lookup"><span data-stu-id="d02f9-297">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="d02f9-298">Bei einer umfangreichen APP ist dies natürlich nicht skalierbar.</span><span class="sxs-lookup"><span data-stu-id="d02f9-298">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="d02f9-299">Im folgenden finden Sie einige Strategien zum Verwalten von Bildern in umfangreichen apps:</span><span class="sxs-lookup"><span data-stu-id="d02f9-299">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="d02f9-300">Ändern der Größe von Bildern während des Buildprozesses</span><span class="sxs-lookup"><span data-stu-id="d02f9-300">Resize images during your build process.</span></span>  
*   <span data-ttu-id="d02f9-301">Erstellen Sie mehrere Größen der einzelnen Bilder während des Buildprozesses, und verwenden `srcset` Sie Sie dann in Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="d02f9-301">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="d02f9-302">Zur Laufzeit sorgt der Browser dafür, welche Größe für das Gerät am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d02f9-302">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="d02f9-303">Verwenden Sie ein Image CDN, mit dem Sie die Größe eines Bilds dynamisch ändern können, wenn Sie es anfordern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-303">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="d02f9-304">Optimieren Sie zumindest jedes Bild.</span><span class="sxs-lookup"><span data-stu-id="d02f9-304">At the very least, optimize each image.</span></span>  <span data-ttu-id="d02f9-305">Dies kann zu enormen Einsparungen führen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-305">This may create huge savings.</span></span>  
  <span data-ttu-id="d02f9-306">Optimierung ist, wenn Sie ein Bild über ein spezielles Programm ausführen, das die Größe der Bilddatei reduziert.</span><span class="sxs-lookup"><span data-stu-id="d02f9-306">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="d02f9-307">Weitere Tipps finden Sie unter [grundlegende Bildoptimierung][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="d02f9-307">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="d02f9-308">Eliminieren von Render-Blockierungs Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d02f9-308">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="d02f9-309">Ihr neuester Bericht besagt, dass das Eliminieren von Render-Blockierungs Ressourcen jetzt die größte Chance darstellt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-309">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="d02f9-310">Eine Render-Blockierungs Ressource ist eine externe JavaScript-oder CSS-Datei, die vom Browser heruntergeladen, analysiert und ausgeführt werden muss, bevor die Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-310">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="d02f9-311">Das Ziel besteht darin, nur den zentralen CSS-und JavaScript-Code auszuführen, der erforderlich ist, um die Seite ordnungsgemäß anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-311">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="d02f9-312">Die erste Aufgabe besteht darin, Code zu finden, den Sie beim Laden der Seite nicht ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-312">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="d02f9-313">Wählen Sie **Render-Blockierungs Ressourcen eliminieren** aus, um die blockierten Ressourcen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="d02f9-313">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="d02f9-314">und `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-314">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="d02f9-316">Weitere Informationen zur Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d02f9-316">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-317">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, mit der Eingabe zu beginnen `Coverage` , und wählen Sie dann **Coverage anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-317">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="d02f9-319">Öffnen des Befehlsmenüs im **Überwachungs** Panel</span><span class="sxs-lookup"><span data-stu-id="d02f9-319">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="d02f9-321">Die Registerkarte " **Coverage** "</span><span class="sxs-lookup"><span data-stu-id="d02f9-321">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-322">Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-322">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="d02f9-323">Die Registerkarte **Coverage** bietet eine Übersicht darüber, wie viel des Codes in `bundle.js` , `jquery.js` und `lodash.js` ausgeführt wird, während die Seite geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-323">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="d02f9-324">In der folgenden Abbildung werden etwa 76% und 30% der jQuery-und Lodash-Dateien nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d02f9-324">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="d02f9-326">Der Bericht "Berichterstattung"</span><span class="sxs-lookup"><span data-stu-id="d02f9-326">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-327">Wählen Sie die Zeile **jquery.js** aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-327">Select the **jquery.js** row.</span></span>  <span data-ttu-id="d02f9-328">DevTools öffnet die Datei im Quellen Panel.</span><span class="sxs-lookup"><span data-stu-id="d02f9-328">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="d02f9-329">Eine Codezeile wird ausgeführt, wenn Sie einen blauen Balken Daneben hat.</span><span class="sxs-lookup"><span data-stu-id="d02f9-329">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="d02f9-330">Eine rote Leiste bedeutet, dass Sie nicht ausgeführt wurde und beim Laden der Seite definitiv nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-330">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="d02f9-332">Anzeigen der jQuery-Datei im **Quellen** Panel</span><span class="sxs-lookup"><span data-stu-id="d02f9-332">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-333">Scrollen Sie ein wenig durch den jQuery-Code.</span><span class="sxs-lookup"><span data-stu-id="d02f9-333">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="d02f9-334">Einige der Zeilen, die "Run" erhalten, sind eigentlich nur Kommentare.</span><span class="sxs-lookup"><span data-stu-id="d02f9-334">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="d02f9-335">Wenn Sie diesen Code über einen minifier ausführen, der Kommentare entfernt, ist eine weitere Möglichkeit, die Größe dieser Datei zu verringern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-335">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="d02f9-336">Kurz gesagt: Wenn Sie mit Ihrem eigenen Code arbeiten, können Sie mithilfe der Registerkarte Coverage Ihren Code, Zeile für Zeile, analysieren und nur den Code versenden, der für die Seitenauslastung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-336">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="d02f9-337">Sind die `jquery.js` und `lodash.js` Dateien auch zum Laden der Seite erforderlich?</span><span class="sxs-lookup"><span data-stu-id="d02f9-337">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="d02f9-338">Auf der Registerkarte Anforderungs Blockierung wird angezeigt, was geschieht, wenn keine Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d02f9-338">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="d02f9-339">Wählen Sie die Registerkarte **Netzwerk** aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-339">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="d02f9-340">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-340">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="d02f9-341">Beginnen `blocking` Sie mit der Eingabe, und wählen Sie dann **Anforderungs Blockierung anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-341">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="d02f9-343">Die Registerkarte ' **Anforderungs Blockierung** '</span><span class="sxs-lookup"><span data-stu-id="d02f9-343">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-344">Wählen Sie **Muster hinzufügen** \ ( ![ Muster hinzufügen ][ImageAddPatternIcon] ) aus, geben Sie ein `/libs/*` , und drücken Sie dann `Enter` , um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-344">Select **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="d02f9-346">Hinzufügen eines Musters zum Blockieren einer Anforderung an das `libs` Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d02f9-346">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-347">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d02f9-347">Refresh the page.</span></span>  <span data-ttu-id="d02f9-348">Die Anforderungen für jQuery und Lodash sind rot, was bedeutet, dass die Anforderungen blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-348">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="d02f9-349">Da die Seite immer noch geladen und interaktiv ist, sieht es so aus, als ob diese Ressourcen überhaupt nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-349">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="d02f9-351">Das **Netzwerk** Panel zeigt, dass die Anforderungen blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-351">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-352">Wählen Sie **alle Muster entfernen** \ ( ![ alle Muster entfernen ][ImageRemoveIcon] \) aus, um das `/libs/*` Blockierungs Muster zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-352">Select **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="d02f9-353">Im Allgemeinen ist die Registerkarte Anforderungs Blockierung hilfreich, um zu simulieren, wie sich die Seite verhält, wenn eine bestimmte Ressource nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d02f9-353">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="d02f9-354">Entfernen Sie nun die Verweise auf diese Dateien aus dem Code, und überwachen Sie die Seite erneut:</span><span class="sxs-lookup"><span data-stu-id="d02f9-354">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="d02f9-355">Zurück auf der Registerkarte "Editor" Öffnen `template.html` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-355">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="d02f9-356">Löschen Sie `<script src="/libs/lodash.js">` und `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="d02f9-356">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="d02f9-357">Warten Sie, bis die Website neu erstellt und erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-357">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="d02f9-358">Überwachen Sie die Seite im **Überwachungs** Panel erneut.</span><span class="sxs-lookup"><span data-stu-id="d02f9-358">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="d02f9-359">Ihre Gesamtpunktzahl sollte erneut verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-359">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="d02f9-361">Ein **Überwachungs** Bericht nach dem Entfernen der Render-Blockierungs Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d02f9-361">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="d02f9-362">Optimieren des kritischen Rendering-Pfads in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="d02f9-362">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="d02f9-363">Der **kritische Rendering-Pfad** bezieht sich auf den Code, der zum Laden einer Seite erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d02f9-363">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="d02f9-364">Im Allgemeinen können Sie die Seitenauslastung beschleunigen, indem Sie nur den Versand von kritischem Code während des Ladens der Seite durchführen und dann alles andere verzögert laden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-364">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="d02f9-365">Es ist unwahrscheinlich, dass Sie in der Lage sind, Skripts zu finden, die Sie direkt entfernen können, aber möglicherweise viele Skripts finden, die Sie beim Laden der Seite nicht anfordern müssen, und stattdessen möglicherweise asynchron angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-365">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="d02f9-366">Wenn Sie ein Framework verwenden, überprüfen Sie, ob es einen Produktionsmodus aufweist.</span><span class="sxs-lookup"><span data-stu-id="d02f9-366">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="d02f9-367">In diesem Modus wird möglicherweise ein Feature wie das [schütteln von Strukturen][WebpackTreeShaking] verwendet, um unnötigen Code zu eliminieren, der das kritische Rendern blockiert.</span><span class="sxs-lookup"><span data-stu-id="d02f9-367">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="d02f9-368">Arbeiten mit einem geringeren Hauptthread</span><span class="sxs-lookup"><span data-stu-id="d02f9-368">Do less main thread work</span></span>   

<span data-ttu-id="d02f9-369">Ihr neuester Bericht zeigt einige kleinere potenzielle Einsparungen im Abschnitt "Verkaufschancen", aber wenn Sie im Abschnitt "Diagnose" nach unten suchen, sieht es so aus, als wäre der größte Engpass zu viel Hauptthread Aktivität.</span><span class="sxs-lookup"><span data-stu-id="d02f9-369">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="d02f9-370">Der Hauptthread ist der Ort, an dem der Browser die meiste Arbeit ausführt, die zum Anzeigen einer Seite erforderlich ist, beispielsweise das analysieren und Ausführen von HTML, CSS und JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d02f9-370">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="d02f9-371">Das Ziel besteht darin, mithilfe des Leistungs Panels zu analysieren, welche Arbeit der Hauptthread beim Laden der Seite unternimmt, und Wege zu finden, um unnötige Arbeit zu verzögern oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-371">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="d02f9-372">Wählen Sie die Registerkarte **Leistung** aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-372">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="d02f9-373">Wählen Sie **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-373">Select **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="d02f9-374">**Netzwerk** auf **langsame 3G** -und **CPU** -zu- **6x-Verlangsamung**einstellen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-374">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="d02f9-375">Bei mobilen Geräten gibt es in der Regel mehr Hardwareeinschränkungen als Laptops oder Desktops, sodass Sie mit diesen Einstellungen das Laden der Seite so erleben können, als ob Sie ein weniger leistungsfähiges Gerät verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-375">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="d02f9-376">Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="d02f9-376">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="d02f9-377">DevTools aktualisiert die Seite und erstellt dann eine Visualisierung aller ausgeführten Arbeiten, um die Seite zu laden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-377">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="d02f9-378">Diese Visualisierung wird als **Ablaufverfolgung**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d02f9-378">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="d02f9-380">Der **Leistungs** Panel-Ablaufverfolgung der Seitenauslastung</span><span class="sxs-lookup"><span data-stu-id="d02f9-380">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d02f9-381">Die Ablaufverfolgung zeigt die Aktivität chronologisch an, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="d02f9-381">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="d02f9-382">Die oben dargestellten fps-, CPU-und net-Diagramme geben Ihnen einen Überblick über Frames pro Sekunde, CPU-Aktivität und Netzwerkaktivität.</span><span class="sxs-lookup"><span data-stu-id="d02f9-382">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="d02f9-383">Der gelb markierte Block, der in der Abbildung nachfolgend angezeigt wird, war die CPU vollständig mit Skriptaktivitäten ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="d02f9-383">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="d02f9-384">Dies ist ein Hinweis darauf, dass Sie möglicherweise die Seitenauslastung beschleunigen können, indem Sie eine geringere JavaScript-Arbeit durchführen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-384">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="d02f9-386">Der Abschnitt "Übersicht" der Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="d02f9-386">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="d02f9-387">Untersuchen Sie die Ablaufverfolgung, um Möglichkeiten für eine geringere JavaScript-Arbeit zu finden:</span><span class="sxs-lookup"><span data-stu-id="d02f9-387">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="d02f9-388">Wählen Sie den Abschnitt **Anzeige** dauern aus, um ihn zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-388">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="d02f9-389">Basierend auf der Tatsache, dass es möglicherweise eine Reihe von [Timings][MDNUserTimingApi] -Maßnahmen von reagieren gibt, scheint es so zu sein, als ob die APP von Tony die Entwicklungsmethode von reagieren verwendet.</span><span class="sxs-lookup"><span data-stu-id="d02f9-389">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="d02f9-390">Wenn Sie auf den Produktionsmodus von reagieren umstellen, kann dies einige einfache Leistungsgewinne hervorbringen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-390">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="d02f9-392">Abschnitt " **Anzeige** dauern"</span><span class="sxs-lookup"><span data-stu-id="d02f9-392">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-393">Wählen Sie erneut **Anzeige** dauern aus, um den Abschnitt zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="d02f9-393">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="d02f9-394">Durchsuchen Sie den **Haupt** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-394">Browse the **Main** section.</span></span>  <span data-ttu-id="d02f9-395">Dieser Abschnitt zeigt ein chronologisches Protokoll der Hauptthread Aktivität, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="d02f9-395">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="d02f9-396">Die y-Achse (von oben nach unten) zeigt, warum Ereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="d02f9-396">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="d02f9-397">In der figyre nach dem folgenden Beispiel hat das Ereignis zum Ausführen der Funktion geführt, die zur Ausführung führte, die `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` zum Ausführen führte usw.</span><span class="sxs-lookup"><span data-stu-id="d02f9-397">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="d02f9-399">Der **Haupt** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d02f9-399">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d02f9-400">Scrollen Sie nach unten zum unteren Rand des **Haupt** Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="d02f9-400">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="d02f9-401">Wenn Sie ein Framework verwenden, wird der größte Teil der oberen Aktivität durch das Framework verursacht, das normalerweise außerhalb des Steuerelements liegt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-401">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="d02f9-402">Die von Ihrer APP verursachte Aktivität befindet sich normalerweise unten.</span><span class="sxs-lookup"><span data-stu-id="d02f9-402">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="d02f9-403">In dieser app scheint es so zu sein, dass eine Funktion mit dem Namen `App` viele Anforderungen an eine `mineBitcoin` Funktion verursacht.</span><span class="sxs-lookup"><span data-stu-id="d02f9-403">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="d02f9-404">Es klingt wie Tony könnte die Geräte seiner Fans verwenden, um cryptocurrency zu vergruben...</span><span class="sxs-lookup"><span data-stu-id="d02f9-404">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="d02f9-406">Zeigen Sie auf die `mineBitcoin` Aktivität.</span><span class="sxs-lookup"><span data-stu-id="d02f9-406">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="d02f9-407">Obwohl die Anforderungen, die Ihr Framework macht, in der Regel nicht in Ihrem Steuerelement enthalten sind, können Sie Ihre APP manchmal so strukturieren, dass das Framework ineffizient ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-407">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="d02f9-408">Die Umstrukturierung ihrer App zur effizienten Verwendung des Frameworks ist eine Möglichkeit, um die Arbeit am Hauptthread zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="d02f9-408">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="d02f9-409">Dies erfordert jedoch ein umfassendes Verständnis der Funktionsweise des Frameworks und der Art von Änderungen, die Sie in Ihrem eigenen Code vornehmen, um das Framework effizienter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-409">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="d02f9-410">Erweitern Sie den Abschnitt **Bottom-up** .</span><span class="sxs-lookup"><span data-stu-id="d02f9-410">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="d02f9-411">Auf dieser Registerkarte wird aufgeschlüsselt, welche Aktivitäten die meiste Zeit in Anspruch genommen haben.</span><span class="sxs-lookup"><span data-stu-id="d02f9-411">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="d02f9-412">Wenn im Abschnitt Bottom-up nichts angezeigt wird, klicken Sie auf die Beschriftung für **Haupt** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-412">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="d02f9-413">Der **Bottom-up-** Abschnitt zeigt nur Informationen zu einer beliebigen Aktivität oder Aktivitätsgruppe, die Sie aktuell ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d02f9-413">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="d02f9-414">Wenn Sie beispielsweise auf eine der Aktivitäten geklickt haben `mineBitcoin` , werden im Abschnitt **Bottom-up** nur Informationen für diese Aktivität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-414">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="d02f9-416">Die Registerkarte " **Bottom-up** "</span><span class="sxs-lookup"><span data-stu-id="d02f9-416">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d02f9-417">In der Spalte **selbst Zeit** wird angezeigt, wie viel Zeit direkt in den einzelnen Aktivitäten aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d02f9-417">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="d02f9-418">In der folgenden Abbildung wurden etwa 63% der Hauptthread Zeit für die Funktion aufgewendet `mineBitcoin` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-418">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="d02f9-419">Zeit, um zu sehen, ob die Auslastung der Seite durch Verwenden des Produktionsmodus und verringern der JavaScript-Aktivität beschleunigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d02f9-419">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="d02f9-420">Beginnen mit dem Produktionsmodus:</span><span class="sxs-lookup"><span data-stu-id="d02f9-420">Start with production mode:</span></span>  

1.  <span data-ttu-id="d02f9-421">Öffnen Sie auf der Registerkarte Editor den Reiter `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-421">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="d02f9-422">Ändern Sie `"mode":"development"` in `"mode":"production"`.</span><span class="sxs-lookup"><span data-stu-id="d02f9-422">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="d02f9-423">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-423">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="d02f9-424">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="d02f9-424">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="d02f9-426">Ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus</span><span class="sxs-lookup"><span data-stu-id="d02f9-426">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d02f9-427">Reduzieren Sie die JavaScript-Aktivität, indem Sie die Anforderung entfernen an `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="d02f9-427">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="d02f9-428">Öffnen Sie auf der Registerkarte Editor den Reiter `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-428">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="d02f9-429">Kommentieren Sie die Anforderung `this.mineBitcoin(1500)` in `constructor` .</span><span class="sxs-lookup"><span data-stu-id="d02f9-429">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="d02f9-430">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d02f9-430">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="d02f9-431">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="d02f9-431">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="d02f9-433">Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit</span><span class="sxs-lookup"><span data-stu-id="d02f9-433">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="d02f9-434">Sieht so aus, als ob diese letzte Änderung einen massiven Sprung in der Leistung verursacht hat!</span><span class="sxs-lookup"><span data-stu-id="d02f9-434">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="d02f9-435">Dieser Abschnitt enthält eine relativ kurze Einführung in das Leistungs Panel.</span><span class="sxs-lookup"><span data-stu-id="d02f9-435">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="d02f9-436">Weitere Informationen zum Analysieren der Seitenleistung finden Sie unter [Referenz zur Leistungsanalyse][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="d02f9-436">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="d02f9-437">Arbeiten mit einem niedrigeren Hauptthread in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="d02f9-437">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="d02f9-438">Im Allgemeinen ist der Bereich " **Leistung** " die häufigste Methode, um zu verstehen, welche Aktivitäten Ihre Website während der Auslastung durchführt, und Möglichkeiten zum Entfernen unnötiger Aktivitäten zu finden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-438">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="d02f9-439">Wenn Sie einen Ansatz bevorzugen, der sich eher wie anfühlt `console.log()` , können Sie mit der API für die [Benutzersteuerung][MDNUserTimingApi] bestimmte Phasen des App-Lebenszyklus willkürlich kennzeichnen, um zu verfolgen, wie lange diese Phasen dauern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-439">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="d02f9-440">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d02f9-440">Summary</span></span>   

*   <span data-ttu-id="d02f9-441">Wenn Sie die Auslastungs Leistung einer Website optimieren möchten, beginnen Sie immer mit einer Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d02f9-441">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="d02f9-442">Mit der Überprüfung wird ein Basisplan erstellt, und Sie erhalten Tipps zum verbessern.</span><span class="sxs-lookup"><span data-stu-id="d02f9-442">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="d02f9-443">Führen Sie jeweils eine Änderung durch, und überprüfen Sie die Seite nach jeder Änderung, um zu sehen, wie sich diese isolierte Änderung auf die Leistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-443">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referenz zur Leistungsanalyse | Microsoft docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Einführung in die Webentwicklungs Klasse | Coursera"  

[EssentialImageOptimization]: https://images.guide "Essentielle Bildoptimierung"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Direktiven – Inhaltscodierung | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Benutzer-Timing-API | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Baum Erschütterung | WebPack"  

> [!NOTE]
> <span data-ttu-id="d02f9-450">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d02f9-450">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d02f9-451">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d02f9-451">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="d02f9-453">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d02f9-453">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
