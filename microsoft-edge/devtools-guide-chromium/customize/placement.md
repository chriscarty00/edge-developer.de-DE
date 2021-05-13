---
description: So verschieben Sie Microsoft Edge DevTools an den unteren oder linken Rand Des Viewports oder in ein separates Fenster.
title: Ändern Microsoft Edge DevTools-Platzierung (Abdocken, Dock nach unten, Dock nach links)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3c6dbf3e4a72b793997fcbe0970c88e4bee07caf
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564364"
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
# <a name="change-microsoft-edge-devtools-placement-undock-dock-to-bottom-dock-to-left"></a>Ändern Microsoft Edge DevTools-Platzierung (Abdocken, Dock nach unten, Dock nach links)  

DevTools wird standardmäßig rechts neben dem Viewport (Fenster) angedockt.  Sie können DevTools auch am unteren oder linken Rand des Fensters andocken oder DevTools an ein separates Fenster andocken.

:::row:::
   :::column span="":::
      DevTools an der linken Seite des Fensters angedockt:
   :::column-end:::
   :::column span="":::
      DevTools am unteren Rand des Fensters angedockt:
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-right-docked.msft.png" alt-text="Wählen Sie Dock nach links aus." lightbox="../media/customize-elements-styles-right-docked.msft.png":::
         Wählen **Sie Dock nach links aus.**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-bottom-docked.msft.png" alt-text="Wählen Sie Dock to Bottom aus." lightbox="../media/customize-elements-styles-bottom-docked.msft.png":::
         Auswählen `Dock to bottom`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

DevTools werden möglicherweise an ein separates Fenster entfernt, das Sie auf einen separaten Monitor verschieben können:

:::row:::
   :::column span="":::
      Browserfenster:
   :::column-end:::
   :::column span="":::
      DevTools in einem separaten Fenster entdockt:
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png" alt-text="Browser im separaten Fenster" lightbox="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png":::
         Browser im separaten Fenster  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png" alt-text="Entdockte DevTools im separaten Fenster" lightbox="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png":::
         Entdockte DevTools im separaten Fenster  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="change-placement-from-the-main-menu"></a>Ändern der Platzierung aus dem Hauptmenü  

1.  Wählen **Sie Anpassen und Steuern von DevTools** \( \) aus, und wählen Sie Abdocken in separates Fenster `...` \( **** ![ Undock ](../media/undock-icon.msft.png) \), Dock to **bottom** \( Dock to bottom \) oder Dock ![ to ](../media/bottom-icon.msft.png) **left** \( Dock to ![ left ](../media/left-icon.msft.png) \).  
    
    :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight.msft.png" alt-text="Wählen Sie In separates Fenster abdocken aus" lightbox="../media/customize-elements-styles-options-dock-side-highlight.msft.png":::
       Wählen **Sie Abdocken in separates Fenster aus.**  
    :::image-end:::  
    
## <a name="change-placement-from-the-command-menu"></a>Ändern der Platzierung im Befehlsmenü  

1.  [Öffnen Sie das Befehlsmenü][DevtoolsCommandMenu], indem `Shift` + `Ctrl` + `P` Sie Windows/Linux oder `Command` + `Shift` + `P` unter macOS auswählen.  
1.  Geben Sie nach dem Zeichen ein, und wählen Sie dann `>` einen der folgenden Befehle `dock` aus:  
    
    *  **Dock to bottom**
    *  **Dock nach links**
    *  **Dock nach rechts**
    *  **Wiederherstellen der letzten Dockposition**
    *  **Abdocken in separates Fenster**
    
    Sie können auch über das Hauptmenü auf [die Befehle zugreifen.](#change-placement-from-the-main-menu) 
    
    :::image type="complex" source="../media/customize-elements-styles-command-menu-undo.msft.png" alt-text="Der Befehl "Abdocken"" lightbox="../media/customize-elements-styles-command-menu-undo.msft.png":::
       Der Befehl "Abdocken"  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenu]: ../command-menu/index.md "Ausführen von Befehlen mit Microsoft Edge DevTools Command | Microsoft Docs"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/customize/placement) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
