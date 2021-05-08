---
description: Emulieren von Authenticators und Debuggen von WebAuthn in Microsoft Edge DevTools.
title: Emulieren von Authatoren und Debuggen von WebAuthn in Microsoft Edge DevTools
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
# Emulieren von Authatoren und Debuggen von WebAuthn in Microsoft Edge DevTools  

Anstatt die Webauthentifizierung in Ihrer Website oder App mit physischen Authentatoren zu debuggen, verwenden Sie das **WebAuthn-Tool** in Microsoft Edge DevTools zum Erstellen und Interagieren mit softwarebasierten virtuellen Authentatoren.  

## Vorbemerkungen  

Ein hervorragender Ort, um mit der Webauthentifizierung zu beginnen, ist die [Webauthentifizierungs-API-Spezifikation.][GithubW3cWebauthn]  

## Einrichten des WebAuthn-Tools  

1.  Navigieren Sie zu einer Webseite, die WebAuthn verwendet, z. B. die folgende Demowebsite.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Melden Sie sich bei der Website an.  
1.  [Öffnen Sie DevTools][DevtoolsGuideChromiumOpen].  
1.  Wählen Sie zum Öffnen des **WebAuthn-Tools** das Symbol **DevTools** anpassen \( \) > `...` ****  >  **WebAuthn**weitere Tools aus.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="WebAuthn-Tool" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       **WebAuthn-Tool**  
    :::image-end:::  
    
1.  Aktivieren Sie **im WebAuthn-Tool** das Kontrollkästchen Virtuelle **Authatorumgebung** aktivieren.  
1.  Nachdem sie aktiviert wurde, wird ein neuer Abschnitt mit dem Namen **Neuer Authentator** angezeigt.  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Aktivieren der virtuellen Authentatorumgebung" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Aktivieren der virtuellen Authentatorumgebung**  
    :::image-end:::  
    
