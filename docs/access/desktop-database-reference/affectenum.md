---
title: AffectEnum (référence de base de données de bureau Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b28aa3900ccff701440ac43c04db7229a9d71082
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62459789"
---
# <a name="affectenum"></a>AffectEnum

**S’applique à** : Access 2013, Office 2013

Indique les enregistrements affectés par une opération.


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
<td><p><strong>adAffectAll</strong></p></td>
<td><p>3</p></td>
<td><p>Si aucun <a href="filter-property-ado.md">filtre</a> n’est appliqué au <strong>Recordset</strong>, affecte tous les enregistrements. Si la <strong>propriété Filter</strong> est définie sur un critère de chaîne ( &quot;tel que Author='Smith'), l’opération&quot; affecte les enregistrements visibles dans le chapitre actuel. Si la <strong>propriété Filter</strong> est définie sur un membre du <a href="filtergroupenum.md">FilterGroupEnum</a> ou un tableau de signets, l’opération affectera toutes les lignes du <strong>jeu d’enregistrements</strong>.</p><p><strong>REMARQUE</strong> : adAffectAll est masqué dans l’explorateur Visual Basic’objet.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4</p></td>
<td><p>Affecte tous les enregistrements de tous les chapitres de même niveau du <strong>Recordset</strong>, notamment ceux non visibles par le <strong>filtre</strong> appliqué.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>N'affecte que l'enregistrement en cours.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>N’affecte que les enregistrements qui répondent aux paramètres de la propriété <a href="filter-property-ado.md">Filter</a> en cours. Pour utiliser cette option, vous devez configurer la propriété <strong>Filter</strong> avec la valeur <strong>FilterGroupEnum</strong> ou un tableau <strong>Bookmarks</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>

