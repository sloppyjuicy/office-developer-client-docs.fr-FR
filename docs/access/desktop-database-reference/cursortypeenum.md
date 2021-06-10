---
title: CursorTypeEnum (référence de base de données de bureau Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295162"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**S’applique à** : Access 2013, Office 2013

Spécifie le type de curseur utilisé dans un objet [Recordset](recordset-object-ado.md).

<br/>

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
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p>2</p></td>
<td><p>Utilise un curseur dynamique. Les ajouts, les modifications et les suppressions effectués par d’autres utilisateurs sont visibles, et tous les types de déplacement dans l’objet <strong>Recordset</strong> sont permis, à l’exception des signets, si le fournisseur ne les prend pas en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>Par défaut. Utilise un curseur "descendant". Identique au curseur statique, sauf que vous ne pouvez que descendre dans les enregistrements. Les performances sont améliorées si vous n'avez besoin de ne passer qu'une fois dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>Utilise un curseur keyset. Identique à un curseur dynamique, sauf que vous ne pouvez pas voir les enregistrements ajoutés par d'autres utilisateurs, bien que les enregistrements supprimés par d'autres utilisateurs ne soient pas accessibles par votre <strong>Recordset</strong>. Les modifications apportées aux données par d'autres utilisateurs sont toujours visibles.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>Utilise un curseur statique. Il s'agit d"une copie statique d'un ensemble d'enregistrements, que vous pouvez utiliser pour trouver des données ou générer des rapports. Les ajouts, les modifications et les suppressions effectués par d'autres utiisateurs ne sont pas visibles.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Ne spécifie pas le type du curseur.</p></td>
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
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CursorType.DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.FORWARDONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.KEYSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.STATIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

