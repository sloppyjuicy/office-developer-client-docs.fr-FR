---
title: MarshalOptions (référence de base de données du bureau Access)
TOCTitle: MarshalOptionsEnum
ms:assetid: 5361884b-a0fe-c480-1b9f-18e53be77f86
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249272(v=office.15)
ms:contentKeyID: 48544867
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c461594687cc8be53a526920a6fcd6ff15a864a8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891190"
---
# <a name="marshaloptionsenum"></a>MarshalOptionsEnum

**S’applique à**: Access 2013, Office 2013

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

