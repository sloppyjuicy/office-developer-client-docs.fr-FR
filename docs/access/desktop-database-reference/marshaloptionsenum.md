---
title: MarshalOptions (référence de base de données du bureau Access)
TOCTitle: MarshalOptionsEnum
ms:assetid: 5361884b-a0fe-c480-1b9f-18e53be77f86
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249272(v=office.15)
ms:contentKeyID: 48544867
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 2ca63d6797f31768dfec9d0d28d9c1f9c577f55a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860363"
---
# <a name="marshaloptionsenum"></a>MarshalOptionsEnum

**S’applique à**: Access 2013 | Office 2013

Spécifie les enregistrements qui doivent être renvoyés au serveur.

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
<td><p><strong>adMarshalAll</strong></p></td>
<td><p>0</p></td>
<td><p>Par défaut. Renvoie toutes les lignes au serveur.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMarshalModifiedOnly</strong></p></td>
<td><p>1</p></td>
<td><p>Ne renvoie que les lignes modifiées au serveur.</p></td>
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
<td><p>AdoEnums.MarshalOptions.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.MarshalOptions.MODIFIEDONLY</p></td>
</tr>
</tbody>
</table>

