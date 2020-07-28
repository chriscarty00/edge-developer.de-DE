---
title: Zugreifen auf lokale Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: daa96b604d5ad48a9de49dd24dc38eab79de9c9b
ms.sourcegitcommit: ad5eb43172280974b8c063867c2097f7c5c0e77d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2020
ms.locfileid: "10898214"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Zugreifen auf lokale Server   




Hosten Sie eine Website auf einem Entwicklungscomputer-Webserver, und greifen Sie dann auf den Inhalt eines Android-Geräts zu.  

Führen Sie mit einem USB-Kabel und Microsoft Edge devtools eine Website von einem Entwicklungscomputer aus, und zeigen Sie dann die Website auf einem Android-Gerät an.  

### Zusammenfassung  

*   Mit der Port Weiterleitung können Sie Inhalte anzeigen, die von dem Webserver gehostet werden, der auf Ihrem Android-Gerät auf Ihrem Entwicklungscomputer ausgeführt wird.  
*   Wenn Ihr Webserver eine benutzerdefinierte Domäne verwendet, richten Sie Ihr Android-Gerät für den Zugriff auf den Inhalt dieser Domäne mit benutzerdefinierter Domänenzuordnung ein.  

## Einrichten der Portweiterleitung   

Mit der Port Weiterleitung kann Ihr Android-Gerät auf Inhalte zugreifen, die auf dem Webserver gehostet werden, der auf Ihrem Entwicklungscomputer ausgeführt wird.  Die Port Weiterleitung funktioniert durch Erstellen eines abhörenden TCP-Ports auf Ihrem Android-Gerät, der einem TCP-Port auf dem Entwicklungscomputer zugeordnet ist.  Der Datenverkehr zwischen den Anschlüssen durchläuft die USB-Verbindung zwischen Ihrem Android-Gerät und dem Entwicklungscomputer, sodass die Verbindung nicht von Ihrer Netzwerkkonfiguration abhängt.  

So aktivieren Sie die Portweiterleitung:  

1.  Richten Sie das [Remotedebuggen][RemoteDebuggingGettingStarted] zwischen Ihrem Entwicklungscomputer und Ihrem Android-Gerät ein.  Wenn Sie den Vorgang beenden, sollten Sie Ihr Android-Gerät im linken Menü des Dialogfelds " **Geräte prüfen** " und einer **verbundenen** Statusanzeige sehen.  
1.  Aktivieren Sie im Dialogfeld **Geräte prüfen** in devtools die **Port Weiterleitung**.  
1.  Wählen Sie **Regel hinzufügen**aus.  
    
    > ##### Abbildung1  
    > Hinzufügen einer Port Weiterleitungsregel  
    > ![Hinzufügen einer Port Weiterleitungsregel][ImageAddRule]  
    
1.  Geben Sie im Textfeld **Device Port** auf der linken Seite die Portnummer ein, auf der `localhost` Sie auf Ihrem Android-Gerät auf die Website zugreifen können möchten.  Wenn Sie beispielsweise auf die Website von Enter aus zugreifen `localhost:5000` möchten `5000` .  
1.  Geben Sie im Textfeld **lokale Adresse** auf der rechten Seite die IP-Adresse oder den Hostnamen ein, auf dem Ihre Website auf dem Webserver gehostet wird, der auf Ihrem Entwicklungscomputer ausgeführt wird, gefolgt von der Portnummer.  Beispiel: Wenn Ihre Website auf Enter ausgeführt wird `localhost:7331` `localhost:7331` .  
1.  Wählen Sie **Hinzufügen** aus.  

Die Port Weiterleitung ist nun eingerichtet.  Sehen Sie sich die Statusanzeige für den Port Forward auf der Registerkarte auf Ihrem Gerät im Dialogfeld " **Geräte überprüfen** " an.  

> ##### Abbildung2  
> Port Weiterleitungsstatus  
> ![Port Weiterleitungsstatus][ImagePortForwardingStatus]  

Wenn Sie den Inhalt anzeigen möchten, öffnen Sie Microsoft Edge auf Ihrem Android-Gerät, und wechseln Sie zu dem `localhost` Port, den Sie im Feld **Device Port** festgelegt haben.  Wenn Sie beispielsweise `5000` in das Feld eingegeben haben, besuchen Sie `localhost:5000` .  

## Zuordnen zu benutzerdefinierten lokalen Domänen   

Mit der benutzerdefinierten Domänenzuordnung können Sie Inhalte auf einem Android-Gerät von einem Webserver auf dem Entwicklungscomputer anzeigen, auf dem eine benutzerdefinierte Domäne verwendet wird.  

