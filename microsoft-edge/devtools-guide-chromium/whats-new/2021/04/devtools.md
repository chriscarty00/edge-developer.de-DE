---
description: Wavy unterstreicht Codeprobleme im Elementtool, in der Zeitachse für Dienstarbeitsaktualisierungen und vieles mehr.
title: Neues in DevTools (Microsoft Edge 91)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3a2be4d309432de4421af73ca7b4d21734ad5221
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514456"
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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a><span data-ttu-id="cbcbe-104">Neues in DevTools (Microsoft Edge 91)</span><span class="sxs-lookup"><span data-stu-id="cbcbe-104">What's New In DevTools (Microsoft Edge 91)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a><span data-ttu-id="cbcbe-105">Wavy unterstreicht Codeprobleme und Verbesserungen im Elementtool</span><span class="sxs-lookup"><span data-stu-id="cbcbe-105">Wavy underlines highlight code issues and improvements in Elements tool</span></span>  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

<span data-ttu-id="cbcbe-106">In den meisten modernen IDEs weisen wellenförmige Unterstreichungen unter Text auf Syntaxfehler hin.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-106">In most modern IDEs, wavy underlines under text indicate syntax errors.</span></span>   <span data-ttu-id="cbcbe-107">In Microsoft Edge Version 91 oder höher werden wellenförmige Unterstreichungen unter HTML in der **DOM-Ansicht** des **Elements-Tools** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-107">In Microsoft Edge version 91 or later, wavy underlines display under HTML in the **DOM** view of the **Elements** tool.</span></span>  <span data-ttu-id="cbcbe-108">Die wellenförmigen Unterstreichungen deuten auf Codeprobleme und Vorschläge im Zusammenhang mit Barrierefreiheit, Kompatibilität, Leistung und so weiter hin.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-108">The wavy underlines indicate code issues and suggestions related to accessibility, compatibility, performance, and so on.</span></span>  <span data-ttu-id="cbcbe-109">Weitere Informationen zum Überprüfen und Bearbeiten von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="cbcbe-109">For more information about how to review and edit issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

<span data-ttu-id="cbcbe-110">Führen Sie **eine** der folgenden Aktionen aus, um das Problem zu öffnen und mehr über das Problem und die Behebung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-110">To open the **Issues** tool and learn more about the issue and how to fix it, complete one of the following actions.</span></span>  

*   <span data-ttu-id="cbcbe-111">Wählen Sie `Shift` aus, halten Sie , und wählen Sie dann eine beliebige wellenförmige Unterstreichung aus.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-111">Select and hold `Shift`, and then choose any wavy underline.</span></span>  
*   <span data-ttu-id="cbcbe-112">Führen Sie die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-112">Complete the following actions.</span></span>  
    1.  <span data-ttu-id="cbcbe-113">Zeigen Sie auf eine beliebige wellenförmige Unterstreichung.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-113">Hover on any wavy underline.</span></span>  
    1.  <span data-ttu-id="cbcbe-114">Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).</span><span class="sxs-lookup"><span data-stu-id="cbcbe-114">Open the contextual menu \(right-click\).</span></span>  
    1.  <span data-ttu-id="cbcbe-115">Wählen **Sie In Problemen anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="cbcbe-115">Choose **Show in Issues**.</span></span>  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Wählen Sie den unterstrichenen Fehler im Elementtool aus." lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         <span data-ttu-id="cbcbe-117">Wählen Sie den unterstrichenen Fehler im **Elementtool** aus.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-117">Choose the underlined error in the **Elements** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Anzeigen von Fehlerdetails im Problemtool" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         <span data-ttu-id="cbcbe-119">Anzeigen von Fehlerdetails im **Problemtool**</span><span class="sxs-lookup"><span data-stu-id="cbcbe-119">Display error details in the **Issues** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="cbcbe-120">Mehr über DevTools mit informativen QuickInfos erfahren</span><span class="sxs-lookup"><span data-stu-id="cbcbe-120">Learn about DevTools with informative tooltips</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

