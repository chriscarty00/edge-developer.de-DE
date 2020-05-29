---
description: Prozess zum Portieren der Chrome-Erweiterung an Microsoft Edge.
title: Port Chrome-Erweiterung an Microsoft (Chrom) Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 794e8806a95ce0a70069c65c306c30131b01e24d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567513"
---
# Port Chrome-Erweiterung zu Microsoft \ (Chrom \) Edge  

Der Vorgang zum Portieren einer Chrome-Erweiterung zu Microsoft Edge ist sehr einfach.  Die für Chrom geschriebenen Erweiterungen werden in den meisten Fällen auf Microsoft Edge mit minimalen Änderungen ausgeführt.  Die von Chrome unterstützten Erweiterungs-APIs und manifestschlüssel sind mit Microsoft Edge Code kompatibel.  Microsoft Edge unterstützt jedoch nicht die folgenden Erweiterungs-APIs:  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> Der Benutzer muss bei Microsoft Edge mit einem MSA-oder Aad-Konto angemeldet sein, um die API verwenden zu können `chrome.identity.getProfileUserInfo` .  Wenn der Benutzer bei Microsoft Edge unter Verwendung einer **lokalen Anzeige**angemeldet ist, gibt die API die `null` e-Mail-und ID-Werte zurück.  

> [!IMPORTANT]
> **Zahlungen**: Microsoft Edge unterstützt nicht direkt eine Erweiterung, die [Chrome Web Store-Zahlungen][ChromeDeveloperWebStorePayments] verwendet, da die Anforderung zum `identity.getAuthtoken` Abrufen des Tokens für Benutzer mit Anmeldedaten zum Senden der auf der Grundlage der Ruhe basierten Lizenzierungs-API-Anforderung verwendet werden muss.  Microsoft Edge unterstützt die `getAuthtoken` Anforderung nicht, sodass dieser Fluss nicht funktioniert.  

Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu portieren:  

1.  Überprüfen Sie die in ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs.  Wenn Sie Features oder APIs verwenden, die von Microsoft Edge nicht unterstützt werden, können Sie Ihre Erweiterung möglicherweise nicht portieren.  
    
    > [!NOTE]
    > Die `getAuthToken` API funktioniert nicht mit Microsoft Edge, jedoch können Sie `launchWebAuthFlow` zum Abrufen eines OAuth2-Tokens verwenden, um Benutzer zu authentifizieren.  
    
1.  Wenn Sie `Chrome` den Namen oder die Beschreibung ihrer Durchwahl verwenden, geben Sie die Erweiterung für neu ein `Microsoft Edge` .  Sie müssen den Zertifizierungsprozess bestehen.  
    
1.  Testen Sie Ihre Erweiterung, um zu überprüfen, ob Sie in Microsoft Edge funktioniert.  Der erste Schritt besteht darin, sicherzustellen, dass die Erweiterungsentwickler Features aktiviert sind.  Dadurch können Sie Erweiterungsdateien in Microsoft Edge laden, damit Sie Ihre Erweiterung während der Entwicklung testen können.  
    
1.  Wenn Sie Probleme haben, Debuggen Sie Ihre Erweiterungen in Microsoft Edge mithilfe des devtools, oder [kontaktieren Sie uns][mailtoExtensionPartnerOpsMicrosoft].  
    
1.  Nun wird Ihre Erweiterung endlich aufpoliert und kann verpackt werden.  Wenn Sie sich auf die Übermittlung an den Microsoft Edge Addons-Katalog vorbereiten möchten \ (Microsoft Edge Addons \), müssen Sie Ihre Erweiterung nicht verpacken.  Befolgen Sie außerdem unsere [Veröffentlichungsrichtlinien][ExtensionsPublishExtension] , um Ihre Erweiterung auf Microsoft Edge-Addons zu veröffentlichen.  
    
    > [!NOTE]
    > Wenn Ihre Erweiterung Nachrichten mit einer systemeigenen Anwendung unter Verwendung der API austauscht `chrome.runtime.connectNative` , stellen Sie sicher, dass Sie `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` in der Manifestdatei des systemeigenen Messaging-Hosts auf "" festzulegen.  Dadurch kann die APP die Erweiterung identifizieren.  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Veröffentlichen einer Erweiterung"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Einmalige Zahlungen – Google Chrome"  
