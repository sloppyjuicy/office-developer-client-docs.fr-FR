---
title: CursorLocationEnum (référence de base de données du bureau Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7f8eedd1245be16d87a2d3b2cd2b9121853529c5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863628"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="d9c4e-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="d9c4e-102">CursorLocationEnum</span></span>

<span data-ttu-id="d9c4e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9c4e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9c4e-104">Spécifie l'emplacement du service de curseur.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9c4e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="d9c4e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d9c4e-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9c4e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d9c4e-107">Description</span><span class="sxs-lookup"><span data-stu-id="d9c4e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9c4e-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4e-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4e-109">3</span><span class="sxs-lookup"><span data-stu-id="d9c4e-109">3</span></span></p></td>
<td><p><span data-ttu-id="d9c4e-110">Utilise les curseurs côté client fournis par une bibliothèque de curseurs local.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="d9c4e-111">Services de curseur locaux souvent permettra de nombreuses fonctionnalités qui pilote curseurs ne peuvent pas, afin que ce paramètre peut fournir un avantage en ce qui concerne les fonctionnalités que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="d9c4e-112">Pour assurer la compatibilité descendante, le synonyme <strong>adUseClientBatch</strong> est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9c4e-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4e-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4e-114">1</span><span class="sxs-lookup"><span data-stu-id="d9c4e-114">1</span></span></p></td>
<td><p><span data-ttu-id="d9c4e-p102">N'utilise pas les services de curseur. (Cette constante est obsolète et n'est présente qu'à des fins de compatibilité ascendante.)</span><span class="sxs-lookup"><span data-stu-id="d9c4e-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9c4e-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="d9c4e-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d9c4e-118">2</span><span class="sxs-lookup"><span data-stu-id="d9c4e-118">2</span></span></p></td>
<td><p><span data-ttu-id="d9c4e-119">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-119">Default.</span></span> <span data-ttu-id="d9c4e-120">Utilise les curseurs pilote ou fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="d9c4e-121">Ces curseurs sont parfois très souples et autoriser plus facilement les modifications apportées à la source de données.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="d9c4e-122">Cependant, certaines fonctionnalités du <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Service de curseur Microsoft pour OLE DB</a> (telles que les objets <a href="recordset-object-ado.md">Recordset</a> dissociées) ne peut pas être simuler avec les curseurs côté serveur, et ces fonctionnalités ne seront pas disponibles avec ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="d9c4e-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d9c4e-123">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d9c4e-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="d9c4e-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d9c4e-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d9c4e-125">Constante</span><span class="sxs-lookup"><span data-stu-id="d9c4e-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9c4e-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="d9c4e-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9c4e-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="d9c4e-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9c4e-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="d9c4e-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

