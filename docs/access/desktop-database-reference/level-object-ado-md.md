---
title: Level, objet (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290113"
---
# <a name="level-object-ado-md"></a><span data-ttu-id="f1b5c-102">Level, objet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f1b5c-102">Level object (ADO MD)</span></span>


<span data-ttu-id="f1b5c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1b5c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1b5c-104">Contient un ensemble de membres, chacun occupant le même rang dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b5c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1b5c-105">Remarks</span></span>

<span data-ttu-id="f1b5c-106">Avec les collections et propriétés d'un objet **Level**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f1b5c-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="f1b5c-107">Identifier le **niveau** à l’aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f1b5c-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="f1b5c-108">Renvoyer une chaîne à utiliser lors de l’affichage du **niveau** à l’aide de la propriété [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f1b5c-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="f1b5c-109">Renvoyer une chaîne significative qui décrit le **niveau** à l’aide de la propriété [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f1b5c-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="f1b5c-110">Renvoyer les objets [Member](member-object-ado-md.md) qui constituent le **niveau** à l’aide de la collection [Members](members-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f1b5c-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="f1b5c-111">Renvoyer le nombre de niveaux à partir de la racine du **niveau** à l’aide de la propriété [Depth](depth-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f1b5c-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="f1b5c-112">Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l’objet **Level**.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="f1b5c-p101">La collection **Properties** renferme les propriétés fournies par le fournisseur. Le tableau suivant dresse la liste des propriétés potentiellement disponibles. La liste réelle des propriétés peut varier en fonction de la mise en œuvre du fournisseur. Reportez-vous à la documentation de votre fournisseur pour une liste plus complète des propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1b5c-117">Nom</span><span class="sxs-lookup"><span data-stu-id="f1b5c-117">Name</span></span></p></th>
<th><p><span data-ttu-id="f1b5c-118">Description</span><span class="sxs-lookup"><span data-stu-id="f1b5c-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1b5c-119">Nomcatalogue</span><span class="sxs-lookup"><span data-stu-id="f1b5c-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-120">Le nom du catalogue auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b5c-121">CubeName</span><span class="sxs-lookup"><span data-stu-id="f1b5c-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-122">Le nom du cube.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b5c-123">Description</span><span class="sxs-lookup"><span data-stu-id="f1b5c-123">Description</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-124">Une description significative du niveau.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b5c-125">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="f1b5c-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-126">Le nom non ambigu de la <a href="dimension-object-ado-md.md">dimension</a>.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b5c-127">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="f1b5c-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-128">Le nom non ambigu de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b5c-129">LevelCaption</span><span class="sxs-lookup"><span data-stu-id="f1b5c-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-130">Une étiquette ou une légende associée au niveau.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b5c-131">LevelCardinality</span><span class="sxs-lookup"><span data-stu-id="f1b5c-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-132">Le nombre de membres du niveau.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b5c-133">LevelGUID</span><span class="sxs-lookup"><span data-stu-id="f1b5c-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-134">Le GUID du niveau.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b5c-135">LevelName,</span><span class="sxs-lookup"><span data-stu-id="f1b5c-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-136">Le nom du niveau.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b5c-137">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="f1b5c-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-138">La distance entre le niveau et la racine de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b5c-139">LevelType</span><span class="sxs-lookup"><span data-stu-id="f1b5c-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-140">Le type de niveau.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1b5c-141">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="f1b5c-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-142">Le nom non ambigu du niveau.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1b5c-143">SchemaName</span><span class="sxs-lookup"><span data-stu-id="f1b5c-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="f1b5c-144">Le nom du schéma auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="f1b5c-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

