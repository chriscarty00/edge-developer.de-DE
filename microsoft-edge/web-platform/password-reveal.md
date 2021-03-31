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
# <span data-ttu-id="397a8-104">Anpassen der Schaltfläche zum Ein-/Aus-/Einsenten von Kennwörtern</span><span class="sxs-lookup"><span data-stu-id="397a8-104">Customize the password reveal button</span></span>  

<span data-ttu-id="397a8-105">Der `password` Eingabetyp in Microsoft Edge enthält ein **Kennwort-Reveal-Steuerelement.**</span><span class="sxs-lookup"><span data-stu-id="397a8-105">The `password` input type in Microsoft Edge includes a **password reveal** control.</span></span>  <span data-ttu-id="397a8-106">Ein Benutzer kann die **Kennworteingabeschaltfläche** auswählen, um das **Kennwortfeld einzugeben.**</span><span class="sxs-lookup"><span data-stu-id="397a8-106">A user may choose the **password input** button to reveal the **password** field.</span></span>  <span data-ttu-id="397a8-107">Das Feld **mit den angezeigten** Kennwörtern hilft dem Benutzer zu überprüfen, ob das Kennwort korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="397a8-107">The revealed **password** field helps the user verify if the password is correctly.</span></span>  <span data-ttu-id="397a8-108">Nachdem ein Benutzer Text  in das Kennwortfeld eingegeben  hat, kann ein Benutzer die Schaltfläche zum Ein-/Aus-/Ein-/Aus-Kennwort auswählen oder die Sichtbarkeit `Alt` + `F8` der Eingabe umschalten.</span><span class="sxs-lookup"><span data-stu-id="397a8-108">After a user has entered text in the **password** field, a user may choose the **password reveal** button or select `Alt`+`F8` to toggle visibility of the input.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="397a8-109">Ein **Kennwortfeld** mit Punkten, in dem die von einem Benutzer eingegebenen Zeichen verborgen sind.</span><span class="sxs-lookup"><span data-stu-id="397a8-109">A **password** field with dots hiding the characters entered by a user.</span></span>  <span data-ttu-id="397a8-110">Die **Schaltfläche zum Einblenden** des Kennworts wird rechts neben dem **Kennwortfeld** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="397a8-110">The **password reveal** button appears to the right of the **password** field.</span></span>
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden." lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         <span data-ttu-id="397a8-112">Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden.</span><span class="sxs-lookup"><span data-stu-id="397a8-112">The eye-shaped icon appears next to the dots that hide the password text</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="397a8-113">Schalten Sie die Schaltfläche **zum Anzeigen** des Kennworts um, um das Augensymbol in ein Augensymbol mit einem Schrägstrich zu ändern und den ursprünglichen Kennworttext einzugeben.</span><span class="sxs-lookup"><span data-stu-id="397a8-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span></span>  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt." lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         <span data-ttu-id="397a8-115">Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="397a8-115">The The eye-shaped icon has a slash on it and the original password text is displayed</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="397a8-116">Standardmäßig wird die Schaltfläche zum Anzeigen **des** Kennworts in das Schatten-DOM aller HTML-Elemente eingefügt, deren `input` Set auf `type` `"password"` .</span><span class="sxs-lookup"><span data-stu-id="397a8-116">By default, the **password reveal** button inserts into the Shadow DOM of all HTML `input` elements with the `type` set to `"password"`.</span></span>  <span data-ttu-id="397a8-117">Ab Microsoft Edge Version 87 können Benutzer [oder][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] Unternehmen dieses Feature global deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="397a8-117">Starting with Microsoft Edge Version 87, users or [enterprises][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] may disable this feature globally.</span></span>  <span data-ttu-id="397a8-118">Sie, Webdesigner und Entwickler, sollten erwarten, dass die meisten Microsoft Edge-Benutzer die Standarderfahrung haben.</span><span class="sxs-lookup"><span data-stu-id="397a8-118">You, web designers and developers, should expect most Microsoft Edge users to have the default experience.</span></span>  

## <span data-ttu-id="397a8-119">Entfernen des Kennwort-Reveal-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="397a8-119">Remove the password reveal control</span></span>  

<span data-ttu-id="397a8-120">Sie können die  Schaltfläche zum Ein-/Aus-Kennwort vollständig entfernen, indem Sie das `::-ms-reveal` Pseudoelement als Ziel festlegen.</span><span class="sxs-lookup"><span data-stu-id="397a8-120">You may completely remove the **password reveal** button by targeting the `::-ms-reveal` pseudo element.</span></span>  

```css
::-ms-reveal {
    display: none;
}
```  

