---
description: Eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge DevTools.
title: Barrierefreiheitsreferenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: e3fed1c4e53c69b7a6837f71c270c0bf2f65b7e2
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398336"
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

# <a name="accessibility-reference"></a>Barrierefreiheitsreferenz  

Diese Seite ist eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge DevTools.  Es richtet sich an Webentwickler, die:  

*   Verfügen Sie über grundlegende Kenntnisse von DevTools, z. B. wie Sie es öffnen.  
*   Sind mit [Barrierefreiheitsgrundsätzen und bewährten Methoden vertraut.][MDNAccessibility]  
    
Dieser Verweis soll Ihnen dabei helfen, alle in DevTools verfügbaren Tools zu entdecken, mit deren Hilfe Sie die Barrierefreiheit einer Seite untersuchen können.  

Wenn Sie Hilfe zum Navigieren in DevTools mit einer Hilfstechnologie wie einer Bildschirmlesehilfe suchen, navigieren Sie zu [Navigieren in Microsoft Edge DevTools with Assistive Technology][DevtoolsAccessibilityNavigation].  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a>Übersicht über Barrierefreiheitsfeatures in Microsoft Edge DevTools  

In diesem Abschnitt wird erläutert, wie DevTools in Ihr allgemeines Toolkit für Barrierefreiheit passt.  

Wenn Sie bestimmen, ob auf eine Seite zugegriffen werden kann, müssen Sie zwei allgemeine Fragen berücksichtigen:  

1.  Sind Sie in der Lage, mit einer Tastatur oder einer [Bildschirmleseausgabe auf der Seite zu navigieren?][MDNScreenReader]  
1.  Sind die Elemente der Seite für Bildschirmlesegeräte ordnungsgemäß gekennzeichnet?  
    
Im Allgemeinen sollten DevTools Ihnen bei der Behebung von Fehlern im Zusammenhang mit fragen #2 helfen, da diese Fehler einfach automatisiert zu erkennen sind.  Fragen #1 ist genauso wichtig, aber leider hilft Ihnen DevTools dort nicht.  Die einzige Möglichkeit, Fehler im Zusammenhang mit fragen #1 zu finden, besteht in der Verwendung einer Seite mit einer Tastatur oder einer Bildschirmleseausgabe selbst.  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a>Überwachen der Barrierefreiheit einer Seite  

> [!NOTE]
> Das **Tool Überwachungen** stellt Links zu Inhalten zur Verfügung, die auf Websites von Drittanbietern gehostet werden.  Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und alle möglicherweise gesammelten Daten.  

Verwenden Sie im Allgemeinen den Bereich Überwachungen, um zu ermitteln, ob:  

*   Eine Seite ist für Bildschirmlesegeräte ordnungsgemäß gekennzeichnet.  
*   Die Textelemente auf einer Seite verfügen über ausreichende Kontrastverhältnisse.  Navigieren Sie [zu Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl.](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker)  

So überwachen Sie eine Seite:  

1.  Navigieren Sie zu der URL, die Sie überwachen möchten.  
1.  Wählen Sie in DevTools das **Tool Überwachungen** aus.  DevTools zeigt Ihnen verschiedene Konfigurationsoptionen.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Konfigurieren von Überwachungen" lightbox="../media/accessibility-audits-pane.msft.png":::
       Konfigurieren von Überwachungen  
    :::image-end:::  
    
    > [!NOTE]
    > Die Screenshots in diesem Abschnitt wurden mit Version 79 von Microsoft Edge erstellt.  Sie können überprüfen, welche Version Sie unter `edge://version` ausführen.  Die **Benutzeroberfläche** des Überwachungsinstruments sieht in früheren Versionen von Microsoft Edge anders aus, der allgemeine Workflow ist jedoch identisch.  
    
