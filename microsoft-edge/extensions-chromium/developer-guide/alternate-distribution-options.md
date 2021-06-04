---
description: Informationen zum Verteilen von Erweiterungen mithilfe alternativer Methoden, die keine überprüften Speicher verwenden
title: Alternative Methode zum Verteilen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: 3b2c72e13488632e2fadea2a7e8eb95888f67170
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343150"
---
# Alternative Erweiterungsverteilungsmethoden  

Im Allgemeinen werden Erweiterungen über den Microsoft Edge-Add-Ons-Speicher verteilt. Es gibt einige Szenarien, in denen Entwickler Erweiterungen mithilfe alternativer Methoden verteilen müssen. Beispiel:

1.  Die Erweiterung ist anderen Software zugeordnet und sollte zusammen mit dem Rest der gebündelten Software installiert werden.   
1.  Netzwerkadministratoren möchten eine Erweiterung in ihrer Organisation verteilen.   

Erweiterungen, die nicht aus dem Edge-Add-Ons-Speicher geladen werden, werden als extern installierte Erweiterungen bezeichnet. Die folgende Liste enthält alternative Methoden zum Verteilen extern installierter Erweiterungen. 

*   Verwenden Sie die Windows-Registrierung (nur Windows).  
*   Verwenden Sie eine einstellungs-JSON-Datei (macOS und Linux).  
    
##  <a name="before-you-begin"></a>Vorbemerkungen  

Stellen Sie sicher, dass Sie Ihre Erweiterung im Microsoft Edge-Add-Ons-Speicher veröffentlichen oder eine Datei packen und sicherstellen, dass sie erfolgreich auf Ihrem `.crx` Computer installiert wird.  Wenn Sie die Datei mithilfe von installieren, stellen Sie sicher, dass Sie unter dieser URL zu `.crx` `update_URL` Ihrer Erweiterung navigieren können.  

Stellen Sie außerdem sicher, dass Sie über die folgenden Informationen verfügen.    

1.  Der Dateipfad der `.crx` Datei oder der Ihrer `update_URL` Erweiterung.
1.  Die Version Ihrer Erweiterung.  Die Versionsinformationen sind in Ihrer Manifestdatei oder in Microsoft Edge unter verfügbar, `edge://extensions` nachdem Sie die gepackte Erweiterung geladen haben.   
1.  Die ID Ihrer Erweiterung.  Die ID-Informationen sind in Microsoft Edge unter `edge://extensions` verfügbar, nachdem Sie die gepackte Erweiterung geladen haben.  

> [!NOTE] 
> Die folgenden Beispiele werden `1.0` als Version und für die ID `aaaaaaaaaabbbbbbbbbbcccccccccc` verwendet.  

##  <a name="use-the-windows-registry-(windows-only)"></a>Verwenden der Windows-Registrierung (nur Windows)  

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung mithilfe der Windows-Registrierung zu verteilen.

1.  Suchen oder erstellen Sie den folgenden Schlüssel in der Registrierung:  
    *   32-Bit-Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .  
    *   64-Bit-Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .  
1.  Erstellen Sie einen neuen Schlüssel oder Ordner unter **Erweiterungen** mit demselben Namen wie die ID Ihrer Erweiterung. Erstellen Sie beispielsweise den Schlüssel mit dem Namen `aaaaaaaaaabbbbbbbbbbcccccccccc` .  
1.  Erstellen Sie **im Schlüssel** Erweiterungen die `update_url` Eigenschaft, und legen Sie den Wert auf . `https://edge.microsoft.com/extensionwebstorebase/v1/crx`  Die `update_url` Eigenschaft verweist auf die Datei Ihrer Erweiterung im Microsoft `.crx` Edge-Add-Ons-Speicher.  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > Wenn Sie eine Erweiterung aus dem Chrome Web Store installieren möchten, legen Sie den Wert auf `update_url` . `https://clients2.google.com/service/update2/crx`  
  
1.  Überprüfen Sie, ob Ihre Erweiterung in Microsoft Edge aufgeführt ist, indem Sie zu `edge://extensions` navigieren.  

##  <a name="use-a-preferences-json-file-(macos-and-linux)"></a>Verwenden einer Einstellungs-JSON-Datei (macOS und Linux)  

Führen Sie die folgenden Schritte aus, um Ihre Erweiterung mithilfe einer Einstellungs-JSON-Datei zu verteilen.

