---
description: Erfahren Sie mehr über das Format der Manifestdatei in einem Erweiterungspaket.
title: Manifestdateiformat
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, web development, html, css, javascript, developer, extensions, mv2, mv3, manifest
ms.openlocfilehash: ac2358f8927a762dcef98f9e10cc9f343d8a93f1
ms.sourcegitcommit: afeeeea9fccc3c4c096d7d44c401f4fe87ea2cd7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "11599431"
---
# <a name="manifest-file-format-for-extensions"></a>Manifestdateiformat für Erweiterungen

Jede Erweiterung für Microsoft Edge (Chromium) verfügt über eine JSON-formatierte Manifestdatei mit dem Namen `manifest.json` .  Die Manifestdatei ist der Blueprint Ihrer Erweiterung.  Die Manifestdatei enthält Informationen wie:

*  Die Versionsnummer der Erweiterung.
*  Der Titel der Erweiterung.
*  Die Berechtigungen, die für die Ausführung der Erweiterung erforderlich sind.

Das Format `manifest.json` für Erweiterungen wechselt von Manifest V2 zu Manifest V3.  Beide Formate werden hier angezeigt.  Navigieren Sie zum Migrieren einer Manifest V2-Erweiterung zu Manifest V3 zu ["Vorbereiten" für die Aktualisierung der Erweiterungen von Manifest v2 auf v3.][MigrateToMV3]


## <a name="format-of-manifestjson-for-extensions-using-manifest-v3"></a>Format der manifest\.jsfür Erweiterungen mit Manifest V3

Der folgende Code zeigt die Felder, die für Erweiterungen für `manifest.json` ein Manifest V3-Paket unterstützt werden.

Um Referenzinformationen zu den einzelnen Feldern zu erhalten, navigieren Sie zum [Manifestdateiformat (V3),][ChromeDeveloperDocsExtensionsMv3Manifest] und wählen Sie dann die Links in den Feldern aus.

```json
{
  // Required
  "manifest_version": 3,
  "name": "My V3 Extension",
  "version": "versionString",

  // Recommended
  "action": {...},
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `service_ worker` is required
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": [...],
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": "aString",
  "web_accessible_resources": [...]
}
```

## <a name="format-of-manifestjson-for-extensions-using-manifest-v2"></a>Format der manifest\.jsfür Erweiterungen, die Manifest V2 verwenden

Der folgende Code zeigt die Felder, die für Erweiterungen für `manifest.json` ein Manifest V2-Paket unterstützt werden.

Um Referenzinformationen zu den einzelnen Feldern zu erhalten, navigieren Sie zum [Manifestdateiformat (V2),][ChromeDeveloperDocsExtensionsMv2Manifest] und wählen Sie dann die Links in den Feldern aus.

```json
{
  // Required
  "manifest_version": 2,
  "name": "My V2 Extension",
  "version": "versionString",

  // Recommended
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Pick one or none
  "browser_action": {...},
  "page_action": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `persistent` is recommended
    "persistent": false,
    // If `background` is included, `service_worker` is optional
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": ...,
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": ...,
  "web_accessible_resources": [...]
}
```

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier.](https://developer.chrome.com/docs/extensions/mv3/manifest/)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies


<!-- links -->
[MigrateToMV3]: ../developer-guide/migrate-your-extension-from-manifest-v2-to-v3.md "Vorbereiten der Aktualisierung der Erweiterungen von Manifest v2 auf v3 | Microsoft-Dokumente"

[ChromeDeveloperDocsExtensionsMv3Manifest]: https://developer.chrome.com/docs/extensions/mv3/manifest "Manifestdateiformat (V3) | Chrome-Entwickler"
[ChromeDeveloperDocsExtensionsMv2Manifest]: https://developer.chrome.com/docs/extensions/mv2/manifest "Manifestdateiformat (V2) | Chrome-Entwickler"
