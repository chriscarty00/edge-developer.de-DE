---
title: Simulieren der geräteausrichtung mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 9e8115819fa6c3209a6c82940e033113783ece0c
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607324"
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





# Simulieren der geräteausrichtung mit Microsoft Edge devtools   



So simulieren Sie unterschiedliche Geräte Ausrichtungen von Microsoft Edge devtools:  

<!--todo: update device orientation section when available -->  

1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.  
    
    > ##### Abbildung1  
    > Das Befehlsmenü  
    > ![Das Befehlsmenü][ImageCommandMenu]  
    
1.  Tippen `sensors` Sie auf **Sensoren anzeigen**und dann auf `Enter` .  Die Registerkarte **Sensoren** wird unten im devtools-Fenster geöffnet.  
1.  Wählen Sie in der Liste **Ausrichtung** eine der vordefinierten Ausrichtungen aus, beispielsweise `Portrait upside down` , oder wählen Sie **benutzerdefinierte Ausrichtung** aus, um eine exakte Ausrichtung zu gewährleisten.  
    
    > ##### Abbildung2  
    > Auswählen `Portrait upside down` aus der **Ausrichtungs** Liste  
    > ![Auswählen von "Hochformat" in der Orientierungsliste][ImageOrientationPortraitUpsideDown]  
    
    Nachdem Sie **benutzerdefinierte Ausrichtung**ausgewählt haben, `alpha` `beta` sind die Felder, und `gamma` aktiviert.  
    <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
    <!--todo: update links to alpha, beta, and gamma section when available -->  
    Sie können auch eine benutzerdefinierte Ausrichtung definieren, indem Sie das **Ausrichtungs Modell**ziehen.  Halten `Shift` Sie vor dem Ziehen gedrückt, um sich entlang der Achse zu drehen `alpha` .  
    
    > ##### Abbildung 3  
    > Das **Orientierungsmodell**  
    > ![Das Orientierungsmodell][ImageOrientationModel]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Abbildung 1: das Befehlsmenü"  
[ImageOrientationPortraitUpsideDown]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png "Abbildung 2: Auswählen von "Hochformat" in der Orientierungsliste"  
[ImageOrientationModel]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-custom.msft.png "Abbildung 3: das Orientierungsmodell"  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation \& Motion"  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
