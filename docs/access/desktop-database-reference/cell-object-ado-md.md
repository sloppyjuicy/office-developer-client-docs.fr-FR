---
title: Objet cell (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2150152cf90b2ae17378ccb154253fee4652f240
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630846"
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

