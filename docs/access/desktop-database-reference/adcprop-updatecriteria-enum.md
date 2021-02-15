---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8be93b0b7e4b32e3c040e871ff7d97a95f1e247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282851"
---
# <a name="adcprop_updatecriteria_enum"></a>ADCPROP \_ UPDATECRITERIA \_ ENUM

**S’applique à** : Access 2013, Office 2013

Indique les champs qui peuvent être utilisés pour détecter les conflits pendant une mise à jour optimiste d'une ligne de la source de données avec un objet [Recordset](recordset-object-ado.md).

Utilisez ces constantes avec la propriété dynamique "**Update Criteria**" du **Recordset**, qui est référencée dans l’[index des propriétés dynamiques ADO](ado-dynamic-property-index.md) et expliquée dans la documentation [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).

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
<td><p><strong>adCriteriaAllCols</strong></p></td>
<td><p>1 </p></td>
<td><p>Détecte des conflits en cas de modification d'une ligne de la source de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaKey</strong></p></td>
<td><p>0</p></td>
<td><p>Détecte des conflits en cas de modification de la colonne de clés de la ligne de source de données, indiquant que la ligne a été supprimée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCriteriaTimeStamp</strong></p></td>
<td><p>3 </p></td>
<td><p>Détecte des conflits si l'horodatage de la ligne de source de données a été modifié, signifiant qu'il y a eu un accès après obtention du <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCriteriaUpdCols</strong></p></td>
<td><p>2 </p></td>
<td><p>Détecte des conflits si une des colonnes de la ligne de source de données correspondant aux champs mis à jour du <strong>Recordset</strong> a été modifiée.</p></td>
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
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.AdcPropUpdateCriteria.ALLCOLS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.KEY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.AdcPropUpdateCriteria.UPDCOLS</p></td>
</tr>
</tbody>
</table>

