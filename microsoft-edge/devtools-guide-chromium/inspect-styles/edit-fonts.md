---
description: Erfahren Sie, wie Sie mit dem Formatvorlagenbereich in Microsoft Edge DevTools die Formatvorlagen und Einstellungen von CSS ändern.
title: Bearbeiten von Css-Schriftartenformaten und -einstellungen im Formatvorlagenbereich in DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 928f7abb0f74839708cbe5c904ad321109ae33f0
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313220"
---
# <span data-ttu-id="0ab85-104">Bearbeiten von Css-Schriftartenformaten und -einstellungen im Formatvorlagenbereich</span><span class="sxs-lookup"><span data-stu-id="0ab85-104">Edit CSS font styles and settings in the Styles pane</span></span>  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

<span data-ttu-id="0ab85-105">Typografie im Web ist ein wichtiger Bestandteil der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="0ab85-105">Typography on the web is an important part of the user experience.</span></span>  <span data-ttu-id="0ab85-106">Sie möchten sicherstellen, dass Sie die Unternehmensrichtlinien für Marken einhalten und Ihre Inhalte auf verschiedenen Geräten wie erwartet angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0ab85-106">You want to ensure you meet corporate brand guidelines, and your content displays as expected on various devices.</span></span>  <span data-ttu-id="0ab85-107">Text muss mithilfe von Größe und Zeilenhöhe leicht lesbar sein.</span><span class="sxs-lookup"><span data-stu-id="0ab85-107">Text must be easy to read using size and line-height.</span></span>  <span data-ttu-id="0ab85-108">Benutzer können die Größe von Schriftarten an die individuellen Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="0ab85-108">Users may resize fonts to meet individual needs.</span></span>  <span data-ttu-id="0ab85-109">In Situationen, in denen bestimmte Schriftarten auf einem Benutzergerät nicht verfügbar sind, sollten Sie Ausweichoptionen für Schriftarten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ab85-109">For situations when specific fonts are not available on a user device, you should provide fallback font options.</span></span>  

<span data-ttu-id="0ab85-110">CSS bietet eine bessere Unterstützung für Typografie in den letzten Jahren.</span><span class="sxs-lookup"><span data-stu-id="0ab85-110">CSS provides better support for typography in recent years.</span></span>  <span data-ttu-id="0ab85-111">Es stehen Dutzende verschiedener CSS-Einheiten zur Verfügung, um die Textgröße zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0ab85-111">There are dozens of different CSS units available to define the size of text.</span></span>  <span data-ttu-id="0ab85-112">Sie verfügen auch über mehrere CSS-Eigenschaften, die sich auf Schriftgrad, Abstand, Zeilenhöhe und andere typografische Features auswirken.</span><span class="sxs-lookup"><span data-stu-id="0ab85-112">You also have several CSS properties that affect font-size, spacing, line height, and other typographic features.</span></span>  

<span data-ttu-id="0ab85-113">Um das Arbeiten mit Typografie zu vereinfachen, befindet sich jetzt ein visueller **Schriftarten-Editor** im **Formatvorlagenbereich.**</span><span class="sxs-lookup"><span data-stu-id="0ab85-113">To make it easier when working with typography, a visual **Font Editor** is now in the **Styles** pane.</span></span>  <span data-ttu-id="0ab85-114">Sie können Ihre Schriftarteinstellungen ändern, und die Änderungen werden sofort im Browser gerendert.</span><span class="sxs-lookup"><span data-stu-id="0ab85-114">You may change your font settings, and the changes are rendered immediately in the browser.</span></span>  <span data-ttu-id="0ab85-115">Alles ohne ausführliche Kenntnisse von CSS.</span><span class="sxs-lookup"><span data-stu-id="0ab85-115">All without in-depth knowledge of CSS.</span></span>  

