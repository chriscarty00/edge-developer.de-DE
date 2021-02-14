---
description: Hosten und Veröffentlichen von Erweiterungen im Unternehmen für Microsoft Edge (Chromium).
title: Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327687"
---
# Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Store  

Die meisten Erweiterungen werden im [Microsoft Edge-Add-Ons-Store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] veröffentlicht, um Benutzer vor bösartigen Erweiterungen zu schützen.  

## Veröffentlichungsoptionen für Erweiterungen  

Alle Erweiterungen werden als spezielle Archivdatei \( \) mit einem Suffix `.zip` an Die Benutzer `.crx` verteilt.  Im Microsoft Edge-Add-Ons-Speicher veröffentlichte Erweiterungen werden als Dateien `.zip` hochgeladen.  Beim Veröffentlichungsprozess wird die Datei `.zip` automatisch in eine Datei `.crx` konvertiert.  

In den folgenden beiden Szenarien müssen Sie Ihre Erweiterung nicht im Microsoft Edge-Add-Ons-Store veröffentlichen.  

*   Erweiterungen, die mithilfe der Unternehmensrichtlinie verteilt werden.  
*   Verwenden von entpackten Erweiterungsverzeichnissen auf einem lokalen Computer, wenn sich Microsoft Edge im Entwicklermodus befindet.  

## Updates für Erweiterungen

Der Microsoft Edge Browser sucht regelmäßig nach neuen Versionen installierter Erweiterungen und aktualisiert diese ohne Benutzereingriff.  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Erweiterungen – Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier.](https://developer.chrome.com/extensions/hosting)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
