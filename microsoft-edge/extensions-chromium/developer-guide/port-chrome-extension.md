---
description: Portieren der Chrome-Erweiterung zu Microsoft Edge
title: Portierung der Chrome-Erweiterung zu Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 6be7d788ac22232475e278ae9a5b04de9b6e17f7
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343136"
---
# Portierung der Erweiterung  

Mit Microsoft Edge können Sie Ihre Chrome-Erweiterung mit minimalen Änderungen portierung.  Die von Chrome unterstützten Erweiterungs-APIs und Manifestschlüssel sind codekompatibel mit Microsoft Edge.  Eine Liste der von Microsoft Edge unterstützten APIs finden Sie unter [API-Unterstützung.][ExtensionApiSupport]  

Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu porten.  

1.  Überprüfen Sie die in Ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs mit der Liste der von Microsoft Edge-Erweiterungen [unterstützten APIs.][ExtensionApiSupport]  
    
    > [!NOTE]
    > Wenn Ihre Erweiterung APIs verwendet, die von Microsoft Edge nicht unterstützt werden, wird sie möglicherweise nicht direkt portierung.  
    
1.  Legen Sie in der Manifestdatei das Feld `update_URL` auf `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  Der Wert verweist auf die Datei Ihrer Erweiterung im `.crx` Microsoft Edge-Add-Ons-Store und ermöglicht Es Microsoft Edge, nach Erweiterungsupdates zu suchen.  
1.  Wenn die Erweiterung entweder im Namen oder in der Beschreibung ihrer Erweiterung verwendet wird, müssen Sie die Erweiterung `Chrome` mit einer neuen Bezeichnung `Microsoft Edge` benennen.  Zum Bestehen des Zertifizierungsprozesses sind die Änderungen erforderlich.  
1.  Testen Sie Ihre Erweiterung, um zu überprüfen, ob sie in Microsoft Edge funktioniert, indem [Sie Ihre Erweiterung querladen.][ExtensionsGettingStartedExtensionSideloading]  
1.  Wenn Probleme auftreten, können Sie Ihre Erweiterungen in Microsoft Edge mithilfe der DevTools debuggen oder [uns kontaktieren.][mailtoExtensionMicrosoft]  
1.  Befolgen Sie [die Veröffentlichungsrichtlinien,][ExtensionsPublishPublishExtension] um Ihre Erweiterung im Microsoft Edge-Add-Ons-Store zu veröffentlichen.  
    
    > [!NOTE]
    > Wenn Ihre Erweiterung Nachrichten mit einer systemeigenen App austauscht, stellen Sie sicher, dass Sie dies in Der manifestdatei des systemeigenen `chrome.runtime.connectNative` `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` Messaginghosts festlegen.  Mit dieser Einstellung kann die App Ihre Erweiterung identifizieren.  
    
## Nächste Schritte  

Nachdem Ihr Erweiterungspaket bereit für die Veröffentlichung im Microsoft Edge-Add-Ons-Store [ist,][ExtensionsPublishCreateDevAccount] erstellen Sie ein Entwicklerkonto, und [veröffentlichen Sie Ihre Erweiterung.][ExtensionsPublishPublishExtension]  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "API-Support-| Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Querladen der Erweiterungs-| Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Entwicklerregistrierungs-| Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Veröffentlichen Der Erweiterungs-| Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Einmalzahlung | Chrome Developer"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
