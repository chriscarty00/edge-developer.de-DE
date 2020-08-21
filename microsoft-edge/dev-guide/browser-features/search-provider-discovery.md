---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Wenn Sie ein Suchanbieter sind, finden Sie Informationen dazu, wie Sie sicherstellen können, dass Microsoft Edge ihren Dienst unterstützt.
title: Suchanbieter Ermittlung – dev-Leitfaden
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, Web-Entwicklung, HTML, CSS, JavaScript, Entwickler
ms.openlocfilehash: 4ac8ea966e9c4736834a0be1130a8c2a8dfb2614
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941969"
---
# <span data-ttu-id="e7d4f-104">Suchanbieterermittlung</span><span class="sxs-lookup"><span data-stu-id="e7d4f-104">Search provider discovery</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="e7d4f-105">Die Rich-Search-Integration ist in die Microsoft Edge-Adressleiste integriert, einschließlich Suchvorschlägen, Ergebnissen aus dem Internet, dem Browserverlauf und Favoriten.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="e7d4f-106">Microsoft Edge folgt der [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) -Spezifikation, um Anbieter von Websuchen zu ermitteln und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-106">Microsoft Edge follows the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification to discover and use web search providers.</span></span>  <span data-ttu-id="e7d4f-107">Wenn Sie ein Suchanbieter sind, gehen Sie wie folgt vor, um sicherzustellen, dass Microsoft Edge ihren Dienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>  

> <span data-ttu-id="e7d4f-108">Wichtig Für Benutzersicherheit und Datenschutz erfordert Microsoft Edge, dass alle Suchvorgänge über SSL durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-108">[IMPORTANT] For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>  

<span data-ttu-id="e7d4f-109">Die folgenden Ressourcen müssen als URLs angegeben werden, damit die `https` Microsoft Edge-Integration Ihrer Suchmaschine möglich ist:</span><span class="sxs-lookup"><span data-stu-id="e7d4f-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>  

*   <span data-ttu-id="e7d4f-110">Die Website, die den Verweis auf das Beschreibungs Dokument enthält</span><span class="sxs-lookup"><span data-stu-id="e7d4f-110">The site that contains the reference to the description document</span></span>  
*   <span data-ttu-id="e7d4f-111">Die URL des Beschreibungs Dokuments selbst</span><span class="sxs-lookup"><span data-stu-id="e7d4f-111">The URL to the description document itself</span></span>  
*   <span data-ttu-id="e7d4f-112">Die Suchabfrage Vorlage</span><span class="sxs-lookup"><span data-stu-id="e7d4f-112">The search query template</span></span>  

1.  <span data-ttu-id="e7d4f-113">Stellen Sie eine OpenSearch-Beschreibungsdatei bereit, die den Namen des Suchanbieters enthält, und die Vorlage, mit der die Suche erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span>  <span data-ttu-id="e7d4f-114">Hier ist ein Beispieldokument:</span><span class="sxs-lookup"><span data-stu-id="e7d4f-114">Here is an example document:</span></span>  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  <span data-ttu-id="e7d4f-115">Fügen Sie einen Verweis auf Ihre OpenSearch-Beschreibungsdatei in den Kopfzeilenbereich Ihrer Seiten ein (in der Regel würde dies die Startseite Ihrer Website und die Suchergebnisseiten umfassen), beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="e7d4f-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>  
    
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
    
<span data-ttu-id="e7d4f-116">Wenn ein Benutzer zu Ihrem Suchdienst durchsucht, wird Ihre OpenSearch-Beschreibung automatisch aufgenommen und zur späteren Verwendung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span>  <span data-ttu-id="e7d4f-117">Der Benutzer kann dann zu den Microsoft Edge-Einstellungen wechseln und den Suchdienst zur Liste der Suchanbieter für die Microsoft Edge-Adressleiste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>  

<span data-ttu-id="e7d4f-118">Weitere Informationen zum Erstellen Ihres OpenSearch-Beschreibungs Dokuments finden Sie in der [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) -Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-118">See the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification for further details on creating your OpenSearch description document.</span></span>  
