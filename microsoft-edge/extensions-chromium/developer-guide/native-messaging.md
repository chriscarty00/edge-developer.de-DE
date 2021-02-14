---
description: Systemeigene Messagingdokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: 2d629762d4c7c75832905cfbf8c2d5311191092d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327701"
---
# Systemeigenes Messaging  

Erweiterungen kommunizieren mit einer systemeigenen Win32-Anwendung, die auf dem Gerät eines Benutzers installiert ist, und verwenden APIs zum Übergeben von Nachrichten.  Der systemeigene Anwendungshost sendet und empfängt Nachrichten mit Erweiterungen mithilfe von Standardeingabe und Standardausgabe.  Erweiterungen, die natives Messaging verwenden, werden in Microsoft Edge ähnlich wie jede andere Erweiterung installiert.  Systemeigene Anwendungen werden jedoch nicht von Microsoft Edge installiert oder verwaltet.  

Um die Erweiterung und den systemeigenen Anwendungshost zu erwerben, verfügen Sie über zwei Verteilungsmodelle.  

*   Packen Sie Ihre Erweiterung und den Host zusammen.  Wenn ein Benutzer das Paket installiert, werden sowohl die Erweiterung als auch der Host installiert.  
*   Installieren Sie Ihre Erweiterung mithilfe des [Microsoft Edge-Add-Ons-Speichers,] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]und Die Benutzer werden aufgefordert, den Host zu installieren.  

Informationen zum Erstellen Ihrer Erweiterung zum Senden und Empfangen von Nachrichten mit systemeigenen Anwendungshosts finden Sie in den folgenden Schritten.  

## Schritt 1: Hinzufügen von Berechtigungen zum Erweiterungsmanifest  

Fügen Sie `nativeMessaging` die Berechtigung zummanifest.js** datei** der Erweiterung hinzu.  Der folgende Codeausschnitt ist ein Beispiel für **manifest.jsauf**.  

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

## Schritt 2: Erstellen der systemeigenen Messaginghostmanifestdatei  

Systemeigene Anwendungen müssen eine systemeigene Messaginghostmanifestdatei bereitstellen.  Die Manifestdatei enthält die folgenden Informationen.  

*   Der Pfad zur nativen Messaginghostlaufzeit.  
*   Die Methode der Kommunikation mit der Erweiterung.  
*   Eine Liste der zulässigen Erweiterungen, mit denen kommuniziert wird.  
    
Der Browser liest und überprüft das systemeigene Messaginghostmanifest.  Der Browser installiert oder verwaltet die systemeigene Messaginghostmanifestdatei nicht.  

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

