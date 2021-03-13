---
description: Debugunterstützung für CSS Flexbox, Leistungskopfanzeige auf der Webseite, Probleme mit Toolupdates und mehr
title: Neues in DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408509"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a><span data-ttu-id="a14a8-104">Neues in DevTools (Microsoft Edge 90)</span><span class="sxs-lookup"><span data-stu-id="a14a8-104">What's New In DevTools (Microsoft Edge 90)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a><span data-ttu-id="a14a8-105">Gruppieren von Tools im Fokusmodus</span><span class="sxs-lookup"><span data-stu-id="a14a8-105">Group tools together in Focus Mode</span></span>  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

<span data-ttu-id="a14a8-106">Der Fokusmodus ist eine experimentelle Schnittstelle, mit der Sie verschiedene Tools basierend auf Ihren eigenen Debuggingszenarien gruppieren können.</span><span class="sxs-lookup"><span data-stu-id="a14a8-106">Focus Mode is an experimental interface that allows you to group different tools together based on your own debugging scenarios.</span></span>  <span data-ttu-id="a14a8-107">Die neue **Aktivitätsleiste,** die auf der linken Seite angezeigt wird, enthält vordefinierte Toolgruppen wie **Layout** und **Debugging.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-107">The new **Activity Bar** displayed on the left includes predefined tool groups such as **Layout** and **Debugging**.</span></span>  <span data-ttu-id="a14a8-108">Schließen Sie zum Anpassen jeder Toolgruppe Tools mit dem Symbol Schließen **\(** \) oder fügen Sie mit dem Symbol Weitere Tools \( \) neue Tools `X` \*\*\*\* `+` hinzu.</span><span class="sxs-lookup"><span data-stu-id="a14a8-108">To customize each tool group, close tools with the **Close** \(`X`\) icon or add new tools with the **More tools** \(`+`\) icon.</span></span>  

<span data-ttu-id="a14a8-109">Navigieren Sie zum Aktivieren [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] des Experiments zu Aktivieren experimenteller Features, und wählen Sie die Kontrollkästchen neben Fokusmodus und **DevTools-Toolinfos** und Registerkartenmenüs Aktivieren + aus, um weitere Tools **zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-109">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="a14a8-110">Weitere Informationen zu diesem Feature oder zum Kommentieren mit Fragen und Ideen finden Sie unter [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="a14a8-110">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Anzeigen der Aktivitätsleiste" lightbox="../../media/2021/02/focus-mode.msft.png":::
   <span data-ttu-id="a14a8-112">Anzeigen der **Aktivitätsleiste**</span><span class="sxs-lookup"><span data-stu-id="a14a8-112">Display the **Activity Bar**</span></span>  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="a14a8-113">Informationen zu DevTools mit informativen QuickInfos</span><span class="sxs-lookup"><span data-stu-id="a14a8-113">Learn about DevTools with informative tooltips</span></span>  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

<span data-ttu-id="a14a8-114">Das DevTools-Tooltips-Feature hilft Ihnen, mehr über alle verschiedenen Tools und Bereiche zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="a14a8-114">The DevTools Tooltips feature helps you learn about all the different tools and panes.</span></span>  <span data-ttu-id="a14a8-115">Wählen Sie das Symbol Hilfe \( \) am unteren Rand der Aktivitätsleiste aus, um `?` quickInfos \*\*\*\* in den DevTools umschalten zu können.</span><span class="sxs-lookup"><span data-stu-id="a14a8-115">Choose the Help \(`?`\) icon at the bottom of the **Activity Bar** to toggle tooltips in the DevTools.</span></span>  <span data-ttu-id="a14a8-116">Wenn QuickInfos verfügbar sind, zeigen Sie auf jeden umrissenen Bereich von DevTools, um mehr über die Verwendung des Tools zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="a14a8-116">When tooltips are on, hover over each outlined region of DevTools to learn more about how to use the tool.</span></span>  <span data-ttu-id="a14a8-117">Navigieren Sie zum Aktivieren [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] des Experiments zu Aktivieren experimenteller Features, und wählen Sie die Kontrollkästchen neben Fokusmodus und **DevTools-Toolinfos** und Registerkartenmenüs Aktivieren + aus, um weitere Tools **zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-117">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="a14a8-118">Weitere Informationen zu diesem Feature oder zum Kommentieren mit Fragen und Ideen finden Sie unter [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="a14a8-118">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Auswählen des Hilfesymbols (?) in der Aktivitätsleiste zum Anzeigen von QuickInfos" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   <span data-ttu-id="a14a8-120">Wählen Sie das Symbol Hilfe \( `?` \) in der **Aktivitätsleiste aus,** um QuickInfos anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="a14a8-120">Choose the Help \(`?`\) icon in the **Activity Bar** to display tooltips</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="a14a8-121">Anpassen von Tastenkombinationen in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a14a8-121">Customize keyboard shortcuts in Settings</span></span>  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

<span data-ttu-id="a14a8-122">Sie können jetzt die Tastenkombination für jede Aktion in den DevTools anpassen.</span><span class="sxs-lookup"><span data-stu-id="a14a8-122">You may now customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="a14a8-123">Führen Sie die folgenden Aktionen aus, um eine Tastenkombination zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a14a8-123">To edit a keyboard shortcut, complete the following actions.</span></span>  

