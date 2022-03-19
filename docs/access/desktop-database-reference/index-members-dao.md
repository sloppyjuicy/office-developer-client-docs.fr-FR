---
title: Index members (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9cbeb55ea4cfdbe798a03ae3ebc077fb6ecb223d
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627507"
---
# <a name="index-members-dao"></a>Index members (DAO)


**S’applique à** : Access 2013, Office 2013

Les objets Index déterminent l'ordre des enregistrements accessibles depuis les tables de base de données et indiquent si les enregistrements en double sont acceptés ou pas, ce qui optimise l'accès aux données. Dans le cas d'une base de données externe, les objets Index décrivent les index définis pour les tables externes (espaces de travail Microsoft Access uniquement).

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
<td><p><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Crée un objet <strong><a href="field-object-dao.md">Field</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
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
<td><p><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si un objet <strong>Index</strong> représente un index cluster pour une table (espaces de travail Microsoft Access uniquement). Valeur de type <strong>Boolean</strong> en lecture-écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></p></td>
<td><p>Renvoie une valeur indiquant le nombre de valeurs uniques pour l'objet <strong><a href="index-object-dao.md">Index</a></strong> inclus dans la table associée (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés de l'objet spécifié. Lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Étranger</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si un objet <strong><a href="index-object-dao.md">Index</a></strong> représente une clé étrangère d'une table (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si les enregistrements ayant des valeurs nulles dans leurs champs d’index ont des entrées d’index (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Primaire</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si un objet <strong><a href="index-object-dao.md">Index</a></strong> représente un index de clé primaire pour une table (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Obligatoire</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si un objet <strong><a href="field-object-dao.md">Field</a></strong> requiert une valeur non Null.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Unique</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si un objet <strong><a href="index-object-dao.md">Index</a></strong> représente un index (une clé) unique d'une table (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
</tbody>
</table>

