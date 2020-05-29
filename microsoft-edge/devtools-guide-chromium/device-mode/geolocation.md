---
title: Überschreiben von Geolocation mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools
ms.openlocfilehash: 307064bedf992e528b6d79eed3a2ade3367830d4
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607440"
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





# <span data-ttu-id="4b164-103">Überschreiben von Geolocation mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="4b164-103">Override Geolocation With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="4b164-104">Viele Websites nutzen den Standort des Benutzers, um den Benutzern eine wichtigere Benutzererfahrung zu bieten.</span><span class="sxs-lookup"><span data-stu-id="4b164-104">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="4b164-105">So kann beispielsweise eine Wetter Website die lokale Prognose im Bereich eines Benutzers anzeigen, nachdem der Benutzer der Website die Berechtigung für den Zugriff auf den aktuellen Nutzerstandort erteilt hat.</span><span class="sxs-lookup"><span data-stu-id="4b164-105">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="4b164-106">Wenn Sie eine Benutzeroberfläche erstellen, die je nachdem, wo sich der Benutzer befindet, geändert wird, möchten Sie wahrscheinlich sicherstellen, dass sich die Website an verschiedenen Orten auf der ganzen Welt korrekt verhält.</span><span class="sxs-lookup"><span data-stu-id="4b164-106">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="4b164-107">So überschreiben Sie Ihre Geolokation in Microsoft Edge devtools:</span><span class="sxs-lookup"><span data-stu-id="4b164-107">To override your geolocation in Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="4b164-108">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4b164-108">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="4b164-109">Abbildung1</span><span class="sxs-lookup"><span data-stu-id="4b164-109">Figure 1</span></span>  
    > <span data-ttu-id="4b164-110">Das Befehlsmenü</span><span class="sxs-lookup"><span data-stu-id="4b164-110">The Command Menu</span></span>  
    > ![Das Befehlsmenü][ImageCommandMenu]  
    
1.  <span data-ttu-id="4b164-112">Tippen `sensors` Sie auf **Sensoren anzeigen**und dann auf `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4b164-112">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="4b164-113">Die Registerkarte **Sensoren** wird unten im devtools-Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4b164-113">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="4b164-114">Wählen Sie in der Liste **Geolocation** eine der voreingestellten Städte aus, `Tokyo` oder wählen Sie **benutzerdefinierter Speicherort** aus, um benutzerdefinierte Längen-und Breitengradkoordinaten einzugeben, oder wählen Sie nicht **verfügbarer Speicherort** aus, um zu sehen, wie sich die Website verhält, wenn der Standort des Benutzers nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4b164-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or select **Custom location** to enter custom longitude and latitude coordinates, or select **Location unavailable** to see how your site behaves when the user's location is not available.</span></span>  
    
    > ##### <span data-ttu-id="4b164-115">Abbildung2</span><span class="sxs-lookup"><span data-stu-id="4b164-115">Figure 2</span></span>  
    > <span data-ttu-id="4b164-116">Auswählen `Tokyo` aus der Liste **Geolocation**</span><span class="sxs-lookup"><span data-stu-id="4b164-116">Selecting `Tokyo` from the **Geolocation** list</span></span>  
    > ![Auswählen von Tokyo in der Liste geolocation][ImageGeolocationTokyo]  
    
<!--## Feedback   

  -->  

<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Abbildung 1: das Befehlsmenü"  
[ImageGeolocationTokyo]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-geolocation-tokyo.msft.png "Abbildung 2: Auswählen von Tokyo aus der Liste geolocation"  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="4b164-120">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b164-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4b164-121">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b164-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="4b164-123">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4b164-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