<span data-ttu-id="cbcbe-121">Das DevTools-Tooltips-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche in DevTools zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-121">The DevTools Tooltips feature helps you learn about all the different tools and panes in DevTools.</span></span>  <span data-ttu-id="cbcbe-122">Wählen Sie aus, um QuickInfos zu `Esc` deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-122">To turn off Tooltips, select `Esc`.</span></span>  <span data-ttu-id="cbcbe-123">Führen Sie eine der folgenden Aktionen aus, um QuickInfos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-123">To turn on Tooltips, complete one of the following actions.</span></span>  

*   <span data-ttu-id="cbcbe-124">Wählen `Ctrl` + `Shift` + `H` Sie \(Windows/Linux\) oder `Cmd` + `Shift` + `H` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="cbcbe-124">Select `Ctrl`+`Shift`+`H` \(Windows/Linux\) or `Cmd`+`Shift`+`H` \(macOS\).</span></span>  
*   <span data-ttu-id="cbcbe-125">[Öffnen Sie das Befehlsmenü,][DevtoolsCommandMenuIndexOpenCommandMenu] und geben Sie dann `tooltips` ein.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-125">[Open the Command Menu][DevtoolsCommandMenuIndexOpenCommandMenu] and then type `tooltips`.</span></span>  
*   <span data-ttu-id="cbcbe-126">Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > **Hilfe**Umschalten der  >  **DevTools-QuickInfos**.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-126">Choose **Customize and control DevTools** \(`...`\) > **Help** > **Toggle the DevTools Tooltips**.</span></span>  

<span data-ttu-id="cbcbe-127">Wenn Sie außerdem das Experiment Fokusmodus und [DevTools-Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] aktivieren, können Sie auch die Schaltfläche **DevTools Tooltips** \( \) am unteren Rand der Aktivitätsleiste umschalten. `?` \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cbcbe-127">Also, if you turn on the [Focus Mode and DevTools Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] experiment, you may also choose the **Toggle the DevTools Tooltips** \(`?`\) button at the bottom of the **Activity Bar**.</span></span>  

<span data-ttu-id="cbcbe-128">Wenn Sie weitere Informationen zur Verwendung der DevTools anzeigen möchten, aktivieren Sie QuickInfos, und zeigen Sie dann auf die einzelnen umrissenen Regionen der DevTools.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-128">To display more information about how to use the DevTools, turn on Tooltips, and then hover on each outlined region of the DevTools.</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des Problemtools, um weitere Details anzuzeigen." lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   <span data-ttu-id="cbcbe-130">Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des **Problemtools,** um weitere Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-130">Hover on anywhere in the highlighted region of the **Issues** tool to display more details</span></span>  
:::image-end:::  

## <a name="service-worker-update-timeline"></a><span data-ttu-id="cbcbe-131">Zeitachse der Dienstarbeitsmitarbeiteraktualisierung</span><span class="sxs-lookup"><span data-stu-id="cbcbe-131">Service worker update timeline</span></span>  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

<span data-ttu-id="cbcbe-132">In Microsoft Edge Version 91 oder höher können Sie, wenn Sie Entwickler von Progressive Web App oder Service Worker sind, den Updatelebenszyklus Ihrer Service Workers als Zeitachse im Anwendungstool **anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="cbcbe-132">In Microsoft Edge version 91 or later, if you are a Progressive Web App or Service Worker developer, you may display the update lifecycle of your Service Workers as a timeline in the **Application** tool.</span></span>  <span data-ttu-id="cbcbe-133">Dieses Feature hilft Ihnen, die Zeit zu verstehen, die Ihr Dienstmitarbeiter in den folgenden Phasen verbringt.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-133">This feature helps you understand the time your Service Worker spends in each of the following stages.</span></span>  

*   **<span data-ttu-id="cbcbe-134">Installieren</span><span class="sxs-lookup"><span data-stu-id="cbcbe-134">Install</span></span>**  
*   **<span data-ttu-id="cbcbe-135">Warte</span><span class="sxs-lookup"><span data-stu-id="cbcbe-135">Wait</span></span>**  
*   **<span data-ttu-id="cbcbe-136">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="cbcbe-136">Activate</span></span>**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Überprüfen der Zeitachse im Aktualisierungszyklus für Ihren Service Worker" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   <span data-ttu-id="cbcbe-138">Überprüfen der **Zeitachse** im **Aktualisierungszyklus für** Ihren Service Worker</span><span class="sxs-lookup"><span data-stu-id="cbcbe-138">Review the **Timeline** in the **Update Cycle** for your Service Worker</span></span>  
:::image-end:::  

