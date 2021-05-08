---
description: Hosten Sie eine Website auf einem Webserver des Entwicklungscomputers, und greifen Sie dann über ein Android-Gerät auf die Inhalte zu.
title: Zugreifen auf lokale Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 51ef0d951d587d310b6474698924d9f87cf68607
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461262"
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
# <a name="access-local-servers"></a>Zugreifen auf lokale Server  

Hosten Sie eine Website auf einem Webserver des Entwicklungscomputers, und greifen Sie dann von einem Android-Gerät auf die Inhalte zu.  

Führen Sie mit einem MICROSOFT EDGE devTools eine Website von einem Entwicklungscomputer aus aus, und zeigen Sie die Website dann auf einem Android-Gerät an.  

### <a name="summary"></a>Zusammenfassung  

*   Mit der Port weiterleitung können Sie Inhalte anzeigen, die vom Webserver auf Ihrem Entwicklungscomputer auf Ihrem Android-Gerät gehostet werden.  
*   Wenn Ihr Webserver eine benutzerdefinierte Domäne verwendet, richten Sie Ihr Android-Gerät ein, um mit benutzerdefinierter Domänenzuordnung auf den Inhalt dieser Domäne zu zugreifen.  

## <a name="set-up-port-forwarding"></a>Einrichten der Port weiterleitung  

Die Port weiterleitung ermöglicht Ihrem Android-Gerät den Zugriff auf Inhalte, die auf dem Webserver gehostet werden, der auf Ihrem Entwicklungscomputer ausgeführt wird.  Die Port weiterleitung funktioniert, indem sie einen lauschenden TCP-Port auf Ihrem Android-Gerät erstellt, der einem TCP-Port auf Ihrem Entwicklungscomputer zuteil wird.  Der Datenverkehr zwischen den Ports wird über die USB-Verbindung zwischen Ihrem Android-Gerät und dem Entwicklungscomputer übertragen, sodass die Verbindung nicht von Ihrer Netzwerkkonfiguration abhängig ist.  

So aktivieren Sie die Port weiterleitung:  

1.  Einrichten des [Remotedebu debuggings][RemoteDebuggingGettingStarted] zwischen Ihrem Entwicklungscomputer und Ihrem Android-Gerät.  Wenn Sie fertig sind, sollte Ihr Android-Gerät im linken **** Menü des Dialogfelds Geräte überprüfen und eine Statusanzeige **verbunden** angezeigt werden.  
1.  Aktivieren Sie **im Dialogfeld Geräte** überprüfen in DevTools port **forwarding**.  
1.  Wählen Sie **Add rule**aus.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Hinzufügen einer Port weiterleitungsregel" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Hinzufügen einer Port weiterleitungsregel  
    :::image-end:::  
    
1.  Geben Sie im Textfeld **Geräteport** auf der linken Seite die Portnummer ein, von der aus Sie auf die Website auf Ihrem `localhost` Android-Gerät zugreifen möchten.  Wenn Sie z. B. über die Eingabe auf die Website `localhost:5000` zugreifen `5000` möchten.  
1.  Geben Sie **im** Textfeld Lokale Adresse auf der rechten Seite die IP-Adresse oder den Hostnamen ein, auf dem Ihre Website auf dem Webserver gehostet wird, der auf dem Entwicklungscomputer ausgeführt wird, gefolgt von der Portnummer.  Wenn Ihre Website z. B. bei der Eingabe `localhost:7331` ausgeführt `localhost:7331` wird.  
1.  Wählen Sie **Hinzufügen**.  
    
Die Port weiterleitung ist jetzt eingerichtet.  Überprüfen Sie die Statusanzeige für den Port vorwärts auf der Registerkarte ihres Geräts im Dialogfeld **Geräte** überprüfen.  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Status der Port weiterleitung" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   Status der Port weiterleitung  
:::image-end:::  

Öffnen Sie zum Anzeigen des Inhalts Microsoft Edge auf Ihrem Android-Gerät, und wechseln Sie zu dem Port, den Sie im Feld `localhost` **Geräteport angegeben** haben.  Wenn Sie z. B. `5000` in das Feld eingegeben haben, besuchen Sie `localhost:5000` .  

## <a name="map-to-custom-local-domains"></a>Zuordnung zu benutzerdefinierten lokalen Domänen  

Mit der benutzerdefinierten Domänenzuordnung können Sie Inhalte auf einem Android-Gerät von einem Webserver auf Ihrem Entwicklungscomputer anzeigen, der eine benutzerdefinierte Domäne verwendet.  

