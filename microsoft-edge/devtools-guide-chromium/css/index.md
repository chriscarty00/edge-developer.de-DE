---
description: Erfahren Sie, wie Sie Microsoft Edge DevTools zum Anzeigen und Ändern des CSS einer Seite verwenden.
title: Erste Schritte mit dem Anzeigen und Ändern von CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: bc629286530e709bef0e04a671f1a0e56eee48ea
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564448"
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
# <a name="get-started-with-viewing-and-changing-css"></a>Erste Schritte mit dem Anzeigen und Ändern von CSS  

Führen Sie diese interaktiven Lernprogramme aus, um die Grundlagen des Anzeigens und Änderns der CSS für eine Seite mithilfe von devTools Microsoft Edge lernen.  

## <a name="open-css-examples"></a>Öffnen von CSS-Beispielen  

1.  Halten `Control` Sie \(Windows, Linux\) oder \(macOS\) fest, und wählen Sie `Command` **CSS-Beispiele aus,** um sie in einem neuen Fenster zu öffnen.  
    
    [CSS-Beispiele][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Wenn Sie Ihr [DevTools-Fenster][DevToolsCustomizePlacement] rechts neben Ihrem Viewport \(in der folgenden Abbildung angezeigt) andocken möchten, wählen Sie Anpassen und Steuern von **DevTools aus.** `...`  Wählen Sie **im Dropdownmenü Anpassen** und Steuern von DevTools im Abschnitt **Dock** nach rechts **Dock aus.**  
    
## <a name="view-the-css-for-an-element"></a>Anzeigen der CSS für ein Element  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Inspect Me!` Maustaste\), und wählen Sie **Überprüfen aus.**  
    1.  In DevTools wird das **Element im Elementtool** im **BEREICH DOM-Struktur** `Inspect Me!` hervorgehoben.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Das überprüfte Element wird in der DOM-Struktur hervorgehoben." lightbox="../media/css-elements-inspect-me.msft.png":::
           Das überprüfte Element wird in der **DOM-Struktur hervorgehoben.**  
        :::image-end:::  
        
    1.  Suchen Sie `Inspect Me!` im Element nach dem Wert des `data-message` Attributs, und kopieren Sie es.  
1.  Geben Sie auf der Seite im **Textfeld Wert von `data-message` :** den Wert ein.  
1.  Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Inspect Me!` Maustaste\), und wählen Sie **Überprüfen aus.**  
    1.  Wählen Sie in DevTools im **Tool Elemente** den Bereich **Formatvorlagen** aus.  
    1.  Im **Bereich Formatvorlagen** wird `Inspect Me!` das Element hervorgehoben.  
    1.  Suchen Sie `Inspect Me!` im Element nach der `aloha` Klassenregel.  
        
        > [!NOTE]
        > Diese Regel wird angezeigt, da sie auf das Element angewendet `Inspect Me!` wird.  
        
    1.  Suchen Sie `aloha` in der Klasse nach dem Wert für die `padding` Formatvorlage, und kopieren Sie sie.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="CSS-Klassen, die auf das überprüfte Element angewendet werden, werden im Bereich Formatvorlagen hervorgehoben." lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           CSS-Klassen werden auf das ausgewählte Element angewendet, z. B. `aloha` , werden im **Formatvorlagenbereich** angezeigt.  
        :::image-end:::  
        
1.  Geben Sie auf der Seite im **Textfeld Wert von `padding` :** den Wert ein.  

## <a name="add-a-css-declaration-to-an-element"></a>Hinzufügen einer CSS-Deklaration zu einem Element  

Verwenden Sie **den Formatvorlagenbereich,** wenn Sie einem Element CSS-Deklarationen ändern oder hinzufügen möchten.  

> [!NOTE]
> Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Add A Background Color To Me!` Maustaste\), und wählen Sie **Überprüfen aus.**  
1.  Wählen `element.style` Sie am oberen Rand des **Formatvorlagenbereichs** aus.  
1.  Geben `background-color` Sie ein, und wählen Sie `Enter` aus.  
1.  Geben `honeydew` Sie ein, und wählen Sie `Enter` aus.  In der **DOM-Struktur**wird eine auf das Element angewendete Inlineformatdeklaration angezeigt.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Hinzufügen einer CSS-Deklaration zum Element mithilfe des Formatvorlagenbereichs" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       Die Deklaration wird mithilfe des Abschnitts `background-color:honeydew` `element.style` des Formatvorlagenbereichs auf das **Element** angewendet.  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a>Hinzufügen einer CSS-Klasse zu einem Element  

Navigieren Sie zum Formatvorlagenbereich, um zu zeigen, wie ein Element aussieht, wenn eine CSS-Klasse auf ein Element angewendet oder aus diesem entfernt **wird.**  

