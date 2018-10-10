---
title: ObjectStateEnum (référence de base de données du bureau Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a08713e5363cb023021e2dd5acb6b38431a6b5e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472420"
---
# <a name="objectstateenum"></a><span data-ttu-id="e1f37-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="e1f37-102">ObjectStateEnum</span></span>


<span data-ttu-id="e1f37-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1f37-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e1f37-104">Spécifie l'état d'un objet : ouvert ou fermé, en cours de connexion à une source de données, d'exécution d'une commande ou d'extraction de données.</span><span class="sxs-lookup"><span data-stu-id="e1f37-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1f37-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e1f37-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e1f37-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1f37-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e1f37-107">Description</span><span class="sxs-lookup"><span data-stu-id="e1f37-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1f37-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="e1f37-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="e1f37-109">0</span><span class="sxs-lookup"><span data-stu-id="e1f37-109">0</span></span></p></td>
<td><p><span data-ttu-id="e1f37-110">Indique que l'objet est fermé.</span><span class="sxs-lookup"><span data-stu-id="e1f37-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1f37-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="e1f37-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="e1f37-112">1</span><span class="sxs-lookup"><span data-stu-id="e1f37-112">1</span></span></p></td>
<td><p><span data-ttu-id="e1f37-113">Indique que l'objet est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e1f37-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1f37-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="e1f37-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="e1f37-115">2</span><span class="sxs-lookup"><span data-stu-id="e1f37-115">2</span></span></p></td>
<td><p><span data-ttu-id="e1f37-116">Indique que l'objet est en train de se connecter.</span><span class="sxs-lookup"><span data-stu-id="e1f37-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1f37-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="e1f37-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="e1f37-118">4</span><span class="sxs-lookup"><span data-stu-id="e1f37-118">4</span></span></p></td>
<td><p><span data-ttu-id="e1f37-119">Indique que l'objet est en train d'exécuter une commande.</span><span class="sxs-lookup"><span data-stu-id="e1f37-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1f37-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="e1f37-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="e1f37-121">8</span><span class="sxs-lookup"><span data-stu-id="e1f37-121">8</span></span></p></td>
<td><p><span data-ttu-id="e1f37-122">Indique que les lignes de l'objet sont en cours d'extraction.</span><span class="sxs-lookup"><span data-stu-id="e1f37-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1f37-123">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="e1f37-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="e1f37-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e1f37-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1f37-125">Constante</span><span class="sxs-lookup"><span data-stu-id="e1f37-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1f37-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="e1f37-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1f37-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="e1f37-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1f37-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="e1f37-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1f37-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="e1f37-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1f37-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="e1f37-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

