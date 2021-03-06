---
ms.assetid: ''
description: Experimentieren Sie sicher für einen bestimmten Zeitraum und geben Sie Feedback zu neuen Plattformfeatures.
title: Herkunfts Versuche
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, origin trials, developer
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397545"
---
# <a name="use-origin-trials-in-microsoft-edge"></a>Verwenden von Origin Trials in Microsoft Edge  

Entwickler können Origin Trials verwenden, um experimentelle APIs auf Livewebsites für einen begrenzten Zeitraum auszuprobieren.  Bei Verwendung von Origin Trials können Benutzer von Microsoft Edge, die Ihre Website besuchen, Code ausführen, der experimentelle APIs verwendet.  Um auf die experimentellen APIs auf jedem Benutzercomputer zu zugreifen, müssen Sie nicht zu feature flags `edge://flags` wechseln und diese aktivieren.  Weitere Informationen finden Sie unter Experimentelle [APIs][DeveloperMicrsoftEdgeOriginTrials].  Darüber hinaus können Sie Feedback zum Entwurf der API, zu Ihren Verwendungsfällen oder zur Verwendung der APIs für Browsertechniker und die Webstandard-Community bereitstellen.  

## <a name="get-started-using-origin-trials"></a>Erste Schritte mit Origin Trials  

Weitere Informationen zu den in Microsoft Edge verfügbaren experimentellen APIs finden Sie unter [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].  Stellen Sie sicher, dass Sie die Mindestversionsanforderungen für Microsoft Edge und das Testenddatum überprüfen, um die Eignung der Verwendung der experimentellen APIs auf Ihrer Website zu bewerten.  

> [!NOTE]
> Ein Experiment kann früher als geplant enden, wenn eine der folgenden Situationen auftritt.  
> *   Ein wichtiger Sicherheitsvorfall.  
> *   Wenn genügend Feedback gesammelt wird, das darauf hinweist, dass eine wesentliche Neugestaltung erforderlich ist, um die Anforderungen von Webentwicklern zu erfüllen.  
> In beiden Fällen wird eine Benachrichtigungs-E-Mail an alle Entwickler gesendet, die derzeit für das Experiment registriert sind.  

### <a name="register-for-a-trial-of-an-experimental-api"></a>Registrieren für eine Testversion einer experimentellen API  

Verwenden Sie die folgenden Schritte, um sich für eine Testversion einer experimentellen API zu registrieren.  

1.  Besuchen Sie die [Seite Microsoft Edge Origin Trials Developer Console.][DeveloperMicrsoftEdgeOriginTrials]  
1.  Wählen Sie in einem der verfügbaren Experimente die Schaltfläche Registrieren aus.  
1.  Melden Sie sich mit Ihrem GitHub-Benutzernamen und -Kennwort bei der Entwicklerkonsole an.  
1.  Wählen **Sie MicrosoftEdge autorisieren aus.**  
1.  Füllen Sie das Formular aus.  
    
    > [!NOTE]
    > Um eine einzelne oder alle Unterdomänen zu registrieren, wählen Sie Festlegen der `Do you need to match all subdomains for the provided origin?` Einstellung auf `Yes` aus.  Beispielsweise handelt es sich um eine einzelne Domäne und verwendet einen Platzhalter, um alle `https://dev.contoso.com` `https://*.contoso.com` Unterdomänen zu repräsentieren.  
    
    > [!IMPORTANT]
    > Die folgenden Ursprungsformate sind nicht zulässig.  
    > *   Angeben eines Unterordners für den Ursprung.  Beispiel: `https://contoso.com/path/subfolder`  
    > 
    > *   Verwenden eines Ursprungs mit Abfragezeichenfolgenparametern.  Beispiel: `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Wählen **Sie ACCEPT und REGISTER aus.**  
    
### <a name="apply-your-token"></a>Anwenden des Tokens  

Ein Token wird sofort generiert und auf der [Seite Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] angezeigt.  Verwenden Sie eine der folgenden Methoden, um die Testversion auf Ihrer Website zu verwenden, um das Token auf Ihre Seite anzuwenden.  

*   Fügen Sie dem Tag auf jeder Seite, die die experimentelle API verwendet, den Attributwert und das Token `origin-trial` `meta` hinzu.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   Fügen `Origin-Trial` Sie dem HTTP-Antwortheader Ihres Servers hinzu.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> Ihr Token ist 6 Wochen gültig.  Bevor Ihre Testversion endet, werden Erinnerungs-E-Mails an Sie gesendet, die Um Ihr Feedback bitten und Sie bitten, ihre Testversion zu verlängern, bevor Ihr Token abläuft.  

### <a name="opt-out-of-an-experiment"></a>Abmelden eines Experiments  

Wenn Sie ein Experiment abmelden möchten, verwenden Sie eine der folgenden Methoden, um Ihr Token zu entfernen.  

*   Entfernen Sie `meta` das Tag von jeder Seite, auf der die experimentelle API verwendet wurde.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Entfernen `Origin-Trial` Sie aus dem HTTP-Antwortheader Ihres Servers.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a>Erkennen experimenteller Features und Bereitstellen eines Fallbacks  

Stellen Sie bei der Verwendung experimenteller APIs sicher, dass Sie allen Besuchern Ihrer Website eine Arbeitserfahrung bieten.  Besucher können Browser verwenden, die die experimentellen APIs, die Sie Ihrem Code hinzugefügt haben, nicht unterstützen.  Wenn Ihr Token abläuft, bevor Sie es verlängern, ist die experimentelle API nicht mehr verfügbar, was zu Fehlern führen kann.  Um diese Situation zu vermeiden, stellen Sie sicher, dass Sie features erkennen, die in Ihrem Browser verfügbar sind.  Weitere Informationen finden Sie unter Implementieren der [Featureerkennung][MDNImplementingFeatureDetection].

### <a name="roadmap-for-allowed-origins"></a>Roadmap für zulässige Ursprünge  

Das Microsoft Edge Origin Trials-Portal unterstützt heute nur SSL-aktivierte Ursprünge, was bedeutet, dass für Websites HTTPS ordnungsgemäß implementiert sein muss, um sich für ein Experiment registrieren zu können.  In Zukunft sind die folgenden sicheren Ursprünge geplant.  

*   Registrieren `http://localhost` Sie sich als Ursprung für Ihre Experimente.  Navigieren Sie `http://localhost` zu, `edge://flags` und legen Sie das Experiment auf Enabled **(Aktiviert) vor,** um es heute zu verwenden.  
*   Verwenden Sie Erweiterungen `extensions://` mit präfixen Ursprüngen, um sich für Experimente zu registrieren.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Microsoft Docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementieren von Featureerkennungs| MDN"  
