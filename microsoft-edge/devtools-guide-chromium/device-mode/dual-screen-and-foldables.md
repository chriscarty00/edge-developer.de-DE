---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge, um Ihre Website für Dualscreen- und faltbare Geräte zu verbessern.
title: Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, emulation, device, simulation, mobile, dual-screen, foldable, Surface Duo, Samsung Galaxy Fold
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313239"
---
# Emulieren von Dualscreen- und faltbaren Geräten in Microsoft Edge DevTools  

In Microsoft Edge, Version 89 oder höher, können Sie die folgenden Dualscreen- und faltbaren Geräte emulieren.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  
    
Emulieren Sie die Geräte, und schalten Sie zwischen den folgenden Haltungen um.  

*   Einzelbildschirm- oder geklappte Haltung  
*   Dual-Screen- oder ungefalte Haltung  
    
Aktivieren Sie [experimentelle Webplattform-APIs,](#turn-on-experimental-apis) und verwenden Sie die [CSS-Medienbildschirm-Spannfunktion][DualScreenDocsCssMedia] und die [JavaScript getWindowSegments-API,][DualScreenDocsJSAPI] um Ihre Website \(oder App\) für Dualscreen- und faltbare Geräte zu verbessern.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emulieren von Surface Duo in Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Emulieren von Surface Duo in Microsoft Edge  
:::image-end:::  

## Aktivieren von experimentellen APIs  

Aktivieren Sie das Flag in Microsoft Edge, um das Feature für die Verwendung des [CSS-Medienbildschirms][DualScreenDocsCssMedia] und der [JavaScript getWindowSegments-API][DualScreenDocsJSAPI] `Experimental Web Platform features` zu verwenden.  Führen Sie die folgenden Schritte aus.  

1.  Navigieren Sie zu `edge://flags`.  
1.  Geben Sie **im Textfeld Suchkennzeichen** die Option Ein, wählen Sie das `Experimental Web Platform features` Kennzeichen Experimentelle **Webplattformfeatures** aus, und ändern Sie **Deaktiviert** in **Aktiviert**.  
1.  Starten Sie Microsoft Edge neu.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Aktivieren des Kennzeichens für Experimentelle Webplattformfeatures" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Aktivieren des **Kennzeichens für Experimentelle Webplattformfeatures**  
:::image-end:::  

> [!NOTE]
> Wenn Sie CSS-Medienabfragen oder die [JavaScript-Windows-Segment-Enumerations-API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für [Surface Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Flag für experimentelle Webplattformfeatures in der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf Ihrem [Surface Duo-Gerät][SurfaceDevicesDuo] aktivieren. [][DualScreenDocsCssMedia] ****  
> 
> Wenn das **Flag** für experimentelle Webplattformfeatures im [Microsoft Edge-Desktop][MicrosoftEdge] aktiviert und in der Android [Microsoft Edge-App][GooglePlayMicrosoftEdge]deaktiviert ist, ist das Verhalten Ihrer Website oder App im Surface Duo-Emulator im Desktop von Microsoft Edge nicht mit der Android [Microsoft Edge-App][GooglePlayMicrosoftEdge] auf Surface [Duo kompatibel.][SurfaceDevicesDuo]  Stellen Sie sicher, dass die Flags für Android und Desktop Microsoft Edge übereinstimmen, um den Surface Duo-Emulator in Microsoft [Edge erfolgreich zu verwenden.][MicrosoftEdge]  

## Testen auf zusammenklappbaren Und Dualscreen-Geräten  

Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einer Dual-Screen-Haltung in Microsoft Edge emulieren, wird die Naht \(der Abstand zwischen den beiden Bildschirmen\) über Ihre Website oder App gezeichnet.  

Die emulierte Anzeige entspricht der Art und Weise, wie Ihre Website \(oder App\) während der Ausführung auf Surface Duo in der [Microsoft Edge Android-App][GooglePlayMicrosoftEdge] [gerendert wird.][SurfaceDevicesDuo]  Möglicherweise müssen Sie Ihre Website \(oder App\) aktualisieren, um entlang der Naht besser angezeigt zu werden.  Weitere Informationen zum Anpassen Ihrer Website \(oder App\) an die Naht finden Sie unter [How to work with the seam][DualScreenIntroductionHowWorkSeam].  

Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] verfügt über zusätzliche Features, mit deren Hilfe Sie Ihre Website oder App in mehreren Haltungen und Ausrichtungen testen können.  Wählen **Sie Drehen** \( Drehen ![ ](../media/rotate-dark-icon.msft.png) \) aus, um den Ansichtsfenster in die Querformatausrichtung zu drehen. Kombinieren Sie das Feature mit **Span** \( Span \), um zwischen einem bildschirm- oder gefalteten und dualen Bildschirm oder aufgeklappten Haltungen ![ ](../media/span-dark-icon.msft.png) umschalten zu können.  Mit den Features können Sie Ihre Website oder App in allen vier möglichen Haltungen und Ausrichtungen testen.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrix von Haltungen und Ausrichtungen für Dualscreen- und faltbare Geräte" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matrix von Haltungen und Ausrichtungen für Dualscreen- und faltbare Geräte  
:::image-end:::  

Das **Symbol Experimental Web Platform features** \( ExperimentalApis \) zeigt den Status des ![ ](../media/experimental-apis-dark-icon.msft.png) **Features-Flag der Experimentellen Webplattform** an.  Wenn das Flag aktiviert ist, wird das Symbol hervorgehoben.  Wenn das Flag deaktiviert ist, wird das Symbol nicht hervorgehoben.  Um das Flag \(oder off\) zu aktivieren, wählen Sie entweder das Symbol aus, oder navigieren Sie zu und schalten `edge://flags` Sie das Flag um.  

> [!NOTE]
> Im Folgenden finden Sie eine Liste der aktuellen bekannten Probleme.  
> 
> *   Wenn Sie einen [Microsoft Remote Desktop-Client][RemoteDesktopClientDocs] verwenden, um eine Verbindung mit einem Remote-PC herzustellen und das [Surface Duo][SurfaceDevicesDuo] oder das [Samsung -Galaxis-Fold-Gerät][SamsungMobileGalaxyFold]zu emulieren, kann der Zeiger wackeln oder stottern.  Wenn Sie das Problem haben, senden [Sie Feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Weitere Ressourcen  

Hier finden Sie weitere Ressourcen, die Ihnen bei der Verbesserung Ihrer Website \(oder App\) für Dual-Screen-Geräte helfen können.  

*   Weitere Informationen zur Webentwicklung auf Dual-Screen-Geräten finden Sie unter [Dual-screen web experiences][DualScreenWebIndex].  
*   Installieren Sie den [Surface Duo-Emulator][DualScreenAndroidUseEmulator].  Der Surface Duo-Emulator ist anders als der Emulator in Microsoft Edge, führt Android aus und integriert sich in [Android Studio.][AndroidDeveloperStudio]  Weitere Informationen finden Sie unter [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Dualscreen-Weberfahrungen | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Laden Sie den Surface Duo-Emulator | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Arbeiten mit der Naht – Einführung in Geräten mit dualem Bildschirm | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden des Surface Duo-Emulators | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Feature „CSS-Medienbildschirmaufteilung“ für die Erkennung von dualem Bildschirm | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die API „getWindowSegments JavaScript“ für Geräte mit dualem Bildschirm | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remotedesktopclients | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxis fold | Samsung"  
