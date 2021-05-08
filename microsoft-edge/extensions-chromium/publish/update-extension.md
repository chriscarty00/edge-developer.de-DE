---
description: Aktualisieren oder Entfernen von Erweiterungen aus dem Microsoft Edge-Add-Ons-Speicher
title: Aktualisieren eines Erweiterungseintrags
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: 692c534ac0586d53002e4a032197e22ae24e2863
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343166"
---
# Aktualisieren oder Entfernen der Erweiterung  

Sie können eine übermittelte Erweiterung aktualisieren oder einen veröffentlichten Erweiterungseintrag jederzeit aus dem Microsoft Edge-Add-Ons-Speicher entfernen.  

## Aktualisieren Ihrer Erweiterung im Microsoft Edge-Add-Ons-Speicher  

> [!NOTE]
> Die Dauer des Zertifizierungsprozesses für ein Update einer Erweiterung kann einige Stunden bis einige Tage dauern.  

### Aktualisieren einer vorhandenen Erweiterung im Microsoft Edge-Add-Ons-Speicher  

Führen Sie die folgenden Schritte aus, um Die Erweiterung im Store zu aktualisieren.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie die Erweiterung aus, die Sie aktualisieren möchten.  
1.  Aktualisieren Sie entweder das Erweiterungspaket oder die Metadaten der Erweiterung.  Wenn Sie das Erweiterungspaket aktualisieren, stellen Sie sicher, dass Sie die Version in der Manifestdatei erhöhen.  
1.  Nachdem Sie die Änderungen vorgenommen haben, wählen Sie **Veröffentlichen**speichern aus,  >  **** um Den Erweiterungseintrag zu aktualisieren, und starten Sie den Zertifizierungsprozess.  
1.  Nachdem die `Status` Spalte angezeigt `In the store` wurde, ist Ihr Erweiterungsupdate im Microsoft Edge-Add-Ons-Speicher verfügbar.  
    
### Aktualisieren Der Erweiterung während des Zertifizierungsschritts  

Während sich Ihre Erweiterung noch in der Zertifizierungsphase befindet und bevor sie im Microsoft Edge-Add-Ons-Speicher veröffentlicht wird, können Sie sie aktualisieren. Wenn bei der Erweiterung der Zertifizierungsprozess fehlschlägt, müssen Sie möglicherweise auch Ihre Erweiterung aktualisieren.    

Navigieren Sie zum Dashboard, das Ihrem Eintrag im Partner Center zugeordnet ist, um den Status Ihrer Erweiterung [zu überprüfen.][MicrosoftPartnerCenter]  

Führen Sie die folgenden Schritte aus, um Ihre Übermittlung zu bearbeiten.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie die Erweiterung aus, die Sie aktualisieren möchten.  Die Informationen, die Sie während der vorherigen Übermittlung ausgefüllt haben, werden angezeigt.  
1.  Verwenden Sie **die** linke Navigationsleiste, um den Abschnitt Erweiterungsübersicht zu öffnen.  Wenn Sie die aktuelle Übermittlung abbrechen möchten, wählen Sie **Übermittlung abbrechen aus.**  
1.  Wechseln Sie zu anderen Abschnitten, und aktualisieren Sie entweder das Erweiterungspaket oder die Metadaten der Erweiterung.  Wenn Sie das Erweiterungspaket aktualisieren, stellen Sie sicher, dass Sie die Version in der Manifestdatei erhöhen, um änderungen seit der vorherigen Paketversion zu entsprechen.  
1.  Nachdem Sie Änderungen vorgenommen haben, wählen Sie **Veröffentlichen**  >  **speichern aus.**  
    
> [!IMPORTANT]
> Der Prozess beendet und entfernt Ihre aktuelle Übermittlung aus der Zertifizierungspipeline für Microsoft Edge-Erweiterungen, und eine neue Überprüfung beginnt mit der neuesten Übermittlung.  

### Aktualisieren Der Erweiterung nach einem Fehler bei der Zertifizierung  

Nachdem der Zertifizierungsprozess für Ihre Erweiterung fehlgeschlagen ist, müssen Sie Ihre Erweiterung aktualisieren und Ihre Erweiterung erneut übermitteln, die das Feedback enthält.  

Führen Sie die folgenden Schritte aus, um die Erweiterung zu bearbeiten.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard,][MicrosoftPartnerCenter] und wählen Sie die Erweiterung aus, bei der der Zertifizierungsprozess fehlgeschlagen ist.  
1.  Aktualisieren Sie entweder das Erweiterungspaket oder die Metadaten, die das feedback enthalten, das vom Zertifizierungsprozess empfangen wurde.  Wenn Sie das Erweiterungspaket aktualisieren, stellen Sie sicher, dass Sie die Version in der Manifestdatei erhöhen.  
1.  Nachdem Sie Änderungen vorgenommen haben, wählen Sie **Veröffentlichen**  >  **speichern aus.**  
    
## Entfernen von Erweiterungen aus dem Microsoft Edge-Add-Ons-Speicher  

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung aus dem Microsoft Edge-Add-Ons-Speicher zu entfernen.  

1.  Navigieren Sie zu Ihrem [Entwicklerdashboard][MicrosoftPartnerCenter].  Wählen Sie auf der Seite Dashboard den zu entfernende Eintrag aus.  
1.  Wählen **Sie Erweiterungsübersicht** in Ihrem Eintrag aus.  
1.  Wählen **Sie Unpublish** aus, um den Eintrag aus dem Microsoft Edge-Add-Ons-Speicher zu entfernen.  
    
Ihre Erweiterung wird nun aus dem Microsoft Edge-Add-Ons-Speicher entfernt.  Benutzer, die Ihre Erweiterung bereits installiert haben, können sie weiterhin verwenden, neue Benutzer finden sie jedoch nicht.  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
