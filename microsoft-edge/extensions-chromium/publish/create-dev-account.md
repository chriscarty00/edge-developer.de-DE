---
description: Erfahren Sie, wie Sie sich bei einem Entwicklerkonto registrieren, um Erweiterungen im Microsoft Edge-Add-ons-Store zu veröffentlichen.
title: Registrieren als Microsoft Edge Extension Developer zum Veröffentlichen von Erweiterungen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-Chromium, Erweiterungen-Entwicklung, Browser-Erweiterungen, Add-ons, Partner Center, Entwickler
ms.openlocfilehash: 87c5dbfdec65ae3957724ae846a06480a2488084
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015744"
---
# Registrieren als Microsoft Edge Extension Developer  

Wenn Sie Ihre Erweiterung an die Microsoft Edge-Add-ons-Website senden möchten, müssen Sie mit dem Microsoft Edge-Programm im [Partner Center][MicrosoftPartnerCenter]als Entwickler registriert sein.  Beim Übermitteln von Erweiterungen an das Microsoft Edge-Programm fällt keine Registrierungsgebühr an.  

## Vorbemerkungen  

Wenn Sie nicht über ein Konto verfügen oder wenn Sie über ein vorhandenes kommerzielles Konto bei Partner Center verfügen, müssen Sie ein neues [Microsoft-Konto (MSA)][WindowsCommunityEverythingAboutMicrosoftAccounts] erstellen, um sich beim Microsoft Edge-Programm registrieren zu können.  Wenn Sie ein Microsoft-Konto (Outlook/Live/Hotmail) erstellen möchten, besuchen Sie [Account.Microsoft.com][MicrosoftAccount] , und wählen Sie **Microsoft-Konto erstellen**aus.  Wenn Sie mit einem Entwicklerkonto im Partner Center registriert sind, verwenden Sie das entsprechende Microsoft-Konto \ (MSA \), um sich anzumelden, und registrieren Sie sich dann beim Microsoft Edge-Programm.  

> [!NOTE]
> Heute unterstützt das Microsoft Edge Extensions-Team die Anmeldung bei einem Firmen-oder Schulkonto nicht.  In Zukunft plant das Microsoft Edge Extensions-Team, die Verknüpfung von Aad-Mandanten mit MSA-Konten für die Erweiterungsverwaltung zu unterstützen.  

## Registrieren des Microsoft Edge-Programms im Partner Center  

