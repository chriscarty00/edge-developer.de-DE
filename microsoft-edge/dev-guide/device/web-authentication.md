---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Erfahren Sie, wie die Webauthentifizierungs-API verwendet werden kann, um Webanwendungen die Verwendung von Windows Hello Biometrie für die Benutzerauthentifizierung zu ermöglichen.
title: Dev Guide – Web-Authentifizierung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: c49d181633ae1b2b35aa0f88287841d28e806f44
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566764"
---
# Web-Authentifizierung und Windows Hello

Die Webauthentifizierungs-API (ehemals *Fido 2,0* ) in Microsoft Edge ermöglicht Webanwendungen die Verwendung von [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) Biometrie für die Benutzerauthentifizierung, damit Sie und Ihre Benutzer alle Probleme und Risiken der Kennwortverwaltung vermeiden können, einschließlich der Kenn Wort erraten, Phishing-und Keylogger-Angriffe. Die aktuelle Microsoft Edge-Implementierung (*MS-* prefixes) basiert auf einem früheren Entwurf der Webauthentifizierungs Spezifikation und wird sich wahrscheinlich in Zukunft ändern. **In diesem Thema wird gezeigt, wie Sie die Windows Hello-Authentifizierung mit Microsoft Edge testen, während Sie Ihren Code auch in Zukunft für Browser Updates überprüfen.**

