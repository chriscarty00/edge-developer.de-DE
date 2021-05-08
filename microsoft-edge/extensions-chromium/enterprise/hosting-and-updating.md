---
description: Hosten und Veröffentlichen von Erweiterungen im Unternehmen für Microsoft Edge (Chromium).
title: Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Speicher
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 2249462b0a2dac86efa4b775171e2a3229a34431
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461220"
---
# <a name="publish-and-update-extensions-in-the-microsoft-edge-add-ons-store"></a>Veröffentlichen und Aktualisieren von Erweiterungen im Microsoft Edge-Add-Ons-Speicher  

Die meisten Erweiterungen werden im [Microsoft Edge-Add-Ons-Speicher][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] veröffentlicht, um Benutzer vor schädlichen Erweiterungen zu schützen.  

## <a name="publish-options-for-extensions"></a>Veröffentlichen von Optionen für Erweiterungen  

Alle Erweiterungen werden als spezielle Archivdatei \( \) mit `.zip` einem Suffix an Benutzer `.crx` verteilt.  Erweiterungen, die im Microsoft Edge-Add-Ons-Speicher veröffentlicht werden, werden als Dateien `.zip` hochgeladen.  Beim Veröffentlichungsprozess wird die Datei `.zip` automatisch in eine Datei `.crx` konvertiert.  

In den folgenden beiden Szenarien müssen Sie Ihre Erweiterung nicht im Microsoft Edge-Add-Ons-Speicher veröffentlichen.  

*   Erweiterungen, die mithilfe Enterprise werden.  
*   Verwenden von auspackten Erweiterungsverzeichnissen auf einem lokalen Computer, Microsoft Edge sich im Entwicklermodus befindet.  

## <a name="updates-to-extensions"></a>Updates für Erweiterungen

Der Microsoft Edge sucht automatisch nach neuen Versionen installierter Erweiterungen. Updates werden ohne Benutzereingriff installiert.  


<!-- image links -->

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Erweiterungen – Microsoft Edge Insider Addons | Microsoft"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/hosting).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
