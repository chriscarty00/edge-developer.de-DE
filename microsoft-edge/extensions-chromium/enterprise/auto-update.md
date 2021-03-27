---
description: Informationen zu automatischen Updates für Erweiterungen in Microsoft Edge
title: Erweiterungen für automatische Updates in Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, Erweiterungenentwicklung, Browsererweiterungen, Add-Ons, Partner Center, Entwickler
ms.openlocfilehash: 0f3f140cd3a2a079cd09f4d61e46a420342e15e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461528"
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
# <a name="auto-update-extensions-in-microsoft-edge"></a>Erweiterungen für automatische Updates in Microsoft Edge  

Das automatische Aktualisieren von Erweiterungen bietet einige der gleichen Vorteile wie die automatische Aktualisierung von Microsoft Edge:   

*   Integrieren sie Fehler- und Sicherheitsbehebungen.  
*   Fügen Sie neue Features oder Leistungsverbesserungen hinzu.  
*   Verbessern Sie die Benutzeroberfläche.  

Früher, als nicht speicherbasierte Erweiterungen unterstützt wurden, konnten die systemeigenen Binärdateien und die Erweiterung gleichzeitig aktualisiert werden.  Jetzt werden diese Erweiterungen im Microsoft Edge-Add-Ons-Speicher gehostet, und Updates werden mit demselben Mechanismus vorgenommen, den Microsoft Edge verwendet, den Sie nicht steuern können.  Beim Aktualisieren von Erweiterungen, die von systemeigenen Binärdateien abhängig sind, sollten Sie vorsichtig sein.  

> [!NOTE]
> Dieses Thema gilt nicht für Erweiterungen, die über das [Partner Center-Dashboard veröffentlicht][MicrosoftPartnerCenter] wurden.  Sie können das Dashboard verwenden, um aktualisierte Versionen für Ihre Benutzer und für den Microsoft Edge-Add-Ons-Speicher zu veröffentlichen.

## <a name="overview"></a>Übersicht  

Alle paar Stunden überprüft Microsoft Edge, ob jede installierte Erweiterung oder App über eine Update-URL verfügt.  Erweiterungen können mithilfe des Felds im Manifest eine Update-URL angeben, die auf einen Speicherort `update_url` verweist, um eine Aktualisierungsprüfung durchzuführen.  Für jeden `update_url` sendet er Anforderungen für aktualisierte Manifest-XML-Dateien.  Wenn in der Updatemanifest-XML-Datei eine neuere Version als die installierte aufgeführt ist, lädt Microsoft Edge die neuere Version herunter und installiert sie.  Der gleiche Prozess funktioniert für manuelle Updates, bei denen die neue Datei mit demselben privaten Schlüssel wie die aktuell installierte `.crx` Version signiert werden muss.  

> [!NOTE]
> Um den Datenschutz der Benutzer zu gewährleisten, sendet Microsoft Edge keine Kopfzeilen mit Manifestanforderungen für automatische Updates und ignoriert alle Kopfzeilen in den Antworten `Cookie` `Set-Cookie` auf diese Anforderungen.  

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
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
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

Der grundlegende Mechanismus für die automatische Aktualisierung ist so einfach wie das Ablegen einer statischen XML-Datei auf einem Beliebigen Webserver wie Apache und das Aktualisieren der XML-Datei, wenn Sie neue Versionen Ihrer Erweiterungen veröffentlichen.  

Sie können die Tatsache nutzen, dass der Updatemanifestanforderung Parameter hinzugefügt werden, die die Erweiterungs-ID und Version angeben. Sie können die gleiche Update-URL für alle Erweiterungen anstelle einer statischen XML-Datei verwenden.  Um dieselbe Update-URL für alle Erweiterungen zu verwenden, zeigen Sie auf eine URL, auf der dynamischer serverseitiger Code ausgeführt wird, um diese Parameter zu testen.  

Im folgenden Beispiel wird das Format der Anforderungsparameter der Update-URL veranschaulicht: `?x={extension_data}` .

In diesem Beispiel `{extension_data}` handelt es sich um eine URL-codierte Zeichenfolge, die das folgende Format verwendet: `id={id}&v={version}` .

Die folgenden beiden Erweiterungen verweisen beispielsweise beide auf die gleiche Update-URL `http://contoso.com/extension_updates.php` .  

*  Erweiterung 1 - ID: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa" Version: "1.1"
*  Erweiterung 2 - ID: "bbbbbbbbbbbbbbbbbbbbbbbbbb" Version: "0,4"


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

Als neue APIs-Version für das Microsoft Edge-Erweiterungssystem können Sie eine aktualisierte Version Ihrer Erweiterung oder App veröffentlichen, die nur mit neueren Microsoft Edge-Versionen funktioniert.  Wenn Microsoft Edge automatisch aktualisiert wird, kann es einige Tage dauern, bis die meisten Benutzer auf diese neue Version aktualisieren.  Um sicherzustellen, dass ein bestimmtes Update nur für Microsoft Edge-Versionen gilt, die aktuell oder neuer als eine bestimmte Version sind, fügen Sie das `prodversionmin` Attribut in Ihrem Updatemanifest hinzu.  Im folgenden Codeausschnitt gibt der Attributwert von an, dass Ihre App nur dann automatisch auf die Version aktualisiert wird, wenn der Benutzer Microsoft Edge oder neuer `prodversionmin` `3.0.193.0` ausgeführt `2.0` `3.0.193.0` hat.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite finden Sie [hier](https://developer.chrome.com/docs/apps/autoupdate/).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
