---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b1ebc5cf8df4a0eab125f788544dba40ec373d02
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880648"
---
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="85c5d-102">ADCPROP\_UPDATECRITERIA\_ENUM</span><span class="sxs-lookup"><span data-stu-id="85c5d-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="85c5d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85c5d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85c5d-104">Indique les champs qui peuvent être utilisés pour détecter les conflits pendant une mise à jour optimiste d'une ligne de la source de données avec un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="85c5d-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="85c5d-105">Utilisez ces constantes avec la propriété dynamique "**Update Criteria**" du **Recordset**, qui est référencée dans l’[index des propriétés dynamiques ADO](ado-dynamic-property-index.md) et expliquée dans la documentation [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="85c5d-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85c5d-106">Constant</span><span class="sxs-lookup"><span data-stu-id="85c5d-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="85c5d-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="85c5d-107">Value</span></span></p></th>
<th><p><span data-ttu-id="85c5d-108">Description</span><span class="sxs-lookup"><span data-stu-id="85c5d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85c5d-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="85c5d-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="85c5d-110">1</span><span class="sxs-lookup"><span data-stu-id="85c5d-110">1</span></span></p></td>
<td><p><span data-ttu-id="85c5d-111">Détecte des conflits en cas de modification d'une ligne de la source de données.</span><span class="sxs-lookup"><span data-stu-id="85c5d-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c5d-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="85c5d-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="85c5d-113">0</span><span class="sxs-lookup"><span data-stu-id="85c5d-113">0</span></span></p></td>
<td><p><span data-ttu-id="85c5d-114">Détecte des conflits en cas de modification de la colonne de clés de la ligne de source de données, indiquant que la ligne a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="85c5d-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85c5d-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="85c5d-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="85c5d-116">3</span><span class="sxs-lookup"><span data-stu-id="85c5d-116">3</span></span></p></td>
<td><p><span data-ttu-id="85c5d-117">Détecte des conflits si l'horodatage de la ligne de source de données a été modifié, signifiant qu'il y a eu un accès après obtention du <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="85c5d-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c5d-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="85c5d-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="85c5d-119">2</span><span class="sxs-lookup"><span data-stu-id="85c5d-119">2</span></span></p></td>
<td><p><span data-ttu-id="85c5d-120">Détecte des conflits si une des colonnes de la ligne de source de données correspondant aux champs mis à jour du <strong>Recordset</strong> a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="85c5d-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="85c5d-121">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="85c5d-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="85c5d-122">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="85c5d-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85c5d-123">Constante</span><span class="sxs-lookup"><span data-stu-id="85c5d-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85c5d-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span><span class="sxs-lookup"><span data-stu-id="85c5d-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c5d-125">AdoEnums.AdcPropUpdateCriteria.KEY</span><span class="sxs-lookup"><span data-stu-id="85c5d-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85c5d-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="85c5d-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c5d-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="85c5d-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

