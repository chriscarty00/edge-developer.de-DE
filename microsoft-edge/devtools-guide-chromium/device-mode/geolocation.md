---
description: Öffnen Sie das Tool Sensoren, und wählen Sie Koordinaten aus der Liste Geolocation aus.
title: Überschreiben der Geolocation mit Microsoft Edge DevTools
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

# <a name="override-geolocation-with-microsoft-edge-devtools"></a><span data-ttu-id="57f00-104">Überschreiben der Geolocation mit Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="57f00-104">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="57f00-105">Viele Websites nutzen den Benutzerspeicherort, um den Benutzern eine relevantere Benutzererfahrung zu bieten.</span><span class="sxs-lookup"><span data-stu-id="57f00-105">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="57f00-106">Beispielsweise kann eine Wetterwebsite die lokale Wettervorhersage im Bereich eines Benutzers anzeigen, nachdem der Benutzer der Website die Berechtigung zum Zugriff auf den aktuellen Benutzerstandort erteilt hat.</span><span class="sxs-lookup"><span data-stu-id="57f00-106">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="57f00-107">Wenn Sie eine Benutzeroberfläche erstellen, die sich je nach Standort des Benutzers ändert, möchten Sie wahrscheinlich sicherstellen, dass sich die Website an verschiedenen Orten auf der ganzen Welt korrekt verhält.</span><span class="sxs-lookup"><span data-stu-id="57f00-107">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="57f00-108">Führen Sie die folgenden Aktionen aus, um Ihre Geolocation in Microsoft Edge DevTools zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="57f00-108">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="57f00-109">Wählen `Control` + `Shift` + `P` Sie \(Windows, Linux\) oder `Command` + `Shift` + `P` \(macOS\) aus, um das **Befehlsmenü zu öffnen.**</span><span class="sxs-lookup"><span data-stu-id="57f00-109">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="57f00-111">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="57f00-111">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="57f00-112">Geben `sensors` Sie ein, wählen **Sie Sensoren anzeigen**aus, und wählen Sie `Enter` aus.</span><span class="sxs-lookup"><span data-stu-id="57f00-112">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="57f00-113">Das **Tool Sensoren** wird am unteren Rand des DevTools-Fensters geöffnet.</span><span class="sxs-lookup"><span data-stu-id="57f00-113">The **Sensors** tool opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="57f00-114">Wählen Sie in der **Liste Geolocation** eine der vordefinierten Städte aus, z. B. , oder wählen Sie Benutzerdefinierter Ort aus, um benutzerdefinierte Längen- und Breitenkoordinaten ein eingeben, oder wählen Sie Standort nicht verfügbar aus, um das Verhalten Ihrer Website zu zeigen, wenn der Standort des Benutzers nicht verfügbar `Tokyo` \*\*\*\* ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="57f00-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or choose **Custom location** to enter custom longitude and latitude coordinates, or choose **Location unavailable** to display how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Wählen Sie Tokio aus der Liste Geolocation aus." lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="57f00-116">Auswählen `Tokyo` aus der Liste **"Geolocation"**</span><span class="sxs-lookup"><span data-stu-id="57f00-116">Choose `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="57f00-117">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="57f00-117">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="57f00-118">Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57f00-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="57f00-119">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.</span><span class="sxs-lookup"><span data-stu-id="57f00-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="57f00-121">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="57f00-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
