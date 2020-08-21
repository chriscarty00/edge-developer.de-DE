---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Erfahren Sie, wie die Webauthentifizierungs-API Webanwendungen die Verwendung von Windows Hello und FIDO2 für die Benutzerauthentifizierung ermöglichen kann.
title: Webauthentifizierung – Entwicklerhandbuch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: b8ff3769434c17b5508978c64b5d9c14e7e3bdaa
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941813"
---
# Web-Authentifizierung und Windows Hello  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Die [Webauthentifizierungs-API](https://w3c.github.io/webauthn) in Microsoft Edge ermöglicht Webanwendungen die Verwendung von [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) -und [externen FIDO2-Geräten](https://fidoalliance.org/fido2) für die Benutzerauthentifizierung, damit Sie und Ihre Benutzer alle Probleme und Risiken der Kennwortverwaltung vermeiden können, einschließlich der Kenn Wort erraten, Phishing-Angriffe und Angriffe auf die Schlüsselprotokollierung.  Die aktuelle Microsoft Edge-Implementierung basiert auf der Kandidaten Empfehlung der Webauthentifizierungs Spezifikation.  

> [!IMPORTANT]
> In diesem Thema wird gezeigt, wie Sie die Windows Hello-und FIDO2-Authentifizierung mit Microsoft Edge testen.  

Mithilfe der Webauthentifizierung sendet der Server eine unformatierte Text Herausforderung an den Browser.  Sobald Microsoft Edge in der Lage ist, den Benutzer über Windows Hello oder ein externes FIDO2-Gerät zu verifizieren, signiert das System die Challenge mit einem zuvor für diesen Benutzer bereitgestellten privaten Schlüssel und sendet die Signatur zurück an den Server.  Wenn der Server die Signatur mit dem öffentlichen Schlüssel überprüfen kann, den Sie für diesen Benutzer hat, und überprüfen Sie, ob die Herausforderung richtig ist, kann Sie den Benutzer sicher authentifizieren.  Bei [asymmetrischer Kryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography) wie dieser ist der öffentliche Schlüssel für sich selbst bedeutungslos, und der private Schlüssel wird nie freigegeben.  Darüber hinaus kann der private Schlüssel nie aus sicheren Elementen oder modernen Systemen mit TPM-fähiger Hardware verschoben werden.  

Es gibt zwei grundlegende Schritte bei der Verwendung der Web-Authentifizierungs-API:  

1.  Registrieren Ihres Benutzers bei `create`  
1.  Authentifizieren des Benutzers mit `get`  

