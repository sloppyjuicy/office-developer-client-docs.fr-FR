---
title: ObjectStateEnum (référence de base de données de bureau Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288524"
---
# <a name="objectstateenum"></a><span data-ttu-id="d4631-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="d4631-102">ObjectStateEnum</span></span>

<span data-ttu-id="d4631-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4631-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d4631-104">Spécifie l'état d'un objet : ouvert ou fermé, en cours de connexion à une source de données, d'exécution d'une commande ou d'extraction de données.</span><span class="sxs-lookup"><span data-stu-id="d4631-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4631-105">Constante</span><span class="sxs-lookup"><span data-stu-id="d4631-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d4631-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4631-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d4631-107">Description</span><span class="sxs-lookup"><span data-stu-id="d4631-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4631-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="d4631-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="d4631-109">0</span><span class="sxs-lookup"><span data-stu-id="d4631-109">0</span></span></p></td>
<td><p><span data-ttu-id="d4631-110">Indique que l'objet est fermé.</span><span class="sxs-lookup"><span data-stu-id="d4631-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4631-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="d4631-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="d4631-112">1</span><span class="sxs-lookup"><span data-stu-id="d4631-112">1</span></span></p></td>
<td><p><span data-ttu-id="d4631-113">Indique que l'objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d4631-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4631-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="d4631-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="d4631-115">2</span><span class="sxs-lookup"><span data-stu-id="d4631-115">2</span></span></p></td>
<td><p><span data-ttu-id="d4631-116">Indique que l'objet est en train de se connecter.</span><span class="sxs-lookup"><span data-stu-id="d4631-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4631-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="d4631-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="d4631-118">4 </span><span class="sxs-lookup"><span data-stu-id="d4631-118">4</span></span></p></td>
<td><p><span data-ttu-id="d4631-119">Indique que l'objet est en train d'exécuter une commande.</span><span class="sxs-lookup"><span data-stu-id="d4631-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4631-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="d4631-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="d4631-121">8 </span><span class="sxs-lookup"><span data-stu-id="d4631-121">8</span></span></p></td>
<td><p><span data-ttu-id="d4631-122">Indique que les lignes de l'objet sont en cours d'extraction.</span><span class="sxs-lookup"><span data-stu-id="d4631-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d4631-123">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d4631-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="d4631-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d4631-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4631-125">Constante</span><span class="sxs-lookup"><span data-stu-id="d4631-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4631-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="d4631-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4631-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="d4631-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4631-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="d4631-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4631-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="d4631-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4631-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="d4631-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

