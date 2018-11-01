---
title: Hierarchy, objet (ADO MD)
TOCTitle: Hierarchy Object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad6eb40873d0cd88b441adaa5568ad57dced83c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869784"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="917b4-102">Hierarchy, objet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="917b4-102">Hierarchy Object (ADO MD)</span></span>


<span data-ttu-id="917b4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="917b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="917b4-p101">Représente un moyen d'agréger ou de « cumuler » les membres d'une [dimension](dimension-object-ado-md.md). Vous pouvez agréger une dimension le long d'une ou de plusieurs hiérarchies.</span><span class="sxs-lookup"><span data-stu-id="917b4-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="917b4-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="917b4-106">Remarks</span></span>

<span data-ttu-id="917b4-107">Avec les collections et propriétés d'un objet **Hierarchy**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="917b4-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="917b4-108">Identifier la **hiérarchie** à l'aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="917b4-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="917b4-109">Renvoyer une chaîne significative qui décrit la **hiérarchie** à l'aide de la propriété [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="917b4-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="917b4-110">Renvoyer les objets [Level](level-object-ado-md.md) qui constituent la **hiérarchie** à l'aide de la collection [Levels](levels-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="917b4-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="917b4-111">Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l'objet **Hierarchy**.</span><span class="sxs-lookup"><span data-stu-id="917b4-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="917b4-p102">La collection **Properties** renferme les propriétés fournies par le fournisseur. Le tableau suivant dresse la liste des propriétés potentiellement disponibles. La liste réelle des propriétés peut varier en fonction de la mise en œuvre du fournisseur. Reportez-vous à la documentation de votre fournisseur pour une liste plus complète des propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="917b4-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="917b4-116">Nom</span><span class="sxs-lookup"><span data-stu-id="917b4-116">Name</span></span></p></th>
<th><p><span data-ttu-id="917b4-117">Description</span><span class="sxs-lookup"><span data-stu-id="917b4-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="917b4-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="917b4-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="917b4-119">Le membre au niveau le plus élevé de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917b4-120">Nom de catalogue</span><span class="sxs-lookup"><span data-stu-id="917b4-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="917b4-121">Le nom du catalogue auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="917b4-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917b4-122">Nom du cube</span><span class="sxs-lookup"><span data-stu-id="917b4-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="917b4-123">Le nom du cube.</span><span class="sxs-lookup"><span data-stu-id="917b4-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917b4-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="917b4-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="917b4-125">Le nom unique du membre par défaut de cette hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917b4-126">Description</span><span class="sxs-lookup"><span data-stu-id="917b4-126">Description</span></span></p></td>
<td><p><span data-ttu-id="917b4-127">Une description significative de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917b4-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="917b4-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="917b4-129">Le type de dimension à laquelle cette hiérarchie appartient.</span><span class="sxs-lookup"><span data-stu-id="917b4-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917b4-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="917b4-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="917b4-131">Le nom non ambigu de la dimension.</span><span class="sxs-lookup"><span data-stu-id="917b4-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917b4-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="917b4-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="917b4-133">Une étiquette ou une légende associée à la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917b4-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="917b4-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="917b4-135">Le nombre de membres de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917b4-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="917b4-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="917b4-137">Le GUID de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917b4-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="917b4-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="917b4-139">Le nom de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="917b4-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="917b4-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="917b4-141">Le nom non ambigu de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="917b4-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="917b4-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="917b4-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="917b4-143">Le nom du schéma auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="917b4-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