1.  Wechseln Sie zur [Seite "Entwicklertools"][MicrosoftPartnerCenter] , und wählen Sie **Gehe zu Dashboard**aus.  
1.  Wenn Sie noch nicht mit einem **Microsoft-Konto**angemeldet sind, melden Sie sich jetzt an, oder erstellen Sie ein neues Microsoft-Konto.  Sie verwenden das gleiche Microsoft-Konto, mit dem Sie sich bei Ihrem Entwicklerkonto anmelden.  Nachdem Sie sich angemeldet haben, wird dieses Registrierungsformular angezeigt.  
    
    Wenn Sie sich beim Microsoft Edge-Programm registrieren möchten, melden Sie sich bei Ihrem Konto an, und füllen Sie das Formular aus.  
    <!-- -->
    :::row:::
       :::column span="1":::
          **Konto für Land/Region**  
       :::column-end:::
       :::column span="2":::
          In diesem Feld können Sie entweder wohnen oder Ihr Unternehmen befindet sich.  
          
          > [!IMPORTANT]
          > Nach der Registrierung können Sie den Wert dieses Felds nicht ändern.  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="1":::
          **Kontotyp**  
       :::column-end:::
       :::column span="2":::
          Das Microsoft Edge-Programm im [Partner Center][MicrosoftPartnerCenter] bietet sowohl Einzel-als auch Unternehmenskonten, die in der folgenden Tabelle ausführlich beschrieben werden.  Beide Kontotypen ermöglichen Ihnen, Erweiterungen im Microsoft Edge-Add-ons-Katalog zu veröffentlichen.  
          
          > [!IMPORTANT]
          > Nach der Registrierung können Sie den Wert dieses Felds nicht ändern.  
          
          *   `Individual account`  
              Ein einzelnes Konto ist für einen Entwickler geeignet, der nicht mit einem Unternehmen verbunden ist.  Die Kontoverifizierung ist kürzer und umfasst die Überprüfung, ob der Anzeigename des Herausgebers verfügbar ist.  

          *   `Company account`  
              Ein Unternehmenskonto ist einer Organisation oder einem Unternehmen zugeordnet.  Der Vorgang zur Kontoüberprüfung ist länger, und es wird bestätigt, dass Sie zum Erstellen des Kontos für Ihr Unternehmen autorisiert sind.  Die Dauer des Prozesses kann zwischen wenigen Tagen und einigen Wochen liegen.  Ihr Unternehmen kann Telefonanrufe von Microsoft Verification-Partnern erhalten.  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="1":::
          **Anzeigename des Herausgebers**  
       :::column-end:::
       :::column span="2":::
          Dieses Feld ist der Name, der Benutzern im Microsoft Edge-Add-ons-Katalog angezeigt wird.  Sie dürfen einen Namen nur verwenden, wenn er verfügbar ist, und Sie haben die Rechte, ihn zu verwenden.  Unternehmenskonten müssen den registrierten Firmennamen Ihrer Organisation verwenden.  
          
          > [!NOTE]
          > Die maximale Länge für dieses Feld beträgt 50 Zeichen.  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="1":::
          **Kontaktdetails**  
       :::column-end:::
       :::column span="2":::
          Dieses Feld enthält alle Kontaktinformationen, die Microsoft verwenden kann, um Sie bezüglich etwaiger Konto Probleme zu kontaktieren.  Nachdem die Registrierung abgeschlossen ist, wird eine e-Mail-Bestätigung an Sie gesendet.  Für ein Unternehmenskonto müssen Sie die registrierte e-Mail-Adresse verwenden, die Ihrer Organisation zugeordnet ist.  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="1":::
          **Genehmigende Person des Unternehmens**  
       :::column-end:::
       :::column span="2":::
          Bei einem Unternehmenskonto müssen Sie die Kontaktinformationen der genehmigenden Person des Unternehmens (Name, e-Mail-Adresse und Telefonnummer) angeben.  Microsoft Contacts die genehmigende Person des Unternehmens, die als Teil des Überprüfungsprozesses angegeben wurde, um sicherzustellen, dass die Erweiterung zu Ihrer Organisation gehört.  
       :::column-end:::
    :::row-end:::  
    <!-- -->
    <!--
    1.  The **Account country/region** field  
        
        This field is where you either live or your business is located.  
        
        > [!IMPORTANT]
        > After enrollment, you are not able to change the value of this field.  
        
    1.  The **Account type** field  
        
        The Microsoft Edge program in [Partner Center][MicrosoftPartnerCenter] offers both individual and company accounts, which are described in detail in the table that follows.  Both account types allow you to publish extensions to the Microsoft Edge add-ons catalog.  
        
        > [!IMPORTANT]
        > After enrollment, you are not able to change the value of this field.  
        
        | Individual account | Company account |  
        |:--- |:--- |  
        | Individual accounts are appropriate for developers not associated with a company.  | Company accounts are associated with organizations and businesses.  |  
        | The account verification process is shorter, and involves verifying that the publisher display name is available.  | The account verification process is longer, and involves confirmation that you are authorized to create the account for your company.  The duration of the process may range from a few days to a few weeks.  Your company may receive phone calls from Microsoft verification partners.  |  
        
    1.  The **Publisher display name** field  
        
        This field is the name shown to users in the Microsoft Edge add-ons catalog.  You may use a name only if it is available, and you have the rights to use it.  Company accounts must use the registered business name of your organization.  
        
        > [!NOTE]
        > The maximum length for this field is 50 characters.  
        
    1.  The **Contact details** field  
        
        Any contact information that Microsoft may use to contact you regarding any account issues.  After registration is complete, an email confirmation is sent to you.  Company accounts must use the registered email address associated with your organization.  
        
    1.  The **Company approver** field  
        
        For company accounts, provide the contact information \(name, email address, and phone number\) of your company approver.  Microsoft contacts the company approver specified as a part of the verification process to ensure that the extensions belong to your organization.  
        -->
1. Bevor Sie Ihr Registrierungsformular übermitteln, lesen und akzeptieren Sie die allgemeinen Geschäftsbedingungen des [Microsoft Edge-Entwickler Vertrags][MicrosoftAppDeveloperAgreement].  
1. Um die Registrierung abzuschließen, wählen Sie **Fertig stellen**aus.  

## Nächste Schritte  

Sie können Ihren Verifizierungsstatus auf der Seite " **Kontoeinstellungen** " im Partner Center einsehen.  Während Sie auf den Abschluss des Überprüfungsvorgangs warten; Sie können Ihre Übermittlungen weiter erstellen, testen und vorbereiten.  

Weitere Informationen finden Sie unter [Veröffentlichen einer Erweiterung][ExtensionsChromiumPublishExtension].  Informationen zu den ersten Schritten mit Erweiterungen finden Sie unter [Erste Schritte mit Microsoft Edge (Chrom)-Erweiterungen][ExtensionsChromiumGettingStartedIndex].  

<!-- links -->  

[ExtensionsChromiumGettingStartedIndex]: ../getting-started/index.md "Erste Schritte mit Microsoft Edge (Chrom)-Erweiterungen | Microsoft docs"  
[ExtensionsChromiumPublishExtension]:  ./publish-extension.md "Veröffentlichen einer Erweiterung | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]:  /legal/windows/agreements/app-developer-agreement "Vereinbarung für App-Entwickler | Microsoft docs"  

[MicrosoftAccount]:  https://account.microsoft.com/account "Microsoft-Konto"  

[MicrosoftPartnerCenter]:  https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[WindowsCommunityEverythingAboutMicrosoftAccounts]:  https://community.windows.com/stories/everything-you-need-to-know-about-microsoft-accounts "Microsoft (oder MSA)"  