Angenommen, Ihre Website verwendet eine JavaScript-Bibliothek eines Drittanbieters, die nur in der Domäne `microsoft-edge.devtools` funktioniert.  Sie erstellen also einen Eintrag in Ihrer Datei auf dem Entwicklungscomputer, um diese Domäne `hosts` `localhost` \(z. B. `127.0.0.1 microsoft-edge.devtools` \) zu zuordnungen.  Nachdem Sie die benutzerdefinierte Domänenzuordnung und Port weiterleitung eingerichtet haben, zeigen Sie die Website auf Ihrem Android-Gerät unter der URL `microsoft-edge.devtools` an.  

### <a name="set-up-port-forwarding-to-proxy-server"></a>Einrichten der Port weiterleitung an den Proxyserver  

Zum Zuordnung einer benutzerdefinierten Domäne müssen Sie einen Proxyserver auf dem Entwicklungscomputer ausführen.  Beispiele für Proxyserver sind [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]und [Fiddler][FiddlerWebDebuggingProxy].  

So richten Sie die Port weiterleitung an einen Proxy ein:  

1.  Führen Sie den Proxyserver aus, und zeichnen Sie den verwendeten Port auf.  
    
    > [!NOTE]
    > Der Proxyserver und der Webserver müssen an unterschiedlichen Ports ausgeführt werden.  
    
1.  Richten Sie [die Port-Weiterleitung an](#set-up-port-forwarding) Ihr Android-Gerät ein.  Geben Sie **für das feld lokale** Adresse gefolgt vom Port ein, auf dem Der `localhost:` Proxyserver ausgeführt wird.  Wenn sie beispielsweise im Port ausgeführt `8000` wird, navigieren Sie zu `localhost:8000` .  Geben Sie **im Feld Geräteport** die Nummer ein, auf der Ihr Android-Gerät lauschen soll, z. B. `3333` .  
    
### <a name="configure-proxy-settings-on-your-device"></a>Konfigurieren von Proxyeinstellungen auf Ihrem Gerät  

Als Nächstes müssen Sie Ihr Android-Gerät für die Kommunikation mit dem Proxyserver konfigurieren.  

1.  Navigieren Sie auf Ihrem Android-Gerät zu **Einstellungen**  >  **WLAN.**  
1.  Drücken Sie lange den Namen des Netzwerks, mit dem Sie derzeit verbunden sind.  
    
    > [!NOTE]
    > Proxyeinstellungen gelten pro Netzwerk.  
    
1.  Wählen **Sie Netzwerk ändern aus.**  
1.  Wählen **Sie Erweiterte Optionen aus.**  Die Proxyeinstellungen werden angezeigt.  
1.  Wählen Sie das **Menü Proxy** aus, und wählen Sie **Manuell aus.**  
1.  Geben Sie **für das Feld Proxyhostname** `localhost` ein.  
1.  Geben Sie **für das Feld Proxyport** die Portnummer ein, die Sie im vorherigen Abschnitt für den **Geräteport** eingegeben haben.  
1.  Wählen Sie **Speichern**aus.  
    
Mit diesen Einstellungen gibt Ihr Gerät alle Anforderungen an den Proxy auf Ihrem Entwicklungscomputer weiter.  Der Proxy stellt Anforderungen im Auftrag Ihres Geräts, sodass Anforderungen an Ihre angepasste lokale Domäne ordnungsgemäß aufgelöst werden.  

Greifen Sie jetzt wie auf dem Entwicklungscomputer auf benutzerdefinierte Domänen auf Ihrem Android-Gerät zu.  

Wenn auf Ihrem Webserver ein nicht standardmäßiger Port ausgeführt wird, denken Sie daran, den Port anzugeben, wenn Sie den Inhalt von Ihrem Android-Gerät anfordern.  Wenn Ihr Webserver beispielsweise die benutzerdefinierte Domäne am Port verwendet, sollten Sie die URL verwenden, wenn Sie die Website von Ihrem `microsoft-edge.devtools` `7331` Android-Gerät aus `microsoft-edge.devtools:7331` anzeigen.  

> [!TIP]
> Denken Sie zum Fortsetzen des normalen Browsens daran, die Proxyeinstellungen auf Ihrem Android-Gerät wiederhergestellt zu haben, nachdem Sie die Verbindung mit dem Entwicklungscomputer getrennt haben.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Erste Schritte mit remote debuggen von Android-Geräten | Microsoft Docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Charles Web Debugging Proxy"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "squid : Optimieren der Webzustellung"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler – Free Web Debugging Proxy"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) befindet sich hier und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) und [Meggin Kearney][MegginKearney] \(Tech Writer\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
