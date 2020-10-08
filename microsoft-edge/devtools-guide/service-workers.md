---
description: Verwenden des Service Worker-Panels zum Verwalten und Debuggen Ihrer Dienstmitarbeiter
title: DevTools-Debugger – Dienstmitarbeiter
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, Debugger, Debuggen, PWA, Service Worker, Cache-API
ms.custom: seodec18
ms.openlocfilehash: 8e1fa62358657a47ce40d0742f95a76f2586d0c8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567592"
---
# Service Workers

Das **Dienstpersonal** -Panel enthält Tools zum Verwalten und Debuggen der Dienstmitarbeiter für Ihre Website, um Ihnen zu helfen:

 - Verschaffen Sie sich einen Überblick über alle Servicemitarbeiter, die Ihrer Website zugeordnet sind, sowie Einzelheiten zu deren Umfang und Status.
 - **Aktualisieren** und verwalten (**aufheben**der Registrierung) der Service Worker-Registrierung für den angegebenen Bereich
 - **Pushen** einer testbenachrichtigung
 - **Stopp** / **Starten** einzelner Servicemitarbeiter und
 - Über **prüfen** der ausgewählten Dienstmitarbeiter in einem separaten Debuggerfenster

![Bereich ' Dienstmitarbeiter Übersicht '](./media/service_worker.png)

Beachten Sie die folgenden Informationen zum Service Worker-Debuggen in Edge devtools:

 - Beim Debuggen eines Dienst Arbeitsthreads wird eine neue Instanz des devtools, die sich von den Tools der Seite trennt, gestartet, da Dienstmitarbeiter auf mehreren Registerkarten freigegeben werden können.
 - Die [**Elemente**](./elements.md) und [**Emulations**](./emulation.md) Panels fehlen im Service Worker-Debugger, da Dienstmitarbeiter im Hintergrund ausgeführt werden und das Front-End Ihrer APP nicht direkt steuern.
 - Zurzeit wird der Netzwerkdatenverkehr für einen Dienstmitarbeiter nur von der devtools-Debugsitzung für diesen Worker und nicht von der Debugger-Instanz für die Seite selbst gemeldet.
 - Wenn Sie einen **Push** aus dem devtools simulieren möchten, müssen Sie einen *Push* -Ereignis-Listener zu Ihrem Dienstmitarbeiter hinzufügen, um dessen Wirkung zu beobachten. Im folgenden Beispiel wird "Test Push Message from devtools" in Ihrer Service Worker- **Konsole**gedruckt.

   ```JavaScript
   self.addEventListener('push', function(event){
       console.log(event.data.text());
   });
   ```

Im folgenden finden Sie einige allgemeine Punkte, die Sie bei der Verwendung von Servicemitarbeitern beachten sollten:

- **Nur HTTPS.** Dienstmitarbeiter funktionieren nicht in http; Sie müssen HTTPS verwenden. Sie können Dienstmitarbeiter jedoch zu `localhost` Testzwecken registrieren.

- **Kein DOM-Zugriff zulässig.** Wie bei Web Workern erhalten Sie keinen Zugriff auf das Objektmodell der Seite. Das bedeutet, dass Sie, wenn Sie etwas über die Seite ändern müssen, [`postMessage`](https://developer.mozilla.org/docs/Web/API/Worker/postMessage) von der Dienstmitarbeiter auf die Seite verwenden müssen, damit Sie DOM-Änderungen auf der Seite behandeln können.

- **Führt eine separate Seite aus.** Da diese Skripts nicht an die Lebensdauer einer Seite gebunden sind, ist es wichtig zu verstehen, dass Sie nicht den gleichen Kontext wie die Seite aufweisen. Abgesehen davon, dass Sie keinen Zugriff auf das DOM haben (wie bereits erwähnt), haben Sie keinen Zugriff auf die gleichen Variablen, die auf der Seite verfügbar sind.

- **Überschreibt den *App-Cache*.** Der APP-Cache wird ignoriert, wenn Dienstmitarbeiter verwendet werden. Die Service Worker-API soll den App-Cache vollständig verdrängen, indem Sie dem Web-Entwickler eine genauere Steuerung bietet.

  - **Das Skript kann nicht auf CDN lauten.** Die JavaScript-Datei für den Dienstmitarbeiter kann nicht in einem Inhalts Verteilungsnetzwerk (CDN) gehostet werden, sondern muss sich in der gleichen Domäne wie die Seite befinden. Wenn Sie möchten, können Sie jedoch Skripts aus Ihrem CDN importieren.

- **Kann jederzeit gekündigt werden.** Dienstmitarbeiter sollen kurzlebig sein und ihre Lebenszeit ist an Ereignisse gebunden. Insbesondere können Servicemitarbeiter ein Zeitlimit angeben, in dem Sie die Ausführung ihrer Ereignishandler beenden müssen. In anderen Fällen kann es vorkommen, dass der Browser oder das Betriebssystem einen Dienstmitarbeiter beendet, der sich auf die Akku-, CPU-oder Speicherauslastung auswirkt. Vermeiden Sie in beiden Fällen die Verwendung globaler Variablen im Service Worker-Skript, wenn für ein nachfolgendes Ereignis, das verarbeitet wird, eine andere Dienst Arbeitskraft-Instanz verwendet wird.

- **Nur asynchrone Anforderungen zulässig.** Synchrone XMLHttpRequest ist hier nicht zulässig! Weder ist localStorage, daher empfiehlt es sich, IndexedDB und die zuvor beschriebene neue Caches-API zu verwenden.

- **Der Dienstmitarbeiter für den Bereich ist 1:1.** Sie können nur einen Dienstmitarbeiter pro Bereich haben. Das bedeutet, wenn Sie versuchen, einen anderen Dienstmitarbeiter für einen Bereich zu registrieren, der bereits über einen Dienstmitarbeiter verfügt, wird dieser Dienstmitarbeiter aktualisiert.
