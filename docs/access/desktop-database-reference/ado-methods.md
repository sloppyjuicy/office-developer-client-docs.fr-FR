---
title: Méthodes d’ActiveX Data Objects (ADO)
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b7a685352063c3c1dd4c9bbd62e9c1fc4cdfe11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469331"
---
# <a name="ado-methods"></a>Méthodes ADO


**S’applique à**: Access 2013 | Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Crée un enregistrement pour un objet <strong>Recordset</strong> actualisable.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>Ajoute un objet à une collection. S'il s'agit de la collection <strong>Fields</strong>, un nouvel objet <strong>Field</strong> peut être créé avant d'être ajouté à la collection.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Cette méthode ajoute des données à un objet <strong>Field</strong> de données binaires ou de texte volumineux ou à un objet <strong>Parameter</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans et RollbackTrans</a></p></td>
<td><p>Gère le traitement des transactions dans un objet <strong>Connection</strong> comme suit : <strong>BeginTrans</strong> : lance une nouvelle transaction.<br />
<strong>CommitTrans</strong>: enregistre les modifications apportées et termine la transaction active. Lance aussi parfois une nouvelle transaction.<br />
<strong>RollbackTrans</strong> : annule les modifications et met fin à transaction en cours. Lance aussi parfois une nouvelle transaction.</p></td>
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
<td><p>Annule toutes les modifications apportées à la ligne active ou à une nouvelle ligne d'un objet <strong>Recordset</strong> ou dans la collection <strong>Fields</strong> d'un objet <strong>Record</strong> avant que la méthode <strong>Update</strong> soit appelée.</p></td>
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
<td><p>Ferme un objet ouvert, ainsi que tous les objets qui en dépendent.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Compare deux signets et retourne une indication de leurs valeurs relatives.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Copie un fichier ou un répertoire, avec tout son contenu, dans un autre emplacement.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copie le nombre de caractères ou d'octets spécifié (selon la propriété <strong>Type</strong>) d'un objet <strong>Stream</strong> vers un autre objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Crée un objet <strong>Parameter</strong> avec les propriétés spécifiées.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Supprimer (Collection de paramètres ADO)</a></p></td>
<td><p>Supprime un objet de la collection <strong>Parameters</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Supprimer (Collection de champs ADO)</a></p></td>
<td><p>Supprime un objet de la collection <strong>Fields</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Supprimer (objet Recordset ADO)</a></p></td>
<td><p>Supprime l'enregistrement actif ou un groupe d'enregistrements.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Supprime un fichier ou un répertoire avec tous ses sous-répertoires.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Exécuter (commande ADO)</a></p></td>
<td><p>Exécute la requête, l'instruction SQL ou la procédure stockée spécifiée dans la propriété <strong>CommandText</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Exécuter (ADO Connection)</a></p></td>
<td><p>Exécute la requête, l’instruction SQL, la procédure stockée ou le texte propre au fournisseur spécifiés.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p>Recherche un objet <strong>Recordset</strong> pour la ligne qui répond aux critères spécifiés.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Vider</a></p></td>
<td><p>Force l'envoi de l'objet <strong>Stream</strong> conservé dans la mémoire tampon ADO vers l'objet sous-jacent auquel cet objet <strong>Stream</strong> est associé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Renvoie un <strong>objet Recordset</strong> dont les lignes représentent les fichiers et sous-répertoires du répertoire représenté par cet <strong>enregistrement</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Renvoie tout ou une partie du contenu d’un objet de <strong>champ</strong> de données binaires ou de texte de grande taille.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Récupère plusieurs enregistrements d'un objet <strong>Recordset</strong> dans un tableau.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Retourne l'objet <strong>Recordset</strong> sous la forme d'une chaîne.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">La méthode LoadFromFile</a></p></td>
<td><p>Charge le contenu d'un fichier existant dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Déplacer</a></p></td>
<td><p>Déplace la position de l'enregistrement actif dans un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext et MovePrevious</a></p></td>
<td><p>Accède au premier, au dernier ou à l'enregistrement suivant d'un objet <strong>Recordset</strong> spécifié et fait de celui-ci l'enregistrement actif.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Déplace un fichier ou un répertoire, avec tout son contenu, vers un autre emplacement.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Efface l'objet <strong>Recordset</strong> actif et retourne l'objet <strong>Recordset</strong> suivant en exécutant une série de commandes.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (objet Connection ADO)</a></p></td>
<td><p>Ouvre une connexion à une source de données.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (objet Record ADO)</a></p></td>
<td><p>Ouvre un objet <strong>Record</strong> existant ou crée un fichier ou un répertoire.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Ouvrir (objet Recordset ADO)</a></p></td>
<td><p>Ouvre un curseur.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Ouvrez (ADO Stream)</a></p></td>
<td><p>Ouvre un objet <strong>Stream</strong> pour manipuler des flux de données binaires ou de texte.</p></td>
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
<td><p>Cette méthode met à jour les données d'un objet <strong>Recordset</strong> en réexécutant la requête sur laquelle l'objet est basé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Cette méthode actualise les données de l'objet <strong>Recordset</strong> actif ou la collection <strong>Fields</strong> d'un objet <strong>Record</strong> à partir de la base de données sous-jacente.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Enregistre l'objet <strong>Recordset</strong> dans un fichier ou un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">Méthode SaveToFile</a></p></td>
<td><p>Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Effectue une recherche dans l'index d'un objet <strong>Recordset</strong> pour retrouver rapidement la ligne qui correspond aux valeurs spécifiées et faire de cette ligne la position de ligne active.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Définit la position qui représente la fin du flux.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Saute une ligne complète lors de la lecture d'un flux de texte.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Fournit les statistiques sur un flux ouvert.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Prend en charge</a></p></td>
<td><p>Détermine si un objet <strong>Recordset</strong> spécifié prend en charge un type de fonctionnalité particulier.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Mettre à jour</a></p></td>
<td><p>Enregistre les modifications apportées à la ligne active d'un objet <strong>Recordset</strong> ou à la collection <strong>Fields</strong> d'un objet <strong>Record</strong>.</p></td>
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

