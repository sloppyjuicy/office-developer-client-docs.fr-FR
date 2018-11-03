---
title: Cancel, méthode (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e80763ddad86a63aec605371b58ffeab383681dd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944017"
---
# <a name="cancel-method-ado"></a>Cancel, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Annule l'exécution d'un appel de méthode asynchrone en attente.

## <a name="syntax"></a>Syntaxe

*objet*. Annuler

## <a name="remarks"></a>Notes

Faites appel à la méthode **Cancel** pour mettre fin à l'exécution d'un appel de méthode asynchrone (à savoir une méthode appelée avec l'option **adAsyncConnect**, **adAsyncExecute** ou **adAsyncFetch** ).

Le tableau suivant indique quelle tâche est terminée lorsque vous utilisez la méthode **Cancel** sur un type d'objet particulier.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />

S'il s'agit d'un <em>objet</em></p></th>
<th><p>Le dernier appel asynchrone de cette méthode est terminé.</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="command-object-ado.md">Command</a></p></td>
<td><p><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</a></p></td>
</tr>
<tr class="even">
<td><p><a href="connection-object-ado.md">Objet Connection</a></p></td>
<td><p><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> ou <a href="open-method-ado-connection.md">Open</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> ou <a href="open-method-ado-record.md">Open</a></p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
</tr>
</tbody>
</table>

