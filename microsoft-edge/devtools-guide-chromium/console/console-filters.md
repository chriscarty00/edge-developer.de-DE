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
# <a name="filter-console-messages"></a>Filtern von Konsolennachrichten  

Wenn Sie im Web surfen, finden Sie möglicherweise, dass die **Konsole** mit allen Arten von Informationen überflutet ist.  Häufig sind die Informationen für Sie nicht relevant.  Beispielsweise Informationen zum Liveprojekt, das ein anderer Entwickler beim Debuggen protokolliert hat.  Oder weitere Informationen zu Verstößen und Warnungen zur Leistung der aktuellen Website, die Sie nicht ändern können.  Es ist sinnvoll, die Filteroptionen der Konsole zu **verwenden,** um das Rauschen zu reduzieren.  

## <a name="filter-by-log-level"></a>Filtern nach Protokollebene  

Jeder Methode des Objekts `console` ist ein Schweregrad zugeordnet.  Die Schweregrade sind `Verbose` , `Info` , oder `Warning` `Error` .  Anzeigen der Schweregrade in der [API-Dokumentation][DevtoolsConsoleApi].  Beispielsweise handelt es sich um eine Nachricht `console.log()` `Info` auf Ebene, aber um eine `console.error()` Nachricht auf `Error` Ebene.  

Verwenden Sie zum Filtern von Nachrichten in **der Konsole**das **Dropdownmenü Protokollebene.**  Sie können den Status der einzelnen Ebenen umschalten.  Entfernen Sie das Häkchen neben jeder Ebene, um die einzelnen Ebenen zu deaktivieren.  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="Das Dropdownmenü filtert Konsolennachrichten mithilfe der Protokollebene" lightbox="../media/console-filter-dropdown.msft.png":::
    Das Dropdownmenü **filtert Konsolennachrichten** mithilfe der Protokollebene  
:::image-end:::  

Da kein Filter angewendet wird, werden in der folgenden Abbildung Dutzende von Nachrichten angezeigt.  Reduzieren und verwalten Sie als Nächstes die Anzahl der Nachrichten.  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Kein Filtersatz bedeutet, dass Sie möglicherweise viele Konsolennachrichten anzeigen" lightbox="../media/console-filter-displays-all.msft.png":::
    Kein Filtersatz bedeutet, dass Sie möglicherweise viele Konsolennachrichten anzeigen  
:::image-end:::  

Wählen Sie aus, um alle Meldungen auf Warnungsebene auszublenden, um das Rauschen zu reduzieren.  Navigieren Sie zum **Dropdownmenü Protokollebenen,** und deaktivieren Sie die `Warnings` Stufe.  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Ausblenden aller Warnmeldungen in der Konsole, um einen großen Teil des Rauschens zu filtern" lightbox="../media/console-filter-hide-warning.msft.png":::
    Ausblenden aller Warnmeldungen in der **Konsole,** um einen großen Teil des Rauschens zu filtern  
:::image-end:::  

## <a name="filter-by-text"></a>Filtern nach Text  

Wenn Sie weitere Details überprüfen möchten, geben Sie zum Filtern von Nachrichten mithilfe von Text eine Zeichenfolge in das **Textfeld Filter** ein.  Geben Sie beispielsweise in das Feld ein, um nur Ihre Nachrichten über den Browser anzuzeigen, der das Laden `block` von Ressourcen blockiert.

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Zeigt die Nachrichten an, die den Wortblock enthalten" lightbox="../media/console-filter-text.msft.png":::
    Zeigt die Nachrichten an, die das Wort enthalten `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a>Filtern nach regulärem Ausdruck

[Reguläre Ausdrücke][MdnDocsWebJavascriptGuideRegularExpressions] sind eine leistungsstarke Möglichkeit zum Filtern von Nachrichten.  Geben Sie beispielsweise in das Textfeld Filter ein, um nur Nachrichten anzeigen zu `/^Tracking/` können, die mit dem Begriff **** `Tracking` beginnen.  Wenn Sie mit regulären Ausdrücken nicht vertraut sind, ist [RegExr][|::ref1::|Main] eine großartige Ressource, um mehr über die Verwendung regulärer Ausdrücke zu erfahren.

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Zeigt die Nachrichten an, die mit dem Wortfilter beginnen, indem ein regulärer Ausdruck im Textfeld Filter verwendet wird." lightbox="../media/console-filter-regex.msft.png":::
    Zeigt die Nachrichten an, die mit dem Wort `filter` beginnen, indem ein regulärer Ausdruck im **Textfeld Filter** verwendet wird.  
:::image-end:::  

## <a name="filter-by-message-source"></a>Filtern nach Nachrichtenquelle  

Sie können auch definieren, welche Art von Nachrichten Sie anzeigen möchten und wo die einzelnen Nachrichten mit der **Sidebar der** Konsole **stammen.**  Wählen Sie dazu die Schaltfläche **Konsolenseite anzeigen** aus.  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Um die Seitenleiste zu öffnen, wählen Sie das Seitenleistensymbol aus." lightbox="../media/console-filter-sidebar-icon.msft.png":::
    Wählen Sie zum Öffnen **der Seitenleiste**die Schaltfläche **Konsolenseite anzeigen** aus.  
:::image-end:::  

Wenn die **Seitenleiste** geöffnet ist, können Sie die Gesamtzahl der Nachrichten und den Ursprung der einzelnen Nachrichten anzeigen.  Die Optionen sind `All messages` , , , , und `User Messages` `Errors` `Warnings` `Info` `Verbose` .  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="Auf der Konsolenseite werden die verschiedenen Quellen angezeigt, die von" lightbox="../media/console-filter-sidebar-open.msft.png":::
    Auf **der Konsolenseite werden** die verschiedenen Quellen angezeigt, die von  
:::image-end:::  

Wählen Sie eine der Optionen aus, um nur die Nachrichten dieses Typs anzuzeigen.  Wenn Sie beispielsweise Benutzernachrichten anzeigen möchten, wählen Sie die Option Benutzernachrichten aus, um weniger Rauschen zu anzeigen.

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Wählen Sie aus, ob nur Benutzernachrichten in der Konsole mithilfe des Filters in der Seitenleiste angezeigt werden sollen." lightbox="../media/console-filter-select-user-messages.msft.png":::
    Wählen Sie aus, ob nur Benutzernachrichten in der **Konsole mithilfe** des Filters in der **Seitenleiste angezeigt werden sollen.**  
:::image-end:::  

Um mehr zu filtern und die Auswahl zu erweitern, wählen Sie das Dreiecksymbol daneben aus.  Auf diese Weise erhalten Sie mehr Auswahlmöglichkeiten, um nur Nachrichten anzeigen zu können, die von einer bestimmten Quelle stammen.  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Wählen Sie das Pfeilsymbol aus, um jeden abschnitt zu erweitern." lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    Wählen Sie das Pfeilsymbol aus, um jeden abschnitt zu erweitern.  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Auswählen einer der neuen Optionen zum Filtern mithilfe von Typ und Quelle" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    Auswählen einer der neuen Optionen zum Filtern mithilfe von Typ und Quelle  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Konsolen-API-| Microsoft Docs"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Reguläre Ausdrücke | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
