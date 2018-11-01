---
title: RelationAttributeEnum Enumeration (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdb1af980d272f24c5803af9cfba0140dba8b05e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874602"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="28d42-102">RelationAttributeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="28d42-102">RelationAttributeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="28d42-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28d42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28d42-104">Cette énumération est utilisée avec la propriété **Attributes** (Attributs) pour déterminer les attributs d'un objet **Relation**.</span><span class="sxs-lookup"><span data-stu-id="28d42-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28d42-105">Nom</span><span class="sxs-lookup"><span data-stu-id="28d42-105">Name</span></span></p></th>
<th><p><span data-ttu-id="28d42-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="28d42-106">Value</span></span></p></th>
<th><p><span data-ttu-id="28d42-107">Description</span><span class="sxs-lookup"><span data-stu-id="28d42-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28d42-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="28d42-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="28d42-109">4096</span><span class="sxs-lookup"><span data-stu-id="28d42-109">4096</span></span></p></td>
<td><p><span data-ttu-id="28d42-110">Suppressions en cascade</span><span class="sxs-lookup"><span data-stu-id="28d42-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d42-111">valeur dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="28d42-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="28d42-112">2</span><span class="sxs-lookup"><span data-stu-id="28d42-112">2</span></span></p></td>
<td><p><span data-ttu-id="28d42-113">Relation non appliquée (aucune intégrité référentielle)</span><span class="sxs-lookup"><span data-stu-id="28d42-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d42-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="28d42-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="28d42-115">4</span><span class="sxs-lookup"><span data-stu-id="28d42-115">4</span></span></p></td>
<td><p><span data-ttu-id="28d42-116">Une relation existe dans la base de données qui contient les deux tables attachées</span><span class="sxs-lookup"><span data-stu-id="28d42-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d42-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="28d42-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="28d42-118">16777216</span><span class="sxs-lookup"><span data-stu-id="28d42-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="28d42-p101">Microsoft Access uniquement. En mode Création, affiche une JOINTURE GAUCHE en tant que type de jointure par défaut.</span><span class="sxs-lookup"><span data-stu-id="28d42-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d42-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="28d42-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="28d42-122">33554432</span><span class="sxs-lookup"><span data-stu-id="28d42-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="28d42-p102">Microsoft Access uniquement. En mode Création, affiche une JOINTURE DROITE en tant que type de jointure par défaut.</span><span class="sxs-lookup"><span data-stu-id="28d42-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d42-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="28d42-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="28d42-126">1</span><span class="sxs-lookup"><span data-stu-id="28d42-126">1</span></span></p></td>
<td><p><span data-ttu-id="28d42-127">Relation un-à-un</span><span class="sxs-lookup"><span data-stu-id="28d42-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d42-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="28d42-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="28d42-129">256</span><span class="sxs-lookup"><span data-stu-id="28d42-129">256</span></span></p></td>
<td><p><span data-ttu-id="28d42-130">Mises à jour en cascade</span><span class="sxs-lookup"><span data-stu-id="28d42-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

