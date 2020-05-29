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
# <span data-ttu-id="0e95b-104">Web-Authentifizierung und Windows Hello</span><span class="sxs-lookup"><span data-stu-id="0e95b-104">Web authentication and Windows Hello</span></span>

<span data-ttu-id="0e95b-105">Die Webauthentifizierungs-API (ehemals *Fido 2,0* ) in Microsoft Edge ermöglicht Webanwendungen die Verwendung von [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) Biometrie für die Benutzerauthentifizierung, damit Sie und Ihre Benutzer alle Probleme und Risiken der Kennwortverwaltung vermeiden können, einschließlich der Kenn Wort erraten, Phishing-und Keylogger-Angriffe.</span><span class="sxs-lookup"><span data-stu-id="0e95b-105">The Web Authentication (formerly *FIDO 2.0* ) API in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometrics for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and keylogging attacks.</span></span> <span data-ttu-id="0e95b-106">Die aktuelle Microsoft Edge-Implementierung (*MS-* prefixes) basiert auf einem früheren Entwurf der Webauthentifizierungs Spezifikation und wird sich wahrscheinlich in Zukunft ändern.</span><span class="sxs-lookup"><span data-stu-id="0e95b-106">The current Microsoft Edge (*ms-* prefixed) implementation is based on an earlier draft of the Web Authentication specification and is likely to change in the future.</span></span> **<span data-ttu-id="0e95b-107">In diesem Thema wird gezeigt, wie Sie die Windows Hello-Authentifizierung mit Microsoft Edge testen, während Sie Ihren Code auch in Zukunft für Browser Updates überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0e95b-107">This topic will show you how to try out Windows Hello authentication with Microsoft Edge while also future-proofing your code against browser updates.</span></span>**

