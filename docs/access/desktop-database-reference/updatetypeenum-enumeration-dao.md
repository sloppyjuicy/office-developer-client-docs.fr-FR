---
title: UpdateTypeEnum Enumeration (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd2ef7888f511b3f1577ec5fe60ef0ef7dda614a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873445"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="a542d-102">UpdateTypeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="a542d-102">UpdateTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="a542d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a542d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a542d-104">Cette énumération est utilisée avec la méthode **Update** pour spécifier les mises à jour à écrire sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a542d-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a542d-105">Nom</span><span class="sxs-lookup"><span data-stu-id="a542d-105">Name</span></span></p></th>
<th><p><span data-ttu-id="a542d-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a542d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a542d-107">Description</span><span class="sxs-lookup"><span data-stu-id="a542d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a542d-108">dbUpdateBatch ne</span><span class="sxs-lookup"><span data-stu-id="a542d-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="a542d-109">4</span><span class="sxs-lookup"><span data-stu-id="a542d-109">4</span></span></p></td>
<td><p><span data-ttu-id="a542d-110">Toutes les modifications en attente dans le cache de mise à jour sont écrites sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a542d-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a542d-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="a542d-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="a542d-112">2</span><span class="sxs-lookup"><span data-stu-id="a542d-112">2</span></span></p></td>
<td><p><span data-ttu-id="a542d-113">Seules les modifications en attente de l'enregistrement actif sont écrites sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a542d-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a542d-114">valeurs de dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="a542d-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="a542d-115">1</span><span class="sxs-lookup"><span data-stu-id="a542d-115">1</span></span></p></td>
<td><p><span data-ttu-id="a542d-116">(Valeur par défaut) Les modifications en attente ne sont pas mises en cache. Elles sont écrites immédiatement sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a542d-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

