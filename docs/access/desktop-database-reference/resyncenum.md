---
title: ResyncEnum (référence de base de données du bureau Access)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 837bc16435ea574bd9d8e2e5e21ae50a4e852ee6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861077"
---
# <a name="resyncenum"></a>ResyncEnum

**S’applique à**: Access 2013 | Office 2013

Spécifie si les valeurs sous-jacentes sont remplacées par un appel à [Resync](resync-method-ado.md).

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adResyncAllValues</strong></p></td>
<td><p>2</p></td>
<td><p>Par défaut. Remplace les données, les mises à jour en attente sont annulées.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUnderlyingValues</strong></p></td>
<td><p>1</p></td>
<td><p>Ne remplace pas les données, les mises à jour en attente ne sont pas annulées.</p></td>
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
<td><p>AdoEnums.Resync.ALLVALUES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Resync.UNDERLYINGVALUES</p></td>
</tr>
</tbody>
</table>

