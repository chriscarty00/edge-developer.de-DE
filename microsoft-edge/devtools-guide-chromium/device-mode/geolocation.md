---
description: Öffnen Sie das Tool Sensoren, und wählen Sie Koordinaten aus der Liste Geolocation aus.
title: Überschreiben der Geolocation Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 8f6ad09b2f8db110f6743aae32e16cc9b1185400
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399001"
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

# <a name="override-geolocation-with-microsoft-edge-devtools"></a>Überschreiben der Geolocation Microsoft Edge DevTools  

Viele Websites nutzen den Benutzerspeicherort, um den Benutzern eine relevantere Benutzererfahrung zu bieten.  Beispielsweise kann eine Wetterwebsite die lokale Wettervorhersage im Bereich eines Benutzers anzeigen, nachdem der Benutzer der Website die Berechtigung zum Zugriff auf den aktuellen Benutzerstandort erteilt hat.  

<!--todo: add link to user location section when available -->  

Wenn Sie eine Benutzeroberfläche erstellen, die sich je nach Standort des Benutzers ändert, möchten Sie wahrscheinlich sicherstellen, dass sich die Website an verschiedenen Orten auf der ganzen Welt korrekt verhält.  Führen Sie die folgenden Aktionen aus, um Ihre Microsoft Edge in DevTools zu überschreiben.  

1.  Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Das **Befehlsmenü**  
    :::image-end:::  
    
1.  Geben `sensors` Sie ein, wählen **Sie Sensoren anzeigen**aus, und wählen Sie `Enter` aus.  Das **Tool Sensoren** wird am unteren Rand des DevTools-Fensters geöffnet.  
1.  Wählen Sie in der **Liste Geolocation** eine der vordefinierten Städte aus, z. B. , oder wählen Sie Benutzerdefinierter Ort aus, um benutzerdefinierte Längen- und Breitenkoordinaten ein eingeben, oder wählen Sie Standort nicht verfügbar aus, um das Verhalten Ihrer Website zu zeigen, wenn der Standort des Benutzers nicht verfügbar `Tokyo` **** ist. ****  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Wählen Sie Tokio aus der Liste Geolocation aus." lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Auswählen `Tokyo` aus der Liste **"Geolocation"**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
