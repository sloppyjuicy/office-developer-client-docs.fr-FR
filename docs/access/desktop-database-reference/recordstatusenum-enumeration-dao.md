---
title: RecordStatusEnum Enumeration (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c2d96c359a913660c146f4850a1846554e3b6856
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875118"
---
# <a name="recordstatusenum-enumeration-dao"></a>RecordStatusEnum Enumeration (DAO)


**S’applique à**: Access 2013, Office 2013

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
<td><p>4</p></td>
<td><p>L'enregistrement a été supprimé localement dans la base de données.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordDeleted</p></td>
<td><p>3</p></td>
<td><p>L'enregistrement a été supprimé, mais il n'a pas encore été supprimé de la base de données.</p></td>
</tr>
<tr class="odd">
<td><p>valeur dbRecordModified</p></td>
<td><p>1</p></td>
<td><p>L'enregistrement a été modifié, mais il n'a pas été mis à jour dans la base de données.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordNew</p></td>
<td><p>2</p></td>
<td><p>L'enregistrement a été ajouté à l'aide de la méthode <strong>AddNew</strong>, mais il n'a pas été encore ajouté à la base de données.</p></td>
</tr>
<tr class="odd">
<td><p>valeur dbRecordUnmodified</p></td>
<td><p>0</p></td>
<td><p>(Valeur par défaut) L'enregistrement n'a pas été modifié ou il a été mis à jour.</p></td>
</tr>
</tbody>
</table>

