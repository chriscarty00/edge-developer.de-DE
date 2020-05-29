---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Erfahren Sie, wie die Web-Benachrichtigungs-API verwendet werden kann, damit Websites Benutzer Benachrichtigungen außerhalb des Kontexts des Microsoft Edge-Browsers senden können.
title: Dev-Leitfaden – webbenachrichtigungs-API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/18/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: da563a333491ef699925adec6f97b3c21d3e54a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567105"
---
# Web-Benachrichtigungs-API

Mit der Web-Benachrichtigungs-API können Websites Benutzer Benachrichtigungen außerhalb des Kontexts einer Webseite innerhalb des Microsoft Edge-Browsers senden. Ein Beispiel für dieses Feature in Aktion wäre eine Messaging-Anwendung wie Skype. Wenn ein Benutzer eine neue Nachricht erhalten würde, wird eine Benachrichtigung auf dem Desktop angezeigt, in der Sie über die Nachricht benachrichtigt werden. Web-Benachrichtigungen sind vollständig in die Benachrichtigungs Plattform und das Wartungs Center in Windows 10 integriert. 

## Erstellen einer Benachrichtigung

Die folgende CodePen erstellt eine Pseudo-Skype-Benachrichtigung, indem Sie ein [`Notification`](https://msdn.microsoft.com/library/mt710818) Objekt mit den Optionen "," und "Optionen" Erstellen [`title`](https://msdn.microsoft.com/library/mt710826) [`icon`](https://msdn.microsoft.com/library/mt710814) [`body`](https://msdn.microsoft.com/library/mt710811) :


<iframe height='295' scrolling='no' title='Web-Benachrichtigungen' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Lesen Sie die Stift <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> -webbenachrichtigungen </a> von Microsoft Edge docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='https://codepen.io'> CodePen </a> .
</iframe>

Es wird dringend empfohlen, `icon` für jede Benachrichtigung eine Angabe anzugeben. Dies verbessert nicht nur eine Benachrichtigung aus Sicht einer Benutzeroberfläche, sondern hilft auch, Benutzer darüber zu informieren, von wo aus die Benachrichtigung gesendet wird.

Schauen Sie sich das folgende Video an, um eine exemplarische Vorgehensweise zum Erstellen einer webbenachrichtigung und zum Anzeigen des Verhaltens in Windows 10 zu sehen!


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### Benachrichtigungseigenschaften

Benachrichtigungen können mit den folgenden Optionen eingestellt werden:

Eigenschaft | Beschreibung
:-------- | :----------
[body](https://msdn.microsoft.com/library/mt710811) | Der Textkörper der Benachrichtigung.
[dir](https://msdn.microsoft.com/library/mt710813) | Die Richtung des Texts der Benachrichtigung.
[icon](https://msdn.microsoft.com/library/mt710814) | Die URL der Benachrichtigung, die für das zugehörige Symbol verwendet wird.
[lang](https://msdn.microsoft.com/library/mt710815) | Die Sprache der Benachrichtigung.
[Berechtigungs](https://msdn.microsoft.com/library/mt670637) | Die aktuelle benachrichtigungsanzeige Berechtigung, die der Benutzer für den aktuellen Ursprung gewährt hat.
[tag](https://msdn.microsoft.com/library/mt710825) | Das Tag der Benachrichtigung.
[title](https://msdn.microsoft.com/library/mt710826) | Der Titel der Benachrichtigung.

### Benachrichtigungsereignisse

Die folgenden Ereignisse werden für das [`Notification`](https://msdn.microsoft.com/library/mt710818) Objekt verwendet:

Ereignis | Beschreibung
:-------- | :----------
[OnClick](https://msdn.microsoft.com/library/mt712180) | Wird ausgelöst, wenn der Benutzer auf eine Benachrichtigung klickt.
[OnClose](https://msdn.microsoft.com/library/mt712178) | Wird ausgelöst, wenn eine Benachrichtigung vom Benutzer geschlossen wird, oder ein automatisches Timeout.
[OnError](https://msdn.microsoft.com/library/mt712181) | Wird ausgelöst, wenn beim Behandeln einer Benachrichtigung ein Fehler auftritt.
[onShow](https://msdn.microsoft.com/library/mt712182) | Wird ausgelöst, wenn eine Benachrichtigung angezeigt wird.

### Benachrichtigungsmethoden

Die folgenden Methoden werden für das [`Notification`](https://msdn.microsoft.com/library/mt710818) Objekt verwendet:

Methode | Beschreibung
:-------- | :----------
[close](https://msdn.microsoft.com/library/mt670636) | Schließt eine angezeigte Benachrichtigung.
[requestPermission](https://msdn.microsoft.com/library/mt710824) | Fordert die Berechtigung des Benutzers an, Benachrichtigungen vom aktuellen Ursprung angezeigt werden zu lassen.

## Benachrichtigungs Berechtigungen

Microsoft Edge ermöglicht Benutzern das Verwalten von Benachrichtigungs Berechtigungen für jede bestimmte Website Domäne. Der Benutzer muss entweder "Ja" oder "Nein" auswählen, wenn er von der Domäne aufgefordert wird, Benachrichtigungen anzuzeigen. Die [`requestPermission`](https://msdn.microsoft.com/library/mt710824) Methode wird verwendet, um den Berechtigungszustand entweder als, oder zu signalisieren `granted` `denied` `default` . Der Wert `default` "gibt an, dass der Benutzer keine Entscheidung getroffen hat, die als äquivalent zu sehen ist `denied` .




## API-Referenz

[Web-Benachrichtigungen](https://msdn.microsoft.com/library/mt710827)

## Spezifikation

[Web-Benachrichtigungen](https://notifications.spec.whatwg.org)
