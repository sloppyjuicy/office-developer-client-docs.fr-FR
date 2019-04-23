---
title: Méthodes ADO (ActiveX Data Objects)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3169b7eaab6ad290bfc385881f5de69edc80111f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283281"
---
# <a name="ado-methods"></a><span data-ttu-id="c459e-102">Méthodes ADO</span><span class="sxs-lookup"><span data-stu-id="c459e-102">ADO methods</span></span>

<span data-ttu-id="c459e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c459e-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="c459e-104">Méthode</span><span class="sxs-lookup"><span data-stu-id="c459e-104">Method</span></span></th>
<th><span data-ttu-id="c459e-105">Description</span><span class="sxs-lookup"><span data-stu-id="c459e-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="c459e-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-107">Crée un nouvel enregistrement pour un objet <strong>Recordset</strong> actualisable.</span><span class="sxs-lookup"><span data-stu-id="c459e-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-108"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="c459e-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-p101">Ajoute un objet à une collection. S'il s'agit de la collection <strong>Fields</strong>, un nouvel objet <strong>Field</strong> peut être créé avant d'être ajouté à la collection.</span><span class="sxs-lookup"><span data-stu-id="c459e-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="c459e-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-112">Ajoute des données à un objet <strong>Field</strong> textuel ou binaire de grande taille ou à un objet <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans et RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="c459e-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-114">Gère le traitement des transactions dans un objet <strong>Connection</strong> comme suit :</span><span class="sxs-lookup"><span data-stu-id="c459e-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="c459e-115"><strong>BeginTrans</strong>: lance une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="c459e-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="c459e-p102">
<strong>CommitTrans</strong>: enregistre les modifications apportées et termine la transaction active. Lance aussi parfois une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="c459e-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="c459e-118">
<strong>RollbackTrans</strong> : annule les modifications et met fin à la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="c459e-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="c459e-119">Cette méthode peut également lancer une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="c459e-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-120"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="c459e-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-121">Annule l'exécution d'un appel de méthode asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="c459e-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="c459e-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-123">Annule une mise à jour par lot en attente.</span><span class="sxs-lookup"><span data-stu-id="c459e-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="c459e-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-125">Annule les modifications apportées à la ligne active ou à la nouvelle ligne d'un objet <strong>Recordset</strong> ou à la collection <strong>Fields</strong> d'un objet <strong>Record</strong> avant d'appeler la méthode <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="c459e-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-127">Supprime tous les objets <strong>Error</strong> de la collection <strong>Errors</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="c459e-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-129">Crée une copie de l'objet <strong>Recordset</strong> à partir d'un objet <strong>Recordset</strong> existant.</span><span class="sxs-lookup"><span data-stu-id="c459e-129">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="c459e-130">Le cas échéant, spécifie que le clone doit être en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c459e-130">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="c459e-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-132">Ferme un objet ouvert et les objets qui en dépendent.</span><span class="sxs-lookup"><span data-stu-id="c459e-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="c459e-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-134">Compare deux signets et retourne une indication de leurs valeurs relatives.</span><span class="sxs-lookup"><span data-stu-id="c459e-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="c459e-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-136">Copie un fichier ou un répertoire, ainsi que son contenu à un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="c459e-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="c459e-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-138">Copie le nombre spécifié de caractères ou d'octets (en fonction du <strong>type</strong>) de l'objet <strong>Stream</strong> dans un autre objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="c459e-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-140">Crée un nouvel objet <strong>Parameter</strong> avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="c459e-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-141"><a href="delete-method-ado-parameters-collection.md">Delete (collection Parameters ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-142">Supprime un objet de la collection <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-143"><a href="delete-method-ado-fields-collection.md">Delete (collection Fields ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-144">Supprime un objet de la collection <strong>Fields</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-145"><a href="delete-method-ado-recordset.md">Delete (objet Recordset ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-146">Supprime l'enregistrement actif ou un groupe d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c459e-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="c459e-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-148">Supprime un fichier ou un répertoire et tous ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="c459e-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (objet Command ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-150">Exécute la requête, l'instruction SQL ou la procédure stockée spécifiée dans la propriété <strong>CommandText </strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (objet Connection ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-152">Exécute la requête, l'instruction SQL, la procédure stockée ou le texte propre au fournisseur spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c459e-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-153"><a href="find-method-ado.md">Chercher</a></span><span class="sxs-lookup"><span data-stu-id="c459e-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-154">Recherche, dans un objet <strong>Recordset </strong>, la ligne qui répond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c459e-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-155"><a href="flush-method-ado.md">Comptabilité</a></span><span class="sxs-lookup"><span data-stu-id="c459e-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-156">Force le transfert du contenu de l'objet <strong>Stream</strong> restant dans la mémoire tampon d'ADO dans l'objet sous-jacent auquel l'objet <strong>Stream</strong> est associé.</span><span class="sxs-lookup"><span data-stu-id="c459e-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="c459e-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-158">Retourne un objet <strong>Recordset</strong> dont les lignes représentent les fichiers et les sous-répertoires dans le répertoire représenté par cet objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="c459e-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-160">Retourne la totalité ou une partie du contenu d'un objet <strong>Field</strong> textuel ou binaire de grande taille.</span><span class="sxs-lookup"><span data-stu-id="c459e-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="c459e-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-162">Extrait plusieurs enregistrements d'un objet <strong>Recordset</strong> dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="c459e-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="c459e-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-164">Retourne l'objet <strong>Recordset</strong> sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="c459e-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="c459e-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-166">Charge le contenu d'un fichier existant dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-167"><a href="move-method-ado.md">Déplacer</a></span><span class="sxs-lookup"><span data-stu-id="c459e-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-168">Change la position de l'enregistrement actif dans un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext et MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="c459e-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-170">Passe au premier ou au dernier enregistrement ou à l'enregistrement suivant ou précédent d'un objet <strong>Recordset</strong> spécifique et sélectionne cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c459e-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="c459e-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-172">Déplace un fichier ou un répertoire et son contenu à un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="c459e-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="c459e-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-174">Efface l'objet <strong>Recordset</strong> actif et retourne l'objet <strong>Recordset</strong> suivant en exécutant une série de commandes.</span><span class="sxs-lookup"><span data-stu-id="c459e-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-175"><a href="open-method-ado-connection.md">Open (objet Connection ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-176">Ouvre une connexion vers une source de données.</span><span class="sxs-lookup"><span data-stu-id="c459e-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-177"><a href="open-method-ado-record.md">Open (objet Record ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-178">Ouvre un objet <strong>Record</strong> existant ou crée un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="c459e-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-179"><a href="open-method-ado-recordset.md">Open (objet Recordset ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-180">Ouvre un curseur.</span><span class="sxs-lookup"><span data-stu-id="c459e-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-181"><a href="open-method-ado-stream.md">Open (objet Stream ADO)</a></span><span class="sxs-lookup"><span data-stu-id="c459e-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-182">Ouvre un objet <strong>Stream</strong> pour manipuler les flux de données textuels ou binaires.</span><span class="sxs-lookup"><span data-stu-id="c459e-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="c459e-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-184">Obtient du fournisseur les informations du schéma de base de données.</span><span class="sxs-lookup"><span data-stu-id="c459e-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-185"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="c459e-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-186">Lit un nombre spécifique d'octets dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="c459e-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-188">Lit un nombre spécifique de caractères dans un objet <strong>Stream</strong> textuel.</span><span class="sxs-lookup"><span data-stu-id="c459e-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="c459e-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-190">Met à jour les objets d'une collection pour qu'ils reflètent les objets disponibles ou spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c459e-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-191"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="c459e-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-192">Met à jour les données d'un objet <strong>Recordset</strong> en réexécutant la requête sur laquelle l'objet est basé.</span><span class="sxs-lookup"><span data-stu-id="c459e-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-193"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="c459e-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-194">Actualise les données de l'objet <strong>Recordset</strong> actif ou la collection <strong>Fields</strong> d'un objet <strong>Record</strong> à partir de la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="c459e-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="c459e-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-196">Enregistre l'objet <strong>Recordset</strong> dans un fichier ou dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="c459e-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-198">Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c459e-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="c459e-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-200">Recherche, dans l'index d'un objet <strong>Recordset</strong>, la ligne qui correspond aux valeurs spécifiées et fait de cette ligne la ligne active.</span><span class="sxs-lookup"><span data-stu-id="c459e-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="c459e-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-202">Définit la position qui correspond à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="c459e-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="c459e-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-204">Ignore une ligne entière lors de la lecture d'un flux de texte.</span><span class="sxs-lookup"><span data-stu-id="c459e-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="c459e-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-206">Fournit les statistiques sur un flux ouvert.</span><span class="sxs-lookup"><span data-stu-id="c459e-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-207"><a href="supports-method-ado.md">Compatible</a></span><span class="sxs-lookup"><span data-stu-id="c459e-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-208">Détermine si un objet <strong>Recordset</strong> spécifique prend en charge un type particulier de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c459e-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-209"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="c459e-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-210">Enregistre les modifications que vous avez apportées à la ligne active d'un objet <strong>Recordset</strong> ou à la collection <strong>Fields</strong> d'un objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="c459e-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-212">Écrit toutes les mises à jour par lot en attente sur le disque.</span><span class="sxs-lookup"><span data-stu-id="c459e-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c459e-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="c459e-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-214">Écrit des données binaires dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c459e-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="c459e-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="c459e-216">Écrit une chaîne de texte spécifiée dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="c459e-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
