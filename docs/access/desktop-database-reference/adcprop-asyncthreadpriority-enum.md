---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281900"
---
# <a name="adcpropasyncthreadpriorityenum"></a>ADCPROP\_ASYNCTHREADPRIORITY\_de l'énumération

**S’applique à** : Access 2013, Office 2013

Pour un objet [Recordset](recordset-object-ado.md) RDS, spécifie la priorité d’exécution du thème asynchrone qui recherche des données.

Utilisez ces constantes avec la propriété dynamique « **Background Thread Priority** » du **Recordset**, qui est référencée dans l’index des propriétés dynamiques ADO et expliquée dans la documentation [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).

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
<td><p><strong>adPriorityAboveNormal</strong></p></td>
<td><p>4</p></td>
<td><p>Définit le niveau de priorité, normal ou maximum.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPriorityBelowNormal</strong></p></td>
<td><p>n°2</p></td>
<td><p>Définit le niveau de priorité, minimum ou normal.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityHighest</strong></p></td>
<td><p>disque</p></td>
<td><p>Définit le niveau de priorité le plus élevé possible.</p></td>
</tr>
<tr class="even">
<td><p><strong>AdPriorityLowest</strong></p></td>
<td><p>0,1</p></td>
<td><p>Définit le niveau de priorité le plus bas possible.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityNormal</strong></p></td>
<td><p>3</p></td>
<td><p>Définit le niveau de priorité normal.</p></td>
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
<td><p>AdoEnums. AdcPropAsyncThreadPriority. ABOVENORMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. BELOWNORMAL</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. HIGHEST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. minimum</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. NORMAL</p></td>
</tr>
</tbody>
</table>