<span data-ttu-id="cbcbe-139">Weitere Informationen zum Lebenszyklus Ihrer Service Workers finden Sie unter [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span><span class="sxs-lookup"><span data-stu-id="cbcbe-139">For more information about the lifecycle of your Service Workers, navigate to [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].</span></span>  <span data-ttu-id="cbcbe-140">Weitere Informationen zu Debuggingtools für Progressive Web Apps and Service Workers in den DevTools finden Sie unter [Service Worker improvements][DevtoolsServiceWorkerIndex].</span><span class="sxs-lookup"><span data-stu-id="cbcbe-140">For more information about debugging tools for Progressive Web Apps and Service Workers in the DevTools, navigate to [Service Worker improvements][DevtoolsServiceWorkerIndex].</span></span>  <span data-ttu-id="cbcbe-141">Navigieren Sie zu Issue [1066604,][CR1066604]um die Echtzeitupdates für dieses Feature Chromium open-source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-141">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1066604][CR1066604].</span></span>  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a><span data-ttu-id="cbcbe-142">Progressive Web Apps zeigen keine Warnungen mehr für nicht quadratische Symbole an</span><span class="sxs-lookup"><span data-stu-id="cbcbe-142">Progressive Web Apps no longer display warnings for non-square icons</span></span>  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

<span data-ttu-id="cbcbe-143">Wenn Sie Microsoft Edge Version [90][DevtoolsWhatsNew202102Devtools] oder früher ein nicht quadratisches Symbol in das Web-App-Manifest Ihrer \*\*\*\* PWA aufgenommen haben, wurde im Abschnitt **Manifest** im Anwendungstool eine Warnung unter **Fehler** und Warnungen für jedes nicht quadratische Symbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-143">In [Microsoft Edge version 90][DevtoolsWhatsNew202102Devtools] or earlier, if you included a non-square icon in the Web App Manifest of your PWA, the **Manifest** section in the **Application** tool displayed a warning under **Errors and Warnings** for each non-square icon.</span></span>  <span data-ttu-id="cbcbe-144">In Microsoft Edge Version 91 oder höher werden \*\*\*\* im **Abschnitt Manifest** im Anwendungstool keine Warnungen angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-144">In Microsoft Edge version 91 or later, the **Manifest** section in the **Application** tool displays no warnings if you provide at least one square icon.</span></span>  <span data-ttu-id="cbcbe-145">Wenn Sie keine quadratischen Symbole bereitstellen, wird die folgende Meldung in einer Warnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-145">If you don't provide any square icons, a warning displays the following message.</span></span>  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt." lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="cbcbe-147">In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-147">In Microsoft Edge version 90 or earlier, an error displays for each icon that is non-square</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         <span data-ttu-id="cbcbe-149">In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen</span><span class="sxs-lookup"><span data-stu-id="cbcbe-149">In Microsoft Edge version 91 or later, no error displays when you provide at least one square icon</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="cbcbe-150">Um Fehler und Warnungen in Ihrem Web App-Manifest zu überprüfen, navigieren Sie zum **Anwendungstool,** und wählen Sie den **Abschnitt Manifest** aus.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-150">To review errors and warnings in your Web App Manifest, navigate to the **Application** tool and choose the **Manifest** section.</span></span>  <span data-ttu-id="cbcbe-151">Fehler und Warnungen werden unter der Überschrift **Fehler und Warnungen** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-151">Errors and warnings are listed under the **Errors and Warnings** heading.</span></span>  <span data-ttu-id="cbcbe-152">Weitere Informationen zum Web App-Manifest finden Sie unter Verwenden des [Web-App-Manifests,][ProgressiveWebAppsWebappmanifests]um Ihre Progressive Web App in das Betriebssystem zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-152">For more information about the Web App Manifest, navigate to [Use the Web App Manifest to integrate your Progressive Web App into the Operating System][ProgressiveWebAppsWebappmanifests].</span></span>  <span data-ttu-id="cbcbe-153">Navigieren Sie zum [PWABuilder][PwabuilderImagegenerator]Image Generator, um Symbole zu erstellen, die in Ihr Web-App-Manifest enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-153">To create icons to include in your Web App Manifest, navigate to the [PWABuilder Image Generator][PwabuilderImagegenerator].</span></span>  <span data-ttu-id="cbcbe-154">Navigieren Sie zu Problem [1185945,][CR1185945]um die Echtzeitupdates für dieses Feature im Chromium open-source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-154">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1185945][CR1185945].</span></span>  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a><span data-ttu-id="cbcbe-155">Lokalisierte DevTools werden jetzt in Chromium Browsern unterstützt</span><span class="sxs-lookup"><span data-stu-id="cbcbe-155">Localized DevTools now supported in Chromium-based browsers</span></span>  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

