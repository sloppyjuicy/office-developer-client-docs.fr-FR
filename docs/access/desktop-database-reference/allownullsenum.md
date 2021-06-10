---
title: AllowNullsEnum (référence de base de données de bureau Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c184253551fa3f974de1840d47654af597881cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297164"
---
# <a name="allownullsenum"></a>AllowNullsEnum

**S’applique à** : Access 2013, Office 2013

Indique si des enregistrements contenant des valeurs Null sont indexés.

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
<td><p><strong>adIndexNullsAllow</strong></p></td>
<td><p>0</p></td>
<td><p>L'index autorise les entrées dans lesquelles les colonnes clés sont Null. L'entrée est insérée dans l'index lorsqu'une valeur Null est entrée dans une colonne clé.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsDisallow</strong></p></td>
<td><p>1</p></td>
<td><p>Valeur par défaut. L'index n'autorise pas d'entrées dans lesquelles les colonnes clés ont la valeur Null. Une erreur se produit lorsqu'une valeur Null est entrée dans une colonne clé.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndexNullsIgnore</strong></p></td>
<td><p>2</p></td>
<td><p>L'index n'insère pas d'entrée contenant des clés de valeur Null. Si une valeur Null est entrée dans une colonne clé, l'entrée est ignorée et aucune erreur ne se produit.</p></td>
</tr>
<tr class="even">
<td><p><strong>adIndexNullsIgnoreAny</strong></p></td>
<td><p>4 </p></td>
<td><p>L'index n'insère pas d'entrée où une colonne clé contient une valeur Null. Dans le cas d'un index possédant une clé multicolonne, si une valeur Null est entrée dans une colonne, l'entrée est ignorée et aucune erreur ne se produit.</p></td>
</tr>
</tbody>
</table>

