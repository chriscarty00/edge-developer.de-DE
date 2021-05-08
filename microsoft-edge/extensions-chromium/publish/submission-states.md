---
description: Erfahren Sie mehr über die verschiedenen Zustände beim Übermitteln von Erweiterungen an den Store
title: Übermittlungszustände für Erweiterungen im Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 881166471ec5fabb66367ead650cb86b883cf01d
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343143"
---
# Übermittlungszustände für Erweiterungen im Microsoft Edge-Add-Ons-Speicher  

Auf der Übersichtsseite im Partner Center wird der Status Ihrer Erweiterung im gesamten Übermittlungsfluss angezeigt.  In diesem Artikel werden die verschiedenen Zustände beschrieben, in den sich Ihre Erweiterung während des Übermittlungs- und Zertifizierungsprozesses jederzeit ein- und ausdingen kann.  

| # |  Status |  Details |  
|:--- |:--- |:--- |  
| 1 |  Im Entwurf |  Sie erstellen Ihre Übermittlung und speichern einen Entwurf in Ihrem Konto.  Sie haben ihr Erweiterungspaket und Ihre Übermittlungsformulardetails nicht zum Veröffentlichen im Microsoft Edge-Add-Ons-Speicher übermittelt.  Ihre Erweiterung steht Benutzern in diesem Zustand nicht zur Verfügung.  |  
| 2|  In Review |  Sie haben Ihre Erweiterung übermittelt.  Ihr Erweiterungspaket und Ihre Übermittlungsformulardetails werden von Microsoft überprüft.  Ihre Erweiterung steht Benutzern in diesem Zustand nicht zur Verfügung.  |  
| 3|  Warten auf Veröffentlichung |  Ihre Übermittlung befindet sich nach Abschluss der Erweiterungsüberprüfung in diesem Zustand, und Ihre Erweiterung wird für die Veröffentlichung im Microsoft Store vorbereitet.  Dieser Zustand ist ein Zwischenzustand zwischen `In review` und `In the store` .  Dieser Status wird möglicherweise nicht für alle Übermittlungen angezeigt.  |  
| 4|  Im Laden |  Die Überprüfung ist nun abgeschlossen, und Ihre Erweiterung wird im Microsoft Edge-Add-Ons-Speicher veröffentlicht.  Ihre Erweiterung ist im Microsoft Store in den von Ihnen angegebenen Märkten verfügbar.  |  
| 5 |  Im Laden.  Update im Test |  Ihre Erweiterung wird im Microsoft Edge-Add-Ons-Store veröffentlicht, und Sie haben ein Update übermittelt, das von Microsoft überprüft wird.  |  
| 6 |  Überprüfung fehlgeschlagen |  Ihre Übermittlung befindet sich in diesem Zustand, wenn ihre Erweiterung eine Überprüfung nicht erfolgreich durchfing.  Eine fehlgeschlagene Überprüfung kann während der ersten Überprüfung oder während eines Updates auftreten.  Sie müssen Korrekturmaßnahmen ergreifen und Ihre Erweiterung erneut übermitteln.  |  
| 7 |  Im Store nicht verfügbar |  Es gibt drei mögliche Szenarien, wenn ihre Erweiterung diesen Status anzeigt: **** Unveröffentlicht aus dem Speicher, **Aus**dem Speicher entfernt und Blockiert . ****  Die Beschreibung der drei Zustände ist in 8, 9 und 10 angegeben.  |  
| 8 |  Unveröffentlicht aus dem Store |  Sie haben die Veröffentlichung Ihrer Erweiterung aus dem Microsoft Edge-Add-Ons-Speicher im Partner Center aufheben können.  Im Partner Center haben Sie **die Veröffentlichung auf der** Seite für die Erweiterungsübermittlung aufheben ausgewählt.  Nach dem Aufheben der Veröffentlichung Ihrer Erweiterung ist sie nicht mehr im Microsoft Edge-Add-Ons-Speicher verfügbar, damit neue Benutzer sie herunterladen können, aber vorhandene Benutzer verwenden möglicherweise weiterhin ihre Kopien Ihrer Erweiterung.  |  
| 9 |  Aus dem Speicher entfernt |  Wenn Ihre Erweiterung gegen die Geschäftsbedingungen des Microsoft Edge-Add-Ons-Speichers verstößt, entfernt Microsoft sie möglicherweise aus dem Edge-Add-Ons-Speicher, und der Status ändert sich in diesem Zustand.  <br />  Nach dem Entfernen Ihrer Erweiterung durch Microsoft steht Ihre Erweiterung nicht mehr im Microsoft Edge-Add-Ons-Store für neue Benutzer zum Herunterladen zur Verfügung, aber vorhandene Benutzer können weiterhin ihre Kopien Ihrer Erweiterung verwenden.  |  
| 10 |  Blockiert |  Wenn Ihre Erweiterung als schädlich festgestellt wird und die Sicherheit und den Datenschutz von Benutzern gefährdet, hat Microsoft das Recht, Ihre Erweiterung aus dem Edge-Add-Ons-Speicher zu blockieren, und der Status ändert sich in diesem Zustand.  Wenn Ihre Erweiterung blockiert ist, wird sie aus dem Edge-Add-Ons-Speicher und von allen Benutzergeräten entfernt.  |  
