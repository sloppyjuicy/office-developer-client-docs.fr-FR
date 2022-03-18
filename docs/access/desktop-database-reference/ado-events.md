---
title: ActiveX Data Objects (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3b28ec0724983cac3bc881fffa7d12a19048d99c
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558527"
---
# <a name="ado-events"></a>Événements ADO

**S’applique à** : Access 2013, Office 2013

<table>
<colgroup>
<col />
<col />
</colgroup>
<tbody>
<tr class="even">
<th>Événement</th>
<th>Description</th>
</tr>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></p></td>
<td><p>Appelé après l'opération <strong>BeginTrans</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></p></td>
<td><p>Appelé après l'opération <strong>CommitTrans</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></p></td>
<td><p>Appelé après l'établissement d'une connexion.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></p></td>
<td><p>Appelé après la fermeture d'une connexion.</p></td>
</tr>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>Appelé lors d'une tentative de déplacement d'une ligne au-delà de la fin de l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p>Appelé à la fin de l'exécution d'une commande.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>Appelé après que tous les enregistrements d'une opération asynchrone de longue durée ont été récupérés dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>Appelé régulièrement au cours d'une opération asynchrone de longue durée pour indiquer le nombre de lignes récupérées jusque là dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Appelé après que la valeur d'un ou plusieurs objets <strong>Field</strong> a changé.</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p>Appelé lorsqu'un avertissement se produit au cours d'une opération <strong>ConnectionEvent</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Appelé après la modification de la position actuelle dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Appelé après la modification d'un ou de plusieurs enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Appelé après la modification de l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></p></td>
<td><p>Appelé après l'opération <strong>RollbackTrans</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Appelé avant qu'une opération en attente change la valeur d'un ou plusieurs objets <strong>Field</strong> dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Appelé avant la modification d'un ou plusieurs enregistrements (lignes) dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>Appelé avant qu'une opération en attente modifie l'objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a></p></td>
<td><p>Appelé avant le début d'une connexion.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a></p></td>
<td><p>Appelé juste avant qu'une commande en attente ne s'exécute sur cette connexion pour permettre à l'utilisateur d'examiner et de modifier les paramètres de la commande.</p></td>
</tr>
<tr class="even">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>L'événement <strong>WillMove</strong> est appelé <em>avant</em> qu'une opération en attente ne change la position actuelle dans l'objet <strong>Recordset</strong>.</p></td>
</tr>
</tbody>
</table>
