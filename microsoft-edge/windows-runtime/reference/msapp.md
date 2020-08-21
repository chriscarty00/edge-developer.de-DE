---
title: MSApp-API-Referenz
description: Stellt Hilfsfunktionen bereit, mit deren Hilfe Sie BLOB-und MSStream-Objekte erstellen können.  MSApp-Objekte und-Member werden für Windows-apps mit JavaScript unterstützt.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, Dateiupload, Blog, MSStream, Windows 10-apps, UWP, Edge
ms.openlocfilehash: 4966f6afbe4e971d6a366de7e9b4f5a6cd2305e0
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942168"
---
# <span data-ttu-id="809be-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="809be-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="809be-106">Das MSApp-Objekt und seine Member werden nur für Windows-Apps unterstützt, die JavaScript verwenden \ (einschließlich PWAs Zugriff auf die Windows-API-Funktionen).</span><span class="sxs-lookup"><span data-stu-id="809be-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="809be-107">Das MSApp-Objekt ist nur im lokalen Kontext eines HTML-Dokuments in einer Windows-app vorhanden, die über das URI-Schema "MS-AppX" geladen wird. Andernfalls ist das Objekt nicht vorhanden (und daher sind keine seiner Methoden und Eigenschaften verfügbar).</span><span class="sxs-lookup"><span data-stu-id="809be-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="809be-108">Sie stellt Hilfsfunktionen bereit, mit deren Hilfe Sie [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) -und [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) -Objekte erstellen können.</span><span class="sxs-lookup"><span data-stu-id="809be-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="809be-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="809be-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="809be-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getviewl](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="809be-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="809be-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="809be-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="809be-112">[aktuell](#current), [groß](#high), [inaktiv](#idle), [Normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="809be-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="809be-113">MSAppAsyncOperation-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="809be-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="809be-114">start</span><span class="sxs-lookup"><span data-stu-id="809be-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="809be-115">MSApp-Methoden</span><span class="sxs-lookup"><span data-stu-id="809be-115">MSApp methods</span></span>  

