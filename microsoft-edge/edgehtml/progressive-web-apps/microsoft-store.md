---
description: Erreichen Sie die Welt von Windows 10-Kunden, indem Sie Ihre PWA über den Microsoft Store verteilen.
title: Progressive Web-Apps im Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Progressive Web-Apps, PWA, Edge, Windows, Microsoft Store, Bing PWA-Index
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dae25bcdf37a2496e181ab915d1686fe5d3a4985
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233894"
---
# Progressive Web-Apps im Microsoft Store

Wenn Sie Ihre Progressive Web App (PWA) im [Microsoft Store](https://developer.microsoft.com/store)veröffentlichen, wird Ihre potenzielle App-Zielgruppe auf die gesamte Windows 10-Installationsbasis von fast 700 Millionen aktiven monatlichen Benutzern erweitert! 

PWAs im Microsoft Store bieten eine Reihe von Vorteilen:

-   **Auffindbarkeit** – apps im Microsoft Store werden über verschiedene Kategorien, kuratierte Sammlungen und Suchfilter bereitgestellt, die eine einfache Browsing-und Einkaufserfahrung für potenzielle Kunden Ihrer APP bieten. Sie können Ihren Store-Eintrag sogar mit Screenshots, einem heldenbild und Video Trailern [verbessern](/windows/uwp/publish/app-screenshots-and-images) !
-   **Vertrauenswürdigkeit** – Windows-Kunden wissen, dass Sie Ihren Microsoft Store-Käufen und-Downloads vertrauen können, da Sie den strengen [Qualitäts-und Sicherheitsstandards](/legal/windows/agreements/store-policies)von Microsoft entsprechen.
-   **Einfache Installation** – der Microsoft Store bietet eine konsistente und benutzerfreundliche Installationsumgebung für [alle Windows 10-apps](https://www.microsoft.com/store/apps/windows?icid=CNavAppsWindowsApps), was es allen Kunden ermöglicht, ihre PWA unabhängig vom technischen Komfort zu installieren.
-   **Business Insights** – das [Windows dev Center-Dashboard](/windows/uwp/publish/using-the-windows-dev-center-dashboard) für den Microsoft Store bietet Ihnen [detaillierte Analysen](/windows/uwp/publish/analytics) zu allem, was davon abgeht, wie viele Windows-Kunden ihre PWA-Anwendung erreicht hat und was Sie zu sagen haben. Sie können auch Metriken und Telemetrie-Daten zu app-Integrität, anzeigen Nutzung und vieles mehr finden.
    
Es gibt zwei Möglichkeiten zum Abrufen ihrer PWA in den Microsoft Store:

1.  Sie können [es manuell übermitteln](#submitting-your-pwa-manually)oder
2.  Wenn Ihre PWA [bestimmte Kriterien](#criteria-for-automatic-submission)erfüllt, kann Sie automatisch vom Bing Web Crawler [indiziert](#automatic-pwa-importing-with-bing) werden. (Sie haben auch die Möglichkeit, die automatische Übermittlung [abzulehnen](#opting-out-of-automatic-microsoft-store-import) .)
    
Unabhängig von der Übermittlungsmethode erhalten Sie Zugriff auf alle oben beschriebenen Vorteile, sobald Ihre PWA im Microsoft Store angenommen wurde.

## Manuelles übermitteln ihrer PWA

Um eine APP über den Microsoft Store zu verteilen und zu bewerben, müssen Sie Sie als Windows-App-Paket (*AppX* -Datei) übermitteln.  Für Server gehostete Web-Apps wie PWAs enthält dieses Paket einfach App-Metadaten und Symbole für den Startbildschirm (und keinen eigentlichen Anwendungscode). Damit kann Ihre Web-App zusammen mit anderen [Windows 10-apps](/windows/uwp/get-started/whats-a-uwp) auf dem Startbildschirm installiert und gestartet werden, indem Sie in einem einfachen, systemeigenen App-Wrapper (*WWAHost.exe* Prozess) ausgeführt wird, unabhängig vom Microsoft Edge-Browserfenster.  

> [!IMPORTANT]
> Das EdgeHTML Web Platform-Modul wird vom WWAHost-App-Wrapper verwendet, der Kompatibilitätsunterschiede für Ihre auf Chrom basierende Microsoft Edge-basierte PWA-Anwendung einführen kann.  Stellen Sie sicher, dass Sie einen vollständigen TestPass für Ihre Anwendung mit Microsoft Edge (EdgeHTML) durchführen, bevor Sie Ihre APP an den Microsoft Store übermitteln, da das EdgeHTML-Modul nicht mehr mit neueren Webstandards aktualisiert wird.  

Gehen Sie dazu wie folgt vor:

### Voraussetzungen

-   **Eine vorhandene PWA**. Hier erfahren Sie, wie Sie [Ihre Web-App in eine PWA-Datei umwandeln,](./get-started.md) Wenn Sie noch nicht vorhanden ist. 
-   **Ein Windows APPX-Paket Tool für PWAs**. Hier erfahren Sie, wie [Sie Ihre PWA unter Windows mit Visual Studio erstellen und ausführen](./windows-features.md) . Sie können auch den [PWA-Generator](https://www.pwabuilder.com/) verwenden, um ein Windows-Paket zu erstellen.
-   [**Microsoft Store-App-Entwicklerkonto**](/windows/uwp/publish/opening-a-developer-account) Je nach gewähltem Kontotyp und Standort gibt es eine [einmalige Gebühr](/windows/uwp/publish/account-types-locations-and-fees) , und für die Registrierung ist ein gültiges [Microsoft-Konto](https://account.microsoft.com/)erforderlich.
    
### Speichern der Übermittlung über *Visual Studio* 

Führen Sie die folgenden Schritte aus, um [eine APP-Paket-Uploaddatei](/windows/uwp/packaging/packaging-uwp-apps#create-an-app-package-upload-file) für Ihre PWA-Datei in Visual Studio zu erstellen. Eine allgemeinere Übersicht über diesen Prozess finden Sie unter [*Verpacken einer UWP-App mit Visual Studio*](/windows/uwp/packaging/packaging-uwp-apps) .

Die Anweisungen führen Sie auch durch Ausführen des [**Windows-App-zertifizierungskits**](https://developer.microsoft.com/windows/develop/app-certification-kit) , um Ihre APP auf die Einhaltung der Microsoft Store-Anforderungen zu testen. Dies ist optional, wird aber dringend empfohlen.

### Speichern der Übermittlung über das *Windows dev Center*

Hier erfahren Sie, wie Sie mithilfe des *PWA-Generators* ein App-Paket für den Upload in das Windows dev Center erstellen.

1.  Generieren Sie Ihre Windows 10-app. Hier erfahren Sie, wie Sie Ihre [PWA als Windows-App mit Visual Studio](./windows-features.md)ausführen. Sie können auch den [PWA-Generator](https://www.pwabuilder.com/) verwenden, um Ihre Windows 10-APP zu generieren.
2.  Reservieren Sie Ihren APP-Namen für den Microsoft Store, indem Sie sich beim [Windows dev Center-Dashboard](https://developer.microsoft.com/dashboard/windows/overview) mit Ihren Kontoinformationen anmelden und die Schritte zum Erstellen der app ausführen, [indem Sie einen Namen](/windows/uwp/publish/create-your-app-by-reserving-a-name)reservieren. Jeder reservierter Name muss im gesamten Microsoft Store eindeutig sein.
3.  Wenn Sie die Pakete Ihrer APP hochladen, müssen die Werte für *Display*Name, *Name*, *Publisher*und *PublisherDisplayName* in Ihrer *appxmanifest* -Datei mit den Werten übereinstimmen, die Ihrer APP im Windows dev Center-Dashboard bei der Beibehaltung des Namens zugewiesen sind. 
    
    Melden Sie sich beim [Windows dev Center-Dashboard](https://developer.microsoft.com/dashboard/windows/overview)an, und suchen Sie die APP-Identitätswerte unter **App-Verwaltungs**-  >  **App-Identität**:
    
    ![Windows dev Center-Dashboard, Einstellungen für die APP-Identität](./media/dashboard-app-identity.png)
    
    Suchen Sie dann `appxmanifest.xml` die Datei, und ersetzen Sie die folgenden Werte durch diejenigen, die im Windows dev Center-Dashboard zugewiesen sind:
    
    -   **<Identity Name = "** *Paket/Identität/Name*
    -   **<Identity Publisher = "** *Paket/Identität/Herausgeber*
    -   **<DisplayName** **>** *Der Name, den Sie für Ihre APP reserviert haben* 
    -   **<PublisherDisplayName** **>** *Paket/Eigenschaften/PublisherDisplayName***</PublisherDisplayName>**
        
4.  Jetzt sind Sie bereit, alle Ihre PWA-Ressourcen in einer einzigen `.appx` Datei zu kompilieren, die Sie in den Microsoft Store hochladen können. Navigieren Sie an einer Eingabeaufforderung zum Verzeichnis Ihres webmanifests, und erstellen Sie ein Windows 10-Paket (angegeben unter w/optionale Debug-Protokollierung):
    
    ```shell
    pwabuilder package -p windows10 -l debug
    ```  
    
    Ihre AppX-Datei wird an diesem Speicherort generiert: `PWA\Store packages\windows10\package\windows.appx` .
    
5.  Bevor Sie Ihre APP für submisison in den Microsoft Store hochladen, empfiehlt es sich, Ihre APP auf die Einhaltung der Microsoft Store-Richtlinien zu testen. Sie können dies tun, indem Sie das [**Windows-App-Zertifizierungs Kit**](https://developer.microsoft.com/windows/develop/app-certification-kit)herunterladen, es starten und dann die *AppX* -Datei Ihrer APP zum Testen auswählen. Sobald alle Tests abgeschlossen sind, erhalten Sie einen Bericht über die anzuwendenden Bereiche.
6.  Laden Sie Ihr Paket hoch, und führen Sie die Übermittlung durch, indem Sie sich wieder im [Windows dev Center-Dashboard](https://developer.microsoft.com/dashboard/windows/overview) anmelden und den Bereich über **mittlungen**  >  **Submisison 1** erweitern. Befolgen Sie die Checkliste, um die [erforderlichen Informationen zum Store-Eintrag](/windows/uwp/publish/app-submissions) abzuschließen und [Ihr App-Paket hochzuladen](/windows/uwp/publish/upload-app-packages).
    
Weitere Informationen zu allen Features und Diensten, die Microsoft Store-App-Entwicklern zur Verfügung stehen, finden Sie unter [*Veröffentlichen von Windows-apps*](https://developer.microsoft.com/store/publish-apps) im [Windows dev Center](https://developer.microsoft.com/windows).

## Automatischer PWA-Import mit Bing

Ebenso wie das Web- [App-Manifest](https://developer.mozilla.org/docs/Web/Manifest) ihrer PWA ein Signal für unterstützende Plattformen ist, dass Ihre APP offline ist und bereit ist, als vollständig integrierte App-Umgebung dargestellt zu werden, ist dies auch ein Hinweis für den Bing-Webcrawler, dass Ihre PWA für die automatische Inklusion in den Microsoft Store berücksichtigt werden sollte. 

Wenn Ihre PWA die folgenden Anforderungen erfüllt, wird der Bing-Indizierungsdienst ihre PWA automatisch im [*AppX*](#submitting-your-pwa-manually) -Format Verpacken, das für die Installation unter Windows 10 erforderlich ist, und die Store-Produktseite ihrer App basierend auf den Metadaten in Ihrem Web App-Manifest zusammenstellen. Nachdem Sie Ihre PWA-Anwendung beansprucht haben, können Sie Ihre Store-Seite weiter anpassen und über das Windows dev Center-Dashboard Zugriff auf die Benutzeranalyse und andere APP-Verwaltungstools erhalten.

### Kriterien für die automatische Übermittlung

Um automatisch verpackt und für den Microsoft Store aufgelistet zu werden, benötigt Ihre PWA:

-   Eine nicht leere Web App-Manifestdatei mit mindestens:
    
    -   Name
    -   Beschreibung
    -   App-Symbol mit mindestens 512 x 512 Pixeln
        
-   Eindeutige Kern Logik (nicht minimal geänderter Code aus einer [App-Standard](https://en.wikipedia.org/wiki/Boilerplate_code) Vorlage)
-   Über eine sichere Verbindung (HTTPS) bereitgestellt werden
-   Dienst Worker-Skript (e)
-   Nicht gegen Gesetze oder [Microsoft Store-Richtlinien](/legal/windows/agreements/store-policies)verstoßen.
    
Wir werden nicht jede APP, die diese Kriterien erfüllt, aufnehmen, sondern Sie in unsere Überlegungen für Kandidaten einbeziehen, während wir unser Programm sukzessive erweitern.

### Deaktivieren des automatischen Microsoft Store-Imports

Ihre PWA kann den automatischen Import in den Microsoft Store deaktivieren, indem Sie eine `robots.txt` Datei, die Folgendes enthält:

```text
User-agent: bingbot
Disallow: /manifest.json
```  

Dadurch wird der Bing Web Crawler (Bingbot) dazu verleitet, Ihre Web-Manifestdatei für PWA-Indizierungs Zwecke zu ignorieren. Dies hat keinen Einfluss auf die Such Rangfolge Ihrer Website in Bings regulärem [webindizierungs Prozess](https://www.bing.com/webmaster/help/help-center-661b2d18).
