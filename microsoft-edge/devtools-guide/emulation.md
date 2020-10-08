---
description: Verwenden des Emulations Panels zum Testen unterschiedlicher Browser Profile, Bildschirmgrößen und Auflösungen sowie GPS-Positionskoordinaten
title: DevTools-Emulation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Geräteemulation, reaktionsfähiges Design, Geolocation, Auflösung
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567637"
---
# <span data-ttu-id="78e1c-104">Emulation</span><span class="sxs-lookup"><span data-stu-id="78e1c-104">Emulation</span></span>

<span data-ttu-id="78e1c-105">Das *Emulations* Panel hilft Ihnen dabei, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="78e1c-105">The *Emulation* panel helps you to:</span></span>
 - <span data-ttu-id="78e1c-106">Simulieren verschiedener [Geräteprofile](#device), [Browser](#browser-profile), [Bildschirmgrößen und Auflösungen](#display)</span><span class="sxs-lookup"><span data-stu-id="78e1c-106">Simulate various [device profiles](#device), [browsers](#browser-profile), [screen sizes and resolutions](#display)</span></span>
 - <span data-ttu-id="78e1c-107">Testen verschiedener [Geolocation-Einstellungen und-Koordinaten](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="78e1c-107">Test different [geolocation settings and coordinates](#geolocation)</span></span>

![Das Microsoft Edge devtools-Emulations Panel](./media/emulation.png)

1. <span data-ttu-id="78e1c-109">Mit der Schaltfläche für die **Beibehaltung der Emulationseinstellungen** werden alle von Ihnen vorgenommenen Änderungen an den Standardeinstellungen für die Desktop Emulation gespeichert, auch wenn Sie das devtools schließen und erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="78e1c-109">The **Persist Emulation settings** button will save any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span> 

2. <span data-ttu-id="78e1c-110">Mit der Schaltfläche " **Emulationseinstellungen zurücksetzen** " werden Ihre Emulationseinstellungen wieder auf das standardmäßige *Desktop* Browserprofil und die Microsoft Edge-Benutzer-Agent-Zeichenfolge zurückgesetzt, wobei GPS deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="78e1c-110">The **Reset Emulation settings** button will reset your emulation settings back to the default *Desktop* browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>

3. <span data-ttu-id="78e1c-111">Wenn eine dieser Optionen von der Standardeinstellung geändert wird, wird auf der Registerkarte **Emulation** eine Informationswarnung angezeigt, die darauf hinweist, dass ein Aspekt des Verhaltens Ihres Browsers emuliert wird.</span><span class="sxs-lookup"><span data-stu-id="78e1c-111">When any of these options are changed from the default, the **Emulation** tab will show an informational alert to indicate that some aspect of your browser's behavior is being emulated.</span></span>

## <span data-ttu-id="78e1c-112">Gerät</span><span class="sxs-lookup"><span data-stu-id="78e1c-112">Device</span></span>

<span data-ttu-id="78e1c-113">Wählen Sie aus einer vordefinierten Liste von Windows-Geräteprofilen aus, die die anderen Emulationsoptionen automatisch konfigurieren oder Ihre eigene *benutzerdefinierte* Konfigurations.</span><span class="sxs-lookup"><span data-stu-id="78e1c-113">Pick from a preset list of Windows device profiles which  automatically configure the other emulation options or specify your own *Custom* configuation.</span></span> <span data-ttu-id="78e1c-114">Wechseln Sie zurück zu *Standard* , um alle Emulations Tools zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="78e1c-114">Switch back to *Default* to reset all the emulation tools.</span></span>

## <span data-ttu-id="78e1c-115">Modus</span><span class="sxs-lookup"><span data-stu-id="78e1c-115">Mode</span></span>

### <span data-ttu-id="78e1c-116">Browser Profil</span><span class="sxs-lookup"><span data-stu-id="78e1c-116">Browser profile</span></span>
<span data-ttu-id="78e1c-117">Eine schnelle Möglichkeit zum Simulieren der auf einem Windows Phone-Gerät ausgeführten Seite besteht darin, die **Browser Profil** Einstellung auf *Windows Phone*zu ändern.</span><span class="sxs-lookup"><span data-stu-id="78e1c-117">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to *Windows Phone*.</span></span>

#### <span data-ttu-id="78e1c-118">Benutzer-Agent-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="78e1c-118">User agent string</span></span>

<span data-ttu-id="78e1c-119">Das Ändern der Zeichenfolge des Benutzer-Agents, um einen anderen Browser zu imitieren, ist ein guter erster Schritt beim Debuggen von Fehlern, die nur in Microsoft Edge stattfinden.</span><span class="sxs-lookup"><span data-stu-id="78e1c-119">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span> 

<span data-ttu-id="78e1c-120">Frontend-und/oder Back-End-Skripte verwenden manchmal die Zeichenfolge des Benutzer-Agents, um zu ermitteln, welchen Browser Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="78e1c-120">Front end and/or back end scripts sometimes use the user agent string  to detect which browser you're using.</span></span> <span data-ttu-id="78e1c-121">Und selbst wenn Sie die Browsererkennung nicht in Ihrem eigenen Code verwenden, verwenden Sie möglicherweise eine JavaScript-Bibliothek eines Drittanbieters oder ein serverseitiges Skript.</span><span class="sxs-lookup"><span data-stu-id="78e1c-121">And even when you're not using browser detection in your own code, you may be using a third-party JavaScript library or server-side script that does.</span></span>

<span data-ttu-id="78e1c-122">Das Problem bei der Browsererkennung besteht darin, dass Sie häufig verwendet wird, um die Features in einer Webseite zu skalieren oder zu ändern, basierend auf dem, was der Entwickler, der das Skript schreibt, von Ihrem Browser abhängt, anstatt zu erkennen, was Ihr Browser tatsächlich mithilfe der Feature-Erkennung tun kann.</span><span class="sxs-lookup"><span data-stu-id="78e1c-122">The problem with browser detection is that it's often used to scale back or change the features in a webpage based on what the developer writing the script thinks your browser can do, rather than detecting what your browser can actually do using feature detection.</span></span> <span data-ttu-id="78e1c-123">Dies kann zu unerwartetem Verhalten führen, da Code, der auf Windows Internet Explorer 8 ausgerichtet ist, in Microsoft Edge sehr unterschiedlich ausgeführt werden kann. oder ein Feature, das Ihr Browser hervorragend unterstützt, ist möglicherweise aufgrund einer vom Entwickler vorgenommenen Annahme deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="78e1c-123">This can cause unexpected behavior, because code targeted at Windows Internet Explorer 8 can run very differently in Microsoft Edge; or a feature your browser is perfectly capable of supporting might be disabled because of an assumption made by the developer.</span></span>

<span data-ttu-id="78e1c-124">Wenn das Problem durch Ändern der Zeichenfolge des Benutzer-Agents behoben wird, ist die Browsererkennung wahrscheinlich eine Ursache.</span><span class="sxs-lookup"><span data-stu-id="78e1c-124">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>

## <span data-ttu-id="78e1c-125">Anzeige</span><span class="sxs-lookup"><span data-stu-id="78e1c-125">Display</span></span>

<span data-ttu-id="78e1c-126">Mit der Anzeige Emulation können Sie eine Vorschau Ihrer Website auf unterschiedlichen Bildschirmgrößen und-Auflösungen anzeigen: von herkömmlichen Desktop Monitoren bis zu kleineren mobilen Bildschirmen oder neueren Displays mit hoher Auflösung.</span><span class="sxs-lookup"><span data-stu-id="78e1c-126">Display emulation lets you preview your site on different screen sizes and resolutions: from conventional desktop monitors to smaller mobile screens or newer high-resolution displays.</span></span>

<span data-ttu-id="78e1c-127">Emulationen sind so angepasst, dass Sie den physikalischen Abmessungen der emulierten Bildschirme entsprechen.</span><span class="sxs-lookup"><span data-stu-id="78e1c-127">Emulations are adapted to try and match the physical dimensions of the screens being emulated.</span></span> <span data-ttu-id="78e1c-128">Emulierte Pixel werden möglicherweise komprimiert oder erweitert angezeigt, und es wird keine Emulation empfohlen, wenn Sie die pixelperfekte Positionierung von HTML-Elementen testen müssen.</span><span class="sxs-lookup"><span data-stu-id="78e1c-128">Emulated pixels might appear compressed or expanded, and emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span> <span data-ttu-id="78e1c-129">Die Emulation eignet sich jedoch gut für das Testen von reaktionsfähigen Designs und das identifizieren größerer Element Positionierungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="78e1c-129">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>

### <span data-ttu-id="78e1c-130">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="78e1c-130">Orientation</span></span>

<span data-ttu-id="78e1c-131">Wählen Sie im *quer* Format oder *Hochformat* aus.</span><span class="sxs-lookup"><span data-stu-id="78e1c-131">Choose from *Landscape* or *Portrait* mode.</span></span>

### <span data-ttu-id="78e1c-132">Lösung</span><span class="sxs-lookup"><span data-stu-id="78e1c-132">Resolution</span></span>

<span data-ttu-id="78e1c-133">Wählen Sie aus einer vordefinierten Liste gängiger Geräte Auflösungen aus, oder geben Sie Ihre eigene *benutzerdefinierte* Konfiguration an. Es werden Auflösungen von bis zu 80 Zoll und 3820 x 2160 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78e1c-133">Choose from a preset list of popular device resolutions, or specify your own *Custom* config. Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>

## <span data-ttu-id="78e1c-134">Geolocation</span><span class="sxs-lookup"><span data-stu-id="78e1c-134">Geolocation</span></span>

<span data-ttu-id="78e1c-135">Wenn Ihre Website die [Geolocation-API](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) verwendet, um standortbasierte Dienste bereitzustellen, können Sie unterschiedliche GPS-Koordinaten und Sensorzustände ganz einfach aus der Bequemlichkeit Ihres Desktops testen.</span><span class="sxs-lookup"><span data-stu-id="78e1c-135">If your site uses the [Geolocation API](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) to provide location-based services, you can easily test different GPS coordinates and sensor states from the convenience of your desktop.</span></span> <span data-ttu-id="78e1c-136">Mit diesen Einstellungen werden alle tatsächlichen GPS-Koordinaten und der Sensorzustand auf Computern, die Geolokation unterstützen, außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="78e1c-136">These settings will override any actual GPS coordinates and the sensor state on machines that support geolocation.</span></span> 

<span data-ttu-id="78e1c-137">Wie bei jeder Verwendung personenbezogener Daten im Internet müssen Ihre Benutzer zunächst Ihrer Website die Berechtigung erteilen, Ihren Standort zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="78e1c-137">As with any usage of personal data on the web, your users will first need to grant your site permission to use their location.</span></span> <span data-ttu-id="78e1c-138">Sie können über den Microsoft Edge *Settings* -Bereich testen, wie sich Ihre Website mit und ohne Standort Berechtigungen verhält:</span><span class="sxs-lookup"><span data-stu-id="78e1c-138">You can test how your site behaves with and without location permissions from the Microsoft Edge *Settings* panel:</span></span>

<span data-ttu-id="78e1c-139">**...** >  **Einstellungen**  >  **Erweiterte Einstellungen anzeigen**  >  **Website Berechtigungen**  >  **Verwalten** von</span><span class="sxs-lookup"><span data-stu-id="78e1c-139">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>

![Verwalten von Websiteberechtigungen über den Microsoft Edge Settings-Dialog](./media/settings_manage_permissions.png)

## <span data-ttu-id="78e1c-141">Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="78e1c-141">Shortcuts</span></span>

| <span data-ttu-id="78e1c-142">Aktion</span><span class="sxs-lookup"><span data-stu-id="78e1c-142">Action</span></span>                   | <span data-ttu-id="78e1c-143">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="78e1c-143">Shortcut</span></span>               |
|:-------------------------|:-----------------------|
| <span data-ttu-id="78e1c-144">Zurücksetzen von Emulationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="78e1c-144">Reset Emulation settings</span></span> | `CTRL` + `SHIFT` + `L` |
