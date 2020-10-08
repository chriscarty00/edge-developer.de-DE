---
description: IE-Modus und Microsoft Edge (Chrom) devtools
title: Internet Explorer-Modus und DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, ie11, Internet Explorer 11, IE-Modus
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003967"
---
# <span data-ttu-id="c4d99-104">Internet Explorer-Modus und DevTools</span><span class="sxs-lookup"><span data-stu-id="c4d99-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="c4d99-105">In diesem Artikel wird beschrieben, wie der Internet Explorer-Modus \ (IE-Modus \) in den Microsoft Edge \ (Chromium \) devtools integriert ist.</span><span class="sxs-lookup"><span data-stu-id="c4d99-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <span data-ttu-id="c4d99-106">Grundlegendes zum IE-Modus</span><span class="sxs-lookup"><span data-stu-id="c4d99-106">Understanding IE mode</span></span>  

<span data-ttu-id="c4d99-107">Mit dem IE-Modus können Unternehmen eine Liste der Websites angeben, die nur in Internet Explorer 11 funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c4d99-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="c4d99-108">Wenn Sie zu diesen Websites in Microsoft Edge (Chrom \) navigieren, wird eine Instanz von Internet Explorer 11 ausgeführt, und die Website wird auf einer Registerkarte gerendert.  Mit dieser Funktion können Unternehmen die Kompatibilität mit Technologien verwalten, die derzeit nicht mit modernen Webbrowsern kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="c4d99-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="c4d99-109">Unterstützung für die folgenden Technologien ist im IE-Modus enthalten.</span><span class="sxs-lookup"><span data-stu-id="c4d99-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="c4d99-110">IE-Dokumentmodi</span><span class="sxs-lookup"><span data-stu-id="c4d99-110">IE document modes</span></span>  
*   <span data-ttu-id="c4d99-111">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c4d99-111">ActiveX controls</span></span>  
*   <span data-ttu-id="c4d99-112">andere Legacykomponenten</span><span class="sxs-lookup"><span data-stu-id="c4d99-112">other legacy components</span></span>  

