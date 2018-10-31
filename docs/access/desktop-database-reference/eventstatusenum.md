---
title: EventStatusEnum (référence de base de données du bureau Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6e8408e2c73a60ae543bc9982de2f2547f54d1d2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861532"
---
# <a name="eventstatusenum"></a><span data-ttu-id="762d5-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="762d5-102">EventStatusEnum</span></span>

<span data-ttu-id="762d5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="762d5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="762d5-104">Spécifie l'état en cours de l'exécution d'un événement.</span><span class="sxs-lookup"><span data-stu-id="762d5-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="762d5-105">Constante</span><span class="sxs-lookup"><span data-stu-id="762d5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="762d5-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="762d5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="762d5-107">Description</span><span class="sxs-lookup"><span data-stu-id="762d5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="762d5-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="762d5-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="762d5-109">4</span><span class="sxs-lookup"><span data-stu-id="762d5-109">4</span></span></p></td>
<td><p><span data-ttu-id="762d5-110">Demande l'annulation de l'opération qui a provoqué l'événement.</span><span class="sxs-lookup"><span data-stu-id="762d5-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="762d5-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="762d5-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="762d5-112">3</span><span class="sxs-lookup"><span data-stu-id="762d5-112">3</span></span></p></td>
<td><p><span data-ttu-id="762d5-113">Indique que l'opération ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="762d5-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="762d5-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="762d5-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="762d5-115">2</span><span class="sxs-lookup"><span data-stu-id="762d5-115">2</span></span></p></td>
<td><p><span data-ttu-id="762d5-116">Indique que l'opération qui a provoqué l'événement a échoué en raison d'une ou plusieurs erreurs.</span><span class="sxs-lookup"><span data-stu-id="762d5-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="762d5-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="762d5-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="762d5-118">1</span><span class="sxs-lookup"><span data-stu-id="762d5-118">1</span></span></p></td>
<td><p><span data-ttu-id="762d5-119">Indique que l'opération qui a provoqué l'événement a réussi.</span><span class="sxs-lookup"><span data-stu-id="762d5-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="762d5-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="762d5-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="762d5-121">5</span><span class="sxs-lookup"><span data-stu-id="762d5-121">5</span></span></p></td>
<td><p><span data-ttu-id="762d5-122">Empêche l'affichage de nouvelles notifications avant la fin de l'exécution de la méthode de l'événement.</span><span class="sxs-lookup"><span data-stu-id="762d5-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="762d5-123">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="762d5-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="762d5-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="762d5-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="762d5-125">Constante</span><span class="sxs-lookup"><span data-stu-id="762d5-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="762d5-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="762d5-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="762d5-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="762d5-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="762d5-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="762d5-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="762d5-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="762d5-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="762d5-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="762d5-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

