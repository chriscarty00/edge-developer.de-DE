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
# <a name="whats-new-in-devtools-microsoft-edge-91"></a>Neues in DevTools (Microsoft Edge 91)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="wavy-underlines-highlight-code-issues-and-improvements-in-elements-tool"></a>Wavy unterstreicht Codeprobleme und Verbesserungen im Elementtool  

<!--  Title: Get code hints in Elements tool  -->  
<!--  Subtitle: Wavy underlines like the ones you see in Visual Studio Code now display in the Elements tool.  Underlines alert you to code issues related to accessibility, compatibility, security, performance, and  so on.  -->  

In den meisten modernen IDEs weisen wellenförmige Unterstreichungen unter Text auf Syntaxfehler hin.   In Microsoft Edge Version 91 oder höher werden wellenförmige Unterstreichungen unter HTML in der **DOM-Ansicht** des **Elements-Tools** angezeigt.  Die wellenförmigen Unterstreichungen deuten auf Codeprobleme und Vorschläge im Zusammenhang mit Barrierefreiheit, Kompatibilität, Leistung und so weiter hin.  Weitere Informationen zum Überprüfen und Bearbeiten von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

Führen Sie **eine** der folgenden Aktionen aus, um das Problem zu öffnen und mehr über das Problem und die Behebung zu erfahren.  

*   Wählen Sie `Shift` aus, halten Sie , und wählen Sie dann eine beliebige wellenförmige Unterstreichung aus.  
*   Führen Sie die folgenden Aktionen aus.  
    1.  Zeigen Sie auf eine beliebige wellenförmige Unterstreichung.  
    1.  Öffnen Sie das Kontextmenü \(mit der rechten Maustaste klicken\).  
    1.  Wählen **Sie In Problemen anzeigen aus.**  
        
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues.msft.png" alt-text="Wählen Sie den unterstrichenen Fehler im Elementtool aus." lightbox="../../media/2021/04/elements-iframe-highlight-issues.msft.png":::
         Wählen Sie den unterstrichenen Fehler im **Elementtool** aus.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png" alt-text="Anzeigen von Fehlerdetails im Problemtool" lightbox="../../media/2021/04/elements-iframe-highlight-issues-focus.msft.png":::
         Anzeigen von Fehlerdetails im **Problemtool**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Mehr über DevTools mit informativen QuickInfos erfahren  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<!--  Title: Learn more about DevTools with DevTools Tooltips  -->  
<!--  Subtitle: Informative overlays are now available in the default DevTools interface.  -->  

Das DevTools-Tooltips-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche in DevTools zu erfahren.  Wählen Sie aus, um QuickInfos zu `Esc` deaktivieren.  Führen Sie eine der folgenden Aktionen aus, um QuickInfos zu aktivieren.  

*   Wählen `Ctrl` + `Shift` + `H` Sie \(Windows/Linux\) oder `Cmd` + `Shift` + `H` \(macOS\).  
*   [Öffnen Sie das Befehlsmenü,][DevtoolsCommandMenuIndexOpenCommandMenu] und geben Sie dann `tooltips` ein.  
*   Wählen **Sie Anpassen und Steuern devTools** \( `...` \) > **Hilfe**Umschalten der  >  **DevTools-QuickInfos**.  

Wenn Sie außerdem das Experiment Fokusmodus und [DevTools-Tooltips][DevtoolsWhatsNew202102DevtoolsGroupToolsTogetherInFocusMode] aktivieren, können Sie auch die Schaltfläche **DevTools Tooltips** \( \) am unteren Rand der Aktivitätsleiste umschalten. `?` ****  

Wenn Sie weitere Informationen zur Verwendung der DevTools anzeigen möchten, aktivieren Sie QuickInfos, und zeigen Sie dann auf die einzelnen umrissenen Regionen der DevTools.  

:::image type="complex" source="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png" alt-text="Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des Problemtools, um weitere Details anzuzeigen." lightbox="../../media/2021/04/elements-issues-focus-mode-tooltips.msft.png":::
   Zeigen Sie auf eine beliebige Stelle im hervorgehobenen Bereich des **Problemtools,** um weitere Details anzuzeigen.  
:::image-end:::  

## <a name="service-worker-update-timeline"></a>Zeitachse der Dienstarbeitsmitarbeiteraktualisierung  

<!--todo:  Update the linked [Service Worker improvements][DevtoolsServiceWorkerIndex] article.  -->  

<!--  Title: The tasks associated with your Service Worker  -->  
<!--  Subtitle: Debug with Service Worker Update Cycle  -->  

In Microsoft Edge Version 91 oder höher können Sie, wenn Sie Entwickler von Progressive Web App oder Service Worker sind, den Updatelebenszyklus Ihrer Service Workers als Zeitachse im Anwendungstool **anzeigen.**  Dieses Feature hilft Ihnen, die Zeit zu verstehen, die Ihr Dienstmitarbeiter in den folgenden Phasen verbringt.  

*   **Installieren**  
*   **Warte**  
*   **Aktivieren**  
    
