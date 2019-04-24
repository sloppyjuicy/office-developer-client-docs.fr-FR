---
title: Connection, membres (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 098f44d87390351c23e61000ecbe47eae35810ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295904"
---
# <a name="connection-members-dao"></a>Connection, membres (DAO)

**S’applique à** : Access 2013, Office 2013

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access. Un objet Connection représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).
 
## <a name="methods"></a>Méthodes

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p>Annule l'exécution d'un appel asynchrone de méthode en attente (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-close-method-dao.md">Close</a></strong></p></td>
<td><p>Ferme un objet <strong>Connection</strong> ouvert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Crée un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Exécute une requête Action ou une instruction SQL sur l'objet spécifié.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="connection-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte. Valeur de type <strong>String</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-database-property-dao.md">Database</a></strong></p></td>
<td><p>Renvoie l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui correspond à cette connexion (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie le nom d'un objet <strong><a href="connection-object-dao.md">Connection</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Renvoie une collection <strong>QueryDefs</strong> qui contient tous les objets <strong>QueryDef</strong> de la connexion spécifiée. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie la durée d'attente (en secondes) avant qu'une erreur d'expiration ne se produise lors de l'exécution d'une requête sur une source de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Renvoie le nombre d'enregistrements affectés par le dernier appel de la méthode <strong><a href="connection-execute-method-dao.md">Execute</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>Renvoie une collection <strong>Recordsets</strong> qui contient tous les jeux d'enregistrements ouverts pour la connexion spécifiée. Valeur en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p>Indique si l'exécution d'une opération asynchrone (c.-à-d. une méthode appelée avec l'option <strong>dbRunAsync</strong>) est terminée (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
</tbody>
</table>

