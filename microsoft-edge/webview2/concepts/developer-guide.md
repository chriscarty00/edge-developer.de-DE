---
description: Erfahren Sie mehr über bewährte Methoden für die Entwicklung ihrer WebView2-Anwendung.
title: Bewährte Methoden für die WebView2-Entwicklung
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/04/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, Webview, Edge, bewährte Methoden
ms.openlocfilehash: 5a09d48cc9972a310c865fcdd6c10e4ed96451fc
ms.sourcegitcommit: b51df5036642060525e03cd744b7d35726326abe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526097"
---
# <a name="webview2-development-best-practices"></a>Bewährte Methoden für die WebView2-Entwicklung  

Jedes Entwicklungsteam folgt beim Erstellen seiner Anwendung unterschiedlichen Methoden. Wenn Sie WebView2-Anwendungen erstellen, empfehlen wir Ihnen, die folgenden Methoden zu befolgen. In diesem Artikel werden diese Empfehlungen und bewährten Methoden für Sie beim Erstellen produktionsbasierter WebView2-Anwendungen beschrieben.


## <a name="use-evergreen-webview2-runtime-recommended"></a>Verwenden von Evergreen WebView2 Runtime (empfohlen)  

Fixed Version verfügt zwar über Anwendungsfälle für Apps mit strengen Kompatibilitätsanforderungen, es wird jedoch im Allgemeinen empfohlen, die Evergreen WebView2 Runtime zu verwenden.  Die Evergreen WebView2-Laufzeit wird automatisch aktualisiert und enthält die neuesten Features und Sicherheitspatches, die für Ihre WebView2-Anwendung verfügbar sind. Die Laufzeit von Evergreen WebView2 erfordert auch weniger Speicherplatz auf dem Datenträger.

Stellen Sie sicher, dass die Evergreen WebView2-Runtime installiert ist, bevor Sie Ihre WebView2-Anwendung verwenden.  Weitere Informationen finden Sie unter [Deploying the Evergreen WebView2 Runtime][Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime].  

## <a name="run-compatibility-tests-regularly-when-using-the-evergreen-webview2-runtime"></a>Führen Sie bei Verwendung der Evergreen WebView2 Runtime regelmäßig Kompatibilitätstests aus.

Stellen Sie bei Verwendung der Evergreen WebView2 Runtime sicher, dass Sie regelmäßige Kompatibilitätstests ausführen. Da die Laufzeit automatisch aktualisiert wird, testen Sie den Webinhalt im WebView2-Steuerelement mit den nicht stabilen Versionen von Microsoft Edge, um sicherzustellen, dass Ihre WebView2-Anwendung wie erwartet ausgeführt wird. Diese Anleitung ähnelt den Anleitungen, die wir Webentwicklern geben. Weitere Informationen finden Sie unter [Stay compatible in Evergreen Mode][Webview2ConceptsDistributionStayCompatibleEvergreenMode].

## <a name="ensure-apis-are-supported-by-the-installed-webview2-runtime"></a>Sicherstellen, dass APIs von der installierten WebView2-Runtime unterstützt werden

WebView2-Anwendungen benötigen sowohl ein Webview2 SDK als auch eine auf dem Computer installierte WebView2-Runtime, um ausgeführt zu werden. Sowohl das SDK als auch die Laufzeit sind versioniert. Da APIs ständig zu WebView2 hinzugefügt werden, werden auch neue Versionen der Laufzeit veröffentlicht, um die neuen APIs zu unterstützen. Sie müssen sicherstellen, dass die apIs, die von Ihrer WebView2-Anwendung verwendet werden, von der WebView2-Runtime unterstützt werden, die auf dem Computer installiert ist. 

Wenn Sie die Evergreen WebView2 Runtime verwenden, gibt es einige Szenarien, in denen die Laufzeit möglicherweise nicht für die Verwendung der neuesten Version aktualisiert wird. Wenn Benutzer beispielsweise keinen Internetzugriff haben, wird die Laufzeit in dieser Umgebung nicht automatisch aktualisiert. Darüber hinaus werden durch die Verwendung einiger Gruppenrichtlinien WebView2-Updates angehalten. Wenn Sie ein Update für Ihre WebView2-Anwendung pushen, kann die Anwendung nicht mehr ausgeführt werden, da sie neuere APIs verwendet, die in der installierten Laufzeit nicht verfügbar sind.   
 
Um diese Situation zu lösen, können Sie die Verfügbarkeit der APIs in der installierten Laufzeit testen, bevor Der Code die API aufruft. Dieser Test auf neuere Funktionen ähnelt anderen bewährten Methoden für die Webentwicklung, die unterstützte Features erkennen, bevor neue Web-APIs verwendet werden. Verwenden Sie zum Testen der API-Verfügbarkeit in der installierten Laufzeit:
* Die `queryinterface` in C/C++. 
* Ein Try/Catch-Block in .NET oder WinUI. 
    
Weitere Informationen finden Sie unter [Determine WebView2 Runtime requirement][Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement].  

## <a name="update-the-fixed-version-runtime"></a>Aktualisieren der Laufzeit für feste Versionen  

