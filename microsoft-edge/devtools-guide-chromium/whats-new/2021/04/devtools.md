---
description: Wavy unterstreicht Codeprobleme im Elementtool, in der Zeitachse für Dienstarbeitsaktualisierungen und vieles mehr.
title: Neues in DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 5f499a6c9f1109f80a9d459edf94ed2226734f19
ms.sourcegitcommit: 87ba918b0910373bb645615377709bf140dc9b19
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "11583459"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="d7501-104">Neues in DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="d7501-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="d7501-105">Wavy unterstreicht Codeprobleme und Verbesserungen im Elementtool</span><span class="sxs-lookup"><span data-stu-id="d7501-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="d7501-106">In den meisten modernen IDEs weisen wellenförmige Unterstreichungen unter Text auf Syntaxfehler hin.</span><span class="sxs-lookup"><span data-stu-id="d7501-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="d7501-107">In Microsoft Edge Version 91 oder höher werden wellenförmige Unterstreichungen unter HTML in der **DOM-Ansicht** des **Elements-Tools** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="d7501-108">Die wellenförmigen Unterstreichungen deuten auf Codeprobleme und Vorschläge im Zusammenhang mit Barrierefreiheit, Kompatibilität, Leistung und so weiter hin.</span><span class="sxs-lookup"><span data-stu-id="d7501-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="d7501-109">Weitere Informationen zum Überprüfen und Bearbeiten von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="d7501-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="d7501-110">Führen Sie **eine** der folgenden Aktionen aus, um das Problem zu öffnen und mehr über das Problem und die Behebung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="d7501-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="d7501-111">Wählen Sie `Shift` aus, halten Sie , und wählen Sie dann eine beliebige wellenförmige Unterstreichung aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="d7501-112">Führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="d7501-113">Zeigen Sie auf eine beliebige wellenförmige Unterstreichung.</span><span class="sxs-lookup"><span data-stu-id="d7501-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="d7501-114">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="d7501-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="d7501-115">Wählen **Sie In Problemen anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="d7501-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Wählen Sie den unterstrichenen Fehler im Elementtool aus." lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="d7501-117">Wählen Sie den unterstrichenen Fehler im **Elementtool** aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Anzeigen von Fehlerdetails im Problemtool" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="d7501-119">Anzeigen von Fehlerdetails im **Problemtool**</span><span class="sxs-lookup"><span data-stu-id="d7501-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="d7501-120">Mehr über DevTools mit informativen QuickInfos erfahren</span><span class="sxs-lookup"><span data-stu-id="d7501-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="d7501-121">Das DevTools-Tooltips-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche in DevTools zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="d7501-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="d7501-122">Wählen Sie aus, um QuickInfos zu `Esc` deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7501-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="d7501-123">Führen Sie eine der folgenden Aktionen aus, um QuickInfos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7501-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="d7501-124">Wählen `Ctrl` + `Shift` + `H` Sie \(Windows/Linux\) oder `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="d7501-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="d7501-125">[Öffnen Sie das Befehlsmenü,][DevtoolsCommandMenuIndexOpenCommandMenu] und geben Sie dann `tooltips` ein.</span><span class="sxs-lookup"><span data-stu-id="d7501-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="d7501-126">Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > **Hilfe**Umschalten der  >  **DevTools-QuickInfos**.</span><span class="sxs-lookup"><span data-stu-id="d7501-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="d7501-127">Wenn Sie außerdem das Experiment Fokusmodus und [DevTools-Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] aktivieren, können Sie auch die Schaltfläche **DevTools Tooltips** \( \) am unteren Rand der Aktivitätsleiste umschalten. `?` \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7501-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="d7501-128">Wenn Sie weitere Informationen zur Verwendung der DevTools anzeigen möchten, aktivieren Sie QuickInfos, und zeigen Sie dann auf die einzelnen umrissenen Regionen der DevTools.</span><span class="sxs-lookup"><span data-stu-id="d7501-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des Problemtools, um weitere Details anzuzeigen." lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="d7501-130">Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des **Problemtools,** um weitere Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7501-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="d7501-131">Zeitachse der Dienstarbeitsmitarbeiteraktualisierung</span><span class="sxs-lookup"><span data-stu-id="d7501-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="d7501-132">In Microsoft Edge Version 91 oder höher, wenn Sie Entwickler von Progressive Web App oder Service Worker sind, zeigen Sie den Updatelebenszyklus Ihrer Service Workers als Zeitachse im Anwendungstool **an.**</span><span class="sxs-lookup"><span data-stu-id="d7501-132">In Microsoft Edge version 91 or later, if you're a Progressive Web App or Service Worker developer, display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="d7501-133">Dieses Feature hilft Ihnen, die Zeit zu verstehen, die Ihr Dienstmitarbeiter in den folgenden Phasen verbringt.</span><span class="sxs-lookup"><span data-stu-id="d7501-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="d7501-134">Installieren</span><span class="sxs-lookup"><span data-stu-id="d7501-134">Install</span></span>**  
*   **<span data-ttu-id="d7501-135">Warte</span><span class="sxs-lookup"><span data-stu-id="d7501-135">Wait</span></span>**  
*   **<span data-ttu-id="d7501-136">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="d7501-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Überprüfen der Zeitachse im Aktualisierungszyklus für Ihren Service Worker" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="d7501-138">Überprüfen der **Zeitachse** im **Aktualisierungszyklus für** Ihren Service Worker</span><span class="sxs-lookup"><span data-stu-id="d7501-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="d7501-139">Weitere Informationen zum Lebenszyklus Ihrer Service Workers finden Sie unter [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span><span class="sxs-lookup"><span data-stu-id="d7501-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="d7501-140">Weitere Informationen zu Debuggingtools für Progressive Web Apps and Service Workers in den DevTools finden Sie unter [Service Worker improvements][DevtoolsServiceWorkerIndex].</span><span class="sxs-lookup"><span data-stu-id="d7501-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="d7501-141">Navigieren Sie zu Issue [1066604,][CR1066604]um die Echtzeitupdates für dieses Feature Chromium open-source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7501-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="d7501-142">Progressive Web Apps zeigen keine Warnungen mehr für nicht quadratische Symbole an</span><span class="sxs-lookup"><span data-stu-id="d7501-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="d7501-143">Wenn [Microsoft Edge Version 90][DevtoolsWhatsNew202102Devtools] oder früher ein nicht quadratisches Symbol enthält, wurde im Abschnitt Fehler und Warnungen für jedes nicht quadratische Symbol eine Warnung angezeigt, wenn das Web-App-Manifest Ihres PWA ein nicht quadratisches Symbol enthielt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7501-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if the Web App Manifest of your PWA included a non-square icon, a warning was displayed in the **Errors and Warnings**  section for each non-square icon.</span></span>  <span data-ttu-id="d7501-144">In Microsoft Edge Version 91 oder höher werden \*\*\*\* im **Abschnitt Manifest** im Anwendungstool keine Warnungen angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d7501-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="d7501-145">Wenn Sie keine quadratischen Symbole bereitstellen, wird die folgende Meldung in einer Warnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt." lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="d7501-147">In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="d7501-149">In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen</span><span class="sxs-lookup"><span data-stu-id="d7501-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d7501-150">Um Fehler und Warnungen in Ihrem Web App-Manifest zu überprüfen, navigieren Sie zum **Anwendungstool,** und wählen Sie den **Abschnitt Manifest** aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="d7501-151">Fehler und Warnungen werden unter der Überschrift **Fehler und Warnungen** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7501-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="d7501-152">Weitere Informationen zum Web App-Manifest finden Sie unter Verwenden des [Web-App-Manifests,][ProgressiveWebAppsWebappmanifests]um Ihre Progressive Web App in das Betriebssystem zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="d7501-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="d7501-153">Navigieren Sie zum [PWABuilder][PwabuilderImagegenerator]Image Generator, um Symbole zu erstellen, die in Ihr Web-App-Manifest enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d7501-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="d7501-154">Navigieren Sie Chromium zu Problem [1185945][CR1185945].</span><span class="sxs-lookup"><span data-stu-id="d7501-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="d7501-155">Lokalisierte DevTools werden jetzt in Chromium Browsern unterstützt</span><span class="sxs-lookup"><span data-stu-id="d7501-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="d7501-156">Ab Microsoft Edge [Version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]wird Microsoft Edge DevTools in Ihrer eigenen Sprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="d7501-157">Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio Code in ihrer eigenen Sprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="d7501-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="d7501-158">Das Microsoft Edge DevTools-Team, das Chrome DevTools-Team und das Google -Leuchtturm-Team haben zusammengearbeitet, um die gleiche Erfahrung in allen Chromium Browsern zu bieten.</span><span class="sxs-lookup"><span data-stu-id="d7501-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="d7501-159">Weitere Informationen zur Verwendung von DevTools in Ihrer Sprache finden Sie unter [Ändern der DevTools-Spracheinstellungen.][DevtoolsCustomizeLocalization]</span><span class="sxs-lookup"><span data-stu-id="d7501-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="d7501-160">Weitere Informationen zur Zusammenarbeit an diesem Feature Chromium Open Source-Projekt finden Sie unter [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="d7501-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge Browser und DevTools auf Japanisch festgelegt" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="d7501-162">Microsoft Edge Browser und DevTools auf Japanisch festgelegt</span><span class="sxs-lookup"><span data-stu-id="d7501-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="d7501-163">Navigieren zu CSS-Variablen mithilfe der Tastatur</span><span class="sxs-lookup"><span data-stu-id="d7501-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="d7501-164">Ab Microsoft Edge [Version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]zeigt \*\*\*\* der Bereich Formatvorlagen CSS-Variablen an und stellt einen Link direkt zur Definition der einzelnen Variablen zur Seite.</span><span class="sxs-lookup"><span data-stu-id="d7501-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="d7501-165">In Microsoft Edge Version 91 oder höher können Sie die Pfeiltasten verwenden, um problemlos zu CSS-Variablen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="d7501-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="d7501-166">Um die Definition im Bereich **Formatvorlagen** zu öffnen, zeigen Sie auf eine Variable, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="d7501-167">Weitere Informationen zu CSS-Variablen finden Sie unter [Verwenden benutzerdefinierter CSS-Eigenschaften (Variablen).][MdnDocsWebCssUsingCssCustomProperties]</span><span class="sxs-lookup"><span data-stu-id="d7501-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="d7501-168">Navigieren Sie Chromium zu Issue [1187735][CR1187735].</span><span class="sxs-lookup"><span data-stu-id="d7501-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Die CSS-Variable --theme-body-background, die im Bereich Formatvorlagen hervorgehoben ist" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="d7501-170">Die `--theme-body-background` im Bereich Formatvorlagen hervorgehobene **CSS-Variable**</span><span class="sxs-lookup"><span data-stu-id="d7501-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="d7501-171">Probleme werden automatisch nach Schweregrad sortiert</span><span class="sxs-lookup"><span data-stu-id="d7501-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="d7501-172">Das **Tool Probleme** zeigt Empfehlungen zur Verbesserung Ihrer Website an, einschließlich Barrierefreiheit, Leistung, Sicherheit und so weiter.</span><span class="sxs-lookup"><span data-stu-id="d7501-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="d7501-173">Basierend auf Ihrem Feedback werden Probleme jetzt automatisch nach Schweregrad sortiert.</span><span class="sxs-lookup"><span data-stu-id="d7501-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="d7501-174">In jeder Feedbackkategorie wird jedes \*\*\*\* als Fehler markierte Problem zuerst angezeigt, gefolgt von jedem Als Warnung gekennzeichneten Problem **und**anschließend jedem Problem, das als Tipp **gekennzeichnet ist.**</span><span class="sxs-lookup"><span data-stu-id="d7501-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="d7501-175">Um Ihre Probleme zu verfeinern, sind zusätzliche Filteroptionen für ein zukünftiges Update geplant.</span><span class="sxs-lookup"><span data-stu-id="d7501-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="d7501-176">Weitere Informationen zum Überprüfen von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="d7501-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="Das Tool Probleme zeigt sortierte Probleme nach Schweregrad an." lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="d7501-178">Das **Tool Probleme** zeigt sortierte Probleme nach Schweregrad an.</span><span class="sxs-lookup"><span data-stu-id="d7501-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="d7501-179">Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.7</span><span class="sxs-lookup"><span data-stu-id="d7501-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="d7501-180">Die [Microsoft Edge Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterung, Version 1.1.7, stellt die DevTools aus Microsoft Edge Version [88 bereit.][DevtoolsWhatsNew202011Devtools]</span><span class="sxs-lookup"><span data-stu-id="d7501-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="d7501-181">Diese Erweiterung unterstützt jetzt ARM Geräte und hängt nicht mehr vom [Debugger][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] für Microsoft Edge ab.</span><span class="sxs-lookup"><span data-stu-id="d7501-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="d7501-182">Version 1.1.7 enthält die folgenden Fehlerbehebungen und Verbesserungen.</span><span class="sxs-lookup"><span data-stu-id="d7501-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="d7501-183">Die Zuverlässigkeit der Zielschließung wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d7501-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="d7501-184">Der Seitenbereich wurde so aktualisiert, dass er automatisch aktualisiert wird, wenn Sie ziele debuggen, die erstellt oder zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="d7501-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="d7501-185">Es wurde ein neues kontextbezogenes Menü hinzugefügt, mit dem Sie schneller auf die Erweiterungseinstellungen und das neueste Changelog zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="d7501-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="d7501-186">Die Veröffentlichung der Erweiterungsdokumentation einschließlich der neuesten Features wurde aktualisiert und vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="d7501-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="d7501-187">Um manuell auf Version 1.1.7 zu aktualisieren, navigieren Sie zu [Manuelles Aktualisieren einer Erweiterung.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="d7501-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="d7501-188">Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] mitwirken.</span><span class="sxs-lookup"><span data-stu-id="d7501-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="d7501-189">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="d7501-189">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="visualize-css-scroll-snap"></a><span data-ttu-id="d7501-190">Visualisieren des CSS-Bildlauf-Snaps</span><span class="sxs-lookup"><span data-stu-id="d7501-190">Visualize CSS scroll-snap</span></span>  

<span data-ttu-id="d7501-191">Sie können jetzt das Signal im Elementtool umschalten, `scroll-snap` um die CSS-Scroll-Snap-Ausrichtung zu überprüfen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d7501-191">You may now toggle the `scroll-snap` badge in the **Elements** tool to inspect the CSS scroll-snap alignment.</span></span>  <span data-ttu-id="d7501-192">Wenn ein HTML-Element auf Ihrer Webseite darauf angewendet wurde, wird im Tool Elemente ein Signal `scroll-snap-type` `scroll-snap` **daneben** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-192">When an HTML element on your webpage has `scroll-snap-type` applied to it, a `scroll-snap` badge displays next to it in the **Elements** tool.</span></span>  <span data-ttu-id="d7501-193">Wählen Sie das Signal aus, um \(oder aus\) die Anzeige einer Bildlaufrastüberlagerung auf der Webseite zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7501-193">Choose the badge to turn on \(or off\) the display of a scroll-snap overlay on the webpage.</span></span>  <span data-ttu-id="d7501-194">Navigieren Sie zum Überprüfen einer Beispielwebseite zu [Scroll Andocken Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span><span class="sxs-lookup"><span data-stu-id="d7501-194">To review an example webpage, navigate to [Scroll Snap Demo][GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml].</span></span>  <span data-ttu-id="d7501-195">Im Beispiel werden Punkte an Einrastkanten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-195">In the example, dots display on snap edges.</span></span>  <span data-ttu-id="d7501-196">Der Bildlaufport hat eine durchgehende Gliederung, während die Einrastelemente Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7501-196">The scroll port has a solid outline while the snap items have dash outlines.</span></span>  <span data-ttu-id="d7501-197">Der Bildlaufabstand wird grün gefüllt, während der Bildlaufrand in Orange gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d7501-197">The scroll padding is filled in green while the scroll margin is filled in orange.</span></span>  <span data-ttu-id="d7501-198">Navigieren Sie zu Issue [862450,][CR862450]um den Verlauf dieses Features im Chromium-Open-Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7501-198">To review the history of this feature in the Chromium open-source project, navigate to Issue [862450][CR862450].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-scroll-snap-highlight.msft.png" alt-text="CSS-Bildlauf-Snap" lightbox="../../media/2021/04/elements-scroll-snap-highlight.msft.png":::
   <span data-ttu-id="d7501-200">CSS-Bildlauf-Snap</span><span class="sxs-lookup"><span data-stu-id="d7501-200">CSS scroll-snap</span></span>  
:::image-end:::  

### <a name="new-memory-inspector-tool"></a><span data-ttu-id="d7501-201">Neues Tool für den Speicherprüfungstool</span><span class="sxs-lookup"><span data-stu-id="d7501-201">New Memory Inspector tool</span></span>  

<span data-ttu-id="d7501-202">Verwenden Sie das neue **Tool Memory Inspector,** um einen `ArrayBuffer` In-JavaScript- und Wasm-Speicher zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7501-202">Use the new **Memory Inspector** tool to inspect an `ArrayBuffer` in JavaScript and Wasm memory.</span></span>  <span data-ttu-id="d7501-203">Öffnen Sie [die Demowebseite Memory in JS.][GlitchMemoryInspectorDemoJsHtml]</span><span class="sxs-lookup"><span data-stu-id="d7501-203">Open the [Memory in JS][GlitchMemoryInspectorDemoJsHtml] demo webpage.</span></span>  <span data-ttu-id="d7501-204">Öffnen Sie **im Tool** Quellen die `memory-write-wasm` Datei, und legen Sie einen Haltepunkt an der Zeile `0x03c` ein.</span><span class="sxs-lookup"><span data-stu-id="d7501-204">In the **Sources** tool, open the `memory-write-wasm` file, and set a breakpoint at line `0x03c`.</span></span>  <span data-ttu-id="d7501-205">Aktualisieren Sie die Webseite.</span><span class="sxs-lookup"><span data-stu-id="d7501-205">Refresh the webpage.</span></span>  <span data-ttu-id="d7501-206">Erweitern Sie **den Abschnitt Bereich** im Debuggerbereich.</span><span class="sxs-lookup"><span data-stu-id="d7501-206">Expand the **Scope** section in the debugger pane.</span></span>  <span data-ttu-id="d7501-207">Das neue Symbol wird neben dem **Pufferwert** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-207">The new icon is displayed next to the **buffer** value.</span></span>  <span data-ttu-id="d7501-208">Wählen Sie es aus, um das neue **Speicherprüfungstool zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="d7501-208">Choose it to open the new **Memory Inspector** tool.</span></span>  

<span data-ttu-id="d7501-209">Weitere Informationen zum Debuggen im **Tool Sources** finden Sie unter Verwenden des [Debuggerbereichs zum Debuggen von JavaScript-Code][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].</span><span class="sxs-lookup"><span data-stu-id="d7501-209">To learn more about debugging in the **Sources** tool, navigate to [Using the Debugger pane to debug JavaScript code][DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode].</span></span>  <span data-ttu-id="d7501-210">Navigieren Sie Chromium zu Issue [1166577][CR1166577].</span><span class="sxs-lookup"><span data-stu-id="d7501-210">To review the history of this feature in the Chromium open-source project, navigate to Issue [1166577][CR1166577].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png" alt-text="Tool "Memory Inspector"" lightbox="../../media/2021/04/sources-memory-write-wasm-breakpoint-scope-reveal-in-memory-inspector-panel.msft.png":::
   <span data-ttu-id="d7501-212">**Speicherprüfungstool**</span><span class="sxs-lookup"><span data-stu-id="d7501-212">**Memory inspector** tool</span></span>  
:::image-end:::  

### <a name="new-badge-settings-pane-in-the-elements-tool"></a><span data-ttu-id="d7501-213">Bereich "Neue Signaleinstellungen" im Tool Elemente</span><span class="sxs-lookup"><span data-stu-id="d7501-213">New Badge settings pane in the Elements tool</span></span>  

<span data-ttu-id="d7501-214">Verwenden Sie jetzt die **Badge-Einstellungen** im **Elementtool,** um einzelne Signale \(oder aus\) zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7501-214">Now, use the **Badge settings** in the **Elements** tool to turn on \(or off\) individual badges.</span></span>  <span data-ttu-id="d7501-215">Verwenden Sie dieses Feature, um wichtige Badges anzupassen und sich auf wichtige Badges zu konzentrieren, während Sie Webseiten überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7501-215">Use this feature to customize and stay focused on important badges while you inspect webpages.</span></span>  <span data-ttu-id="d7501-216">Führen Sie die folgenden Aktionen aus, um den Bereich "Signaleinstellungen" am oberen Rand des **Elements-Tools** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7501-216">To display the badge settings pane at the top of the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7501-217">Zeigen Sie auf ein beliebiges Element.</span><span class="sxs-lookup"><span data-stu-id="d7501-217">Hover on any element.</span></span>  
1.  <span data-ttu-id="d7501-218">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="d7501-218">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="d7501-219">Wählen **Sie Signaleinstellungen... aus.**</span><span class="sxs-lookup"><span data-stu-id="d7501-219">Choose **Badge settings...**.</span></span>  
    
<span data-ttu-id="d7501-220">Zum Anzeigen \(oder Ausblenden\) der Signalen wählen Sie \(oder entfernen\) das Kontrollkästchen neben dem Signalnamen aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-220">To display \(or hide\) the badges, choose \(or remove\) the checkbox next to the badge name.</span></span>  

<!--  To review the history of this feature in the Chromium open-source project, navigate to Issue [1066772][CR1066772].  -->  

:::image type="complex" source="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png" alt-text="Bereich "Signaleinstellungen" im Elementtool" lightbox="../../media/2021/04/elements-contextual-menu-badge-settings.msft.png":::
   <span data-ttu-id="d7501-222">**Bereich "Signaleinstellungen"** im **Elementtool**</span><span class="sxs-lookup"><span data-stu-id="d7501-222">**Badge settings** pane in the **Elements** tool</span></span>  
:::image-end:::  

### <a name="enhanced-image-preview-with-aspect-ratio-information"></a><span data-ttu-id="d7501-223">Erweiterte Bildvorschau mit Seitenverhältnisinformationen</span><span class="sxs-lookup"><span data-stu-id="d7501-223">Enhanced image preview with aspect ratio information</span></span>  

<span data-ttu-id="d7501-224">Die Bildvorschau in den DevTools wurde erweitert, um weitere Informationen anzuzeigen, einschließlich der folgenden Details.</span><span class="sxs-lookup"><span data-stu-id="d7501-224">Image previews in the DevTools have been enhanced to display more information, including the following details.</span></span>  

*   <span data-ttu-id="d7501-225">Gerenderte Größe</span><span class="sxs-lookup"><span data-stu-id="d7501-225">Rendered size</span></span>  
*   <span data-ttu-id="d7501-226">Gerenderte Seitenverhältnisse</span><span class="sxs-lookup"><span data-stu-id="d7501-226">Rendered aspect ratio</span></span>  
*   <span data-ttu-id="d7501-227">Systeminterne Größe</span><span class="sxs-lookup"><span data-stu-id="d7501-227">Intrinsic size</span></span>  
*   <span data-ttu-id="d7501-228">Systeminternes Seitenverhältnis</span><span class="sxs-lookup"><span data-stu-id="d7501-228">Intrinsic aspect ratio</span></span>  
*   <span data-ttu-id="d7501-229">Dateigröße</span><span class="sxs-lookup"><span data-stu-id="d7501-229">File size</span></span>  
    
<span data-ttu-id="d7501-230">Die Informationen helfen Ihnen, Ihre Bilder besser zu verstehen und die Optimierung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="d7501-230">The  information helps you better understand your images and apply optimization.</span></span>  <span data-ttu-id="d7501-231">Die Informationen zum Bildaspektverhältnis sind auch im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.</span><span class="sxs-lookup"><span data-stu-id="d7501-231">The image aspect ratio information is also available in the **Network** tool, when you choose an image preview.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d7501-232">Im **Elementtool** zeigt die Bildvorschau nun weitere Informationen zum Bild an.</span><span class="sxs-lookup"><span data-stu-id="d7501-232">In the **Elements** tool, image preview now displays more information about the image.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d7501-233">Darüber hinaus sind die Informationen zum Bildaspektverhältnis im **Netzwerktool** verfügbar, wenn Sie eine Bildvorschau auswählen.</span><span class="sxs-lookup"><span data-stu-id="d7501-233">Also, the image aspect ratio information is available in the **Network** tool, when you choose an image preview.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png" alt-text="Bildvorschau mit Seitenverhältnisinformationen im Elementtool" lightbox="../../media/2021/04/elements-inspect-image-src-hover-preview.msft.png":::
         <span data-ttu-id="d7501-235">Bildvorschau mit Seitenverhältnisinformationen im **Elementtool**</span><span class="sxs-lookup"><span data-stu-id="d7501-235">Image preview with aspect ratio information in the **Element** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/network-img-name-filters-preview.msft.png" alt-text="Informationen zum Bild seitenverhältnis im Netzwerktool" lightbox="../../media/2021/04/network-img-name-filters-preview.msft.png":::
         <span data-ttu-id="d7501-237">Informationen zum Bild seitenverhältnis im **Netzwerktool**</span><span class="sxs-lookup"><span data-stu-id="d7501-237">Image aspect ratio information in the **Network** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d7501-238">Navigieren Sie zu Probleme [1149832][CR1149832] und [1170656][CR1149832] und [1170656][CR1170656]. Chromium</span><span class="sxs-lookup"><span data-stu-id="d7501-238">To review the history of this feature in the Chromium open-source project, navigate to Issues [1149832][CR1149832] and [1170656][CR1170656].</span></span>  

### <a name="new-options-to-configure-content-encodings-in-the-network-conditions-tool"></a><span data-ttu-id="d7501-239">Neue Optionen zum Konfigurieren von Inhaltscodierungen im Tool für Netzwerkbedingungen</span><span class="sxs-lookup"><span data-stu-id="d7501-239">New options to configure Content-Encodings in the Network conditions tool</span></span> 

<span data-ttu-id="d7501-240">Wählen Sie im **Tool** Netzwerk die neue Schaltfläche \*\*\*\* Weitere **Netzwerkbedingungen...** neben dem Dropdownmenü Einschränkung aus, um das Tool **Netzwerkbedingungen zu** öffnen.</span><span class="sxs-lookup"><span data-stu-id="d7501-240">In the **Network** tool, choose the new **More network conditions...** button next to the **Throttling** dropdown menu to open the **Network conditions** tool.</span></span>  <span data-ttu-id="d7501-241">Führen Sie die folgenden Aktionen aus, um zu testen, ob Serverantworten für Browser korrekt codiert sind, die [gzip,][GnuSoftwareGzipManual] [brotli][|::ref1::|Main]oder eine andere Zukunft `Content-Encoding` nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d7501-241">To test if server responses are correctly encoded for browsers that don't support [gzip][GnuSoftwareGzipManual], [brotli][|::ref1::|Main], or another future `Content-Encoding`, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7501-242">Öffnen des **Tools für Netzwerkbedingungen**</span><span class="sxs-lookup"><span data-stu-id="d7501-242">Open the **Network conditions** tool</span></span>
1.  <span data-ttu-id="d7501-243">Navigieren Sie zu **Akzeptierte Inhaltscodierungen**.</span><span class="sxs-lookup"><span data-stu-id="d7501-243">Navigate to **Accepted Content-Encodings**.</span></span> 
1.  <span data-ttu-id="d7501-244">Entfernen Sie das Kontrollkästchen neben `Content-Encoding` dem, das Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7501-244">Remove the checkbox next to the `Content-Encoding` you want to test.</span></span>  
    
<span data-ttu-id="d7501-245">Navigieren Sie Chromium zu Issue [1162042][CR1162042].</span><span class="sxs-lookup"><span data-stu-id="d7501-245">To review the history of this feature in the Chromium open-source project, navigate to Issue [1162042][CR1162042].</span></span>  

:::image type="complex" source="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png" alt-text="Neue Weitere Netzwerkbedingungen... -Schaltfläche öffnet das Tool "Netzwerkbedingungen", um die Inhaltscodierung zu konfigurieren." lightbox="../../media/2021/04/network-more-network-conditions-accepted-content-encodings.msft.png":::
   <span data-ttu-id="d7501-247">Neue **Schaltfläche Weitere Netzwerkbedingungen...** öffnet das **Tool "Netzwerkbedingungen"** zum Konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d7501-247">New **More network conditions...** button opens the **Network conditions** tool to configure</span></span> `Content-Encoding`  
:::image-end:::  

### <a name="styles-pane-enhancements"></a><span data-ttu-id="d7501-248">Verbesserungen des Formatbereichs</span><span class="sxs-lookup"><span data-stu-id="d7501-248">Styles pane enhancements</span></span>  

#### <a name="new-shortcut-to-display-computed-value-in-the-styles-pane"></a><span data-ttu-id="d7501-249">Neue Verknüpfung zum Anzeigen des berechneten Werts im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="d7501-249">New shortcut to display computed value in the Styles pane</span></span>  

<span data-ttu-id="d7501-250">Führen Sie nun die folgenden Aktionen aus, um den berechneten CSS-Wert im Bereich **Formatvorlagen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7501-250">Now, to display the computed CSS value in the **Styles** pane, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7501-251">Zeigen Sie auf eine CSS-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d7501-251">Hover on a CSS property.</span></span>  
1.  <span data-ttu-id="d7501-252">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="d7501-252">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="d7501-253">Wählen **Sie Berechneten Wert anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="d7501-253">Choose **View computed value**.</span></span>  
    
<span data-ttu-id="d7501-254">Navigieren Sie zum Überprüfen des Verlaufs dieses Features im Chromium Open Source-Projekt zu Issue [1076198][CR1076198].</span><span class="sxs-lookup"><span data-stu-id="d7501-254">To review the history of this feature in the Chromium open-source project, navigate to Issue [1076198][CR1076198].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png" alt-text="Neue Verknüpfung zum Anzeigen des berechneten Werts" lightbox="../../media/2021/04/elements-styles-highlight-view-computed-value.msft.png":::
   <span data-ttu-id="d7501-256">Neue Verknüpfung zum Anzeigen des berechneten Werts</span><span class="sxs-lookup"><span data-stu-id="d7501-256">New shortcut to display computed value</span></span>  
:::image-end:::  

#### <a name="support-for-the-accent-color-keyword"></a><span data-ttu-id="d7501-257">Unterstützung für das Schlüsselwort akzentuiert</span><span class="sxs-lookup"><span data-stu-id="d7501-257">Support for the accent-color keyword</span></span>  

<span data-ttu-id="d7501-258">Die benutzeroberfläche für die \*\*\*\* automatische Vervollständigung des Bereichs Formatvorlagen erkennt nun das SCHLÜSSELWORT CSS, mit dem Sie die Akzentfarbe für vom Element generierte Benutzeroberflächensteuerelemente `accent-color` angeben können.</span><span class="sxs-lookup"><span data-stu-id="d7501-258">The autocomplete UI of the **Styles** pane now detects the `accent-color` CSS keyword, which allows you to specify the accent color for UI controls generated by the element.</span></span>  <span data-ttu-id="d7501-259">Beispiele für benutzeroberflächensteuerelemente, die von einem Element generiert werden, sind Kontrollkästchen oder Optionsfelder.</span><span class="sxs-lookup"><span data-stu-id="d7501-259">Examples of UI controls that are generated by an element include checkboxes or radio buttons.</span></span> <span data-ttu-id="d7501-260">Weitere Informationen zum Status der Chromium finden Sie unter [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].</span><span class="sxs-lookup"><span data-stu-id="d7501-260">For more information about the status of the Chromium implementation, navigate to [Feature: accent-color CSS property][ChromestatusFeature4752739957473280].</span></span>  <span data-ttu-id="d7501-261">Um dieses Feature zu aktivieren, navigieren Sie `edge://flags#enable-experimental-web-platform-features` zu, und legen Sie das Kontrollkästchen auf **Aktiviert .**</span><span class="sxs-lookup"><span data-stu-id="d7501-261">To turn on this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and set the checkbox to **Enabled**.</span></span>  <span data-ttu-id="d7501-262">Navigieren Sie Chromium zu Issue [1092093][CR1092093].</span><span class="sxs-lookup"><span data-stu-id="d7501-262">To review the history of this feature in the Chromium open-source project, navigate to Issue [1092093][CR1092093].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-accent-color.msft.png" alt-text="schlüsselwort accent-color CSS" lightbox="../../media/2021/04/elements-styles-accent-color.msft.png":::
   `accent-color` <span data-ttu-id="d7501-264">CSS-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="d7501-264">CSS keyword</span></span>
