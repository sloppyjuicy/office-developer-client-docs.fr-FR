---
title: IsolationLevelEnum (référence de base de données du bureau Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80e7d22a5152b24894bf746b939f705739d4220d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472429"
---
# <a name="isolationlevelenum"></a>IsolationLevelEnum


**S’applique à**: Access 2013 | Office 2013

Spécifie le niveau d'isolement de transaction d'un objet [Connection](connection-object-ado.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>: adXactUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Indique que le fournisseur applique un niveau d’isolement différent de celui spécifié, mais que ce niveau ne peut être déterminé.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactChaos</strong></p></td>
<td><p>16</p></td>
<td><p>Indique que les modifications en attente de transactions mieux isolées ne peuvent être remplacées.</p></td>
</tr>
<tr class="odd">
<td><p><strong>à adXactBrowse</strong></p></td>
<td><p>256</p></td>
<td><p>Indique qu'à partir d'une transaction, vous pouvez visualiser les modifications non validées des autres transactions.</p></td>
</tr>
<tr class="even">
<td><p><strong>valeur adXactReadUncommitted</strong></p></td>
<td><p>256</p></td>
<td><p>Identique à <strong>adXactBrowse</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>à adXactCursorStability</strong></p></td>
<td><p>4096</p></td>
<td><p>Indique qu'à partir d'une transaction, vous pouvez visualiser les modifications d'autres transactions uniquement si elles ont été validées.</p></td>
</tr>
<tr class="even">
<td><p><strong>adXactReadCommitted</strong></p></td>
<td><p>4096</p></td>
<td><p>Identique à <strong>adXactCursorStability</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactRepeatableRead</strong></p></td>
<td><p>65536</p></td>
<td><p>Indique qu'à partir d'une transaction, vous ne pouvez pas voir les modifications des autres transactions, mais qu'une nouvelle requête peut extraire de nouveaux objets <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>à adXactIsolated</strong></p></td>
<td><p>1048576</p></td>
<td><p>Indique que les transactions sont réalisées indépendamment d'autres transactions.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adXactSerializable</strong></p></td>
<td><p>1048576</p></td>
<td><p>Identique à <strong>adXactIsolated</strong>.</p></td>
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
<td><p>AdoEnums.IsolationLevel.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.CHAOS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.BROWSE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.READUNCOMMITTED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.CURSORSTABILITY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.READCOMMITTED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.REPEATABLEREAD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.IsolationLevel.ISOLATED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.IsolationLevel.SERIALIZABLE</p></td>
</tr>
</tbody>
</table>

