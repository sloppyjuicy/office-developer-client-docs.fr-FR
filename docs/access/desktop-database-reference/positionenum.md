---
title: PositionEnum (référence de base de données de bureau Access)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6a13183d985849e44dd6ab1931c117bfe3aad97b
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462086"
---
# <a name="positionenum"></a>PositionEnum

**S’applique à** : Access 2013, Office 2013

Spécifie la position en cours du pointeur de l’enregistrement dans un objet [Recordset](recordset-object-ado.md).


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adPosBOF</strong></p></td>
<td><p>-2</p></td>
<td><p>Indique que le pointeur de l’enregistrement en cours est de type BOF (la propriété <a href="bof-eof-properties-ado.md">BOF</a> est <strong>True</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPosEOF</strong></p></td>
<td><p>-3</p></td>
<td><p>Indique que le pointeur de l’enregistrement en cours est de type EOF (la propriété <a href="bof-eof-properties-ado.md">EOF</a> est <strong>True</strong>).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPosUnknown</strong></p></td>
<td><p>-1</p></td>
<td><p>Indique que l’objet <strong>Recordset</strong> est vide, que la position en cours n’est pas connue, ou que le fournisseur ne prend pas en charge la propriété <a href="absolutepage-property-ado.md">AbsolutePage</a> ou <a href="absoluteposition-property-ado.md">AbsolutePosition</a>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Position.BOF</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Position.EOF</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Position.UNKNOWN</p></td>
</tr>
</tbody>
</table>

