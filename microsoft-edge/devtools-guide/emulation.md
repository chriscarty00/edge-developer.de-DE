---
description: Verwenden des Emulations Panels zum Testen unterschiedlicher Browser Profile, Bildschirmgrößen und Auflösungen sowie GPS-Positionskoordinaten
title: DevTools-Emulation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Geräteemulation, reaktionsfähiges Design, Geolocation, Auflösung
ms.custom: seodec18
ms.openlocfilehash: 6eaa8d79cfd64473dcc52beff5659b39054e2a48
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104847"
---
# <span data-ttu-id="d2ad2-104">Emulation</span><span class="sxs-lookup"><span data-stu-id="d2ad2-104">Emulation</span></span>  

> [!NOTE]
> <span data-ttu-id="d2ad2-105">Der neue Microsoft Edge basiert auf Chromium, und beginnt mit Version 75.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-105">The new Microsoft Edge is built using Chromium, and starts at version 75.</span></span>  <span data-ttu-id="d2ad2-106">Wenn Sie weitere Informationen wünschen, [Laden Sie den neuen Microsoft Edge herunter][MicrosoftNewEdge], und probieren Sie die neuen [Microsoft Edge (Chrom)-Entwickler Tools][DevtoolsGuideChromium]aus.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-106">For more information, [download the new Microsoft Edge][MicrosoftNewEdge], and try out the new [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromium].</span></span>  
> 
> <span data-ttu-id="d2ad2-107">Wenn Sie unterschiedliche Geräte, Browser, Bildschirmgrößen und Auflösungen im neuen devtools emulieren möchten, navigieren Sie zum [emulieren mobiler Geräte in Microsoft Edge \ (Chrom \) devtools][DevtoolsGuideChromiumDeviceMode].</span><span class="sxs-lookup"><span data-stu-id="d2ad2-107">To emulate different devices, browsers, screen sizes, and resolutions in the new DevTools, navigate to [Emulate Mobile Devices in Microsoft Edge \(Chromium\) DevTools][DevtoolsGuideChromiumDeviceMode].</span></span>  

<span data-ttu-id="d2ad2-108">Das **Emulations** Panel hilft bei den folgenden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-108">The **Emulation** panel helps with the following activities.</span></span>    

