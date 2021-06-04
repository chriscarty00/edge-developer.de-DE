---
description: Informationen zum Erstellen, Entwerfen und Testen barrierefreier Websites innerhalb Microsoft Edge.
title: Barrierefreiheit
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: Barrierefreiheit, Barrierefreiheit für Entwickler, barrierefreie Websites, Edge, Webentwicklung, ARIA, Entwickler, UIA, Benutzeroberflächenautomatisierung
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233726"
---
# Barrierefreiheit – Übersicht  

> "\[T\]er Auswirkungen von Behinderungen werden im Web grundlegend geändert, da das Web Hindernisse für Kommunikation und Interaktion beseitigt, mit der viele Menschen in der physischen Welt zu sehen sind." [(Barrierefreiheit | W3C)][W3CAccessibility]  

Die [Who Health Organization][WHODisabilities] definiert Behinderung als "einen Konflikt in der Interaktion zwischen den Features des Körpers einer Person und den Features der Umgebung, in der sie leben".  Behinderungen reichen von situationenbezogenen Behinderungen, z. B. eingeschränkter Mobilität beim Halten eines Babys oder hellem Sonnenlicht auf einem Telefon, bis zu anderen physischen, auditorischen, visuellen oder altersbezogenen Beeinträchtigungen.  

Das Entwerfen von Websites und anderen Technologien für die Inklusion sorgt für eine für jede Person angenehme Erfahrung.  Inklusives Design und Barrierefreiheit im Web ermöglichen und unterstützen alle, das Web zu nutzen.  

Hier finden Sie einige bewährte Methoden, Codebeispiele und weitere Ressourcen, [][AccessibilityTest] um mehr über [das Entwerfen,][AccessibilityDesign]Erstellen [und][AccessibilityBuild]Testen barrierefreier Websites in Microsoft Edge.  

##  <a name="accessibility-in-microsoft-edge"></a>Barrierefreiheit in Microsoft Edge  

In Microsoft Edge haben wir die moderne [Benutzeroberflächenautomatisierungs-API][WindowsWin32AutoEntryui] \(UIA-API\) eingeführt.  Die Umstellung auf UIA war eine wichtige Investition in die Barrierefreiheit von Browsern und legt die Grundlage für eine inklusivere Weberfahrung für Benutzer, die auf Hilfstechnologie in Windows 10.  Benutzer profitieren auch vom immergrünen Charakter des Chromium Engine.  

Das Barrierefreiheitssystem in Microsoft Edge unterstützt grundsätzlich moderne Webstandards wie ARIA, HTML5 und CSS3.  Das folgende Diagramm der vereinfachten Browserpipeline folgt Webseiteninhalten in einer barrierefreien Präsentationsebene.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="In das Modulmodell transformierte Inhalte werden in visuelle Ansichten und Barrierefreiheitsansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden":::
   In das Modulmodell transformierte Inhalte werden in visuelle Ansichten und Barrierefreiheitsansichten projiziert, die entweder als visuelle oder barrierefreie Präsentation dargestellt werden  
:::image-end:::  

Das Microsoft Edge arbeitet kontinuierlich mit dem W3C und anderen Browseranbietern zusammen, um sicherzustellen, dass neue Webplattformfeatures über ausreichende integrierte Barrierefreiheit verfügen.  

Informationen dazu, welche neuen HTML5-Features von der Microsoft Edge unterstützt werden, finden Sie unter [HTML5Accessibility][HTML5Accessibility].  

##  <a name="resources"></a>Ressourcen  

#### Microsoft Windows Ui Automation Blog  

Der [Microsoft Windows-Benutzeroberflächenautomatisierungsblog][ArchiveBlogsWinuiautomation] behandelt Themen im Zusammenhang mit Windows Automatisierungs-API.  

#### Web Accessibility Initiative (WAI)  

Die [Web Accessibility Initiative (WAI),][W3CWaiHome] die bt das W3C bereitgestellt hat, ist ein Versuch, die Barrierefreiheit des Webs zu verbessern.  Die Website bietet eine Vielzahl von Ressourcen für erste Schritte mit [Webbarrierefreiheit,][W3CWaiGettingstartedOverview] [Entwerfen für][W3CWaiFundamentals]Inklusion, Lernprogramme und Präsentationen und [vieles][W3CWaiTeachAdvocate]mehr.  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Erstellen von Barrierefreien Websites | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Entwerfen von barrierefreien Websites | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Barrierefreiheitstests | Microsoft Docs"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Benutzeroberflächenautomatisierung | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Microsoft Windows Ui Automation Blog | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "HTML5-Barrierefreiheit"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Barrierefreiheit | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Einführung in web accessibility | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Erste Schritte: So können Sie auf eine Website | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Teach and Advocate Overview | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Behinderungen | WHO"  

