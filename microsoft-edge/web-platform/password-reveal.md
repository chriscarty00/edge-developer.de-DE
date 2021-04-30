---
description: Enthält Anleitungen zum Anpassen der Anzeige der Schaltfläche für die Kennwortanzeige
title: Anpassen der Schaltfläche zum Einhüllen von Kennwörtern
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, password reveal, eye icon
ms.openlocfilehash: 93f618d28e5fa2f16dda87b4122a097ef40618c9
ms.sourcegitcommit: 1f0b2534b51417bb19d05945fea54ddad977e88f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526158"
---
# <a name="customize-the-password-reveal-button"></a>Anpassen der Schaltfläche zum Einhüllen von Kennwörtern  

Der `password` Eingabetyp in Microsoft Edge enthält ein **Kennwort-Einschlusssteuerelement.**  Ein Benutzer kann die **Kennworteingabeschaltfläche** auswählen, um das **Kennwortfeld einzugeben.**  Das Feld **"Gedeckte** Kennwörter" hilft dem Benutzer zu überprüfen, ob das Kennwort korrekt ist.  Nachdem ein Benutzer Text **** in das Kennwortfeld eingegeben **** hat, kann ein Benutzer die Schaltfläche "Kennwort ein- oder auswählen" auswählen, um die Sichtbarkeit `Alt` + `F8` der Eingabe umschalten zu können.  

:::row:::
   :::column span="":::
      Ein **Kennwortfeld** mit Punkten, die die von einem Benutzer eingegebenen Zeichen ausblenden.  Die **Schaltfläche** zum Einblenden von Kennwörtern wird rechts neben dem **Kennwortfeld** angezeigt.
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Umschalten **** Sie die Schaltfläche zum Anzeigen des Kennworts, um das Augensymbol in ein Augensymbol mit einem Schrägstrich zu ändern und den ursprünglichen Kennworttext einzugeben.  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt." lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt. :::image-end:::  
   :::column-end:::
:::row-end:::  

Standardmäßig wird die Schaltfläche **für die** Kennwortentsprechung in das Schatten-DOM aller HTML-Elemente mit dem Set `input` auf `type` `"password"` eingefügt.  Ab Microsoft Edge Version 87 [][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] können Benutzer oder Unternehmen dieses Feature global deaktivieren.  Sie, Webdesigner und Entwickler, sollten erwarten, dass die meisten Microsoft Edge-Benutzer die Standarderfahrung haben.  

## <a name="remove-the-password-reveal-control"></a>Entfernen des Kennwort-Einschlusssteuerelements  

Sie können die Schaltfläche zum Ein- und **Ausschalten des** Kennworts vollständig entfernen, indem Sie auf das `::-ms-reveal` Pseudoelement zielen.  

```css
::-ms-reveal {
    display: none;
}
```  

Sie sollten jedoch erwägen, die Schaltfläche "Kennwort **einzugeben" zu** nutzen.  Die Native **Password Reveal-Schaltfläche** verfügt über wichtige [Sicherheitsmaßnahmen, die](#visibility-of-the-control) in das Verhalten integrierte sind.  

## <a name="customize-the-control-style"></a>Anpassen der Steuerelementart  

Anstatt das Steuerelement vollständig zu entfernen, können **** Sie stattdessen das Format der Schaltfläche für die Kennwortenthüllen ändern, um besser mit der visuellen Sprache der Website zu übereinstimmen.  Der folgende Codeausschnitt enthält ein Beispiel für eine solche Formatierung.  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

Beachten Sie die folgenden Punkte, wenn Sie die Schaltfläche zum Ein- und **Auslassen von Kennwörtern** formatiern.  

*   Das Augensymbol wird als Hintergrundbild implementiert.  Verwenden Sie die CSS-Eigenschaft anstelle der **** `background-color` Shorthand-Eigenschaft, um der Schaltfläche für die Kennwortentblichung eine `background` Hintergrundfarbe hinzuzufügen.  
*   Sie können die Größe und Skalierung der Schaltfläche für die **Kennwortentbung** anpassen.  
    
    > [!NOTE]
    >Der Browser blendet alle Überläufe außerhalb der Grenzen des Kennworteingabesteuerelements aus.  
    
*   Zurzeit sind keine Statusauswahlen verfügbar, um den Umschaltstatus der Schaltfläche zum Ein- und Ausschalten des **Kennworts zu** formatieren.  
    
## <a name="visibility-of-the-control"></a>Sichtbarkeit des Steuerelements  

Die **Schaltfläche für** die Kennwortentsprechung ist erst verfügbar, wenn der Benutzer Text in das **Kennwortfeld einzugeben** hat.  Um die Kennworteingabe des Benutzers zu schützen, unterdrückt der Browser die Schaltfläche in den folgenden Szenarien.

*   Wenn sich der Fokus vom **Kennwortfeld entfernt,** entfernt der Browser die Schaltfläche zur Kennwortentsprechung. ****  
*   Wenn Skripts das **Kennwortfeld** ändern, entfernt der Browser die Schaltfläche zur Kennwortentsprechung. ****  

Wenn die Schaltfläche "Kennwortanzeige" entfernt wird, **** muss der Benutzer den Inhalt des Kennwortfelds löschen, bevor die Schaltfläche "Kennwortanzeige" erneut angezeigt wird. **** **** Dieses Verhalten hindert einen Benutzer daran, eine geringfügige Anpassung an die Anzeige des Kennworts zu vornehmen, falls der Benutzer von einem entsperrten Gerät entfernt wird.
    
Die **Schaltfläche für** die Kennwortentsprechung ist nicht verfügbar, wenn das Kennwortfeld mithilfe des Kennwort-Managers automatisch ausgefüllt wird. ****  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled – Microsoft Edge – Richtlinien | Microsoft Docs"  
