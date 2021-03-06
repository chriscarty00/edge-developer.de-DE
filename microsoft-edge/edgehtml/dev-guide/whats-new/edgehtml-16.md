---
description: Dieses Handbuch bietet eine Übersicht über die Entwicklerfeatures und -standards, die in EdgeHTML 16 enthalten sind.
title: Neue Features und APIs in EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, web development, html, css, javascript, developer
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399197"
---
# <a name="whats-new-in-edgehtml-16"></a>Neues in EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Hier finden Sie eine Liste der neuen und aktualisierten Features, die im Rahmen des [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\) auf der [EdgeHTML 16-Webplattform](https://blogs.windows.com/msedgedev/2017/10/17) ausgeliefert wurden.  Änderungen an bestimmten Windows Insider Preview-Builds finden Sie unter [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) und [What's New in EdgeHTML](../whats-new.md).  

Hier sehen Sie den Permalink für die folgende Liste der Änderungen:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .  

## <a name="new-and-updated-features"></a>Neue und aktualisierte Features  

### <a name="css-grid-layout"></a>CSS-Rasterlayout  

Microsoft Edge unterstützt jetzt die implementierung ohne Präfix von [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).  [Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) definiert ein zweidimensionales rasterbasiertes Layoutsystem, das mehr Layoutfluidität als möglich durch positionierung mithilfe von Floats oder Skripts ermöglicht.  Im folgenden Beispiel wird css Grid Layout verwendet, um die Struktur für eine einfache Webseite zu erstellen.  

<iframe height='303' scrolling='no' title='CSS-Rasterlayout' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Weitere Informationen finden Sie im <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> Stift-CSS-Rasterlayout </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) auf </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

### <a name="css-object-fit-and-object-position"></a>CSS-Objekt-Anpassung und Objektposition  

In EdgeHTML 16 wird die Unterstützung von CSS-Eigenschaften und [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) . [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position)  Diese Eigenschaften steuern die Position und Größe des ersetzten Inhalts innerhalb des Inhaltsfelds.  

### <a name="developer-tools"></a>Entwicklungstools  

In dieser Version haben wir eine wichtige Umgestaltung von Microsoft Edge DevTools für eine verbesserte Robustheit und Leistung gestartet und außerdem eine Reihe neuer Features hinzugefügt, die Sie heute auf [Windows-Insider-Builds verwenden](https://insider.windows.com) können.  Weitere Informationen zu den Geänderten finden Sie im [Microsoft Edge DevTools-Handbuch.](../whats-new.md)  

### <a name="javascript"></a>JavaScript  

[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) baut auf Javascript-Leistungsoptimierungen früherer Versionen auf, indem die Fähigkeit des Moduls zum Zurück-/Zurückspeichern von Funktionen erweitert, polymorphe Inlinecaches verwendet und Funktionen mit Blöcken optimiert `try` / `finally` werden.  

Darüber hinaus sind features first previewed in EdgeHTML 15 jetzt stabil und standardmäßig aktiviert:  

#### <a name="new-features"></a>Neue Features  

Standardmäßig aktiviert  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([Demo](https://webassembly.org/demo)\)  
*   [Freigegebener Speicher und Atome](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a>Payments Request-API  

Die [Zahlungsanforderungs-API](../windows-integration/payment-request-api.md) ist ein offener, browserübergreifender Standard, mit dem Browser als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden \(z. B. Kreditkarten\) fungieren können, die Verbraucher in der Cloud gespeichert haben.  Die API in EdgeHTML 16 wurde so aktualisiert, dass sie der neuesten W3C [Payment Request-API-Spezifikation](https://w3c.github.io/payment-request) entspricht.  Dies umfasst Folgendes:  

*   Unterstützung für die `canMakePayment()` Methode  
*   Unterstützung für die `requestId` Eigenschaft  
*   Unterstützung für die `id` Eigenschaft  
*   Der Standardwert für den Parameter `complete()` der Methode wurde von " " in `result` "unbekannt" geändert.  

### <a name="service-workers"></a>Service Workers  

[Service Workers](https://www.w3.org/TR/service-workers-1) sind ereignisgesteuerte Skripts, die im Hintergrund einer Webseite ausgeführt werden.  Service workers aktivieren Funktionen, die bisher nur für systemeigene Apps verfügbar waren, z. B. das Abfangen und Behandeln von Anforderungen aus dem Netzwerk, das Verwalten und Behandeln der Hintergrundsynchronisierung, des lokalen Speichers und der Pushbenachrichtigungen.  Die Unterstützung für Servicemitarbeiter befindet sich noch in der Entwicklung, Aber Sie können Ihre PWA in Microsoft Edge mit unserer experimentellen Service worker-Unterstützung testen, indem Sie das Service Worker-Feature in `about:flags` aktivieren.  

### <a name="webvr"></a>WebVR  

WebVR für Microsoft Edge hat unterstützung für [Bewegungscontroller hinzugefügt.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)  Diese Controller haben eine präzise Position im Raum, sodass eine feinkörnige Interaktion mit digitalen Objekten in der virtuellen Realität ermöglicht wird.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Bewegungscontroller" lightbox="../media/MotionControllers.jpg":::
   Bewegungscontroller  
:::image-end:::  

WebVR wurde außerdem optimiert, um zwei verschiedene Arten von Erfahrungen zu unterstützen.  

**Windows Mixed Reality PCs** – Desktops und Laptops mit integrierten Grafiken.  Wenn sie an diese Geräte angeschlossen werden, werden unsere immersiven Headsets mit 60 Frames pro Sekunde ausgeführt.  
**Windows Mixed Reality Ultra PCs** – Desktops und Laptops mit separaten Grafiken.  Wenn sie an diese Geräte angeschlossen werden, werden unsere immersiven Headsets mit 90 Frames pro Sekunde ausgeführt.  

Beide Setups unterstützen dieselbe immersive Video- und Spielerfahrung.  

Weitere Informationen zu den anstehenden Windows Mixed Reality-Updates finden Sie im [Windows Mixed Reality-Blogbeitrag](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) zum Feiertagsupdate.  

Anleitungen und Demos finden Sie im [WebVR Developer Guide](/microsoft-edge/webvr).  

 > [!NOTE] 
 > Da die WebVR-Spezifikation noch in der Entwicklung ist, kann sich die Implementierung von Microsoft Edge später ändern.  

## <a name="new-apis-in-edgehtml-16"></a>Neue APIs in EdgeHTML 16  

Hier ist die vollständige Liste der neuen APIs in EdgeHTML 16.  Sie sind im Format `[interface name].[api name]` aufgeführt.

> [!NOTE] 
> Obwohl die folgenden APIs im DOM verfügbar gemacht werden, ist das End-to-End-Verhalten einiger möglicherweise noch in der Entwicklung.  Das offizielle Wort zur Featureunterstützung finden Sie unter Microsoft Edge-Plattformstatus. [](https://developer.microsoft.com/microsoft-edge/platform/status)  

---  

<iframe height='559' scrolling='no' title='Neue APIs in EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Weitere Informationen finden Sie in den neuen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> APIs des Stifts in EdgeHTML 16 </a> von MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) auf </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

---  

## <a name="previous-edgehtml-releases"></a>Frühere EdgeHTML-Versionen  

[EdgeHTML 12 / Windows Build 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Windows Build 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14 / Windows Build 14393 (8/2016)](./edgehtml-14.md)  

[EdgeHTML 15 / Windows Build 15063 (4/2017)](./edgehtml-15.md)  
