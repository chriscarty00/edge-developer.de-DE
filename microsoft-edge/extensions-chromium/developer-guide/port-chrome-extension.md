---
description: Portierung der Chrome-Erweiterung zu Microsoft Edge
title: Port chrome extension To Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 6be7d788ac22232475e278ae9a5b04de9b6e17f7
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343136"
---
# Portierung Der Erweiterung  

Microsoft Edge können Sie Ihre Chrome-Erweiterung mit minimalen Änderungen porten.  Die von Chrome unterstützten Erweiterungs-APIs und Manifestschlüssel sind codekompatibel mit Microsoft Edge.  Eine Liste der apIs, die von Microsoft Edge unterstützt werden, finden Sie unter [API-Unterstützung][ExtensionApiSupport].  

Führen Sie die folgenden Schritte aus, um Ihre Chrome-Erweiterung zu portierung.  

1.  Überprüfen Sie die in Ihren Erweiterungen verwendeten Chrome-Erweiterungs-APIs mit der Liste Microsoft Edge [unterstützten APIs][ExtensionApiSupport] für Erweiterungen.  
    
    > [!NOTE]
    > Wenn Ihre Erweiterung APIs verwendet, die nicht von der Microsoft Edge werden, wird sie möglicherweise nicht direkt Portierung.  
    
1.  Legen Sie in der Manifestdatei das `update_URL` Feld auf . `https://edge.microsoft.com/extensionwebstorebase/v1/crx`  Der Wert verweist auf die Datei Ihrer Erweiterung im Microsoft Edge Add-Ons-Speicher und ermöglicht Microsoft Edge, nach `.crx` Erweiterungsupdates zu suchen.  
1.  Wenn sie entweder im Namen oder in der Beschreibung Ihrer Erweiterung verwendet `Chrome` wird, benennen Sie Ihre Erweiterung mit `Microsoft Edge` neu.  Zum Bestehen des Zertifizierungsprozesses sind die Änderungen erforderlich.  
1.  Testen Sie Ihre Erweiterung, um zu überprüfen, ob sie in Microsoft Edge durch [Querladen der Erweiterung funktioniert.][ExtensionsGettingStartedExtensionSideloading]  
1.  Wenn Probleme auftreten, können Sie Ihre Erweiterungen in Microsoft Edge DevTools debuggen oder [uns kontaktieren.][mailtoExtensionMicrosoft]  
1.  Befolgen Sie [die Veröffentlichungsrichtlinien,][ExtensionsPublishPublishExtension] um Ihre Erweiterung im Microsoft Edge zu veröffentlichen.  
    
    > [!NOTE]
    > Wenn Ihre Erweiterung Nachrichten mit einer systemeigenen App mit austauscht, stellen Sie sicher, dass Sie in Ihrer nativen `chrome.runtime.connectNative` `allowed_origins` Messaginghostmanifestdatei `extension://[Microsoft-Catalog-extensionID]` festlegen.  Die Einstellung ermöglicht es der App, Ihre Erweiterung zu identifizieren.  
    
## Nächste Schritte  

Nachdem Das Erweiterungspaket im Microsoft Edge veröffentlicht werden [kann,][ExtensionsPublishCreateDevAccount] erstellen Sie ein Entwicklerkonto, und veröffentlichen Sie [Ihre Erweiterung.][ExtensionsPublishPublishExtension]  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "API-Support | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Querladen Der Erweiterungs-| Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Entwicklerregistrierungs-| Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Veröffentlichen Der Erweiterungs-| Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "One-Time Payments | Chrome Developer"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
