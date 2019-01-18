---
title: RelationAttributeEnum, énumération (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbb8ca2e1a63154f17bd814a26fe79ed405765cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711118"
---
# <a name="relationattributeenum-enumeration-dao"></a>RelationAttributeEnum, énumération (DAO)


**S’applique à**: Access 2013, Office 2013

Cette énumération est utilisée avec la propriété **Attributes** (Attributs) pour déterminer les attributs d'un objet **Relation**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbRelationDeleteCascade</p></td>
<td><p>4096</p></td>
<td><p>Suppressions en cascade</p></td>
</tr>
<tr class="even">
<td><p>valeur dbRelationDontEnforce</p></td>
<td><p>2</p></td>
<td><p>Relation non appliquée (aucune intégrité référentielle)</p></td>
</tr>
<tr class="odd">
<td><p>dbRelationInherited</p></td>
<td><p>4</p></td>
<td><p>Une relation existe dans la base de données qui contient les deux tables attachées</p></td>
</tr>
<tr class="even">
<td><p>dbRelationLeft</p></td>
<td><p>16777216</p></td>
<td><p>Microsoft Access uniquement. En mode Création, affiche une JOINTURE GAUCHE en tant que type de jointure par défaut.</p></td>
</tr>
<tr class="odd">
<td><p>dbRelationRight</p></td>
<td><p>33554432</p></td>
<td><p>Microsoft Access uniquement. En mode Création, affiche une JOINTURE DROITE en tant que type de jointure par défaut.</p></td>
</tr>
<tr class="even">
<td><p>dbRelationUnique</p></td>
<td><p>1</p></td>
<td><p>Relation un-à-un</p></td>
</tr>
<tr class="odd">
<td><p>dbRelationUpdateCascade</p></td>
<td><p>256</p></td>
<td><p>Mises à jour en cascade</p></td>
</tr>
</tbody>
</table>

