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
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a>Bearbeiten von CSS-Schriftartenstilen und -einstellungen im Bereich Formatvorlagen  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

Die Typografie im Web ist ein wichtiger Bestandteil der Benutzeroberfläche.  Sie möchten sicherstellen, dass Sie die Unternehmensmarkenrichtlinien einhalten, und Ihre Inhalte werden wie erwartet auf verschiedenen Geräten angezeigt.  Text muss mithilfe von Größe und Zeilenhöhe leicht lesbar sein.  Benutzer können die Größe der Schriftarten an die individuellen Anforderungen anpassen.  In Situationen, in denen bestimmte Schriftarten auf einem Benutzergerät nicht verfügbar sind, sollten Sie Optionen für Fallbackschriftarten bereitstellen.  

CSS bietet in den letzten Jahren eine bessere Unterstützung für die Typografie.  Es stehen Dutzende von verschiedenen CSS-Einheiten zur Verfügung, um die Textgröße zu definieren.  Sie verfügen auch über mehrere CSS-Eigenschaften, die sich auf Schriftgrad, Abstand, Zeilenhöhe und andere typografische Features auswirken.  

Um die Arbeit mit Typografie zu vereinfachen, befindet sich jetzt ein visueller **Schriftarten-Editor** im **Bereich Formatvorlagen.**  Sie können ihre Schriftarteinstellungen ändern, und die Änderungen werden sofort im Browser gerendert.  Alle ohne ausführliche Kenntnisse von CSS.  

