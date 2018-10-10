---
title: EventReasonEnum (référence de base de données du bureau Access)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec32b47d8e69c065d167fe86553aafdec906bc24
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469160"
---
# <a name="eventreasonenum"></a>EventReasonEnum


**S’applique à**: Access 2013 | Office 2013

Spécifie la cause à l'origine d'un événement.

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
<td><p><strong>adRsnAddNew</strong></p></td>
<td><p>1</p></td>
<td><p>Une opération a ajouté un nouvel enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnClose</strong></p></td>
<td><p>9</p></td>
<td><p>Une opération a fermé l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnDelete</strong></p></td>
<td><p>2</p></td>
<td><p>Une opération a supprimé un enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnFirstChange</strong></p></td>
<td><p>11</p></td>
<td><p>Une opération a effectué la première modification à un enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMove</strong></p></td>
<td><p>10</p></td>
<td><p>Une opération a déplacé le pointeur de l'enregistrement à l'intérieur de l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveFirst</strong></p></td>
<td><p>12</p></td>
<td><p>Une opération a déplacé le pointeur vers le premier enregistrement à l'intérieur de l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMoveLast</strong></p></td>
<td><p>15</p></td>
<td><p>Une opération a déplacé le pointeur vers le dernier enregistrement dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveNext</strong></p></td>
<td><p>13</p></td>
<td><p>Une opération a déplacé le pointeur vers l'enregistrement suivant dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMovePrevious</strong></p></td>
<td><p>14</p></td>
<td><p>Une opération a déplacé le pointeur vers l'enregistrement précédent dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnRequery</strong></p></td>
<td><p>7</p></td>
<td><p>Une opération a de nouveau interrogé l’objet <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnResynch</strong></p></td>
<td><p>8</p></td>
<td><p>Une opération a resynchronisé l'objet <strong>Recordset</strong> avec la base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoAddNew</strong></p></td>
<td><p>5</p></td>
<td><p>Une opération a annulé l'ajout d'un nouvel enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUndoDelete</strong></p></td>
<td><p>6</p></td>
<td><p>Une opération a annulé la suppression d'un enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoUpdate</strong></p></td>
<td><p>4</p></td>
<td><p>Une opération a annulé la mise à jour d'un enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUpdate</strong></p></td>
<td><p>3</p></td>
<td><p>Une opération a annulé un enregistrement existant.</p></td>
</tr>
</tbody>
</table>


**Équivalent ADO/WFC**

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.EventReason.ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.CLOSE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.DELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.FIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.MOVEFIRST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVELAST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.MOVENEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVEPREVIOUS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.REQUERY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.RESYNCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.UNDOADDNEW</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.UNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.UNDOUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.UPDATE</p></td>
</tr>
</tbody>
</table>