<span data-ttu-id="397a8-121">Sie sollten jedoch in Betracht ziehen, die Schaltfläche zum Ein-/Aus-/Ein-/Aus-Kennwort **zu** nutzen.</span><span class="sxs-lookup"><span data-stu-id="397a8-121">However, you should consider taking advantage of the **password reveal** button.</span></span>  <span data-ttu-id="397a8-122">Die **systemeigene Schaltfläche zum** Ein-/Aus-/Einsenten von Kennwörtern verfügt über wichtige Sicherheitsmaßnahmen, [die](#visibility-of-the-control) in das Verhalten integrierten sind.</span><span class="sxs-lookup"><span data-stu-id="397a8-122">The native **password reveal** button has important [security measures](#visibility-of-the-control) built into the behavior.</span></span>  

## <span data-ttu-id="397a8-123">Anpassen des Steuerelementstils</span><span class="sxs-lookup"><span data-stu-id="397a8-123">Customize the control style</span></span>  

<span data-ttu-id="397a8-124">Anstatt das Steuerelement vollständig zu entfernen, können  Sie stattdessen das Format der Schaltfläche zum Ein-/Ein-/Aus-Kennwort so ändern, dass es besser an die visuelle Sprache der Website anpasst.</span><span class="sxs-lookup"><span data-stu-id="397a8-124">Instead of fully removing the control, you may instead modify the styling of the **password reveal** button to better match the visual language of the website.</span></span>  <span data-ttu-id="397a8-125">Der folgende Codeausschnitt enthält ein Beispiel für eine solche Formatierung.</span><span class="sxs-lookup"><span data-stu-id="397a8-125">The following snippet provides an example of such styling.</span></span>  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

<span data-ttu-id="397a8-126">Beachten Sie die folgenden Punkte,  wenn Sie die Schaltfläche zum Ein-/Aus-/Ein-/Aus-Kennwort formatiern.</span><span class="sxs-lookup"><span data-stu-id="397a8-126">Keep the following things in mind when you style the **password reveal** button.</span></span>  

*   <span data-ttu-id="397a8-127">Das Augensymbol wird als Hintergrundbild implementiert.</span><span class="sxs-lookup"><span data-stu-id="397a8-127">The eye icon implements as a background image.</span></span>  <span data-ttu-id="397a8-128">Verwenden Sie zum Hinzufügen  einer Hintergrundfarbe zur Schaltfläche zum Ein-/Aus reveal-Kennwort die CSS-Eigenschaft `background-color` anstelle der `background` Kurzhandeigenschaft.</span><span class="sxs-lookup"><span data-stu-id="397a8-128">To add a background color to the **password reveal** button, use the CSS `background-color` property instead of the `background` shorthand property.</span></span>  
*   <span data-ttu-id="397a8-129">Sie können die Größe und Skalierung der Schaltfläche zum Ein-/Aus-/Einfing **von Kennwörtern** anpassen.</span><span class="sxs-lookup"><span data-stu-id="397a8-129">You may adjust the size and scale of the **password reveal** button.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="397a8-130">Der Browser blendet alle Überläufe außerhalb der Grenzen des Kennworteingabesteuerelements aus.</span><span class="sxs-lookup"><span data-stu-id="397a8-130">The browser hides any overflow outside of the bounds of the password input control.</span></span>  
    
*   <span data-ttu-id="397a8-131">Derzeit sind keine Zustands selektoren verfügbar, um den Umschaltzustand der Schaltfläche zum Ein-/Aus-/Einschalten des **Kennworts zu** formatieren.</span><span class="sxs-lookup"><span data-stu-id="397a8-131">Currently, no state selectors are available to style the toggled state of the **password reveal** button.</span></span>  
    
## <span data-ttu-id="397a8-132">Sichtbarkeit des Steuerelements</span><span class="sxs-lookup"><span data-stu-id="397a8-132">Visibility of the control</span></span>  

<span data-ttu-id="397a8-133">Die **Schaltfläche "Kennwort ein** reveal" ist erst verfügbar, wenn der Benutzer Text in das **Kennwortfeld ein eingeben** kann.</span><span class="sxs-lookup"><span data-stu-id="397a8-133">The **password reveal** button is unavailable until the user enters text into the **password** field.</span></span>  <span data-ttu-id="397a8-134">Um die Kennworteingabe des Benutzers zu schützen, unterdrückt der Browser die Schaltfläche in den folgenden Szenarien.</span><span class="sxs-lookup"><span data-stu-id="397a8-134">To help keep the user's password entry secure, the browser suppresses the button in the following scenarios.</span></span>

*   <span data-ttu-id="397a8-135">Wenn sich der Fokus vom Kennwortfeld **entfernt,** entfernt der Browser die Schaltfläche **zum Anzeigen des** Kennworts.</span><span class="sxs-lookup"><span data-stu-id="397a8-135">If focus moves away from the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="397a8-136">Wenn Skripts das **Kennwortfeld** ändern, entfernt der Browser die Schaltfläche **zum Anzeigen von** Kennwörtern.</span><span class="sxs-lookup"><span data-stu-id="397a8-136">If scripts modify the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="397a8-137">Wenn ein Benutzer die Schaltfläche zum Anzeigen von Kennwörtern  entfernt,  muss der Benutzer den Inhalt des Kennwortfelds löschen, bevor die Schaltfläche zum Anzeigen des Kennworts erneut angezeigt wird. </span><span class="sxs-lookup"><span data-stu-id="397a8-137">If a user removes the **password reveal** button, the user must delete the contents of the **password** field before the **password reveal** button displays again.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="397a8-138">Dieses Feature verhindert, dass jemand eine geringfügige Anpassung zum Anzeigen des Kennworts vor sich hat, wenn der Benutzer von einem entsperrten Gerät entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="397a8-138">This feature prevents someone from making a minor adjustment to view the password, should the user step away from an unlocked device.</span></span>
    
<span data-ttu-id="397a8-139">Die **Schaltfläche "Kennwort ein**  reveal" ist nicht verfügbar, wenn das Kennwortfeld mithilfe des Kennwort-Managers automatisch ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="397a8-139">The **password reveal** button is unavailable if the **password** field autofills using the password manager.</span></span>  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled – Microsoft Edge – Richtlinien | Microsoft Docs"  
