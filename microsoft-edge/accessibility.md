---
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
description: Erfahren Sie, wie Sie barrierefreie Websites in Microsoft Edge erstellen, entwerfen und testen können.
title: Bedienungshilfen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Web-Entwicklung, Aria, Developer, UIA, UI-Automatisierung
ms.openlocfilehash: 6ad95e9c250aa6a4a61ca09470cea86efd715427
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583105"
---
# Bedienungshilfen  

> "\ [T \] die Auswirkungen einer Behinderung werden im Internet grundlegend geändert, weil das Internet Hindernisse für Kommunikation und Interaktion entfernt, die viele Menschen in der physischen Welt sehen." [(Barrierefreiheit | W3C][W3CAccessibility]  

Die [Weltgesundheitsorganisation][WHODisabilities] definiert Behinderung als "ein Missverhältnis zwischen den Funktionen des Körpers einer Person und den Eigenschaften der Umgebung, in der Sie leben".  Behinderungen reichern von situationsbedingten Behinderungen wie eingeschränkter Mobilität, während Sie ein Baby oder ein helles Sonnenlicht auf einem Telefon halten, bis zu anderen körperlichen, auditiven, visuellen oder altersbedingten Beeinträchtigungen.  

Das Entwerfen von Websites und anderen Technologien für die Integration sorgt für ein angenehmes Erlebnis jeder Person.  Inklusive Design und Barrierefreiheit im Web ermöglicht und unterstützt jeden, das Internet zu nutzen.  

Im folgenden finden Sie einige bewährte Methoden, Codebeispiele und weitere Ressourcen, mit denen Sie mehr über das [entwerfen][AccessibilityDesign], [Erstellen][AccessibilityBuild]und [Testen][AccessibilityTest] von barrierefreien Websites in Microsoft Edge erfahren.  

## Barrierefreiheit in Microsoft Edge  

In Microsoft Edge haben wir eine moderne [UI-Automatisierung-API][WindowsWin32AutoEntryui] (UIA-API \) eingeführt.  Die Änderung an UIA war eine wichtige Investition in die Barrierefreiheit des Browsers und bildet die Grundlage für ein umfassenderes Weberlebnis für Benutzer, die von Hilfstechnologien in Windows 10 abhängig sind.  Benutzer profitieren auch vom immergrünen Charakter der Chrom Maschine.  

Das Barrierefreiheits System in Microsoft Edge unterstützt inhärent moderne Web-Standards wie Aria, HTML5 und CSS3.  Das folgende Diagramm der vereinfachten Browser Pipeline folgt dem Inhalt einer Webseite in einer barrierefreien Präsentationsschicht.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Inhalte, die in das Modul Modell umgewandelt werden, werden in visuelle und Barrierefreiheits Ansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden.&quot;:::
   Abbildung1.  Inhalte, die in das Modul Modell umgewandelt werden, werden in visuelle und Barrierefreiheits Ansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden.
:::image-end:::

<!--![Figure 1.  Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation][ImageAccessibilityArchitecture]  -->  

Das Microsoft Edge-Team arbeitet kontinuierlich mit dem W3C und anderen Browser Anbietern zusammen, um sicherzustellen, dass die Features der neuen Webplattform genügend integrierte Barrierefreiheit aufweisen.  

Informationen zu den neuen HTML5-Features, die von Microsoft Edge zugänglich unterstützt werden, finden Sie unter [HTML5Accessibility][HTML5Accessibility].  

## Ressourcen  

#### Microsoft Windows-Benutzeroberflächen Automatisierungs Blog  

Der [Microsoft Windows-Benutzeroberflächen Automatisierungs Blog][ArchiveBlogsWinuiautomation] behandelt Themen im Zusammenhang mit der Windows-Automatisierungs-API.  

#### Web Accessibility Initiative (WAI)  

Die [Web Accessibility Initiative (WAI)][W3CWaiHome] , die BT im W3C zur Verfügung stellt, ist eine Bemühung, die Barrierefreiheit im Internet zu verbessern.  Die Website bietet eine Reihe von Ressourcen für den Einstieg [in die Barrierefreiheit im Web][W3CWaiGettingstartedOverview], das [Entwerfen für Inklusion][W3CWaiFundamentals], [Tutorials und Präsentationen][W3CWaiTeachAdvocate]und vieles mehr.  


<!-- image links -->  

<!--[ImageAccessibilityArchitecture]: ./media/accessibilityarchitecture.png &quot;Figure 1: Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation&quot;  -->  

<!-- links -->  

[AccessibilityBuild]: ./accessibility/build.md &quot;Erstellen von barrierefreien Websites&quot;  
[AccessibilityDesign]: ./accessibility/design.md &quot;Entwerfen barrierefreier Websites&quot;  
[AccessibilityTest]: ./accessibility/test.md &quot;Barrierefreiheits Tests&quot;  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 &quot;Benutzeroberflächenautomatisierungs&quot;  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ &quot;Microsoft Windows-Benutzeroberflächen Automatisierungs Blog&quot;  

[HTML5Accessibility]: https://html5accessibility.com &quot;Barrierefreiheit in HTML5&quot;  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility &quot;Barrierefreiheit | W3C&quot;  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro &quot;Einführung in Barrierefreiheit im Web | Web Accessibility Initiative (WAI) | W3C&quot;  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview &quot;Erste Schritte: Erstellen einer Website für Barrierefreiheit | Web Accessibility Initiative (WAI) | W3C&quot;  
[W3CWaiHome]: https://w3.org/wai &quot;Web Accessibility Initiative (WAI) | W3C&quot;  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate &quot;Übersicht über unterrichten und Fürsprecher | Web Accessibility Initiative (WAI) | W3C&quot;  

[WHODisabilities]: https://who.int/topics/disabilities &quot;Behinderungen | Wer"  

