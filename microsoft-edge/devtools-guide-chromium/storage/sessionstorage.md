---
description: Anzeigen und Bearbeiten von sessionStorage mit dem Sitzungsspeicherbereich und der Konsole.
title: Anzeigen und Bearbeiten des Sitzungsspeichers mit Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, Entwicklungstools
ms.openlocfilehash: cf00d71302e7a1f16ba1cceaa17c9380245d12f8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398007"
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

# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a>Anzeigen und Bearbeiten des Sitzungsspeichers mit Microsoft Edge DevTools  

In diesem Handbuch erfahren Sie, wie [Sie Microsoft Edge DevTools][MicrosoftEdgeDevTools] zum Anzeigen, Bearbeiten und Löschen von SessionStorage-Schlüssel-Wert-Paaren verwenden. [][MDNSessionStorage]  

## <a name="view-sessionstorage-keys-and-values"></a>Anzeigen von sessionStorage-Schlüsseln und -Werten  

1.  Wählen Sie die **Registerkarte Anwendung** aus, um das **Anwendungstool zu** öffnen.  Der **Manifestbereich** wird standardmäßig angezeigt.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Der Manifestbereich" lightbox="../media/storage-application-manifest.msft.png":::
       Der **Manifestbereich**  
    :::image-end:::  
    
1.  Erweitern Sie **das Menü Sitzungsspeicher.**  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Das Menü "Sitzungsspeicher"" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       Das **Menü "Sitzungsspeicher"**  
    :::image-end:::  
    
1.  Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Die SessionStorage-Schlüssel-Wert-Paare" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Die `sessionStorage` Schlüssel-Wert-Paare  
    :::image-end:::  
    
1.  Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unterhalb der Tabelle anzeigen zu können.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Anzeigen des Werts des x-sid-Schlüssels" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Anzeigen des Werts des `x-sid` Schlüssels  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a>Erstellen eines neuen sessionStorage-Schlüssel-Wert-Paars  

1.  [Zeigen Sie die sessionStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)  
1.  Doppelklicken Sie auf den leeren Teil der Tabelle.  DevTools erstellt eine neue Zeile und konzentriert den Cursor in der **Spalte Schlüssel.**  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen." lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       Der leere Teil der Tabelle, auf den sie doppelklicken soll, um ein neues Schlüssel-Wert-Paar zu erstellen.  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a>Bearbeiten von sessionStorage-Schlüsseln oder -Werten  

1.  [Zeigen Sie die sessionStorage-Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)  
1.  Doppelklicken Sie in der Spalte **Schlüssel** oder **Wert** auf eine Zelle, um diesen Schlüssel oder Wert zu bearbeiten.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Bearbeiten eines sessionStorage-Schlüssels" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Bearbeiten eines `sessionStorage` Schlüssels  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a>SessionStorage-Schlüssel-Wert-Paare löschen  

1.  [Zeigen Sie `sessionStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt es blau hervor, um anzugeben, dass es ausgewählt ist.  
1.  Wählen Sie `Delete` den Schlüssel aus, oder wählen **Sie Ausgewählte \(** ![ Ausgewählte Option löschen ][ImageDeleteIcon] \) aus.  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a>Löschen aller sessionStorage-Schlüssel-Wert-Paare für eine Domäne  

1.  [Zeigen Sie `sessionStorage` die Schlüssel-Wert-Paare einer Domäne an.](#view-sessionstorage-keys-and-values)  
1.  Wählen **Sie Alle löschen** \( Alle löschen ![ ][ImageClearIcon] \).  
    
## <a name="interact-with-sessionstorage-from-the-console"></a>Interagieren mit sessionStorage über die Konsole  

Da Sie JavaScript in der Konsole **** ausführen können **und**die Konsole Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit über die Konsole `sessionStorage` zu **interagieren.**  

1.  Verwenden Sie **das Menü JavaScript-Kontexte,** **** um den JavaScript-Kontext der Konsole zu ändern, wenn Sie auf die Schlüssel-Wert-Paare einer anderen Domäne als der Seite zugreifen möchten, auf der `sessionStorage` Sie sich befinden.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Ändern des JavaScript-Kontexts der Konsole" lightbox="../media/storage-console-domain-selection.msft.png":::
       Ändern des JavaScript-Kontexts der **Konsole**  
    :::image-end:::  
    
1.  Führen Sie `sessionStorage` Ihre Ausdrücke in **der Konsole**aus, die mit Ihrem JavaScript identisch ist.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagieren mit sessionStorage über die Konsole" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interagieren mit `sessionStorage` über die **Konsole**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Mit dem Microsoft Edge-Entwicklungstools-Team Kontakt aufnehmen  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Entwicklertools | Microsoft Docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf [von Google erstellten und freigegebenen][GoogleSitePolicies] Werken basieren und gemäß den in der [Creative Commons Attribution 4.0 International License][CCA4IL] beschriebenen Bestimmungen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) und wird von [Kayce Basken][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) verfasst.  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
