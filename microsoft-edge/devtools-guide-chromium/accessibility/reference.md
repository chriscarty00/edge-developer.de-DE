---
title: Barrierefreiheits Referenz
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 7417388023612b6e1ca651deba28e099e3c8e3d8
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581573"
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





# Barrierefreiheits Referenz   



Diese Seite ist eine umfassende Referenz zu Barrierefreiheitsfeatures in Microsoft Edge devtools.  Sie ist für Web-Entwickler gedacht, die:  

*   Grundlegende Kenntnisse in devtools, beispielsweise zum Öffnen.  
*   Sind mit [Grundsätzen der Barrierefreiheit und bewährten Methoden][MDNAccessibility]vertraut.  

Dieser Bezug soll Ihnen helfen, alle in devtools verfügbaren Tools zu finden, die Ihnen bei der Untersuchung der Barrierefreiheit einer Seite helfen.  

Weitere Informationen finden Sie unter [Navigieren in Microsoft Edge devtools mit Hilfstechnologien][DevtoolsAccessibilityNavigation] , wenn Sie Hilfe beim Navigieren in devtools mit einer Hilfstechnologie wie einer Bildschirmsprachausgabe suchen.  

## Übersicht über Barrierefreiheitsfeatures in Microsoft Edge devtools   

In diesem Abschnitt wird erläutert, wie sich devtools in Ihr gesamtes Barrierefreiheits-Toolkit einfügt.  

Wenn Sie feststellen möchten, ob eine Seite barrierefrei ist, müssen Sie zwei allgemeine Fragen berücksichtigen:  

1.  Können Sie auf der Seite mit einer Tastatur oder einer [Sprachausgabe][MDNScreenReader]navigieren?  
1.  Sind die Elemente der Seite für Bildschirmsprachausgaben richtig markiert?  

Im Allgemeinen sollte devtools Sie bei der Behebung von Fehlern in Bezug auf Fragen #2 unterstützen, da diese Fehler in automatisierter Weise leicht zu erkennen sind.  Frage #1 ist genauso wichtig, aber leider hilft Ihnen devtools nicht.  Die einzige Möglichkeit, Fehler im Zusammenhang mit der Frage #1 zu finden, besteht darin, eine Seite mit einer Tastatur oder einer Bildschirmsprachausgabe selbst zu verwenden.  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## Überwachen der Barrierefreiheit einer Seite   

> [!NOTE]
> Das **Überwachungs** Panel enthält Links zu Inhalten, die auf Websites von Drittanbietern gehostet werden.  Microsoft ist nicht verantwortlich und hat keine Kontrolle über den Inhalt dieser Websites und alle Daten, die möglicherweise erfasst werden.  

Im Allgemeinen können Sie mithilfe des Überwachungs Panels feststellen, ob:  

*   Eine Seite ist für Bildschirmsprachausgaben richtig markiert.  
*   Die Textelemente auf einer Seite verfügen über ein ausreichendes Kontrastverhältnis. Siehe auch [Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).  

So überprüfen Sie eine Seite:  

1.  Wechseln Sie zu der URL, die Sie überwachen möchten.  
1.  Klicken Sie in devtools auf die Registerkarte **Audits** .  DevTools zeigt Ihnen verschiedene Konfigurationsoptionen.  
    
    > ##### Abbildung1  
    > Konfigurieren von Audits  
    > ![Konfigurieren von Audits][ImageConfiguringAudits]  
    
    > [!NOTE]
    > Die Screenshots in diesem Abschnitt wurden mit Version 79 von Microsoft Edge übernommen.  Sie können überprüfen, welche Version Sie Ausführen `edge://version` .  Die Benutzeroberfläche des **Überwachungs** Panels sieht in früheren Versionen von Microsoft Edge anders aus, der allgemeine Workflow ist jedoch identisch.  
    