1.  Wählen **Sie für**Gerät Mobile **aus,** wenn Sie ein mobiles Gerät simulieren möchten.  Mit dieser Option wird die Zeichenfolge des Benutzer-Agents geändert und die Größe des Viewports geändert.  Wenn die mobile Version der Seite anders als die Desktopversion angezeigt wird, kann diese Option erhebliche Auswirkungen auf die Ergebnisse Ihrer Überwachung haben.  
1.  Stellen Sie **im Abschnitt Überwachungen** sicher, dass **Barrierefreiheit** aktiviert ist.  Deaktivieren Sie die anderen Kategorien, wenn Sie sie aus Ihrem Bericht ausschließen möchten.  Lassen Sie sie aktiviert, wenn Sie andere Möglichkeiten zur Verbesserung der Qualität Ihrer Seite finden möchten.  
1.  Im **Abschnitt Einschränkung** können Sie das Netzwerk und die CPU drosseln, was bei der Analyse der Lastleistung hilfreich ist.  Diese Option sollte für Ihre Barrierefreiheitsnote irrelevant sein, sodass Sie die von Ihnen bevorzugten Optionen verwenden können.  
1.  Mit **dem Kontrollkästchen Speicher** löschen können Sie den speicherplatz vor dem Laden der Seite löschen oder den Speicher zwischen Seitenlasten beibehalten.  Diese Option ist wahrscheinlich auch für die Barrierefreiheitsnote irrelevant, sodass Sie die von Ihnen bevorzugten Optionen verwenden können.  
1.  Wählen **Sie Überwachungen ausführen aus.** Nach 10 bis 30 Sekunden stellt DevTools einen Bericht zur Verfügung.  Ihr Bericht enthält verschiedene Tipps, wie Sie die Barrierefreiheit der Seite verbessern können.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Ein Bericht" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Ein Bericht  
    :::image-end:::  
    
1.  Wählen Sie eine Überwachung aus, um mehr darüber zu erfahren.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Weitere Informationen zu einer Überwachung" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Weitere Informationen zu einer Überwachung  
    :::image-end:::  
    
1.  Wählen **Sie Weitere Informationen aus,** um die Dokumentation dieser Überwachung anzeigen zu können.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Anzeigen der Dokumentation einer Überwachung" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Anzeigen der Dokumentation einer Überwachung  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a>Siehe auch: aXe-Erweiterung  

Möglicherweise verwenden Sie lieber die [aXe-Erweiterung][ChromeWebStoreAxe] als das **Überwachungstool.**  
Die Erweiterung aXe stellt im Allgemeinen dieselben Informationen zur Verfügung, da es sich um das zugrunde liegende Modul handelt, das die Überwachungen unterstützt.  Die aXe-Erweiterung hat eine andere Benutzeroberfläche und beschreibt Prüfungen geringfügig anders.  
Ein Vorteil der Erweiterung aXe gegenüber dem **Tool "Überwachungen"** besteht in der Möglichkeit, fehlerhafte Knoten zu prüfen und zu markieren.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Die Erweiterung aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   Die Erweiterung aXe  
:::image-end:::  

## <a name="the-accessibility-panel"></a>Der Bereich Barrierefreiheit  

Im **Bereich** Barrierefreiheit werden die Barrierefreiheitsstruktur, ARIA-Attribute und berechneten Barrierefreiheitseigenschaften von DOM-Knoten angezeigt.  

So öffnen Sie den **Bereich Barrierefreiheit:**  

1.  Wählen Sie das **Elementtool** aus.  
1.  Wählen Sie **in der DOM-Struktur**das Element aus, das Sie überprüfen möchten.  
1.  Wählen Sie den **Bereich Barrierefreiheit** aus.  Dieser Bereich wird möglicherweise hinter der Schaltfläche **Weitere Registerkarten** ![ \( Weitere ][ImageMoreTabsIcon] Registerkarten \) ausgeblendet.  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Überprüfen des h1-Elements der DevTools-Homepage im Bereich Barrierefreiheit" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Überprüfen des `h1` Elements der DevTools-Homepage im **Bereich Barrierefreiheit**  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Anzeigen der Position eines Elements in der Barrierefreiheitsstruktur  

Die [Barrierefreiheitsstruktur][MDNAccessibilityTree] ist eine Teilmenge der DOM-Struktur.  Es enthält nur Elemente aus der DOM-Struktur, die für die Anzeige des Inhalts einer Seite in einer Bildschirmleseausgabe relevant und nützlich sind.  

