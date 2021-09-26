---
title: EditModeEnum (référence de base de données de bureau Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 86006f3a15b105a58fb04695e9c7977e189f2171
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626791"
---
# <a name="editmodeenum"></a>EditModeEnum

**S’applique à** : Access 2013, Office 2013

Spécifie l'état d'édition d'un enregistrement.

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
<td><p><strong>adEditNone</strong></p></td>
<td><p>0</p></td>
<td><p>Indique qu'aucune opération d'édition n'est en cours.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>1</p></td>
<td><p>Indique que les données de l'enregistrement en cours ont été modifiées, mais pas enregistrées.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>2</p></td>
<td><p>Indique que la méthode <a href="addnew-method-ado.md">AddNew</a> a été appelée et que l’enregistrement en cours dans la zone tampon de copie est un nouvel enregistrement qui n’a pas été enregistré dans la base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>4 </p></td>
<td><p>Indique que l'enregistrement en cours a été supprimé.</p></td>
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
<td><p>AdoEnums.EditMode.NONE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EditMode.INPROGRESS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EditMode.ADD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EditMode.DELETE</p></td>
</tr>
</tbody>
</table>

