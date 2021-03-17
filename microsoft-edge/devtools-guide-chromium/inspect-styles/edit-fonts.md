---
description: Erfahren Sie, wie Sie CSS-Schriftartenarten und -einstellungen mithilfe des Bereichs Formatvorlagen in Microsoft Edge DevTools ändern.
title: Bearbeiten von CSS-Schriftarten und -Einstellungen im Bereich Formatvorlagen in DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
no-loc:
- Enable new font editor tool within the Styles pane
ms.openlocfilehash: 5d9074ca65f9cb98662a1bc181f70ead4c4232e1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439493"
---
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a><span data-ttu-id="32f9d-104">Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="32f9d-104">Edit CSS font styles and settings in the Styles pane</span></span>  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

<span data-ttu-id="32f9d-105">Die Typografie im Web ist ein wichtiger Bestandteil der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="32f9d-105">Typography on the web is an important part of the user experience.</span></span>  <span data-ttu-id="32f9d-106">Sie möchten sicherstellen, dass Sie die Unternehmensmarkenrichtlinien einhalten, und Ihre Inhalte werden wie erwartet auf verschiedenen Geräten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32f9d-106">You want to ensure you meet corporate brand guidelines, and your content displays as expected on various devices.</span></span>  <span data-ttu-id="32f9d-107">Text muss mithilfe von Größe und Zeilenhöhe leicht lesbar sein.</span><span class="sxs-lookup"><span data-stu-id="32f9d-107">Text must be easy to read using size and line-height.</span></span>  <span data-ttu-id="32f9d-108">Benutzer können die Größe der Schriftarten an die individuellen Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="32f9d-108">Users may resize fonts to meet individual needs.</span></span>  <span data-ttu-id="32f9d-109">In Situationen, in denen bestimmte Schriftarten auf einem Benutzergerät nicht verfügbar sind, sollten Sie Optionen für Fallbackschriftarten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="32f9d-109">For situations when specific fonts are not available on a user device, you should provide fallback font options.</span></span>  

<span data-ttu-id="32f9d-110">CSS bietet in den letzten Jahren eine bessere Unterstützung für die Typografie.</span><span class="sxs-lookup"><span data-stu-id="32f9d-110">CSS provides better support for typography in recent years.</span></span>  <span data-ttu-id="32f9d-111">Es stehen Dutzende von verschiedenen CSS-Einheiten zur Verfügung, um die Textgröße zu definieren.</span><span class="sxs-lookup"><span data-stu-id="32f9d-111">Dozens of different CSS units are available to define the size of text.</span></span>  <span data-ttu-id="32f9d-112">Sie verfügen auch über mehrere CSS-Eigenschaften, die sich auf Schriftgrad, Abstand, Zeilenhöhe und andere typografische Features auswirken.</span><span class="sxs-lookup"><span data-stu-id="32f9d-112">You also have several CSS properties that affect font-size, spacing, line height, and other typographic features.</span></span>  

<span data-ttu-id="32f9d-113">Um die Arbeit mit Typografie zu vereinfachen, befindet sich jetzt ein visueller **Schriftarten-Editor** im **Bereich Formatvorlagen.**</span><span class="sxs-lookup"><span data-stu-id="32f9d-113">To make it easier when working with typography, a visual **Font Editor** is now in the **Styles** pane.</span></span>  <span data-ttu-id="32f9d-114">Sie können ihre Schriftarteinstellungen ändern, und die Änderungen werden sofort im Browser gerendert.</span><span class="sxs-lookup"><span data-stu-id="32f9d-114">You may change your font settings, and the changes are rendered immediately in the browser.</span></span>  <span data-ttu-id="32f9d-115">Alle ohne ausführliche Kenntnisse von CSS.</span><span class="sxs-lookup"><span data-stu-id="32f9d-115">All without in-depth knowledge of CSS.</span></span>  