Das folgende dev-Handbuch führt Sie durch diesen Fluss mit der [webauthn-Beispiel-App](https://github.com/MicrosoftEdge/webauthnsample).  

## Registrieren des Benutzers  

Wenn Sie als Identitätsanbieter fungieren, müssen Sie zuerst eine Webauthentifizierungs Anmeldeinformationen für den Benutzer mit der `navigator.credentials.create` Methode erstellen.  Bevor Sie diese Anmeldeinformationen für den Benutzer auf dem Server registrieren, müssen Sie die Identität des Benutzers bestätigen.  Dies kann geschehen, wenn Sie dem Nutzer eine Bestätigung per e-Mail senden oder ihn bitten, seine herkömmliche Anmeldemethode zu verwenden.  

Die `create` Methode verwendet die folgenden Parameter:  

:::row:::
   :::column span="1":::
      **Informationen zur vertrauenden Seite**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      rp: {
          name: "WebAuthn Sample App",
          icon: "https://example.com/rpIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Informationen zum Benutzerkonto**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      user: {
          id: stringToArrayBuffer("some.user.id"),
          name: "bob.smith@contoso.com",
          displayName: "Bob Smith",
          icon: "https://example.com/userIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Crypto-Parameter**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      pubKeyCredParams: [
          {
              //External authenticators support the ES256 algorithm
              type: "public-key",
              alg: -7                 
          }, 
          {
              //Windows Hello supports the RS256 algorithm
              type: "public-key",
              alg: -257
          }
      ],
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Authentifikator-Auswahlparameter**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      authenticatorSelection: {
          //Select authenticators that support username-less flows
          requireResidentKey: true,
          //Select authenticators that have a second factor (such as PIN, Bio)
          userVerification: "required",
          //Selects between bound or detachable authenticators
          authenticatorAttachment: "platform"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Weitere Optionen**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      //Select larger timeout values, as Microsoft Edge shows UI
      timeout: 50000,
      //an opaque challenge that the authenticator signs over
      challenge: challenge,
      //prevent re-registration by specifying existing credentials here
      excludeCredentials: [],
      //specifies whether you need an attestation statement
      attestation: "none" 
      ```  
   :::column-end:::
:::row-end:::  

Sie können [Anmelde Informations Erstellungsparameter](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) verwenden, um die Anmeldeinformationen zu konfigurieren, die Sie erstellen möchten.  Insbesondere können Sie auswählen, ob Sie eine Windows Hello-Anmeldeinformationen erstellen möchten, indem Sie auf ein `authenticatorAttachment` `platform` externes FIDO2-Gerät oder auf ein Roaming-Anmeldeinformationen festlegen `authenticatorAttachment` `cross-platform` .  

Wenn Sie die `create` Methode verwenden, fordert Microsoft Edge zunächst den Benutzer auf, seinen Anwesenheitsstatus zu überprüfen, indem er sein Angesicht oder seinen Fingerabdruck scannt, eine PIN eingibt oder auf einem externen FIDO2-Gerät eine Aktion durchführt.  Nach Abschluss dieses Schritts generiert der Authentifikator ein publicprivate-Schlüsselpaar und speichert den privaten Schlüssel.  Diese Anmeldeinformationen werden pro Herkunft und Konto erstellt und können nicht extrahiert werden, da Sie sicher auf dem Authentifizierungsgerät gespeichert werden.  

Die resultierende Versprechung gibt ein [Testat-Objekt](https://w3c.github.io/webauthn#sctn-attestation) zurück, das die neuen Anmeldeinformationen darstellt.  Das Testat-Objekt enthält den öffentlichen Schlüssel für die Anmeldeinformationen.  Sie senden dieses Objekt an den Server, um zukünftige Authentifizierungen zu überprüfen.  Bevor Sie zum Server zurückkehren, müssen Sie die unformatierten Daten Base64-codiert codieren.  

**Client**  

```javascript
<script>
    navigator.credentials.create({
        publicKey: createCredentialOptions
    }).then(rawAttestation => {
        var attestation = {
            id: base64encode(rawAttestation.rawId),
            clientDataJSON: arrayBufferToString(rawAttestation.response.clientDataJSON),
            attestationObject: base64encode(rawAttestation.response.attestationObject)
        };
        return rest_put("/credentials", attestation);
    })
</script>
```  

Der Server sollte dann das Bestätigungs Objekt decodieren, Überprüfungsschritte ausführen, den öffentlichen Schlüssel für diese Anmeldeinformationen extrahieren und für zukünftige Authentifizierungen speichern.  Eine detaillierte Liste der Schritte finden Sie im Algorithmus zur [Registrierung von Anmeldeinformationen](https://w3c.github.io/webauthn#registering-a-new-credential) in der webauthn-Spezifikation.  

**Server**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## Authentifizieren des Benutzers  

Nachdem die Anmeldeinformationen auf dem Client erstellt wurden, können Sie das nächste Mal, wenn der Benutzer versucht, sich bei der Website anzumelden, Ihnen anbieten, diese mithilfe ihrer Webauthentifizierungs Anmeldeinformationen anstelle eines Kennworts mit einem Anruf an zu signieren `navigator.credentials.get` .  

Die `get` Methode nimmt die Herausforderung als einzigen erforderlichen Parameter an.  Die Herausforderung ist eine undurchsichtige Bytefolge, die vom Server an einen Client gesendet wird, um mit dem privaten Schlüssel des Benutzers zu signieren.  Zum Beispiel:  

**Server**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

Nachdem Sie eine Herausforderung vom Server abgerufen haben, rufen Sie die Get-API zusammen mit den Optionen für die [Anmelde Informationsanforderung](https://w3c.github.io/webauthn#credentialrequestoptions-extension)auf.  Microsoft Edge zeigt eine Aufforderung an, mit der die Identität des Benutzers mit Windows Hello oder einem externen FIDO2-Gerät überprüft wird.  Nachdem der Benutzer überprüft wurde, wird die Herausforderung innerhalb des TPM-oder FIDO2-Geräts signiert, und die Versprechung wird mit einem [Assertions Objekt](https://w3c.github.io/webauthn#authenticatorassertionresponse) zurückgegeben, das die Signatur und andere Metadaten enthält, die Sie an den Server senden.  

**Client**  

```javascript
    var credentialRequestOptions = {
        //specifies which credential IDs are allowed to authenticate the user
        //if empty, any credential can authenticate the users
        allowCredentials: allowCredentials,
        //an opaque challenge that the authenticator signs over
        challenge: challenge,
        //Select larger timeout values, as Microsoft Edge shows UI
        timeout: 50000
    };

    navigator.credentials.get({
        publicKey: credentialRequestOptions
    }).then(rawAssertion => {
        var assertion = {
            id: base64encode(rawAssertion.rawId),
            clientDataJSON: arrayBufferToString(rawAssertion.response.clientDataJSON),
            userHandle: base64encode(rawAssertion.response.userHandle),
            signature: base64encode(rawAssertion.response.signature),
            authenticatorData: base64encode(rawAssertion.response.authenticatorData)
        };
        return rest_put("/assertion", assertion);
    })
```  

Nachdem Sie die Assertion auf dem Server erhalten haben, müssen Sie die Signatur überprüfen, um den Benutzer zu authentifizieren.  Im folgenden sind einige Beispielcodes zu entschlüsseln.  Eine detaillierte Liste der Schritte finden Sie im Algorithmus zur [Assertionsüberprüfung](https://w3c.github.io/webauthn#verifying-assertion) in der webauthn-Spezifikation.  

**Server**  

```javascript
    var jwkToPem = require('jwk-to-pem')
    var crypto = require('crypto');

    ...

    // Using credential’s id attribute, look up the corresponding 
    // credential public key.
    var credential = await storage.Credentials.findOne({
        id: assertion.id
    });

    //Refer to sample to see how to verify client data and authenticator data

    ...

    //Using the credential public key from lookup, verify that sig is a valid
    //signature over the binary concatenation of authData and hash.
    var publicKey = credential.publicKeyJwk;
    var verify = (publicKey.kty === "RSA") ? crypto.createVerify('RSA-SHA256') : crypto.createVerify('sha256');
    verify.update(authData);
    verify.update(hash);
    if (!verify.verify(jwkToPem(publicKey), sig))
        throw new Error("Could not verify signature");

    //Verify signCount has increased or is zero 
    if (authenticatorData.signCount != 0 &&
        authenticatorData.signCount < credential.signCount) {
        throw new Error("Received signCount of " + authenticatorData.signCount +
            " expected signCount > " + credential.signCount);
    }
```  

## Implementierungshinweise  

### Unterstützte Plattformen  

*   Die Version der Kandidaten Empfehlung der Webauthentifizierungs-API kann von Microsoft Edge beginnend mit EdgeHTML 18 \ (Windows Insider Preview-Version 17713 oder höher) verwendet werden.  
*   Die vorangestellte [Preview-Version](https://blogs.windows.com/msedgedev/2016/04/12) der Webauthentifizierungs-API wurde entfernt und steht nicht mehr zur Verfügung.  
*   Die Webauthentifizierungs-API steht für UWP-apps und-PWAs noch nicht zur Verfügung.  
*   Internet Explorer unterstützt die Webauthentifizierungs-API nicht.  

### Unterstützte Authentifikatoren  

Mit der Web-Authentifizierungs-API in Microsoft Edge können Sie Benutzer mit den folgenden Technologien authentifizieren:  

*   **Windows Hello**  Ermöglicht die kennwortgeschützte Authentifizierung auf einem Gerät mit Face, Fingerabdruck oder PIN  
*   **FIDO2**  Ermöglicht die kennwortlos-Roaming-Authentifizierung mit einem Wechselmedium und einem Fingerabdruck oder einer PIN  
*   **U2F**  Ermöglicht eine starke Authentifizierung des zweiten Faktors für Websites, die nicht bereit sind, zu einem Kenn Wort unfähigen Modell zu wechseln  

### Besondere Überlegungen für Windows Hello  

Einige Dinge, die Sie bei der Verwendung des Windows Hello-Authentifikators beachten sollten:  

*   Sie können feststellen, ob Windows Hello auf einem PC verfügbar ist, indem Sie die `isUserVerifyingPlatformAuthenticatorAvailable` API aufrufen.  Weitere Informationen zu dieser API [finden Sie hier](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).  
*   Wenn Sie eine Anmeldeinformationen für Windows Hello erstellen, sollten `authenticatorAttachment` Sie `platform` für eine optimale Benutzererfahrung festzulegen.
*   Windows Hello unterstützt nur RS256 \ (AIG-257 \) als öffentlichen Schlüsselalgorithmus.  Stellen Sie sicher, dass Sie bei der Erstellung von Anmeldeinformationen diesen Algorithmus angeben.  
*   Um eine [TPM-Bestätigungsanweisung](https://w3c.github.io/webauthn#tpm-attestation)zu erhalten, legen Sie die Bescheinigung beim Aufrufen der API auf "Direct" fest `create` .  Die TPM-Bescheinigung ist ein optimaler Aufwand.  Nur PCs mit TPM 2,0 geben eine TPM-Bestätigungsanweisung zurück, und der Bestätigungsprozess kann aus verschiedenen Gründen fehlschlagen.  
*   Windows Hello verwendet verschiedene Möglichkeiten, um Benutzeranmeldeinformationen zu schützen.  Sie können überprüfen, welche Methode zum Schützen von Anmeldeinformationen verwendet wurde, indem Sie das [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) -Feld im Bestätigungs Objekt verwenden, das bei der Erstellung von Anmeldeinformationen zurückgegeben wird.  Die folgende Liste enthält die AAGUIDs, die von Windows Hello zurückgegeben werden können:   
    *   Software-gesicherte Authentifikatoren  
        *   Windows Hello-Software-Authentifikator:  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   Windows Hello VBS-Software-Authentifikator:  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   Vertrauenswürdiges Plattformmodul \ (TPM \) gesicherte Authentifikatoren  
        *   Windows Hello-Hardware-Authentifikator:  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   Windows Hello VBS-Hardware-Authentifikator:  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### API-Oberfläche  

*   Microsoft Edge verfügt über eine vollständige Implementierung der Kandidaten Empfehlungs Version der Core Web Authentication-Spezifikation.  
*   Die [Erweiterung](https://w3c.github.io/webauthn#sctn-appid-extension) für die Erweiterung wird unterstützt.  
*   Es werden keine weiteren Erweiterungen unterstützt.  

## Demos  

[Beispiel für Client-und Servercode](https://github.com/MicrosoftEdge/webauthnsample)  

[Windows Hello Test Drive-Demo](https://webauthnsample.azurewebsites.net)  

## Spezifikation  

[Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen](http://w3c.github.io/webauthn)  
