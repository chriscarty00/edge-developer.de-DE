---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Wenn Sie ein Suchanbieter sind, finden Sie Informationen dazu, wie Sie sicherstellen können, dass Microsoft Edge ihren Dienst unterstützt.
title: Dev Guide-Suchanbieter Ermittlung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: ac23c2c62d436d5772b498208a56ad306eb8cb3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566765"
---
# Suchanbieter Ermittlung


Die Rich-Search-Integration ist in die Microsoft Edge-Adressleiste integriert, einschließlich Suchvorschlägen, Ergebnissen aus dem Internet, dem Browserverlauf und Favoriten. Microsoft Edge folgt der [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) -Spezifikation, um Anbieter von Websuchen zu ermitteln und zu verwenden. Wenn Sie ein Suchanbieter sind, gehen Sie wie folgt vor, um sicherzustellen, dass Microsoft Edge ihren Dienst unterstützt.

**Für Benutzersicherheit und Datenschutz erfordert Microsoft Edge, dass alle Suchvorgänge über SSL durchgeführt werden.** Die folgenden Ressourcen müssen als URLs angegeben werden, damit die `https` Microsoft Edge-Integration Ihrer Suchmaschine möglich ist:
* Die Website, die den Verweis auf das Beschreibungs Dokument enthält
* Die URL des Beschreibungs Dokuments selbst
* Die Suchabfrage Vorlage 

1.  Stellen Sie eine OpenSearch-Beschreibungsdatei bereit, die den Namen des Suchanbieters enthält, und die Vorlage, mit der die Suche erstellt werden soll. Hier ist ein Beispieldokument:

    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```

2.  Fügen Sie einen Verweis auf Ihre OpenSearch-Beschreibungsdatei in den Kopfzeilenbereich Ihrer Seiten ein (in der Regel würde dies die Startseite Ihrer Website und die Suchergebnisseiten umfassen), beispielsweise:

    ```html
    <html>
        <head>
            <link rel="search" 
                type="application/opensearchdescription+xml"  
                href="https://contoso.com/content-search.xml" 
                title="Contoso search" /> 
        </head> 
        <body> 
        ...
    ```

Wenn ein Benutzer zu Ihrem Suchdienst durchsucht, wird Ihre OpenSearch-Beschreibung automatisch aufgenommen und zur späteren Verwendung gespeichert. Der Benutzer kann dann zu den Microsoft Edge-Einstellungen wechseln und den Suchdienst zur Liste der Suchanbieter für die Microsoft Edge-Adressleiste hinzufügen.

Weitere Informationen zum Erstellen Ihres OpenSearch-Beschreibungs Dokuments finden Sie in der [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) -Spezifikation.