*   <span data-ttu-id="d2ad2-109">Simulieren verschiedener [Geräteprofile](#device), [Browser](#browser-profile)und [Bildschirmgrößen und-Auflösungen](#display)</span><span class="sxs-lookup"><span data-stu-id="d2ad2-109">Simulate various [device profiles](#device), [browsers](#browser-profile), and [screen sizes and resolutions](#display)</span></span>  
*   <span data-ttu-id="d2ad2-110">Testen verschiedener [Geolocation-Einstellungen und-Koordinaten](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="d2ad2-110">Test different [geolocation settings and coordinates](#geolocation)</span></span>  

:::image type="complex" source="./media/emulation.png" alt-text="Das Microsoft Edge devtools-Emulations Panel" lightbox="./media/emulation.png":::
   <span data-ttu-id="d2ad2-112">Das Microsoft Edge devtools- **Emulations** Panel</span><span class="sxs-lookup"><span data-stu-id="d2ad2-112">The Microsoft Edge DevTools **Emulation** panel</span></span>  
:::image-end:::  

1.  <span data-ttu-id="d2ad2-113">Die Schaltfläche für die **Beibehaltung der Emulationseinstellungen** speichert alle von Ihnen vorgenommenen Änderungen an den Standardeinstellungen für die Desktop Emulation, auch wenn Sie das devtools schließen und erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-113">The **Persist Emulation settings** button saves any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span>  

1.  <span data-ttu-id="d2ad2-114">Mit der Schaltfläche " **Emulationseinstellungen zurücksetzen** " werden Ihre Emulationseinstellungen wieder auf das standardmäßige Desktop Browserprofil und die Microsoft Edge-Benutzer-Agent-Zeichenfolge zurückgesetzt, wobei GPS deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-114">The **Reset Emulation settings** button resets your emulation settings back to the default Desktop browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>  

1.  <span data-ttu-id="d2ad2-115">Wenn eine dieser Optionen von der Standardeinstellung geändert wird, wird auf der Registerkarte **Emulation** eine Informationswarnung angezeigt, die darauf hinweist, dass einige Aspekte des Verhaltens Ihres Browsers emuliert werden.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-115">When any of these options are changed from the default, the **Emulation** tab displays an informational alert to indicate that some aspect of the behavior of your browser is being emulated.</span></span>  

## <span data-ttu-id="d2ad2-116">Gerät</span><span class="sxs-lookup"><span data-stu-id="d2ad2-116">Device</span></span>  

<span data-ttu-id="d2ad2-117">Wählen Sie aus einer vordefinierten Liste von Windows-Geräteprofilen aus, die die anderen Emulationsoptionen automatisch konfigurieren oder Ihre eigene **benutzerdefinierte** Konfiguration angeben.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-117">Pick from a preset list of Windows device profiles that automatically configure the other emulation options or specify your own **Custom** configuration.</span></span>  <span data-ttu-id="d2ad2-118">Wechseln Sie zurück zu **Standard** , um alle Emulations Tools zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-118">Switch back to **Default** to reset all the emulation tools.</span></span>  

## <span data-ttu-id="d2ad2-119">Modus</span><span class="sxs-lookup"><span data-stu-id="d2ad2-119">Mode</span></span>  

### <span data-ttu-id="d2ad2-120">Browser Profil</span><span class="sxs-lookup"><span data-stu-id="d2ad2-120">Browser profile</span></span>  

<span data-ttu-id="d2ad2-121">Eine schnelle Möglichkeit zum Simulieren der auf einem Windows Phone-Gerät ausgeführten Seite besteht darin, die **Browser Profil** Einstellung auf **Windows Phone**zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-121">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to **Windows Phone**.</span></span>  

#### <span data-ttu-id="d2ad2-122">Benutzer-Agent-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d2ad2-122">User agent string</span></span>  

<span data-ttu-id="d2ad2-123">Das Ändern der Zeichenfolge des Benutzer-Agents, um einen anderen Browser zu imitieren, ist ein guter erster Schritt beim Debuggen von Fehlern, die nur in Microsoft Edge stattfinden.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-123">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span>  

<span data-ttu-id="d2ad2-124">Skripts verwenden die Zeichenfolge des Benutzer-Agents, um festzustellen, welcher Browser verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-124">Scripts use the user agent string to detect which browser is used.</span></span>  <span data-ttu-id="d2ad2-125">Das Skript kann Front-End-, Back-End-oder Front-End-und Back-End-Daten sein.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-125">Script may be front-end, back-end, or front-end and back-end.</span></span>  <span data-ttu-id="d2ad2-126">Obwohl Ihr Code keine Browsererkennung verwendet, kann der Code ihn von einer JavaScript-Bibliothek eines Drittanbieters oder von einem serverseitigen Skript erben.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-126">Although your code does not use browser detection, your code may inherit it from a third-party JavaScript library or server-side script.</span></span>  

<span data-ttu-id="d2ad2-127">Das Problem bei der Browsererkennung besteht darin, dass Sie Funktionen in Ihrer Webseite mithilfe von Annahmen zu Browserfunktionen skalieren oder ändern können.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-127">The problem with browser detection is that you may scale-back \(or change\) features in your webpage using assumptions about browser capabilities.</span></span> <span data-ttu-id="d2ad2-128">Stattdessen sollten Sie die Funktionserkennung verwenden, um die Funktionen Ihres Browsers zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-128">Instead, you should consider using feature detection to detect the capabilities of your browser.</span></span>  <span data-ttu-id="d2ad2-129">Unerwartetes Verhalten kann aufgrund einer der folgenden Situationen auftreten.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-129">Unexpected behavior may occur because of one of the following situations.</span></span>  

*   <span data-ttu-id="d2ad2-130">Code, der auf Windows Internet Explorer 8 ausgerichtet ist, kann in Microsoft Edge anders ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-130">Code targeted at Windows Internet Explorer 8 may run differently in Microsoft Edge.</span></span>  
*   <span data-ttu-id="d2ad2-131">Ein Feature, das Ihr Browser unterstützen sollte, ist aufgrund einer vom Entwickler vorgenommenen Annahme deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-131">A feature that your browser should support is disabled, because of an assumption made by the developer.</span></span>  

<span data-ttu-id="d2ad2-132">Wenn das Problem durch Ändern der Zeichenfolge des Benutzer-Agents behoben wird, ist die Browsererkennung wahrscheinlich eine Ursache.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-132">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>  

## <span data-ttu-id="d2ad2-133">Anzeige</span><span class="sxs-lookup"><span data-stu-id="d2ad2-133">Display</span></span>  

<span data-ttu-id="d2ad2-134">Zeigen Sie Emulation an, um eine Vorschau Ihrer Website auf unterschiedlichen Bildschirmgrößen und Auflösungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-134">Display emulation to preview your site on different screen sizes and resolutions.</span></span>  

*   <span data-ttu-id="d2ad2-135">herkömmliche Desktop Monitore</span><span class="sxs-lookup"><span data-stu-id="d2ad2-135">conventional desktop monitors</span></span>  
*   <span data-ttu-id="d2ad2-136">kleinere mobile Bildschirme</span><span class="sxs-lookup"><span data-stu-id="d2ad2-136">smaller mobile screens</span></span>  
*   <span data-ttu-id="d2ad2-137">neuere Monitore mit hoher Auflösung</span><span class="sxs-lookup"><span data-stu-id="d2ad2-137">newer high-resolution displays</span></span>  

<span data-ttu-id="d2ad2-138">Emulationen werden angepasst, um zu versuchen, die physikalischen Dimensionen der emulierten Bildschirme anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-138">Emulations are adapted to try to match the physical dimensions of the screens being emulated.</span></span>  <span data-ttu-id="d2ad2-139">Emulierte Pixel können komprimiert oder erweitert angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-139">Emulated pixels may appear compressed or expanded.</span></span> <span data-ttu-id="d2ad2-140">Eine Emulation wird nicht empfohlen, wenn Sie die pixelperfekte Positionierung von HTML-Elementen testen müssen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-140">Emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span>  <span data-ttu-id="d2ad2-141">Die Emulation eignet sich jedoch gut für das Testen von reaktionsfähigen Designs und das identifizieren größerer Element Positionierungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-141">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>  

### <span data-ttu-id="d2ad2-142">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="d2ad2-142">Orientation</span></span>  

<span data-ttu-id="d2ad2-143">Wählen Sie im **quer** Format oder **Hochformat** aus.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-143">Choose from **Landscape** or **Portrait** mode.</span></span>  

### <span data-ttu-id="d2ad2-144">Lösung</span><span class="sxs-lookup"><span data-stu-id="d2ad2-144">Resolution</span></span>  

<span data-ttu-id="d2ad2-145">Wählen Sie aus einer vordefinierten Liste gängiger Geräte Auflösungen aus, oder geben Sie Ihre eigene **benutzerdefinierte** Konfiguration an.  Es werden Auflösungen von bis zu 80 Zoll und 3820 x 2160 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-145">Choose from a preset list of popular device resolutions, or specify your own **Custom** config.  Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>  

## <span data-ttu-id="d2ad2-146">Geolocation</span><span class="sxs-lookup"><span data-stu-id="d2ad2-146">Geolocation</span></span>  

<span data-ttu-id="d2ad2-147">Wenn Ihre Website die [Geolocation-API][MdnGeolocationUsing] zum Bereitstellen von standortbasierten Diensten verwendet, stehen die folgenden Aktivitäten über die Bequemlichkeit Ihres Desktops zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-147">If your website uses the [Geolocation API][MdnGeolocationUsing] to provide location-based services, the following activities are available from the convenience of your desktop.</span></span>  

*   <span data-ttu-id="d2ad2-148">Einfaches Testen unterschiedlicher GPS-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="d2ad2-148">easily test different GPS coordinates</span></span>  
*   <span data-ttu-id="d2ad2-149">Einfaches Testen unterschiedlicher Sensorzustände</span><span class="sxs-lookup"><span data-stu-id="d2ad2-149">easily test different sensor states</span></span>  

<span data-ttu-id="d2ad2-150">Die Einstellungen setzen alle tatsächlichen GPS-Koordinaten und den Sensorzustand auf Geräten außer Kraft, die Geolokation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-150">The settings override any actual GPS coordinates and the sensor state on devices that support geolocation.</span></span>  

<span data-ttu-id="d2ad2-151">Ihre Website muss vor der Verwendung des Gerätespeicher Orts die Berechtigung eines Benutzers anfordern und ihm die Genehmigung erteilen.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-151">Your website must request and be granted permission from a user before using the device location.</span></span>  <span data-ttu-id="d2ad2-152">Testen Sie, wie sich Ihre Website über den Microsoft Edge **Settings** -Bereich mit und ohne Standort Berechtigungen verhält.</span><span class="sxs-lookup"><span data-stu-id="d2ad2-152">Test how your site behaves with and without location permissions from the Microsoft Edge **Settings** panel.</span></span>  

<span data-ttu-id="d2ad2-153">**...** >  **Einstellungen**  >  **Erweiterte Einstellungen anzeigen**  >  **Website Berechtigungen**  >  **Verwalten** von</span><span class="sxs-lookup"><span data-stu-id="d2ad2-153">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Das Microsoft Edge devtools-Emulations Panel" lightbox="./media/settings_manage_permissions.png":::
   <span data-ttu-id="d2ad2-155">Verwalten von Websiteberechtigungen über den Microsoft Edge **Settings** -Dialog</span><span class="sxs-lookup"><span data-stu-id="d2ad2-155">Manage website permissions from the Microsoft Edge **Settings** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="d2ad2-156">Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="d2ad2-156">Shortcuts</span></span>

| <span data-ttu-id="d2ad2-157">Aktion</span><span class="sxs-lookup"><span data-stu-id="d2ad2-157">Action</span></span>  | <span data-ttu-id="d2ad2-158">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="d2ad2-158">Shortcut</span></span>  |  
|:--- |:--- |  
| <span data-ttu-id="d2ad2-159">Zurücksetzen von Emulationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d2ad2-159">Reset Emulation settings</span></span> | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Emulieren von mobilen Geräten in Microsoft Edge devtools | Microsoft docs"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Den neuen Microsoft Edge-Browser herunterladen"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "Geolocation-API | MDN"  