:::image type="complex" source="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png" alt-text="Überprüfen der Zeitachse im Aktualisierungszyklus für Ihren Service Worker" lightbox="../../media/2021/04/application-service-workers-update-cycle-version-73-focus.msft.png":::
   Überprüfen der **Zeitachse** im **Aktualisierungszyklus für** Ihren Service Worker  
:::image-end:::  

Weitere Informationen zum Lebenszyklus Ihrer Service Workers finden Sie unter [The Service Worker lifecycle][ProgressiveWebAppsServiceworkerServiceWorkerLifecycle].  Weitere Informationen zu Debuggingtools für Progressive Web Apps and Service Workers in den DevTools finden Sie unter [Service Worker improvements][DevtoolsServiceWorkerIndex].  Navigieren Sie zu Issue [1066604,][CR1066604]um die Echtzeitupdates für dieses Feature Chromium open-source-Projekt zu überprüfen.  

## <a name="progressive-web-apps-no-longer-display-warnings-for-non-square-icons"></a>Progressive Web Apps zeigen keine Warnungen mehr für nicht quadratische Symbole an  

<!--  Title: Non-square icons in app manifest no longer produce warnings  -->  
<!--  Subtitle: As long as square icons are included in the app manifest, non-square icons no longer produce warnings  -->  

Wenn Sie Microsoft Edge Version [90][DevtoolsWhatsNew202102Devtools] oder früher ein nicht quadratisches Symbol in das Web-App-Manifest Ihrer **** PWA aufgenommen haben, wurde im Abschnitt **Manifest** im Anwendungstool eine Warnung unter **Fehler** und Warnungen für jedes nicht quadratische Symbol angezeigt.  In Microsoft Edge Version 91 oder höher werden **** im **Abschnitt Manifest** im Anwendungstool keine Warnungen angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen.  Wenn Sie keine quadratischen Symbole bereitstellen, wird die folgende Meldung in einer Warnung angezeigt.  

```output
Most operating systems require square icons.  Please include at least one square icon in the array.  
```  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt." lightbox="../../media/2021/04/edge89-application-manifest-errors-and-warnings.msft.png":::
         In Microsoft Edge Version 90 oder früher wird für jedes nicht quadratische Symbol ein Fehler angezeigt.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png" alt-text="In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen" lightbox="../../media/2021/04/edge91-application-manifest-errors-and-warnings.msft.png":::
         In Microsoft Edge Version 91 oder höher wird kein Fehler angezeigt, wenn Sie mindestens ein quadratisches Symbol bereitstellen  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Um Fehler und Warnungen in Ihrem Web App-Manifest zu überprüfen, navigieren Sie zum **Anwendungstool,** und wählen Sie den **Abschnitt Manifest** aus.  Fehler und Warnungen werden unter der Überschrift **Fehler und Warnungen** aufgeführt.  Weitere Informationen zum Web App-Manifest finden Sie unter Verwenden des [Web-App-Manifests,][ProgressiveWebAppsWebappmanifests]um Ihre Progressive Web App in das Betriebssystem zu integrieren.  Navigieren Sie zum [PWABuilder][PwabuilderImagegenerator]Image Generator, um Symbole zu erstellen, die in Ihr Web-App-Manifest enthalten sind.  Navigieren Sie zu Problem [1185945,][CR1185945]um die Echtzeitupdates für dieses Feature im Chromium open-source-Projekt zu überprüfen.  

## <a name="localized-devtools-now-supported-in-chromium-based-browsers"></a>Lokalisierte DevTools werden jetzt in Chromium Browsern unterstützt  

<!--  Title: Localization for all  -->  
<!--  Subtitle: Match browser language enabled to all Chromium-based browsers  -->  

Ab Microsoft Edge [Version 81][DevtoolsWhatsNew202001DevtoolsUsingDevtoolsInOtherLanguages]wird Microsoft Edge DevTools in Ihrer eigenen Sprache angezeigt.  Viele Entwickler verwenden andere Entwicklertools wie StackOverflow und Visual Studio Code in ihrer eigenen Sprache, nicht nur in Englisch.  Das Microsoft Edge DevTools-Team, das Chrome DevTools-Team und das Google -Leuchtturm-Team haben zusammengearbeitet, um die gleiche Erfahrung in allen Chromium Browsern zu bieten.  Weitere Informationen zur Verwendung von DevTools in Ihrer Sprache finden Sie unter [Ändern der DevTools-Spracheinstellungen.][DevtoolsCustomizeLocalization]  Weitere Informationen zur Zusammenarbeit an diesem Feature in Chromium Open Source-Projekt finden Sie unter [1136655][CR1136655].  

:::image type="complex" source="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png" alt-text="Microsoft Edge Browser und DevTools auf Japanisch festgelegt" lightbox="../../media/2021/04/japanese-browser-japanese-navigation-elements-3d-view.msft.png":::
   Microsoft Edge Browser und DevTools auf Japanisch festgelegt  
:::image-end:::  

## <a name="use-the-keyboard-to-navigate-to-css-variables"></a>Navigieren zu CSS-Variablen mithilfe der Tastatur  