Überprüfen Sie die Position eines Elements in der Barrierefreiheitsstruktur im [Bereich Barrierefreiheit.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Abschnitt "Barrierefreiheitsstruktur"" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Abschnitt **"Barrierefreiheitsstruktur"**  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a>Anzeigen der ARIA-Attribute eines Elements  

ARIA-Attribute stellen sicher, dass die Bildschirmlesegeräte über alle Informationen verfügen, die sie benötigen, um den Inhalt einer Seite ordnungsgemäß darstellen zu können.  

Zeigen Sie die ARIA-Attribute eines Elements im Bereich [Barrierefreiheit](#the-accessibility-panel) an.  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Der Abschnitt "ARIA Attributes"" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Der **Abschnitt "ARIA Attributes"**  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a>Anzeigen der berechneten Barrierefreiheitseigenschaften eines Elements  

> [!NOTE]
> Wenn Sie nach berechneten CSS-Eigenschaften suchen, navigieren Sie zu [Berechneter][DevtoolsCssReferenceViewActuallyAppliedElements] Bereich.  

Einige Barrierefreiheitseigenschaften werden vom Browser dynamisch berechnet.  Diese Eigenschaften werden im Abschnitt **Berechnete Eigenschaften** im **Bereich** Barrierefreiheit angezeigt.  

Zeigen Sie die berechneten Barrierefreiheitseigenschaften eines Elements im Bereich [Barrierefreiheit](#the-accessibility-panel) an.  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Der Abschnitt Berechnete Eigenschaften des Barrierefreiheitsbereichs" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Der **Abschnitt Berechnete Eigenschaften** des **Barrierefreiheitsbereichs**  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a>Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl  

Einige Personen mit niedriger Sehkraft sehen Bereiche nicht als sehr hell oder sehr dunkel.  Alles wird in der Regel ungefähr mit der gleichen Helligkeit angezeigt, was es schwierig macht, Gliederungen und Kanten zu unterscheiden.  

Das Kontrastverhältnis misst den Helligkeitsunterschied zwischen dem Vordergrund und dem Hintergrund des Texts.  Wenn Ihr Text ein niedriges Kontrastverhältnis hat, können diese Benutzer mit niedriger Sehkraft Ihre Website im wahrsten Sinne des Wortes als leeren Bildschirm sehen.  

Mit der Farbauswahl können Sie überprüfen, ob Ihr Text die empfohlenen Kontrastverhältnisstufen erfüllt:  

1.  Wählen Sie das **Elementtool** aus.  
1.  Wählen Sie **in der DOM-Struktur**das Textelement aus, das Sie überprüfen möchten.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Überprüfen eines Absatzes in der DOM-Struktur" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Überprüfen eines Absatzes in der **DOM-Struktur**  
    :::image-end:::  
    
1.  Wählen Sie **im Bereich** Formatvorlagen das Farbfeld neben dem Wert des `color` Elements aus.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Die Color-Eigenschaft des Elements" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       Die `color` Eigenschaft des Elements  
    :::image-end:::  
    
1.  Überprüfen Sie **den Abschnitt Kontrastverhältnis** der Farbauswahl.  Ein Häkchen bedeutet, dass das Element die [Mindestempfehlung erfüllt.][W3CContrastMinimum]  Zwei Häkchen bedeutet, dass es die erweiterte [Empfehlung erfüllt.][W3CContrastEnhanced]  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="Der Abschnitt Kontrastverhältnis der Farbauswahl zeigt 2 Häkchen und einen Wert von 13,97 an." lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       Der **Abschnitt Kontrastverhältnis** der Farbauswahl zeigt 2 Häkchen und einen Wert von `13.97`  
    :::image-end:::  
    
1.  Weitere Informationen finden Sie im Abschnitt **Kontrastverhältnis.**  Oben in der Farbauswahl wird in der visuellen Auswahl eine Linie angezeigt.  Wenn die aktuelle Farbe Empfehlungen erfüllt, entspricht auch alles auf derselben Seite der Linie den Empfehlungen.  Wenn die aktuelle Farbe den Empfehlungen nicht gerecht wird, erfüllt auch nichts auf derselben Seite empfehlungen.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Die Kontrastverhältnislinie in der visuellen Auswahl" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Die **Kontrastverhältnislinie** in der visuellen Auswahl  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navigieren Sie zu Microsoft Edge DevTools mit Hilfstechnologie| Microsoft Docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Nur das CSS anzeigen, das tatsächlich auf ein Element angewendet wird – CSS Reference | Microsoft Docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Web Accessibility Testing - Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Barrierefreiheitsstruktur (Accessibility Tree, AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Barrierefreiheit | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Bildschirmleseprogramm | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contrast (Enhanced) Level AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Kontrast (Minimum) Level AA | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
