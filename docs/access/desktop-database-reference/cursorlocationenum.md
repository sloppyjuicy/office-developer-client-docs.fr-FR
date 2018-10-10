---
title: CursorLocationEnum (référence de base de données du bureau Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470451"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="f2789-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="f2789-102">CursorLocationEnum</span></span>


<span data-ttu-id="f2789-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2789-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f2789-104">Spécifie l'emplacement du service de curseur.</span><span class="sxs-lookup"><span data-stu-id="f2789-104">Specifies the location of the cursor service.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2789-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f2789-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f2789-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2789-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f2789-107">Description</span><span class="sxs-lookup"><span data-stu-id="f2789-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2789-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="f2789-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="f2789-109">3</span><span class="sxs-lookup"><span data-stu-id="f2789-109">3</span></span></p></td>
<td><p><span data-ttu-id="f2789-110">Utilise les curseurs côté client fournis par une bibliothèque de curseurs local.</span><span class="sxs-lookup"><span data-stu-id="f2789-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="f2789-111">Services de curseur locaux souvent permettra de nombreuses fonctionnalités qui pilote curseurs ne peuvent pas, afin que ce paramètre peut fournir un avantage en ce qui concerne les fonctionnalités que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="f2789-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="f2789-112">Pour assurer la compatibilité descendante, le synonyme <strong>adUseClientBatch</strong> est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f2789-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2789-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="f2789-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="f2789-114">1</span><span class="sxs-lookup"><span data-stu-id="f2789-114">1</span></span></p></td>
<td><p><span data-ttu-id="f2789-p102">N'utilise pas les services de curseur. (Cette constante est obsolète et n'est présente qu'à des fins de compatibilité ascendante.)</span><span class="sxs-lookup"><span data-stu-id="f2789-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2789-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="f2789-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="f2789-118">2</span><span class="sxs-lookup"><span data-stu-id="f2789-118">2</span></span></p></td>
<td><p><span data-ttu-id="f2789-p103">Par défaut. Utilise des curseurs de type données ou pilote. Ces curseurs sont parfois très souples et acceptent plus facilement les modifications apportées aux données sources. Toutefois, certaines fonctions du <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (comme les objets <a href="recordset-object-ado.md">Recordset</a> dissocciés) ne peuvent être simulés avec les curseurs de type serveur ; ces fonctions seront indisponibles avec ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2789-p103">Default. Uses data-provider or driver-supplied cursors. These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source. However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2789-123">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="f2789-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="f2789-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f2789-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2789-125">Constante</span><span class="sxs-lookup"><span data-stu-id="f2789-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2789-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="f2789-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2789-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="f2789-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2789-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="f2789-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

