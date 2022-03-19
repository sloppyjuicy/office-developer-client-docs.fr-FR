---
title: Limites d'un jeu d'enregistrements
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3f3422fc4bd284aa293afe1a9fd550db4c4889a5
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634169"
---
# <a name="limits-of-a-recordset"></a>Limites d’un recordset


**S’applique à** : Access 2013, Office 2013

Utilisez les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites d'un objet **Recordset** en vous déplaçant d'un enregistrement à l'autre. Considérez les propriétés **BOF** et **EOF** comme des enregistrements « fantômes » placés au début et à la fin de l'objet **Recordset**. En se basant sur l'exemple d'objet **Recordset** présenté dans [Examen des données](chapter-3-examining-data.md), on obtient les résultats suivants :

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>ProductID</p></th>
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
<td><p>7 </p></td>
<td><p>Pêches séchées bio Oncle Bob</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14 </p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>Choucroute Frau Kraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Pommes séchées Manjimup</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Tofu LongVi</p></td>
<td><p>10.0000</p></td>
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

Si vous ouvrez un objet **Recordset** ne contenant aucun enregistrement, les propriétés **BOF** et **EOF** ont toutes deux la valeur **True** et la valeur définie pour la propriété **RecordCount** de l'objet **Recordset** dépend du type de curseur. -1 est renvoyé pour les curseurs dynamiques (**CursorTypeadOpenDynamic** = ) et 0 pour les autres curseurs.

Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement est l'enregistrement actif. Les propriétés **BOF** et **EOF** ont, dans ce cas, la valeur **False**.

Si vous supprimez le dernier enregistrement restant de l'objet **Recordset**, le curseur reste dans un état indéterminé. Selon le fournisseur, les propriétés **BOF** et **EOF** peuvent conserver la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.

