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
# <a name="customize-the-password-reveal-button"></a><span data-ttu-id="5549e-104">Anpassen der Schaltfläche zum Einhüllen von Kennwörtern</span><span class="sxs-lookup"><span data-stu-id="5549e-104">Customize the password reveal button</span></span>  

<span data-ttu-id="5549e-105">Der `password` Eingabetyp in Microsoft Edge enthält ein **Kennwort-Einschlusssteuerelement.**</span><span class="sxs-lookup"><span data-stu-id="5549e-105">The `password` input type in Microsoft Edge includes a **password reveal** control.</span></span>  <span data-ttu-id="5549e-106">Ein Benutzer kann die **Kennworteingabeschaltfläche** auswählen, um das **Kennwortfeld einzugeben.**</span><span class="sxs-lookup"><span data-stu-id="5549e-106">A user may choose the **password input** button to reveal the **password** field.</span></span>  <span data-ttu-id="5549e-107">Das Feld **"Gedeckte** Kennwörter" hilft dem Benutzer zu überprüfen, ob das Kennwort korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="5549e-107">The revealed **password** field helps the user verify if the password is correctly.</span></span>  <span data-ttu-id="5549e-108">Nachdem ein Benutzer Text \*\*\*\* in das Kennwortfeld eingegeben \*\*\*\* hat, kann ein Benutzer die Schaltfläche "Kennwort ein- oder auswählen" auswählen, um die Sichtbarkeit `Alt` + `F8` der Eingabe umschalten zu können.</span><span class="sxs-lookup"><span data-stu-id="5549e-108">After a user has entered text in the **password** field, a user may choose the **password reveal** button or select `Alt`+`F8` to toggle visibility of the input.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5549e-109">Ein **Kennwortfeld** mit Punkten, die die von einem Benutzer eingegebenen Zeichen ausblenden.</span><span class="sxs-lookup"><span data-stu-id="5549e-109">A **password** field with dots hiding the characters entered by a user.</span></span>  <span data-ttu-id="5549e-110">Die **Schaltfläche** zum Einblenden von Kennwörtern wird rechts neben dem **Kennwortfeld** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5549e-110">The **password reveal** button appears to the right of the **password** field.</span></span>
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         <span data-ttu-id="5549e-112">Das augenförmige Symbol wird neben den Punkten angezeigt, die den Kennworttext ausblenden</span><span class="sxs-lookup"><span data-stu-id="5549e-112">The eye-shaped icon appears next to the dots that hide the password text</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5549e-113">Umschalten \*\*\*\* Sie die Schaltfläche zum Anzeigen des Kennworts, um das Augensymbol in ein Augensymbol mit einem Schrägstrich zu ändern und den ursprünglichen Kennworttext einzugeben.</span><span class="sxs-lookup"><span data-stu-id="5549e-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span></span>  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt." lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         <span data-ttu-id="5549e-115">Das augenförmige Symbol hat einen Schrägstrich, und der ursprüngliche Kennworttext wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5549e-115">The The eye-shaped icon has a slash on it and the original password text is displayed</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5549e-116">Standardmäßig wird die Schaltfläche **für die** Kennwortentsprechung in das Schatten-DOM aller HTML-Elemente mit dem Set `input` auf `type` `"password"` eingefügt.</span><span class="sxs-lookup"><span data-stu-id="5549e-116">By default, the **password reveal** button inserts into the Shadow DOM of all HTML `input` elements with the `type` set to `"password"`.</span></span>  <span data-ttu-id="5549e-117">Ab Microsoft Edge Version 87 können Benutzer [][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] oder Unternehmen dieses Feature global deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5549e-117">Starting with Microsoft Edge Version 87, users or [enterprises][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] may disable this feature globally.</span></span>  <span data-ttu-id="5549e-118">Sie, Webdesigner und Entwickler, sollten erwarten, dass die Microsoft Edge Benutzer die Standarderfahrung haben.</span><span class="sxs-lookup"><span data-stu-id="5549e-118">You, web designers and developers, should expect most Microsoft Edge users to have the default experience.</span></span>  

## <a name="remove-the-password-reveal-control"></a><span data-ttu-id="5549e-119">Entfernen des Kennwort-Einschlusssteuerelements</span><span class="sxs-lookup"><span data-stu-id="5549e-119">Remove the password reveal control</span></span>  

<span data-ttu-id="5549e-120">Sie können die Schaltfläche zum Ein- und **Ausschalten des** Kennworts vollständig entfernen, indem Sie auf das `::-ms-reveal` Pseudoelement zielen.</span><span class="sxs-lookup"><span data-stu-id="5549e-120">You may completely remove the **password reveal** button by targeting the `::-ms-reveal` pseudo element.</span></span>  

```css
::-ms-reveal {
    display: none;
}
```  

