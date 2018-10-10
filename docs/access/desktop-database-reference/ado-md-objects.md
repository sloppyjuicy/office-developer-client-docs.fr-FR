---
title: Objets ADO MD (référence de base de données du bureau Access)
TOCTitle: ADO MD Objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0bde8dfebd4351275ede6e08cbeec7d8e3d710c3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471120"
---
# <a name="ado-md-objects"></a>Objets ADO MD


**S’applique à**: Access 2013 | Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="axis-object-ado-md.md">Axe</a></p></td>
<td><p>Représente un axe de position ou de filtrage d'un ensemble de cellules, contenant des membres sélectionnés d'une ou plusieurs dimensions.</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">Catalogue</a></p></td>
<td><p>Contient les informations de schéma multidimensionnel (en d'autres termes, les cubes et dimensions sous-jacentes, les hiérarchies, les niveaux et les membres) spécifiques à un fournisseur de données multidimensionnelles (MDP).</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>Représente les données situées à l'intersection des coordonnées et contenues dans un ensemble de cellules.</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Ensemble de cellules</a></p></td>
<td><p>Représente les résultats d'une requête multidimensionnelle. Il s'agit d'une collection de cellules sélectionnées dans des cubes ou d'autres ensembles de cellules.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">CubeDef</a></p></td>
<td><p>Représente un cube issu d'un schéma multidimensionnel, contenant un ensemble de dimensions connexes.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimension</a></p></td>
<td><p>Représente une des dimensions d'un cube multidimensionnel, contenant une ou plusieurs hiérarchies de membres.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hiérarchie</a></p></td>
<td><p>Représente un mode qui les membres d’une dimension peuvent être regroupés ou &quot;reportées. &quot; Une dimension peut être agrégée selon une ou plusieurs hiérarchies.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Level</a></p></td>
<td><p>Contient un ensemble de membres, chacun occupant le même rang dans une hiérarchie.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Membre</a></p></td>
<td><p>Représente un membre d'un niveau dans un cube, l'enfant d'un membre d'un niveau ou un membre d'une position le long d'un axe d'un ensemble de cellules.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Représente un ensemble d'un ou plusieurs membres de différentes dimensions définissant un point le long d'un axe.</p></td>
</tr>
</tbody>
</table>


En outre, l'objet **Catalog** est lié à un objet ADO **Connection**, qui est inclus dans la bibliothèque ADO standard :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="connection-object-ado.md">Objet Connection</a></p></td>
<td><p>Représente une connexion ouverte à une source de données.</p></td>
</tr>
</tbody>
</table>


De nombreux objets ADO MD peuvent être contenus dans une collection correspondante. Par exemple, un objet [CubeDef](cubedef-object-ado-md.md) peut être contenu dans une collection [CubeDefs](cubedefs-collection-ado-md.md) d'un objet **Catalog**. Pour plus d'informations, consultez la rubrique [Collections ADO MD](ado-md-collections.md).

