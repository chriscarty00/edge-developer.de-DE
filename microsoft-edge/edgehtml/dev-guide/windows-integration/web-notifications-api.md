---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Erfahren Sie, wie die Web-Benachrichtigungs-API verwendet werden kann, damit Websites Benutzer Benachrichtigungen außerhalb des Kontexts des Microsoft Edge-Browsers senden können.
title: Web-Benachrichtigungs-API – dev-Leitfaden
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2be201a790c6fca1526c8b6eb13e4203e8e53206
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234046"
---
# Webbenachrichtigungs-API  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Mit der Web-Benachrichtigungs-API können Websites Benutzer Benachrichtigungen außerhalb des Kontexts einer Webseite innerhalb des Microsoft Edge-Browsers senden.  Ein Beispiel für dieses Feature in Aktion wäre eine Messaging-Anwendung wie Skype.  Wenn ein Benutzer eine neue Nachricht erhalten würde, wird eine Benachrichtigung auf dem Desktop angezeigt, in der Sie über die Nachricht benachrichtigt werden.  Web-Benachrichtigungen sind vollständig in die Benachrichtigungs Plattform und das Wartungs Center in Windows 10 integriert.  

## Erstellen einer Benachrichtigung  

In der folgenden CodePen wird eine Pseudo-Skype-Benachrichtigung erstellt, indem ein [Benachrichtigungs](https://msdn.microsoft.com/library/mt710818) Objekt mit den Optionen [Titel](https://msdn.microsoft.com/library/mt710826), [Symbol](https://msdn.microsoft.com/library/mt710814)und [Textkörper](https://msdn.microsoft.com/library/mt710811) eingerichtet wird:  

<iframe height='295' scrolling='no' title='Web-Benachrichtigungen' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Lesen Sie die Stift <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> -webbenachrichtigungen </a> von Microsoft Edge docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) auf <a href='https://codepen.io'> CodePen </a> .</iframe>  

Es wird dringend empfohlen, für jede Benachrichtigung ein **Symbol** anzugeben.  Dies verbessert nicht nur eine Benachrichtigung aus Sicht einer Benutzeroberfläche, sondern hilft auch, Benutzer darüber zu informieren, von wo aus die Benachrichtigung gesendet wird.  

Schauen Sie sich das folgende Video an, um eine exemplarische Vorgehensweise zum Erstellen einer webbenachrichtigung und zum Anzeigen des Verhaltens in Windows 10 zu sehen!  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### Benachrichtigungseigenschaften  

Benachrichtigungen können mit den folgenden Eigenschaften eingerichtet werden:  

:::row:::
   :::column span="1":::
      [body](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      Der Textkörper der Benachrichtigung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [dir](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      Die Richtung des Texts der Benachrichtigung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [icon](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      Die URL der Benachrichtigung, die für das zugehörige Symbol verwendet wird.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [lang](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      Die Sprache der Benachrichtigung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Berechtigungs](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      Die aktuelle benachrichtigungsanzeige Berechtigung, die der Benutzer für den aktuellen Ursprung gewährt hat.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [tag](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      Das Tag der Benachrichtigung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [title](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      Der Titel der Benachrichtigung.  
   :::column-end:::
:::row-end:::  

### Benachrichtigungsereignisse  

Die folgenden Ereignisse werden mit dem [Benachrichtigungs](https://developer.mozilla.org/docs/Web/API/Notification) Objekt verwendet:  

:::row:::
   :::column span="1":::
      [OnClick](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      Wird ausgelöst, wenn der Benutzer auf eine Benachrichtigung klickt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [OnClose](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      Wird ausgelöst, wenn eine Benachrichtigung vom Benutzer geschlossen wird, oder ein automatisches Timeout.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [OnError](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      Wird ausgelöst, wenn beim Behandeln einer Benachrichtigung ein Fehler auftritt.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onShow](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      Wird ausgelöst, wenn eine Benachrichtigung angezeigt wird.  
   :::column-end:::
:::row-end:::  

### Benachrichtigungsmethoden  

Die folgenden Methoden werden mit dem [Benachrichtigungs](https://developer.mozilla.org/docs/Web/API/Notification) Objekt verwendet:  

:::row:::
   :::column span="1":::
      [close](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      Schließt eine angezeigte Benachrichtigung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      Fordert die Berechtigung des Benutzers an, Benachrichtigungen vom aktuellen Ursprung angezeigt werden zu lassen.  
   :::column-end:::
:::row-end:::  

## Benachrichtigungs Berechtigungen  

Microsoft Edge ermöglicht Benutzern das Verwalten von Benachrichtigungs Berechtigungen für jede bestimmte Website Domäne.  Der Benutzer muss entweder " **Ja** " oder " **Nein** " auswählen, wenn er von der Domäne gefragt wird, ob Benachrichtigungen angezeigt werden sollen.  Die [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) -Methode wird verwendet, um den Berechtigungszustand als entweder `granted` , oder zu signalisieren `denied` `default` .  Der Wert `default` "gibt an, dass der Benutzer keine Entscheidung getroffen hat, die als äquivalent zu sehen ist `denied` .  

## API-Referenz  

[Web-Benachrichtigungen](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## Spezifikation  

[Web-Benachrichtigungen](https://notifications.spec.whatwg.org)  