1.  Wählen Sie für **Gerät**den Eintrag **Handy** aus, wenn Sie ein mobiles Gerät simulieren möchten.  Mit dieser Option wird die Zeichenfolge des Benutzer-Agents geändert und die Größe des Viewports geändert.  Wenn die Mobile Version der Seite anders als die Desktop Version angezeigt wird, kann sich diese Option erheblich auf die Ergebnisse ihrer Überwachung auswirken.  
1.  Stellen Sie im Abschnitt **Audits** sicher, dass die **Barrierefreiheit** aktiviert ist.  Deaktivieren Sie die anderen Kategorien, wenn Sie Sie aus dem Bericht ausschließen möchten.  Lassen Sie sie aktiviert, wenn Sie andere Möglichkeiten entdecken möchten, um die Qualität Ihrer Seite zu verbessern.  
1.  Im Abschnitt **Drosselung** können Sie das Netzwerk und die CPU Drosseln, was bei der Analyse der Auslastungs Leistung hilfreich ist.  Diese Option sollte für den Zugriff auf die Barrierefreiheit irrelevant sein, daher können Sie das, was Sie bevorzugen, verwenden.  
1.  Mit dem Kontrollkästchen **Speicher löschen** können Sie den gesamten Speicher löschen, bevor Sie die Seite laden, oder den Speicherplatz zwischen den Seitenlasten bewahren.  Diese Option ist möglicherweise auch für das Ergebnis der Barrierefreiheit irrelevant, sodass Sie die von Ihnen bevorzugten Optionen verwenden können.  
1.  Klicken Sie auf **Überwachungen ausführen**. Nach 10 bis 30 Sekunden bietet devtools einen Bericht.  Ihr Bericht gibt Ihnen verschiedene Tipps, wie Sie die Barrierefreiheit der Seite verbessern können.  
    
    > ##### Abbildung2  
    > Einen Bericht  
    > ![Einen Bericht][ImageReport]  
    
1.  Klicken Sie auf eine Überwachung, um mehr darüber zu erfahren.  
    
    > ##### Abbildung 3  
    > Weitere Informationen zu einer Überwachung  
    > ![Weitere Informationen zu einer Überwachung][ImageAttributes]  
    
1.  Klicken Sie auf **Weitere Informationen** , um die Dokumentation dieser Überwachung anzuzeigen.
    
    > ##### Abbildung4  
    > Anzeigen der Dokumentation einer Überwachung  
    > ![Anzeigen der Dokumentation einer Überwachung][ImageAuditDocumentation]  
    
### Siehe auch: aXe Extension   

Möglicherweise bevorzugen Sie die [Axt-Erweiterung][ChromeWebStoreAxe] anstelle des **Überwachungs** Panels.  
Die aXe-Erweiterung bietet im Allgemeinen dieselben Informationen, da es sich um das zugrunde liegende Modul handelt, das das Überwachungs Panel ausmacht.  Die aXe-Erweiterung hat eine andere Benutzeroberfläche und beschreibt die Überwachungen etwas anders.  
Ein Vorteil, den die Axt-Erweiterung über das **Überwachungs** Panel hat, besteht darin, dass Sie fehlerhafte Knoten überprüfen und markieren können.  

> ##### Abbildung5  
> Die Axt-Erweiterung  
> ![Die Axt-Erweiterung][ImageAxeExtension]  

## Der Bereich "Barrierefreiheit"   

Im Bereich " **Barrierefreiheit** " werden die Barrierefreiheits Struktur, Aria-Attribute und berechnete Barrierefreiheitseigenschaften von DOM-Knoten angezeigt.  

So öffnen Sie den Bereich **Barrierefreiheit** :  

1.  Klicken Sie auf die Registerkarte **Elemente** .  
1.  Wählen Sie in der **DOM-Struktur**das Element aus, das Sie überprüfen möchten.  
1.  Klicken Sie auf die Registerkarte **Barrierefreiheit** .  Diese Registerkarte ist möglicherweise **More Tabs** hinter der ![ Schaltfläche weitere Registerkarten weitere Tabstopps verborgen ][ImageMoreTabsIcon] .  

