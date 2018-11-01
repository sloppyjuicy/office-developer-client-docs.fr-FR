---
title: Dimension, objet (ADO MD)
TOCTitle: Dimension Object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3581f9bce5e2e56b341928df3415a1b9b223beb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872885"
---
# <a name="dimension-object-ado-md"></a>Dimension, objet (ADO MD)


**S’applique à**: Access 2013, Office 2013

Représente une des dimensions d'un cube multidimensionnel, contenant une ou plusieurs hiérarchies de membres.

## <a name="remarks"></a>Remarques

Avec les collections et propriétés d'un objet **Dimension**, vous pouvez :

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
<td><p>Nom de catalogue</p></td>
<td><p>Le nom du catalogue auquel ce cube appartient.</p></td>
</tr>
<tr class="even">
<td><p>Nom du cube</p></td>
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
<td><p>Nomdimension</p></td>
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

