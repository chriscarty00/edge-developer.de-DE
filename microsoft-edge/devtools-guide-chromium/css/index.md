---
title: Erste Schritte beim Anzeigen und Ändern von CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601817"
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





# Erste Schritte beim Anzeigen und Ändern von CSS   



Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen für das Anzeigen und Ändern des CSS für eine Seite mit Microsoft Edge devtools zu erlernen.  

## Öffnen von CSS-Beispielen  

1.  Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und klicken Sie auf **CSS-Beispiele** , um Sie in einem neuen Fenster zu öffnen.  
    
    [CSS-Beispiele][GlitchDevToolsCssExamples]  

> [!NOTE]
> Wenn Sie Ihr devtools-Fenster auf der rechten Seite Ihres Viewports [Andocken][DevToolsCustomizePlacement] möchten (wird in [Abbildung 1](#figure-1)angezeigt), klicken Sie auf **anpassen, und Steuern Sie devtools** `...` .  Wählen Sie im Dropdownmenü **anpassen und Steuern des devtools** im Abschnitt **Docking Seite** die Option **Dock to right**aus.  
    
## Anzeigen des CSS für ein Element   

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Klicken Sie mit der rechten Maustaste auf den `Inspect Me!` Text, und wählen Sie **prüfen**aus.  
    1.  In devtools wird das Element im Panel **Elemente** auf der Registerkarte **DOM** -Struktur `Inspect Me!` hervorgehoben.  
        
        > ##### Abbildung1  
        > Das geprüfte Element ist in der **DOM-Struktur** hervorgehoben.  
        > ![Das geprüfte Element ist in der DOM-Struktur hervorgehoben.][ImageInspect]  
        
    1.  `Inspect Me!`Suchen Sie im Element den Wert des Attributs, `data-message` und kopieren Sie ihn.  
1.  Geben Sie auf der Seite im **Wert von `data-message` :** TextBox den Wert ein.  
1.  Klicken Sie mit der rechten Maustaste auf den `Inspect Me!` Text, und wählen Sie **prüfen**aus.  
    
    1.  Wählen Sie in devtools im Panel **Elemente** die Registerkarte **Formatvorlagen** aus.  
    1.  Auf der Registerkarte **Formatvorlagen** `Inspect Me!` ist das Element hervorgehoben.  
    1.  `Inspect Me!`Suchen Sie im Element die `aloha` Klassen Regel.  
        
        > [!NOTE]
        > Diese Regel wird angezeigt, weil Sie auf das Element angewendet wird `Inspect Me!` .  
        
    1.  `aloha`Suchen Sie in der Klasse den Wert für die `padding` Formatvorlage, und kopieren Sie Sie.  
        
        > ##### Abbildung2  
        > Auf das ausgewählte Element angewendete CSS-Klassen wie `aloha` "werden auf der Registerkarte" **Formatvorlagen** "angezeigt  
        > ![Auf das geprüfte Element angewendete CSS-Klassen werden auf der Registerkarte "Formatvorlagen" hervorgehoben.][ImageAloha]  
        
1.  Geben Sie auf der Seite im **Wert von `padding` :** TextBox den Wert ein.  

## Hinzufügen einer CSS-Deklaration zu einem Element   

Verwenden Sie die Registerkarte **Formatvorlagen** , wenn Sie einem Element CSS-Deklarationen ändern oder hinzufügen möchten.  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Klicken Sie mit der rechten Maustaste auf den `Add A Background Color To Me!` Text, und wählen Sie **prüfen**aus.  
1.  Klicken Sie oben auf der `element.style` Registerkarte **Formatvorlagen** auf oben.  
1.  Geben `background-color` Sie ein, und drücken Sie `Enter` .  
1.  Geben `honeydew` Sie ein, und drücken Sie `Enter` .  In der **DOM-Struktur** sollten Sie sehen, dass eine Inlineformatvorlagen Deklaration auf das Element angewendet wurde.  

> ##### Abbildung 3  
> Die `background-color:honeydew` Deklaration wurde auf das Element über den `element.style` Abschnitt auf der Registerkarte " **Formatvorlagen** " angewendet.  
> ![Hinzufügen einer CSS-Deklaration zum Element mithilfe der Registerkarte "Formatvorlagen"][ImageDeclaration]  

## Hinzufügen einer CSS-Klasse zu einem Element   

Verwenden Sie die Registerkarte **Formatvorlagen** , um zu sehen, wie ein Element aussieht, wenn eine CSS-Klasse auf ein Element angewendet oder daraus entfernt wurde.  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Klicken Sie mit der rechten Maustaste auf das `Add A Class To Me!` Element, und wählen Sie **prüfen**aus.  
1.  Klicken Sie auf **. CLS**.  DevTools zeigt ein Textfeld an, in dem Sie dem ausgewählten Elementklassen hinzufügen können.  
1.  Geben `color_me` Sie in das Textfeld **neue Klasse hinzufügen** ein, und drücken Sie dann `Enter` .  Unterhalb des Textfelds **neue Klasse hinzufügen** wird ein Kontrollkästchen eingeblendet, in dem Sie die Klasse ein-und ausblenden können.  Wenn `Add A Class To Me!` auf das Element andere Klassen angewendet werden, können Sie auch von hier aus umschalten.  

> ##### Abbildung4  
> Die `color_me` Klasse wurde auf das Element mit dem Abschnitt " **. CLS** " auf der Registerkarte " **Formatvorlagen** " angewendet.  
> ![Anwenden der color_me Klasse auf das Element][ImageApplyClass]  

## Hinzufügen eines PseudoState zu einer Klasse   

Verwenden Sie die Registerkarte **Formatvorlagen** , um eine CSS-PseudoState dauerhaft auf ein Element anzuwenden.  DevTools unterstützt `:active` , `:focus` , `:hover` und `:visited` .  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie mit der Maus auf den `Hover Over Me!` Text.  Die Hintergrundfarbe ändert sich.  
1.  Klicken Sie mit der rechten Maustaste auf den `Hover Over Me!` Text, und wählen Sie **prüfen**aus.  
1.  Klicken Sie auf der Registerkarte **Formatvorlagen** auf **: Hov**.  
1.  Aktivieren Sie das Kontrollkästchen **Hover** .  Die Hintergrundfarbe ändert sich wie zuvor, auch wenn Sie nicht tatsächlich auf das Element zeigen.  

> ##### Abbildung5  
> Umschalten des `:hover` PseudoState für ein Element  
> ![Umschalten des Hover-PseudoState für ein Element][ImageSetHover]  

## Ändern der Abmessungen eines Elements   

Verwenden Sie das interaktive Diagramm des **Feld Modells** auf der Registerkarte **Formatvorlagen** , um die Breite, Höhe, Abstand, Seitenrand oder die Rahmenlänge eines Elements zu ändern.  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Klicken Sie mit der rechten Maustaste auf das `Change My Margin!` Element, und wählen Sie **prüfen**aus.  
1.  Zeigen Sie im Diagramm **Feld Modell** auf der Registerkarte **Formatvorlagen** auf **Abstand**.  Der Abstand eines Elements wird im Viewport hervorgehoben.  

    > [!NOTE]
    > Je nach Größe des devtools-Fensters müssen Sie möglicherweise an den unteren Rand der Registerkarte **Formatvorlagen** scrollen, um das **Feld Modell**anzuzeigen.  

1.  Doppelklicken Sie auf den linken Rand im **Feld Modell**, das derzeit den Wert Bedeutung hat, `-` dass das Element keinen linken Rand aufweist.  
1.  Geben `100px` Sie ein, und drücken Sie `Enter` .  Das **Feld Modell** ist standardmäßig Pixel, akzeptiert aber auch andere Werte wie " `25%` oder" `10vw` .  

> ##### Abbildung6  
> Bewegen des Mauszeigers über den Abstand des Elements  
> ![Bewegen des Mauszeigers über den Abstand des Elements][ImageShowPadding]  

> ##### Abbildung7  
> Ändern des linken Rands des Elements  
> ![Ändern des linken Rands des Elements][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Abbildung 1: das geprüfte Element ist in der DOM-Struktur hervorgehoben"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Abbildung 2: CSS-Klassen, die auf das geprüfte Element angewendet werden, werden auf der Registerkarte "Formatvorlagen" hervorgehoben."  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Abbildung 3: Hinzufügen einer CSS-Deklaration zum Element mithilfe der Registerkarte "Formatvorlagen""  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Abbildung 4: Anwenden der color_me Klasse auf das Element"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Abbildung 5: Umschalten des Hover-PseudoState für ein Element"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Abbildung 6: Bewegen des Mauszeigers über den Abstand des Elements"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Abbildung 7: Ändern des linken Rands des Elements"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "CSS-Beispiele – Microsoft Edge (Chrom) devtools | Glitch"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