### <span data-ttu-id="809be-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="809be-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-117">Löscht Cache-und indexedDB-Daten für die APP oder [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="809be-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-118">Parameters</span></span>**  
      
      <span data-ttu-id="809be-119">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="809be-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-120">Return value</span></span>**  
      
      <span data-ttu-id="809be-121">Geben Sie Folgendes ein: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="809be-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="809be-122">Stellt eine asynchrone Aktion dar.</span><span class="sxs-lookup"><span data-stu-id="809be-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-123">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-123">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-124">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-125">Remarks</span></span>**  
      
      <span data-ttu-id="809be-126">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="809be-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-129">Erstellt ein [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) aus einem [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="809be-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="809be-130">Diese Methode sollte beim Umgang mit `IRandomAccessStream` Objekten in Apps verwendet werden, um ein W3C-basiertes Objekt aus dem Datenstrom zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="809be-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="809be-131">Nachdem das BLOB erstellt wurde, kann es mit [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL-APIs](https://developer.mozilla.org/docs/Web/API/URL)und [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="809be-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="809be-133">in</span><span class="sxs-lookup"><span data-stu-id="809be-133">[in]</span></span>  
      
      | <span data-ttu-id="809be-134">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-134">Type</span></span> | <span data-ttu-id="809be-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="809be-136">String</span></span> | <span data-ttu-id="809be-137">Inhaltstyp der Daten.</span><span class="sxs-lookup"><span data-stu-id="809be-137">Content type of the data.</span></span>  <span data-ttu-id="809be-138">Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="809be-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="809be-139">in</span><span class="sxs-lookup"><span data-stu-id="809be-139">[in]</span></span>  
      
      | <span data-ttu-id="809be-140">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-140">Type</span></span> | <span data-ttu-id="809be-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-142">Any</span><span class="sxs-lookup"><span data-stu-id="809be-142">Any</span></span> | <span data-ttu-id="809be-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) , der im BLOB gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="809be-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-144">Return value</span></span>**  
      
      | <span data-ttu-id="809be-145">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-145">Type</span></span> | <span data-ttu-id="809be-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-147">BLOB</span><span class="sxs-lookup"><span data-stu-id="809be-147">Blob</span></span> | <span data-ttu-id="809be-148">Neues BLOB-Objekt, das den Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="809be-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-149">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="809be-150">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="809be-150">Exception</span></span> | <span data-ttu-id="809be-151">Bedingung</span><span class="sxs-lookup"><span data-stu-id="809be-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="809be-152">TypeMismatchError</span></span> | <span data-ttu-id="809be-153">Der Knotentyp ist mit dem erwarteten Parametertyp nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="809be-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="809be-154">Bei älteren Versionen als Internet Explorer 10 wird TYPE_MISMATCH_ERR zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="809be-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-155">Remarks</span></span>**  
      
      <span data-ttu-id="809be-156">Erstellt ein BLOB aus Windows-Runtime-Typen über den MSApp-Namespace für das Window-Objekt.</span><span class="sxs-lookup"><span data-stu-id="809be-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="809be-157">Diese Methode erstellt ein BLOB, das im Wesentlichen ein Licht Wrapper über dem [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) -Objekt ist, das ihm bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="809be-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="809be-158">Das BLOB besitzt die Lebensdauer dieses Streams, und der Datenstrom wird geschlossen, wenn das BLOB zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="809be-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-159">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-159">Example</span></span>**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="809be-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-161">Wandelt den angegebenen Bereich des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="809be-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="809be-163">in</span><span class="sxs-lookup"><span data-stu-id="809be-163">[in]</span></span>  
      
      | <span data-ttu-id="809be-164">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-164">Type</span></span> | <span data-ttu-id="809be-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-166">Any</span><span class="sxs-lookup"><span data-stu-id="809be-166">Any</span></span> | <span data-ttu-id="809be-167">Dieser Bereich kann entweder aus einem Selection-Objekt, beispielsweise: `window.selection.getRangeAt(0)` oder manuell, erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="809be-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-168">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-168">Return value</span></span>**  
      
      | <span data-ttu-id="809be-169">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-169">Type</span></span> | <span data-ttu-id="809be-170">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-171">Any</span><span class="sxs-lookup"><span data-stu-id="809be-171">Any</span></span> | <span data-ttu-id="809be-172">Enthält das HTML-Markup für den angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="809be-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-173">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-173">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-174">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-175">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-175">Remarks</span></span>**  
      
      <span data-ttu-id="809be-176">Diese Methode unterstützt nur den [DOM-Bereich (Document Object Model)](https://developer.mozilla.org/docs/Web/API/Range), nicht [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="809be-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="809be-177">Das zurückgegebene Datenpaket für den angegebenen Bereich enthält HTML-Markup im Zwischenablageformat.</span><span class="sxs-lookup"><span data-stu-id="809be-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="809be-178">Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.</span><span class="sxs-lookup"><span data-stu-id="809be-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-179">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-179">Example</span></span>**  
      
      <span data-ttu-id="809be-180">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="809be-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-182">Wandelt die Auswahl des Benutzers oder der Anwendung in ein HTML-Fragment um, das freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="809be-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-183">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-183">Parameters</span></span>**  
      
      <span data-ttu-id="809be-184">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="809be-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-185">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-185">Return value</span></span>**  
      
      | <span data-ttu-id="809be-186">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-186">Type</span></span> | <span data-ttu-id="809be-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-188">Any</span><span class="sxs-lookup"><span data-stu-id="809be-188">Any</span></span> | <span data-ttu-id="809be-189">Enthält das HTML-Markup für den angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="809be-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-190">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-190">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-191">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-192">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-192">Remarks</span></span>**  
      
      <span data-ttu-id="809be-193">Das zurückgegebene Datenpaket für die Auswahl enthält HTML-Markup im Zwischenablageformat.</span><span class="sxs-lookup"><span data-stu-id="809be-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="809be-194">Wenn keine Benutzerauswahl an einer beliebigen Stelle auf der Benutzeroberfläche der Anwendung vorhanden ist, wird der Wert `createDataPackageFromSelection` zurückgegeben `null` .</span><span class="sxs-lookup"><span data-stu-id="809be-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="809be-195">Es gibt keine verfügbaren Eigenschaften für das zurückgegebene Datenpaket.</span><span class="sxs-lookup"><span data-stu-id="809be-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-196">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <span data-ttu-id="809be-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="809be-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-198">Konvertiert eine [WinRT](/uwp/api/) - [Speicher](/uwp/api/windows.storage.storagefile) Datei in ein Standard-W3C- [Datei](https://developer.mozilla.org/docs/Web/API/File) Objekt.</span><span class="sxs-lookup"><span data-stu-id="809be-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-199">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="809be-200">in</span><span class="sxs-lookup"><span data-stu-id="809be-200">[in]</span></span>
      
      | <span data-ttu-id="809be-201">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-201">Type</span></span> | <span data-ttu-id="809be-202">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-203">Any</span><span class="sxs-lookup"><span data-stu-id="809be-203">Any</span></span> | <span data-ttu-id="809be-204">Enthält die Speicherdatei.</span><span class="sxs-lookup"><span data-stu-id="809be-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-205">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-205">Return value</span></span>**
      
      <span data-ttu-id="809be-206">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-207">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="809be-208">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="809be-208">Exception</span></span> | <span data-ttu-id="809be-209">Bedingung</span><span class="sxs-lookup"><span data-stu-id="809be-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="809be-210">TypeMismatchError</span></span> | <span data-ttu-id="809be-211">Der angegebene W3C-Dateiverweis ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="809be-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="809be-212">Für Versionen, die älter als Internet Explorer 10 sind, `TYPE_MISMATCH_ERR` wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="809be-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-213">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-213">Remarks</span></span>**  
      
      <span data-ttu-id="809be-214">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-215">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="809be-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-217">Erstellt eine [MSStream](https://msdn.microsoft.com/library/hh772328) aus einem [InputStream](https://msdn.microsoft.com/library/hh772327).</span><span class="sxs-lookup"><span data-stu-id="809be-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-218">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="809be-219">in</span><span class="sxs-lookup"><span data-stu-id="809be-219">[in]</span></span>
      
      | <span data-ttu-id="809be-220">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-220">Type</span></span> | <span data-ttu-id="809be-221">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-222">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-222">DOMString</span></span> | <span data-ttu-id="809be-223">Inhaltstyp der Daten.</span><span class="sxs-lookup"><span data-stu-id="809be-223">Content type of the data.</span></span>  <span data-ttu-id="809be-224">Diese Zeichenfolge sollte das Format aufweisen, das in dem in Abschnitt 3,7 von RFC 2616 definierten Media-Type-Token angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="809be-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="809be-225">\ ([Siehe MIME-Typen] (wie,,,,,,,, usw https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` `text/html` `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` . \).</span><span class="sxs-lookup"><span data-stu-id="809be-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="809be-226">in</span><span class="sxs-lookup"><span data-stu-id="809be-226">[in]</span></span>
      
      | <span data-ttu-id="809be-227">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-227">Type</span></span> | <span data-ttu-id="809be-228">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-229">Any</span><span class="sxs-lookup"><span data-stu-id="809be-229">Any</span></span> | <span data-ttu-id="809be-230">Die [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) , die in der gespeichert werden soll `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="809be-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-231">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-231">Return value</span></span>**
      
      <span data-ttu-id="809be-232">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-233">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-233">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-234">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-235">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-235">Remarks</span></span>**  
      
      <span data-ttu-id="809be-236">Diese Methode verwendet einen Inhaltstyp und den `IInputStream` Verweis.</span><span class="sxs-lookup"><span data-stu-id="809be-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="809be-237">Die Methode überprüft dann, ob es sich bei dem übergebenen Datenstrom Verweis um eine Instanz von Type handelt `IInputStream` , und wenn dies nicht der Fall ist, wird ausgelöst `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="809be-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="809be-238">Wenn kein Fehler auftritt, wird `createStreamFromInputStream` ein `MSStream` \ (aus seinen Eingaben \) erstellt.</span><span class="sxs-lookup"><span data-stu-id="809be-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-239">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-239">Example</span></span>**  
      
      <span data-ttu-id="809be-240">Eine `IInputStream` kann verwendet werden, um eine zu erstellen `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="809be-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="809be-241">Da `MSStreams` es sich um eigenständige Objekte mit einmaliger Verwendung handelt, werden alle von Ihnen erstellten URLs `URL.createObjectURL` beim erstmaligen lösen durch das Image-Element aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="809be-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="809be-242">Darüber hinaus schlägt die Anforderung einer zweiten URL für dieses Objekt, nachdem der Datenstrom verwendet wurde, fehl.</span><span class="sxs-lookup"><span data-stu-id="809be-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="809be-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-244">Plant einen Rückruf, der zu einem späteren Zeitpunkt entsprechend der angegebenen Priorität ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="809be-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-245">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="809be-246">in</span><span class="sxs-lookup"><span data-stu-id="809be-246">[in]</span></span>
      
      | <span data-ttu-id="809be-247">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-247">Type</span></span> | <span data-ttu-id="809be-248">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-249">Funktion</span><span class="sxs-lookup"><span data-stu-id="809be-249">Function</span></span> | <span data-ttu-id="809be-250">Die Rückruffunktion, die asynchron ausgeführt werden soll, wird mit der angegebenen Prioritäts Priorität verteilt.</span><span class="sxs-lookup"><span data-stu-id="809be-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="809be-251">in</span><span class="sxs-lookup"><span data-stu-id="809be-251">[in]</span></span>
      
      | <span data-ttu-id="809be-252">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-252">Type</span></span> | <span data-ttu-id="809be-253">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-254">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-254">DOMString</span></span> | <span data-ttu-id="809be-255">Der kontextbezogene Prioritätswert, in dem der asynchronousCallback-Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="809be-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="809be-256">Siehe [MSApp-Konstanten](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="809be-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="809be-257">in</span><span class="sxs-lookup"><span data-stu-id="809be-257">[in]</span></span>
      
      | <span data-ttu-id="809be-258">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-258">Type</span></span> | <span data-ttu-id="809be-259">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="809be-260">Any</span><span class="sxs-lookup"><span data-stu-id="809be-260">Any</span></span> | <span data-ttu-id="809be-261">Eine optionale Reihe von Argumenten, die an die synchronousCallback-Rückruffunktion \ (als Parameter 1 usw. \) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="809be-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-262">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-262">Return value</span></span>**  
      
      <span data-ttu-id="809be-263">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="809be-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-264">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-264">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-265">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-266">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-266">Remarks</span></span>**  
      
      <span data-ttu-id="809be-267">Die bereitgestellte `asynchronousCallback` Rückruffunktion wird später asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="809be-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="809be-268">wird entsprechend der angegebenen Priorität versandt.</span><span class="sxs-lookup"><span data-stu-id="809be-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="809be-269">Die normale Priorität entspricht der vorhandenen [setimmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="809be-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="809be-270">Wenn der Rückruf ausgeführt wird, wird die aktuelle kontextbezogene Priorität für die Dauer der Ausführung des Rückrufs auf den angegebenen Prioritäts Parameterwert gesetzt.</span><span class="sxs-lookup"><span data-stu-id="809be-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="809be-271">Der `asynchronousCallback` Rückrufparameter kann eine beliebige Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="809be-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="809be-272">Wenn Argumente nach dem Parameter bereitgestellt werden `priority` , werden Sie alle an die Rückruffunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="809be-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="809be-273">Im Gegensatz dazu `execAtPriority` wird jedes von der Rückruffunktion zurückgegebene Objekt `asynchronousCallback` ignoriert \ (und nicht über `execAsyncAtPriority` \) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="809be-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-274">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="809be-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-276">Führt die angegebene Rückruffunktion unter der angegebenen Kontext Priorität aus.</span><span class="sxs-lookup"><span data-stu-id="809be-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-277">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="809be-278">in</span><span class="sxs-lookup"><span data-stu-id="809be-278">[in]</span></span>  
      
      | <span data-ttu-id="809be-279">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-279">Type</span></span> | <span data-ttu-id="809be-280">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-281">Funktion</span><span class="sxs-lookup"><span data-stu-id="809be-281">Function</span></span> | <span data-ttu-id="809be-282">Die Rückruffunktion, die mit der angegebenen Prioritäts Kontext Priorität synchron ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="809be-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="809be-283">in</span><span class="sxs-lookup"><span data-stu-id="809be-283">[in]</span></span>  
      
      | <span data-ttu-id="809be-284">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-284">Type</span></span> | <span data-ttu-id="809be-285">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-286">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-286">DOMString</span></span> | <span data-ttu-id="809be-287">Der angegebene Prioritätswert, auf den der aktuelle kontextabhängige Prioritätswert festgelegt wird, wenn die `synchronousCallback` Rückruffunktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="809be-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="809be-288">Siehe [MSApp-Konstanten](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="809be-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="809be-289">in</span><span class="sxs-lookup"><span data-stu-id="809be-289">[in]</span></span>  
      
      | <span data-ttu-id="809be-290">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-290">Type</span></span> | <span data-ttu-id="809be-291">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-292">Any</span><span class="sxs-lookup"><span data-stu-id="809be-292">Any</span></span> | <span data-ttu-id="809be-293">Eine optionale Reihe von Argumenten, die an die `synchronousCallback` Rückruffunktion \ (als Parameter 1 usw. \) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="809be-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-294">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-294">Return value</span></span>**  
      
      | <span data-ttu-id="809be-295">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-295">Type</span></span> | <span data-ttu-id="809be-296">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-297">Any</span><span class="sxs-lookup"><span data-stu-id="809be-297">Any</span></span> | <span data-ttu-id="809be-298">Gibt den Rückgabewert des `synchronousCallback` Rückrufs zurück \ (sofern zutreffend \).</span><span class="sxs-lookup"><span data-stu-id="809be-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-299">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-299">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-300">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-301">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-301">Remarks</span></span>**  
      
      <span data-ttu-id="809be-302">Die bereitgestellte `synchronousCallback` Rückrufmethode wird synchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="809be-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="809be-303">Die aktuelle kontextbezogene Priorität wird für die Dauer der bereitgestellten Rückruffunktion in den angegebenen Prioritätswert (angegeben durch das Prioritäts Argument) geändert.</span><span class="sxs-lookup"><span data-stu-id="809be-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="809be-304">Sobald die Rückruffunktion die Ausführung beendet hat, wird die Priorität vor dem Aufruf an den vorherigen Wert zurückgegeben `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="809be-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="809be-305">Der Rückgabewert von `execAtPriority` ist der Rückgabewert der Rückrufmethode \ (wie angegeben \).</span><span class="sxs-lookup"><span data-stu-id="809be-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="809be-306">Der `synchronousCallback` Rückrufparameter kann eine beliebige Funktion sein.</span><span class="sxs-lookup"><span data-stu-id="809be-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="809be-307">Wenn nach dem Priority-Parameter Argumente bereitgestellt werden, werden Sie an die bereitgestellte Rückrufmethode übergeben.</span><span class="sxs-lookup"><span data-stu-id="809be-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="809be-308">Wenn der Rückrufparameter einen Wert zurückgibt, wird dieser Wert ebenfalls zum Rückgabewert `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="809be-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-309">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-309">Example</span></span>**  
      
      ```javascript
      var user = Windows.System.UserProfile.UserInformation;
      
      MSApp.execAtPriority(function () { // This callback executes synchronously.
        user.getFirstNameAsync().then(function () { // Dispatches at high priority.
          return user.getLastNameAsync();
        }).done(function () { // Dispatches at high priority.
          // USEFUL CODE HERE
        });
      }, MSApp.HIGH); // The second argument of the execAtPriority method.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="809be-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-311">Gibt die aktuelle kontextbezogene Priorität zurück.</span><span class="sxs-lookup"><span data-stu-id="809be-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-312">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-312">Parameters</span></span>**  
      
      <span data-ttu-id="809be-313">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-314">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-314">Return value</span></span>**  
      
      | <span data-ttu-id="809be-315">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-315">Type</span></span> | <span data-ttu-id="809be-316">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-317">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-317">DOMString</span></span> | <span data-ttu-id="809be-318">Der Rückgabewert ist eine der Zeichenfolgen `MSApp.HIGH` , `MSApp.NORMAL` oder `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="809be-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-319">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-319">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-320">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-321">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-321">Remarks</span></span>**  
      
      <span data-ttu-id="809be-322">Diese Methode gibt die aktuelle kontextbezogene Priorität zurück (siehe [MSApp-Konstanten](#msapp-constants)\), die über und geändert werden kann `execAtPriority` `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="809be-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-323">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-323">Example</span></span>**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="809be-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="809be-325">Synchrone API, die als veraltet markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="809be-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="809be-326">Informationen zu Windows 10 finden Sie unter `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="809be-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="809be-327">Informationen zu Windows 8-und 8,1-apps finden Sie im MSDN-Eintrag für [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="809be-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="809be-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="809be-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-329">Gibt den Quellinhalt zurück, der gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="809be-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-330">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="809be-331">in</span><span class="sxs-lookup"><span data-stu-id="809be-331">[in]</span></span>  
      
      | <span data-ttu-id="809be-332">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-332">Type</span></span> | <span data-ttu-id="809be-333">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-334">Dokument</span><span class="sxs-lookup"><span data-stu-id="809be-334">Document</span></span> | <span data-ttu-id="809be-335">Das HTML-Dokument, das gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="809be-335">The HTML document to be printed.</span></span>  <span data-ttu-id="809be-336">Dies kann das Stammdokument, das Dokument in einem IFRAME, ein Dokument Fragment oder ein SVG-Dokument sein.</span><span class="sxs-lookup"><span data-stu-id="809be-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="809be-337">Beachten Sie, dass htmlDoc ein Dokument und kein Element sein muss.</span><span class="sxs-lookup"><span data-stu-id="809be-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-338">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-338">Return value</span></span>**
      
      <span data-ttu-id="809be-339">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-340">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-340">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-341">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-342">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-342">Remarks</span></span>**  
      
      <span data-ttu-id="809be-343">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-344">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="809be-344">Example 1</span></span>**  
      
      ```javascript
      var printTask = event.request.createPrintTask(title, function (args) {
              var deferral = args.getDeferral();
              var getPrintDocumentSourceAsync;
              if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                  getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
              } else {
                  getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
              }
              getPrintDocumentSourceAsync.then(function (source) {
                  args.setSource(source);
                  deferral.complete();
              }, function (error) {
                  console.error(error);
                  deferral.complete();
              });
      });
      ```  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-345">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="809be-345">Example 2</span></span>**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
      }
      
      // Variable to hold the document source to print
      var gHtmlPrintDocumentSource = null;
      
      // Print event handler for printing via the PrintManager API.
      function onPrintTaskRequested(printEvent) {
          var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
              args.setSource(gHtmlPrintDocumentSource);
      
              // Register the handler for print task completion event
              printTask.oncompleted = onPrintTaskCompleted;
          });
      }
      
      // Print Task event handler is invoked when the print job is completed.
      function onPrintTaskCompleted(printTaskCompletionEvent) {
          // Notify the user about the failure
          if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
              console.log("Failed to print.", "sample", "error");
          }
      }
      
      // Executed just before printing.
      var beforePrint = function () {
          // Replace with code to be executed just before printing the current document:
      };
      
      // Executed immediately after printing.
      var afterPrint = function () {
          // Replace with code to be executed immediately after printing the current document:
      };
      
      function printButtonHandler() {
          // Optionally, functions to be executed immediately before and after printing can be configured as following:
          window.document.body.onbeforeprint = beforePrint;
          window.document.body.onafterprint = afterPrint;
          
          // Get document source to print
          MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
              gHtmlPrintDocumentSource = htmlPrintDocumentSource;
      
              // If the print contract is registered, the print experience is invoked.
              Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
          });
      }
      ```  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-346">GetView-Nr.</span><span class="sxs-lookup"><span data-stu-id="809be-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-347">Unterstützung für mehrere Fenster.</span><span class="sxs-lookup"><span data-stu-id="809be-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="809be-348">In Win 8.1 JavaScript UWP-apps wurden mehrere Fenster unterstützt, die MSApp-DOM-APIs verwenden, die jetzt depricated sind.</span><span class="sxs-lookup"><span data-stu-id="809be-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="809be-349">Verwenden Sie für Windows 10 `window.open` `window` und das neue `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="809be-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="809be-350">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-350">Description</span></span> |<span data-ttu-id="809be-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="809be-351">Windows 10</span></span> | <span data-ttu-id="809be-352">Windows8.1</span><span class="sxs-lookup"><span data-stu-id="809be-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="809be-353">Neues Fenster erstellen</span><span class="sxs-lookup"><span data-stu-id="809be-353">Create new window</span></span> | [<span data-ttu-id="809be-354">Window. Open</span><span class="sxs-lookup"><span data-stu-id="809be-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="809be-355">MSApp. createNewView</span><span class="sxs-lookup"><span data-stu-id="809be-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="809be-356">Neues Fensterobjekt</span><span class="sxs-lookup"><span data-stu-id="809be-356">New window object</span></span> | [<span data-ttu-id="809be-357">Fenster</span><span class="sxs-lookup"><span data-stu-id="809be-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="809be-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="809be-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-359">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="809be-360">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-360">Type</span></span> | <span data-ttu-id="809be-361">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-362">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-362">DOMString</span></span> | <span data-ttu-id="809be-363">Ein Objekt, das ein Fenster darstellt, das ein DOM-Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="809be-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-364">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="809be-365">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-365">Type</span></span> | <span data-ttu-id="809be-366">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-367">Zahl</span><span class="sxs-lookup"><span data-stu-id="809be-367">Number</span></span> | <span data-ttu-id="809be-368">Kann mit den verschiedenen [Windows. UI. ViewManagement. ApplicationViewSwitcher-](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="809be-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-369">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-369">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-370">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-371">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-371">Remarks</span></span>**  
      
      <span data-ttu-id="809be-372">Verwenden Sie [Window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) und [Window](https://developer.mozilla.org/docs/Web/API/Window) zum Erstellen neuer Fenster, aber um dann mit WinRT-APIs zu interagieren, fügen Sie die `MSApp.getViewId` API hinzu.</span><span class="sxs-lookup"><span data-stu-id="809be-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="809be-373">Sie nimmt ein `window` Objekt als Parameter an und gibt eine `viewId` Zahl zurück, die mit den verschiedenen [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) -APIs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="809be-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="809be-374">Verzögern der Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="809be-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="809be-375">Ansichten in WinRT werden normalerweise ausgeblendet, und der endentwickler verwendet so etwas wie `TryShowAsStandaloneAsync` , um die Ansicht anzuzeigen, sobald Sie vollständig vorbereitet ist.</span><span class="sxs-lookup"><span data-stu-id="809be-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="809be-376">In der Web-Welt wird `window.open` sofort ein Fenster angezeigt, und der Endbenutzer kann beobachten, wie Inhalte geladen und gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="809be-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="809be-377">Damit Ihre neuen Windows-Ansichten in WinRT und nicht sofort angezeigt werden, haben wir eine Option hinzugefügt `window.open` .</span><span class="sxs-lookup"><span data-stu-id="809be-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="809be-378">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="809be-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="809be-379">Unterschiede im primären Fenster</span><span class="sxs-lookup"><span data-stu-id="809be-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="809be-380">Das primäre Fenster, das zunächst vom Betriebssystem geöffnet wird, fungiert anders als das von ihm geöffnete sekundäre Fenster:</span><span class="sxs-lookup"><span data-stu-id="809be-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="809be-381">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-381">Description</span></span> | <span data-ttu-id="809be-382">Primär</span><span class="sxs-lookup"><span data-stu-id="809be-382">Primary</span></span> | <span data-ttu-id="809be-383">Sekundärer</span><span class="sxs-lookup"><span data-stu-id="809be-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="809be-384">Window. Open</span><span class="sxs-lookup"><span data-stu-id="809be-384">window.open</span></span> | <span data-ttu-id="809be-385">Zugelassen</span><span class="sxs-lookup"><span data-stu-id="809be-385">Allowed</span></span> | <span data-ttu-id="809be-386">Disallowed</span><span class="sxs-lookup"><span data-stu-id="809be-386">Disallowed</span></span> |  
          | <span data-ttu-id="809be-387">Fenster. Schließen</span><span class="sxs-lookup"><span data-stu-id="809be-387">window.close</span></span> | <span data-ttu-id="809be-388">APP schließen</span><span class="sxs-lookup"><span data-stu-id="809be-388">Close app</span></span> | <span data-ttu-id="809be-389">Fenster schließen</span><span class="sxs-lookup"><span data-stu-id="809be-389">Close window</span></span> |  
          | <span data-ttu-id="809be-390">Navigations Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="809be-390">Navigation restrictions</span></span> | <span data-ttu-id="809be-391">Nur ACUR</span><span class="sxs-lookup"><span data-stu-id="809be-391">ACUR only</span></span> | <span data-ttu-id="809be-392">Keine Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="809be-392">No restrictions</span></span> |  
          
          <span data-ttu-id="809be-393">Die Einschränkung, dass sekundäre Fenster nicht geöffnet werden können, kann sich in Zukunft je nach [Feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)ändern.</span><span class="sxs-lookup"><span data-stu-id="809be-393">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>  
      
      *   <span data-ttu-id="809be-394">Kommunikationseinschränkungen für denselben Ursprung</span><span class="sxs-lookup"><span data-stu-id="809be-394">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="809be-395">Es gibt ein schwieriges technisches Problem, das die korrekte Unterstützung für synchrone, identische Ursprungs-, Fenster-und Skriptaufrufe verhindert.</span><span class="sxs-lookup"><span data-stu-id="809be-395">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="809be-396">Wenn Sie ein Fenster öffnen, das denselben Ursprung hat, kann das Skript in einem Fensterfunktionen direkt im anderen Fenster aufrufen, und einige dieser Aufrufe können nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="809be-396">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="809be-397">Anrufe funktionieren prima und sind die empfohlene Vorgehensweise, wenn es möglich ist.</span><span class="sxs-lookup"><span data-stu-id="809be-397">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="809be-398">Arbeiten zur Verbesserung dieses Problems sind in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="809be-398">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-399">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-399">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <span data-ttu-id="809be-400">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="809be-400">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-401">Gibt einen booleschen Wert zurück, der angibt, ob die Arbeit auf der angegebenen Prioritätsstufe oder höher aussteht.</span><span class="sxs-lookup"><span data-stu-id="809be-401">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-402">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-402">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="809be-403">in</span><span class="sxs-lookup"><span data-stu-id="809be-403">[in]</span></span>
      
      | <span data-ttu-id="809be-404">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-404">Type</span></span> | <span data-ttu-id="809be-405">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-405">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-406">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-406">DOMString</span></span> | <span data-ttu-id="809be-407">Ein Prioritätswert \ (siehe [MSApp-Konstanten](#msapp-constants)\), der die Prioritätsstufe und höher angibt, um nach ausstehender in der Warteschlange befindlicher Arbeit zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="809be-407">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-408">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-408">Return value</span></span>**  
      
      | <span data-ttu-id="809be-409">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-409">Type</span></span> | <span data-ttu-id="809be-410">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-410">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-411">Boolesch</span><span class="sxs-lookup"><span data-stu-id="809be-411">Boolean</span></span> | <span data-ttu-id="809be-412">Gibt zurück `true` , wenn Warteschlangen Arbeit auf der angegebenen Prioritätsstufe oder höher vorhanden ist, `false` andernfalls.</span><span class="sxs-lookup"><span data-stu-id="809be-412">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-413">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-413">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-414">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-414">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-415">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-415">Remarks</span></span>**  
      
      <span data-ttu-id="809be-416">Die `isTaskScheduledAtPriorityOrHigher` Methode bietet eine Möglichkeit für JavaScript-Code, um festzustellen, ob die Arbeit auf den verschiedenen Prioritätsebenen \ (oder darüber \) aussteht, mit der Absicht, dass der aufrufende JavaScript-Code dann beschließen kann, der Arbeit mit höherer Priorität nachzugeben.</span><span class="sxs-lookup"><span data-stu-id="809be-416">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-417">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-417">Example</span></span>**  
      
      ```javascript
      function performIdleWork(array_in) {
          var idx = 0;
          
          function performIdleWorkHelper() {
              for (; idx < array_in.length; ++idx) {
                  
                  // USEFUL CODE HERE 
                  
                  if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
                      MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
                      break;
                  } // if
              } // for
          } // performIdleWorkHelper
          
          performIdleWorkHelper();
      } // performIdleWork
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-418">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="809be-418">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-419">Wird verwendet, um eine Aktualisierung des Start Pfads (Seiten neu laden) vor jedem Activate-Ereignis zu vermeiden \ (wie klicken auf eine Benachrichtigung oder auf eine angeheftete Kachel).</span><span class="sxs-lookup"><span data-stu-id="809be-419">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-420">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-420">Parameters</span></span>**  
      
      | <span data-ttu-id="809be-421">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-421">Type</span></span> | <span data-ttu-id="809be-422">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-422">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-423">Boolesch</span><span class="sxs-lookup"><span data-stu-id="809be-423">Boolean</span></span> | <span data-ttu-id="809be-424">Verwenden Sie `MSApp.pageHandlesAllApplicationActivations(true)` diese Option, um die Aktualisierung des startpfads (Seite neu laden) immer zu überspringen und stattdessen direkt zum Auslösen des Activated-Ereignisses zu springen `WebUIApplication` .</span><span class="sxs-lookup"><span data-stu-id="809be-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="809be-425">Erfordert, dass alle Seiten Aktivierungsereignisse separat behandeln.</span><span class="sxs-lookup"><span data-stu-id="809be-425">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="809be-426">Wenn Sie diese Methode definieren `true` , wird beim Klicken auf ein aktiviertes Ereignis \ (wie eine Benachrichtigung \) das erneute Laden nicht ausgelöst, was ein wesentlicher Faktor für einzelne Seiten-Apps ist, die das erneute Laden von Seiten vermeiden möchten.</span><span class="sxs-lookup"><span data-stu-id="809be-426">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-427">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-427">Return value</span></span>**
      
      <span data-ttu-id="809be-428">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-428">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-429">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-429">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-430">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-430">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-431">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-431">Remarks</span></span>**  
      
      <span data-ttu-id="809be-432">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-432">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-433">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-433">Example</span></span>**  
      
      ```javascript
      // Without this, the app will first refresh to the start path before every activate event
      window.MSApp.pageHandlesAllApplicationActivations(true); 
      
      // This must not be deffered so that it can receive the initial `activated` event in time
      window.Windows.UI.WebUI.WebUIApplication.addEventListener(
          `activated`,
          e =>
              microsoftInterface.handleActivatedEvent(e);
          }),
          false
      );
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-434">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="809be-434">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-435">Steuert, ob eine APP während des Downloads von Ressourcen mögliche Authentifizierungs Aufforderungen unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="809be-435">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-436">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-436">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="809be-437">in</span><span class="sxs-lookup"><span data-stu-id="809be-437">[in]</span></span>
      
      | <span data-ttu-id="809be-438">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-438">Type</span></span> | <span data-ttu-id="809be-439">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-439">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-440">Boolesch</span><span class="sxs-lookup"><span data-stu-id="809be-440">Boolean</span></span> | <span data-ttu-id="809be-441">Der Wert true unterdrückt potenzielle Authentifizierungs Aufforderungen.</span><span class="sxs-lookup"><span data-stu-id="809be-441">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="809be-442">Der Wert false unterdrückt keine potenziellen Authentifizierungs Aufforderungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="809be-442">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-443">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-443">Return value</span></span>**  
      
      <span data-ttu-id="809be-444">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-444">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-445">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-445">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-446">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-446">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-447">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-447">Remarks</span></span>**  
      
      <span data-ttu-id="809be-448">Die `suppressSubdownloadCredentialPrompts` Methode steuert, ob eine APP potenzielle Authentifizierungs Aufforderungen während des Downloads von Ressourcen unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="809be-448">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="809be-449">Das Standardverhalten besteht darin, Anmeldeinformationen nicht zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="809be-449">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="809be-450">ist für die Verwendung durch Apps vorgesehen, die möglicherweise eine übermäßige Anzahl von Ressourcen laden, die eine Authentifizierung erfordern, wie etwa eine e-Mail-App \ (die einen Newsletter mit einer Reihe von Bildern enthalten kann, in denen jedes Bild eine Authentifizierung erfordert \).</span><span class="sxs-lookup"><span data-stu-id="809be-450">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="809be-451">Wenn Sie Anmeldeinformationen unterdrücken, werden Dialogfelder für die Authentifizierung bei Servern beim Zugriff auf Ressourcen, die eine Authentifizierung erfordern, nicht angezeigt, und die Ressource wird nicht heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="809be-451">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="809be-452">Beachten Sie, dass dies `suppressSubdownloadCredentialPrompts` keine Auswirkungen auf andere mögliche Eingabeaufforderungen wie Proxyauthentifizierung oder Client Zertifizierungs Anforderungs Dialogfelder hat und sich auch nicht auf XMLHttpRequest auswirkt.</span><span class="sxs-lookup"><span data-stu-id="809be-452">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="809be-453">Beachten Sie, dass `suppressSubdownloadCredentialPrompts` alle Inhalte in der Anwendung, einschließlich der Inhalte, die im Element gehostet werden, beeinträchtigt werden `webview` .</span><span class="sxs-lookup"><span data-stu-id="809be-453">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="809be-454">Entscheidungen für Anmeldeinformationen werden zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="809be-454">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="809be-455">Daher wird die Unterdrückung von Anmeldeinformationen für Anmeldeinformationen sofort wirksam, sodass die Eingabeaufforderung für Anmeldeinformationen nach dem unterdrücken möglicherweise ein erneutes Laden des Dokuments benötigt, damit es wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="809be-455">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-456">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-456">Example</span></span>**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-457">terminateApp</span><span class="sxs-lookup"><span data-stu-id="809be-457">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="809be-458">Beendet die aktuelle Anwendung und generiert einen Fehlerbericht.</span><span class="sxs-lookup"><span data-stu-id="809be-458">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-459">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-459">Parameters</span></span>**  
      
      `error` <span data-ttu-id="809be-460">in</span><span class="sxs-lookup"><span data-stu-id="809be-460">[in]</span></span>
      
      | <span data-ttu-id="809be-461">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-461">Type</span></span> | <span data-ttu-id="809be-462">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-462">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-463">Fehler</span><span class="sxs-lookup"><span data-stu-id="809be-463">Error</span></span> | <span data-ttu-id="809be-464">Ein `Error` Objekt, das Sie verwenden können, um den Fehler zu beschreiben, der die Kündigung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="809be-464">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="809be-465">Das `Error` Objekt muss die Eigenschaften Number, Description und Stack enthalten; es wird kein Fehlerbericht generiert, wenn das Objekt diese Eigenschaften nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="809be-465">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-466">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-466">Return value</span></span>**
      
      <span data-ttu-id="809be-467">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-467">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-468">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="809be-468">Exceptions</span></span>**  
      
      <span data-ttu-id="809be-469">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-469">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-470">Hinweise</span><span class="sxs-lookup"><span data-stu-id="809be-470">Remarks</span></span>**  
      
      <span data-ttu-id="809be-471">Wenn das gemeldete Problem zu `terminateApp` einem der 5 häufigsten Probleme Ihrer APP wird, wird es auf der Qualitätsseite der App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="809be-471">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-472">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-472">Example</span></span>**  
      
      <span data-ttu-id="809be-473">In diesem Beispiel `terminateApp` wird aufgerufen, wenn eine Ausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="809be-473">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="809be-474">Sie verwendet das `Error` Objekt, das beim Abfangen einer Ausnahme bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="809be-474">It uses the `Error` object provided when you catch an exception.</span></span>  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="809be-475">MSApp-Konstanten</span><span class="sxs-lookup"><span data-stu-id="809be-475">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-476">Zulässige Prioritätswerte, die mit `execAsyncAtPriority` , `execAtPriority` , und verknüpft sind `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="809be-476">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="809be-477">Aktuell</span><span class="sxs-lookup"><span data-stu-id="809be-477">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="809be-478">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-478">Type</span></span> | <span data-ttu-id="809be-479">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-479">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-480">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-480">DOMString</span></span> | <span data-ttu-id="809be-481">Bei `current` Verwendung mit der entsprechenden Methode \ (siehe auch Abschnitt \) verwendet die Methode die aktuelle kontextbezogene Priorität, wenn der angeforderte Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="809be-481">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="809be-482">Hoch </span><span class="sxs-lookup"><span data-stu-id="809be-482">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="809be-483">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-483">Type</span></span> | <span data-ttu-id="809be-484">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-484">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-485">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-485">DOMString</span></span> | <span data-ttu-id="809be-486">Wenn `high` mit der entsprechenden Methode \ (siehe auch Abschnitt \) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine höhere Priorität als normal, und die Operation wird vor jeder vorhandenen normalen Priorität ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="809be-486">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="809be-487">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="809be-487">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="809be-488">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-488">Type</span></span> | <span data-ttu-id="809be-489">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-489">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-490">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-490">DOMString</span></span> | <span data-ttu-id="809be-491">Wenn `ideal` mit der entsprechenden Methode \ (siehe auch Abschnitt \) verwendet wird, verwendet die Methode beim Ausführen des angeforderten Vorgangs eine niedrigere Priorität als normal, und die Operation wird nach jeder vorhandenen normalen Priorität ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="809be-491">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="809be-492">Normal</span><span class="sxs-lookup"><span data-stu-id="809be-492">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="809be-493">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-493">Type</span></span> | <span data-ttu-id="809be-494">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-494">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-495">Dom</span><span class="sxs-lookup"><span data-stu-id="809be-495">DOMString</span></span> | <span data-ttu-id="809be-496">Wenn die `normal` Methode mit der entsprechenden Methode verwendet wird (siehe auch Abschnitt), verwendet die Methode beim Ausführen des angeforderten Vorgangs die normale vorhandene Priorität.</span><span class="sxs-lookup"><span data-stu-id="809be-496">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-497">Beispiel</span><span class="sxs-lookup"><span data-stu-id="809be-497">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-498">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="809be-498">Requirements</span></span>**  
      
      | <span data-ttu-id="809be-499">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-499">Type</span></span> | <span data-ttu-id="809be-500">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-500">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-501">IDL</span><span class="sxs-lookup"><span data-stu-id="809be-501">IDL</span></span> | <span data-ttu-id="809be-502">MSHTML. idl</span><span class="sxs-lookup"><span data-stu-id="809be-502">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="809be-503">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="809be-503">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <span data-ttu-id="809be-504">start</span><span class="sxs-lookup"><span data-stu-id="809be-504">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="809be-505">Startet das `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="809be-505">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="809be-506">Parameter</span><span class="sxs-lookup"><span data-stu-id="809be-506">Parameters</span></span>**  
      
      <span data-ttu-id="809be-507">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-507">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="809be-508">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="809be-508">Return value</span></span>**
      
      <span data-ttu-id="809be-509">Keine</span><span class="sxs-lookup"><span data-stu-id="809be-509">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="809be-510">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="809be-510">Properties</span></span>**  
      
      `error` <span data-ttu-id="809be-511">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="809be-511">property</span></span>  
      
      | <span data-ttu-id="809be-512">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-512">Type</span></span> | <span data-ttu-id="809be-513">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-513">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-514">DOMError</span><span class="sxs-lookup"><span data-stu-id="809be-514">DOMError</span></span> | <span data-ttu-id="809be-515">Stellt einen Fehler in dar `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="809be-515">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="809be-516">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="809be-516">property</span></span>  
      
      | <span data-ttu-id="809be-517">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-517">Type</span></span> | <span data-ttu-id="809be-518">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-518">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-519">EventHandler</span><span class="sxs-lookup"><span data-stu-id="809be-519">EventHandler</span></span> | <span data-ttu-id="809be-520">Eigenschaft zum Festlegen eines Ereignishandlers nach Abschluss von `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="809be-520">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="809be-521">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="809be-521">property</span></span>  
      
      | <span data-ttu-id="809be-522">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-522">Type</span></span> | <span data-ttu-id="809be-523">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-523">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-524">EventHandler</span><span class="sxs-lookup"><span data-stu-id="809be-524">EventHandler</span></span> | <span data-ttu-id="809be-525">Eigenschaft zum Festlegen eines Ereignishandlers bei einem Fehler `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="809be-525">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="809be-526">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="809be-526">property</span></span>  
      
      | <span data-ttu-id="809be-527">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-527">Type</span></span> | <span data-ttu-id="809be-528">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-528">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-529">Zahl</span><span class="sxs-lookup"><span data-stu-id="809be-529">Number</span></span> | <span data-ttu-id="809be-530">Stellt den Zustand des asynchronen Vorgangs in der Windows-App mit JavaScript dar.</span><span class="sxs-lookup"><span data-stu-id="809be-530">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="809be-531">Zu den Werten gehören: `Started[0]` , `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="809be-531">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="809be-532">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="809be-532">property</span></span>  
      
      | <span data-ttu-id="809be-533">Typ</span><span class="sxs-lookup"><span data-stu-id="809be-533">Type</span></span> | <span data-ttu-id="809be-534">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="809be-534">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="809be-535">Any</span><span class="sxs-lookup"><span data-stu-id="809be-535">Any</span></span> |<span data-ttu-id="809be-536">Stellt das Ergebnis von dar `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="809be-536">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
