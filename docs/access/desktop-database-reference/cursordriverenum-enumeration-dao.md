---
title: CursorDriverEnum Enumeration (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d264c1e91982231e025f17c00db79e47a1d5c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880739"
---
# <a name="cursordriverenum-enumeration-dao"></a>CursorDriverEnum Enumeration (DAO)


**S’applique à**: Access 2013, Office 2013

Spécifie le type de pilote de curseur.

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
<td><p>dbUseClientBatchCursor</p></td>
<td><p>3</p></td>
<td><p>Utilise toujours la bibliothèque de curseurs FoxPro. Cette option est obligatoire pour effectuer des mises à jour par lot.</p></td>
</tr>
<tr class="even">
<td><p>dbUseDefaultCursor</p></td>
<td><p>-1</p></td>
<td><p>(Valeur par défaut) Utilise des curseurs du côté serveur si le serveur les prend en charge. Si ce n'est pas le cas, utilise la bibliothèque de curseurs ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>en d’autres termes</p></td>
<td><p>4</p></td>
<td><p>Ouvre tous les curseurs (c'est-à-dire, les objets <strong>Recordset</strong> ) en tant que type avant uniquement, en lecture seule, avec une taille de jeu de lignes de 1. Également appelé &quot;requêtes sans curseur.&quot;</p></td>
</tr>
<tr class="even">
<td><p>dbUseODBCCursor</p></td>
<td><p>1</p></td>
<td><p>Utilise toujours la bibliothèque de curseurs ODBC. Cette option permet d'améliorer les performances pour les jeux de résultats de petite taille. Les performances diminuent toutefois rapidement pour les jeux de résultats volumineux.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseServerCursor</p></td>
<td><p>2</p></td>
<td><p>Utilise toujours des curseurs du côté serveur. Cette option améliore les performances pour la plupart des opérations importantes. Elle risque toutefois d'augmenter le trafic réseau.</p></td>
</tr>
</tbody>
</table>

