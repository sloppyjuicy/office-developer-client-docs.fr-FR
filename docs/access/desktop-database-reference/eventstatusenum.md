---
title: EventStatusEnum (référence de base de données du bureau Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712581"
---
# <a name="eventstatusenum"></a><span data-ttu-id="a757c-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="a757c-102">EventStatusEnum</span></span>

<span data-ttu-id="a757c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a757c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a757c-104">Spécifie l'état en cours de l'exécution d'un événement.</span><span class="sxs-lookup"><span data-stu-id="a757c-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a757c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a757c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a757c-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a757c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a757c-107">Description</span><span class="sxs-lookup"><span data-stu-id="a757c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a757c-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="a757c-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="a757c-109">4</span><span class="sxs-lookup"><span data-stu-id="a757c-109">4</span></span></p></td>
<td><p><span data-ttu-id="a757c-110">Demande l'annulation de l'opération qui a provoqué l'événement.</span><span class="sxs-lookup"><span data-stu-id="a757c-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a757c-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="a757c-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="a757c-112">3</span><span class="sxs-lookup"><span data-stu-id="a757c-112">3</span></span></p></td>
<td><p><span data-ttu-id="a757c-113">Indique que l'opération ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="a757c-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a757c-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="a757c-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="a757c-115">2</span><span class="sxs-lookup"><span data-stu-id="a757c-115">2</span></span></p></td>
<td><p><span data-ttu-id="a757c-116">Indique que l'opération qui a provoqué l'événement a échoué en raison d'une ou plusieurs erreurs.</span><span class="sxs-lookup"><span data-stu-id="a757c-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a757c-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="a757c-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="a757c-118">1</span><span class="sxs-lookup"><span data-stu-id="a757c-118">1</span></span></p></td>
<td><p><span data-ttu-id="a757c-119">Indique que l'opération qui a provoqué l'événement a réussi.</span><span class="sxs-lookup"><span data-stu-id="a757c-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a757c-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="a757c-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="a757c-121">5</span><span class="sxs-lookup"><span data-stu-id="a757c-121">5</span></span></p></td>
<td><p><span data-ttu-id="a757c-122">Empêche l'affichage de nouvelles notifications avant la fin de l'exécution de la méthode de l'événement.</span><span class="sxs-lookup"><span data-stu-id="a757c-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a757c-123">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a757c-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="a757c-124">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a757c-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a757c-125">Constante</span><span class="sxs-lookup"><span data-stu-id="a757c-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a757c-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="a757c-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a757c-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="a757c-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a757c-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="a757c-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a757c-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="a757c-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a757c-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="a757c-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

