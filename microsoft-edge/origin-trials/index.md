---
ms.assetid: ''
description: Experimentieren Sie sicher während eines bestimmten Zeitraums, und geben Sie Feedback zu neuen Plattformfeatures.
title: Origin-Testversionen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, Origin Trials, Entwickler
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846528"
---
# Verwenden von Ursprungs versuchen in Microsoft Edge  

Entwickler können mithilfe von Origin Trials experimentelle APIs auf Live-Websites für einen bestimmten Zeitraum testen.  Bei Verwendung von Ursprungs Testversionen können Benutzer von Microsoft Edge, die Ihre Website besuchen, Code ausführen, der experimentelle APIs verwendet.  Wenn Sie auf die experimentellen APIs auf jedem Benutzer Computer zugreifen möchten, müssen Sie nicht zu den `edge://flags` Feature-Flags wechseln und diese aktivieren.  Weitere Informationen finden Sie unter [experimentelle APIs][DeveloperMicrsoftEdgeOriginTrials].  Darüber hinaus können Sie Feedback über das Design der API, ihre Anwendungsfälle oder Ihre Erfahrungen mithilfe der APIs für Browser Ingenieure und die Web-Standard Community bereitstellen.  

## Erste Schritte mit Origin-Testversionen  

Weitere Informationen zu den in Microsoft Edge verfügbaren experimentellen APIs finden Sie unter [Entwicklerkonsole für Microsoft Edge Origin Trials][DeveloperMicrsoftEdgeOriginTrials].  Stellen Sie sicher, dass Sie die Mindestsystemanforderungen für Microsoft Edge und das Enddatum der Testversion überprüfen, um die Eignung der Verwendung der experimentellen APIs auf Ihrer Website zu bewerten.  

> [!NOTE]
> Ein Experiment kann früher als geplant enden, wenn eine der folgenden Situationen eintritt.  
> *   Ein wichtiger Sicherheitsvorfall.  
> *   Wenn genügend Feedback erfasst wird, das darauf hinweist, dass eine größere Neugestaltung erforderlich ist, um die Anforderungen von Webentwicklern zu erfüllen.  
> In beiden Fällen wird eine Benachrichtigungs-e-Mail an alle Entwickler gesendet, die zurzeit beim Experiment registriert sind.  

### Registrieren für eine Testversion einer experimentellen API  

Führen Sie die folgenden Schritte aus, um sich für eine Testversion einer experimentellen API zu registrieren.  

1.  Besuchen Sie die [Microsoft Edge Origin Trials-Entwickler Konsolen][DeveloperMicrsoftEdgeOriginTrials] Seite.  
1.  Wählen Sie die Schaltfläche Registrieren in einem der verfügbaren Experimente aus.  
1.  Melden Sie sich mit Ihrem GitHub-Nutzernamen und Kennwort bei der Entwicklerkonsole an.  
1.  Wählen Sie **MicrosoftEdge autorisieren**aus.  
1.  Füllen Sie das Formular aus.  
    
    > [!NOTE]
    > Wenn Sie eine einzelne oder alle Unterdomänen registrieren möchten, wählen Sie `Do you need to match all subdomains for the provided origin?` Einstellung festlegen auf aus `Yes` .  Beispielsweise `https://dev.contoso.com` handelt es sich um eine einzelne Domäne, bei der `https://*.contoso.com` alle Unterdomänen als Platzhalter dargestellt werden.  
    
    > [!IMPORTANT]
    > Die folgenden Ursprungs Formate sind nicht zulässig.  
    > *   Angeben eines Unterordners für den Ursprung  Beispiel: `https://contoso.com/path/subfolder`  
    > 
    > *   Verwenden eines Ursprungs mit Abfragezeichenfolgenparametern  Beispiel: `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Wählen Sie **annehmen und registrieren**aus.  

### Anwenden des Tokens  

Ein Token wird sofort generiert und auf der [Microsoft Edge Origin Trials-Entwickler Konsolen][DeveloperMicrsoftEdgeOriginTrials] Seite angezeigt.  Wenn Sie die Testversion auf Ihrer Website verwenden möchten, verwenden Sie eine der folgenden Methoden, um das Token auf Ihre Seite anzuwenden.  

*   Fügen Sie dem `origin-trial` `meta` Tag auf jeder Seite, die die experimental-API verwendet, den Attributwert und das Token hinzu.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   Fügen Sie `Origin-Trial` den HTTP-Antwortheader Ihres Servers hinzu.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> Ihr Token ist für 6 Wochen gültig.  Bevor Ihr Testabonnement endet, werden Erinnerungs-e-Mails an Sie gesendet, die nach Ihrem Feedback Fragen, und Sie bitten, Ihre Testversion zu erneuern, bevor Ihr Token abläuft.  

### Deaktivieren eines Experiments  

Wenn Sie ein Experiment deaktivieren möchten, verwenden Sie eine der folgenden Methoden, um Ihr Token zu entfernen.  

*   Entfernen Sie die `meta` Kategorie von jeder Seite, die die experimental-API verwendet hat.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Entfernen Sie `Origin-Trial` aus dem HTTP-Antwortheader Ihres Servers.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### Erkennen experimenteller Features und Bereitstellen eines Fallbacks  

Stellen Sie bei der Verwendung von experimentellen APIs sicher, dass Sie allen Besuchern Ihrer Website ein Arbeitserlebnis bieten.  Besucher können Browser verwenden, die die experimentellen APIs, die Sie Ihrem Code hinzugefügt haben, nicht unterstützen.  Wenn Ihr Token abläuft, bevor Sie es erneuern, ist die experimentelle API nicht mehr verfügbar, was zu Fehlern führen kann.  Um dies zu vermeiden, stellen Sie sicher, dass Sie die in Ihrem Browser verfügbaren Funktionen erkennen.  Weitere Informationen finden Sie unter [Implementieren der Feature-Erkennung][MDNImplementingFeatureDetection].

### Roadmap für zulässige Ursprünge  

Das Microsoft Edge-Ursprungs testportal unterstützt heute nur SSL-aktivierte Ursprünge, was bedeutet, dass für Websites https richtig implementiert sein muss, damit Sie sich für ein Experiment registrieren können.  In Zukunft sind die folgenden sicheren Ursprünge geplant.  

*   Registrieren `http://localhost` Sie sich als Ursprung für ihre Experimente.  Um heute zu verwenden `http://localhost` , wechseln Sie zu, `edge://flags` und legen Sie das Experiment auf **aktiviert**.  
*   Verwenden Sie Erweiterungen mit `extensions://` vorfesten Ursprüngen, um sich bei Experimenten zu registrieren.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials-Entwicklerkonsole | Microsoft docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementieren der Feature-Erkennung | MDN"  
