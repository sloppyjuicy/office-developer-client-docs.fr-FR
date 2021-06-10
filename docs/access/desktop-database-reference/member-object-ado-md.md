---
title: Objet Member (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289421"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="fb8e7-102">Objet Member (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="fb8e7-102">Member object (ADO MD)</span></span>


<span data-ttu-id="fb8e7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb8e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb8e7-104">Représente un membre d'un niveau dans un cube, l'enfant d'un membre d'un niveau ou un membre d'une position le long d'un axe d'un ensemble de cellules.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb8e7-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb8e7-105">Remarks</span></span>

<span data-ttu-id="fb8e7-p101">Les propriétés d’un **membre** dépendent du contexte dans lequel il est utilisé. Un **membre** d’un [niveau](level-object-ado-md.md) dans un [CubeDef](cubedef-object-ado-md.md) a la propriété [Children](children-property-ado-md.md) qui renvoie les **membres** du niveau inférieur suivant dans la hiérarchie du **membre** actif. Pour un **membre** d’une [position](position-object-ado-md.md), la collection **Children** est toujours vide. Par ailleurs, la propriété [Type](type-property-ado-md.md) s’applique uniquement aux **membres** d’un **niveau**.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-p101">The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="fb8e7-p102">Un **membre** d'une **position** a deux propriétés : [DrilledDown](drilleddown-property-ado-md.md) et [ParentSameAsPrev](parentsameasprev-property-ado-md.md), qui permettent d'afficher l'[ensemble de cellules](cellset-object-ado-md.md). Une erreur survient si vous accédez à ces propriétés sur un **membre** d'un **niveau**.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-p102">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="fb8e7-112">Avec les collections et propriétés d'un objet **Member** d'un **niveau**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="fb8e7-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="fb8e7-113">Identifier le **membre** à l’aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fb8e7-114">Renvoyer une chaîne à utiliser lors de l’affichage du **membre** à l’aide de la propriété [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fb8e7-115">Renvoyer une chaîne significative décrivant le **membre** d’une mesure ou d’une formule à l’aide de la propriété [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fb8e7-116">Déterminer la nature du **membre** à l’aide de la propriété [Type](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fb8e7-117">Obtenir des informations relatives au **niveau** du **membre** à l’aide des propriétés [LevelDepth](leveldepth-property-ado-md.md) et [LevelName](levelname-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fb8e7-118">Obtenir les **membres** connexes d’une [hiérarchie](hierarchy-object-ado-md.md) à l’aide des propriétés [Parent](parent-property-ado-md.md) et [Children](children-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fb8e7-119">Comptabiliser les enfants d’un **membre** à l’aide de la propriété [ChildCount](childcount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fb8e7-120">Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l’objet **Level**.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="fb8e7-121">Avec les collections et propriétés d’un **membre** d’une **position** le long d’un [axe](axis-object-ado-md.md), vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="fb8e7-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="fb8e7-122">Identifier le **membre** à l’aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fb8e7-123">Renvoyer une chaîne à utiliser lors de l’affichage du **membre** à l’aide de la propriété [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fb8e7-124">Renvoyer une chaîne significative décrivant le **membre** d’une mesure ou d’une formule à l’aide de la propriété [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fb8e7-125">Obtenir des informations relatives au **niveau** du **membre** à l’aide des propriétés [LevelDepth](leveldepth-property-ado-md.md) et [LevelName](levelname-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fb8e7-126">Comptabiliser les enfants d’un **membre** à l’aide de la propriété [ChildCount](childcount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fb8e7-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fb8e7-127">Utiliser la propriété [DrilledDown](drilleddown-property-ado-md.md) pour déterminer si au moins un enfant sur l’**axe** suit immédiatement ce **membre**.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="fb8e7-128">Utiliser la propriété [ParentSameAsPrev](parentsameasprev-property-ado-md.md) pour déterminer si le parent de ce **membre** est le même que le parent du **membre** précédent.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="fb8e7-129">Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l’objet **Level**.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="fb8e7-p103">La collection **Properties** renferme les propriétés fournies par le fournisseur. Le tableau suivant dresse la liste des propriétés potentiellement disponibles. La liste réelle des propriétés peut varier en fonction de la mise en œuvre du fournisseur. Reportez-vous à la documentation de votre fournisseur pour une liste plus complète des propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-p103">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb8e7-134">Nom</span><span class="sxs-lookup"><span data-stu-id="fb8e7-134">Name</span></span></p></th>
<th><p><span data-ttu-id="fb8e7-135">Description</span><span class="sxs-lookup"><span data-stu-id="fb8e7-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-136">CatalogName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-137">Le nom du catalogue auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="fb8e7-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-139">Le nombre d'enfants de ce membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-140">CubeName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-141">Le nom du cube.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-142">Description</span><span class="sxs-lookup"><span data-stu-id="fb8e7-142">Description</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-143">Une description significative du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-145">Le nom non ambigu de la <a href="dimension-object-ado-md.md">dimension</a>.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-147">Le nom non ambigu de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="fb8e7-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-149">La distance entre le niveau et la racine de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-150">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-151">Le nom non ambigu du niveau.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="fb8e7-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-153">Une étiquette ou une légende associée au membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="fb8e7-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-155">Le GUID du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-156">MemberName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-157">Le nom du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="fb8e7-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-159">Le numéro ordinal du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="fb8e7-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-161">Le type du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-163">Le nom non ambigu du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="fb8e7-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-165">Le nombre de parents de ce membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="fb8e7-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-167">Le numéro de niveau du parent du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb8e7-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-169">Le nom non ambigu du parent du membre.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb8e7-170">SchemaName</span><span class="sxs-lookup"><span data-stu-id="fb8e7-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="fb8e7-171">Le nom du schéma auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="fb8e7-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

