---
title: FilterGroupEnum (référence de base de données de bureau Access)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 115d56690859daf7cd3984ee38f0f187090f21be
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632804"
---
# <a name="filtergroupenum"></a>FilterGroupEnum

**S’applique à** : Access 2013, Office 2013

Spécifie le groupe d’enregistrements à filtrer depuis un objet [Recordset](recordset-object-ado.md).


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
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>2</p></td>
<td><p>Filtres pour ne visualiser que les enregistrements affectés par le dernier appel <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a> ou <a href="cancelbatch-method-ado.md">CancelBatch</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>5</p></td>
<td><p>Filtres pour visualiser les enregistrements qui ont échoué à la dernière mise à jour par lots.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>3</p></td>
<td><p>Filtres pour visualiser les enregistrements se trouvant en mémoire cache  —- en fait, les résultats de la dernière extraction d'enregistrements de la base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>0</p></td>
<td><p>Supprime le filtre en cours et restaure tous les enregistrements pour visualisation.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterPendingRecords</strong></p></td>
<td><p>1</p></td>
<td><p>Filtres permettant de ne visualiser que les enregistrements modifiés mais pas encore envoyés au serveur. Applicables seulement en mode de mise à jour par lots.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.AFFECTEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.CONFLICTINGRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.FETCHEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.PENDINGRECORDS</p></td>
</tr>
</tbody>
</table>

