---
title: Événements ADO (ActiveX Data Objects)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cc2ef73798dca18e00c42768fde78da2abdb56a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283337"
---
# <a name="ado-events"></a><span data-ttu-id="f82f6-102">Événements ADO</span><span class="sxs-lookup"><span data-stu-id="f82f6-102">ADO events</span></span>

<span data-ttu-id="f82f6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f82f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="f82f6-104">Événement</span><span class="sxs-lookup"><span data-stu-id="f82f6-104">Event</span></span></th>
<th><span data-ttu-id="f82f6-105">Description</span><span class="sxs-lookup"><span data-stu-id="f82f6-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-106"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-107">Appelé après l'opération <strong>BeginTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-107">Called after the <strong>BeginTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-108"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-109">Appelé après l'opération <strong>CommitTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-109">Called after the <strong>CommitTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-110"><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-111">Appelé après l'établissement d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="f82f6-111">Called after a connection starts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-112"><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-113">Appelé après la fermeture d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="f82f6-113">Called after a connection ends.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-114"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-115">Appelé lors d'une tentative de déplacement d'une ligne au-delà de la fin de l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-115">Called when there is an attempt to move to a row past the end of the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-116"><a href="executecomplete-event-ado.md">ExecuteComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-117">Appelé à la fin de l'exécution d'une commande.</span><span class="sxs-lookup"><span data-stu-id="f82f6-117">Called after a command has finished executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-118"><a href="fetchcomplete-event-ado.md">FetchComplete,</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-118"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-119">Appelé après que tous les enregistrements d'une opération asynchrone de longue durée ont été récupérés dans l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-119">Called after all the records in a lengthy asynchronous operation have been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-120"><a href="fetchprogress-event-ado.md">FetchProgress,</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-120"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-121">Appelé régulièrement au cours d'une opération asynchrone de longue durée pour indiquer le nombre de lignes récupérées jusque là dans l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-121">Called periodically during a lengthy asynchronous operation to report how many rows have currently been retrieved into the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-122"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-123">Appelé après que la valeur d'un ou plusieurs objets <strong>Field</strong> a changé.</span><span class="sxs-lookup"><span data-stu-id="f82f6-123">Called after the value of one or more <strong>Field</strong> objects has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-124"><a href="infomessage-event-ado.md">InfoMessage,</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-124"><a href="infomessage-event-ado.md">InfoMessage</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-125">Appelé lorsqu'un avertissement se produit au cours d'une opération <strong>ConnectionEvent</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-125">Called whenever a warning occurs during a <strong>ConnectionEvent</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-126"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-127">Appelé après la modification de la position actuelle dans l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-127">Called after the current position in the <strong>Recordset</strong> changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-128"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-129">Appelé après la modification d'un ou de plusieurs enregistrements.</span><span class="sxs-lookup"><span data-stu-id="f82f6-129">Called after one or more records change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-130"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-131">Appelé après la modification de l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-131">Called after the <strong>Recordset</strong> has changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete,</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-132"><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-133">Appelé après l'opération <strong>RollbackTrans</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-133">Called after the <strong>RollbackTrans</strong> operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-134"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-135">Appelé avant qu'une opération en attente change la valeur d'un ou plusieurs objets <strong>Field</strong> dans l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-135">Called before a pending operation changes the value of one or more <strong>Field</strong> objects in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-136"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-137">Appelé avant la modification d'un ou plusieurs enregistrements (lignes) dans l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-137">Called before one or more records (rows) in the <strong>Recordset</strong> change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-138"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-139">Appelé avant qu'une opération en attente modifie l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-139">Called before a pending operation changes the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-140"><a href="willconnect-event-ado.md">WillConnect</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-140"><a href="willconnect-event-ado.md">WillConnect</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-141">Appelé avant le début d'une connexion.</span><span class="sxs-lookup"><span data-stu-id="f82f6-141">Called before a connection starts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f82f6-142"><a href="willexecute-event-ado.md">WillExecute,</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-142"><a href="willexecute-event-ado.md">WillExecute</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-143">Appelé juste avant qu'une commande en attente ne s'exécute sur cette connexion pour permettre à l'utilisateur d'examiner et de modifier les paramètres de la commande.</span><span class="sxs-lookup"><span data-stu-id="f82f6-143">Called just before a pending command executes on this connection and affords the user an opportunity to examine and modify the pending execution parameters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f82f6-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="f82f6-144"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="f82f6-145">L'événement <strong>WillMove</strong> est appelé <em>avant</em> qu'une opération en attente ne change la position actuelle dans l'objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f82f6-145">The <strong>WillMove</strong> event is called <em>before</em> a pending operation changes the current position in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
