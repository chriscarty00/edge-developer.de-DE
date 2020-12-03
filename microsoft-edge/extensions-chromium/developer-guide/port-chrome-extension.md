---
description: Prozess zum Portieren der Chrome-Erweiterung an Microsoft Edge.
title: Port Chrome-Erweiterung zu Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195159"
---
# Portieren der Erweiterung  

Mit Microsoft Edge können Sie Ihre Chrome-Erweiterung mit minimalen Änderungen portieren.  Die von Chrome unterstützten Erweiterungs-APIs und manifestschlüssel sind mit Microsoft Edge Code kompatibel.  Wenn Sie eine Liste der von Microsoft Edge unterstützten APIs finden möchten, navigieren Sie zu [API-Support][ExtensionApiSupport].  

Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu portieren.  

1.  Überprüfen Sie die in ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs mit der Liste der [unterstützten APIs][ExtensionApiSupport] für Microsoft-Edge-Erweiterungen.  
    
    > [!NOTE]
    > Wenn Ihre Erweiterung APIs verwendet, die von Microsoft Edge nicht unterstützt werden, kann Sie nicht direkt portiert werden.  
    
1.  Wenn der Name `Chrome` entweder im Namen oder in der Beschreibung der Erweiterung verwendet wird, geben Sie die Erweiterung für neu ein `Microsoft Edge` .  Dieser Schritt ist erforderlich, um den Zertifizierungsprozess durchlaufen zu lassen.  
1.  Testen Sie Ihre Erweiterung, um zu überprüfen, ob Sie in Microsoft Edge funktioniert, indem Sie [Ihre Erweiterung Sideloading][ExtensionsGettingStartedExtensionSideloading].  
1.  Wenn Sie Probleme haben, können Sie Ihre Erweiterungen in Microsoft Edge mithilfe des devtools Debuggen oder [sich mit uns in Verbindung setzen][mailtoExtensionMicrosoft].  
1.  Befolgen Sie die [Veröffentlichungsrichtlinien][ExtensionsPublishPublishExtension] , um Ihre Erweiterung im Microsoft Edge-Add-on-Store zu veröffentlichen.  
    
    > [!NOTE]
    > Wenn die Erweiterung Nachrichten mit einer systemeigenen App mit API austauscht `chrome.runtime.connectNative` , stellen Sie sicher, dass Sie `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` in der Manifestdatei des systemeigenen Messaging-Hosts auf festzulegen.  Dadurch kann die APP die Erweiterung identifizieren.  
    
## Nächste Schritte  

Sobald das Erweiterungspaket im Microsoft Edge-Add-ons-Store veröffentlicht werden kann, [Erstellen Sie ein Entwicklerkonto][ExtensionsPublishCreateDevAccount] , und [veröffentlichen Sie Ihre Erweiterung][ExtensionsPublishPublishExtension].  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "API-Unterstützung | Microsoft docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Querladen-Erweiterung | Microsoft docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Entwickler Registrierung | Microsoft docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Veröffentlichen Ihrer Erweiterung | Microsoft docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Einmalige Zahlungen | Chrome-Entwickler"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