1.  Stellen Sie bei Der Verwendung von Linux sicher, dass Ihre Erweiterungsdatei auf dem Computer verfügbar ist, auf dem `.crx` die Erweiterung installiert wird. Kopieren Sie die Erweiterungsdatei in ein lokales Verzeichnis, oder verwenden Sie eine Netzwerkfreigabe, die vom `.crx` Computer aus erreichbar ist. 
1.  Erstellen Sie eine JSON-Datei, in der der Name der Datei der ID Ihrer Erweiterung entspricht. Erstellen Sie beispielsweise eine JSON-Datei mit dem Dateinamen `aaaaaaaaaabbbbbbbbbbcccccccccc.json` .  
1.  Speichern Sie die JSON-Datei je nach Betriebssystem in einem der folgenden Ordner.   
    *   **macOS**  
        *   Benutzerspezifisch: `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   Alle Benutzer: `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        Um zu verhindern, dass nicht autorisierte Benutzer Erweiterungen für alle Benutzer installieren, stellen Sie sicher, dass Ihre Erweiterungsdatei schreibgeschützt ist. Stellen Sie außerdem sicher, dass die folgenden Bedingungen erfüllt sind:
        
        *   Jedes Verzeichnis im Pfad gehört dem Benutzerstamm.  
        *   Jedes Verzeichnis im Pfad wird der `admin` Oder-Gruppe `wheel` zugewiesen.  
        *   Jedes Verzeichnis im Pfad ist nicht weltbeschreibbar.  
        *   Der Pfad muss auch frei von symbolischen Verknüpfungen sein.  
        
    *   **Linux**  
        *   Benutzerspezifisch: `~/.config/microsoft-edge/External Extensions/`  
        *   Alle Benutzer: `/usr/share/microsoft-edge/extensions/`  
1.  Kopieren Sie je nach Szenario den entsprechenden Code, der in Ihre JSON-Datei folgt. 
    *   Gilt nur für Linux. Wenn Sie aus einer Datei installieren, geben Sie den Speicherort und die Version mit `external_crx` und `external_version` an.  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   Gilt für macOS und Linux. Wenn Sie von einem `update_URL` installieren, geben Sie die Update-URL mit `external_update_url` an. 
        
        Kopieren Sie den folgenden Code in Ihre JSON-Datei, wenn Sie nur aus lokalen `.crx` Dateien unter Linux installieren.  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  Kopieren Sie den folgenden Code bei der Installation aus dem Microsoft Edge-Add-Ons-Speicher unter macOS und Linux in Ihre JSON-Datei.
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  Wenn Sie Erweiterungen für bestimmte Locales installieren möchten, listen Sie die unterstützten Locales mithilfe von `supported_locale` auf.  Sie können auch übergeordnete Locales angeben, um Die Erweiterung für alle Sprach-Locales zu installieren, die dieses übergeordnete Element verwenden. Wenn Sie beispielsweise das übergeordnete Locale verwenden, wird Ihre Erweiterung für alle englischen Locales installiert, z. B. `en` `en-US` , und so `en-GB` weiter.  Wenn Benutzer ihr Locale in ihrem Browser ändern, werden extern installierte Erweiterungen deinstalliert.  Verwenden Sie nicht , um Die Erweiterung für ein Beliebiges Locale zu `supported_locales` installieren.  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  Überprüfen Sie, ob Ihre Erweiterung in Microsoft Edge installiert ist, indem Sie zu `edge://extensions` navigieren.  

##  <a name="update-and-uninstall-externally-installed-extensions"></a>Aktualisieren und Deinstallieren extern installierter Erweiterungen

Microsoft Edge überprüft die Metadateneinträge in der Registrierung jedes Mal, wenn der Browser gestartet wird, und nimmt änderungen an den extern installierten Erweiterungen vor.  

Wenn Sie Ihre Erweiterung auf eine neue Version aktualisieren möchten, aktualisieren Sie die Version in der Manifestdatei, und aktualisieren Sie dann die Version in der Registrierung.  

Möglicherweise müssen Sie extern installierte Erweiterungen deinstallieren, die als Teil eines Softwarepakets installiert wurden, das zuvor auf dem Computer installiert wurde.  Um Ihre Erweiterung zu deinstallieren, entfernen Sie die Einstellungs-JSON-Datei, oder entfernen Sie den Schlüssel aus der Registrierung.   

<!-- links -->  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/apps/external_extensions).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
