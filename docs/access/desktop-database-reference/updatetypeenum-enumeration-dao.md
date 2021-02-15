---
title: UpdateTypeEnum, éumération (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d1e4ecbc216ab4a00dabd85f623bc134772dfd4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306187"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="8a078-102">UpdateTypeEnum, éumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="8a078-102">UpdateTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="8a078-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a078-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a078-104">Cette énumération est utilisée avec la méthode **Update** pour spécifier les mises à jour à écrire sur le disque.</span><span class="sxs-lookup"><span data-stu-id="8a078-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a078-105">Nom</span><span class="sxs-lookup"><span data-stu-id="8a078-105">Name</span></span></p></th>
<th><p><span data-ttu-id="8a078-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a078-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8a078-107">Description</span><span class="sxs-lookup"><span data-stu-id="8a078-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a078-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="8a078-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="8a078-109">4 </span><span class="sxs-lookup"><span data-stu-id="8a078-109">4</span></span></p></td>
<td><p><span data-ttu-id="8a078-110">Toutes les modifications en attente dans le cache de mise à jour sont écrites sur le disque.</span><span class="sxs-lookup"><span data-stu-id="8a078-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a078-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="8a078-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="8a078-112">2 </span><span class="sxs-lookup"><span data-stu-id="8a078-112">2</span></span></p></td>
<td><p><span data-ttu-id="8a078-113">Seules les modifications en attente de l'enregistrement actif sont écrites sur le disque.</span><span class="sxs-lookup"><span data-stu-id="8a078-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a078-114">dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="8a078-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="8a078-115">1 </span><span class="sxs-lookup"><span data-stu-id="8a078-115">1</span></span></p></td>
<td><p><span data-ttu-id="8a078-116">(Valeur par défaut) Les modifications en attente ne sont pas mises en cache. Elles sont écrites immédiatement sur le disque.</span><span class="sxs-lookup"><span data-stu-id="8a078-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

