---
title: Objet CubeDef (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c82c95a430da76694fe26300e877e86f86a2eb4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295309"
---
# <a name="cubedef-object-ado-md"></a>CubeDef, objet (ADO MD)


**S’applique à** : Access 2013, Office 2013

Représente un cube issu d'un schéma multidimensionnel, contenant un ensemble de dimensions connexes.

## <a name="remarks"></a>Remarques

Avec les collections et propriétés d'un objet **CubeDef**, vous pouvez :

  - Identifier un **CubeDef** à l'aide de la propriété [Name](name-property-ado-md.md).

  - Renvoyer une chaîne décrivant le cube à l'aide de la propriété [Description](description-property-ado-md.md).

  - Renvoyer les dimensions constituant le cube à l'aide de la collection [Dimensions](dimensions-collection-ado-md.md).

  - Obtenir des informations supplémentaires relatives au **CubeDef** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).

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
<td><p>CreatedOn</p></td>
<td><p>Date et heure de création du cube.</p></td>
</tr>
<tr class="odd">
<td><p>CubeGUID</p></td>
<td><p>GUID du cube.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>Le nom du cube.</p></td>
</tr>
<tr class="odd">
<td><p>CubeType</p></td>
<td><p>Le type du cube.</p></td>
</tr>
<tr class="even">
<td><p>DataUpdatedBy</p></td>
<td><p>ID d'utilisateur de la personne à l'origine de la dernière mise à jour des données.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Une description significative du cube.</p></td>
</tr>
<tr class="even">
<td><p>LastSchemaUpdate</p></td>
<td><p>Date et heure de la dernière mise à jour du schéma.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Le nom du schéma auquel ce cube appartient.</p></td>
</tr>
<tr class="even">
<td><p>SchemaUpdatedBy</p></td>
<td><p>ID d'utilisateur de la personne à l'origine de la dernière mise à jour du schéma.</p></td>
</tr>
</tbody>
</table>

