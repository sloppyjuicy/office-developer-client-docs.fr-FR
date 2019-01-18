---
title: Membres de l’index (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709158"
---
# <a name="index-members-dao"></a>Membres de l’index (DAO)


**S’applique à**: Access 2013, Office 2013

Les objets Index déterminent l'ordre des enregistrements accessibles depuis les tables de base de données et indiquent si les enregistrements en double sont acceptés ou pas, ce qui optimise l'accès aux données. Dans le cas d'une base de données externe, les objets Index décrivent les index définis pour les tables externes (espaces de travail Microsoft Access uniquement).

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
<td><p><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Crée un objet <strong><a href="field-object-dao.md">Field</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
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
<td><p><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si un objet <strong>Index</strong> représente un index cluster pour une table (espaces de travail Microsoft Access uniquement). Valeur de type <strong>Boolean</strong> en lecture-écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></p></td>
<td><p>Renvoie une valeur indiquant le nombre de valeurs uniques pour l'objet <strong><a href="index-object-dao.md">Index</a></strong> inclus dans la table associée (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Champs</a></strong></p></td>
<td><p>Renvoie une collection <strong>Fields</strong> qui représente tous les objets <strong>Field</strong> stockés de l'objet spécifié. Lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si un objet <strong><a href="index-object-dao.md">Index</a></strong> représente une clé étrangère d'une table (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si les enregistrements ayant des valeurs nulles dans leurs champs d'index ont des entrées d'index (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Nom</a></strong></p></td>
<td><p>Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Primary</a></strong></p></td>
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

