---
description: Liste der Verweise für unterstützte Domänen in Microsoft Edge devtools Protocol, Version 0,2.
title: Domains-devtools Protocol Version 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 32634df94320e6474170726dfcd6164c5d02631a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567536"
---
# DevTools-Protokoll Domänen
## [CSS](css.md)
Diese Domäne macht CSS-Lese-und Schreibvorgänge verfügbar. Alle CSS-Objekte (Stylesheets, Regeln und Formatvorlagen) verfügen über ein zugeordnetes `id` Objekt, das in nachfolgenden Vorgängen des verknüpften Objekts verwendet wird. Jeder Objekttyp hat eine bestimmte `id` Struktur, die nicht zwischen Objekten unterschiedlicher Art austauschbar sind. CSS-Objekte können mithilfe der `get*ForNode()` Aufrufe (die eine DOM-Knoten-ID akzeptieren) geladen werden. Ein Client kann über die Ereignisse auch Stylesheets nachverfolgen `styleSheetAdded` / `styleSheetRemoved` und anschließend die erforderlichen Stylesheet-Inhalte mit den `getStyleSheet[Text]()` Methoden laden.
## [DOM](dom.md)
Diese Domäne macht Dom-Lese-und Schreibvorgänge verfügbar. Jeder DOM-Knoten wird mit seinem Spiegelungs Objekt dargestellt, das über ein `id` . Damit `id` können zusätzliche Informationen auf dem Knoten abgerufen, in den JavaScript-Objektwrapper aufgelöst werden usw. Es ist wichtig, dass der Client DOM-Ereignisse nur für die Knoten empfängt, die dem Client bekannt sind. Das Back-End verfolgt die Knoten, die an den Client gesendet wurden, und sendet nie denselben Knoten zweimal. Es obliegt dem Kunden, Informationen zu den Knoten zu sammeln, die an den Client gesendet wurden.<p>Beachten Sie, dass `iframe` Besitzer Elemente die entsprechenden Dokumentelemente als untergeordnete Knoten zurückgeben.</p>
## [DOMDebugger](domdebugger.md)
Dom-Debuggen ermöglicht das Festlegen von Haltepunkten für bestimmte Dom-Vorgänge und-Ereignisse. Die JavaScript-Ausführung wird bei diesen Vorgängen so beendet, als ob ein regulärer Haltepunkt festgesetzt wurde.
## [Debugger](debugger.md)
Die Debugger-Domäne macht JavaScript-Debugfunktionen verfügbar. Sie ermöglicht das Festlegen und Entfernen von Haltepunkten, durchlaufen der Ausführung, Durchsuchen von Stapelablaufverfolgungen usw.
## [Überlagerung](overlay.md)
Overlay-Domäne macht visuelle Elemente und Interaktion zwischen Knotenauswahl verfügbar
## [Seite](page.md)
Aktionen und Ereignisse im Zusammenhang mit der geprüften Seite gehören der Seiten Domäne an.
## [Runtime](runtime.md)
Runtime-Domäne macht JavaScript-Runtime mithilfe von Remote Auswertungs-und Spiegel Objekten verfügbar. Evaluierungsergebnisse werden als Spiegelungs Objekt zurückgegeben, die den Objekttyp, die Zeichenfolgendarstellung und den eindeutigen Bezeichner verfügbar machen, die für weitere Objektverweise verwendet werden können. Ursprüngliche Objekte werden im Arbeitsspeicher verwaltet, sofern Sie nicht explizit freigegeben werden.
## [Schema](schema.md)
Enthält Informationen zum Protokollschema.