<span data-ttu-id="5549e-121">Sie sollten jedoch erwägen, die Schaltfläche "Kennwort **einzugeben" zu** nutzen.</span><span class="sxs-lookup"><span data-stu-id="5549e-121">However, you should consider taking advantage of the **password reveal** button.</span></span>  <span data-ttu-id="5549e-122">Die Native **Password Reveal-Schaltfläche** verfügt über wichtige [Sicherheitsmaßnahmen, die](#visibility-of-the-control) in das Verhalten integrierte sind.</span><span class="sxs-lookup"><span data-stu-id="5549e-122">The native **password reveal** button has important [security measures](#visibility-of-the-control) built into the behavior.</span></span>  

## <a name="customize-the-control-style"></a><span data-ttu-id="5549e-123">Anpassen der Steuerelementart</span><span class="sxs-lookup"><span data-stu-id="5549e-123">Customize the control style</span></span>  

<span data-ttu-id="5549e-124">Anstatt das Steuerelement vollständig zu entfernen, können \*\*\*\* Sie stattdessen das Format der Schaltfläche für die Kennwortenthüllen ändern, um besser mit der visuellen Sprache der Website zu übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5549e-124">Instead of fully removing the control, you may instead modify the styling of the **password reveal** button to better match the visual language of the website.</span></span>  <span data-ttu-id="5549e-125">Der folgende Codeausschnitt enthält ein Beispiel für eine solche Formatierung.</span><span class="sxs-lookup"><span data-stu-id="5549e-125">The following snippet provides an example of such styling.</span></span>  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

<span data-ttu-id="5549e-126">Beachten Sie die folgenden Punkte, wenn Sie die Schaltfläche zum Ein- und **Auslassen von Kennwörtern** formatiern.</span><span class="sxs-lookup"><span data-stu-id="5549e-126">Keep the following things in mind when you style the **password reveal** button.</span></span>  

*   <span data-ttu-id="5549e-127">Das Augensymbol wird als Hintergrundbild implementiert.</span><span class="sxs-lookup"><span data-stu-id="5549e-127">The eye icon implements as a background image.</span></span>  <span data-ttu-id="5549e-128">Verwenden Sie die CSS-Eigenschaft anstelle der \*\*\*\* `background-color` Shorthand-Eigenschaft, um der Schaltfläche für die Kennwortentblichung eine `background` Hintergrundfarbe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5549e-128">To add a background color to the **password reveal** button, use the CSS `background-color` property instead of the `background` shorthand property.</span></span>  
*   <span data-ttu-id="5549e-129">Sie können die Größe und Skalierung der Schaltfläche für die **Kennwortentbung** anpassen.</span><span class="sxs-lookup"><span data-stu-id="5549e-129">You may adjust the size and scale of the **password reveal** button.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="5549e-130">Der Browser blendet alle Überläufe außerhalb der Grenzen des Kennworteingabesteuerelements aus.</span><span class="sxs-lookup"><span data-stu-id="5549e-130">The browser hides any overflow outside of the bounds of the password input control.</span></span>  
    
*   <span data-ttu-id="5549e-131">Zurzeit sind keine Statusauswahlen verfügbar, um den Umschaltstatus der Schaltfläche zum Ein- und Ausschalten des **Kennworts zu** formatieren.</span><span class="sxs-lookup"><span data-stu-id="5549e-131">Currently, no state selectors are available to style the toggled state of the **password reveal** button.</span></span>  
    
## <a name="visibility-of-the-control"></a><span data-ttu-id="5549e-132">Sichtbarkeit des Steuerelements</span><span class="sxs-lookup"><span data-stu-id="5549e-132">Visibility of the control</span></span>  

<span data-ttu-id="5549e-133">Die **Schaltfläche für** die Kennwortentsprechung ist erst verfügbar, wenn der Benutzer Text in das **Kennwortfeld einzugeben** hat.</span><span class="sxs-lookup"><span data-stu-id="5549e-133">The **password reveal** button is unavailable until the user enters text into the **password** field.</span></span>  <span data-ttu-id="5549e-134">Um die Kennworteingabe des Benutzers zu schützen, unterdrückt der Browser die Schaltfläche in den folgenden Szenarien.</span><span class="sxs-lookup"><span data-stu-id="5549e-134">To help keep the user's password entry secure, the browser suppresses the button in the following scenarios.</span></span>

*   <span data-ttu-id="5549e-135">Wenn sich der Fokus vom **Kennwortfeld entfernt,** entfernt der Browser die Schaltfläche zur Kennwortentsprechung. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5549e-135">If focus moves away from the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="5549e-136">Wenn Skripts das **Kennwortfeld** ändern, entfernt der Browser die Schaltfläche zur Kennwortentsprechung. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5549e-136">If scripts modify the **password** field, the browser removes the **password reveal** button.</span></span>  

<span data-ttu-id="5549e-137">Wenn die Schaltfläche "Kennwortanzeige" entfernt wird, \*\*\*\* muss der Benutzer den Inhalt des Kennwortfelds löschen, bevor die Schaltfläche "Kennwortanzeige" erneut angezeigt wird. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5549e-137">If the **password reveal** button is removed, the user must delete the contents of the **password** field before the **password reveal** button displays again.</span></span> <span data-ttu-id="5549e-138">Dieses Verhalten hindert einen Benutzer daran, eine geringfügige Anpassung an die Anzeige des Kennworts zu vornehmen, falls der Benutzer von einem entsperrten Gerät entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5549e-138">This behavior prevents someone from making a minor adjustment to display the password, should the user step away from an unlocked device.</span></span>
    
<span data-ttu-id="5549e-139">Die **Schaltfläche für** die Kennwortentsprechung ist nicht verfügbar, wenn das Kennwortfeld mithilfe des Kennwort-Managers automatisch ausgefüllt wird. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5549e-139">The **password reveal** button is unavailable if the **password** field autofills using the password manager.</span></span>  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Richtlinien | Microsoft Docs"  
