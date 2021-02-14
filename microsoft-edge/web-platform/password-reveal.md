---
description: Enthält Anleitungen zum Anpassen der Anzeige der Schaltfläche für die Kennwortanzeige
title: Anpassen der Schaltfläche zum Ein-/Aus-/Einsenten von Kennwörtern
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Kompatibilität, Webplattform, Kennwort-Reveal, Augensymbol
ms.openlocfilehash: af8120aad7316ffc051113591e770fa913814eb3
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327717"
---
# Anpassen der Schaltfläche zum Ein-/Aus-/Einsenten von Kennwörtern  

Der `password` Eingabetyp in Microsoft Edge enthält ein **Kennwort-Reveal-Steuerelement.**  Ein Benutzer kann die **Kennworteingabeschaltfläche** auswählen, um das **Kennwortfeld einzugeben.**  Das Feld **mit den angezeigten** Kennwörtern hilft dem Benutzer zu überprüfen, ob das Kennwort korrekt ist.  Nachdem ein Benutzer Text **** in das Kennwortfeld eingegeben **** hat, kann ein Benutzer die Schaltfläche zum Ein-/Aus-/Ein-/Aus-Kennwort auswählen oder die Sichtbarkeit `Alt` + `F8` der Eingabe umschalten.  

:::row:::
   :::column span="":::
      Ein **Kennwortfeld** mit Punkten, in dem die von einem Benutzer eingegebenen Zeichen verborgen sind.  Die **Schaltfläche zum Einblenden** des Kennworts wird rechts neben dem **Kennwortfeld** angezeigt.
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden." lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Schalten Sie die Schaltfläche **zum Anzeigen** des Kennworts um, um das Augensymbol in ein Augensymbol mit einem Schrägstrich zu ändern und den ursprünglichen Kennworttext einzugeben.  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt." lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt. :::image-end:::  
   :::column-end:::
:::row-end:::  

Standardmäßig wird die Schaltfläche zum Anzeigen **des** Kennworts in das Schatten-DOM aller HTML-Elemente eingefügt, deren `input` Set auf `type` `"password"` .  Ab Microsoft Edge Version 87 können Benutzer [oder][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] Unternehmen dieses Feature global deaktivieren.  Sie, Webdesigner und Entwickler, sollten erwarten, dass die meisten Microsoft Edge-Benutzer die Standarderfahrung haben.  

## Entfernen des Kennwort-Reveal-Steuerelements  

Sie können die **** Schaltfläche zum Ein-/Aus-Kennwort vollständig entfernen, indem Sie das `::-ms-reveal` Pseudoelement als Ziel festlegen.  

```css
::-ms-reveal {
    display: none;
}
```  

Sie sollten jedoch in Betracht ziehen, die Schaltfläche zum Ein-/Aus-/Ein-/Aus-Kennwort **zu** nutzen.  Die **systemeigene Schaltfläche zum** Ein-/Aus-/Einsenten von Kennwörtern verfügt über wichtige Sicherheitsmaßnahmen, [die](#visibility-of-the-control) in das Verhalten integrierten sind.  

## Anpassen des Steuerelementstils  

Anstatt das Steuerelement vollständig zu entfernen, können **** Sie stattdessen das Format der Schaltfläche zum Ein-/Ein-/Aus-Kennwort so ändern, dass es besser an die visuelle Sprache der Website anpasst.  Der folgende Codeausschnitt enthält ein Beispiel für eine solche Formatierung.  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

Beachten Sie die folgenden Punkte, **** wenn Sie die Schaltfläche zum Ein-/Aus-/Ein-/Aus-Kennwort formatiern.  

*   Das Augensymbol wird als Hintergrundbild implementiert.  Verwenden Sie zum Hinzufügen **** einer Hintergrundfarbe zur Schaltfläche zum Ein-/Aus reveal-Kennwort die CSS-Eigenschaft `background-color` anstelle der `background` Kurzhandeigenschaft.  
*   Sie können die Größe und Skalierung der Schaltfläche zum Ein-/Aus-/Einfing **von Kennwörtern** anpassen.  
    
    > [!NOTE]
    >Der Browser blendet alle Überläufe außerhalb der Grenzen des Kennworteingabesteuerelements aus.  
    
*   Derzeit sind keine Zustands selektoren verfügbar, um den Umschaltzustand der Schaltfläche zum Ein-/Aus-/Einschalten des **Kennworts zu** formatieren.  
    
## Sichtbarkeit des Steuerelements  

Die **Schaltfläche "Kennwort ein** reveal" ist erst verfügbar, wenn der Benutzer Text in das **Kennwortfeld ein eingeben** kann.  Um die Kennworteingabe des Benutzers zu schützen, unterdrückt der Browser die Schaltfläche in den folgenden Szenarien.

*   Wenn sich der Fokus vom Kennwortfeld **entfernt,** entfernt der Browser die Schaltfläche **zum Anzeigen des** Kennworts.  
*   Wenn Skripts das **Kennwortfeld** ändern, entfernt der Browser die Schaltfläche **zum Anzeigen von** Kennwörtern.  
*   Wenn ein Benutzer die Schaltfläche zum Anzeigen von Kennwörtern **** entfernt, **** muss der Benutzer den Inhalt des Kennwortfelds löschen, bevor die Schaltfläche zum Anzeigen des Kennworts erneut angezeigt wird. ****  
    
    > [!NOTE]
    > Dieses Feature verhindert, dass jemand eine geringfügige Anpassung zum Anzeigen des Kennworts vor sich hat, wenn der Benutzer von einem entsperrten Gerät entfernt wird.
    
Die **Schaltfläche "Kennwort ein** **** reveal" ist nicht verfügbar, wenn das Kennwortfeld mithilfe des Kennwort-Managers automatisch ausgefüllt wird.  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled – Microsoft Edge – Richtlinien | Microsoft Docs"  
