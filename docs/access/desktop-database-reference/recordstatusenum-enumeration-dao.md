---
title: RecordStatusEnum, éumération (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb7bffaf91db9e1170702d2e36393da669dbe0c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309233"
---
# <a name="recordstatusenum-enumeration-dao"></a>RecordStatusEnum, éumération (DAO)


**S’applique à** : Access 2013, Office 2013

Cette énumération est utilisée avec la propriété **RecordStatus** pour indiquer l'état de mise à jour de l'enregistrement actif s'il fait partie d'une mise à jour par lot.

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
<td><p>dbRecordDBDeleted</p></td>
<td><p>4 </p></td>
<td><p>L'enregistrement a été supprimé localement dans la base de données.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordDeleted</p></td>
<td><p>3 </p></td>
<td><p>L'enregistrement a été supprimé, mais il n'a pas encore été supprimé de la base de données.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordModified</p></td>
<td><p>1 </p></td>
<td><p>L'enregistrement a été modifié, mais il n'a pas été mis à jour dans la base de données.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordNew</p></td>
<td><p>2 </p></td>
<td><p>L'enregistrement a été ajouté à l'aide de la méthode <strong>AddNew</strong>, mais il n'a pas été encore ajouté à la base de données.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordUnmodified</p></td>
<td><p>0</p></td>
<td><p>(Valeur par défaut) L'enregistrement n'a pas été modifié ou il a été mis à jour.</p></td>
</tr>
</tbody>
</table>

