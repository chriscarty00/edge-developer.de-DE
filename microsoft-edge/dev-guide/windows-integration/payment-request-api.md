---
description: Erfahren Sie, wie thePayment Request APIenables Microsoft Edge als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden für Verbraucher in der Cloud fungiert.
title: Dev Guide-API für Zahlungsanforderungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: b082e311dcbe5cff3101f084e7ff2c145e6e83df
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902864"
---
# <span data-ttu-id="55501-104">API für Zahlungsanforderungen (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="55501-104">Payment Request API (EdgeHTML)</span></span>

> [!NOTE]
> <span data-ttu-id="55501-105">In diesem Artikel wird der Workflow beschrieben, der in der [Legacy Version von Microsoft Edge][MicrosoftSupport44533505]unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="55501-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="55501-106">Microsoft Edge \ (Chrom \) unterstützt die Zahlungs Anforderungs-API mit einer anderen Implementierung basierend auf dem Chromium-Projekt.</span><span class="sxs-lookup"><span data-stu-id="55501-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="55501-107">E-Commerce-Umsätze wachsen weiterhin rasant.</span><span class="sxs-lookup"><span data-stu-id="55501-107">E-commerce sales continue growing at a rapid pace.</span></span> <span data-ttu-id="55501-108">Laut [eMarketer](https://www.emarketer.com/)wird der digitale Umsatz von 2018 um 23% auf die in 2013 gemessenen Werte steigen.</span><span class="sxs-lookup"><span data-stu-id="55501-108">According to [eMarketer](https://www.emarketer.com/), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="55501-109">Während Verbraucher und Unternehmen den Vorteil von e-Commerce-Verkäufen genießen, bestehen weiterhin Herausforderungen.</span><span class="sxs-lookup"><span data-stu-id="55501-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="55501-110">Heute muss jeder e-Commerce-Websitebesitzer Zeit investieren, um qualitativ hochwertige Zahlungs Checkout-Abläufe und Gültigkeitsprüfungsregeln zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="55501-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="55501-111">Verbraucher müssen in verschiedenen Zahlungs Auszahlungs strömen navigieren und die gleichen Zahlungs-und Versandinformationen auf jeder Website, auf der Sie einkaufen, erneut eingeben.</span><span class="sxs-lookup"><span data-stu-id="55501-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="55501-112">Dies kann für die Verbraucher zeitaufwendig und frustrierend sein, was zu einer großen Anzahl von Einkaufswagen und verminderten Verkäufen für Händler führt.</span><span class="sxs-lookup"><span data-stu-id="55501-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span> <span data-ttu-id="55501-113">Händler [schätzen](http://baymard.com/lists/cart-abandonment-rate) , dass zwischen 60% und 70% der Einkaufswagen aufgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="55501-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>      

<span data-ttu-id="55501-114">Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request/) standardisiert den Zahlungs Checkout-Prozess.</span><span class="sxs-lookup"><span data-stu-id="55501-114">The [Payment Request API](https://w3.org/TR/payment-request/) standardizes the payment checkout process.</span></span> <span data-ttu-id="55501-115">Diese API erfordert weniger benutzerdefinierte Anpassungen für Webentwickler und bietet eine schnellere, konsistentere und daher weniger verwirrende Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="55501-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="55501-116">Da die Verbraucher Zahlungsinstrumente und Versandadressen von Ihrem Microsoft-Konto aus auswählen können, müssen Sie weniger Daten eingeben, um Käufe abzuschließen, wodurch die Zeit und die Dateneingabe reduziert werden, die zum Abschließen einer Zahlung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="55501-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>   

<span data-ttu-id="55501-117">Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request/) ist ein offener, browserübergreifender Standard, der es Browsern ermöglicht, als Vermittler zwischen Händlern, Verbrauchern und den Zahlungsmethoden (z.b. Kreditkarten) zu fungieren, die Verbraucher in der Cloud gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="55501-117">The [Payment Request API](https://w3.org/TR/payment-request/) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods (e.g. credit cards) that consumers have stored in the cloud.</span></span> 
  
<span data-ttu-id="55501-118">Zusammenfassend können die Kunden bei der Verwendung der [API für Zahlungsanforderungen](https://w3.org/TR/payment-request/)wie gewohnt auf Händler Websites einkaufen.</span><span class="sxs-lookup"><span data-stu-id="55501-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request/), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="55501-119">Wenn Sie zur Zahlung bereit sind, ruft die Händler-Website die API zur **Zahlungsanforderung** an, um eine **Zahlungsanforderung** zu erstellen, und übergibt die entsprechenden Zahlungsinformationen (beispielsweise unterstützte Zahlungsmethoden, Kaufbetrag, Währung usw.) an den Browser.</span><span class="sxs-lookup"><span data-stu-id="55501-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information (e.g. supported payment methods, purchase amount, currency, etc.) to the browser.</span></span>

![Zahlungs Anforderungs Konstrukt](./../media/payment_request_construct.png)

<span data-ttu-id="55501-121">Der Browser authentifiziert den Benutzer, ermöglicht es dem Benutzer, eine unterstützte Zahlungsmethode für die Datei auszuwählen und die Zahlungsdetails zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="55501-121">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span> <span data-ttu-id="55501-122">Der Browser sendet dann die Informationen zur Zahlungsinformation zurück an die Händler-Website, damit der Händler die Zahlung abschließen kann.</span><span class="sxs-lookup"><span data-stu-id="55501-122">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="55501-123">Zusätzlich zum Empfang von Zahlungsinformationen kann der Händler auch beschließen, Versandinformationen im Rahmen der **Zahlungsaufforderung**zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="55501-123">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

![Konstrukt "Zahlungsantwort"](./../media/payment_response_construct.png)

<span data-ttu-id="55501-125">Schauen Sie sich dieses Video an, um die API zur Zahlungsanforderung in Aktion zu sehen und sich einen Überblick darüber zu verschaffen, wie Sie Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="55501-125">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> <span data-ttu-id="55501-126">Die API für Zahlungsanforderungen wird in Microsoft Edge Build 14992 + unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55501-126">The Payment Request API is supported in Microsoft Edge build 14992+.</span></span>


## <span data-ttu-id="55501-127">Erstellen einer Zahlungsanforderung</span><span class="sxs-lookup"><span data-stu-id="55501-127">Creating a Payment Request</span></span> 
<span data-ttu-id="55501-128">Webseiten erstellen eine **Zahlungsanforderung** in der Regel, wenn der Benutzer einen Zahlungsvorgang initiiert, indem Sie auf die Schaltfläche "kaufen" klicken.</span><span class="sxs-lookup"><span data-stu-id="55501-128">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="55501-129">Der [Konstruktor](https://msdn.microsoft.com/library/mt790440) für **Zahlungsanforderungen** umfasst methodData, Details und Optionen.</span><span class="sxs-lookup"><span data-stu-id="55501-129">The **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) includes methodData, details, and options.</span></span> 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

<span data-ttu-id="55501-130">Der [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter enthält eine Liste der Zahlungsmethoden und Netzwerke, die von der Website akzeptiert werden, sowie alle zugehörigen Zahlungsmethoden spezifischen Daten.</span><span class="sxs-lookup"><span data-stu-id="55501-130">The [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span> <span data-ttu-id="55501-131">In Microsoft Edge wird diese Liste mit den unterstützten Zahlungsmethoden abgeglichen, die der Käufer in seinem Microsoft-Konto gespeichert hat, und führt in der Liste "Zahlung mit" zur Zahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="55501-131">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>

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

<span data-ttu-id="55501-133">Der [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter enthält Informationen, die der Händler dem Kunden über die Transaktion übermitteln möchte.</span><span class="sxs-lookup"><span data-stu-id="55501-133">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="55501-134">Dazu zählen Bestell Zusammenfassungs Elemente wie Summe, Steuern, Versand Betrag und andere Zusammenfassungs Ebenen, die sich auf den Zahlungsbetrag auswirken.</span><span class="sxs-lookup"><span data-stu-id="55501-134">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span> <span data-ttu-id="55501-135">Diese sind nicht als Auftragspositionen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="55501-135">These are not intended to be order line items.</span></span> 
  
<span data-ttu-id="55501-136">Der [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter wird auch verwendet, um Versandoptionen zu definieren, die dem Kunden bei Bedarf zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="55501-136">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="55501-137">Weitere Informationen finden Sie unten im Abschnitt **Zahlungsanforderung** mit Versand.</span><span class="sxs-lookup"><span data-stu-id="55501-137">More details are included in the **Payment Request** with Shipping section below.</span></span> 

<span data-ttu-id="55501-138">Jede [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Zeile enthält eine Bezeichnung für die Währung und den Betrag.</span><span class="sxs-lookup"><span data-stu-id="55501-138">Each [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="55501-139">Die **Zahlungsanforderung** berechnet nicht die Summe oder Summe dieser Beträge.</span><span class="sxs-lookup"><span data-stu-id="55501-139">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="55501-140">Es liegt in der Verantwortung der Website des Händlers, sicherzustellen, dass die Einzelposten richtig sind.</span><span class="sxs-lookup"><span data-stu-id="55501-140">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>   


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

<span data-ttu-id="55501-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)unterstützt keine Rückerstattungen, daher sollten die Beträge immer positiv sein; einzelne Listenelemente können negativ sein, beispielsweise Rabatte.</span><span class="sxs-lookup"><span data-stu-id="55501-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span> 

<span data-ttu-id="55501-143">Der Browser rendert die Beschriftungen, während Sie Sie definieren, und rendert automatisch die richtige Währungsformatierung basierend auf dem Gebietsschema des Kunden.</span><span class="sxs-lookup"><span data-stu-id="55501-143">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span> <span data-ttu-id="55501-144">Beachten Sie, dass die Beschriftungen in der gleichen Sprache wie Ihre Inhalte gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55501-144">Note that the labels should be rendered in the same language as your content.</span></span> 

<span data-ttu-id="55501-145">Der [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter definiert Daten, die auf der Webseite von der **Zahlungsanforderung**zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55501-145">The [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span> <span data-ttu-id="55501-146">Damit werden auch die Daten definiert, die erfasst werden müssen, einschließlich, wenn Versand, e-Mail-Adresse und/oder Telefonnummer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="55501-146">This also defines the data that needs to be collected, including if shipping, email address, and/or phone number are required.</span></span>

![Dropdownliste "e-Mail-Adresse"](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## <span data-ttu-id="55501-148">Zahlungsanforderung anzeigen</span><span class="sxs-lookup"><span data-stu-id="55501-148">Showing the Payment Request</span></span>

<span data-ttu-id="55501-149">Die [`show()`](https://msdn.microsoft.com/library/mt790448) Methode wird von der Webseite aufgerufen, um dem Benutzer die Interaktion mit der Benutzeroberfläche der **Zahlungsanforderung** zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="55501-149">The [`show()`](https://msdn.microsoft.com/library/mt790448) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="55501-150">Die [`show()`](https://msdn.microsoft.com/library/mt790448) Methode gibt eine Versprechung zurück, die aufgelöst wird, wenn der Benutzer die Zahlungsanforderung autorisiert.</span><span class="sxs-lookup"><span data-stu-id="55501-150">The [`show()`](https://msdn.microsoft.com/library/mt790448) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Details bestätigen und bezahlen](./../media/pay_screen_default.png)

## <span data-ttu-id="55501-152">Abbrechen einer Zahlungsanforderung</span><span class="sxs-lookup"><span data-stu-id="55501-152">Aborting a Payment Request</span></span>
 
<span data-ttu-id="55501-153">Die [`abort()`](https://msdn.microsoft.com/library/mt790437) Methode kann von der Webseite zu einem beliebigen Zeitpunkt aufgerufen werden, nachdem die [`show()`](https://msdn.microsoft.com/library/mt790448) Methode aufgerufen wurde, bis zu dem Punkt, an dem die Verheißung aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="55501-153">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method can be called by the web page any time after the [`show()`](https://msdn.microsoft.com/library/mt790448) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="55501-154">Die [`abort()`](https://msdn.microsoft.com/library/mt790437) Methode bewirkt, dass der Browser die **Zahlungsanforderung** abbricht und die Benutzeroberfläche für die **Zahlungsanforderung** schließt.</span><span class="sxs-lookup"><span data-stu-id="55501-154">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="55501-155">So kann beispielsweise eine Webseite abgebrochen werden, wenn der Benutzer die Transaktion nicht im erforderlichen Zeitraum abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="55501-155">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>

```js
payment.abort();
``` 

## <span data-ttu-id="55501-156">Zahlungsantwort</span><span class="sxs-lookup"><span data-stu-id="55501-156">Payment Response</span></span>
<span data-ttu-id="55501-157">Wenn der Kunde die **Zahlungsanforderung**genehmigt, wird eine **Zahlungsantwort** an die Website zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="55501-157">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span> <span data-ttu-id="55501-158">Die **Zahlungsantwort** enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55501-158">The **Payment Response** includes the following:</span></span> 

 <span data-ttu-id="55501-159">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55501-159">Property</span></span>      | <span data-ttu-id="55501-160">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55501-160">Description</span></span> | <span data-ttu-id="55501-161">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="55501-161">Required</span></span> | <span data-ttu-id="55501-162">Zusätzliche Infos</span><span class="sxs-lookup"><span data-stu-id="55501-162">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | <span data-ttu-id="55501-163">Die ID für die vom Benutzer ausgewählte Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="55501-163">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="55501-164">Y</span><span class="sxs-lookup"><span data-stu-id="55501-164">Y</span></span> | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | <span data-ttu-id="55501-165">Ein JSON-Objekt, das alle Daten enthält, die der Händler benötigt, um die Transaktion mit der ausgewählten Zahlungsmethode oder einem Zahlungs Token zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="55501-165">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="55501-166">Y</span><span class="sxs-lookup"><span data-stu-id="55501-166">Y</span></span> | <span data-ttu-id="55501-167">[Standardkarte](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: Karten Inhabername; cardNumber expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="55501-167">[Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | <span data-ttu-id="55501-168">Die vom Benutzer ausgewählte Versandadresse</span><span class="sxs-lookup"><span data-stu-id="55501-168">The shipping address selected by the user</span></span>  |  <span data-ttu-id="55501-169">Optional.</span><span class="sxs-lookup"><span data-stu-id="55501-169">Optional.</span></span> <span data-ttu-id="55501-170">Erforderlich, wenn [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**</span><span class="sxs-lookup"><span data-stu-id="55501-170">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | <span data-ttu-id="55501-171">Adressverzeichnis: Land; addressLine Region Stadt dependentLocality; PostalCode sortingCode; languageCode Organisation Empfänger Telefon</span><span class="sxs-lookup"><span data-stu-id="55501-171">Address dictionary: country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | <span data-ttu-id="55501-172">Die ID für die ausgewählte Versandoption</span><span class="sxs-lookup"><span data-stu-id="55501-172">The ID for the selected shipping option</span></span> | <span data-ttu-id="55501-173">Optional.</span><span class="sxs-lookup"><span data-stu-id="55501-173">Optional.</span></span> <span data-ttu-id="55501-174">Erforderlich, wenn [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**</span><span class="sxs-lookup"><span data-stu-id="55501-174">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="55501-175">Der vom Benutzer angegebene Name</span><span class="sxs-lookup"><span data-stu-id="55501-175">The name provided by the user</span></span>  | <span data-ttu-id="55501-176">Optional.</span><span class="sxs-lookup"><span data-stu-id="55501-176">Optional.</span></span> <span data-ttu-id="55501-177">Erforderlich, wenn [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**</span><span class="sxs-lookup"><span data-stu-id="55501-177">Required when [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="55501-178">Die vom Benutzer ausgewählte e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="55501-178">The email address selected by the user</span></span> | <span data-ttu-id="55501-179">Optional.</span><span class="sxs-lookup"><span data-stu-id="55501-179">Optional.</span></span> <span data-ttu-id="55501-180">Erforderlich, wenn [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**</span><span class="sxs-lookup"><span data-stu-id="55501-180">Required when [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="55501-181">Die vom Benutzer ausgewählte Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="55501-181">The phone number selected by the user</span></span> | <span data-ttu-id="55501-182">Optional.</span><span class="sxs-lookup"><span data-stu-id="55501-182">Optional.</span></span> <span data-ttu-id="55501-183">Erforderlich, wenn [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) ist **wahr**</span><span class="sxs-lookup"><span data-stu-id="55501-183">Required when [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |

<span data-ttu-id="55501-184">Das [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON-Objekt in der **Zahlungsantwort** enthält die Zahlungsdaten, die vom Händler zur Abwicklung einer Zahlung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="55501-184">The [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span> <span data-ttu-id="55501-185">In ihrer einfachsten Form wird die Antwort eine [einfache Karten](https://go.microsoft.com/fwlink/?linkid=834965) Nutzlast mit Klartext-Zahlungskarten Details sein.</span><span class="sxs-lookup"><span data-stu-id="55501-185">In its simplest form, the response will be a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) payload containing cleartext payment card details.</span></span> <span data-ttu-id="55501-186">Wenn Händler über Vereinbarungen mit zusätzlichen Gateway/Prozessor-Partnern verfügen, um Zahlungen zu unterstützen, kann der Händler eine Nutzlast anfordern, die der Prozessor verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="55501-186">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span> <span data-ttu-id="55501-187">Diese können die Form eines Prozessor/Gateway-Tokens oder eines verschlüsselten Zahlungsinstruments annehmen.</span><span class="sxs-lookup"><span data-stu-id="55501-187">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span> <span data-ttu-id="55501-188">Diese Zahlungsmethoden liegen außerhalb des Anwendungsbereichs dieses Dokuments und werden in der für den prozessorspezifischen Dokumentation behandelt.</span><span class="sxs-lookup"><span data-stu-id="55501-188">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span> <span data-ttu-id="55501-189">Darüber hinaus ist für den Entwickler keine zusätzliche Onboarding-Lösung erforderlich, um eine [einfache Karten](https://go.microsoft.com/fwlink/?linkid=834965) Antwort zu erhalten, im Gegensatz zu anderen Prozessor/Gateway-spezifischen Zahlungsmethoden, die möglicherweise einen Verschlüsselungsschlüssel Onboarding oder eine Autorisierung anfordern (OAuth).</span><span class="sxs-lookup"><span data-stu-id="55501-189">Additionally, to receive a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization (oauth).</span></span> 

<span data-ttu-id="55501-190">Nach Eingang der **Zahlungsantwort**übermittelt die Website die Zahlungsinformationen an Ihren Zahlungsprozessor.</span><span class="sxs-lookup"><span data-stu-id="55501-190">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="55501-191">Der Browser zeigt eine Drehfeld-Seite an, während die Zahlung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="55501-191">The browser will display a spinner page while the payment is being processed.</span></span>

![Die Seite, die angezeigt wird, wenn die Zahlung verarbeitet wird](./../media/loading_screen.png)

<span data-ttu-id="55501-193">Nach Abschluss der Zahlung Ruft die Webseite die [`complete()`](https://msdn.microsoft.com/library/mt790642) Methode auf und übergibt den Wert **Success** oder **Fail**.</span><span class="sxs-lookup"><span data-stu-id="55501-193">Once the payment is complete, the web page calls the [`complete()`](https://msdn.microsoft.com/library/mt790642) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="55501-194">Die [`complete()`](https://msdn.microsoft.com/library/mt790642) Methode informiert den Browser, dass der Kauf beendet ist, und der entsprechende abschließende UI-Bildschirm sollte je nach dem Wert von **Success** oder **Fail**angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="55501-194">The [`complete()`](https://msdn.microsoft.com/library/mt790642) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span> 

![<span data-ttu-id="55501-195">Die Benutzeroberfläche, die angezeigt wird, wenn der Kauf die ](./../media/response_payment-request_complete.png)
![ Benutzeroberfläche, die beim Kauf fehlgeschlagen ist, erfolgreich war</span><span class="sxs-lookup"><span data-stu-id="55501-195">The UI displayed when the purchase succeeded](./../media/response_payment-request_complete.png)
![The UI displayed when the purchase failed</span></span>](./../media/response_payment-request_failure.png)

## <span data-ttu-id="55501-196">Zahlungsanforderung mit Versand</span><span class="sxs-lookup"><span data-stu-id="55501-196">Payment Request with Shipping</span></span>

### <span data-ttu-id="55501-197">Lieferadresse</span><span class="sxs-lookup"><span data-stu-id="55501-197">Shipping Address</span></span>

<span data-ttu-id="55501-198">Für Verkäufe, die den Versand physischer waren erfordern, ist eine Lieferadresse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="55501-198">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="55501-199">Wenn Sie eine Lieferadresse angeben möchten, setzen Sie `requestShipping = True` den [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="55501-199">To include a shipping address, set `requestShipping = True` in the [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter of the request.</span></span>   

<span data-ttu-id="55501-200">Wenn der Benutzer die Versandadresse auswählt oder aktualisiert, [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) wird das Ereignis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55501-200">When the user selects or updates the shipping address, the [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) event will run.</span></span>  <span data-ttu-id="55501-201">Die Website, die einen Ereignis-Listener verwendet, ist sich der Änderung bewusst und kann dann die Adresse überprüfen, die Versandkosten und Steuern neu berechnen sowie [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) die geänderten Kosten und Versandoptionen für die ausgewählte Adresse (falls zutreffend) aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55501-201">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to reflect the changed costs and shipping options available for the address selected (if applicable).</span></span> 

### <span data-ttu-id="55501-202">Versandoptionen</span><span class="sxs-lookup"><span data-stu-id="55501-202">Shipping Options</span></span> 

<span data-ttu-id="55501-203">Versandoptionen können dem Kunden angezeigt werden, indem [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) Sie dem Parameter hinzugefügt werden [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) .</span><span class="sxs-lookup"><span data-stu-id="55501-203">Shipping options can be presented to the customer by adding [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="55501-204">Eine Standardeinstellung kann festgelegt werden, indem eine der Versandoptionen festgelegt wird `selected = True` .</span><span class="sxs-lookup"><span data-stu-id="55501-204">A default can be established by setting `selected = True` for one of the shipping options.</span></span> 
 
<span data-ttu-id="55501-205">Wenn der Benutzer die Versandarten auswählt oder aktualisiert, [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) wird das Ereignis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55501-205">When the user selects or updates the shippingOptions, the [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) event will run.</span></span>  <span data-ttu-id="55501-206">Die Website mit einem Ereignis-Listener ist sich der Änderung bewusst und kann den [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) Parameter mit dem korrekten Versand Betrag aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55501-206">The website, using an event listener, will be aware of the change and can update the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter with the correct shipping amount.</span></span>   

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

## <span data-ttu-id="55501-207">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="55501-207">API Reference</span></span>
[<span data-ttu-id="55501-208">Payments Request-API</span><span class="sxs-lookup"><span data-stu-id="55501-208">Payment Request API</span></span>](https://msdn.microsoft.com/library/mt790447)

## <span data-ttu-id="55501-209">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="55501-209">Specification</span></span>
[<span data-ttu-id="55501-210">Payments Request-API</span><span class="sxs-lookup"><span data-stu-id="55501-210">Payment Request API</span></span>](https://w3.org/TR/payment-request/)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Was ist Microsoft Edge Legacy?"  
