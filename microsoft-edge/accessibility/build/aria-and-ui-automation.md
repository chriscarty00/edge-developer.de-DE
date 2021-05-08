---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Erfahren Sie Microsoft Edge ARIA-Informationen erkennen und dann hilfstechnologien zur Verfügung stellt, die dann Microsoft UI Automation APIs verwenden können.
title: Barrierefreiheit – ARIA- und Benutzeroberflächenautomatisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Webentwicklung, ARIA, Entwickler, UIA, Benutzeroberflächenautomatisierung
ms.custom: seodec18
ms.openlocfilehash: 2fcc8160c830b5a62d8023a5cb7cc9df376c49ca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566742"
---
# ARIA und Benutzeroberflächenautomatisierung in Microsoft Edge

Der W3C definiert Accessible Rich Internet Applications (ARIA) als Syntax zum Zugriff auf dynamische Webinhalte und benutzerdefinierte Benutzeroberflächen. Microsoft Edge erkennt die ARIA-Rollen-, Status- und Eigenschaftsinformationen und macht sie Hilfstechnologien verfügbar, die wiederum die [Microsoft UI Automation](https://blogs.msdn.microsoft.com/winuiautomation/) APIs zum Abrufen der Informationen verwenden können.

Unter [HTML5Accessibility](https://html5accessibility.com) finden Sie Informationen dazu, welche neuen HTML5-Features von der Website Microsoft Edge.

Das Microsoft Edge -Renderingmodul (EdgeHTML) erstellt eine barrierefreie Projektion von Webseiten, die den folgenden W3C-Spezifikationen entspricht:

1. Die [Spezifikation HTML Accessibility API Mappings](https://w3.org/TR/html-aam-1.0/) definiert, wie HTML-Elemente und -Attribute ARIA- und UI-Automatisierungsobjekten zugeordnet werden.
   * [Arbeitsentwurf](https://w3.org/TR/html-aam-1.0/) – stabile Version der Spezifikation
   * [Editor-Entwurf](https://w3c.github.io/html-aam/) – In Bearbeitung. Beachten Sie, dass diese Spezifikation zwar die neuesten Änderungen hat, die Änderungen jedoch möglicherweise noch nicht in Microsoft Edge sind.


2. Die [Spezifikation Core Accessibility API Mappings](https://w3.org/TR/core-aam-1.1/) definiert allgemeine Prinzipien zum Erstellen der Barrierefreiheitsstruktur und zum Zuordnen von ARIA-Elementen und -Attributen zu Objekten der Benutzeroberflächenautomatisierung.
   * [Arbeitsentwurf](https://w3.org/TR/core-aam-1.1/) – stabile Version der Spezifikation
   * [Editor-Entwurf](https://w3c.github.io/core-aam/) – In Bearbeitung. Beachten Sie, dass diese Spezifikation zwar die neuesten Änderungen hat, die Änderungen jedoch möglicherweise noch nicht in Microsoft Edge sind.  

3. Die Spezifikation Barrierefreier Name und Beschreibung: Berechnung und [API-Zuordnungen](https://w3.org/TR/accname-aam-1.1/) definiert, wie der Name und die Beschreibung von barrierefreien Objekten berechnet werden, wenn die HTML- und die ARIA-Elemente und -Attribute für die barrierefreien Elemente verfügbar sind.
   * [Arbeitsentwurf](https://w3.org/TR/accname-aam-1.1/) – stabile Version der Spezifikation  
   * [Editor-Entwurf](https://w3c.github.io/accname/) – In Bearbeitung. Beachten Sie, dass diese Spezifikation zwar die neuesten Änderungen hat, die Änderungen jedoch möglicherweise noch nicht in Microsoft Edge sind.   

Weitere Informationen zur Barrierefreiheitsarchitektur in Microsoft Edge finden Sie im [Blogbeitrag Erstellen einer barrierefreien](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/) Webplattform.  Beispiele dafür, wie die neue Architektur die Benutzererfahrung des Endbenutzers verbessert und insbesondere wie Markup die Navigation mit Hilfstechnologien wie Bildschirmlesegeräten definiert, finden Sie unter Erstellen einer barrierefreien Benutzeroberfläche mit HTML5 und [UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).
