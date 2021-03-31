---
description: IE-Modus und Microsoft Edge (Chromium) DevTools
title: Internet Explorer-Modus und devTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, ie11, internet explorer 11, ie mode
ms.openlocfilehash: e65869cd88b449dcde0aec25c77df27f99b78f8d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398602"
---
# <a name="internet-explorer-mode-and-the-devtools"></a><span data-ttu-id="d8ce4-104">Internet Explorer-Modus und devTools</span><span class="sxs-lookup"><span data-stu-id="d8ce4-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="d8ce4-105">In diesem Artikel wird beschrieben, wie der Internet Explorer-Modus \(IE-Modus\) in microsoft Edge \(Chromium\) DevTools integriert wird.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <a name="understanding-ie-mode"></a><span data-ttu-id="d8ce4-106">Grundlegendes zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="d8ce4-106">Understanding IE mode</span></span>  

<span data-ttu-id="d8ce4-107">Im IE-Modus können Unternehmen eine Liste der Websites angeben, die nur in Internet Explorer 11 funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="d8ce4-108">Wenn Sie zu diesen Websites in Microsoft Edge \(Chromium\) navigieren, wird eine Instanz von Internet Explorer 11 ausgeführt und die Website auf einer Registerkarte gerendert.  Mit der Funktionalität können Unternehmen die Kompatibilität mit Technologien verwalten, die derzeit nicht mit modernen Webbrowsern kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="d8ce4-109">Unterstützung für die folgenden Technologien ist im IE-Modus enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="d8ce4-110">IE-Dokumentmodi</span><span class="sxs-lookup"><span data-stu-id="d8ce4-110">IE document modes</span></span>  
*   <span data-ttu-id="d8ce4-111">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d8ce4-111">ActiveX controls</span></span>  
*   <span data-ttu-id="d8ce4-112">andere Legacykomponenten</span><span class="sxs-lookup"><span data-stu-id="d8ce4-112">other legacy components</span></span>  

