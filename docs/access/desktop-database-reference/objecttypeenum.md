---
title: ObjectTypeEnum (référence de base de données du bureau Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c5fb9dbf86823ab4d84327d97eceb037eb77dec0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863714"
---
# <a name="objecttypeenum"></a>ObjectTypeEnum

**S’applique à**: Access 2013 | Office 2013

Indique le type d'objet de base de données dont il faut définir les autorisations ou le propriétaire.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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

