---
description: Stellen Sie Ihre Erweiterung für verschiedene Sprachen barrierefrei zur Verfügung, und testen Sie Ihre Sprachzeichenfolgen mit dem Internationalisierungs Leit Faden.
title: Erweiterungen – Internationalisierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbbc847ebd2103cba2eca8a791009b4e72f93a6f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234180"
---
# Internationalisierung  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Damit Ihre Erweiterung für eine Vielzahl unterschiedlicher Personen zugänglich ist, ist es wichtig, sich mit anderen Ländern zu entwickeln. Mit Microsoft Edge Extensions können Sie Ihren Erweiterungen unterschiedliche Sprachzeichenfolgen hinzufügen, damit Ihre Sprache problemlos geändert werden kann.

Weitere Informationen zum Internationalisierung ihrer Erweiterung finden Sie im [Leitfaden zur Internationalisierung](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)von MDN.


## Testen von Sprachen

Um Ihre Sprachzeichenfolgen zu testen, müssen Sie zuerst die Windows-Anzeigesprache auf die Sprache einstellen, auf die Sie testen möchten.

Führen Sie die folgenden Schritte aus, um die Windows-Anzeigesprache zu ändern:

1. Öffnen Sie die App Einstellungen.

   ![Einstellungsanwendung](./../media/loc-settings.png)
2. Wählen Sie "Uhrzeit & Sprache" aus.
3. Wählen Sie "Region & Sprache" aus.
4. Wählen Sie "+ Sprache hinzufügen" aus, um die Sprache der Liste der möglichen Sprachen hinzuzufügen.
5. Wählen Sie die gewünschte Sprache in der Liste "Sprachen" aus, die Sie testen möchten.
6. Wählen Sie die Schaltfläche "als Standard festlegen" aus (möglicherweise müssen Sie Ihren PC neu starten).
7. Öffnen Sie Microsoft Edge, und überprüfen Sie, ob die für das Gebietsschema definierten Zeichenfolgen wie erwartet angezeigt werden.

Mithilfe der [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) -Eigenschaft können Sie überprüfen, ob die Sprache, die Microsoft Edge für die Windows-Anzeigesprache festgelegt hat, richtig ist.

Klicken Sie auf die Schaltfläche im CodePen unten, um die Anzeigesprache Ihres Browsers anzuzeigen.

<iframe height='300' scrolling='no' title='Gebietsschema abrufen' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Weitere Informationen finden Sie unter <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> </a> MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='http://codepen.io'> CodePen </a> .
</iframe>
