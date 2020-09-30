---
description: Systemeigene Messaging-Dokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088555"
---
# Systemeigenes Messaging  

Erweiterungen können mit einer nativen Win32-Anwendung kommunizieren, die auf dem Gerät eines Benutzers mithilfe von Nachrichtenübergabe-APIs installiert ist. Der systemeigene Anwendungshost kann Nachrichten mit Erweiterungen mit Standardeingabe und Standardausgabe senden und empfangen. Erweiterungen mit systemeigenem Messaging werden in Microsoft Edge ähnlich wie bei jeder anderen Erweiterung installiert. Systemeigene Anwendungen werden jedoch nicht von Microsoft Edge installiert oder verwaltet.

Um die Erweiterung und den systemeigenen Anwendungshost zu erwerben, haben Sie folgende Möglichkeiten:

1. Verpacken Sie die Erweiterung und den Host zusammen. Wenn Benutzer das Paket installieren, werden sowohl die Erweiterung als auch der Host installiert.
1. Installieren Sie die Erweiterung aus dem [Microsoft Edge-Add-ons-Store][EdgeAddons], und bitten Sie Ihre Durchwahl Benutzer, den Host zu installieren. 

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung zum Senden und empfangen von Nachrichten mit systemeigenen Anwendungshosts einzurichten.

### Schritt 1: Hinzufügen von Berechtigungen zum Erweiterungs Manifest

Fügen Sie die nativeMessaging-Berechtigung für die Datei **manifest.js** der Erweiterung hinzu. Nachfolgend finden Sie ein Beispiel für manifest.jsauf:

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```

### Schritt 2: Erstellen einer systemeigenen Messaging-Host Manifestdatei
    
Systemeigene Anwendungen müssen eine systemeigene Messaging-Host Manifestdatei bereitstellen. Diese Manifestdatei enthält den Pfad zur ausführbaren systemeigenen Messaginghost-Datei, die Methode der Kommunikation mit der Erweiterung und eine Liste der zulässigen Erweiterungen, mit denen Sie kommunizieren kann. Browser lesen und überprüfen das systemeigene Messaging-Host Manifest, werden aber nie vom Browser installiert oder verwaltet. Die Host Manifestdatei muss eine gültige JSON-Datei mit den folgenden Feldern sein.

    
```json
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




| Name | Beschreibung |  
|:--- |:--- |  
| `name` | Der Name des systemeigenen Messaginghosts. Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .  Dieser Name darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.  Der Name darf nicht mit einem Punkt beginnen oder enden, und auf einen Punkt darf kein anderer Punkt folgen. |  
| `description` | Kurze Beschreibung der Anwendung. |  
| `path` | Der Pfad zur nativen Messaging-Host-Binärdatei. Auf Windows-Geräten können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält. Unter macOS und Linux muss der Pfad absolut sein. Der Hostprozess wird gestartet, wobei das aktuelle Verzeichnis auf das Verzeichnis festgesetzt ist, das die Host-Binärdatei enthält. Wenn dieser Parameter beispielsweise auf gesetzt ist `C:\Application\nm_host.exe` , wird die Binärdatei mit dem aktuellen Verzeichnis gestartet `C:\Application\` . |  
| `type` | Der Typ der Schnittstelle, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.  Derzeit gibt es nur einen möglichen Wert für diesen Parameter: `stdio` .  Dieser Wert gibt an, dass Microsoft Edge `stdin` `stdout` die Kommunikation mit dem Host verwenden soll. |  
| `allowed_origins` |  Liste der Erweiterungen, die möglicherweise auf den systemeigenen Messaging-Host zugreifen können  Damit Ihre Anwendung eine Erweiterung identifizieren und mit Ihnen kommunizieren kann, legen Sie Sie `allowed_origins` `chrome-extension://[Microsoft-Catalog-extensionID]` in der Manifestdatei des systemeigenen Messaging-Hosts auf fest. |  


Während der Entwicklung können Sie Ihre Erweiterung querladen, um systemeigene Nachrichten mit dem Host zu testen, indem Sie Folgendes ausführen:
1. Navigieren Sie zu `edge://extensions` , und aktivieren Sie dann die Umschaltfläche des Entwicklermodus. 
1. Wählen Sie laden entpackt aus, und wählen Sie dann Ihr Erweiterungspaket für querladen aus.  
1. Wählen Sie „OK“.
1. Überprüfen Sie, ob auf der `edge://extensions` Seite jetzt Ihre Erweiterung aufgeführt ist. 
1. Kopieren Sie den Schlüssel aus der ID aus dem Erweiterungs Eintrag auf der Seite.

Wenn Sie bereit sind, ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-ons-Store. Die Erweiterungs-ID der veröffentlichten Erweiterung kann sich von der ID unterscheiden, die beim Sideloading ihrer Erweiterung verwendet wird. Wenn die ID geändert wurde, aktualisieren `allowed_origins` Sie in der Host Manifestdatei die ID der veröffentlichten Erweiterung. 



### Schritt 3: Kopieren der systemeigenen Messaging-Host Manifestdatei auf Ihr System

Der letzte Schritt besteht darin, die systemeigene Messaging-Host Manifestdatei auf Ihren Computer zu kopieren und sicherzustellen, dass Sie ordnungsgemäß konfiguriert ist. Führen Sie die folgenden Schritte aus, um sicherzustellen, dass die systemeigene Messaging-Host Datei am erwarteten Ort abgelegt wird, da Sie je nach Plattform variiert.
    
**Windows**. Die Manifestdatei befindet sich möglicherweise an einer beliebigen Stelle im Dateisystem. Das Anwendungs Installationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert für diesen Schlüssel auf den vollständigen Pfad der Manifestdatei festlegen. Die folgenden Befehle sind Beispiele für Registrierungsschlüssel.
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    oder  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`,  
    
Führen Sie an einer Eingabeaufforderung den folgenden Befehl aus, um dem Ordner mit der Manifestdatei einen Registrierungsschlüssel hinzuzufügen.
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
Alternativ können Sie den folgenden Befehl in eine REG-Datei kopieren und ausführen, um den Registrierungsschlüssel hinzuzufügen. 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  Microsoft Edge fragt zuerst die 32-Bit-Registrierung und dann die 64-Bit-Registrierung ab, um systemeigene Messaginghosts zu identifizieren. Wenn Sie die obige reg-Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie Sie über eine Eingabeaufforderung des Administrators ausführen.


**Mac OS**. Die Manifestdatei muss wie folgt gespeichert werden:

1. Systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert. Beispielsweise muss die Manifestdatei in gespeichert werden. `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im NativeMessagingHosts-Unterverzeichnis im Benutzerprofilverzeichnis. Beispielsweise muss die Manifestdatei in gespeichert werden.  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    dabei `ChannelName` kann es sich um Canary, dev oder Beta handeln. Bei Verwendung des stable-Kanals `ChannelName` ist dies nicht erforderlich.


**Linux** Die Manifestdatei muss wie folgt gespeichert werden:

1. Systemweite systemeigene Messaginghosts:  `~/.config/microsoft-edge/NativeMessagingHosts`

1. Benutzerspezifische systemeigene Messaginghosts:  `/etc/opt/edge/native-messaging-hosts`


> [!NOTE]
> Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei angeben, und führen Sie Berechtigungen für die ausführbare Host-Datei aus.


> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-ons"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
