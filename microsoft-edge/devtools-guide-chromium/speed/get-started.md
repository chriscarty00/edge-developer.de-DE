---
title: Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 42b742316ccaa64aa35fc1d21c5277e448b2d5b7
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984670"
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





# <span data-ttu-id="aecfc-103">Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="aecfc-103">Optimize website speed with Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="aecfc-104">Ziel des Lernprogramms</span><span class="sxs-lookup"><span data-stu-id="aecfc-104">Goal of tutorial</span></span>  

<span data-ttu-id="aecfc-105">In diesem Lernprogramm erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um Wege zu finden, wie Sie Ihre Websites schneller laden können.</span><span class="sxs-lookup"><span data-stu-id="aecfc-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="aecfc-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="aecfc-106">Prerequisites</span></span>  

*   <span data-ttu-id="aecfc-107">Sie sollten über grundlegende Webentwicklungsfunktionen verfügen, ähnlich wie in dieser [Einführung in die Webentwicklungs Klasse][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="aecfc-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="aecfc-108">Sie müssen nichts über die Ladeleistung wissen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="aecfc-109">In diesem Lernprogramm erfahren Sie mehr darüber!</span><span class="sxs-lookup"><span data-stu-id="aecfc-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="aecfc-110">Einführung</span><span class="sxs-lookup"><span data-stu-id="aecfc-110">Introduction</span></span>   

<span data-ttu-id="aecfc-111">Das ist Tony.</span><span class="sxs-lookup"><span data-stu-id="aecfc-111">This is Tony.</span></span>  <span data-ttu-id="aecfc-112">Tony ist in der Cat Society sehr bekannt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="aecfc-113">Er hat eine Website entwickelt, damit seine Fans mehr über seine bevorzugten Lebensmittel erfahren können.</span><span class="sxs-lookup"><span data-stu-id="aecfc-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="aecfc-114">Seine Fans lieben die Website, aber Tony hört immer wieder Beschwerden, dass die Website langsam geladen wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="aecfc-115">Tony hat Sie gebeten, ihm beim Beschleunigen der Website zu helfen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-115">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony the Cat" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="aecfc-117">Tony the Cat</span><span class="sxs-lookup"><span data-stu-id="aecfc-117">Tony the cat</span></span>  
:::image-end:::  

## <span data-ttu-id="aecfc-118">Schritt 1: Überwachen der Website</span><span class="sxs-lookup"><span data-stu-id="aecfc-118">Step 1: Audit the site</span></span>   

<span data-ttu-id="aecfc-119">Wenn Sie die Ladeleistung einer Website verbessern möchten, **beginnen Sie immer mit einer Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="aecfc-119">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="aecfc-120">Das Audit hat zwei wichtige Funktionen:</span><span class="sxs-lookup"><span data-stu-id="aecfc-120">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="aecfc-121">Sie erstellt einen **Basisplan** , in dem Sie nachfolgende Änderungen messen können.</span><span class="sxs-lookup"><span data-stu-id="aecfc-121">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="aecfc-122">Es gibt Ihnen **umsetzbare Tipps** , welche Änderungen die meisten Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="aecfc-122">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <span data-ttu-id="aecfc-123">Einrichtung</span><span class="sxs-lookup"><span data-stu-id="aecfc-123">Set up</span></span>   

<span data-ttu-id="aecfc-124">Zunächst müssen Sie die Website so einrichten, dass Sie später Änderungen daran vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="aecfc-124">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="aecfc-125">[Öffnen Sie den Quellcode für die Website](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="aecfc-125">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="aecfc-126">Diese Registerkarte wird als **Registerkarte "Editor"** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="aecfc-126">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Die Registerkarte "Editor"" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="aecfc-128">Die **Registerkarte "Editor"**</span><span class="sxs-lookup"><span data-stu-id="aecfc-128">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-129">Wählen Sie **Tony**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-129">Select **tony**.</span></span>  <span data-ttu-id="aecfc-130">Ein Menü wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-130">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Das Menü, das nach dem Klicken auf "Tony" angezeigt wird" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="aecfc-132">Das Menü, das nach dem Klicken auf " **Tony** " angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="aecfc-132">The menu that appears after clicking **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-133">Wählen Sie **Remix Project**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-133">Select **Remix Project**.</span></span>  <span data-ttu-id="aecfc-134">Der Name des Projekts wechselt von **Tony** zu einem zufällig generierten Namen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-134">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="aecfc-135">Sie haben jetzt eine eigene bearbeitbare Kopie des Codes.</span><span class="sxs-lookup"><span data-stu-id="aecfc-135">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="aecfc-136">Später können Sie Änderungen an diesem Code vornehmen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-136">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="aecfc-137">Wählen Sie **in einem neuen Fenster** **anzeigen** und auswählen aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-137">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="aecfc-138">Die Demo wird in einer neuen Registerkarte geöffnet.  Diese Registerkarte wird als **Registerkarte Demo**bezeichnet.  Das Laden der Website kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-138">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Die Registerkarte "Demo"" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="aecfc-140">Die Registerkarte "Demo"</span><span class="sxs-lookup"><span data-stu-id="aecfc-140">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-141">Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="aecfc-141">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="aecfc-142">Microsoft Edge devtools wird parallel zur Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="aecfc-142">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools und die Demo" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="aecfc-144">DevTools und die Demo</span><span class="sxs-lookup"><span data-stu-id="aecfc-144">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aecfc-145">Für die restlichen Screenshots in diesem Lernprogramm wird devtools in einem separaten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-145">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="aecfc-146">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, einzugeben `Undock` , und wählen Sie dann **in separates Fenster Abdocken**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-146">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Nicht angedockte devtools" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="aecfc-148">Nicht angedockte devtools</span><span class="sxs-lookup"><span data-stu-id="aecfc-148">Undocked DevTools</span></span>  
:::image-end:::  

### <span data-ttu-id="aecfc-149">Festlegen eines Basisplans</span><span class="sxs-lookup"><span data-stu-id="aecfc-149">Establish a baseline</span></span>   

<span data-ttu-id="aecfc-150">Der Basisplan ist eine Aufzeichnung der Vorgehensweise der Website, bevor Sie Leistungsverbesserungen durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="aecfc-150">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="aecfc-151">Wählen Sie die Registerkarte **Audits** aus.  Sie ist möglicherweise hinter der Schaltfläche " **Weitere Panels** \ ![ ][ImageMorePanelsIcon] " verborgen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-151">Select the **Audits** tab.  It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="aecfc-152">Auf diesem Panel befindet sich ein Leuchtturm, weil das Projekt, das das Audit Panel anbietet, den Namen **Lighthouse**trägt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-152">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Überwachungs Panel" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="aecfc-154">**Überwachungs** Panel</span><span class="sxs-lookup"><span data-stu-id="aecfc-154">The **Audits** panel</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="aecfc-155">Vergleichen Sie Ihre Überwachungs Konfigurationseinstellungen mit denen in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="aecfc-155">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="aecfc-156">Nachfolgend finden Sie eine Erläuterung der verschiedenen Optionen:</span><span class="sxs-lookup"><span data-stu-id="aecfc-156">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="aecfc-157">**Gerät**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-157">**Device**.</span></span>  <span data-ttu-id="aecfc-158">Wenn Sie auf **Mobile** festlegen, ändert sich die Zeichenfolge des Benutzer-Agents und simuliert ein mobiles Viewport.</span><span class="sxs-lookup"><span data-stu-id="aecfc-158">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="aecfc-159">Durch die Einstellung auf den **Desktop** werden die **mobilen** Änderungen so ziemlich deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="aecfc-159">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="aecfc-160">**Audits**.</span><span class="sxs-lookup"><span data-stu-id="aecfc-160">**Audits**.</span></span>  <span data-ttu-id="aecfc-161">Durch das Deaktivieren einer Kategorie wird verhindert, dass der Überwachungsbereich diese Audits ausführt, und diese Audits werden aus dem Bericht ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-161">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="aecfc-162">Lassen Sie die anderen Kategorien aktiviert, wenn Sie die Typen von Empfehlungen anzeigen möchten, die bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-162">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="aecfc-163">Das Deaktivieren von Kategorien beschleunigt den Überwachungsvorgang etwas.</span><span class="sxs-lookup"><span data-stu-id="aecfc-163">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="aecfc-164">**Einschränkung**.</span><span class="sxs-lookup"><span data-stu-id="aecfc-164">**Throttling**.</span></span>  <span data-ttu-id="aecfc-165">Einstellung auf **simulierte langsame 4G, vierfache CPU-Verlangsamung** simuliert die typischen Bedingungen für das Browsen auf einem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="aecfc-165">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="aecfc-166">Sie wird als "simuliert" bezeichnet, da das Überwachungs Panel während des Überwachungsprozesses nicht tatsächlich gedrosselt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-166">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="aecfc-167">Stattdessen wird nur extrapoliert, wie lange es dauert, bis die Seite unter mobilen Bedingungen geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="aecfc-167">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="aecfc-168">Mit der Einstellung " **angewendet...** " wird dagegen Ihre CPU und Ihr Netzwerk tatsächlich gedrosselt, mit dem Kompromiss eines längeren Überwachungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="aecfc-168">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="aecfc-169">**Speicher löschen**.</span><span class="sxs-lookup"><span data-stu-id="aecfc-169">**Clear Storage**.</span></span>  <span data-ttu-id="aecfc-170">Wenn Sie dieses Kontrollkästchen aktivieren, wird vor jeder Überwachung der gesamte Speicherplatz gelöscht, der der Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aecfc-170">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="aecfc-171">Belasse diese Einstellung, wenn Sie überprüfen möchten, wie die Besucher Ihrer Website erst einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="aecfc-171">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="aecfc-172">Deaktivieren Sie diese Einstellung, wenn Sie die Wiederholungs Besuchs Erfahrung wünschen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-172">Disable this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="aecfc-173">Wählen Sie **Audits ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-173">Select **Run Audits**.</span></span>  <span data-ttu-id="aecfc-174">Nach 10 bis 30 Sekunden wird im Überwachungs Panel ein Bericht über die Leistung der Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-174">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Der Bericht für das Audits-Panel über die Leistung der Website" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="aecfc-176">Der Bericht für das Audits-Panel über die Leistung der Website</span><span class="sxs-lookup"><span data-stu-id="aecfc-176">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="aecfc-177">Behandeln von Berichts Fehlern</span><span class="sxs-lookup"><span data-stu-id="aecfc-177">Handling report errors</span></span>   

<span data-ttu-id="aecfc-178">Wenn Sie in Ihrem Audits-Panel-Bericht jemals eine Fehlermeldung erhalten, versuchen Sie, die Registerkarte Demo in einem **InPrivate** -Fenster auszuführen, ohne dass weitere Registerkarten geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="aecfc-178">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="aecfc-179">Dadurch wird sichergestellt, dass Sie Microsoft Edge in einem sauberen Zustand ausführen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-179">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="aecfc-180">Insbesondere Microsoft-Edge-Erweiterungen stören häufig den Überwachungsprozess.</span><span class="sxs-lookup"><span data-stu-id="aecfc-180">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <span data-ttu-id="aecfc-181">Grundlegendes zu Ihrem Bericht</span><span class="sxs-lookup"><span data-stu-id="aecfc-181">Understand your report</span></span>   

<span data-ttu-id="aecfc-182">Die Zahl am oberen Rand des Berichts entspricht dem Gesamtleistungsfaktor für die Website.</span><span class="sxs-lookup"><span data-stu-id="aecfc-182">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="aecfc-183">Wenn Sie später Änderungen am Code vornehmen, sollte diese Zahl steigen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-183">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="aecfc-184">Eine höhere Punktzahl bedeutet eine bessere Leistung.</span><span class="sxs-lookup"><span data-stu-id="aecfc-184">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Der Gesamtleistungsfaktor" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="aecfc-186">Der Gesamtleistungsfaktor</span><span class="sxs-lookup"><span data-stu-id="aecfc-186">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-187">Der Abschnitt **Metriken** bietet quantitative Maße für die Leistung der Website.</span><span class="sxs-lookup"><span data-stu-id="aecfc-187">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="aecfc-188">Jede Metrik bietet Einblicke in einen anderen Aspekt der Leistung.</span><span class="sxs-lookup"><span data-stu-id="aecfc-188">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="aecfc-189">Beispielsweise erfahren Sie in der **ersten Inhaltsfarbe** , wann Inhalte zuerst auf dem Bildschirm gemalt werden, was ein wichtiger Meilenstein für die Wahrnehmung der Seitenauslastung durch den Benutzer ist, während die **Zeit für interaktive** Kennzeichnung den Punkt angibt, an dem die Seite für die Behandlung von Benutzerinteraktionen bereit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-189">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Abschnitt "Metriken"" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="aecfc-191">Abschnitt " **Metriken** "</span><span class="sxs-lookup"><span data-stu-id="aecfc-191">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-192">Wählen Sie die hervorgehobene Umschaltfläche in der folgenden Abbildung aus, um eine Beschreibung für jede Metrik anzuzeigen, und klicken Sie auf **Weitere Informationen** , um die Dokumentation dazu zu lesen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-192">Select the highlighted toggle button in the following figure to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der Metriken Elemente" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="aecfc-194">Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der Metriken Elemente</span><span class="sxs-lookup"><span data-stu-id="aecfc-194">Select the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-195">Unter Metriken finden Sie eine Sammlung von Screenshots, die Ihnen zeigen, wie die Seite beim Laden aussah.</span><span class="sxs-lookup"><span data-stu-id="aecfc-195">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Screenshots, wie die Seite beim Laden aussah" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="aecfc-197">Screenshots, wie die Seite beim Laden aussah</span><span class="sxs-lookup"><span data-stu-id="aecfc-197">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-198">Im Abschnitt " **Verkaufschancen** " finden Sie spezielle Tipps zum Verbessern der Auslastungs Leistung dieser bestimmten Seite.</span><span class="sxs-lookup"><span data-stu-id="aecfc-198">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Der Abschnitt "Verkaufschancen"" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="aecfc-200">Der Abschnitt " **Verkaufschancen** "</span><span class="sxs-lookup"><span data-stu-id="aecfc-200">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-201">Wählen Sie eine Gelegenheit aus, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="aecfc-201">Select an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminieren von Render-Blockierungs Ressourcen" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="aecfc-203">**Eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="aecfc-203">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-204">Wählen Sie **Weitere Informationen** aus, um die Dokumentation dazu anzuzeigen, warum eine Verkaufschance wichtig ist, und spezifische Empfehlungen zur Behebung.</span><span class="sxs-lookup"><span data-stu-id="aecfc-204">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Dokumentation für die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="aecfc-206">Dokumentation für die Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="aecfc-206">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-207">Der Abschnitt **Diagnostics** enthält weitere Informationen zu Faktoren, die zur Ladezeit der Seite beitragen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-207">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Abschnitt "Diagnose"" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="aecfc-209">Abschnitt " **Diagnose** "</span><span class="sxs-lookup"><span data-stu-id="aecfc-209">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-210">Im Abschnitt "übertragene **Prüfungen** " wird gezeigt, was die Website richtig macht.</span><span class="sxs-lookup"><span data-stu-id="aecfc-210">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="aecfc-211">Wählen Sie diese Option aus, um den Abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-211">Select to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Abschnitt "übergebene Überprüfungen"" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="aecfc-213">Abschnitt " **übergebene Überprüfungen** "</span><span class="sxs-lookup"><span data-stu-id="aecfc-213">The **Passed Audits** section</span></span>  
:::image-end:::  

## <span data-ttu-id="aecfc-214">Schritt 2: experimentieren</span><span class="sxs-lookup"><span data-stu-id="aecfc-214">Step 2: Experiment</span></span>   

<span data-ttu-id="aecfc-215">Im Abschnitt "Verkaufschancen" Ihres Überwachungsberichts erhalten Sie Tipps, wie Sie die Leistung der Seite verbessern können.</span><span class="sxs-lookup"><span data-stu-id="aecfc-215">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="aecfc-216">In diesem Abschnitt implementieren Sie die empfohlenen Änderungen an der CodeBase, indem Sie die Website nach jeder Änderung überwachen, um zu messen, wie sich dies auf die Geschwindigkeit der Website auswirkt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-216">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="aecfc-217">Aktivieren der Text Komprimierung</span><span class="sxs-lookup"><span data-stu-id="aecfc-217">Enable text compression</span></span>   

<span data-ttu-id="aecfc-218">Ihr Bericht besagt, dass die Vermeidung von enormen Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-218">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="aecfc-219">Das Aktivieren der Text Komprimierung bietet die Möglichkeit, die Leistung der Seite zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-219">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="aecfc-220">Die Text Komprimierung erfolgt, wenn Sie die Größe einer Textdatei reduzieren oder komprimieren, bevor Sie Sie über das Netzwerk senden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-220">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="aecfc-221">Eine Art gefällt Ihnen, wie Sie einen Ordner komprimieren können, bevor Sie ihn per e-Mail senden, um die Größe zu verringern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-221">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="aecfc-222">Bevor Sie die Komprimierung aktivieren, gibt es eine Reihe von Möglichkeiten, um manuell zu überprüfen, ob Textressourcen komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-222">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="aecfc-223">Wählen Sie die Registerkarte **Netzwerk** aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-223">Select the **Network** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Netzwerk Panel" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="aecfc-225">**Netzwerk** Panel</span><span class="sxs-lookup"><span data-stu-id="aecfc-225">The **Network** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-226">Wählen Sie das Symbol **Netzwerkeinstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-226">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="aecfc-227">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** .</span><span class="sxs-lookup"><span data-stu-id="aecfc-227">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="aecfc-228">Die Höhe der Zeilen in der Tabelle der Netzwerkanforderungen nimmt zu.</span><span class="sxs-lookup"><span data-stu-id="aecfc-228">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Große Zeilen in der Tabelle "Netzwerkanforderungen"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="aecfc-230">Große Zeilen in der Tabelle "Netzwerkanforderungen"</span><span class="sxs-lookup"><span data-stu-id="aecfc-230">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-231">Wenn die Spalte **Größe** in der Tabelle der Netzwerkanforderungen nicht angezeigt wird, klicken Sie auf die Tabellenüberschrift, und wählen Sie dann **Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-231">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="aecfc-232">Jede **Größen** Zelle enthält zwei Werte.</span><span class="sxs-lookup"><span data-stu-id="aecfc-232">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="aecfc-233">Der oberste Wert ist die Größe der heruntergeladenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="aecfc-233">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="aecfc-234">Der untere Wert gibt die Größe der unkomprimierten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="aecfc-234">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="aecfc-235">Wenn die beiden Werte identisch sind, wird die Ressource nicht komprimiert, wenn Sie über das Netzwerk gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-235">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="aecfc-236">In der vorhergehenden Abbildung sind die oberen und unteren Werte für " `bundle.js` sind" `1.2 MB` und " `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-236">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="aecfc-237">Überprüfen Sie auf Komprimierung, indem Sie die HTTP-Header einer Ressource prüfen:</span><span class="sxs-lookup"><span data-stu-id="aecfc-237">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="aecfc-238">Wählen Sie **bundle.js**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-238">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="aecfc-239">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-239">Select the **Headers** tab.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Die Registerkarte "Überschriften"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="aecfc-241">Die Registerkarte "über **Schriften** "</span><span class="sxs-lookup"><span data-stu-id="aecfc-241">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-242">Durchsuchen Sie den Abschnitt **Antwort Kopfzeilen** nach einer `content-encoding` Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="aecfc-242">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="aecfc-243">Sie sollten keines sehen, was bedeutet, dass es sich nicht um eine `bundle.js` Komprimierung handelt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-243">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="aecfc-244">Wenn eine Ressource komprimiert ist, wird in der Regel dieser Header auf `gzip` , `deflate` oder gesetzt `br` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-244">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="aecfc-245">Eine Erläuterung dieser Werte finden Sie unter [Direktiven][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="aecfc-245">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="aecfc-246">Genug mit den Erläuterungen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-246">Enough with the explanations.</span></span>  <span data-ttu-id="aecfc-247">Zeit, einige Änderungen vorzunehmen!</span><span class="sxs-lookup"><span data-stu-id="aecfc-247">Time to make some changes!</span></span>  <span data-ttu-id="aecfc-248">Aktivieren Sie die Text Komprimierung, indem Sie ein paar Codezeilen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="aecfc-248">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="aecfc-249">Klicken Sie auf der Registerkarte Editor auf **server.js**.</span><span class="sxs-lookup"><span data-stu-id="aecfc-249">In the editor tab, click **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="server.js bearbeiten" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="aecfc-251">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="aecfc-251">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-252">Fügen Sie **server.js**den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="aecfc-252">Add the following code to **server.js**.</span></span>  <span data-ttu-id="aecfc-253">Stellen Sie sicher, dass Sie dies tun `app.use(compression())` `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-253">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="aecfc-254">In der Regel müssen Sie das `compression` Paket über einen ähnlichen `npm i -S compression` Vorgang installieren, dies wurde aber bereits für Sie erledigt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-254">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="aecfc-255">Warten Sie, bis glitch den neuen Build der Website bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="aecfc-255">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="aecfc-256">Die raffinierte Animation neben **Tools** bedeutet, dass die Website neu erstellt und erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-256">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="aecfc-257">Die Änderung ist fertig, wenn die Animation neben **Tools** verschwindet.</span><span class="sxs-lookup"><span data-stu-id="aecfc-257">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="aecfc-258">Wählen Sie wieder **in einem neuen Fenster** **anzeigen** und auswählen aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-258">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="aecfc-259">Verwenden Sie die zuvor gelernten Workflows, um manuell zu überprüfen, ob die Komprimierung funktioniert:</span><span class="sxs-lookup"><span data-stu-id="aecfc-259">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="aecfc-260">Wechseln Sie zur Registerkarte Demo zurück, und laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="aecfc-260">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="aecfc-261">In der Spalte **Größe** sollten nun zwei unterschiedliche Werte für Textressourcen wie angezeigt werden `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-261">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="aecfc-262">In der folgenden Abbildung ist der oberste Wert von für die `256 KB` Größe der Datei, die `bundle.js` über das Netzwerk gesendet wurde, und der untere Wert von `1.2 MB` ist die unkomprimierte Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="aecfc-262">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="In der Spalte "Größe" werden nun zwei unterschiedliche Werte für Textressourcen angezeigt." lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="aecfc-264">In der Spalte " **Größe** " werden nun zwei unterschiedliche Werte für Textressourcen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-264">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-265">Im Abschnitt " **Antwort Kopfzeilen** " `bundle.js` sollte nun eine `content-encoding: gzip` Kopfzeile enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="aecfc-265">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Der Abschnitt "Antwort Kopfzeilen" enthält jetzt einen Inhalts Codierungs Header." lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="aecfc-267">Der Abschnitt " **Antwort Kopfzeilen** " enthält jetzt einen Inhalts Codierungs Header.</span><span class="sxs-lookup"><span data-stu-id="aecfc-267">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aecfc-268">Überwachen Sie die Seite erneut, um zu messen, welche Art von Auswirkungen die Text Komprimierung auf die Ladeleistung der Seite hat:</span><span class="sxs-lookup"><span data-stu-id="aecfc-268">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="aecfc-269">Wählen Sie die Registerkarte **Audits** aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-269">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="aecfc-270">Wählen Sie **Audit durchführen** \ ( ![ Audit durchführen ][ImagePerformIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-270">Select **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="aecfc-271">Belasse die Einstellungen wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="aecfc-271">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="aecfc-272">Wählen Sie **Audit ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-272">Select **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Aktivierung der Text Komprimierung" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="aecfc-274">Ein Überwachungsbericht nach der Aktivierung der Text Komprimierung</span><span class="sxs-lookup"><span data-stu-id="aecfc-274">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="aecfc-275">Ihr Gesamtleistungsfaktor sollte zugenommen haben, was bedeutet, dass die Website schneller wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-275">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="aecfc-276">Text Komprimierung in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="aecfc-276">Text compression in the real world</span></span>   

<span data-ttu-id="aecfc-277">Bei den meisten Servern gibt es wirklich einfache Fehlerbehebungen wie diese zum Aktivieren von Komprimierung!</span><span class="sxs-lookup"><span data-stu-id="aecfc-277">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="aecfc-278">Führen Sie einfach eine Suche durch, um zu konfigurieren, welcher Server zum Komprimieren von Text verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-278">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="aecfc-279">Ändern der Größe von Bildern</span><span class="sxs-lookup"><span data-stu-id="aecfc-279">Resize images</span></span>   

<span data-ttu-id="aecfc-280">Ihr Bericht weist darauf hin, dass die Vermeidung enormer Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-280">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="aecfc-281">Durch Ändern der Größe von Bildern kann die Größe der Netzwerk Nutzlast verringert werden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-281">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="aecfc-282">Wenn der Benutzer Ihre Bilder auf einem Bildschirm mit einem mobilen Gerät anzeigt, der 500 Pixel breit ist, ist es wirklich unwichtig, ein 1500-Pixel breites Bild zu senden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-282">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="aecfc-283">Im Idealfall senden Sie höchstens ein Bild mit einer Breite von 500 Pixel.</span><span class="sxs-lookup"><span data-stu-id="aecfc-283">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="aecfc-284">Klicken Sie in Ihrem Bericht auf **enorme Netzwerk Nutzlasten vermeiden** , um festzustellen, welche Bilder geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-284">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="aecfc-285">Es sieht so aus, als ob 2 der JPG-Dateien über 2000 KB liegen, was größer als notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="aecfc-285">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="aecfc-286">Zurück auf der Registerkarte "Editor" Öffnen `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-286">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="aecfc-287">Ersetzen Sie `const dir = 'big'` durch `const dir = 'small'`.</span><span class="sxs-lookup"><span data-stu-id="aecfc-287">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="aecfc-288">Dieses Verzeichnis enthält Kopien der gleichen Bilder, deren Größe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="aecfc-288">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="aecfc-289">Überprüfen Sie die Seite erneut, um zu sehen, wie sich diese Änderung auf die Ladeleistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-289">Audit the page again to see how this change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Ändern der Größe von Bildern" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="aecfc-291">Ein Überwachungsbericht nach dem Ändern der Größe von Bildern</span><span class="sxs-lookup"><span data-stu-id="aecfc-291">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aecfc-292">Sieht so aus, als ob die Änderung nur eine geringfügige Auswirkung auf den Gesamtleistungsfaktor hat.</span><span class="sxs-lookup"><span data-stu-id="aecfc-292">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="aecfc-293">Die Punktzahl zeigt jedoch nicht eindeutig, wie viel Netzwerkdaten Sie für Ihre Benutzer speichern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-293">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="aecfc-294">Die Gesamtgröße der alten Fotos betrug etwa 5,3 Megabyte, während es jetzt nur noch etwa 0,18 Megabytes gibt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-294">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="aecfc-295">Ändern der Größe von Bildern in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="aecfc-295">Resizing images in the real world</span></span>   

<span data-ttu-id="aecfc-296">Bei einer kleinen app kann eine einmalige Größenänderung so gut wie möglich sein.</span><span class="sxs-lookup"><span data-stu-id="aecfc-296">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="aecfc-297">Bei einer umfangreichen APP ist dies natürlich nicht skalierbar.</span><span class="sxs-lookup"><span data-stu-id="aecfc-297">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="aecfc-298">Im folgenden finden Sie einige Strategien zum Verwalten von Bildern in umfangreichen apps:</span><span class="sxs-lookup"><span data-stu-id="aecfc-298">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="aecfc-299">Ändern der Größe von Bildern während des Buildprozesses</span><span class="sxs-lookup"><span data-stu-id="aecfc-299">Resize images during your build process.</span></span>  
*   <span data-ttu-id="aecfc-300">Erstellen Sie mehrere Größen der einzelnen Bilder während des Buildprozesses, und verwenden `srcset` Sie Sie dann in Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="aecfc-300">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="aecfc-301">Zur Laufzeit sorgt der Browser dafür, welche Größe für das Gerät am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="aecfc-301">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="aecfc-302">Verwenden Sie ein Image CDN, mit dem Sie die Größe eines Bilds dynamisch ändern können, wenn Sie es anfordern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-302">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="aecfc-303">Optimieren Sie zumindest jedes Bild.</span><span class="sxs-lookup"><span data-stu-id="aecfc-303">At the very least, optimize each image.</span></span>  <span data-ttu-id="aecfc-304">Dies kann zu enormen Einsparungen führen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-304">This may create huge savings.</span></span>  
  <span data-ttu-id="aecfc-305">Optimierung ist, wenn Sie ein Bild über ein spezielles Programm ausführen, das die Größe der Bilddatei reduziert.</span><span class="sxs-lookup"><span data-stu-id="aecfc-305">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="aecfc-306">Weitere Tipps finden Sie unter [grundlegende Bildoptimierung][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="aecfc-306">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  
    
### <span data-ttu-id="aecfc-307">Eliminieren von Render-Blockierungs Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aecfc-307">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="aecfc-308">Ihr neuester Bericht besagt, dass das Eliminieren von Render-Blockierungs Ressourcen jetzt die größte Chance darstellt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-308">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="aecfc-309">Eine Render-Blockierungs Ressource ist eine externe JavaScript-oder CSS-Datei, die vom Browser heruntergeladen, analysiert und ausgeführt werden muss, bevor die Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-309">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="aecfc-310">Das Ziel besteht darin, nur den zentralen CSS-und JavaScript-Code auszuführen, der erforderlich ist, um die Seite ordnungsgemäß anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-310">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="aecfc-311">Die erste Aufgabe besteht darin, Code zu finden, den Sie beim Laden der Seite nicht ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-311">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="aecfc-312">Wählen Sie **Render-Blockierungs Ressourcen eliminieren** aus, um die blockierten Ressourcen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="aecfc-312">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="aecfc-313">und `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-313">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Weitere Informationen zur Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="aecfc-315">Weitere Informationen zur Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="aecfc-315">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-316">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, mit der Eingabe zu beginnen `Coverage` , und wählen Sie dann **Coverage anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-316">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Öffnen des Befehlsmenüs im Überwachungs Panel" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="aecfc-318">Öffnen des Befehlsmenüs im **Überwachungs** Panel</span><span class="sxs-lookup"><span data-stu-id="aecfc-318">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Die Registerkarte "Coverage"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="aecfc-320">Die Registerkarte " **Coverage** "</span><span class="sxs-lookup"><span data-stu-id="aecfc-320">The **Coverage** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-321">Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-321">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="aecfc-322">Die Registerkarte **Coverage** bietet eine Übersicht darüber, wie viel des Codes in `bundle.js` , `jquery.js` und `lodash.js` ausgeführt wird, während die Seite geladen wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-322">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="aecfc-323">In der folgenden Abbildung werden etwa 76% und 30% der jQuery-und Lodash-Dateien nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aecfc-323">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Der Bericht "Berichterstattung"" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="aecfc-325">Der Bericht "Berichterstattung"</span><span class="sxs-lookup"><span data-stu-id="aecfc-325">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-326">Wählen Sie die Zeile **jquery.js** aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-326">Select the **jquery.js** row.</span></span>  <span data-ttu-id="aecfc-327">DevTools öffnet die Datei im Quellen Panel.</span><span class="sxs-lookup"><span data-stu-id="aecfc-327">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="aecfc-328">Eine Codezeile wird ausgeführt, wenn Sie einen blauen Balken Daneben hat.</span><span class="sxs-lookup"><span data-stu-id="aecfc-328">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="aecfc-329">Eine rote Leiste bedeutet, dass Sie nicht ausgeführt wurde und beim Laden der Seite definitiv nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-329">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Anzeigen der jQuery-Datei im Quellen Panel" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="aecfc-331">Anzeigen der jQuery-Datei im **Quellen** Panel</span><span class="sxs-lookup"><span data-stu-id="aecfc-331">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-332">Scrollen Sie ein wenig durch den jQuery-Code.</span><span class="sxs-lookup"><span data-stu-id="aecfc-332">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="aecfc-333">Einige der Zeilen, die "Run" erhalten, sind eigentlich nur Kommentare.</span><span class="sxs-lookup"><span data-stu-id="aecfc-333">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="aecfc-334">Wenn Sie diesen Code über einen minifier ausführen, der Kommentare entfernt, ist eine weitere Möglichkeit, die Größe dieser Datei zu verringern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-334">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="aecfc-335">Kurz gesagt: Wenn Sie mit Ihrem eigenen Code arbeiten, können Sie mithilfe der Registerkarte Coverage Ihren Code, Zeile für Zeile, analysieren und nur den Code versenden, der für die Seitenauslastung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-335">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="aecfc-336">Sind die `jquery.js` und `lodash.js` Dateien auch zum Laden der Seite erforderlich?</span><span class="sxs-lookup"><span data-stu-id="aecfc-336">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="aecfc-337">Auf der Registerkarte Anforderungs Blockierung wird angezeigt, was geschieht, wenn keine Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="aecfc-337">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="aecfc-338">Wählen Sie die Registerkarte **Netzwerk** aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-338">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="aecfc-339">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-339">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="aecfc-340">Beginnen `blocking` Sie mit der Eingabe, und wählen Sie dann **Anforderungs Blockierung anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-340">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Die Registerkarte ' Anforderungs Blockierung '" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="aecfc-342">Die Registerkarte ' **Anforderungs Blockierung** '</span><span class="sxs-lookup"><span data-stu-id="aecfc-342">The **Request Blocking** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-343">Wählen Sie **Muster hinzufügen** \ ( ![ Muster hinzufügen ][ImageAddPatternIcon] ) aus, geben Sie ein `/libs/*` , und drücken Sie dann `Enter` , um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-343">Select **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Hinzufügen eines Musters, um jede Anforderung an das libs-Verzeichnis zu blockieren" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="aecfc-345">Hinzufügen eines Musters zum Blockieren einer Anforderung an das `libs` Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="aecfc-345">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-346">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="aecfc-346">Refresh the page.</span></span>  <span data-ttu-id="aecfc-347">Die Anforderungen für jQuery und Lodash sind rot, was bedeutet, dass die Anforderungen blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-347">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="aecfc-348">Da die Seite immer noch geladen und interaktiv ist, sieht es so aus, als ob diese Ressourcen überhaupt nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-348">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden." lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="aecfc-350">Das **Netzwerk** Panel zeigt, dass die Anforderungen blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-350">The **Network** panel shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-351">Wählen Sie **alle Muster entfernen** \ ( ![ alle Muster entfernen ][ImageRemoveIcon] \) aus, um das `/libs/*` Blockierungs Muster zu löschen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-351">Select **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="aecfc-352">Im Allgemeinen ist die Registerkarte Anforderungs Blockierung hilfreich, um zu simulieren, wie sich die Seite verhält, wenn eine bestimmte Ressource nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aecfc-352">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="aecfc-353">Entfernen Sie nun die Verweise auf diese Dateien aus dem Code, und überwachen Sie die Seite erneut:</span><span class="sxs-lookup"><span data-stu-id="aecfc-353">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="aecfc-354">Zurück auf der Registerkarte "Editor" Öffnen `template.html` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-354">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="aecfc-355">Löschen Sie `<script src="/libs/lodash.js">` und `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="aecfc-355">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="aecfc-356">Warten Sie, bis die Website neu erstellt und erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-356">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="aecfc-357">Überwachen Sie die Seite im **Überwachungs** Panel erneut.</span><span class="sxs-lookup"><span data-stu-id="aecfc-357">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="aecfc-358">Ihre Gesamtpunktzahl sollte erneut verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-358">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="aecfc-360">Ein **Überwachungs** Bericht nach dem Entfernen der Render-Blockierungs Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aecfc-360">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="aecfc-361">Optimieren des kritischen Rendering-Pfads in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="aecfc-361">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="aecfc-362">Der **kritische Rendering-Pfad** bezieht sich auf den Code, der zum Laden einer Seite erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aecfc-362">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="aecfc-363">Im Allgemeinen können Sie die Seitenauslastung beschleunigen, indem Sie nur den Versand von kritischem Code während des Ladens der Seite durchführen und dann alles andere verzögert laden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-363">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="aecfc-364">Es ist unwahrscheinlich, dass Sie in der Lage sind, Skripts zu finden, die Sie direkt entfernen können, aber möglicherweise viele Skripts finden, die Sie beim Laden der Seite nicht anfordern müssen, und stattdessen möglicherweise asynchron angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-364">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="aecfc-365">Wenn Sie ein Framework verwenden, überprüfen Sie, ob es einen Produktionsmodus aufweist.</span><span class="sxs-lookup"><span data-stu-id="aecfc-365">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="aecfc-366">In diesem Modus wird möglicherweise ein Feature wie das [schütteln von Strukturen][WebpackTreeShaking] verwendet, um unnötigen Code zu eliminieren, der das kritische Rendern blockiert.</span><span class="sxs-lookup"><span data-stu-id="aecfc-366">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="aecfc-367">Arbeiten mit einem geringeren Hauptthread</span><span class="sxs-lookup"><span data-stu-id="aecfc-367">Do less main thread work</span></span>   

<span data-ttu-id="aecfc-368">Ihr neuester Bericht zeigt einige kleinere potenzielle Einsparungen im Abschnitt "Verkaufschancen", aber wenn Sie im Abschnitt "Diagnose" nach unten suchen, sieht es so aus, als wäre der größte Engpass zu viel Hauptthread Aktivität.</span><span class="sxs-lookup"><span data-stu-id="aecfc-368">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="aecfc-369">Der Hauptthread ist der Ort, an dem der Browser die meiste Arbeit ausführt, die zum Anzeigen einer Seite erforderlich ist, beispielsweise das analysieren und Ausführen von HTML, CSS und JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aecfc-369">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="aecfc-370">Das Ziel besteht darin, mithilfe des Leistungs Panels zu analysieren, welche Arbeit der Hauptthread beim Laden der Seite unternimmt, und Wege zu finden, um unnötige Arbeit zu verzögern oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-370">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="aecfc-371">Wählen Sie die Registerkarte **Leistung** aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-371">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="aecfc-372">Wählen Sie **aufnahmeeinstellungen** \ ( ![ Aufnahmeeinstellungen ][ImageCaptureIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-372">Select **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="aecfc-373">**Netzwerk** auf **langsame 3G** -und **CPU** -zu- **6x-Verlangsamung**einstellen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-373">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="aecfc-374">Bei mobilen Geräten gibt es in der Regel mehr Hardwareeinschränkungen als Laptops oder Desktops, sodass Sie mit diesen Einstellungen das Laden der Seite so erleben können, als ob Sie ein weniger leistungsfähiges Gerät verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-374">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="aecfc-375">Wählen Sie **Aktualisieren** \ ( ![ aktualisieren ][ImageRefreshIcon] \) aus.</span><span class="sxs-lookup"><span data-stu-id="aecfc-375">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="aecfc-376">DevTools aktualisiert die Seite und erstellt dann eine Visualisierung aller ausgeführten Arbeiten, um die Seite zu laden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-376">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="aecfc-377">Diese Visualisierung wird als **Ablaufverfolgung**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="aecfc-377">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Der Leistungs Panel-Ablaufverfolgung der Seitenauslastung" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="aecfc-379">Der **Leistungs** Panel-Ablaufverfolgung der Seitenauslastung</span><span class="sxs-lookup"><span data-stu-id="aecfc-379">The **Performance** panel trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aecfc-380">Die Ablaufverfolgung zeigt die Aktivität chronologisch an, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="aecfc-380">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="aecfc-381">Die oben dargestellten fps-, CPU-und net-Diagramme geben Ihnen einen Überblick über Frames pro Sekunde, CPU-Aktivität und Netzwerkaktivität.</span><span class="sxs-lookup"><span data-stu-id="aecfc-381">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="aecfc-382">Der gelb markierte Block, der in der Abbildung nachfolgend angezeigt wird, war die CPU vollständig mit Skriptaktivitäten ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="aecfc-382">The block of yellow selected that you see in the figure after the following, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="aecfc-383">Dies ist ein Hinweis darauf, dass Sie möglicherweise die Seitenauslastung beschleunigen können, indem Sie eine geringere JavaScript-Arbeit durchführen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-383">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Der Abschnitt "Übersicht" der Ablaufverfolgung" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="aecfc-385">Der Abschnitt "Übersicht" der Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="aecfc-385">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="aecfc-386">Untersuchen Sie die Ablaufverfolgung, um Möglichkeiten für eine geringere JavaScript-Arbeit zu finden:</span><span class="sxs-lookup"><span data-stu-id="aecfc-386">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="aecfc-387">Wählen Sie den Abschnitt **Anzeige** dauern aus, um ihn zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-387">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="aecfc-388">Basierend auf der Tatsache, dass es möglicherweise eine Reihe von [Timings][MDNUserTimingApi] -Maßnahmen von reagieren gibt, scheint es so zu sein, als ob die APP von Tony die Entwicklungsmethode von reagieren verwendet.</span><span class="sxs-lookup"><span data-stu-id="aecfc-388">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="aecfc-389">Wenn Sie auf den Produktionsmodus von reagieren umstellen, kann dies einige einfache Leistungsgewinne hervorbringen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-389">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Abschnitt "Anzeigedauern"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="aecfc-391">Abschnitt " **Anzeige** dauern"</span><span class="sxs-lookup"><span data-stu-id="aecfc-391">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-392">Wählen Sie erneut **Anzeige** dauern aus, um den Abschnitt zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="aecfc-392">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="aecfc-393">Durchsuchen Sie den **Haupt** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-393">Browse the **Main** section.</span></span>  <span data-ttu-id="aecfc-394">Dieser Abschnitt zeigt ein chronologisches Protokoll der Hauptthread Aktivität, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="aecfc-394">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="aecfc-395">Die y-Achse (von oben nach unten) zeigt, warum Ereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="aecfc-395">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="aecfc-396">In der figyre nach dem folgenden Beispiel hat das Ereignis zum Ausführen der Funktion geführt, die zur Ausführung führte, die `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` zum Ausführen führte usw.</span><span class="sxs-lookup"><span data-stu-id="aecfc-396">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Der Hauptabschnitt" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="aecfc-398">Der **Haupt** Abschnitt</span><span class="sxs-lookup"><span data-stu-id="aecfc-398">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aecfc-399">Scrollen Sie nach unten zum unteren Rand des **Haupt** Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="aecfc-399">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="aecfc-400">Wenn Sie ein Framework verwenden, wird der größte Teil der oberen Aktivität durch das Framework verursacht, das normalerweise außerhalb des Steuerelements liegt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-400">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="aecfc-401">Die von Ihrer APP verursachte Aktivität befindet sich normalerweise unten.</span><span class="sxs-lookup"><span data-stu-id="aecfc-401">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="aecfc-402">In dieser app scheint es so zu sein, dass eine Funktion mit dem Namen `App` viele Anforderungen an eine `mineBitcoin` Funktion verursacht.</span><span class="sxs-lookup"><span data-stu-id="aecfc-402">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="aecfc-403">Es klingt wie Tony könnte die Geräte seiner Fans verwenden, um cryptocurrency zu vergruben...</span><span class="sxs-lookup"><span data-stu-id="aecfc-403">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Zeigen Sie auf die mineBitcoin-Aktivität." lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="aecfc-405">Zeigen Sie auf die `mineBitcoin` Aktivität.</span><span class="sxs-lookup"><span data-stu-id="aecfc-405">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="aecfc-406">Obwohl die Anforderungen, die Ihr Framework macht, in der Regel nicht in Ihrem Steuerelement enthalten sind, können Sie Ihre APP manchmal so strukturieren, dass das Framework ineffizient ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-406">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="aecfc-407">Die Umstrukturierung ihrer App zur effizienten Verwendung des Frameworks ist eine Möglichkeit, um die Arbeit am Hauptthread zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="aecfc-407">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="aecfc-408">Dies erfordert jedoch ein umfassendes Verständnis der Funktionsweise des Frameworks und der Art von Änderungen, die Sie in Ihrem eigenen Code vornehmen, um das Framework effizienter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-408">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="aecfc-409">Erweitern Sie den Abschnitt **Bottom-up** .</span><span class="sxs-lookup"><span data-stu-id="aecfc-409">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="aecfc-410">Auf dieser Registerkarte wird aufgeschlüsselt, welche Aktivitäten die meiste Zeit in Anspruch genommen haben.</span><span class="sxs-lookup"><span data-stu-id="aecfc-410">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="aecfc-411">Wenn im Abschnitt Bottom-up nichts angezeigt wird, klicken Sie auf die Beschriftung für **Haupt** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-411">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="aecfc-412">Der **Bottom-up-** Abschnitt zeigt nur Informationen zu einer beliebigen Aktivität oder Aktivitätsgruppe, die Sie aktuell ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="aecfc-412">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="aecfc-413">Wenn Sie beispielsweise auf eine der Aktivitäten geklickt haben `mineBitcoin` , werden im Abschnitt **Bottom-up** nur Informationen für diese Aktivität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-413">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Die Registerkarte "Bottom-up"" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="aecfc-415">Die Registerkarte " **Bottom-up** "</span><span class="sxs-lookup"><span data-stu-id="aecfc-415">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aecfc-416">In der Spalte **selbst Zeit** wird angezeigt, wie viel Zeit direkt in den einzelnen Aktivitäten aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="aecfc-416">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="aecfc-417">In der folgenden Abbildung wurden etwa 63% der Hauptthread Zeit für die Funktion aufgewendet `mineBitcoin` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-417">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="aecfc-418">Zeit, um zu sehen, ob die Auslastung der Seite durch Verwenden des Produktionsmodus und verringern der JavaScript-Aktivität beschleunigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="aecfc-418">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="aecfc-419">Beginnen mit dem Produktionsmodus:</span><span class="sxs-lookup"><span data-stu-id="aecfc-419">Start with production mode:</span></span>  

1.  <span data-ttu-id="aecfc-420">Öffnen Sie auf der Registerkarte Editor den Reiter `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-420">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="aecfc-421">Ändern Sie `"mode":"development"` in `"mode":"production"`.</span><span class="sxs-lookup"><span data-stu-id="aecfc-421">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="aecfc-422">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-422">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="aecfc-423">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="aecfc-423">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="aecfc-425">Ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus</span><span class="sxs-lookup"><span data-stu-id="aecfc-425">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aecfc-426">Reduzieren Sie die JavaScript-Aktivität, indem Sie die Anforderung entfernen an `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="aecfc-426">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="aecfc-427">Öffnen Sie auf der Registerkarte Editor den Reiter `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-427">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="aecfc-428">Kommentieren Sie die Anforderung `this.mineBitcoin(1500)` in `constructor` .</span><span class="sxs-lookup"><span data-stu-id="aecfc-428">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="aecfc-429">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aecfc-429">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="aecfc-430">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="aecfc-430">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="aecfc-432">Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit</span><span class="sxs-lookup"><span data-stu-id="aecfc-432">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aecfc-433">Sieht so aus, als ob diese letzte Änderung einen massiven Sprung in der Leistung verursacht hat!</span><span class="sxs-lookup"><span data-stu-id="aecfc-433">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="aecfc-434">Dieser Abschnitt enthält eine relativ kurze Einführung in das Leistungs Panel.</span><span class="sxs-lookup"><span data-stu-id="aecfc-434">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="aecfc-435">Weitere Informationen zum Analysieren der Seitenleistung finden Sie unter [Referenz zur Leistungsanalyse][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="aecfc-435">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="aecfc-436">Arbeiten mit einem niedrigeren Hauptthread in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="aecfc-436">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="aecfc-437">Im Allgemeinen ist der Bereich " **Leistung** " die häufigste Methode, um zu verstehen, welche Aktivitäten Ihre Website während der Auslastung durchführt, und Möglichkeiten zum Entfernen unnötiger Aktivitäten zu finden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-437">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="aecfc-438">Wenn Sie einen Ansatz bevorzugen, der sich eher wie anfühlt `console.log()` , können Sie mit der API für die [Benutzersteuerung][MDNUserTimingApi] bestimmte Phasen des App-Lebenszyklus willkürlich kennzeichnen, um zu verfolgen, wie lange diese Phasen dauern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-438">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="aecfc-439">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="aecfc-439">Summary</span></span>   

*   <span data-ttu-id="aecfc-440">Wenn Sie die Auslastungs Leistung einer Website optimieren möchten, beginnen Sie immer mit einer Überwachung.</span><span class="sxs-lookup"><span data-stu-id="aecfc-440">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="aecfc-441">Mit der Überprüfung wird ein Basisplan erstellt, und Sie erhalten Tipps zum verbessern.</span><span class="sxs-lookup"><span data-stu-id="aecfc-441">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="aecfc-442">Führen Sie jeweils eine Änderung durch, und überprüfen Sie die Seite nach jeder Änderung, um zu sehen, wie sich diese isolierte Änderung auf die Leistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-442">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

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
> <span data-ttu-id="aecfc-449">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aecfc-449">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aecfc-450">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="aecfc-450">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="aecfc-452">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aecfc-452">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