Die Webauthentifizierungs-API ist ein neuer Standard, der von der [Fido-Allianz](https://fidoalliance.org/) mit dem Ziel bereitgestellt wird, eine interoperable Methode für die Webauthentifizierung mit Windows Hello und anderen biometrischen Geräten in Browsern bereitzustellen. Die Webauthentifizierungs Spezifikation definiert zwei Authentifizierungsszenarien: Kennwort-less und zwei-Faktor. Im Fall eines Kennworts muss sich der Benutzer nicht mit einem Benutzernamen oder Kennwort bei der Webseite anmelden – er kann sich nur mithilfe von Windows Hello anmelden. Im Fall von zwei Faktoren meldet sich der Benutzer normalerweise mit einem Benutzernamen und Kennwort an, aber Windows Hello wird als zweite Faktor Überprüfung verwendet, um die allgemeine Authentifizierung zu verstärken.

Wenn Sie die Webauthentifizierung mit Windows Hello kombinieren, sendet der Server eine unformatierte Text Herausforderung an den Browser. Sobald Microsoft Edge in der Lage ist, den Benutzer über Windows Hello zu überprüfen, signiert das System die Challenge mit einem zuvor für diesen Benutzer bereitgestellten privaten Schlüssel und sendet die Signatur wieder an den Server. Wenn der Server die Signatur mit dem öffentlichen Schlüssel überprüfen kann, den Sie für diesen Benutzer hat, und überprüfen Sie, ob die Herausforderung richtig ist, kann Sie den Benutzer sicher authentifizieren. Bei [asymmetrischer Kryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography) wie dieser ist der öffentliche Schlüssel für sich selbst bedeutungslos, und der private Schlüssel wird nie freigegeben. Darüber hinaus kann der private Schlüssel nie aus modernen Systemen mit TPM-fähiger Hardware verschoben werden.

Es gibt zwei grundlegende Schritte bei der Verwendung der Web-Authentifizierungs-API:

**1. registrieren Sie Ihren Nutzer bei `makeCredential`**

**2. authentifizieren Sie Ihren Benutzer mit `getAssertion`**

Im folgenden werden Sie durch diesen Fluss unter Verwendung der empfohlenen [webauthn. js-Polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)-Anwendung geführt. Der [vollständige Code](https://github.com/adrianba/fido-snippets/) steht für diese Server-und clientseitige Demo zur Verfügung. [C#](https://github.com/adrianba/fido-snippets/tree/master/csharp)-, [php](https://github.com/adrianba/fido-snippets/tree/master/php)-und [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) -serverseitige Versionen sind verfügbar.

## Registrieren des Benutzers

Wenn Sie als *Identitätsanbieter*fungieren, müssen Sie zuerst eine Webauthentifizierungs Anmeldeinformationen für Ihren Benutzer mit dem Fenster. webauthn erstellen. **makeCredential** -Methode. Bevor Sie diese Anmeldeinformationen für den Benutzer auf dem Server registrieren, müssen Sie die Identität des Benutzers bestätigen. Dies kann geschehen, wenn Sie dem Nutzer eine Bestätigung per e-Mail senden oder ihn bitten, seine herkömmliche Anmeldemethode zu verwenden.

Die makeCredential-Methode verwendet die folgenden Parameter:
 - **Informationen zum Benutzerkonto**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **Crypto-Parameter**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

Die resultierende Versprechung gibt ein Objekt zurück, das die Anmeldeinformationen darstellt, die Sie dann zurück an den Server senden, um zukünftige Authentifizierungen zu überprüfen:

**Client**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var email = '<%=user.email%>';
    var name = '<%=user.name%>';

    webauthn.makeCredential(userAccountInformation, cryptoParams)
        .then(function (creds) {
            document.getElementById('form-id').value = creds.credential.id;
            document.getElementById('form-pk').value = JSON.stringify(creds.publicKey);
            document.getElementById('form-email').value = email;
            document.getElementById('form-name').value = name;
            document.getElementById('theform').submit();
        }).catch(function (err) {
            // No acceptable authenticator or user refused consent. Handle appropriately.
            alert(err);
        });
</script>
```

Wenn Sie die makeCredential-Methode verwenden, fordert Microsoft Edge zunächst Windows Hello auf, die Face-oder Fingerabdruck Kennung zu verwenden, um zu überprüfen, ob der Benutzer derselbe Benutzer wie der beim Windows-Konto angemeldet ist. Nach Abschluss dieses Schritts generiert Microsoft Passport ein öffentliches/privates Schlüsselpaar und speichert den privaten Schlüssel im Trusted Platform Module (TPM), der dedizierten Crypto-Prozessor-Hardware, die zum Speichern von Anmeldeinformationen verwendet wird. Wenn der Benutzer nicht über ein TPM-fähiges Gerät verfügt, werden diese Schlüssel in der Software gespeichert. Diese Anmeldeinformationen werden pro Herkunft, pro Windows-Konto erstellt und werden nicht durchlaufen, weil Sie mit dem Gerät verbunden sind. Das bedeutet, dass Sie sicherstellen müssen, dass der Benutzer sich registriert, um Windows Hello für jedes verwendete Gerät zu verwenden.

## Authentifizieren des Benutzers

Nachdem die Anmeldeinformationen auf dem Client erstellt wurden, können Sie das nächste Mal, wenn der Benutzer versucht, sich bei der Website anzumelden, Ihnen anbieten, Sie unter Verwendung von Windows Hello anstelle eines Kennworts mit einem Anruf an Window. webauthn zu signieren. **getassertion**.

Die getassertion-Methode nimmt die *Herausforderung* als einzigen erforderlichen Parameter an. Die Herausforderung ist die nach dem Zufallsprinzip generierte Menge, die vom Server an einen Client gesendet wird, um mit dem privaten Schlüssel des Benutzers zu signieren. Beispiel:

**Server**

```
var crypto = require('crypto');

Strategy.prototype.generateChallenge = function() {
    return this.generateVerifiableString(crypto.randomBytes(32));
};

Strategy.prototype.generateVerifiableString = function(data) {
    // Create cipher using secret
    var d = new Buffer(data);
    var c = crypto.createCipher('aes192',new Buffer(this._secret));

    // Encrypt data
    c.update(d);

    // Hash results of encrypting data
    var hash = crypto.createHash('sha256');
    hash.update(c.final());

    // Combine original data with hash
    return d.toString('hex') + string_separator + hash.digest('hex');
};
```

Nachdem der getassertions-Anruf durchgeführt wurde, zeigt Microsoft Edge die Windows Hello-Eingabeaufforderung an, mit der die Identität des Benutzers über die Biometrie überprüft wird. Nachdem der Benutzer überprüft wurde, wird die Herausforderung im TPM signiert, und die Versprechung wird mit einem Assertions Objekt zurückgegeben, das die Signatur und andere Metadaten enthält, die Sie an den Server senden möchten:

**Client**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var challenge = '<%=challenge%>';

    webauthn.getAssertion(challenge)
    .then(function(assertion) {
      document.getElementById("form-id").value = assertion.credential.id;
      document.getElementById("form-type").value = assertion.credential.type;
      document.getElementById("form-data").value = assertion.clientData;
      document.getElementById("form-sig").value = assertion.signature;
      document.getElementById("form-authnr").value = assertion.authenticatorData;
      document.getElementById("form-challenge").value = challenge;
      document.getElementById("theform").submit();
    })
    .catch(function(err) {
      if(err && err.name) {
        document.getElementById("form-err").value = err.name;
      } else {
        document.getElementById("form-err").value = "unknown";
      }
      document.getElementById("theform").submit();
    });

</script>
```

Nachdem Sie die Assertion auf dem Server erhalten haben, müssen Sie die Signatur überprüfen, um den Benutzer zu authentifizieren. Beispiel (in Node. js):

**Server**

```
var jwkToPem = require('jwk-to-pem')
var crypto = require('crypto');

var fidoAuthenticator = {
     validateSignature: function (publicKey, clientData, authnrData, signature, challenge) {
         // Make sure the challenge in the client data
         // matches the expected challenge
         var c = new Buffer(clientData, 'base64');
         var cc = JSON.parse(c.toString().replace(/\0/g,''));
         if(cc.challenge != challenge) return false;

         // Hash data with sha256
         const hash = crypto.createHash('sha256');
         hash.update(c);
         var h = hash.digest();

         // Verify signature is correct for authnrData + hash
         var verify = crypto.createVerify('RSA-SHA256');
         verify.update(new Buffer(authnrData,'base64'));
         verify.update(h);
         return verify.verify(jwkToPem(JSON.parse(publicKey)), signature, 'base64');
     }
};   
```

## Unterschiede zwischen Microsoft Edge und der Spezifikation

> [!NOTE]
> Wenn Sie die Webauthentifizierungs-API mit Windows Hello in Microsoft Edge testen, empfehlen wir die Verwendung von webauthen. js Polyfill wie oben beschrieben, um zu vermeiden, dass Sie die hier aufgelisteten Diskrepanzen berücksichtigen müssen. Wir aktualisieren diese Polyfill-Datei für jede wichtige veröffentlichte Version der Spezifikation.


Die aktuelle Microsoft Edge-Implementierung basiert auf einem früheren Entwurf der Webauthentifizierungs Spezifikation und wird sich wahrscheinlich in zukünftigen Builds ändern, während sich die Spezifikation entwickelt. Zu den aktuellen Unterschieden gehören:

- Microsoft Edge-APIs sind MS-Präfixe.
- Microsoft Edge unterstützt noch keine externen Anmeldeinformationen wie USB-Schlüssel oder Bluetooth-Geräte. Die aktuelle API ist auf eingebettete im TPM gespeicherte Anmeldeinformationen limitiert.
- Das aktuell angemeldete Windows-Benutzerkonto muss so konfiguriert sein, dass es mindestens eine PIN und vorzugsweise eine Fingerabdruck-oder Fingerabdruckbiometrie unterstützt. Dadurch wird sichergestellt, dass Windows den Zugriff auf das TPM authentifizieren kann.
- Die Microsoft Edge-Implementierung unterstützt noch nicht die Benutzeroberfläche für die Kontoauswahl.
- Ein zweiter *Filter* Parameter, der die Anmelde Informations-ID angibt, ist derzeit für Anrufe an msCredentials erforderlich. [getassertion](https://msdn.microsoft.com/library/mt697640). Daher müssen Sie Ihre Anmeldeinformationen-ID-Informationen im lokalen Speicher auf dem Client speichern, entweder in indexDB oder localStorage, wenn Sie Ihre Anmeldeinformationen vornehmen. Wenn ein Benutzer seinen Browserverlauf, einschließlich des lokalen Speichers, löscht, muss er sich erneut registrieren, um Windows Hello bei der nächsten Anmeldung zu verwenden.
- Microsoft Edge unterstützt nicht alle Optionen im aktuellen Entwurf einer Webauthentifizierungs Spezifikation, beispielsweise Erweiterungen oder Timeouts.

In diesem letzten Punkt werden die spezifischen Microsoft-Edge-Unterschiede in den folgenden Webauthentifizierungs Spezifikations Definitionen aufgeführt:

### W3C-Spezifikation

```
partial interface Window {
    readonly attribute WebAuthentication webauthn; // msCredentials
};

interface WebAuthentication { // MSCredentials
    Promise <ScopedCredentialInfo> makeCredential (
        Account                                 accountInformation,
        sequence <ScopedCredentialParameters>   cryptoParameters,
        DOMString                               attestationChallenge, // Optional in Microsoft Edge
        optional unsigned long                  credentialTimeoutSeconds, // Not yet supported
        optional sequence <Credential>          blacklist, // Not yet supported
        optional WebAuthnExtensions             credentialExtensions // Not yet supported
    );

    Promise <WebAuthnAssertion> getAssertion (
        DOMString                        assertionChallenge,
        optional unsigned long           assertionTimeoutSeconds, // Not yet supported
        optional sequence <Credential>   whitelist, // Not yet supported
        optional WebAuthnExtensions      assertionExtensions // Not yet supported
    );
};

interface ScopedCredentialInfo { // MSAssertion
    readonly attribute Credential           credential;
    readonly attribute any                  publicKey;
    readonly attribute AttestationStatement attestation;
};

dictionary Account { // MSAccountInfo
    required DOMString rpDisplayName;
    required DOMString displayName;
    DOMString          name; // Not yet supported
    DOMString          id; // Not yet supported
    DOMString          imageUri; // Not yet supported
};

dictionary ScopedCredentialParameters { // MSCredentialParameters
    required CredentialType        type;
    required AlgorithmIdentifier   algorithm;
};

enum CredentialType { // MSCredentialType
    "ScopedCred" // Must be "FIDO_2_0" in Microsoft Edge
};

interface Credential { // MSCredentialSpec
    readonly attribute CredentialType type;
    readonly attribute DOMString      id;
};

dictionary WebAuthnExtensions { // Not supported
};
```



## API-Referenz

[MSCredentials](https://msdn.microsoft.com/library/mt697639)

[makeCredential](https://msdn.microsoft.com/library/mt697641)

[getassertion](https://msdn.microsoft.com/library/mt697640)

## Demos

[Client-und Servercode Beispiele](https://github.com/adrianba/fido-snippets/)

[Webauthn. js Polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[Windows Hello Test Drive-Demo](https://testdrive-fido.azurewebsites.net/)

## Spezifikation

[Webauthentifizierung: eine WebAPI für den Zugriff auf Gültigkeitsbereich-Anmeldeinformationen 1](http://w3c.github.io/webauthn/)  
