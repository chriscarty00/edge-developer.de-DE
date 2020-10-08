---
description: Systemeigene Messaging-Dokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: c5da9acf79225c88ad5829c2b7f57d1d833ca49b
ms.sourcegitcommit: 75c200a029d19fe372c1505c0006dbfbfad90bf5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100252"
---
# Systemeigenes Messaging  

Erweiterungen kommunizieren mit einer nativen Win32-Anwendung, die mithilfe von Nachrichtenübergabe-APIs auf dem Gerät eines Benutzers installiert ist.  Der systemeigene Anwendungshost sendet und empfängt Nachrichten mit Erweiterungen mit Standardeingabe und Standardausgabe.  Erweiterungen mit systemeigenem Messaging werden in Microsoft Edge ähnlich wie bei jeder anderen Erweiterung installiert.  Systemeigene Anwendungen werden jedoch nicht von Microsoft Edge installiert oder verwaltet.  

Sie verfügen über zwei Verteilungsmodelle, um die Erweiterung und den systemeigenen Anwendungshost zu erwerben.  

*   Verpacken Sie Ihre Erweiterung und den Host zusammen.  Wenn ein Benutzer das Paket installiert, werden sowohl die Erweiterung als auch der Host installiert.
*   Installieren Sie Ihre Erweiterung mit dem [Microsoft Edge-Add-on-Store][EdgeAddons], und ihre Erweiterung fordert die Benutzer auf, den Host zu installieren.  

Wenn Sie Ihre Erweiterung zum Senden und empfangen von Nachrichten mit systemeigenen Anwendungshosts erstellen möchten, lesen Sie die folgenden Schritte.  

## Schritt 1: Hinzufügen von Berechtigungen zum Erweiterungs Manifest  

Fügen Sie die `nativeMessaging` Berechtigung zum **manifest.js** Datei der Erweiterung hinzu.  Der folgende Codeausschnitt ist ein Beispiel für **manifest.js**ein.  

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

## Schritt 2 – Erstellen einer systemeigenen Messaging-Host Manifestdatei  

Systemeigene Anwendungen müssen eine systemeigene Messaging-Host Manifestdatei bereitstellen.  Die Manifestdatei enthält den Pfad zur systemeigenen Messaging-Host Laufzeit, die Methode der Kommunikation mit der Erweiterung und eine Liste der zulässigen Erweiterungen, mit denen Sie kommuniziert.  Der Browser liest und überprüft das systemeigene Messaging-Host Manifest.  Der Browser installiert oder verwaltet die systemeigene Messaging-Host Manifestdatei nicht.  

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

