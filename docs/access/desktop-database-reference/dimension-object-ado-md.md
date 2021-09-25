---
title: Dimension, objet (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1390d169af300a382a1cfe7705bc30e0f0a6da6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585752"
---
# <a name="dimension-object-ado-md"></a>Dimension, objet (ADO MD)


**S’applique à** : Access 2013, Office 2013

Représente une des dimensions d’un cube multidimensionnel, contenant une ou plusieurs hiérarchies de membres.

## <a name="remarks"></a>Remarques

Avec les collections et propriétés d'un objet **Dimension**, vous pouvez :

  - Identifier la **dimension** à l'aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).

  - Renvoyer une chaîne significative qui décrit la **dimension** à l'aide de la propriété [Description](description-property-ado-md.md).

  - Renvoyer les objets [Hierarchy](hierarchy-object-ado-md.md) qui constituent la **dimension** à l'aide de la collection [Hierarchies](hierarchies-collection-ado-md.md).

  - Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l'objet **Dimension**.

La collection **Properties** renferme les propriétés fournies par le fournisseur. Le tableau suivant dresse la liste des propriétés potentiellement disponibles. La liste réelle des propriétés peut varier en fonction de la mise en œuvre du fournisseur. Reportez-vous à la documentation de votre fournisseur pour une liste plus complète des propriétés disponibles.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CatalogName</p></td>
<td><p>Le nom du catalogue auquel ce cube appartient.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>Le nom du cube.</p></td>
</tr>
<tr class="odd">
<td><p>DefaultHierarchy</p></td>
<td><p>Le nom unique de la hiérarchie par défaut.</p></td>
</tr>
<tr class="even">
<td><p>Description</p></td>
<td><p>Une description significative du cube.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionCaption</p></td>
<td><p>Une étiquette ou une légende associée à la dimension.</p></td>
</tr>
<tr class="even">
<td><p>DimensionCardinality</p></td>
<td><p>Le nombre de membres de la dimension.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionGUID</p></td>
<td><p>Le GUID de la dimension.</p></td>
</tr>
<tr class="even">
<td><p>DimensionName</p></td>
<td><p>Le nom de la dimension.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionOrdinal</p></td>
<td><p>Le numéro ordinal de la dimension parmi le groupe de dimensions constituant le cube.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Le type de dimension.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Le nom non ambigu de la dimension.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Le nom du schéma auquel ce cube appartient.</p></td>
</tr>
</tbody>
</table>