<!--  Title: Navigate to CSS variables with the arrow keys  -->  
<!--  Subtitle: In the Styles pane, use the arrow keys to choose CSS variables.  Select `Enter` to see the variable definition.  -->  

Ab Microsoft Edge [Version 88][DevtoolsWhatsNew202011DevtoolsCssVariableDefinitionsInStylesPane]zeigt **** der Bereich Formatvorlagen CSS-Variablen an und stellt einen Link direkt zur Definition der einzelnen Variablen zur Seite.  In Microsoft Edge Version 91 oder höher können Sie die Pfeiltasten verwenden, um problemlos zu CSS-Variablen zu navigieren.  Um die Definition im Bereich **Formatvorlagen** zu öffnen, zeigen Sie auf eine Variable, und wählen Sie dann `Enter` aus.  Weitere Informationen zu CSS-Variablen finden Sie unter [Verwenden benutzerdefinierter CSS-Eigenschaften (Variablen).][MdnDocsWebCssUsingCssCustomProperties]  Navigieren Sie zu Issue [1187735,][CR1187735]um Echtzeitupdates für dieses Feature im Chromium open-source-Projekt zu überprüfen.  

:::image type="complex" source="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png" alt-text="Die CSS-Variable --theme-body-background, die im Bereich Formatvorlagen hervorgehoben ist" lightbox="../../media/2021/04/elements-styles-body-background-color-theme-body-background.msft.png":::
   Die `--theme-body-background` im Bereich Formatvorlagen hervorgehobene **CSS-Variable**  
:::image-end:::  

## <a name="issues-are-automatically-sorted-by-severity"></a>Probleme werden automatisch nach Schweregrad sortiert  

<!-- Title: Display Issues in severity order  -->  
<!-- Subtitle: Entries in the Issues tool now display in severity order and allow you to focus your updates on the most important issues. -->  

Das **Tool Probleme** zeigt Empfehlungen zur Verbesserung Ihrer Website an, einschließlich Barrierefreiheit, Leistung, Sicherheit und so weiter. Basierend auf Ihrem Feedback werden Probleme jetzt automatisch nach Schweregrad sortiert.  In jeder Feedbackkategorie wird jedes **** als Fehler markierte Problem zuerst angezeigt, gefolgt von jedem Als Warnung gekennzeichneten Problem **und**anschließend jedem Problem, das als Tipp **gekennzeichnet ist.**  Um Ihre Probleme zu verfeinern, sind zusätzliche Filteroptionen für ein zukünftiges Update geplant.  Weitere Informationen zum Überprüfen von Problemen finden Sie unter Suchen und Beheben von Problemen [mit dem Tool Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2021/04/elements-issues-ordered-issues.msft.png" alt-text="Das Tool Probleme zeigt sortierte Probleme nach Schweregrad an." lightbox="../../media/2021/04/elements-issues-ordered-issues.msft.png":::
   Das **Tool Probleme** zeigt sortierte Probleme nach Schweregrad an.  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-117"></a>Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.7  

<!-- Title: Microsoft Edge DevTools for Visual Studio version 1.1.7  -->  
<!-- Subtitle: Increased target closure reliability, automatically update the side panel, new contextual menu for settings and Changelog, and more. -->  

Die [Microsoft Edge Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterung, Version 1.1.7, stellt die DevTools aus Microsoft Edge Version [88 bereit.][DevtoolsWhatsNew202011Devtools]  Diese Erweiterung unterstützt jetzt ARM Geräte und hängt nicht mehr vom [Debugger][VisualstudioMarketplaceMsjsdiagDebuggerForEdge] für Microsoft Edge ab.  Version 1.1.7 enthält die folgenden Fehlerbehebungen und Verbesserungen.  

*   Die Zuverlässigkeit der Zielschließung wurde aktualisiert.  
*   Der Seitenbereich wurde so aktualisiert, dass er automatisch aktualisiert wird, wenn Sie ziele debuggen, die erstellt oder zerstört werden.  
*   Es wurde ein neues kontextbezogenes Menü hinzugefügt, mit dem Sie schneller auf die Erweiterungseinstellungen und das neueste Changelog zugreifen können.  
*   Die Veröffentlichung der Erweiterungsdokumentation einschließlich der neuesten Features wurde aktualisiert und vereinfacht.  
    
Um manuell auf Version 1.1.7 zu aktualisieren, navigieren Sie zu [Manuelles Aktualisieren einer Erweiterung.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] mitwirken.  

<!--## Announcements from the Chromium project  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Ipsum et Chromium  

Lorem al lorem et Chromium  To review the history of this feature in the Chromium open-source project, navigate to Issue [xxxxxxx][CRxxxxxxx].  

:::image type="complex" source="../../media/2021/04/lorem-et-chromium.msft.png" alt-text="Ipsum et Chromium" lightbox="../../media/2021/04/lorem-et-chromium.msft.png":::
   Ipsum et Chromium  
:::image-end:::  -->  

## <a name="download-the-microsoft-edge-preview-channels"></a>Herunterladen der Microsoft Edge-Vorschaukanäle  

Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.  Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen  

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
