---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Erfahren Sie, wie die Webauthentifizierungs-API Webanwendungen die Verwendung von Windows Hello und FIDO2 für die Benutzerauthentifizierung ermöglichen kann.
title: Webauthentifizierung – Entwicklerhandbuch
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 07f1de47156f43ff4726e8907a123c2cb1afc337
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233840"
---
# <span data-ttu-id="e39f7-104">Web-Authentifizierung und Windows Hello</span><span class="sxs-lookup"><span data-stu-id="e39f7-104">Web Authentication and Windows Hello</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="e39f7-105">Die [Webauthentifizierungs-API](https://w3c.github.io/webauthn) in Microsoft Edge ermöglicht Webanwendungen die Verwendung von [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) -und [externen FIDO2-Geräten](https://fidoalliance.org/fido2) für die Benutzerauthentifizierung, damit Sie und Ihre Benutzer alle Probleme und Risiken der Kennwortverwaltung vermeiden können, einschließlich der Kenn Wort erraten, Phishing-Angriffe und Angriffe auf die Schlüsselprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="e39f7-105">The [Web Authentication API](https://w3c.github.io/webauthn) in Microsoft Edge enables web applications to use [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) and [external FIDO2 devices](https://fidoalliance.org/fido2) for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and key-logging attacks.</span></span>  <span data-ttu-id="e39f7-106">Die aktuelle Microsoft Edge-Implementierung basiert auf der Kandidaten Empfehlung der Webauthentifizierungs Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e39f7-106">The current Microsoft Edge implementation is based on the Candidate Recommendation of the Web Authentication specification.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="e39f7-107">In diesem Thema wird gezeigt, wie Sie die Windows Hello-und FIDO2-Authentifizierung mit Microsoft Edge testen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-107">This topic will show you how to try out Windows Hello and FIDO2 authentication with Microsoft Edge.</span></span>  

<span data-ttu-id="e39f7-108">Mithilfe der Webauthentifizierung sendet der Server eine unformatierte Text Herausforderung an den Browser.</span><span class="sxs-lookup"><span data-stu-id="e39f7-108">Using Web Authentication, the server sends down a plain text challenge to the browser.</span></span>  <span data-ttu-id="e39f7-109">Sobald Microsoft Edge in der Lage ist, den Benutzer über Windows Hello oder ein externes FIDO2-Gerät zu verifizieren, signiert das System die Challenge mit einem zuvor für diesen Benutzer bereitgestellten privaten Schlüssel und sendet die Signatur zurück an den Server.</span><span class="sxs-lookup"><span data-stu-id="e39f7-109">Once Microsoft Edge is able to verify the user through Windows Hello or an external FIDO2 device, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span>  <span data-ttu-id="e39f7-110">Wenn der Server die Signatur mit dem öffentlichen Schlüssel überprüfen kann, den Sie für diesen Benutzer hat, und überprüfen Sie, ob die Herausforderung richtig ist, kann Sie den Benutzer sicher authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e39f7-110">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span>  <span data-ttu-id="e39f7-111">Bei [asymmetrischer Kryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography) wie dieser ist der öffentliche Schlüssel für sich selbst bedeutungslos, und der private Schlüssel wird nie freigegeben.</span><span class="sxs-lookup"><span data-stu-id="e39f7-111">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span>  <span data-ttu-id="e39f7-112">Darüber hinaus kann der private Schlüssel nie aus sicheren Elementen oder modernen Systemen mit TPM-fähiger Hardware verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="e39f7-112">Furthermore, the private key can never be moved from secure elements or modern systems with TPM-enabled hardware.</span></span>  

<span data-ttu-id="e39f7-113">Es gibt zwei grundlegende Schritte bei der Verwendung der Web-Authentifizierungs-API:</span><span class="sxs-lookup"><span data-stu-id="e39f7-113">There are two basic steps to using the Web Authentication API:</span></span>  

1.  <span data-ttu-id="e39f7-114">Registrieren Ihres Benutzers bei</span><span class="sxs-lookup"><span data-stu-id="e39f7-114">Register your user with</span></span> `create`  
1.  <span data-ttu-id="e39f7-115">Authentifizieren des Benutzers mit</span><span class="sxs-lookup"><span data-stu-id="e39f7-115">Authenticate your user with</span></span> `get`  

