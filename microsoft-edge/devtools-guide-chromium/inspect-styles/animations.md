---
description: Überprüfen und Ändern von Animationen mit dem Animations Inspektor für Microsoft Edge devtools
title: Überprüfen von Animationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: e867cc373286666f73bee3b8fb886f60fa1b94f6
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015772"
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

# Überprüfen von Animationen  

Überprüfen und Ändern von Animationen mit dem Animations Inspektor für Microsoft Edge devtools  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Animations Inspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   Animations Inspektor  
:::image-end:::  

### Zusammenfassung  

*   Zeichnen Sie Animationen auf, indem Sie den Animations Inspektor öffnen.  Der Animations Inspektor erkennt und sortiert Animationen automatisch in Gruppen.  
*   Überprüfen Sie Animationen, indem Sie Sie verlangsamen, jede einzelne wiedergeben oder den Quellcode anzeigen.  
*   Sie können Animationen ändern, indem Sie den Offset für Anzeigedauer, Verzögerung, Dauer oder Keyframe ändern.  

## Übersicht  

Der Microsoft Edge devtools-Animations Inspektor hat zwei Hauptaufgaben.  

*   Untersuchen von Animationen  Sie möchten den Quellcode für eine Animationsgruppe verlangsamen, wiedergeben oder überprüfen.  
*   Ändern von Animationen  Sie möchten die Zeitmessung, die Verzögerung, die Dauer oder den Keyframe-Offset einer Animationsgruppe ändern.  Bezier-und Keyframe-Bearbeitung werden zurzeit nicht unterstützt.  

Der Animations Inspektor unterstützt CSS-Animationen, CSS-Übergänge und Web-Animationen.  `requestAnimationFrame` Animationen werden zurzeit nicht unterstützt.  

### Was ist eine Animationsgruppe?  

Bei einer Animationsgruppe handelt es sich um eine Gruppe von Animationen, die möglicherweise miteinander in Beziehung stehen.  Derzeit hat das Web kein echtes Konzept einer Gruppen Animation, daher müssen Motion-Designer und-Entwickler einzelne Animationen zusammenstellen und verfassen, damit die Animationen als ein kohärenter visueller Effekt gerendert werden.  Der Animations Inspektor prognostiziert, welche Animationen auf der Grundlage der Startzeit \ (ohne Verzögerungen usw.) zusammenhängen.  Der Animations Inspektor gruppiert auch die Animationen nebeneinander.  
Mit anderen Worten: eine Gruppe von Animationen, die alle im gleichen Skriptblock ausgelöst werden, wird zusammen gruppiert.  Wenn eine Animation asynchron ist, wird Sie in eine separate Gruppe verschoben.  

## Erste Schritte  

Es gibt zwei Möglichkeiten, den Animations Inspektor zu öffnen:  

*   Öffnen des Menüs zum **anpassen und Steuern des devtools**  
    1.  Navigieren Sie zum unter Menü **Weitere Tools** .  
    1.  Wählen Sie **Animationen**aus:  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animationen mithilfe des Hauptmenüs" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Animationen** mithilfe des Hauptmenüs  
    :::image-end:::  
        
*   Öffnen des **Befehlsmenüs**  
    1.  Geben Sie `Drawer: Show Animations` ein.  

Der Animations Inspektor wird als Registerkarte neben dem Konsolen Einzug geöffnet.  Da es sich bei dem Animations Inspektor um eine Schublade handelt, können Sie den Animations Inspektor in einem beliebigen devtools-Fenster verwenden.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Animations Inspektor leeren" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Animations Inspektor leeren  
:::image-end:::  

Der Animations Inspektor ist in vier Hauptabschnitte unterteilt \ (oder Bereiche \).  Dieser Leitfaden bezieht sich auf jeden Bereich wie folgt:  

| Index | Bereich | Beschreibung |  
|:--- |:--- |:--- |  
| 1 | **Steuerelemente** | Hier können Sie alle aktuell aufgenommenen Animationsgruppen löschen oder die Geschwindigkeit der aktuell ausgewählten Animationsgruppe ändern. |  
| 2 | **Übersicht** | Wählen Sie hier eine Animationsgruppe aus, um Sie im **Detail** Bereich zu überprüfen und zu ändern. |  
| 3 | **Zeitachse** | Pausieren und starten Sie eine Animation von hier aus, oder springen Sie zu einer bestimmten Stelle in der Animation. |  
| 4 | **Details** | Überprüfen und Ändern der aktuell ausgewählten Animationsgruppe |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Animations Inspektor mit Anmerkungen" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Animations Inspektor mit Anmerkungen  
:::image-end:::  

