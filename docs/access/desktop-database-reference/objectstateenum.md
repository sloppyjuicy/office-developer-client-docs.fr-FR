---
title: ObjectStateEnum (référence de base de données de bureau Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 275d8b9e6542a1205656861833053cf818620154
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631399"
---
# <a name="objectstateenum"></a>ObjectStateEnum

**S’applique à** : Access 2013, Office 2013

Spécifie l'état d'un objet : ouvert ou fermé, en cours de connexion à une source de données, d'exécution d'une commande ou d'extraction de données.


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
<td><p><strong>adStateClosed</strong></p></td>
<td><p>0</p></td>
<td><p>Indique que l'objet est fermé.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateOpen</strong></p></td>
<td><p>1</p></td>
<td><p>Indique que l'objet est ouvert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateConnecting</strong></p></td>
<td><p>2</p></td>
<td><p>Indique que l'objet est en train de se connecter.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStateExecuting</strong></p></td>
<td><p>4</p></td>
<td><p>Indique que l'objet est en train d'exécuter une commande.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStateFetching</strong></p></td>
<td><p>8 </p></td>
<td><p>Indique que les lignes de l'objet sont en cours d'extraction.</p></td>
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
<td><p>AdoEnums.ObjectState.CLOSED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ObjectState.OPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ObjectState.CONNECTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ObjectState.EXECUTING</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ObjectState.FETCHING</p></td>
</tr>
</tbody>
</table>

