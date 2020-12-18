---
description: Emulieren Sie Authentifikatoren, und Debuggen Sie webauthn in Microsoft Edge devtools.
title: Emulieren von Authentifikatoren und Debuggen von webauthn in Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 3200f22485bfd642a37a7d34ac727b8da4500d06
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231181"
---
# Emulieren von Authentifikatoren und Debuggen von webauthn in Microsoft Edge devtools  

Anstatt die Webauthentifizierung in Ihrer Website oder App mit physikalischen Authentifikatoren zu debuggen, verwenden Sie das **webauthn** -Tool in Microsoft Edge devtools, um softwarebasierte virtuelle Authentifikatoren zu erstellen und mit Ihnen zu interagieren.  

## Vorbemerkungen  

Die [Webauthentifizierungs-API-Spezifikation][GithubW3cWebauthn]eignet sich hervorragend für die ersten Schritte mit der Webauthentifizierung.  

## Einrichten des webauthn-Tools  

1.  Navigieren Sie zu einer Webseite, die webauthen verwendet, beispielsweise die folgende Demo-Website.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Registrieren Sie sich bei der Website.  
1.  [Öffnen Sie devtools][DevtoolsGuideChromiumOpen].  
1.  Um das **webauthn** -Tool zu öffnen, wählen Sie das Symbol **anpassen und Steuern devtools** \ ( `...` \) > **Weitere Tools**  >  **webauthn**aus.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Webauthn-Tool" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       **Webauthn** -Tool  
    :::image-end:::  
    
1.  Aktivieren Sie im **webauthn** -Tool das Kontrollkästchen **virtuelle Authentifikator-Umgebung aktivieren** .  
1.  Nach der Aktivierung wird ein neuer Abschnitt mit dem Namen **neuer Authentifikator** angezeigt.  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Aktivieren der virtuellen Authentifikator-Umgebung" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Aktivieren der virtuellen Authentifikator-Umgebung**  
    :::image-end:::  
    
