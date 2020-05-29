---
title: Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7efc76fbcb3d1ed6cbd0760f789c8c952030d70c
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611889"
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





# <span data-ttu-id="e6280-103">Optimieren der Website Geschwindigkeit mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="e6280-103">Optimize Website Speed With Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="e6280-104">Ziel des Lernprogramms</span><span class="sxs-lookup"><span data-stu-id="e6280-104">Goal of tutorial</span></span>  

<span data-ttu-id="e6280-105">In diesem Lernprogramm erfahren Sie, wie Sie Microsoft Edge devtools verwenden, um Wege zu finden, wie Sie Ihre Websites schneller laden können.</span><span class="sxs-lookup"><span data-stu-id="e6280-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="e6280-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e6280-106">Prerequisites</span></span>  

*   <span data-ttu-id="e6280-107">Sie sollten über grundlegende Webentwicklungsfunktionen verfügen, ähnlich wie in dieser [Einführung in die Webentwicklungs Klasse][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="e6280-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="e6280-108">Sie müssen nichts über die Ladeleistung wissen.</span><span class="sxs-lookup"><span data-stu-id="e6280-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="e6280-109">In diesem Lernprogramm erfahren Sie mehr darüber!</span><span class="sxs-lookup"><span data-stu-id="e6280-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="e6280-110">Einführung</span><span class="sxs-lookup"><span data-stu-id="e6280-110">Introduction</span></span>   

<span data-ttu-id="e6280-111">Das ist Tony.</span><span class="sxs-lookup"><span data-stu-id="e6280-111">This is Tony.</span></span>  <span data-ttu-id="e6280-112">Tony ist in der Cat Society sehr bekannt.</span><span class="sxs-lookup"><span data-stu-id="e6280-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="e6280-113">Er hat eine Website entwickelt, damit seine Fans mehr über seine bevorzugten Lebensmittel erfahren können.</span><span class="sxs-lookup"><span data-stu-id="e6280-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="e6280-114">Seine Fans lieben die Website, aber Tony hört immer wieder Beschwerden, dass die Website langsam geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="e6280-115">Tony hat Sie gebeten, ihm beim Beschleunigen der Website zu helfen.</span><span class="sxs-lookup"><span data-stu-id="e6280-115">Tony has asked you to help him speed the site up.</span></span>  

> ##### <span data-ttu-id="e6280-116">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="e6280-116">Figure 1</span></span>  
> <span data-ttu-id="e6280-117">Tony the Cat</span><span class="sxs-lookup"><span data-stu-id="e6280-117">Tony the cat</span></span>  
> ![Tony the Cat][ImageTony]  

## <span data-ttu-id="e6280-119">Schritt 1: Überwachen der Website</span><span class="sxs-lookup"><span data-stu-id="e6280-119">Step 1: Audit the site</span></span>   

<span data-ttu-id="e6280-120">Wenn Sie die Ladeleistung einer Website verbessern möchten, **beginnen Sie immer mit einer Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="e6280-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="e6280-121">Das Audit hat zwei wichtige Funktionen:</span><span class="sxs-lookup"><span data-stu-id="e6280-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="e6280-122">Sie erstellt einen **Basisplan** , in dem Sie nachfolgende Änderungen messen können.</span><span class="sxs-lookup"><span data-stu-id="e6280-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="e6280-123">Es gibt Ihnen **umsetzbare Tipps** , welche Änderungen die meisten Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="e6280-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  

### <span data-ttu-id="e6280-124">Einrichtung</span><span class="sxs-lookup"><span data-stu-id="e6280-124">Set up</span></span>   

<span data-ttu-id="e6280-125">Zunächst müssen Sie die Website so einrichten, dass Sie später Änderungen daran vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="e6280-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="e6280-126">[Öffnen Sie den Quellcode für die Website](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="e6280-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="e6280-127">Diese Registerkarte wird als **Registerkarte "Editor"** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e6280-127">This tab is referred to as the **editor tab**.</span></span>  
    
    > ##### <span data-ttu-id="e6280-128">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="e6280-128">Figure 2</span></span>  
    > <span data-ttu-id="e6280-129">Die Registerkarte "Editor"</span><span class="sxs-lookup"><span data-stu-id="e6280-129">The editor tab</span></span>  
    > ![Die Registerkarte "Editor"][ImageEditor]  

1.  <span data-ttu-id="e6280-131">Wählen Sie **Tony**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-131">Select **tony**.</span></span>  <span data-ttu-id="e6280-132">Ein Menü wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6280-132">A menu appears.</span></span>  
    
    > ##### <span data-ttu-id="e6280-133">Abbildung 3</span><span class="sxs-lookup"><span data-stu-id="e6280-133">Figure 3</span></span>  
    > <span data-ttu-id="e6280-134">Das Menü, das nach dem Klicken auf " **Tony** " angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="e6280-134">The menu that appears after clicking **tony**</span></span>  
    > ![Das Menü, das nach dem Klicken auf "Tony" angezeigt wird][ImageMenu]  
    
1.  <span data-ttu-id="e6280-136">Wählen Sie **Remix Project**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-136">Select **Remix Project**.</span></span>  <span data-ttu-id="e6280-137">Der Name des Projekts wechselt von **Tony** zu einem zufällig generierten Namen.</span><span class="sxs-lookup"><span data-stu-id="e6280-137">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="e6280-138">Sie haben jetzt eine eigene bearbeitbare Kopie des Codes.</span><span class="sxs-lookup"><span data-stu-id="e6280-138">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="e6280-139">Später können Sie Änderungen an diesem Code vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e6280-139">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="e6280-140">Wählen Sie **in einem neuen Fenster** **anzeigen** und auswählen aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-140">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="e6280-141">Die Demo wird in einer neuen Registerkarte geöffnet.  Diese Registerkarte wird als **Registerkarte Demo**bezeichnet.  Das Laden der Website kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="e6280-141">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    > ##### <span data-ttu-id="e6280-142">Abbildung4</span><span class="sxs-lookup"><span data-stu-id="e6280-142">Figure 4</span></span>  
    > <span data-ttu-id="e6280-143">Die Registerkarte "Demo"</span><span class="sxs-lookup"><span data-stu-id="e6280-143">The demo tab</span></span>  
    > ![Die Registerkarte "Demo"][ImageDemo]  

1.  <span data-ttu-id="e6280-145">Drücken Sie `Control` + `Shift` + `J` \ (Windows \) oder `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="e6280-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="e6280-146">Microsoft Edge devtools wird parallel zur Demo geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e6280-146">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    > ##### <span data-ttu-id="e6280-147">Abbildung5</span><span class="sxs-lookup"><span data-stu-id="e6280-147">Figure 5</span></span>  
    > <span data-ttu-id="e6280-148">DevTools und die Demo</span><span class="sxs-lookup"><span data-stu-id="e6280-148">DevTools and the demo</span></span>  
    > ![DevTools und die Demo][ImageDevtools]  

<span data-ttu-id="e6280-150">Für die restlichen Screenshots in diesem Lernprogramm wird devtools in einem separaten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6280-150">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="e6280-151">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, einzugeben `Undock` , und wählen Sie dann **in separates Fenster Abdocken**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-151">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

> ##### <span data-ttu-id="e6280-152">Abbildung6</span><span class="sxs-lookup"><span data-stu-id="e6280-152">Figure 6</span></span>  
> <span data-ttu-id="e6280-153">Nicht angedockte devtools</span><span class="sxs-lookup"><span data-stu-id="e6280-153">Undocked DevTools</span></span>  
> ![Nicht angedockte devtools][ImageUndocked]  

### <span data-ttu-id="e6280-155">Festlegen eines Basisplans</span><span class="sxs-lookup"><span data-stu-id="e6280-155">Establish a baseline</span></span>   

<span data-ttu-id="e6280-156">Der Basisplan ist eine Aufzeichnung der Vorgehensweise der Website, bevor Sie Leistungsverbesserungen durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="e6280-156">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="e6280-157">Wählen Sie die Registerkarte **Audits** aus.  **Die** ![ Schaltfläche "Weitere Panels" ist möglicherweise ausgeblendet ][ImageMorePanelsIcon] .</span><span class="sxs-lookup"><span data-stu-id="e6280-157">Select the **Audits** tab.  It may be hidden behind the **More Panels** ![More Panels][ImageMorePanelsIcon] button.</span></span>  <span data-ttu-id="e6280-158">Auf diesem Panel befindet sich ein Leuchtturm, weil das Projekt, das das Audit Panel anbietet, den Namen **Lighthouse**trägt.</span><span class="sxs-lookup"><span data-stu-id="e6280-158">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    > ##### <span data-ttu-id="e6280-159">Abbildung7</span><span class="sxs-lookup"><span data-stu-id="e6280-159">Figure 7</span></span>  
    > <span data-ttu-id="e6280-160">Überwachungs Panel</span><span class="sxs-lookup"><span data-stu-id="e6280-160">The Audits panel</span></span>  
    > ![Überwachungs Panel][ImageAudits]  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="e6280-162">Vergleichen Sie Ihre Überwachungs Konfigurationseinstellungen mit denen in [Abbildung 7](#figure-7).</span><span class="sxs-lookup"><span data-stu-id="e6280-162">Match your audit configuration settings to those in [Figure 7](#figure-7).</span></span>  <span data-ttu-id="e6280-163">Nachfolgend finden Sie eine Erläuterung der verschiedenen Optionen:</span><span class="sxs-lookup"><span data-stu-id="e6280-163">Here is an explanation of the different options:</span></span>  

    *   <span data-ttu-id="e6280-164">**Gerät**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-164">**Device**.</span></span>  <span data-ttu-id="e6280-165">Wenn Sie auf **Mobile** festlegen, ändert sich die Zeichenfolge des Benutzer-Agents und simuliert ein mobiles Viewport.</span><span class="sxs-lookup"><span data-stu-id="e6280-165">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="e6280-166">Durch die Einstellung auf den **Desktop** werden die **mobilen** Änderungen so ziemlich deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e6280-166">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="e6280-167">**Audits**.</span><span class="sxs-lookup"><span data-stu-id="e6280-167">**Audits**.</span></span>  <span data-ttu-id="e6280-168">Durch das Deaktivieren einer Kategorie wird verhindert, dass der Überwachungsbereich diese Audits ausführt, und diese Audits werden aus dem Bericht ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e6280-168">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="e6280-169">Lassen Sie die anderen Kategorien aktiviert, wenn Sie die Typen von Empfehlungen anzeigen möchten, die bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-169">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="e6280-170">Das Deaktivieren von Kategorien beschleunigt den Überwachungsvorgang etwas.</span><span class="sxs-lookup"><span data-stu-id="e6280-170">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="e6280-171">**Einschränkung**.</span><span class="sxs-lookup"><span data-stu-id="e6280-171">**Throttling**.</span></span>  <span data-ttu-id="e6280-172">Einstellung auf **simulierte langsame 4G, vierfache CPU-Verlangsamung** simuliert die typischen Bedingungen für das Browsen auf einem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="e6280-172">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="e6280-173">Sie wird als "simuliert" bezeichnet, da das Überwachungs Panel während des Überwachungsprozesses nicht tatsächlich gedrosselt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-173">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="e6280-174">Stattdessen wird nur extrapoliert, wie lange es dauert, bis die Seite unter mobilen Bedingungen geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="e6280-174">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="e6280-175">Mit der Einstellung " **angewendet...** " wird dagegen Ihre CPU und Ihr Netzwerk tatsächlich gedrosselt, mit dem Kompromiss eines längeren Überwachungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="e6280-175">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="e6280-176">**Speicher löschen**.</span><span class="sxs-lookup"><span data-stu-id="e6280-176">**Clear Storage**.</span></span>  <span data-ttu-id="e6280-177">Wenn Sie dieses Kontrollkästchen aktivieren, wird vor jeder Überwachung der gesamte Speicherplatz gelöscht, der der Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e6280-177">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="e6280-178">Belasse diese Einstellung, wenn Sie überprüfen möchten, wie die Besucher Ihrer Website erst einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="e6280-178">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="e6280-179">Deaktivieren Sie diese Einstellung, wenn Sie die Wiederholungs Besuchs Erfahrung wünschen.</span><span class="sxs-lookup"><span data-stu-id="e6280-179">Disable this setting when you want the repeat-visit experience.</span></span>  

1.  <span data-ttu-id="e6280-180">Wählen Sie **Audits ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-180">Select **Run Audits**.</span></span>  <span data-ttu-id="e6280-181">Nach 10 bis 30 Sekunden wird im Überwachungs Panel ein Bericht über die Leistung der Website angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6280-181">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    > ##### <span data-ttu-id="e6280-182">Abbildung8</span><span class="sxs-lookup"><span data-stu-id="e6280-182">Figure 8</span></span>  
    > <span data-ttu-id="e6280-183">Der Bericht für das Audits-Panel über die Leistung der Website</span><span class="sxs-lookup"><span data-stu-id="e6280-183">The report for the Audits panel of the performance of the site</span></span>  
    > ![Der Bericht für das Audits-Panel über die Leistung der Website][ImageReport]  

#### <span data-ttu-id="e6280-185">Behandeln von Berichts Fehlern</span><span class="sxs-lookup"><span data-stu-id="e6280-185">Handling report errors</span></span>   

<span data-ttu-id="e6280-186">Wenn Sie in Ihrem Audits-Panel-Bericht jemals eine Fehlermeldung erhalten, versuchen Sie, die Registerkarte Demo in einem **InPrivate** -Fenster auszuführen, ohne dass weitere Registerkarten geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="e6280-186">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="e6280-187">Dadurch wird sichergestellt, dass Sie Microsoft Edge in einem sauberen Zustand ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6280-187">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="e6280-188">Insbesondere Microsoft-Edge-Erweiterungen stören häufig den Überwachungsprozess.</span><span class="sxs-lookup"><span data-stu-id="e6280-188">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
> ##### old Figure 9  
> A report that errored  
> ![A report that errored][ImageError]  
-->  

### <span data-ttu-id="e6280-189">Grundlegendes zu Ihrem Bericht</span><span class="sxs-lookup"><span data-stu-id="e6280-189">Understand your report</span></span>   

<span data-ttu-id="e6280-190">Die Zahl am oberen Rand des Berichts entspricht dem Gesamtleistungsfaktor für die Website.</span><span class="sxs-lookup"><span data-stu-id="e6280-190">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="e6280-191">Wenn Sie später Änderungen am Code vornehmen, sollte diese Zahl steigen.</span><span class="sxs-lookup"><span data-stu-id="e6280-191">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="e6280-192">Eine höhere Punktzahl bedeutet eine bessere Leistung.</span><span class="sxs-lookup"><span data-stu-id="e6280-192">A higher score means better performance.</span></span>  

> ##### <span data-ttu-id="e6280-193">Abbildung 9</span><span class="sxs-lookup"><span data-stu-id="e6280-193">Figure 9</span></span>  
> <span data-ttu-id="e6280-194">Der Gesamtleistungsfaktor</span><span class="sxs-lookup"><span data-stu-id="e6280-194">The overall performance score</span></span>  
> <span data-ttu-id="e6280-195">! [Der Gesamtleistungsfaktor] [Imagegesamt]</span><span class="sxs-lookup"><span data-stu-id="e6280-195">![The overall performance score][ImageOverall]</span></span>  

<span data-ttu-id="e6280-196">Der Abschnitt **Metriken** bietet quantitative Maße für die Leistung der Website.</span><span class="sxs-lookup"><span data-stu-id="e6280-196">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="e6280-197">Jede Metrik bietet Einblicke in einen anderen Aspekt der Leistung.</span><span class="sxs-lookup"><span data-stu-id="e6280-197">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="e6280-198">Beispielsweise erfahren Sie in der **ersten Inhaltsfarbe** , wann Inhalte zuerst auf dem Bildschirm gemalt werden, was ein wichtiger Meilenstein für die Wahrnehmung der Seitenauslastung durch den Benutzer ist, während die **Zeit für interaktive** Kennzeichnung den Punkt angibt, an dem die Seite für die Behandlung von Benutzerinteraktionen bereit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-198">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

> ##### <span data-ttu-id="e6280-199">Abbildung 10</span><span class="sxs-lookup"><span data-stu-id="e6280-199">Figure 10</span></span>  
> <span data-ttu-id="e6280-200">Abschnitt "Metriken"</span><span class="sxs-lookup"><span data-stu-id="e6280-200">The Metrics section</span></span>  
> <span data-ttu-id="e6280-201">! [Der Abschnitt ' Metriken '] [Imagemetrics]</span><span class="sxs-lookup"><span data-stu-id="e6280-201">![The Metrics section][ImageMetrics]</span></span>  

<span data-ttu-id="e6280-202">Wählen Sie in [Abbildung 11](#figure-11) die hervorgehobene Umschaltfläche aus, um eine Beschreibung für jede Metrik anzuzeigen, und klicken Sie auf **Weitere Informationen** , um die Dokumentation dazu zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e6280-202">Select the highlighted toggle button in [Figure 11](#figure-11) to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

> ##### <span data-ttu-id="e6280-203">Abbildung 11</span><span class="sxs-lookup"><span data-stu-id="e6280-203">Figure 11</span></span>  
> <span data-ttu-id="e6280-204">Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der **Metriken** Elemente</span><span class="sxs-lookup"><span data-stu-id="e6280-204">Select the highlighted toggle button to expand the **Metrics** items</span></span>  
> <span data-ttu-id="e6280-205">! [Wählen Sie die hervorgehobene Umschaltfläche aus, um die Elemente für Metriken zu erweitern] [ImageFirstMeaningfulPaint]</span><span class="sxs-lookup"><span data-stu-id="e6280-205">![Select the highlighted toggle button to expand the Metrics items][ImageFirstMeaningfulPaint]</span></span>  

<span data-ttu-id="e6280-206">Unter Metriken finden Sie eine Sammlung von Screenshots, die Ihnen zeigen, wie die Seite beim Laden aussah.</span><span class="sxs-lookup"><span data-stu-id="e6280-206">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

> ##### <span data-ttu-id="e6280-207">Abbildung 12</span><span class="sxs-lookup"><span data-stu-id="e6280-207">Figure 12</span></span>  
> <span data-ttu-id="e6280-208">Screenshots, wie die Seite beim Laden aussah</span><span class="sxs-lookup"><span data-stu-id="e6280-208">Screenshots of how the page looked while loading</span></span>  
> <span data-ttu-id="e6280-209">! [Screenshots, wie die Seite während des Ladens aussah] [Imagescreenshots]</span><span class="sxs-lookup"><span data-stu-id="e6280-209">![Screenshots of how the page looked while loading][ImageScreenshots]</span></span>  

<span data-ttu-id="e6280-210">Im Abschnitt " **Verkaufschancen** " finden Sie spezielle Tipps zum Verbessern der Auslastungs Leistung dieser bestimmten Seite.</span><span class="sxs-lookup"><span data-stu-id="e6280-210">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

> ##### <span data-ttu-id="e6280-211">Abbildung 13</span><span class="sxs-lookup"><span data-stu-id="e6280-211">Figure 13</span></span>  
> <span data-ttu-id="e6280-212">Der Abschnitt "Verkaufschancen"</span><span class="sxs-lookup"><span data-stu-id="e6280-212">The Opportunities section</span></span>  
> <span data-ttu-id="e6280-213">! [Der Abschnitt "Verkaufschancen"] [Imageopportunities]</span><span class="sxs-lookup"><span data-stu-id="e6280-213">![The Opportunities section][ImageOpportunities]</span></span>  

<span data-ttu-id="e6280-214">Wählen Sie eine Gelegenheit aus, um mehr darüber zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="e6280-214">Select an opportunity to learn more about it.</span></span>  

> ##### <span data-ttu-id="e6280-215">Abbildung 14</span><span class="sxs-lookup"><span data-stu-id="e6280-215">Figure 14</span></span>  
> <span data-ttu-id="e6280-216">**Eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e6280-216">**Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="e6280-217">! [Eliminieren der Render-Blockierung von Ressourcen – Opportunity] [Imagekomprimierung]</span><span class="sxs-lookup"><span data-stu-id="e6280-217">![Eliminate render-blocking resources opportunity][ImageCompression]</span></span>  

<span data-ttu-id="e6280-218">Wählen Sie **Weitere Informationen** aus, um die Dokumentation dazu anzuzeigen, warum eine Verkaufschance wichtig ist, und spezifische Empfehlungen zur Behebung.</span><span class="sxs-lookup"><span data-stu-id="e6280-218">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

> ##### <span data-ttu-id="e6280-219">Abbildung 15</span><span class="sxs-lookup"><span data-stu-id="e6280-219">Figure 15</span></span>  
> <span data-ttu-id="e6280-220">Dokumentation für die Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e6280-220">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="e6280-221">! [Dokumentation für die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen] [Imagereference]</span><span class="sxs-lookup"><span data-stu-id="e6280-221">![Documentation for the Eliminate render-blocking resources opportunity][ImageReference]</span></span>  

<span data-ttu-id="e6280-222">Der Abschnitt **Diagnostics** enthält weitere Informationen zu Faktoren, die zur Ladezeit der Seite beitragen.</span><span class="sxs-lookup"><span data-stu-id="e6280-222">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

> ##### <span data-ttu-id="e6280-223">Abbildung 16</span><span class="sxs-lookup"><span data-stu-id="e6280-223">Figure 16</span></span>  
> <span data-ttu-id="e6280-224">Abschnitt "Diagnose"</span><span class="sxs-lookup"><span data-stu-id="e6280-224">The Diagnostics section</span></span>  
> <span data-ttu-id="e6280-225">! [Der Abschnitt Diagnose] [Imagediagnostics]</span><span class="sxs-lookup"><span data-stu-id="e6280-225">![The Diagnostics section][ImageDiagnostics]</span></span>  

<span data-ttu-id="e6280-226">Im Abschnitt "übertragene **Prüfungen** " wird gezeigt, was die Website richtig macht.</span><span class="sxs-lookup"><span data-stu-id="e6280-226">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="e6280-227">Wählen Sie diese Option aus, um den Abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="e6280-227">Select to expand the section.</span></span>  

> ##### <span data-ttu-id="e6280-228">Abbildung 17</span><span class="sxs-lookup"><span data-stu-id="e6280-228">Figure 17</span></span>  
> <span data-ttu-id="e6280-229">Abschnitt "übergebene Überprüfungen"</span><span class="sxs-lookup"><span data-stu-id="e6280-229">The Passed Audits section</span></span>  
> <span data-ttu-id="e6280-230">! [Der Abschnitt ' übertragene Audits] [Imagepassed]</span><span class="sxs-lookup"><span data-stu-id="e6280-230">![The Passed Audits section][ImagePassed]</span></span>  

## <span data-ttu-id="e6280-231">Schritt 2: experimentieren</span><span class="sxs-lookup"><span data-stu-id="e6280-231">Step 2: Experiment</span></span>   

<span data-ttu-id="e6280-232">Im Abschnitt "Verkaufschancen" Ihres Überwachungsberichts erhalten Sie Tipps, wie Sie die Leistung der Seite verbessern können.</span><span class="sxs-lookup"><span data-stu-id="e6280-232">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="e6280-233">In diesem Abschnitt implementieren Sie die empfohlenen Änderungen an der CodeBase, indem Sie die Website nach jeder Änderung überwachen, um zu messen, wie sich dies auf die Geschwindigkeit der Website auswirkt.</span><span class="sxs-lookup"><span data-stu-id="e6280-233">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="e6280-234">Aktivieren der Text Komprimierung</span><span class="sxs-lookup"><span data-stu-id="e6280-234">Enable text compression</span></span>   

<span data-ttu-id="e6280-235">Ihr Bericht besagt, dass die Vermeidung von enormen Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="e6280-235">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="e6280-236">Das Aktivieren der Text Komprimierung bietet die Möglichkeit, die Leistung der Seite zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="e6280-236">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="e6280-237">Die Text Komprimierung erfolgt, wenn Sie die Größe einer Textdatei reduzieren oder komprimieren, bevor Sie Sie über das Netzwerk senden.</span><span class="sxs-lookup"><span data-stu-id="e6280-237">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="e6280-238">Eine Art gefällt Ihnen, wie Sie einen Ordner komprimieren können, bevor Sie ihn per e-Mail senden, um die Größe zu verringern.</span><span class="sxs-lookup"><span data-stu-id="e6280-238">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="e6280-239">Bevor Sie die Komprimierung aktivieren, gibt es eine Reihe von Möglichkeiten, um manuell zu überprüfen, ob Textressourcen komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-239">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="e6280-240">Wählen Sie die Registerkarte **Netzwerk** aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-240">Select the **Network** tab.</span></span>  
    
    > ##### <span data-ttu-id="e6280-241">Abbildung 18</span><span class="sxs-lookup"><span data-stu-id="e6280-241">Figure 18</span></span>  
    > <span data-ttu-id="e6280-242">Netzwerk Panel</span><span class="sxs-lookup"><span data-stu-id="e6280-242">The Network panel</span></span>  
    > <span data-ttu-id="e6280-243">! [Netzwerk Panel] [Imagenetwork]</span><span class="sxs-lookup"><span data-stu-id="e6280-243">![The Network panel][ImageNetwork]</span></span>  
    
1.  <span data-ttu-id="e6280-244">Wählen Sie das Symbol **Netzwerkeinstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-244">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="e6280-245">Aktivieren Sie das Kontrollkästchen **große Anforderungs Zeilen verwenden** .</span><span class="sxs-lookup"><span data-stu-id="e6280-245">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="e6280-246">Die Höhe der Zeilen in der Tabelle der Netzwerkanforderungen nimmt zu.</span><span class="sxs-lookup"><span data-stu-id="e6280-246">The height of the rows in the table of network requests increases.</span></span>  
    
    > ##### <span data-ttu-id="e6280-247">Abbildung 19</span><span class="sxs-lookup"><span data-stu-id="e6280-247">Figure 19</span></span>  
    > <span data-ttu-id="e6280-248">Große Zeilen in der Tabelle "Netzwerkanforderungen"</span><span class="sxs-lookup"><span data-stu-id="e6280-248">Large rows in the network requests table</span></span>  
    > <span data-ttu-id="e6280-249">! [Große Zeilen in der Tabelle ' Netzwerkanforderungen '] [ImageLargeRows]</span><span class="sxs-lookup"><span data-stu-id="e6280-249">![Large rows in the network requests table][ImageLargeRows]</span></span>  
    
1.  <span data-ttu-id="e6280-250">Wenn die Spalte **Größe** in der Tabelle der Netzwerkanforderungen nicht angezeigt wird, klicken Sie auf die Tabellenüberschrift, und wählen Sie dann **Größe**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-250">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="e6280-251">Jede **Größen** Zelle enthält zwei Werte.</span><span class="sxs-lookup"><span data-stu-id="e6280-251">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="e6280-252">Der oberste Wert ist die Größe der heruntergeladenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="e6280-252">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="e6280-253">Der untere Wert gibt die Größe der unkomprimierten Ressource an.</span><span class="sxs-lookup"><span data-stu-id="e6280-253">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="e6280-254">Wenn die beiden Werte identisch sind, wird die Ressource nicht komprimiert, wenn Sie über das Netzwerk gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-254">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="e6280-255">In [Abbildung 19](#figure-19) finden Sie beispielsweise die oberen und unteren Werte für " `bundle.js` sind" und " `1.2 MB` `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="e6280-255">For example, in [Figure 19](#figure-19) the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="e6280-256">Überprüfen Sie auf Komprimierung, indem Sie die HTTP-Header einer Ressource prüfen:</span><span class="sxs-lookup"><span data-stu-id="e6280-256">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="e6280-257">Wählen Sie **Bundle. js**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-257">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="e6280-258">Wählen Sie die Registerkarte über **Schriften** aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-258">Select the **Headers** tab.</span></span>  
    
    > ##### <span data-ttu-id="e6280-259">Abbildung 20</span><span class="sxs-lookup"><span data-stu-id="e6280-259">Figure 20</span></span>  
    > <span data-ttu-id="e6280-260">Die Registerkarte "Überschriften"</span><span class="sxs-lookup"><span data-stu-id="e6280-260">The Headers tab</span></span>  
    > <span data-ttu-id="e6280-261">! [Die Registerkarte ' Überschriften '] [Imageheaders]</span><span class="sxs-lookup"><span data-stu-id="e6280-261">![The Headers tab][ImageHeaders]</span></span>  
    
1.  <span data-ttu-id="e6280-262">Durchsuchen Sie den Abschnitt **Antwort Kopfzeilen** nach einer `content-encoding` Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="e6280-262">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="e6280-263">Sie sollten keines sehen, was bedeutet, dass es sich nicht um eine `bundle.js` Komprimierung handelt.</span><span class="sxs-lookup"><span data-stu-id="e6280-263">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="e6280-264">Wenn eine Ressource komprimiert ist, wird in der Regel dieser Header auf `gzip` , `deflate` oder gesetzt `br` .</span><span class="sxs-lookup"><span data-stu-id="e6280-264">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="e6280-265">Eine Erläuterung dieser Werte finden Sie unter [Direktiven][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="e6280-265">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="e6280-266">Genug mit den Erläuterungen.</span><span class="sxs-lookup"><span data-stu-id="e6280-266">Enough with the explanations.</span></span>  <span data-ttu-id="e6280-267">Zeit, einige Änderungen vorzunehmen!</span><span class="sxs-lookup"><span data-stu-id="e6280-267">Time to make some changes!</span></span>  <span data-ttu-id="e6280-268">Aktivieren Sie die Text Komprimierung, indem Sie ein paar Codezeilen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="e6280-268">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="e6280-269">Klicken Sie auf der Registerkarte Editor auf **Server. js**.</span><span class="sxs-lookup"><span data-stu-id="e6280-269">In the editor tab, click **server.js**.</span></span>  
    
    > ##### <span data-ttu-id="e6280-270">Abbildung 21</span><span class="sxs-lookup"><span data-stu-id="e6280-270">Figure 21</span></span>  
    > <span data-ttu-id="e6280-271">Bearbeiten von Server. js</span><span class="sxs-lookup"><span data-stu-id="e6280-271">Editing server.js</span></span>  
    > <span data-ttu-id="e6280-272">! [Bearbeiten von Server. js] Helios</span><span class="sxs-lookup"><span data-stu-id="e6280-272">![Editing server.js][ImageServer]</span></span>  
    
1.  <span data-ttu-id="e6280-273">Fügen Sie den folgenden Code zu " **Server. js**" hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6280-273">Add the following code to **server.js**.</span></span>  <span data-ttu-id="e6280-274">Stellen Sie sicher, dass Sie dies tun `app.use(compression())` `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="e6280-274">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

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
    > <span data-ttu-id="e6280-275">In der Regel müssen Sie das `compression` Paket über einen ähnlichen `npm i -S compression` Vorgang installieren, dies wurde aber bereits für Sie erledigt.</span><span class="sxs-lookup"><span data-stu-id="e6280-275">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="e6280-276">Warten Sie, bis glitch den neuen Build der Website bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="e6280-276">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="e6280-277">Die raffinierte Animation neben **Tools** bedeutet, dass die Website neu erstellt und erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-277">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="e6280-278">Die Änderung ist fertig, wenn die Animation neben **Tools** verschwindet.</span><span class="sxs-lookup"><span data-stu-id="e6280-278">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="e6280-279">Wählen Sie wieder **in einem neuen Fenster** **anzeigen** und auswählen aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-279">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    > ##### Old Figure 22  
    > The animation that indicates that the site is getting built  
    > ![The animation that indicates that the site is getting built][ImageBuilding]  
    -->  
    
<span data-ttu-id="e6280-280">Verwenden Sie die zuvor gelernten Workflows, um manuell zu überprüfen, ob die Komprimierung funktioniert:</span><span class="sxs-lookup"><span data-stu-id="e6280-280">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="e6280-281">Wechseln Sie zur Registerkarte Demo zurück, und laden Sie die Seite neu.</span><span class="sxs-lookup"><span data-stu-id="e6280-281">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="e6280-282">In der Spalte **Größe** sollten nun zwei unterschiedliche Werte für Textressourcen wie angezeigt werden `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="e6280-282">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="e6280-283">In [Abbildung 23](#figure-23) ist der oberste Wert von `256 KB` für `bundle.js` die Größe der Datei, die über das Netzwerk gesendet wurde, und der untere Wert von `1.2 MB` ist die unkomprimierte Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="e6280-283">In [Figure 23](#figure-23) the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    > ##### <span data-ttu-id="e6280-284">Abbildung 22</span><span class="sxs-lookup"><span data-stu-id="e6280-284">Figure 22</span></span>  
    > <span data-ttu-id="e6280-285">In der Spalte "Größe" werden nun zwei unterschiedliche Werte für Textressourcen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6280-285">The Size column now shows 2 different values for text resources</span></span>  
    > <span data-ttu-id="e6280-286">! [In der Spalte ' Größe ' werden nun zwei unterschiedliche Werte für Textressourcen angezeigt] [Imagerequests]</span><span class="sxs-lookup"><span data-stu-id="e6280-286">![The Size column now shows 2 different values for text resources][ImageRequests]</span></span>  
    
1.  <span data-ttu-id="e6280-287">Im Abschnitt " **Antwort Kopfzeilen** " `bundle.js` sollte nun eine `content-encoding: gzip` Kopfzeile enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="e6280-287">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    > ##### <span data-ttu-id="e6280-288">Abbildung 23</span><span class="sxs-lookup"><span data-stu-id="e6280-288">Figure 23</span></span>  
    > <span data-ttu-id="e6280-289">Der Abschnitt "Antwort Kopfzeilen" enthält jetzt einen Inhalts Codierungs Header.</span><span class="sxs-lookup"><span data-stu-id="e6280-289">The Response Headers section now contains a content-encoding header</span></span>  
    > <span data-ttu-id="e6280-290">! [Der Abschnitt "Antwort Kopfzeilen" enthält jetzt einen Content-Encoding-Header] [Imagegzip]</span><span class="sxs-lookup"><span data-stu-id="e6280-290">![The Response Headers section now contains a content-encoding header][ImageGzip]</span></span>  
    
<span data-ttu-id="e6280-291">Überwachen Sie die Seite erneut, um zu messen, welche Art von Auswirkungen die Text Komprimierung auf die Ladeleistung der Seite hat:</span><span class="sxs-lookup"><span data-stu-id="e6280-291">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="e6280-292">Wählen Sie die Registerkarte **Audits** aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-292">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="e6280-293">Wählen Sie Audit durchführen einer Überwachung durch **führen** aus ![ ][ImagePerformIcon] .</span><span class="sxs-lookup"><span data-stu-id="e6280-293">Select **Perform an audit** ![Perform an audit][ImagePerformIcon].</span></span>  
1.  <span data-ttu-id="e6280-294">Belasse die Einstellungen wie zuvor.</span><span class="sxs-lookup"><span data-stu-id="e6280-294">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="e6280-295">Wählen Sie **Audit ausführen**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-295">Select **Run audit**.</span></span>  
    
    > ##### <span data-ttu-id="e6280-296">Abbildung 24</span><span class="sxs-lookup"><span data-stu-id="e6280-296">Figure 24</span></span>  
    > <span data-ttu-id="e6280-297">Ein Überwachungsbericht nach der Aktivierung der Text Komprimierung</span><span class="sxs-lookup"><span data-stu-id="e6280-297">An Audits report after enabling text compression</span></span>  
    > <span data-ttu-id="e6280-298">! [Ein Auditbericht nach der Aktivierung der Text Komprimierung] [ImageReport2]</span><span class="sxs-lookup"><span data-stu-id="e6280-298">![An Audits report after enabling text compression][ImageReport2]</span></span>  
    
<span data-ttu-id="e6280-299">Woohoo!</span><span class="sxs-lookup"><span data-stu-id="e6280-299">Woohoo!</span></span>  <span data-ttu-id="e6280-300">Das sieht wie ein Fortschritt aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-300">That looks like progress.</span></span>  <span data-ttu-id="e6280-301">Ihr Gesamtleistungsfaktor sollte zugenommen haben, was bedeutet, dass die Website schneller wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-301">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="e6280-302">Text Komprimierung in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="e6280-302">Text compression in the real world</span></span>   

<span data-ttu-id="e6280-303">Bei den meisten Servern gibt es wirklich einfache Fehlerbehebungen wie diese zum Aktivieren von Komprimierung!</span><span class="sxs-lookup"><span data-stu-id="e6280-303">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="e6280-304">Führen Sie einfach eine Suche durch, um zu konfigurieren, welcher Server zum Komprimieren von Text verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-304">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="e6280-305">Ändern der Größe von Bildern</span><span class="sxs-lookup"><span data-stu-id="e6280-305">Resize images</span></span>   

<span data-ttu-id="e6280-306">Ihr Bericht weist darauf hin, dass die Vermeidung enormer Netzwerklasten eine der besten Möglichkeiten zur Verbesserung der Leistung der Seite darstellt.</span><span class="sxs-lookup"><span data-stu-id="e6280-306">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="e6280-307">Durch Ändern der Größe von Bildern kann die Größe der Netzwerk Nutzlast verringert werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-307">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="e6280-308">Wenn der Benutzer Ihre Bilder auf einem Bildschirm mit einem mobilen Gerät anzeigt, der 500 Pixel breit ist, ist es wirklich unwichtig, ein 1500-Pixel breites Bild zu senden.</span><span class="sxs-lookup"><span data-stu-id="e6280-308">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="e6280-309">Im Idealfall senden Sie höchstens ein Bild mit einer Breite von 500 Pixel.</span><span class="sxs-lookup"><span data-stu-id="e6280-309">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="e6280-310">Klicken Sie in Ihrem Bericht auf **enorme Netzwerk Nutzlasten vermeiden** , um festzustellen, welche Bilder geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6280-310">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="e6280-311">Es sieht so aus, als ob 2 der JPG-Dateien über 2000 KB liegen, was größer als notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="e6280-311">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    > ##### Old Figure 27  
    > Details about the **Properly size images** opportunity  
    > ![Details about the properly size images opportunity][ImageResize]  
    -->

1.  <span data-ttu-id="e6280-312">Zurück auf der Registerkarte "Editor" Öffnen `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="e6280-312">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="e6280-313">Ersetzen Sie `const dir = 'big'` durch `const dir = 'small'`.</span><span class="sxs-lookup"><span data-stu-id="e6280-313">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="e6280-314">Dieses Verzeichnis enthält Kopien der gleichen Bilder, deren Größe geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e6280-314">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="e6280-315">Überprüfen Sie die Seite erneut, um zu sehen, wie sich diese Änderung auf die Ladeleistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="e6280-315">Audit the page again to see how this change affects load performance.</span></span>  
    
    > ##### <span data-ttu-id="e6280-316">Abbildung 25</span><span class="sxs-lookup"><span data-stu-id="e6280-316">Figure 25</span></span>  
    > <span data-ttu-id="e6280-317">Ein Überwachungsbericht nach dem Ändern der Größe von Bildern</span><span class="sxs-lookup"><span data-stu-id="e6280-317">An Audits report after resizing images</span></span>  
    > <span data-ttu-id="e6280-318">! [Ein Überwachungsbericht nach dem Ändern der Größe von Bildern] [ImageReport3]</span><span class="sxs-lookup"><span data-stu-id="e6280-318">![An Audits report after resizing images][ImageReport3]</span></span>  

<span data-ttu-id="e6280-319">Sieht so aus, als ob die Änderung nur eine geringfügige Auswirkung auf den Gesamtleistungsfaktor hat.</span><span class="sxs-lookup"><span data-stu-id="e6280-319">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="e6280-320">Die Punktzahl zeigt jedoch nicht eindeutig, wie viel Netzwerkdaten Sie für Ihre Benutzer speichern.</span><span class="sxs-lookup"><span data-stu-id="e6280-320">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="e6280-321">Die Gesamtgröße der alten Fotos betrug etwa 5,3 Megabyte, während es jetzt nur noch etwa 0,18 Megabytes gibt.</span><span class="sxs-lookup"><span data-stu-id="e6280-321">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="e6280-322">Ändern der Größe von Bildern in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="e6280-322">Resizing images in the real world</span></span>   

<span data-ttu-id="e6280-323">Bei einer kleinen app kann eine einmalige Größenänderung so gut wie möglich sein.</span><span class="sxs-lookup"><span data-stu-id="e6280-323">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="e6280-324">Bei einer umfangreichen APP ist dies natürlich nicht skalierbar.</span><span class="sxs-lookup"><span data-stu-id="e6280-324">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="e6280-325">Im folgenden finden Sie einige Strategien zum Verwalten von Bildern in umfangreichen apps:</span><span class="sxs-lookup"><span data-stu-id="e6280-325">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="e6280-326">Ändern der Größe von Bildern während des Buildprozesses</span><span class="sxs-lookup"><span data-stu-id="e6280-326">Resize images during your build process.</span></span>  
*   <span data-ttu-id="e6280-327">Erstellen Sie mehrere Größen der einzelnen Bilder während des Buildprozesses, und verwenden `srcset` Sie Sie dann in Ihrem Code.</span><span class="sxs-lookup"><span data-stu-id="e6280-327">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="e6280-328">Zur Laufzeit sorgt der Browser dafür, welche Größe für das Gerät am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="e6280-328">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->

<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="e6280-329">Verwenden Sie ein Image CDN, mit dem Sie die Größe eines Bilds dynamisch ändern können, wenn Sie es anfordern.</span><span class="sxs-lookup"><span data-stu-id="e6280-329">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="e6280-330">Optimieren Sie zumindest jedes Bild.</span><span class="sxs-lookup"><span data-stu-id="e6280-330">At the very least, optimize each image.</span></span>  <span data-ttu-id="e6280-331">Dies kann zu enormen Einsparungen führen.</span><span class="sxs-lookup"><span data-stu-id="e6280-331">This may create huge savings.</span></span>  
  <span data-ttu-id="e6280-332">Optimierung ist, wenn Sie ein Bild über ein spezielles Programm ausführen, das die Größe der Bilddatei reduziert.</span><span class="sxs-lookup"><span data-stu-id="e6280-332">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="e6280-333">Weitere Tipps finden Sie unter [grundlegende Bildoptimierung][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="e6280-333">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  

### <span data-ttu-id="e6280-334">Eliminieren von Render-Blockierungs Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6280-334">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="e6280-335">Ihr neuester Bericht besagt, dass das Eliminieren von Render-Blockierungs Ressourcen jetzt die größte Chance darstellt.</span><span class="sxs-lookup"><span data-stu-id="e6280-335">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="e6280-336">Eine Render-Blockierungs Ressource ist eine externe JavaScript-oder CSS-Datei, die vom Browser heruntergeladen, analysiert und ausgeführt werden muss, bevor die Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-336">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="e6280-337">Das Ziel besteht darin, nur den zentralen CSS-und JavaScript-Code auszuführen, der erforderlich ist, um die Seite ordnungsgemäß anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e6280-337">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="e6280-338">Die erste Aufgabe besteht darin, Code zu finden, den Sie beim Laden der Seite nicht ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="e6280-338">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="e6280-339">Wählen Sie **Render-Blockierungs Ressourcen eliminieren** aus, um die blockierten Ressourcen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="e6280-339">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="e6280-340">und `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="e6280-340">and `jquery.js`.</span></span>  
    
    > ##### <span data-ttu-id="e6280-341">Abbildung 26</span><span class="sxs-lookup"><span data-stu-id="e6280-341">Figure 26</span></span>  
    > <span data-ttu-id="e6280-342">Weitere Informationen zur Möglichkeit zum **eliminieren von Render-Blockierungs Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e6280-342">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    > <span data-ttu-id="e6280-343">! [Weitere Informationen über die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen] [Imagerender]</span><span class="sxs-lookup"><span data-stu-id="e6280-343">![More information about the Eliminate render-blocking resources opportunity][ImageRender]</span></span>  
    
1.  <span data-ttu-id="e6280-344">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü zu öffnen, mit der Eingabe zu beginnen `Coverage` , und wählen Sie dann **Coverage anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-344">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    > ##### <span data-ttu-id="e6280-345">Abbildung 27</span><span class="sxs-lookup"><span data-stu-id="e6280-345">Figure 27</span></span>  
    > <span data-ttu-id="e6280-346">Öffnen des Befehlsmenüs im Überwachungs Panel</span><span class="sxs-lookup"><span data-stu-id="e6280-346">Opening the Command Menu from the Audits panel</span></span>  
    > <span data-ttu-id="e6280-347">! [Öffnen des Befehlsmenüs im Überwachungs Panel] [ImageCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="e6280-347">![Opening the Command Menu from the Audits panel][ImageCommandMenu]</span></span>  
    
    > ##### <span data-ttu-id="e6280-348">Abbildung 28</span><span class="sxs-lookup"><span data-stu-id="e6280-348">Figure 28</span></span>  
    > <span data-ttu-id="e6280-349">Die Registerkarte "Coverage"</span><span class="sxs-lookup"><span data-stu-id="e6280-349">The Coverage tab</span></span>  
    > <span data-ttu-id="e6280-350">! [Die Registerkarte ' Berichterstattung '] [Imagebelag]</span><span class="sxs-lookup"><span data-stu-id="e6280-350">![The Coverage tab][ImageCoverage]</span></span>  
    
1.  <span data-ttu-id="e6280-351">Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="e6280-351">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="e6280-352">Die Registerkarte **Coverage** bietet eine Übersicht darüber, wie viel des Codes in `bundle.js` , `jquery.js` und `lodash.js` ausgeführt wird, während die Seite geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-352">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="e6280-353">[Abbildung 30](#figure-30) besagt, dass etwa 76% und 30% der jQuery-und Lodash-Dateien nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-353">[Figure 30](#figure-30) says that about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    > ##### <span data-ttu-id="e6280-354">Abbildung 29</span><span class="sxs-lookup"><span data-stu-id="e6280-354">Figure 29</span></span>  
    > <span data-ttu-id="e6280-355">Der Bericht "Berichterstattung"</span><span class="sxs-lookup"><span data-stu-id="e6280-355">The Coverage report</span></span>  
    > <span data-ttu-id="e6280-356">! [Der Bericht zur Berichterstattung] [ImageCoverageReport]</span><span class="sxs-lookup"><span data-stu-id="e6280-356">![The Coverage report][ImageCoverageReport]</span></span>  
    
1.  <span data-ttu-id="e6280-357">Wählen Sie die Zeile **jQuery. js** aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-357">Select the **jquery.js** row.</span></span>  <span data-ttu-id="e6280-358">DevTools öffnet die Datei im Quellen Panel.</span><span class="sxs-lookup"><span data-stu-id="e6280-358">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="e6280-359">Eine Codezeile wird ausgeführt, wenn Sie einen blauen Balken Daneben hat.</span><span class="sxs-lookup"><span data-stu-id="e6280-359">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="e6280-360">Eine rote Leiste bedeutet, dass Sie nicht ausgeführt wurde und beim Laden der Seite definitiv nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-360">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    > ##### <span data-ttu-id="e6280-361">Abbildung 30</span><span class="sxs-lookup"><span data-stu-id="e6280-361">Figure 30</span></span>  
    > <span data-ttu-id="e6280-362">Anzeigen der jQuery-Datei im Quellen Panel</span><span class="sxs-lookup"><span data-stu-id="e6280-362">Viewing the jQuery file in the Sources panel</span></span>  
    > <span data-ttu-id="e6280-363">! [Anzeigen der jQuery-Datei im Quellen Panel] [Imagejquery]</span><span class="sxs-lookup"><span data-stu-id="e6280-363">![Viewing the jQuery file in the Sources panel][ImageJQuery]</span></span>  
    
1.  <span data-ttu-id="e6280-364">Scrollen Sie ein wenig durch den jQuery-Code.</span><span class="sxs-lookup"><span data-stu-id="e6280-364">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="e6280-365">Einige der Zeilen, die "Run" erhalten, sind eigentlich nur Kommentare.</span><span class="sxs-lookup"><span data-stu-id="e6280-365">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="e6280-366">Wenn Sie diesen Code über einen minifier ausführen, der Kommentare entfernt, ist eine weitere Möglichkeit, die Größe dieser Datei zu verringern.</span><span class="sxs-lookup"><span data-stu-id="e6280-366">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="e6280-367">Kurz gesagt: Wenn Sie mit Ihrem eigenen Code arbeiten, können Sie mithilfe der Registerkarte Coverage Ihren Code, Zeile für Zeile, analysieren und nur den Code versenden, der für die Seitenauslastung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-367">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="e6280-368">Sind die `jquery.js` und `lodash.js` Dateien auch zum Laden der Seite erforderlich?</span><span class="sxs-lookup"><span data-stu-id="e6280-368">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="e6280-369">Auf der Registerkarte Anforderungs Blockierung wird angezeigt, was geschieht, wenn keine Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e6280-369">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="e6280-370">Wählen Sie die Registerkarte **Netzwerk** aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-370">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="e6280-371">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das Befehlsmenü erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e6280-371">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="e6280-372">Beginnen `blocking` Sie mit der Eingabe, und wählen Sie dann **Anforderungs Blockierung anzeigen**aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-372">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    > ##### <span data-ttu-id="e6280-373">Abbildung 31</span><span class="sxs-lookup"><span data-stu-id="e6280-373">Figure 31</span></span>  
    > <span data-ttu-id="e6280-374">Die Registerkarte ' Anforderungs Blockierung '</span><span class="sxs-lookup"><span data-stu-id="e6280-374">The Request Blocking tab</span></span>  
    > <span data-ttu-id="e6280-375">! [Die Registerkarte ' Anforderungs Blockierung] [Imageblocking]</span><span class="sxs-lookup"><span data-stu-id="e6280-375">![The Request Blocking tab][ImageBlocking]</span></span>  
    
1.  <span data-ttu-id="e6280-376">Wählen Sie **Muster** hinzufügen hinzufügen aus ![ , geben Sie ein ][ImageAddPatternIcon] `/libs/*` , und drücken Sie dann `Enter` , um zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="e6280-376">Select **Add Pattern** ![Add Pattern][ImageAddPatternIcon], type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    > ##### <span data-ttu-id="e6280-377">Abbildung 32</span><span class="sxs-lookup"><span data-stu-id="e6280-377">Figure 32</span></span>  
    > <span data-ttu-id="e6280-378">Hinzufügen eines Musters zum Blockieren einer Anforderung an das `libs` Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="e6280-378">Adding a pattern to block any request to the `libs` directory</span></span>  
    > <span data-ttu-id="e6280-379">! [Hinzufügen eines Musters, um eine Anfrage an das libs-Verzeichnis zu blockieren] [Imagelibs]</span><span class="sxs-lookup"><span data-stu-id="e6280-379">![Adding a pattern to block any request to the libs directory][ImageLibs]</span></span>  
    
1.  <span data-ttu-id="e6280-380">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e6280-380">Refresh the page.</span></span>  <span data-ttu-id="e6280-381">Die Anforderungen für jQuery und Lodash sind rot, was bedeutet, dass die Anforderungen blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e6280-381">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="e6280-382">Da die Seite immer noch geladen und interaktiv ist, sieht es so aus, als ob diese Ressourcen überhaupt nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-382">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    > ##### <span data-ttu-id="e6280-383">Abbildung 33</span><span class="sxs-lookup"><span data-stu-id="e6280-383">Figure 33</span></span>  
    > <span data-ttu-id="e6280-384">Das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e6280-384">The Network panel shows that the requests have been blocked</span></span>  
    > <span data-ttu-id="e6280-385">! [Das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden] [ImageBlockedLibs]</span><span class="sxs-lookup"><span data-stu-id="e6280-385">![The Network panel shows that the requests have been blocked][ImageBlockedLibs]</span></span>  
    
1.  <span data-ttu-id="e6280-386">Wählen Sie **alle** Muster entfernen aus ![ ][ImageRemoveIcon] , um das `/libs/*` Blockierungs Muster zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e6280-386">Select **Remove all patterns** ![Remove all patterns][ImageRemoveIcon] to delete the `/libs/*` blocking pattern.</span></span>  

<span data-ttu-id="e6280-387">Im Allgemeinen ist die Registerkarte Anforderungs Blockierung hilfreich, um zu simulieren, wie sich die Seite verhält, wenn eine bestimmte Ressource nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e6280-387">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="e6280-388">Entfernen Sie nun die Verweise auf diese Dateien aus dem Code, und überwachen Sie die Seite erneut:</span><span class="sxs-lookup"><span data-stu-id="e6280-388">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="e6280-389">Zurück auf der Registerkarte "Editor" Öffnen `template.html` .</span><span class="sxs-lookup"><span data-stu-id="e6280-389">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="e6280-390">Löschen Sie `<script src="/libs/lodash.js">` und `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="e6280-390">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="e6280-391">Warten Sie, bis die Website neu erstellt und erneut bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-391">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="e6280-392">Überwachen Sie die Seite im **Überwachungs** Panel erneut.</span><span class="sxs-lookup"><span data-stu-id="e6280-392">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="e6280-393">Ihre Gesamtpunktzahl sollte erneut verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-393">Your overall score should have improved again.</span></span>  
    
    > ##### <span data-ttu-id="e6280-394">Abbildung 34</span><span class="sxs-lookup"><span data-stu-id="e6280-394">Figure 34</span></span>  
    > <span data-ttu-id="e6280-395">Ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6280-395">An Audits report after removing the render-blocking resources</span></span>  
    > <span data-ttu-id="e6280-396">! [Ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen] [ImageReport4]</span><span class="sxs-lookup"><span data-stu-id="e6280-396">![An Audits report after removing the render-blocking resources][ImageReport4]</span></span>  

#### <span data-ttu-id="e6280-397">Optimieren des kritischen Rendering-Pfads in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="e6280-397">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="e6280-398">Der **kritische Rendering-Pfad** bezieht sich auf den Code, der zum Laden einer Seite erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e6280-398">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="e6280-399">Im Allgemeinen können Sie die Seitenauslastung beschleunigen, indem Sie nur den Versand von kritischem Code während des Ladens der Seite durchführen und dann alles andere verzögert laden.</span><span class="sxs-lookup"><span data-stu-id="e6280-399">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="e6280-400">Es ist unwahrscheinlich, dass Sie in der Lage sind, Skripts zu finden, die Sie direkt entfernen können, aber möglicherweise viele Skripts finden, die Sie beim Laden der Seite nicht anfordern müssen, und stattdessen möglicherweise asynchron angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-400">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="e6280-401">Wenn Sie ein Framework verwenden, überprüfen Sie, ob es einen Produktionsmodus aufweist.</span><span class="sxs-lookup"><span data-stu-id="e6280-401">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="e6280-402">In diesem Modus wird möglicherweise ein Feature wie das [schütteln von Strukturen][WebpackTreeShaking] verwendet, um unnötigen Code zu eliminieren, der das kritische Rendern blockiert.</span><span class="sxs-lookup"><span data-stu-id="e6280-402">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  

<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="e6280-403">Arbeiten mit einem geringeren Hauptthread</span><span class="sxs-lookup"><span data-stu-id="e6280-403">Do less main thread work</span></span>   

<span data-ttu-id="e6280-404">Ihr neuester Bericht zeigt einige kleinere potenzielle Einsparungen im Abschnitt "Verkaufschancen", aber wenn Sie im Abschnitt "Diagnose" nach unten suchen, sieht es so aus, als wäre der größte Engpass zu viel Hauptthread Aktivität.</span><span class="sxs-lookup"><span data-stu-id="e6280-404">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="e6280-405">Der Hauptthread ist der Ort, an dem der Browser die meiste Arbeit ausführt, die zum Anzeigen einer Seite erforderlich ist, beispielsweise das analysieren und Ausführen von HTML, CSS und JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e6280-405">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="e6280-406">Das Ziel besteht darin, mithilfe des Leistungs Panels zu analysieren, welche Arbeit der Hauptthread beim Laden der Seite unternimmt, und Wege zu finden, um unnötige Arbeit zu verzögern oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e6280-406">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="e6280-407">Wählen Sie die Registerkarte **Leistung** aus.</span><span class="sxs-lookup"><span data-stu-id="e6280-407">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="e6280-408">Wählen Sie Einstellungen für Aufnahme **Einstellungen** aus ![ ][ImageCaptureIcon] .</span><span class="sxs-lookup"><span data-stu-id="e6280-408">Select **Capture Settings** ![Capture Settings][ImageCaptureIcon].</span></span>  
1.  <span data-ttu-id="e6280-409">**Netzwerk** auf **langsame 3G** -und **CPU** -zu- **6x-Verlangsamung**einstellen.</span><span class="sxs-lookup"><span data-stu-id="e6280-409">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="e6280-410">Bei mobilen Geräten gibt es in der Regel mehr Hardwareeinschränkungen als Laptops oder Desktops, sodass Sie mit diesen Einstellungen das Laden der Seite so erleben können, als ob Sie ein weniger leistungsfähiges Gerät verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="e6280-410">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="e6280-411">Wählen **Sie Aktualisierung aktualisieren aus** ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="e6280-411">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="e6280-412">DevTools aktualisiert die Seite und erstellt dann eine Visualisierung aller ausgeführten Arbeiten, um die Seite zu laden.</span><span class="sxs-lookup"><span data-stu-id="e6280-412">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="e6280-413">Diese Visualisierung wird als **Ablaufverfolgung**bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e6280-413">This visualization is referred to as the **trace**.</span></span>  
    
    > ##### <span data-ttu-id="e6280-414">Abbildung 35</span><span class="sxs-lookup"><span data-stu-id="e6280-414">Figure 35</span></span>  
    > <span data-ttu-id="e6280-415">Der Leistungs Panel-Ablaufverfolgung der Seitenauslastung</span><span class="sxs-lookup"><span data-stu-id="e6280-415">The Performance panel trace of the page load</span></span>  
    > <span data-ttu-id="e6280-416">! [Der Leistungs Panel-Ablaufverfolgung der Seitenauslastung] [Imageperformance]</span><span class="sxs-lookup"><span data-stu-id="e6280-416">![The Performance panel trace of the page load][ImagePerformance]</span></span>  

<span data-ttu-id="e6280-417">Die Ablaufverfolgung zeigt die Aktivität chronologisch an, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="e6280-417">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="e6280-418">Die oben dargestellten fps-, CPU-und net-Diagramme geben Ihnen einen Überblick über Frames pro Sekunde, CPU-Aktivität und Netzwerkaktivität.</span><span class="sxs-lookup"><span data-stu-id="e6280-418">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="e6280-419">Der in [Abbildung 37](#figure-37) ausgewählte gelb markierte Block bedeutet, dass die CPU vollständig mit Skriptaktivitäten ausgelastet war.</span><span class="sxs-lookup"><span data-stu-id="e6280-419">The block of yellow selected that you see in [Figure 37](#figure-37) means that the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="e6280-420">Dies ist ein Hinweis darauf, dass Sie möglicherweise die Seitenauslastung beschleunigen können, indem Sie eine geringere JavaScript-Arbeit durchführen.</span><span class="sxs-lookup"><span data-stu-id="e6280-420">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

> ##### <span data-ttu-id="e6280-421">Abbildung 36</span><span class="sxs-lookup"><span data-stu-id="e6280-421">Figure 36</span></span>  
> <span data-ttu-id="e6280-422">Der Abschnitt "Übersicht" der Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="e6280-422">The Overview section of the trace</span></span>  
> <span data-ttu-id="e6280-423">! [Der Abschnitt ' Übersicht ' der Ablaufverfolgung] [Imageoverview]</span><span class="sxs-lookup"><span data-stu-id="e6280-423">![The Overview section of the trace][ImageOverview]</span></span>  

<span data-ttu-id="e6280-424">Untersuchen Sie die Ablaufverfolgung, um Möglichkeiten für eine geringere JavaScript-Arbeit zu finden:</span><span class="sxs-lookup"><span data-stu-id="e6280-424">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="e6280-425">Wählen Sie den Abschnitt **Anzeige** dauern aus, um ihn zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="e6280-425">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="e6280-426">Basierend auf der Tatsache, dass es möglicherweise eine Reihe von [Timings][MDNUserTimingApi] -Maßnahmen von reagieren gibt, scheint es so zu sein, als ob die APP von Tony die Entwicklungsmethode von reagieren verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6280-426">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="e6280-427">Wenn Sie auf den Produktionsmodus von reagieren umstellen, kann dies einige einfache Leistungsgewinne hervorbringen.</span><span class="sxs-lookup"><span data-stu-id="e6280-427">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    > ##### <span data-ttu-id="e6280-428">Abbildung 37</span><span class="sxs-lookup"><span data-stu-id="e6280-428">Figure 37</span></span>  
    > <span data-ttu-id="e6280-429">Abschnitt "Anzeigedauern"</span><span class="sxs-lookup"><span data-stu-id="e6280-429">The Timings section</span></span>  
    > <span data-ttu-id="e6280-430">! [Der Abschnitt "Anzeigedauer"] [ImageUserTiming]</span><span class="sxs-lookup"><span data-stu-id="e6280-430">![The Timings section][ImageUserTiming]</span></span>  

1.  <span data-ttu-id="e6280-431">Wählen Sie erneut **Anzeige** dauern aus, um den Abschnitt zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="e6280-431">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="e6280-432">Durchsuchen Sie den **Haupt** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="e6280-432">Browse the **Main** section.</span></span>  <span data-ttu-id="e6280-433">Dieser Abschnitt zeigt ein chronologisches Protokoll der Hauptthread Aktivität, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="e6280-433">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="e6280-434">Die y-Achse (von oben nach unten) zeigt, warum Ereignisse aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e6280-434">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="e6280-435">In [Abbildung 39](#figure-39)führte das Ereignis beispielsweise dazu, dass die Funktion ausgeführt wurde, die zur Ausführung führte, `Evaluate Script` `(anonymous)` `(anonymous)` die `__webpack__require__` zur Ausführung führte usw.</span><span class="sxs-lookup"><span data-stu-id="e6280-435">For example, in [Figure 39](#figure-39), the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    > ##### <span data-ttu-id="e6280-436">Abbildung 38</span><span class="sxs-lookup"><span data-stu-id="e6280-436">Figure 38</span></span>  
    > <span data-ttu-id="e6280-437">Der Hauptabschnitt</span><span class="sxs-lookup"><span data-stu-id="e6280-437">The Main section</span></span>  
    > <span data-ttu-id="e6280-438">! [Der Hauptbereich] [Imagemain]</span><span class="sxs-lookup"><span data-stu-id="e6280-438">![The Main section][ImageMain]</span></span>  

1.  <span data-ttu-id="e6280-439">Scrollen Sie nach unten zum unteren Rand des **Haupt** Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="e6280-439">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="e6280-440">Wenn Sie ein Framework verwenden, wird der größte Teil der oberen Aktivität durch das Framework verursacht, das normalerweise außerhalb des Steuerelements liegt.</span><span class="sxs-lookup"><span data-stu-id="e6280-440">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="e6280-441">Die von Ihrer APP verursachte Aktivität befindet sich normalerweise unten.</span><span class="sxs-lookup"><span data-stu-id="e6280-441">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="e6280-442">In dieser app scheint es so zu sein, dass eine Funktion mit dem Namen `App` viele Anforderungen an eine `mineBitcoin` Funktion verursacht.</span><span class="sxs-lookup"><span data-stu-id="e6280-442">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="e6280-443">Es klingt wie Tony könnte die Geräte seiner Fans verwenden, um cryptocurrency zu vergruben...</span><span class="sxs-lookup"><span data-stu-id="e6280-443">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    > ##### <span data-ttu-id="e6280-444">Abbildung 39</span><span class="sxs-lookup"><span data-stu-id="e6280-444">Figure 39</span></span>  
    > <span data-ttu-id="e6280-445">Über die Aktivität zeigen `mineBitcoin`</span><span class="sxs-lookup"><span data-stu-id="e6280-445">Hovering over the `mineBitcoin` activity</span></span>  
    > <span data-ttu-id="e6280-446">! [Schwebt über der mineBitcoin-Aktivität] [Imagemine]</span><span class="sxs-lookup"><span data-stu-id="e6280-446">![Hovering over the mineBitcoin activity][ImageMine]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e6280-447">Obwohl die Anforderungen, die Ihr Framework macht, in der Regel nicht in Ihrem Steuerelement enthalten sind, können Sie Ihre APP manchmal so strukturieren, dass das Framework ineffizient ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-447">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="e6280-448">Die Umstrukturierung ihrer App zur effizienten Verwendung des Frameworks ist eine Möglichkeit, um die Arbeit am Hauptthread zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="e6280-448">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="e6280-449">Dies erfordert jedoch ein umfassendes Verständnis der Funktionsweise des Frameworks und der Art von Änderungen, die Sie in Ihrem eigenen Code vornehmen, um das Framework effizienter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6280-449">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  

1.  <span data-ttu-id="e6280-450">Erweitern Sie den Abschnitt **Bottom-up** .</span><span class="sxs-lookup"><span data-stu-id="e6280-450">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="e6280-451">Auf dieser Registerkarte wird aufgeschlüsselt, welche Aktivitäten die meiste Zeit in Anspruch genommen haben.</span><span class="sxs-lookup"><span data-stu-id="e6280-451">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="e6280-452">Wenn im Abschnitt Bottom-up nichts angezeigt wird, klicken Sie auf die Beschriftung für **Haupt** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="e6280-452">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="e6280-453">Der **Bottom-up-** Abschnitt zeigt nur Informationen zu einer beliebigen Aktivität oder Aktivitätsgruppe, die Sie aktuell ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="e6280-453">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="e6280-454">Wenn Sie beispielsweise auf eine der Aktivitäten geklickt haben `mineBitcoin` , werden im Abschnitt **Bottom-up** nur Informationen für diese Aktivität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6280-454">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    > ##### <span data-ttu-id="e6280-455">Abbildung 40</span><span class="sxs-lookup"><span data-stu-id="e6280-455">Figure 40</span></span>  
    > <span data-ttu-id="e6280-456">Die Registerkarte "Bottom-up"</span><span class="sxs-lookup"><span data-stu-id="e6280-456">The Bottom-Up tab</span></span>  
    > <span data-ttu-id="e6280-457">! [Die untere Registerkarte] [ImageBottomUp]</span><span class="sxs-lookup"><span data-stu-id="e6280-457">![The Bottom-Up tab][ImageBottomUp]</span></span>  

<span data-ttu-id="e6280-458">In der Spalte **selbst Zeit** wird angezeigt, wie viel Zeit direkt in den einzelnen Aktivitäten aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e6280-458">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="e6280-459">[Abbildung 41](#figure-41) zeigt beispielsweise, dass etwa 63% der Hauptthread Zeit für die Funktion aufgewendet wurden `mineBitcoin` .</span><span class="sxs-lookup"><span data-stu-id="e6280-459">For example, [Figure 41](#figure-41) shows that about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="e6280-460">Zeit, um zu sehen, ob die Auslastung der Seite durch Verwenden des Produktionsmodus und verringern der JavaScript-Aktivität beschleunigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6280-460">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="e6280-461">Beginnen mit dem Produktionsmodus:</span><span class="sxs-lookup"><span data-stu-id="e6280-461">Start with production mode:</span></span>  

1.  <span data-ttu-id="e6280-462">Öffnen Sie auf der Registerkarte Editor den Reiter `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="e6280-462">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="e6280-463">Ändern Sie `"mode":"development"` in `"mode":"production"`.</span><span class="sxs-lookup"><span data-stu-id="e6280-463">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="e6280-464">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-464">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="e6280-465">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="e6280-465">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="e6280-466">Abbildung 41</span><span class="sxs-lookup"><span data-stu-id="e6280-466">Figure 41</span></span>  
    > <span data-ttu-id="e6280-467">Ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus</span><span class="sxs-lookup"><span data-stu-id="e6280-467">An Audits report after configuring webpack to use production mode</span></span>  
    > <span data-ttu-id="e6280-468">! [Ein Auditbericht nach der Konfiguration von WebPack zur Verwendung des Produktionsmodus] [ImageReport5]</span><span class="sxs-lookup"><span data-stu-id="e6280-468">![An Audits report after configuring webpack to use production mode][ImageReport5]</span></span>  

<span data-ttu-id="e6280-469">Reduzieren Sie die JavaScript-Aktivität, indem Sie die Anforderung entfernen an `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="e6280-469">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="e6280-470">Öffnen Sie auf der Registerkarte Editor den Reiter `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="e6280-470">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="e6280-471">Kommentieren Sie die Anforderung `this.mineBitcoin(1500)` in `constructor` .</span><span class="sxs-lookup"><span data-stu-id="e6280-471">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="e6280-472">Warten Sie, bis der neue Build bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e6280-472">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="e6280-473">Überwachen Sie die Seite erneut.</span><span class="sxs-lookup"><span data-stu-id="e6280-473">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="e6280-474">Abbildung 42</span><span class="sxs-lookup"><span data-stu-id="e6280-474">Figure 42</span></span>  
    > <span data-ttu-id="e6280-475">Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit</span><span class="sxs-lookup"><span data-stu-id="e6280-475">An Audits report after removing unnecessary JavaScript work</span></span>  
    > <span data-ttu-id="e6280-476">! [Ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit] [ImageReport6]</span><span class="sxs-lookup"><span data-stu-id="e6280-476">![An Audits report after removing unnecessary JavaScript work][ImageReport6]</span></span>  

<span data-ttu-id="e6280-477">Sieht so aus, als ob diese letzte Änderung einen massiven Sprung in der Leistung verursacht hat!</span><span class="sxs-lookup"><span data-stu-id="e6280-477">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="e6280-478">Dieser Abschnitt enthält eine relativ kurze Einführung in das Leistungs Panel.</span><span class="sxs-lookup"><span data-stu-id="e6280-478">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="e6280-479">Weitere Informationen zum Analysieren der Seitenleistung finden Sie unter [Referenz zur Leistungsanalyse][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="e6280-479">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="e6280-480">Arbeiten mit einem niedrigeren Hauptthread in der realen Welt</span><span class="sxs-lookup"><span data-stu-id="e6280-480">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="e6280-481">Im Allgemeinen ist der Bereich " **Leistung** " die häufigste Methode, um zu verstehen, welche Aktivitäten Ihre Website während der Auslastung durchführt, und Möglichkeiten zum Entfernen unnötiger Aktivitäten zu finden.</span><span class="sxs-lookup"><span data-stu-id="e6280-481">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="e6280-482">Wenn Sie einen Ansatz bevorzugen, der sich eher wie anfühlt `console.log()` , können Sie mit der API für die [Benutzersteuerung][MDNUserTimingApi] bestimmte Phasen des App-Lebenszyklus willkürlich kennzeichnen, um zu verfolgen, wie lange diese Phasen dauern.</span><span class="sxs-lookup"><span data-stu-id="e6280-482">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="e6280-483">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="e6280-483">Summary</span></span>   

*   <span data-ttu-id="e6280-484">Wenn Sie die Auslastungs Leistung einer Website optimieren möchten, beginnen Sie immer mit einer Überwachung.</span><span class="sxs-lookup"><span data-stu-id="e6280-484">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="e6280-485">Mit der Überprüfung wird ein Basisplan erstellt, und Sie erhalten Tipps zum verbessern.</span><span class="sxs-lookup"><span data-stu-id="e6280-485">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="e6280-486">Führen Sie jeweils eine Änderung durch, und überprüfen Sie die Seite nach jeder Änderung, um zu sehen, wie sich diese isolierte Änderung auf die Leistung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="e6280-486">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--    -->  



<!-- image links -->  

[ImageAddPatternIcon]: /microsoft-edge/devtools-guide-chromium/media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-panels-icon.msft.png  
[ImagePerformIcon]: /microsoft-edge/devtools-guide-chromium/media/perform-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRemoveIcon]: /microsoft-edge/devtools-guide-chromium/media/remove-icon.msft.png  

[ImageTony]: /microsoft-edge/devtools-guide-chromium/media/speed-tony.msft.png "Abbildung 1: Tony the Cat"  
[ImageEditor]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js.msft.png "Abbildung 2: die Registerkarte "Editor""  
[ImageMenu]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js-remix-project.msft.png "Abbildung 3: das Menü, das nach dem Klicken auf "Tony" angezeigt wird"  
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live.msft.png "Abbildung 4: die Registerkarte "Demo""  
[ImageDevtools]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live-console.msft.png "Abbildung 5: devtools und die Demo"  
[ImageUndocked]: /microsoft-edge/devtools-guide-chromium/media/speed-console.msft.png "Abbildung 6: nicht angedockte devtools"  
[ImageAudits]: /microsoft-edge/devtools-guide-chromium/media/speed-audits-performance.msft.png "Abbildung 7: Überwachungs Panel"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png "Abbildung 8: der Bericht für das Audits-Panel zur Leistung der Website"  
<!--[ImageError]: /microsoft-edge/devtools-guide-chromium/media/speed-.msft.png "Old Figure 9: A report that errored"  -->  
[Imagegesamt]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Metrics-Collapsed-Metrics-highlighted.msft.png "Abbildung 9: der Gesamtleistungsfaktor"
[ImageOverall]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png "Figure 9: The overall performance score"  
[Imagemetrics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Metrics-Collapsed-highlighted.msft.png "Abbildung 10: der Abschnitt" Metriken "
[ImageMetrics]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png "Figure 10: The Metrics section"  
[ImageFirstMeaningfulPaint]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Metrics-Expanded.msft.png "Abbildung 11: Auswählen der hervorgehobenen Umschaltfläche zum Erweitern der Metriken"  
[Imagescreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-View-Trace.msft.png "Abbildung 12: Screenshots, wie die Seite beim Laden aussah"
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png "Figure 12: Screenshots of how the page looked while loading"  
[Imageopportunities]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Opportunities.msft.png "Abbildung 13: der Abschnitt" Verkaufschancen "
[ImageOpportunities]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-opportunities.msft.png "Figure 13: The Opportunities section"  
[Imagecompression]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Opportunities-Expanded.msft.png "Abbildung 14: eliminieren von Render-Blockierungs Ressourcen"
[ImageCompression]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png "Figure 14: Eliminate render-blocking resources opportunity"  
[Imagereference]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Web-dev-Performance-Audits.msft.png "Abbildung 15: Dokumentation für die Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen"
[ImageReference]: /microsoft-edge/devtools-guide-chromium/media/speed-web-dev-performance-audits.msft.png "Figure 15: Documentation for the Eliminate render-blocking resources opportunity"  
[Imagediagnostics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-Diagnostics.msft.png "Abbildung 16: der Abschnitt" Diagnose "
[ImageDiagnostics]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png "Figure 16: The Diagnostics section"  
[Imagepassed]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Audits-Performance-passed-Audits.msft.png "Abbildung 17: der Abschnitt" übergebene Überprüfungen "
[ImagePassed]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png "Figure 17: The Passed Audits section"  
[Imagenetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network.msft.png "Abbildung 18: Netzwerk Panel"
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-network.msft.png "Figure 18: The Network panel"  
[ImageLargeRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-use-Large-Request-Rows.msft.png "Abbildung 19: große Zeilen in der Tabelle" Netzwerkanforderungen "  
[Imageheaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-use-Large-Request-Rows-Bundle-js.msft.png "Abbildung 20: die Registerkarte" Überschriften "
[ImageHeaders]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png "Figure 20: The Headers tab"  
[ImageServer]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Server-js.msft.png "Abbildung 21: Bearbeiten von Server. js"  
<!--[ImageBuilding]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-server-js-edited.msft.png "Old Figure 22: The animation that indicates that the site is getting built"  -->  
[Imagerequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-Main.msft.png "Abbildung 22: die Spalte" Größe "zeigt jetzt zwei unterschiedliche Werte für Textressourcen an."
[ImageRequests]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-network-main.msft.png "Figure 22: The Size column now shows 2 different values for text resources"  
[Imagegzip]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-Bundle-js-Headers-Response.msft.png "Abbildung 23: der Abschnitt mit den Antwortheadern enthält jetzt eine `content-encoding` Kopfzeile"
[ImageGzip]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png "Figure 23: The Response Headers section now contains a `content-encoding` header"  
[ImageReport2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance.msft.png "Abbildung 24: ein Überwachungsbericht nach der Aktivierung der Text Komprimierung"  
<!--[ImageResize]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png "Old Figure 27: Details about the properly size images opportunity"  -->
[ImageReport3]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Compression-Small-Images-Audits-Performance.msft.png "Abbildung 25: ein Überwachungsbericht nach dem Ändern der Größe von Bildern"  
[Imagerender]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded.msft.png "Abbildung 26: Weitere Informationen zur Möglichkeit zum Eliminieren von Render-Blockierungs Ressourcen"
[ImageRender]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png "Figure 26: More information about the Eliminate render-blocking resources opportunity"  
[ImageCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded-Command-Coverage.msft.png "Abbildung 27: Öffnen des Befehlsmenüs im Überwachungs Panel  
[Imagedeckment]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded-drawer-Coverage.msft.png "Abbildung 28: die Registerkarte" Abdeckung "
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png "Figure 28: The Coverage tab"  
[ImageCoverageReport]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Audits-Performance-oppportunities-Expanded-drawer-Coverage-Reloaded.msft.png "Abbildung 29: der Coverage-Bericht"  
[Imagejquery]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-sources-drawer-Coverage-Reloaded-jQuery-js.msft.png "Abbildung 30: Anzeigen der jQuery-Datei im Quellen Panel"
[ImageJQuery]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png "Figure 30: Viewing the jQuery file in the Sources panel"  
[Imageblocking]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-network-drawer-Request-Blocking-Empty.msft.png "Abbildung 31: die Registerkarte" Anforderungs Blockierung "
[ImageBlocking]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png "Figure 31: The Request Blocking tab"  
[Imagelibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-network-drawer-Request-Blocking-Added.msft.png "Abbildung 32: Hinzufügen eines Musters zum Blockieren einer Anforderung an das libs-Verzeichnis"
[ImageLibs]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png "Figure 32: Adding a pattern to block any request to the libs directory"  
[ImageBlockedLibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-network-Reloaded-drawer-Request-Blocking-Added.msft.png "Abbildung 33: das Netzwerk Panel zeigt, dass die Anforderungen blockiert wurden"  
[ImageReport4]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-2-Audits-Performance.msft.png "Abbildung 34: ein Überwachungsbericht nach dem Entfernen der Render-Blockierungs Ressourcen"  
[Imageperformance]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU.msft.png "Abbildung 35: die Spur des Leistungs Panels der Seitenlast"
[ImagePerformance]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png "Figure 35: The Performance panel trace of the page load"  
[Imageoverview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Main-Highlight.msft.png "Abbildung 36: der Abschnitt" Übersicht "der Ablaufverfolgung"
[ImageOverview]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png "Figure 36: The Overview section of the trace"  
[ImageUserTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Timings.msft.png "Abbildung 37: der Abschnitt" Anzeigedauer "  
[Imagemain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Main.msft.png "Abbildung 38: der Hauptabschnitt"
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png "Figure 38: The Main section"  
[Imagemine]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Timings-minebitcoin.msft.png "Abbildung 39: Hovern über die minebitcoin-Aktivität"
[ImageMine]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png "Figure 39: Hovering over the mineBitcoin activity"  
[ImageBottomUp]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Performance-Slow-Network-Slow-CPU-Timings-Summary-minebitcoin.msft.png "Abbildung 40: die Bottom-up-Registerkarte"  
[ImageReport5]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-3-Audits-Performance.msft.png "Abbildung 41: ein Überwachungsbericht nach der Konfiguration von WebPack für die Verwendung des Produktionsmodus"  
[ImageReport6]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-4-Audits-Performance.msft.png "Abbildung 42: ein Überwachungsbericht nach dem Entfernen unnötiger JavaScript-Arbeit"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referenz zur Leistungsanalyse"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Einführung in die Webentwicklungs Klasse | Coursera"  

[EssentialImageOptimization]: https://images.guide "Essentielle Bildoptimierung"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Direktiven – Inhaltscodierung | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Benutzer-Timing-API | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Baum Erschütterung | WebPack"  

> [!NOTE]
> <span data-ttu-id="e6280-535">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6280-535">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e6280-536">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6280-536">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="e6280-538">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e6280-538">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
