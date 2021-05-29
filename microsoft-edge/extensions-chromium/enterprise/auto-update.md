---
description: Informationen zu automatischen Updates für Erweiterungen in Microsoft Edge
title: Automatisches Aktualisieren von Erweiterungen in Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: d9901f9c39dabfab111eb7e0c34a3e267a317110
ms.sourcegitcommit: 59d8043e37b89da814f63bc85daf84e0e7167eab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "11586388"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="automatically-update-extensions-in-microsoft-edge"></a>Automatisches Aktualisieren von Erweiterungen in Microsoft Edge  

Wenn Sie festlegen, dass Ihre Erweiterung automatisch aktualisiert wird, werden die folgenden Vorteile für Microsoft Edge, wenn sie auf automatische Aktualisierung festgelegt ist.  

*   Integrieren sie Fehler- und Sicherheitsbehebungen.  
*   Fügen Sie neue Features oder Leistungsverbesserungen hinzu.  
*   Verbessern Sie die Benutzeroberfläche.  

Zuvor wurden nicht speicherbasierte Erweiterungen unterstützt.  Außerdem haben Sie die systemeigenen Binärdateien und die Erweiterung gleichzeitig aktualisiert.  

Jetzt hostet Microsoft Edge Add-Ons-Speicher Ihre Erweiterungen, und Sie aktualisieren Ihre Erweiterung mit demselben Mechanismus wie Microsoft Edge.  Sie steuern den Updatemechanismus nicht.  Seien Sie vorsichtig, wenn Sie Erweiterungen aktualisieren, die von systemeigenen Binärdateien abhängig sind.  

> [!NOTE]
> Dieser Artikel gilt nicht für Erweiterungen, die Sie mit dem [Partner Center-Dashboard][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] veröffentlichen.  Sie können das Dashboard verwenden, um aktualisierte Versionen für Ihre Benutzer und für den Microsoft Edge-Add-Ons-Speicher zu veröffentlichen.  Weitere Informationen finden Sie unter [Aktualisieren oder Entfernen der Erweiterung.][ExtensionsPublishUpdateExtension]  

## <a name="overview"></a>Übersicht  

Alle paar Stunden überprüft Microsoft Edge, ob jede installierte Erweiterung oder App über eine Update-URL verfügt.  Verwenden Sie das Feld im Manifest, um eine Update-URL für Ihre `update_url` Erweiterung anzugeben.  Das `update_url` Feld im Manifest zeigt auf einen Speicherort, um eine Aktualisierungsprüfung zu vervollständigen.  Für jeden `update_url` sendet er Anforderungen für aktualisierte Manifest-XML-Dateien.  Wenn in der Updatemanifest-XML-Datei eine neuere Version als die installierte aufgeführt ist, Microsoft Edge die neuere Version heruntergeladen und installiert.  Der gleiche Prozess funktioniert für manuelle Updates, bei denen die neue Datei mit demselben privaten Schlüssel wie die aktuell installierte `.crx` Version signiert werden muss.  

> [!NOTE]
> Um den Datenschutz der Benutzer zu gewährleisten, sendet Microsoft Edge keine Kopfzeilen mit Manifestanforderungen für automatische Updates und ignoriert alle Kopfzeilen in den Antworten auf `Cookie` `Set-Cookie` diese Anforderungen.  

## <a name="update-url"></a>Update-URL  

Wenn Sie Ihre eigene Erweiterung oder App hosten, müssen Sie der Datei `update_url` das Feld `manifest.json` hinzufügen.  Überprüfen Sie den folgenden Codeausschnitt für ein Beispiel für `update_url` .  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a>Aktualisiertes Manifest  

Das aktualisierte Manifest, das vom Server zurückgegeben wird, sollte ein XML-Dokument sein.  Überprüfen Sie den folgenden Codeausschnitt für ein Beispiel der aktualisierten Manifest-XML-Datei.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

In der folgenden Tabelle werden die Attribute der aktualisierten Manifest-XML-Datei beschrieben.  

| Attribut | Details | 
|:--- |:--- |  
| `appid` | Die Erweiterungs-ID wird basierend auf einem Hash des öffentlichen Schlüssels generiert.  Um die ID einer Erweiterung zu finden, öffnen Sie Microsoft Edge, und navigieren Sie zu `edge://extensions` . |  
| `codebase` | Eine URL zur `.crx` Datei. |  
| `version` | Dieser Attributwert wird von Microsoft Edge verwendet, um zu bestimmen, ob die `.crx` durch angegebene Datei heruntergeladen werden `codebase` soll.  Es sollte mit dem Wert `version` in der Datei der Datei `manifest.json` `.crx` übereinstimmen. |  

