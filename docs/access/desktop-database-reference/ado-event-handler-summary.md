---
title: Résumé du gestionnaire d’événements ADO
TOCTitle: ADO event handler summary
ms:assetid: f50b9eb4-df6e-7b9d-0b3d-dca8945167a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250247(v=office.15)
ms:contentKeyID: 48548701
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c37c1257ad3f3cb046f7faf82ffcb93f067b1ff5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283372"
---
# <a name="ado-event-handler-summary"></a><span data-ttu-id="e8ba7-102">Résumé du gestionnaire d’événements ADO</span><span class="sxs-lookup"><span data-stu-id="e8ba7-102">ADO Event Handler Summary</span></span>


<span data-ttu-id="e8ba7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8ba7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8ba7-p101">Deux objets ADO peuvent déclencher des événements : l'objet [Connection](connection-object-ado.md) et l'objet [Recordset](recordset-object-ado.md). La famille **ConnectionEvent** est liée aux opérations sur l'objet **Connection** et la famille **RecordsetEvent** aux opérations sur l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-p101">Two ADO objects can raise events: the [Connection](connection-object-ado.md) object and the [Recordset](recordset-object-ado.md) object. The **ConnectionEvent** family pertains to operations on the **Connection** object, and the **RecordsetEvent** family pertains to operations on the **Recordset** object.</span></span>

- <span data-ttu-id="e8ba7-106">**Événements Connection**: événements déclenchés lorsqu'une transaction sur une connexion est exécutée, validée ou annulée, lorsqu'un objet [Command](command-object-ado.md) est exécuté, lorsqu'un avertissement est émis au cours d'une opération sur un **événement Connection** ou lorsqu'un objet **Connection** est établi ou fermé.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-106">**Connection Events**: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a [Command](command-object-ado.md) executes; when a warning occurs during a **Connection Event** operation; or when a **Connection** starts or ends.</span></span>

- <span data-ttu-id="e8ba7-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-107">**Recordset Events**: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a **Recordset** object, change a field in a row of a **Recordset**, change a row in a **Recordset**, open a **Recordset** with a server-side cursor, close a **Recordset**, or make any change whatsoever in the **Recordset**.</span></span>

<span data-ttu-id="e8ba7-108">Les tableaux suivants présentent et décrivent les événements.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-108">The following tables summarize the events and their descriptions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8ba7-109">ConnectionEvent</span><span class="sxs-lookup"><span data-stu-id="e8ba7-109">ConnectionEvent</span></span></p></th>
<th><p><span data-ttu-id="e8ba7-110">Description</span><span class="sxs-lookup"><span data-stu-id="e8ba7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8ba7-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete,</span><span class="sxs-lookup"><span data-stu-id="e8ba7-111"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a>, CommitTransComplete, RollbackTransComplete</span></span></p></td>
<td><p><span data-ttu-id="e8ba7-112"><strong>Gestion des transactions</strong>  : notification signalant que la transaction active sur la connexion a été lancée, validée ou annulée.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-112"><strong>Transaction Management</strong> — Notification that the current transaction on the connection has started, committed, or rolled back.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba7-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-113"><a href="willconnect-event-ado.md">WillConnect</a>, <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete, Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-114"><strong>Gestion des connexions</strong>  : notification signalant que la connexion active va être établie, qu'elle est établie ou qu'elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-114"><strong>Connection Management</strong> — Notification that the current connection will start, has started, or has ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba7-115"><a href="willexecute-event-ado.md">WillExecute,</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-115"><a href="willexecute-event-ado.md">WillExecute</a>, <a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-116"><strong>Gestion de l'exécution des commandes</strong>  : notification signalant que l'exécution de la commande active sur la connexion va être effectuée ou qu'elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-116"><strong>Command Execution Management</strong> — Notification that the execution of the current command on the connection will start or has ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba7-117"><a href="infomessage-event-ado.md">InfoMessage,</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-117"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-118"><strong>Informatif</strong>  : notification signalant que des informations supplémentaires sont disponibles concernant l'opération active.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-118"><strong>Informational</strong> — Notification that there is additional information about the current operation.</span></span></p></td>
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
<th><p><span data-ttu-id="e8ba7-119">RecordsetEvent</span><span class="sxs-lookup"><span data-stu-id="e8ba7-119">RecordsetEvent</span></span></p></th>
<th><p><span data-ttu-id="e8ba7-120">Description</span><span class="sxs-lookup"><span data-stu-id="e8ba7-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8ba7-121"><a href="fetchprogress-event-ado.md">FetchProgress,</a>, <a href="fetchcomplete-event-ado.md">FetchComplete,</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-121"><a href="fetchprogress-event-ado.md">FetchProgress</a>, <a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-p102"><strong>État d'extraction</strong>  : notification de la progression d'une opération d'extraction de données ou de la fin d'une opération d'extraction. Ces événements ne sont déclenchés que si l'objet <strong>Recordset</strong> a été ouvert à l'aide d'un curseur côté client.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-p102"><strong>Retrieval Status</strong> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed. These events are only available if the <strong>Recordset</strong> was opened using a client-side cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba7-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-124"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField, FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-125"><strong>Gestion des modifications des champs</strong>  : notification signalant que la valeur du champ actif va changer ou qu'elle a changé.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-125"><strong>Field Change Management</strong> — Notification that the value of the current field will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba7-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-126"><a href="willmove-and-movecomplete-events-ado.md">WillMove, MoveComplete</a>, <a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-127"><strong>Gestion de la navigation</strong>  : notification signalant que la position de la ligne active dans un objet <strong>Recordset</strong> va changer, qu'elle a changé ou qu'elle a atteint la fin de l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-127"><strong>Navigation Management</strong> — Notification that the current row position in a <strong>Recordset</strong> will change, has changed, or has reached the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba7-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord, RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-129"><strong>Gestion des modifications des lignes</strong>  : notification signalant qu'un élément de la ligne active de l'objet <strong>Recordset</strong> va changer ou a changé.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-129"><strong>Row Change Management</strong> — Notification that something in the current row of the <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba7-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e8ba7-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset, RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e8ba7-131"><strong>Gestion des modifications de l'objet Recordset</strong>  : notification signalant qu'un élément de l'objet <strong>Recordset</strong> actif va changer ou a changé.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-131"><strong>Recordset Change Management</strong> — Notification that something in the current <strong>Recordset</strong> will change, or has changed.</span></span></p></td>
</tr>
</tbody>
</table>