> [!NOTE]
> Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Add A Class To Me!` Maustaste\), und wählen Sie **Überprüfen aus.**  
1.  Wählen **Sie .cls**aus.  DevTools zeigt ein Textfeld an, in dem Sie dem ausgewählten Element Klassen hinzufügen können.  
1.  Geben `color_me` Sie in das Textfeld Neue Klasse **hinzufügen** ein, und wählen Sie dann `Enter` aus.  Unterhalb des Textfelds Neue **Klasse** hinzufügen wird ein Kontrollkästchen angezeigt, in dem Sie die Klasse ein- und ausschalten können.  Wenn auf das Element andere Klassen angewendet wurden, können Sie auch von hier aus `Add A Class To Me!` umschalten.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Anwenden der color_me-Klasse auf das Element" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       Die `color_me` Klasse wird mithilfe des **Abschnitts CLS** des Formatvorlagenbereichs auf das **Element** angewendet.  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a>Hinzufügen eines Pseudozustands zu einer Klasse  

Verwenden Sie **den Formatvorlagenbereich,** um einen CSS-Pseudozustand dauerhaft auf ein Element anzuwenden.  DevTools unterstützt `:active` , `:focus` , und `:hover` `:visited` .  

> [!NOTE]
> Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den `Hover Over Me!` Text.  Die Hintergrundfarbe ändert sich.  
1.  Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Hover Over Me!` Maustaste\), und wählen Sie **Überprüfen aus.**  
1.  Wählen Sie **im Bereich** Formatvorlagen die Option **:hov aus.**  
1.  Aktivieren Sie das **Kontrollkästchen :hover.**  Die Hintergrundfarbe ändert sich wie zuvor, auch wenn Sie nicht mit dem Mauszeiger auf das Element zeigen.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Umschalten des Hover-Pseudozustands für ein Element" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Umschalten des `:hover` Pseudozustands für ein Element  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a>Ändern der Dimensionen eines Elements  

Verwenden Sie **das interaktive** **** Diagramm Box Model im Bereich Formatvorlagen, um die Breite, Höhe, Abstand, Rand- oder Rahmenlänge eines Elements zu ändern.  

> [!NOTE]
> Führen Sie das [Lernprogramm Css für ein Element anzeigen](#view-the-css-for-an-element) aus, bevor Sie dieses Lernprogramm verwenden.  

1.  [Öffnen Sie CSS-Beispiele](#open-css-examples).  
1.  Zeigen Sie auf den Text, öffnen Sie das Kontextmenü \(klicken Sie mit der rechten `Change My Margin!` Maustaste\), und wählen Sie **Überprüfen aus.**  
1.  Zeigen Sie **im Diagramm Feldmodell** im Bereich **Formatvorlagen** auf **Abstand.**  Der Abstand eines Elements wird im Viewport hervorgehoben.  

    > [!NOTE]
    > Abhängig von der Größe Ihres DevTools-Fensters müssen Sie **** möglicherweise einen Bildlauf zum unteren Rand des Formatvorlagenbereichs durchführen, um das **Feldmodell anzuzeigen.**  

1.  Doppelklicken Sie im **Feldmodell**auf den linken Rand, der aktuell bedeutet, dass das Element keinen linken `-` Rand hat.  
1.  Geben `100px` Sie ein, und wählen Sie `Enter` aus.  Das **Feldmodell** ist standardmäßig auf Pixel festgelegt, akzeptiert aber auch andere Werte, z. B. `25%` , oder `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Zeigen auf den Abstand des Elements" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Zeigen auf den Abstand des Elements  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Ändern des linken Rands des Elements" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Ändern des linken Rands des Elements  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a>Debuggen von Medienabfragen  

[Medienabfragen][MDNUsingMediaGueries] sind eine Möglichkeit, ihr Webprodukt auf Änderungen in den Konfigurationseinstellungen für jeden Benutzer zu reagieren.  Der wichtigste Verwendungsfall ist die Bereitstellung eines anderen CSS-Layouts in Abhängigkeit von den Abmessungen des Viewports.  Die Verwendung separater Layouts ermöglicht ein einspaltiges Layout für mobile Geräte und mehrspaltige Layouts, wenn mehr Bildschirmaufteilung verfügbar ist.  

Wenn Sie die in Ihrer CSS definierten Medienabfragen debuggen oder testen möchten, verwenden Sie die folgenden Schritte.  

1.  Öffnen Sie die Entwicklertools, und wählen Sie auf der linken oberen Seite das Symbol Symbolleiste des Umschaltgeräts aus, oder wählen Sie **** `Ctrl` + `Shift` + `M` \( unter `Cmd` + `Shift` + `M` macOS\).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Öffnen der Gerätesymbolleiste" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Öffnen der Gerätesymbolleiste  
    :::image-end:::  
    
1.  Wenn die Gerätesymbolleiste geöffnet ist, wählen Sie das `...` Menü oben rechts aus, und wählen Sie **Medienabfragen anzeigen aus.**  Die farbigen Balken, die über der Webseite angezeigt werden, stellen die verschiedenen Medienabfragen dar.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Anzeigen von Medienabfragen in der Gerätesymbolleiste" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Anzeigen von Medienabfragen in der Gerätesymbolleiste  
    :::image-end:::  
    
1.  Zeigen Sie auf die Begrenzungen in den Balken, um die Werte der verschiedenen Medienabfragen anzeigen zu können.  Wählen Sie jeweils aus, um die zu ändernde Webseite zu ändern.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Auswählen von Medienabfragen in der Vorschauleiste" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Auswählen von Medienabfragen in der Vorschauleiste  
    :::image-end:::  
    
1.  Um Medienabfragen zu debuggen und die #A0 im Editor zu öffnen, zeigen Sie auf eines der Balkensegmente, öffnen Sie das Kontextmenü `Sources` \(rechtsklicken\), und wählen Sie `reveal in source code` aus.  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Enthebnen von Medienabfragen im Quellen-Editor" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Enthebnen von Medienabfragen im Quellen-Editor  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Ändern Microsoft Edge DevTools-Platzierung (Abdocken, Dock nach unten, Dock nach links)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "CSS-Beispiele – Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Verwenden von Medienabfragen | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/css/index) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
