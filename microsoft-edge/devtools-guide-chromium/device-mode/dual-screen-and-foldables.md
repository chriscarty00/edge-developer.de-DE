---
description: Verwenden Sie virtuelle Geräte in Microsoft Edge, um Ihre Website für Dualbildschirme und ausklappbare Geräte zu verbessern.
title: Emulieren von Dualbildschirmen und ausklappbaren Geräten in Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, f12-Tools, DevTools, Emulation, Gerät, Simulation, mobil, Dual-Screen, ausklappbar, Surface Duo, Samsung Unterdruck Fold
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313239"
---
# Emulieren von Dualbildschirmen und ausklappbaren Geräten in Microsoft Edge DevTools  

In Microsoft Edge, Version 89 oder höher, können Sie die folgenden Dualbildschirme und ausklappbaren Geräte emulieren.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Verknappung][SamsungMobileGalaxyFold]  
    
Emulieren Sie die Geräte, und schalten Sie zwischen den folgenden Haltungen um.  

*   Einzelbildschirm oder geklappte Haltung  
*   Dualbildschirm oder aufgefunktioniertes Bild  
    
Aktivieren Sie [experimentelle Webplattform-APIs,](#turn-on-experimental-apis) und verwenden Sie die [CSS-Medienbildschirm-übergreifende][DualScreenDocsCssMedia] Funktion und [javaScript getWindowSegments-API,][DualScreenDocsJSAPI] um Ihre Website \(oder App\) für Dualbildschirme und ausklappbare Geräte zu verbessern.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emulieren von Surface Duo in Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Emulieren von Surface Duo in Microsoft Edge  
:::image-end:::  

## Aktivieren experimenteller APIs  

Aktivieren Sie das Flag in Microsoft Edge, um das Feature für den Bildschirmbereich von [CSS-Medien][DualScreenDocsCssMedia] und die [JavaScript-getWindowSegments-API][DualScreenDocsJSAPI] `Experimental Web Platform features` zu verwenden.  Führen Sie die folgenden Schritte aus.  

1.  Navigieren Sie zu `edge://flags` .  
1.  Geben Sie **im Textfeld "Suchkennzeichen"** die Option `Experimental Web Platform features` **"Experimentelle Webplattform-Features"** ein, und ändern Sie **"Deaktiviert"** in **"Aktiviert".**  
1.  Starten Sie Microsoft Edge neu.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Aktivieren der Kennzeichnung für experimentelle Webplattformfeatures" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Aktivieren der **Kennzeichnung für experimentelle Webplattformfeatures**  
:::image-end:::  

> [!NOTE]
> Wenn Sie CSS-Medienabfragen oder die [JavaScript-Windows-Segment-Enumerations-API][DualScreenDocsJSAPI] verwenden, um Ihre Website oder App für [Surface Duo][SurfaceDevicesDuo]zu verbessern, müssen Sie auch das Flag **"Experimentelle WebPlattform-Features"** in der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf Ihrem [Surface Duo-Gerät][SurfaceDevicesDuo] aktivieren. [][DualScreenDocsCssMedia]  
> 
> Wenn das Flag für experimentelle Webplattformfeatures im Microsoft [Edge][MicrosoftEdge] Desktop aktiviert und in der [Android Microsoft][GooglePlayMicrosoftEdge]Edge-App deaktiviert ist, ist das Verhalten Ihrer Website oder App im Surface Duo-Emulator im Desktop von Microsoft Edge nicht mit der [Android Microsoft Edge-App][GooglePlayMicrosoftEdge] auf [Surface Duo kompatibel.][SurfaceDevicesDuo] ****  Stellen Sie sicher, dass die Flags in Android- und Desktop-Microsoft Edge übereinstimmen, um den Surface Duo-Emulator im Microsoft Edge [Desktop erfolgreich zu verwenden.][MicrosoftEdge]  

## Testen auf ausklappbaren und Dualbildschirmgeräten  

Wenn Sie das [Surface Duo][SurfaceDevicesDuo] in einem dualen Bildschirm in Microsoft Edge emulieren, wird die Naht \(der Abstand zwischen den beiden Bildschirmen\) über Ihrer Website oder App gezeichnet.  

Die emulierte Anzeige entspricht der Art und Weise, wie Ihre Website \(oder App\) in der [Microsoft Edge -Android-App][GooglePlayMicrosoftEdge] gerendert wird, während sie auf [Surface Duo ausgeführt wird.][SurfaceDevicesDuo]  Möglicherweise müssen Sie Ihre Website \(oder App\) aktualisieren, damit sie am Nahtstrich besser angezeigt wird.  Weitere Informationen zum Anpassen Ihrer Website \(oder app\) an die Naht finden Sie unter "Arbeiten mit [der Naht".][DualScreenIntroductionHowWorkSeam]  