Die Hostmanifestdatei muss eine gültige JSON-Datei sein, die die folgenden Schlüssel enthält.  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      Gibt den Namen des systemeigenen Messaginghosts an.  Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .  
      
      *   Dieser Wert darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.  
      *   Dieser Wert darf nicht mit einem Punkt beginnen oder enden, und einem Punkt darf kein weiterer Punkt folgen.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      Beschreibt die Anwendung.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      Gibt den Pfad zur nativen Messaginghost-Binärdatei an.  
      
      *   Auf Windows-Geräten können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält.  
      *   Unter macOS und Linux muss der Pfad absolut sein.  
      
      Der Hostprozess beginnt mit dem Verzeichnis, das die Host binär enthält, mit dem aktuellen Verzeichnis.  Wenn dieser Parameter beispielsweise auf \(Windows\) festgelegt ist, wird die Binärdatei mit dem aktuellen `C:\Application\nm_host.exe` Verzeichnis \( `C:\Application\` \) gestartet.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Gibt den Typ der Schnittstelle an, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.  Dieser Wert gibt Microsoft Edge an, den Host zu `stdin` verwenden und mit ihm zu `stdout` kommunizieren.  
      Der einzige zulässige Wert ist `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Gibt die Liste der Erweiterungen an, die Zugriff auf den systemeigenen Messaginghost haben.  Damit Ihre Anwendung eine Erweiterung identifizieren und mit dieser kommunizieren kann, legen Sie in der systemeigenen Messaginghostmanifestdatei den folgenden Wert festgelegt.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Laden Sie Ihre Erweiterung quer, um systemeigenes Messaging mit dem Host zu testen.  
Führen Sie die folgenden Schritte aus, um die Erweiterung während der Entwicklung quer zu laden und `microsoft_catalog_extension_id` abzurufen.  

1.  Navigieren Sie `edge://extensions` zu , und aktivieren Sie dann die Umschaltfläche für den Entwicklermodus.  
1.  Choose **Load unpacked**, and then select your extension package to sideload.  
1.  Klicken Sie auf **OK**.  
1.  Navigieren Sie zu `edge://extensions` der Seite, und überprüfen Sie, ob Ihre Erweiterung aufgeführt ist.  
1.  Kopieren Sie den Schlüssel von `microsoft_catalog_extension_id` \(ID\) aus dem Erweiterungseintrag auf der Seite.  

Wenn Sie bereit sind, Ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-Ons-Store.  Die Erweiterungs-ID der veröffentlichten Erweiterung kann sich von der ID unterscheiden, die beim Querladen der Erweiterung verwendet wird.  Wenn sich die ID geändert hat, aktualisieren Sie `allowed_origins` in der Hostmanifestdatei mit der ID Ihrer veröffentlichten Erweiterung.  

## Schritt 3: Kopieren der systemeigenen Messaginghostmanifestdatei in Ihr System  

Im letzten Schritt wird die systemeigene Messaginghostmanifestdatei auf Ihren Computer kopiert und sichergestellt, dass die Manifestdatei ordnungsgemäß konfiguriert ist.  Führen Sie die folgenden Schritte aus, um sicherzustellen, dass sich die Manifestdatei am erwarteten Speicherort befindet.  Der Standort variiert je nach Plattform.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

Die Manifestdatei kann sich an einer beliebigen Stelle im Dateisystem befinden.  Das Anwendungsinstallationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert für den Schlüssel auf den vollständigen Pfad der Manifestdatei festlegen.  Die folgenden Befehle sind Beispiele für Registrierungsschlüssel.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

So fügen Sie dem Verzeichnis mit dem Manifestschlüssel einen Registrierungsschlüssel hinzu.  

*   Führen Sie den Befehl an der Eingabeaufforderung aus.  
    
    1.  Führen Sie den folgenden Befehl aus.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   Erstellen Sie `.reg` eine Datei, und führen Sie sie aus.  
    
    1.  Kopieren Sie den folgenden Befehl in eine `.reg` Datei.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Führen Sie die `.reg` Datei aus.  
    
Microsoft Edge fragt den `HKEY_CURRENT_USER` Stammschlüssel ab, gefolgt von `HKEY_LOCAL_MACHINE` .  In beiden Schlüsseln wird zuerst die 32-Bit-Registrierung durchsucht, und dann wird die 64-Bit-Registrierung durchsucht, um systemeigene Messaginghosts zu identifizieren.  Der Registrierungsschlüssel gibt den Speicherort des systemeigenen Messaginghostmanifests an.  Wenn Microsoft Edge den Registrierungsschlüssel an einem der zuvor aufgeführten Speicherorte findet, werden die in diesem Absatz aufgeführten Speicherorte nicht abgefragt.  Wenn Sie die obige Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie sie über `.reg` eine Administratorbefehlsaufforderung ausführen.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.  

*   Systemweite systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.  Die Manifestdatei muss z. B. an folgendem Speicherort gespeichert werden.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.  Die Manifestdatei muss z. B. an folgendem Speicherort gespeichert werden.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    Das  `{Channel_Name}` In muss einer der folgenden Werte `Microsoft Edge {Channel_Name}` sein.  
    
    *   Canary  
    *   Dev  
    *   Beta  

    Bei Verwendung des `{Channel_Name}` Stable-Kanals ist dies nicht erforderlich.  

### [Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.  

*   Systemweite systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.  Die Manifestdatei muss an folgendem Speicherort gespeichert werden.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.  Die Manifestdatei muss an folgendem Speicherort gespeichert werden.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei bereitstellen und Berechtigungen für die Hostlaufzeit ausführen.  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-Ons"

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier.](https://developer.chrome.com/extensions/nativeMessaging)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
