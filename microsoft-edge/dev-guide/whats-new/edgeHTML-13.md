---
description: Auf dieser Seite finden Sie eine Übersicht über die Neuerungen in EdgeHTML 13.
title: Neuerungen in EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 8fb9d6bd78af5d595e217fa2bf210632f4c1a61f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566749"
---
# Neuerungen in EdgeHTML 13
Hier sind die Änderungen, die mit EdgeHTML 13 ausgeliefert wurden, dem Modul, das den Microsoft Edge-Browser im [ersten wichtigen Update](https://blogs.windows.com/windowsexperience/2015/11/12/first-major-update-for-windows-10-available-today/) für Windows 10 (11/2015, Build 10586) einmacht. Eine Übersicht über Änderungen am gesamten Microsoft Edge-Browser finden Sie unter [Introducing EdgeHTML 13, unser erstes Platt Form Update für Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16/introducing-edgehtml-13-our-first-platform-update-for-microsoft-edge/).

Hier ist der Permalink für die folgende Liste der [https://aka.ms/devguide_edgehtml_13](https://aka.ms/devguide_edgehtml_13) Änderungen:

## Features

### CSS
' ' EdgeHTML 13 unterstützt neue CSS-Features, einschließlich:
* [Pseudo Klassen für CSS-Veränderlichkeit](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses/)
* [Pseudo Klassen für CSS-Bereich](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses/)
* CSS- [anfangs](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue/) -und [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue/) -Schlüsselwörter

### Verschlüsselte Medienerweiterungen
Microsoft Edge unterstützt jetzt die neuen APIs für [verschlüsselte Medienerweiterungen](https://w3.org/TR/encrypted-media/) mit unpräfixen. Mit verschlüsselten Medienerweiterungen (EME) werden die Video-und Audioelemente erweitert, um DRM-geschützte Inhalte (Digital Rights Management) zu aktivieren, ohne Plug-ins zu verwenden. Weitere Informationen finden Sie unter eme: [verschlüsselte Medienerweiterungen](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/encrypted-media-extensions).

### Grafiken

EdgeHTML 13 stellt die folgenden Grafik Updates vor:
* [Canvas-Ellipse](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse/)
* [Füllmethoden für Leinwand](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d/)
* [`<picture>` Element ](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement/)
* [SVG-externer Inhalt](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent/)

### JavaScript
EdgeHTML 13 umfasst [wichtige Verbesserungen und die Unterstützung neuer Features in Chakra](https://blogs.windows.com/msedgedev/2015/09/30/asynchronous-code-gets-easier-with-es2016-async-function-support-in-chakra-and-microsoft-edge/), dem JavaScript-Modul, das Microsoft Edge anbietet, einschließlich:

#### Neue Features (standardmäßig aktiviert)

* [ASM. js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) standardmäßig aktiviert ([Blogbeitrag](https://blogs.windows.com/msedgedev/2015/11/10/supercharging-javascript-performance-with-asm-js/), [Demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess/))
* [Klassen](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) (ES2015)

#### Experimentelle JavaScript-Features (aktiviert mit *about: Flags*)

* [Asynchrone Funktionen](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) (ES2016)
* [Exponentialwert-Operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) (ES2016)
* [Destrukturierung](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) (ES2015)

### Benutzereingabe
Die folgenden in EdgeHTML 13 eingeführten Features verbessern die Benutzereingabe:
* [`<meter>` Element ](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement/)
* [`oninvalid` Ereignishandler für das Element Dokument und-Fenster](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler/)

### Zeiger Sperre
Microsoft Edge unterstützt jetzt die Pointer Lock-API (zuvor als "Maus Sperre" bezeichnet) für den Zugriff auf unformatierte Mausbewegungen, wobei das Ziel von Mausereignissen auf ein einzelnes Element gesperrt wird, wodurch Grenzwerte für die Mausbewegung in einer einzigen Richtung beseitigt werden, und der Cursor aus der Ansicht entfernt wird. 


## Neue APIs in EdgeHTML 13 "" ""

Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 13. Sie werden im Format **[Schnittstellenname] aufgeführt. [ API-Name]**.
<iframe height='584' scrolling='no' title='Neue APIs in EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> in EdgeHTML 13 </a> von Microsoft Edge docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='http://codepen.io'> CodePen </a> .</iframe>""''""''""
