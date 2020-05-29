---
description: Der Prozess der Verteilung der Erweiterung um einen anderen Mechanismus als überprüfte Speicher
title: Alternative Methode zur Verteilung der Erweiterung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: a1a3ffe7a54f96df7e665ab5dc6f5b99bacb8b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567518"
---
# Alternative Methode zur Verteilung der Erweiterung  

Wenn Sie ein Entwickler sind, der eine Erweiterung als Teil des Installationsvorgangs für andere Software oder einen Netzwerkadministrator verteilen möchte, der eine Erweiterung in der gesamten Organisation verteilen möchte, unterstützt Microsoft Edge die folgenden Erweiterungs Installationsmethoden:  

*   **Verwenden der Windows-Registrierung \ (nur Windows \)**  

Microsoft Edge unterstützt die Installation einer Erweiterung, die auf einer `update_URL` .  Unter Windows muss der `update_URL` Verweis auf den Microsoft Edge Addons-Katalog (Microsoft Edge Addons \) verweisen, in dem die Erweiterung gehostet werden muss.  

> [!NOTE]
> Externe Installation der Erweiterung über eine JSON-Einstellungen-Datei für macOS <!--and Linux--> werden noch nicht unterstützt.  Dieser Funktions Support steht in Kürze zur Verfügung.

## Verwenden der Windows-Registrierung  

Veröffentlichen Sie zunächst die Erweiterung in den Microsoft Edge-Addons, oder Verpacken Sie eine. Wagon-Datei, und stellen Sie sicher, dass Sie erfolgreich installiert wird.  

Die Schritte zum Installieren der Erweiterung über die Registrierung in Windows sind:  

*   Suchen oder erstellen Sie den folgenden Schlüssel in der Registrierung:  
    *   32-Bit-Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   64-Bit-Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   Erstellen Sie einen neuen Schlüssel \ (Ordner \) unter dem Erweiterungs Schlüssel mit dem gleichen Namen wie die ID der Erweiterung \ (beispielsweise `aaaaaaaaaabbbbbbbbbbcccccccccc` \).  
*   Erstellen Sie in Ihrem Erweiterungs Schlüssel eine Eigenschaft, `update_url` und legen Sie Sie auf den Wert: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (dieser verweist auf den Namen ihrer Erweiterung in Microsoft Edge-Addons). Wenn Sie eine Erweiterung aus dem Chrome Web Store installieren möchten, geben Sie die URL des Chrome Web Store-Updates an `https://clients2.google.com/service/update2/crx` .  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   Starten Sie den Browser, und wechseln `edge://extensions` Sie zu; die Erweiterung wird angezeigt.  

## Aktualisieren und deinstallieren  

Microsoft Edge scannt die Metadaten-Einträge in der Registrierung jedes Mal, wenn der Browser gestartet wird, und nimmt alle erforderlichen Änderungen an den installierten externen Erweiterungen vor.  

Wenn Sie Ihre Erweiterung auf eine neue Version aktualisieren möchten, aktualisieren Sie die Datei, und aktualisieren Sie dann die Version in der Registrierung.  

Wenn Sie Ihre Erweiterung deinstallieren möchten (beispielsweise wenn Ihre Software deinstalliert wird), entfernen Sie Ihre Einstellungsdatei \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) oder die Metadaten aus der Registrierung.  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/apps/external_extensions).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
