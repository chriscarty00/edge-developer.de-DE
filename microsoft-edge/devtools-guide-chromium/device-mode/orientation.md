---
title: Simulieren der geräteausrichtung mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: e11af27681f3aa1aaeefb62505908fdc6cd7a0e9
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986150"
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

# <span data-ttu-id="fc64a-103">Simulieren der geräteausrichtung mit Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="fc64a-103">Simulate device orientation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="fc64a-104">Führen Sie die folgenden Aktionen aus, um unterschiedliche Geräte Ausrichtungen von Microsoft Edge devtools zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="fc64a-104">Complete the following actions to simulate different device orientations from Microsoft Edge DevTools.</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="fc64a-105">Drücken Sie `Control` + `Shift` + `P` \ (Windows \) oder `Command` + `Shift` + `P` \ (macOS \), um das **Befehlsmenü**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc64a-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Das Befehlsmenü" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="fc64a-107">Das **Befehlsmenü**</span><span class="sxs-lookup"><span data-stu-id="fc64a-107">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="fc64a-108">Tippen `sensors` Sie auf **Sensoren anzeigen**und dann auf `Enter` .</span><span class="sxs-lookup"><span data-stu-id="fc64a-108">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="fc64a-109">Die Registerkarte **Sensoren** wird unten im devtools-Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc64a-109">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="fc64a-110">Wählen Sie in der Liste **Ausrichtung** eine der vordefinierten Ausrichtungen aus, beispielsweise `Portrait upside down` , oder wählen Sie **benutzerdefinierte Ausrichtung** aus, um eine exakte Ausrichtung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="fc64a-110">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or select **Custom orientation** to provide your own exact orientation.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Auswählen von "Hochformat" in der Orientierungsliste" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             <span data-ttu-id="fc64a-112">Auswählen `Portrait upside down` aus der **Ausrichtungs** Liste</span><span class="sxs-lookup"><span data-stu-id="fc64a-112">Select `Portrait upside down` from the **Orientation** list</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="fc64a-113">Nachdem Sie **benutzerdefinierte Ausrichtung**ausgewählt haben `alpha` , `beta` sind die Felder, und `gamma` aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fc64a-113">After you select **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
          <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how each axis works.  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          <span data-ttu-id="fc64a-114">Sie können auch eine benutzerdefinierte Ausrichtung definieren, indem Sie das **Ausrichtungs Modell**ziehen.</span><span class="sxs-lookup"><span data-stu-id="fc64a-114">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="fc64a-115">Halten `Shift` Sie vor dem Ziehen gedrückt, um sich entlang der Achse zu drehen `alpha` .</span><span class="sxs-lookup"><span data-stu-id="fc64a-115">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Das Orientierungsmodell" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             <span data-ttu-id="fc64a-117">Das **Orientierungsmodell**</span><span class="sxs-lookup"><span data-stu-id="fc64a-117">The **Orientation Model**</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="fc64a-118">Kontakt mit dem Microsoft Edge devtools-Team</span><span class="sxs-lookup"><span data-stu-id="fc64a-118">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> <span data-ttu-id="fc64a-119">Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc64a-119">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fc64a-120">Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc64a-120">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
<span data-ttu-id="fc64a-122">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fc64a-122">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
