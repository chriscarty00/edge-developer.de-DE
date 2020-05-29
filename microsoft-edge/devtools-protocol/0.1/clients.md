---
description: Microsoft Edge devtools Protocol, Version 0,1, unterstützt die folgenden Tooling-Clients.
title: DevTools-Protokoll Version 0,1-Clients
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a537102bab7b5d914fd721aeca8bed57817e9216
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567571"
---
# DevTools-Protokoll Clients

> [!NOTE]
> Das Microsoft Edge devtools-Protokoll funktioniert nur unter [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) und später [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.

Das **devtools-Protokoll 0,1** unterstützt die folgenden Tooling-Clients.

[ ![ Microsoft Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Microsoft Visual Studio 15,7 Preview 2](../media/visual-studio-2017.png)](#microsoft-visual-studio-preview)

## Microsoft Edge devtools Preview

Sie können die eigenständige [**Microsoft Edge devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10-App aus dem Microsoft Store zum Remotedebuggen eines Hostgeräts mit Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) oder höher) verwenden.

Diese vorläufige Version 0,1 Version des devtools-Protokolls bietet grundlegende Debugfunktionen wie das Festlegen von Haltepunkten, das Durchlaufen von Code und das Untersuchen von Stapelablaufverfolgungen. In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die im [**Debuggerfenster**](../../devtools-guide/debugger.md) zur Verfügung steht, minus Cache Überprüfung (für Web Storage, Service Worker, Cache-API und IndexedDB). Derzeit ist das Microsoft Edge-Remotedebuggen auf Desktop Hosts mit Unterstützung für andere Windows 10-Geräte in zukünftigen Versionen limitiert.

Hier erfahren Sie, wie Sie das Remotedebuggen mit der Microsoft Edge devtools Preview-App einrichten. Das devtools-Protokoll befindet sich in Preview und erfordert [Windows 10 April 2018-Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) oder einen späteren Windows Insider Preview-Build auf dem Host-Computer (debugee). Die Edge devtools Preview-app (auf dem Debugger-Computer verwendet) wird im Fall Creators Update (Version 1709) und Windows Insider Preview-Builds ausgeführt.

**Auf dem Hostcomputer (debugee)...**

1. Wenn Sie ein WLAN-Netzwerk haben, stellen Sie sicher, dass das Netzwerk entweder als " **Domäne** " oder " **Privat**" gekennzeichnet ist. Sie können dies überprüfen, indem Sie die [**Windows Defender-Sicherheits Center**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) -APP öffnen, auf **Firewall & Netzwerkschutz** klicken und überprüfen, ob Ihr Netzwerk als *Domänennetzwerk* oder *privates Netzwerk*aufgeführt ist. 

    Wenn die Liste als *öffentlich*aufgeführt ist, wechseln Sie zu **Einstellungen**  >  **Netzwerk & Internet**  >  **WLAN**, klicken Sie auf Ihr Netzwerk, und schalten Sie die Schaltfläche *Netzwerkprofil* auf **Privat**.

2. Öffnen Sie die Systemsteuerung **für Entwickler** unter Windows- *Einstellungen* (suchen Sie nach *Entwickler* , und klicken Sie auf *Entwicklerfeatures verwenden*) und: 

    a. Wechseln Sie im **Entwicklermodus**. Dadurch wird das *Entwicklermodus* -Paket installiert, das Remotetools für Desktops ermöglicht.

    b. Aktivieren des [**Geräte Portals**](/windows/uwp/debug-test-perf/device-portal) (Aktivieren der*Remote Diagnose über lokale Netzwerkverbindungen*) und **Geräteerkennung** (*machen Sie Ihr Gerät für USB-Verbindungen und Ihr lokales Netzwerk sichtbar*).

    c. Aktivieren Sie die **Authentifizierung** , und geben Sie einen Benutzernamen/ein Kennwort ein.

    d. Beachten Sie, dass die IP-Adresse des Computers und der Verbindungsanschluss (50443) angezeigt werden.

3. Öffnen Sie die Registerkarten in Microsoft Edge, die Sie auf dem Clientcomputer debuggen möchten.

**Auf dem Clientcomputer (Debugger)...**

1.  Installieren und starten Sie die eigenständige [Microsoft Edge devtools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) -App aus dem Microsoft Store.

2. Öffnen Sie den Bereich **Remote** , und geben Sie den Netzwerkspeicherort (URL und Port) des Hostcomputers ein, und klicken Sie auf **verbinden**.

3. **Installieren** Sie das Zertifikat des Hostcomputers aus dem Dialogfeld "nicht *vertrauenswürdiges Zertifikat* ", das angezeigt wird.

4. Geben Sie den Benutzernamen/das Kennwort an, den Sie für die Geräte Portal Authentifizierung festgelegt haben.

5. Das *Remote* Panel lädt eine Liste von debugfähigen-Seiten Zielen auf dem Hostcomputer. Wählen Sie eine aus, um mit dem Debuggen zu beginnen.

6. Verwenden Sie die Schaltfläche **Aktualisieren** , um die Liste der Remote Seiten Ziele auf dem Hostcomputer zu aktualisieren und neu zu laden. Klicken Sie auf die Schaltfläche " **trennen** ", um zum Bildschirm "mit *einem Remotegerät verbinden* " zurückzukehren und an einen anderen Host anzufügen.

## Microsoft Visual Studio Preview

Mit dem neuesten [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) -Build (Visual Studio 15,7 Preview 1 oder höher) können Sie Microsoft Edge in einem beliebigen ASP.net-oder .net Core-Projekt in der IDE starten und Debuggen. Das devtools-Protokoll befindet sich derzeit in der Vorschau und erfordert, dass Sie einen [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Build ausführen.

Hier erfahren Sie, wie Sie Microsoft Edge-Debuggen mit Visual Studio einrichten:

1.  Installieren und starten Sie den neuesten [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) -Build (Visual Studio 15,7 Preview 1 oder höher).

2. Öffnen Sie ein vorhandenes ASP.net-oder .net Core-Projekt, oder erstellen Sie ein **Neues Projekt** , indem Sie eine der **Visual C#** .net-Vorlagen verwenden.

3. Öffnen Sie im Projekt **Mappen-Explorer**die JavaScript-Dateien, die Sie debuggen möchten, und setzen Sie Haltepunkte in der IDE genauso wie bei serverseitigem Code.

4. Drücken Sie `F5` zum Starten von Microsoft Edge, auf dem der devtools-Server ausgeführt wird. Wenn ein Haltepunkt erreicht ist, brechen Sie in Visual Studio ab und können den Code von dort aus weiter überprüfen und durchlaufen.
