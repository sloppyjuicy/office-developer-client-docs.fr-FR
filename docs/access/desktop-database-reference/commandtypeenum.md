---
title: CommandTypeEnum (référence de base de données du bureau Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b694d2d691766063f418aba6535fd9c7a8e3ca95
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469135"
---
# <a name="commandtypeenum"></a>CommandTypeEnum


**S’applique à**: Access 2013 | Office 2013

Spécifie comment interpréter un argument de commande.

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
<td><p><strong>adCmdUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Ne spécifie pas l'argument du type de commande.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdText</strong></p></td>
<td><p>1</p></td>
<td><p>Evalue <a href="commandtext-property-ado.md">CommandText</a> comme définition textuelle d’une commande ou d’un appel de procédure stockée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>valeur Command.CommandType</strong></p></td>
<td><p>2</p></td>
<td><p>Evalue <strong>CommandText</strong> comme nom de table dont les colonnes sont toutes renvoyées par une requête SQL générée en interne.</p></td>
</tr>
<tr class="even">
<td><p><strong>valeur adCmdStoredProc</strong></p></td>
<td><p>4</p></td>
<td><p>Evalue <strong>CommandText</strong> comme nom de procédure stockée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdUnknown</strong></p></td>
<td><p>8</p></td>
<td><p>Par défaut. Indique que le type de la commande dans la propriété <strong>CommandText</strong> n'est pas connu.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdFile</strong></p></td>
<td><p>256</p></td>
<td><p>Evalue <strong>CommandText</strong> comme nom de fichier d’un <a href="recordset-object-ado.md">Recordset</a> stocké avec persistance. S’utilise uniquement avec <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> et <a href="requery-method-ado.md">Requery</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTableDirect</strong></p></td>
<td><p>512</p></td>
<td><p>Evalue <strong>CommandText</strong> comme nom de table dont les colonnes sont toutes renvoyées. Utilisé uniquement avec <strong>Recordset.Open</strong> et <strong>Requery</strong> . Pour utiliser la méthode <a href="seek-method-ado.md">Seek</a> , le <strong>Recordset</strong> doit être ouvert avec <strong>adCmdTableDirect</strong>. Cette valeur ne peut être combinée avec la valeur <a href="executeoptionenum.md">ExecuteOptionEnum </a><strong>adAsyncExecute</strong>.</p></td>
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
<td><p>AdoEnums.CommandType.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.TEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.STOREDPROC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.FILE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLEDIRECT</p></td>
</tr>
</tbody>
</table>

