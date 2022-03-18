---
title: ActiveX data objects (ADO)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e028b33a75846e083979daa658ec859ff30a3163
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558368"
---
# <a name="ado-methods"></a>Méthodes ADO

**S’applique à** : Access 2013, Office 2013


<table>
<colgroup>
<col />
<col />
</colgroup>
<tbody>
<tr class="even">
<th>Méthode</th>
<th>Description</th>
</tr>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Crée un nouvel enregistrement pour un objet <strong>Recordset</strong> actualisable.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>Ajoute un objet à une collection. S'il s'agit de la collection <strong>Fields</strong>, un nouvel objet <strong>Field</strong> peut être créé avant d'être ajouté à la collection.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Ajoute des données à un objet <strong>Field</strong> textuel ou binaire de grande taille ou à un objet <strong>Parameter</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans et RollbackTrans</a></p></td>
<td><p>Gère le traitement des transactions dans un objet <strong>Connection</strong> comme suit :<br/><br/><strong>BeginTrans</strong>: lance une nouvelle transaction.<br/><strong>CommitTrans</strong>: enregistre les modifications apportées et termine la transaction active. Lance aussi parfois une nouvelle transaction.<br/><strong>RollbackTrans</strong> : annule toutes les modifications et met fin à la transaction en cours. Cette méthode peut également lancer une nouvelle transaction.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Annule l'exécution d'un appel de méthode asynchrone en attente.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Annule une mise à jour par lot en attente.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Annule les modifications apportées à la ligne active ou à la nouvelle ligne d'un objet <strong>Recordset</strong> ou à la collection <strong>Fields</strong> d'un objet <strong>Record</strong> avant d'appeler la méthode <strong>Update</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p>Supprime tous les objets <strong>Error</strong> de la collection <strong>Errors</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Crée une copie de l'objet <strong>Recordset</strong> à partir d'un objet <strong>Recordset</strong> existant. Spécifie éventuellement que le clone doit être en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Ferme un objet ouvert et les objets qui en dépendent.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Compare deux signets et retourne une indication de leurs valeurs relatives.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Copie un fichier ou un répertoire, ainsi que son contenu à un autre emplacement.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copie le nombre spécifié de caractères ou d'octets (en fonction du <strong>type</strong>) de l'objet <strong>Stream</strong> dans un autre objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Crée un nouvel objet <strong>Parameter</strong> avec les propriétés spécifiées.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (collection Parameters ADO)</a></p></td>
<td><p>Supprime un objet de la collection <strong>Parameters</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Delete (collection Fields ADO)</a></p></td>
<td><p>Supprime un objet de la collection <strong>Fields</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (objet Recordset ADO)</a></p></td>
<td><p>Supprime l'enregistrement actif ou un groupe d'enregistrements.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Supprime un fichier ou un répertoire et tous ses sous-répertoires.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (objet Command ADO)</a></p></td>
<td><p>Exécute la requête, l'instruction SQL ou la procédure stockée spécifiée dans la propriété <strong>CommandText </strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (objet Connection ADO)</a></p></td>
<td><p>Exécute la requête, l'instruction SQL, la procédure stockée ou le texte propre au fournisseur spécifiés.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p>Recherche, dans un objet <strong>Recordset </strong>, la ligne qui répond aux critères spécifiés.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Flush</a></p></td>
<td><p>Force le transfert du contenu de l'objet <strong>Stream</strong> restant dans la mémoire tampon d'ADO dans l'objet sous-jacent auquel l'objet <strong>Stream</strong> est associé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Retourne un objet <strong>Recordset</strong> dont les lignes représentent les fichiers et les sous-répertoires dans le répertoire représenté par cet objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Retourne la totalité ou une partie du contenu d'un objet <strong>Field</strong> textuel ou binaire de grande taille.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Extrait plusieurs enregistrements d'un objet <strong>Recordset</strong> dans un tableau.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Retourne l'objet <strong>Recordset</strong> sous forme de chaîne.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Charge le contenu d'un fichier existant dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Change la position de l'enregistrement actif dans un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext et MovePrevious</a></p></td>
<td><p>Passe au premier ou au dernier enregistrement ou à l'enregistrement suivant ou précédent d'un objet <strong>Recordset</strong> spécifique et sélectionne cet enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Déplace un fichier ou un répertoire et son contenu à un autre emplacement.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Efface l'objet <strong>Recordset</strong> actif et retourne l'objet <strong>Recordset</strong> suivant en exécutant une série de commandes.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (objet Connection ADO)</a></p></td>
<td><p>Ouvre une connexion vers une source de données.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (objet Record ADO)</a></p></td>
<td><p>Ouvre un objet <strong>Record</strong> existant ou crée un fichier ou un répertoire.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open (objet Recordset ADO)</a></p></td>
<td><p>Ouvre un curseur.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open (objet Stream ADO)</a></p></td>
<td><p>Ouvre un objet <strong>Stream</strong> pour manipuler les flux de données textuels ou binaires.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Obtient du fournisseur les informations du schéma de base de données.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Lit un nombre spécifique d'octets dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lit un nombre spécifique de caractères dans un objet <strong>Stream</strong> textuel.</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>Met à jour les objets d'une collection pour qu'ils reflètent les objets disponibles ou spécifiques au fournisseur.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Actualiser</a></p></td>
<td><p>Met à jour les données d'un objet <strong>Recordset</strong> en réexécutant la requête sur laquelle l'objet est basé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Actualise les données de l'objet <strong>Recordset</strong> actif ou la collection <strong>Fields</strong> d'un objet <strong>Record</strong> à partir de la base de données sous-jacente.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Enregistre l'objet <strong>Recordset</strong> dans un fichier ou dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Recherche, dans l'index d'un objet <strong>Recordset</strong>, la ligne qui correspond aux valeurs spécifiées et fait de cette ligne la ligne active.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Définit la position qui correspond à la fin du flux.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Ignore une ligne entière lors de la lecture d'un flux de texte.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Fournit les statistiques sur un flux ouvert.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Prend en charge</a></p></td>
<td><p>Détermine si un objet <strong>Recordset</strong> spécifique prend en charge un type particulier de fonctionnalité.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Mise à jour</a></p></td>
<td><p>Enregistre les modifications que vous avez apportées à la ligne active d'un objet <strong>Recordset</strong> ou à la collection <strong>Fields</strong> d'un objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Écrit toutes les mises à jour par lot en attente sur le disque.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Écrit des données binaires dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Écrit une chaîne de texte spécifiée dans un objet <strong>Stream</strong>.</p></td>
</tr>
</tbody>
</table>

