---
description: Native Messagingdokumentation
title: Systemeigenes Messaging
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/31/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Addons, Partner Center, Entwickler
ms.openlocfilehash: e6233289794bc1c3ef235af46402c23173c09857
ms.sourcegitcommit: e6a4f73be57439149e3cc56491d7364831d0079e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "11475211"
---
# <a name="native-messaging"></a>Systemeigenes Messaging  

Erweiterungen kommunizieren mit einer systemeigenen Win32-App, die auf dem Gerät eines Benutzers installiert ist, mithilfe von APIs, die Nachrichten übergeben.  Der systemeigene App-Host sendet und empfängt Nachrichten mit Erweiterungen mithilfe von Standardeingaben und Standardausgabe.  Erweiterungen mit systemeigenem Messaging werden in Microsoft Edge wie jede andere Erweiterung installiert.  Native Apps werden jedoch nicht von der Microsoft Edge.  

Zum Erwerben der Erweiterung und des nativen App-Hosts verfügen Sie über zwei Verteilungsmodelle.  

*   Packen Sie Ihre Erweiterung und den Host zusammen.  Wenn ein Benutzer das Paket installiert, werden sowohl die Erweiterung als auch der Host installiert.  
*   Installieren Sie Ihre Erweiterung [mithilfe Microsoft Edge Add-Ons-Speichers,][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]und Ihre Erweiterung fordert Benutzer auf, den Host zu installieren.  

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung zum Senden und Empfangen von Nachrichten mit systemeigenen App-Hosts zu erstellen.  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a>Schritt 1 : Hinzufügen von Berechtigungen zum Erweiterungsmanifest  

Fügen Sie `nativeMessaging` der Dateimanifest.js** der** Erweiterung die Berechtigung hinzu.  Der folgende Codeausschnitt ist ein Beispiel für **manifest.jsin**.  

```json
{
    "name": "Native Messaging Example",
    "version": "1.0",
    "manifest_version": 2, 
    "description": "Send a message to a native app.",
    "app": { 
        "launch": { 
            "local_path": "main.html" 
        } 
    }, 
    "icons": { 
        "128": "icon-128.png"
    }, 
    "permissions": ["nativeMessaging"] 
}
```  

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a>Schritt 2 : Erstellen Der systemeigenen Messaginghostmanifestdatei  

Systemeigene Apps müssen eine systemeigene Messaginghostmanifestdatei bereitstellen.  Die Manifestdatei enthält die folgenden Informationen.  

*   Der Pfad zur nativen Messaginghost-Laufzeit.  
*   Die Methode der Kommunikation mit der Erweiterung.  
*   Eine Liste der zulässigen Erweiterungen, mit denen sie kommuniziert.  
    
Der Browser liest und überprüft das systemeigene Messaginghostmanifest.  Der Browser installiert oder verwaltet die systemeigene Messaginghostmanifestdatei nicht.  

```json
{
    "name": "com.my_company.my_app",
    "description": "My App",
    "path": "C:\\Program Files\\My App\\chrome_native_messaging_host.exe",
    "type": "stdio",
    "allowed_origins": [
        "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

Die Hostmanifestdatei muss eine gültige JSON-Datei sein, die die folgenden Schlüssel enthält.  

:::row:::
   :::column span="1":::
      **Schlüssel**  
   :::column-end:::
   :::column span="3":::
      **Details**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Gibt den Namen des systemeigenen Messaginghosts an.  Clients übergeben die Zeichenfolge an `runtime.connectNative` oder `runtime.sendNativeMessage` .  
      
      *   Der Wert darf nur alphanumerische Kleinbuchstaben, Unterstriche und Punkte enthalten.  
      *   Der Wert darf nicht mit einem Punkt beginnen oder enden, und einem Punkt darf kein weiterer Punkt gefolgt werden.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Beschreibt die App.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Gibt den Pfad zur nativen Messaginghost-Binärdatei an.  
      
      *   Auf Windows können Sie relative Pfade zu dem Verzeichnis verwenden, das die Manifestdatei enthält.  
      *   Unter macOS und Linux muss der Pfad absolut sein.  
          
      Der Hostprozess beginnt mit dem aktuellen Verzeichnis, das auf das Verzeichnis festgelegt ist, das die Host binär enthält.  Beispiel: \(Windows\), wenn der Parameter auf festgelegt ist, wird die Binärdatei mit dem aktuellen Verzeichnis `C:\App\nm_host.exe` \( `C:\App\` \) gestartet.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Gibt den Typ der Schnittstelle an, die für die Kommunikation mit dem systemeigenen Messaginghost verwendet wird.  Der Wert gibt Microsoft Edge an, den Host zu `stdin` verwenden und mit ihm zu `stdout` kommunizieren.  
      Der einzige akzeptable Wert ist `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      Gibt die Liste der Erweiterungen an, die Zugriff auf den systemeigenen Messaginghost haben.  Um Ihre App für die Identifizierung und Kommunikation mit einer Erweiterung zu aktivieren, legen Sie in der manifesten Datei des nativen Messaginghosts den folgenden Wert ein.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Querladen Der Erweiterung, um systemeigene Messaging mit dem Host zu testen.  
Führen Sie die folgenden Aktionen aus, um die Erweiterung während der Entwicklung quer zu laden und `microsoft_catalog_extension_id` abzurufen.  

