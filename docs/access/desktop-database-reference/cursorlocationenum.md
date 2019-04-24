---
title: CursorLocationEnum (référence de base de données de bureau Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295211"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="6d991-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="6d991-102">CursorLocationEnum</span></span>

<span data-ttu-id="6d991-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d991-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d991-104">Spécifie l'emplacement du service de curseur.</span><span class="sxs-lookup"><span data-stu-id="6d991-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d991-105">Constante</span><span class="sxs-lookup"><span data-stu-id="6d991-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6d991-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d991-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6d991-107">Description</span><span class="sxs-lookup"><span data-stu-id="6d991-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d991-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="6d991-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="6d991-109">3</span><span class="sxs-lookup"><span data-stu-id="6d991-109">3</span></span></p></td>
<td><p><span data-ttu-id="6d991-110">Utilise des curseurs côté client fournis par une bibliothèque locale de curseurs.</span><span class="sxs-lookup"><span data-stu-id="6d991-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="6d991-111">Les services de curseur locaux disposent de beaucoup plus de fonctions que les curseurs fournis par les pilotes ; ce paramètre peut donc présenter un avantage pour les fonctions activées.</span><span class="sxs-lookup"><span data-stu-id="6d991-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="6d991-112">Pour des questions de compatibilité ascendante, le synonyme <strong>adUseClientBatch</strong> est également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6d991-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d991-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="6d991-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6d991-114">0,1</span><span class="sxs-lookup"><span data-stu-id="6d991-114">1</span></span></p></td>
<td><p><span data-ttu-id="6d991-p102">N'utilise pas les services de curseur. (Cette constante est obsolète et n'est présente qu'à des fins de compatibilité ascendante.)</span><span class="sxs-lookup"><span data-stu-id="6d991-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d991-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="6d991-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6d991-118">n°2</span><span class="sxs-lookup"><span data-stu-id="6d991-118">2</span></span></p></td>
<td><p><span data-ttu-id="6d991-119">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="6d991-119">Default.</span></span> <span data-ttu-id="6d991-120">Utilise des curseurs de type données ou pilote.</span><span class="sxs-lookup"><span data-stu-id="6d991-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="6d991-121">Ces curseurs sont parfois très souples et acceptent plus facilement les modifications apportées aux données sources.</span><span class="sxs-lookup"><span data-stu-id="6d991-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="6d991-122">Toutefois, certaines fonctionnalités du <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">service de curseur Microsoft pour OLE DB</a> (telles que les objets <a href="recordset-object-ado.md">Recordset</a> non associés) ne peuvent pas être simulées avec des curseurs côté serveur, et ces fonctionnalités ne seront pas disponibles avec ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="6d991-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6d991-123">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="6d991-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="6d991-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6d991-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d991-125">Constante</span><span class="sxs-lookup"><span data-stu-id="6d991-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d991-126">AdoEnums. CursorLocation. CLIENT</span><span class="sxs-lookup"><span data-stu-id="6d991-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d991-127">AdoEnums. CursorLocation. NONE</span><span class="sxs-lookup"><span data-stu-id="6d991-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d991-128">AdoEnums. CursorLocation. SERVER</span><span class="sxs-lookup"><span data-stu-id="6d991-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

