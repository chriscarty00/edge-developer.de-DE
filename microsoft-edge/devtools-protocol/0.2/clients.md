---
description: Microsoft Edge devtools Protocol, Version 0,2, unterstützt die folgenden Tooling-Clients.
title: Microsoft Edge devtools-Protokoll Version 0,2-Clients
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 657d594b85c47cc1d5c80b8f2ac3ecc4bd4e4502
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567548"
---
# DevTools-Protokoll Clients

> [!NOTE]
> Version 0,2 des Microsoft Edge devtools-Protokolls funktioniert nur auf dem [Windows 10 October 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) und später in [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) -Builds.  

Das **devtools-Protokoll 0,2** unterstützt die folgenden Tooling-Clients.

[ ![ Microsoft Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Visual Studio-Code](../media/visual-studio-code.png)](#visual-studio-code) [ ![ Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)

## Microsoft Edge devtools Preview

Sie können die eigenständige [**Microsoft Edge devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10-App aus dem Microsoft Store zum Remotedebuggen eines Hostgeräts mit Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) oder höher) verwenden.

Version 0,2 des devtools-Protokolls bietet neue Domänen für das Debuggen von Stilen und Layouts sowie Konsolen-APIs sowie die in Version 0,1 eingeführten Kernskript Debugging-Funktionen. In der Benutzeroberfläche von Edge devtools wird dadurch die Funktionalität übersetzt, die in den Panels [**Elemente**](../../devtools-guide/elements.md), [**Konsole**](../../devtools-guide/console.md) und [**Debugger**](../../devtools-guide/debugger.md) zur Verfügung steht. Derzeit ist das Microsoft Edge-Remotedebuggen auf Desktop Hosts mit Unterstützung für andere Windows 10-Geräte in zukünftigen Versionen limitiert.

Hier erfahren Sie, wie Sie das Remotedebuggen mit der Microsoft Edge devtools Preview-App einrichten. Das devtools-Protokoll, Version 0,2, erfordert [Windows 10 Oktober 2018-Update](/windows/uwp/whats-new/windows-10-build-17763) oder einen späteren Windows Insider Preview-Build auf dem Hostcomputer (debugee). Die Edge devtools Preview-app (auf dem Debugger-Computer verwendet) wird unter Windows 10 Version 16299 (Windows 10 Fall Creators Update, 10/2017) oder höher ausgeführt.

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

## Visual Studio Code

Mit dem [Debugger für Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) -vs-Code Erweiterung können Sie Skripts, die in Microsoft Edge ausgeführt werden, direkt in Visual Studio-Code Debuggen. Die Erweiterung setzt voraus, dass Sie Ihre Webanwendung von localhost aus bedienen, was Sie entweder über die Befehlszeile oder über eine [Aufgabe](https://code.visualstudio.com/docs/editor/tasks)starten können.

Erste Schritte:

1. Installieren Sie den [Debugger für Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) -vs-Code Erweiterung.

2. Starten Sie vs-Code neu, öffnen Sie den Ordner, in dem sich das Projekt befindet, das Sie debuggen möchten, und legen Sie Haltepunkte im Code ab.

3. Konfigurieren Sie eine localhost- [Startaufgabe](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) , um die gewünschte Seite Ihres Projekts zu öffnen: **Debug**-  >  **Add-Konfiguration.**... Zum Beispiel:

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    [*Die Verwendung des Debuggers*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) bietet mehr Informationen zu den Startkonfigurationseinstellungen. 

4. Starten Sie den Server auf localhost, und klicken Sie auf die Schaltfläche **Debuggen starten** (wiedergeben), oder starten Sie `F5` Microsoft Edge. Wenn ein Haltepunkt erreicht ist, brechen Sie in den vs-Code auf und können den Code von dort aus weiter prüfen und durchlaufen.

Weitere Informationen finden Sie im [vs-Code-Debugger für Microsoft Edge-](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) Dokumentation.

## Microsoft Visual Studio

Mit der neuesten Version von [**Visual Studio**](https://www.visualstudio.com) (Visual Studio 15,8 oder höher), die unter [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763)ausgeführt wird, können Sie Microsoft Edge in einem beliebigen ASP.net-oder .net Core-Projekt in der IDE starten und Debuggen.

Hier erfahren Sie, wie Sie Microsoft Edge-Debuggen mit Visual Studio einrichten:

1.  Installieren und starten Sie das neueste [**Visual Studio**](https://www.visualstudio.com/) (Visual Studio 15,8 oder höher).

2. Öffnen Sie ein vorhandenes ASP.net-oder .net Core-Projekt, oder erstellen Sie ein **Neues Projekt** , indem Sie eine der **Visual C#** .net-Vorlagen verwenden.

3. Öffnen Sie im Projekt **Mappen-Explorer**die JavaScript-Dateien, die Sie debuggen möchten, und setzen Sie Haltepunkte in der IDE genauso wie bei serverseitigem Code.

4. Drücken Sie `F5` zum Starten von Microsoft Edge, auf dem der devtools-Server ausgeführt wird. Wenn ein Haltepunkt erreicht ist, brechen Sie in Visual Studio ab und können den Code von dort aus weiter überprüfen und durchlaufen.
