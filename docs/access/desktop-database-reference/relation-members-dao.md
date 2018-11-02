---
title: Membres de relation (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d4b1b1a3a06d0605793667f8c9258ea5b6336f5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923727"
---
# <a name="relation-members-dao"></a>Membres de relation (DAO)


**S’applique à**: Access 2013, Office 2013

Un objet Relation représente une relation entre des champs de tables ou de requêtes (bases de données de moteur de base de données Microsoft Access uniquement).

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
<td><p><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Crée un objet <strong><a href="field-object-dao.md">Field</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
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
<td><p><strong><a href="relation-attributes-property-dao.md">Attributs</a></strong></p></td>
<td><p>Définit ou renvoie une valeur spécifiant une ou plusieurs caractéristiques d'un objet <strong>Relation</strong>. Type <strong>Long</strong> en lecture-écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-fields-property-dao.md">Champs</a></strong></p></td>
<td><p>Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés pour l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></p></td>
<td><p>Définit ou renvoie le nom de la table étrangère d'une relation (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></p></td>
<td><p>Définit ou renvoie une valeur sur une <strong>Relation</strong> indiquant si cette relation doit être prise en compte lors du remplissage d'un réplica partiel à partir d'un réplica complet. (Bases de données de moteur de base de données Microsoft Access uniquement). Type de données <strong>Boolean</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-table-property-dao.md">Tableau</a></strong></p></td>
<td><p>Indique le nom d'une table primaire d'un objet <strong><a href="relation-object-dao.md">Relation</a></strong>. Ce nom doit correspondre à la valeur de la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> d'un objet <strong><a href="tabledef-object-dao.md">TableDef</a></strong> ou <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
</tbody>
</table>