Die [Gerätesymbolleiste][DevtoolsDeviceModeIndexSimulateMobileViewport] bietet zusätzliche Features, mit deren Hilfe Sie Ihre Website oder App in mehreren Haltungen und Ausrichtungen testen können.  Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation. Kombinieren Sie das Feature mit **Span** \( Span \), um zwischen einem einzelnen Bildschirm oder gefalteten und dualen Bildschirmen oder aufgeklappten ![ ](../media/span-dark-icon.msft.png) Postures umschalten zu können.  Zusammen können Sie mit den Features Ihre Website oder App in allen vier möglichen Haltungen und Ausrichtungen testen.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrix der Haltungen und Ausrichtungen für Dualbildschirme und ausklappbare Geräte" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matrix der Haltungen und Ausrichtungen für Dualbildschirme und ausklappbare Geräte  
:::image-end:::  

Das **Symbol für experimentelle Webplattformfeatures** \( ExperimentalApis \) zeigt den Status des Features der ![ ](../media/experimental-apis-dark-icon.msft.png) **experimentellen Webplattform** an.  Wenn das Flag aktiviert ist, wird das Symbol hervorgehoben.  Wenn das Flag deaktiviert ist, wird das Symbol nicht hervorgehoben.  Um das Flag zu aktivieren (oder zu deaktivieren), wählen Sie entweder das Symbol aus, oder navigieren Sie zu dem Flag, und schalten `edge://flags` Sie es um.  

> [!NOTE]
> Im Folgenden finden Sie eine Liste der aktuellen bekannten Probleme.  
> 
> *   Wenn Sie einen [Microsoft Remote Desktop Client][RemoteDesktopClientDocs] verwenden, um eine Verbindung mit einem Remote-PC herzustellen und das Surface [Duo][SurfaceDevicesDuo] oder [Das Unterflag von Samsung zu][SamsungMobileGalaxyFold]emulieren, kann der Zeiger wackeln oder unübersichtlich werden.  Wenn das Problem vor sich geht, senden [Sie Feedback.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Weitere Ressourcen  

Hier finden Sie weitere Ressourcen, die Sie bei der Verbesserung Ihrer Website \(oder App\) für Dual-Screen-Geräte unterstützen können.  

*   Weitere Informationen zur Webentwicklung auf Dual-Screen-Geräten finden Sie unter ["Dual-screen web experiences".][DualScreenWebIndex]  
*   Installieren Sie den [Surface Duo-Emulator.][DualScreenAndroidUseEmulator]  Der Surface Duo Emulator ist anders als der Emulator in Microsoft Edge, führt Android aus und kann in [Android Studio integriert werden.][AndroidDeveloperStudio]  Weitere Informationen finden Sie unter ["Surface Duo SDK erhalten".][DualScreenAndroidGetDuoSdk]  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simulieren mobiler Geräte mit dem Gerätemodus in Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Weberfahrungen auf zwei | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Surface Duo-Emulator-| Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "So arbeiten Sie mit der Naht – Einführung in duale Bildschirmgeräte | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Verwenden der Surface Duo-Emulator-| Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Feature für bildschirmübergreifende CSS-Medien für die Erkennung von | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "Die getWindowSegments-JavaScript-API für Dualbildschirmgeräte | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Remotedesktopclients | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "1-1-| Samsung"  
