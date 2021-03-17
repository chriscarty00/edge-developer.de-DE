---
description: Überprüfen und Ändern von Animationen mit dem Microsoft Edge DevTools Animation Inspector.
title: Überprüfen von Animationen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: dba948087ca06015f686d17ba48584199373805a
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439542"
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

# <a name="inspect-animations"></a>Überprüfen von Animationen  

Überprüfen und Ändern von Animationen mit dem Microsoft Edge DevTools Animation Inspector.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Animationsinspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   Animationsinspektor  
:::image-end:::  

### <a name="summary"></a>Zusammenfassung  

*   Erfassen Sie Animationen, indem Sie den Animationsinspektor öffnen.  Der Animationsinspektor erkennt und sortiert Animationen automatisch in Gruppen.  
*   Überprüfen Sie Animationen, indem Sie die einzelnen Animationen verlangsamen, jeweils wiedergeben oder den Quellcode anzeigen.  
*   Ändern Sie Animationen, indem Sie den Zeit-, Verzögerungs-, Dauer- oder Keyframeversatz ändern.  

## <a name="overview"></a>Übersicht  

Der Microsoft Edge DevTools Animation Inspector hat zwei Hauptzwecke.  

*   Überprüfen von Animationen.  Sie möchten den Quellcode für eine Animationsgruppe verlangsamen, wiedergeben oder überprüfen.  
*   Ändern von Animationen.  Sie möchten den Zeit-, Verzögerungs-, Dauer- oder Keyframeoffset einer Animationsgruppe ändern.  Die Bearbeitung von Bézier- und Keyframes wird derzeit nicht unterstützt.  

Der Animationsinspektor unterstützt CSS-Animationen, CSS-Übergänge und Webanimationen.  `requestAnimationFrame` Animationen werden derzeit nicht unterstützt.  

### <a name="what-is-an-animation-group"></a>Was ist eine Animationsgruppe?  

Eine Animationsgruppe ist eine Gruppe von Animationen, die miteinander in Zusammenhang stehen können.  Derzeit verfügt das Web nicht über ein echtes Konzept einer Gruppenanimation, daher müssen Bewegungsdesigner und Entwickler einzelne Animationen verfassen und zeitigen, sodass die Animationen als ein zusammenhängender visueller Effekt gerendert werden.  Der Animationsinspektor prognostiziert, welche Animationen basierend auf der Startzeit \(ohne Verzögerungen und so weiter\) verknüpft sind.  Der Animationsinspektor gruppen die Animationen auch nebeneinander.  
Anders ausgedrückt: Eine Reihe von Animationen, die alle im gleichen Skriptblock ausgelöst werden, werden zusammen gruppieren.  Wenn eine Animation asynchron ist, wird sie in einer separaten Gruppe platziert.  

## <a name="get-started"></a>Erste Schritte  

Es gibt zwei Möglichkeiten, den Animationsinspektor zu öffnen:  

*   Öffnen Sie **das Menü Anpassen und Steuern von DevTools**  
    1.  Navigieren Sie zum **Untermenü Weitere** Tools.  
    1.  Wählen Sie **Animationen**aus:  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animationen mithilfe des Hauptmenüs" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Animationen** mithilfe des Hauptmenüs  
    :::image-end:::  
        
*   Öffnen des **Befehlsmenüs**  
    1.  Geben Sie `Drawer: Show Animations` ein.  

Der Animationsinspektor wird neben dem **Konsolentool** geöffnet.  Da der Animationsinspektor ein Drawer-Tool ist, können Sie den Animationsinspektor aus einem beliebigen DevTools-Bereich verwenden.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Leerer Animationsinspektor" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Leerer Animationsinspektor  
:::image-end:::  

Der Animationsinspektor ist in vier Hauptabschnitte \(oder Bereiche\) unterteilt.  Dieses Handbuch bezieht sich wie folgt auf jeden Bereich:  

| Index | Bereich | Beschreibung |  
|:--- |:--- |:--- |  
| 1 | **Steuerelemente** | Hier können Sie alle aktuell erfassten Animationsgruppen löschen oder die Geschwindigkeit der aktuell ausgewählten Animationsgruppe ändern. |  
| 2 | **Übersicht** | Wählen Sie hier eine Animationsgruppe aus, um sie im Detailbereich zu überprüfen **und zu** ändern. |  
| 3 | **Zeitachse** | Unterbrechen Und starten Sie eine Animation von hier aus, oder springen Sie zu einem bestimmten Punkt in der Animation. |  
| 4 | **Details** | Überprüfen und ändern Sie die aktuell ausgewählte Animationsgruppe. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Animationsinspektor mit Anmerkungen" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Animationsinspektor mit Anmerkungen  
:::image-end:::  

