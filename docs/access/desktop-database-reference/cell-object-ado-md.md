---
title: Objet cell (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1fd28f453ef38b8a2e71f0e479c19fcd05c50aca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590099"
---
# <a name="cell-object-ado-md"></a>Objet cell (ADO MD)


**S’applique à** : Access 2013, Office 2013

Représente les données à l'intersection des coordonnées des axes d'un ensemble de cellules.

## <a name="remarks"></a>Remarques

Un objet **Cell** est renvoyé par la propriété [Item](item-property-ado-md-cellset.md) d’un objet [Cellset](cellset-object-ado-md.md).

Avec les collections et propriétés d'un objet **Cell**, vous pouvez :

- Renvoyer les données de la **cellule** à l'aide de la propriété [Value](value-property-ado-md.md).

- Renvoyer la chaîne représentant l'affichage mis en forme de la propriété **Value** à l'aide de la propriété [FormattedValue](formattedvalue-property-ado-md.md).

- Renvoyer la valeur ordinale de la **cellule** au sein de l' **ensemble de cellules** à l'aide de la propriété [Ordinal](ordinal-property-ado-md-cell.md).

- Déterminer la position de la **cellule** au sein de l'objet [CubeDef](cubedef-object-ado-md.md) à l'aide de la collection [Positions](positions-collection-ado-md.md).

- Extraire d'autres informations relatives à la **cellule** à l'aide de la collection ADO [Properties](properties-collection-ado.md) standard.

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
<td><p>BackColor</p></td>
<td><p>Couleur de fond utilisée pour l'affichage de la cellule.</p></td>
</tr>
<tr class="even">
<td><p>FontFlags</p></td>
<td><p>Masque binaire détaillant les effets de la police.</p></td>
</tr>
<tr class="odd">
<td><p>FontName</p></td>
<td><p>Police utilisée pour afficher la valeur de la cellule.</p></td>
</tr>
<tr class="even">
<td><p>FontSize</p></td>
<td><p>Taille de police utilisée pour afficher la valeur de la cellule.</p></td>
</tr>
<tr class="odd">
<td><p>ForeColor</p></td>
<td><p>Couleur de premier plan utilisée pour l'affichage de la cellule.</p></td>
</tr>
<tr class="even">
<td><p>FormatString</p></td>
<td><p>Valeur dans une chaîne mise en forme.</p></td>
</tr>
</tbody>
</table>

