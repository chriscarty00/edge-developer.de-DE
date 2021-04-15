---
description: Wenn Sie die gleichen JavaScript-Ausdrücke wiederholt in die Konsole eingeben, versuchen Sie es stattdessen mit Live-Ausdrücken.
title: Beobachten von JavaScript-Ausdruckswerten in Echtzeit mit Live-Ausdrücken
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 51b7aa5119775f43861a84c1055ac9149a626d8a
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483135"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a><span data-ttu-id="747f8-104">Überwachen von Änderungen in JavaScript mithilfe von Liveausdrücken</span><span class="sxs-lookup"><span data-stu-id="747f8-104">Monitor changes in JavaScript using Live Expressions</span></span>  

<span data-ttu-id="747f8-105">**Live-Ausdrücke** sind eine hervorragende Möglichkeit, um JavaScript-Ausdrücke zu überwachen, die sich sehr ändern.</span><span class="sxs-lookup"><span data-stu-id="747f8-105">**Live Expressions** are an excellent way to monitor JavaScript expressions that change a lot.</span></span>    <span data-ttu-id="747f8-106">Anstatt viele Konsolennachrichten zu lesen und zu navigieren, können Sie Ihre spezifischen JavaScript-Ausdrücke am oberen Rand der Konsole **anheften.**</span><span class="sxs-lookup"><span data-stu-id="747f8-106">Instead of having many Console messages to read and navigate, you may pin your specific JavaScript expressions to the top of the **Console**.</span></span>  

## <a name="add-a-new-live-expression"></a><span data-ttu-id="747f8-107">Hinzufügen eines neuen Liveausdrucks</span><span class="sxs-lookup"><span data-stu-id="747f8-107">Add a new live expression</span></span>  

<span data-ttu-id="747f8-108">Wählen Sie zu Beginn die Schaltfläche **Liveausdruck** erstellen \(Eye\) neben dem **Textfeld Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="747f8-108">To start, choose the **Create live expression** \(eye\) button next to the **Filter** textbox.</span></span>  <span data-ttu-id="747f8-109">Nachdem Sie ihn auswählen, wird ein Textfeld angezeigt, in das Sie Ihren neuen Ausdruck eingeben können.</span><span class="sxs-lookup"><span data-stu-id="747f8-109">After you choose it, a textbox is displayed for you to enter your new expression in it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Wählen Sie die Schaltfläche Neuer Liveausdruck aus, um ein Textfeld zum Eingeben eines Ausdrucks zu öffnen." lightbox="../media/console-live-expressions-new.msft.png":::
    <span data-ttu-id="747f8-111">Klicken Sie `New live expression` auf die Schaltfläche, um ein Textfeld zum Eingeben eines Ausdrucks zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="747f8-111">Choose the `New live expression` button to open a textbox to type an expression</span></span>  
:::image-end:::  

<span data-ttu-id="747f8-112">**Live-Ausdrücke** können ein beliebiger gültiger JavaScript-Ausdruck sein.</span><span class="sxs-lookup"><span data-stu-id="747f8-112">**Live Expressions** may be any valid JavaScript expression.</span></span>  <span data-ttu-id="747f8-113">Führen Sie die folgenden Aktionen aus, um dies zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="747f8-113">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="747f8-114">Öffnen Sie das **Textfeld Live Expression.**</span><span class="sxs-lookup"><span data-stu-id="747f8-114">Open the **Live Expression** textbox.</span></span>  
1.  <span data-ttu-id="747f8-115">Geben Sie `document.activeElement` ein.</span><span class="sxs-lookup"><span data-stu-id="747f8-115">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="747f8-116">Führen Sie zum Speichern des Ausdrucks eine der folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="747f8-116">To save the expression, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="747f8-117">Wählen `Control` + `Enter` Sie \(Windows, Linux\) oder `Command` + `Enter` \(macOS\) aus.</span><span class="sxs-lookup"><span data-stu-id="747f8-117">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    *   <span data-ttu-id="747f8-118">Wählen Sie außerhalb des **Textfelds Live Expression** aus.</span><span class="sxs-lookup"><span data-stu-id="747f8-118">Choose outside the **Live Expression** textbox.</span></span>  
        