Führen Sie zum Erfassen einer Animation einfach die Interaktion aus, die die Animation auslöst, während der Animationsinspektor geöffnet ist.  Wenn eine Animation beim Laden der Seite ausgelöst wird, aktualisieren Sie die Seite, wenn der Animationsinspektor geöffnet ist, um die Animation zu erkennen.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a>Überprüfen von Animationen  

Nachdem Sie eine Animation erfasst haben, gibt es einige Möglichkeiten, sie wieder zu wiedergeben:  

*   Zeigen Sie auf die Miniaturansicht **im** Bereich Übersicht, um eine Vorschau anzuzeigen.  
*   Wählen Sie die **** Animationsgruppe im Bereich Übersicht \(so, dass sie im **Detailbereich** angezeigt wird\) aus, und wählen Sie das Wiedergabesymbol **\(** ![ Wiedergabesymbol ](../media/replay-button-icon.msft.png) \) aus.  Die Animation wird im Viewport wiedergegeben.  Wählen Sie **die Symbole für animationsgeschwindigkeit** \( Animationsgeschwindigkeit \) aus, um die Vorschaugeschwindigkeit der aktuell ausgewählten ![ ](../media/animation-speed-buttons-icon.msft.png) Animationsgruppe zu ändern.  Sie können die rote vertikale Leiste verwenden, um Ihre aktuelle Position zu ändern.  
*   Wählen Sie die rote vertikale Leiste aus, und ziehen Sie sie, um die Viewportanimation zu bereinigungen.  
    
### <a name="view-animation-details"></a>Anzeigen von Animationsdetails  

Nachdem Sie eine Animationsgruppe erfasst haben, wählen Sie sie im Bereich **Übersicht** aus, um die Details anzuzeigen.  Im **Detailbereich** wird jeder einzelnen Animation die Zeile zugewiesen.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Details zur Animationsgruppe" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Details zur Animationsgruppe  
:::image-end:::  

Zeigen Sie auf eine Animation, um sie im Viewport zu markieren.  Wählen Sie die Animation aus, um sie im **Elementtool auszuwählen.**  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Zeigen Sie auf die Animation, um sie im Viewport zu markieren." lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Zeigen Sie auf die Animation, um sie im Viewport zu markieren.  
:::image-end:::  

Der ganz links, dunklere Abschnitt einer Animation ist die Definition.  Der rechte, verblasste Abschnitt stellt Iterationen dar.  In der folgenden Abbildung stellen die Abschnitte 2 und 3 beispielsweise Iterationen von Abschnitt 1 dar.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagramm von Animationsiterationen" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Diagramm von Animationsiterationen  
:::image-end:::  

Wenn zwei Elemente die gleiche Animation angewendet haben, weist der Animationsinspektor den Elementen dieselbe Farbe zu.  Die Farbe ist zufällig und hat keine Bedeutung.  In der folgenden Abbildung werden z. B. die beiden Elemente mit derselben Animation `div.cwccw.earlier` `div.cwccw.later` \( \) angewendet, wie die `spinrightleft` `div.ccwcw.earlier` elemente `div.ccwcw.later` and.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Farbcodete Animationen" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Farbcodete Animationen  
:::image-end:::  

## <a name="modify-animations"></a>Ändern von Animationen  

Es gibt drei Möglichkeiten, eine Animation mit dem Animationsinspektor zu ändern.  

*   Animationsdauer.  
*   Keyframe-Timings.  
*   Startzeitverzögerung.  
    
In der folgenden Abbildung wird die ursprüngliche Animation dargestellt.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Originalanimation vor Änderung" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Originalanimation vor Änderung  
:::image-end:::  

Um die Dauer einer Animation zu ändern, wählen Sie den ersten oder letzten Kreis aus, und ziehen Sie ihn.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Geänderte Dauer" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Geänderte Dauer  
:::image-end:::  

Wenn die Animation Keyframeregeln definiert, werden diese als weiße innere Kreise dargestellt.  Wählen Sie einen dieser Elemente aus, und ziehen Sie ihn, um den Zeitpunkt des Keyframes zu ändern.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Geändertes Keyframe" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Geändertes Keyframe  
:::image-end:::  

Wenn Sie einer Animation eine Verzögerung hinzufügen möchten, wählen Sie sie aus, und ziehen Sie sie an eine beliebige Stelle mit Ausnahme der Kreise.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Geänderte Verzögerung" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Geänderte Verzögerung  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

(.. /media/animation-speed-buttons-icon.msft.png): .. /media/animation-speed-buttons-icon.msft.png  
(.. /media/replay-button-icon.msft.png): .. /media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
