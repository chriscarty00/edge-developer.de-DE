---
description: Erfahren Sie mehr über die verschiedenen Zustände beim Übermitteln von Erweiterungen an den Store.
title: Übermittlungszustände für Erweiterungen im Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 881166471ec5fabb66367ead650cb86b883cf01d
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343143"
---
# Übermittlungszustände für Erweiterungen im Microsoft Edge-Add-Ons-Store  

Auf der Übersichtsseite im Partner Center wird der Status Ihrer Erweiterung im gesamten Übermittlungsfluss angezeigt.  In diesem Artikel werden die verschiedenen Zustände beschrieben, in den sich Ihre Erweiterung während des Übermittlungs- und Zertifizierungsprozesses jederzeit ein-/ausdingen kann.  

| # |  Status |  Details |  
|:--- |:--- |:--- |  
| 1 |  Im Entwurf |  Sie erstellen Ihre Übermittlung und speichern einen Entwurf in Ihrem Konto.  Sie haben ihr Erweiterungspaket und Ihre Übermittlungsformulardetails nicht übermittelt, um sie im Microsoft Edge-Add-Ons-Store zu veröffentlichen.  Die Erweiterung ist für Benutzer in diesem Status nicht verfügbar.  |  
| 2|  In Überprüfung |  Sie haben Ihre Erweiterung übermittelt.  Die Details ihres Erweiterungspakets und Ihres Übermittlungsformulars werden von Microsoft überprüft.  Die Erweiterung ist für Benutzer in diesem Status nicht verfügbar.  |  
| 3|  Warten auf Veröffentlichung |  Ihre Übermittlung befindet sich in diesem Zustand, nachdem Die Erweiterungsüberprüfung abgeschlossen ist und Ihre Erweiterung für die Veröffentlichung im Microsoft Store vorbereitet wird.  Dieser Zustand ist ein Zwischenzustand zwischen `In review` und `In the store` .  Dieser Status wird möglicherweise nicht für alle Übermittlungen angezeigt.  |  
| 4|  Im Laden |  Die Überprüfung ist nun abgeschlossen, und Ihre Erweiterung wird im Microsoft Edge-Add-Ons-Store veröffentlicht.  Ihre Erweiterung ist im Microsoft Store in den von Ihnen angegebenen Märkten verfügbar.  |  
| 5 |  Im Laden.  Update in Überprüfung |  Ihre Erweiterung wird im Microsoft Edge-Add-Ons-Store veröffentlicht, und Sie haben ein Update übermittelt, das von Microsoft überprüft wird.  |  
| 6 |  Überprüfung fehlgeschlagen |  Ihre Übermittlung befindet sich in diesem Zustand, wenn ihre Erweiterung eine Überprüfung nicht besteht.  Eine fehlgeschlagene Überprüfung kann während der ersten Überprüfung oder während eines Updates auftreten.  Sie müssen Korrekturmaßnahmen ergreifen und Ihre Erweiterung erneut übermitteln.  |  
| 7 |  Nicht verfügbar im Speicher |  Es gibt drei mögliche Szenarien, in denen die Erweiterung **** diesen Status anzeigt: **"Aus**Speicher entfernt" und **"Blockiert"** aufgehoben.  Die Beschreibung der drei Zustände wird in 8, 9 und 10 angegeben.  |  
| 8 |  Unpublished from store |  Sie haben die Veröffentlichung Ihrer Erweiterung aus dem Microsoft Edge-Add-Ons-Store im Partner Center aufheben können.  Im Partner Center haben Sie die **Veröffentlichung** auf der Seite für die Erweiterungsübermittlung aufheben.  Nach dem Aufheben der Veröffentlichung ihrer Erweiterung ist sie nicht mehr im Microsoft Edge-Add-Ons-Store für neue Benutzer zum Herunterladen verfügbar, vorhandene Benutzer können jedoch weiterhin ihre Kopien Ihrer Erweiterung verwenden.  |  
| 9 |  Aus dem Speicher entfernt |  Wenn festgestellt wird, dass Ihre Erweiterung gegen die Geschäftsbedingungen des Microsoft Edge-Add-Ons-Store verstößt, entfernt Microsoft sie möglicherweise aus dem Edge-Add-Ons-Store, und der Status ändert sich in diesen Zustand.  <br />  Nachdem Sie Ihre Erweiterung von Microsoft entfernt haben, steht Ihre Erweiterung nicht mehr im Microsoft Edge-Add-Ons-Store für neue Benutzer zum Herunterladen zur Verfügung, vorhandene Benutzer verwenden jedoch möglicherweise weiterhin ihre Kopien Ihrer Erweiterung.  |  
| 10 |  Blockiert |  Wenn Festgestellt wird, dass Ihre Erweiterung bösartig ist und die Sicherheit und den Datenschutz von Benutzern beeinträchtigt, hat Microsoft das Recht, Ihre Erweiterung aus dem Edge-Add-Ons-Store zu blockieren, und der Status ändert sich in diesen Zustand.  Wenn Ihre Erweiterung blockiert ist, wird sie aus dem Edge-Add-Ons-Speicher und von allen Benutzergeräten entfernt.  |  
