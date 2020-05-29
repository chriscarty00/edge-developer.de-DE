---
description: Der Vorgang zum Aktualisieren der Erweiterung auf dem Microsoft Store.
title: Aktualisieren eines Erweiterungs Eintrags
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 67b0eddfa7f8641a0db5a4f7b5693c876dd5e345
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607370"
---
# Aktualisieren eines Erweiterungs Eintrags  

Aktualisieren eines vorhandenen Eintrags im Microsoft Edge Addons-Katalog \ (Microsoft Edge Addons \).  Sie haben die Möglichkeit, eine veröffentlichte Erweiterung zu einem beliebigen Zeitpunkt zu ändern.  Während Sie die Aktualisierung durchführen, müssen Sie die gesamte Erweiterung nicht aktualisieren, um nur wenige Änderungen vorzunehmen, beispielsweise die Beschreibung oder das Logo zu aktualisieren.  Wenn Sie aber Ihr Erweiterungspaket aktualisieren, denken Sie daran, die Versionsnummer jedes Mal zu erhöhen.  

## Aktualisieren einer bereits veröffentlichten Erweiterung  

Führen Sie die folgenden Schritte aus, um Ihren Eintrag zu aktualisieren:  

1.  Wechseln Sie zu Ihrem [entwicklerdashboard][MicrosoftPartnerCenter].  Klicken Sie auf der Seite Übersicht auf den Eintrag, den Sie aktualisieren möchten.  Dadurch werden die Angaben zum Übermittlungsformular eingeblendet, die Sie während der Veröffentlichung ausgefüllt haben.  
1.  Nehmen Sie die gewünschten Änderungen an dem Paket, der Beschreibung, den Grafikobjekten oder anderen Einstellungen vor.  Wenn Sie die Paketdatei aktualisieren, stellen Sie sicher, dass die Version im Manifest höher als die vorherige Paketversion ist.
1.  Nachdem Sie die Änderungen vorgenommen haben, klicken Sie auf Speichern und dann auf veröffentlichen.
1.  Besuchen Sie das [Partner Center][MicrosoftPartnerCenter] -entwicklerdashboard, um zu sehen, in welchem Status Ihr Eintrag geändert wurde `In the store` `In the store.  Certification in progress` .  

> [!NOTE]
> Die Dauer des Update Veröffentlichungsprozesses reicht von einigen Stunden bis zu wenigen Tagen.  

Sobald die `Status` Spalte angezeigt wird `In the store` , ist Ihr Erweiterungs Update in Microsoft Edge-Addons verfügbar.  

## Aktualisieren einer Erweiterung während des Zertifizierungs Schritts  

Sie können Ihre Verlängerungs Übermittlung bearbeiten und aktualisieren, nachdem Sie sich vor der Eingabe des Veröffentlichungs Schritts eingereicht haben.  Sie können den Status Ihrer Durchwahl auf der Übersichtsseite der **Erweiterung** überprüfen, die Ihrem Eintrag im [Partner Center][MicrosoftPartnerCenter]zugeordnet ist.  

Führen Sie die folgenden Schritte aus, um ihre Übermittlung zu bearbeiten:  

1.  Wechseln Sie zu Ihrem [entwicklerdashboard][MicrosoftPartnerCenter].  Klicken Sie auf der Seite **Übersicht** auf den Eintrag, den Sie aktualisieren möchten.  Dadurch werden die Angaben zum Übermittlungsformular eingeblendet, die Sie während der Veröffentlichung ausgefüllt haben.  
1.  Wechseln Sie mit der linken Navigationsleiste wie in der Abbildung gezeigt zur **Übersicht über die Erweiterung** .  Abbrechen der aktuellen Übermittlung durch Klicken auf die Schaltfläche " **Übermittlung abbrechen** ".  
1.  Wechseln Sie zu anderer Abschnitt, und nehmen Sie die gewünschten Änderungen an dem Paket, der Beschreibung, den Grafikobjekten oder anderen Einstellungen vor.  Wenn Sie die Paketdatei aktualisieren, stellen Sie sicher, dass die Version im Manifest höher als die vorherige Paketversion ist.  
1.  Nachdem Sie die Änderungen vorgenommen haben, klicken Sie auf **Speichern** und dann auf **veröffentlichen**.  

> [!IMPORTANT]
> Dieser Vorgang beendet und entfernt ihre aktuelle Übermittlung aus unserer Zertifizierungspipeline, und eine neue Überprüfung beginnt mit der neuesten Übermittlung.  

> [!NOTE]
> Die Dauer des Update Veröffentlichungsprozesses reicht von einigen Stunden bis zu wenigen Tagen.  

Sobald die `Status` Spalte angezeigt wird `In the store` , ist Ihr Erweiterungs Update in Microsoft Edge-Addons verfügbar.  

## Entfernen der Erweiterung von Microsoft Edge-Addons  

Gehen Sie wie folgt vor, um Ihre Erweiterung von Microsoft Edge-Addons zu entfernen:  

1.  Wechseln Sie zu Ihrem [entwicklerdashboard][MicrosoftPartnerCenter].  Klicken Sie auf der Seite **Übersicht** auf den Eintrag, den Sie entfernen möchten.  
1.  Öffnen Sie die Seite mit der **Erweiterungs Übersicht** Ihres Eintrags.  
1.  Klicken Sie auf **Veröffentlichung**aufheben.  Dadurch wird der Eintrag von Microsoft Edge Addons nicht veröffentlicht.  

Mit diesen Schritten wird die Erweiterung von Microsoft Edge Addons entfernt, was bedeutet, dass neue Benutzer ihre Erweiterung nicht finden oder installieren können, aber Benutzer, die die Erweiterung bereits installiert haben, Sie möglicherweise weiterhin verwenden.  

<!-- image links -->  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
