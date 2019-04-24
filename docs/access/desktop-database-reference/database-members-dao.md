---
title: Membres de base de données (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2254aeff94aeb2b8b078fc4f4cd4d3ef807e597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294924"
---
# <a name="database-members-dao"></a>Membres de base de données (DAO)


**S’applique à** : Access 2013, Office 2013

Un objet Database représente une base de données ouverte.

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
<td><p><strong><a href="database-close-method-dao.md">Close</a></strong></p></td>
<td><p>Ferme un objet <strong>Database</strong> ouvert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Crée un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></p></td>
<td><p>Crée un nouvel objet <strong><a href="relation-object-dao.md">relation</a></strong> (espaces de travail Microsoft Access uniquement). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></p></td>
<td><p>Crée un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong> (espaces de travail Microsoft Access uniquement). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Exécute une requête Action ou une instruction SQL sur l'objet spécifié.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></p></td>
<td><p>Crée un nouveau réplica à partir d'un autre réplica de base de données (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></p></td>
<td><p>Permet de modifier le mot de passe d'une base de données existante du moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></p></td>
<td><p>Synchronise les modifications d'un réplica partiel avec le réplica complet, efface tous les enregistrements du réplica partiel, puis remplit à nouveau ce dernier en fonction des filtres de réplica actifs. (Bases de données du moteur de base de données Microsoft Access uniquement.)</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-synchronize-method-dao.md">Synchronize</a></strong></p></td>
<td><p>Synchronise deux réplicas. (espaces de travail Microsoft Access uniquement).</p></td>
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
<td><p><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur <strong>Long</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui fournit des informations sur la source d'une base de données ouverte. Valeur de type <strong>String</strong> en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-connection-property-dao.md">Connection</a></strong></p></td>
<td><p><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p>
<p>Renvoie l'objet <strong><a href="connection-object-dao.md">Connection</a></strong> qui correspond à la base de données (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-containers-property-dao.md">Containers</a></strong></p></td>
<td><p>Renvoie une collection <strong>Containers</strong> qui représente tous les objets <strong>Container</strong> de la base de données spécifiée. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></p></td>
<td><p>Définit ou renvoie une valeur de 16 octets qui identifie de façon unique le réplica-maître d'un jeu de réplicas (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie le nom de l'objet spécifié. En lecture seule <strong>chaîne</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Renvoie une collection <strong>QueryDefs</strong> qui contient tous les objets <strong>QueryDef</strong> de la base de données spécifiée. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie la durée d'attente (en secondes) avant qu'une erreur d'expiration ne se produise lors de l'exécution d'une requête sur une source de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Renvoie le nombre d'enregistrements affectés par le dernier appel de la méthode <strong><a href="connection-execute-method-dao.md">Execute</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>Renvoie une collection <strong>Recordsets</strong> qui contient tous les jeux d'enregistrements ouverts pour la base de données spécifiée. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-relations-property-dao.md">Relations</a></strong></p></td>
<td><p>Renvoie une collection <strong>Relations</strong> qui contient tous les objets <strong>Relation</strong> enregistrés pour la base de données spécifiée. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-replicaid-property-dao.md">Attribué</a></strong></p></td>
<td><p>Renvoie une valeur de 16 octets qui identifie de façon unique un réplica de base de données (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></p></td>
<td><p>Renvoie une collection <strong>TableDefs</strong> qui contient tous les objets <strong>TableDef</strong> enregistrés dans la base de données spécifiée. Valeur en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-version-property-dao.md">Version</a></strong></p></td>
<td><p>Dans un espace de travail Microsoft Access, renvoie la version du moteur de base de données Microsoft Jet ou Microsoft Access qui a créé la base de données. Valeur <strong>String</strong> en lecture seule</p></td>
</tr>
</tbody>
</table>