Die Updatemanifest-XML-Datei kann Informationen zu mehreren Erweiterungen enthalten, indem mehrere Elemente hinzugefügt werden.  

## <a name="testing"></a>Testen  

Die Standardhäufigkeit der Aktualisierungsprüfung beträgt mehrere Stunden.  Um ein Update zu erzwingen, navigieren Sie zu `edge://extensions` und wählen Sie die Schaltfläche Erweiterungen **jetzt** aktualisieren aus.  

## <a name="advanced-usage-request-parameters"></a>Erweiterte Verwendung: Anforderungsparameter  

Der grundlegende Mechanismus ist einfach.  Führen Sie die folgenden Aktionen aus, um Die Erweiterung automatisch zu aktualisieren.  

1.  Hochladen Ihre statische XML-Datei auf Dem Webserver, z. B. Apache.  
1.  Aktualisieren Sie die XML-Datei, wenn Sie neue Versionen Ihrer Erweiterungen veröffentlichen.  
    
Nutzen Sie die Tatsache, dass einige Parameter, die der Updatemanifestanforderung hinzugefügt wurden, die Erweiterung und `ID` `version` angeben.  Sie können dasselbe für alle Erweiterungen anstelle einer `update URL` statischen XML-Datei verwenden.  Um dasselbe für alle Erweiterungen zu verwenden, zeigen Sie auf eine URL, auf der dynamischer serverseitiger Code ausgeführt wird, `update URL` um die Parameter zu testen.  

Im folgenden Beispiel wird das Format der Anforderungsparameter der Update-URL veranschaulicht.  

```url
?x={extension_data}
```  

In diesem Beispiel `{extension_data}` handelt es sich um eine URL-codierte Zeichenfolge, die das folgende Format verwendet.  

```url
id={id}&v={version}
```  

Die folgenden beiden Erweiterungen verweisen beispielsweise beide auf die gleiche Update-URL `http://contoso.com/extension_updates.php` .  

*   Erweiterung 1  
    *   ID: `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
    *   Update-URL: `http://contoso.com/extension_updates.php`
    *   Version: `1.1`  
*   Erweiterung 2  
    *   ID: `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb`  
    *   Update-URL: `http://contoso.com/extension_updates.php`
    *   Version: `0.4`  


Im Folgenden sind die Anforderungen zum Aktualisieren jeder Erweiterung zu finden.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

Sie können auch mehrere Erweiterungen in einer einzigen Anforderung für jede eindeutige Update-URL auflisten.  Im folgenden Beispiel werden die vorherigen Anforderungen in einer einzigen Anforderung zusammengeführt.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

Wenn Sie eine einzelne Anforderung senden und die Anzahl der installierten Erweiterungen, die dieselbe Update-URL verwenden, zu lang ist, werden bei der Updateüberprüfung weitere Anforderungen `GET` gestellt.  Eine `GET` Anforderungs-URL ist zu lang, wenn sie ungefähr 2000 Zeichen lang ist.  

> [!NOTE]
> In Zukunft kann eine einzelne `POST` Anforderung mehrere Anforderungen `GET` ersetzen.  Die `POST` Anforderung kann die Anforderungsparameter im `POST` Textkörper enthalten.  

## <a name="advanced-usage-minimum-browser-version"></a>Erweiterte Verwendung: Minimale Browserversion  

Als neue APIs-Version für das Microsoft Edge können Sie eine aktualisierte Version Ihrer Erweiterung oder App veröffentlichen, die nur mit neueren versionen Microsoft Edge kann.  Wenn Microsoft Edge automatisch aktualisiert wird, kann es einige Tage dauern, bis die meisten Benutzer auf diese neue Version aktualisieren.  Um sicherzustellen, dass ein bestimmtes Update nur für Microsoft Edge versionen gilt, die aktuell oder neuer als eine bestimmte Version sind, fügen Sie das `prodversionmin` Attribut in Ihrem Updatemanifest hinzu.  Im folgenden Codeausschnitt gibt der Attributwert von an, dass Ihre App automatisch auf die Version aktualisiert wird, wenn der Benutzer Microsoft Edge `prodversionmin` `3.0.193.0` oder neuer ausgeführt `2.0` `3.0.193.0` wird.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[ExtensionsPublishUpdateExtension]: ../publish/update-extension.md "Aktualisieren oder Entfernen Der Erweiterungs-| Microsoft Docs"  

[MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/docs/apps/autoupdate).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
