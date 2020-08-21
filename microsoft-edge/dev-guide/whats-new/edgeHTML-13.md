---
description: Auf dieser Seite finden Sie eine Übersicht über die Neuerungen in EdgeHTML 13.
title: Neue Features und APIs in EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 033b8dacb107492624f3b8c7775a47285c9893dd
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941911"
---
# Neuerungen in EdgeHTML 13  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Hier sind die Änderungen, die im Lieferumfang von EdgeHTML 13 enthalten sind, dem Modul, das den Microsoft Edge-Browser im [ersten wichtigen Update](https://blogs.windows.com/windowsexperience/2015/11/12) für Windows 10 (11/2015, Build 10586 \) einmacht.  Eine Übersicht über Änderungen am gesamten Microsoft Edge-Browser finden Sie unter [Introducing EdgeHTML 13, unser erstes Platt Form Update für Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).  

Hier ist der Permalink für die folgende Liste der  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) Änderungen:  

## Features  

### CSS  

EdgeHTML 13 unterstützt neue CSS-Features, einschließlich:  

*   [Pseudo Klassen für CSS-Veränderlichkeit](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [Pseudo Klassen für CSS-Bereich](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   CSS- [anfangs](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) -und [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) -Schlüsselwörter  

### Verschlüsselte Medienerweiterungen  

Microsoft Edge unterstützt jetzt die neuen APIs für [verschlüsselte Medienerweiterungen](https://w3.org/TR/encrypted-media) mit unpräfixen.  Verschlüsselte Medienerweiterungen \ (EME \) erweitert die Video-und Audioelemente, um DRM-geschützte Inhalte (Digital Rights Management) zu aktivieren, ohne Plug-ins zu verwenden.  Weitere Informationen finden Sie unter eme:  [verschlüsselte Medienerweiterungen](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).  

### Grafiken  

EdgeHTML 13 stellt die folgenden Grafik Updates vor:  

*   [Canvas-Ellipse](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [Füllmethoden für Leinwand](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> Element ](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [SVG-externer Inhalt](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### JavaScript  

EdgeHTML 13 umfasst [wichtige Verbesserungen und die Unterstützung neuer Features in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), dem JavaScript-Modul, das Microsoft Edge anbietet, einschließlich:  

#### Neue Funktionen  

Standardmäßig aktiviert  

*   Standardmäßig aktiviert [asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) \ ([Blogbeitrag](https://blogs.windows.com/msedgedev/2015/11/10), [Demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)  
*   [Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \ (ES2015 \)  

#### Experimentelle JavaScript-Features  

Aktiviert mit `about:flags`  

*   [Asynchrone Funktionen](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \ (ES2016 \)  
*   [Potenz Operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \ (ES2016 \)  
*   [Destrukturierung](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \ (ES2015 \)  

### Benutzereingabe  

Die folgenden in EdgeHTML 13 eingeführten Features verbessern die Benutzereingabe:  

*   [<meter> Element ](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [oninvalid-Ereignishandler für das Element Dokument und-Fenster](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### Zeiger Sperre  

Microsoft Edge unterstützt jetzt die Pointer Lock-API \ (zuvor als "Maus Sperre" bezeichnet) für den Zugriff auf rohe Mausbewegungen, das Ziel von Mausereignissen auf ein einzelnes Element sperren, wodurch Grenzwerte für die Mausbewegung in einer einzelnen Richtung beseitigt werden und der Cursor aus der Ansicht entfernt werden kann.  

## Neue APIs in EdgeHTML 13  

Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 13.  Sie werden im Format von angezeigt `[interface name].[api name]` .  

<iframe height='584' scrolling='no' title='Neue APIs in EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'>Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> in EdgeHTML 13 </a> von Microsoft Edge docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='http://codepen.io'> CodePen </a> .</iframe>  
