---
title: ObjectTypeEnum (référence de base de données de bureau Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 030224af10fd77faf30f82ba703f4e069f223e98
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631406"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**S’applique à** : Access 2013, Office 2013

Indique le type d'objet de base de données dont il faut définir les autorisations ou le propriétaire.


<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adPermObjColumn</strong></p></td>
<td><p>2</p></td>
<td><p>L'objet est une colonne.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjDatabase</strong></p></td>
<td><p>3</p></td>
<td><p>L'objet est une base de données.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjProcedure</strong></p></td>
<td><p>4</p></td>
<td><p>L'objet est une procédure.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>L’objet est un type défini par le fournisseur. Une erreur se produit lorsque le paramètre <em>TypeObjet</em> a la valeur <strong>adPermObjProviderSpecific</strong> et que le paramètre<em>IdTypeObjet</em> n’est pas fourni.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPermObjTable</strong></p></td>
<td><p>1</p></td>
<td><p>L'objet est une table.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPermObjView</strong></p></td>
<td><p>5</p></td>
<td><p>L'objet est une vue.</p></td>
</tr>
</tbody>
</table>

