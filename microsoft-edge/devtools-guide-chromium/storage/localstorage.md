---
description: Anzeigen und Bearbeiten von localStorage mit dem Bereich "Lokaler Speicher" und der Konsole.
title: Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: 4eebf3108e7b1c6ecaecbfed445e8f3fe26215c4
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439675"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a>Anzeigen und Bearbeiten des lokalen Speichers mit Microsoft Edge DevTools  

In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools][MicrosoftEdgeDevTools] zum Anzeigen, Bearbeiten und Löschen von localStorage-Schlüssel-Wert-Paaren verwenden. [][MDNWindowsLocalStorage]  

## <a name="view-localstorage-keys-and-values"></a>Anzeigen von localStorage-Schlüsseln und -Werten  

1.  Wählen Sie die **Registerkarte Anwendung** aus, um das **Anwendungstool zu** öffnen.  Der **Manifestbereich** wird standardmäßig angezeigt.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       Der **Manifestbereich**  
    :::image-end:::  
    
1.  Erweitern Sie **das Menü Lokaler Speicher.**  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Menü Lokaler Speicher" lightbox="../media/storage-application-local-storage.msft.png":::
       Menü **"Lokaler Speicher"**  
    :::image-end:::  
    
1.  Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Die localStorage-Schlüssel-Wert-Paare für die https://www.bing.com Domäne" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       Die `localStorage` Schlüssel-Wert-Paare für die `https://www.bing.com` Domäne  
    :::image-end:::  
    
1.  Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unterhalb der Tabelle anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Anzeigen des Werts des eventLogQueue_Online Schlüssels" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Anzeigen des Werts des `eventLogQueue_Online` Schlüssels  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a>Erstellen eines neuen localStorage-Schlüssel-Wert-Paars  

1.  [Zeigen Sie die localStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)  
1.  Doppelklicken Sie auf den leeren Teil der Tabelle.  DevTools erstellt eine neue Zeile und konzentriert den Cursor in der **Spalte Schlüssel.**  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen." lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen.  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a>Bearbeiten von localStorage-Schlüsseln oder -Werten  

1.  [Zeigen Sie die localStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)  
1.  Doppelklicken Sie in der Spalte **Schlüssel** oder **Wert** auf eine Zelle, um diesen Schlüssel oder Wert zu bearbeiten.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Bearbeiten eines localStorage-Schlüssels" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Bearbeiten eines `localStorage` Schlüssels  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a>Löschen von localStorage-Schlüssel-Wert-Paaren  

1.  [Zeigen Sie `localStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt es blau hervor, um anzugeben, dass es ausgewählt ist.  
1.  Wählen Sie `Delete` den Schlüssel aus, oder wählen **Sie Ausgewählte \(** ![ Ausgewählte Option löschen ](../media/delete-icon.msft.png) \) aus.  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a>Löschen aller `localStorage` Schlüssel-Wert-Paare für eine Domäne  

1.  [Zeigen Sie `localStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-localstorage-keys-and-values)  
1.  Wählen **Sie Alle löschen** \( Alle löschen ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-localstorage-from-the-console"></a>Interagieren mit localStorage über die Konsole  

Da Sie JavaScript in der Konsole ausführen **** können **und**die Konsole Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit über die Konsole `localStorage` zu **interagieren.**  

1.  Verwenden Sie **das Menü JavaScript-Kontexte,** um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die Schlüssel-Wert-Paare einer anderen Domäne als der angezeigten Seite `localStorage` zugreifen möchten.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Ändern des JavaScript-Kontexts der Konsole" lightbox="../media/storage-console-local-storage.msft.png":::
       Ändern des JavaScript-Kontexts der Konsole  
    :::image-end:::  
    
1.  Führen Sie `localStorage` Ihre Ausdrücke in der Konsole aus, genauso wie in Ihrem JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagieren mit localStorage über die Konsole" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interagieren mit `localStorage` über die **Konsole**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