<span data-ttu-id="0e95b-108">Die Webauthentifizierungs-API ist ein neuer Standard, der von der [Fido-Allianz](https://fidoalliance.org/) mit dem Ziel bereitgestellt wird, eine interoperable Methode für die Webauthentifizierung mit Windows Hello und anderen biometrischen Geräten in Browsern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0e95b-108">The Web Authentication API is an emerging standard put forth by the [FIDO Alliance](https://fidoalliance.org/) with the aim of providing an interoperable way of doing web authentication using Windows Hello and other biometric devices across browsers.</span></span> <span data-ttu-id="0e95b-109">Die Webauthentifizierungs Spezifikation definiert zwei Authentifizierungsszenarien: Kennwort-less und zwei-Faktor.</span><span class="sxs-lookup"><span data-stu-id="0e95b-109">The Web Authentication specification defines two authentication scenarios: password-less and two factor.</span></span> <span data-ttu-id="0e95b-110">Im Fall eines Kennworts muss sich der Benutzer nicht mit einem Benutzernamen oder Kennwort bei der Webseite anmelden – er kann sich nur mithilfe von Windows Hello anmelden.</span><span class="sxs-lookup"><span data-stu-id="0e95b-110">In the password-less case, the user does not need to log into the web page using a user name or password – they can login solely using Windows Hello.</span></span> <span data-ttu-id="0e95b-111">Im Fall von zwei Faktoren meldet sich der Benutzer normalerweise mit einem Benutzernamen und Kennwort an, aber Windows Hello wird als zweite Faktor Überprüfung verwendet, um die allgemeine Authentifizierung zu verstärken.</span><span class="sxs-lookup"><span data-stu-id="0e95b-111">In the two factor case, the user logs in normally using a username and password, but Windows Hello is used as a second factor check to make the overall authentication stronger.</span></span>

<span data-ttu-id="0e95b-112">Wenn Sie die Webauthentifizierung mit Windows Hello kombinieren, sendet der Server eine unformatierte Text Herausforderung an den Browser.</span><span class="sxs-lookup"><span data-stu-id="0e95b-112">Using Web Authentication combined with Windows Hello, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="0e95b-113">Sobald Microsoft Edge in der Lage ist, den Benutzer über Windows Hello zu überprüfen, signiert das System die Challenge mit einem zuvor für diesen Benutzer bereitgestellten privaten Schlüssel und sendet die Signatur wieder an den Server.</span><span class="sxs-lookup"><span data-stu-id="0e95b-113">Once Microsoft Edge is able to verify the user through Windows Hello, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="0e95b-114">Wenn der Server die Signatur mit dem öffentlichen Schlüssel überprüfen kann, den Sie für diesen Benutzer hat, und überprüfen Sie, ob die Herausforderung richtig ist, kann Sie den Benutzer sicher authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="0e95b-114">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="0e95b-115">Bei [asymmetrischer Kryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography) wie dieser ist der öffentliche Schlüssel für sich selbst bedeutungslos, und der private Schlüssel wird nie freigegeben.</span><span class="sxs-lookup"><span data-stu-id="0e95b-115">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="0e95b-116">Darüber hinaus kann der private Schlüssel nie aus modernen Systemen mit TPM-fähiger Hardware verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="0e95b-116">Furthermore, the private key can never be moved from modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="0e95b-117">Es gibt zwei grundlegende Schritte bei der Verwendung der Web-Authentifizierungs-API:</span><span class="sxs-lookup"><span data-stu-id="0e95b-117">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="0e95b-118">1. registrieren Sie Ihren Nutzer bei</span><span class="sxs-lookup"><span data-stu-id="0e95b-118">1. Register your user with</span></span> `makeCredential`**

**<span data-ttu-id="0e95b-119">2. authentifizieren Sie Ihren Benutzer mit</span><span class="sxs-lookup"><span data-stu-id="0e95b-119">2. Authenticate your user with</span></span> `getAssertion`**

<span data-ttu-id="0e95b-120">Im folgenden werden Sie durch diesen Fluss unter Verwendung der empfohlenen [webauthn. js-Polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)-Anwendung geführt.</span><span class="sxs-lookup"><span data-stu-id="0e95b-120">The following will walk you through this flow using the recommended [Webauthn.js polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span></span> <span data-ttu-id="0e95b-121">Der [vollständige Code](https://github.com/adrianba/fido-snippets/) steht für diese Server-und clientseitige Demo zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0e95b-121">The [complete code](https://github.com/adrianba/fido-snippets/) is available for this server and client side demo.</span></span> <span data-ttu-id="0e95b-122">[C#](https://github.com/adrianba/fido-snippets/tree/master/csharp)-, [php](https://github.com/adrianba/fido-snippets/tree/master/php)-und [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) -serverseitige Versionen sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e95b-122">[C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [PHP](https://github.com/adrianba/fido-snippets/tree/master/php), and [Node.JS](https://github.com/adrianba/fido-snippets/tree/master/nodejs) server side versions are available.</span></span>

## <span data-ttu-id="0e95b-123">Registrieren des Benutzers</span><span class="sxs-lookup"><span data-stu-id="0e95b-123">Register your user</span></span>

<span data-ttu-id="0e95b-124">Wenn Sie als *Identitätsanbieter*fungieren, müssen Sie zuerst eine Webauthentifizierungs Anmeldeinformationen für Ihren Benutzer mit dem Fenster. webauthn erstellen. **makeCredential** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0e95b-124">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the window.webauthn.**makeCredential** method.</span></span> <span data-ttu-id="0e95b-125">Bevor Sie diese Anmeldeinformationen für den Benutzer auf dem Server registrieren, müssen Sie die Identität des Benutzers bestätigen.</span><span class="sxs-lookup"><span data-stu-id="0e95b-125">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="0e95b-126">Dies kann geschehen, wenn Sie dem Nutzer eine Bestätigung per e-Mail senden oder ihn bitten, seine herkömmliche Anmeldemethode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e95b-126">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>

<span data-ttu-id="0e95b-127">Die makeCredential-Methode verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="0e95b-127">The makeCredential method takes the following parameters:</span></span>
 - **<span data-ttu-id="0e95b-128">Informationen zum Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="0e95b-128">user account information</span></span>**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **<span data-ttu-id="0e95b-129">Crypto-Parameter</span><span class="sxs-lookup"><span data-stu-id="0e95b-129">crypto parameters</span></span>**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

<span data-ttu-id="0e95b-130">Die resultierende Versprechung gibt ein Objekt zurück, das die Anmeldeinformationen darstellt, die Sie dann zurück an den Server senden, um zukünftige Authentifizierungen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="0e95b-130">The resulting promise returns an object representing the credential that you then send back to the server for validating future authentications:</span></span>

**<span data-ttu-id="0e95b-131">Client</span><span class="sxs-lookup"><span data-stu-id="0e95b-131">Client</span></span>**

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

<span data-ttu-id="0e95b-132">Wenn Sie die makeCredential-Methode verwenden, fordert Microsoft Edge zunächst Windows Hello auf, die Face-oder Fingerabdruck Kennung zu verwenden, um zu überprüfen, ob der Benutzer derselbe Benutzer wie der beim Windows-Konto angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="0e95b-132">When you use the makeCredential method, Microsoft Edge will first ask Windows Hello to use face or fingerprint identification to verify that the user is the same user as the one logged into the Windows account.</span></span> <span data-ttu-id="0e95b-133">Nach Abschluss dieses Schritts generiert Microsoft Passport ein öffentliches/privates Schlüsselpaar und speichert den privaten Schlüssel im Trusted Platform Module (TPM), der dedizierten Crypto-Prozessor-Hardware, die zum Speichern von Anmeldeinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e95b-133">Once this step is completed, Microsoft Passport will generate a public/private key pair and store the private key in the Trusted Platform Module (TPM), the dedicated crypto processor hardware used to store credentials.</span></span> <span data-ttu-id="0e95b-134">Wenn der Benutzer nicht über ein TPM-fähiges Gerät verfügt, werden diese Schlüssel in der Software gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0e95b-134">If the user doesn’t have a TPM enabled device, these keys will be stored in software.</span></span> <span data-ttu-id="0e95b-135">Diese Anmeldeinformationen werden pro Herkunft, pro Windows-Konto erstellt und werden nicht durchlaufen, weil Sie mit dem Gerät verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="0e95b-135">These credentials are created per origin, per Windows account, and will not be roamed because they are tied to the device.</span></span> <span data-ttu-id="0e95b-136">Das bedeutet, dass Sie sicherstellen müssen, dass der Benutzer sich registriert, um Windows Hello für jedes verwendete Gerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e95b-136">This means that you’ll need to make sure the user registers to use Windows Hello for every device they use.</span></span>

## <span data-ttu-id="0e95b-137">Authentifizieren des Benutzers</span><span class="sxs-lookup"><span data-stu-id="0e95b-137">Authenticate your user</span></span>

<span data-ttu-id="0e95b-138">Nachdem die Anmeldeinformationen auf dem Client erstellt wurden, können Sie das nächste Mal, wenn der Benutzer versucht, sich bei der Website anzumelden, Ihnen anbieten, Sie unter Verwendung von Windows Hello anstelle eines Kennworts mit einem Anruf an Window. webauthn zu signieren. **getassertion**.</span><span class="sxs-lookup"><span data-stu-id="0e95b-138">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using Windows Hello instead of a password with a call to window.webauthn.**getAssertion**.</span></span>

<span data-ttu-id="0e95b-139">Die getassertion-Methode nimmt die *Herausforderung* als einzigen erforderlichen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="0e95b-139">The getAssertion method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="0e95b-140">Die Herausforderung ist die nach dem Zufallsprinzip generierte Menge, die vom Server an einen Client gesendet wird, um mit dem privaten Schlüssel des Benutzers zu signieren.</span><span class="sxs-lookup"><span data-stu-id="0e95b-140">The challenge is the randomly generated quantity that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="0e95b-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0e95b-141">For example:</span></span>

**<span data-ttu-id="0e95b-142">Server</span><span class="sxs-lookup"><span data-stu-id="0e95b-142">Server</span></span>**

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

<span data-ttu-id="0e95b-143">Nachdem der getassertions-Anruf durchgeführt wurde, zeigt Microsoft Edge die Windows Hello-Eingabeaufforderung an, mit der die Identität des Benutzers über die Biometrie überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="0e95b-143">Once the getAssertion call is made, Microsoft Edge will show the Windows Hello prompt, which will verify the identity of the user using biometrics.</span></span> <span data-ttu-id="0e95b-144">Nachdem der Benutzer überprüft wurde, wird die Herausforderung im TPM signiert, und die Versprechung wird mit einem Assertions Objekt zurückgegeben, das die Signatur und andere Metadaten enthält, die Sie an den Server senden möchten:</span><span class="sxs-lookup"><span data-stu-id="0e95b-144">After the user is verified, the challenge will be signed within the TPM and the promise will return with an assertion object that contains the signature and other metadata for you to send to the server:</span></span>

**<span data-ttu-id="0e95b-145">Client</span><span class="sxs-lookup"><span data-stu-id="0e95b-145">Client</span></span>**

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

<span data-ttu-id="0e95b-146">Nachdem Sie die Assertion auf dem Server erhalten haben, müssen Sie die Signatur überprüfen, um den Benutzer zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="0e95b-146">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="0e95b-147">Beispiel (in Node. js):</span><span class="sxs-lookup"><span data-stu-id="0e95b-147">For example (in Node.JS):</span></span>

**<span data-ttu-id="0e95b-148">Server</span><span class="sxs-lookup"><span data-stu-id="0e95b-148">Server</span></span>**

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

## <span data-ttu-id="0e95b-149">Unterschiede zwischen Microsoft Edge und der Spezifikation</span><span class="sxs-lookup"><span data-stu-id="0e95b-149">Differences between Microsoft Edge and the spec</span></span>

> [!NOTE]
> <span data-ttu-id="0e95b-150">Wenn Sie die Webauthentifizierungs-API mit Windows Hello in Microsoft Edge testen, empfehlen wir die Verwendung von webauthen. js Polyfill wie oben beschrieben, um zu vermeiden, dass Sie die hier aufgelisteten Diskrepanzen berücksichtigen müssen.</span><span class="sxs-lookup"><span data-stu-id="0e95b-150">When trying out the Web Authentication API with Windows Hello in Microsoft Edge, we recommend using the Webauthn.js polyfill as shown above to avoid having to account for the discrepancies listed here.</span></span> <span data-ttu-id="0e95b-151">Wir aktualisieren diese Polyfill-Datei für jede wichtige veröffentlichte Version der Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="0e95b-151">We'll update this polyfill for every major published version of the specification.</span></span>


<span data-ttu-id="0e95b-152">Die aktuelle Microsoft Edge-Implementierung basiert auf einem früheren Entwurf der Webauthentifizierungs Spezifikation und wird sich wahrscheinlich in zukünftigen Builds ändern, während sich die Spezifikation entwickelt.</span><span class="sxs-lookup"><span data-stu-id="0e95b-152">The current Microsoft Edge implementation is based on an earlier draft of the Web Authentication specification and is likely to change in future builds and as the spec evolves.</span></span> <span data-ttu-id="0e95b-153">Zu den aktuellen Unterschieden gehören:</span><span class="sxs-lookup"><span data-stu-id="0e95b-153">The current differences include:</span></span>

- <span data-ttu-id="0e95b-154">Microsoft Edge-APIs sind MS-Präfixe.</span><span class="sxs-lookup"><span data-stu-id="0e95b-154">Microsoft Edge APIs are MS- prefixed.</span></span>
- <span data-ttu-id="0e95b-155">Microsoft Edge unterstützt noch keine externen Anmeldeinformationen wie USB-Schlüssel oder Bluetooth-Geräte.</span><span class="sxs-lookup"><span data-stu-id="0e95b-155">Microsoft Edge does not yet support external credentials like USB keys or Bluetooth devices.</span></span> <span data-ttu-id="0e95b-156">Die aktuelle API ist auf eingebettete im TPM gespeicherte Anmeldeinformationen limitiert.</span><span class="sxs-lookup"><span data-stu-id="0e95b-156">The current API is limited to embedded credentials stored in the TPM.</span></span>
- <span data-ttu-id="0e95b-157">Das aktuell angemeldete Windows-Benutzerkonto muss so konfiguriert sein, dass es mindestens eine PIN und vorzugsweise eine Fingerabdruck-oder Fingerabdruckbiometrie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e95b-157">The currently logged in Windows user account must be configured to support at least a PIN, and preferably face or fingerprint biometrics.</span></span> <span data-ttu-id="0e95b-158">Dadurch wird sichergestellt, dass Windows den Zugriff auf das TPM authentifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="0e95b-158">This is to ensure that Windows can authenticate the access to the TPM.</span></span>
- <span data-ttu-id="0e95b-159">Die Microsoft Edge-Implementierung unterstützt noch nicht die Benutzeroberfläche für die Kontoauswahl.</span><span class="sxs-lookup"><span data-stu-id="0e95b-159">The Microsoft Edge implementation does not yet support the account picker experience.</span></span>
- <span data-ttu-id="0e95b-160">Ein zweiter *Filter* Parameter, der die Anmelde Informations-ID angibt, ist derzeit für Anrufe an msCredentials erforderlich. [getassertion](https://msdn.microsoft.com/library/mt697640).</span><span class="sxs-lookup"><span data-stu-id="0e95b-160">A second *filters* parameter specifying the credential id is currently required for calls to msCredentials.[getAssertion](https://msdn.microsoft.com/library/mt697640).</span></span> <span data-ttu-id="0e95b-161">Daher müssen Sie Ihre Anmeldeinformationen-ID-Informationen im lokalen Speicher auf dem Client speichern, entweder in indexDB oder localStorage, wenn Sie Ihre Anmeldeinformationen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0e95b-161">As such, you’ll need to store your credential ID information in local storage on the client, either in indexDB or localStorage when making your credential.</span></span> <span data-ttu-id="0e95b-162">Wenn ein Benutzer seinen Browserverlauf, einschließlich des lokalen Speichers, löscht, muss er sich erneut registrieren, um Windows Hello bei der nächsten Anmeldung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e95b-162">If a user deletes their browsing history, including local storage, they will need to re-register to use Windows Hello the next time they log in.</span></span>
- <span data-ttu-id="0e95b-163">Microsoft Edge unterstützt nicht alle Optionen im aktuellen Entwurf einer Webauthentifizierungs Spezifikation, beispielsweise Erweiterungen oder Timeouts.</span><span class="sxs-lookup"><span data-stu-id="0e95b-163">Microsoft Edge does not support all of the options in the current Web Authentication specification draft, such as extensions or timeouts.</span></span>

<span data-ttu-id="0e95b-164">In diesem letzten Punkt werden die spezifischen Microsoft-Edge-Unterschiede in den folgenden Webauthentifizierungs Spezifikations Definitionen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="0e95b-164">On that last point, the specific Microsoft Edge differences are noted in the following Web Authentication spec definitions:</span></span>

### <span data-ttu-id="0e95b-165">W3C-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="0e95b-165">W3C spec</span></span>

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



## <span data-ttu-id="0e95b-166">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="0e95b-166">API Reference</span></span>

[<span data-ttu-id="0e95b-167">MSCredentials</span><span class="sxs-lookup"><span data-stu-id="0e95b-167">MSCredentials</span></span>](https://msdn.microsoft.com/library/mt697639)

[<span data-ttu-id="0e95b-168">makeCredential</span><span class="sxs-lookup"><span data-stu-id="0e95b-168">makeCredential</span></span>](https://msdn.microsoft.com/library/mt697641)

[<span data-ttu-id="0e95b-169">getassertion</span><span class="sxs-lookup"><span data-stu-id="0e95b-169">getAssertion</span></span>](https://msdn.microsoft.com/library/mt697640)

## <span data-ttu-id="0e95b-170">Demos</span><span class="sxs-lookup"><span data-stu-id="0e95b-170">Demos</span></span>

[<span data-ttu-id="0e95b-171">Client-und Servercode Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e95b-171">Client and server code samples</span></span>](https://github.com/adrianba/fido-snippets/)

[<span data-ttu-id="0e95b-172">Webauthn. js Polyfill</span><span class="sxs-lookup"><span data-stu-id="0e95b-172">Webauthn.js polyfill</span></span>](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[<span data-ttu-id="0e95b-173">Windows Hello Test Drive-Demo</span><span class="sxs-lookup"><span data-stu-id="0e95b-173">Windows Hello Test Drive demo</span></span>](https://testdrive-fido.azurewebsites.net/)

## <span data-ttu-id="0e95b-174">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="0e95b-174">Specification</span></span>

[<span data-ttu-id="0e95b-175">Webauthentifizierung: eine WebAPI für den Zugriff auf Gültigkeitsbereich-Anmeldeinformationen 1</span><span class="sxs-lookup"><span data-stu-id="0e95b-175">Web Authentication: A Web API for accessing scoped credentials 1</span></span>](http://w3c.github.io/webauthn/)  