> ##### Abbildung6  
> Überprüfen des `h1` Elements der devtools-Homepage im Bereich " **Barrierefreiheit** "  
> ![Überprüfen des H1-Elements der devtools-Homepage im Bereich "Barrierefreiheit"][ImageA11yPane]  

### Anzeigen der Position eines Elements in der Barrierefreiheits Struktur   

Die [Barrierefreiheits Struktur][MDNAccessibilityTree] ist eine Teilmenge der DOM-Struktur.  Sie enthält nur Elemente aus der DOM-Struktur, die für die Anzeige des Inhalts einer Seite in einer Sprachausgabe relevant und nützlich sind.  

Überprüfen Sie die Position eines Elements in der Barrierefreiheits Struktur aus dem [Bereich Barrierefreiheit](#the-accessibility-pane).  

> ##### Abbildung7  
> Abschnitt "Barrierefreiheits Struktur"  
> ![Abschnitt "Barrierefreiheits Struktur"][ImageAllyTree]  

### Anzeigen der Aria-Attribute eines Elements   

Aria-Attribute stellen sicher, dass Bildschirmsprachausgaben alle Informationen enthalten, die Sie benötigen, um den Inhalt einer Seite ordnungsgemäß darzustellen.  

Zeigen Sie die Aria-Attribute eines Elements im [Bereich "Barrierefreiheit"](#the-accessibility-pane)an.  

> ##### Abbildung8  
> Der Abschnitt "Aria-Attribute"  
> ![Der Abschnitt "Aria-Attribute"][ImageAriaAttributesSection]  

### Anzeigen der berechneten Barrierefreiheitseigenschaften eines Elements   

> [!NOTE]
> Wenn Sie nach berechneten CSS-Eigenschaften suchen, lesen Sie die [Registerkarte berechnet][DevtoolsCssReferenceViewActuallyAppliedElements].  

Einige Barrierefreiheitseigenschaften werden vom Browser dynamisch berechnet.  Diese Eigenschaften werden im Abschnitt " **berechnete Eigenschaften** " des **Barrierefreiheits** Bereichs angezeigt.  

Zeigen Sie die berechneten Barrierefreiheitseigenschaften eines Elements im [Bereich "Barrierefreiheit"](#the-accessibility-pane)an.  

> ##### Abbildung 9  
> Der Abschnitt "berechnete (Barrierefreiheits-) Eigenschaften"  
> ![Der Abschnitt "berechnete (Barrierefreiheits-) Eigenschaften"][ImageComputedA11yPropertiesSection]  

## Anzeigen des Kontrastverhältnisses eines Textelements in der Farbauswahl   

Einige Personen mit Sehbehinderungen sehen keine Bereiche als sehr hell oder sehr dunkel.  Alles neigt dazu, bei ungefähr der gleichen Helligkeit zu erscheinen, wodurch es schwierig ist, Konturen und Kanten zu unterscheiden.  
Das Kontrastverhältnis misst den Helligkeitsunterschied zwischen Vordergrund und Hintergrund des Texts.  Wenn Ihr Text ein kontrastarmes Verhältnis hat, können diese sehbehinderten Benutzer Ihre Website buchstäblich als einen leeren Bildschirm sehen.  

Mit der Farbauswahl können Sie überprüfen, ob Ihr Text die empfohlenen Kontrast Raten erfüllt:  

1.  Klicken Sie auf die Registerkarte **Elemente** .  
1.  Wählen Sie in der **DOM-Struktur**das Textelement aus, das Sie überprüfen möchten.  
    
    > ##### Abbildung 10  
    > Überprüfen eines Absatzes in der DOM-Struktur  
    > ![Überprüfen eines Absatzes in der DOM-Struktur][ImageInspectDomTree]  
    
1.  Klicken Sie im Bereich **Formatvorlagen** auf das Farbquadrat neben dem `color` Wert des Elements.  
    
    > ##### Abbildung 11  
    > Die `color` Eigenschaft des Elements  
    > ![Die Color-Eigenschaft des Elements][ImageColorElement]  
    
1.  Überprüfen Sie den Abschnitt **Kontrastverhältnis** der Farbauswahl.  Ein Häkchen bedeutet, dass das Element die [minimale Empfehlung][W3CContrastMinimum]erfüllt.  Zwei Kontrollkästchen bedeuten, dass die [Erweiterte Empfehlung][W3CContrastEnhanced]erfüllt ist.
    
    > ##### Abbildung 12  
    > Der Abschnitt "Kontrastverhältnis" der Farbauswahl zeigt zwei Häkchen und einen Wert von `13.97`  
    > ![Der Abschnitt "Kontrastverhältnis" der Farbauswahl zeigt zwei Häkchen und einen Wert von 13,97.][ImageColorPickerContrastRatio]  
    
1.  Klicken Sie auf den Abschnitt **Kontrastverhältnis** , um weitere Informationen anzuzeigen.  Eine Zeile wird in der visuellen Auswahl oben in der Farbauswahl angezeigt.  Wenn die aktuelle Farbe Empfehlungen erfüllt, entspricht alles, was auf der gleichen Seite der Zeile steht, auch Empfehlungen.  Wenn die aktuelle Farbe keine Empfehlungen erfüllt, entspricht alles auf der gleichen Seite auch nicht den Empfehlungen.  
    
    > ##### Abbildung 13  
    > Die Zeile "Kontrastverhältnis" in der visuellen Auswahl  
    > ![Die Zeile "Kontrastverhältnis" in der visuellen Auswahl][ImageContrastRatioLine]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  

[ImageConfiguringAudits]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-pane.msft.png "Abbildung 1: Konfigurieren von Audits"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result.msft.png "Abbildung 2: eine Zahl"  
[ImageAttributes]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result-issues-expanded.msft.png "Abbildung 3: Weitere Informationen zu einer Überwachung"  
[ImageAuditDocumentation]: /microsoft-edge/devtools-guide-chromium/media/accessibility-web-dev-accessibility-audits-learn-more.msft.png "Abbildung 4: Anzeigen der Dokumentation einer Überwachung"  
[ImageAxeExtension]: /microsoft-edge/devtools-guide-chromium/media/accessibility-devtools-extension-axe-panel.msft.png "Abbildung 5: die Axt-Erweiterung"  
[ImageA11yPane]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility.msft.png "Abbildung 6: Überprüfen des H1-Elements der devtools-Homepage im Bereich "Barrierefreiheit""  
[ImageAllyTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-tree.msft.png "Abbildung 7: Abschnitt "Barrierefreiheits Struktur""  
[ImageAriaAttributesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-aria-attributes.msft.png "Abbildung 8: Abschnitt "Aria-Attribute""  
[ImageComputedA11yPropertiesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-computed-properties.msft.png "Abbildung 9: der Abschnitt "berechnete Eigenschaften (Barrierefreiheit)""  
[ImageInspectDomTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-paragraph-highlight.msft.png "Abbildung 10: Überprüfen eines Absatzes in der DOM-Struktur"  
[ImageColorElement]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color.msft.png "Abbildung 11: die Color-Eigenschaft des Elements"  
[ImageColorPickerContrastRatio]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png "Abbildung 12: der Abschnitt "Kontrastverhältnis" der Farbauswahl zeigt zwei Häkchen und einen Wert von 13,97."  
[ImageContrastRatioLine]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png "Abbildung 13: die Zeile "Kontrastverhältnis" in der visuellen Auswahl"  
<!-- links -->  

[DevtoolsAccessibilityNavigation]: navigation.md "Navigieren in Microsoft Edge devtools mit Hilfstechnologien"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Anzeigen nur des CSS, das tatsächlich auf ein Element angewendet wird-CSS-Referenz"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe – Web-Barrierefreiheits Tests – Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Barrierefreiheits Struktur (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Barrierefreiheit | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Sprachausgabe | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Kontrast (erweitert) AAA-Ebene | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Kontrast (Mindest) Ebene AA | W3C"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
