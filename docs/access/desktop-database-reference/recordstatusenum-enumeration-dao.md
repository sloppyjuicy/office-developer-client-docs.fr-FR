---
title: RecordStatusEnum Enumeration (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c2d96c359a913660c146f4850a1846554e3b6856
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875118"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="ccbc3-102">RecordStatusEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="ccbc3-102">RecordStatusEnum Enumeration (DAO)</span></span>


<span data-ttu-id="ccbc3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccbc3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ccbc3-104">Cette énumération est utilisée avec la propriété **RecordStatus** pour indiquer l'état de mise à jour de l'enregistrement actif s'il fait partie d'une mise à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="ccbc3-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ccbc3-105">Nom</span><span class="sxs-lookup"><span data-stu-id="ccbc3-105">Name</span></span></p></th>
<th><p><span data-ttu-id="ccbc3-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccbc3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ccbc3-107">Description</span><span class="sxs-lookup"><span data-stu-id="ccbc3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccbc3-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="ccbc3-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-109">4</span><span class="sxs-lookup"><span data-stu-id="ccbc3-109">4</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-110">L'enregistrement a été supprimé localement dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="ccbc3-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccbc3-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="ccbc3-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-112">3</span><span class="sxs-lookup"><span data-stu-id="ccbc3-112">3</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-113">L'enregistrement a été supprimé, mais il n'a pas encore été supprimé de la base de données.</span><span class="sxs-lookup"><span data-stu-id="ccbc3-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccbc3-114">valeur dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="ccbc3-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-115">1</span><span class="sxs-lookup"><span data-stu-id="ccbc3-115">1</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-116">L'enregistrement a été modifié, mais il n'a pas été mis à jour dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="ccbc3-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccbc3-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="ccbc3-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-118">2</span><span class="sxs-lookup"><span data-stu-id="ccbc3-118">2</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-119">L'enregistrement a été ajouté à l'aide de la méthode <strong>AddNew</strong>, mais il n'a pas été encore ajouté à la base de données.</span><span class="sxs-lookup"><span data-stu-id="ccbc3-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccbc3-120">valeur dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="ccbc3-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-121">0</span><span class="sxs-lookup"><span data-stu-id="ccbc3-121">0</span></span></p></td>
<td><p><span data-ttu-id="ccbc3-122">(Valeur par défaut) L'enregistrement n'a pas été modifié ou il a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="ccbc3-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

