---
title: Recordset2 Members (DAO)
TOCTitle: Recordset2 Members
ms:assetid: 6ef57191-9da4-7904-d55c-60b59b895a50
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195572(v=office.15)
ms:contentKeyID: 48545523
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 336ef56f373f4fb75d481bff09c1cd5a341af1d0
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63723393"
---
# <a name="recordset2-members-dao"></a>Recordset2 Members (DAO)


**S’applique à** : Access 2013, Office 2013

Un objet Recordset2 représente les enregistrements d'une table de base ou les enregistrements générés suite à l'exécution d'une requête.

## <a name="methods"></a>Méthodes

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></p></td>
<td><p>Crée un enregistrement pour un objet <strong>Recordset2</strong> modifiable.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-cancel-method-dao.md">Annuler</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Annule l'exécution d'un appel asynchrone de méthode en attente (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p>Annule les mises à jour en attente pour un objet<strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> en double qui fait référence à l'objet <strong>Recordset2</strong> d'origine.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-close-method-dao.md">Close</a></strong></p></td>
<td><p>Ferme un <strong>Recordset</strong> ouvert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>Renvoie un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong> qui est une copie de l’objet <strong>QueryDef</strong> utilisée pour créer l’objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> représenté par l’espace réservé recordset (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></p></td>
<td><p>Non pris en charge pour cet objet.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>Copie l’enregistrement actif à partir d’un objet<strong><a href="recordset-object-dao.md">Recordset</a></strong> à la mémoire tampon de copie pour les éditions futures.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Remplit tout ou partie d'un cache local pour un objet <strong>Recordset</strong> contenant les données d'une source de données ODBC connectée au moteur de base de données Microsoft Access (bases de données ODBC connectées au moteur de base de données Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>Localise le premier enregistrement dans un objet <strong>Recordset</strong> de type feuille de réponse dynamique ou capture instantanée qui remplit les critères spécifiés et rend l’enregistrement actif (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>Recherche le dernier enregistrement dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>Recherche l'enregistrement suivant dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>Recherche l'enregistrement précédent dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p>Récupère plusieurs lignes à partir d’un objet<strong> <a href="recordset-object-dao.md">Recordset</a> </strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-move-method-dao.md">Move</a></strong></p></td>
<td><p>Déplace l’enregistrement actif d’un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></p></td>
<td><p>Atteint le premier enregistrement d’un objet <strong>Recordset</strong> spécifié et en fait l’enregistrement actif.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>Atteint le dernier enregistrement d’un objet <strong>Recordset</strong> spécifié et en fait l’enregistrement actif.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>Atteint l’enregistrement d’un objet <strong>Recordset</strong>suivant spécifié et en fait l’enregistrement actif.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>Atteint l’enregistrement d’un objet <strong>Recordset</strong>précédent spécifié et en fait l’enregistrement actif.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Obtient le jeu d'enregistrements suivant, le cas échéant, qui est renvoyé par une requête Sélection à parties multiples dans le cadre d'un appel <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong>, et renvoie une valeur de type <strong>Boolean</strong> indiquant si un ou plusieurs enregistrements supplémentaires sont en attente (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l’ajoute à la collection <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></p></td>
<td><p>Met à jour les données dans un objet<strong><a href="recordset-object-dao.md">Recordset</a></strong>en exécutant de nouveau la requête sur laquelle l’objet est basé.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></p></td>
<td><p>Localise l’enregistrement dans un objet <strong>Recordset</strong> de type table indexé qui correspond aux critères spécifiés pour l’index actuel et fait de cet enregistrement l’enregistrement actif (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-update-method-dao.md">Update</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Enregistre le contenu de la mémoire tampon de la copie dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> modifiable.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></p></td>
<td><p>Définit ou renvoie le nombre d’enregistrements relatif de l’enregistrement actif d’un objet <strong>Recordset2</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Renvoie le nombre d'enregistrements dont la dernière mise à jour par lot n'a pas pu se terminer (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Renvoie un tableau de signets indiquant les lignes à l'origine de conflits dans la dernière opération de mise à jour par lot (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Définit ou renvoie le nombre d'instructions renvoyées au serveur dans chaque lot (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si la position d'enregistrement actuelle précède le premier enregistrement d'un objet <strong>Recordset</strong>. Type <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></p></td>
<td><p>Définit ou renvoie un signet qui identifie de façon unique l'enregistrement actif dans un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si un objet<strong>Recordset</strong>prend en charge les signets, pouvant être défini en utilisant la propriétéSignet.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local. Valeur <strong>Long</strong> en en lecture et en écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>Définit ou renvoie une valeur spécifiant le signet du premier enregistrement d'un objet Recordset de type feuille de réponse dynamique qui contient des données d'une source de données ODBC à placer dans le cache local (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></p></td>
<td><p>Renvoie l’objet<strong> <a href="connection-object-dao.md">connexion</a> </strong> qui correspond à la base de données.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Renvoie la date et l'heure de création d'une table de base (espaces de travail Microsoft Access uniquement). Type <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>Renvoie une valeur qui indique l’état de modification pour l’enregistrement actif.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si la position d'enregistrement actuelle suit le dernier enregistrement d'un objet <strong>Recordset</strong>. Type <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés pour l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui détermine les enregistrements inclus dans un objet <strong>Recordset</strong> ouvert par la suite (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture et en écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-index-property-dao.md">Index</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le nom de l’objet <strong><a href="index-object-dao.md">Index</a></strong> actuel dans un type de tableau<strong><a href="recordset-object-dao.md">Recordset</a></strong>(Microsoft Access Espaces de travail uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>Renvoie un signet indiquant l’enregistrement le plus récemment ajouté ou modifié.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Renvoie la date et l'heure de la dernière modification apportée à une table de base. Type <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>Définit ou renvoie une valeur indiquant le type de verrouillage qui est appliqué lorsque vous effectuez une modification.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie le nom de l'objet spécifié. Type <strong>chaîne</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p>Indique si un enregistrement particulier a été trouvé à l’aide de la méthode<strong> <a href="recordset2-seek-method-dao.md">Recherche</a> </strong> ou une des méthodes<strong> <a href="recordset2-findfirst-method-dao.md">Trouver</a> </strong> (Microsoft Access espaces de travail uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></p></td>
<td><p>Renvoie l'objet <strong>Recordset</strong> parent de l'objet Recordset défini. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p>Définit ou renvoie une valeur indiquant l'emplacement approximatif de l'enregistrement actif dans l'objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> en fonction du pourcentage d'enregistrements dans cet objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Renvoie le nombre d'enregistrements accédés dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> ou le nombre total d'enregistrements dans un objet <strong>Recordset</strong> de type table ou un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. Type <strong>Long</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Renvoie un valeur indiquant l'état de mise à jour de l'enregistrement actif s'il fait partie d'une mise à jour par lot (espaces de travail ODBCDirect uniquement). Type <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p>Renvoie une valeur indiquant si un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> prend en charge la méthode <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong>, laquelle réexécute la requête sur laquelle l'objet <strong>Recordset</strong> est basé.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></p></td>
<td><p>Définit ou renvoie l’ordre de tri des enregistrements d’un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> (espace de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Indique si l'exécution d'une opération asynchrone (c.-à-d. une méthode appelée avec l'option <strong>dbRunAsync</strong>) est terminée (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-type-property-dao.md">Type</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données <strong>Integer</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Valeur <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
<p>Définit ou renvoie une valeur qui indique la manière dont est construite la clause WHERE pour chaque enregistrement pendant une mise à jour par lot, et si cette dernière doit utiliser une instruction UPDATE ou DELETE suivie d'un INSERT (espaces de travail ODBCDirect uniquement). Type de données <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>. En lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui valide les données dans un champ au moment de leur modification ou de leur ajout à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Définit ou renvoie une valeur spécifiant le texte du message affiché par votre application si la valeur d'un objet <strong>Field</strong> ne respecte pas la règle de validation définie par le paramètre de la propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture seule.</p></td>
</tr>
</tbody>
</table>

