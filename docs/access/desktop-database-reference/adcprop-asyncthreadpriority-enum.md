---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700276"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="1b0af-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span><span class="sxs-lookup"><span data-stu-id="1b0af-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="1b0af-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b0af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b0af-104">Pour un objet [Recordset](recordset-object-ado.md) RDS, spécifie la priorité d'exécution du thème asynchrone qui recherche des données.</span><span class="sxs-lookup"><span data-stu-id="1b0af-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="1b0af-105">Utilisez ces constantes avec la propriété dynamique « **Background Thread Priority** » du **Recordset**, qui est référencée dans l’index des propriétés dynamiques ADO et expliquée dans la documentation [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="1b0af-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b0af-106">Constante</span><span class="sxs-lookup"><span data-stu-id="1b0af-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="1b0af-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b0af-107">Value</span></span></p></th>
<th><p><span data-ttu-id="1b0af-108">Description</span><span class="sxs-lookup"><span data-stu-id="1b0af-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b0af-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="1b0af-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="1b0af-110">4</span><span class="sxs-lookup"><span data-stu-id="1b0af-110">4</span></span></p></td>
<td><p><span data-ttu-id="1b0af-111">Définit le niveau de priorité, normal ou maximum.</span><span class="sxs-lookup"><span data-stu-id="1b0af-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b0af-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="1b0af-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="1b0af-113">2</span><span class="sxs-lookup"><span data-stu-id="1b0af-113">2</span></span></p></td>
<td><p><span data-ttu-id="1b0af-114">Définit le niveau de priorité, minimum ou normal.</span><span class="sxs-lookup"><span data-stu-id="1b0af-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b0af-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="1b0af-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="1b0af-116">5</span><span class="sxs-lookup"><span data-stu-id="1b0af-116">5</span></span></p></td>
<td><p><span data-ttu-id="1b0af-117">Définit le niveau de priorité le plus élevé possible.</span><span class="sxs-lookup"><span data-stu-id="1b0af-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b0af-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="1b0af-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="1b0af-119">1</span><span class="sxs-lookup"><span data-stu-id="1b0af-119">1</span></span></p></td>
<td><p><span data-ttu-id="1b0af-120">Définit le niveau de priorité le plus bas possible.</span><span class="sxs-lookup"><span data-stu-id="1b0af-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b0af-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="1b0af-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="1b0af-122">3</span><span class="sxs-lookup"><span data-stu-id="1b0af-122">3</span></span></p></td>
<td><p><span data-ttu-id="1b0af-123">Définit le niveau de priorité normal.</span><span class="sxs-lookup"><span data-stu-id="1b0af-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="1b0af-124">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="1b0af-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="1b0af-125">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1b0af-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b0af-126">Constante</span><span class="sxs-lookup"><span data-stu-id="1b0af-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b0af-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="1b0af-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b0af-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="1b0af-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b0af-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="1b0af-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b0af-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="1b0af-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b0af-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="1b0af-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

