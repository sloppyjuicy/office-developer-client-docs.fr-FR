---
title: UpdateCriteriaEnum, éumération (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e27eb1bdfb9b393df76af8bdf54bc7f05fd82c2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306369"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>UpdateCriteriaEnum, éumération (DAO)


**S’applique à** : Access 2013, Office 2013

Cette énumération est utilisée avec la méthode **UpdateOptions** pour spécifier la construction d'une mise à jour par lot.

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
<td><p>dbCriteriaAllCols</p></td>
<td><p>4 </p></td>
<td><p>Utilise les colonnes clé et toutes les colonnes dans la clause WHERE.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaDeleteInsert</p></td>
<td><p>16 </p></td>
<td><p>Utilise une instruction DELETE et une instruction INSERT pour chaque ligne modifiée.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaKey</p></td>
<td><p>1 </p></td>
<td><p>Utilise les colonnes clé dans la clause WHERE.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaModValues</p></td>
<td><p>2 </p></td>
<td><p>Utilise les colonnes clé et toutes les colonnes mises à jour dans la clause WHERE.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaTimestamp</p></td>
<td><p>8 </p></td>
<td><p>Utilise la colonne horodateur si elle est disponible (génère une erreur d'exécution si aucune colonne horodateur ne se trouve dans le jeu de résultats).</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaUpdate</p></td>
<td><p>32</p></td>
<td><p>Utilise une instruction UPDATE pour chaque ligne modifiée.</p></td>
</tr>
</tbody>
</table>