<span data-ttu-id="e39f7-116">Das folgende dev-Handbuch führt Sie durch diesen Fluss mit der [webauthn-Beispiel-App](https://github.com/MicrosoftEdge/webauthnsample).</span><span class="sxs-lookup"><span data-stu-id="e39f7-116">The following dev guide will walk you through this flow using the [WebAuthn Sample App](https://github.com/MicrosoftEdge/webauthnsample).</span></span>  

## <span data-ttu-id="e39f7-117">Registrieren des Benutzers</span><span class="sxs-lookup"><span data-stu-id="e39f7-117">Register your user</span></span>  

<span data-ttu-id="e39f7-118">Wenn Sie als Identitätsanbieter fungieren, müssen Sie zuerst eine Webauthentifizierungs Anmeldeinformationen für den Benutzer mit der `navigator.credentials.create` Methode erstellen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-118">Acting as an identity provider, you will first need to create a Web Authentication credential for your user with the `navigator.credentials.create` method.</span></span>  <span data-ttu-id="e39f7-119">Bevor Sie diese Anmeldeinformationen für den Benutzer auf dem Server registrieren, müssen Sie die Identität des Benutzers bestätigen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-119">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span>  <span data-ttu-id="e39f7-120">Dies kann geschehen, wenn Sie dem Nutzer eine Bestätigung per e-Mail senden oder ihn bitten, seine herkömmliche Anmeldemethode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e39f7-120">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>  

<span data-ttu-id="e39f7-121">Die `create` Methode verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="e39f7-121">The `create` method takes the following parameters:</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="e39f7-122">Informationen zur vertrauenden Seite</span><span class="sxs-lookup"><span data-stu-id="e39f7-122">relying party information</span></span>**  
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
      **<span data-ttu-id="e39f7-123">Informationen zum Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="e39f7-123">user account information</span></span>**  
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
      **<span data-ttu-id="e39f7-124">Crypto-Parameter</span><span class="sxs-lookup"><span data-stu-id="e39f7-124">crypto parameters</span></span>**  
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
      **<span data-ttu-id="e39f7-125">Authentifikator-Auswahlparameter</span><span class="sxs-lookup"><span data-stu-id="e39f7-125">authenticator selection parameters</span></span>**  
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
      **<span data-ttu-id="e39f7-126">Weitere Optionen</span><span class="sxs-lookup"><span data-stu-id="e39f7-126">other options</span></span>**  
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

<span data-ttu-id="e39f7-127">Sie können [Anmelde Informations Erstellungsparameter](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) verwenden, um die Anmeldeinformationen zu konfigurieren, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e39f7-127">You can use [credential creation parameters](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) to configure the credential you want to create.</span></span>  <span data-ttu-id="e39f7-128">Insbesondere können Sie auswählen, ob Sie eine Windows Hello-Anmeldeinformationen erstellen möchten, indem Sie auf ein `authenticatorAttachment` `platform` externes FIDO2-Gerät oder auf ein Roaming-Anmeldeinformationen festlegen `authenticatorAttachment` `cross-platform` .</span><span class="sxs-lookup"><span data-stu-id="e39f7-128">In particular, you can choose to create a Windows Hello credential by setting `authenticatorAttachment` to `platform`, or a roaming credential on an external FIDO2 device by setting `authenticatorAttachment` to `cross-platform`.</span></span>  

<span data-ttu-id="e39f7-129">Wenn Sie die `create` Methode verwenden, fordert Microsoft Edge zunächst den Benutzer auf, seinen Anwesenheitsstatus zu überprüfen, indem er sein Angesicht oder seinen Fingerabdruck scannt, eine PIN eingibt oder auf einem externen FIDO2-Gerät eine Aktion durchführt.</span><span class="sxs-lookup"><span data-stu-id="e39f7-129">When you use the `create` method, Microsoft Edge will first ask the user to verify their presence by scanning their face or fingerprint, entering a PIN, or taking action on an external FIDO2 device.</span></span>  <span data-ttu-id="e39f7-130">Nach Abschluss dieses Schritts generiert der Authentifikator ein publicprivate-Schlüsselpaar und speichert den privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e39f7-130">Once this step is completed the authenticator will generate a publicprivate key pair and store the private key.</span></span>  <span data-ttu-id="e39f7-131">Diese Anmeldeinformationen werden pro Herkunft und Konto erstellt und können nicht extrahiert werden, da Sie sicher auf dem Authentifizierungsgerät gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e39f7-131">These credentials are created per origin, per account, and cannot be extracted because they are stored securely to the authentication device.</span></span>  

<span data-ttu-id="e39f7-132">Die resultierende Versprechung gibt ein [Testat-Objekt](https://w3c.github.io/webauthn#sctn-attestation) zurück, das die neuen Anmeldeinformationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="e39f7-132">The resulting promise returns an [attestation object](https://w3c.github.io/webauthn#sctn-attestation) representing the new credential.</span></span>  <span data-ttu-id="e39f7-133">Das Testat-Objekt enthält den öffentlichen Schlüssel für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-133">The attestation object contains the public key for the credential.</span></span>  <span data-ttu-id="e39f7-134">Sie senden dieses Objekt an den Server, um zukünftige Authentifizierungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-134">You'll send this object to the server for validating future authentications.</span></span>  <span data-ttu-id="e39f7-135">Bevor Sie zum Server zurückkehren, müssen Sie die unformatierten Daten Base64-codiert codieren.</span><span class="sxs-lookup"><span data-stu-id="e39f7-135">Before sending back to the server, you'll need to base64-encode the raw data.</span></span>  

**<span data-ttu-id="e39f7-136">Client</span><span class="sxs-lookup"><span data-stu-id="e39f7-136">Client</span></span>**  

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

<span data-ttu-id="e39f7-137">Der Server sollte dann das Bestätigungs Objekt decodieren, Überprüfungsschritte ausführen, den öffentlichen Schlüssel für diese Anmeldeinformationen extrahieren und für zukünftige Authentifizierungen speichern.</span><span class="sxs-lookup"><span data-stu-id="e39f7-137">The server should then decode the attestation object, perform verification steps, extract the public key for this credential, and store it for future authentications.</span></span>  <span data-ttu-id="e39f7-138">Eine detaillierte Liste der Schritte finden Sie im Algorithmus zur [Registrierung von Anmeldeinformationen](https://w3c.github.io/webauthn#registering-a-new-credential) in der webauthn-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e39f7-138">A detailed list of steps can be found in the [credential registration algorithm](https://w3c.github.io/webauthn#registering-a-new-credential) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="e39f7-139">Server</span><span class="sxs-lookup"><span data-stu-id="e39f7-139">Server</span></span>**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## <span data-ttu-id="e39f7-140">Authentifizieren des Benutzers</span><span class="sxs-lookup"><span data-stu-id="e39f7-140">Authenticate your user</span></span>  

<span data-ttu-id="e39f7-141">Nachdem die Anmeldeinformationen auf dem Client erstellt wurden, können Sie das nächste Mal, wenn der Benutzer versucht, sich bei der Website anzumelden, Ihnen anbieten, diese mithilfe ihrer Webauthentifizierungs Anmeldeinformationen anstelle eines Kennworts mit einem Anruf an zu signieren `navigator.credentials.get` .</span><span class="sxs-lookup"><span data-stu-id="e39f7-141">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using their Web Authentication credential instead of a password with a call to `navigator.credentials.get`.</span></span>  

<span data-ttu-id="e39f7-142">Die `get` Methode nimmt die Herausforderung als einzigen erforderlichen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="e39f7-142">The `get` method takes the challenge as its only required parameter.</span></span>  <span data-ttu-id="e39f7-143">Die Herausforderung ist eine undurchsichtige Bytefolge, die vom Server an einen Client gesendet wird, um mit dem privaten Schlüssel des Benutzers zu signieren.</span><span class="sxs-lookup"><span data-stu-id="e39f7-143">The challenge is an opaque sequence of bytes that the server will send down to a client to sign with the user's private key.</span></span>  <span data-ttu-id="e39f7-144">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e39f7-144">For example:</span></span>  

**<span data-ttu-id="e39f7-145">Server</span><span class="sxs-lookup"><span data-stu-id="e39f7-145">Server</span></span>**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

<span data-ttu-id="e39f7-146">Nachdem Sie eine Herausforderung vom Server abgerufen haben, rufen Sie die Get-API zusammen mit den Optionen für die [Anmelde Informationsanforderung](https://w3c.github.io/webauthn#credentialrequestoptions-extension)auf.</span><span class="sxs-lookup"><span data-stu-id="e39f7-146">After retrieving a challenge from the server, you'll call the get API along with [credential request options](https://w3c.github.io/webauthn#credentialrequestoptions-extension).</span></span>  <span data-ttu-id="e39f7-147">Microsoft Edge zeigt eine Aufforderung an, mit der die Identität des Benutzers mit Windows Hello oder einem externen FIDO2-Gerät überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="e39f7-147">Microsoft Edge will show a prompt, which will verify the identity of the user using Windows Hello or an external FIDO2 device.</span></span>  <span data-ttu-id="e39f7-148">Nachdem der Benutzer überprüft wurde, wird die Herausforderung innerhalb des TPM-oder FIDO2-Geräts signiert, und die Versprechung wird mit einem [Assertions Objekt](https://w3c.github.io/webauthn#authenticatorassertionresponse) zurückgegeben, das die Signatur und andere Metadaten enthält, die Sie an den Server senden.</span><span class="sxs-lookup"><span data-stu-id="e39f7-148">After the user is verified, the challenge will be signed within the TPM or FIDO2 device and the promise will return with an [assertion object](https://w3c.github.io/webauthn#authenticatorassertionresponse) that contains the signature and other metadata for you to send to the server.</span></span>  

**<span data-ttu-id="e39f7-149">Client</span><span class="sxs-lookup"><span data-stu-id="e39f7-149">Client</span></span>**  

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

<span data-ttu-id="e39f7-150">Nachdem Sie die Assertion auf dem Server erhalten haben, müssen Sie die Signatur überprüfen, um den Benutzer zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e39f7-150">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span>  <span data-ttu-id="e39f7-151">Im folgenden sind einige Beispielcodes zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="e39f7-151">The following is some sample code.</span></span>  <span data-ttu-id="e39f7-152">Eine detaillierte Liste der Schritte finden Sie im Algorithmus zur [Assertionsüberprüfung](https://w3c.github.io/webauthn#verifying-assertion) in der webauthn-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e39f7-152">A detailed list of steps can be found in the [assertion verification algorithm](https://w3c.github.io/webauthn#verifying-assertion) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="e39f7-153">Server</span><span class="sxs-lookup"><span data-stu-id="e39f7-153">Server</span></span>**  

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

## <span data-ttu-id="e39f7-154">Implementierungshinweise</span><span class="sxs-lookup"><span data-stu-id="e39f7-154">Implementation notes</span></span>  

### <span data-ttu-id="e39f7-155">Unterstützte Plattformen</span><span class="sxs-lookup"><span data-stu-id="e39f7-155">Supported platforms</span></span>  

*   <span data-ttu-id="e39f7-156">Die Version der Kandidaten Empfehlung der Webauthentifizierungs-API kann von Microsoft Edge beginnend mit EdgeHTML 18 \ (Windows Insider Preview-Version 17713 oder höher) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e39f7-156">The Candidate Recommendation version of the Web Authentication API can be used from Microsoft Edge beginning with EdgeHTML 18 \(Windows Insider Preview version 17713 or newer\).</span></span>  
*   <span data-ttu-id="e39f7-157">Die vorangestellte [Preview-Version](https://blogs.windows.com/msedgedev/2016/04/12) der Webauthentifizierungs-API wurde entfernt und steht nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e39f7-157">The [prefixed, preview version](https://blogs.windows.com/msedgedev/2016/04/12) of the Web Authentication API has been removed and is no longer available.</span></span>  
*   <span data-ttu-id="e39f7-158">Die Webauthentifizierungs-API steht für UWP-apps und-PWAs noch nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e39f7-158">The Web Authentication API is not yet available to UWP apps and PWAs.</span></span>  
*   <span data-ttu-id="e39f7-159">Internet Explorer unterstützt die Webauthentifizierungs-API nicht.</span><span class="sxs-lookup"><span data-stu-id="e39f7-159">Internet Explorer does not support the Web Authentication API.</span></span>  

### <span data-ttu-id="e39f7-160">Unterstützte Authentifikatoren</span><span class="sxs-lookup"><span data-stu-id="e39f7-160">Supported authenticators</span></span>  

<span data-ttu-id="e39f7-161">Mit der Web-Authentifizierungs-API in Microsoft Edge können Sie Benutzer mit den folgenden Technologien authentifizieren:</span><span class="sxs-lookup"><span data-stu-id="e39f7-161">With the Web Authentication API in Microsoft Edge, you can authenticate users with the following technologies:</span></span>  

*   <span data-ttu-id="e39f7-162">**Windows Hello**  Ermöglicht die kennwortgeschützte Authentifizierung auf einem Gerät mit Face, Fingerabdruck oder PIN</span><span class="sxs-lookup"><span data-stu-id="e39f7-162">**Windows Hello**  Enables passwordless on-device authentication with  face, fingerprint, or PIN</span></span>  
*   <span data-ttu-id="e39f7-163">**FIDO2**  Ermöglicht die kennwortlos-Roaming-Authentifizierung mit einem Wechselmedium und einem Fingerabdruck oder einer PIN</span><span class="sxs-lookup"><span data-stu-id="e39f7-163">**FIDO2**  Enables passwordless roaming authentication with a removable device and a fingerprint or PIN</span></span>  
*   <span data-ttu-id="e39f7-164">**U2F**  Ermöglicht eine starke Authentifizierung des zweiten Faktors für Websites, die nicht bereit sind, zu einem Kenn Wort unfähigen Modell zu wechseln</span><span class="sxs-lookup"><span data-stu-id="e39f7-164">**U2F**  Enables strong second factor authentication for websites that are not ready to move to a passwordless model</span></span>  

### <span data-ttu-id="e39f7-165">Besondere Überlegungen für Windows Hello</span><span class="sxs-lookup"><span data-stu-id="e39f7-165">Special considerations for Windows Hello</span></span>  

<span data-ttu-id="e39f7-166">Einige Dinge, die Sie bei der Verwendung des Windows Hello-Authentifikators beachten sollten:</span><span class="sxs-lookup"><span data-stu-id="e39f7-166">A few things to note when using the Windows Hello authenticator:</span></span>  

*   <span data-ttu-id="e39f7-167">Sie können feststellen, ob Windows Hello auf einem PC verfügbar ist, indem Sie die `isUserVerifyingPlatformAuthenticatorAvailable` API aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-167">You can detect if Windows Hello is available on a PC by calling the `isUserVerifyingPlatformAuthenticatorAvailable` API.</span></span>  <span data-ttu-id="e39f7-168">Weitere Informationen zu dieser API [finden Sie hier](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).</span><span class="sxs-lookup"><span data-stu-id="e39f7-168">Learn more about this API [here](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).</span></span>  
*   <span data-ttu-id="e39f7-169">Wenn Sie eine Anmeldeinformationen für Windows Hello erstellen, sollten `authenticatorAttachment` Sie `platform` für eine optimale Benutzererfahrung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-169">When creating a credential for Windows Hello, you should set `authenticatorAttachment` to `platform` for the best user experience.</span></span>
*   <span data-ttu-id="e39f7-170">Windows Hello unterstützt nur RS256 \ (AIG-257 \) als öffentlichen Schlüsselalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="e39f7-170">Windows Hello only supports RS256 \(alg -257\) as its public key algorithm.</span></span>  <span data-ttu-id="e39f7-171">Stellen Sie sicher, dass Sie bei der Erstellung von Anmeldeinformationen diesen Algorithmus angeben.</span><span class="sxs-lookup"><span data-stu-id="e39f7-171">Be sure to specify this algorithm when creating a credential.</span></span>  
*   <span data-ttu-id="e39f7-172">Um eine [TPM-Bestätigungsanweisung](https://w3c.github.io/webauthn#tpm-attestation)zu erhalten, legen Sie die Bescheinigung beim Aufrufen der API auf "Direct" fest `create` .</span><span class="sxs-lookup"><span data-stu-id="e39f7-172">To receive a [TPM attestation statement](https://w3c.github.io/webauthn#tpm-attestation), set attestation to "direct" when calling the `create` API.</span></span>  <span data-ttu-id="e39f7-173">Die TPM-Bescheinigung ist ein optimaler Aufwand.</span><span class="sxs-lookup"><span data-stu-id="e39f7-173">TPM attestation is a best effort.</span></span>  <span data-ttu-id="e39f7-174">Nur PCs mit TPM 2,0 geben eine TPM-Bestätigungsanweisung zurück, und der Bestätigungsprozess kann aus verschiedenen Gründen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-174">Only PCs with TPM 2.0 will return a TPM attestation statement, and the attestation process could fail for a variety of reasons.</span></span>  
*   <span data-ttu-id="e39f7-175">Windows Hello verwendet verschiedene Möglichkeiten, um Benutzeranmeldeinformationen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="e39f7-175">Windows Hello employs a variety of ways to protect user credentials.</span></span>  <span data-ttu-id="e39f7-176">Sie können überprüfen, welche Methode zum Schützen von Anmeldeinformationen verwendet wurde, indem Sie das [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) -Feld im Bestätigungs Objekt verwenden, das bei der Erstellung von Anmeldeinformationen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e39f7-176">You can check which method has been used to protect a credential by consuming the [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) field in the attestation object returned at credential creation.</span></span>  <span data-ttu-id="e39f7-177">Die folgende Liste enthält die AAGUIDs, die von Windows Hello zurückgegeben werden können:</span><span class="sxs-lookup"><span data-stu-id="e39f7-177">The following is the list of AAGUIDs that Windows Hello may return:</span></span>   
    *   <span data-ttu-id="e39f7-178">Software-gesicherte Authentifikatoren</span><span class="sxs-lookup"><span data-stu-id="e39f7-178">Software backed authenticators</span></span>  
        *   <span data-ttu-id="e39f7-179">Windows Hello-Software-Authentifikator:</span><span class="sxs-lookup"><span data-stu-id="e39f7-179">Windows Hello software authenticator:</span></span>  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   <span data-ttu-id="e39f7-180">Windows Hello VBS-Software-Authentifikator:</span><span class="sxs-lookup"><span data-stu-id="e39f7-180">Windows Hello VBS software authenticator:</span></span>  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   <span data-ttu-id="e39f7-181">Vertrauenswürdiges Plattformmodul \ (TPM \) gesicherte Authentifikatoren</span><span class="sxs-lookup"><span data-stu-id="e39f7-181">Trusted Platform Module \(TPM\) backed authenticators</span></span>  
        *   <span data-ttu-id="e39f7-182">Windows Hello-Hardware-Authentifikator:</span><span class="sxs-lookup"><span data-stu-id="e39f7-182">Windows Hello hardware authenticator:</span></span>  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   <span data-ttu-id="e39f7-183">Windows Hello VBS-Hardware-Authentifikator:</span><span class="sxs-lookup"><span data-stu-id="e39f7-183">Windows Hello VBS hardware authenticator:</span></span>  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### <span data-ttu-id="e39f7-184">API-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="e39f7-184">API surface</span></span>  

*   <span data-ttu-id="e39f7-185">Microsoft Edge verfügt über eine vollständige Implementierung der Kandidaten Empfehlungs Version der Core Web Authentication-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e39f7-185">Microsoft Edge has a complete implementation of the Candidate Recommendation version of the core Web Authentication specification.</span></span>  
*   <span data-ttu-id="e39f7-186">Die [Erweiterung](https://w3c.github.io/webauthn#sctn-appid-extension) für die Erweiterung wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e39f7-186">The [AppID extension](https://w3c.github.io/webauthn#sctn-appid-extension) is supported.</span></span>  
*   <span data-ttu-id="e39f7-187">Es werden keine weiteren Erweiterungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e39f7-187">No other extensions are supported.</span></span>  

## <span data-ttu-id="e39f7-188">Demos</span><span class="sxs-lookup"><span data-stu-id="e39f7-188">Demos</span></span>  

[<span data-ttu-id="e39f7-189">Beispiel für Client-und Servercode</span><span class="sxs-lookup"><span data-stu-id="e39f7-189">Client and server code sample</span></span>](https://github.com/MicrosoftEdge/webauthnsample)  

[<span data-ttu-id="e39f7-190">Windows Hello Test Drive-Demo</span><span class="sxs-lookup"><span data-stu-id="e39f7-190">Windows Hello Test Drive demo</span></span>](https://webauthnsample.azurewebsites.net)  

## <span data-ttu-id="e39f7-191">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e39f7-191">Specification</span></span>  

[<span data-ttu-id="e39f7-192">Webauthentifizierung: eine API für den Zugriff auf öffentliche Schlüssel-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e39f7-192">Web Authentication: An API for accessing Public Key Credentials</span></span>](http://w3c.github.io/webauthn)  
