---
description: Kennenlernen der Microsoft Edge (Chrom)-Entwickler Tools
title: Microsoft Edge (Chrom)-Entwickler Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: ba925c402d33ba75c558006c7c43c5dc05515911
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003936"
---
# Microsoft Edge (Chrom)-Entwickler Tools  

Microsoft Edge hat das Chrom-Open-Source-Projekt angenommen, um eine bessere Web-Kompatibilität und geringere Fragmentierung unterschiedlicher zugrunde liegender Webplattformen zu schaffen.  Diese Änderung sollte es für Sie einfacher machen, ihre Websites in Microsoft Edge zu erstellen und zu testen und sicherzustellen, dass Sie auch in einem anderen Chrom basierten Browser wie erwartet funktionieren (wie Google Chrome, Vivaldi, Opera oder Brave \).  

Da das Web in einem immer größer werdenden Array von Gerätetypen in der Nutzung zugenommen hat, ist die Komplexität und der Overhead beim Testen von Websites explodiert. Da Webentwickler \ (insbesondere bei kleinen Unternehmen \) auf so vielen unterschiedlichen Systemen testen müssen, ist es möglicherweise nahezu unmöglich, sicherzustellen, dass Websites auf allen Gerätetypen und allen Browsern optimal funktionieren.  Nachdem Microsoft Edge nun auf Chrom basiert, hat das Microsoft Edge-Team die Matrix vereinfacht, indem die Microsoft Edge-Webplattform mit anderen Chrom basierten Browsern ausgerichtet und eine erstklassige Entwicklertools-Umgebung bereitgestellt wird, sowohl im Browser als auch mit den anderen Entwicklertools, die Sie täglich verwenden (beispielsweise Visual Studio-Code \).  

