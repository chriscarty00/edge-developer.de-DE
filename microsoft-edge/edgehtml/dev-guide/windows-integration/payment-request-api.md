---
description: Erfahren Sie, wie die API für Zahlungsanforderungen Microsoft Edge dazu befähigt, als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden für Konsumenten zu fungieren, die in der Cloud gespeichert sind.
title: API für Zahlungsanforderungen – dev-Leitfaden
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: efcad701fec73f858fa9490f12b094259cd8c793
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233841"
---
# <span data-ttu-id="e11af-104">API für Zahlungsanforderungen (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e11af-104">Payment Request API (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="e11af-105">In diesem Artikel wird der Workflow beschrieben, der in der [Legacy Version von Microsoft Edge][MicrosoftSupport44533505]unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e11af-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="e11af-106">Microsoft Edge \(Chrom \) unterstützt die Zahlungs Anforderungs-API mit einer anderen Implementierung basierend auf dem Chromium-Projekt.</span><span class="sxs-lookup"><span data-stu-id="e11af-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="e11af-107">E-Commerce-Umsätze wachsen weiterhin rasant.</span><span class="sxs-lookup"><span data-stu-id="e11af-107">E-commerce sales continue growing at a rapid pace.</span></span>  <span data-ttu-id="e11af-108">Laut [eMarketer](https://www.emarketer.com)wird der digitale Umsatz von 2018 um 23% auf die in 2013 gemessenen Werte steigen.</span><span class="sxs-lookup"><span data-stu-id="e11af-108">According to [eMarketer](https://www.emarketer.com), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="e11af-109">Während Verbraucher und Unternehmen den Vorteil von e-Commerce-Verkäufen genießen, bestehen weiterhin Herausforderungen.</span><span class="sxs-lookup"><span data-stu-id="e11af-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="e11af-110">Heute muss jeder e-Commerce-Websitebesitzer Zeit investieren, um qualitativ hochwertige Zahlungs Checkout-Abläufe und Gültigkeitsprüfungsregeln zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="e11af-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="e11af-111">Verbraucher müssen in verschiedenen Zahlungs Auszahlungs strömen navigieren und die gleichen Zahlungs-und Versandinformationen auf jeder Website, auf der Sie einkaufen, erneut eingeben.</span><span class="sxs-lookup"><span data-stu-id="e11af-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="e11af-112">Dies kann für die Verbraucher zeitaufwendig und frustrierend sein, was zu einer großen Anzahl von Einkaufswagen und verminderten Verkäufen für Händler führt.</span><span class="sxs-lookup"><span data-stu-id="e11af-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span>  <span data-ttu-id="e11af-113">Händler [schätzen](http://baymard.com/lists/cart-abandonment-rate) , dass zwischen 60% und 70% der Einkaufswagen aufgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e11af-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>  

