---
title: Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601346"
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





# Ändern der Platzierung von Microsoft Edge devtools (abdocken, docken an den unteren Rand, docken nach links)   



Standardmäßig ist devtools an der rechten Seite des Viewports verankert.  Sie können auch an der Unterseite andocken, an der linken Seite andocken oder das devtools in einem separaten Fenster Abdocken.  

> ##### Abbildung1  
> An Links Andocken  
> ![An Links Andocken][ImageDockLeft]  

> ##### Abbildung2  
> An den unteren Rand Andocken  
> ![An den unteren Rand Andocken][ImageDockBottom]  

> ##### Abbildung 3  
> Browser in einem separaten Fenster  
> ![Browser in einem separaten Fenster][ImageUndockBrowser]  

> ##### Abbildung4  
> Abdocken von devtools in einem separaten Fenster  
> ![Abdocken von devtools in einem separaten Fenster][ImageUndockDevTools]  

## Ändern der Platzierung aus dem Hauptmenü   

1.  Klicken Sie auf **anpassen und Steuern von devtools** , `...` und wählen Sie **Abdocken in separates Fenster** ![ Abdocken aus ][ImageUndockIcon] , **docken** Sie an die untere ![ Docking-Station an den unteren Rand an ][ImageBottomIcon] , oder **docken** ![ ][ImageLeftIcon] Sie nach links  
    
    > ##### Abbildung5  
    > Auswählen der Option **"Abdocken" in separates Fenster**  
    > ![Auswählen der Option "Abdocken" in separates Fenster][ImageUndockSettings]  
    
## Ändern der Platzierung über das Befehlsmenü   

1.  [Öffnen des Befehlsmenüs][DevtoolsCommandMenu]  
1.  Führen Sie einen der folgenden Befehle aus: `Dock To Bottom` , `Undock Into Separate Window` .  Derzeit gibt es keinen Befehl zum Andocken an Left, aber Sie können über das [Hauptmenü](#change-placement-from-the-main-menu)darauf zugreifen.  
    
    > ##### Abbildung6  
    > Befehl "Abdocken"  
    > ![Befehl "Abdocken"][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Abbildung 1: Andocken nach links"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Abbildung 2: Andocken an den unteren Rand"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Abbildung 3: Browser in einem separaten Fenster"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Abbildung 4: Abdocken von devtools in einem separaten Fenster"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Abbildung 5: Auswählen der Option "Abdocken" in separates Fenster"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Abbildung 6: Befehl "Abdocken""  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ausführen von Befehlen mit dem Befehlsmenü von Microsoft Edge devtools"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/customize/placement) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
