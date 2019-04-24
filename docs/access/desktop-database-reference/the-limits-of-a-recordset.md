---
title: Limites d'un jeu d'enregistrements
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d0da48080b64e43cc39b9567275e1a8755a8881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314111"
---
# <a name="limits-of-a-recordset"></a>Limites d’un recordset


**S’applique à** : Access 2013, Office 2013

Utilisez les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites d'un objet **Recordset** en vous déplaçant d'un enregistrement à l'autre. Considérez les propriétés **BOF** et **EOF** comme des enregistrements « fantômes » placés au début et à la fin de l'objet **Recordset**. En se basant sur l'exemple d'objet **Recordset** présenté dans [Examen des données](chapter-3-examining-data.md), on obtient les résultats suivants :

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Mentionnées</p></th>
<th><p>ProductName</p></th>
<th><p>UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p>7j/7</p></td>
<td><p>Pêches séchées bio Oncle Bob</p></td>
<td><p>30,0000</p></td>
</tr>
<tr class="odd">
<td><p>13</p></td>
<td><p>Longvi</p></td>
<td><p>23,2500</p></td>
</tr>
<tr class="even">
<td><p>vingt</p></td>
<td><p>Choucroute Frau Kraut</p></td>
<td><p>45,6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Pommes séchées Manjimup</p></td>
<td><p>53,0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Tofu LongVi</p></td>
<td><p>10,0000</p></td>
</tr>
<tr class="odd">
<td><p>EOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


La propriété **BOF** retourne la valeur **True** (-1) si la position d'enregistrement actif est située avant le premier enregistrement et la valeur **False** (0) si la position d'enregistrement actif est située au niveau du premier enregistrement ou après celui-ci.

La propriété **EOF** renvoie la valeur **True** si la position d'enregistrement actif est située après le dernier enregistrement et la valeur **False** si la position d'enregistrement actif est située au niveau du dernier enregistrement ou avant celui-ci.

Si la propriété **BOF** ou **EOF** a la valeur **True**, cela signifie qu'il n'y a aucun enregistrement actif, comme l'illustre le code suivant :

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

Si vous ouvrez un objet **Recordset** ne contenant aucun enregistrement, les propriétés **BOF** et **EOF** ont toutes deux la valeur **True** et la valeur définie pour la propriété **RecordCount** de l'objet **Recordset** dépend du type de curseur. -1 sera renvoyé pour les curseurs dynamiques (**CursorType** = **adOpenDynamic**) et 0 sera renvoyé pour les autres curseurs.

Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement est l'enregistrement actif. Les propriétés **BOF** et **EOF** ont, dans ce cas, la valeur **False**.

Si vous supprimez le dernier enregistrement restant de l'objet **Recordset**, le curseur reste dans un état indéterminé. Selon le fournisseur, les propriétés **BOF** et **EOF** peuvent conserver la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.

