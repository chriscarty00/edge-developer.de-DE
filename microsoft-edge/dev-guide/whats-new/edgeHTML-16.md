---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Dieser Leitfaden enthält eine Übersicht über die Entwicklerfeatures und-Standards, die in Microsoft Edge enthalten sind.
title: Dev-Leitfaden
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 36c5e6530ff584a97e4b42910757495362a1960d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566782"
---
# Neuerungen in EdgeHTML 16

Nachfolgend finden Sie eine Liste der neuen und aktualisierten Features, die in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17/edgehtml-16-fall-creators-update/) Web Platform ausgeliefert wurden, als Teil des [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update/) (10/2017, Build 16299). Änderungen an bestimmten Windows Insider Preview-Builds finden Sie im [Microsoft Edge-Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/) und [Neuerungen in EdgeHTML](../whats-new.md).

Hier ist der Permalink für die folgende Liste der [https://aka.ms/devguide_edgehtml_16](https://aka.ms/devguide_edgehtml_16) Änderungen:

## Neue und aktualisierte Features

### CSS-Raster Layout

Microsoft Edge unterstützt jetzt die Implementierung des CSS- [Rasterlayouts](https://www.w3.org/TR/css-grid-1/)mit unpräfixen. Das [Rasterlayout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) definiert ein zweidimensionales Grid-basiertes Layoutsystem, das mehr Layout-Fluidität als möglich mit der Positionierung mithilfe von Floats oder Skripts ermöglicht. Im folgenden Beispiel wird das CSS-Raster Layout verwendet, um die Struktur für eine einfache Webseite zu erstellen.


<iframe height='303' scrolling='no' title='CSS-Raster Layout' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Sehen Sie sich das Layout "Stift <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> -CSS-Raster" </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .
</iframe>


### CSS `object-fit` und `object-position`

EdgeHTML 16 führt Unterstützung für CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) -Eigenschaften und [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Diese Eigenschaften steuern die Position und Größe des ersetzten Inhalts im Feldinhalt.  

### Entwicklungstools

In dieser Version haben wir einen wichtigen Microsoft Edge devtools-Umgestaltungs Aufwand für verbesserte Robustheit und Leistung gestartet und außerdem eine Reihe neuer Funktionen hinzugefügt, die Sie heute auf [Windows-Insider](https://insider.windows.com/) -Builds verwenden können.  Weitere Informationen zu den Änderungen finden Sie im [Microsoft Edge devtools-Leitfaden](../../devtools-guide/whats-new.md) .

### JavaScript

[EdgeHTML 16 baut auf JavaScript-Leistungs](https://blogs.windows.com/msedgedev/2017/10/31/optimizations-webassembly-sharedarraybuffer-atomics-edgehtml-16/#FodxEPHxR4WkbtyA.97) Optimierungen früherer Versionen auf, indem die Fähigkeit des Chakra-Moduls erweitert wird, Funktionen zu verzögern/erneut zu verzögern, polymorphe Inline-Caches zu verwenden und Funktionen mit *try/finally* -Blöcken zu optimieren.

Darüber hinaus sind Features, die in EdgeHTML 15 erstmals in der Vorschau angezeigt werden, jetzt stabil und standardmäßig aktiviert:

#### Neue Features (standardmäßig aktiviert)

* [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP ([Demo](https://webassembly.org/demo/))
* [Shared Memory und Atomics](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

### API für Zahlungsanforderungen

Die [Zahlungs Anforderungs-API](../windows-integration/payment-request-api.md) ist ein offener, browserübergreifender Standard, mit dem Browser als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden fungieren können (beispielsweise Kreditkarten), die von Verbrauchern in der Cloud gespeichert wurden.  Die API in EdgeHTML 16 wurde so aktualisiert, dass Sie der neuesten API-Spezifikation für die W3C [-Zahlungsanforderung](https://w3c.github.io/payment-request/) entspricht. Dies umfasst Folgendes:
* Unterstützung für die `canMakePayment()` Methode
* Unterstützung für die `requestId` Eigenschaft
* Unterstützung für die `id` Eigenschaft
* Der Standardwert für den `complete()` Parameter der Methode `result` wurde von "" in "unbekannt" geändert.

### Dienstmitarbeiter

[Dienstmitarbeiter](https://www.w3.org/TR/service-workers-1/) sind ereignisgesteuerte Skripts, die im Hintergrund einer Webseite ausgeführt werden. Dienstmitarbeiter aktivieren Funktionen, die zuvor nur für systemeigene apps verfügbar waren, wie das Abfangen und behandeln von Anforderungen aus dem Netzwerk, verwalten und behandeln von Hintergrundsynchronisierung, lokalem Speicher und Push-Benachrichtigungen. Die Unterstützung für Service Worker befindet sich noch in der Entwicklung, doch Sie können Ihre PWA in Microsoft Edge mit unserem experimental Service Worker-Support testen, indem Sie das Feature "Dienstmitarbeiter" in **about: Flags**aktivieren.

### WebVR
WebVR für Microsoft Edge hat Unterstützung für [Motion Controller](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)hinzugefügt. Diese Controller haben eine präzise Position im Raum, was eine feinkörnige Interaktion mit digitalen Objekten in der virtuellen Realität ermöglicht.

![Motion-Controller](../media/MotionControllers.jpg)

WebVR wurde ebenfalls optimiert, um zwei unterschiedliche Arten von Erfahrungen zu unterstützen.

**Windows Mixed Reality-PCs** – Desktops und Laptops mit integrierter Grafik.  Wenn Sie an diese Geräte angeschlossen sind, können unsere immersiven Headsets mit 60 Frames pro Sekunde ausgeführt werden.  
**Windows Mixed Reality Ultra-PCs** – Desktops und Laptops mit diskreten Grafiken. Wenn Sie an diese Geräte angeschlossen sind, können unsere immersiven Headsets mit 90 Frames pro Sekunde ausgeführt werden.   

Beide Setups unterstützen die gleichen immersiven Video-und Spielerlebnisse. 

Weitere Informationen zu den bevorstehenden Windows-Mixed-Reality-Updates finden Sie im Blogbeitrag [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update/) Holiday Update. 

Anleitungen und Demos finden Sie im [WebVR-Entwicklerhandbuch](https://docs.microsoft.com/microsoft-edge/webvr/).

 > [!NOTE] 
 > Da sich die WebVR-Spezifikation noch in der Entwicklung befindet, kann sich die Implementierung von Microsoft Edge später in der Zeile ändern.

## Neue APIs in EdgeHTML 16

Hier finden Sie die vollständige Liste der neuen APIs in EdgeHTML 16. Sie werden im Format **[Schnittstellenname] aufgeführt. [ API-Name]**.

> [!NOTE] 
> Obwohl die folgenden APIs im DOM verfügbar gemacht werden, kann sich das End-to-End-Verhalten einiger Entwickler weiterhin entwickeln. Informationen zum offiziellen Word-Feature-Support finden Sie im [Microsoft Edge-Platt Form Status](https://developer.microsoft.com/microsoft-edge/platform/status/) .

<iframe height='559' scrolling='no' title='Neue APIs in EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Weitere Informationen finden Sie in den neuen APIs für Stifte <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> in EdgeHTML 16 </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) auf <a href='https://codepen.io'> CodePen </a> .</iframe></p>

<h2 id="previous-edgehtml-releases">Vorherige EdgeHTML-Versionen</h2>
<p><a href="https://aka.ms/devguide_edgehtml_12" data-raw-source="[EdgeHTML 12 / Windows build 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)">EdgeHTML 12/Windows Build 10240 (7/2015)</a>

[EdgeHTML 13/Windows Build 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows Build 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows Build 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)
