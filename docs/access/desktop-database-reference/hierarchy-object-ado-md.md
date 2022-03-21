---
title: Hierarchy, objet (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dbe185e17309365ce5df74d955c690776e5336cf
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630636"
---
# <a name="hierarchy-object-ado-md"></a>Hierarchy, objet (ADO MD)


**S’applique à** : Access 2013, Office 2013

Représente un moyen d'agréger ou de « cumuler » les membres d'une [dimension](dimension-object-ado-md.md). Vous pouvez agréger une dimension le long d'une ou de plusieurs hiérarchies.

## <a name="remarks"></a>Remarques

Avec les collections et propriétés d'un objet **Hierarchy**, vous pouvez :

  - Identifier la **hiérarchie** à l'aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).

  - Renvoyer une chaîne significative qui décrit la **hiérarchie** à l'aide de la propriété [Description](description-property-ado-md.md).

  - Renvoyer les objets [Level](level-object-ado-md.md) qui constituent la **hiérarchie** à l'aide de la collection [Levels](levels-collection-ado-md.md).

  - Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l'objet **Hierarchy**.

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
<td><p>AllMember</p></td>
<td><p>Le membre au niveau le plus élevé de la hiérarchie.</p></td>
</tr>
<tr class="even">
<td><p>CatalogName</p></td>
<td><p>Le nom du catalogue auquel ce cube appartient.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Le nom du cube.</p></td>
</tr>
<tr class="even">
<td><p>DefaultMember</p></td>
<td><p>Le nom unique du membre par défaut de cette hiérarchie.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Une description significative de la hiérarchie.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Le type de dimension à laquelle cette hiérarchie appartient.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Le nom non ambigu de la dimension.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyCaption</p></td>
<td><p>Une étiquette ou une légende associée à la hiérarchie.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyCardinality</p></td>
<td><p>Le nombre de membres de la hiérarchie.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyGUID</p></td>
<td><p>Le GUID de la hiérarchie.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyName</p></td>
<td><p>Le nom de la hiérarchie.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Le nom non ambigu de la hiérarchie.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Le nom du schéma auquel ce cube appartient.</p></td>
</tr>
</tbody>
</table>

