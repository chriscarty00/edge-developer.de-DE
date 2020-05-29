---
description: Erfahren Sie, wie thePayment Request APIenables Microsoft Edge als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden für Verbraucher in der Cloud fungiert.
title: Dev Guide-API für Zahlungsanforderungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 75c596570a222336a4ba0c371acb8770f97804ee
ms.sourcegitcommit: e690bb4d1cb9e73c93b468c9f55d91ea6fb6c654
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/10/2020
ms.locfileid: "10568745"
---
# API für Zahlungsanforderungen

E-Commerce-Umsätze wachsen weiterhin rasant. Laut [eMarketer](https://www.emarketer.com/)wird der digitale Umsatz von 2018 um 23% auf die in 2013 gemessenen Werte steigen.  Während Verbraucher und Unternehmen den Vorteil von e-Commerce-Verkäufen genießen, bestehen weiterhin Herausforderungen.  Heute muss jeder e-Commerce-Websitebesitzer Zeit investieren, um qualitativ hochwertige Zahlungs Checkout-Abläufe und Gültigkeitsprüfungsregeln zu entwickeln.  Verbraucher müssen in verschiedenen Zahlungs Auszahlungs strömen navigieren und die gleichen Zahlungs-und Versandinformationen auf jeder Website, auf der Sie einkaufen, erneut eingeben.  Dies kann für die Verbraucher zeitaufwendig und frustrierend sein, was zu einer großen Anzahl von Einkaufswagen und verminderten Verkäufen für Händler führt. Händler [schätzen](http://baymard.com/lists/cart-abandonment-rate) , dass zwischen 60% und 70% der Einkaufswagen aufgegeben werden.      

Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request/) standardisiert den Zahlungs Checkout-Prozess. Diese API erfordert weniger benutzerdefinierte Anpassungen für Webentwickler und bietet eine schnellere, konsistentere und daher weniger verwirrende Benutzeroberfläche.  Da die Verbraucher Zahlungsinstrumente und Versandadressen von Ihrem Microsoft-Konto aus auswählen können, müssen Sie weniger Daten eingeben, um Käufe abzuschließen, wodurch die Zeit und die Dateneingabe reduziert werden, die zum Abschließen einer Zahlung erforderlich sind.   

Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request/) ist ein offener, browserübergreifender Standard, der es Browsern ermöglicht, als Vermittler zwischen Händlern, Verbrauchern und den Zahlungsmethoden (z.b. Kreditkarten) zu fungieren, die Verbraucher in der Cloud gespeichert haben. 
  