1.  Konfigurieren Sie **im Abschnitt Neuer** Authentator die folgenden Optionen.  
    
    | Option | Wert | Details |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] oder [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | Das Protokoll, das der virtuelle Authentisierungsgerät für die Codierung und Decodierung verwendet |  
    | `Transport` |   `usb`, `nfc` `ble` , oder `internal` | Der virtuelle Authentator simuliert den ausgewählten Transport für die Kommunikation mit Clients, um eine Assertion für eine bestimmte Anmeldeinformationen zu erhalten.  Weitere Informationen finden Sie unter [Authenticator Transport Enumeration][GithubW3cWebauthnEnumTransport] |  
    |  `Supports resident keys` | Aktivieren Sie \(oder off\) mithilfe des Kontrollkästchens. | Aktivieren Sie, wenn Ihre Web-App auf residenten Schlüsseln \(auch als clientseitiges Erkennen von Anmeldeinformationen\) bekannt ist.  Weitere Informationen finden Sie unter [Resident Key Requirement Enumeration][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Aktivieren Sie \(oder off\) mithilfe des Kontrollkästchens. | Aktivieren Sie, wenn Ihre Web-App mithilfe von Gestenmodalitäten wie Toucheingabe und Pincode, Kennworteingabe oder biometrischer Erkennung auf lokale Autorisierung angewiesen ist.  Weitere Informationen finden Sie unter [Benutzerüberprüfung.][GithubW3cWebauthnEnumUserverification] |  
    
1.  Klicken Sie auf die Schaltfläche **Hinzufügen**.  
1.  Ein neuer Abschnitt des neu erstellten Authentator wird angezeigt.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
Der **Authenticator** enthält eine **Credentials-Tabelle.**  Die Tabelle ist leer, bis eine Anmeldeinformationen für den Authentator registriert sind.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Keine Anmeldeinformationen" lightbox="../media/webauthn-no-cred.msft.png":::
   Keine Anmeldeinformationen  
:::image-end:::  

## Registrieren neuer Anmeldeinformationen  

Führen Sie die folgenden Schritte aus, um neue Anmeldeinformationen zu registrieren.  Weitere Informationen zur [Webauthentifizierungs-API][GithubW3cWebauthn] beim Registrieren neuer Anmeldeinformationen finden Sie unter [Create a New Credential][GithubW3cWebauthnSctnCreatecredential].  

1.  Wählen Sie auf der Demowebsite die Option **Neue Anmeldeinformationen registrieren aus.**  
1.  Der Tabelle "Anmeldeinformationen" **** im WebAuthn-Tool werden nun neue Anmeldeinformationen hinzugefügt.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Anzeigen von Anmeldeinformationen" lightbox="../media/webauthn-view-cred.msft.png":::
       Anzeigen von Anmeldeinformationen  
    :::image-end:::  
    
Wählen Sie auf der Demowebsite die Schaltfläche **Authentifizieren** aus.  Stellen Sie [sicher,][GithubW3cWebauthnSctnSignCounter] dass die Anzahl der Anmeldeinformationen in der **Tabelle** Anmeldeinformationen um 1 erhöht wurde, was einen erfolgreichen [AuthenticatorGetAssertion-Vorgang][GithubW3cWebauthnAuthenticatorgetassertion] kennzeichnet.  

## Exportieren und Entfernen von Anmeldeinformationen  

Zum Exportieren oder Entfernen von Anmeldeinformationen wählen Sie die Schaltfläche **Exportieren** **oder** Entfernen aus.  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportieren oder Entfernen von Anmeldeinformationen" lightbox="../media/webauthn-export-remove.msft.png":::
   Exportieren oder Entfernen von Anmeldeinformationen  
:::image-end:::  

## Umbenennen eines Authentators  

Führen Sie die folgenden Schritte aus, um einen Authentator umzubenennen.  

1.  Wählen Sie neben dem Namen des Authentator die Schaltfläche **Bearbeiten** aus.  
1.  Bearbeiten Sie den Namen, und klicken Sie dann auf **Eingabe,** um die Änderungen zu speichern.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Umbenennen eines Authentators" lightbox="../media/webauthn-rename.msft.png":::
   Umbenennen eines Authentators  
:::image-end:::  

## Festlegen des aktiven Authentators  

Ein neu erstellter Authentator wird automatisch aktiviert.  Um einen anderen virtuellen Authentator zu verwenden, wählen Sie das **Optionsfeld Aktiv** neben dem Authentator aus.  

> [!NOTE]
> DevTools unterstützt zu einem beliebigen Zeitpunkt nur einen aktiven virtuellen Authentator.  Wenn Sie den aktiven Authentator entfernen, wird nicht automatisch ein anderer Authentator aktiviert.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Festlegen des aktiven Authentator" lightbox="../media/webauthn-set-active.msft.png":::
   Festlegen des aktiven Authentator  
:::image-end:::  

## Entfernen eines virtuellen Authentators  

Um einen virtuellen Authentator zu entfernen, wählen Sie neben dem Authentator die Schaltfläche **Entfernen** aus.  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Entfernen des Authentator" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Entfernen des Authentator  
:::image-end:::  

## Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Öffnen Microsoft Edge DevTools | Microsoft Docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Webauthn demo | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Client to Authenticator Protocol (CTAP) | fido alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Übersicht über den universellen 2nd-Faktor (U2F) | fido alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "Der AuthenticatorGetAssertion-Vorgang – Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Transport enumeration (enum AuthenticatorTransport) - Web Authentication: An API for accessing Public Key Credentials Level 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Resident Key Requirement Enumeration (enum ResidentKeyRequirement) - Web authentication: An API for accessing Public Key Credentials Level 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Benutzerüberprüfung – Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Create a New Credential - PublicKeyCredential's [[Create]](origin, options, sameOriginWithAncestors) Method - Web Authentication: An API for accessing Public Key Credentials Level 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Überlegungen zum Signaturindikator – Webauthentifizierung: Eine API für den Zugriff auf Anmeldeinformationen der Stufe 2 | GitHub"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite findet sich [hier](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) und wurde von [Jecelyn Yeen][JecelynYeen] \(Developer Advocate, Chrome DevTools\) erstellt.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