<span data-ttu-id="747f8-119">Der Ausdruck ist jetzt live und wird `body` als Ergebnis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="747f8-119">The expression is now live and displays `body` as the result.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="Liveausdruck für document.activeElement zeigt text als Ergebnis an" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    <span data-ttu-id="747f8-121">Liveausdruck für `document.activeElement` den Anzeigetext als Ergebnis</span><span class="sxs-lookup"><span data-stu-id="747f8-121">Live expression for `document.activeElement` displays body as the result</span></span>  
:::image-end:::  

<span data-ttu-id="747f8-122">Wenn Sie auf der Webseite navigieren, ändert sich der Wert.</span><span class="sxs-lookup"><span data-stu-id="747f8-122">If you navigate around the webpage, the value changes.</span></span>  <span data-ttu-id="747f8-123">In der folgenden Abbildung öffnen Sie beispielsweise das Suchmenü auf der Webseite, und der Ausdruck wird nun `button.nav-bar-button.focus-visible` als Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="747f8-123">For example, in the following figure you open the search menu in the webpage and the expression now displays `button.nav-bar-button.focus-visible` as the value.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Um den Wert des Liveausdrucks zu ändern, interagieren Sie mit verschiedenen Elementen auf der Webseite" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    <span data-ttu-id="747f8-125">Um den Wert des Liveausdrucks **zu ändern,** interagieren Sie mit verschiedenen Elementen auf der Webseite</span><span class="sxs-lookup"><span data-stu-id="747f8-125">To change the value of the **Live Expression**, interact with different elements on the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="747f8-126">Um den Wert erneut zu ändern, öffnen Sie das Textfeld Suchen auf der Webseite.</span><span class="sxs-lookup"><span data-stu-id="747f8-126">To change the value again, open and choose the Search textbox on the webpage.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Navigieren Sie zu einem anderen Element auf der Webseite, um den Liveausdruck zu aktualisieren." lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    <span data-ttu-id="747f8-128">Navigieren Sie zu einem anderen Element auf der Webseite, um den **Liveausdruck zu aktualisieren.**</span><span class="sxs-lookup"><span data-stu-id="747f8-128">Navigate to a different element in the webpage to update the **Live Expression**</span></span>  
:::image-end:::  

## <a name="remove-live-expressions"></a><span data-ttu-id="747f8-129">Entfernen von Liveausdrücken</span><span class="sxs-lookup"><span data-stu-id="747f8-129">Remove Live Expressions</span></span>  

<span data-ttu-id="747f8-130">Ein **Live-Ausdruck** ist verfügbar, solange Sie ihn aktiv halten.</span><span class="sxs-lookup"><span data-stu-id="747f8-130">A **Live Expression** is available as long as you keep it active.</span></span>  <span data-ttu-id="747f8-131">Wählen Sie den nächsten Ausdruck aus, um einen **Liveausdruck** `x` zu loswerden.</span><span class="sxs-lookup"><span data-stu-id="747f8-131">To get rid of a **Live Expression**, choose the `x` next to it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Um Liveausdrücke zu entfernen, wählen Sie das x daneben aus." lightbox="../media/console-live-expressions-remove.msft.png":::
    <span data-ttu-id="747f8-133">Wählen Sie zum Entfernen von **Liveausdrücken** `x` den nächsten aus.</span><span class="sxs-lookup"><span data-stu-id="747f8-133">To remove **Live Expressions**, choose the `x` next to it</span></span>  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a><span data-ttu-id="747f8-134">Ersetzen der Konsolenprotokollierung durch Liveausdrücke</span><span class="sxs-lookup"><span data-stu-id="747f8-134">Replace Console logging with Live Expressions</span></span>  

<span data-ttu-id="747f8-135">Sie können so viele Ausdrücke erstellen, wie Sie möchten, und die einzelnen Ausdrücke in Browsersitzungen und Fenstern beibehalten.</span><span class="sxs-lookup"><span data-stu-id="747f8-135">You may create as many expressions as you want and persist each across browser sessions and windows.</span></span>  <span data-ttu-id="747f8-136">**Live-Ausdrücke** sind eine Möglichkeit, das Rauschen in Ihrem Debugworkflow zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="747f8-136">**Live Expressions** are a way to cut down on noise in your debugging workflow.</span></span>  

