---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Erfahren Sie, wie Aria-Informationen von Microsoft Edge erkannt und dann für Hilfstechnologien verfügbar gemacht werden, die dann Microsoft-Benutzeroberflächenautomatisierungs-APIs verwenden können.
title: Barrierefreiheit – Aria und Benutzeroberflächenautomatisierungs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Web-Entwicklung, Aria, Developer, UIA, UI-Automatisierung
ms.custom: seodec18
ms.openlocfilehash: 2fcc8160c830b5a62d8023a5cb7cc9df376c49ca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566742"
---
# Aria und UI-Automatisierung in Microsoft Edge

Das W3C definiert barrierefreie Rich-Internet-Anwendungen (Aria) als Syntax, um dynamische Webinhalte und benutzerdefinierte Benutzeroberflächen barrierefrei zu gestalten. Microsoft Edge erkennt die Aria-Rollen-, Zustands-und Eigenschaftsinformationen und macht Sie für Hilfstechnologien verfügbar, die wiederum die [Microsoft-Benutzeroberflächenautomatisierungs](https://blogs.msdn.microsoft.com/winuiautomation/) -APIs zum Abrufen der Informationen verwenden können.

Besuchen Sie [HTML5Accessibility](https://html5accessibility.com) , um Informationen darüber zu erhalten, welche neuen HTML5-Features von Microsoft Edge zugänglich unterstützt werden.

Das Microsoft-Edge-Rendering-Modul (EdgeHTML) erstellt eine barrierefreie Projektion von Webseiten, die den folgenden W3C-Spezifikationen entspricht:

1. Die [HTML-Spezifikation für Barrierefreiheits-API-Zuordnungen](https://w3.org/TR/html-aam-1.0/) definiert, wie HTML-Elemente und-Attribute zu Aria-und Benutzeroberflächenautomatisierungs-Objekten zugeordnet werden.
   * [Arbeitsentwurf](https://w3.org/TR/html-aam-1.0/) – stabile Version der Spezifikation
   * [Entwurf des Herausgebers](https://w3c.github.io/html-aam/) – work in Progress. Beachten Sie, dass die Änderungen möglicherweise noch nicht in Microsoft Edge verfügbar sind, während diese Spezifikation die neuesten Änderungen enthält.


2. Die [Core-Spezifikation für Barrierefreiheits-API-Zuordnungen](https://w3.org/TR/core-aam-1.1/) definiert Allgemeine Grundlagen für die Erstellung der Barrierefreiheits Struktur und das Zuordnen von Aria-Elementen und-Attributen zu Benutzeroberflächenautomatisierungs-Objekten.
   * [Arbeitsentwurf](https://w3.org/TR/core-aam-1.1/) – stabile Version der Spezifikation
   * [Entwurf des Herausgebers](https://w3c.github.io/core-aam/) – work in Progress. Beachten Sie, dass die Änderungen möglicherweise noch nicht in Microsoft Edge verfügbar sind, während diese Spezifikation die neuesten Änderungen enthält.  

3. Der Name und die Beschreibung für den Namen und die [Beschreibung: Berechnungs-und API-Zuordnungs](https://w3.org/TR/accname-aam-1.1/) Spezifikationen definieren, wie der Name und die Beschreibung von barrierefreien Objekten mit dem HTML-Wert und den Aria-Elementen und-Attributen berechnet werden, die für die barrierefreien Elemente verfügbar sind.
   * [Arbeitsentwurf](https://w3.org/TR/accname-aam-1.1/) – stabile Version der Spezifikation  
   * [Entwurf des Herausgebers](https://w3c.github.io/accname/) – work in Progress. Beachten Sie, dass die Änderungen möglicherweise noch nicht in Microsoft Edge verfügbar sind, während diese Spezifikation die neuesten Änderungen enthält.   

Weitere Informationen zur barrierefreien Architektur in Microsoft Edge finden Sie im Blogbeitrag [Erstellen einer barrierefreieren Web-Plattform](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/) .  Beispiele dafür, wie die neue Architektur die Oberfläche des Endbenutzers verbessert, und insbesondere, wie Markup die Erfahrung der Navigation mit Hilfstechnologien wie Bildschirmsprachausgaben definiert, finden Sie unter [Erstellen einer barrierefreieren Benutzeroberfläche mit HTML5 und UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).