1.  Navigieren Sie `edge://extensions` zu , und aktivieren Sie dann die Umschaltfläche Entwicklermodus.  
1.  Wählen **Sie Auspacken laden**aus, und wählen Sie dann ihr Erweiterungspaket aus, das quergeladen werden soll.  
1.  Klicken Sie auf **OK**.  
1.  Navigieren Sie zu `edge://extensions` Seite, und überprüfen Sie, ob Ihre Erweiterung aufgeführt ist.  
1.  Kopieren Sie den Schlüssel `microsoft_catalog_extension_id` aus \(ID\) aus dem Erweiterungseintrag auf der Seite.  
    
Wenn Sie bereit sind, Ihre Erweiterung an Benutzer zu verteilen, veröffentlichen Sie Ihre Erweiterung im Microsoft Edge Add-Ons-Speicher.  Die Erweiterungs-ID der veröffentlichten Erweiterung kann sich von der ID unterscheiden, die beim Querladen der Erweiterung verwendet wird.  Wenn die ID geändert wurde, aktualisieren Sie `allowed_origins` in der Hostmanifestdatei mit der ID Ihrer veröffentlichten Erweiterung.  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a>Schritt 3 : Kopieren der systemeigenen Messaginghostmanifestdatei in Ihr System  

Der letzte Schritt besteht darin, die systemeigene Messaginghostmanifestdatei auf Ihren Computer zu kopieren und sicherzustellen, dass die Manifestdatei ordnungsgemäß konfiguriert ist.  Führen Sie die folgenden Aktionen aus, um sicherzustellen, dass die Manifestdatei am erwarteten Speicherort platziert wird.  Der Standort variiert je nach Plattform.

> [!NOTE]
> Stellen Sie sicher, dass Sie Leseberechtigungen für die Manifestdatei bereitstellen und Berechtigungen für die Hostlaufzeit ausführen.  

### [<a name="windows"></a>Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

Die Manifestdatei kann sich an einer beliebigen Stelle im Dateisystem befinden.  Das App-Installationsprogramm muss einen Registrierungsschlüssel erstellen und den Standardwert des Schlüssels auf den vollständigen Pfad der Manifestdatei festlegen.  Die folgenden Speicherorte sind Beispiele für Registrierungsschlüssel.  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

Führen Sie eine der folgenden Aktionen aus, um dem Verzeichnis einen Registrierungsschlüssel mit dem Manifestschlüssel hinzuzufügen.  

*   Führen Sie den Befehl in der Eingabeaufforderung aus.  
    
    1.  Führen Sie den folgenden Befehl aus.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   Erstellen Sie `.reg` eine Datei, und führen Sie sie aus.  
    
    1.  Kopieren Sie den folgenden Befehl in eine `.reg` Datei.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Führen Sie die `.reg` Datei aus.  
        
Microsoft Edge fragt den `HKEY_CURRENT_USER` Stammschlüssel ab, gefolgt von `HKEY_LOCAL_MACHINE` .  In beiden Schlüsseln wird zuerst die 32-Bit-Registrierung durchsucht, und dann wird die 64-Bit-Registrierung durchsucht, um systemeigene Messaginghosts zu identifizieren.  Der Registrierungsschlüssel gibt den Speicherort des systemeigenen Messaginghostmanifests an.  Wenn die Registrierungseinträge für Microsoft Edge nicht den Speicherort des Hostmanifests haben, werden die Registrierungsspeicherorte Chromium und Chrome als Ausweichoptionen verwendet.  Wenn Microsoft Edge den Registrierungsschlüssel an einem der zuvor aufgeführten Speicherorte findet, werden die im folgenden Codeausschnitt aufgeführten Speicherorte nicht abgefragt.  Wenn Sie die erstellte Datei als Teil eines Batchskripts ausführen, stellen Sie sicher, dass Sie sie mithilfe einer `.reg` Administrator-Eingabeaufforderung ausführen.

Die folgende Liste ist die Suchreihenfolge für die Registrierungsstandorte.  

```output
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\

HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\
```  
 
> [!NOTE] 
> Wenn Sie Erweiterungen für die Microsoft Edge-Add-Ons und den Chrome Webstore haben, müssen Sie die Erweiterungs-IDs hinzufügen, die beiden Speichern in der Hostmanifestdatei entspricht, da nur das Hostmanifest gelesen wird, das dem ersten gefundenen Registrierungsspeicherort `allowed_origins` entspricht.  

### [<a name="macos"></a>macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.  

*   Systemweite systemweite native Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.  Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   Benutzerspezifische native Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.  Beispielsweise muss die Manifestdatei an folgendem Speicherort gespeichert werden.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    Der  `{Channel_Name}` `Microsoft Edge {Channel_Name}` In-Wert muss einer der folgenden Werte sein.  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    Bei Verwendung des ` {Channel_Name}` Stable-Kanals ist dies nicht erforderlich.  
    
### [<a name="linux"></a>Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Führen Sie eine der folgenden Aktionen aus, um die Manifestdatei zu speichern.  

*   Systemweite systemweite native Messaginghosts, die für alle Benutzer verfügbar sind, werden an einem festen Speicherort gespeichert.  Die Manifestdatei muss an folgendem Speicherort gespeichert werden.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Benutzerspezifische native Messaginghosts, die nur für den aktuellen Benutzer verfügbar sind, befinden sich im Unterverzeichnis `NativeMessagingHosts` im Benutzerprofilverzeichnis.  Die Manifestdatei muss an folgendem Speicherort gespeichert werden.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Microsoft Edge-Add-Ons"

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/extensions/nativeMessaging).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