Die Host Manifestdatei muss eine gültige JSON-Datei mit den folgenden Schlüsseln sein.  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      Gibt den Namen des systemeigenen Messaginghosts an.  Clients übergeben diese Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .  
      
      *   Dieser Wert darf nur alphanumerische Zeichen, Unterstriche und Punkte in Kleinbuchstaben enthalten.  
      *   Dieser Wert darf nicht mit einem Punkt beginnen oder enden, und auf einen Punkt darf kein anderer Punkt folgen.  
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
      Gibt den Pfad zur nativen Messaging-Host-Binärdatei an.  
      
      *   Auf Windows-Geräten können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält.  
      *   Unter macOS und Linux muss der Pfad absolut sein.  
      
      Der Hostprozess beginnt mit dem aktuellen Verzeichnis, das auf das Verzeichnis festgesetzt ist, das die Host-Binärdatei enthält.  Beispiel: \ (Windows \), wenn dieser Parameter auf gesetzt ist `C:\Application\nm_host.exe` , wird die Binärdatei mit dem aktuellen Verzeichnis gestartet \ ( `C:\Application\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Gibt den Typ der Schnittstelle an, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.  Dieser Wert weist Microsoft Edge an, zu verwenden `stdin` und `stdout` mit dem Host zu kommunizieren.  
      Der einzige akzeptable Wert ist `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Gibt die Liste der Erweiterungen an, die auf den systemeigenen Messaging-Host zugreifen können.  Damit Ihre Anwendung eine Erweiterung erkennen und mit Ihnen kommunizieren kann, legen Sie in der systemeigenen Messaging-Host Manifestdatei den folgenden Wert fest.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Querladen Sie Ihre Erweiterung, um systemeigene Nachrichten mit dem Host zu testen.  
`microsoft_catalog_extension_id`Führen Sie die folgenden Schritte aus, um die Erweiterung während der Entwicklung zu querladen und abzurufen.  

1.  Navigieren Sie zu `edge://extensions` , und aktivieren Sie dann die Umschaltfläche des Entwicklermodus.  
1.  Wählen Sie **Laden entpackt**aus, und wählen Sie dann Ihr Erweiterungspaket für querladen aus.  
1.  Klicken Sie auf **OK**.
1.  Navigieren Sie zu `edge://extensions` Seite, und überprüfen Sie, ob Ihre Erweiterung aufgeführt ist.  
1.  Kopieren Sie den Schlüssel von `microsoft_catalog_extension_id` \ (ID \) aus dem Erweiterungs Eintrag auf der Seite.

Wenn Sie bereit sind, ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge-Add-ons-Store.  Die Erweiterungs-ID der veröffentlichten Erweiterung kann von der beim Sideloading der Erweiterung verwendeten ID abweichen.  Wenn die ID geändert wurde, aktualisieren `allowed_origins` Sie in der Host Manifestdatei die ID der veröffentlichten Erweiterung.  

## Schritt 3 – Kopieren der systemeigenen Messaging-Host Manifestdatei auf Ihr System  

Der letzte Schritt besteht darin, die systemeigene Messaging-Host Manifestdatei auf Ihren Computer zu kopieren und sicherzustellen, dass Sie ordnungsgemäß konfiguriert ist.  Führen Sie die folgenden Schritte aus, um sicherzustellen, dass Ihre Manifestdatei an dem erwarteten Ort abgelegt wird.  Der Standort variiert je nach Plattform.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

Die Manifestdatei befindet sich möglicherweise an einer beliebigen Stelle im Dateisystem.  Das Anwendungs Installationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert für diesen Schlüssel auf den vollständigen Pfad der Manifestdatei festlegen.  Die folgenden Befehle sind Beispiele für Registrierungsschlüssel.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

So fügen Sie dem Verzeichnis mit dem manifestschlüssel einen Registrierungsschlüssel hinzu  

*   Befehl "ausführen" in der Eingabeaufforderung    
    
    1.  Führen Sie den folgenden Befehl aus.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   Erstellen `.reg` Sie eine Datei, und führen Sie Sie aus.  
    
    1.  Kopieren Sie den folgenden Befehl in eine `.reg` Datei.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Führen Sie die `.reg` Datei aus.  
    
Microsoft Edge fragt zuerst die 32-Bit-Registrierung und dann die 64-Bit-Registrierung ab, um systemeigene Messaginghosts zu identifizieren.  Wenn Sie die obige `.reg` Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie Sie über eine Eingabeaufforderung des Administrators ausführen.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.  

*   Systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.  Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden. 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im unter `NativeMessagingHosts` Verzeichnis des Benutzerprofilverzeichnisses.  Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    Die  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` muss einer der folgenden Werte sein.  
    
    *   Canary  
    *   Dev  
    *   Beta  

    Bei Verwendung des stable-Kanals `{Channel_Name}` ist dies nicht erforderlich.  

### [Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.  

*   Systemweite systemeigene Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.  Die Manifestdatei muss an folgendem Speicherort gespeichert werden.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Benutzerspezifische systemeigene Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im unter `NativeMessagingHosts` Verzeichnis des Benutzerprofilverzeichnisses.  Die Manifestdatei muss an folgendem Speicherort gespeichert werden.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei angeben, und führen Sie Berechtigungen für die Host Laufzeit aus.  

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-ons"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
