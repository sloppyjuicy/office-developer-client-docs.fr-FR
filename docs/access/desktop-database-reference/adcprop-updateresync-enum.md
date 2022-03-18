---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 86014ad92ee5cbc8a1df12e4ce2b3585502c2622
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558641"
---
# <a name="adcprop_updateresync_enum"></a>ADCPROPUPDATERESYNCENUM\_\_

**S’applique à** : Access 2013, Office 2013

Indique si la méthode [UpdateBatch](updatebatch-method-ado.md) est suivie d’une opération implicite de la méthode [Resync](resync-method-ado.md) et, dans ce cas, la portée de cette opération.


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
<td><p><strong>adResyncAll</strong></p></td>
<td><p>15 </p></td>
<td><p>Appelle <strong>Resync</strong> avec la valeur combinée de tous les autres membes ADCPROP_UPDATERESYNC_ENUM.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1</p></td>
<td><p>Par défaut. Recherche la nouvelle valeur d'identité des colonnes automatiquement incrémentées ou générées par la source des données, comme les champs Microsoft Jet AutoNumber ou les colonnes Microsoft SQL Server Identity.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2</p></td>
<td><p>Appelle <strong>Resync</strong> pour toutes les lignes dans lesquelles l'opération de mise à jour ou de suppression a échoué en raison d'un conflit de concurrence.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8 </p></td>
<td><p>Appelle <strong>Resync</strong> pour toutes les lignes insérées avec succès. Toutefois, les valeurs des colonnes AutoIncrement ne sont pas resynchronisées. En fait, le contenu des nouvelles lignes insérées est resynchronisé sur la base de la valeur de clé primaire existante. Si la clé primaire est une valeur AutoIncrement, <strong>Resync</strong> ne recherchera pas le contenu de la ligne concernée. Pour incrémenter automatiquement les valeurs de clé primaire AutoIncrement, appelez <strong>UpdateBatch</strong> avec la valeur combinée <strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p>N'appelle pas <strong>Resync</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4</p></td>
<td><p>Appelle <strong>Resync</strong> pour toutes les lignes mises à jour avec succès.</p></td>
</tr>
</tbody>
</table>