<span data-ttu-id="747f8-137">Beispielsweise möchten Sie die Mausbewegung auf der aktuellen Webseite überwachen.</span><span class="sxs-lookup"><span data-stu-id="747f8-137">For example, you want to monitor the mouse movement in the current webpage.</span></span>  <span data-ttu-id="747f8-138">Navigieren Sie [zu Protokollierungs-Mausbewegungsdemo,][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]öffnen Sie die **Konsole,** und bewegen Sie die Maus, um die Protokolle mit vielen Informationen angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="747f8-138">Navigate to [Logging Mouse Movement demo][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml], open the **Console**, and move your mouse around to display the logs with a lot of information.</span></span>  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="Konsole zeigt viele Informationen zur Mausposition an" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    <span data-ttu-id="747f8-140">**Konsole** zeigt viele Informationen zur Mausposition an</span><span class="sxs-lookup"><span data-stu-id="747f8-140">**Console** displays much information on mouse position</span></span>  
:::image-end:::  

<span data-ttu-id="747f8-141">Die große Menge an Informationen verlangsamt nicht nur den Debugprozess, sondern macht es auch einfach, die Änderungen zu verpassen, die Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="747f8-141">The large amount of information not only slows your debug process, but also makes it easy to miss the changes you want to review.</span></span>  <span data-ttu-id="747f8-142">Wenn die **Konsole** weitere Nachrichten anzeigt und Sie die Maus bewegen, werden die Werte, die Sie überprüfen möchten, vom Bildschirm gescrollt.</span><span class="sxs-lookup"><span data-stu-id="747f8-142">As the **Console** displays more messages and you move your mouse, the values you want to review scroll off the screen.</span></span>  

<span data-ttu-id="747f8-143">Führen Sie die folgenden Aktionen aus, um **Liveausdrücke** als Alternative zu testen.</span><span class="sxs-lookup"><span data-stu-id="747f8-143">To try **Live Expressions** as an alternative, complete the following actions.</span></span>  

1.  <span data-ttu-id="747f8-144">Navigieren Sie zur [Mausbewegung, ohne demo protokollieren zu müssen.][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]</span><span class="sxs-lookup"><span data-stu-id="747f8-144">Navigate to the [Mouse movement without logging demo][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].</span></span>  
1.  <span data-ttu-id="747f8-145">Erstellen **von Liveausdrücken** für `x` und `y` .</span><span class="sxs-lookup"><span data-stu-id="747f8-145">Create **Live Expressions** for `x` and `y`.</span></span>  
    
<span data-ttu-id="747f8-146">Wenn Sie **Liveausdrücke verwenden,** erhalten Sie immer die Informationen \*\*\*\* auf demselben Bildschirmteil und behalten Konsolenprotokolle für Werte bei, die sich nicht so stark ändern.</span><span class="sxs-lookup"><span data-stu-id="747f8-146">When you use **Live Expressions**, you always get the information on the same part of your screen and keep **Console** logs for values that don't change as much.</span></span>

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Anzeigen der x- und y-Position der Maus als Liveausdrücke" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    <span data-ttu-id="747f8-148">Anzeigen der `x` Position und der Maus als `y` **Liveausdrücke**</span><span class="sxs-lookup"><span data-stu-id="747f8-148">Display the `x` and `y` position of the mouse as **Live Expressions**</span></span>  
:::image-end:::  

<span data-ttu-id="747f8-149">**Liveausdrücke** werden ausschließlich auf Ihrem Computer ausgeführt, und Sie müssen nichts in Ihrem Code ändern, um ihn anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="747f8-149">**Live Expressions** run exclusively on your computer and you don't need to change anything in your code to display.</span></span>  <span data-ttu-id="747f8-150">**Live-Ausdrücke** sind eine hervorragende Möglichkeit, um sicherzustellen, dass Sie nur die Informationen anzeigen, die Sie debuggen möchten.</span><span class="sxs-lookup"><span data-stu-id="747f8-150">**Live Expressions** are a great way to ensure that you only display the information you want to debug.</span></span>  <span data-ttu-id="747f8-151">Darüber hinaus **helfen Ihnen Live-Ausdrücke,** das Rauschen auf den Computern Ihrer Benutzer zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="747f8-151">Also, **Live Expressions** help you limit the noise on your users' computers.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="747f8-152">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="747f8-152">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Beispiele für Konsolenmeldungen: Verwenden von | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Mausbewegung ohne Protokollierung | GitHub"  
