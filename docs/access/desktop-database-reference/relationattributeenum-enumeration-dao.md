---
title: RelationAttributeEnum, éumération (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7eb11e7da4a529bd50d81f6dbb697b22fcc8a047
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576939"
---
# <a name="relationattributeenum-enumeration-dao"></a>RelationAttributeEnum, éumération (DAO)


**S’applique à** : Access 2013, Office 2013

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
<td><p>dbRelationDontEnforce</p></td>
<td><p>2</p></td>
<td><p>Relation non appliquée (aucune intégrité référentielle)</p></td>
</tr>
<tr class="odd">
<td><p>dbRelationInherited</p></td>
<td><p>4 </p></td>
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