Wenn Sie die Fixed Version Runtime verwenden, stellen Sie sicher, dass Sie Ihre Laufzeit regelmäßig aktualisieren, um potenzielle Sicherheitsrisiken zu reduzieren. Bei der Verwendung von Drittanbieterinhalten in Webview2-Anwendungen sollten Sie den Inhalt immer als nicht vertrauenswürdig betrachten.  Weitere Informationen finden Sie unter [Fixed Version distribution mode][Webview2ConceptsDistributionFixedVersionDistributionMode].  

## <a name="manage-new-versions-of-the-runtime"></a>Verwalten neuer Versionen der Laufzeit  

Wenn eine neue Version der Evergreen WebView2 Runtime auf das Gerät heruntergeladen wird, wird die Ausführung von WebView2-Anwendungen mit der vorherigen Laufzeit fortgesetzt, bis der Browserprozess freigegeben wird. Dieses Verhalten ermöglicht die kontinuierliche Ausführung von Anwendungen und verhindert, dass die vorherige Laufzeit gelöscht wird. Um die neue Version der Laufzeit zu verwenden, müssen Sie alle Verweise auf die vorherigen WebView2-Umgebungsobjekte veröffentlichen oder Die Anwendung neu starten. Beim nächsten Erstellen einer neuen WebView2-Umgebung wird die neue Version verwendet.

Wenn eine neue Version verfügbar ist, z. B. den Benutzer zum Neustart der Anwendung benachrichtigen, können Sie das [Ereignis add_NewBrowserVersionAvailable(Win32)][Webview2ReferenceaddNewBrowserVersionAvailable] oder [CoreWebView2Environment.NewBrowserVersionAvailable(.NET)][Webview2ReferenceNewBrowserVersionAvailable] in Ihrem Code verwenden. Wenn der Code den Neustart der Anwendung behandelt, sollten Sie den Benutzerstatus speichern, bevor die WebView2-Anwendung beendet wird.  

## <a name="manage-the-lifetime-of-the-user-data-folder"></a>Verwalten der Lebensdauer des Benutzerdatenordners 
WebView2-Apps erstellen einen Benutzerdatenordner zum Speichern von Daten wie Cookies, Anmeldeinformationen, Berechtigungen und so weiter. Nach dem Erstellen des Ordners ist Ihre App für die Verwaltung der Lebensdauer des Benutzerdatenordners verantwortlich, einschließlich der Bereinigung, wenn die App deinstalliert wird.  Weitere Informationen finden Sie unter [Managing the User Data Folder][Webview2ConceptsUserdatafolder].  

## <a name="follow-recommended-webview2-security-best-practices"></a>Befolgen empfohlener bewährter WebView2-Sicherheitsmethoden 
Stellen Sie sicher, dass Sie für jede WebView2-Anwendung die empfohlenen bewährten WebView2-Sicherheitsmethoden befolgen.  Weitere Informationen finden Sie unter [Best practices for developing secure WebView2 applications][Webview2ConceptsSecurity].  


<!-- links -->  

[Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]: ../concepts/distribution.md#deploying-the-evergreen-webview2-runtime "Bereitstellen der Evergreen WebView2 Runtime – Verteilung von Apps mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ../concepts/distribution.md#fixed-version-distribution-mode "Verteilungsmodus mit fester Version – Verteilung von Apps mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionStayCompatibleEvergreenMode]: ../concepts/distribution.md#stay-compatible-in-evergreen-mode "Im Immergrünmodus kompatibel bleiben – Verteilung von Apps mithilfe von WebView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ../concepts/security.md "Bewährte Methoden für die Entwicklung sicherer WebView2-| Microsoft Docs"  
[Webview2ConceptsUserdatafolder]: ../concepts/userdatafolder.md "Verwalten des Benutzerdatenordners | Microsoft Docs"  
[Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]: ../concepts/versioning.md#determine-webview2-runtime-requirement "Bestimmen der WebView2-Laufzeitanforderung – Verstehen der WebView2 SDK-| Microsoft Docs"  
[Webview2GettingstartedWin32]: ../gettingstarted/win32.md "Erste Schritte mit WebView2 | Microsoft Docs"  
[Webview2GettingstartedWinforms]: ../gettingstarted/winforms.md "Erste Schritte mit WebView2 in Windows Forms | Microsoft Docs"  
[Webview2GettingstartedWinui]: ../gettingstarted/winui.md "Erste Schritte mit WebView2 in WinUI 3 (Vorschau) | Microsoft Docs"  
[Webview2GettingstartedWpf]: ../gettingstarted/wpf.md "Erste Schritte mit WebView2 in WPF | Microsoft Docs"  
[Webview2ReferenceaddNewBrowserVersionAvailable]: https://docs.microsoft.com/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable "add_NewBrowserVersionAvailable | Microsoft Docs"  
[Webview2ReferenceNewBrowserVersionAvailable]: https://docs.microsoft.com/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable "CoreWebView2Environment.NewBrowserVersionAvailable Event | Microsoft Docs"  