---
title: RelationAttributeEnum, éumération (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbb8ca2e1a63154f17bd814a26fe79ed405765cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306978"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="1eaa9-102">RelationAttributeEnum, éumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="1eaa9-102">RelationAttributeEnum enumeration (DAO)</span></span>


<span data-ttu-id="1eaa9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1eaa9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1eaa9-104">Cette énumération est utilisée avec la propriété **Attributes** (Attributs) pour déterminer les attributs d'un objet **Relation**.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1eaa9-105">Nom</span><span class="sxs-lookup"><span data-stu-id="1eaa9-105">Name</span></span></p></th>
<th><p><span data-ttu-id="1eaa9-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eaa9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1eaa9-107">Description</span><span class="sxs-lookup"><span data-stu-id="1eaa9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1eaa9-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="1eaa9-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-109">4096</span><span class="sxs-lookup"><span data-stu-id="1eaa9-109">4096</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-110">Suppressions en cascade</span><span class="sxs-lookup"><span data-stu-id="1eaa9-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1eaa9-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="1eaa9-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-112">2</span><span class="sxs-lookup"><span data-stu-id="1eaa9-112">2</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-113">Relation non appliquée (aucune intégrité référentielle)</span><span class="sxs-lookup"><span data-stu-id="1eaa9-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1eaa9-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="1eaa9-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-115">4 </span><span class="sxs-lookup"><span data-stu-id="1eaa9-115">4</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-116">Une relation existe dans la base de données qui contient les deux tables attachées</span><span class="sxs-lookup"><span data-stu-id="1eaa9-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1eaa9-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="1eaa9-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-118">16777216</span><span class="sxs-lookup"><span data-stu-id="1eaa9-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-p101">Microsoft Access uniquement. En mode Création, affiche une JOINTURE GAUCHE en tant que type de jointure par défaut.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1eaa9-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="1eaa9-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-122">33554432</span><span class="sxs-lookup"><span data-stu-id="1eaa9-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-p102">Microsoft Access uniquement. En mode Création, affiche une JOINTURE DROITE en tant que type de jointure par défaut.</span><span class="sxs-lookup"><span data-stu-id="1eaa9-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1eaa9-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="1eaa9-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-126">1</span><span class="sxs-lookup"><span data-stu-id="1eaa9-126">1</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-127">Relation un-à-un</span><span class="sxs-lookup"><span data-stu-id="1eaa9-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1eaa9-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="1eaa9-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-129">256</span><span class="sxs-lookup"><span data-stu-id="1eaa9-129">256</span></span></p></td>
<td><p><span data-ttu-id="1eaa9-130">Mises à jour en cascade</span><span class="sxs-lookup"><span data-stu-id="1eaa9-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

