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
# Bearbeiten von Css-Schriftartenformaten und -einstellungen im Formatvorlagenbereich  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

Typografie im Web ist ein wichtiger Bestandteil der Benutzeroberfläche.  Sie möchten sicherstellen, dass Sie die Unternehmensrichtlinien für Marken einhalten und Ihre Inhalte auf verschiedenen Geräten wie erwartet angezeigt werden.  Text muss mithilfe von Größe und Zeilenhöhe leicht lesbar sein.  Benutzer können die Größe von Schriftarten an die individuellen Anforderungen anpassen.  In Situationen, in denen bestimmte Schriftarten auf einem Benutzergerät nicht verfügbar sind, sollten Sie Ausweichoptionen für Schriftarten bereitstellen.  

CSS bietet eine bessere Unterstützung für Typografie in den letzten Jahren.  Es stehen Dutzende verschiedener CSS-Einheiten zur Verfügung, um die Textgröße zu definieren.  Sie verfügen auch über mehrere CSS-Eigenschaften, die sich auf Schriftgrad, Abstand, Zeilenhöhe und andere typografische Features auswirken.  

Um das Arbeiten mit Typografie zu vereinfachen, befindet sich jetzt ein visueller **Schriftarten-Editor** im **Formatvorlagenbereich.**  Sie können Ihre Schriftarteinstellungen ändern, und die Änderungen werden sofort im Browser gerendert.  Alles ohne ausführliche Kenntnisse von CSS.  

