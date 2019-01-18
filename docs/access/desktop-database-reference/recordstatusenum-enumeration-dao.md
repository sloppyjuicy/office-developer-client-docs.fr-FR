---
title: RecordStatusEnum, énumération (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb7bffaf91db9e1170702d2e36393da669dbe0c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710502"
---
# <a name="recordstatusenum-enumeration-dao"></a>RecordStatusEnum, énumération (DAO)


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

