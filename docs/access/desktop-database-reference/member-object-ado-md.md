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
# <a name="member-object-ado-md"></a>Objet Member (ADO MD)


**S’applique à** : Access 2013, Office 2013

Représente un membre d'un niveau dans un cube, l'enfant d'un membre d'un niveau ou un membre d'une position le long d'un axe d'un ensemble de cellules.

## <a name="remarks"></a>Remarques

Les propriétés d’un **membre** dépendent du contexte dans lequel il est utilisé. Un **membre** d’un [niveau](level-object-ado-md.md) dans un [CubeDef](cubedef-object-ado-md.md) a la propriété [Children](children-property-ado-md.md) qui renvoie les **membres** du niveau inférieur suivant dans la hiérarchie du **membre** actif. Pour un **membre** d’une [position](position-object-ado-md.md), la collection **Children** est toujours vide. Par ailleurs, la propriété [Type](type-property-ado-md.md) s’applique uniquement aux **membres** d’un **niveau**.

Un **membre** d'une **position** a deux propriétés : [DrilledDown](drilleddown-property-ado-md.md) et [ParentSameAsPrev](parentsameasprev-property-ado-md.md), qui permettent d'afficher l'[ensemble de cellules](cellset-object-ado-md.md). Une erreur survient si vous accédez à ces propriétés sur un **membre** d'un **niveau**.

Avec les collections et propriétés d'un objet **Member** d'un **niveau**, vous pouvez :

  - Identifier le **membre** à l’aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).

  - Renvoyer une chaîne à utiliser lors de l’affichage du **membre** à l’aide de la propriété [Caption](caption-property-ado-md.md).

  - Renvoyer une chaîne significative décrivant le **membre** d’une mesure ou d’une formule à l’aide de la propriété [Description](description-property-ado-md.md).

  - Déterminer la nature du **membre** à l’aide de la propriété [Type](type-property-ado-md.md).

  - Obtenir des informations relatives au **niveau** du **membre** à l’aide des propriétés [LevelDepth](leveldepth-property-ado-md.md) et [LevelName](levelname-property-ado-md.md).

  - Obtenir les **membres** connexes d’une [hiérarchie](hierarchy-object-ado-md.md) à l’aide des propriétés [Parent](parent-property-ado-md.md) et [Children](children-property-ado-md.md).

  - Comptabiliser les enfants d’un **membre** à l’aide de la propriété [ChildCount](childcount-property-ado-md.md).

  - Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l’objet **Level**.

Avec les collections et propriétés d’un **membre** d’une **position** le long d’un [axe](axis-object-ado-md.md), vous pouvez :

  - Identifier le **membre** à l’aide des propriétés [Name](name-property-ado-md.md) et [UniqueName](uniquename-property-ado-md.md).

  - Renvoyer une chaîne à utiliser lors de l’affichage du **membre** à l’aide de la propriété [Caption](caption-property-ado-md.md).

  - Renvoyer une chaîne significative décrivant le **membre** d’une mesure ou d’une formule à l’aide de la propriété [Description](description-property-ado-md.md).

  - Obtenir des informations relatives au **niveau** du **membre** à l’aide des propriétés [LevelDepth](leveldepth-property-ado-md.md) et [LevelName](levelname-property-ado-md.md).

  - Comptabiliser les enfants d’un **membre** à l’aide de la propriété [ChildCount](childcount-property-ado-md.md).

  - Utiliser la propriété [DrilledDown](drilleddown-property-ado-md.md) pour déterminer si au moins un enfant sur l’**axe** suit immédiatement ce **membre**.

  - Utiliser la propriété [ParentSameAsPrev](parentsameasprev-property-ado-md.md) pour déterminer si le parent de ce **membre** est le même que le parent du **membre** précédent.

  - Utiliser la collection ADO standard [Properties](properties-collection-ado.md) pour obtenir des informations supplémentaires à propos de l’objet **Level**.

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
<td><p>ChildrenCardinality</p></td>
<td><p>Le nombre d'enfants de ce membre.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Le nom du cube.</p></td>
</tr>
<tr class="even">
<td><p>Description</p></td>
<td><p>Une description significative du membre.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Le nom non ambigu de la <a href="dimension-object-ado-md.md">dimension</a>.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Le nom non ambigu de la hiérarchie.</p></td>
</tr>
<tr class="odd">
<td><p>LevelNumber</p></td>
<td><p>La distance entre le niveau et la racine de la hiérarchie.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Le nom non ambigu du niveau.</p></td>
</tr>
<tr class="odd">
<td><p>MemberCaption</p></td>
<td><p>Une étiquette ou une légende associée au membre.</p></td>
</tr>
<tr class="even">
<td><p>MemberGUID</p></td>
<td><p>Le GUID du membre.</p></td>
</tr>
<tr class="odd">
<td><p>MemberName</p></td>
<td><p>Le nom du membre.</p></td>
</tr>
<tr class="even">
<td><p>MemberOrdinal</p></td>
<td><p>Le numéro ordinal du membre.</p></td>
</tr>
<tr class="odd">
<td><p>MemberType</p></td>
<td><p>Le type du membre.</p></td>
</tr>
<tr class="even">
<td><p>MemberUniqueName</p></td>
<td><p>Le nom non ambigu du membre.</p></td>
</tr>
<tr class="odd">
<td><p>ParentCount</p></td>
<td><p>Le nombre de parents de ce membre.</p></td>
</tr>
<tr class="even">
<td><p>ParentLevel</p></td>
<td><p>Le numéro de niveau du parent du membre.</p></td>
</tr>
<tr class="odd">
<td><p>ParentUniqueName</p></td>
<td><p>Le nom non ambigu du parent du membre.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Le nom du schéma auquel ce cube appartient.</p></td>
</tr>
</tbody>
</table>

