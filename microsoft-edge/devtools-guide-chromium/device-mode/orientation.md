---
description: Öffnen Sie das Tool Sensoren, und navigieren Sie zum Abschnitt Ausrichtung.
title: Simulieren der Geräteausrichtung mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 754df3b271b44f986802c2847862624f6a8b5bd9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398714"
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

# <a name="simulate-device-orientation-with-microsoft-edge-devtools"></a>Simulieren der Geräteausrichtung mit Microsoft Edge DevTools  

Führen Sie die folgenden Aktionen aus, um verschiedene Geräteausrichtungen von devTools Microsoft Edge zu simulieren.  

<!--todo: update device orientation section when available -->  

1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `sensors` Sie ein, wählen **Sie Sensoren anzeigen**aus, und wählen Sie `Enter` aus.  Das **Tool Sensoren** wird am unteren Rand des DevTools-Fensters geöffnet.  
1.  Wählen Sie in der **Liste** Ausrichtung eine der voreingestellten Ausrichtungen aus, z. B. , oder wählen Sie Benutzerdefinierte Ausrichtung aus, um Eine `Portrait upside down` eigene genaue Ausrichtung zu bieten. ****  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Wählen Sie in der Liste Ausrichtung kopfüber Hochformat aus." lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             Auswählen `Portrait upside down` aus der Liste **Ausrichtung**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Nachdem Sie **benutzerdefinierte Ausrichtung auswählen,** werden `alpha` die Felder , und `beta` `gamma` aktiviert.  
          <!--To understand how each axis works, navigate to [Alpha][alpha], [Beta][beta], and [Gamma][gamma].  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          Sie können auch eine benutzerdefinierte Ausrichtung festlegen, indem Sie das **Ausrichtungsmodell ziehen.**  Halten `Shift` Sie vor dem Ziehen gedrückt, um die Achse entlang zu `alpha` drehen.  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Das Ausrichtungsmodell" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             Das **Ausrichtungsmodell**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