Derzeit ist **das Neue Schriftarten-Editor-Tool** im Formatvorlagenbereichsfeature experimentell, und Sie müssen es für [Microsoft Edge Developer Tools aktivieren.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  

Alle CSS **** im Formatvorlagenbereich, entweder Schriftartdefinitionen oder Inlineformatvorlagen, zeigen automatisch ein Symbol an, das den visuellen **Schriftarten-Editor öffnet.**  Wählen Sie zum Öffnen des **visuellen Schriftarten-Editors**das **Symbol "Schriftart-Editor"** aus.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Das Symbol im Formatvorlagenbereich zum Bearbeiten von Schriftarteinstellungen" lightbox="../media/font-editor-icon.msft.png":::
         Das Symbol **** im Formatvorlagenbereich zum Bearbeiten von Schriftarteinstellungen  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Der Schriftarten-Editor, der oben im Formatvorlagenbereich geöffnet wird" lightbox="../media/font-editor-open.msft.png":::
         Der **Schriftarten-Editor,** der oben im **Formatvorlagenbereich geöffnet** wird  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Alle Felder im visuellen **Schriftarten-Editor** werden aus den Werten im CSS im **Formatvorlagenbereich** aufgefüllt.  Die Definition wird beispielsweise im Formatvorlagenbereich festgelegt, sodass das Textfeld für die Zeilenhöhe angezeigt wird `line-height` `160%` und das **** `160` Einheitendropdown angezeigt `%` wird.  Außerdem wird der Schieberegler automatisch so festgelegt, dass er mit den Werten des Textfelds übereinstimmen kann.  

Der **Schriftarten-Editor** besteht aus zwei Teilen: der Schriftartfamilienauswahl und dem CSS-Eigenschaften-Editor.  

## Die Schriftartfamilienauswahl  

Die Schriftartfamilienauswahl ist der obere Teil des visuellen **Schriftarten-Editors.**  Um die Schriftarten der CSS-Regel auszuwählen, **** verwenden Sie im CSS-Editor die Schriftartfamilienauswahl.  Sie können Haupt- und Fallbackschriftarten für jede CSS-Regel auswählen.  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="The Font Editor open on top of the Styles pane with the Font Family selector highlighted" lightbox="../media/font-editor-font-family.msft.png":::
   The **Font Editor** open on top of the **Styles** pane with the Font **Family** selector highlighted  
:::image-end:::  

Verwenden Sie das **Dropdownmenü** "Schriftartfamilie", um aus einer Liste von Schriftarten zu wählen.  Schriftarten sind in vier Gruppen unterteilt.  

1.  Berechnete Schriftarten, die im Stylesheet im Formatvorlagenbereich **verfügbar** sind.  
1.  Systemschriftarten, bei denen es sich um die Schriftarten handelt, die unter dem aktuellen Betriebssystem verfügbar sind.  
1.  Generische Schriftfamilien, z. B. `serif` oder `sans-serif` .  
1.  Globale Werte, z. B. `inherit` `initial` , und `unset` .  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="The font editor open on top of the Styles pane with the Font Family selector highlighted" lightbox="../media/font-editor-font-family-list.msft.png":::
   The **Font Editor** open on top of the **Styles** pane with the Font **Family** selector highlighted  
:::image-end:::  

Nachdem Sie eine Schriftart ausgewählt haben, wird ein weiteres Dropdownmenü angezeigt, in dem Sie Ausweichschriftarten auswählen können.  Sie können bis zu acht Ausweichschriftarten auswählen.  Um eine Schriftart zu entfernen, wählen Sie das Symbol **"Schriftartfamilie löschen"** aus.  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> Wenn Sie einen globalen Wert für die Schriftartfamilie auswählen, erhalten Sie kein weiteres Dropdown, da es kein Fallback dafür in CSS gibt.  

## Der Editor für DIE CSS-Eigenschaften  

Sie können die Eigenschaften der CSS-Schriftart im unteren Teil des visuellen **Schriftarten-Editors ändern.**  Sie können den Schriftgrad, die Zeilenhöhe, die Schriftgewichtung und den Buchstabenabstand mithilfe eines der Benutzeroberflächensteuerelemente ändern.  Ihre Änderungen werden sofort im Browser angewendet.  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="Der Schriftarten-Editor, der oben im Formatvorlagenbereich geöffnet wird, mit hervorgehobenen CSS-Eigenschaften" lightbox="../media/font-editor-css-properties.msft.png":::
   The **Font Editor** open on top of the **Styles** pane with the CSS properties highlighted  
:::image-end:::  

Sie können auch mit dem visuellen Schriftarten-Editor **CSS-Einheiten konvertieren.**  Beispielsweise können Sie das Tool für eine CSS-Regel verwenden, bei der der **Schieberegler** für den Schriftgrad anfänglich auf festgelegt `16 pixels` ist.  Verwenden Sie nun das Einheitendropdown, und wählen Sie den Wert `em` aus.  Der `1 em` angezeigte Wert ist gleich `16 pixels` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Ändern des Schriftgrads in 16 Pixel" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         Ändern des Schriftgrads in `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Öffnen Sie das Einheitendropdown, um es in em zu konvertieren." lightbox="../media/font-editor-converted-to-em.msft.png":::
         Öffnen Sie das Einheitendropdown, in das konvertiert werden soll. `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Das Einheitendropdown enthält alle verfügbaren numerischen CSS-Einheiten.  Schriftgrad, Zeilenhöhe, Schriftgrad und Abstand verwenden unterschiedliche Einheiten.  Wenn die Textfelder den Fokus haben, können Sie die Und-Tasten auswählen, `arrow up` um Ihre Einstellungen zu `arrow down` optimieren.  Um die Schieberegler mit einer Tastatur zu verwenden, wählen Sie die Tasten `arrow left` und die `arrow down` Tasten aus.  

Der Editor für CSS-Eigenschaften enthält auch vordefinierte Schlüsselwörter.  Um die voreingestellten Schlüsselwörter zu verwenden, wählen Sie auf der rechten Seite das Symbol `Toggle Input Type` aus.  Die Benutzeroberfläche ändert sich, und es wird eine Dropdownliste mit vordefinierten Schlüsselwörtern angezeigt.  Um mit dem Schieberegler und anderen Benutzeroberflächensteuerelementen zur Benutzeroberfläche zurückzukehren, wählen Sie das `Toggle Input Type` Symbol erneut aus.  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Öffnen der voreingestellten Schlüsselwortschnittstelle" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   Öffnen der voreingestellten Schlüsselwortschnittstelle  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium)-Entwicklertools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Experimentelle Features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Aktivieren experimenteller Features – experimentelle Features | Microsoft Docs"  