<span data-ttu-id="c4d99-113">Im IE-Modus basiert der Renderingprozess auf Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="c4d99-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="c4d99-114">Der Microsoft Edge-Prozess-Manager (Chrom) verarbeitet die Lebensdauer des Rendering-Prozesses.</span><span class="sxs-lookup"><span data-stu-id="c4d99-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="c4d99-115">Sie ist auf die Lebensdauer der Registerkarte für eine bestimmte Website beschränkt \ (oder App \).</span><span class="sxs-lookup"><span data-stu-id="c4d99-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="c4d99-116">Wenn eine Registerkarte im IE-Modus gerendert wird, wird in der Adressleiste für die jeweilige Registerkarte ein Badge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4d99-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="IE-Modus-Abzeichen in der Adressleiste" lightbox="./media/ie-mode-badge.msft.png":::
   <span data-ttu-id="c4d99-118">IE-Modus-Abzeichen in der Adressleiste</span><span class="sxs-lookup"><span data-stu-id="c4d99-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="c4d99-119">Der IE-Modus ist derzeit unter Windows 10, Version 1903, verfügbar (Mai 2019-Update \), wird aber in Kürze für alle unterstützten Windows-Plattformen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c4d99-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <span data-ttu-id="c4d99-120">Starten des devtools auf einer Registerkarte im IE-Modus</span><span class="sxs-lookup"><span data-stu-id="c4d99-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="c4d99-121">Wenn Sie versuchen, den Dokumentmodus einer Website im IE-Modus anzuzeigen, wählen Sie das Abzeichen in der Adressleiste aus.</span><span class="sxs-lookup"><span data-stu-id="c4d99-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="IE-Modus-Abzeichen in der Adressleiste" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="c4d99-123">Anzeigen des Dokumentmodus mithilfe des IE-Modus-Badges</span><span class="sxs-lookup"><span data-stu-id="c4d99-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="c4d99-124">Wenn eine Registerkarte den IE-Modus verwendet, funktionieren die devtools nicht, und die folgenden Bedingungen treten auf.</span><span class="sxs-lookup"><span data-stu-id="c4d99-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="c4d99-125">Wenn Sie auswählen `F12` oder auswählen `Ctrl` + `Shift` + `I` , wird eine leere Instanz des Microsoft Edge \ (Chrom \) devtools gestartet, und die folgende Meldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4d99-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="c4d99-126">Wenn Sie ein Kontextmenü öffnen (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Quelle anzeigen**aus, wird der Editor gestartet.</span><span class="sxs-lookup"><span data-stu-id="c4d99-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="c4d99-127">Wenn Sie ein Kontextmenü öffnen \ (mit der rechten Maustaste auf \), wird das **Inspect-Element** nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4d99-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="c4d99-128">Der Grund dafür, dass eine Reihe von Tools innerhalb des devtools \ (wie **Netzwerk** -und **Leistungs** Tools \) nicht funktioniert, ist die Rendering-Engine, die im IE-Modus von Chrom zu Internet Explorer 11 wechselt.</span><span class="sxs-lookup"><span data-stu-id="c4d99-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="c4d99-129">Wenn Sie Feedback bereitstellen möchten, navigieren Sie zum [Kontakt mit dem Microsoft Edge devtools-Team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="c4d99-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="IE-Modus-Abzeichen in der Adressleiste" lightbox="./media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="c4d99-131">DevTools im IE-Modus gestartet</span><span class="sxs-lookup"><span data-stu-id="c4d99-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="c4d99-132">Führen Sie die folgenden Schritte aus, um Ihre Internet Explorer 11-basierte Website \ (oder App \) in Internet Explorer 11 und dem IE-Modus zu testen.</span><span class="sxs-lookup"><span data-stu-id="c4d99-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="c4d99-133">Öffnen Sie Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="c4d99-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="c4d99-134">Suchen Sie unter Windows 10 die Verknüpfung für Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="c4d99-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="c4d99-135">**Startmenü**  >  **Windows-Zubehör**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="c4d99-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="c4d99-136">Suchen Sie unter Windows 7 nach Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="c4d99-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="c4d99-137">**Startmenü**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="c4d99-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="c4d99-138">Öffnen Sie in Internet Explorer 11 dieselbe Webseite.</span><span class="sxs-lookup"><span data-stu-id="c4d99-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="c4d99-139">Starten Sie die Internet Explorer-devtools.</span><span class="sxs-lookup"><span data-stu-id="c4d99-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="c4d99-140">Wählen Sie aus `F12` .</span><span class="sxs-lookup"><span data-stu-id="c4d99-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="c4d99-141">Zeigen Sie auf eine beliebige Stelle, öffnen Sie ein Kontextmenü \ (Klicken Sie mit der rechten Maustaste auf \), und wählen Sie **Element prüfen**aus.</span><span class="sxs-lookup"><span data-stu-id="c4d99-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="c4d99-142">Weitere Informationen zur Verwendung dieser Tools finden Sie unter [Verwenden der F12-Entwicklertools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span><span class="sxs-lookup"><span data-stu-id="c4d99-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <span data-ttu-id="c4d99-143">Remote Debuggen und IE-Modus</span><span class="sxs-lookup"><span data-stu-id="c4d99-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="c4d99-144">Starten Sie Microsoft Edge \ (Chromium \) mit aktiviertem Remotedebuggen über die Befehlszeilenschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c4d99-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="c4d99-145">Visual Studio, Visual Studio-Code und andere Entwicklungstools führen in der Regel einen Befehl aus, um Microsoft Edge zu starten.</span><span class="sxs-lookup"><span data-stu-id="c4d99-145">Visual Studio, Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="c4d99-146">Mit dem folgenden Befehl wird Microsoft Edge gestartet, wobei der Remote Debugging-Port auf eingestellt ist `9222` .</span><span class="sxs-lookup"><span data-stu-id="c4d99-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="c4d99-147">Nachdem Sie Microsoft Edge \ (Chrom \) mithilfe eines Befehlszeilenarguments gestartet haben, ist der IE-Modus nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4d99-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="c4d99-148">Sie können weiterhin zu Websites \ (oder apps \) navigieren, die andernfalls im IE-Modus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c4d99-148">You may still navigate to websites \(or apps\) that would otherwise display in IE mode.</span></span> <span data-ttu-id="c4d99-149">Der Inhalt der Website \ (oder App \) wird mit Chrom und nicht mit Internet Explorer 11 gerendert.</span><span class="sxs-lookup"><span data-stu-id="c4d99-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="c4d99-150">Es wird davon ausgegangen, dass die Teile der Seiten, die auf IE11 basieren, wie ActiveX-Steuerelemente, nicht richtig gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="c4d99-150">Expect the parts of the pages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="c4d99-151">Das IE-Modus-Abzeichen wird in der Adressleiste nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4d99-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="c4d99-152">Der IE-Modus bleibt erst verfügbar, wenn Sie Microsoft Edge (Chrom) vollständig schließen und neu starten.</span><span class="sxs-lookup"><span data-stu-id="c4d99-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="c4d99-153">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="c4d99-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Verwenden der F12-Entwicklertools | Microsoft docs"  