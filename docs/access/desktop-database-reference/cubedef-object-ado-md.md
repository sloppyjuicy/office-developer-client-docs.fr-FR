---
title: CubeDef, objet (ADO MD)
TOCTitle: CubeDef Object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7dc244483c3111e6e354496f1ffbbd12f463800
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878294"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="e4a6e-102">CubeDef, objet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e4a6e-102">CubeDef Object (ADO MD)</span></span>


<span data-ttu-id="e4a6e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4a6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4a6e-104">Représente un cube issu d'un schéma multidimensionnel, contenant un ensemble de dimensions connexes.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a6e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4a6e-105">Remarks</span></span>

<span data-ttu-id="e4a6e-106">Avec les collections et propriétés d'un objet **CubeDef**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e4a6e-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="e4a6e-107">Identifier un **CubeDef** à l'aide de la propriété [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6e-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e4a6e-108">Renvoyer une chaîne décrivant le cube à l'aide de la propriété [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6e-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e4a6e-109">Renvoyer les dimensions constituant le cube à l'aide de la collection [Dimensions](dimensions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6e-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="e4a6e-110">Obtenir des informations supplémentaires relatives au **CubeDef** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6e-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="e4a6e-p101">La collection **Properties** renferme les propriétés fournies par le fournisseur. Le tableau suivant dresse la liste des propriétés potentiellement disponibles. La liste réelle des propriétés peut varier en fonction de la mise en œuvre du fournisseur. Reportez-vous à la documentation de votre fournisseur pour une liste plus complète des propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4a6e-115">Nom</span><span class="sxs-lookup"><span data-stu-id="e4a6e-115">Name</span></span></p></th>
<th><p><span data-ttu-id="e4a6e-116">Description</span><span class="sxs-lookup"><span data-stu-id="e4a6e-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4a6e-117">Nom de catalogue</span><span class="sxs-lookup"><span data-stu-id="e4a6e-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-118">Le nom du catalogue auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a6e-119">Créé</span><span class="sxs-lookup"><span data-stu-id="e4a6e-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-120">Date et heure de création du cube.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a6e-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="e4a6e-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-122">GUID du cube.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a6e-123">Nom du cube</span><span class="sxs-lookup"><span data-stu-id="e4a6e-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-124">Le nom du cube.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a6e-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="e4a6e-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-126">Le type du cube.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a6e-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="e4a6e-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-128">ID d'utilisateur de la personne à l'origine de la dernière mise à jour des données.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a6e-129">Description</span><span class="sxs-lookup"><span data-stu-id="e4a6e-129">Description</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-130">Une description significative du cube.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a6e-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="e4a6e-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-132">Date et heure de la dernière mise à jour du schéma.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4a6e-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="e4a6e-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-134">Le nom du schéma auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4a6e-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="e4a6e-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="e4a6e-136">ID d'utilisateur de la personne à l'origine de la dernière mise à jour du schéma.</span><span class="sxs-lookup"><span data-stu-id="e4a6e-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