:::image-end:::  

### <a name="display-details-about-blocked-features-in-the-frame-details-view"></a><span data-ttu-id="d7501-265">Anzeigen von Details zu blockierten Features in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="d7501-265">Display details about blocked features in the Frame details view</span></span>  

<span data-ttu-id="d7501-266">Die Berechtigungsrichtlinie ist eine Webplattform-API, mit der eine Website die Verwendung von Browserfeatures in einem einzelnen Frame oder in einem eingebetteten Frame zulassen oder `iframe` blockieren kann.</span><span class="sxs-lookup"><span data-stu-id="d7501-266">Permissions Policy is a web platform API that gives a website the ability to allow or block the use of browser features in an individual frame or in an `iframe` that it embeds.</span></span> <span data-ttu-id="d7501-267">Weitere Informationen finden Sie unter [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span><span class="sxs-lookup"><span data-stu-id="d7501-267">For more information, navigate to [Permissions Policy Explainer][GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd].</span></span>  <span data-ttu-id="d7501-268">Führen Sie die folgenden Aktionen aus, um die Details anzuzeigen, warum ein Feature blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="d7501-268">To display the details on why a feature is blocked, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7501-269">Navigieren Sie zu [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].</span><span class="sxs-lookup"><span data-stu-id="d7501-269">Navigate to [OOPIF Permissions Policy][GlitchPermissionPolicyDemoMain].</span></span>  
1.  <span data-ttu-id="d7501-270">Navigieren Sie zum **Anwendungstool.**</span><span class="sxs-lookup"><span data-stu-id="d7501-270">Navigate to the **Application** tool.</span></span>  
1.  <span data-ttu-id="d7501-271">Wählen Sie einen Frame aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-271">Choose a frame.</span></span>  
1.  <span data-ttu-id="d7501-272">Navigieren Sie zum **Abschnitt Berechtigungsrichtlinie.**</span><span class="sxs-lookup"><span data-stu-id="d7501-272">Navigate to the **Permissions Policy** section.</span></span>  
1.  <span data-ttu-id="d7501-273">Navigieren Sie zur **Disabled Features-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="d7501-273">Navigate to the **Disabled Features** property.</span></span>  
1.  <span data-ttu-id="d7501-274">Wählen Sie **Details anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="d7501-274">Choose **Show details**.</span></span>  
1.  <span data-ttu-id="d7501-275">Wählen Sie das Symbol neben jeder Richtlinie aus, um zu der Netzwerkanforderung zu navigieren, `iframe` die das Feature blockiert hat.</span><span class="sxs-lookup"><span data-stu-id="d7501-275">Choose the icon next to each policy to navigate to the `iframe` or network request that blocked the feature.</span></span>  
    
<span data-ttu-id="d7501-276">Navigieren Sie Chromium zu Issue [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="d7501-276">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png" alt-text="Blockierte Features in der Frame-Detailansicht" lightbox="../../media/2021/04/application-frames-top-permission-policy-disabled-features-show-details-highlight.msft.png":::
   <span data-ttu-id="d7501-278">Blockierte Features in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="d7501-278">Blocked features in the Frame details view</span></span>  
:::image-end:::  

### <a name="filter-experiments-in-the-experiments-setting"></a><span data-ttu-id="d7501-279">Filtern von Experimenten in der Einstellung Experimente</span><span class="sxs-lookup"><span data-stu-id="d7501-279">Filter experiments in the Experiments setting</span></span>  

<span data-ttu-id="d7501-280">Suchen Sie mit dem neuen Experimentfilter schneller nach Experimenten.</span><span class="sxs-lookup"><span data-stu-id="d7501-280">Find experiments quicker with the new experiment filter.</span></span>  <span data-ttu-id="d7501-281">Führen Sie beispielsweise die folgenden Aktionen aus, um neue Experimente für Codeprobleme zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7501-281">For example, to turn on new experiments for code issues, complete the following actions.</span></span>
``

1.  <span data-ttu-id="d7501-282">Navigieren Sie zu **Einstellungen**  >  **Experiments**.</span><span class="sxs-lookup"><span data-stu-id="d7501-282">Navigate to **Settings** > **Experiments**.</span></span>  
1.  <span data-ttu-id="d7501-283">Navigieren Sie zum **Textfeld Filter.**</span><span class="sxs-lookup"><span data-stu-id="d7501-283">Navigate to the **Filter** textbox.</span></span>  
1.  <span data-ttu-id="d7501-284">Geben Sie `issues` ein.</span><span class="sxs-lookup"><span data-stu-id="d7501-284">Type `issues`.</span></span>  
    
:::image type="complex" source="../../media/2021/04/settings-experiments-filter-by-issues.msft.png" alt-text="Filtern von Experimenten in der Einstellung Experimente" lightbox="../../media/2021/04/settings-experiments-filter-by-issues.msft.png":::
   <span data-ttu-id="d7501-286">Filtern von Experimenten in der **Einstellung Experimente**</span><span class="sxs-lookup"><span data-stu-id="d7501-286">Filter experiments in the **Experiments** setting</span></span>  
:::image-end:::  

### <a name="new-vary-header-column-in-the-cache-storage-pane"></a><span data-ttu-id="d7501-287">Spalte "New Vary Header" im Speicherbereich "Cache"</span><span class="sxs-lookup"><span data-stu-id="d7501-287">New Vary Header column in the Cache storage pane</span></span>  

<span data-ttu-id="d7501-288">Verwenden Sie die neue Spalte im Bereich `Vary Header` **Cache Storage,** um die [Werte der Http-Antwortheader][HttpwgSpecsRfc7231HtmlHeaderVary] variieren anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7501-288">Use the new `Vary Header` column in the **Cache Storage** pane to display the [Vary][HttpwgSpecsRfc7231HtmlHeaderVary] HTTP response header values.</span></span>  <span data-ttu-id="d7501-289">Navigieren Sie Chromium zu Issue [1186049][CR1186049].</span><span class="sxs-lookup"><span data-stu-id="d7501-289">To review the history of this feature in the Chromium open-source project, navigate to Issue [1186049][CR1186049].</span></span>  

:::image type="complex" source="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png" alt-text="Spalte "Kopfzeile variieren"" lightbox="../../media/2021/04/application-cache-cache-storage-highlighted-vary-header.msft.png":::
   <span data-ttu-id="d7501-291">Spalte "Kopfzeile variieren"</span><span class="sxs-lookup"><span data-stu-id="d7501-291">Vary Header column</span></span>  
:::image-end:::  

### <a name="sources-tool-improvements"></a><span data-ttu-id="d7501-292">Verbesserungen des Quellentools</span><span class="sxs-lookup"><span data-stu-id="d7501-292">Sources tool improvements</span></span>  

#### <a name="support-for-new-javascript-features"></a><span data-ttu-id="d7501-293">Unterstützung für neue JavaScript-Features</span><span class="sxs-lookup"><span data-stu-id="d7501-293">Support for new JavaScript features</span></span>  

<span data-ttu-id="d7501-294">DevTools unterstützt jetzt die neue [Private-Markenprüfungen a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript-Sprachfeatures.</span><span class="sxs-lookup"><span data-stu-id="d7501-294">DevTools now support the new [Private brand checks a.k.a. #foo in obj][V8DevFeaturesPrivateBrandChecks] JavaScript language feature.</span></span>  <span data-ttu-id="d7501-295">Das Feature für private Markenüberprüfungen erweitert den [In-Operator,][MdnDocsWebJavascriptReferenceOperatorsIn] um [Private Klassenfelder für][V8DevFeaturesClassFieldsPrivateClassFields] ein bestimmtes Objekt zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d7501-295">The private brand checks feature extends the [in operator][MdnDocsWebJavascriptReferenceOperatorsIn] to support [Private class fields][V8DevFeaturesClassFieldsPrivateClassFields] on a specific object.</span></span>  <span data-ttu-id="d7501-296">Versuchen Sie es in den **Konsolen-** und **Quellentools.**</span><span class="sxs-lookup"><span data-stu-id="d7501-296">Try it in the **Console** and **Sources** tools.</span></span>  <span data-ttu-id="d7501-297">Führen Sie außerdem die folgenden Aktionen aus, um die privaten Felder zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7501-297">Also, to inspect the private fields, complete the following actions.</span></span>  

1.  <span data-ttu-id="d7501-298">Navigieren Sie **zum Debuggerbereich.**</span><span class="sxs-lookup"><span data-stu-id="d7501-298">Navigate to **debugger** pane.</span></span>  
1.  <span data-ttu-id="d7501-299">Navigieren Sie zum **Abschnitt Bereich.**</span><span class="sxs-lookup"><span data-stu-id="d7501-299">Navigate to the **Scope** section.</span></span>  
    
<span data-ttu-id="d7501-300">Navigieren Sie zu Problem [11374,][CR11374]um den Verlauf dieses Features Chromium Open Source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7501-300">To review the history of this feature in the Chromium open-source project, navigate to Issue [11374][CR11374].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png" alt-text="JavaScript-Überprüfungen privater Marken" lightbox="../../media/2021/04/sources-page-pen-js-breakpoint-scope-script-dog.msft.png":::
   <span data-ttu-id="d7501-302">JavaScript-Überprüfungen privater Marken</span><span class="sxs-lookup"><span data-stu-id="d7501-302">JavaScript private brand checks</span></span>  
:::image-end:::  

#### <a name="enhanced-support-for-breakpoints-debugging"></a><span data-ttu-id="d7501-303">Erweiterte Unterstützung für das Debuggen von Haltepunkten</span><span class="sxs-lookup"><span data-stu-id="d7501-303">Enhanced support for breakpoints debugging</span></span>  

<span data-ttu-id="d7501-304">Moderne JavaScript-Bundleer wie [Webpack][WebpackJsMain]und [Rollup unterstützen][RollupjsMain] die Codeteilung.</span><span class="sxs-lookup"><span data-stu-id="d7501-304">Modern JavaScript bundlers like [Webpack][WebpackJsMain], and [Rollup][RollupjsMain] support code splitting.</span></span>  <span data-ttu-id="d7501-305">Weitere Informationen zum Teilen von Code finden Sie unter [Code splitting][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span><span class="sxs-lookup"><span data-stu-id="d7501-305">To learn more about code splitting, navigate to [Code splitting][JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules].</span></span>  <span data-ttu-id="d7501-306">In Microsoft Edge Version 90 oder früher legen DevTools nur Haltepunkte in einem einzigen Bündel an.</span><span class="sxs-lookup"><span data-stu-id="d7501-306">In Microsoft Edge version 90 or earlier, DevTools only set breakpoints in a single bundle.</span></span>  <span data-ttu-id="d7501-307">In Microsoft Edge Version 91 oder höher legt DevTools haltepunkte in mehreren Bündeln richtig fest, wenn Sie eine freigegebene Komponente debuggen.</span><span class="sxs-lookup"><span data-stu-id="d7501-307">In Microsoft Edge version 91 or later, DevTools properly sets breakpoints in multiple bundles when you debug a shared component.</span></span>  <span data-ttu-id="d7501-308">Navigieren Sie zum Überprüfen des Verlaufs dieses Features im Chromium-Open-Source-Projekt zu Probleme [1142705][CR1142705], [979000][CR979000]und [1180794][CR1180794].</span><span class="sxs-lookup"><span data-stu-id="d7501-308">To review the history of this feature in the Chromium open-source project, navigate to Issues [1142705][CR1142705], [979000][CR979000], and [1180794][CR1180794].</span></span>  

#### <a name="support-hover-preview-with-bracket-notation"></a><span data-ttu-id="d7501-309">Unterstützen der Hovervorschau mit Klammern-Notation</span><span class="sxs-lookup"><span data-stu-id="d7501-309">Support hover preview with bracket notation</span></span>  

<span data-ttu-id="d7501-310">DevTools unterstützt jetzt die Hovervorschau für JavaScript-Memberausdrücke, die die `[]` Notation im **Tool Quellen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7501-310">DevTools now support hover preview on JavaScript member expressions that use the `[]` notation in the **Sources** tool.</span></span>  <span data-ttu-id="d7501-311">Navigieren Sie Chromium zu Issue [1178305][CR1178305].</span><span class="sxs-lookup"><span data-stu-id="d7501-311">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178305][CR1178305].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png" alt-text="Unterstützen der Hovervorschau mit [] Notation" lightbox="../../media/2021/04/sources-page-pen.js-breakpoint-arr-i-a.msft.png":::
   <span data-ttu-id="d7501-313">Unterstützen der Hovervorschau mit `[]` Notation</span><span class="sxs-lookup"><span data-stu-id="d7501-313">Support hover preview with `[]` notation</span></span>  
:::image-end:::  

#### <a name="improved-outline-of-html-files"></a><span data-ttu-id="d7501-314">Verbesserte Gliederung von HTML-Dateien</span><span class="sxs-lookup"><span data-stu-id="d7501-314">Improved outline of HTML files</span></span>  

<span data-ttu-id="d7501-315">DevTools bietet jetzt eine bessere Gliederungsunterstützung für `.html` Dateien.</span><span class="sxs-lookup"><span data-stu-id="d7501-315">DevTools now has better outline support for `.html` files.</span></span>  <span data-ttu-id="d7501-316">Öffnen Sie **im Tool** Quellen die `.html` Datei.</span><span class="sxs-lookup"><span data-stu-id="d7501-316">In the **Sources** tool, open the `.html` file.</span></span>  <span data-ttu-id="d7501-317">Um \(oder aus\) die Codegliederung zu aktivieren, wählen Sie `Ctrl` + `Shift` + `O` unter Windows/Linux oder `Cmd` + `Shift` + `O` unter macOS aus.</span><span class="sxs-lookup"><span data-stu-id="d7501-317">To turn on \(or off\) the code outline, select `Ctrl`+`Shift`+`O` on Windows/Linux or `Cmd`+`Shift`+`O` on macOS.</span></span>  <span data-ttu-id="d7501-318">In der folgenden Abbildung listet DevTools nun ordnungsgemäß alle Funktionen in der Gliederung auf.</span><span class="sxs-lookup"><span data-stu-id="d7501-318">In the following figure, DevTools now correctly list all functions in the outline.</span></span>  <span data-ttu-id="d7501-319">Zuvor hat DevTools nur einige der Funktionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-319">Previously, DevTools only displayed some of the functions.</span></span>  <span data-ttu-id="d7501-320">Navigieren Sie zu Issues [761019][CR761019] und [1191465][CR1191465]. Chromium</span><span class="sxs-lookup"><span data-stu-id="d7501-320">To review the history of this feature in the Chromium open-source project, navigate to Issues [761019][CR761019] and [1191465][CR1191465].</span></span>  

:::image type="complex" source="../../media/2021/04/sources-page-jobobbx-at.msft.png" alt-text=" Verbesserte Gliederung von HTML-Dateien" lightbox="../../media/2021/04/sources-page-jobobbx-at.msft.png":::
   <span data-ttu-id="d7501-322">Verbesserte Gliederung von HTML-Dateien</span><span class="sxs-lookup"><span data-stu-id="d7501-322">Improved outline of HTML files</span></span>  
:::image-end:::  

#### <a name="proper-error-stack-traces-for-wasm-debugging"></a><span data-ttu-id="d7501-323">Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging</span><span class="sxs-lookup"><span data-stu-id="d7501-323">Proper error stack traces for Wasm debugging</span></span>  

<span data-ttu-id="d7501-324">In Microsoft Edge Version 90 oder früher hat DevTools nur generische Wasm-Verweise in Fehlerstapelverfolgungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-324">In Microsoft Edge version 90 or earlier, DevTools only displayed generic Wasm references in Error stack traces.</span></span>  <span data-ttu-id="d7501-325">In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt den Quellspeicherort unter Fehlerstapelverfolgungen für das Wasm-Debuggen an.</span><span class="sxs-lookup"><span data-stu-id="d7501-325">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays the source location in Error stack traces for Wasm debugging.</span></span>  <span data-ttu-id="d7501-326">Um mehr über Fehlerstapelverfolgungen in der Konsole zu **erfahren,** navigieren Sie zu [Error][DevtoolsConsoleApiError].</span><span class="sxs-lookup"><span data-stu-id="d7501-326">To learn more about Error stack traces in the **Console**, navigate to [error][DevtoolsConsoleApiError].</span></span>  

<span data-ttu-id="d7501-327">In Microsoft Edge Version 91 oder höher löst DevTools Inlinefunktionsanforderungen auf und zeigt ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging an.</span><span class="sxs-lookup"><span data-stu-id="d7501-327">In Microsoft Edge version 91 or later, DevTools resolves inline function requests and displays proper error stack traces for Wasm debugging.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="d7501-328">In Microsoft Edge Version 90 und früher wird der Quellspeicherort nicht in den Fehlerstapelverfolgungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-328">In Microsoft Edge version 90 and earlier, the source location doesn't display in the Error stack traces.</span></span>  <span data-ttu-id="d7501-329">Quellstandorte sind `dsquare` .</span><span class="sxs-lookup"><span data-stu-id="d7501-329">Source locations include `dsquare`.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d7501-330">In Microsoft Edge Version 91 und höher wird der Quellspeicherort in der Fehlerstapelverfolgung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7501-330">In Microsoft Edge version 91 and later, the source location displays in the Error stack traces.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png" alt-text="Frühere Fehlerstapelverfolgungen für das Wasm-Debuggen" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error-old.msft.png":::
         <span data-ttu-id="d7501-332">Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging</span><span class="sxs-lookup"><span data-stu-id="d7501-332">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png" alt-text="Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging" lightbox="../../media/2021/04/sources-page-inlining-dwarf-wasm-breakpoint-console-new-error.msft.png":::
         <span data-ttu-id="d7501-334">Ordnungsgemäße Fehlerstapelverfolgungen für das Wasm-Debugging</span><span class="sxs-lookup"><span data-stu-id="d7501-334">Proper error stack traces for Wasm debugging</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d7501-335">Navigieren Sie Chromium zu Issue [1189161][CR1189161].</span><span class="sxs-lookup"><span data-stu-id="d7501-335">To review the history of this feature in the Chromium open-source project, navigate to Issue [1189161][CR1189161].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="d7501-336">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="d7501-336">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="d7501-337">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7501-337">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="d7501-338">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="d7501-338">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="d7501-339">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d7501-339">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Verwenden der DevTools in anderen Sprachen – Neues in DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Neues in DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: ../../2020/11/devtools.md#css-variable-definitions-in-styles-pane "CSS-Variablendefinitionen im Formatvorlagenbereich – Neues in DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Neues in DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Gruppentools im Fokusmodus – Neues in DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: ../../../command-menu/index.md#open-the-command-menu "Öffnen Sie das Befehlsmenü - Befehle ausführen mit Microsoft Edge DevTools Command-Menü | Microsoft Docs"  
[DevtoolsConsoleApiError]: ../../../console/api.md#error "error – Konsolen-API-| Microsoft Docs"  
[DevtoolsCustomizeLocalization]: ../../../customize/localization.md "Ändern der DevTools-Spracheinstellungen | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: ../../../service-workers/index.md "Service Worker-Verbesserungen | Microsoft Docs"  
[DevtoolsSourcesUsingDebuggerPaneToDebugJavascriptCode]: ../../../sources/index.md#using-the-debugger-pane-to-debug-javascript-code "Verwenden des Debuggerbereichs zum Debuggen von JavaScript-Code – Übersicht über das | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: ../../../../progressive-web-apps-chromium/serviceworker.md#the-service-worker-lifecycle "Service Worker-Lebenszyklus – Verwenden von Service Workers zum Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: ../../../../progressive-web-apps-chromium/webappmanifests.md "Verwenden Sie das Web-App-Manifest, um Ihre Progressive Web App in das Betriebssystem zu | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[BrotliMain]: https://www.brotli.org "Brotli"  

[ChromestatusFeature4752739957473280]: https://chromestatus.com/feature/4752739957473280 "Feature: accent-color CSS property | Status der Chrome-Plattform"  

[CsswgDraftsCssUi4WidgetAccent]: https://drafts.csswg.org/css-ui-4/#widget-accent "Widget Accent Colors: die Accent-color-Eigenschaft – CSS Basic User Interface Module Level 4 | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR11374]: https://crbug.com/v8/11374 "Problem 11374: Implementieren der ergonomischen Markenüberprüfung für private Felder"  
[CR761019]: https://crbug.com/761019 "Problem 761019: &quot;Zum Symbol wechseln&quot; verpasst die erste Funktion und bevorzugt eine schlechtere Übereinstimmung, wenn sie alle typisiert zeichen enthält"  
[CR862450]: https://crbug.com/862450 "Problem 862450: [css-scroll-snap] Erwägen Sie das Hinzufügen der Devtools-Funktion für css-Bildlauf-Snap"  
[CR979000]: https://crbug.com/979000 "Problem 979000: Quellzuordnungen mit kollidierenden Quellenpfaden funktionieren nicht."  
[CR1066604]: https://crbug.com/1066604 "Problem 1066604: DevTools: Weitere Informationen zur Installation und Aktivierung von Ereignissen durch ServiceWorker | Chromium Fehler"  
<!--  [CR1066772]: https://crbug.com/1066772 "Issue 1066772: "  locked  -->  
[CR1076198]: https://crbug.com/1076198 "Issue 1076198: [Feature Request] Jump to computed property from `styles` tab"  
[CR1092093]: https://crbug.com/1092093 "Issue 1092093: Make form controls more color stylable by supporting the 'accent-color' CSS property"  
[CR1136655]: https://crbug.com/1136655 "Issue 1136655: Devtools: Localization V2 | Chromium Fehler"  
[CR1142705]: https://crbug.com/1142705 "Issue 1142705: Breakpoints stop working when 2 sourcemaps point to the same virtual file when using webpack"  
[CR1149832]: https://crbug.com/1149832 "Issue 1149832: Feature request: image preview should also show file size"  
[CR1158827]: https://crbug.com/1158827 "Issue 1158827: [Permissions Policy] Implement devtool support for permissions policy"  
[CR1162042]: https://crbug.com/1162042 "Issue 1162042: DevTools: support disabling gzip/brotli/jxl content-encoding"  
[CR1166577]: https://crbug.com/1166577 "Issue 1166577: ☂️ Linear Memory Inspector 1.0"  
[CR1170656]: https://crbug.com/1170656 "Issue 1170656: Show intrinsic aspect-ratio"  
[CR1178305]: "Problem 1178305: Debugger zeigt den Eigenschaftswert eines indizierten Elements nicht an, wenn es mit dem Mauszeiger bewegt https://crbug.com/1178305 wird"  
[CR1180794]: https://crbug.com/1180794 "Issue 1180794: Breakpoints don't work with Closure Compiler inlining optimization"  
[CR1185945]: https://crbug.com/1185945 "Issue 1185945: Manifest warning implies all icons must be square | Chromium Fehler"  
[CR1186049]: https://crbug.com/1186049 "Issue 1186049: Column for Vary: header in Cache Storage viewer"  
[CR1187735]: https://crbug.com/1187735 "Issue 1187735: Accessibility: MAS2.1.1: Keyboard: Unable to invoke the 'Var(..)' function using keyboard | Chromium Fehler"  
[CR1189161]: https://crbug.com/1189161 "Issue 1189161: `new Error` stacktraces are not transformed via DWARF"  
[CR1191465]: https://crbug.com/1191465 "Problem 1191465: STRG+Umschalt+O in HTML unterbrochen"  

[GithubW3cWebappsecPermissionsPolicyPermissionsPolicyExplainerMd]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[GlitchMemoryInspectorDemoJsHtml]: https://memory-inspector.glitch.me/demo-js.html "Arbeitsspeicher in JS | Glitch"  
[GlitchMemoryInspectorDemoWasmHtml]: https://memory-inspector.glitch.me/demo-wasm.html "Arbeitsspeicher in Wasm | Glitch"  

[GlitchMicrosoftEdgeChromiumDevtoolsCssDbgStoriesCssScrollSnapHtml]: https://microsoft-edge-chromium-devtools.glitch.me/css-dbg-stories/css-scroll-snap.html "Scrollen Andocken demo | Glitch"  

[GlitchPermissionPolicyDemoMain]: http://permission-policy-demo.glitch.me "OOPIF Permissions Policy | Glitch"  

[GnuSoftwareGzipManual]: https://www.gnu.org/software/gzip/manual "gzip: Das Datenkomprimierungsprogramm | BETRIEBSSYSTEM &quot;GNU&quot;"  

[HttpwgSpecsRfc7231HtmlHeaderVary]: https://httpwg.org/specs/rfc7231.html#header.vary "Vary - Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content | IETF HTTP Working Group"  

[JsWebpackGuidesCodeSplittingTextThereAreThreeGeneralApproachesToCodeSplittingSplitCodeViaInlineFunctionCallsWithinModules]: https://webpack.js.org/guides/code-splitting/#:~:text=There%20are%20three%20general%20approaches%20to%20code%20splitting,Split%20code%20via%20inline%20function%20calls%20within%20modules. "Es stehen drei allgemeine Ansätze für die Codeteilung zur Verfügung: Einstiegspunkte: Manuell geteilter Code mithilfe der Eingabekonfiguration.  Duplizierung verhindern: Verwenden Sie Eintragsabhängigkeiten oder SplitChunksPlugin zum Deduplizieren und Teilen von Blöcken.  Dynamische Importe: Geteilter Code über Inlinefunktionsaufrufe innerhalb von Modulen. - Codeteilungs-| webpack"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  

[MdnDocsWebJavascriptReferenceOperatorsIn]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/in "in operator | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

[RollupjsMain]: https://rollupjs.org "rollup.js"  

[V8DevFeaturesPrivateBrandChecks]: https://v8.dev/features/private-brand-checks "Private Marke überprüft a.k.a. #foo in obj | V8"  
[V8DevFeaturesClassFieldsPrivateClassFields]: https://v8.dev/features/class-fields#private-class-fields "Private Klassenfelder – Öffentliche und private Klassenfelder | V8"  

[WebpackJsMain]: https://webpack.js.org "webpack"  

> [!NOTE]
> <span data-ttu-id="d7501-398">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7501-398">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d7501-399">Die ursprüngliche Seite findet sich [hier](https://developer.chrome.com/blog/new-in-devtools-91) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7501-399">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="d7501-401">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d7501-401">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
