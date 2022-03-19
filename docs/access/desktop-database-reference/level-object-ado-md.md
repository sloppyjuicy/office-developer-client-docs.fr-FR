---
title: Level, objet (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4ee7a93ffc1b5c93e508d70caa506cb920dbe168
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634190"
---
# <a name="level-object-ado-md"></a>Level, objet (ADO MD)


**S’applique à** : Access 2013, Office 2013

Contient un ensemble de membres, chacun occupant le même rang dans une hiérarchie.

## <a name="remarks"></a>Remarques

Avec les collections et propriétés d'un objet **Level**, vous pouvez :

  - Identifier le **niveau** à l’aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).

  - Renvoyer une chaîne à utiliser lors de l’affichage du **niveau** à l’aide de la propriété [Caption](caption-property-ado-md.md).

  - Renvoyer une chaîne significative qui décrit le **niveau** à l’aide de la propriété [Description](description-property-ado-md.md).

  - Renvoyer les objets [Member](member-object-ado-md.md) qui constituent le **niveau** à l’aide de la collection [Members](members-collection-ado-md.md).

  - Renvoyer le nombre de niveaux à partir de la racine du **niveau** à l’aide de la propriété [Depth](depth-property-ado-md.md).

  - Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l’objet **Level**.

La collection **Properties** renferme les propriétés fournies par le fournisseur. Le tableau suivant dresse la liste des propriétés potentiellement disponibles. La liste réelle des propriétés peut varier en fonction de la mise en œuvre du fournisseur. Reportez-vous à la documentation de votre fournisseur pour une liste plus complète des propriétés disponibles.

<table>
<colgroup>
<col />
<col />
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
<td><p>Description</p></td>
<td><p>Une description significative du niveau.</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p>Le nom non ambigu de la <a href="dimension-object-ado-md.md">dimension</a>.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyUniqueName</p></td>
<td><p>Le nom non ambigu de la hiérarchie.</p></td>
</tr>
<tr class="even">
<td><p>LevelCaption</p></td>
<td><p>Une étiquette ou une légende associée au niveau.</p></td>
</tr>
<tr class="odd">
<td><p>LevelCardinality</p></td>
<td><p>Le nombre de membres du niveau.</p></td>
</tr>
<tr class="even">
<td><p>LevelGUID</p></td>
<td><p>Le GUID du niveau.</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>Le nom du niveau.</p></td>
</tr>
<tr class="even">
<td><p>LevelNumber</p></td>
<td><p>La distance entre le niveau et la racine de la hiérarchie.</p></td>
</tr>
<tr class="odd">
<td><p>LevelType</p></td>
<td><p>Le type de niveau.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Le nom non ambigu du niveau.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Le nom du schéma auquel ce cube appartient.</p></td>
</tr>
</tbody>
</table>

