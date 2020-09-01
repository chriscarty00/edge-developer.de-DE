---
title: Überschreiben von Geolocation mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 1bd6da8d0e4c170fa94fed995a26e77b119992f1
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981827"
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





# Überschreiben von Geolocation mit Microsoft Edge devtools   



Viele Websites nutzen den Standort des Benutzers, um den Benutzern eine wichtigere Benutzererfahrung zu bieten.  So kann beispielsweise eine Wetter Website die lokale Prognose im Bereich eines Benutzers anzeigen, nachdem der Benutzer der Website die Berechtigung für den Zugriff auf den aktuellen Nutzerstandort erteilt hat.  

<!--todo: add link to user location section when available -->  

Wenn Sie eine Benutzeroberfläche erstellen, die je nachdem, wo sich der Benutzer befindet, geändert wird, möchten Sie wahrscheinlich sicherstellen, dass sich die Website an verschiedenen Orten auf der ganzen Welt korrekt verhält.  Führen Sie die folgenden Aktionen aus, um Ihre Geoposition in Microsoft Edge devtools zu überschreiben.  

1.  Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Tippen `sensors` Sie auf **Sensoren anzeigen**und dann auf `Enter` .  Die Registerkarte **Sensoren** wird unten im devtools-Fenster geöffnet.  
1.  Wählen Sie in der Liste **Geolocation** eine der voreingestellten Städte aus, `Tokyo` oder wählen Sie **benutzerdefinierter Speicherort** aus, um benutzerdefinierte Längen-und Breitengradkoordinaten einzugeben, oder wählen Sie nicht **verfügbarer Speicherort** aus, um zu sehen, wie sich die Website verhält, wenn der Standort des Benutzers nicht verfügbar ist.  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Wählen Sie in der Liste Geolocation den Eintrag Tokyo aus." lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Wählen Sie `Tokyo` aus der Liste **Geolocation** aus.  
    :::image-end:::  
    
<!--  
## Feedback   

  
-->  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