<span data-ttu-id="e11af-114">Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request) standardisiert den Zahlungs Checkout-Prozess.</span><span class="sxs-lookup"><span data-stu-id="e11af-114">The [Payment Request API](https://w3.org/TR/payment-request) standardizes the payment checkout process.</span></span>  <span data-ttu-id="e11af-115">Diese API erfordert weniger benutzerdefinierte Anpassungen für Webentwickler und bietet eine schnellere, konsistentere und daher weniger verwirrende Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="e11af-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="e11af-116">Da die Verbraucher Zahlungsinstrumente und Versandadressen von Ihrem Microsoft-Konto aus auswählen können, müssen Sie weniger Daten eingeben, um Käufe abzuschließen, wodurch die Zeit und die Dateneingabe reduziert werden, die zum Abschließen einer Zahlung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e11af-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>  

<span data-ttu-id="e11af-117">Die [Zahlungs Anforderungs-API](https://w3.org/TR/payment-request) ist ein offener, browserübergreifender Standard, der es Browsern ermöglicht, als Vermittler zwischen Händlern, Verbrauchern und Zahlungsmethoden zu fungieren (wie Kreditkarten \), die von Verbrauchern in der Cloud gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="e11af-117">The [Payment Request API](https://w3.org/TR/payment-request) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  
  
<span data-ttu-id="e11af-118">Zusammenfassend können die Kunden bei der Verwendung der [API für Zahlungsanforderungen](https://w3.org/TR/payment-request)wie gewohnt auf Händler Websites einkaufen.</span><span class="sxs-lookup"><span data-stu-id="e11af-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="e11af-119">Wenn Sie zur Zahlung bereit sind, ruft die Händler Website die API zur **Zahlungsanforderung** an, um eine **Zahlungsanforderung** zu erstellen, und übergibt die entsprechenden Zahlungsinformationen (wie unterstützte Zahlungsmethoden, Einkaufsbetrag, Währung usw.) an den Browser.</span><span class="sxs-lookup"><span data-stu-id="e11af-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information \(such as supported payment methods, purchase amount, currency, and so on\) to the browser.</span></span>  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Zahlungs Anforderungs Konstrukt" lightbox="../media/payment_request_construct.png":::
   <span data-ttu-id="e11af-121">Zahlungs Anforderungs Konstrukt</span><span class="sxs-lookup"><span data-stu-id="e11af-121">Payment request construct</span></span>  
:::image-end:::  

<span data-ttu-id="e11af-122">Der Browser authentifiziert den Benutzer, ermöglicht es dem Benutzer, eine unterstützte Zahlungsmethode für die Datei auszuwählen und die Zahlungsdetails zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e11af-122">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span>  <span data-ttu-id="e11af-123">Der Browser sendet dann die Informationen zur Zahlungsinformation zurück an die Händler-Website, damit der Händler die Zahlung abschließen kann.</span><span class="sxs-lookup"><span data-stu-id="e11af-123">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="e11af-124">Zusätzlich zum Empfang von Zahlungsinformationen kann der Händler auch beschließen, Versandinformationen im Rahmen der **Zahlungsaufforderung**zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e11af-124">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Konstrukt Zahlungsantwort" lightbox="../media/payment_response_construct.png":::
   <span data-ttu-id="e11af-126">Konstrukt "Zahlungsantwort"</span><span class="sxs-lookup"><span data-stu-id="e11af-126">Payment response construct</span></span>  
:::image-end:::  

<span data-ttu-id="e11af-127">Schauen Sie sich dieses Video an, um die API zur Zahlungsanforderung in Aktion zu sehen und sich einen Überblick darüber zu verschaffen, wie Sie Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e11af-127">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> <span data-ttu-id="e11af-128">Die API für Zahlungsanforderungen wird in Microsoft Edge Build 14992 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e11af-128">The Payment Request API is supported in Microsoft Edge build 14992 or newer.</span></span>  

## <span data-ttu-id="e11af-129">Erstellen einer Zahlungsanforderung</span><span class="sxs-lookup"><span data-stu-id="e11af-129">Creating a Payment Request</span></span>  

<span data-ttu-id="e11af-130">Webseiten erstellen eine **Zahlungsanforderung** in der Regel, wenn der Benutzer einen Zahlungsvorgang initiiert, indem Sie auf die Schaltfläche "kaufen" klicken.</span><span class="sxs-lookup"><span data-stu-id="e11af-130">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="e11af-131">Der [Konstruktor](/previous-versions/mt790440(v=vs.85)) für **Zahlungsanforderungen** umfasst methodData, Details und Optionen.</span><span class="sxs-lookup"><span data-stu-id="e11af-131">The **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) includes methodData, details, and options.</span></span>  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

<span data-ttu-id="e11af-132">Der [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter enthält eine Liste der Zahlungsmethoden und Netzwerke, die von der Website akzeptiert werden, sowie alle zugehörigen Zahlungsmethoden spezifischen Daten.</span><span class="sxs-lookup"><span data-stu-id="e11af-132">The [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span>  <span data-ttu-id="e11af-133">In Microsoft Edge wird diese Liste mit den unterstützten Zahlungsmethoden abgeglichen, die der Käufer in seinem Microsoft-Konto gespeichert hat, und führt in der Liste "Zahlung mit" zur Zahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="e11af-133">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="Die Liste bezahlen mit in der Microsoft Wallet-Benutzeroberfläche" lightbox="../media/pay_with.png":::
         <span data-ttu-id="e11af-135">Die Liste " **bezahlen mit** " in der Microsoft Wallet-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="e11af-135">The **pay with** list in the Microsoft Wallet user experience</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var supportedInstruments = [{
          supportedMethods: ['basic-card'],
          data: {
              supportedNetworks: ['visa', 'mastercard', 'amex'],
              supportedTypes: ['credit'] 
          }         
      }]; 
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e11af-136">Der Parameter [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) enthält Informationen, die der Händler dem Kunden über die Transaktion übermitteln möchte.</span><span class="sxs-lookup"><span data-stu-id="e11af-136">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="e11af-137">Dazu zählen Bestell Zusammenfassungs Elemente wie Summe, Steuern, Versand Betrag und andere Zusammenfassungs Ebenen, die sich auf den Zahlungsbetrag auswirken.</span><span class="sxs-lookup"><span data-stu-id="e11af-137">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span>  <span data-ttu-id="e11af-138">Diese sind nicht als Auftragspositionen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e11af-138">These are not intended to be order line items.</span></span>  
  
<span data-ttu-id="e11af-139">Der Parameter [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) wird auch verwendet, um Versandoptionen zu definieren, die dem Kunden bei Bedarf zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e11af-139">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="e11af-140">Weitere Informationen finden Sie unten im Abschnitt **Zahlungsanforderung** mit Versand.</span><span class="sxs-lookup"><span data-stu-id="e11af-140">More details are included in the **Payment Request** with Shipping section below.</span></span>  

<span data-ttu-id="e11af-141">Jede [Detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) Zeile enthält eine Bezeichnung für die Währung und den Betrag.</span><span class="sxs-lookup"><span data-stu-id="e11af-141">Each [detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="e11af-142">Die **Zahlungsanforderung** berechnet nicht die Summe oder Summe dieser Beträge.</span><span class="sxs-lookup"><span data-stu-id="e11af-142">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="e11af-143">Es liegt in der Verantwortung der Website des Händlers, sicherzustellen, dass die Einzelposten richtig sind.</span><span class="sxs-lookup"><span data-stu-id="e11af-143">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Zwischensumme, Versand, Steuern und Gesamt Details" lightbox="../media/show_details.png":::
         <span data-ttu-id="e11af-145">Zwischensumme, Versand, Steuern und Gesamt Details</span><span class="sxs-lookup"><span data-stu-id="e11af-145">Subtotal, shipping, taxes, and total details</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
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
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e11af-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) unterstützt keine Rückerstattungen, daher sollten die Beträge immer positiv sein; einzelne Listenelemente können negativ sein, beispielsweise Rabatte.</span><span class="sxs-lookup"><span data-stu-id="e11af-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span>  

<span data-ttu-id="e11af-147">Der Browser rendert die Beschriftungen, während Sie Sie definieren, und rendert automatisch die richtige Währungsformatierung basierend auf dem Gebietsschema des Kunden.</span><span class="sxs-lookup"><span data-stu-id="e11af-147">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span>  <span data-ttu-id="e11af-148">Beachten Sie, dass die Beschriftungen in der gleichen Sprache wie Ihre Inhalte gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e11af-148">Note that the labels should be rendered in the same language as your content.</span></span>  

<span data-ttu-id="e11af-149">Der [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter definiert Daten, die die Webseite aus der **Zahlungsanforderung**zurückgeben möchte.</span><span class="sxs-lookup"><span data-stu-id="e11af-149">The [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span>  <span data-ttu-id="e11af-150">Damit werden auch die Daten definiert, die erfasst werden müssen, einschließlich, wenn Versand, e-Mail-Adresse, Telefonnummer oder alle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e11af-150">This also defines the data that needs to be collected, including if shipping, email address, phone number or all are required.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Dropdownliste e-Mail-Adresse" lightbox="../media/email_snippet.png":::
         <span data-ttu-id="e11af-152">Dropdownliste "e-Mail-Adresse"</span><span class="sxs-lookup"><span data-stu-id="e11af-152">Email address dropdown</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var options =
          {
              requestPayerEmail: true
          }; 
      ```  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e11af-153">Zahlungsanforderung anzeigen</span><span class="sxs-lookup"><span data-stu-id="e11af-153">Showing the Payment Request</span></span>  

<span data-ttu-id="e11af-154">Die [Show ()](/previous-versions/mt790448(v=vs.85)) -Methode wird von der Webseite aufgerufen, um dem Benutzer die Interaktion mit der Benutzeroberfläche der **Zahlungsanforderung** zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e11af-154">The [show()](/previous-versions/mt790448(v=vs.85)) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="e11af-155">Die [Show ()](/previous-versions/mt790448(v=vs.85)) -Methode gibt eine Versprechung zurück, die aufgelöst wird, wenn der Benutzer die Zahlungsanforderung autorisiert.</span><span class="sxs-lookup"><span data-stu-id="e11af-155">The [show()](/previous-versions/mt790448(v=vs.85)) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Details bestätigen und bezahlen" lightbox="../media/pay_screen_default.png":::
         <span data-ttu-id="e11af-157">Details bestätigen und bezahlen</span><span class="sxs-lookup"><span data-stu-id="e11af-157">Confirm and pay details</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      paymentRequest.show().then(paymentInstrumentResponse => {
          paymentInstrumentResponse.complete('success').then().catch(error => {
              handlePaymentRequestError(error); 
      });
      ```  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e11af-158">Abbrechen einer Zahlungsanforderung</span><span class="sxs-lookup"><span data-stu-id="e11af-158">Aborting a Payment Request</span></span>  
 
<span data-ttu-id="e11af-159">Die [Abort ()](/previous-versions/mt790437(v=vs.85)) -Methode kann von der Webseite zu einem beliebigen Zeitpunkt aufgerufen werden, nachdem die [Show ()](/previous-versions/mt790448(v=vs.85)) -Methode aufgerufen wurde, bis zu dem Punkt, an dem die Verheißung aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="e11af-159">The [abort()](/previous-versions/mt790437(v=vs.85)) method can be called by the web page any time after the [show()](/previous-versions/mt790448(v=vs.85)) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="e11af-160">Die [Abort ()](/previous-versions/mt790437(v=vs.85)) -Methode führt dazu, dass der Browser die **Zahlungsanforderung** abbricht und die Benutzeroberfläche für die **Zahlungsanforderung** schließt.</span><span class="sxs-lookup"><span data-stu-id="e11af-160">The [abort()](/previous-versions/mt790437(v=vs.85)) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="e11af-161">So kann beispielsweise eine Webseite abgebrochen werden, wenn der Benutzer die Transaktion nicht im erforderlichen Zeitraum abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="e11af-161">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>  

```javascript
payment.abort();
```  

## <span data-ttu-id="e11af-162">Zahlungsantwort</span><span class="sxs-lookup"><span data-stu-id="e11af-162">Payment Response</span></span>  
<span data-ttu-id="e11af-163">Wenn der Kunde die **Zahlungsanforderung**genehmigt, wird eine **Zahlungsantwort** an die Website zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e11af-163">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span>  <span data-ttu-id="e11af-164">Die **Zahlungsantwort** enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e11af-164">The **Payment Response** includes the following:</span></span>  

 <span data-ttu-id="e11af-165">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e11af-165">Property</span></span>      | <span data-ttu-id="e11af-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e11af-166">Description</span></span> | <span data-ttu-id="e11af-167">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e11af-167">Required</span></span> | <span data-ttu-id="e11af-168">Zusätzliche Infos</span><span class="sxs-lookup"><span data-stu-id="e11af-168">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[<span data-ttu-id="e11af-169">MethodName</span><span class="sxs-lookup"><span data-stu-id="e11af-169">methodName</span></span>](/previous-versions/mt790656(v=vs.85)) | <span data-ttu-id="e11af-170">Die ID für die vom Benutzer ausgewählte Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="e11af-170">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="e11af-171">Y</span><span class="sxs-lookup"><span data-stu-id="e11af-171">Y</span></span> | |   
[<span data-ttu-id="e11af-172">details</span><span class="sxs-lookup"><span data-stu-id="e11af-172">details</span></span>](/previous-versions/mt790655(v=vs.85)) | <span data-ttu-id="e11af-173">Ein JSON-Objekt, das alle Daten enthält, die der Händler benötigt, um die Transaktion mit der ausgewählten Zahlungsmethode oder einem Zahlungs Token zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="e11af-173">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="e11af-174">Y</span><span class="sxs-lookup"><span data-stu-id="e11af-174">Y</span></span> | <span data-ttu-id="e11af-175">[Standardkarte](https://w3c.github.io/payment-method-basic-card) Dictionary: Karten Inhabername; cardNumber expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="e11af-175">[Basic Card](https://w3c.github.io/payment-method-basic-card) Dictionary:  cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> |   
[<span data-ttu-id="e11af-176">"shippingaddress"</span><span class="sxs-lookup"><span data-stu-id="e11af-176">shippingAddress</span></span>](/previous-versions/mt790445(v=vs.85)) | <span data-ttu-id="e11af-177">Die vom Benutzer ausgewählte Versandadresse</span><span class="sxs-lookup"><span data-stu-id="e11af-177">The shipping address selected by the user</span></span>  |  <span data-ttu-id="e11af-178">Optional.</span><span class="sxs-lookup"><span data-stu-id="e11af-178">Optional.</span></span>  <span data-ttu-id="e11af-179">Erforderlich, wenn [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist</span><span class="sxs-lookup"><span data-stu-id="e11af-179">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | <span data-ttu-id="e11af-180">Adressverzeichnis: Land; addressLine Region Stadt dependentLocality; PostalCode sortingCode; languageCode Organisation Empfänger Telefon</span><span class="sxs-lookup"><span data-stu-id="e11af-180">Address dictionary:  country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |  
[<span data-ttu-id="e11af-181">shippingOption</span><span class="sxs-lookup"><span data-stu-id="e11af-181">shippingOption</span></span>](/previous-versions/mt790446(v=vs.85)) | <span data-ttu-id="e11af-182">Die ID für die ausgewählte Versandoption</span><span class="sxs-lookup"><span data-stu-id="e11af-182">The ID for the selected shipping option</span></span> | <span data-ttu-id="e11af-183">Optional.</span><span class="sxs-lookup"><span data-stu-id="e11af-183">Optional.</span></span>  <span data-ttu-id="e11af-184">Erforderlich, wenn [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist</span><span class="sxs-lookup"><span data-stu-id="e11af-184">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |   
[<span data-ttu-id="e11af-185">payername</span><span class="sxs-lookup"><span data-stu-id="e11af-185">payerName</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="e11af-186">Der vom Benutzer angegebene Name</span><span class="sxs-lookup"><span data-stu-id="e11af-186">The name provided by the user</span></span>  | <span data-ttu-id="e11af-187">Optional.</span><span class="sxs-lookup"><span data-stu-id="e11af-187">Optional.</span></span>  <span data-ttu-id="e11af-188">Erforderlich, wenn [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist</span><span class="sxs-lookup"><span data-stu-id="e11af-188">Required when [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  
[<span data-ttu-id="e11af-189">payerEmail</span><span class="sxs-lookup"><span data-stu-id="e11af-189">payerEmail</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="e11af-190">Die vom Benutzer ausgewählte e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="e11af-190">The email address selected by the user</span></span> | <span data-ttu-id="e11af-191">Optional.</span><span class="sxs-lookup"><span data-stu-id="e11af-191">Optional.</span></span>  <span data-ttu-id="e11af-192">Erforderlich, wenn [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist</span><span class="sxs-lookup"><span data-stu-id="e11af-192">Required when [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |  
[<span data-ttu-id="e11af-193">PayerPhone</span><span class="sxs-lookup"><span data-stu-id="e11af-193">PayerPhone</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="e11af-194">Die vom Benutzer ausgewählte Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="e11af-194">The phone number selected by the user</span></span> | <span data-ttu-id="e11af-195">Optional.</span><span class="sxs-lookup"><span data-stu-id="e11af-195">Optional.</span></span>  <span data-ttu-id="e11af-196">Erforderlich, wenn [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) ist</span><span class="sxs-lookup"><span data-stu-id="e11af-196">Required when [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  

<span data-ttu-id="e11af-197">Das JSON-Objekt " [Details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) " in der **Zahlungsantwort** enthält die Zahlungsdaten, die vom Händler zur Abwicklung einer Zahlung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="e11af-197">The [details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span>  <span data-ttu-id="e11af-198">In ihrer einfachsten Form wird die Antwort eine [einfache Karten](https://w3c.github.io/payment-method-basic-card) Nutzlast mit Klartext-Zahlungskarten Details sein.</span><span class="sxs-lookup"><span data-stu-id="e11af-198">In its simplest form, the response will be a [Basic Card](https://w3c.github.io/payment-method-basic-card) payload containing cleartext payment card details.</span></span>  <span data-ttu-id="e11af-199">Wenn Händler über Vereinbarungen mit zusätzlichen Gateway/Prozessor-Partnern verfügen, um Zahlungen zu unterstützen, kann der Händler eine Nutzlast anfordern, die der Prozessor verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="e11af-199">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span>  <span data-ttu-id="e11af-200">Diese können die Form eines Prozessor/Gateway-Tokens oder eines verschlüsselten Zahlungsinstruments annehmen.</span><span class="sxs-lookup"><span data-stu-id="e11af-200">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span>  <span data-ttu-id="e11af-201">Diese Zahlungsmethoden liegen außerhalb des Anwendungsbereichs dieses Dokuments und werden in der für den prozessorspezifischen Dokumentation behandelt.</span><span class="sxs-lookup"><span data-stu-id="e11af-201">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span>  <span data-ttu-id="e11af-202">Darüber hinaus ist für den Entwickler keine zusätzliche Onboarding-Lösung erforderlich, um eine [einfache Karten](https://w3c.github.io/payment-method-basic-card) Antwort zu erhalten, im Gegensatz zu anderen Prozessor/Gateway-spezifischen Zahlungsmethoden, die möglicherweise eine Onboarding-Verschlüsselung oder eine Autorisierung anfordern \(oAuth \).</span><span class="sxs-lookup"><span data-stu-id="e11af-202">Additionally, to receive a [Basic Card](https://w3c.github.io/payment-method-basic-card) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization \(oAuth\).</span></span>  

<span data-ttu-id="e11af-203">Nach Eingang der **Zahlungsantwort**übermittelt die Website die Zahlungsinformationen an Ihren Zahlungsprozessor.</span><span class="sxs-lookup"><span data-stu-id="e11af-203">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="e11af-204">Der Browser zeigt eine Drehfeld-Seite an, während die Zahlung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="e11af-204">The browser will display a spinner page while the payment is being processed.</span></span>  

:::image type="complex" source="../media/loading_screen.png" alt-text="Die Seite, die angezeigt wird, wenn die Zahlung verarbeitet wird" lightbox="../media/loading_screen.png":::
   <span data-ttu-id="e11af-206">Die Seite, die angezeigt wird, wenn die Zahlung verarbeitet wird</span><span class="sxs-lookup"><span data-stu-id="e11af-206">The page displayed when the payment is being processed</span></span>  
:::image-end:::  

<span data-ttu-id="e11af-207">Nach Abschluss der Zahlung Ruft die Webseite die [vollständige ()](/previous-versions/mt790642(v=vs.85)) -Methode auf und übergibt den Wert **Success** oder **Fail**.</span><span class="sxs-lookup"><span data-stu-id="e11af-207">Once the payment is complete, the web page calls the [complete()](/previous-versions/mt790642(v=vs.85)) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="e11af-208">Mit der [Complete ()](/previous-versions/mt790642(v=vs.85)) -Methode wird der Browser darüber informiert, dass der Kauf abgeschlossen ist, und der entsprechende abschließende UI-Bildschirm sollte je nach dem Wert von **Success** oder **Fail**angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e11af-208">The [complete()](/previous-versions/mt790642(v=vs.85)) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="Die beim erfolgreichen Kauf angezeigte Benutzeroberfläche" lightbox="../media/response_payment-request_complete.png":::
         <span data-ttu-id="e11af-210">Die beim erfolgreichen Kauf angezeigte Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="e11af-210">The UI displayed when the purchase succeeded</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="Die Benutzeroberfläche, die beim Kauf nicht angezeigt wird" lightbox="../media/response_payment-request_failure.png":::
         <span data-ttu-id="e11af-212">Die Benutzeroberfläche, die beim Kauf nicht angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="e11af-212">The UI displayed when the purchase failed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e11af-213">Zahlungsanforderung mit Versand</span><span class="sxs-lookup"><span data-stu-id="e11af-213">Payment Request with Shipping</span></span>  

### <span data-ttu-id="e11af-214">Lieferadresse</span><span class="sxs-lookup"><span data-stu-id="e11af-214">Shipping Address</span></span>  

<span data-ttu-id="e11af-215">Für Verkäufe, die den Versand physischer waren erfordern, ist eine Lieferadresse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e11af-215">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="e11af-216">Wenn Sie eine Lieferadresse angeben möchten, legen Sie `requestShipping = True` die Optionen in den [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e11af-216">To include a shipping address, set `requestShipping = True` in the [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter of the request.</span></span>  

<span data-ttu-id="e11af-217">Wenn der Benutzer die Versandadresse auswählt oder aktualisiert, wird das [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) -Ereignis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e11af-217">When the user selects or updates the shipping address, the [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) event will run.</span></span>  <span data-ttu-id="e11af-218">Die Website mit einem Ereignislistener ist sich der Änderung bewusst und kann dann die Adresse überprüfen, die Versandkosten und Steuern neu berechnen sowie [Versand](/previous-versions/mt790440(v=vs.85)) Optionen aktualisieren, um die geänderten Kosten und Versandoptionen anzuzeigen, die für die ausgewählte Adresse verfügbar sind \(falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="e11af-218">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [shippingOptions](/previous-versions/mt790440(v=vs.85)) to reflect the changed costs and shipping options available for the address selected \(if applicable\).</span></span>  

### <span data-ttu-id="e11af-219">Versandoptionen</span><span class="sxs-lookup"><span data-stu-id="e11af-219">Shipping Options</span></span>  

<span data-ttu-id="e11af-220">Versandoptionen können dem Kunden angezeigt werden, indem dem [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) -Parameter [shippingoptions](/previous-versions/mt790440(v=vs.85)) hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e11af-220">Shipping options can be presented to the customer by adding [shippingOptions](/previous-versions/mt790440(v=vs.85)) to the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="e11af-221">Eine Standardeinstellung kann festgelegt werden, indem eine der Versandoptionen festgelegt wird `selected = True` .</span><span class="sxs-lookup"><span data-stu-id="e11af-221">A default can be established by setting `selected = True` for one of the shipping options.</span></span>  
 
<span data-ttu-id="e11af-222">Wenn der Benutzer die Versandarten auswählt oder aktualisiert, wird das [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) -Ereignis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e11af-222">When the user selects or updates the shippingOptions, the [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) event will run.</span></span>  <span data-ttu-id="e11af-223">Die Website mit einem Ereignis-Listener ist sich der Änderung bewusst und kann den Parameter [Details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) mit dem korrekten Versand Betrag aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e11af-223">The website, using an event listener, will be aware of the change and can update the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter with the correct shipping amount.</span></span>  

```javascript
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

## <span data-ttu-id="e11af-224">API-Referenz</span><span class="sxs-lookup"><span data-stu-id="e11af-224">API Reference</span></span>  

[<span data-ttu-id="e11af-225">Payments Request-API</span><span class="sxs-lookup"><span data-stu-id="e11af-225">Payment Request API</span></span>](/previous-versions/mt790447(v=vs.85))  

## <span data-ttu-id="e11af-226">Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e11af-226">Specification</span></span>
[<span data-ttu-id="e11af-227">Payments Request-API</span><span class="sxs-lookup"><span data-stu-id="e11af-227">Payment Request API</span></span>](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Microsoft Edge (Chrom)-Entwickler Tools | Microsoft docs"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Was ist Microsoft Edge Legacy?"  
