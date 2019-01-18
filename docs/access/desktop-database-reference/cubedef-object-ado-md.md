---
title: CubeDef, objet (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c82c95a430da76694fe26300e877e86f86a2eb4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719903"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="94bf0-102">CubeDef, objet (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="94bf0-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="94bf0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94bf0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94bf0-104">Représente un cube issu d'un schéma multidimensionnel, contenant un ensemble de dimensions connexes.</span><span class="sxs-lookup"><span data-stu-id="94bf0-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="94bf0-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="94bf0-105">Remarks</span></span>

<span data-ttu-id="94bf0-106">Avec les collections et propriétés d'un objet **CubeDef**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="94bf0-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="94bf0-107">Identifier un **CubeDef** à l'aide de la propriété [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="94bf0-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="94bf0-108">Renvoyer une chaîne décrivant le cube à l'aide de la propriété [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="94bf0-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="94bf0-109">Renvoyer les dimensions constituant le cube à l'aide de la collection [Dimensions](dimensions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="94bf0-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="94bf0-110">Obtenir des informations supplémentaires relatives au **CubeDef** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="94bf0-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="94bf0-p101">La collection **Properties** renferme les propriétés fournies par le fournisseur. Le tableau suivant dresse la liste des propriétés potentiellement disponibles. La liste réelle des propriétés peut varier en fonction de la mise en œuvre du fournisseur. Reportez-vous à la documentation de votre fournisseur pour une liste plus complète des propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="94bf0-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94bf0-115">Nom</span><span class="sxs-lookup"><span data-stu-id="94bf0-115">Name</span></span></p></th>
<th><p><span data-ttu-id="94bf0-116">Description</span><span class="sxs-lookup"><span data-stu-id="94bf0-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94bf0-117">Nom de catalogue</span><span class="sxs-lookup"><span data-stu-id="94bf0-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="94bf0-118">Le nom du catalogue auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="94bf0-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94bf0-119">Créé</span><span class="sxs-lookup"><span data-stu-id="94bf0-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="94bf0-120">Date et heure de création du cube.</span><span class="sxs-lookup"><span data-stu-id="94bf0-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94bf0-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="94bf0-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="94bf0-122">GUID du cube.</span><span class="sxs-lookup"><span data-stu-id="94bf0-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94bf0-123">Nom du cube</span><span class="sxs-lookup"><span data-stu-id="94bf0-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="94bf0-124">Le nom du cube.</span><span class="sxs-lookup"><span data-stu-id="94bf0-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94bf0-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="94bf0-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="94bf0-126">Le type du cube.</span><span class="sxs-lookup"><span data-stu-id="94bf0-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94bf0-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="94bf0-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="94bf0-128">ID d'utilisateur de la personne à l'origine de la dernière mise à jour des données.</span><span class="sxs-lookup"><span data-stu-id="94bf0-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94bf0-129">Description</span><span class="sxs-lookup"><span data-stu-id="94bf0-129">Description</span></span></p></td>
<td><p><span data-ttu-id="94bf0-130">Une description significative du cube.</span><span class="sxs-lookup"><span data-stu-id="94bf0-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94bf0-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="94bf0-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="94bf0-132">Date et heure de la dernière mise à jour du schéma.</span><span class="sxs-lookup"><span data-stu-id="94bf0-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94bf0-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="94bf0-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="94bf0-134">Le nom du schéma auquel ce cube appartient.</span><span class="sxs-lookup"><span data-stu-id="94bf0-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94bf0-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="94bf0-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="94bf0-136">ID d'utilisateur de la personne à l'origine de la dernière mise à jour du schéma.</span><span class="sxs-lookup"><span data-stu-id="94bf0-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

