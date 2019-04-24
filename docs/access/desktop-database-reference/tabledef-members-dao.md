---
title: TableDef, membres (DAO)
TOCTitle: TableDef Members
ms:assetid: bc55315e-bafe-d89e-ad31-fd4c9bb6486e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822714(v=office.15)
ms:contentKeyID: 48547408
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff9f6841b50b70f8846c829f0ee7b911c84c0e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314902"
---
# <a name="tabledef-members-dao"></a>TableDef, membres (DAO)


**S’applique à** : Access 2013, Office 2013

Un objet TableDef représente la définition stockée d'une table de base ou d'une table liée (espaces de travail Microsoft Access uniquement).

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
<td><p><strong><a href="tabledef-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Crée un objet <strong><a href="field-object-dao.md">Field</a></strong> (espaces de travail Microsoft Access uniquement). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-createindex-method-dao.md">CreateIndex</a></strong></p></td>
<td><p>Crée un nouvel objet <strong><a href="index-object-dao.md">index</a></strong> (espaces de travail Microsoft Access uniquement). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-refreshlink-method-dao.md">RefreshLink</a></strong></p></td>
<td><p>Met à jour les informations de connexion d’une table liée (espaces de travail Microsoft Access uniquement).</p></td>
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
<td><p><strong><a href="tabledef-attributes-property-dao.md">Attributs</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet <strong>TableDef</strong>. Type de données <strong>Long</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-conflicttable-property-dao.md">ConflictTable,</a></strong></p></td>
<td><p>Renvoie le nom d'une table de conflits contenant les enregistrements de base de données qui sont entrés en conflit lors de la synchronisation de deux réplicas (espaces de travail Microsoft Access uniquement). Valeur de type <strong>String</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui donne des informations sur une table liée. Type de données <strong>String</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement). Valeur <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés pour l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-indexes-property-dao.md">Indexes</a></strong></p></td>
<td><p>Renvoie une collection <strong>Indexes</strong> qui contient tous les objets <strong>Index</strong> stockés pour la table spécifiée. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-name-property-dao.md">Name</a></strong></p></td>
<td><p>Cette propriété renvoie ou définit le nom de l'objet spécifié. En lecture/écriture, <strong>chaîne</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. Valeur en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Renvoie le nombre total d'enregistrements dans un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. Type de données <strong>Long</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-replicafilter-property-dao.md">ReplicaFilter</a></strong></p></td>
<td><p>Définit ou renvoie une valeur sur un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong> au sein d'un réplica partiel qui indique le sous-ensemble d'enregistrements répliqué vers cette table à partir d'un réplica complet. (Espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong></p></td>
<td><p>Définit ou renvoie un valeur spécifiant le nom d'une table liée ou celui d'une table de base (espaces de travail Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui valide les données dans un champ au moment de leur modification ou de leur ajout à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet <strong>Field</strong> n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</p></td>
</tr>
</tbody>
</table>

