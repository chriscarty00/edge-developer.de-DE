---
description: Features, die dem Microsoft Edge-devtools im Windows 10 April 2018-Update (EdgeHTML 17) hinzugefügt wurden
title: DevTools in EdgeHTML 17
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Web-Entwicklung, F12-Tools, devtools, edgehtml 17
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 937525f349a1db650b795db1efb983f1359fcaa5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11234030"
---
# DevTools im Windows 10 April 2018-Update (EdgeHTML 17)

Die EdgeHTML 17-Version von devtools wird auf zwei Arten ausgeliefert: als herkömmliche in-Browser ( `F12` )-Tools für Microsoft Edge und Vorschau als eigenständige [Windows 10-App](#microsoft-edge-devtools-app-preview) aus dem Microsoft Store!

Die Tools wurden mit einer Reihe wichtiger Features aktualisiert, einschließlich der grundlegenden Unterstützung für das [Remotedebuggen](../index.md#remote-debugging) (über unser neues [devtools-Protokoll](#devtools-protocol)), [PWA-Debuggingfunktionen](#pwa-debugging), [IndexedDB-Cache-Verwaltung](#indexeddb-inspection), [vertikales Andocken](#docking-to-the-right-in-microsoft-edge) und vieles mehr! Darüber hinaus haben wir den Gesamtaufwand für die [Umgestaltung](./edgehtml-16.md) der letzten Version im Rahmen der laufenden Investitionen in Leistung und Zuverlässigkeit fortgesetzt.

Hier sind die neuesten Microsoft Edge devtools-Features, die im [Windows 10 April 2018-Update](/windows/uwp/whats-new/windows-10-build-17134) ([EdgeHTML 17](https://aka.ms/devguide_edgehtml_17)) ausgeliefert wurden.

## Microsoft Edge devtools App Preview

![Microsoft Edge devtools-App](../../devtools-protocol/media/microsoft-edge-devtools.png) 

Die [Microsoft Edge-devtools](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) sind jetzt für die Vorschau als eigenständige Windows 10-App aus dem Microsoft Store verfügbar. Die Store-Version enthält einen Bereich *Auswahl* zum Anfügen an geöffnete lokale und remote Seitenziele und ein Layout im Registerkartenformat für den einfachen Wechsel zwischen DevTools-Instanzen. Ebenfalls exklusiv für die devtools-APP ist die Möglichkeit zum Debuggen von Webinhalten in apps \(wie Add-Ins für Office, Cortana, EdgeHTML [WebView](../../hosting/webview/index.md)und [Windows-installierte PWAs](../../progressive-web-apps/windows-features.md)\).

Die Edge-devtools sind auch weiterhin ( `F12` ) im Browser verfügbar (ohne den Auswahlbereich).

Die Entkopplung des devtools aus dem Browser bietet die folgenden Vorteile für UX und Architektur:

- Die devtools werden in einer separaten App-Container-Sandbox von Microsoft Edge ausgeführt, was eine höhere Zuverlässigkeit für beide bietet.
- Die APP bietet einen einfachen Wechsel zwischen aktiven devtools-Instanzen Registerkarten (anstatt zwischen geöffneten Microsoft Edge-Registerkarten wechseln zu müssen).
- Wir sind in der Lage, das *EdgeHTML* -Browsermodul zu instrumentieren und es im größeren devtools-Ökosystem mit [browserübergreifenden APIs](https://github.com/WICG/devtools-protocol/)zu öffnen.
- Wir können devtools-Updates unabhängig vom Windows-und EdgeHTML-Freigabezyklus versenden.

Im *devtools-Leitfaden* finden Sie weitere Informationen zum [lokalen und Remotedebuggen mithilfe der devtools-App](../index.md).

## DevTools-Protokoll

Entwicklertools können das [**Microsoft Edge devtools-Protokoll**](../../devtools-protocol/index.md) verwenden, um den Microsoft Edge-Browser zu überprüfen und zu debuggen. Sie stellt eine Reihe von Methoden und Ereignissen bereit, die in verschiedenen [Domänen](../../devtools-protocol/0.1/domains/index.md) der EdgeHTML-Modul Instrumentation organisiert sind.

 Tooling-Clients können diese Methoden aufrufen und diese Ereignisse über JSON Web Socket-Nachrichten überwachen, die mit dem von Microsoft Edge oder dem [Windows Device Portal](/windows/mixed-reality/using-the-windows-device-portal)gehosteten *devtools-Server* ausgetauscht werden. 
 
 Microsoft Edge devtools verwendet dieses Protokoll, um das [Remotedebuggen](../../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) eines Hostcomputers mit Microsoft Edge vom [eigenständigen devtools-Client](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) zu aktivieren, der im Microsoft Store verfügbar ist. Derzeit ist diese Preview-Unterstützung auf das js-Debuggen einer anderen Kante auf einem anderen Desktop Gerät oder virtuellen Computer limitiert. Im Laufe der Zeit fügen wir Unterstützung für den vollständigen Satz von devtools für jede EdgeHTML-Instanz auf einem Windows 10-Gerät hinzu.  
 
 Die neuesten Builds für die [**Visual Studio-Vorschau**](https://www.visualstudio.com/vs/preview/) (Visual Studio 15,7 Preview 1 oder höher) verwenden das devtools-Protokoll, um das Starten und Debuggen von Microsoft Edge (JavaScript-Code) in der Visual Studio-IDE eines beliebigen ASP.net-oder .net Core-Projekts zu ermöglichen.

## IndexedDB Inspektion

Neu im [**Debugger**](../debugger.md) diese Version ist ein [IndexedDB-Manager](../storage.md#indexeddb-manager) mit Unterstützung für das überprüfen und Aktualisieren Ihrer Objektspeicher und das Löschen einzelner Schlüssel-Wert-Einträge. Erwarten Sie in zukünftigen Versionen noch mehr Funktionalität.

## PWA-Debuggen

Die Unterstützung für das Debuggen von Progressive Web Apps (PWAs) ist jetzt standardmäßig aktiviert und bietet Tool Registerkarten für [**Dienstmitarbeiter**](../service-workers.md), [**Cache-API**](../storage.md#cache-manager)und [**IndexedDB**](../storage.md#indexeddb-manager) -Verwaltung.

Darüber hinaus verfügt die [Symbolleiste des Netzwerk Panels](../network.md#toolbar) über eine neue Schaltfläche, **Bypass Service Worker für alle Netzwerkanforderungen**, um Ihre registrierten Service Mitarbeiter als Netzwerk Proxys ein-und auszuschalten:

![Schaltfläche "Netzwerk-Symbolleiste": umgehen von Service Worker für alle Netzwerkanforderungen](../media/network_toolbar_bypass_sw.png)

Sie können Ihre [PWA als installierte Windows 10-App](../../progressive-web-apps/windows-features.md) Debuggen, indem Sie Sie in der Auswahl der [eigenständigen devtools-App](../index.md#microsoft-store-app)in der Liste der [**lokalen**](../../progressive-web-apps/windows-features.md#debug-your-pwa-edgehtml-as-a-windows-app) Ziele (Browserregister Karte/PWA/WebView) auswählen.  

## Andocken rechts in Microsoft Edge

Sie können jetzt das devtools rechts neben der Seite, die Sie Debuggen, in Microsoft Edge andocken, zusätzlich zum Andocken am unteren Rand und zum Abdocken des devtools aus dem Browserfenster. Verwenden `Ctrl+Shift+D` Sie diese Schaltfläche, um zwischen dem **Dock unten**, dem **Dock rechts**und dem **Abdocken** von Positionen oder den Symbolen in der oberen rechten Ecke des devtools zu wechseln:

![DevTools (in unverankertem Zustand) Andockoptionen](../media/docking_buttons.png) 
