---
description: Machen Sie Ihre PWA durch Veröffentlichung im Microsoft Store besser auf entdeckungsfähiger
title: Veröffentlichen Ihrer Progressive Web App im Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: progressive Web-Apps, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 68471535446a2270a23b32205717da225fd9e4bf
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461521"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a>Veröffentlichen Ihrer Progressive Web App im Microsoft Store  

Die Veröffentlichung Ihrer Progressive Web App \(PWA\) im [Microsoft Store][WindowsUwpPublishIndex] bietet die folgenden Vorteile.  

:::row:::
   :::column span="1":::
      **Erkennbarkeit**  
   :::column-end:::
   :::column span="2":::
      Benutzer suchen natürlich nach Apps im App Store.  Durch die Veröffentlichung im Microsoft Store können Millionen von Windows-Benutzern Ihre PWA zusammen mit anderen Windows-Apps ermitteln.  Im Store werden Apps über Kategorien, kuratierte Sammlungen und vieles mehr angezeigt.  Die App-Discovery-Portale bieten potenziellen Benutzern Ihrer App ein einfaches Browsen und Einkaufserlebnis.  Sie können Ihren [Store-Eintrag sogar][WindowsUwpPublishAppScreenshotsImages] um Screenshots, ein Heldenbild und Videotrailer erweitern.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Vertrauenswürdigkeit**  
   :::column-end:::
   :::column span="2":::
      Windows-Kunden wissen, dass sie ihren Microsoft Store-Käufen und Downloads vertrauen können, da sie die strengen [Microsoft-Qualitäts- und Sicherheitsstandards einhalten.][LegalWindowsAgreementsStorePolicies]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Einfache Installation**  
   :::column-end:::
   :::column span="2":::
      Der Microsoft Store bietet eine konsistente und benutzerfreundliche Installationserfahrung in [allen Windows 10-Apps.][MicrosoftStoreAppsWindows]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **App-Analyse**  
   :::column-end:::
   :::column span="2":::
      Das [Windows Partner Center-Dashboard][WindowsUwpPublishIndex] bietet Ihnen [detaillierte][WindowsUwpPublishAnalytics] Analysen zu Ihrer App-Integrität, -Nutzung und vielem mehr.  
   :::column-end:::
:::row-end:::  

Um Ihre PWA im Microsoft Store zu veröffentlichen, sind keine Codeänderungen erforderlich.  Stattdessen erstellen Sie eine App-Reservierung, packen Ihre PWA und übermitteln Ihr Paket an den Store.  In den folgenden Abschnitten werden die Schritte erläutert.   

## <a name="create-an-app-reservation"></a>Erstellen einer App-Reservierung  

[Windows Partner Center ist][MicrosoftPartnerDashboardWindowsOverview] der Hub, an dem Sie Ihre App an den Microsoft Store übermitteln können.  

Führen Sie die folgenden Aktionen aus, um eine App-Reservierung zu erstellen.  

1.  Führen Sie die folgenden Aktionen aus, um die registrierten Programme anzeigen zu können.  
    1.  Melden Sie sich mit Ihrem Microsoft-Konto beim Windows Partner Center an, und navigieren Sie zum [Partner Center Dashboard][MicrosoftPartnerDashboardHome].  
    1.  Navigieren zu **Windows & Xbox**  
        *   Wenn **Windows & Xbox** angezeigt wird, ist Ihre App bereits registriert.  
        *   Wenn **Windows & Xbox** nicht angezeigt wird, wählen Sie Programm hinzufügen **aus.**  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Hinzufügen eines Programms im Windows Partner Center-Dashboard" lightbox="./media/windows-partner-center-add-program.msft.png":::
       Hinzufügen eines Programms im Windows Partner Center-Dashboard
    :::image-end:::  
    
1.  Führen Sie die folgenden Aktionen aus, um sich beim Entwicklerprogramm zu registrieren.  
    1.  Navigieren Sie **zu Windows & Xbox**.  
    1.  Wählen **Sie Erste Schritte aus.**  
    1.  Befolgen Sie die Anweisungen.  