1.  <span data-ttu-id="a14a8-124">Öffnen Sie die DevTools, und wählen Sie dann **Einstellungen**  >  **Verknüpfungen aus.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-124">Open the DevTools, and then choose **Settings** > **Shortcuts**.</span></span>  
1.  <span data-ttu-id="a14a8-125">Wählen Sie die Aktion aus, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="a14a8-125">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="a14a8-126">Wählen Sie bearbeiten \(</span><span class="sxs-lookup"><span data-stu-id="a14a8-126">Choose the Edit \(</span></span>![Bearbeiten des Tastenkombinationssymbols](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)<span data-ttu-id="a14a8-128">\) symbol.</span><span class="sxs-lookup"><span data-stu-id="a14a8-128">\) icon.</span></span>  
1.  <span data-ttu-id="a14a8-129">Wählen Sie die Schlüssel aus, die Sie an die Aktion binden möchten.</span><span class="sxs-lookup"><span data-stu-id="a14a8-129">Select the keys you want to bind to the action.</span></span>  
1.  <span data-ttu-id="a14a8-130">Aktivieren Sie das Häkchen \(</span><span class="sxs-lookup"><span data-stu-id="a14a8-130">Choose the checkmark \(</span></span>![Symbol für die Tastenkombination "Häkchen".](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="a14a8-132">\) symbol.</span><span class="sxs-lookup"><span data-stu-id="a14a8-132">\) icon.</span></span>  
    
<span data-ttu-id="a14a8-133">Weitere Informationen zum Anpassen und Bearbeiten von Verknüpfungen finden Sie unter Anpassen von Tastenkombinationen [in den Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="a14a8-133">For more information about customizing and editing shortcuts, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="a14a8-134">Um Echtzeitupdates für dieses Feature im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="a14a8-134">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Anpassen von Tastenkombinationen in den DevTools-Einstellungen für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   <span data-ttu-id="a14a8-136">Anpassen von Tastenkombinationen in den [DevTools-Einstellungen][DevtoolsCustomizeIndexSettings] für Verknüpfungen mit einer Verknüpfung im Bearbeitungsmodus</span><span class="sxs-lookup"><span data-stu-id="a14a8-136">Customize keyboard shortcuts in the [DevTools Settings][DevtoolsCustomizeIndexSettings] on Shortcuts with a shortcut in edit mode</span></span>  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a><span data-ttu-id="a14a8-137">Microsoft Edge DevTools für Visual Studio Codeerweiterungsupdate 1.1.4</span><span class="sxs-lookup"><span data-stu-id="a14a8-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span></span>  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

<span data-ttu-id="a14a8-138">Die [Microsoft Edge Developer Tools für Visual Studio Codeerweiterung][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Version 1.1.4 für Microsoft Visual Studio Code zeigt jetzt neben jeder DevTools-Instanz einen Favicon an.</span><span class="sxs-lookup"><span data-stu-id="a14a8-138">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code now displays a favicon next to each of the DevTools instances.</span></span>  <span data-ttu-id="a14a8-139">Konsolennachrichten von Microsoft Edge werden jetzt in der **DevTools-Konsole** unter **Ausgabe** von Microsoft Visual Studio angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-139">Console messages from Microsoft Edge now display in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  <span data-ttu-id="a14a8-140">Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="a14a8-140">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="a14a8-141">Navigieren Sie zum manuellen Aktualisieren auf Version 1.1.4 zu [Manuelles Aktualisieren einer Erweiterung.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="a14a8-141">To manually update to version 1.1.4, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="a14a8-142">Sie können Probleme datein und zur Erweiterung im [vscode-edge-devtools-GitHub-Repository][GithubMicrosoftVscodeEdgeDevtools] beitragen.</span><span class="sxs-lookup"><span data-stu-id="a14a8-142">You may file issues and contribute to the extension on the [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub repo.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a14a8-143">In der folgenden Abbildung werden Nachrichten von einer Beispielwebseite angezeigt, die im **Konsolentool** in Microsoft Edge protokolliert wurde.</span><span class="sxs-lookup"><span data-stu-id="a14a8-143">The following figure displays messages from an example webpage logged in the **Console** tool in Microsoft Edge.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a14a8-144">In der folgenden Abbildung werden die gleichen Nachrichten von der Beispielwebseite angezeigt, die in der **DevTools-Konsole** unter **Ausgabe** von Microsoft Visual Studio ist.</span><span class="sxs-lookup"><span data-stu-id="a14a8-144">The following figure displays the same messages from the example webpage logged in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         <span data-ttu-id="a14a8-146">Anzeigen einer Nachricht in der Konsole in Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a14a8-146">Display a message in Console in Microsoft Edge DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Anzeigen derselben Meldung in der DevTools-Konsole unter Ausgabe von Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         <span data-ttu-id="a14a8-148">Anzeigen derselben Meldung in der DevTools-Konsole unter Ausgabe von Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a14a8-148">Display the same message in the DevTools Console under Output of Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a><span data-ttu-id="a14a8-149">Verbesserte CSS-Flexboxbearbeitung mit visuellem Flexbox-Editor und mehreren Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="a14a8-149">Improved CSS flexbox editing with visual flexbox editor and multiple overlays</span></span>  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

<span data-ttu-id="a14a8-150">DevTools verfügt jetzt über dedizierte CSS-Flexbox-Debuggingtools.</span><span class="sxs-lookup"><span data-stu-id="a14a8-150">DevTools now has dedicated CSS flexbox debugging tools.</span></span>  <span data-ttu-id="a14a8-151">Wenn die `display: flex` Oder `display: inline-flex` -CSS-Formatvorlage auf ein HTML-Element angewendet wird, wird neben diesem Element im Tool Elemente ein `flex` **Symbol** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-151">If the `display: flex` or `display: inline-flex` CSS style is applied to an HTML element, a `flex` icon displays next to that element in the **Elements** tool.</span></span>  <span data-ttu-id="a14a8-152">Zum Anzeigen \(oder Ausblenden\) einer Flexüberlagerung auf der Webseite wählen Sie das `flex` Symbol aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-152">To display \(or hide\) a flex overlay on the webpage, choose the `flex` icon.</span></span>  <span data-ttu-id="a14a8-153">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1166710][CR1166710] und [1175699][CR1175699].</span><span class="sxs-lookup"><span data-stu-id="a14a8-153">To review the history of this feature in the Chromium open-source project, navigate to Issues [1166710][CR1166710] and [1175699][CR1175699].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a14a8-154">Navigieren Sie zum Öffnen des \*\*\*\* **Flexbox-Editors** zum Bereich `display: flex` Formatvorlagen, und wählen Sie das neue Symbol neben dem Format oder `display: inline-flex` aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-154">To open the **Flexbox** editor, navigate to the **Styles** pane and choose the new icon next to the `display: flex` or `display: inline-flex` style.</span></span>  <span data-ttu-id="a14a8-155">Der **Flexbox-Editor** bietet eine schnelle Möglichkeit zum Bearbeiten der flexbox-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a14a8-155">The **Flexbox** editor provides a quick way to edit the flexbox properties.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a14a8-156">Darüber hinaus werden im **Abschnitt Flexbox** im **Layoutbereich** alle flexbox-Elemente auf der Webseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-156">In addition, the **Flexbox** section in the **Layout** pane displays all of the flexbox elements on the webpage.</span></span>  <span data-ttu-id="a14a8-157">Sie können die Überlagerung der einzelnen Elemente umschalten.</span><span class="sxs-lookup"><span data-stu-id="a14a8-157">You may toggle the overlay of each element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="CSS-Flexbox-Debuggingtools" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         <span data-ttu-id="a14a8-159">CSS-Flexbox-Debuggingtools</span><span class="sxs-lookup"><span data-stu-id="a14a8-159">CSS flexbox debugging tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Abschnitt "Flexbox" im Layoutbereich" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         <span data-ttu-id="a14a8-161">**Abschnitt "Flexbox"** im **Layoutbereich**</span><span class="sxs-lookup"><span data-stu-id="a14a8-161">**Flexbox** section in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a><span data-ttu-id="a14a8-162">Verbesserungen bei der Tastaturnavigation für Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="a14a8-162">Keyboard navigation improvements for network requests</span></span>  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

<span data-ttu-id="a14a8-163">Zuvor waren Sie nicht in der Lage, die Kette von Anforderungen mithilfe der Pfeiltasten auf der Tastatur im **Bereich Initiator** zu erweitern oder zu reduzieren, im Gegensatz zum DOM im **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-163">Previously, you were not able to expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane, unlike the DOM in the **Elements** tool.</span></span>  <span data-ttu-id="a14a8-164">Wenn eine Netzwerkanforderung im \*\*\*\* Netzwerktool ausgewählt ist, zeigt der **Bereich Initiator** die Kette der Anforderungen an, die die aktuell ausgewählte Anforderung initiiert haben.</span><span class="sxs-lookup"><span data-stu-id="a14a8-164">When a network request is selected in the **Network** tool, the **Initiator** pane displays the chain of requests that initiated the currently selected request.</span></span>  

<span data-ttu-id="a14a8-165">In Microsoft Edge, Version 90, können Sie die Kette von Anforderungen mithilfe der Pfeiltasten auf der Tastatur im Bereich **Initiator** erweitern oder reduzieren.</span><span class="sxs-lookup"><span data-stu-id="a14a8-165">In Microsoft Edge version 90, you may expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane.</span></span>  <span data-ttu-id="a14a8-166">Die fokussierte Netzwerkanforderung in der Kette wird nun ebenfalls hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a14a8-166">The focused network request in the chain is also now highlighted.</span></span>  <span data-ttu-id="a14a8-167">Weitere Informationen zu Initiatoren im **Netzwerktool** finden Sie unter [Anzeigen von Initiatoren und Abhängigkeiten.][DevtoolsNetworkReferenceDisplayInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="a14a8-167">To learn more about initiators in the **Network** tool, navigate to [Display initiators and dependencies][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span></span>  <span data-ttu-id="a14a8-168">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Probleme [1158276][CR1158276] und [1160637][CR1160637].</span><span class="sxs-lookup"><span data-stu-id="a14a8-168">To review the history of this feature in the Chromium open-source project, navigate to Issues [1158276][CR1158276] and [1160637][CR1160637].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Wählen Sie eine Netzwerkanforderung aus, und wählen Sie den Bereich Initiator aus." lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         <span data-ttu-id="a14a8-170">Wählen Sie eine Netzwerkanforderung aus, und wählen Sie den **Bereich Initiator** aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-170">Choose a Network request and choose the **Initiator** pane</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Erweitern oder Reduzieren der Anforderungsinitiatorkette und Folgen der hervorgehobenen Zeile" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         <span data-ttu-id="a14a8-172">Erweitern oder Reduzieren der Anforderungsinitiatorkette und Folgen der hervorgehobenen Zeile</span><span class="sxs-lookup"><span data-stu-id="a14a8-172">Expand or collapse the request initiator chain and follow the highlighted row</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a><span data-ttu-id="a14a8-173">Filtern in der Konsole ist konsistenter</span><span class="sxs-lookup"><span data-stu-id="a14a8-173">Filtering in the Console is more consistent</span></span>  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

<span data-ttu-id="a14a8-174">Während Sie mit der [Konsolenseite filtern,][DevtoolsConsoleReferenceOpenConsoleSidebar]sind die Filter im Dropdownmenü [Protokollebenen][DevtoolsConsoleReferenceFilterByLogLevel] nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a14a8-174">While you filter with the [Console Sidebar][DevtoolsConsoleReferenceOpenConsoleSidebar], the filters in the [Log Levels][DevtoolsConsoleReferenceFilterByLogLevel] dropdown are not available.</span></span>  <span data-ttu-id="a14a8-175">Zuvor wurde das **Dropdown "Protokollebenen"** hervorgehoben, wenn Sie mit dem Mauszeiger auf sie zeigen, auch wenn ein Filter aus der **Konsolen-Seitenleiste** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="a14a8-175">Previously, the **Log Levels** dropdown highlighted when you hovered on it, even while a filter from the **Console Sidebar** was chosen.</span></span>  <span data-ttu-id="a14a8-176">In Microsoft Edge, Version 90, wird das Dropdown **"Protokollebenen"** nicht mehr hervorgehoben, wenn Sie den Mauszeiger auf sie zeigen, während ein Filter aus der **Konsolenseite ausgewählt** wird.</span><span class="sxs-lookup"><span data-stu-id="a14a8-176">In Microsoft Edge version 90, the **Log Levels** dropdown no longer highlights when you hover on it while a filter from the **Console Sidebar** is chosen.</span></span>  <span data-ttu-id="a14a8-177">Weitere Informationen zum Filtern in der **Konsole finden**Sie unter Filtern [von Nachrichten][DevtoolsConsoleReferenceFilterMessages].</span><span class="sxs-lookup"><span data-stu-id="a14a8-177">To learn more about filtering in the **Console**, navigate to [Filter Messages][DevtoolsConsoleReferenceFilterMessages].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Wenn Sie zuvor die Konsolen-Seitenleiste öffnen und auf Standardebenen zeigen, wurde sie hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         <span data-ttu-id="a14a8-179">Wenn Sie zuvor die Konsolen-Seitenleiste öffnen und auf Standardebenen zeigen, **wurde** sie hervorgehoben. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a14a8-179">Previously, if you open the **Console sidebar** and hover on **Default levels** it was highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="Wenn Sie ab Microsoft Edge 90 die Konsolen-Seitenleiste auswählen und auf Standardebenen zeigen, wird dies nicht hervorgehoben." lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         <span data-ttu-id="a14a8-181">Wenn Sie ab Microsoft Edge 90 die Konsolen-Seitenleiste auswählen und auf Standardebenen **zeigen,** wird dies nicht hervorgehoben. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a14a8-181">Starting in Microsoft Edge 90, if you choose the **Console sidebar** and hover on **Default levels**, it does not highlight</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="a14a8-182">Ankündigungen aus dem Chromium-Projekt</span><span class="sxs-lookup"><span data-stu-id="a14a8-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a><span data-ttu-id="a14a8-183">Die Konsole entweicht jetzt doppelten Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="a14a8-183">The Console now escapes double quote characters</span></span>  

<span data-ttu-id="a14a8-184">Zuvor hat die **Konsole** keine gültigen doppelten Anführungszeichen \( `"` \) in JavaScript-Zeichenfolgen ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="a14a8-184">Previously, the **Console** did not output valid double quote \(`"`\) characters in JavaScript strings.</span></span>  <span data-ttu-id="a14a8-185">Ab Microsoft Edge, Version 90, gibt die **Konsole** JavaScript-Zeichenfolgen unter Verwendung von Escape-Doppelanführungszeichen \( `"` \) aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-185">Starting in Microsoft Edge version 90, the **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters.</span></span>  <span data-ttu-id="a14a8-186">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1178530][CR1178530].</span><span class="sxs-lookup"><span data-stu-id="a14a8-186">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178530][CR1178530].</span></span>  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="Die Konsole gibt JavaScript-Zeichenfolgen mithilfe von Escapezeichen für doppelte Anführungszeichen (&#0022;) aus." lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   <span data-ttu-id="a14a8-188">Die **Konsole gibt** JavaScript-Zeichenfolgen unter Verwendung von Escape-Doppelanführungszeichen \( `"` \) aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-188">The **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters</span></span>  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a><span data-ttu-id="a14a8-189">Emulieren des CSS-Farbskala-Medienfeatures</span><span class="sxs-lookup"><span data-stu-id="a14a8-189">Emulate the CSS color-gamut media feature</span></span>  

<span data-ttu-id="a14a8-190">Die [Farbskala-Medienabfrage][ChromestatusFeature5354410980933632] emuliert den ungefähren Farbbereich, der vom Browser und dem getesteten Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a14a8-190">The [color-gamut][ChromestatusFeature5354410980933632] media query emulates the approximate range of colors supported by the browser and the device you are testing.</span></span>  <span data-ttu-id="a14a8-191">Das Dropdown unter **Emulieren der Farbskala** des CSS-Medienfeatures enthält Farbräume, die DevTools emulieren kann.</span><span class="sxs-lookup"><span data-stu-id="a14a8-191">The dropdown under **Emulate CSS media feature color-gamut** contains color spaces that DevTools may emulate.</span></span>  <span data-ttu-id="a14a8-192">Um beispielsweise eine Medienabfrage auszulösen, wählen Sie im `color-gamut: p3` **Dropdownmenü Farbskala: p3** aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-192">For example, to trigger a `color-gamut: p3` media query, choose **color-gamut: p3** from the dropdown.</span></span>  

<span data-ttu-id="a14a8-193">Führen Sie die folgenden Aktionen aus, um das CSS-Farb gamut-Medienfeature zu emulieren.</span><span class="sxs-lookup"><span data-stu-id="a14a8-193">To emulate the CSS color-gamut media feature, complete the following actions.</span></span>  

1.  <span data-ttu-id="a14a8-194">Öffnen Sie das [Befehlsmenü][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="a14a8-194">Open the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
1.  <span data-ttu-id="a14a8-195">Geben Sie `Rendering` ein.</span><span class="sxs-lookup"><span data-stu-id="a14a8-195">Type `Rendering`.</span></span>  
1.  <span data-ttu-id="a14a8-196">Führen Sie den **Befehl Rendering anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-196">Run the **Show Rendering** command.</span></span>  
1.  <span data-ttu-id="a14a8-197">Navigieren Sie **zu Css-Medienfeature-Farbskala emulieren,** und wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="a14a8-197">Navigate to **Emulate CSS media feature color-gamut** and choose an option.</span></span>  

<span data-ttu-id="a14a8-198">Um mehr über das Feature zu `color-gamut` erfahren, navigieren Sie zu [Farbanzeigequalität: das Feature "Farbskala".][CsswgDraftsMediaqueries4ColorGamut]</span><span class="sxs-lookup"><span data-stu-id="a14a8-198">To learn more about the `color-gamut` feature, navigate to [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span></span>  <span data-ttu-id="a14a8-199">Navigieren Sie zu Issue [1073887,][CR1073887]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a14a8-199">To review the history of this feature in the Chromium open-source project, navigate to Issue [1073887][CR1073887].</span></span>  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emulieren des CSS-Farbskala-Medienfeatures" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   <span data-ttu-id="a14a8-201">Emulieren des CSS-Farbskala-Medienfeatures</span><span class="sxs-lookup"><span data-stu-id="a14a8-201">Emulate the CSS color-gamut media feature</span></span>  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a><span data-ttu-id="a14a8-202">Verbesserte Progressive Web Apps-Tools</span><span class="sxs-lookup"><span data-stu-id="a14a8-202">Improved Progressive Web Apps tooling</span></span>  

#### <a name="pwa-installability-warning-in-the-console"></a><span data-ttu-id="a14a8-203">Warnung zur Installation von PWA in der Konsole</span><span class="sxs-lookup"><span data-stu-id="a14a8-203">PWA installability warning in the Console</span></span>  

<span data-ttu-id="a14a8-204">Die **Konsole** zeigt nun eine ausführlichere Warnung zur Installation von [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] mit einem Link zur Verbesserung der [Progressive Web App-Offlineunterstützungserkennung an.][ChromeDeveloperBlogImprovedPwaOfflineDetection]</span><span class="sxs-lookup"><span data-stu-id="a14a8-204">The **Console** now displays a more detailed [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] installability warning message with a link to [Improving Progressive Web App offline support detection][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span></span>  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Warnung zur Installation von PWA im Konsolentool" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   <span data-ttu-id="a14a8-206">Warnung zur Installation von PWA im **Konsolentool**</span><span class="sxs-lookup"><span data-stu-id="a14a8-206">PWA installability warning in **Console** tool</span></span>  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a><span data-ttu-id="a14a8-207">Warnung zur Länge der PWA-Beschreibung im Manifestbereich</span><span class="sxs-lookup"><span data-stu-id="a14a8-207">PWA description length warning in the Manifest pane</span></span>

<span data-ttu-id="a14a8-208">Im **Manifestbereich** wird nun eine Warnmeldung angezeigt, wenn die Manifestbeschreibung 324 Zeichen überschreitet.</span><span class="sxs-lookup"><span data-stu-id="a14a8-208">The **Manifest** pane now displays a warning message if the manifest description exceeds 324 characters.</span></span>  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Warnung zum Kürzen der PWA-Beschreibung" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   <span data-ttu-id="a14a8-210">Warnung zum Kürzen der PWA-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a14a8-210">PWA description truncate warning</span></span>  
:::image-end:::  

<span data-ttu-id="a14a8-211">Navigieren Sie zu Probleme [965802,][CR965802] [1146450][CR1146450]und [1169689,][CR1169689]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a14a8-211">To review the history of this feature in the Chromium open-source project, navigate to Issues [965802][CR965802], [1146450][CR1146450], and [1169689][CR1169689].</span></span>  

### <a name="new-remote-address-space-column-in-the-network-tool"></a><span data-ttu-id="a14a8-212">Neue Spalte "Remote address space" im Netzwerktool</span><span class="sxs-lookup"><span data-stu-id="a14a8-212">New Remote Address Space column in the Network tool</span></span>  

<!-- does not work in canary 90.0.813.0 -->  
<span data-ttu-id="a14a8-213">In der neuen **Spalte Remoteadressenraum** wird der Netzwerk-IP-Adressraum jeder Netzwerkressource angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-213">The new **Remote Address Space** column displays the network IP address space of each network resource.</span></span>  <span data-ttu-id="a14a8-214">Führen Sie die folgenden Aktionen aus, um die neue Spalte Remoteadressenraum anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="a14a8-214">To display the new Remote Address Space column, complete the following actions.</span></span>  

1.  <span data-ttu-id="a14a8-215">Navigieren Sie zum **Netzwerktool.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-215">Navigate to the **Network** tool.</span></span>  
1.  <span data-ttu-id="a14a8-216">Zeigen Sie in der Tabelle Anforderungen auf die Kopfzeile, und öffnen Sie das Kontextmenü \(klicken Sie mit der rechten Maustaste\).</span><span class="sxs-lookup"><span data-stu-id="a14a8-216">In the Requests table, hover on the header row, and open the contextual menu \(right-click\).</span></span>  <span data-ttu-id="a14a8-217">Informationen zum Hinzufügen oder Entfernen von Spalten aus der Tabelle Anforderungen finden Sie unter [Hinzufügen oder Entfernen von Spalten.][DevtoolsNetworkReferenceAddRemoveColumns]</span><span class="sxs-lookup"><span data-stu-id="a14a8-217">To learn how to add or remove columns from the Requests table, navigate to [Add or remove columns][DevtoolsNetworkReferenceAddRemoveColumns].</span></span>  
1.  <span data-ttu-id="a14a8-218">Wählen **Sie Remoteadressenbereich aus.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-218">Choose **Remote Address Space**.</span></span>  
    
<span data-ttu-id="a14a8-219">In der Tabelle Anforderungen wird nun eine neue Spalte mit der Kopfzeile **"Remote address Space" angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-219">The Requests table now displays a new column with the header named **Remote Address Space**.</span></span>  <span data-ttu-id="a14a8-220">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1128885][CR1128885].</span><span class="sxs-lookup"><span data-stu-id="a14a8-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1128885][CR1128885].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="Wählen Sie im Kontextmenü Remoteadressenbereich aus." lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         <span data-ttu-id="a14a8-222">Wählen Sie im Kontextmenü den **Remoteadressenbereich aus.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-222">In the contextual menu, choose the **Remote Address Space**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="In der Tabelle Anforderungen wird nun die Spalte Remoteadressenbereich angezeigt." lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         <span data-ttu-id="a14a8-224">In der Tabelle Anforderungen wird nun die **Spalte Remoteadressenbereich** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-224">The Requests table now displays the **Remote Address Space** column</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a><span data-ttu-id="a14a8-225">Anzeigen zulässiger und nicht zulässiger Features in der Frame-Detailansicht</span><span class="sxs-lookup"><span data-stu-id="a14a8-225">Display allowed and disallowed features in the Frame details view</span></span>  

<span data-ttu-id="a14a8-226">Die Frame-Detailansicht zeigt nun eine Liste der zulässigen und nicht zulässigen Browserfeatures an, die durch die [Berechtigungsrichtlinie gesteuert werden.][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]</span><span class="sxs-lookup"><span data-stu-id="a14a8-226">The Frame details view now displays a list of allowed and disallowed browser features controlled by the [Permissions Policy][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span></span>  <span data-ttu-id="a14a8-227">Die Berechtigungsrichtlinie ist eine Webplattform-API, mit der eine Webseite die Verwendung von Browserfeatures in einem einzelnen Frame oder in iframes ermöglicht wird, die sie einbettet.</span><span class="sxs-lookup"><span data-stu-id="a14a8-227">Permissions Policy is a web platform API that allows \(or blocks\) a webpage the use of browser features in an individual frame or in iframes that it embeds.</span></span>  <span data-ttu-id="a14a8-228">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="a14a8-228">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Zugelassene und nicht zulässige Features basierend auf der Berechtigungsrichtlinie" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   <span data-ttu-id="a14a8-230">Zugelassene und nicht zulässige Features basierend auf der Berechtigungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="a14a8-230">Allowed and disallowed features based on the Permission Policy</span></span>  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a><span data-ttu-id="a14a8-231">Neue Spalte SameParty im Bereich Cookies</span><span class="sxs-lookup"><span data-stu-id="a14a8-231">New SameParty column in the Cookies pane</span></span>  

<span data-ttu-id="a14a8-232">Im **Bereich Cookies** im **Anwendungstool** wird nun das `SameParty` Attribut für jedes Cookie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-232">The **Cookies** pane in the **Application** tool now displays the `SameParty` attribute for each cookie.</span></span>  <span data-ttu-id="a14a8-233">Das Attribut ist ein neues boolesches Attribut, das angibt, ob ein Cookie in Anforderungen an Ursprünge derselben `SameParty` [First-Party-Sets enthalten ist.][GithubPrivacycgFirstPartySets]</span><span class="sxs-lookup"><span data-stu-id="a14a8-233">The `SameParty` attribute is a new boolean attribute to indicate whether a cookie is included in requests to origins of the same [First-Party Sets][GithubPrivacycgFirstPartySets].</span></span>  <span data-ttu-id="a14a8-234">Navigieren Sie zu Issue [1161427,][CR1161427]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a14a8-234">To review the history of this feature in the Chromium open-source project, navigate to Issue [1161427][CR1161427].</span></span>  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Spalte SameParty im Bereich Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   <span data-ttu-id="a14a8-236">**Spalte SameParty** im **Bereich Cookies**</span><span class="sxs-lookup"><span data-stu-id="a14a8-236">**SameParty** column in the **Cookies** pane</span></span>  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a><span data-ttu-id="a14a8-237">Die fn.displayName-Eigenschaft im Konsolentool ist nun veraltet.</span><span class="sxs-lookup"><span data-stu-id="a14a8-237">fn.displayName property in the Console tool is now deprecated</span></span>  

<span data-ttu-id="a14a8-238">Zuvor konnten Sie mit der Eigenschaft Debugnamen für Funktionen steuern, die in und `fn.displayName` `error.stack` in DevTools-Stapelverfolgungen angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="a14a8-238">Previously, the `fn.displayName` property allowed you to control debug names for functions to display in `error.stack` and in DevTools stack traces.</span></span>  <span data-ttu-id="a14a8-239">Ab Microsoft Edge, Version 90, ist die Eigenschaft veraltet `fn.displayName` und wird durch die Eigenschaft `fn.name` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-239">Starting in Microsoft Edge version 90, the `fn.displayName` property is now deprecated, and replaced by the `fn.name` property.</span></span>  <span data-ttu-id="a14a8-240">Verwenden Sie die `Object.defineProperty` Standardmethode, um die Eigenschaft `fn.name` zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a14a8-240">Use the standard `Object.defineProperty` method to define the `fn.name` property.</span></span>  <span data-ttu-id="a14a8-241">Um mehr über zu `fn.name` erfahren, navigieren Sie [zu Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span><span class="sxs-lookup"><span data-stu-id="a14a8-241">To learn more about `fn.name`, navigate to [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span></span>  <span data-ttu-id="a14a8-242">Navigieren Sie zu Issue [1177685,][CR1177685]um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a14a8-242">To review the history of this feature in the Chromium open-source project, navigate to Issue [1177685][CR1177685].</span></span>  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Ein Beispiel für die fn.name-Eigenschaft zum Steuern von Debugnamen für Funktionen" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   <span data-ttu-id="a14a8-244">Ein Beispiel für die `fn.name` Eigenschaft zum Steuern von Debugnamen für Funktionen</span><span class="sxs-lookup"><span data-stu-id="a14a8-244">An example of the `fn.name` property to control debug names for functions</span></span>  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a><span data-ttu-id="a14a8-245">Vollständige Barrierefreiheitsstrukturansicht im Elementtool</span><span class="sxs-lookup"><span data-stu-id="a14a8-245">Full accessibility tree view in the Elements tool</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="a14a8-246">Dieses Experiment bietet eine **vollständige Barrierefreiheitsstrukturansicht** im **Elementtool.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-246">This experiment provides a **full accessibility tree view** in the **Elements** tool.</span></span>  <span data-ttu-id="a14a8-247">Der [Bereich Barrierefreiheit][DevtoolsAccessibilityReferenceTheAccessibilityPane] bietet eine teilweise Barrierefreiheitsstrukturansicht, in der die direkte Vorgängerkette vom Stammknoten zum überprüften Knoten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a14a8-247">The [Accessibility][DevtoolsAccessibilityReferenceTheAccessibilityPane] pane provides a partial accessibility tree view, that displays the direct ancestor chain from the root node to the inspected node.</span></span>  
<span data-ttu-id="a14a8-248">Nachdem Sie dieses Experiment aktivieren und die DevTools neu laden, wählen Sie eine der folgenden Schaltflächen aus, um die Anzeige im Elementtool für alle Elemente auf der Webseite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a14a8-248">After you turn on this experiment and reload the DevTools, choose one of the following buttons to switch the display in the Elements tool for all elements on the webpage.</span></span>  

*   <span data-ttu-id="a14a8-249">Wählen Sie zum Anzeigen der vollständigen Barrierefreiheitsstrukturansicht die **Ansicht Barrierefreiheitsstruktur wechseln aus.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-249">To display the full accessibility tree view , choose the **Switch to Accessibility Tree view**.</span></span>  
*   <span data-ttu-id="a14a8-250">Wählen Sie zum Anzeigen der DOM-Strukturansicht die **Ansicht Wechseln zu DOM-Struktur aus.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-250">To display the DOM tree view, choose the **Switch to DOM Tree view**.</span></span>  
    
<span data-ttu-id="a14a8-251">Um das Experiment zu aktivieren, navigieren Sie zu Experimentelle Features [aktivieren,][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] und aktivieren Sie das Kontrollkästchen neben Vollständige Barrierefreiheitsstrukturansicht aktivieren **im Bereich Elemente.**</span><span class="sxs-lookup"><span data-stu-id="a14a8-251">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkbox next to **Enable full accessibility tree view in Elements pane**.</span></span>  <span data-ttu-id="a14a8-252">Um den Verlauf dieses Features im Open-Source-Projekt Chromium zu überprüfen, navigieren Sie zu Issue [887173][CR887173].</span><span class="sxs-lookup"><span data-stu-id="a14a8-252">To review the history of this feature in the Chromium open-source project, navigate to Issue [887173][CR887173].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Anzeigen der DOM-Strukturansicht" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         <span data-ttu-id="a14a8-254">Anzeigen der **DOM-Ansicht**</span><span class="sxs-lookup"><span data-stu-id="a14a8-254">Display the **DOM view**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Anzeigen der vollständigen Barrierefreiheitsstrukturansicht" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         <span data-ttu-id="a14a8-256">Anzeigen der **Vollständigen Barrierefreiheitsstrukturansicht**</span><span class="sxs-lookup"><span data-stu-id="a14a8-256">Display the **Full Accessibility Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="a14a8-257">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="a14a8-257">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="a14a8-258">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="a14a8-258">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="a14a8-259">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="a14a8-259">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="a14a8-260">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="a14a8-260">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "Der Bereich Barrierefreiheit – Barrierefreiheitsreferenz | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit der Microsoft Edge DevTools-Befehlsmenüleiste | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtern nach Protokollebene – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filtern von Nachrichten – Konsolenreferenz | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Öffnen Sie die Konsolenseite – Konsolenreferenz | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Einstellungen – Anpassen von Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Anpassen von Tastenkombinationen in der Microsoft Edge DevTools-| Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Aktivieren sie + Schaltflächenmenüs, um weitere Tools zu öffnen – Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Hinzufügen oder Entfernen von Spalten – Netzwerkanalysereferenz | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Anzeigen von Initiatoren und Abhängigkeiten – Netzwerkanalysereferenz | Microsoft Docs"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Übersicht über progressive Web Apps unter Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge Preview Channels"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterung Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Verbessern der Erkennung von Progressive Web App-Offlineunterstützung | Chrome Developers"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "Farbskala-Medienabfragen | Status der Chrome-Plattform"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Chromium-Fehler"  
[CR174309]: https://crbug.com/174309 "Problem 174309: DevTools: Zulassen der Anpassung von Tastenkombinationen/Tastenbindungen | Chromium-Fehler"  
[CR887173]: https://crbug.com/887173 "Issue 887173: DevTools: Full Accessibility Tree Inspection | Chromium-Fehler"  
[CR965802]: https://crbug.com/965802 "Problem 965802: Implementieren einer genaueren Erkennung von Offlinefunktionen | Chromium-Fehler"  
[CR1073887]: https://crbug.com/1073887 "Issue 1073887: DevTools: @media (color-gamut: ...) colorspace emulation | Chromium-Fehler"  
[CR1128885]: https://crbug.com/1128885 "Problem 1128885: DevTools-Unterstützung für CORS-RFC1918 | Chromium-Fehler"  
[CR1146450]: https://crbug.com/1146450 "Issue 1146450: [Android] Implement bottom sheet installs | Chromium-Fehler"  
[CR1158276]: https://crbug.com/1158276 "Problem 1158276: Bereich "Initiatorkette anfordern" kann nicht mithilfe von Pfeiltasten im Abschnitt "Netzwerk" von DevTools erweitert/| Chromium-Fehler"  
[CR1158827]: https://crbug.com/1158827 "Issue 1158827: [Permissions Policy] Implement devtool support for permissions policy | Chromium-Fehler"  
[CR1160637]: https://crbug.com/1160637 "Problem 1160637: Der Fokus auf "Anforderungsinitiatorkette" wird im Abschnitt "Netzwerk" des Fensters "Dev Tools" als unvollständig | Chromium-Bugs"  
[CR1161427]: https://crbug.com/1161427 "Problem 1161427: &#9730; Support SameParty cookie attribute debugging in DevTools | Chromium-Fehler"  
[CR1166710]: https://crbug.com/1166710 "Problem 1166710: Aktivieren des Flexboxtool-Experiments standardmäßig | Chromium-Fehler"  
[CR1169689]: https://crbug.com/1169689 "Problem 1169689: Das untere Blatt für die PWA-Installation sollte keine Kategorien | Chromium-Fehler"  
[CR1175699]: https://crbug.com/1175699 "Problem 1175699: Flexbox-Editor | Chromium-Fehler"  
[CR1177685]: https://crbug.com/1177685 "Problem 1177685: Entfernen von nicht standardmäßigen fn.displayName-| Chromium-Fehler"  
[CR1178530]: https://crbug.com/1178530 "Problem 1178530: Die Konsole entweicht keine Doppelquote beim Drucken von Zeichenfolgen | Chromium-Fehler"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Farbanzeigequalität: Das Feature "Farbskala" | Entwürfe des CSS-Arbeitsgruppen-Editors"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Fokusmodus-UI – MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "First-Party Sets | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Berechtigungsrichtlinienerklärer | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> <span data-ttu-id="a14a8-300">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a14a8-300">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a14a8-301">Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/updates/2021/02/devtools/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.</span><span class="sxs-lookup"><span data-stu-id="a14a8-301">The original page is found [here](https://developers.google.com/web/updates/2021/02/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a14a8-303">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a14a8-303">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
