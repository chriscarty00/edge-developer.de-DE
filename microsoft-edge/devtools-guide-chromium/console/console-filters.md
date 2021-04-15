---
description: Informationen zum Filtern von Konsolennachrichten
title: Erste Schritte mit dem Filtern von Nachrichten in der Konsole
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: b493bb790b48bc1c4dca0e6802d2f638099b7644
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483491"
---
# <a name="filter-console-messages"></a><span data-ttu-id="ff2c9-104">Filtern von Konsolennachrichten</span><span class="sxs-lookup"><span data-stu-id="ff2c9-104">Filter Console messages</span></span>  

<span data-ttu-id="ff2c9-105">Wenn Sie im Web surfen, finden Sie möglicherweise, dass die **Konsole** mit allen Arten von Informationen überflutet ist.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-105">When you surf the web, you may find the **Console** is flooded with all kinds of information.</span></span>  <span data-ttu-id="ff2c9-106">Häufig sind die Informationen für Sie nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-106">Often the information isn't relevant to you.</span></span>  <span data-ttu-id="ff2c9-107">Beispielsweise Informationen zum Liveprojekt, das ein anderer Entwickler beim Debuggen protokolliert hat.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-107">Such as information about the live project that another developer logged while you debug.</span></span>  <span data-ttu-id="ff2c9-108">Oder weitere Informationen zu Verstößen und Warnungen zur Leistung der aktuellen Website, die Sie nicht ändern können.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-108">Or more information about violations and warnings about the performance of the current site that you aren't able to change.</span></span>  <span data-ttu-id="ff2c9-109">Es ist sinnvoll, die Filteroptionen der Konsole zu **verwenden,** um das Rauschen zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-109">It makes sense to use the filter options of **Console** to reduce the noise.</span></span>  

## <a name="filter-by-log-level"></a><span data-ttu-id="ff2c9-110">Filtern nach Protokollebene</span><span class="sxs-lookup"><span data-stu-id="ff2c9-110">Filter by log level</span></span>  

<span data-ttu-id="ff2c9-111">Jeder Methode des Objekts `console` ist ein Schweregrad zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-111">Each method of the `console` object has a severity level attached to it.</span></span>  <span data-ttu-id="ff2c9-112">Die Schweregrade sind `Verbose` , `Info` , oder `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="ff2c9-112">The severity levels are `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="ff2c9-113">Anzeigen der Schweregrade in der [API-Dokumentation][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="ff2c9-113">Display the severity levels in the [API documentation][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="ff2c9-114">Beispielsweise handelt es sich um eine Nachricht `console.log()` `Info` auf Ebene, aber um eine `console.error()` Nachricht auf `Error` Ebene.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-114">For example, `console.log()` is an `Info`-level message, but `console.error()` is an `Error`-level message.</span></span>  

<span data-ttu-id="ff2c9-115">Verwenden Sie zum Filtern von Nachrichten in **der Konsole**das **Dropdownmenü Protokollebene.**</span><span class="sxs-lookup"><span data-stu-id="ff2c9-115">To filter messages in the **Console**, use the **Log Level** dropdown menu.</span></span>  <span data-ttu-id="ff2c9-116">Sie können den Status der einzelnen Ebenen umschalten.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-116">You may toggle the state of each level.</span></span>  <span data-ttu-id="ff2c9-117">Entfernen Sie das Häkchen neben jeder Ebene, um die einzelnen Ebenen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-117">To turn off each level, remove the checkmark next to each.</span></span>  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="Das Dropdownmenü filtert Konsolennachrichten mithilfe der Protokollebene" lightbox="../media/console-filter-dropdown.msft.png":::
    <span data-ttu-id="ff2c9-119">Das Dropdownmenü **filtert Konsolennachrichten** mithilfe der Protokollebene</span><span class="sxs-lookup"><span data-stu-id="ff2c9-119">The dropdown menu filters **Console** messages using the log level</span></span>  
:::image-end:::  

<span data-ttu-id="ff2c9-120">Da kein Filter angewendet wird, werden in der folgenden Abbildung Dutzende von Nachrichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-120">Since no filter is applied, the following figure displays dozens of messages.</span></span>  <span data-ttu-id="ff2c9-121">Reduzieren und verwalten Sie als Nächstes die Anzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-121">Next, reduce and manage the number of messages.</span></span>  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Kein Filtersatz bedeutet, dass Sie möglicherweise viele Konsolennachrichten anzeigen" lightbox="../media/console-filter-displays-all.msft.png":::
    <span data-ttu-id="ff2c9-123">Kein Filtersatz bedeutet, dass Sie möglicherweise viele Konsolennachrichten anzeigen</span><span class="sxs-lookup"><span data-stu-id="ff2c9-123">No filter set means you may display many console messages</span></span>  
