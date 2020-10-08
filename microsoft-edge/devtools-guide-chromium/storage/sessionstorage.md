---
description: Informationen zum Anzeigen und Bearbeiten von sessionStorage mit dem Sitzungsspeicher Bereich und der Konsole.
title: Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, Webentwicklung, F12-Tools, DevTools
ms.openlocfilehash: 24fca3fd3a068f3b2ffbe4ec1c23e6b80b968953
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993548"
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





# Anzeigen und Bearbeiten des Sitzungs Speichers mit Microsoft Edge devtools   

  

In diesem Leitfaden wird gezeigt, wie Sie mit [Microsoft Edge devtools][MicrosoftEdgeDevTools] [`sessionStorage`][MDNSessionStorage] Schlüssel-Wert-Paare anzeigen, bearbeiten und löschen können.  

## Anzeigen von sessionStorage-Schlüsseln und-Werten   

1.  Wählen Sie die Registerkarte **Anwendung** aus, um den **Anwendungs** Panel zu öffnen.  Standardmäßig wird der Bereich **Manifest** angezeigt.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-manifest.msft.png":::
       Bereich ' **Manifest** '  
    :::image-end:::  
    
1.  Erweitern Sie das Menü **Sitzungsspeicher** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       Das Menü " **Sitzungsspeicher** "  
    :::image-end:::  
    
1.  Wählen Sie eine Domäne aus, um die Schlüssel-Wert-Paare anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Die `sessionStorage` Schlüssel-Wert-Paare  
    :::image-end:::  
    
1.  Wählen Sie eine Zeile der Tabelle aus, um den Wert im Viewer unter der Tabelle anzuzeigen.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Anzeigen des Werts des `x-sid` Schlüssels  
    :::image-end:::  
    
## Erstellen eines neuen sessionStorage-Schlüssel-Wert-Paars   

1.  [Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)  
1.  Doppelklicken Sie auf den leeren Teil der Tabelle.  DevTools erstellt eine neue Zeile und fokussiert den Cursor in der **Schlüssel** Spalte.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       Der leere Teil der Tabelle zum doppelklicken, um ein neues Schlüssel-Wert-Paar zu erstellen  
    :::image-end:::  
    
## Bearbeiten von sessionStorage-Schlüsseln oder-Werten   

1.  [Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)  
1.  Doppelklicken Sie auf eine Zelle in der Spalte **Schlüssel** oder **Wert** , um diesen Schlüssel oder Wert zu bearbeiten.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Bearbeiten eines `sessionStorage` Schlüssels  
    :::image-end:::  
    
## Löschen von sessionStorage-Schlüssel-Wert-Paaren   

1.  [Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)  
1.  Wählen Sie das Schlüssel-Wert-Paar aus, das Sie löschen möchten.  DevTools hebt das Blau hervor, um anzugeben, dass es markiert ist.  
1.  Drücken Sie die Eingabe `Delete` Taste, oder klicken Sie auf **Ausgewählte löschen** \ ( ![ Auswahl löschen ][ImageDeleteIcon] \).  
    
## Löschen aller sessionStorage-Schlüssel-Wert-Paare für eine Domäne   

1.  [Anzeigen der `sessionStorage` Schlüssel-Wert-Paare einer Domäne](#view-sessionstorage-keys-and-values)  
1.  Wählen Sie **Alle löschen** \ ( ![ Alle löschen ][ImageClearIcon] \) aus.  
    
## Interagieren mit sessionStorage über die Konsole   

Da sie JavaScript in der **Konsole**ausführen können und die **Konsole** Zugriff auf die JavaScript-Kontexte der Seite hat, ist es möglich, mit `sessionStorage` der **Konsole**zu interagieren.  

1.  Verwenden Sie das **JavaScript** -Kontextmenü, um den JavaScript-Kontext der **Konsole** zu ändern, wenn Sie auf die `sessionStorage` Schlüssel-Wert-Paare einer anderen Domäne als auf die Seite zugreifen möchten, auf der Sie sich befinden.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-console-domain-selection.msft.png":::
       Ändern des JavaScript-Kontexts der Konsole  
    :::image-end:::  
    
1.  Führen Sie Ihre `sessionStorage` Ausdrücke in der Konsole wie in Ihrem JavaScript aus.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Bereich ' Manifest '" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interagieren mit `sessionStorage` der **Konsole**  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Microsoft Edge (Chrom)-Entwicklertools | Microsoft docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> Teile dieser Seite sind Änderungen, die auf der [von Google erstellten und freigegebenen][GoogleSitePolicies] Arbeit basieren und gemäß den in der [Creative Commons Attribution 4,0 International-Lizenz][CCA4IL]beschriebenen Begriffen verwendet werden.  
> Die ursprüngliche Seite befindet sich [hier](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) und wird von [Kayce Basken][KayceBasques] (Technical Writer, Chrome devtools \ & Lighthouse \) erstellt.  

[![Creative Commons-Lizenz][CCby4Image]][CCA4IL]  
Diese Arbeit unterliegt einer [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
