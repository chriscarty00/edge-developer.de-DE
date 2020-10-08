---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Wenn Sie sicherstellen möchten, dass das Symbol ihrer Erweiterung im hellen und im dunklen Modus angezeigt wird, folgen Sie dem Leitfaden zur Barrierefreiheit.
title: Barrierefreiheits Erweiterungen (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 60e794467c6d054e390ce61c40559afa3a110c21
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882793"
---
# Barrierefreiheits Erweiterungen (EdgeHTML)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Erstellen von barrierefreien Erweiterungssymbolen für Microsoft Edge

Entwickler von Drittanbieter-Erweiterungen werden ermutigt, Bildressourcen zu verwenden, die den strengen Barrierefreiheitsanforderungen von Microsoft entsprechen, damit Symbole für helle und dunkle Designs deutlich sichtbar sind. Wir empfehlen, dass alle Erweiterungssymbole ein 14:1-Verhältnis zwischen der Hintergrundfarbe des Symbols und der dominierenden Farbe des Symbols selbst aufweisen.


Von Microsoft entwickelte First-Party-Erweiterungen wenden eine visuelle Behandlung mit "Aufklebern" an, um diese Anforderungen zu erfüllen.

### Beispiele für "Aufkleber"

Das Hauptziel von "Aufklebern" besteht darin, das Symbol visuell auf jeder Hintergrundfarbe zugänglich zu machen. Das empfohlene Farb Verhältnis zwischen dem weißen äußeren Strich und dem Symbol sollte 14:1 sein, um die hohen Kontrast Anforderungen zu unterstützen.

#### Gutes Symbol
Mit Aufklebern bleibt ein in erster Linie dunkleres Symbol auf jeder Hintergrundfarbe sichtbar.


![Abbildung des Symbols, das auf einer beliebigen Hintergrundfarbe angezeigt wird](./../media/accessibility-light-to-dark-good.png)

#### Ungültiges Symbol
Ohne Aufkleber kann ein Symbol in den Hintergrund integriert werden, sodass es nicht mehr zu sehen ist.


![Abbildung des Symbols, das in schwarzen Hintergrund verschmilzt](./../media/accessibility-light-to-dark-bad.png)

### "Aufkleber" für Ihr Erweiterungssymbol

In den folgenden fünf Schritten wird die vorgeschlagene Methode zum Erstellen eines Erweiterungssymbols erläutert, das den Barrierefreiheitsanforderungen von Microsoft entspricht:


| Schritt 1                                       | Schritt 2                                       | Schritt 3                                                                                 | Schritt 4                                                                          | Schritt 5                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| Setzen Sie das Symbol innerhalb des angegebenen Rasters.    | Verringern Sie die Größe des Symbols um 2 Pixel.           | Kopieren Sie das Symbol, und fügen Sie es ein. Erstellen Sie einen äußeren Strich mit 2 Pixeln mit abgerundeten Ecken. | Skizzieren Sie den Strich, geben Sie den zusammengesetzten Pfad frei, und verbinden Sie die restlichen Shapes. | Färben Sie den äußeren Strich weiß und das innere Symbol, wie Sie möchten. |
| ![step1](./../media/accessibility-step1.png) | ![step2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![Schritt4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

