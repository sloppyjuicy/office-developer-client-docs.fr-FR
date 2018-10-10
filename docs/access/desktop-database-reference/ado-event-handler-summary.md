---
title: Résumé du gestionnaire d'événements ADO
TOCTitle: ADO Event Handler Summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9042bdbf3271f5aed65f44d8c7f76f1dcbee1d9c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470730"
---
# <a name="ado-event-handler-summary"></a>Résumé du gestionnaire d'événements ADO


**S’applique à**: Access 2013 | Office 2013

Deux objets ADO peuvent déclencher des événements : l'objet [Connection](connection-object-ado.md) et l'objet [Recordset](recordset-object-ado.md). La famille **ConnectionEvent** est liée aux opérations sur l'objet **Connection** et la famille **RecordsetEvent** aux opérations sur l'objet **Recordset**.

  - **Événements Connection**: événements déclenchés lorsqu'une transaction sur une connexion est exécutée, validée ou annulée, lorsqu'un objet [Command](command-object-ado.md) est exécuté, lorsqu'un avertissement est émis au cours d'une opération sur un **événement Connection** ou lorsqu'un objet **Connection** est établi ou fermé.

  - **Événements Recordset**: événements sont émises autour des opérations d’extraction asynchrone, ainsi que lorsque vous naviguez dans les lignes d’un objet **Recordset** , modifiez un champ dans une ligne d’un **jeu d’enregistrements**, modifier une ligne dans un **jeu d’enregistrements**, ouvrez un ** Jeu d’enregistrements** avec un curseur côté serveur, fermer un **jeu d’enregistrements**ou modifier une quelconque dans le **jeu d’enregistrements**.

Les tableaux suivants présentent et décrivent les événements.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ConnectionEvent</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</p></td>
<td><p><strong>Gestion des transactions</strong>  : notification signalant que la transaction active sur la connexion a été lancée, validée ou annulée.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, déconnecter</a></p></td>
<td><p><strong>Gestion des connexions</strong>  : notification signalant que la connexion active va être établie, qu'elle est établie ou qu'elle est terminée.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p><strong>Gestion de l'exécution des commandes</strong>  : notification signalant que l'exécution de la commande active sur la connexion va être effectuée ou qu'elle est terminée.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p><strong>Informatif</strong>  : notification signalant que des informations supplémentaires sont disponibles concernant l'opération active.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>RecordsetEvent</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">événement FetchComplete</a></p></td>
<td><p><strong>État d'extraction</strong>  : notification de la progression d'une opération d'extraction de données ou de la fin d'une opération d'extraction. Ces événements ne sont déclenchés que si l'objet <strong>Recordset</strong> a été ouvert à l'aide d'un curseur côté client.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></p></td>
<td><p><strong>Gestion des modifications des champs</strong>  : notification signalant que la valeur du champ actif va changer ou qu'elle a changé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">événement EndOfRecordset</a></p></td>
<td><p><strong>Gestion de la navigation</strong>  : notification signalant que la position de la ligne active dans un objet <strong>Recordset</strong> va changer, qu'elle a changé ou qu'elle a atteint la fin de l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></p></td>
<td><p><strong>Gestion des modifications des lignes</strong>  : notification signalant qu'un élément de la ligne active de l'objet <strong>Recordset</strong> va changer ou a changé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></p></td>
<td><p><strong>Gestion des modifications de l'objet Recordset</strong>  : notification signalant qu'un élément de l'objet <strong>Recordset</strong> actif va changer ou a changé.</p></td>
</tr>
</tbody>
</table>

