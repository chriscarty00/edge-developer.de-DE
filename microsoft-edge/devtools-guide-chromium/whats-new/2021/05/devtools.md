---
description: Die Schaltfläche "Weitere Tools", die Kontextdokumentation für die ersten Schritte mit der DevTools-Erweiterung, die erweiterte Unterstützung für Bildschirmleseprogramme in der Konsole und vieles mehr.
title: Neuigkeiten in DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590867"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a><span data-ttu-id="c7cff-104">Neuigkeiten in DevTools (Microsoft Edge 92)</span><span class="sxs-lookup"><span data-stu-id="c7cff-104">What's New In DevTools (Microsoft Edge 92)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> <span data-ttu-id="c7cff-105">Die **Microsoft Build 2021-Konferenz** war vom 25. bis 27. Mai.</span><span class="sxs-lookup"><span data-stu-id="c7cff-105">The **Microsoft Build 2021** conference was on May 25-27.</span></span>  <span data-ttu-id="c7cff-106">Hier ist ein Video von Build über die Updates für DevTools: [Microsoft Edge | Status der Plattform][YoutubeEdgeStateOfThePlatform] – Microsoft Edge bietet eine überzeugende und konsistente Plattform mit Tools für Entwickler.</span><span class="sxs-lookup"><span data-stu-id="c7cff-106">Here's a video from Build about the updates to DevTools: [Microsoft Edge | State of the Platform][YoutubeEdgeStateOfThePlatform] - Microsoft Edge brings a compelling and consistent platform with tools for developers.</span></span>  <span data-ttu-id="c7cff-107">Wenn der Support für unsere älteren Browser eingestellt wird, wird Edge in Kürze der einzige unterstützte Browser von Microsoft auf Windows 10 sein.</span><span class="sxs-lookup"><span data-stu-id="c7cff-107">As our legacy browsers phase out of support, Edge will soon be the only supported browser from Microsoft on Windows 10.</span></span>  <span data-ttu-id="c7cff-108">Nehmen Sie an uns teil, um mehr über die neuesten Informationen auf der Edge-Plattform, den Tools und Web-Apps zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="c7cff-108">Join us to learn about the latest across the Edge platform, tools, and web apps.</span></span>


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a><span data-ttu-id="c7cff-109">Die Schaltfläche "Schließen" ist nicht mehr ausgeblendet, wenn DevTools schmal ist</span><span class="sxs-lookup"><span data-stu-id="c7cff-109">The Close button is no longer hidden when DevTools is narrow</span></span>

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

<span data-ttu-id="c7cff-110">In Microsoft Edge Version 91 oder früheren Versionen wird die Schaltfläche **"Schließen",** um DevTools zu schließen, nicht angezeigt, wenn der DevTools-Viewport schmal ist.</span><span class="sxs-lookup"><span data-stu-id="c7cff-110">In Microsoft Edge version 91 or earlier, the **Close** button to close DevTools isn't displayed when the DevTools viewport is narrow.</span></span>  <span data-ttu-id="c7cff-111">In Microsoft Edge Version 92 ist die Schaltfläche **"Schließen"** in den DevTools immer vorhanden, unabhängig von der Breite des DevTools-Viewports.</span><span class="sxs-lookup"><span data-stu-id="c7cff-111">In Microsoft Edge version 92, the **Close** button in the DevTools is always present, regardless of the DevTools viewport width.</span></span>

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="Die Schaltfläche "DevTools schließen" ist jetzt auch dann vorhanden, wenn der Viewport schmal ist." lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   <span data-ttu-id="c7cff-113">Die Schaltfläche **"DevTools schließen"** ist jetzt auch dann vorhanden, wenn der Viewport schmal ist.</span><span class="sxs-lookup"><span data-stu-id="c7cff-113">The **Close** DevTools button is now present even when the viewport is narrow</span></span>  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a><span data-ttu-id="c7cff-114">Schnelles Hinzufügen von Tools mit der neuen Schaltfläche "Weitere Tools"</span><span class="sxs-lookup"><span data-stu-id="c7cff-114">Add tools quickly with the new More Tools button</span></span>

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