<span data-ttu-id="d8ce4-113">Im IE-Modus basiert der Rendervorgang auf Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="d8ce4-114">Der Microsoft Edge \(Chromium\)-Prozess-Manager übernimmt die Lebensdauer des Renderingprozesses.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="d8ce4-115">Sie ist auf die Lebensdauer der Registerkarte für eine bestimmte Website \(oder App\) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="d8ce4-116">Wenn eine Registerkarte im IE-Modus gerendert wird, wird in der Adressleiste für die spezifische Registerkarte ein Signal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="IE-Modus-Signal in der Adressleiste" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="d8ce4-118">IE-Modus-Signal in der Adressleiste</span><span class="sxs-lookup"><span data-stu-id="d8ce4-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="d8ce4-119">Der IE-Modus ist derzeit unter Windows 10 Version 1903 \(Mai 2019 Update\) verfügbar, wird aber bald für alle unterstützten Windows-Plattformen verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a><span data-ttu-id="d8ce4-120">Starten der DevTools auf einer Registerkarte im IE-Modus</span><span class="sxs-lookup"><span data-stu-id="d8ce4-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="d8ce4-121">Wenn Sie versuchen, den Dokumentmodus einer Website im IE-Modus zu sehen, wählen Sie das Signal in der Adressleiste aus.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badges" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="d8ce4-123">Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badges</span><span class="sxs-lookup"><span data-stu-id="d8ce4-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="d8ce4-124">Wenn eine Registerkarte den IE-Modus verwendet, funktionieren die DevTools nicht, und die folgenden Bedingungen treten auf.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="d8ce4-125">Wenn Sie auswählen oder auswählen, wird die folgende Meldung angezeigt, wenn eine leere Instanz von `F12` `Ctrl` + `Shift` + `I` Microsoft Edge \(Chromium\) DevTools gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="d8ce4-126">Wenn Sie ein kontextbezogenes Menü \(rechtsklicken\) öffnen und Quelle **anzeigen**auswählen, wird Editor gestartet.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="d8ce4-127">Wenn Sie ein kontextbezogenes Menü \(mit der rechten Maustaste klicken\) öffnen, ist das **Inspect-Element** nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="d8ce4-128">Der Grund, warum eine Reihe der Tools innerhalb  der  DevTools \(wie die Netzwerk- und Leistungstools\) nicht funktioniert, ist der Wechsel des Renderingmoduls von Chromium zu Internet Explorer 11 im IE-Modus.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="d8ce4-129">Um Feedback zu geben, navigieren Sie zu Kontakt mit dem [Microsoft Edge DevTools-Team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="d8ce4-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools im IE-Modus gestartet" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="d8ce4-131">DevTools im IE-Modus gestartet</span><span class="sxs-lookup"><span data-stu-id="d8ce4-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="d8ce4-132">Führen Sie die folgenden Schritte aus, um Ihre Internet Explorer 11-basierte Website \(oder App\) im Internet Explorer 11- und IE-Modus zu testen.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="d8ce4-133">Öffnen Sie Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="d8ce4-134">Suchen Sie unter Windows 10 nach der Verknüpfung für Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="d8ce4-135">**Startmenü**  >  **Windows-Zubehör**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="d8ce4-136">Suchen Sie unter Windows 7 nach Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="d8ce4-137">**Startmenü**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="d8ce4-138">Öffnen Sie in Internet Explorer 11 dieselbe Webseite.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="d8ce4-139">Starten Sie Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="d8ce4-140">Wählen Sie `F12` aus.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="d8ce4-141">Zeigen Sie auf eine beliebige Stelle, öffnen Sie ein kontextbezogenes Menü \(klicken Sie mit der rechten Maustaste\), und wählen Sie **Inspect-Element aus.**</span><span class="sxs-lookup"><span data-stu-id="d8ce4-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="d8ce4-142">Weitere Informationen zur Verwendung dieser Tools finden Sie unter [Verwenden der F12-Entwicklertools.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]</span><span class="sxs-lookup"><span data-stu-id="d8ce4-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <a name="remote-debugging-and-ie-mode"></a><span data-ttu-id="d8ce4-143">Remotedebuding und IE-Modus</span><span class="sxs-lookup"><span data-stu-id="d8ce4-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="d8ce4-144">Starten Sie Microsoft Edge \(Chromium\) mit aktiviertem Remotedebu debugging über die Befehlszeilenschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="d8ce4-145">Microsoft Visual Studio, Microsoft Visual Studio Code und andere Entwicklungstools führen in der Regel einen Befehl aus, um Microsoft Edge zu starten.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-145">Microsoft Visual Studio, Microsoft Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="d8ce4-146">Mit dem folgenden Befehl wird Microsoft Edge gestartet, und der Remotedebugport ist auf `9222` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="d8ce4-147">Nachdem Sie Microsoft Edge \(Chromium\) mithilfe eines Befehlszeilenarguments gestartet haben, ist der IE-Modus nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="d8ce4-148">Sie können weiterhin zu Websites \(oder Apps\) navigieren, die andernfalls im IE-Modus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-148">You may still navigate to websites \(or apps\) that are otherwise displayed in IE mode.</span></span>  <span data-ttu-id="d8ce4-149">Der Inhalt der Website \(oder App\) wird mit Chromium gerendert, nicht mit Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="d8ce4-150">Erwarten Sie, dass die Teile der Webseiten, die auf IE11 beruhen, z. B. ActiveX Steuerelemente, nicht ordnungsgemäß gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-150">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="d8ce4-151">Das IE-Modus-Signal wird nicht in der Adressleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="d8ce4-152">Der IE-Modus ist erst verfügbar, wenn Sie Microsoft Edge \(Chromium\) vollständig schließen und neu starten.</span><span class="sxs-lookup"><span data-stu-id="d8ce4-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d8ce4-153">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="d8ce4-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Verwenden der F12-Entwicklertools | Microsoft Docs"  