<span data-ttu-id="cbcbe-156">Ab Microsoft Edge [Version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]wird Microsoft Edge DevTools in Ihrer eigenen Sprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-156">Starting in [Microsoft Edge version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages], Microsoft Edge DevTools displays in your own language.</span></span>  <span data-ttu-id="cbcbe-157">Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio Code in ihrer eigenen Sprache, nicht nur in Englisch.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-157">Many developers use other developer tools like StackOverflow and Visual Studio Code in their native language, not just in English.</span></span>  <span data-ttu-id="cbcbe-158">Das Microsoft Edge DevTools-Team, das Chrome DevTools-Team und das Google -Leuchtturm-Team haben zusammengearbeitet, um die gleiche Erfahrung in allen Chromium Browsern zu bieten.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-158">The Microsoft Edge DevTools team, Chrome DevTools team, and the Google Lighthouse team collaborated to provide the same experience in all Chromium-based browsers.</span></span>  <span data-ttu-id="cbcbe-159">Weitere Informationen zur Verwendung von DevTools in Ihrer Sprache finden Sie unter [Ändern der DevTools-Spracheinstellungen.][DevtoolsCustomizeLocalization]</span><span class="sxs-lookup"><span data-stu-id="cbcbe-159">For more information about how to use DevTools in your language, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  <span data-ttu-id="cbcbe-160">Weitere Informationen zur Zusammenarbeit an diesem Feature in Chromium Open Source-Projekt finden Sie unter [1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="cbcbe-160">For more information about the collaboration on this feature in the Chromium open-source project, navigate to [1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge Browser und DevTools auf Japanisch festgelegt" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   <span data-ttu-id="cbcbe-162">Microsoft Edge Browser und DevTools auf Japanisch festgelegt</span><span class="sxs-lookup"><span data-stu-id="cbcbe-162">Microsoft Edge browser and DevTools set to Japanese</span></span>  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a><span data-ttu-id="cbcbe-163">Navigieren zu CSS-Variablen mithilfe der Tastatur</span><span class="sxs-lookup"><span data-stu-id="cbcbe-163">Use the keyboard to navigate to CSS variables</span></span>  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