:::image-end:::  

<span data-ttu-id="ff2c9-124">Wählen Sie aus, um alle Meldungen auf Warnungsebene auszublenden, um das Rauschen zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-124">Choose to hide all the Warning-level messages to cut down on the noise.</span></span>  <span data-ttu-id="ff2c9-125">Navigieren Sie zum **Dropdownmenü Protokollebenen,** und deaktivieren Sie die `Warnings` Stufe.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-125">Navigate to the **Log Levels** dropdown and uncheck the `Warnings` level.</span></span>  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Ausblenden aller Warnmeldungen in der Konsole, um einen großen Teil des Rauschens zu filtern" lightbox="../media/console-filter-hide-warning.msft.png":::
    <span data-ttu-id="ff2c9-127">Ausblenden aller Warnmeldungen in der **Konsole,** um einen großen Teil des Rauschens zu filtern</span><span class="sxs-lookup"><span data-stu-id="ff2c9-127">Hide all the warning level messages in the **Console** to filter much of the noise</span></span>  
:::image-end:::  

## <a name="filter-by-text"></a><span data-ttu-id="ff2c9-128">Filtern nach Text</span><span class="sxs-lookup"><span data-stu-id="ff2c9-128">Filter by text</span></span>  

<span data-ttu-id="ff2c9-129">Wenn Sie weitere Details überprüfen möchten, geben Sie zum Filtern von Nachrichten mithilfe von Text eine Zeichenfolge in das **Textfeld Filter** ein.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-129">If you want to review more detail, to filter messages using text, type a string into the **Filter** textbox.</span></span>  <span data-ttu-id="ff2c9-130">Geben Sie beispielsweise in das Feld ein, um nur Ihre Nachrichten über den Browser anzuzeigen, der das Laden `block` von Ressourcen blockiert.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-130">For example, type `block` into the box to only display your messages about the browser blocking resources from loading.</span></span>

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Zeigt die Nachrichten an, die den Wortblock enthalten" lightbox="../media/console-filter-text.msft.png":::
    <span data-ttu-id="ff2c9-132">Zeigt die Nachrichten an, die das Wort enthalten</span><span class="sxs-lookup"><span data-stu-id="ff2c9-132">Displays the messages that contain the word</span></span> `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a><span data-ttu-id="ff2c9-133">Filtern nach regulärem Ausdruck</span><span class="sxs-lookup"><span data-stu-id="ff2c9-133">Filter by regular expression</span></span>

<span data-ttu-id="ff2c9-134">[Reguläre Ausdrücke][MdnDocsWebJavascriptGuideRegularExpressions] sind eine leistungsstarke Möglichkeit zum Filtern von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-134">[Regular expressions][MdnDocsWebJavascriptGuideRegularExpressions] are a powerful way to filter messages.</span></span>  <span data-ttu-id="ff2c9-135">Geben Sie beispielsweise in das Textfeld Filter ein, um nur Nachrichten anzeigen zu `/^Tracking/` können, die mit dem Begriff \*\*\*\* `Tracking` beginnen.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-135">For example, type `/^Tracking/` into the **Filter** textbox to only displays messages that start with the term `Tracking`.</span></span>  <span data-ttu-id="ff2c9-136">Wenn Sie mit regulären Ausdrücken nicht vertraut sind, ist [RegExr][|::ref1::|Main] eine großartige Ressource, um mehr über die Verwendung regulärer Ausdrücke zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-136">If you're unfamiliar with regular expressions, [RegExr][|::ref1::|Main] is a great resource to learn about using regular expressions.</span></span>

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Zeigt die Nachrichten an, die mit dem Wortfilter beginnen, indem ein regulärer Ausdruck im Textfeld Filter verwendet wird." lightbox="../media/console-filter-regex.msft.png":::
    <span data-ttu-id="ff2c9-138">Zeigt die Nachrichten an, die mit dem Wort `filter` beginnen, indem ein regulärer Ausdruck im **Textfeld Filter** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-138">Displays the messages that start with the word `filter` using a regular expression in the **Filter** textbox</span></span>  
:::image-end:::  

## <a name="filter-by-message-source"></a><span data-ttu-id="ff2c9-139">Filtern nach Nachrichtenquelle</span><span class="sxs-lookup"><span data-stu-id="ff2c9-139">Filter by message source</span></span>  

<span data-ttu-id="ff2c9-140">Sie können auch definieren, welche Art von Nachrichten Sie anzeigen möchten und wo die einzelnen Nachrichten mit der **Sidebar der** Konsole **stammen.**</span><span class="sxs-lookup"><span data-stu-id="ff2c9-140">You may also define what kind of messages you want to display and where each originated using the **Sidebar** of the **Console**.</span></span>  <span data-ttu-id="ff2c9-141">Wählen Sie dazu die Schaltfläche **Konsolenseite anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-141">To do it, choose the **Show console sidebar** button.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Um die Seitenleiste zu öffnen, wählen Sie das Seitenleistensymbol aus." lightbox="../media/console-filter-sidebar-icon.msft.png":::
    <span data-ttu-id="ff2c9-143">Wählen Sie zum Öffnen **der Seitenleiste**die Schaltfläche **Konsolenseite anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-143">To open the **Sidebar**, choose the **Show console sidebar** button</span></span>  
:::image-end:::  

<span data-ttu-id="ff2c9-144">Wenn die **Seitenleiste** geöffnet ist, können Sie die Gesamtzahl der Nachrichten und den Ursprung der einzelnen Nachrichten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-144">When the **Sidebar** is open, you may display the overall number of messages and where each originated.</span></span>  <span data-ttu-id="ff2c9-145">Die Optionen sind `All messages` , , , , und `User Messages` `Errors` `Warnings` `Info` `Verbose` .</span><span class="sxs-lookup"><span data-stu-id="ff2c9-145">The options are `All messages`, `User Messages`, `Errors`, `Warnings`, `Info`, and `Verbose`.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="Auf der Konsolenseite werden die verschiedenen Quellen angezeigt, die von" lightbox="../media/console-filter-sidebar-open.msft.png":::
    <span data-ttu-id="ff2c9-147">Auf **der Konsolenseite werden** die verschiedenen Quellen angezeigt, die von</span><span class="sxs-lookup"><span data-stu-id="ff2c9-147">The **Console Sidebar** displays the different sources messages originated from</span></span>  
:::image-end:::  

<span data-ttu-id="ff2c9-148">Wählen Sie eine der Optionen aus, um nur die Nachrichten dieses Typs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-148">Choose any of the options to display only the messages of that type.</span></span>  <span data-ttu-id="ff2c9-149">Wenn Sie beispielsweise Benutzernachrichten anzeigen möchten, wählen Sie die Option Benutzernachrichten aus, um weniger Rauschen zu anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-149">For example, to display user messages, choose the user messages option to display less noise.</span></span>

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Wählen Sie aus, ob nur Benutzernachrichten in der Konsole mithilfe des Filters in der Seitenleiste angezeigt werden sollen." lightbox="../media/console-filter-select-user-messages.msft.png":::
    <span data-ttu-id="ff2c9-151">Wählen Sie aus, ob nur Benutzernachrichten in der **Konsole mithilfe** des Filters in der **Seitenleiste angezeigt werden sollen.**</span><span class="sxs-lookup"><span data-stu-id="ff2c9-151">Choose to display only user messages in the **Console** using the filter in the **Sidebar**</span></span>  
:::image-end:::  

<span data-ttu-id="ff2c9-152">Um mehr zu filtern und die Auswahl zu erweitern, wählen Sie das Dreiecksymbol daneben aus.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-152">To filter more and expand the choice, choose the triangle icon next to it.</span></span>  <span data-ttu-id="ff2c9-153">Auf diese Weise erhalten Sie mehr Auswahlmöglichkeiten, um nur Nachrichten anzeigen zu können, die von einer bestimmten Quelle stammen.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-153">That way you get more choices to display only messages that originate from a specific source.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Wählen Sie das Pfeilsymbol aus, um jeden abschnitt zu erweitern." lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    <span data-ttu-id="ff2c9-155">Wählen Sie das Pfeilsymbol aus, um jeden abschnitt zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="ff2c9-155">Choose the arrow icon expands each of the sections</span></span>  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Auswählen einer der neuen Optionen zum Filtern mithilfe von Typ und Quelle" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    <span data-ttu-id="ff2c9-157">Auswählen einer der neuen Optionen zum Filtern mithilfe von Typ und Quelle</span><span class="sxs-lookup"><span data-stu-id="ff2c9-157">Choose any of the new options to filter using type and source</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ff2c9-158">Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen</span><span class="sxs-lookup"><span data-stu-id="ff2c9-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
