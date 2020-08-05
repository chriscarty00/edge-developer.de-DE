---
title: Erste Schritte mit dem Anzeigen und Ändern von CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 346145a7deb9e8ac951ed0578a5060da72817463
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710385"
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

# Erste Schritte mit dem Anzeigen und Ändern von CSS  

Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen für das Anzeigen und Ändern des CSS für eine Seite mit Microsoft Edge devtools zu erlernen.  

## Öffnen von CSS-Beispielen  

1.  Halten `Control` Sie \ (Windows \) oder `Command` \ (macOS \) gedrückt, und wählen Sie **CSS-Beispiele** aus, um Sie in einem neuen Fenster zu öffnen.  
    
    [CSS-Beispiele][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Wenn Sie Ihr devtools-Fenster auf der rechten Seite Ihres Viewports [Andocken][DevToolsCustomizePlacement] möchten (in der folgenden Abbildung dargestellt \), wählen Sie **anpassen und Steuer devtools** `...` .  Wählen Sie im Dropdownmenü **anpassen und Steuern des devtools** im Abschnitt **Docking Seite** die Option **Dock to right**aus.  
    
## Anzeigen des CSS für ein Element  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den `Inspect Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
    1.  In devtools wird das Element im Panel **Elemente** auf der Registerkarte **DOM** -Struktur `Inspect Me!` hervorgehoben.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Das geprüfte Element ist in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-inspect-me.msft.png":::
           Abbildung 1: das geprüfte Element ist in der **DOM-Struktur** hervorgehoben  
        :::image-end:::  
        
    1.  `Inspect Me!`Suchen Sie im Element den Wert des Attributs, `data-message` und kopieren Sie ihn.  
1.  Geben Sie auf der Seite im **Wert von `data-message` :** TextBox den Wert ein.  
1.  Zeigen Sie auf den `Inspect Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
    1.  Wählen Sie in devtools im Panel **Elemente** die Registerkarte **Formatvorlagen** aus.  
    1.  Auf der Registerkarte **Formatvorlagen** `Inspect Me!` ist das Element hervorgehoben.  
    1.  `Inspect Me!`Suchen Sie im Element die `aloha` Klassen Regel.  
        
        > [!NOTE]
        > Diese Regel wird angezeigt, weil Sie auf das Element angewendet wird `Inspect Me!` .  
        
    1.  `aloha`Suchen Sie in der Klasse den Wert für die `padding` Formatvorlage, und kopieren Sie Sie.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Auf das geprüfte Element angewendete CSS-Klassen werden auf der Registerkarte Formatvorlagen hervorgehoben." lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Abbildung 2: CSS-Klassen, die auf das ausgewählte Element angewendet werden, wie etwa `aloha` , werden auf der Registerkarte " **Formatvorlagen** " angezeigt  
        :::image-end:::  
        
1.  Geben Sie auf der Seite im **Wert von `padding` :** TextBox den Wert ein.  

## Hinzufügen einer CSS-Deklaration zu einem Element  

Verwenden Sie die Registerkarte **Formatvorlagen** , wenn Sie einem Element CSS-Deklarationen ändern oder hinzufügen möchten.  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den `Add A Background Color To Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
1.  Wählen Sie am `element.style` oberen Rand der Registerkarte **Formatvorlagen** aus.  
1.  Geben `background-color` Sie ein, und drücken Sie `Enter` .  
1.  Geben `honeydew` Sie ein, und drücken Sie `Enter` .  In der **DOM-Struktur** sollten Sie sehen, dass eine Inlineformatvorlagen Deklaration auf das Element angewendet wurde.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Hinzufügen einer CSS-Deklaration zum Element mithilfe der Registerkarte Formatvorlagen" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       Abbildung 3: die `background-color:honeydew` Deklaration wurde auf das Element über den `element.style` Abschnitt der Registerkarte " **Formatvorlagen** " angewendet  
    :::image-end:::  
    
## Hinzufügen einer CSS-Klasse zu einem Element  

Verwenden Sie die Registerkarte **Formatvorlagen** , um zu sehen, wie ein Element aussieht, wenn eine CSS-Klasse auf ein Element angewendet oder daraus entfernt wurde.  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den `Add A Class To Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
1.  Wählen Sie **CLS**aus.  DevTools zeigt ein Textfeld an, in dem Sie dem ausgewählten Elementklassen hinzufügen können.  
1.  Geben `color_me` Sie in das Textfeld **neue Klasse hinzufügen** ein, und drücken Sie dann `Enter` .  Unterhalb des Textfelds **neue Klasse hinzufügen** wird ein Kontrollkästchen eingeblendet, in dem Sie die Klasse ein-und ausblenden können.  Wenn `Add A Class To Me!` auf das Element andere Klassen angewendet werden, können Sie auch von hier aus umschalten.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Anwenden der color_me Klasse auf das Element" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       Abbildung 4: die `color_me` Klasse wurde auf das Element mit dem Abschnitt " **. CLS** " auf der Registerkarte " **Formatvorlagen** " angewendet.  
    :::image-end:::  
    
## Hinzufügen eines PseudoState zu einer Klasse  

Verwenden Sie die Registerkarte **Formatvorlagen** , um eine CSS-PseudoState dauerhaft auf ein Element anzuwenden.  DevTools unterstützt `:active` , `:focus` , `:hover` und `:visited` .  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie mit der Maus auf den `Hover Over Me!` Text.  Die Hintergrundfarbe ändert sich.  
1.  Zeigen Sie auf den `Hover Over Me!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
1.  Wählen Sie auf der Registerkarte **Formatvorlagen** die Option **: Hov**aus.  
1.  Aktivieren Sie das Kontrollkästchen **Hover** .  Die Hintergrundfarbe ändert sich wie zuvor, auch wenn Sie nicht tatsächlich auf das Element zeigen.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Umschalten des Hover-PseudoState für ein Element" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Abbildung 5: `:hover` Umschalten des PseudoState für ein Element  
    :::image-end:::  
    
## Ändern der Abmessungen eines Elements  

Verwenden Sie das interaktive Diagramm des **Feld Modells** auf der Registerkarte **Formatvorlagen** , um die Breite, Höhe, Abstand, Seitenrand oder die Rahmenlänge eines Elements zu ändern.  

> [!NOTE]
> Führen Sie die [Ansicht CSS für ein Element](#view-the-css-for-an-element) -Lernprogramm aus, bevor Sie diesen Vorgang ausführen.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den `Change My Margin!` Text, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie über **prüfen**aus.  
1.  Zeigen Sie im Diagramm **Feld Modell** auf der Registerkarte **Formatvorlagen** auf **Abstand**.  Der Abstand eines Elements wird im Viewport hervorgehoben.  

    > [!NOTE]
    > Je nach Größe des devtools-Fensters müssen Sie möglicherweise an den unteren Rand der Registerkarte **Formatvorlagen** scrollen, um das **Feld Modell**anzuzeigen.  

1.  Doppelklicken Sie auf den linken Rand im **Feld Modell**, das derzeit den Wert Bedeutung hat, `-` dass das Element keinen linken Rand aufweist.  
1.  Geben `100px` Sie ein, und drücken Sie `Enter` .  Das **Feld Modell** ist standardmäßig Pixel, akzeptiert aber auch andere Werte wie " `25%` oder" `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Bewegen des Mauszeigers über den Abstand des Elements" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Abbildung 6: Bewegen des Mauszeigers über den Abstand des Elements  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Ändern des linken Rands des Elements" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Abbildung 7: Ändern des linken Rands des Elements  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Debuggen von medienabfragen  

[Medienabfragen][MDNUsingMediaGueries] stellen eine Möglichkeit dar, damit Ihr Web-Produkt auf Änderungen in den Konfigurationseinstellungen für jeden Benutzer reagiert.  Der bedeutendste Anwendungsfall besteht darin, dem Produkt je nach Größe des Viewports ein anderes CSS-Layout bereitzustellen.  Das Verwenden separater Layouts ermöglicht ein Layout mit einer Spalte für mobile Geräte und mehrspaltige Layouts, wenn mehr Bildschirm Auflagen zur Verfügung stehen.  

Führen Sie die folgenden Schritte aus, wenn Sie die medienabfragen, die Sie in Ihrem CSS definiert haben, Debuggen oder testen möchten.  

1.  Öffnen Sie die Entwicklertools, und wählen Sie in der oberen linken Ecke das Symbol " **Gerätesymbolleiste umschalten** " aus, oder drücken Sie `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` unter macOS \).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Öffnen der Gerätesymbolleiste" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Abbildung 8: Öffnen der Gerätesymbolleiste  
    :::image-end:::  
    
1.  Wenn die Gerätesymbolleiste geöffnet ist, wählen Sie das `...` Menü oben rechts aus, und wählen Sie **medienabfragen anzeigen**aus.  Oberhalb der Anzeige der Seite sollten farbige Balken angezeigt werden, die die verschiedenen medienabfragen darstellen.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Anzeigen von medienabfragen in der Gerätesymbolleiste" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Abbildung 9: Anzeigen von medienabfragen in der Gerätesymbolleiste  
    :::image-end:::  
    
1.  Zeigen Sie mit der Maus auf die Begrenzungen in den Balken, um die Werte der verschiedenen medienabfragen anzuzeigen. Wählen Sie die einzelnen Seiten aus, um die Größe der Webseite anzupassen.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Auswählen der medienabfrage aus der Vorschauleiste" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Abbildung 10: Auswählen der medienabfrage aus der Vorschauleiste  
    :::image-end:::  
    
1.  Um medienabfragen zu Debuggen und die CSS-Datei im Editor zu öffnen, bewegen Sie den `Sources` Mauszeiger auf einem beliebigen Balkensegment, öffnen Sie das Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie aus `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Anzeigen von medienabfragen im Quellen-Editor" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Abbildung 11: Anzeigen von medienabfragen im Quellen-Editor  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "CSS-Beispiele – Microsoft Edge (Chrom) devtools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Verwenden von medienabfragen | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/index) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