1.  Jetzt ist Ihre App im App-Entwicklerprogramm registriert. Führen Sie die folgenden Aktionen aus, um eine App-Reservierung zu erstellen.  
    1.  Navigieren Sie **zu Windows & Xbox**.  
    1.  Wählen **Sie Übersicht**Erstellen einer neuen App  >  **aus.**  
    1.  Geben Sie ihren PWA-Namen in die Eingabeaufforderung ein.  
    1.  Wählen Sie `Reserve product name` aus.  
    
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Erstellen einer App-Reservierung im Windows Partner Center" lightbox="./media/windows-partner-center-create-app.msft.png":::
       Erstellen einer App-Reservierung im Windows Partner Center  
    :::image-end:::  

1.  Wählen Sie **Produktverwaltung**Produktidentität aus, um Ihre Herausgeberdetails für die Verwendung im Abschnitt [Paket Ihres PWA](#package-your-pwa)  >  **anzuzeigen.**  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Kopieren von Herausgeberinformationen aus Windows Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       Kopieren von Herausgeberinformationen aus Windows Partner Center  
    :::image-end:::  

1.  Kopieren und speichern Sie die folgenden Werte.  
    *   **Paket-ID**  
    *   **Herausgeber-ID**  
    *   **Publisher-Anzeigename**  
        
## <a name="package-your-pwa"></a>Packen Ihres PWA  

Generieren Sie ein Windows-App-Paket für Ihre PWA.  

Das App-Paket ist eine Datei, die die Metadaten Ihrer App enthält, einschließlich `.msixbundle` Name, Beschreibung, Symbolen und so weiter.  Es verwendet das [gehostete App-Modell,][WindowsBlogWindowsdeveloperHostedAppModel]und Microsoft Edge unterstützt Ihre PWA.  In diesem Modell verwendet Ihre PWA moderne Webfunktionen, während sie als Windows-App funktioniert.  Zu den modernen Webfunktionen gehören Service worker, offline, Pushbenachrichtigungen, Badging und vieles mehr.  

Führen Sie die folgenden Aktionen aus, um ein App-Paket zu generieren.  

1.  Navigieren Sie zu [PWA Builder][PwabuilderMain].  
1.  Geben Sie die URL Ihres PWA ein.  
1.  Wählen **Sie Start**Build My  >  **PWA**  >  **Windows**Options  >  **aus.**  
1.  Fügen Sie die folgenden Werte ein, die Sie im Abschnitt [Erstellen einer App-Reservierung gespeichert](#create-an-app-reservation) haben.  
    *   **Paket-ID**  
    *   **Herausgeber-ID**  
    *   **Publisher-Anzeigename**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Einfügen von Herausgeberinformationen in PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       Einfügen von Herausgeberinformationen in PWABuilder  
    :::image-end:::  
    
1.  Wählen Sie **Fertig**aus.  
1.  Wenn Sie Ihr Windows-App-Paket herunterladen möchten, wählen Sie **Herunterladen aus.**  Ihr Download ist ein `.zip` Archiv mit einer `.msixbundle` Datei.  Verwenden Sie `.msixbundle` die Datei im Abschnitt Senden Ihres [App-Pakets an den Store.](#submit-your-app-package-to-the-store)  

### <a name="submit-your-app-package-to-the-store"></a>Übermitteln Ihres App-Pakets an den Store  

Jetzt haben Sie Ihr `.msixbundle` App-Paket.  Führen Sie die folgenden Aktionen aus, um Ihr App-Paket an den Store zu übermitteln.  

1.  Navigieren zu [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] 
1.  Wählen Sie Ihre App aus.  
1.  Wählen **Sie Übermittlung starten aus.**  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Starten einer neuen App-Übermittlung im Windows Partner Center" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       Starten einer neuen App-Übermittlung im Windows Partner Center  
    :::image-end:::  
    
1.  Führen Sie die folgenden Eingabeaufforderungen für Informationen zu Ihrer App aus.
    *   pricing  
    *   Altersfreigabe  
    *   und mehr  
        
1.  Wählen Sie **in der Paketaufforderung** die Datei aus, die Sie `.msixbundle` im Abschnitt Paket Ihren [PWA generiert](#package-your-pwa) haben.  

Nachdem Sie ihre Übermittlung abgeschlossen haben, wird Ihre App in der Regel innerhalb von 24 bis 48 Stunden überprüft.  Nachdem Sie die Genehmigung erhalten haben, ist Ihr PWA im Microsoft Store verfügbar.  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store-Richtlinien | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analysieren der Leistung | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "App-Screenshots, Bilder und Trailer | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Veröffentlichen von Windows-Apps und | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Startseite | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Ressourcen für Partner| Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Hosted App Model | Windows-Entwicklerblog"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  