<span data-ttu-id="c7cff-115">Es gibt eine neue Möglichkeit, weitere Tools in Microsoft Edge DevTools zu öffnen: das Menü **"Weitere Tools** ( `+` ) ".</span><span class="sxs-lookup"><span data-stu-id="c7cff-115">There's a new way to open more tools in Microsoft Edge DevTools: the **More Tools** (`+`) menu.</span></span> <span data-ttu-id="c7cff-116">Das Menü **"Weitere Tools"** wird auf der Symbolleiste im Hauptbereich und auf der Symbolleiste der Schublade angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7cff-116">The **More Tools** menu appears on the toolbar in the main panel and on the toolbar of the drawer.</span></span> <span data-ttu-id="c7cff-117">Wenn Sie ein Tool aus dem Menü **"Weitere Tools"** auswählen, wird das Tool zur Symbolleiste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c7cff-117">Selecting a tool from the **More Tools** menu adds the tool to the toolbar.</span></span>

<span data-ttu-id="c7cff-118">Um die Registerkarten auf beiden Symbolleisten neu anzuordnen, wählen Sie die Registerkarten aus, und ziehen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="c7cff-118">To reorder the tabs on either toolbar, select and drag the tabs.</span></span>  

<span data-ttu-id="c7cff-119">Das Menü **"Weitere Tools"** war in Microsoft Edge Version 89 als Experiment verfügbar und ist jetzt immer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7cff-119">The **More Tools** menu was available as an experiment in Microsoft Edge version 89, and is now always present.</span></span>

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="Die Schaltfläche "Weitere Tools" auf der oberen Symbolleiste und der Schublade-Symbolleiste" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   <span data-ttu-id="c7cff-121">Die Schaltfläche **"Weitere Tools"** auf der oberen Symbolleiste und der Schublade-Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="c7cff-121">The **More Tools** button on the upper toolbar and drawer toolbar</span></span>
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Das Menü "Weitere Tools"" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   <span data-ttu-id="c7cff-123">Das Menü **"Weitere Tools"**</span><span class="sxs-lookup"><span data-stu-id="c7cff-123">The **More Tools** menu</span></span>
:::image-end:::  


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a><span data-ttu-id="c7cff-124">Verbesserungen beim Zeigen, Auswählen und Schließen von Tools</span><span class="sxs-lookup"><span data-stu-id="c7cff-124">Improvements for hovering, selecting, and closing tools</span></span>

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

<span data-ttu-id="c7cff-125">Registerkarten für jedes Tool wurden neu formatiert, um die Wahrscheinlichkeit zu verringern, dass ein Tool versehentlich geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c7cff-125">Tabs for each tool have been reformatted to reduce the chance of accidentally closing a tool.</span></span>  <span data-ttu-id="c7cff-126">Auf jeder Registerkarte in der Hauptsymbolleiste und in der Symbolleiste der Schublade haben wir Folgendes hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="c7cff-126">On each tab in the main toolbar and in the toolbar of the drawer, we added:</span></span>
*  <span data-ttu-id="c7cff-127">Abstand um die Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="c7cff-127">Spacing around the tab.</span></span>
*  <span data-ttu-id="c7cff-128">Abstand um die Schaltfläche "Schließen" `x` ()" auf der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="c7cff-128">Spacing around the close (`x`) button in the tab.</span></span>
*  <span data-ttu-id="c7cff-129">Eine Hintergrundfarbe beim Bewegen über die Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="c7cff-129">A background color when hovering over the tab.</span></span>
*  <span data-ttu-id="c7cff-130">Eine QuickInfo für die Schaltfläche zum Schließen ( `x` ) der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="c7cff-130">A tooltip for the close (`x`) button of the tab.</span></span>
*  <span data-ttu-id="c7cff-131">Höherer Kontrast für die Schaltfläche zum Schließen ( `x` ) der Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="c7cff-131">Higher contrast for the close (`x`) button of the tab.</span></span>

<span data-ttu-id="c7cff-132">Wenn Sie sich beispielsweise im **Leistungstool** befinden und auf die Registerkarte des **Netzwerktools** zeigen, verhindern diese Verbesserungen das versehentliche Schließen des **Netzwerktools.**</span><span class="sxs-lookup"><span data-stu-id="c7cff-132">For example, when you are in the **Performance** tool and you hover over the **Network** tool's tab, these improvements help prevent accidentally closing the **Network** tool.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Registerkarten vor der Neuformatierung" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           <span data-ttu-id="c7cff-134">Registerkarten vor der Neuformatierung</span><span class="sxs-lookup"><span data-stu-id="c7cff-134">Tabs before reformatting</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Registerkarten nach der Neuformatierung" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           <span data-ttu-id="c7cff-136">Registerkarten nach der Neuformatierung</span><span class="sxs-lookup"><span data-stu-id="c7cff-136">Tabs after reformatting</span></span> :::image-end:::
    :::column-end:::
