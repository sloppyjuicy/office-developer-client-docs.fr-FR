---
title: Méthodes d’ActiveX Data Objects (ADO)
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ef05e7f322b769102ce25aab7dfc26a75b0aa22
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879332"
---
# <a name="ado-methods"></a><span data-ttu-id="e481d-102">Méthodes ADO</span><span class="sxs-lookup"><span data-stu-id="e481d-102">ADO Methods</span></span>


<span data-ttu-id="e481d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e481d-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e481d-104"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="e481d-104"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-105">Crée un enregistrement pour un objet <strong>Recordset</strong> actualisable.</span><span class="sxs-lookup"><span data-stu-id="e481d-105">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-106"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="e481d-106"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-p101">Ajoute un objet à une collection. S'il s'agit de la collection <strong>Fields</strong>, un nouvel objet <strong>Field</strong> peut être créé avant d'être ajouté à la collection.</span><span class="sxs-lookup"><span data-stu-id="e481d-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="e481d-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-110">Cette méthode ajoute des données à un objet <strong>Field</strong> de données binaires ou de texte volumineux ou à un objet <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-110">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans et RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="e481d-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-112">Gère le traitement des transactions dans un objet <strong>Connection</strong> comme suit : <strong>BeginTrans</strong> : lance une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="e481d-112">Manages transaction processing within a <strong>Connection</strong> object as follows: <strong>BeginTrans</strong> — Begins a new transaction.</span></span><br /><span data-ttu-id="e481d-p102">
<strong>CommitTrans</strong>: enregistre les modifications apportées et termine la transaction active. Lance aussi parfois une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="e481d-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br /><span data-ttu-id="e481d-115">
<strong>RollbackTrans</strong> : annule les modifications et met fin à transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="e481d-115">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="e481d-116">Lance aussi parfois une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="e481d-116">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-117"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="e481d-117"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-118">Annule l'exécution d'un appel de méthode asynchrone en attente.</span><span class="sxs-lookup"><span data-stu-id="e481d-118">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="e481d-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-120">Annule une mise à jour par lot en attente.</span><span class="sxs-lookup"><span data-stu-id="e481d-120">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="e481d-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-122">Annule toutes les modifications apportées à la ligne active ou à une nouvelle ligne d'un objet <strong>Recordset</strong> ou dans la collection <strong>Fields</strong> d'un objet <strong>Record</strong> avant que la méthode <strong>Update</strong> soit appelée.</span><span class="sxs-lookup"><span data-stu-id="e481d-122">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-123"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="e481d-123"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-124">Supprime tous les objets <strong>Error</strong> de la collection <strong>Errors</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-124">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-125"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="e481d-125"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-p104">Crée une copie de l'objet <strong>Recordset</strong> à partir d'un objet <strong>Recordset</strong> existant. Spécifie éventuellement que le clone doit être en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e481d-p104">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object. Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-128"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="e481d-128"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-129">Ferme un objet ouvert, ainsi que tous les objets qui en dépendent.</span><span class="sxs-lookup"><span data-stu-id="e481d-129">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="e481d-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-131">Compare deux signets et retourne une indication de leurs valeurs relatives.</span><span class="sxs-lookup"><span data-stu-id="e481d-131">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="e481d-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-133">Copie un fichier ou un répertoire, avec tout son contenu, dans un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="e481d-133">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-134"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="e481d-134"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-135">Copie le nombre de caractères ou d'octets spécifié (selon la propriété <strong>Type</strong>) d'un objet <strong>Stream</strong> vers un autre objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-135">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-136"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="e481d-136"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-137">Crée un objet <strong>Parameter</strong> avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="e481d-137">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-138"><a href="delete-method-ado-parameters-collection.md">Supprimer (Collection de paramètres ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-138"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-139">Supprime un objet de la collection <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-139">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-140"><a href="delete-method-ado-fields-collection.md">Supprimer (Collection de champs ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-140"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-141">Supprime un objet de la collection <strong>Fields</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-141">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-142"><a href="delete-method-ado-recordset.md">Supprimer (objet Recordset ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-142"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-143">Supprime l'enregistrement actif ou un groupe d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="e481d-143">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="e481d-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-145">Supprime un fichier ou un répertoire avec tous ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="e481d-145">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Exécuter (commande ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-147">Exécute la requête, l'instruction SQL ou la procédure stockée spécifiée dans la propriété <strong>CommandText</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-147">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Exécuter (ADO Connection)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-149">Exécute la requête, l’instruction SQL, la procédure stockée ou le texte propre au fournisseur spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e481d-149">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-150"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="e481d-150"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-151">Recherche un objet <strong>Recordset</strong> pour la ligne qui répond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e481d-151">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-152"><a href="flush-method-ado.md">Vider</a></span><span class="sxs-lookup"><span data-stu-id="e481d-152"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-153">Force l'envoi de l'objet <strong>Stream</strong> conservé dans la mémoire tampon ADO vers l'objet sous-jacent auquel cet objet <strong>Stream</strong> est associé.</span><span class="sxs-lookup"><span data-stu-id="e481d-153">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-154"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="e481d-154"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-155">Renvoie un <strong>objet Recordset</strong> dont les lignes représentent les fichiers et sous-répertoires du répertoire représenté par cet <strong>enregistrement</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-155">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-156"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="e481d-156"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-157">Renvoie tout ou une partie du contenu d’un objet de <strong>champ</strong> de données binaires ou de texte de grande taille.</span><span class="sxs-lookup"><span data-stu-id="e481d-157">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-158"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="e481d-158"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-159">Récupère plusieurs enregistrements d'un objet <strong>Recordset</strong> dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="e481d-159">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-160"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="e481d-160"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-161">Retourne l'objet <strong>Recordset</strong> sous la forme d'une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e481d-161">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-162"><a href="loadfromfile-method-ado.md">La méthode LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="e481d-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-163">Charge le contenu d'un fichier existant dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-163">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-164"><a href="move-method-ado.md">Déplacer</a></span><span class="sxs-lookup"><span data-stu-id="e481d-164"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-165">Déplace la position de l'enregistrement actif dans un objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-165">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext et MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="e481d-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-167">Accède au premier, au dernier ou à l'enregistrement suivant d'un objet <strong>Recordset</strong> spécifié et fait de celui-ci l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="e481d-167">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-168"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="e481d-168"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-169">Déplace un fichier ou un répertoire, avec tout son contenu, vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="e481d-169">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e481d-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-171">Efface l'objet <strong>Recordset</strong> actif et retourne l'objet <strong>Recordset</strong> suivant en exécutant une série de commandes.</span><span class="sxs-lookup"><span data-stu-id="e481d-171">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-172"><a href="open-method-ado-connection.md">Open (objet Connection ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-172"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-173">Ouvre une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="e481d-173">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-174"><a href="open-method-ado-record.md">Open (objet Record ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-174"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-175">Ouvre un objet <strong>Record</strong> existant ou crée un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="e481d-175">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-176"><a href="open-method-ado-recordset.md">Ouvrir (objet Recordset ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-176"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-177">Ouvre un curseur.</span><span class="sxs-lookup"><span data-stu-id="e481d-177">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-178"><a href="open-method-ado-stream.md">Ouvrez (ADO Stream)</a></span><span class="sxs-lookup"><span data-stu-id="e481d-178"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-179">Ouvre un objet <strong>Stream</strong> pour manipuler des flux de données binaires ou de texte.</span><span class="sxs-lookup"><span data-stu-id="e481d-179">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-180"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="e481d-180"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-181">Obtient du fournisseur les informations du schéma de base de données.</span><span class="sxs-lookup"><span data-stu-id="e481d-181">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-182"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="e481d-182"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-183">Lit un nombre spécifique d'octets dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-183">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-184"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="e481d-184"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-185">Lit un nombre spécifique de caractères dans un objet <strong>Stream</strong> textuel.</span><span class="sxs-lookup"><span data-stu-id="e481d-185">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-186"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="e481d-186"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-187">Met à jour les objets d'une collection pour qu'ils reflètent les objets disponibles ou spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e481d-187">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-188"><a href="requery-method-ado.md">Actualiser</a></span><span class="sxs-lookup"><span data-stu-id="e481d-188"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-189">Cette méthode met à jour les données d'un objet <strong>Recordset</strong> en réexécutant la requête sur laquelle l'objet est basé.</span><span class="sxs-lookup"><span data-stu-id="e481d-189">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-190"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="e481d-190"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-191">Cette méthode actualise les données de l'objet <strong>Recordset</strong> actif ou la collection <strong>Fields</strong> d'un objet <strong>Record</strong> à partir de la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e481d-191">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-192"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="e481d-192"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-193">Enregistre l'objet <strong>Recordset</strong> dans un fichier ou un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-193">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-194"><a href="savetofile-method-ado.md">Méthode SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="e481d-194"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-195">Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="e481d-195">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-196"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="e481d-196"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-197">Effectue une recherche dans l'index d'un objet <strong>Recordset</strong> pour retrouver rapidement la ligne qui correspond aux valeurs spécifiées et faire de cette ligne la position de ligne active.</span><span class="sxs-lookup"><span data-stu-id="e481d-197">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-198"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="e481d-198"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-199">Définit la position qui représente la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="e481d-199">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-200"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="e481d-200"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-201">Saute une ligne complète lors de la lecture d'un flux de texte.</span><span class="sxs-lookup"><span data-stu-id="e481d-201">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-202"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="e481d-202"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-203">Fournit les statistiques sur un flux ouvert.</span><span class="sxs-lookup"><span data-stu-id="e481d-203">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-204"><a href="supports-method-ado.md">Prend en charge</a></span><span class="sxs-lookup"><span data-stu-id="e481d-204"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-205">Détermine si un objet <strong>Recordset</strong> spécifié prend en charge un type de fonctionnalité particulier.</span><span class="sxs-lookup"><span data-stu-id="e481d-205">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-206"><a href="update-method-ado.md">Mettre à jour</a></span><span class="sxs-lookup"><span data-stu-id="e481d-206"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-207">Enregistre les modifications apportées à la ligne active d'un objet <strong>Recordset</strong> ou à la collection <strong>Fields</strong> d'un objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-207">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="e481d-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-209">Écrit toutes les mises à jour par lot en attente sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e481d-209">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e481d-210"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="e481d-210"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-211">Écrit des données binaires dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-211">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e481d-212"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="e481d-212"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="e481d-213">Écrit une chaîne de texte spécifiée dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="e481d-213">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