1.  Konfigurieren Sie im Abschnitt **neuer Authentifikator** die folgenden Optionen.  
    
    | Option | Wert | Details |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] oder [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | Das Protokoll, das der virtuelle Authentifikator für die Codierung und Decodierung verwendet |  
    | `Transport` |   `usb`, `nfc` , `ble` oder `internal` | Der virtuelle Authentifikator simuliert den ausgewählten Transport für die Kommunikation mit Clients, um eine Assertion für bestimmte Anmeldeinformationen zu erhalten.  Weitere Informationen finden Sie unter [Authentifikator-Transport-Enumeration][GithubW3cWebauthnEnumTransport] . |  
    |  `Supports resident keys` | Aktivieren von \ (oder Off \) mithilfe des Kontrollkästchens | Aktivieren Sie diese Option, wenn Ihre Web-App auf Resident Keys (auch als "clientseitig erkennbare Anmeldeinformationen" bezeichnet) basiert.  Wenn Sie weitere Informationen erhalten möchten, navigieren Sie zur [Anforderungs Enumeration für residente Schlüssel][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Aktivieren von \ (oder Off \) mithilfe des Kontrollkästchens | Aktivieren Sie diese Option, wenn Ihre Web-App die lokale Autorisierung mithilfe von Gesten Modalitäten wie Touch plus PIN-Code, Kennworteingabe oder biometrische Erkennung anvertraut.  Weitere Informationen finden Sie unter [Benutzerüberprüfung][GithubW3cWebauthnEnumUserverification] . |  
    
1.  Klicken Sie auf die Schaltfläche **Hinzufügen**.  
1.  Ein neuer Abschnitt Ihres neu erstellten Authentifikators wird angezeigt.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
Der **Authentifikator** -Abschnitt enthält eine Tabelle mit **Anmeldeinformationen** .  Die Tabelle ist leer, bis die Anmeldeinformationen für den Authentifikator registriert sind.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Keine Anmeldeinformationen" lightbox="../media/webauthn-no-cred.msft.png":::
   Keine Anmeldeinformationen  
:::image-end:::  

## Registrieren einer neuen Anmeldeinformationen  

Führen Sie die folgenden Schritte aus, um eine neue Anmeldeinformationen zu registrieren.  Weitere Informationen dazu, was die [Webauthentifizierungs-API][GithubW3cWebauthn] beim Registrieren einer neuen Anmeldeinformationen tut, finden Sie unter [Erstellen einer neuen Anmelde][GithubW3cWebauthnSctnCreatecredential]Informationen.  

1.  Wählen Sie auf der Demo-Website **neue Anmeldeinformationen registrieren**aus.  
1.  Im webauthn-Tool wird nun eine neue Anmeldeinformation zur Tabelle " **Anmeldeinformationen** " hinzugefügt.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Anzeigen von Anmeldeinformationen" lightbox="../media/webauthn-view-cred.msft.png":::
       Anzeigen von Anmeldeinformationen  
    :::image-end:::  
    
Klicken Sie auf der Demo-Website auf die Schaltfläche **Authentifizieren** .  Überprüfen Sie, ob die [Anzahl][GithubW3cWebauthnSctnSignCounter] der Anmeldeinformationen in der Tabelle mit den **Anmeldeinformationen** um 1 erhöht wurde, wodurch ein erfolgreicher [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] -Vorgang markiert wird.  

## Exportieren und Entfernen von Anmeldeinformationen  

Wenn Sie eine Anmeldeinformationen exportieren oder entfernen möchten, wählen Sie die Schaltfläche **exportieren** oder **Entfernen** aus.  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportieren oder Entfernen von Anmeldeinformationen" lightbox="../media/webauthn-export-remove.msft.png":::
   Exportieren oder Entfernen von Anmeldeinformationen  
:::image-end:::  

## Umbenennen eines Authentifikators  

Führen Sie die folgenden Schritte aus, um einen Authentifikator umzubenennen.  

1.  Wählen Sie neben dem Namen des Authentifikators die Schaltfläche **Bearbeiten** aus.  
1.  Bearbeiten Sie den Namen, und wählen **Sie dann Enter** aus, um die Änderungen zu speichern.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Umbenennen eines Authentifikators" lightbox="../media/webauthn-rename.msft.png":::
   Umbenennen eines Authentifikators  
:::image-end:::  

## Einrichten des aktiven Authentifikators  

Ein neu erstellter Authentifikator wird automatisch aktiviert.  Wenn Sie einen anderen virtuellen Authentifikator verwenden möchten, wählen Sie das **aktive** Optionsfeld neben dem Authentifikator aus.  

> [!NOTE]
> DevTools unterstützt zu einem beliebigen Zeitpunkt nur einen aktiven virtuellen Authentifikator.  Wenn Sie den aktiven Authentifikator entfernen, wird ein anderer Authentifikator nicht automatisch aktiviert.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Aktiven Authentifikator einrichten" lightbox="../media/webauthn-set-active.msft.png":::
   Aktiven Authentifikator einrichten  
:::image-end:::  

## Entfernen eines virtuellen Authentifikators  

Um einen virtuellen Authentifikator zu entfernen, klicken Sie neben dem Authentifikator auf die Schaltfläche **Entfernen** .  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Authentifikator entfernen" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Authentifikator entfernen  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Sie Microsoft Edge devtools | Microsoft docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Webauthn-Demo | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Client-zu-Authentifikator-Protokoll (CTAP) | Fido-Allianz"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Übersicht über den universellen zweiten Faktor (U2F) | Fido-Allianz"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen für öffentliche Schlüssel-Ebene 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Der authenticatorGetAssertion-Vorgang – Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen Ebene 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authentifikator-Transport-Enumeration (Enum-AuthenticatorTransport) – Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen Ebene 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeration für residente Schlüsselanforderungen (Enum ResidentKeyRequirement) – Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen für öffentliche Schlüssel Ebene 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Benutzerüberprüfung – Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen Ebene 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Erstellen Sie eine neue Anmeldeinformationen-PublicKeyCredential [[Create]] (Origin, Options, sameOriginWithAncestors)-Methode – Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen des öffentlichen Schlüssels Ebene 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Überlegungen zum Signatur Indikator – Webauthentifizierung: eine API für den Zugriff auf die Anmeldeinformationen für öffentliche Schlüssel (Ebene 2) | GitHub"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