Nehmen wir beispielsweise an, dass Ihre Website eine JavaScript-Bibliothek eines Drittanbieters verwendet, die nur in der Domäne funktioniert `microsoft-edge.devtools` .  So erstellen Sie einen Eintrag in Ihrer `hosts` Datei auf Ihrem Entwicklungscomputer, um diese Domäne an `localhost` \ (beispielsweise `127.0.0.1 microsoft-edge.devtools` \) zuzuordnen.  Nachdem Sie die benutzerdefinierte Domänenzuordnung und Portweiterleitung eingerichtet haben, können Sie die Website auf Ihrem Android-Gerät unter der URL anzeigen `microsoft-edge.devtools` .  

### Einrichten der Portweiterleitung an Proxy Server  

Wenn Sie eine benutzerdefinierte Domäne zuordnen möchten, müssen Sie einen Proxy Server auf Ihrem Entwicklungscomputer ausführen.  Beispiele für Proxy Server sind [Charles][CharlesWebDebuggingProxy], [squid][SquidOptimisingWebDelivery]und [Fiddler][FiddlerWebDebuggingProxy].  

So richten Sie die Portweiterleitung an einen Proxy ein:  

1.  Führen Sie den Proxy Server aus, und notieren Sie den verwendeten Port.  
    
    > [!NOTE]
    > Der Proxy Server und Ihr Webserver müssen auf unterschiedlichen Ports ausgeführt werden.  
    
1.  Richten Sie die [Portweiterleitung](#set-up-port-forwarding) auf Ihr Android-Gerät ein.  Geben Sie für das Feld **lokale Adresse** `localhost:` den Port ein, auf dem Ihr Proxy Server ausgeführt wird.  Wenn Sie beispielsweise auf Port ausgeführt wird `8000` , besuchen Sie `localhost:8000` .  Geben Sie im Feld **Device Port** die Nummer ein, die Ihr Android-Gerät hören soll, beispielsweise `3333` .  

### Konfigurieren von Proxyeinstellungen auf Ihrem Gerät  

Als nächstes müssen Sie Ihr Android-Gerät für die Kommunikation mit dem Proxy Server konfigurieren.  

1.  Wechseln Sie auf Ihrem Android-Gerät zu **Einstellungen**  >  **Wi-Fi**.  
1.  Lange – drücken Sie den Namen des Netzwerks, mit dem Sie gerade verbunden sind.  
    
    > [!NOTE]
    > Proxy Einstellungen gelten pro Netzwerk.  
    
1.  Wählen Sie **Netzwerk ändern**aus.  
1.  Wählen Sie **Erweiterte Optionen**aus.  Die Proxyeinstellungen werden angezeigt.  
1.  Wählen Sie das **Proxy** -Menü und dann **manuell**aus.  
1.  Geben Sie für das Feld **Proxy Hostname** ein `localhost` .  
1.  Geben Sie im Feld **Proxy Port** die Portnummer ein, die Sie im vorherigen Abschnitt für den **Geräteanschluss** eingegeben haben.  
1.  Wählen Sie **Speichern**.  

Mit diesen Einstellungen leitet Ihr Gerät alle seine Anforderungen an den Proxy auf dem Entwicklungscomputer weiter.  Der Proxy stellt Anforderungen für Ihr Gerät, damit Anforderungen an Ihre angepasste lokale Domäne ordnungsgemäß aufgelöst werden.  

Auf Ihrem Android-Gerät können Sie nun auf benutzerdefinierte Domänen zugreifen, genau wie auf dem Entwicklungscomputer.  

Wenn Ihr Webserver von einem nicht standardmäßigen Port ausgeführt wird, denken Sie daran, den Port anzugeben, wenn Sie den Inhalt von Ihrem Android-Gerät anfordern.  Wenn Ihr Webserver beispielsweise die benutzerdefinierte Domäne `microsoft-edge.devtools` am Port verwendet `7331` , sollten Sie die URL verwenden, wenn Sie die Website von Ihrem Android-Gerät aus anzeigen `microsoft-edge.devtools:7331` .  

> [!TIP]
> Wenn Sie das normale Browsen fortsetzen möchten, denken Sie daran, die Proxyeinstellungen auf Ihrem Android-Gerät zurückzusetzen, nachdem Sie die Verbindung mit dem Entwicklungscomputer getrennt haben.  

<!--  -->  



<!-- image links -->  

[ImageAddRule]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png "Abbildung 1: Hinzufügen einer Port Weiterleitungsregel"  
[ImagePortForwardingStatus]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png "Abbildung 2: Port Weiterleitungsstatus"  

<!-- links -->  

[RemoteDebuggingGettingStarted]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Erste Schritte mit dem Remote Debuggen von Android-Geräten"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Charles Web Debugging-Proxy"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: Optimieren der Web-Zustellung"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler-Free Web Debugging Proxy"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite wird [hier](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) gefunden und von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) und [Meggin Kearney][MegginKearney] \ (Tech Writer \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
