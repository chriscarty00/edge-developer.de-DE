---
description: Das Aktualisieren oder Entfernen von Erweiterungen aus dem Microsoft Edge-Add-Ons-Speicher
title: Aktualisieren eines Erweiterungseintrags
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: 930d0f835e89451d09743a20ac4097c596ea5c30
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327484"
---
# Aktualisieren oder Entfernen der Erweiterung  

Sie können eine übermittelte Erweiterung aktualisieren oder einen veröffentlichten Erweiterungseintrag jederzeit aus dem Microsoft Edge-Add-Ons-Store entfernen.  

## Aktualisieren Ihrer Erweiterung im Microsoft Edge-Add-Ons-Store  

> [!NOTE]
> Die Dauer des Zertifizierungsprozesses für ein Update einer Erweiterung kann zwischen einigen Stunden und einigen Tagen dauern.  

### Aktualisieren einer vorhandenen Erweiterung im Microsoft Edge-Add-Ons-Store  

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung im Store zu aktualisieren.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie die Erweiterung aus, die Sie aktualisieren möchten.  
1.  Aktualisieren Sie entweder das Erweiterungspaket oder die Metadaten der Erweiterung.  Wenn Sie das Erweiterungspaket aktualisieren, stellen Sie sicher, dass Sie die Version in der Manifestdatei erhöhen.  
1.  Nachdem Sie die Änderungen vorgenommen haben, **wählen**Sie "Veröffentlichen speichern" aus, um ihren Erweiterungseintrag zu  >  **** aktualisieren, und starten Sie den Zertifizierungsprozess.  
1.  Nachdem die Spalte angezeigt wurde, ist Ihr Erweiterungsupdate `Status` `In the store` im Microsoft Edge-Add-Ons-Store verfügbar.  
    
### Aktualisieren Der Erweiterung während des Zertifizierungsschritts  

Während sich Ihre Erweiterung noch in der Zertifizierungsphase befindet und bevor sie im Microsoft Edge-Add-Ons-Store veröffentlicht wird, können Sie sie aktualisieren. Wenn die Erweiterung den Zertifizierungsprozess nicht erfolgreich ist, müssen Sie die Erweiterung möglicherweise auch aktualisieren.    

Um den Status Ihrer Erweiterung zu überprüfen, navigieren Sie zu dem Dashboard, das Ihrem Eintrag im [Partner Center zugeordnet ist.][MicrosoftPartnerCenter]  

Führen Sie die folgenden Schritte aus, um Ihre Übermittlung zu bearbeiten.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie die Erweiterung aus, die Sie aktualisieren möchten.  Die Informationen, die Sie während der vorherigen Übermittlung ausgefüllt haben, werden angezeigt.  
1.  Verwenden Sie **die** linke Navigationsleiste, um den Abschnitt "Erweiterungsübersicht" zu öffnen.  Wenn Sie die aktuelle Übermittlung abbrechen möchten, wählen Sie **"Übermittlung abbrechen" aus.**  
1.  Wechseln Sie zu anderen Abschnitten, und aktualisieren Sie entweder das Erweiterungspaket oder die Metadaten der Erweiterung.  Wenn Sie das Erweiterungspaket aktualisieren, stellen Sie sicher, dass Sie die Version in der Manifestdatei so erhöhen, dass sie den Änderungen seit der vorherigen Paketversion entsprechen.  
1.  Nachdem Sie Änderungen vorgenommen haben, wählen Sie **"Veröffentlichen**  >  **speichern" aus.**  
    
> [!IMPORTANT]
> Der Prozess wird beendet und entfernt Ihre aktuelle Übermittlung aus der Zertifizierungspipeline für Microsoft Edge-Erweiterungen, und eine neue Überprüfung beginnt mit der neuesten Übermittlung.  

### Aktualisieren Der Erweiterung, nachdem die Zertifizierung fehlgeschlagen ist  

Nachdem der Zertifizierungsprozess der Erweiterung fehlgeschlagen ist, müssen Sie die Erweiterung aktualisieren und die Erweiterung erneut übermitteln, die das Feedback enthält.  

Führen Sie zum Bearbeiten der Erweiterung die folgenden Schritte aus.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie die Erweiterung aus, bei der der Zertifizierungsprozess fehlgeschlagen ist.  
1.  Aktualisieren Sie entweder das Erweiterungspaket oder die Metadaten, die das Feedback aus dem Zertifizierungsprozess enthalten.  Wenn Sie das Erweiterungspaket aktualisieren, stellen Sie sicher, dass Sie die Version in der Manifestdatei erhöhen.  
1.  Nachdem Sie Änderungen vorgenommen haben, wählen Sie **"Veröffentlichen**  >  **speichern" aus.**  
    
## Entfernen von Erweiterungen aus dem Microsoft Edge-Add-Ons-Speicher  

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung aus dem Microsoft Edge-Add-Ons-Speicher zu entfernen.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard.][MicrosoftPartnerCenter]  Wählen Sie auf der Dashboardseite den zu entfernende Eintrag aus.  
1.  Choose **Extension Overview** on your listing.  
1.  Wählen **Sie "Aufheben der Veröffentlichung"** aus, um den Eintrag aus dem Microsoft Edge-Add-Ons-Store zu entfernen.  
    
Ihre Erweiterung wurde nun aus dem Microsoft Edge-Add-Ons-Store entfernt.  Benutzer, die Ihre Erweiterung bereits installiert haben, verwenden sie möglicherweise weiterhin, aber neue Benutzer finden sie nicht.  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