Derzeit ist das Feature experimentell, und Sie müssen es für **Enable new font editor tool within the Styles pane** Microsoft Edge Developer Tools [aktivieren.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  

Alle CSS im **Bereich Formatvorlagen,** entweder Schriftartdefinitionen oder Inlineformatvorlagen, zeigt automatisch ein Symbol an, das den visuellen **Schriftarten-Editor öffnet.**  Um den visuellen **Schriftarten-Editor zu öffnen,** wählen Sie das **Symbol Schriftart-Editor** aus.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Das Symbol im Bereich Formatvorlagen zum Bearbeiten von Schriftarteinstellungen" lightbox="../media/font-editor-icon.msft.png":::
         Das Symbol im **Bereich Formatvorlagen** zum Bearbeiten von Schriftarteinstellungen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet." lightbox="../media/font-editor-open.msft.png":::
         Der **Schriftarten-Editor** wird oben im Bereich **Formatvorlagen** geöffnet.  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Alle Felder im visuellen **Schriftarten-Editor** werden aus den Werten im CSS im Bereich **Formatvorlagen** aufgefüllt.  Beispielsweise wird die Definition im Bereich Formatvorlagen auf festgelegt, sodass das Textfeld Zeilenhöhe angezeigt wird, und das `line-height` `160%` **** `160` Einheitendropdown wird `%` angezeigt.  Außerdem wird der Schieberegler automatisch auf die Werte des Textfelds festgelegt.  

Der **Schriftarten-Editor** besteht aus zwei Teilen: der Auswahl der Schriftartfamilie und dem EDITOR für CSS-Eigenschaften.  

## <a name="the-font-family-selector"></a>Die Schriftartfamilienauswahl  

Die Auswahl der Schriftartfamilie ist der obere Teil des visuellen **Schriftarten-Editors.**  Verwenden Sie zum Auswählen der Schriftarten der CSS-Regel im CSS-Editor die Schriftartfamilienauswahl. ****  Sie können haupt- und fallbackschriftarten für jede CSS-Regel auswählen.  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet, und die Schriftartfamilienauswahl ist hervorgehoben." lightbox="../media/font-editor-font-family.msft.png":::
   Der **Schriftarten-Editor** wird oben im **Bereich** Formatvorlagen geöffnet, und **die** Schriftartfamilienauswahl ist hervorgehoben.  
:::image-end:::  

Verwenden Sie das **Dropdownmenü Schriftartfamilie,** um aus einer Liste von Schriftarten zu wählen.  Schriftarten sind in vier Gruppen unterteilt.  

1.  Berechnete Schriftarten, bei denen es sich um die Schriftarten handelt, die im Stylesheet im Bereich **Formatvorlagen verfügbar** sind.  
1.  Systemschriftarten, bei denen es sich um die Schriftarten handelt, die auf dem aktuellen Betriebssystem verfügbar sind.  
1.  Generische Schriftartenfamilien, z. B. `serif` oder `sans-serif` .  
1.  Globale Werte wie `inherit` , `initial` und `unset` .  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet, und die Schriftartfamilienauswahl ist hervorgehoben." lightbox="../media/font-editor-font-family-list.msft.png":::
   Der **Schriftarten-Editor** wird oben im **Bereich** Formatvorlagen geöffnet, und **die** Schriftartfamilienauswahl ist hervorgehoben.  
:::image-end:::  

Nachdem Sie eine Schriftart ausgewählt haben, wird ein weiteres Dropdownmenü angezeigt, in dem Sie Fallbackschriftarten auswählen können.  Sie können bis zu acht Fallbackschriftarten auswählen.  Wenn Sie eine Schriftart entfernen möchten, wählen Sie das **Symbol Schriftartfamilie** löschen aus.  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> Wenn Sie einen globalen Wert für die Schriftfamilie auswählen, erhalten Sie kein weiteres Dropdown, da es in CSS kein Fallback dafür gibt.  

## <a name="the-css-properties-editor"></a>Der Editor für CSS-Eigenschaften  

Sie können die Eigenschaften von CSS-Schriftarten im unteren Teil des visuellen **Schriftarten-Editors ändern.**  Sie können den Schriftgrad, die Zeilenhöhe, die Schriftgewichtung und den Buchstabenabstand mithilfe eines beliebigen Benutzeroberflächensteuerelements ändern.  Ihre Änderungen werden sofort im Browser angewendet.  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Der Schriftarten-Editor wird oben im Bereich Formatvorlagen geöffnet, und die CSS-Eigenschaften sind hervorgehoben." lightbox="../media/font-editor-css-properties.msft.png":::
   Der **Schriftarten-Editor** wird oben im Bereich **Formatvorlagen** geöffnet, und die CSS-Eigenschaften sind hervorgehoben.  
:::image-end:::  

Sie können auch CSS-Einheiten mit dem visuellen **Schriftarten-Editor konvertieren.**  Beispielsweise können Sie das Tool für eine CSS-Regel verwenden, bei der der **Schieberegler** Schriftgrad anfänglich auf festgelegt `16 pixels` ist.  Verwenden Sie nun das Dropdownmenü der Einheit, und wählen Sie den Wert `em` aus.  Die `1 em` angezeigte ist gleich `16 pixels` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Ändern der Schriftgröße in 16 Pixel" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         Ändern des Schriftgrads in `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Öffnen Sie das Einheitendropdown, um in em zu konvertieren" lightbox="../media/font-editor-converted-to-em.msft.png":::
         Öffnen Sie das Dropdownmenü der Einheit, in das konvertiert werden soll. `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Das Einheitendropdown stellt alle verfügbaren numerischen CSS-Einheiten bereit.  Schriftgrad, Zeilenhöhe, Schriftgrad und Abstand verwenden unterschiedliche Einheiten.  Wenn die Textfelder den Fokus haben, können Sie die Und-Tasten auswählen, `arrow up` um Ihre Einstellungen zu `arrow down` optimieren.  Um die Schieberegler mit einer Tastatur zu verwenden, wählen Sie die `arrow left` Tasten und `arrow down` aus.  

Der Editor für CSS-Eigenschaften enthält auch voreingestellte Schlüsselwörter.  Um die voreingestellten Schlüsselwörter zu verwenden, wählen Sie auf der rechten Seite das Symbol `Toggle Input Type` aus.  Die Benutzeroberfläche ändert sich, und es wird eine Dropdownliste mit vordefinierten Schlüsselwörtern angezeigt.  Um mit dem Schieberegler und anderen Benutzeroberflächensteuerelementen zur Benutzeroberfläche zurückzukehren, wählen Sie das `Toggle Input Type` Symbol erneut aus.  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Öffnen der vordefinierten Schlüsselwortschnittstelle" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   Öffnen der vordefinierten Schlüsselwortschnittstelle  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) -Entwicklertools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – Experimentelle Features | Microsoft Docs"  