Wenn Sie Microsoft Edge Auschecken und sich hauptsächlich in einem Chrom basierten Browser entwickeln, sollten Sie sich wie zu Hause fühlen.  Die Microsoft Edge \ (Chrom \)-Entwicklertools funktionieren auf die gleiche Weise wie die Entwicklertools, die Sie bereits kennen und verwenden.  Weitere Informationen finden Sie unter [Neuerungen in Microsoft Edge (Chrom) devtools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="Microsoft Edge (Chrom) devtools":::
   Microsoft Edge (Chrom) devtools  
:::image-end:::  

Wenn Sie die nächste Version von Microsoft Edge Auschecken und zuvor in Microsoft Edge \ (EdgeHTML \) entwickelt haben, verfügen Sie nun über einige hervorragende neue Tools, die es einfacher und schneller machen, ihre Websites in Microsoft Edge zu erstellen und zu testen!  

## Öffnen des devtools  

Wenn Sie das devtools noch nie zuvor verwendet haben, handelt es sich bei den Microsoft Edge-Entwicklertools um eine Reihe von Tools, die direkt in den Microsoft Edge-Browser integriert sind.  Mit diesen devtools können Sie die folgenden Aktionen ausführen:  

*   Überprüfen und Ändern der HTML-Website  
*   CSS bearbeiten und sofort anzeigen, wie Ihre Website gerendert wird  
*   Anzeigen aller `console.log()` Anweisungen aus dem Front-End-JavaScript-Code  
*   Debuggen des Skripts durch Festlegen von Haltepunkten und Durchführen einer Zeile für Zeile  

alle direkt im Browser.  Dies sind nur einige Beispiele für einige der Features, die die devtools bereitstellen, damit Sie Ihre Websites in Microsoft Edge einfacher und schneller erstellen und testen können.  

So öffnen Sie das devtools  

*   drücken Sie `F12` 
*   Drücken Sie `Ctrl` + `Shift` + `I` auf Windows \ ( `Command` + `Option` + `I` unter macOS \).  

Wenn Sie den HTML-oder CSS-Code für ein Element auf Ihrer Website anzeigen möchten, klicken Sie mit der rechten Maustaste auf das Element, und wählen Sie über **prüfen** aus, um in das Panel Elemente zu wechseln.  Sie können auch `Ctrl` + `Shift` + `C` auf Windows \ ( `Command` + `Option` + `C` unter macOS \) drücken, um das devtools im Kontroll **Element Modus** zu öffnen, in dem Sie ein Element auf der Website auswählen und den HTML-und **Elements** CSS-Code im Element Panel sehen können.  

Wenn Sie die Protokolle aus Ihrem Front-End-JavaScript-Code anzeigen oder schnell ein Skript ausführen möchten, drücken Sie `Ctrl` + `Shift` + `J` auf Windows oder `Command` + `Option` + `J` auf macOS, um den Konsolenbereich im devtools zu starten.  

## Grundlegende Tools  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="Microsoft Edge (Chrom) devtools":::
   Microsoft Edge (Chrom) devtools-Kern Tools  
:::image-end::: 

Zu den Microsoft Edge \ (Chromium \) devtools gehören die folgenden Panels.  

*   Einen Bereich **Elemente** zum Bearbeiten von HTML und CSS, Untersuchen von Barrierefreiheitseigenschaften, Anzeigen von Ereignis-Listenern und Festlegen von Haltepunkten für DOM-Mutationen  
*   Eine **Konsole** zum Anzeigen und Filtern von Protokollmeldungen, zum Überprüfen von JavaScript-Objekten und DOM-Knoten sowie zum Ausführen von JavaScript im Kontext des ausgewählten Fensters oder Rahmens  
*   Ein **Quellen** Panel zum Öffnen und Live Bearbeiten Ihres Codes, Festlegen von Haltepunkten, durchlaufen des Codes und Anzeigen des Zustands Ihrer Website in einer Zeile mit JavaScript gleichzeitig  
*   Einen Bereich **Netzwerk** zum Überwachen und Überprüfen von Anforderungen und Antworten aus dem Netzwerk- und Browsercache   
*   Einen Bereich **Leistung**, um die Zeit und Systemressourcen zu ermitteln, die für Ihre Website erforderlich sind  
*   Einen Bereich **Arbeitsspeicher** zum Messen der Nutzung von Speicherressourcen und Vergleichen von Heap-Momentaufnahmen in unterschiedlichen Zuständen der Code-Runtime  
*   Ein **Anwendungs** Panel zum Überprüfen, ändern und Debuggen von Web App-Manifesten, Servicemitarbeitern und Service Worker-Caches.  Sie können auch Speicher, Datenbanken und Caches über den **Anwendungs** Panel prüfen und verwalten.  
*   Ein **Sicherheits** Bereich, um Sicherheitsprobleme zu Debuggen und sicherzustellen, dass Sie HTTPS auf Ihrer Website richtig implementiert haben.  HTTPS bietet kritische Sicherheit und Datenintegrität sowohl für Ihre Website als auch für Ihre Benutzer, die persönliche Informationen auf Ihrer Website bereitstellen.  
*   Ein **Überwachungs** Panel \ (jetzt **Lighthouse**umbenannt), um eine Überprüfung Ihrer Website durchzuführen.  Die Ergebnisse der Prüfung helfen Ihnen, die Qualität Ihrer Website auf folgende Weise zu verbessern.  
    *   Häufig auftretende Fehler im Zusammenhang mit dem Erstellen einer barrierefreien, sicheren, leistungsfähigen Website usw.  
    *   Beheben Sie die einzelnen Fehler.  
    *   Erstellen Sie eine PWA.  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

Bitte senden Sie Ihre [Feedback-und Funktionswünsche](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Extensions  

Sie haben möglicherweise Erweiterungen des devtools verwendet, um Ihnen beim Erstellen von Websites oder apps beim Diagnostizieren und Debuggen von Problemen zu helfen.  Sie können Erweiterungen für Microsoft Edge über die [Microsoft Edge Addons][MicrosoftEdgeAddonsExtensions] -Seite erwerben.  Auf der [Microsoft Edge-Addons][MicrosoftEdgeAddonsExtensions] -Seite können Sie devtools-Erweiterungen aus der Kategorie **Entwicklertools** durchsuchen oder nach einer bestimmten Erweiterung suchen.  

Sie können auch Erweiterungen aus dem [Chrome Web Store][GoogleChromeWebstoreExtensions]hinzufügen.  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="Microsoft Edge (Chrom) devtools":::
   Chrome Web Store in Microsoft Edge  
:::image-end:::  

Wählen Sie oben im Dialogfeld, das angezeigt wird, die Option **Erweiterungen von anderen speichern zulassen aus** , und wählen Sie dann **zulassen** aus.  

> [!NOTE]
> Erweiterungen, die von anderen Quellen als dem Microsoft Store installiert wurden, werden nicht überprüft und können sich auf die Browserleistung auswirken.  

Wählen Sie **zu Chrome hinzufügen** aus, um Ihre devtools-Erweiterung zu Microsoft Edge hinzuzufügen!  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="Microsoft Edge (Chrom) devtools"  