<span data-ttu-id="32f9d-116">Derzeit ist das Feature experimentell, und Sie müssen es für **Enable new font editor tool within the Styles pane** Microsoft Edge Developer Tools [aktivieren.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="32f9d-116">Currently the **Enable new font editor tool within the Styles pane** feature is experimental and you need to [turn it on for Microsoft Edge Developer Tools][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures].</span></span>  

<span data-ttu-id="32f9d-117">Alle CSS im **Bereich Formatvorlagen,** entweder Schriftartdefinitionen oder Inlineformatvorlagen, zeigt automatisch ein Symbol an, das den visuellen **Schriftarten-Editor öffnet.**</span><span class="sxs-lookup"><span data-stu-id="32f9d-117">Any CSS in the **Styles** pane, either font definitions or inline styles, automatically displays an icon that opens the visual **Font Editor**.</span></span>  <span data-ttu-id="32f9d-118">Um den visuellen **Schriftarten-Editor zu öffnen,** wählen Sie das **Symbol Schriftart-Editor** aus.</span><span class="sxs-lookup"><span data-stu-id="32f9d-118">To open the visual **Font Editor**, choose the **Font Editor** icon.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Das Symbol im Bereich Formatvorlagen zum Bearbeiten von Schriftarteinstellungen" lightbox="../media/font-editor-icon.msft.png":::
         <span data-ttu-id="32f9d-120">Das Symbol im **Bereich Formatvorlagen** zum Bearbeiten von Schriftarteinstellungen</span><span class="sxs-lookup"><span data-stu-id="32f9d-120">The icon in the **Styles** pane to edit font settings</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet." lightbox="../media/font-editor-open.msft.png":::
         <span data-ttu-id="32f9d-122">Der **Schriftarten-Editor** wird oben im Bereich **Formatvorlagen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="32f9d-122">The **Font Editor** open on top of the **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="32f9d-123">Alle Felder im visuellen **Schriftarten-Editor** werden aus den Werten im CSS im Bereich **Formatvorlagen** aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="32f9d-123">All fields in the visual **Font Editor** are populated from the values in the CSS in the **Styles** pane.</span></span>  <span data-ttu-id="32f9d-124">Beispielsweise wird die Definition im Bereich Formatvorlagen auf festgelegt, sodass das Textfeld Zeilenhöhe angezeigt wird, und das `line-height` `160%` \*\*\*\* `160` Einheitendropdown wird `%` angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32f9d-124">For example, the `line-height` definition is set to `160%` in the **Styles** pane, so the line height text field displays `160`, and the unit dropdown displays `%`.</span></span>  <span data-ttu-id="32f9d-125">Außerdem wird der Schieberegler automatisch auf die Werte des Textfelds festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32f9d-125">Also, the slider is automatically set to match the values of the text field.</span></span>  

<span data-ttu-id="32f9d-126">Der **Schriftarten-Editor** besteht aus zwei Teilen: der Auswahl der Schriftartfamilie und dem EDITOR für CSS-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="32f9d-126">The **Font Editor** consists of two parts:  the Font Family selector, and the CSS Properties editor.</span></span>  

## <a name="the-font-family-selector"></a><span data-ttu-id="32f9d-127">Die Schriftartfamilienauswahl</span><span class="sxs-lookup"><span data-stu-id="32f9d-127">The Font Family selector</span></span>  

<span data-ttu-id="32f9d-128">Die Auswahl der Schriftartfamilie ist der obere Teil des visuellen **Schriftarten-Editors.**</span><span class="sxs-lookup"><span data-stu-id="32f9d-128">The Font Family selector is the upper part of the visual **Font Editor**.</span></span>  <span data-ttu-id="32f9d-129">Verwenden Sie zum Auswählen der Schriftarten der CSS-Regel im CSS-Editor die Schriftartfamilienauswahl. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="32f9d-129">To choose the fonts of the CSS rule, in the CSS editor, use the **Font Family** selector.</span></span>  <span data-ttu-id="32f9d-130">Sie können haupt- und fallbackschriftarten für jede CSS-Regel auswählen.</span><span class="sxs-lookup"><span data-stu-id="32f9d-130">You may choose main and fallback fonts for each CSS rule.</span></span>  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet, und die Schriftartfamilienauswahl ist hervorgehoben." lightbox="../media/font-editor-font-family.msft.png":::
   <span data-ttu-id="32f9d-132">Der **Schriftarten-Editor** wird oben im **Bereich** Formatvorlagen geöffnet, und **die** Schriftartfamilienauswahl ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="32f9d-132">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="32f9d-133">Verwenden Sie das **Dropdownmenü Schriftartfamilie,** um aus einer Liste von Schriftarten zu wählen.</span><span class="sxs-lookup"><span data-stu-id="32f9d-133">Use the **Font Family** dropdown to choose from a list of fonts.</span></span>  <span data-ttu-id="32f9d-134">Schriftarten sind in vier Gruppen unterteilt.</span><span class="sxs-lookup"><span data-stu-id="32f9d-134">Fonts are organized into four groups.</span></span>  

1.  <span data-ttu-id="32f9d-135">Berechnete Schriftarten, bei denen es sich um die Schriftarten handelt, die im Stylesheet im Bereich **Formatvorlagen verfügbar** sind.</span><span class="sxs-lookup"><span data-stu-id="32f9d-135">Computed fonts, which are the fonts available in the stylesheet in the **Styles** pane.</span></span>  
1.  <span data-ttu-id="32f9d-136">Systemschriftarten, bei denen es sich um die Schriftarten handelt, die auf dem aktuellen Betriebssystem verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="32f9d-136">System fonts, which are the fonts that are available on the current operating system.</span></span>  
1.  <span data-ttu-id="32f9d-137">Generische Schriftartenfamilien, z. B. `serif` oder `sans-serif` .</span><span class="sxs-lookup"><span data-stu-id="32f9d-137">Generic font families, such as `serif` or `sans-serif`.</span></span>  
1.  <span data-ttu-id="32f9d-138">Globale Werte wie `inherit` , `initial` und `unset` .</span><span class="sxs-lookup"><span data-stu-id="32f9d-138">Global values, such as `inherit`, `initial`, and `unset`.</span></span>  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet, und die Schriftartfamilienauswahl ist hervorgehoben." lightbox="../media/font-editor-font-family-list.msft.png":::
   <span data-ttu-id="32f9d-140">Der **Schriftarten-Editor** wird oben im **Bereich** Formatvorlagen geöffnet, und **die** Schriftartfamilienauswahl ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="32f9d-140">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="32f9d-141">Nachdem Sie eine Schriftart ausgewählt haben, wird ein weiteres Dropdownmenü angezeigt, in dem Sie Fallbackschriftarten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="32f9d-141">After you choose a font, another dropdown menu is displayed for you to choose fallback fonts.</span></span>  <span data-ttu-id="32f9d-142">Sie können bis zu acht Fallbackschriftarten auswählen.</span><span class="sxs-lookup"><span data-stu-id="32f9d-142">You may choose up to eight fallback fonts.</span></span>  <span data-ttu-id="32f9d-143">Wenn Sie eine Schriftart entfernen möchten, wählen Sie das **Symbol Schriftartfamilie** löschen aus.</span><span class="sxs-lookup"><span data-stu-id="32f9d-143">To remove a font, choose the **Delete Font Family** icon.</span></span>  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> <span data-ttu-id="32f9d-144">Wenn Sie einen globalen Wert für die Schriftfamilie auswählen, erhalten Sie kein weiteres Dropdown, da es in CSS kein Fallback dafür gibt.</span><span class="sxs-lookup"><span data-stu-id="32f9d-144">If you choose a global value for font family, you do not get another dropdown since there is no fallback for it in CSS.</span></span>  

## <a name="the-css-properties-editor"></a><span data-ttu-id="32f9d-145">Der Editor für CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32f9d-145">The CSS Properties editor</span></span>  

<span data-ttu-id="32f9d-146">Sie können die Eigenschaften von CSS-Schriftarten im unteren Teil des visuellen **Schriftarten-Editors ändern.**</span><span class="sxs-lookup"><span data-stu-id="32f9d-146">You may change CSS font properties in the lower part of the visual **Font Editor**.</span></span>  <span data-ttu-id="32f9d-147">Sie können den Schriftgrad, die Zeilenhöhe, die Schriftgewichtung und den Buchstabenabstand mithilfe eines beliebigen Benutzeroberflächensteuerelements ändern.</span><span class="sxs-lookup"><span data-stu-id="32f9d-147">You may change the font size, line height, font weight, and letter spacing using any of the UI controls.</span></span>  <span data-ttu-id="32f9d-148">Ihre Änderungen werden sofort im Browser angewendet.</span><span class="sxs-lookup"><span data-stu-id="32f9d-148">Your changes are applied immediately in the browser.</span></span>  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet, und die CSS-Eigenschaften sind hervorgehoben." lightbox="../media/font-editor-css-properties.msft.png":::
   <span data-ttu-id="32f9d-150">Der **Schriftarten-Editor** wird oben im Bereich **Formatvorlagen** geöffnet, und die CSS-Eigenschaften sind hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="32f9d-150">The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="32f9d-151">Sie können auch CSS-Einheiten mit dem visuellen **Schriftarten-Editor konvertieren.**</span><span class="sxs-lookup"><span data-stu-id="32f9d-151">You may also convert CSS units using the visual **Font Editor**.</span></span>  <span data-ttu-id="32f9d-152">Beispielsweise können Sie das Tool für eine CSS-Regel verwenden, bei der der **Schieberegler** Schriftgrad anfänglich auf festgelegt `16 pixels` ist.</span><span class="sxs-lookup"><span data-stu-id="32f9d-152">For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels`.</span></span>  <span data-ttu-id="32f9d-153">Verwenden Sie nun das Dropdownmenü der Einheit, und wählen Sie den Wert `em` aus.</span><span class="sxs-lookup"><span data-stu-id="32f9d-153">Now, use the unit dropdown and choose the value `em`.</span></span>  <span data-ttu-id="32f9d-154">Die `1 em` angezeigte ist gleich `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="32f9d-154">The `1 em` displayed is equal to `16 pixels`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Ändern der Schriftgröße in 16 Pixel" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         <span data-ttu-id="32f9d-156">Ändern des Schriftgrads in</span><span class="sxs-lookup"><span data-stu-id="32f9d-156">Change the font size to</span></span> `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Öffnen Sie das Einheitendropdown, um in em zu konvertieren" lightbox="../media/font-editor-converted-to-em.msft.png":::
         <span data-ttu-id="32f9d-158">Öffnen Sie das Dropdownmenü der Einheit, in das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="32f9d-158">Open the unit dropdown to convert to</span></span> `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="32f9d-159">Das Einheitendropdown stellt alle verfügbaren numerischen CSS-Einheiten bereit.</span><span class="sxs-lookup"><span data-stu-id="32f9d-159">The unit dropdown provides all the numeric CSS units that are available.</span></span>  <span data-ttu-id="32f9d-160">Schriftgrad, Zeilenhöhe, Schriftgrad und Abstand verwenden unterschiedliche Einheiten.</span><span class="sxs-lookup"><span data-stu-id="32f9d-160">Font size, line height, font weight, and spacing all use different units.</span></span>  <span data-ttu-id="32f9d-161">Wenn die Textfelder den Fokus haben, können Sie die Und-Tasten auswählen, `arrow up` um Ihre Einstellungen zu `arrow down` optimieren.</span><span class="sxs-lookup"><span data-stu-id="32f9d-161">When the text boxes have focus, you may select the `arrow up` and `arrow down` keys to fine-tune your settings.</span></span>  <span data-ttu-id="32f9d-162">Um die Schieberegler mit einer Tastatur zu verwenden, wählen Sie die `arrow left` Tasten und `arrow down` aus.</span><span class="sxs-lookup"><span data-stu-id="32f9d-162">To use the sliders with a keyboard, select the `arrow left` and `arrow down` keys.</span></span>  

<span data-ttu-id="32f9d-163">Der Editor für CSS-Eigenschaften enthält auch voreingestellte Schlüsselwörter.</span><span class="sxs-lookup"><span data-stu-id="32f9d-163">The CSS Properties editor also includes preset keywords.</span></span>  <span data-ttu-id="32f9d-164">Um die voreingestellten Schlüsselwörter zu verwenden, wählen Sie auf der rechten Seite das Symbol `Toggle Input Type` aus.</span><span class="sxs-lookup"><span data-stu-id="32f9d-164">To use the preset keywords, on the right-hand side, choose the `Toggle Input Type` icon.</span></span>  <span data-ttu-id="32f9d-165">Die Benutzeroberfläche ändert sich, und es wird eine Dropdownliste mit vordefinierten Schlüsselwörtern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32f9d-165">The UI changes, and a dropdown of preset keywords are displayed.</span></span>  <span data-ttu-id="32f9d-166">Um mit dem Schieberegler und anderen Benutzeroberflächensteuerelementen zur Benutzeroberfläche zurückzukehren, wählen Sie das `Toggle Input Type` Symbol erneut aus.</span><span class="sxs-lookup"><span data-stu-id="32f9d-166">To return to the UI with the slider and other UI controls, choose the `Toggle Input Type` icon again.</span></span>  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Öffnen der vordefinierten Schlüsselwortschnittstelle" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   <span data-ttu-id="32f9d-168">Öffnen der vordefinierten Schlüsselwortschnittstelle</span><span class="sxs-lookup"><span data-stu-id="32f9d-168">Open the preset keyword interface</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="32f9d-169">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="32f9d-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
