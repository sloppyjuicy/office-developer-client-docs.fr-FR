---
title: EventStatusEnum (référence de base de données du bureau Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f49f584603c25997e1b01b94f23aaf9f5429a9e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469068"
---
# <a name="eventstatusenum"></a><span data-ttu-id="84895-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="84895-102">EventStatusEnum</span></span>


<span data-ttu-id="84895-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="84895-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="84895-104">Spécifie l'état en cours de l'exécution d'un événement.</span><span class="sxs-lookup"><span data-stu-id="84895-104">Specifies the current status of the execution of an event.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84895-105">Constante</span><span class="sxs-lookup"><span data-stu-id="84895-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="84895-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="84895-106">Value</span></span></p></th>
<th><p><span data-ttu-id="84895-107">Description</span><span class="sxs-lookup"><span data-stu-id="84895-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84895-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="84895-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="84895-109">4</span><span class="sxs-lookup"><span data-stu-id="84895-109">4</span></span></p></td>
<td><p><span data-ttu-id="84895-110">Demande l'annulation de l'opération qui a provoqué l'événement.</span><span class="sxs-lookup"><span data-stu-id="84895-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84895-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="84895-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="84895-112">3</span><span class="sxs-lookup"><span data-stu-id="84895-112">3</span></span></p></td>
<td><p><span data-ttu-id="84895-113">Indique que l'opération ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="84895-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84895-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="84895-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="84895-115">2</span><span class="sxs-lookup"><span data-stu-id="84895-115">2</span></span></p></td>
<td><p><span data-ttu-id="84895-116">Indique que l'opération qui a provoqué l'événement a échoué en raison d'une ou plusieurs erreurs.</span><span class="sxs-lookup"><span data-stu-id="84895-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84895-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="84895-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="84895-118">1</span><span class="sxs-lookup"><span data-stu-id="84895-118">1</span></span></p></td>
<td><p><span data-ttu-id="84895-119">Indique que l'opération qui a provoqué l'événement a réussi.</span><span class="sxs-lookup"><span data-stu-id="84895-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84895-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="84895-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="84895-121">5</span><span class="sxs-lookup"><span data-stu-id="84895-121">5</span></span></p></td>
<td><p><span data-ttu-id="84895-122">Empêche l'affichage de nouvelles notifications avant la fin de l'exécution de la méthode de l'événement.</span><span class="sxs-lookup"><span data-stu-id="84895-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84895-123">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="84895-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="84895-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="84895-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84895-125">Constante</span><span class="sxs-lookup"><span data-stu-id="84895-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84895-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="84895-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84895-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="84895-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84895-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="84895-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84895-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="84895-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84895-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="84895-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

