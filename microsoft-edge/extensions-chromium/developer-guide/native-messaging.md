---
description: Unterschiede im nativen Messaging aus der Chrome-Dokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/31/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 0fe45ea681c54ddea7b27a8d954022b8bda45770
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10567514"
---
# Systemeigenes Messaging  

Microsoft Edge ermöglicht jetzt die Erweiterung, die über den Microsoft Edge Addons-Katalog \ (Microsoft Edge Addons \) installiert wurde, um Nachrichten mit einer systemeigenen Anwendung mithilfe von Nachrichtenübergabe-APIs auszutauschen.  Wenn Sie das Feature aktivieren möchten, müssen Sie beim Implementieren des systemeigenen Messaginghosts ihrer systemeigenen Anwendung sicherstellen, dass Sie die folgenden Schritte ausführen.  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  **Systemeigener Messaging-Host**:  
    
    Um einen systemeigenen Messaging-Host zu registrieren, muss die Anwendung eine Manifestdatei installieren, die die systemeigene Messaginghost Konfiguration definiert.  Nachfolgend finden Sie ein Beispiel für die Manifestdatei:  
    
    ```xml
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
    ```  
    
Die systemeigene Messaging-Host Manifestdatei muss ein gültiges JSON-Dokument sein und die folgenden Felder enthalten:  

| Name | Beschreibung |  
|:--- |:--- |  
| `name` | Der Name des systemeigenen Messaginghosts. Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .  Dieser Name darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.  Der Name darf nicht mit einem Punkt beginnen oder enden, und auf einen Punkt darf kein anderer Punkt folgen. |  
| `description` | Kurze Anwendungsbeschreibung. |  
| `path` | Der Pfad zur nativen Messaging-Host-Binärdatei.  Unter Windows kann der Pfad relativ zu dem Verzeichnis sein, in dem sich die Manifestdatei befindet.  Unter macOS muss der Pfad absolut sein.  Der Hostprozess wird gestartet, wobei das aktuelle Verzeichnis auf das Verzeichnis festgesetzt ist, das die Host-Binärdatei enthält. Wenn dieser Parameter beispielsweise auf gesetzt ist `C:\Application\nm_host.exe` , wird die Binärdatei mit dem aktuellen Verzeichnis gestartet `C:\Application\` . |  
| `type` | Der Typ der Schnittstelle, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.  Derzeit gibt es nur einen möglichen Wert für diesen Parameter: `stdio` .  Dieser Wert gibt an, dass Chrome verwenden `stdin` und `stdout` mit dem Host kommunizieren soll. |  
| `allowed_origins` |  Liste der Erweiterung, die auf den systemeigenen Messaging-Host zugreifen soll  Damit Ihre systemeigene Anwendung die Microsoft Edge Addons-Erweiterung identifizieren und kommunizieren kann, legen Sie Sie `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` in ihrer systemeigenen Messaging-Host Manifestdatei auf fest. |  

1.  **Systemeigener Messaging-Hostspeicherort**  
    
    Der Speicherort der Manifestdatei hängt von der Plattform ab.  
    
    Unter Windows kann sich die Manifestdatei an einer beliebigen Stelle im Dateisystem befinden.  Das Anwendungs Installationsprogramm muss Registrierungsschlüssel erstellen  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    oder  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`,  
    
    und legen Sie den Standardwert für diesen Schlüssel auf den vollständigen Pfad zur Manifestdatei fest.  Verwenden Sie beispielsweise den folgenden Befehl:  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    oder verwenden Sie die folgende REG-Datei:  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    Wenn Microsoft Edge nach systemeigenen Messaginghosts sucht, wird zuerst die 32-Bit-Registrierung abgefragt, dann die 64-Bit-Registrierung.  

Unter macOS werden die systemweiten systemeigenen Messaginghosts an einem festen Speicherort nachgeschlagen, während die nativen Messaginghosts auf Benutzerebene in einem Unterverzeichnis im Benutzerprofilverzeichnis nachgeschlagen werden `NativeMessagingHosts` .  

Microsoft Edge unter macOS \ (systemweit \):  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

Microsoft Edge unter macOS \ (benutzerspezifischer Standardpfad \):  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` kann Canary, dev oder Beta sein. Für stable-Kanal `Microsoft Edge` sollte nur verwendet werden, `<ChannelName`>"ist nicht erforderlich.

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