Wenn Sie eine Animation aufzeichnen möchten, führen Sie einfach die Interaktion aus, mit der die Animation ausgelöst wird, während der Animations Inspektor geöffnet ist.  Wenn beim Laden einer Seite eine Animation ausgelöst wird, laden Sie die Seite neu, wobei der Animations Inspektor geöffnet wird, um die Animation zu erkennen.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Überprüfen von Animationen  

Nachdem Sie eine Animation aufgenommen haben, gibt es verschiedene Möglichkeiten, Sie wiederzugeben:  

*   Zeigen Sie **mit der Maus** auf die Miniaturansicht im Übersichtsbereich, um eine Vorschau davon anzuzeigen.  
*   Wählen **Sie im Übersichtsbereich die** Gruppe Animation aus, damit Sie im **Detail** Bereich angezeigt wird, und drücken Sie dann das Symbol **Wiedergabe** \ ( ![ Wiedergabe ][ImageReplayButtonIcon] -Symbol).  Die Animation wird im Viewport wiedergegeben.  Klicken Sie auf die Symbole **Animationsgeschwindigkeit** \ ( ![ Animations Geschwindigkeits Symbole ][ImageAnimationSpeedButtonsIcon] \), um die Vorschau Geschwindigkeit der aktuell ausgewählten Animationsgruppe zu ändern.  Sie können die rote vertikale Leiste verwenden, um Ihre aktuelle Position zu ändern.  
*   Klicken Sie, und ziehen Sie den roten vertikalen Balken, um die Animation des Viewports zu schrubben.  
    
### Anzeigen von Animations Details  

Nachdem Sie eine Animationsgruppe erfasst haben, klicken **Sie im Übersichtsbereich darauf** , um die Details anzuzeigen.  Im **Detail** Bereich wird jeder einzelnen Animation die Zeile a zugewiesen.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Animationsgruppen Details" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Animationsgruppen Details  
:::image-end:::  

Zeigen Sie mit der Maus auf eine Animation, um Sie im Viewport zu markieren.  Klicken Sie auf die Animation, um Sie im **Element** Panel zu markieren.  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Zeigen Sie mit der Maus auf die Animation, um Sie im Viewport hervorzuheben" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Zeigen Sie mit der Maus auf die Animation, um Sie im Viewport hervorzuheben  
:::image-end:::  

Der linke, dunklere Abschnitt einer Animation ist die Definition.  Der Rechte, verblasstere Abschnitt stellt Iterationen dar.  In der folgenden Abbildung stellen die Abschnitte zwei und drei beispielsweise Iterationen von Abschnitt eins dar.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramm der Animations Iterationen" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Diagramm der Animations Iterationen  
:::image-end:::  

Wenn für zwei Elemente dieselbe Animation angewendet wurde, weist der Animations Inspektor den Elementen dieselbe Farbe zu.  Die Farbe ist zufällig und hat keine Bedeutung.  In der folgenden Abbildung finden Sie beispielsweise die beiden Elemente, `div.cwccw.earlier` und es werden die `div.cwccw.later` gleichen Animationen `spinrightleft` wie die `div.ccwcw.earlier` und- `div.ccwcw.later` Elemente angewendet.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Farbcodierte Animationen" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Farbcodierte Animationen  
:::image-end:::  

## Ändern von Animationen  

Es gibt drei Möglichkeiten, wie Sie eine Animation mit dem Animations Inspektor ändern können.  

*   Animationsdauer.  
*   Keyframe-Anzeigedauern.  
*   Anfangszeit Verzögerung.  
    
In der folgenden Abbildung wird die ursprüngliche Animation dargestellt.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Ursprüngliche Animation vor der Änderung" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Ursprüngliche Animation vor der Änderung  
:::image-end:::  

Wenn Sie die Dauer einer Animation ändern möchten, klicken Sie auf den ersten oder letzten Kreis, und ziehen Sie ihn.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Geänderte Dauer" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Geänderte Dauer  
:::image-end:::  

Wenn die Animation Keyframe-Regeln definiert, werden diese als weiße innere Kreise dargestellt.  Klicken Sie, und ziehen Sie eine der folgenden Schritte, um die Anzeigedauer des Keyframes zu ändern.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Geänderter Keyframe" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Geänderter Keyframe  
:::image-end:::  

Wenn Sie einer Animation eine Verzögerung hinzufügen möchten, klicken Sie darauf, und ziehen Sie Sie mit Ausnahme der Kreise an eine beliebige Stelle.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Geänderte Verzögerung" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Geänderte Verzögerung  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