:::row-end:::

<span data-ttu-id="c7cff-137">Diese Verbesserungen sind besonders für Benutzer lokalisierter DevTools relevant, bei denen die Registerkarten möglicherweise schmaler sind und versehentlich leichter geschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="c7cff-137">These improvements are especially relevant for users of localized DevTools, in which the tabs may be narrower and easier to accidentally close.</span></span>

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="Lokalisierte DevTools mit schmalen Registerkarten" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   <span data-ttu-id="c7cff-139">Lokalisierte DevTools mit schmalen Registerkarten</span><span class="sxs-lookup"><span data-stu-id="c7cff-139">Localized DevTools with narrow tabs</span></span>
:::image-end:::

<span data-ttu-id="c7cff-140">Außerdem wurde es einfacher, ein Tool, das Sie geschlossen haben, erneut hinzuzufügen, indem ein [Menü "Weitere Tools"](#add-tools-quickly-with-the-new-more-tools-button) zur Hauptsymbolleiste und der Schublade-Symbolleiste hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c7cff-140">We also made it easier to re-add a tool that you closed by adding a [More Tools menu](#add-tools-quickly-with-the-new-more-tools-button) to the main toolbar and drawer toolbar.</span></span>


## <a name="better-support-for-screen-readers-in-the-console"></a><span data-ttu-id="c7cff-141">Bessere Unterstützung für Bildschirmleseprogramme in der Konsole</span><span class="sxs-lookup"><span data-stu-id="c7cff-141">Better support for screen readers in the Console</span></span>

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

<span data-ttu-id="c7cff-142">Vor Microsoft Edge Version 92 haben Hilfstechnologien wie Sprachausgabe in der **Konsole**keine Vorschläge zur automatischen Vervollständigung oder die Ergebnisse ausgewerteter Ausdrücke angekündigt.</span><span class="sxs-lookup"><span data-stu-id="c7cff-142">Prior to Microsoft Edge version 92, in the **Console**, assistive technologies such as screen readers didn't announce autocomplete suggestions or the results of evaluated expressions.</span></span> <span data-ttu-id="c7cff-143">Dies wurde jetzt behoben.</span><span class="sxs-lookup"><span data-stu-id="c7cff-143">This has been fixed now.</span></span>

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="In der Konsole kündigen Bildschirmleseprogramme jetzt den aktuell ausgewählten AutoVervollständigen-Vorschlag an." lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           <span data-ttu-id="c7cff-145">In der **Konsole**kündigen Bildschirmleseprogramme jetzt den aktuell ausgewählten Vorschlag für automatisches Vervollständigen an.</span><span class="sxs-lookup"><span data-stu-id="c7cff-145">In the **Console**, screen readers now announce the currently selected autocomplete suggestion</span></span> :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="In der Konsole kündigen Bildschirmleseprogramme nun das Ergebnis eines ausgewerteten Ausdrucks an." lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           <span data-ttu-id="c7cff-147">In der **Konsole**kündigen Bildschirmleseprogramme nun das Ergebnis eines ausgewerteten Ausdrucks an.</span><span class="sxs-lookup"><span data-stu-id="c7cff-147">In the **Console**, screen readers now announce the result of an evaluated expression</span></span> :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a><span data-ttu-id="c7cff-148">Microsoft Edge Entwicklertools für Visual Studio Code Version 1.1.8</span><span class="sxs-lookup"><span data-stu-id="c7cff-148">Microsoft Edge Developer Tools for Visual Studio Code version 1.1.8</span></span>

<span data-ttu-id="c7cff-149">Die [Microsoft Edge Developer Tools für Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] Erweiterungsversion 1.1.8 für Microsoft Visual Studio Code weist seit der vorherigen Version die folgenden Änderungen auf.</span><span class="sxs-lookup"><span data-stu-id="c7cff-149">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code has the following changes since the previous release.</span></span>  <span data-ttu-id="c7cff-150">Microsoft Visual Studio Code aktualisiert Erweiterungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="c7cff-150">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="c7cff-151">Um die Version 1.1.8 manuell zu aktualisieren, navigieren Sie manuell zu ["Erweiterung aktualisieren".][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="c7cff-151">To manually update to version 1.1.8, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  

<span data-ttu-id="c7cff-152">Sie können Probleme melden und zur Erweiterung im [vscode-edge-devtools GitHub Repo][GithubMicrosoftVscodeEdgeDevtools]beitragen.</span><span class="sxs-lookup"><span data-stu-id="c7cff-152">You can file issues and contribute to the extension on the [vscode-edge-devtools GitHub repo][GithubMicrosoftVscodeEdgeDevtools].</span></span>  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a><span data-ttu-id="c7cff-153">Kontextdokumentation und Benutzeroberfläche, um die Verwendung der DevTools-Erweiterung zu vereinfachen</span><span class="sxs-lookup"><span data-stu-id="c7cff-153">In-context documentation and UI to make it easier to use the DevTools extension</span></span>

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

<span data-ttu-id="c7cff-154">Version 1.1.8 der [Microsoft Edge Developer Tools für Visual Studio Code-Erweiterung][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] bietet jetzt eine einfachere Möglichkeit, eine neue Instanz von Microsoft Edge zu starten, indem Anweisungen, Schaltflächen, Links und eine Dokumentationsseite zur Anleitung präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7cff-154">Version 1.1.8 of the [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension now features a simpler way to start a new instance of Microsoft Edge, by presenting instructions, buttons, links, and a documentation page to guide you.</span></span>

*  <span data-ttu-id="c7cff-155">Wenn Sie die Schaltfläche **Microsoft Edge Tools** in der **Aktivitätsleiste** von Visual Studio Code auswählen, werden im Bereich **Microsoft Edge Tools: Targets** nun erläuternder Text, Schaltflächen und Links zur Anleitung anstelle eines leeren Bereichs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7cff-155">When you select the **Microsoft Edge Tools** button in the **Activity Bar** of Visual Studio Code, the **Microsoft Edge Tools: Targets** panel now presents explanatory text, buttons, and links to guide you, instead of a blank panel.</span></span>

*  <span data-ttu-id="c7cff-156">Wenn Sie eine neue Instanz von Microsoft Edge in Visual Studio Code öffnen, zeigt Microsoft Edge jetzt eine Startseite an, auf der erläutert wird, wie die Entwicklertools-Erweiterung anstelle einer leeren Seite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7cff-156">When you open a new instance of Microsoft Edge from within Visual Studio Code, Microsoft Edge now shows a start page that explains how to use the Developer Tools extension, instead of a blank page.</span></span>

*  <span data-ttu-id="c7cff-157">Der Bereich **Microsoft Edge Tools: Targets** verfügt jetzt über eine Schaltfläche **"Generieren launch.js"** und Anweisungen, um das Projekt zum Debuggen in Microsoft Edge zu starten.</span><span class="sxs-lookup"><span data-stu-id="c7cff-157">The **Microsoft Edge Tools: Targets** panel now has a **Generate launch.json** button and instructions, to help launch your project for debugging in Microsoft Edge.</span></span>

<span data-ttu-id="c7cff-158">Navigieren Sie zu ["Verwenden der Tools",][GithubIoDevToolsUsing]um weitere Informationen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="c7cff-158">For more information, navigate to [Using the tools][GithubIoDevToolsUsing].</span></span>


## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="c7cff-159">Herunterladen der Microsoft Edge-Vorschaukanäle</span><span class="sxs-lookup"><span data-stu-id="c7cff-159">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="c7cff-160">Wenn Sie unter Windows, Linux oder macOS arbeiten, sollten Sie die [Microsoft Edge-Vorschaukanäle][MicrosoftEdgePreviewChannels] als Standardentwicklungsbrowser verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7cff-160">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="c7cff-161">Über die Vorschaukanäle erhalten Sie Zugriff auf die neuesten DevTools-Features.</span><span class="sxs-lookup"><span data-stu-id="c7cff-161">The preview channels give you access to the latest DevTools features.</span></span>  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="c7cff-162">Mit dem Microsoft Edge DevTools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="c7cff-162">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Verwenden der Tools | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Microsoft Edge-Vorschaukanäle"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Manuelles Aktualisieren einer Erweiterung – Erweiterungs-Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Entwicklertools für Visual Studio Code | Visual Studio Markt"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: Status des Plattform-| Youtube"

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c7cff-170">Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7cff-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