Zusammenfassend können die Kunden bei der Verwendung der [API für Zahlungsanforderungen](https://w3.org/TR/payment-request/)wie gewohnt auf Händler Websites einkaufen.  Wenn Sie zur Zahlung bereit sind, ruft die Händler-Website die API zur **Zahlungsanforderung** an, um eine **Zahlungsanforderung** zu erstellen, und übergibt die entsprechenden Zahlungsinformationen (beispielsweise unterstützte Zahlungsmethoden, Kaufbetrag, Währung usw.) an den Browser.

![Zahlungs Anforderungs Konstrukt](./../media/payment_request_construct.png)

Der Browser authentifiziert den Benutzer, ermöglicht es dem Benutzer, eine unterstützte Zahlungsmethode für die Datei auszuwählen und die Zahlungsdetails zu verarbeiten. Der Browser sendet dann die Informationen zur Zahlungsinformation zurück an die Händler-Website, damit der Händler die Zahlung abschließen kann.  Zusätzlich zum Empfang von Zahlungsinformationen kann der Händler auch beschließen, Versandinformationen im Rahmen der **Zahlungsaufforderung**zu erhalten.  

![Konstrukt "Zahlungsantwort"](./../media/payment_response_construct.png)

Schauen Sie sich dieses Video an, um die API zur Zahlungsanforderung in Aktion zu sehen und sich einen Überblick darüber zu verschaffen, wie Sie Sie verwenden können.

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> Die API für Zahlungsanforderungen wird in Microsoft Edge Build 14992 + unterstützt.


## Erstellen einer Zahlungsanforderung 
Webseiten erstellen eine **Zahlungsanforderung** in der Regel, wenn der Benutzer einen Zahlungsvorgang initiiert, indem Sie auf die Schaltfläche "kaufen" klicken.  Der [Konstruktor](https://msdn.microsoft.com/library/mt790440) für **Zahlungsanforderungen** umfasst methodData, Details und Optionen. 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

Der [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter enthält eine Liste der Zahlungsmethoden und Netzwerke, die von der Website akzeptiert werden, sowie alle zugehörigen Zahlungsmethoden spezifischen Daten. In Microsoft Edge wird diese Liste mit den unterstützten Zahlungsmethoden abgeglichen, die der Käufer in seinem Microsoft-Konto gespeichert hat, und führt in der Liste "Zahlung mit" zur Zahlungsmethode.

![Die Liste "bezahlen mit" in der Microsoft Wallet-Benutzeroberfläche](./../media/pay_with.png)

```js
var supportedInstruments = [{
    supportedMethods: ['basic-card'],
    data: {
        supportedNetworks: ['visa', 'mastercard', 'amex'],
        supportedTypes: ['credit'] 
    }         
}]; 
```

Der [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter enthält Informationen, die der Händler dem Kunden über die Transaktion übermitteln möchte.  Dazu zählen Bestell Zusammenfassungs Elemente wie Summe, Steuern, Versand Betrag und andere Zusammenfassungs Ebenen, die sich auf den Zahlungsbetrag auswirken. Diese sind nicht als Auftragspositionen vorgesehen. 
  
Der [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter wird auch verwendet, um Versandoptionen zu definieren, die dem Kunden bei Bedarf zur Verfügung stehen.  Weitere Informationen finden Sie unten im Abschnitt **Zahlungsanforderung** mit Versand. 

Jede [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Zeile enthält eine Bezeichnung für die Währung und den Betrag.  

> [!NOTE]
> Die **Zahlungsanforderung** berechnet nicht die Summe oder Summe dieser Beträge.  Es liegt in der Verantwortung der Website des Händlers, sicherzustellen, dass die Einzelposten richtig sind.   


![Zwischensumme, Versand, Steuern und Gesamt Details](./../media/show_details.png)

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
        label: 'Subtotal',
        amount: {currency: 'USD', value: '174.99'}
    }, {
        label: 'Taxes',
        amount: {currency: "USD", value: '18.99'}
    }],
};  
```

[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)unterstützt keine Rückerstattungen, daher sollten die Beträge immer positiv sein; einzelne Listenelemente können negativ sein, beispielsweise Rabatte. 

Der Browser rendert die Beschriftungen, während Sie Sie definieren, und rendert automatisch die richtige Währungsformatierung basierend auf dem Gebietsschema des Kunden. Beachten Sie, dass die Beschriftungen in der gleichen Sprache wie Ihre Inhalte gerendert werden sollen. 

Der [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter definiert Daten, die auf der Webseite von der **Zahlungsanforderung**zurückgegeben werden sollen. Damit werden auch die Daten definiert, die erfasst werden müssen, einschließlich, wenn Versand, e-Mail-Adresse und/oder Telefonnummer erforderlich sind.

![Dropdownliste "e-Mail-Adresse"](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## Zahlungsanforderung anzeigen

Die [`show()`](https://msdn.microsoft.com/library/mt790448) Methode wird von der Webseite aufgerufen, um dem Benutzer die Interaktion mit der Benutzeroberfläche der **Zahlungsanforderung** zu ermöglichen.  Die [`show()`](https://msdn.microsoft.com/library/mt790448) Methode gibt eine Versprechung zurück, die aufgelöst wird, wenn der Benutzer die Zahlungsanforderung autorisiert.  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Details bestätigen und bezahlen](./../media/pay_screen_default.png)

## Abbrechen einer Zahlungsanforderung
 
Die [`abort()`](https://msdn.microsoft.com/library/mt790437) Methode kann von der Webseite zu einem beliebigen Zeitpunkt aufgerufen werden, nachdem die [`show()`](https://msdn.microsoft.com/library/mt790448) Methode aufgerufen wurde, bis zu dem Punkt, an dem die Verheißung aufgelöst wurde.  Die [`abort()`](https://msdn.microsoft.com/library/mt790437) Methode bewirkt, dass der Browser die **Zahlungsanforderung** abbricht und die Benutzeroberfläche für die **Zahlungsanforderung** schließt.  So kann beispielsweise eine Webseite abgebrochen werden, wenn der Benutzer die Transaktion nicht im erforderlichen Zeitraum abgeschlossen hat.

```js
payment.abort();
``` 

## Zahlungsantwort
Wenn der Kunde die **Zahlungsanforderung**genehmigt, wird eine **Zahlungsantwort** an die Website zurückgegeben. Die **Zahlungsantwort** enthält Folgendes: 

 Eigenschaft      | Beschreibung | Erforderlich | Zusätzliche Infos
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | Die ID für die vom Benutzer ausgewählte Zahlungsmethode | Y | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | Ein JSON-Objekt, das alle Daten enthält, die der Händler benötigt, um die Transaktion mit der ausgewählten Zahlungsmethode oder einem Zahlungs Token zu verarbeiten | Y | [Standardkarte](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: Karten Inhabername; cardNumber expiryMonth; expiryYear; cardSecurityCode; billingAddress; | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | Die vom Benutzer ausgewählte Versandadresse  |  Optional. Erforderlich, wenn [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**  | Adressverzeichnis: Land; addressLine Region Stadt dependentLocality; PostalCode sortingCode; languageCode Organisation Empfänger Telefon |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | Die ID für die ausgewählte Versandoption | Optional. Erforderlich, wenn [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | Der vom Benutzer angegebene Name  | Optional. Erforderlich, wenn [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr** | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | Die vom Benutzer ausgewählte e-Mail-Adresse | Optional. Erforderlich, wenn [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | Die vom Benutzer ausgewählte Telefonnummer | Optional. Erforderlich, wenn [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr** | |

Das [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON-Objekt in der **Zahlungsantwort** enthält die Zahlungsdaten, die vom Händler zur Abwicklung einer Zahlung benötigt werden. In ihrer einfachsten Form wird die Antwort eine [einfache Karten](https://go.microsoft.com/fwlink/?linkid=834965) Nutzlast mit Klartext-Zahlungskarten Details sein. Wenn Händler über Vereinbarungen mit zusätzlichen Gateway/Prozessor-Partnern verfügen, um Zahlungen zu unterstützen, kann der Händler eine Nutzlast anfordern, die der Prozessor verarbeiten kann. Diese können die Form eines Prozessor/Gateway-Tokens oder eines verschlüsselten Zahlungsinstruments annehmen. Diese Zahlungsmethoden liegen außerhalb des Anwendungsbereichs dieses Dokuments und werden in der für den prozessorspezifischen Dokumentation behandelt. Darüber hinaus ist für den Entwickler keine zusätzliche Onboarding-Lösung erforderlich, um eine [einfache Karten](https://go.microsoft.com/fwlink/?linkid=834965) Antwort zu erhalten, im Gegensatz zu anderen Prozessor/Gateway-spezifischen Zahlungsmethoden, die möglicherweise einen Verschlüsselungsschlüssel Onboarding oder eine Autorisierung anfordern (OAuth). 

Nach Eingang der **Zahlungsantwort**übermittelt die Website die Zahlungsinformationen an Ihren Zahlungsprozessor.  Der Browser zeigt eine Drehfeld-Seite an, während die Zahlung verarbeitet wird.

![Die Seite, die angezeigt wird, wenn die Zahlung verarbeitet wird](./../media/loading_screen.png)

Nach Abschluss der Zahlung Ruft die Webseite die [`complete()`](https://msdn.microsoft.com/library/mt790642) Methode auf und übergibt den Wert **Success** oder **Fail**.  Die [`complete()`](https://msdn.microsoft.com/library/mt790642) Methode informiert den Browser, dass der Kauf beendet ist, und der entsprechende abschließende UI-Bildschirm sollte je nach dem Wert von **Success** oder **Fail**angezeigt werden. 

![Die Benutzeroberfläche, die angezeigt wird, wenn der Kauf die ](./../media/response_payment-request_complete.png)
![ Benutzeroberfläche, die beim Kauf fehlgeschlagen ist, erfolgreich war](./../media/response_payment-request_failure.png)

## Zahlungsanforderung mit Versand

### Lieferadresse

Für Verkäufe, die den Versand physischer waren erfordern, ist eine Lieferadresse erforderlich.  Wenn Sie eine Lieferadresse angeben möchten, setzen Sie `requestShipping = True` den [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter der Anforderung.   

Wenn der Benutzer die Versandadresse auswählt oder aktualisiert, [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) wird das Ereignis ausgeführt.  Die Website, die einen Ereignis-Listener verwendet, ist sich der Änderung bewusst und kann dann die Adresse überprüfen, die Versandkosten und Steuern neu berechnen sowie [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) die geänderten Kosten und Versandoptionen für die ausgewählte Adresse (falls zutreffend) aktualisieren. 

### Versandoptionen 

Versandoptionen können dem Kunden angezeigt werden, indem [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) Sie dem Parameter hinzugefügt werden [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) .  Eine Standardeinstellung kann festgelegt werden, indem eine der Versandoptionen festgelegt wird `selected = True` . 
 
Wenn der Benutzer die Versandarten auswählt oder aktualisiert, [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) wird das Ereignis ausgeführt.  Die Website mit einem Ereignis-Listener ist sich der Änderung bewusst und kann den [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter mit dem korrekten Versand Betrag aktualisieren.   

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
 
```

## API-Referenz
[API für Zahlungsanforderungen](https://msdn.microsoft.com/library/mt790447)

## Spezifikation
[API für Zahlungsanforderungen](https://w3.org/TR/payment-request/)