<span data-ttu-id="cbcbe-164">Ab Microsoft Edge [Version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]zeigt \*\*\*\* der Bereich Formatvorlagen CSS-Variablen an und stellt einen Link direkt zur Definition der einzelnen Variablen zur Seite.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-164">Starting in [Microsoft Edge version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane], the **Styles** pane displays CSS variables and provides a link directly to the definition of each variable.</span></span>  <span data-ttu-id="cbcbe-165">In Microsoft Edge Version 91 oder höher können Sie die Pfeiltasten verwenden, um problemlos zu CSS-Variablen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-165">In Microsoft Edge version 91 or later, you may use the arrow keys to easily navigate to CSS variables.</span></span>  <span data-ttu-id="cbcbe-166">Um die Definition im Bereich **Formatvorlagen** zu öffnen, zeigen Sie auf eine Variable, und wählen Sie dann `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-166">To open the definition in the **Styles** pane, hover on a variable, and then select `Enter`.</span></span>  <span data-ttu-id="cbcbe-167">Weitere Informationen zu CSS-Variablen finden Sie unter [Verwenden benutzerdefinierter CSS-Eigenschaften (Variablen).][MdnDocsWebCssUsingCssCustomProperties]</span><span class="sxs-lookup"><span data-stu-id="cbcbe-167">For more information about CSS variables, navigate to [Using CSS custom properties (variables)][MdnDocsWebCssUsingCssCustomProperties].</span></span>  <span data-ttu-id="cbcbe-168">Navigieren Sie zu Issue [1187735,][CR1187735]um Echtzeitupdates für dieses Feature im Chromium open-source-Projekt zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-168">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1187735][CR1187735].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Die CSS-Variable --theme-body-background, die im Bereich Formatvorlagen hervorgehoben ist" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   <span data-ttu-id="cbcbe-170">Die `--theme-body-background` im Bereich Formatvorlagen hervorgehobene **CSS-Variable**</span><span class="sxs-lookup"><span data-stu-id="cbcbe-170">The `--theme-body-background` CSS variable highlighted in the **Styles** pane</span></span>  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a><span data-ttu-id="cbcbe-171">Probleme werden automatisch nach Schweregrad sortiert</span><span class="sxs-lookup"><span data-stu-id="cbcbe-171">Issues are automatically sorted by severity</span></span>  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

<span data-ttu-id="cbcbe-172">Das **Tool Probleme** zeigt Empfehlungen zur Verbesserung Ihrer Website an, einschließlich Barrierefreiheit, Leistung, Sicherheit und so weiter.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-172">The **Issues** tool displays recommendations to improve your website, including accessibility, performance, security, and so on.</span></span> <span data-ttu-id="cbcbe-173">Basierend auf Ihrem Feedback werden Probleme jetzt automatisch nach Schweregrad sortiert.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-173">Based on your feedback, issues are now automatically sorted by severity.</span></span>  <span data-ttu-id="cbcbe-174">In jeder Feedbackkategorie wird jedes \*\*\*\* als Fehler markierte Problem zuerst angezeigt, gefolgt von jedem Als Warnung gekennzeichneten Problem **und**anschließend jedem Problem, das als Tipp **gekennzeichnet ist.**</span><span class="sxs-lookup"><span data-stu-id="cbcbe-174">In each feedback category, each issue marked as an **Error** appears first, followed each issue marked as a **Warning**, then each issue marked as a **Tip**.</span></span>  <span data-ttu-id="cbcbe-175">Um Ihre Probleme zu verfeinern, sind zusätzliche Filteroptionen für ein zukünftiges Update geplant.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-175">To help you refine your issues, extra filter options are planned for a future update.</span></span>  <span data-ttu-id="cbcbe-176">Weitere Informationen zum Überprüfen von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="cbcbe-176">For more information about how to review issues, navigate to [Find and fix problems with the Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="Das Tool Probleme zeigt sortierte Probleme nach Schweregrad an." lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   <span data-ttu-id="cbcbe-178">Das **Tool Probleme** zeigt sortierte Probleme nach Schweregrad an.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-178">The **Issues** tool displays sorted issues by severity</span></span>  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a><span data-ttu-id="cbcbe-179">Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.7</span><span class="sxs-lookup"><span data-stu-id="cbcbe-179">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.7</span></span>  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

<span data-ttu-id="cbcbe-180">Die [Microsoft Edge Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterung, Version 1.1.7, stellt die DevTools aus Microsoft Edge Version [88 bereit.][DevtoolsWhatsNew202011Devtools]</span><span class="sxs-lookup"><span data-stu-id="cbcbe-180">The [Microsoft Edge Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.7 provides the DevTools from [Microsoft Edge version 88][DevtoolsWhatsNew202011Devtools].</span></span>  <span data-ttu-id="cbcbe-181">Diese Erweiterung unterstützt jetzt ARM Geräte und hängt nicht mehr vom [Debugger][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] für Microsoft Edge ab.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-181">This extension now supports ARM devices and no longer depends on the [Debugger for Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] extension.</span></span>  <span data-ttu-id="cbcbe-182">Version 1.1.7 enthält die folgenden Fehlerbehebungen und Verbesserungen.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-182">Version 1.1.7 includes the following bug fixes and improvements.</span></span>  

*   <span data-ttu-id="cbcbe-183">Die Zuverlässigkeit der Zielschließung wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-183">Updated the reliability of target closure.</span></span>  
*   <span data-ttu-id="cbcbe-184">Der Seitenbereich wurde so aktualisiert, dass er automatisch aktualisiert wird, wenn Sie ziele debuggen, die erstellt oder zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-184">Updated the side panel to automatically refreshes when you debug targets that are created or destroyed.</span></span>  
*   <span data-ttu-id="cbcbe-185">Es wurde ein neues kontextbezogenes Menü hinzugefügt, mit dem Sie schneller auf die Erweiterungseinstellungen und das neueste Changelog zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-185">Added a new contextual menu that gives you faster access to the extension settings and the latest Changelog.</span></span>  
*   <span data-ttu-id="cbcbe-186">Die Veröffentlichung der Erweiterungsdokumentation einschließlich der neuesten Features wurde aktualisiert und vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-186">Updated and simplified the release of extension documentation including the newest features.</span></span>  
    
<span data-ttu-id="cbcbe-187">Um manuell auf Version 1.1.7 zu aktualisieren, navigieren Sie zu [Manuelles Aktualisieren einer Erweiterung.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="cbcbe-187">To manually update to version 1.1.7, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="cbcbe-188">Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] mitwirken.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-188">You may file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="cbcbe-189">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="cbcbe-189">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="cbcbe-190">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-190">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="cbcbe-191">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="cbcbe-191">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="cbcbe-192">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="cbcbe-192">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]: ../../2020/01/devtools.md#using-the-devtools-in-other-languages "Verwenden der DevTools in anderen Sprachen – Neues in DevTools (Microsoft Edge 81) | Microsoft Docs"  
[DevtoolsWhatsNew202011Devtools]: ../../2020/11/devtools.md "Neues in DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools#css-variable-definitions-in-styles-pane "CSS-Variablendefinitionen im Formatvorlagenbereich – Neues in DevTools (Microsoft Edge 88) | Microsoft Docs"  
[DevtoolsWhatsNew202102Devtools]: ../02/devtools.md "Neues in DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode]: ../02/devtools.md#group-tools-together-in-focus-mode "Gruppentools im Fokusmodus – Neues in DevTools (Microsoft Edge 90) | Microsoft Docs"  

[DevtoolsCommandMenuIndexOpenCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Öffnen Sie das Befehlsmenü - Befehle ausführen mit Microsoft Edge DevTools Command-Menü | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Ändern der DevTools-Spracheinstellungen | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Erkennen und Beheben von Problemen mit dem Microsoft Edge DevTools-Tool „Probleme“ | Microsoft Docs"  
[DevtoolsServiceWorkerIndex]: /microsoft-edge/devtools-guide-chromium/service-workers/index "Service Worker-Verbesserungen | Microsoft Docs"  

[ProgressiveWebAppsServiceworkerServiceWorkerLifecycle]: /microsoft-edge/progressive-web-apps-chromium/serviceworker#the-service-worker-lifecycle "Service Worker-Lebenszyklus – Verwenden von Service Workers zum Verwalten von Netzwerkanforderungen und Pushbenachrichtigungen | Microsoft Docs"  
[ProgressiveWebAppsWebappmanifests]: /microsoft-edge/progressive-web-apps-chromium/webappmanifests "Verwenden Sie das Web-App-Manifest, um Ihre Progressive Web App in das Betriebssystem zu | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
<!--[GithubMicrosoftVscodeEdgeDevtoolsPullxxx]: https://github.com/microsoft/vscode-edge-devtools/pull/xxx "Pull xxx: Lorem al Ipsum | GitHub"  -->  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools für Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerForEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Debugger für Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR1066604]: https://crbug.com/1066604 "Problem 1066604: DevTools: Weitere Informationen zur Installation und Aktivierung von Ereignissen durch ServiceWorker | Chromium-Fehler"  
[CR1136655]: https://crbug.com/1136655 "Problem 1136655: Devtools: Lokalisierung V2 | Chromium-Fehler"  
[CR1185945]: https://crbug.com/1185945 "Problem 1185945: Manifestwarnung impliziert, dass alle Symbole quadratisch sein | Chromium-Fehler"  
[CR1187735]: https://crbug.com/1187735 "Problem 1187735: Barrierefreiheit: MAS2.1.1: Tastatur: Die Var(..)-Funktion kann nicht mithilfe von Tastatureingaben | Chromium-Fehler"  

[MdnDocsWebCssUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Verwenden von benutzerdefinierten CSS-Eigenschaften (Variablen) | MDN"  

[PwabuilderImagegenerator]: https://www.pwabuilder.com/imageGenerator "Image Generator | PWABuilder"  

<!--  > [!NOTE]
> Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].  
> The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-91) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen
-->