<span data-ttu-id="0ab85-116">Derzeit ist **das Neue Schriftarten-Editor-Tool** im Formatvorlagenbereichsfeature experimentell, und Sie müssen es für [Microsoft Edge Developer Tools aktivieren.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="0ab85-116">Currently the **Enable new font editor tool within the Styles pane** feature is experimental and you need to [turn it on for Microsoft Edge Developer Tools][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures].</span></span>  

<span data-ttu-id="0ab85-117">Alle CSS \*\*\*\* im Formatvorlagenbereich, entweder Schriftartdefinitionen oder Inlineformatvorlagen, zeigen automatisch ein Symbol an, das den visuellen **Schriftarten-Editor öffnet.**</span><span class="sxs-lookup"><span data-stu-id="0ab85-117">Any CSS in the **Styles** pane, either font definitions or inline styles, automatically displays an icon that opens the visual **Font Editor**.</span></span>  <span data-ttu-id="0ab85-118">Wählen Sie zum Öffnen des **visuellen Schriftarten-Editors**das **Symbol "Schriftart-Editor"** aus.</span><span class="sxs-lookup"><span data-stu-id="0ab85-118">To open the visual **Font Editor**, choose the **Font Editor** icon.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Das Symbol im Formatvorlagenbereich zum Bearbeiten von Schriftarteinstellungen" lightbox="../media/font-editor-icon.msft.png":::
         <span data-ttu-id="0ab85-120">Das Symbol \*\*\*\* im Formatvorlagenbereich zum Bearbeiten von Schriftarteinstellungen</span><span class="sxs-lookup"><span data-stu-id="0ab85-120">The icon in the **Styles** pane to edit font settings</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der Schriftarten-Editor, der oben im Formatvorlagenbereich geöffnet wird" lightbox="../media/font-editor-open.msft.png":::
         <span data-ttu-id="0ab85-122">Der **Schriftarten-Editor,** der oben im **Formatvorlagenbereich geöffnet** wird</span><span class="sxs-lookup"><span data-stu-id="0ab85-122">The **Font Editor** open on top of the **Styles** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="0ab85-123">Alle Felder im visuellen **Schriftarten-Editor** werden aus den Werten im CSS im **Formatvorlagenbereich** aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="0ab85-123">All fields in the visual **Font Editor** are populated from the values in the CSS in the **Styles** pane.</span></span>  <span data-ttu-id="0ab85-124">Die Definition wird beispielsweise im Formatvorlagenbereich festgelegt, sodass das Textfeld für die Zeilenhöhe angezeigt wird `line-height` `160%` und das \*\*\*\* `160` Einheitendropdown angezeigt `%` wird.</span><span class="sxs-lookup"><span data-stu-id="0ab85-124">For example, the `line-height` definition is set to `160%` in the **Styles** pane, so the line height text field displays `160`, and the unit dropdown displays `%`.</span></span>  <span data-ttu-id="0ab85-125">Außerdem wird der Schieberegler automatisch so festgelegt, dass er mit den Werten des Textfelds übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="0ab85-125">Also, the slider is automatically set to match the values of the text field.</span></span>  

<span data-ttu-id="0ab85-126">Der **Schriftarten-Editor** besteht aus zwei Teilen: der Schriftartfamilienauswahl und dem CSS-Eigenschaften-Editor.</span><span class="sxs-lookup"><span data-stu-id="0ab85-126">The **Font Editor** consists of two parts:  the Font Family selector, and the CSS Properties editor.</span></span>  

## <span data-ttu-id="0ab85-127">Die Schriftartfamilienauswahl</span><span class="sxs-lookup"><span data-stu-id="0ab85-127">The Font Family selector</span></span>  

<span data-ttu-id="0ab85-128">Die Schriftartfamilienauswahl ist der obere Teil des visuellen **Schriftarten-Editors.**</span><span class="sxs-lookup"><span data-stu-id="0ab85-128">The Font Family selector is the upper part of the visual **Font Editor**.</span></span>  <span data-ttu-id="0ab85-129">Um die Schriftarten der CSS-Regel auszuwählen, \*\*\*\* verwenden Sie im CSS-Editor die Schriftartfamilienauswahl.</span><span class="sxs-lookup"><span data-stu-id="0ab85-129">To choose the fonts of the CSS rule, in the CSS editor, use the **Font Family** selector.</span></span>  <span data-ttu-id="0ab85-130">Sie können Haupt- und Fallbackschriftarten für jede CSS-Regel auswählen.</span><span class="sxs-lookup"><span data-stu-id="0ab85-130">You may choose main and fallback fonts for each CSS rule.</span></span>  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="The Font Editor open on top of the Styles pane with the Font Family selector highlighted" lightbox="../media/font-editor-font-family.msft.png":::
   <span data-ttu-id="0ab85-132">The **Font Editor** open on top of the **Styles** pane with the Font **Family** selector highlighted</span><span class="sxs-lookup"><span data-stu-id="0ab85-132">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="0ab85-133">Verwenden Sie das **Dropdownmenü** "Schriftartfamilie", um aus einer Liste von Schriftarten zu wählen.</span><span class="sxs-lookup"><span data-stu-id="0ab85-133">Use the **Font Family** dropdown to choose from a list of fonts.</span></span>  <span data-ttu-id="0ab85-134">Schriftarten sind in vier Gruppen unterteilt.</span><span class="sxs-lookup"><span data-stu-id="0ab85-134">Fonts are organized into four groups.</span></span>  

1.  <span data-ttu-id="0ab85-135">Berechnete Schriftarten, die im Stylesheet im Formatvorlagenbereich **verfügbar** sind.</span><span class="sxs-lookup"><span data-stu-id="0ab85-135">Computed fonts, which are the fonts available in the stylesheet in the **Styles** pane.</span></span>  
1.  <span data-ttu-id="0ab85-136">Systemschriftarten, bei denen es sich um die Schriftarten handelt, die unter dem aktuellen Betriebssystem verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="0ab85-136">System fonts, which are the fonts that are available on the current operating system.</span></span>  
1.  <span data-ttu-id="0ab85-137">Generische Schriftfamilien, z. B. `serif` oder `sans-serif` .</span><span class="sxs-lookup"><span data-stu-id="0ab85-137">Generic font families, such as `serif` or `sans-serif`.</span></span>  
1.  <span data-ttu-id="0ab85-138">Globale Werte, z. B. `inherit` `initial` , und `unset` .</span><span class="sxs-lookup"><span data-stu-id="0ab85-138">Global values, such as `inherit`, `initial`, and `unset`.</span></span>  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="The font editor open on top of the Styles pane with the Font Family selector highlighted" lightbox="../media/font-editor-font-family-list.msft.png":::
   <span data-ttu-id="0ab85-140">The **Font Editor** open on top of the **Styles** pane with the Font **Family** selector highlighted</span><span class="sxs-lookup"><span data-stu-id="0ab85-140">The **Font Editor** open on top of the **Styles** pane with the **Font Family** selector highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="0ab85-141">Nachdem Sie eine Schriftart ausgewählt haben, wird ein weiteres Dropdownmenü angezeigt, in dem Sie Ausweichschriftarten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="0ab85-141">After you choose a font, another dropdown menu is displayed for you to choose fallback fonts.</span></span>  <span data-ttu-id="0ab85-142">Sie können bis zu acht Ausweichschriftarten auswählen.</span><span class="sxs-lookup"><span data-stu-id="0ab85-142">You may choose up to eight fallback fonts.</span></span>  <span data-ttu-id="0ab85-143">Um eine Schriftart zu entfernen, wählen Sie das Symbol **"Schriftartfamilie löschen"** aus.</span><span class="sxs-lookup"><span data-stu-id="0ab85-143">To remove a font, choose the **Delete Font Family** icon.</span></span>  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> <span data-ttu-id="0ab85-144">Wenn Sie einen globalen Wert für die Schriftartfamilie auswählen, erhalten Sie kein weiteres Dropdown, da es kein Fallback dafür in CSS gibt.</span><span class="sxs-lookup"><span data-stu-id="0ab85-144">If you choose a global value for font family, you do not get another dropdown since there is no fallback for it in CSS.</span></span>  

## <span data-ttu-id="0ab85-145">Der Editor für DIE CSS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ab85-145">The CSS Properties editor</span></span>  

<span data-ttu-id="0ab85-146">Sie können die Eigenschaften der CSS-Schriftart im unteren Teil des visuellen **Schriftarten-Editors ändern.**</span><span class="sxs-lookup"><span data-stu-id="0ab85-146">You may change CSS font properties in the lower part of the visual **Font Editor**.</span></span>  <span data-ttu-id="0ab85-147">Sie können den Schriftgrad, die Zeilenhöhe, die Schriftgewichtung und den Buchstabenabstand mithilfe eines der Benutzeroberflächensteuerelemente ändern.</span><span class="sxs-lookup"><span data-stu-id="0ab85-147">You may change the font size, line height, font weight, and letter spacing using any of the UI controls.</span></span>  <span data-ttu-id="0ab85-148">Ihre Änderungen werden sofort im Browser angewendet.</span><span class="sxs-lookup"><span data-stu-id="0ab85-148">Your changes are applied immediately in the browser.</span></span>  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Der Schriftarten-Editor, der oben im Formatvorlagenbereich geöffnet wird, mit hervorgehobenen CSS-Eigenschaften" lightbox="../media/font-editor-css-properties.msft.png":::
   <span data-ttu-id="0ab85-150">The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted</span><span class="sxs-lookup"><span data-stu-id="0ab85-150">The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted</span></span>  
:::image-end:::  

<span data-ttu-id="0ab85-151">Sie können auch mit dem visuellen Schriftarten-Editor **CSS-Einheiten konvertieren.**</span><span class="sxs-lookup"><span data-stu-id="0ab85-151">You may also convert CSS units using the visual **Font Editor**.</span></span>  <span data-ttu-id="0ab85-152">Beispielsweise können Sie das Tool für eine CSS-Regel verwenden, bei der der **Schieberegler** für den Schriftgrad anfänglich auf festgelegt `16 pixels` ist.</span><span class="sxs-lookup"><span data-stu-id="0ab85-152">For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels`.</span></span>  <span data-ttu-id="0ab85-153">Verwenden Sie nun das Einheitendropdown, und wählen Sie den Wert `em` aus.</span><span class="sxs-lookup"><span data-stu-id="0ab85-153">Now, use the unit dropdown and choose the value `em`.</span></span>  <span data-ttu-id="0ab85-154">Der `1 em` angezeigte Wert ist gleich `16 pixels` .</span><span class="sxs-lookup"><span data-stu-id="0ab85-154">The `1 em` displayed is equal to `16 pixels`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Ändern des Schriftgrads in 16 Pixel" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         <span data-ttu-id="0ab85-156">Ändern des Schriftgrads in</span><span class="sxs-lookup"><span data-stu-id="0ab85-156">Change the font size to</span></span> `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Öffnen Sie das Einheitendropdown, um es in em zu konvertieren." lightbox="../media/font-editor-converted-to-em.msft.png":::
         <span data-ttu-id="0ab85-158">Öffnen Sie das Einheitendropdown, in das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ab85-158">Open the unit dropdown to convert to</span></span> `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="0ab85-159">Das Einheitendropdown enthält alle verfügbaren numerischen CSS-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="0ab85-159">The unit dropdown provides all the numeric CSS units that are available.</span></span>  <span data-ttu-id="0ab85-160">Schriftgrad, Zeilenhöhe, Schriftgrad und Abstand verwenden unterschiedliche Einheiten.</span><span class="sxs-lookup"><span data-stu-id="0ab85-160">Font size, line height, font weight, and spacing all use different units.</span></span>  <span data-ttu-id="0ab85-161">Wenn die Textfelder den Fokus haben, können Sie die Und-Tasten auswählen, `arrow up` um Ihre Einstellungen zu `arrow down` optimieren.</span><span class="sxs-lookup"><span data-stu-id="0ab85-161">When the text boxes have focus, you may select the `arrow up` and `arrow down` keys to fine-tune your settings.</span></span>  <span data-ttu-id="0ab85-162">Um die Schieberegler mit einer Tastatur zu verwenden, wählen Sie die Tasten `arrow left` und die `arrow down` Tasten aus.</span><span class="sxs-lookup"><span data-stu-id="0ab85-162">To use the sliders with a keyboard, select the `arrow left` and `arrow down` keys.</span></span>  

<span data-ttu-id="0ab85-163">Der Editor für CSS-Eigenschaften enthält auch vordefinierte Schlüsselwörter.</span><span class="sxs-lookup"><span data-stu-id="0ab85-163">The CSS Properties editor also includes preset keywords.</span></span>  <span data-ttu-id="0ab85-164">Um die voreingestellten Schlüsselwörter zu verwenden, wählen Sie auf der rechten Seite das Symbol `Toggle Input Type` aus.</span><span class="sxs-lookup"><span data-stu-id="0ab85-164">To use the preset keywords, on the right-hand side, choose the `Toggle Input Type` icon.</span></span>  <span data-ttu-id="0ab85-165">Die Benutzeroberfläche ändert sich, und es wird eine Dropdownliste mit vordefinierten Schlüsselwörtern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ab85-165">The UI changes, and a dropdown of preset keywords are displayed.</span></span>  <span data-ttu-id="0ab85-166">Um mit dem Schieberegler und anderen Benutzeroberflächensteuerelementen zur Benutzeroberfläche zurückzukehren, wählen Sie das `Toggle Input Type` Symbol erneut aus.</span><span class="sxs-lookup"><span data-stu-id="0ab85-166">To return to the UI with the slider and other UI controls, choose the `Toggle Input Type` icon again.</span></span>  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Öffnen der voreingestellten Schlüsselwortschnittstelle" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   <span data-ttu-id="0ab85-168">Öffnen der voreingestellten Schlüsselwortschnittstelle</span><span class="sxs-lookup"><span data-stu-id="0ab85-168">Open the preset keyword interface</span></span>  
:::image-end:::  

## <span data-ttu-id="0ab85-169">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="0ab85-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium)-Entwicklertools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – experimentelle Features | Microsoft Docs"  
